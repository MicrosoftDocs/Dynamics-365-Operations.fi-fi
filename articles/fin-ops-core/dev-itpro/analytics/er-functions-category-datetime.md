---
title: Luettelo ER-funktioista päivämäärä- ja aikaluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista päivämäärä- ja aikafunktioista.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916565"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="53c1e-103">Luettelo ER-funktioista päivämäärä- ja aikaluokassa</span><span class="sxs-lookup"><span data-stu-id="53c1e-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53c1e-104">Sähköisen raportoinnin (ER) päivämäärä- ja aikafunktioiden avulla voidaan poimia tietoja päivämäärä- ja aika-arvoista sekä suorittaa niitä koskevia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="53c1e-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="53c1e-105">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="53c1e-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="53c1e-106">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="53c1e-106">List of supported functions</span></span>

| <span data-ttu-id="53c1e-107">Toiminto</span><span class="sxs-lookup"><span data-stu-id="53c1e-107">Function</span></span> | <span data-ttu-id="53c1e-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="53c1e-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="53c1e-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="53c1e-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="53c1e-110">Tämä funktio palauttaa *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="53c1e-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="53c1e-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="53c1e-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="53c1e-112">Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="53c1e-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="53c1e-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="53c1e-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="53c1e-114">Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="53c1e-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="53c1e-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="53c1e-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="53c1e-116">Tämä funktio palauttaa *DateTime-arvon*, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="53c1e-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="53c1e-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="53c1e-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="53c1e-118">Tämä funktio palauttaa *DateTime-arvon* , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="53c1e-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="53c1e-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="53c1e-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="53c1e-120">Tämä funktio palauttaa *Date-arvon*, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä kulttuurissa päivämääräarvoksi.</span><span class="sxs-lookup"><span data-stu-id="53c1e-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="53c1e-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="53c1e-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="53c1e-122">Tämä toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="53c1e-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="53c1e-123">Päivää</span><span class="sxs-lookup"><span data-stu-id="53c1e-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="53c1e-124">Tämä toiminto palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="53c1e-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="53c1e-125">Now</span><span class="sxs-lookup"><span data-stu-id="53c1e-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="53c1e-126">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="53c1e-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="53c1e-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="53c1e-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="53c1e-128">Tämä funktio palauttaa *päivämäärän* arvon, joka vastaa **Null** -arvoa (1. tammikuuta 1900).</span><span class="sxs-lookup"><span data-stu-id="53c1e-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="53c1e-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="53c1e-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="53c1e-130">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan.</span><span class="sxs-lookup"><span data-stu-id="53c1e-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="53c1e-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="53c1e-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="53c1e-132">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="53c1e-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="53c1e-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="53c1e-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="53c1e-134">Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="53c1e-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="53c1e-135">Tänään</span><span class="sxs-lookup"><span data-stu-id="53c1e-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="53c1e-136">Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="53c1e-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="53c1e-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="53c1e-137">Additional resources</span></span>

[<span data-ttu-id="53c1e-138">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="53c1e-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="53c1e-139">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="53c1e-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="53c1e-140">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="53c1e-140">Electronic reporting formula language</span></span>](er-formula-language.md)
