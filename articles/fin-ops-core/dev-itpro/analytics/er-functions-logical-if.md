---
title: IF ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) IF-funktiota käytetään.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a69675e3c743154e8119ba6c04da5897f23a8422
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565901"
---
# <a name="if-er-function"></a><span data-ttu-id="8d2b4-103">IF ER -funktio</span><span class="sxs-lookup"><span data-stu-id="8d2b4-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d2b4-104">`IF`- funktio palauttaa ensimmäisen määritetyn arvon, jos määritetyt ehdot täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="8d2b4-105">Muussa tapauksessa se palauttaa toisen määritetyn arvon.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="8d2b4-106">Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2b4-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="8d2b4-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="8d2b4-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="8d2b4-108">Arguments</span></span>

<span data-ttu-id="8d2b4-109">`condition`: *Totuusarvo*</span><span class="sxs-lookup"><span data-stu-id="8d2b4-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="8d2b4-110">Kelvollinen ehdollinen lauseke, joka on testattava.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="8d2b4-111">`first value`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="8d2b4-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="8d2b4-112">Tulos, joka palautetaan, jos ehto täyttyy.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="8d2b4-113">`second value`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="8d2b4-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="8d2b4-114">Tulos, joka palautetaan, jos ehto ei täyty.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d2b4-115">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="8d2b4-115">Return values</span></span>

<span data-ttu-id="8d2b4-116">*Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="8d2b4-116">*Any of the supported data types*</span></span>

<span data-ttu-id="8d2b4-117">Minkä tahansa tuettujen tietotyyppien tulokseksi saatava arvo.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d2b4-118">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="8d2b4-118">Usage notes</span></span>

<span data-ttu-id="8d2b4-119">`first value` ja `second value` -argumentit on määritettävä käyttämällä samaa tietotyyppiä.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="8d2b4-120">Poikkeus on heitetty suunnittelun aikana, jos määritettyjen arvojen tietotyypit eivät vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="8d2b4-121">Jos ensimmäinen arvo ja toinen arvo ovat *Säilön (tietueen)* tai *Tietueluettelon* tietotyypin arvoja, tuloksessa on vain kentät, jotka ovat molemmissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="8d2b4-122">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8d2b4-122">Example</span></span>

<span data-ttu-id="8d2b4-123">`IF (1=2, "condition is met", "condition is not met")` palauttaa merkkijonon **"ehto ei täyty"**.</span><span class="sxs-lookup"><span data-stu-id="8d2b4-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d2b4-124">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8d2b4-124">Additional resources</span></span>

[<span data-ttu-id="8d2b4-125">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="8d2b4-125">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]