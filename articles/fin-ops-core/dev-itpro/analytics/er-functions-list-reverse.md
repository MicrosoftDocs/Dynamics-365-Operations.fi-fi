---
title: REVERSE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) REVERSE-funktiota käytetään.
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
ms.openlocfilehash: 746a736c8797c1c1c5bd71d7d803be4212984595
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755201"
---
# <a name="reverse-er-function"></a><span data-ttu-id="a5307-103">REVERSE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="a5307-103">REVERSE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5307-104">`REVERSE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi käänteisen lajittelujärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="a5307-104">The `REVERSE` function returns the specified list as a *Record list* value in reversed sort order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5307-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="a5307-105">Syntax</span></span>

```vb
REVERSE (list)
```

## <a name="arguments"></a><span data-ttu-id="a5307-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="a5307-106">Arguments</span></span>

<span data-ttu-id="a5307-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a5307-107">`list`: *Record list*</span></span>

<span data-ttu-id="a5307-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="a5307-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="a5307-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="a5307-109">Return values</span></span>

<span data-ttu-id="a5307-110">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="a5307-110">*Record list*</span></span>

<span data-ttu-id="a5307-111">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="a5307-111">The resulting list of records.</span></span>

## <a name="example-1"></a><span data-ttu-id="a5307-112">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="a5307-112">Example 1</span></span>

<span data-ttu-id="a5307-113">Jos syötät *Lasketun kenttä*-tyypin **DS**-tietolähteen, ja se sisältää lausekkeen `SPLIT ("C|B|A", "|")`, lauseke `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` palauttaa tekstiarvon **C**.</span><span class="sxs-lookup"><span data-stu-id="a5307-113">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("C|B|A", "|")`, the expression `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` returns the text value **"C"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a5307-114">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="a5307-114">Example 2</span></span>

<span data-ttu-id="a5307-115">Jos **Toimittaja** on määritetty sähköisen raportoinnin (ER) tietolähteeksi, joka viittaa VendTable-tauluun, lauseke `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` palauttaa toimittajaluettelon, joka on lajiteltu nimen mukaan laskevassa järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="a5307-115">If **Vendor** is configured as an Electronic reporting (ER) data source that refers to the VendTable table, the expression `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` returns a list of vendors that is sorted by name in descending order.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5307-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a5307-116">Additional resources</span></span>

[<span data-ttu-id="a5307-117">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="a5307-117">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]