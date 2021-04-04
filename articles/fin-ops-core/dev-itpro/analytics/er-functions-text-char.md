---
title: CHAR ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CHAR-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563195"
---
# <a name="char-er-function"></a><span data-ttu-id="c2b86-103">CHAR ER -funktio</span><span class="sxs-lookup"><span data-stu-id="c2b86-103">CHAR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2b86-104">`CHAR`-funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla.</span><span class="sxs-lookup"><span data-stu-id="c2b86-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b86-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="c2b86-105">Syntax</span></span>

```vb
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="c2b86-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="c2b86-106">Arguments</span></span>

<span data-ttu-id="c2b86-107">`number`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="c2b86-107">`number`: *Integer*</span></span>

<span data-ttu-id="c2b86-108">Numero, joka vastaa odotettua yksittäistä merkkiä.</span><span class="sxs-lookup"><span data-stu-id="c2b86-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="c2b86-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="c2b86-109">Return values</span></span>

<span data-ttu-id="c2b86-110">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="c2b86-110">*String*</span></span>

<span data-ttu-id="c2b86-111">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="c2b86-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c2b86-112">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="c2b86-112">Usage notes</span></span>

<span data-ttu-id="c2b86-113">Tämän funktion palauttama merkkijono määräytyy koodauksen mukaan, joka on valittu ylemmän tason **FILE**-muotoisessa elementissä.</span><span class="sxs-lookup"><span data-stu-id="c2b86-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="c2b86-114">Luettelo tuetuista koodauksista on kohdassa [Koodausluokka](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="c2b86-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="c2b86-115">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="c2b86-115">Example</span></span>

<span data-ttu-id="c2b86-116">`CHAR (255)` palauttaa arvon **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="c2b86-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2b86-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c2b86-117">Additional resources</span></span>

[<span data-ttu-id="c2b86-118">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="c2b86-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]