---
title: DATETODATETIME ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) DATETODATETIME-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916381"
---
# <span data-ttu-id="dff05-103"><a name="DATETODATETIME">DATETODATETIME ER-funktio</a></span><span class="sxs-lookup"><span data-stu-id="dff05-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dff05-104">`DATETODATETIME`-funktio palauttaa *DateTime*-arvon , joka muunnetaan tietyn päivämäärän arvosta päivämäärä- ja aika-arvoksi koordinoidussa yleisajassa (Greenwichin aika \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="dff05-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="dff05-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="dff05-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="dff05-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="dff05-106">Arguments</span></span>

<span data-ttu-id="dff05-107">`date`: *Päivämäärä*</span><span class="sxs-lookup"><span data-stu-id="dff05-107">`date`: *Date*</span></span>

<span data-ttu-id="dff05-108">Päivämääräarvo, joka vastaa muunnettavaa päivämäärää.</span><span class="sxs-lookup"><span data-stu-id="dff05-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="dff05-109">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="dff05-109">Return values</span></span>

<span data-ttu-id="dff05-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="dff05-110">*DateTime*</span></span>

<span data-ttu-id="dff05-111">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="dff05-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="dff05-112">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="dff05-112">Example 1</span></span>

<span data-ttu-id="dff05-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` palauttaa nykyisen Microsoft Dynamics 365 Finance -istunnon päivämäärän, 24. joulukuuta 2015, muodossa **12/24/2015 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="dff05-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="dff05-114">Tässä esimerkissä **CompInfo** on **Finance and Operations/taulu** -tyypin sähköisen raportoinnin ER-tietolähde, joka viittaa CompanyInfo-tauluun.</span><span class="sxs-lookup"><span data-stu-id="dff05-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="dff05-115">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="dff05-115">Example 2</span></span>

<span data-ttu-id="dff05-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` palauttaa päivämäärän ja kellonajan arvon **11/12/2019 12:00:00 AM**.</span><span class="sxs-lookup"><span data-stu-id="dff05-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dff05-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dff05-117">Additional resources</span></span>

[<span data-ttu-id="dff05-118">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="dff05-118">Date and time functions</span></span>](er-functions-category-datetime.md)
