---
title: IF ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) IF-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 87e252a2751beeecb51e512cae38b271c1456fae
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744692"
---
# <a name="if-er-function"></a><span data-ttu-id="cb581-103">IF ER -funktio</span><span class="sxs-lookup"><span data-stu-id="cb581-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb581-104">`IF`- funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="cb581-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="cb581-105">Muussa tapauksessa se palauttaa toisen määritetyn arvon.</span><span class="sxs-lookup"><span data-stu-id="cb581-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="cb581-106">Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.</span><span class="sxs-lookup"><span data-stu-id="cb581-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb581-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="cb581-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="cb581-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="cb581-108">Arguments</span></span>

<span data-ttu-id="cb581-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="cb581-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="cb581-110">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="cb581-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="cb581-111">`first value`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="cb581-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="cb581-112">Tulos, joka palautetaan, jos ehto täyttyy.</span><span class="sxs-lookup"><span data-stu-id="cb581-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="cb581-113">`second value`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="cb581-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="cb581-114">Tulos, joka palautetaan, jos ehto ei täyty.</span><span class="sxs-lookup"><span data-stu-id="cb581-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb581-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="cb581-115">Return values</span></span>

<span data-ttu-id="cb581-116">*Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="cb581-116">*Any of the supported data types*</span></span>

<span data-ttu-id="cb581-117">Minkä tahansa tuettujen tietotyyppien tulokseksi saatava arvo.</span><span class="sxs-lookup"><span data-stu-id="cb581-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="cb581-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="cb581-118">Usage notes</span></span>

<span data-ttu-id="cb581-119">`first value` ja `second value` -argumentit on määritettävä käyttämällä samaa tietotyyppiä.</span><span class="sxs-lookup"><span data-stu-id="cb581-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="cb581-120">Poikkeus on heitetty suunnittelun aikana, jos määritettyjen arvojen tietotyypit eivät vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="cb581-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="cb581-121">Jos ensimmäinen arvo ja toinen arvo ovat *Säilön (tietueen)* tai *Tietueluettelon* tietotyypin arvoja, tuloksessa on vain kentät, jotka ovat molemmissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="cb581-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="cb581-122">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="cb581-122">Example</span></span>

<span data-ttu-id="cb581-123">`IF (1=2, "condition is met", "condition is not met")` palauttaa merkkijonon **"ehto ei täyty"**.</span><span class="sxs-lookup"><span data-stu-id="cb581-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb581-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="cb581-124">Additional resources</span></span>

[<span data-ttu-id="cb581-125">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="cb581-125">Logical functions</span></span>](er-functions-category-logical.md)
