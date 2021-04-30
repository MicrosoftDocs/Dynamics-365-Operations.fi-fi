---
title: DATEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEFORMAT-funktiota käytetään.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 1b3a0a2608328b233004034f7ab2ccfa833c17e3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890907"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="26547-103">DATEFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="26547-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26547-104">`DATEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="26547-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="26547-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="26547-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="26547-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="26547-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="26547-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="26547-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="26547-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="26547-108">Arguments</span></span>

<span data-ttu-id="26547-109">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="26547-109">`date`: *Date*</span></span>

<span data-ttu-id="26547-110">Päivämääräarvo, joka vastaa muokattavaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="26547-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="26547-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="26547-111">`format`: *String*</span></span>

<span data-ttu-id="26547-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="26547-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="26547-113">Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto.</span><span class="sxs-lookup"><span data-stu-id="26547-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="26547-114">Esimerkiksi [vakiomuotoinen](/dotnet/standard/base-types/standard-date-and-time-format-strings) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="26547-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="26547-115">Lisäksi [mukautetun](/dotnet/standard/base-types/custom-date-and-time-format-strings) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.</span><span class="sxs-lookup"><span data-stu-id="26547-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="26547-116">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="26547-116">`culture`: *String*</span></span>

<span data-ttu-id="26547-117">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="26547-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="26547-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="26547-118">Return values</span></span>

<span data-ttu-id="26547-119">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="26547-119">*String*</span></span>

<span data-ttu-id="26547-120">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="26547-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="26547-121">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="26547-121">Usage notes</span></span>

<span data-ttu-id="26547-122">Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="26547-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="26547-123">Jos `DATEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="26547-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="26547-124">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="26547-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="26547-125">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="26547-125">Example 1</span></span>

<span data-ttu-id="26547-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="26547-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="26547-127">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="26547-127">Example 2</span></span>

<span data-ttu-id="26547-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="26547-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26547-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="26547-129">Additional resources</span></span>

[<span data-ttu-id="26547-130">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="26547-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]