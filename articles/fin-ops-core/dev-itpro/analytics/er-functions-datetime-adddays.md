---
title: ADDDAYS ER-funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) ADDDAYS-funktiota käytetään.
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743372"
---
# <a name="adddays-er-function"></a><span data-ttu-id="17758-103">ADDDAYS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="17758-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17758-104">`ADDDAYS`-funktio laskee *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="17758-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="17758-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="17758-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="17758-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="17758-106">Arguments</span></span>

<span data-ttu-id="17758-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="17758-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="17758-108">Päivämäärä-/aika-arvo, joka vastaa alkamispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="17758-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="17758-109">`days`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="17758-109">`days`: *Integer*</span></span>

<span data-ttu-id="17758-110">Päivien lukumäärä ennen tai jälkeen `datetime`.</span><span class="sxs-lookup"><span data-stu-id="17758-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="17758-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="17758-111">Return values</span></span>

<span data-ttu-id="17758-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="17758-112">*DateTime*</span></span>

<span data-ttu-id="17758-113">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="17758-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17758-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="17758-114">Usage notes</span></span>

<span data-ttu-id="17758-115">Positiivinen arvo tuotoille `days` viittaa tulevaan päivään.</span><span class="sxs-lookup"><span data-stu-id="17758-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="17758-116">Negatiivinen arvo tuottaa kuluneen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="17758-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="17758-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="17758-117">Example 1</span></span>

<span data-ttu-id="17758-118">`ADDDAYS (NOW(), 7)` palauttaa päivämäärän ja ajan seitsemän päivän kuluttua.</span><span class="sxs-lookup"><span data-stu-id="17758-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="17758-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="17758-119">Example 2</span></span>

<span data-ttu-id="17758-120">`ADDDAYS (NOW(), -3)` palauttaa päivämäärän ja ajan kolme päivää sitten.</span><span class="sxs-lookup"><span data-stu-id="17758-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17758-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="17758-121">Additional resources</span></span>

[<span data-ttu-id="17758-122">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="17758-122">Date and time functions</span></span>](er-functions-category-datetime.md)
