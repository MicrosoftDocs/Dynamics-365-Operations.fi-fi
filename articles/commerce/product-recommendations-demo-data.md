---
title: Suositusten luominen esittelytietojen avulla
description: Tämä artikkeli antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a0e6666cc163f97567cf5c6f820d436ef6ef4cca
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874892"
---
# <a name="create-recommendations-with-demo-data"></a>Suositusten luominen esittelytietojen avulla

[!include [banner](includes/banner.md)]

Tämä artikkeli antaa ohjeita monikanavan tuotesuositusten käyttämiseen tason 1 yhden ruudun ympäristöissä käyttämällä valmiiksi täytettyjä ja mukautettavia esittelytietoja.

Monikanavan tuotesuositukset tarjoavat joukon manuaalisesti koottuja tai ohjelmallisesti luotuja tuoteluetteloita. Näitä luetteloita voidaan käyttää useissa skenaarioissa liiketoimintatarpeiden mukaan. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

Tason 2 ja sitä korkeampien Dynamics 365 -ympäristöjen tuotesuositukset lasketaan automaattisesti asiakastietojen perusteella. Tuotesuositusten demotietojen käyttäminen ei poista käytöstä mitään ympäristöön lisättyä tuotesuositusten ratkaisua tai mitään sen käyttöön liittyviä kustannuksia.

Tason 1 ympäristöjen tuotesuositukset perustuvat vain .csv-tiedoston sisältämiin staattisiin esittelytietoihin.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Tuotesuositusten demotietojen ottaminen käyttöön ympäristössä
Jos haluat ottaa käyttöön tuotesuositusten esittelypäivämäärän, sinun on otettava käyttöön Dynamics 365 Commerce -esikatselun esittelylaajennus kyseisessä ympäristössä. Kun näin tehdään, tuotesuositusten esittelytiedot otetaan automaattisesti käyttöön.

## <a name="default-demo-data"></a>Oletusarvoiset demotiedot
Jokaisessa Onebox-tyyppisessä ympäristössä on valmiita tuotesuositusten demotietoja. Ne on tallennettu pilkuilla erotettuun reco_demo_data.csv-tiedostoon, joka sijaitsee samassa kansiossa kuin tämä asiakirja Commerce Scale Unitissa.

Tiedot on järjestetty seuraaviin sarakkeisiin.

| Sarakkeen nimi         | Pakollinen          | kuvaus                                                                                                                                 | Mahdolliset arvot                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Tuotesuosituksen tietty luettelotyyppi, jonka esittelytietojen piste luo.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Tietty toimintayksikön numero, jossa tuotesuositusten odotetaan näkyvän.                                        |                                                                              |
| Luokka            |                    |    Luokka, jolle määritetty luettelo tulisi palauttaa. Jos luokkaa ei ole määritetty, luettelo koskee vain siirtymishierarkian ylätasoa.    |                                                                              |
| SeedItemId          |                    |    Jos luettelo edellyttää alkuarvoa (RecoPeopleAlsoBuy ja RecoCart), tuote, jolle näiden luetteloiden tulisi näyttää lisätuotteita.            |                                                                              |
| Asiakastunnus          |                    |    Luettelo, joka edellyttää asiakastunnusta (RecoPicks).  Oletusarvo 0 koskee kaikkia asiakkaita.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Yksi tai useampi tuloksena palautettava tuote, erotettu toisistaan ‘;’-merkillä.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Mukauta demotietoja
Voit muokata oletusarvoisia esittelytietoja HQ:ssa määritettyjen tuote- ja luokkatietojen avulla. Sen jälkeen, kun .csv on päivitetty, asiakkaille palautetut tuotesuositukset päivitetään heti muutosten mukaisesti.

Laajennus sisältää datatiedoston nimeltään RecoMockDataset.csv. Sen avulla asiakas voi hallita tietojoukkoa, jota käytetään suositusten esimerkkitulosten luomiseen. Tiedoston nimeä voidaan hallita laajennuksen kokoonpanon kautta käyttämällä **ext.Recommendations.DemoFilePath**-asetusta. Näin käytettävissä voi olla useita tietojoukkoja, joita voidaan vaihtaa helposti kokoonpanon kautta.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Azure Data Lake Storagen käyttöönotto Dynamics 365 Commerce -ympäristössä](enable-adls-environment.md)

[Tuotesuositusten ottaminen käyttöön](enable-product-recommendations.md)

[Kohdennettujen suositusten ottaminen käyttöön](personalized-recommendations.md)

[Kohdennetuista tuotesuosituksista kieltäytyminen](personalization-gdpr.md)

["Osta samankaltaisia tyylejä" -suositusten käyttöönotto](shop-similar-looks.md)

[Tuotesuositusten lisääminen myyntipisteessä](product.md)

[Suositusten lisääminen tapahtumanäyttöön](add-recommendations-control-pos-screen.md)

[AI-ML-suositusten tulosten muokkaaminen](modify-product-recommendation-results.md)

[Kuratoitujen suositusten manuaalinen luominen](create-editorial-recommendation-lists.md)

[Tuotesuositukset – usein kysytyt kysymykset](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]