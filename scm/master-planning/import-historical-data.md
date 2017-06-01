---
title: "Kysynnän ennusteiden historiallisten tietojen tuominen"
description: "Jos haluat hakea tarkat kysynnän ennusteet, pyydä historialliset kysyntätiedot nimikettä tai nimikkeen kohdistustunnusta kohti. Tässä aiheessa kerrotaan, miten tietojen entiteettejä käytetään historiallisten kysyntätietojen tuomisessa mistä tahansa järjestelmästä niin, että kysynnän ennusteen tietoja on pidemmältä ajalta."
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0d1e2b9a51c2d7a7c30c2458b7babf8ac5c08118
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="import-historical-data-for-demand-forecasts"></a>Kysynnän ennusteiden historiallisten tietojen tuominen

[!include[banner](../includes/banner.md)]

Ennusteiden tarkkuuden varmistamiseksi historiallisia kysyntätietoja tulee olla niin paljon kuin niitä saadaan nimikettä tai nimikkeen kohdistustunnusta kohti. Jos historiallisia kysyntätietoja ei ole vielä tuotu, tuo ne Microsoft Dynamics 365 for Operations -ohjelman **Historiallinen ulkoinen kysyntä** (ReqDemPlanHistoricalExternalDemandEntity) -tietoyksikön avulla.

**Tietojen hallinta** -työtila sisältää yksikön kaikkien kenttien yleiskatsauksen.

1. Avaa **Tietojen hallinta** -työtila.
2. Valitse **Tietoyksiköt**-ruutu.
3. Suorita haku **Historiallinen ulkoinen kysyntä** -kohdan yksikköluettelosta.
4. Valitse **Kohdekentät**. Seuraavat yksikkökentät ovat pakollisia: sivusto (**DeliveringSiteId**), päivämäärä (**DemandDate**), määrä (**DemandQuantity**) ja joko nimikenumero (**ItemNumber**) tai nimikkeen kohdistustunnus (**ProductAllocationKeyId**).

Voit käyttää tietoyksikköä, kun käytössä on historialliset kysyntätiedot sisältävä Microsoft Excel -tiedosto tai CSV-tiedosto (pilkulla erotettujen arvojen tiedosto). Seuraavassa esimerkissä näytetään, miten tiedot tuodaan CSV-tiedostosta.

## <a name="example"></a>Esimerkki

Voit käyttää esimerkkinä seuraavaa tiedostoa. Lataa [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Tämä tiedosto sisältää nimikkeen D0001 historialliset kysyntätiedot. Se sisältää vain seuraavat pakolliset kentät: sivusto, määrä ja kysynnän päivämäärä.

1. Valitse yritys, johon historialliset kysyntätiedot tuodaan.
2. Avaa **Tietojen hallinta** -työtila.
3. Valitse **Tuo**-ruutu.
4. Syötä tuontiprojektin nimi, kuten **Nimikkeen D0001 historiallisen kysynnän tuominen**.
5. Valitse **Lähdetietojen muoto** -kenttään tuotavan tiedoston muoto. Voit tuoda tämän esimerkin HistoricalDemandData-tiedoston valitsemalla **CSV**.
6. Valitse **Yksikön nimi** -kenttään **Historiallinen ulkoinen kysyntä**.
7. Tallenna tiedosto tietokoneeseen ja lataa se.
8. Valitse **Tuo**.
9. **Suorituksen yhteenveto** -sivu avautuu automaattisesti. Tarkista sivun tuodut tiedot.

Kun historialliset kysyntätiedot on tuotu, voit luoda kysynnän ennusteen.

## <a name="see-also"></a>Lisätietoja

[Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)

