---
title: Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren tila liitetään julkaistuun päätuotteeseen ja sen variantteihin.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62078025623a0cfc1ed6797c84907c7872dfaf38095855240b306e08f3decca7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716513"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren tila liitetään julkaistuun päätuotteeseen ja sen variantteihin. Edellytykset: Sinun on toistettava ensin Uuden tuotteen elinkaaren tilan luominen -tehtäväopas ja varmistettava, että luotuna on vähintään yksi tuotteen elinkaaren tila, ennen kuin toistat tämän tehtäväoppaan.


## <a name="find-a-released-product-master"></a>Etsi julkaistu päätuote
1. Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.
2. Etsi haluamasi tietue luettelosta ja valitse se.

> [!NOTE]
> Päätuotteen tuotteen alatyyppi on Päätuote.  

## <a name="update-the-lifecycle-state"></a>Elinkaaren tilan päivittäminen
1. Valitse Muokkaa.
2. Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.
3. Valitse Tallenna.
4. Valitse Kyllä.

> [!NOTE]
> Jos valittuna on Kyllä, kaikki liittyvät julkaistut tuotevariantit, joilla on sama alkuperäinen tila kuin julkaistulla päätuotteella, päivitetään myös uuden tuotteen elinkaaren tilan mukaisesti. Jos valittuna on Ei, kaikkien varianttien tila pysyy entisellään. Variantteja, joilla on eri tuotteen elinkaaren tila kuin julkaistulla päätuotteella, ei päivitetä.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Varianttien elinkaaren tilan tarkistaminen
1. Valitse Vapautetut tuotevariantit.

> [!NOTE]
> Huomaa, että kaikki variantit ovat perineet valitun elinkaaren tilan julkaistulta päätuotteelta.  

2. Merkitse valittu rivi luettelossa.
3. Syötä tai valitse arvo Tuotteen elinkaaren tila -kenttään.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]