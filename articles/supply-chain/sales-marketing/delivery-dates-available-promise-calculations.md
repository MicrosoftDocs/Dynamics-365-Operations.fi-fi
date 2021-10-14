---
title: Luvatut tilaukset
description: Tässä ohjeaiheessa on tietoja tilaustenkäsittelyn lupauksista. Tilauksen lupausten avulla voit luvata toimituspäivämäärät asiakkaillesi luotettavasti ja antaa sinulle joustavuuden, jonka avulla voit toteuttaa lupauksesi.
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f7535ba28358fef21784956da38cd334a4aebe7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572598"
---
# <a name="order-promising"></a>Luvatut tilaukset

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja tilaustenkäsittelyn lupauksista. Tilauksen lupausten avulla voit luvata toimituspäivämäärät asiakkaillesi luotettavasti ja antaa sinulle joustavuuden, jonka avulla voit toteuttaa lupauksesi.

Luvatuissa tilauksissa lasketaan, mikä on aikaisin lähetys- ja vastaanottopäivä toimituspäivän valvontapäivän ja kuljetuspäivien perusteella. Valittavana on neljä toimituspäivän valvontamenetelmää:

-   **Myynnin läpimenoaika** – Myynnin läpimenoaika on myyntitilauksen luomisen ja nimikkeiden toimituksen välinen aika. Toimituspäivän laskenta perustuu päivien oletusmäärään eikä siinä oteta huomioon varastotilannetta, tiedettyä kysyntää eikä suunniteltua tarjontaa.
-   **Luvattavissa oleva määrä (ATP)** – ATP on nimikkeen käytettävissä oleva määrä, joka voidaan luvata asiakkaalle tiettynä päivänä. ATP-laskelmaan sisältyy varaamaton varasto, läpimenoajat, suunnitellut vastaanotot ja varasto-otot.
-   **ATP + toimitusmarginaali** – Lähetyspäivämäärä vastaa ATP-päivämäärää sekä nimikkeen toimitusmarginaalia. Toimitusmarginaali on lähetettävien nimikkeiden valmisteluun kuluva aika.
-   **Saatavuus (CTP)**– Saatavuus lasketaan hajotuksen avulla.

> [!NOTE]
> Kun myyntitilausta päivitetään, toimituksen lupaamistiedot päivitetään vain, jos aiempaa toimituksen lupaamispäivämäärää ei voida toteuttaa, kuten seuraavissa esimerkeissä:
> 
> - **Esimerkki 1**: Toimituksen nykyinen lupaamispäivä on 20. heinäkuuta, mutta kasvaneen määrän vuoksi toimitus on mahdollista vasta 25. heinäkuuta. Koska nykyistä päivämäärää ei enää pystytä toteuttamaan, toimituksen lupaaminen käynnistyy.
> -  **Esimerkki 2**: Nykyisen toimituksen lupaamisen päivämäärä on 20. heinäkuuta 20, mutta vähentyneen määrän vuoksi, toimitus on nyt mahdollista tehdä 15. heinäkuuta. Koska nykyinen päivämäärä on edelleen toteutettavissa, toimituksen lupaamista ei käynnistetä ja 20. heinäkuuta jää toimituksen lupaamispäiväksi.

## <a name="atp-calculations"></a>ATP-laskelmat
ATP-määrä lasketaan "ennakoivan kumulatiivisen ATP-määrän" avulla. Tämän ATP-laskentamenetelmän pääasiallinen etu on mahdollisuus käsitellä myös tilanteet, joissa vastaanottojen välisten varasto-ottojen summa on suurempi kuin uusin vastaanotto (esim. kun tarpeen täyttäminen edellyttää aiemman vastaanoton määrän käyttämistä). Ennakoiva kumulatiivinen ATP -laskentatapa sisällyttää kaikki varasto-otot, kunnes vastaanotettavien kumulatiivinen määrä ylittää otettavien kumulatiivisen määrän. Niinpä tämä ATP-laskentatapa arvioi, voidaanko osaa aiemman kauden määrästä käyttää myöhemmällä kaudella.  

ATP-määrä on ensimmäisen kauden varaamaton varastosaldo. Tavallisesti se lasketaan jokaiselle kaudelle, jolle on ajoitettu vastaanotto. Ohjelma laskee ATP-kauden päivinä ja käyttää kuluvaa päivää ATP-määrän ensimmäisen päivämääränä. Ensimmäisellä kaudella ATP ottaa mukaan käytettävissä olevan varaston, josta vähennetään erääntyvät ja erääntyneet asiakastilaukset.  

ATP-määrä lasketaan seuraavaa kaavaa käyttäen:  

ATP = edeltävän kauden ATP + nykyisen kauden vastaanotot – nykyisen kauden varasto-otot – jokaisen tulevan kauden varasto-ottojen nettosumma siihen kauteen saakka, jonka kohdalla kaikkien tulevien kausien vastaanottojen summa kyseinen tuleva kausi mukaan lukien on suurempi kuin varasto-ottojen summa kyseinen tuleva kausi mukaan lukien.  

Huomaa, että ATP-laskennassa ei ole tietoja erääntymispäivästä eikä ATP-aikarajan jälkeisistä tiedoista, joita järjestelmä odottaa, kun mitään määrää voidaan luvata.

Kun huomioitavia varasto-ottoja tai vastaanottoja ei enää ole, seuraavien päivämäärien ATP-määrä on sama kuin viimeinen laskettu ATP-määrä.  

Jos kaikkia nimikkeessä käytettäviä dimensioita ei anneta, kun ATP-tarkistus on valmis, ne voidaan silti määrittää varasto-ottoon ja vastaanottoihin. Tässä tilanteessa ATP-laskenta edellyttää, että vastaanotot ja varasto-otot on koottava valmiisiin dimensioihin, jotta ATP-laskennassa käytettävien vastaanotto- ja varasto-ottorivien määrää voidaan vähentää.  

Näytettävä ATP-määrä on aina suurempi tai yhtä suuri kuin 0 (nolla). Jos laskutoimituksen tulos on negatiivinen ATP-määrä (jos aiemmin luvattu määrä on esimerkiksi suurempi kuin käytettävissä oleva määrä), määräksi määritetään automaattisesti 0.

### <a name="example"></a>Esimerkki

**ATP:n kysynnän aikaraja (taaksepäin)** -kenttä määrittää, kuinka kaukaa viivästyneen kysynnän tilauksia tai varasto-ottoja etsitään. **ATP:n toimituksen aikaraja (taaksepäin)** -kenttä määrittää, kuinka kaukaa viivästyneen toimituksen tilauksia tai varastovastaanottoja etsitään. Jos esimerkiksi vain seitsemän päivää viivästyneet tilaukset otetaan huomioon ATP-laskennassa, kummankin kentän arvoksi on valittava **7**.  

**ATP:n viivästyneen kysynnän vastakirjauksen aika**- ja **ATP:n viivästyneen toimituksen vastakirjauksen aika** -kentät määrittävät, milloin viivästynyt kysyntä tai toimitus otetaan huomioon ATP-laskennassa. Jos esimerkiksi viivästynyt kysyntä ja tilaukset otetaan huomioon ATP-laskennassa ylihuomenna, kummankin kentän arvoksi on valittava **2**. Arvo **2** tarkoittaa, että viivästyneen ostotilauksen nimikkeen määrä, joka pitäisi ottaa huomioon ATP-laskennassa, nähdään käytettävissä olevana kaksi päivää kuluvan päivän jälkeen.  

Seuraavassa esimerkissä **7** annetaan **ATP:n kysynnän aikaraja (taaksepäin)**- ja **ATP:n toimituksen aikaraja (taaksepäin)** -kenttien arvoksi ja **1** annetaan **ATP:n viivästyneen kysynnän vastakirjauksen aika**- ja **ATP:n viivästyneen toimituksen vastakirjauksen aika** -kenttien arvoksi.  

200 kappaleen tuotteen ostotilausta ei ole vielä vastaanotettu, vaikka se olisi pitänyt vastaanottaa kolme päivää sitten. Niinpä saman tuotteen 75 kappaleen myyntitilausriviä ei ole lähetetty, vaikka se piti lähettää eilen.  

Asiakas soittaa ja haluaa tilata 150 kappaletta samaa tuotetta. Kun tarkistat tuotteen saatavuuden, havaitset, että tuotteella on toinen 100 kappaleen ostotilaus, jonka toimitus on 10 päivää myöhemmin.  

Luot myyntitilausrivin tuotteelle ja ilmoitat määräksi **150**.  

Koska toimituspäivän valvontamenetelmä on ATP, aikaisin mahdollinen lähetyspäivä etsitään laskemalla ATP-tiedot. Asetusten mukaisesti viivästyneet osto- ja myyntitilaukset otetaan huomioon, jolloin kuluvan päivän ATP-määräksi saadaan 0 Seuraavana päivänä, jolloin oletetaan, että viivästynyt ostotilaus vastaanotetaan, ATP-määrä lasketaan suuremmaksi kuin 0 (tässä tapauksessa arvoksi lasketaan 125) Kuitenkin tästä päivästä 10 päivän kuluttua, jolloin odotetaan 100 kappaleen lisäostotilauksen vastaanottoa, ATP-määrä on yli 150.  

Tämän vuoksi ATP-laskennan perusteella lähetyspäivä määritetään 10 päivän päähän tästä päivästä. Voitkin siis ilmoittaa asiakkaalle, että pyydetty määrä voidaan toimittaa 10 päivän kuluttua tästä päivästä.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]