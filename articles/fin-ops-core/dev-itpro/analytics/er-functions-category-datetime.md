---
title: Luettelo ER-funktioista päivämäärä- ja aikaluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista päivämäärä- ja aikafunktioista.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2dd8524c9cd368f0fe64347e3212b419bb0902b4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744558"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="79ed0-103">Luettelo ER-funktioista päivämäärä- ja aikaluokassa</span><span class="sxs-lookup"><span data-stu-id="79ed0-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="79ed0-104">Sähköisen raportoinnin (ER) päivämäärä- ja aikafunktioiden avulla voidaan poimia tietoja päivämäärä- ja aika-arvoista sekä suorittaa niitä koskevia toimintoja.</span><span class="sxs-lookup"><span data-stu-id="79ed0-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="79ed0-105">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="79ed0-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="79ed0-106">Luettelo tuetuista toiminnoista</span><span class="sxs-lookup"><span data-stu-id="79ed0-106">List of supported functions</span></span>

| <span data-ttu-id="79ed0-107">Toiminto</span><span class="sxs-lookup"><span data-stu-id="79ed0-107">Function</span></span> | <span data-ttu-id="79ed0-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="79ed0-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="79ed0-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="79ed0-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="79ed0-110">Tämä funktio palauttaa *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="79ed0-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="79ed0-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="79ed0-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="79ed0-112">Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämääräarvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="79ed0-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="79ed0-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="79ed0-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="79ed0-114">Tämä funktio palauttaa *Merkkijonoarvon*, joka esittää tietyn päivämäärä-/aika-arvon tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="79ed0-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="79ed0-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="79ed0-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="79ed0-116">Tämä funktio palauttaa *DateTime-arvon*, joka muunnetaan tietystä tekstiarvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="79ed0-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="79ed0-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="79ed0-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="79ed0-118">Tämä funktio palauttaa *DateTime-arvon* , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="79ed0-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="79ed0-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="79ed0-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="79ed0-120">Tämä funktio palauttaa *Date-arvon*, joka muunnetaan annetusta tekstiarvosta määrätyssä muodossa ja valinnaisesti määritellyssä kulttuurissa päivämääräarvoksi.</span><span class="sxs-lookup"><span data-stu-id="79ed0-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="79ed0-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="79ed0-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="79ed0-122">Tämä toiminto palauttaa tammikuun 1. päivän ja määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="79ed0-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="79ed0-123">Päivää</span><span class="sxs-lookup"><span data-stu-id="79ed0-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="79ed0-124">Tämä toiminto palauttaa ensimmäisen määritetyn päivämäärän ja toisen määritetyn päivämäärän välisten päivien määrää kuvaavan arvon *kokonaislukuna*.</span><span class="sxs-lookup"><span data-stu-id="79ed0-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="79ed0-125">Now</span><span class="sxs-lookup"><span data-stu-id="79ed0-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="79ed0-126">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="79ed0-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="79ed0-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="79ed0-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="79ed0-128">Tämä funktio palauttaa *päivämäärän* arvon, joka vastaa **Null** -arvoa (1. tammikuuta 1900).</span><span class="sxs-lookup"><span data-stu-id="79ed0-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="79ed0-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="79ed0-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="79ed0-130">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa **Null**-arvoista päivämäärä- ja aika-arvoa (1. tammikuuta 1900) koordinoituun yleisaikaan.</span><span class="sxs-lookup"><span data-stu-id="79ed0-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="79ed0-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="79ed0-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="79ed0-132">Tämä funktio palauttaa *DateTime*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="79ed0-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="79ed0-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="79ed0-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="79ed0-134">Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovellusistunnon päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="79ed0-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="79ed0-135">Tänään</span><span class="sxs-lookup"><span data-stu-id="79ed0-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="79ed0-136">Tämä funktio palauttaa *Date*-arvon, joka edustaa nykyistä sovelluspalvelimen päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="79ed0-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="79ed0-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="79ed0-137">Additional resources</span></span>

[<span data-ttu-id="79ed0-138">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="79ed0-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="79ed0-139">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="79ed0-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="79ed0-140">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="79ed0-140">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]