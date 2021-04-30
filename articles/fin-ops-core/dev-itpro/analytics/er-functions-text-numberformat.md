---
title: NUMBERFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERFORMAT-funktiota käytetään.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890380"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="98923-103">NUMBERFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="98923-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98923-104">`NUMBERFORMAT`-funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="98923-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="98923-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-numeric-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="98923-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="98923-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="98923-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="98923-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="98923-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="98923-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="98923-108">Arguments</span></span>

<span data-ttu-id="98923-109">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="98923-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="98923-110">Numeerinen arvo, joka määrittää muotoiltava lukumäärän.</span><span class="sxs-lookup"><span data-stu-id="98923-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="98923-111">`format` : *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="98923-111">`format` : *String*</span></span>

<span data-ttu-id="98923-112">*Merkkijono*-arvo, joka esittelee alkuperäisen muodon.</span><span class="sxs-lookup"><span data-stu-id="98923-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="98923-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="98923-113">`culture`: *String*</span></span>

<span data-ttu-id="98923-114">*Merkkijono*-arvo, joka edustaa muotoilussa käytettävää kulttuuria.</span><span class="sxs-lookup"><span data-stu-id="98923-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="98923-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="98923-115">Return values</span></span>

<span data-ttu-id="98923-116">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="98923-116">*String*</span></span>

<span data-ttu-id="98923-117">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="98923-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="98923-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="98923-118">Usage notes</span></span>

<span data-ttu-id="98923-119">Jos kulttuuria ei ole määritetty kutsuttujen funktioiden argumentiksi, sen konteksti, jossa tämä funktio suoritetaan, määrittää lukujen muotoilussa käytettävän kulttuurin.</span><span class="sxs-lookup"><span data-stu-id="98923-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="98923-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="98923-120">Example 1</span></span>

<span data-ttu-id="98923-121">Jos maa-asetukset ovat **EN-US**, `NUMBERFORMAT (0.45, "p")` palauttaa arvon **45.00 %** ja `NUMBERFORMAT (10.45, "#")` palauttaa arvon **10**.</span><span class="sxs-lookup"><span data-stu-id="98923-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="98923-122">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="98923-122">Example 2</span></span>

<span data-ttu-id="98923-123">`NUMBERFORMAT (10/3, "F2", "de")`-funktio palauttaa arvon **3,33**, kun `NUMBERFORMAT (10/3, "F2", "en-us")` palauttaa arvon **3.33**.</span><span class="sxs-lookup"><span data-stu-id="98923-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="98923-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="98923-124">Additional resources</span></span>

[<span data-ttu-id="98923-125">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="98923-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]