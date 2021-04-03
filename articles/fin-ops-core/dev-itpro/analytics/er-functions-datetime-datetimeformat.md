---
title: DATETIMEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEFORMAT-funktiota käytetään.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563627"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="aef45-103">DATETIMEFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="aef45-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aef45-104">`DATETIMEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="aef45-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="aef45-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="aef45-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="aef45-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="aef45-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="aef45-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="aef45-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="aef45-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="aef45-108">Arguments</span></span>

<span data-ttu-id="aef45-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="aef45-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="aef45-110">Päivämäärä-/aika-arvo, joka vastaa muokattavaa päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="aef45-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="aef45-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="aef45-111">`format`: *String*</span></span>

<span data-ttu-id="aef45-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="aef45-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="aef45-113">Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto.</span><span class="sxs-lookup"><span data-stu-id="aef45-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="aef45-114">Esimerkiksi [vakiomuotoinen](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="aef45-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="aef45-115">Lisäksi [mukautetun](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.</span><span class="sxs-lookup"><span data-stu-id="aef45-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="aef45-116">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="aef45-116">`culture`: *String*</span></span>

<span data-ttu-id="aef45-117">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="aef45-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="aef45-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="aef45-118">Return values</span></span>

<span data-ttu-id="aef45-119">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="aef45-119">*String*</span></span>

<span data-ttu-id="aef45-120">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="aef45-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aef45-121">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="aef45-121">Usage notes</span></span>

<span data-ttu-id="aef45-122">Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="aef45-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="aef45-123">Jos `DATETIMEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="aef45-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="aef45-124">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="aef45-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="aef45-125">Kun `DATETIMEFORMAT`-funktio muuntaa tietyn päivämäärä- ja aika-arvon, se harkitsee sen sovelluksen käyttäjän aikavyöhykeasetusta, joka suorittaa ER-muotoa ja jota funktiota kutsutaan järjestelmän kontekstissa.</span><span class="sxs-lookup"><span data-stu-id="aef45-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="aef45-126">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="aef45-126">Example 1</span></span>

<span data-ttu-id="aef45-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärä-/aika-arvon 24. joulukuuta 2015 muodossa **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="aef45-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="aef45-128">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="aef45-128">Example 2</span></span>

<span data-ttu-id="aef45-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärä-/aika-arvon, 24. joulukuuta 2015, merkkijonona **"24.12.2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="aef45-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="aef45-130">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="aef45-130">Example 3</span></span>

<span data-ttu-id="aef45-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` palauttaa merkkijonon arvon **2019-11-12T 08:00:00.0000000-08:00**, kun funktiota kutsutaan prosessin aikana, jonka käynnistäneen sovelluskäyttäjän aikavyöhykkeen arvo on **(GMT-08:00) Tyynenmeren normaaliaika (USA ja Kanada)** **Kieli- ja alue-asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="aef45-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aef45-132">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="aef45-132">Additional resources</span></span>

[<span data-ttu-id="aef45-133">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="aef45-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]