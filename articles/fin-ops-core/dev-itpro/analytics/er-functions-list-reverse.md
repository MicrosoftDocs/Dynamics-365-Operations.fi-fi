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
ms.openlocfilehash: a6134ae7eb1a8044cf906f2a8d02eb153522a6cf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041926"
---
# <span data-ttu-id="1caaa-103"><a name="REVERSE">REVERSE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="1caaa-103"><a name="REVERSE">REVERSE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1caaa-104">`REVERSE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi käänteisen lajittelujärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="1caaa-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1caaa-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="1caaa-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="1caaa-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="1caaa-106">Arguments</span></span>

<span data-ttu-id="1caaa-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="1caaa-107">`list`: *Record list*</span></span>

<span data-ttu-id="1caaa-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="1caaa-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="1caaa-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="1caaa-109">Return values</span></span>

<span data-ttu-id="1caaa-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="1caaa-110">*Record list*</span></span>

<span data-ttu-id="1caaa-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="1caaa-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="1caaa-112">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="1caaa-112">Example 1</span></span>

<span data-ttu-id="1caaa-113">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` palauttaa tekstiarvon **C**.</span><span class="sxs-lookup"><span data-stu-id="1caaa-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1caaa-114">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="1caaa-114">Example 2</span></span>

<span data-ttu-id="1caaa-115">Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="1caaa-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1caaa-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1caaa-116">Additional resources</span></span>

[<span data-ttu-id="1caaa-117">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="1caaa-117">List functions</span></span>](er-functions-category-list.md)
