---
title: Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen
description: Tässä menettelyssä kerrotaan, miten tuotteen elinkaaren tila liitetään julkaistuun päätuotteeseen ja sen variantteihin.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555905"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Tuotteen elinkaaren tilan liittäminen vapautettuun päätuotteeseen

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

