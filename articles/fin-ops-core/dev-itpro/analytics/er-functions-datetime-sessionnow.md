---
title: SESSIONNOW ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) SESSIONNOW-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d70acb06194a28af0cc85eea440e9e4e937bc3bb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683840"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="d2166-103">SESSIONNOW ER -funktio</span><span class="sxs-lookup"><span data-stu-id="d2166-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2166-104">`SESSIONNOW`-funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="d2166-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2166-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="d2166-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="d2166-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="d2166-106">Return values</span></span>

<span data-ttu-id="d2166-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="d2166-107">*DateTime*</span></span>

<span data-ttu-id="d2166-108">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="d2166-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="d2166-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d2166-109">Example</span></span>

<span data-ttu-id="d2166-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="d2166-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2166-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d2166-111">Additional resources</span></span>

[<span data-ttu-id="d2166-112">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="d2166-112">Date and time functions</span></span>](er-functions-category-datetime.md)
