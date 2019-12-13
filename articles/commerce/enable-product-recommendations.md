---
title: Ota tuotesuositukset käyttöön
description: Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770136"
---
# <a name="enable-product-recommendations"></a>Ota tuotesuositukset käyttöön

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Suositusten esitarkistus
Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain F&O-asiakkaille, joilla on käytössä versio 10.0.6 ja jotka ovat siirtäneet tallennustilan käyttämään BDL-ratkaisua. 

Varmista myös, että RetailSale-mittarit on otettu käyttöön. Lisätietoja tästä määritysprosessista on [täällä.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Suositusten ottaminen käyttöön

Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail** &gt; **Tuotesuositukset** &gt; **Suositusparametrit**.
1. Valitse vähittäismyynnin jaettujen parametrien luettelossa **Suositusluettelot**.
1. Määritä **Ota suositukset käyttöön** -asetukseksi **Kyllä**.

![ota tuotesuositukset käyttöön](./media/enableproductrecommendations.png)

> [!NOTE]
> Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin. Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 for Commerce -sovelluksessa voi kestää useita tunteja.

## <a name="configure-recommendation-list-parameters"></a>Suositusluettelon parametrien määrittäminen
Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot. Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla. Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Suositusten näyttäminen myyntipistelaitteissa
Kun suositukset on otettu käyttöön taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla. Lisätietoja tästä prosessista on [täällä.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Tuotesuositusluetteloiden lisääminen sivuille](add-reco-list-to-page.md)

[Suositusten paneelin lisääminen myyntipistelaitteisiin](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


