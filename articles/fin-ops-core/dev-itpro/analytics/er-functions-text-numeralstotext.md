---
title: NUMERALSTOTEXT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) NUMERALSTOTEXT-funktiota käytetään.
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
ms.openlocfilehash: a820c894ee4d28f87588c475c982bd6447676740
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744380"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="2542c-103">NUMERALSTOTEXT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="2542c-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2542c-104">`NUMERALSTOTEXT`-funktio palauttaa määritetyn numeron *Merkkijono*-arvona sen jälkeen, kun se on kirjoitettu (muunnetaan tekstimerkkijonoiksi) määritetyllä kielellä.</span><span class="sxs-lookup"><span data-stu-id="2542c-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="2542c-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="2542c-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="2542c-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="2542c-106">Arguments</span></span>

<span data-ttu-id="2542c-107">`number`: *Kokonaisluku* tai *Todellinen*</span><span class="sxs-lookup"><span data-stu-id="2542c-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="2542c-108">Numeerinen arvo, joka määrittää lukumäärän, joka täytyy tavata.</span><span class="sxs-lookup"><span data-stu-id="2542c-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="2542c-109">`language`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2542c-109">`language`: *String*</span></span>

<span data-ttu-id="2542c-110">*Merkkijono*-arvo, joka esittelee kielikoodin.</span><span class="sxs-lookup"><span data-stu-id="2542c-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="2542c-111">`currency`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2542c-111">`currency`: *String*</span></span>

<span data-ttu-id="2542c-112">*Merkkijono*-arvo, joka esittelee valuuttakoodin.</span><span class="sxs-lookup"><span data-stu-id="2542c-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="2542c-113">`print currency name flag`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="2542c-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="2542c-114">*Totuusarvo*, joka ilmaisee, onko kirjoitettuun tekstin lisättävä valuutan nimi.</span><span class="sxs-lookup"><span data-stu-id="2542c-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="2542c-115">`decimal points`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="2542c-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="2542c-116">*Kokonaislukuarvo*, joka ilmaisee, kuinka monta desimaalia kirjoitetussa tekstissä pitäisi olla.</span><span class="sxs-lookup"><span data-stu-id="2542c-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="2542c-117">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="2542c-117">Return values</span></span>

<span data-ttu-id="2542c-118">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="2542c-118">*String*</span></span>

<span data-ttu-id="2542c-119">Tulokseksi saatava tekstiarvo.</span><span class="sxs-lookup"><span data-stu-id="2542c-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2542c-120">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="2542c-120">Usage notes</span></span>

<span data-ttu-id="2542c-121">Kielikoodi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="2542c-121">The language code is optional.</span></span> <span data-ttu-id="2542c-122">Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin kielikoodia käytetään.</span><span class="sxs-lookup"><span data-stu-id="2542c-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="2542c-123">Oletuskielikoodi on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="2542c-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="2542c-124">Käynnissä olevan kontekstin kielikoodi määritetään käynnissä olevan sähköisen raportoinnin (ER) **Kansiossa** tai **Tiedosto**-elementissä.</span><span class="sxs-lookup"><span data-stu-id="2542c-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="2542c-125">Valuuttakoodi on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="2542c-125">The currency code is optional.</span></span> <span data-ttu-id="2542c-126">Jos se on määritetty tyhjänä merkkijonona, suorituskontekstin yrityksen valuuttaa käytetään.</span><span class="sxs-lookup"><span data-stu-id="2542c-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="2542c-127">`print currency name flag` ja `decimal points`-argumentit analysoidaan vain seuraaville kielikoodeille: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ja **RU**.</span><span class="sxs-lookup"><span data-stu-id="2542c-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="2542c-128">Lisäksi `print currency name flag`-argumentti analysoidaan vain niissä yrityksissä, joiden maa- tai alueyhteys tukee valuutan nimen taivutusta.</span><span class="sxs-lookup"><span data-stu-id="2542c-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="2542c-129">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="2542c-129">Example 1</span></span>

<span data-ttu-id="2542c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` palauttaa arvon **Tuhat kaksisataa kolmekymmentä neljä ja 56**.</span><span class="sxs-lookup"><span data-stu-id="2542c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2542c-131">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="2542c-131">Example 2</span></span>

<span data-ttu-id="2542c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)`-funktio palauttaa arvon **Sto dwadzieścia**.</span><span class="sxs-lookup"><span data-stu-id="2542c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="2542c-133">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="2542c-133">Example 3</span></span>

<span data-ttu-id="2542c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` palauttaa arvon **сто двадцать евро 21 евроцент**.</span><span class="sxs-lookup"><span data-stu-id="2542c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2542c-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2542c-135">Additional resources</span></span>

[<span data-ttu-id="2542c-136">Tekstitoiminnot</span><span class="sxs-lookup"><span data-stu-id="2542c-136">Text functions</span></span>](er-functions-category-text.md)
