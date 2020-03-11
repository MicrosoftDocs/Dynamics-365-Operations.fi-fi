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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040960"
---
# <span data-ttu-id="73e1f-103"><a name="PADLEFT">PADLEFT ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="73e1f-103"><a name="PADLEFT">PADLEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73e1f-104">`PADLEFT`-funktio palauttaa määritetyn pituisen *merkkijonon* arvon, jossa määritetyn merkkijonon alkua on täydennetty määritetyillä merkeillä.</span><span class="sxs-lookup"><span data-stu-id="73e1f-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="73e1f-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="73e1f-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="73e1f-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="73e1f-106">Arguments</span></span>

<span data-ttu-id="73e1f-107">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="73e1f-107">`text`: *String*</span></span>

<span data-ttu-id="73e1f-108">*Merkkijono*-arvo, joka esittelee alkuperäisen tekstin.</span><span class="sxs-lookup"><span data-stu-id="73e1f-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="73e1f-109">`length`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="73e1f-109">`length`: *Integer*</span></span>

<span data-ttu-id="73e1f-110">*Kokonaislukuarvo*, joka vastaa täydennetyn merkkijonon lopullista merkkien määrää.</span><span class="sxs-lookup"><span data-stu-id="73e1f-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="73e1f-111">`padding chars`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="73e1f-111">`padding chars`: *String*</span></span>

<span data-ttu-id="73e1f-112">Täydennyskäyttöön käytettävät merkit.</span><span class="sxs-lookup"><span data-stu-id="73e1f-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="73e1f-113">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="73e1f-113">Return values</span></span>

<span data-ttu-id="73e1f-114">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="73e1f-114">*String*</span></span>

<span data-ttu-id="73e1f-115">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="73e1f-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="73e1f-116">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="73e1f-116">Example</span></span>

<span data-ttu-id="73e1f-117">`PADLEFT ("1234", 10, "`&nbsp;`")` palauttaa tekstimerkkijonon **&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234**</span><span class="sxs-lookup"><span data-stu-id="73e1f-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73e1f-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="73e1f-118">Additional resources</span></span>

[<span data-ttu-id="73e1f-119">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="73e1f-119">Text functions</span></span>](er-functions-category-text.md)
