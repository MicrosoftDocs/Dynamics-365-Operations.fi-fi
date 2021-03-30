---
title: Kysynnän ennusteiden historiallisten tietojen tuominen
description: Jos haluat hakea tarkat kysynnän ennusteet, pyydä historialliset kysyntätiedot nimikettä tai nimikkeen kohdistustunnusta kohti. Tässä aiheessa kerrotaan, miten tietojen entiteettejä käytetään historiallisten kysyntätietojen tuomisessa mistä tahansa järjestelmästä niin, että kysynnän ennusteen tietoja on pidemmältä ajalta.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d415895bd05b9ab1a2311ab69cc3757047df91db
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204613"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Kysynnän ennusteiden historiallisten tietojen tuominen

[!include [banner](../includes/banner.md)]

Ennusteiden tarkkuuden varmistamiseksi historiallisia kysyntätietoja tulee olla niin paljon kuin niitä saadaan nimikettä tai nimikkeen kohdistustunnusta kohti. Jos historiallisia kysyntätietoja ei ole vielä tuotu, tuo ne Dynamics 365 Supply Chain Managementin **Historiallinen ulkoinen kysyntä** (ReqDemPlanHistoricalExternalDemandEntity) -tietoyksikön avulla.

**Tietojen hallinta** -työtila sisältää yksikön kaikkien kenttien yleiskatsauksen.

1. Avaa **Tietojen hallinta** -työtila.
2. Valitse **Tietoyksiköt**-ruutu.
3. Suorita haku **Historiallinen ulkoinen kysyntä** -kohdan yksikköluettelosta.
4. Valitse **Kohdekentät**. Seuraavat yksikkökentät ovat pakollisia: sivusto (**DeliveringSiteId**), päivämäärä (**DemandDate**), määrä (**DemandQuantity**) ja joko nimikenumero (**ItemNumber**) tai nimikkeen kohdistustunnus (**ProductAllocationKeyId**).

Voit käyttää tietoyksikköä, kun käytössä on historialliset kysyntätiedot sisältävä Microsoft Excel -tiedosto tai CSV-tiedosto (pilkulla erotettujen arvojen tiedosto). Seuraavassa esimerkissä näytetään, miten tiedot tuodaan CSV-tiedostosta.

Lisätietoja tietojen tuonnista sekä tietojen tyhjentämisestä tuonnin jälkeen on kohdassa [Tietojen tuonti- ja vientityöt – yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) ja siihen liittyvissä aiheissa.

## <a name="example"></a>Esimerkki

Voit käyttää esimerkkinä seuraavaa tiedostoa. Lataa [HistoricalDemandData](https://docs.microsoft.com/dynamics/s-e/). Tämä tiedosto sisältää nimikkeen D0001 historialliset kysyntätiedot. Se sisältää vain seuraavat pakolliset kentät: sivusto, määrä ja kysynnän päivämäärä.

1. Valitse yritys, johon historialliset kysyntätiedot tuodaan.
2. Avaa **Tietojen hallinta** -työtila.
3. Valitse **Tuonti**-ruutu.
4. Syötä tuontiprojektin nimi, kuten **Nimikkeen D0001 historiallisen kysynnän tuominen**.
5. Valitse **Lähdetietojen muoto** -kenttään tuotavan tiedoston muoto. Voit tuoda tämän esimerkin HistoricalDemandData-tiedoston valitsemalla **CSV**.
6. Valitse **Yksikön nimi** -kenttään **Historiallinen ulkoinen kysyntä**.
7. Tallenna tiedosto tietokoneeseen ja lataa se.
8. Valitse **Tuo**.
9. **Suorituksen yhteenveto** -sivu avautuu automaattisesti. Tarkista sivun tuodut tiedot.

Kun historialliset kysyntätiedot on tuotu, voit luoda kysynnän ennusteen.

## <a name="additional-resources"></a>Lisäresurssit

[Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)  
[Tietojen tuonti- ja vientityöt – yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]