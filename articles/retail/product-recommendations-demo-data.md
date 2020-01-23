---
title: Omni-Channel-tuotesuositusten demotiedot
description: Tämän asiakirjan tarkoituksena on antaa ohjeita Omni-Channel-tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia demotietoja.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872323"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Omni-Channel-tuotesuositusten demotiedot

Tämän asiakirjan tarkoituksena on antaa ohjeita Omni-Channel-tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia demotietoja.

Omni-Channel-tuotesuositukset tarjoavat joukon manuaalisesti koottuja tai ohjelmallisesti luotuja tuoteluetteloita järjestyksessä. Näitä luetteloita voidaan käyttää useissa skenaarioissa liiketoimintatarpeiden mukaan. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md).

Tason 2 ja sitä korkeampien Dynamics-ympäristöjen tuotesuositukset lasketaan automaattisesti asiakastietojen perusteella.
Tuotesuositusten demotietojen käyttäminen ei poista käytöstä mitään ympäristöön lisättyä tuotesuositusten ratkaisua tai mitään sen käyttöön liittyviä kustannuksia.

Tason 1 ympäristöjen tuotesuositukset perustuvat vain CSV-tiedoston sisältämiin staattisiin demotietoihin.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tuotesuositusten demotietojen ottaminen käyttöön ympäristössä

Asiakkaiden on otettava käyttöön **Dynamics 365 Commerce -esikatselun demo-laajennus** kyseisessä ympäristössä, mikä ottaa tuotesuositusten demotiedot automaattisesti käyttöön.

## <a name="default-demo-data"></a>Oletusarvoiset demotiedot
Jokaisessa Onebox-tyyppisessä ympäristössä on valmiita tuotesuositusten demotietoja. Ne on tallennettu pilkuilla erotettuun **reco_demo_data.csv**-tiedostoon, joka sijaitsee samassa kansiossa kuin tämä asiakirja Retail Serverissä.

Nämä tiedot on järjestetty seuraaviin sarakkeisiin.

| Sarakkeen nimi         | Pakollinen          | Kuvaus                                                                                                                                 | Mahdolliset arvot                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tuotesuosituksen tietty luettelotyyppi, jonka demotietojen piste luo.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Tietty toimintayksikön numero, jossa tuotesuositusten odotetaan näkyvän.                                        |                                                                              |
| Luokka            |                    |    Luokka, jolle määritetty luettelo tulisi palauttaa. Jos luokkaa ei ole määritetty, luettelo koskee vain siirtymishierarkian ylätasoa.    |                                                                              |
| SeedItemId          |                    |    Jos luettelo edellyttää alkuarvoa (RecoPeopleAlsoBuy ja RecoCart), tuote, jolle näiden luetteloiden tulisi näyttää lisätuotteita.            |                                                                              |
| ItemIds             | :heavy_check_mark: | Yksi tai useampi tuloksena palautettava tuote, erotettu toisistaan **‘;’**-merkillä.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Mukauta demotietoja
Asiakkaat voivat muokata oletusarvoisia demotietoja HQ:ssa määritettyjen tuote- ja luokkatietojen avulla. Kun CSV on päivitetty, asiakkaille palautetut tuotesuositukset päivitetään heti muutosten mukaisesti.

Laajennus sisältää datatiedoston nimeltään RecoMockDataset.csv. Sen avulla asiakas voi hallita tietojoukkoa, jota käytetään suositusten esimerkkitulosten luomiseen. Tiedoston nimeä voidaan hallita laajennuksen kokoonpanon kautta käyttämällä **ext.Recommendations.DemoFilePath**-asetusta. Näin asiakkaalla voi olla käytettävissä useita tietojoukkoja, joita voidaan vaihtaa helposti kokoonpanon kautta.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](../commerce/product-recommendations.md)

[Työympäristön suunnittelu](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
