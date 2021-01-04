---
title: CHAR ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CHAR-funktiota käytetään.
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
ms.openlocfilehash: a9f0f70c250592bf74b1a1df823e66803e853a64
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682988"
---
# <a name="char-er-function"></a><span data-ttu-id="8652f-103">CHAR ER -funktio</span><span class="sxs-lookup"><span data-stu-id="8652f-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8652f-104">`CHAR`-funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla.</span><span class="sxs-lookup"><span data-stu-id="8652f-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8652f-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8652f-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="8652f-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8652f-106">Arguments</span></span>

<span data-ttu-id="8652f-107">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="8652f-107">`number`: *Integer*</span></span>

<span data-ttu-id="8652f-108">Numero, joka vastaa odotettua yksittäistä merkkiä.</span><span class="sxs-lookup"><span data-stu-id="8652f-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="8652f-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8652f-109">Return values</span></span>

<span data-ttu-id="8652f-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="8652f-110">*String*</span></span>

<span data-ttu-id="8652f-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="8652f-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8652f-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="8652f-112">Usage notes</span></span>

<span data-ttu-id="8652f-113">Tämän funktion palauttama merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason **FILE**-muotoisessa elementissä.</span><span class="sxs-lookup"><span data-stu-id="8652f-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="8652f-114">Luettelo tuetuista koodauksista on kohdassa [Koodausluokka](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="8652f-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="8652f-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8652f-115">Example</span></span>

<span data-ttu-id="8652f-116">`CHAR (255)` palauttaa arvon **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="8652f-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8652f-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8652f-117">Additional resources</span></span>

[<span data-ttu-id="8652f-118">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="8652f-118">Text functions</span></span>](er-functions-category-text.md)
