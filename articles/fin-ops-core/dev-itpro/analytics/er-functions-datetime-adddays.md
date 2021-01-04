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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d90c19ddc64286843347976c000267e416bf05
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688440"
---
# <a name="adddays-er-function"></a><span data-ttu-id="8647c-103">ADDDAYS ER-funktio</span><span class="sxs-lookup"><span data-stu-id="8647c-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8647c-104">`ADDDAYS`-funktio laskee *DateTime*-arvon, joka on määritetty päivien määrä ennen määritettyä alkamispäivää tai sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8647c-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="8647c-105">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8647c-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="8647c-106">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8647c-106">Arguments</span></span>

<span data-ttu-id="8647c-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="8647c-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="8647c-108">Päivämäärä-/aika-arvo, joka vastaa alkamispäivämäärää.</span><span class="sxs-lookup"><span data-stu-id="8647c-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="8647c-109">`days`: *Kokonaisluku*</span><span class="sxs-lookup"><span data-stu-id="8647c-109">`days`: *Integer*</span></span>

<span data-ttu-id="8647c-110">Päivien lukumäärä ennen tai jälkeen `datetime`.</span><span class="sxs-lookup"><span data-stu-id="8647c-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="8647c-111">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8647c-111">Return values</span></span>

<span data-ttu-id="8647c-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="8647c-112">*DateTime*</span></span>

<span data-ttu-id="8647c-113">Tulokseksi saatava päivämäärä-/aika-arvo.</span><span class="sxs-lookup"><span data-stu-id="8647c-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8647c-114">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="8647c-114">Usage notes</span></span>

<span data-ttu-id="8647c-115">Positiivinen arvo tuotoille `days` viittaa tulevaan päivään.</span><span class="sxs-lookup"><span data-stu-id="8647c-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="8647c-116">Negatiivinen arvo tuottaa kuluneen päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="8647c-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="8647c-117">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="8647c-117">Example 1</span></span>

<span data-ttu-id="8647c-118">`ADDDAYS (NOW(), 7)` palauttaa päivämäärän ja ajan seitsemän päivän kuluttua.</span><span class="sxs-lookup"><span data-stu-id="8647c-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="8647c-119">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="8647c-119">Example 2</span></span>

<span data-ttu-id="8647c-120">`ADDDAYS (NOW(), -3)` palauttaa päivämäärän ja ajan kolme päivää sitten.</span><span class="sxs-lookup"><span data-stu-id="8647c-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8647c-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8647c-121">Additional resources</span></span>

[<span data-ttu-id="8647c-122">Päivämäärä- ja aikatoiminnot</span><span class="sxs-lookup"><span data-stu-id="8647c-122">Date and time functions</span></span>](er-functions-category-datetime.md)
