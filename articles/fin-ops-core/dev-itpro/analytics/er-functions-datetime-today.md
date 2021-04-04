---
title: TODAY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) TODAY-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9288baf4e6123a7c03152f524a852eae9b671dde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567913"
---
# <a name="today-er-function"></a><span data-ttu-id="231ca-103">TODAY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="231ca-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="231ca-104">`TODAY`-funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="231ca-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="231ca-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="231ca-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="231ca-106">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="231ca-106">Return values</span></span>

<span data-ttu-id="231ca-107">*Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="231ca-107">*Date*</span></span>

<span data-ttu-id="231ca-108">Tulokseksi saatava päivämääräarvo.</span><span class="sxs-lookup"><span data-stu-id="231ca-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="231ca-109">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="231ca-109">Example</span></span>

<span data-ttu-id="231ca-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="231ca-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="231ca-111">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="231ca-111">Additional resources</span></span>

[<span data-ttu-id="231ca-112">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="231ca-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]