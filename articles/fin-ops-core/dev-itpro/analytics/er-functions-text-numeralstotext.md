---
title: NUMERALSTOTEXT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMERALSTOTEXT-funktiota käytetään.
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746144"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="f7a11-103">NUMERALSTOTEXT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="f7a11-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7a11-104">`NUMERALSTOTEXT`-funktio palauttaa määritetyn numeron *Merkkijono*-arvona sen jälkeen, kun se on kirjoitettu (muunnetaan tekstimerkkijonoiksi) määritetyllä kielellä.</span><span class="sxs-lookup"><span data-stu-id="f7a11-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a11-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="f7a11-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="f7a11-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="f7a11-106">Arguments</span></span>

<span data-ttu-id="f7a11-107">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="f7a11-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="f7a11-108">Numeerinen arvo, joka määrittää lukumäärän, joka täytyy tavata.</span><span class="sxs-lookup"><span data-stu-id="f7a11-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="f7a11-109">`language`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f7a11-109">`language`: *String*</span></span>

<span data-ttu-id="f7a11-110">*Merkkijono*-arvo, joka esittelee kielikoodin.</span><span class="sxs-lookup"><span data-stu-id="f7a11-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="f7a11-111">`currency`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f7a11-111">`currency`: *String*</span></span>

<span data-ttu-id="f7a11-112">*Merkkijono*-arvo, joka esittelee valuuttakoodin.</span><span class="sxs-lookup"><span data-stu-id="f7a11-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="f7a11-113">`print currency name flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="f7a11-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="f7a11-114">*Totuusarvo*, joka ilmaisee, onko kirjoitettuun tekstin lisättävä valuutan nimi.</span><span class="sxs-lookup"><span data-stu-id="f7a11-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="f7a11-115">`decimal points`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="f7a11-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="f7a11-116">*Kokonaislukuarvo*, joka ilmaisee, kuinka monta desimaalia kirjoitetussa tekstissä pitäisi olla.</span><span class="sxs-lookup"><span data-stu-id="f7a11-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="f7a11-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="f7a11-117">Return values</span></span>

<span data-ttu-id="f7a11-118">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="f7a11-118">*String*</span></span>

<span data-ttu-id="f7a11-119">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="f7a11-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f7a11-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="f7a11-120">Usage notes</span></span>

<span data-ttu-id="f7a11-121">Kielikoodi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="f7a11-121">The language code is optional.</span></span> <span data-ttu-id="f7a11-122">Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin kielikoodia käytetään.</span><span class="sxs-lookup"><span data-stu-id="f7a11-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="f7a11-123">Oletuskielikoodi on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="f7a11-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="f7a11-124">Käynnissä olevan kontekstin kielikoodi määritetään käynnissä olevan sähköisen raportoinnin (ER) **Kansiossa** tai **Tiedosto**-elementissä.</span><span class="sxs-lookup"><span data-stu-id="f7a11-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="f7a11-125">Valuuttakoodi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="f7a11-125">The currency code is optional.</span></span> <span data-ttu-id="f7a11-126">Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin yrityksen valuuttaa käytetään.</span><span class="sxs-lookup"><span data-stu-id="f7a11-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="f7a11-127">`print currency name flag` ja `decimal points`-argumentit analysoidaan vain seuraaville kielikoodeille: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ja **RU**.</span><span class="sxs-lookup"><span data-stu-id="f7a11-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="f7a11-128">Lisäksi `print currency name flag`-argumentti analysoidaan vain niissä yrityksissä, joiden maa- tai alueyhteys tukee valuutan nimen taivutusta.</span><span class="sxs-lookup"><span data-stu-id="f7a11-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="f7a11-129">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="f7a11-129">Example 1</span></span>

<span data-ttu-id="f7a11-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` palauttaa arvon **Tuhat kaksisataa kolmekymmentä neljä ja 56**.</span><span class="sxs-lookup"><span data-stu-id="f7a11-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f7a11-131">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="f7a11-131">Example 2</span></span>

<span data-ttu-id="f7a11-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)`-funktio palauttaa arvon **Sto dwadzieścia**.</span><span class="sxs-lookup"><span data-stu-id="f7a11-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="f7a11-133">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="f7a11-133">Example 3</span></span>

<span data-ttu-id="f7a11-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` palauttaa arvon **сто двадцать евро 21 евроцент**.</span><span class="sxs-lookup"><span data-stu-id="f7a11-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f7a11-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f7a11-135">Additional resources</span></span>

[<span data-ttu-id="f7a11-136">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="f7a11-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]