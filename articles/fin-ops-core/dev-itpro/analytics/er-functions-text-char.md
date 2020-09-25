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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744958"
---
# <a name="char-er-function"></a><span data-ttu-id="08dd0-103">CHAR ER -funktio</span><span class="sxs-lookup"><span data-stu-id="08dd0-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08dd0-104">`CHAR`-funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla.</span><span class="sxs-lookup"><span data-stu-id="08dd0-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="08dd0-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="08dd0-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="08dd0-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="08dd0-106">Arguments</span></span>

<span data-ttu-id="08dd0-107">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="08dd0-107">`number`: *Integer*</span></span>

<span data-ttu-id="08dd0-108">Numero, joka vastaa odotettua yksittäistä merkkiä.</span><span class="sxs-lookup"><span data-stu-id="08dd0-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="08dd0-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="08dd0-109">Return values</span></span>

<span data-ttu-id="08dd0-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="08dd0-110">*String*</span></span>

<span data-ttu-id="08dd0-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="08dd0-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="08dd0-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="08dd0-112">Usage notes</span></span>

<span data-ttu-id="08dd0-113">Tämän funktion palauttama merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason **FILE**-muotoisessa elementissä.</span><span class="sxs-lookup"><span data-stu-id="08dd0-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="08dd0-114">Luettelo tuetuista koodauksista on kohdassa [Koodausluokka](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="08dd0-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="08dd0-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="08dd0-115">Example</span></span>

<span data-ttu-id="08dd0-116">`CHAR (255)` palauttaa arvon **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="08dd0-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08dd0-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="08dd0-117">Additional resources</span></span>

[<span data-ttu-id="08dd0-118">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="08dd0-118">Text functions</span></span>](er-functions-category-text.md)
