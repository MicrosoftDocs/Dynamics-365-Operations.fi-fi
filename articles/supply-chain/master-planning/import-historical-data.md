---
title: Kysynnän ennusteiden historiallisten tietojen tuominen
description: Jos haluat hakea tarkat kysynnän ennusteet, pyydä historialliset kysyntätiedot nimikettä tai nimikkeen kohdistustunnusta kohti. Tässä aiheessa kerrotaan, miten tietojen entiteettejä käytetään historiallisten kysyntätietojen tuomisessa mistä tahansa järjestelmästä niin, että kysynnän ennusteen tietoja on pidemmältä ajalta.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5489a23ed885f28e66a6eb300ce9d254bad8af68496d7f9f37cbb51e11b18eba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782536"
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

Katso myös [Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]