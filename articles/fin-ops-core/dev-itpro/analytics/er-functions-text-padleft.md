---
title: PADLEFT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) PADLEFT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916772"
---
# <span data-ttu-id="06c4b-103"><a name="PADLEFT">PADLEFT ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="06c4b-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06c4b-104">`PADLEFT`-funktio palauttaa määritetyn pituisen *merkkijonon* arvon, jossa määritetyn merkkijonon alkua on täydennetty määritetyillä merkeillä.</span><span class="sxs-lookup"><span data-stu-id="06c4b-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c4b-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="06c4b-105">Syntax</span></span>

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="06c4b-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="06c4b-106">Arguments</span></span>

<span data-ttu-id="06c4b-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06c4b-107">`text`: *String*</span></span>

<span data-ttu-id="06c4b-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="06c4b-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="06c4b-109">`length`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="06c4b-109">`length`: *Integer*</span></span>

<span data-ttu-id="06c4b-110">*Kokonaislukuarvo*, joka vastaa täydennetyn merkkijonon lopullista merkkien määrää.</span><span class="sxs-lookup"><span data-stu-id="06c4b-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="06c4b-111">`padding chars`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06c4b-111">`padding chars`: *String*</span></span>

<span data-ttu-id="06c4b-112">Täydennyskäyttöön käytettävät merkit.</span><span class="sxs-lookup"><span data-stu-id="06c4b-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="06c4b-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="06c4b-113">Return values</span></span>

<span data-ttu-id="06c4b-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06c4b-114">*String*</span></span>

<span data-ttu-id="06c4b-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="06c4b-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="06c4b-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="06c4b-116">Example</span></span>

<span data-ttu-id="06c4b-117">`PADLEFT ("1234", 10, "`&nbsp;`")` palauttaa tekstimerkkijonon **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**</span><span class="sxs-lookup"><span data-stu-id="06c4b-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06c4b-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="06c4b-118">Additional resources</span></span>

[<span data-ttu-id="06c4b-119">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="06c4b-119">Text functions</span></span>](er-functions-category-text.md)
