---
title: DATEFORMAT ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATEFORMAT-funktiota käytetään.
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917577"
---
# <span data-ttu-id="1e5cf-103"><a name="DATEFORMAT">DATEFORMAT ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="1e5cf-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e5cf-104">`DATEFORMAT`-funktio palauttaa *Merkkijono*-arvon, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="1e5cf-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="1e5cf-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="1e5cf-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1e5cf-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="1e5cf-106">Syntax 1</span></span>

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="1e5cf-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="1e5cf-107">Syntax 2</span></span>

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="1e5cf-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="1e5cf-108">Arguments</span></span>

<span data-ttu-id="1e5cf-109">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="1e5cf-109">`date`: *Date*</span></span>

<span data-ttu-id="1e5cf-110">Päivämääräarvo, joka vastaa muokattavaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="1e5cf-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="1e5cf-111">`format`: *String*</span></span>

<span data-ttu-id="1e5cf-112">Tulostusmerkkijonon muoto</span><span class="sxs-lookup"><span data-stu-id="1e5cf-112">The format of the output string.</span></span>

<span data-ttu-id="1e5cf-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="1e5cf-113">`culture`: *String*</span></span>

<span data-ttu-id="1e5cf-114">Muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e5cf-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="1e5cf-115">Return values</span></span>

<span data-ttu-id="1e5cf-116">*merkkijono*</span><span class="sxs-lookup"><span data-stu-id="1e5cf-116">*String*</span></span>

<span data-ttu-id="1e5cf-117">Tuloksena oleva merkkijonoarvo.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1e5cf-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="1e5cf-118">Usage notes</span></span>

<span data-ttu-id="1e5cf-119">Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="1e5cf-120">Jos `DATEFORMAT`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="1e5cf-121">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="1e5cf-122">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="1e5cf-122">Example 1</span></span>

<span data-ttu-id="1e5cf-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` palauttaa nykyisen sovelluspalvelimen päivämäärän 24. joulukuuta 2015 merkkirivinä **24-12-2015** määritetyn mukautetun muodon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="1e5cf-124">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="1e5cf-124">Example 2</span></span>

<span data-ttu-id="1e5cf-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` palauttaa nykyisen sovellusistunnon päivämäärän, 24. joulukuuta 2015, merkkijonona **"24-12-2015"**, joka perustuu valittuun Saksan kulttuuriin ja määritettyyn muotoon.</span><span class="sxs-lookup"><span data-stu-id="1e5cf-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e5cf-126">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="1e5cf-126">Additional resources</span></span>

[<span data-ttu-id="1e5cf-127">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="1e5cf-127">Date and time functions</span></span>](er-functions-category-datetime.md)
