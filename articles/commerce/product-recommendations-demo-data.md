---
title: Tuotesuositusten luonti esittelytietojen avulla
description: Tämän asiakirja antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af8a30e69d9ed143e045950efdcece207f6da14c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697931"
---
# <a name="get-product-recommendations-using-demo-data"></a>Tuotesuositusten luonti esittelytietojen avulla
Tämän asiakirja antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.

Monikanavan tuotesuositukset tarjoavat joukon manuaalisesti koottuja tai ohjelmallisesti luotuja tuoteluetteloita. Näitä luetteloita voidaan käyttää useissa skenaarioissa liiketoimintatarpeiden mukaan. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

Tason 2 ja sitä korkeampien Dynamics 365 -ympäristöjen tuotesuositukset lasketaan automaattisesti asiakastietojen perusteella. Tuotesuositusten demotietojen käyttäminen ei poista käytöstä mitään ympäristöön lisättyä tuotesuositusten ratkaisua tai mitään sen käyttöön liittyviä kustannuksia.

Tason 1 ympäristöjen tuotesuositukset perustuvat vain .csv-tiedoston sisältämiin staattisiin esittelytietoihin.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tuotesuositusten demotietojen ottaminen käyttöön ympäristössä
Jos haluat ottaa käyttöön tuotesuositusten esittelypäivämäärän, sinun on otettava käyttöön Dynamics 365 Commerce -esikatselun esittelylaajennus kyseisessä ympäristössä. Kun näin tehdään, tuotesuositusten esittelytiedot otetaan automaattisesti käyttöön.

## <a name="default-demo-data"></a>Oletusarvoiset demotiedot
Jokaisessa Onebox-tyyppisessä ympäristössä on valmiita tuotesuositusten demotietoja. Ne on tallennettu pilkuilla erotettuun reco_demo_data.csv-tiedostoon, joka sijaitsee samassa kansiossa kuin tämä asiakirja Retail Serverissä.

Tiedot on järjestetty seuraaviin sarakkeisiin.

| Sarakkeen nimi         | Pakollinen          | Kuvaus                                                                                                                                 | Mahdolliset arvot                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tuotesuosituksen tietty luettelotyyppi, jonka esittelytietojen piste luo.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Tietty toimintayksikön numero, jossa tuotesuositusten odotetaan näkyvän.                                        |                                                                              |
| Luokka            |                    |    Luokka, jolle määritetty luettelo tulisi palauttaa. Jos luokkaa ei ole määritetty, luettelo koskee vain siirtymishierarkian ylätasoa.    |                                                                              |
| SeedItemId          |                    |    Jos luettelo edellyttää alkuarvoa (RecoPeopleAlsoBuy ja RecoCart), tuote, jolle näiden luetteloiden tulisi näyttää lisätuotteita.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Yksi tai useampi tuloksena palautettava tuote, erotettu toisistaan ‘;’.-merkillä.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Mukauta demotietoja
Voit muokata oletusarvoisia esittelytietoja HQ:ssa määritettyjen tuote- ja luokkatietojen avulla. Kun .csv on päivitetty, asiakkaille palautetut tuotesuositukset päivitetään heti muutosten mukaisesti.

Laajennus sisältää datatiedoston nimeltään RecoMockDataset.csv. Sen avulla asiakas voi hallita tietojoukkoa, jota käytetään suositusten esimerkkitulosten luomiseen. Tiedoston nimeä voidaan hallita laajennuksen kokoonpanon kautta käyttämällä **ext.Recommendations.DemoFilePath**-asetusta. Näin käytettävissä voi olla useita tietojoukkoja, joita voidaan vaihtaa helposti kokoonpanon kautta.


```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Työympäristön suunnittelu](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
