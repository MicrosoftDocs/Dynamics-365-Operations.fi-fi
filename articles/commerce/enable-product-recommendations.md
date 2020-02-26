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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024953"
---
# <a name="enable-product-recommendations"></a>Ota tuotesuositukset käyttöön

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa kerrotaa, miten tekoälyn koneoppimiseen perustuvia tuotesuosituksia voidaan tehdä Microsoft Dynamics 365 Commerce -asiakkaiden käyttöä varten. Lisätietoja tuotesuositusten luetteloista on kohdassa [Tuotesuositusten yleiskatsaus](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Suositusten esitarkistus

Ota huomioon ennen käyttöönottoa, että tuotesuosituksia tuetaan vain Commerce-asiakkaille, jotka ovat siirtäneet tallennustilansa Azure Data Lake Storagea (ADLS:ää) käyttäen. 

Katso ADLS:n käyttöönoton vaiheet kohdasta [ADLS:n käyttöönotto Dynamics 365 -ympäristössä](enable-ADLS-environment.md).

Varmista myös, että RetailSale-mittarit on otettu käyttöön. Lisätietoja tästä määritysprosessista on [täällä.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Suositusten ottaminen käyttöön

Voit ottaa tuotesuositukset käyttöön noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Retail ja Commerce &gt; Tuotesuositukset &gt; Suositusparametrit**.
1. Valitse jaettujen parametrien luettelossa **Suositusluettelot**.
1. Määritä **Ota suositukset käyttöön** -asetukseksi **Kyllä**.

![ota tuotesuositukset käyttöön](./media/enableproductrecommendations.png)

> [!NOTE]
> Tämä menettely käynnistää tuotesuositusluetteloiden luontiprosessin. Luetteloiden luominen, niiden saaminen käyttöön ja näkyminen myyntipisteessä tai Dynamics 365 Commerce -sovelluksessa voi kestää useita tunteja.

## <a name="configure-recommendation-list-parameters"></a>Suositusluettelon parametrien määrittäminen

Oletusarvoisesti tekoälyyn perustuva tuotesuositusluettelo sisältää ehdotetut arvot. Voit muuttaa ehdotettuja oletusarvoja haluamallasi tavalla. Lisätietoja oletusparametrien muuttamisesta on kohdassa [Tekoälyn koneoppimiseen perustuvan tuotesuositusluettelon hallinta](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Suositusten näyttäminen myyntipistelaitteissa

Kun suositukset on otettu käyttöön Commercen taustatoiminnossa, suosituspaneeli on lisättävä ohjausobjektin myyntipistenäyttöön asettelutyökalun avulla. Lisä tietoja tästä prosessista on kohdassa [Suositusten ohjausobjektin lisääminen myyntipisteen laitteen tapahtumaruudulle](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Ota käyttöön kohdennetut tuotesuositukset

Lisätietoja mukautettujen suositusten vastaanottamisesta on kohdassa [Mukautettujen suositusten ottaminen käyttöön](personalized-recommendations.md).

## <a name="additional-resources"></a>Lisäresurssit

[Tuotesuositusten yleiskatsaus](product-recommendations.md)

[Ota käyttöön kohdennetut tuotesuositukset](personalized-recommendations.md)

[Tuotesuositusluetteloiden lisääminen sivuille](add-reco-list-to-page.md)

[Suositusten paneelin lisääminen myyntipistelaitteisiin](add-recommendations-control-pos-screen.md)

[Tuotekokoelmamoduulin yleiskuvaus](product-collection-module-overview.md)

[ADLS:n käyttöönotto Dynamics 365 -ympäristössä](enable-ADLS-environment.md)

