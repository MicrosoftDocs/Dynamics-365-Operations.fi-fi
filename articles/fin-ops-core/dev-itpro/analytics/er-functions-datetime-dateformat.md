---
title: DATEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEFORMAT-funktiota käytetään.
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
ms.openlocfilehash: 0a9580b0ab9e472796375f498059ec0864a919ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563651"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="4fca9-103">DATEFORMAT ER-funktio</span><span class="sxs-lookup"><span data-stu-id="4fca9-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fca9-104">`DATEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="4fca9-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="4fca9-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="4fca9-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4fca9-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="4fca9-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4fca9-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="4fca9-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4fca9-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="4fca9-108">Arguments</span></span>

<span data-ttu-id="4fca9-109">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="4fca9-109">`date`: *Date*</span></span>

<span data-ttu-id="4fca9-110">Päivämääräarvo, joka vastaa muokattavaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="4fca9-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="4fca9-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4fca9-111">`format`: *String*</span></span>

<span data-ttu-id="4fca9-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="4fca9-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="4fca9-113">Muodon merkkijono ottaa kirjainkoon huomioon, kun käytössä joko vakiomuoto tai mukautettu muoto.</span><span class="sxs-lookup"><span data-stu-id="4fca9-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="4fca9-114">Esimerkiksi [vakiomuotoinen](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) d-määrite palauttaa päivämäärän käyttämällä lyhyt päivämäärämalli, kun taas vakiomuotoinen D-määrite palauttaa pitkää päivämäärämallia käyttävän päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="4fca9-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="4fca9-115">Lisäksi [mukautetun](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) muodon M-määrite palauttaa kuukaudet 1–12, kun taas mukautetun muodon m-määrite palauttaa minuutit 0–59.</span><span class="sxs-lookup"><span data-stu-id="4fca9-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="4fca9-116">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4fca9-116">`culture`: *String*</span></span>

<span data-ttu-id="4fca9-117">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="4fca9-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="4fca9-118">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="4fca9-118">Return values</span></span>

<span data-ttu-id="4fca9-119">*Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="4fca9-119">*String*</span></span>

<span data-ttu-id="4fca9-120">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="4fca9-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4fca9-121">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="4fca9-121">Usage notes</span></span>

<span data-ttu-id="4fca9-122">Jos kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="4fca9-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="4fca9-123">Jos `DATEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="4fca9-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="4fca9-124">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="4fca9-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="4fca9-125">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="4fca9-125">Example 1</span></span>

<span data-ttu-id="4fca9-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4fca9-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="4fca9-127">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="4fca9-127">Example 2</span></span>

<span data-ttu-id="4fca9-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="4fca9-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fca9-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="4fca9-129">Additional resources</span></span>

[<span data-ttu-id="4fca9-130">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="4fca9-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]