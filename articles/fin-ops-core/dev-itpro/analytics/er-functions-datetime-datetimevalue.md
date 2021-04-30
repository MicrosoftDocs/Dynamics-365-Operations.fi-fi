---
title: DATETIMEVALUE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEVALUE-funktiota käytetään.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891278"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="e1773-103">DATETIMEVALUE ER-funktio</span><span class="sxs-lookup"><span data-stu-id="e1773-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1773-104">`DATETIMEVALUE`-funktio palauttaa *DateTime*-arvon, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="e1773-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="e1773-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](/dotnet/standard/base-types/standard-date-and-time-format-strings) ja [mukautettu](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="e1773-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e1773-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="e1773-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e1773-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="e1773-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e1773-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="e1773-108">Arguments</span></span>

<span data-ttu-id="e1773-109">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e1773-109">`text`: *String*</span></span>

<span data-ttu-id="e1773-110">Teksti, joka vastaa muokattavaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="e1773-110">Text that represents the value to format.</span></span>

<span data-ttu-id="e1773-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e1773-111">`format`: *String*</span></span>

<span data-ttu-id="e1773-112">Annetun tekstin muoto.</span><span class="sxs-lookup"><span data-stu-id="e1773-112">The format of the given text.</span></span>

<span data-ttu-id="e1773-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="e1773-113">`culture`: *String*</span></span>

<span data-ttu-id="e1773-114">Tietyn tekstin muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="e1773-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="e1773-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="e1773-115">Return values</span></span>

<span data-ttu-id="e1773-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="e1773-116">*DateTime*</span></span>

<span data-ttu-id="e1773-117">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="e1773-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e1773-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="e1773-118">Usage notes</span></span>

<span data-ttu-id="e1773-119">Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="e1773-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e1773-120">Jos `DATETIMEVALUE`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="e1773-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e1773-121">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="e1773-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="e1773-122">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="e1773-122">Example 1</span></span>

<span data-ttu-id="e1773-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` palauttaa arvon **2:55:00 am 21. joulukuuta 2016**, joka perustuu määritettyyn mukautettuun muotoon ja oletussovelluksen **EN-US** -kulttuuriin.</span><span class="sxs-lookup"><span data-stu-id="e1773-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="e1773-124">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="e1773-124">Example 2</span></span>

<span data-ttu-id="e1773-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` palauttaa arvon **2:55:00 AM 21. joulukuuta 2016** perustuen määritettyyn mukautettuun muotoon ja kulttuuriin.</span><span class="sxs-lookup"><span data-stu-id="e1773-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="e1773-126">Kuitenkin `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämäärä-/aika-arvoksi tietylle kulttuurille.</span><span class="sxs-lookup"><span data-stu-id="e1773-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1773-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e1773-127">Additional resources</span></span>

[<span data-ttu-id="e1773-128">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="e1773-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]