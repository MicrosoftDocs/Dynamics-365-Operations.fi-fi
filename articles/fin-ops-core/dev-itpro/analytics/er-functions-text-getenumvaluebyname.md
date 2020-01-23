---
title: GETENUMVALUEBYNAME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) GETENUMVALUEBYNAME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4ded0c62b4556b21e731cd9b98db2863ec6ec442
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916841"
---
# <span data-ttu-id="c2272-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="c2272-103"><a name="GETENUMVALUEBYNAME">GETENUMVALUEBYNAME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2272-104">`GETENUMVALUEBYNAME`-funktio etsii määritetystä luettelointitietolähteestä tiettyä *Enum*-arvoa käyttämällä *merkkijono*-arvona määritettyä luetteloinnin nimeä.</span><span class="sxs-lookup"><span data-stu-id="c2272-104">The `GETENUMVALUEBYNAME` function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="c2272-105">Jos *Enum*-arvo löytyy, funktio palauttaa sen.</span><span class="sxs-lookup"><span data-stu-id="c2272-105">If the *Enum* value is found, the function returns it.</span></span> <span data-ttu-id="c2272-106">Muussa tapauksessa funktio palauttaa **Null**-luettelointiarvon.</span><span class="sxs-lookup"><span data-stu-id="c2272-106">Otherwise, the function returns the **null** enumeration value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2272-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c2272-107">Syntax</span></span>

```
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a><span data-ttu-id="c2272-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c2272-108">Arguments</span></span>

<span data-ttu-id="c2272-109">`enumeration data source path`: *Luettelointi*</span><span class="sxs-lookup"><span data-stu-id="c2272-109">`enumeration data source path`: *Enumeration*</span></span>

<span data-ttu-id="c2272-110">Tieto lähteen kelvollinen polku, joka on jokin seuraavista luettelointityypeistä:</span><span class="sxs-lookup"><span data-stu-id="c2272-110">The valid path of a data source of one of the following enumeration types:</span></span>

- <span data-ttu-id="c2272-111">Sähköisen raportointimallin (ER) numerointi</span><span class="sxs-lookup"><span data-stu-id="c2272-111">Electronic reporting (ER) model enumeration</span></span>
- <span data-ttu-id="c2272-112">ER-muodon numerointi</span><span class="sxs-lookup"><span data-stu-id="c2272-112">ER format enumeration</span></span>
- <span data-ttu-id="c2272-113">Microsoft Dynamics 365 Financen numerointi</span><span class="sxs-lookup"><span data-stu-id="c2272-113">Microsoft Dynamics 365 Finance enumeration</span></span>

<span data-ttu-id="c2272-114">`enumeration value text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c2272-114">`enumeration value text`: *String*</span></span>

<span data-ttu-id="c2272-115">Merkkijonoarvo, joka edustaa yksittäisen luettelointiarvon nimeä.</span><span class="sxs-lookup"><span data-stu-id="c2272-115">A string value that represents the name of a single enumeration value.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2272-116">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c2272-116">Return values</span></span>

<span data-ttu-id="c2272-117">Tyhjäarvot salliva *Enum*</span><span class="sxs-lookup"><span data-stu-id="c2272-117">Nullable *Enum*</span></span>

<span data-ttu-id="c2272-118">Tulokseksi saatava luettelointiarvo.</span><span class="sxs-lookup"><span data-stu-id="c2272-118">The resulting enumeration value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c2272-119">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c2272-119">Usage notes</span></span>

<span data-ttu-id="c2272-120">Poikkeusta ei heitetä, jos *Enum*-arvoa ei löydy *merkkijono*-arvona määritetyn luettelointiarvon nimen avulla.</span><span class="sxs-lookup"><span data-stu-id="c2272-120">No exception is thrown if an *Enum* value isn't found by using the name of the enumeration value that is specified as a *String* value.</span></span>

## <a name="example"></a><span data-ttu-id="c2272-121">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c2272-121">Example</span></span>

<span data-ttu-id="c2272-122">Seuraavassa kuvassa on tietomallin **ReportDirection**-luettelointi.</span><span class="sxs-lookup"><span data-stu-id="c2272-122">In the following illustration, the **ReportDirection** enumeration is introduced in a data model.</span></span> <span data-ttu-id="c2272-123">Huomaa, että luettelointiarvoille on määritetty otsikot.</span><span class="sxs-lookup"><span data-stu-id="c2272-123">Notice that labels are defined for the enumeration values.</span></span>

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="c2272-124">Seuraavassa kuvassa on nämä tiedot:</span><span class="sxs-lookup"><span data-stu-id="c2272-124">The following illustration shows these details:</span></span>

- <span data-ttu-id="c2272-125">**$Direction**-tietolähde määritetään ER-raportissa.</span><span class="sxs-lookup"><span data-stu-id="c2272-125">The **$Direction** data source is configured in an ER report.</span></span> <span data-ttu-id="c2272-126">Tämä tietolähde määritetään **ReportDirection**-mallin luetteloinnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="c2272-126">This data source is configured based on the **ReportDirection** model enumeration.</span></span>
- <span data-ttu-id="c2272-127">`$IsArrivals`-lauseke on suunniteltu käyttämään mallin luettelointiin perustuvaa **$Direction**-tietolähdettä tämän toiminnon parametrina.</span><span class="sxs-lookup"><span data-stu-id="c2272-127">The `$IsArrivals` expression is designed to use the model enumeration–based **$Direction** data source as a parameter of this function.</span></span>
- <span data-ttu-id="c2272-128">Tämän vertailulausekkeen arvo on **TOSI**.</span><span class="sxs-lookup"><span data-stu-id="c2272-128">The value of this comparison expression is **TRUE**.</span></span>

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a><span data-ttu-id="c2272-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c2272-129">Additional resources</span></span>

[<span data-ttu-id="c2272-130">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="c2272-130">Text functions</span></span>](er-functions-category-text.md)
