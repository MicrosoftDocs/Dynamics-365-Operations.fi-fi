---
title: NUMBERFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMBERFORMAT-funktiota käytetään.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680263"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="06fea-103">NUMBERFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="06fea-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06fea-104">`NUMBERFORMAT`-funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="06fea-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="06fea-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="06fea-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="06fea-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="06fea-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="06fea-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="06fea-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="06fea-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="06fea-108">Arguments</span></span>

<span data-ttu-id="06fea-109">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="06fea-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="06fea-110">Numeerinen arvo, joka määrittää muotoiltava lukumäärän.</span><span class="sxs-lookup"><span data-stu-id="06fea-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="06fea-111">`format` : *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06fea-111">`format` : *String*</span></span>

<span data-ttu-id="06fea-112">*Merkkijono*-arvo, joka esittelee alkuperäisen muodon.</span><span class="sxs-lookup"><span data-stu-id="06fea-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="06fea-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06fea-113">`culture`: *String*</span></span>

<span data-ttu-id="06fea-114">*Merkkijono*-arvo, joka edustaa muotoilussa käytettävää kulttuuria.</span><span class="sxs-lookup"><span data-stu-id="06fea-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="06fea-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="06fea-115">Return values</span></span>

<span data-ttu-id="06fea-116">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="06fea-116">*String*</span></span>

<span data-ttu-id="06fea-117">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="06fea-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="06fea-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="06fea-118">Usage notes</span></span>

<span data-ttu-id="06fea-119">Jos kulttuuria ei ole määritetty kutsuttujen funktioiden argumentiksi, sen konteksti, jossa tämä funktio suoritetaan, määrittää lukujen muotoilussa käytettävän kulttuurin.</span><span class="sxs-lookup"><span data-stu-id="06fea-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="06fea-120">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="06fea-120">Example 1</span></span>

<span data-ttu-id="06fea-121">Jos maa-asetukset ovat **EN-US**, `NUMBERFORMAT (0.45, "p")` palauttaa arvon **45.00 %** ja `NUMBERFORMAT (10.45, "#")` palauttaa arvon **10**.</span><span class="sxs-lookup"><span data-stu-id="06fea-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="06fea-122">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="06fea-122">Example 2</span></span>

<span data-ttu-id="06fea-123">`NUMBERFORMAT (10/3, "F2", "de")`-funktio palauttaa arvon **3,33**, kun `NUMBERFORMAT (10/3, "F2", "en-us")` palauttaa arvon **3.33**.</span><span class="sxs-lookup"><span data-stu-id="06fea-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06fea-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="06fea-124">Additional resources</span></span>

[<span data-ttu-id="06fea-125">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="06fea-125">Text functions</span></span>](er-functions-category-text.md)
