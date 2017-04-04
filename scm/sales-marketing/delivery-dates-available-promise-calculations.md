---
title: Luvatut tilaukset
description: "Tässä artikkelissa on tietoja tilaustenkäsittelyn lupauksista. Tilauksen lupausten avulla voit luvata toimituspäivämäärät asiakkaillesi luotettavasti ja antaa sinulle joustavuuden, jonka avulla voit toteuttaa lupauksesi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Luvatut tilaukset

Tässä artikkelissa on tietoja tilaustenkäsittelyn lupauksista. Tilauksen lupausten avulla voit luvata toimituspäivämäärät asiakkaillesi luotettavasti ja antaa sinulle joustavuuden, jonka avulla voit toteuttaa lupauksesi.

Luvatuissa tilauksissa lasketaan, mikä on aikaisin lähetys- ja vastaanottopäivä toimituspäivän valvontapäivän ja kuljetuspäivien perusteella. Valittavana on neljä toimituspäivän valvontamenetelmää:

-   **Myynnin läpimenoaika** – Myynnin läpimenoaika on myyntitilauksen luomisen ja nimikkeiden toimituksen välisenä aikana. Toimituspäivämäärän laskenta perustuu oletuskesto päivinä ja ei myöskään varastotilanteen ja kysynnän tunnettu tai suunniteltu tarjonta.
-   **ATP (käytettävissä luvattavaksi)** – ATP on kohde, joka on käytettävissä ja voi luvata asiakkaalle tiettynä päivänä. ATP-laskelmaan sisältyy varaamaton varasto, läpimenoajat, suunnitellut vastaanotot ja varasto-otot.
-   **ATP + toimitusmarginaali ** – Lähetyspäivämäärä vastaa ATP-päivämäärää sekä nimikkeen toimitusmarginaalia. Toimitusmarginaali on lähetettävien nimikkeiden valmisteluun kuluva aika.
-   **Saatavuus (CTP) **– Saatavuus lasketaan hajotuksen avulla.

## <a name="atp-calculations"></a>ATP-laskelmat
ATP-määrä lasketaan "kumulatiiviseen ATP sijoitetulla"-menetelmällä. Tätä ATP-laskentamenetelmän tärkein etu on, että se voi käsitellä tapauksia, joissa kesken vastaanottojen varasto-ottojen summa on suurempi kuin uusin vastaanotto (esimerkiksi silloin, kun käytettävä täyttäminen edellyttää aiemman vastaanoton määrän). "Kanssa sijoitetulla kumulatiiviseen ATP-laskentamenetelmän sisältää kaikki ongelmat, kunnes kumulatiivinen määrä saa ylittää kumulatiivinen määrä. Niinpä tämä ATP-laskentatapa arvioi, voidaanko osaa aiemman kauden määrästä käyttää myöhemmällä kaudella.  

ATP-määrä on ensimmäisen kauden varaamaton varastosaldo. Tavallisesti se lasketaan jokaiselle kaudelle, jolle on ajoitettu vastaanotto. Ohjelma laskee ATP-kauden päivinä ja käyttää kuluvaa päivää ATP-määrän ensimmäisen päivämääränä. Ensimmäisellä kaudella ATP ottaa mukaan käytettävissä olevan varaston, josta vähennetään erääntyvät ja erääntyneet asiakastilaukset.  

ATP-määrä lasketaan seuraavaa kaavaa käyttäen:  

ATP = ATP + edellisen kauden vastaanotot – nykyisen kauden ongelmat – nykyisen kauden Net ongelma määrän jokaisen tulevan kauden vasta kun kyseinen tuleva kausi mukaan lukien kaikkien tulevien kausien vastaanottojen summa on suurempi kuin varasto-ottojen summa enintään tilikaudella ja kyseinen tuleva kausi mukaan lukien.  

Kun huomioitavia varasto-ottoja tai vastaanottoja ei enää ole, seuraavien päivämäärien ATP-määrä on sama kuin viimeinen laskettu ATP-määrä.  

Jos kaikkia nimikkeessä käytettäviä dimensioita ei anneta, kun ATP-tarkistus on valmis, ne voidaan silti määrittää varasto-ottoon ja vastaanottoihin. Tässä tilanteessa ATP-laskenta edellyttää, että vastaanotot ja varasto-otot on koottava valmiisiin dimensioihin, jotta ATP-laskennassa käytettävien vastaanotto- ja varasto-ottorivien määrää voidaan vähentää.  

Näytettävä ATP-määrä on aina suurempi tai yhtä suuri kuin 0 (nolla). Jos laskutoimituksen tulos on negatiivinen ATP-määrä (jos aiemmin luvattu määrä on esimerkiksi suurempi kuin käytettävissä oleva määrä), ohjelma määrittää määräksi automaattisesti **0**.

### <a name="example"></a>Esimerkki

**ATP:n kysynnän aikaraja (taaksepäin)** -kenttä määrittää, kuinka kaukaa viivästyneen kysynnän tilauksia tai varasto-ottoja etsitään. **ATP:n toimituksen aikaraja (taaksepäin)** -kenttä määrittää, kuinka kaukaa viivästyneen toimituksen tilauksia tai varastovastaanottoja etsitään. Jos esimerkiksi vain seitsemän päivää viivästyneet tilaukset otetaan huomioon ATP-laskennassa, kummankin kentän arvoksi on valittava **7**.  

**ATP:n viivästyneen kysynnän vastakirjauksen aika**- ja **ATP:n viivästyneen toimituksen vastakirjauksen aika** -kentät määrittävät, milloin viivästynyt kysyntä tai toimitus otetaan huomioon ATP-laskennassa. Jos esimerkiksi viivästynyt kysyntä ja tilaukset otetaan huomioon ATP-laskennassa ylihuomenna, kummankin kentän arvoksi on valittava **2**. Arvo **2** tarkoittaa, että viivästyneen ostotilauksen nimikkeen määrä, joka pitäisi ottaa huomioon ATP-laskennassa, nähdään käytettävissä olevana kaksi päivää kuluvan päivän jälkeen.  

Seuraavassa esimerkissä **7** annetaan **ATP:n kysynnän aikaraja (taaksepäin)**- ja **ATP:n toimituksen aikaraja (taaksepäin)** -kenttien arvoksi ja **1** annetaan **ATP:n viivästyneen kysynnän vastakirjauksen aika**- ja **ATP:n viivästyneen toimituksen vastakirjauksen aika** -kenttien arvoksi.  

200 kappaleen tuotteen ostotilausta ei ole vielä vastaanotettu, vaikka se olisi pitänyt vastaanottaa kolme päivää sitten. Niinpä saman tuotteen 75 kappaleen myyntitilausriviä ei ole lähetetty, vaikka se piti lähettää eilen.  

Asiakas soittaa ja haluaa tilata 150 kappaletta samaa tuotetta. Kun tarkistat tuotteen saatavuuden, havaitset, että tuotteella on toinen 100 kappaleen ostotilaus, jonka toimitus on 10 päivää myöhemmin.  

Luot myyntitilausrivin tuotteelle ja ilmoitat määräksi **150**.  

Koska toimituspäivän valvontamenetelmä on ATP, aikaisin mahdollinen lähetyspäivä etsitään laskemalla ATP-tiedot. Asetusten perusteella katsotaan viivästyneen ostotilauksen ja myyntitilauksen ja nykyisen päivämäärän tuloksena ATP-määrä on 0. Huomenna, viivästyneet ostotilaus on odotettavissa, kun ATP-määrä lasketaan yli 0 (Tässä tapauksessa se lasketaan 125). Kuitenkin 10 päivää nyt, kun muita ostotilauksen 100 kappaletta on odotettavissa, ATP-määrä on yli 150.  

Siksi lähetyspäivämäärä on 10 päivää nyt on ATP-laskennan perusteella. Voitkin siis ilmoittaa asiakkaalle, että pyydetty määrä voidaan toimittaa 10 päivän kuluttua tästä päivästä.


