---
title: DATETIMEVALUE ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETIMEVALUE-funktiota käytetään.
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070687"
---
# <span data-ttu-id="cbb77-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="cbb77-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cbb77-104">`DATETIMEVALUE`-funktio palauttaa *DateTime*-arvon, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä [kulttuurissa](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="cbb77-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="cbb77-105">Lisätietoja tuetuista muodoista on kohdassa [vakio](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [mukautettu](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="cbb77-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="cbb77-106">Syntaksi 1</span><span class="sxs-lookup"><span data-stu-id="cbb77-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="cbb77-107">Syntaksi 2</span><span class="sxs-lookup"><span data-stu-id="cbb77-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="cbb77-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="cbb77-108">Arguments</span></span>

<span data-ttu-id="cbb77-109">`text`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="cbb77-109">`text`: *String*</span></span>

<span data-ttu-id="cbb77-110">Teksti, joka vastaa muokattavaa arvoa.</span><span class="sxs-lookup"><span data-stu-id="cbb77-110">Text that represents the value to format.</span></span>

<span data-ttu-id="cbb77-111">`format`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="cbb77-111">`format`: *String*</span></span>

<span data-ttu-id="cbb77-112">Annetun tekstin muoto.</span><span class="sxs-lookup"><span data-stu-id="cbb77-112">The format of the given text.</span></span>

<span data-ttu-id="cbb77-113">`culture`: *Merkkijono*</span><span class="sxs-lookup"><span data-stu-id="cbb77-113">`culture`: *String*</span></span>

<span data-ttu-id="cbb77-114">Tietyn tekstin muotoilussa käytettävä kulttuuri.</span><span class="sxs-lookup"><span data-stu-id="cbb77-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="cbb77-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="cbb77-115">Return values</span></span>

<span data-ttu-id="cbb77-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="cbb77-116">*DateTime*</span></span>

<span data-ttu-id="cbb77-117">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="cbb77-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cbb77-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="cbb77-118">Usage notes</span></span>

<span data-ttu-id="cbb77-119">Kun kulttuuria ei ole määritetty kutsutun funktion argumentiksi, kutsuvan kontekstin määrittämä arvo `culture` määritetään.</span><span class="sxs-lookup"><span data-stu-id="cbb77-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="cbb77-120">Jos `DATETIMEVALUE`-funktiota kutsutaan esimerkiksi käyttämällä syntaksia 1 sähköisen raportoinnin (ER) muodossa **TIEDOSTO**-elementille, joka on määritetty käyttämään Saksan kulttuuria, muuntaminen tehdään Saksan kulttuurin avulla.</span><span class="sxs-lookup"><span data-stu-id="cbb77-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="cbb77-121">`culture`-arvon oletusarvo on **FI-FI**.</span><span class="sxs-lookup"><span data-stu-id="cbb77-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="cbb77-122">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="cbb77-122">Example 1</span></span>

<span data-ttu-id="cbb77-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` palauttaa arvon **2:55:00 am 21. joulukuuta 2016**, joka perustuu määritettyyn mukautettuun muotoon ja oletussovelluksen **EN-US** -kulttuuriin.</span><span class="sxs-lookup"><span data-stu-id="cbb77-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="cbb77-124">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="cbb77-124">Example 2</span></span>

<span data-ttu-id="cbb77-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` palauttaa arvon **2:55:00 AM 21. joulukuuta 2016** perustuen määritettyyn mukautettuun muotoon ja kulttuuriin.</span><span class="sxs-lookup"><span data-stu-id="cbb77-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="cbb77-126">Kuitenkin `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` aiheuttaa poikkeuksen, joka ilmoittaa käyttäjälle, että määritettyä merkkijonoa ei tunnisteta kelvolliseksi päivämäärä-/aika-arvoksi tietylle kulttuurille.</span><span class="sxs-lookup"><span data-stu-id="cbb77-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cbb77-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="cbb77-127">Additional resources</span></span>

[<span data-ttu-id="cbb77-128">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="cbb77-128">Date and time functions</span></span>](er-functions-category-datetime.md)
