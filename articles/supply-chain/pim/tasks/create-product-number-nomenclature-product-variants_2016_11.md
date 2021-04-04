---
title: Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille
description: Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258872"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="135f1-103">Luo tuotenumeroiden nimikkeistö määritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="135f1-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="135f1-104">Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään konfiguroiduille tuotevarianteille ja miten se voidaan liittää konfiguroitavaan päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="135f1-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="135f1-105">Tässä ohjeaiheessa kerrotaan myös, miten tuotteen kokoonpanomallin osan konfiguraationimikkeistö rakennetaan.</span><span class="sxs-lookup"><span data-stu-id="135f1-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="135f1-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="135f1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="135f1-107">Uusi tuotenumeroiden nimikkeistö on määritetty päätuotteelle D0004.</span><span class="sxs-lookup"><span data-stu-id="135f1-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="135f1-108">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="135f1-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="135f1-109">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="135f1-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="135f1-110">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="135f1-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="135f1-111">Valitse Tuotenimikkeistö.</span><span class="sxs-lookup"><span data-stu-id="135f1-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="135f1-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="135f1-112">Click New.</span></span>
4. <span data-ttu-id="135f1-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="135f1-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="135f1-115">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-115">Click Add.</span></span>
7. <span data-ttu-id="135f1-116">Valitse Päätuotteen numero.</span><span class="sxs-lookup"><span data-stu-id="135f1-116">Click Product master number.</span></span>
8. <span data-ttu-id="135f1-117">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-117">Click Add.</span></span>
9. <span data-ttu-id="135f1-118">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="135f1-118">Click Text constant.</span></span>
10. <span data-ttu-id="135f1-119">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="135f1-120">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="135f1-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-121">Click Add.</span></span>
13. <span data-ttu-id="135f1-122">Valitse Konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="135f1-122">Click Configuration.</span></span>
14. <span data-ttu-id="135f1-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="135f1-124">Tuotenumeroiden nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="135f1-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="135f1-125">Valitse Päätuotteet.</span><span class="sxs-lookup"><span data-stu-id="135f1-125">Click Product masters.</span></span>
2. <span data-ttu-id="135f1-126">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="135f1-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="135f1-127">Voit esimerkiksi suodattaa Tuotenumero-kenttää arvolla D.</span><span class="sxs-lookup"><span data-stu-id="135f1-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="135f1-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="135f1-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="135f1-129">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="135f1-129">Click Edit.</span></span>
5. <span data-ttu-id="135f1-130">Valitse Käytä nimikkeistöä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="135f1-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="135f1-131">Syötä tai valitse arvo Tuotevariantin numeron nimikkeistö -kentässä.</span><span class="sxs-lookup"><span data-stu-id="135f1-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="135f1-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-132">Close the page.</span></span>
8. <span data-ttu-id="135f1-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="135f1-134">Nimikkeistön luominen tuotemääritysmallin osalle</span><span class="sxs-lookup"><span data-stu-id="135f1-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="135f1-135">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="135f1-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="135f1-136">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="135f1-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="135f1-137">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="135f1-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="135f1-138">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="135f1-138">Click Edit.</span></span>
5. <span data-ttu-id="135f1-139">Valitse Käytä konfiguraationimikkeistöä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="135f1-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="135f1-140">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-140">Click Add.</span></span>
7. <span data-ttu-id="135f1-141">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-141">Click Attribute value.</span></span>
8. <span data-ttu-id="135f1-142">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="135f1-143">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="135f1-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="135f1-144">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-144">Click Add.</span></span>
11. <span data-ttu-id="135f1-145">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="135f1-145">Click Text constant.</span></span>
12. <span data-ttu-id="135f1-146">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="135f1-147">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="135f1-148">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-148">Click Add.</span></span>
15. <span data-ttu-id="135f1-149">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-149">Click Attribute value.</span></span>
16. <span data-ttu-id="135f1-150">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="135f1-151">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="135f1-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="135f1-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-152">Click Add.</span></span>
19. <span data-ttu-id="135f1-153">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="135f1-153">Click Text constant.</span></span>
20. <span data-ttu-id="135f1-154">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="135f1-155">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="135f1-156">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-156">Click Add.</span></span>
23. <span data-ttu-id="135f1-157">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-157">Click Attribute value.</span></span>
24. <span data-ttu-id="135f1-158">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="135f1-159">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="135f1-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="135f1-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-160">Click Add.</span></span>
27. <span data-ttu-id="135f1-161">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="135f1-161">Click Text constant.</span></span>
28. <span data-ttu-id="135f1-162">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="135f1-163">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="135f1-164">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-164">Click Add.</span></span>
31. <span data-ttu-id="135f1-165">Valitse Määritteen arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-165">Click Attribute value.</span></span>
32. <span data-ttu-id="135f1-166">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="135f1-167">Syötä tai valitse arvo kentässä Määrite.</span><span class="sxs-lookup"><span data-stu-id="135f1-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="135f1-168">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-168">Click Add.</span></span>
35. <span data-ttu-id="135f1-169">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="135f1-169">Click Text constant.</span></span>
36. <span data-ttu-id="135f1-170">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="135f1-171">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="135f1-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="135f1-172">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="135f1-172">Click Add.</span></span>
39. <span data-ttu-id="135f1-173">Valitse Numerosarjan arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="135f1-174">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="135f1-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="135f1-175">Anna tai valitse Numerojärjestys-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="135f1-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="135f1-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-176">Close the page.</span></span>
43. <span data-ttu-id="135f1-177">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-177">Close the page.</span></span>
44. <span data-ttu-id="135f1-178">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="135f1-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]