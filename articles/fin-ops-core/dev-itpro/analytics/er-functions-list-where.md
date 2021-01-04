---
title: WHERE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) WHERE-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1cc47c5001cf456b1fc600b326f826ea3b8b43ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687047"
---
# <a name="where-er-function"></a><span data-ttu-id="7e22e-103">WHERE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="7e22e-103">WHERE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e22e-104">`WHERE`-funktio palauttaa määritetyn luettelon *Tietueluettelon* arvoksi sen jälkeen, kun se on suodatettu määritettyjen ehtojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7e22e-104">The `WHERE` function returns the specified list as a *Record list* value after it has been filtered according to the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e22e-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="7e22e-105">Syntax</span></span>

```vb
WHERE (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="7e22e-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="7e22e-106">Arguments</span></span>

<span data-ttu-id="7e22e-107">`list`: *Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="7e22e-107">`list`: *Record list*</span></span>

<span data-ttu-id="7e22e-108">*Tietueluettelo*-tietotyypin tietolähteen kelvollinen polku.</span><span class="sxs-lookup"><span data-stu-id="7e22e-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="7e22e-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="7e22e-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="7e22e-110">Kelvollinen ehtolauseke, jota käytetään määritetyn luettelon tietueiden suodattamiseen.</span><span class="sxs-lookup"><span data-stu-id="7e22e-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="7e22e-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="7e22e-111">Return values</span></span>

<span data-ttu-id="7e22e-112">*Tietueluettelo*</span><span class="sxs-lookup"><span data-stu-id="7e22e-112">*Record list*</span></span>

<span data-ttu-id="7e22e-113">Tuloksena oleva tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="7e22e-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7e22e-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="7e22e-114">Usage notes</span></span>

<span data-ttu-id="7e22e-115">Funktio eroaa [FILTER](er-functions-list-filter.md)-funktiosta, koska määritettyä ehtoa käytetään muistissa oleviin kaikkiin *Tietueluettelo*-tyypin elektronisen raportoinnin (ER) tietolähteisiin.</span><span class="sxs-lookup"><span data-stu-id="7e22e-115">This function differs from the [FILTER](er-functions-list-filter.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="7e22e-116">Jos toiminnolle määritetyt argumentit (`list` ja `condition`) sallivat tämän pyynnön kääntyä suoraan SQL-puheluun, suunnitteluaikaan tulee varoitusviesti.</span><span class="sxs-lookup"><span data-stu-id="7e22e-116">If the arguments that are configured for this function (`list` and `condition`) allow this request to be translated to the direct SQL call, a warning message is thrown at design time.</span></span> <span data-ttu-id="7e22e-117">Tämä sanoma ilmoittaa käyttäjälle, että suorituskykyä voidaan parantaa, jos [FILTER](er-functions-list-filter.md)-toimintoa käytetään `WHERE`-funktion asemesta.</span><span class="sxs-lookup"><span data-stu-id="7e22e-117">This message informs the user that performance might be improved if the [FILTER](er-functions-list-filter.md) function is used instead of `WHERE`.</span></span>

## <a name="example-1"></a><span data-ttu-id="7e22e-118">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="7e22e-118">Example 1</span></span>

<span data-ttu-id="7e22e-119">Jos **Toimittaja** on määritetty VendTable-tauluun viittaavaksi ER-tietolähteeksi, lauseke `WHERE (Vendors, Vendors.VendGroup = "40")` palauttaa luettelon toimittajista, jotka kuuluvat vain toimittajaryhmään 40.</span><span class="sxs-lookup"><span data-stu-id="7e22e-119">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `WHERE (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="7e22e-120">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="7e22e-120">Example 2</span></span>

<span data-ttu-id="7e22e-121">Jos syötät tietolähteen **DS** *laskettuun kenttätyyppiin* ja se sisältää lausekkeen `SPLIT ("A|B|C", "|")`, lauseke `WHERE( DS, DS.Value = "B")` palauttaa ainoastaan yhden tietueen luettelon, joka sisältää tekstiarvon **B** **Arvo**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="7e22e-121">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `WHERE( DS, DS.Value = "B")` returns a list of only one record that contains the text **"B"** in the **Value** field.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e22e-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7e22e-122">Additional resources</span></span>

[<span data-ttu-id="7e22e-123">Luettelotoiminnot</span><span class="sxs-lookup"><span data-stu-id="7e22e-123">List functions</span></span>](er-functions-category-list.md)
