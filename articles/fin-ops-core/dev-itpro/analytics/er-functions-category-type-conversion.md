---
title: Luettelo ER-funktioista tyypinmuutosluokassa
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin (ER) tukemista muunnosfunktioista.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561515"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="d10a5-103">Luettelo ER-funktioista tyypinmuutosluokassa</span><span class="sxs-lookup"><span data-stu-id="d10a5-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d10a5-104">Sähköisen raportoinnin (ER) tyyppimuuntofunktioita voidaan käyttää arvojen muuntamiseen tyyppien välillä.</span><span class="sxs-lookup"><span data-stu-id="d10a5-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="d10a5-105">Tässä aiheessa on yhteenveto näistä funktioista.</span><span class="sxs-lookup"><span data-stu-id="d10a5-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="d10a5-106">Tyypin muuntamisen toiminnot</span><span class="sxs-lookup"><span data-stu-id="d10a5-106">Type conversion functions</span></span>

| <span data-ttu-id="d10a5-107">Toiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-107">Function</span></span> | <span data-ttu-id="d10a5-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d10a5-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="d10a5-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="d10a5-110">Tämä funktio palauttaa *Int64*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="d10a5-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="d10a5-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="d10a5-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="d10a5-112">Tämä funktio palauttaa *Int*-arvon, joka edustaa määritettyä merkkijonoa.</span><span class="sxs-lookup"><span data-stu-id="d10a5-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="d10a5-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="d10a5-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="d10a5-114">Tämä funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkki* arvosta.</span><span class="sxs-lookup"><span data-stu-id="d10a5-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="d10a5-115">Muuntamisen aikana otetaan huomioon määritetyt desimaali- ja numeroryhmittelyerottimet.</span><span class="sxs-lookup"><span data-stu-id="d10a5-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="d10a5-116">Arvo</span><span class="sxs-lookup"><span data-stu-id="d10a5-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="d10a5-117">Tämä funktio palauttaa *todellisen* arvon, joka muunnetaan määritetystä *merkki* arvosta.</span><span class="sxs-lookup"><span data-stu-id="d10a5-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="d10a5-118">Säilöluokan tyyppimuuntofunktiot</span><span class="sxs-lookup"><span data-stu-id="d10a5-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="d10a5-119">Seuraavassa taulukossa kuvataan [säilöluokan](er-functions-category-container.md) tyyppimuuntofunktiot.</span><span class="sxs-lookup"><span data-stu-id="d10a5-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="d10a5-120">Toiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-120">Function</span></span> | <span data-ttu-id="d10a5-121">kuvaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d10a5-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="d10a5-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="d10a5-123">Tämä funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *Säilö*-tyypin tietokohteeksi.</span><span class="sxs-lookup"><span data-stu-id="d10a5-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="d10a5-124">Syötä muuntofunktiot päivämäärä- ja aikaluokassa</span><span class="sxs-lookup"><span data-stu-id="d10a5-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="d10a5-125">Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [päivämäärä- ja aikaluokassa](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="d10a5-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="d10a5-126">Toiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-126">Function</span></span> | <span data-ttu-id="d10a5-127">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d10a5-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="d10a5-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="d10a5-129">Tämä funktio palauttaa *DateTime*-arvon, joka muunnetaan tietystä *Merkki*-arvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="d10a5-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="d10a5-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="d10a5-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="d10a5-131">Tämä funktio palauttaa *DateTime*-arvon , joka muunnetaan tietyn *päivämäärän* arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="d10a5-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="d10a5-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="d10a5-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="d10a5-133">Tämä funktio palauttaa *Date*-arvon, joka muunnetaan tietystä *Merkki*-arvosta tekstinä määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa päivämäärä-/aika-arvoksi.</span><span class="sxs-lookup"><span data-stu-id="d10a5-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="d10a5-134">Kirjoita muuntamisfunktiot luetteloluokkaan</span><span class="sxs-lookup"><span data-stu-id="d10a5-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="d10a5-135">Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [luettelokategoriassa](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="d10a5-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="d10a5-136">Toiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-136">Function</span></span> | <span data-ttu-id="d10a5-137">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d10a5-138">Luettelo</span><span class="sxs-lookup"><span data-stu-id="d10a5-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="d10a5-139">Tämä funktio palauttaa *Tietueluettelon* arvon uutena luettelona, joka luodaan *säilö (tietue)* -tyypin määritetyistä argumenteista.</span><span class="sxs-lookup"><span data-stu-id="d10a5-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="d10a5-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="d10a5-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="d10a5-141">Tämä funktio palauttaa *Tietueluettelon* arvon, joka luodaan *luettelointi*- tai *säilö (tietue)* -tyypin tietyn argumentin rakenteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d10a5-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="d10a5-142">Jako</span><span class="sxs-lookup"><span data-stu-id="d10a5-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="d10a5-143">Tämä funktio jakaa määritetyn *merkkijono*-arvon alimerkkijonoiksi ja palauttaa tuloksen uudeksi *Tietueluettelon* arvoksi.</span><span class="sxs-lookup"><span data-stu-id="d10a5-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="d10a5-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="d10a5-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="d10a5-145">Tämä funktio palauttaa määritetystä luettelosta *merkkijonon*, joka koostuu määritetyn kentän ketjutetuista arvoista tietystä *Tietueluettelon* arvosta.</span><span class="sxs-lookup"><span data-stu-id="d10a5-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="d10a5-146">Arvot voidaan erottaa määritetyllä erottimella.</span><span class="sxs-lookup"><span data-stu-id="d10a5-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="d10a5-147">Kirjoita muuntamisfunktiot tekstiluokkaan</span><span class="sxs-lookup"><span data-stu-id="d10a5-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="d10a5-148">Seuraavassa taulukossa kuvataan tyyppimuuntofunktiot [tekstikategoriassa](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="d10a5-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="d10a5-149">Toiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-149">Function</span></span> | <span data-ttu-id="d10a5-150">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="d10a5-151">Char</span><span class="sxs-lookup"><span data-stu-id="d10a5-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="d10a5-152">Tämä funktio palauttaa *Merkkijono*-arvon, joka edustaa yksittäistä merkkiä, johon viitataan määritetyllä Unicode-numerolla.</span><span class="sxs-lookup"><span data-stu-id="d10a5-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="d10a5-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="d10a5-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="d10a5-154">Tämä funktio muuntaa *Merkkijono*-tyypin määritetyn syötteen *GUID*-tyypin tietokohteeksi.</span><span class="sxs-lookup"><span data-stu-id="d10a5-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="d10a5-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="d10a5-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="d10a5-156">Tämä funktio palauttaa *Merkkijonoarvon*, joka edustaa määritetyn numeron määritetyssä muodossa ja valinnaisesti määritetyssä kulttuurissa.</span><span class="sxs-lookup"><span data-stu-id="d10a5-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="d10a5-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="d10a5-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="d10a5-158">Tämä funktio palauttaa *Säilön* arvon, joka esittää määritetyn merkkijonon nopean vastauskoodin (QR Code) binaarimuodossa.</span><span class="sxs-lookup"><span data-stu-id="d10a5-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="d10a5-159">Teksti</span><span class="sxs-lookup"><span data-stu-id="d10a5-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="d10a5-160">Tämä funktio palauttaa määritetyn *merkkijono*-arvon, joka edustaa määritettyä numeroa sen jälkeen, kun se on muunnettu tekstimerkkijonoksi. Se puolestaan muotoillaan nykyisen sovellusesiintymän palvelimen aluekohtaisten asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="d10a5-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d10a5-161">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d10a5-161">Additional resources</span></span>

[<span data-ttu-id="d10a5-162">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d10a5-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="d10a5-163">Sähköisen raportoinnin kaavojen suunnittelutoiminto</span><span class="sxs-lookup"><span data-stu-id="d10a5-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="d10a5-164">Sähköisen raportoinnin kaavakieli</span><span class="sxs-lookup"><span data-stu-id="d10a5-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]