---
title: Lähetyksen konsolidoinnin käytännöt
description: Tässä ohjeaiheessa on lähetyksen konsolidointikäytäntöjen joustavan määrityksen mahdollistavan toiminnon yleiskatsaus.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 1f2e1bcd220f0cd94fb1515e42fd3f8250c1c621
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016352"
---
# <a name="shipment-consolidation-policies"></a>Lähetyksen konsolidoinnin käytännöt

Lähetyksen konsolidointikäytäntöjä käyttävän lähetyksen konsolidointiprosessin avulla voidaan tehdä automaattinen lähetyksen konsolidointi automaattisen ja manuaaliseen varastoon vapautuksen aikana. Ennen tätä toimintoa käytössä ollut automatisoitu konsolidointi käyttöönotettiin kiinteäsit koodatuissa kentissä, ja se perustui varastolle määritettyyn **Konsolidoi lähetys varastoon vapautettaessa** -kenttään.

Lähetyksen konsolidointikäytäntöjä käytetään seuraavissa toiminnoissa:

- Automaattisesti varastoon vapauttava erätyö
- Myynti- tai siirtotilauksen **Vapauta varastoon** -komento
- Oma **Vapauta varastoon** -sivu
- **Vapauta varastoon** -komento **Kuormasuunnittelun työtila** -sivulla
- Lähetysten manuaalinen konsolidointi **Konsolidoi lähetykset** - ja **Lähetyksen konsolidoinnin työtila** -sivuilla

Ennen lähetyksen konsolidointikäytäntöjen käyttöönottoa konsolisointitoiminto oli varastotason asetus. Kaikkien saman varaston asiakkaiden kaikilla tilauksilla katsottiin olevan samat konsolidointitarpeet. Lähetyksen konsolidointikäytännöillä lisätään sellaisten skenaarioiden tuki, joissa eri organisaatioilla on erilaiset lähetyksen konsolidointitarpeet.

Käytettävä lähetyksen konsolidointikäytäntö määritetään kyselyjen avulla, minkä jälkeen muokattavalla kenttäjoukolla määritetään kuormarivien määritys lähetystasolla. (Tämä malli muistuttaa aaltomallien käyttämää mallia.) Jokaiseen käytäntöön on lisäksi lisätty **Konsolidoi aiemmin luotujen lähetysten kanssa** -vaihtoehto. Kun tämä vaihtoehto on valittu, *Vapauta varastoon* -menettely etsii konsolidoitavat lähetykset tekemällä haun niissä aiemmin luoduissa lähetyksissä, jotka perustuvat samaan konsolidointikäytäntöön. Tässä tapauksessa järjestelmä valitsee aiemmin luodun lähetyksen tai kuorman sen sijaan, että se loisi uuden. Järjestelmä kuitenkin konsolidoi vain sellaiset aiemmin luodut lähetykset, joiden tila on *Avoin*. Konsolidointikohteina ei pidetä lähetyksiä, jotka kuuluvat aaltojulkaisuun ja joiden tila on vähintään *Vapautettu*.

Kun lähetyksen konsolidointikäytännöt saadaan käyttöön, aiemmin **Varastot** -asetussivulla ollut **Konsolidoi lähetys varastoon vapautettaessa** -asetus piilotetaan. Uuteen lähetyksen konsolidointitoimintoon siirtymistä helpottaa **Lähetyksen konsolidointikäytännöt** -sivulla oleva toiminto, jonka luoma oletuskäytäntö sisältää automaattisesti nykyisten varastojen vanhan asetuksen. Kun tämä oletuskäytäntö on luotu, **Varastot** -asetussivun **Konsolidoi lähetys varastoon vapautettaessa** -asetusta ei oteta enää huomioon.

Voit korvata käytettävän konsolidointikäytännön manuaalisesti **Vapauta varastoon** -sivulla samalla tavoin kuin täyttämiskäytännöt korvataan.

Voit käyttää **Kuormasuunnittelun työtila** -sivun **Vapauta \> Vapauta varastoa** -käyttää muodostaa lähteviä myynti- ja siirtotilausriveihin perustuvia kuormia ennen varastoon vapauttamista. Nämä kuormat käyttävät samaa konsolidointilogiikkaa, joka otettiin käyttöön yhdessä lähetyksen konsolidointikäytäntöjen kanssa.

Voit konsolidoida **Lähetyksen konsolidoinnin työtila** -sivulla sellaiset aiemmin luodut lähetykset, joita ei ole vielä vahvistettu mutta jotka on jo vapautettu varastoon. Tämä toiminto tukee skenaarioita, joissa oman lähetyksen konsolidoinnin sisältävä automaattinen vapautusprosessi suoritetaan monta kertaa päivässä mutta joissa mahdolliset lisäkonsolidoinnit tunnistetaan manuaalisesti, ennen kuin lähetys rahdinkuljettajille valmistuu vahvistusprosessin aikana. Tällä toiminnolla voi konsolidoida myynti- tai siirtotilausriveiltä luodut lähtevät lähetykset koska tahansa sen jälkeen, kun lähetykset on vapautettu varastoon mutta ennen kuin ne vahvistettu.

**Lähetyksen konsolidoinnin työtila** -sivu toimii samalla tavoin kuin kuorman luonnin työtila, jossa voi arvioida useita lähetyksiä samanaikaisesti ja määrittää konsolidoimattoman tilauksen tiettyyn lähetykseen. Voit arvioida ehdotetut konsolidoinnit useita kertoja ja vahvistaa ne käyttämällä lähetyksen konsolidointimalleja. Osa käytetyistä säännöistä estää luvattoman konsolidoinnin ja varoittaa mahdollisista virheistä.

## <a name="overview-of-new-functionality"></a>Uusien toimintojen yleiskatsaus

Tässä osassa käsitellään sivuja, komentoja ja toimintoja, jotka ovat muuttuneet tai jotka lisätään, kun otat *Lähetyksen konsolidointikäytännöt* -toiminnon käyttöön ja käytät sitä.

### <a name="shipment-consolidation-policies-page"></a>Lähetyksen konsolidointikäytännöt -sivu

Käytännöt erotellaan työtilauksen tyypin mukaan. **Myyntitilaukset** -tyyppi vastaa _Myyntitilaus_ -lähetyksiä ja **Siirtotilaukset** -tyyppi vastaa _Siirtovarasto-otto_ -lähetyksiä.

Jokaisessa lähetyksen konsolidointikäytännössä on kysely, joka määrittää, miten sitä käytetään, ja järjestysnumero, joka määrittää suoritusjärjestyksen. Konsolidointia käytetään jokaisessa valittujen kenttien yksilöllisessä yhdistelmässä. Annettua lisäparametria käytetään konsolidointiin aiemmin luotujen (avoimien) lähetysten kanssa. Käytännöt arvioidaan ja niitä käytetään aina, kun uusi lähetys luodaan (ennen aallon käsittelyä).

Jos pakollisia kenttiä puuttuu käytännöstä tai jos siinä on kiellettyjä kenttiä, käytäntö merkitään ei-kelpaavaksi **Valitut** -osassa. Pakollisten ja kiellettyjen kenttien luettelot ovat kiinteästi koodattuja, ja niitä voi laajentaa.

Seuraava luettelo sisältää pakolliset kentät. Koska lähetykset jaetaan aina näitten kenttien perusteella, sellaisia lähetyksiä ei voi ryhmittää, joissa näiden kenttien arvot poikkeavat toisistaan.

- Myyntitilaukset:

    - **Tilinumero:** _WHSShipmentTable.AccountNum_
    - **Toimituksen vastaanottaja:** _WHSShipmentTable.DeliveryName_
    - **Postiosoite (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Varasto:** _WHSShipmentTable.InventLocationId_

- Siirtotilaukset:

    - **Varastosta:** _InventTransferTable.InventLocationIdFrom_
    - **Varastoon:** _InventTransferTable.InventLocationIdTo_

Seuraavat kentät eivät ole käytettävissä kaikissa tiedostotyypeissä. Nämä kentät eivät näy käyttöliittymässä, eikä niitä voi käyttää konsolidoinnissa.

- **Lähetyksen tunnus:** _WHSShipmentTable.ShipmentId_
- **Tila:** _WHSShipmentTable.ShipmentStatus_
- **Lähetyksen konsolidointikäytäntö:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **Työtapahtuman tyyppi:** _WHSShipmentTable.WorkTransType_
- **Aallon tunnus:** _WHSShipmentTable.WaveId_
- **Kuorman tunnus:** _WHSShipmentTable.LoadId_
- **Lähetyksen tunnus:** _WHSLoadLine.ShipmentId_
- **Kuorman tunnus:** _WHSLoadLine.LoadId_

Kun käytäntö luodaan, pakollisten kenttien joukkoa käytetään oletusarvoisesti konsolidointikenttinä. Voit kuitenkin muokata luetteloa vasemmalla ja oikealla nuolipainikkeella. (Prosessi muistuttaa aaltomallien menetelmien valintaprosessia.)

Käyttäjän näihin kenttiin valitsimia arvoja käytetään kaikissa juuri luoduissa lähetyksissä tai ne lisätään aiemmin luotuihin lähetyksiin kyseisten lähetysten konsolidoinnin aikana. Jos kahdessa lähetyksessä on sama arvo kyseisten lähetysten konsolidointiin valitussa kentässä, lähetykset konsolidoidaan. Sama periaate koskee kaikkia seuraavia valittuja konsolidointikenttiä. Jos arvot poikkeavat toisistaan, toinen lähetys hylätään ja valitaan uuteen lähetykseen. Automaattinen konsolidointiprosessi koostuu kaikkien lähetyksen konsolidointikenttien arvojen ainutkertaisten yhdistelmien luomisesta ja lähetyksen määrittämisestä sitten sopivaan yhdistelmään.

Valitsemattomat kentät ohitetaan konsolidointiprosessin aikana. Jos kahdessa lähetyksessä on eri arvot valitsemattomassa kentässä, kenttä tyhjennetään (eli se määritetään tyhjäksi). Jos molemmissa lähetyksissä on sama arvo valitsemattomassa kentässä, kenttä täytetään.

Konsolidointikenttien (eli kenttien, jotka voidaan tyhjentää, jos arvot poikkeavat toisistaan) luettelo on kiinteästi koodattu. Luettelo sisältää kaikki kentät, jotka käynnistetään myynti- tai siirtotilausriviltä, kun uusi lähetys luodaan. Toisin sanoen jos kenttää ei käynnistetä myynti- tai siirtotilausriviltä, se ohitetaan, kun uutta tietoa lisätään aiemmin luotuun lähetykseen.

### <a name="release-to-warehouse-page"></a>Vapauta varastoon -sivu

- Alaruudukossa oleva uusi kenttää osoittaa, että konsolidointikäytäntöä käytettiin.
- Uudella painikkeella voi manuaalisesti valita ja/tai korvata konsolidointikäytännön.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Vapauta varastoon -komento Kuormasuunnittelun työtila -sivulla

- Logiikka muokattiin käyttämään käytettyjä konsolidointikäytäntöjä.
- Lähetykset konsolidoidaan nyt vain yhden kuorman sisällä.

### <a name="consolidate-shipments-page"></a>Konsolidoi lähetykset -sivu

- Samankaltaisten lähetysten (eli konsolidointiehdokkaiden) hakua muutettiin siten, että se käyttää lähetyksen konsolidointikäytännössä valittuja kenttiä.
- Kentät, joiden arvot ovat erilaisia eri lähetyksissä, määritetään nyt tyhjiksi. (Aiemmin käytettiin valitun peruslähetyksen arvoja.)

### <a name="shipment-consolidation-workbench-page"></a>Lähetyksen konsolidoinnin työtila -sivu

- Uudet toiminnot replikoivat manuaalisen konsolidointiprosessin laajamittaisena.
- Tämä sivu avataan nyt **Varastonhallinta** -moduulin **Vapauta varastoon** -valikossa.
- Algoritmi analysoi vielä lähettämättömät aiemmin luodut lähetykset. Se ehdottaa sitten konsilidointia konsolidointikäytännöissä valittujen kenttien perusteella.

## <a name="comparison-of-functionality"></a>Toimintojen vertailu

Seuraavassa taulukossa on yhteenveto siitä, miten lähetyksen konsolidointi toimii, kun lähetyksen konsolidointikäytäntöjä ei käytetä ja kun niitä käytetään.

| Lähetyksen konsolidointikäytännöt eivät ole käytössä | Lähetyksen konsolidointikäytännöt ovat käytössä |
|---|----|
| Ei käytettävissä | Konsolidointiin varatuilla myynti- tai siirtolähetyksillä on oltava sama konsolidointikäytäntö kuin luotavalla lähetyksellä. Vaihtoehtoisesti ne on määritettävä avoimeen lähetykseen (jossa **Konsolidoi aiemmin luotujen lähetysten kanssa** -vaihtoehto on otettu käyttöön.) |
| *Vapauta varastoon* -menettely ei etsi konsolidoitavaa lähetystä tekemällä haun aiemmin luoduissa lähetyksissä. Vain *Vapauta varastoon* -menettelyn nykyisessä esiintymässä luotuja lähetyksiä käytetään etsittäessä konsolidoitavaa lähetystä. | Jos **Konsolidoi aiemmin luotujen lähetysten kanssa** -vaihtoehto on otettu käyttöön käytettävänä olevassa konsolidointikäytännössä, *Vapauta varastoon* -menettely etsii konsolidoitavaa lähetystä tekemällä haun niissä aiemmin luoduissa lähetyksissä, jotka luotiin saman konsolidointikäytännön perusteella. Niinpä jo käytäntöjä on kaksi, käytännön 2 perusteella luotavaa lähetystä ei koskaan konsolidoida käytännön 1 perusteella luotavan lähetyksen kanssa. |
| Ei käytettävissä | Jos konsolidointikäytännön kenttäluettelo on tyhjä tai jos käytäntöä ei löydy, kullekin myynti- tai siirtotilausriville luodaan uusi lähetys. |
| Seuraava konsolidointikenttä määrittää ainutkertaisen arvoyhdistelmän, jota käytetään *siirtorivin* lähetysten konsolidointiin. (Kaikki muut kentät ohitetaan.)<ul><li>Tilausnumero (OrderNum)</li></ul> | Seuraavat konsolidointikentät määrittävät ainutkertaisen arvoyhdistelmän, jota käytetään *siirtorivin* lähetysten konsolidointiin. (Kaikki muut kentät ohitetaan.)<ul><li>Tilausnumero (OrderNum)</li><li>Toimituksen vastaanottaja (DeliveryName)</li><li>Postiosoite (DeliveryPostalAddress)</li><li>ISO-maakoodi (CountryRegionISOCode)</li><li>Osoite (Address)</li><li>Toimipaikka (InventSiteId)</li><li>Varasto (InventLocationId)</li><li>Rahdinkuljettaja (CarrierCode)</li><li>Rahdinkuljettajan palvelu (CarrierServiceCode)</li><li>Toimitustapa (ModeCode)</li><li>Rahdinkuljettajaryhmä (CarrierGroupCode)</li><li>Toimitusehdot (DlvTermId)</li></ul>Ainoastaan nämä kentät ovat käytettävissä ja niitä käytetään uutta lähetystä luotaessa. |
| Seuraavat konsolidointikentät määrittävät ainutkertaisen arvoyhdistelmän, jota käytetään *myyntirivin* lähetysten konsolidointiin. (Kaikki muut kentät ohitetaan.)<ul><li>Tilausnumero (OrderNum)</li><li>Asiakasviite (CustomerRef)</li><li>Asiakkaan tilaus (CustomerReq)</li><li>Toimitusehdot (DlvTermId)</li></ul> | Seuraavat konsolidointikentät määrittävät ainutkertaisen arvoyhdistelmän, jota käytetään *myyntirivin* lähetysten konsolidointiin. (Kaikki muut kentät ohitetaan.)<ul><li>Tilausnumero (OrderNum)</li><li>Tilinumero (AccountNum)</li><li>Toimituksen vastaanottaja (DeliveryName)</li><li>Postiosoite (DeliveryPostalAddress)</li><li>ISO-maakoodi (CountryRegionISOCode)</li><li>Osoite (Address)</li><li>Toimipaikka (InventSiteId)</li><li>Varasto (InventLocationId)</li><li>Rahdinkuljettaja (CarrierCode)</li><li>Rahdinkuljettajan palvelu (CarrierServiceCode)</li><li>Toimitustapa (ModeCode)</li><li>Rahdinkuljettajaryhmä (CarrierGroupCode)</li><li>Välittäjän tunnus (BrokerCode)</li><li>Suunta (LoadDirection)</li><li>Toimitusehdot (DlvTermId)</li><li>Asiakasviite (CustomerRef)</li><li>Asiakkaan tilaus (CustomerReq)</li></ul>Ainoastaan nämä kentät ovat käytettävissä ja niitä käytetään uutta lähetystä luotaessa. |
| Ei käytettävissä | Seuraavat konsolidointikentät ovat pakollisia *myyntirivin* osalta eikä niitä voi poistaa:<ul><li>Tilinumero (AccountNum)</li><li>Toimituksen vastaanottaja (DeliveryName)</li><li>Postiosoite (DeliveryPostalAddress)</li><li>Varasto (InventLocationId)</li></ul>Nämä kentät määritetään oletusarvoisesti, kun uusi käytäntö luodaan. Niitä ei voi poistaa. |
| **Kuormasuunnittelun työtila** -sivun *Kuormien vapautus varastoon* -menettely käyttää oma erillistä koodia lähetysten ja aaltojen luontiin. | Lähetyksen konsolidointikäytäntöjä käytetään määrittämään, mitkä kentät on arvioitava konsolidointia varten. Lähetykset konsolidoidaan vain yhden kuorman sisällä. |
| **Kaikki lähetykset** -sivulla voi valita ensin manuaalisesti **Konsolidoi lähetykset** ja sitten peruslähetyskohteen. Suodatin ehdottaa aiemmin luotuja lähetyksiä, joiden useiden avainkenttiä arvot ovat samat. | **Kaikki lähetykset** -sivulla voi valita ensin manuaalisesti **Konsolidoi lähetykset** ja sitten peruslähetyskohteen. Järjestelmä ehdottaa muita aiemmin luotuja lähetyksiä vertaamalla useiden sellaisten avainkenttien arvoja, jotka on määritetty soveltuville lähetyksen konsolidointikäytännöille. |
| **Kaikki lähetykset** -sivun **Konsolidoi lähetykset** -komentoa voi käyttää vain samassa lähetyksessä. | **Lähetyksen konsolidoinnin työtila** -sivun avulla voi etsiä lähetyksiä, joiden tilana ei ole vielä lähetetty. Nämä lähetykset analysoidaan useiden lähetyksen konsolidointikäytännöissä määritettyjen avainkenttien perusteella. Kaikkia lähetyksiä, joissa on vastaavat arvot kyseisissä kentissä, ehdotetaan konsolidoitaviksi.<p>Konsolidointia voi ylläpitää manuaalisesti poistamalla lähetyksiä ehdotetuista konsolidoinneista ja/tai lisäämällä lähetyksiä niihin. Vaikka erilaisia virheitä voi esiintyä, jotkin niistä voidaan ohittaa.</p> |
| **Rakennetta koskeva huomautus:** *Myyntilausten automaattinen vapautus varastoon* -menettely jakaa rivit ryhmiin. Kussakin ryhmässä on oma yksilöivä **ReleaseToWarehouseId** -arvo, ja *Vapauta varastoon* -menettely käsittelee sen erikseen. Tämä menettely luo uuden työn työn katkoasetuksista riippumatta. | **Rakennetta koskeva huomautus:** *Myyntitilausten automaattinen vapautus varastoon* -menettely määrittää saman **ReleaseToWarehouseId** -arvon kaikille käsiteltäville myyntiriveille. *Vapauta varastoon* -menettely käsittelee kaikki myyntirivit samanaikaisesti. Aiemman toiminnan voi varmistaa määrittämällä työn katkon lähetyksen tunnuksen mukaan. |

## <a name="additional-resources"></a>Lisäresurssit

- [Lähetyksen konsolidointikäytäntöjen määrittäminen](configure-shipment-consolidation-policies.md)
