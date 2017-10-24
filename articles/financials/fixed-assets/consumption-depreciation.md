---
title: Kulutuspoisto
description: "Tässä artikkelissa on yleiskuvaus poiston kulutusmenetelmästä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0c48877058edf8251ef6eb5dd63d7eecd1866f33
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="consumption-depreciation"></a><span data-ttu-id="42c97-103">Kulutuspoisto</span><span class="sxs-lookup"><span data-stu-id="42c97-103">Consumption depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="42c97-104">Tässä artikkelissa on yleiskuvaus poiston kulutusmenetelmästä.</span><span class="sxs-lookup"><span data-stu-id="42c97-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="42c97-105">Kun määrität käyttöomaisuuksien poistoprofiilin ja valitset **Poistoprofiilit**-sivun **Menetelmä**-kentässä **Kulutus**, poistoprofiiliin määritetyt käyttöomaisuudet perustuvat niiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="42c97-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="42c97-106">Prosenttiosuuksia ja välejä ei tarvitse määrittää **Poistoprofiilit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="42c97-107">Kun olet luonut kulutusmenetelmää käyttävän poistoprofiilin, voit määrittää menetelmän monella tavalla.</span><span class="sxs-lookup"><span data-stu-id="42c97-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="42c97-108">Kulutuspoiston määrittäminen ja käyttö</span><span class="sxs-lookup"><span data-stu-id="42c97-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="42c97-109">Luo poistoprofiili valitsemalla **Poistoprofiilit**-sivu.</span><span class="sxs-lookup"><span data-stu-id="42c97-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="42c97-110">Kulutuslaskelmia varten poistoprofiililla on oltava tunnus ja nimi. Lisäksi **Menetelmä**-kentässä on valittava **Kulutus**.</span><span class="sxs-lookup"><span data-stu-id="42c97-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="42c97-111">Määritä kulutuskertoimet **Kulutuskertoimet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="42c97-112">Jokaisella kulutuskertoimelle on oltava tunnus ja nimi. Lisäksi kulutuskertoimen on oltava määritetty määräksi tai prosenttiosuudeksi.</span><span class="sxs-lookup"><span data-stu-id="42c97-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="42c97-113">Määritä kulutusyksiköt **Kulutusyksiköt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="42c97-114">Jokaisella kulutusyksiköillä on oltava tunnus ja nimi.</span><span class="sxs-lookup"><span data-stu-id="42c97-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="42c97-115">Poistoyksiköitä käytetään laskemaan kulutuspoisto **Kulutuspoisto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="42c97-116">Yksiköitä ovat esimerkiksi kilometri (km), kilogramma (kg) ja tunti.</span><span class="sxs-lookup"><span data-stu-id="42c97-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="42c97-117">Määritä yksittäiset käyttöomaisuudet **Käyttöomaisuudet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="42c97-118">Valitse kullekin käyttöomaisuudelle arvomallit ja poistokirjat, joilla on poistoprofiilit.</span><span class="sxs-lookup"><span data-stu-id="42c97-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="42c97-119">Kulutuspoistolle on määritettävä arvomallit tai poistokirjat, jos jokin käyttöomaisuuksista käyttää kulutusmenetelmään perustuvia poistoprofiileja.</span><span class="sxs-lookup"><span data-stu-id="42c97-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="42c97-120">Tämä määritys tehdään joko **Arvomallit**-sivun **Poisto**-välilehdessä tai **Poistoprofiili**-sivun **Yleinen**-pikavälilehdessä.</span><span class="sxs-lookup"><span data-stu-id="42c97-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="42c97-121">Samaa arvomallia voi käyttää useissa käyttöomaisuuksissa.</span><span class="sxs-lookup"><span data-stu-id="42c97-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="42c97-122">Poistoprofiilit ovat osa kullekin käyttöomaisuuserälle valittua arvomallia tai poistokirjaa.</span><span class="sxs-lookup"><span data-stu-id="42c97-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="42c97-123">Ei voi lisätä etkä muokata poistoprofiileja suoraan **Käyttöomaisuudet**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="42c97-124">Voit muokata poistoprofiileja vain **Poistokirjat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="42c97-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="42c97-125">Anna tiedot seuraaviin **Arvomallit**- tai **Poistokirjat**-sivun **Kulutuspoisto**-kenttäryhmän kenttiin:</span><span class="sxs-lookup"><span data-stu-id="42c97-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="42c97-126">Kulutuskerroin</span><span class="sxs-lookup"><span data-stu-id="42c97-126">Consumption factor</span></span>
    -   <span data-ttu-id="42c97-127">Yksikkö</span><span class="sxs-lookup"><span data-stu-id="42c97-127">Unit</span></span>
    -   <span data-ttu-id="42c97-128">Yksikköpoistot</span><span class="sxs-lookup"><span data-stu-id="42c97-128">Unit depreciation</span></span>
    -   <span data-ttu-id="42c97-129">Arvioitu kulutus</span><span class="sxs-lookup"><span data-stu-id="42c97-129">Estimated consumption</span></span>

    <span data-ttu-id="42c97-130">**Kirjattu kulutus** -kentässä näkyy yksikköinä kulutuspoisto, joka on jo kirjattu joko käyttöomaisuus- ja arvomalliyhdistelmälle tai poistokirjaan.</span><span class="sxs-lookup"><span data-stu-id="42c97-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="42c97-131">Et voi päivittää tämän kentän arvoa manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="42c97-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="42c97-132">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="42c97-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="42c97-133">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="42c97-133">Example 1</span></span>

<span data-ttu-id="42c97-134">Seuraava kulutuskerroin on määritetty tammikuun 31. päivälle:</span><span class="sxs-lookup"><span data-stu-id="42c97-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="42c97-135">Määrä on 1 000.</span><span class="sxs-lookup"><span data-stu-id="42c97-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="42c97-136">Kiinteälle omaisuudelle määritetty yksikön poistohinta on 1,5.</span><span class="sxs-lookup"><span data-stu-id="42c97-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="42c97-137">Tammikuun 31. päivän poistoehdotus on seuraava: määrä x yksikkö poisto 1 000 × 1,5 = 1 500 Jos käyttöomaisuudelle määritetty kerroin on prosenttikerroin, käyttöomaisuuden arvomallin **Arvioitu kulutus** -kentässä arvioitu määrä kerrotaan valitulle päättymispäivälle määritetyllä prosentilla.</span><span class="sxs-lookup"><span data-stu-id="42c97-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="42c97-138">Tulokseksi saatavaa määrää ehdotetaan sitten kauden poistomääräksi.</span><span class="sxs-lookup"><span data-stu-id="42c97-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="42c97-139">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="42c97-139">Example 2</span></span>

<span data-ttu-id="42c97-140">Seuraava kulutuspoiston kerroin on määritetty tammikuun 31. päivälle:</span><span class="sxs-lookup"><span data-stu-id="42c97-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="42c97-141">Prosentti on 10 prosenttia.</span><span class="sxs-lookup"><span data-stu-id="42c97-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="42c97-142">Kiinteälle omaisuudelle määritetty yksikön poistohinta on 1,5.</span><span class="sxs-lookup"><span data-stu-id="42c97-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="42c97-143">Käyttöomaisuuserän arvioitu määrä on 2 000.</span><span class="sxs-lookup"><span data-stu-id="42c97-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="42c97-144">Tammikuun 31. päivän poistoehdotus on seuraava: arvioitu määrä × prosentti × yksikköpoisto 2 000 × 0,10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="42c97-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




