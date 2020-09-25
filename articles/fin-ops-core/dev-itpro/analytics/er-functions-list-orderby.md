---
title: ORDERBY ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ORDERBY-funktiota käytetään.
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
ms.openlocfilehash: 6ff280d66fd2c418984f2d7fd31a32609932e89c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745006"
---
# <a name="orderby-er-function"></a><span data-ttu-id="3c9a6-103">ORDERBY ER-funktio</span><span class="sxs-lookup"><span data-stu-id="3c9a6-103">ORDERBY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c9a6-104">`ORDERBY`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on lajiteltu määritettyjen argumenttien mukaan.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-104">The `ORDERBY` function returns the specified list as a *Record list* value after it has been sorted according to the specified arguments.</span></span> <span data-ttu-id="3c9a6-105">Nämä argumentit voivaan määrittää lausekkeina.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-105">These arguments can be defined as expressions.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c9a6-106">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="3c9a6-106">Syntax</span></span>

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a><span data-ttu-id="3c9a6-107">Argumentit</span><span class="sxs-lookup"><span data-stu-id="3c9a6-107">Arguments</span></span>

<span data-ttu-id="3c9a6-108">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="3c9a6-108">`list`: *Record list*</span></span>

<span data-ttu-id="3c9a6-109">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="3c9a6-110">`expression 1`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="3c9a6-110">`expression 1`: *Field*</span></span>

<span data-ttu-id="3c9a6-111">Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-111">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="3c9a6-112">Viitatun kentän on oltava primitiivisen tietotyypin kenttä.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-112">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="3c9a6-113">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-113">This argument is required.</span></span>

<span data-ttu-id="3c9a6-114">`expression N`: *Kenttä*</span><span class="sxs-lookup"><span data-stu-id="3c9a6-114">`expression N`: *Field*</span></span>

<span data-ttu-id="3c9a6-115">Tietolähteen kentän kelvollinen polku, johon kutsutun funktion `list`-argumentti viittaa.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-115">The valid path of a field of the data source that is referenced by the `list` argument of the called function.</span></span> <span data-ttu-id="3c9a6-116">Viitatun kentän on oltava primitiivisen tietotyypin kenttä.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-116">The referenced field must be a field of the primitive data type.</span></span> <span data-ttu-id="3c9a6-117">Nämä lisäargumentit ovat valinnaisia.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-117">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3c9a6-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="3c9a6-118">Return values</span></span>

<span data-ttu-id="3c9a6-119">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="3c9a6-119">*Record list*</span></span>

<span data-ttu-id="3c9a6-120">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-120">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="3c9a6-121">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="3c9a6-121">Example 1</span></span>

<span data-ttu-id="3c9a6-122">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( ORDERBY( DS, DS. Value)).Value` palauttaa tekstiarvon **A**.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-122">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( ORDERBY( DS, DS. Value)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="3c9a6-123">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="3c9a6-123">Example 2</span></span>

<span data-ttu-id="3c9a6-124">Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `ORDERBY (Vendors, Vendors.'name()')` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan nousevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="3c9a6-124">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `ORDERBY (Vendors, Vendors.'name()')` returns a list of vendors that is sorted by name in ascending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c9a6-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3c9a6-125">Additional resources</span></span>

[<span data-ttu-id="3c9a6-126">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="3c9a6-126">List functions</span></span>](er-functions-category-list.md)
