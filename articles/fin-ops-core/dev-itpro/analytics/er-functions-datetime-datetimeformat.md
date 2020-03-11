---
title: DATETIMEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEFORMAT-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070710"
---
# <span data-ttu-id="83c48-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="83c48-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83c48-104">`DATETIMEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="83c48-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="83c48-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="83c48-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="83c48-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="83c48-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="83c48-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="83c48-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="83c48-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="83c48-108">Arguments</span></span>

<span data-ttu-id="83c48-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="83c48-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="83c48-110">Päivämäärä-/aika-arvo, joka vastaa muokattavaa päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="83c48-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="83c48-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="83c48-111">`format`: *String*</span></span>

<span data-ttu-id="83c48-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="83c48-112">The format of the output string.</span></span>

<span data-ttu-id="83c48-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="83c48-113">`culture`: *String*</span></span>

<span data-ttu-id="83c48-114">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="83c48-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="83c48-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="83c48-115">Return values</span></span>

<span data-ttu-id="83c48-116">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="83c48-116">*String*</span></span>

<span data-ttu-id="83c48-117">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="83c48-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="83c48-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="83c48-118">Usage notes</span></span>

<span data-ttu-id="83c48-119">Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="83c48-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="83c48-120">Jos `DATETIMEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="83c48-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="83c48-121">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="83c48-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="83c48-122">Kun `DATETIMEFORMAT`-funktio muuntaa tietyn päivämäärä- ja aika-arvon, se harkitsee sen sovelluksen käyttäjän aikavyöhykeasetusta, joka suorittaa ER-muotoa ja jota funktiota kutsutaan järjestelmän kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="83c48-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="83c48-123">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="83c48-123">Example 1</span></span>

<span data-ttu-id="83c48-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärä-/aika-arvon 24. joulukuuta 2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="83c48-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="83c48-125">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="83c48-125">Example 2</span></span>

<span data-ttu-id="83c48-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="83c48-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="83c48-127">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="83c48-127">Example 3</span></span>

<span data-ttu-id="83c48-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` palauttaa merkkijonon arvon **2019-11-12T 08:00:00.0000000-08:00**, kun sitä kutsutaan prosessin aikana, jonka on käynnistänyt sovelluskäyttäjä, jolla on aikavyöhyke arvo **(GMT-08:00) Tyynenmeren normaaliaika (USA & Kanada)** **kieli ja maa/alue-asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="83c48-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="83c48-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="83c48-129">Additional resources</span></span>

[<span data-ttu-id="83c48-130">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="83c48-130">Date and time functions</span></span>](er-functions-category-datetime.md)
