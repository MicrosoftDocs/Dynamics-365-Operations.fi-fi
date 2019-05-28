---
title: Töiden ajoittamisen Gantt-kaavio
description: Tuotannon suunnittelijat voivat käyttää Gantt-kaavioita tuotantosuunnitelmien hallintaan ja optimointiin.
author: johanhoffmann
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301db69fce18c2ed32e201e7418e628ac57db543
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571833"
---
# <a name="gantt-chart-for-job-scheduling"></a>Töiden ajoittamisen Gantt-kaavio

[!include [banner](../includes/banner.md)]

Gantt-kaavio on suunniteltu mahdollistamaan tuotannon suunnittelijoille tuotantosuunnitelman valvontaa ja optimointia varten. Gantt-kaavio tekee työnkulusta avoimia ja helpottaa tuotantoaikataulun säätämistä ottaen huomioon materiaali- tai resurssipuutteet. Näin suunnittelijat voivat parhaiten hyödyntää käytettäviä resursseja, pienentää keskeneräisten töiden määrää ja optimoida tuotantotilausten läpimenoaikoja.

Gantt-kaavio on määritetylle ajanjaksolle ajoitettujen tehtävien visuaalinen esitystapa. Tehtävät ajoitetaan resurssien perustella, joiden kapasiteettikalenterin mukainen kapasiteetti. Seuraavantyyppisiä tehtäviä voidaan näyttää Gantt-kaaviossa.

-   Työt työn mukaan ajoitetuista tuotantotilauksista.
-   Työt suunnitelluista tuotantotilauksista.
-   Tuntiennuste-tyyppiset työn mukaan ajoitetut projektitehtävät.

Gantt-kaavion voit avata kahdessa näkymässä, jotka ovat **tilausnäkymä** ja **resurssinäkymä**[](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true). **Tilausnäkymässä** aktiviteetit on ryhmitelty tuotantotilausten mukaan. Tästä voi olla hyötyä esimerkiksi, jos haluat säilyttää kaikkien samoihin tilauksiin kuuluvien töiden yhteenvedon. **Resurssinäkymässä** kaikki työt on ryhmitelty yksittäisten resurssien mukaan. Tästä näkymästä voi olla hyötyä suunnitelman optimoinnissa resurssitasolla, esimerkiksi laitteen tai laiteryhmän tasolla. Seuraavissa kuvissa esitetyissä Gantt-kaavioissa **Tilausnäkymä** ja **Resurssinäkymä**, on nämä pääelementit:

1.  Gantt-kaavion tehtävä
2.  Materiaalipuute-kuvake
3.  Materiaalin saatavuus -kuvake
4.  Tilauksen toimituspäivä -kuvake
5.  Kapasiteettipalkki

## <a name="order-view"></a>Tilausnäkymä

[![Tilausnäkymä](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Resurssinäkymä
[![Resurssinäkymä](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Tehtävät
Tehtävät näkyvät palkkeina ja järjestetään aika-asteikkoruudukossa ajoitetun aloitus- ja päättymisajan mukaan, jossa palkkien pituus näytetään suhteessa aikaan, joka tarvitaan tehtävän suorittamiseen. Tehtävät näkyvät aika-asteikon mukaan. Voit säätää valikon aika-asteikkoa, jossa voit valita aloitus ja päättymispäivämäärän ja ajan yksikön, esimerkiksi tunteet tai päivät. Säätämällä aika-asteikkoa voit määrittää aikavälin, jossa haluat hallita tehtäviä. 

Yhteenvedon selkeyttämiseksi tehtävien väreille voidaan määrittää erilaiset valinnat. Voit määrittää yksittäisten värin tehtäville, käyttää teemaväriä yleisenä sovelluksen väriteemana tai asettaa värin tuotantotilausten hallitsemiseksi värikoodeittain. 

Määrätyn aikavälin tehtävillä on tietty taustaväri. Aikajaksot, joilla on valkoinen tausta, ilmaisevat aikavälin, jolle on määritetty kapasiteetti tietylle tehtävälle, kun taas harmaalla taustalla merkityt aikajaksot osoittavat aikaväliä, joilla ei ole määritettyä kapasiteettia. 

Kaavion vasemmalla puolella on lisätietoja tehtävästä, esimerkiksi resurssi, jolle tehtävä on ajoitettu, ja tuotannon tilausnumero. Samaan tilaukseen kuuluvien töiden välissä näkyy nuoli. 

Saat lisätietoja tehtävästä tehtävän valintaikkunassa. Avaa valintaikkuna kaksoisnapsauttamalla tehtävää tai valitse **Tietoja**-valikko. Tehtävän valintaikkunassa näkyy ajoitettu alkamis- ja päättymispäivämäärän ja kellonajan tiedot siitä, mitä materiaaleja tehtävässä on määrä kuluttaa. 

Tehtävät voidaan ryhmittää ryhmittelytason mukaan. Ryhmittelytasot ovat hierarkkisia ja niitä voidaan käyttää toimintojen loogiseen ryhmittämiseen. Jos esimerkiksi käytössä on asettelu, missä valmistustehtäviä ryhmitellään toimipaikan, tuotantoyksikön, resurssiryhmän ja resurssin mukaan, voit käyttää ryhmittelytasoja tehtävien ryhmittelyyn kyseisen asettelun mukaan. Ryhmittelytasoja voidaan laajentaa ja tiivistää yksittäisellä ryhmittelytasolla tai kaikilla tasoilla kaaviossa käyttämällä **Laajenna kaikki** ja **Tiivistä kaikki** -painikkeita valikossa. Voit myös määrittää laajennettavat tai tiivistettävät ryhmittelytasot, kun kaavio avataan.

### <a name="material-availability"></a>Materiaalien saatavuus

Gantt-kaavio voidaan määrittää tuottamaan suunnittelutoiminnon, joka sisältää yksityiskohtaisia tietoja materiaalin tilasta yksittäisissä tehtävissä. Esimerkiksi tästä voi olla hyötyä, jos materiaali viivästyy ja vaikuttaa tuotantosuunnitelmaan. Tällöin materiaaliongelmat näkyvät Gantt-kaaviossa korostettuina, jotta suunnittelija ymmärtää seuraukset ja tekee tarvittavat oikaisut. 

Työssä näkyy materiaalipuutteiden kuvake, jos aikataulun mukainen työn aloituspäivä on myöhempi kuin työssä kulutetun materiaalin saatavuuspäivämäärä. Materiaalin saatavuuspäivämäärä lasketaan dynaamisen pääsuunnitelman tarvekohdistustietojen perusteella. Materiaalipuutteiden kuvake näkyy esimerkiksi työssä, jossa käytetään materiaalia, joka on tarvekohdistettu ostotilaukseen ja materiaalin vastaanotto on myöhemmin kuin työn suunniteltu aloituspäivä.

### <a name="indicator-of-material-availability-date"></a>Materiaalin saatavuuspäivämäärän osoitus

Kaavion töissä määritetyn materiaalipuutteen kuvakkeen ohella voit määrittää kyseiseen työhön näkymään myös materiaalin saatavuuspäivämäärän kuvake. Kuvake näkyy vain jos materiaalin saatavuuspäivämäärä sijoittuu kaavion määritettyyn aikaväliin. Jos materiaalin saatavuuspäivämäärä on määritetyn aikavälin ulkopuolella, yksityiskohtaisemmat materiaalin saatavuustiedot saadaan materiaaliluettelosta valintaikkunassa. Luettelossa on myös kuvake, joka näyttää työn myöhässä olevat materiaalit. Voit ajoittaa työn uudelleen käytettämällä materiaalin saatavuuspäivämäärää aloituspäivämääränä.

### <a name="indicator-of-order-delivery-date"></a>Tilauksen toimituspäivän osoitus

Kuvake ilmaisee tuotantotilauksen toimituspäivämäärän. Kuvake näkyy vain tilausnäkymässä.

### <a name="capacity-bar"></a>Kapasiteettipalkki

Voit määrittää kaavion siten, että resurssien kapasiteettipalkki näkyy. Tämä palkki näyttää työn resurssikapasiteetin yhteenvedon määritetyllä aikavälillä kaaviossa. Kapasiteettipalkkia ei näytetä aikajaksoissa, joissa resurssia ei ole varattu. Ajanjaksoissa, joissa resurssi on varattu kapasiteetille, kapasiteettipalkki näkyy kiinteänä. Ajanjaksoissa, joissa resurssi on ylivarattu, palkki näkyy paksumpana ja punaisena. Esimerkiksi jos kaksi työtä on päällekkäin, kapasiteettipalkki ilmaisee ylivarausta päällekkäisellä aikavälillä. Kapasiteettipalkki päivittyy dynaamisesti, kun ajoitat työn. Kapasiteettipalkki otetaan käyttöön **Näytä kapasiteettipalkki** -valikosta. Se voidaan näyttää vain **Resurssinäkymässä**. Jos haluat nähdä yksityiskohtaisemman näkymän resurssin kuormituskapasiteetista, käytä **Kapasiteetin kuormitus** -kaaviota, joka voidaan avata valitun tehtävän valikosta tai pikavalikosta.

## <a name="job-scheduling-in-the-gantt-chart"></a>Töiden ajoittamisen Gantt-kaaviossa
Gantt-kaavion avulla on useita mahdollisuuksia tehdä tuotantosuunnitelman oikaisuja. Gantt-kaaviossa voi ajoittaa uudelleen toimintoja vedä ja pudota -toiminnolla tai aikatauluvalikosta. Voit ottaa suunnitteluprosessissa huomioon resurssikapasiteetin, resurssien suorituskyvyn ja materiaalirajoitukset.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Töiden ajoittaminen Vedä ja pudota -toiminnolla

Voit ajoittaa työn uudelleen määritetyn ajanjakson sisällä vedä ja pudota -toiminnolla. Vain ajoittaa työn uudelleen ainoastaan samalle resurssille ja voit ajoittaa vain yhden työn kerrallaan.

### <a name="schedule-a-job-from-the-menu"></a>Työn ajoittaminen valikosta

**Ajoita työt** -valikossa voidaan ajoittaa vähintään yksi valittu työ kaaviossa ajoituksen suunnan ja ajoituksen päivämäärän perusteella. Käytettävissä on kolme eri ajoitussuuntaa.

-   Ajoituspäivästä eteenpäin
-   Ajoituspäivästä taaksepäin
-   Siirrä eteenpäin materiaalin saatavuuspäivämäärästä

Työtä ei voi ajoittaa Gantt-kaavion määritetyn aikavälin ulkopuolella. Jos näin tehdään, työ jää ajoittamattomaksi ja näyttöön tulee virhesanoma "Työtä ei voitu ajoittaa määritettynä ajanjaksona".

### <a name="schedule-previous-jobs"></a>Ajoita aiemmat työt

Tehtäväverkossa, kuten samaan tuotantotilaukseen kuuluvissa töissä, voit käyttää **Ajoita aiemmat työt** -toimintoa ajoittaessasi edelliset työt suhteessa valittuun työhön verkossa. Seuraavassa esimerkissä korostettu tehtävä on valittu työ. Kaavio näkyy ennen edellisen työn ajoitusta ja seuraavan työn ajoituksen jälkeen. 

[![Ajoita aiempi työ](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Ajoita seuraavat työt

Voit ajoittaa tehtäväverkon valittua työtä seuraavat työt **Ajoita seuraavat työt** -toiminnolla. Seuraavassa esimerkissä korostettu tehtävä on valittu työ. Kaavio näkyy ennen seuraavan työn ajoitusta ja seuraavan työn ajoituksen jälkeen. 

[![Ajoita seuraavat työ](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Ajoita työn ympärille

Voit ajoittaa tehtäväverkon valittua työtä seuraavan ja edellisen työn **Ajoita työn ympärille** -toiminnolla. Seuraavassa esimerkissä korostettu tehtävä on valittu työ. Kaavio näkyy ennen työn ajoitusta ja työn ajoituksen jälkeen. 

[![Ajoita työn ympärille](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Järjestä työt

Voit käyttää **Järjestä** -toimintoa ja ajoittaa saman resurssin valitut tehtävät. Nämä toiminnot voi olla samassa tehtäväverkossa mutta voivat kuulua myös eri verkkoihin. Kun käytät järjestä-toimintoa, valittujen tehtävien väliajat poistuvat. Tämän toiminnon avulla voit optimoida resurssien kapasiteetin käytön. Kaavio näkyy ennen työn ajoitusta ja työn ajoituksen jälkeen. 

[![Järjestä työ](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Tehtävien määrittäminen uudelleen resurssista toiseen

Voit määrittää tehtävän uudelleen resurssista toiseen. Tämä voi olla hyödyllistä tilanteissa, jossa laite on epäkunnossa tai ylivarattu, ja haluat löytää toisen käytettävissä resurssin, joka voi tehdä tehtävän.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Tehtävän määrittäminen uudelleen vedä ja pudota -toiminnolla

**Resurssi**-näkymässä voit määrittää tehtävän uudelleen toiselle resurssille Gantt-kaaviossa vedä ja pudota -toiminnolla. Voit tehdä sen valitsemalla rivin, jossa tehtävä on ajoitettu. Kun rivi on valittu, voit vetää ja pudottaa rivin kaaviossa resurssiin, joka on ryhmitelty toisen resurssin ryhmittelytasolle.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Tehtävän määrittäminen uudelleen Ajoita työt -valikosta

Voit määrittää työn uudelleen **Ajoita työ** -valintaikkunasta, joka avautuu **Ajoita työ** -valikosta. Tästä valikosta voit ainoastaan määrittää työn uudelleen resurssille, joka on ladattu aiemmin Gantt-kaavioon. Jos valitset vain yhden työn, pudotettu resurssi lajitellaan käytettävien resurssien mukaan. Jos valitset useampia töitä, resurssiluettelosta käytettävien resurssien tietoja ei saada.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Lisäresurssien lataaminen Gantt-kaavioon
**Resurssinäkymästä** voit ladata Gantt-kaavioon lisäresursseja. Tämä voi olla hyödyllistä, jos etsitään vaihtoehtoisia resursseja työlle, joka on ajoitettu ylivaratulle tai rikkoutuneelle laitteelle. **Lisäresurssien lataaminen** -sivulla saat luettelon resursseista, jotka ovat ajanmukaisia luettelon avaamispäivämäärästä lähtien. Gantt-kaaviossa valittuun työhön käytettävissä olevat resurssit luetellaan ensimmäisenä. Jos useita töitä on valittu, käytettävissä olevia resursseja ei näy ennen luettelon avaamista. **Lisäresurssien lataaminen** -sivulla voit valita yhden tai useamman resurssin, joka ladataan Gantt-kaavioon kun olet vahvistanut valintasi. Jos valitulle resurssille ei ole ajoitettuja töitä Gantt-kaavion aikavälillä, resurssi sijoitetaan resurssin ryhmittelytasolle Gantt-kaavion tehtäväluettelon loppuun.

### <a name="access-the-gantt-chart"></a>Gantt-kaavion käyttäminen

Gantt-kaavion voit avata seuraavilta sivuilta.


|                                                 <strong>Sivu</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Kuvaus</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Tuotantotilausluettelo ja tiedot</strong>                                    | <strong>Tuotantotilausluettelo ja tiedot</strong> -sivulla voit avata Gantt-kaavion vähintään yhdestä valituista tilauksesta. Kun kaavio avataan <strong>Gantt-kaaviosta</strong>, valikon nimike lataa kaikki valittuun tuotantotilaukseen liittyvät työt sekä työt muista tuotantotilauksista, jotka on ajoitettu samoille resursseille. Jos kaavio avataan <strong>Gantt-kaavio – pikakatselusta</strong>, valikon nimike lataa vain valittuun tuotantotilaukseen liittyvät työt. Tässä näkymässä ei voi ajoittaa töitä. |
|                                               <strong>Resurssi</strong>                                                |                                                                                                                                                        <strong>Resurssi</strong>-sivulla voit avata Gantt-kaavion valikkokohdasta <strong>Gantt-kaavio</strong>. Kun tämä valitaan, kaikki valittuna ajanjaksona resurssille ajoitetut työt ladataan kaavioon.                                                                                                                                                         |
|                                            <strong>Resurssiryhmä</strong>                                             |                                                                                                                                                 <strong>Resurssiryhmä</strong>-sivulla voit avata Gantt-kaavion valikkokohdasta <strong>Gantt</strong>-kaavio. Kun tämä valitaan, kaikki valittuna ajanjaksona resurssiryhmän resurssille ajoitetut työt näytetään.                                                                                                                                                 |
|                                             <strong>Gantt-kaaviot</strong>                                              |                                                                                 <strong>Gantt-kaavio</strong> sivulla voit määrittää Gantt-kaaviot resursseittain ja resurssiryhmittäin. Esimerkiksi jos haluat hallita tiettyjen resurssisarjojen tai resurssiryhmien tuotantotehtäviä, voit tehdä niille yksittäisiä konfiguraatioita <strong>Gantt-kaavio</strong> -sivulla. Voit avata Gantt-kaavion jokaisesta konfiguraatiosta.                                                                                 |
|                                       <strong>Tuntiennusteet</strong> (projekti)                                        |                                                                                                                              <strong>Tuntiennuste</strong>-tyyppiset työn mukaan ajoitetut projektitehtävät voidaan ajoittaa resursseille. <strong>Tuntiennuste</strong>-sivulla <strong>Aikataulutus</strong>-valikossa voit avata Gantt-kaavion tilauksesta ja tarkastella ajoitettuja tuntiennustetyyppisiä projektitehtäviä.                                                                                                                               |
|           <strong>Suoritettava työ</strong> (luettelo <strong>Tuotannon hallinta</strong> -työtilassa)            |                                                                                               <strong>Suoritettava työ -luettelo Tuotannon hallinta</strong> -työtilassa näkyvät tuotanto- ja erätilausten työt, jotka ovat käynnissä työtilan valituilla resursseilla. <strong>Gantt-kaavio</strong> -valikon nimikkeestä voit avata Gantt-kaavion, jossa kaikki luettelossa valitut työt ladataan kaavioon.                                                                                               |
| <strong>Julkaistavat tuotantotilaukset</strong> (avataan <strong>Tuotannon hallinta</strong> -työtilasta) |                                                                                                                                         Julkaistavat tuotantotilaukset -sivu avataan <strong>Tuotannon hallinta</strong> -työtilasta. Tällä sivulla näkyvät ajoitetut tuotanto- ja erätilaukset odottamassa vapautusta. Tällä sivulla voit avata Gantt-kaavion valittujen tuotantotilausten osalta.                                                                                                                                          |

## <a name="additional-resources"></a>Lisäresurssit  
[Visuaalinen ajoitus tuotanto- ja erätilausten Gantt-kaavion avulla (Video)](https://youtu.be/BtbuShkGj4I)

[Tuotannon visuaalinen ajoitus (esittelykäsikirjoitus)](https://mbs.microsoft.com/customersource/northamerica/365Enterprise/learning/documentation/how-to-articles/365finoptvisschep)

