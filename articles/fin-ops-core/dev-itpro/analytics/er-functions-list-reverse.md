---
title: REVERSE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REVERSE-funktiota käytetään.
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
ms.openlocfilehash: ab953136b7500665bdb13e6ff585e3b76896c9ee
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744982"
---
# <a name="reverse-er-function"></a><span data-ttu-id="096cf-103">REVERSE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="096cf-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="096cf-104">`REVERSE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi käänteisen lajittelujärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="096cf-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="096cf-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="096cf-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="096cf-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="096cf-106">Arguments</span></span>

<span data-ttu-id="096cf-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="096cf-107">`list`: *Record list*</span></span>

<span data-ttu-id="096cf-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="096cf-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="096cf-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="096cf-109">Return values</span></span>

<span data-ttu-id="096cf-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="096cf-110">*Record list*</span></span>

<span data-ttu-id="096cf-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="096cf-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="096cf-112">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="096cf-112">Example 1</span></span>

<span data-ttu-id="096cf-113">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` palauttaa tekstiarvon **C**.</span><span class="sxs-lookup"><span data-stu-id="096cf-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="096cf-114">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="096cf-114">Example 2</span></span>

<span data-ttu-id="096cf-115">Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="096cf-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="096cf-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="096cf-116">Additional resources</span></span>

[<span data-ttu-id="096cf-117">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="096cf-117">List functions</span></span>](er-functions-category-list.md)
