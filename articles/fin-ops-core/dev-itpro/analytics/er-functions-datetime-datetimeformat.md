---
title: DATETIMEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEFORMAT-funktiota käytetään.
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891254"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="e0a72-103">DATETIMEFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="e0a72-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0a72-104">`DATETIMEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="e0a72-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="e0a72-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="e0a72-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e0a72-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="e0a72-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e0a72-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="e0a72-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e0a72-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="e0a72-108">Arguments</span></span>

<span data-ttu-id="e0a72-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="e0a72-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="e0a72-110">Päivämäärä-/aika-arvo, joka vastaa muokattavaa päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="e0a72-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="e0a72-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e0a72-111">`format`: *String*</span></span>

<span data-ttu-id="e0a72-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="e0a72-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="e0a72-113">Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto.</span><span class="sxs-lookup"><span data-stu-id="e0a72-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="e0a72-114">Esimerkiksi [vakiomuotoinen](/dotnet/standard/base-types/standard-date-and-time-format-strings) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="e0a72-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="e0a72-115">Lisäksi [mukautetun](/dotnet/standard/base-types/custom-date-and-time-format-strings) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.</span><span class="sxs-lookup"><span data-stu-id="e0a72-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="e0a72-116">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e0a72-116">`culture`: *String*</span></span>

<span data-ttu-id="e0a72-117">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="e0a72-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="e0a72-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="e0a72-118">Return values</span></span>

<span data-ttu-id="e0a72-119">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e0a72-119">*String*</span></span>

<span data-ttu-id="e0a72-120">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="e0a72-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e0a72-121">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="e0a72-121">Usage notes</span></span>

<span data-ttu-id="e0a72-122">Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="e0a72-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e0a72-123">Jos `DATETIMEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="e0a72-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e0a72-124">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="e0a72-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="e0a72-125">Kun `DATETIMEFORMAT`-funktio muuntaa tietyn päivämäärä- ja aika-arvon, se harkitsee sen sovelluksen käyttäjän aikavyöhykeasetusta, joka suorittaa ER-muotoa ja jota funktiota kutsutaan järjestelmän kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="e0a72-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="e0a72-126">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e0a72-126">Example 1</span></span>

<span data-ttu-id="e0a72-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärä-/aika-arvon 24. joulukuuta 2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e0a72-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e0a72-128">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e0a72-128">Example 2</span></span>

<span data-ttu-id="e0a72-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="e0a72-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="e0a72-130">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="e0a72-130">Example 3</span></span>

<span data-ttu-id="e0a72-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` palauttaa merkkijonon arvon **2019-11-12T 08:00:00.0000000-08:00**, kun funktiota kutsutaan prosessin aikana, jonka käynnistäneen sovelluskäyttäjän aikavyöhykkeen arvo on **(GMT-08:00) Tyynenmeren normaaliaika (USA ja Kanada)** **Kieli- ja alue-asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="e0a72-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0a72-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e0a72-132">Additional resources</span></span>

[<span data-ttu-id="e0a72-133">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="e0a72-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]