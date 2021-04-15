---
title: CASE ER -funktio
description: Tässä ohjeaiheessa on tietoja siitä, miten sähköisen raportoinnin (ER) CASE-funktiota käytetään.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745446"
---
# <a name="case-er-function"></a><span data-ttu-id="418b8-103">CASE ER -funktio</span><span class="sxs-lookup"><span data-stu-id="418b8-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="418b8-104">`CASE`-funktio arvioi määritetyn lausekkeen arvon määritettyjen vaihtoehtoisten asetusten mukaan ja palauttaa ensimmäisen vaihtoehdon tuloksen, joka on yhtä suuri kuin määritetyn lausekkeen arvo.</span><span class="sxs-lookup"><span data-stu-id="418b8-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="418b8-105">Muussa tapauksessa se palauttaa valinnaisen oletustuloksen, jos oletustulos määritetään kutsutussa funktiossa viimeisenä argumenttina, jota ei edellä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="418b8-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="418b8-106">Palautettava arvo voi olla minkä tahansa tuettujen tietotyyppien arvo.</span><span class="sxs-lookup"><span data-stu-id="418b8-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="418b8-107">Syntaksi</span><span class="sxs-lookup"><span data-stu-id="418b8-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="418b8-108">Argumentit</span><span class="sxs-lookup"><span data-stu-id="418b8-108">Arguments</span></span>

<span data-ttu-id="418b8-109">`expression`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)</span><span class="sxs-lookup"><span data-stu-id="418b8-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="418b8-110">Kelvollinen lauseke, joka palauttaa primitiivisen tietotyypin arvon.</span><span class="sxs-lookup"><span data-stu-id="418b8-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="418b8-111">`option 1`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)</span><span class="sxs-lookup"><span data-stu-id="418b8-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="418b8-112">Kelvollinen lauseke, joka palauttaa saman primitiivisen tietotyypin arvon kutsutun funktion `expression`-argumentiksi.</span><span class="sxs-lookup"><span data-stu-id="418b8-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="418b8-113">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="418b8-113">This argument is required.</span></span>

<span data-ttu-id="418b8-114">`result 1`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="418b8-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="418b8-115">Edellistä vaihtoehtoa vastaava palautettu tulos.</span><span class="sxs-lookup"><span data-stu-id="418b8-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="418b8-116">Tämä argumentti on pakollinen.</span><span class="sxs-lookup"><span data-stu-id="418b8-116">This argument is required.</span></span>

<span data-ttu-id="418b8-117">`option N`: *Primitiivinen tietotyyppi* (totuusarvo, numeerinen tai teksti)</span><span class="sxs-lookup"><span data-stu-id="418b8-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="418b8-118">Kelvollinen lauseke, joka palauttaa saman primitiivisen tietotyypin arvon kutsutun funktion `expression`-argumentiksi.</span><span class="sxs-lookup"><span data-stu-id="418b8-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="418b8-119">Tämä argumentti on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="418b8-119">This argument is optional.</span></span>

<span data-ttu-id="418b8-120">`result N`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="418b8-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="418b8-121">Edellistä vaihtoehtoa vastaava palautettu tulos.</span><span class="sxs-lookup"><span data-stu-id="418b8-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="418b8-122">Tämä argumentti on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="418b8-122">This argument is optional.</span></span>

<span data-ttu-id="418b8-123">`default result`: *Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="418b8-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="418b8-124">Tulos, joka tulisi palauttaa, jos vastaavuutta ei ole.</span><span class="sxs-lookup"><span data-stu-id="418b8-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="418b8-125">Tämä argumentti on valinnainen.</span><span class="sxs-lookup"><span data-stu-id="418b8-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="418b8-126">Palautusarvot</span><span class="sxs-lookup"><span data-stu-id="418b8-126">Return values</span></span>

<span data-ttu-id="418b8-127">*Jokin tuetuista tietotyypeistä*</span><span class="sxs-lookup"><span data-stu-id="418b8-127">*Any of the supported data types*</span></span>

<span data-ttu-id="418b8-128">Minkä tahansa tuettujen tietotyyppien tulokseksi saatava arvo.</span><span class="sxs-lookup"><span data-stu-id="418b8-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="418b8-129">Käyttöhuomautukset</span><span class="sxs-lookup"><span data-stu-id="418b8-129">Usage notes</span></span>

<span data-ttu-id="418b8-130">Poikkeus on heitetty suorituksen aikana, jos vastaavuutta ei ole ja valinnaista oletustulosta ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="418b8-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="418b8-131">Kaikki tulokset on määritettävä käyttämällä samaa tietotyyppiä.</span><span class="sxs-lookup"><span data-stu-id="418b8-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="418b8-132">Poikkeus on heitetty suunnittelun aikana, jos määritettyjen tulosten tietotyypit eivät vastaa toisiaan.</span><span class="sxs-lookup"><span data-stu-id="418b8-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="418b8-133">Jos ensimmäinen tulosarvo ja *N*:s arvo ovat *Säilön (tietueen)* tai *Tietueluettelon* tietotyypin arvoja, tuloksessa on vain kentät, jotka ovat molemmissa arvoissa.</span><span class="sxs-lookup"><span data-stu-id="418b8-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="418b8-134">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="418b8-134">Example</span></span>

<span data-ttu-id="418b8-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` palauttaa merkkijonon **TALVI**, jos nykyinen sovellusistunnon päivämäärä on loka-joulukuun välissä.</span><span class="sxs-lookup"><span data-stu-id="418b8-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="418b8-136">Muussa tapauksessa se palauttaa tyhjän merkkijonon.</span><span class="sxs-lookup"><span data-stu-id="418b8-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="418b8-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="418b8-137">Additional resources</span></span>

[<span data-ttu-id="418b8-138">Loogiset toiminnot</span><span class="sxs-lookup"><span data-stu-id="418b8-138">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]