---
title: ORDERBY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ORDERBY-funktiota käytetään.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 51da7f3766f5af901c8be6668bc2511cd8e2f9e9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753189"
---
# <a name="orderby-er-function"></a><span data-ttu-id="f812f-103">ORDERBY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="f812f-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f812f-104">`ORDERBY`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on lajiteltu määritettyjen argumenttien mukaan.</span><span class="sxs-lookup"><span data-stu-id="f812f-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="f812f-105">Nämä argumentit voivaan määrittää lausekkeina.</span><span class="sxs-lookup"><span data-stu-id="f812f-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="f812f-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f812f-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="f812f-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f812f-107">Arguments</span></span>

<span data-ttu-id="f812f-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="f812f-108">`list`: *Record list*</span></span>

<span data-ttu-id="f812f-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="f812f-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="f812f-110">`expression 1`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="f812f-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="f812f-111">Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa.</span><span class="sxs-lookup"><span data-stu-id="f812f-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="f812f-112">Viitatun kentän on oltava primitiivisen tietotyypin kenttä.</span><span class="sxs-lookup"><span data-stu-id="f812f-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="f812f-113">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="f812f-113">This argument is required.</span></span>

<span data-ttu-id="f812f-114">`expression N`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="f812f-114">`expression N`: *Field*</span></span>

<span data-ttu-id="f812f-115">Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa.</span><span class="sxs-lookup"><span data-stu-id="f812f-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="f812f-116">Viitatun kentän on oltava primitiivisen tietotyypin kenttä.</span><span class="sxs-lookup"><span data-stu-id="f812f-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="f812f-117">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="f812f-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="f812f-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f812f-118">Return values</span></span>

<span data-ttu-id="f812f-119">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="f812f-119">*Record list*</span></span>

<span data-ttu-id="f812f-120">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="f812f-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="f812f-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="f812f-121">Example 1</span></span>

<span data-ttu-id="f812f-122">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( ORDERBY( DS, DS. Value)).Value` palauttaa tekstiarvon **A**.</span><span class="sxs-lookup"><span data-stu-id="f812f-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f812f-123">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="f812f-123">Example 2</span></span>

<span data-ttu-id="f812f-124">Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `ORDERBY (Vendors, Vendors.'name()')` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="f812f-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f812f-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f812f-125">Additional resources</span></span>

[<span data-ttu-id="f812f-126">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="f812f-126">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]