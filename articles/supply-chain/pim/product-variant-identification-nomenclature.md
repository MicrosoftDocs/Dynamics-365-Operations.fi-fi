---
title: "Tuotevariantin numeroiden ja nimien nimikkeistö"
description: "Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli]. Uusi nimikkeistö sisältää kohdennetun muodon, joka sisältää päätuotteen numeron, aktiiviset tuotedimensiot ja haluamasi tekstierottimet. Myös tuotenimille voi luoda nimikkeistön. Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla. Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: db01d26376ec3ca6997b1ad2cb62e7b3ecc4b330
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="22cae-107">Tuotevariantin numeroiden ja nimien nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="22cae-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="22cae-108">Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli].</span><span class="sxs-lookup"><span data-stu-id="22cae-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="22cae-109">Uusi nimikkeistö sisältää kohdennetun muodon, joka sisältää päätuotteen numeron, aktiiviset tuotedimensiot ja haluamasi tekstierottimet.</span><span class="sxs-lookup"><span data-stu-id="22cae-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="22cae-110">Myös tuotenimille voi luoda nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="22cae-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="22cae-111">Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla.</span><span class="sxs-lookup"><span data-stu-id="22cae-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="22cae-112">Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä.</span><span class="sxs-lookup"><span data-stu-id="22cae-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="22cae-113">Tuotevariantin numeroiden ja nimien uusien nimikkeistöjen avulla voi sisällyttää segmenttejä tuotevarianttien tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="22cae-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="22cae-114">Nämä segmentit voivat sisältää päätuotenumeron ja nimen, tuotedimensioiden tunnukset ja nimet, numerosarjat, tekstivakioita ja määritteitä.</span><span class="sxs-lookup"><span data-stu-id="22cae-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="22cae-115">Kun luot myyntitilauksen tai ostotilauksen, löydät nopeasti tietyt tuotevariantit tämän toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="22cae-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="22cae-116">Sekä tuotevariantin numeroille että nimille voi luoda nimikkeistöjä **Tuotenimikkeistö**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="22cae-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="22cae-117">Avaa tämä sivu valitsemalla **Tuotetietojen hallinta** &gt; **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="22cae-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="22cae-118">Ennalta määritettyjen tuotevarianttien nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="22cae-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="22cae-119">Tuotevariantit luodaan päätuotteelle jollain kolmesta määritysmenetelmästä:</span><span class="sxs-lookup"><span data-stu-id="22cae-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="22cae-120">Ennalta määritetyt variantit</span><span class="sxs-lookup"><span data-stu-id="22cae-120">Predefined variants</span></span>
-   <span data-ttu-id="22cae-121">Rajoitukseen perustuva</span><span class="sxs-lookup"><span data-stu-id="22cae-121">Constraint-based</span></span>
-   <span data-ttu-id="22cae-122">Dimensioon perustuva</span><span class="sxs-lookup"><span data-stu-id="22cae-122">Dimension-based</span></span>

<span data-ttu-id="22cae-123">Jokaisella tuotevariantilla on numero ja nimi, ja tuotevariantin numeroiden nimikkeistöjen avulla voi valita segmentit, jotka sisällytetään tuotevariantin numeroihin tai nimiin.</span><span class="sxs-lookup"><span data-stu-id="22cae-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="22cae-124">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="22cae-125">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="22cae-125">Product master number</span></span>
-   <span data-ttu-id="22cae-126">Päätuotteen nimi</span><span class="sxs-lookup"><span data-stu-id="22cae-126">Product master name</span></span>
-   <span data-ttu-id="22cae-127">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="22cae-127">Number sequence value</span></span>
-   <span data-ttu-id="22cae-128">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="22cae-128">Text constant</span></span>
-   <span data-ttu-id="22cae-129">Tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="22cae-129">Product dimensions</span></span>
    -   <span data-ttu-id="22cae-130">Konfiguraation tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="22cae-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="22cae-131">Värin tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="22cae-131">Color ID or name</span></span>
    -   <span data-ttu-id="22cae-132">Koon tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="22cae-132">Size ID or name</span></span>
    -   <span data-ttu-id="22cae-133">Tyylin tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="22cae-133">Style ID or name</span></span>

<span data-ttu-id="22cae-134">Kun olet määrittänyt tuotevariantin numeron nimikkeistön, voit yhdistää sen tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="22cae-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="22cae-135">Tämän jälkeen kaikki tähän tuotedimensioryhmään viittaavat päätuotteet määritetään tuotevariantin numeroille nimikkeistön mukaan.</span><span class="sxs-lookup"><span data-stu-id="22cae-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="22cae-136">Tuotevariantin nimien nimikkeistöjä ei kuitenkaan voi yhdistää tuotedimensioryhmiin.</span><span class="sxs-lookup"><span data-stu-id="22cae-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="22cae-137">Voit myös yhdistää tuotevariantin tunnuksen nimikkeistön suoraan päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="22cae-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="22cae-138">Tässä tapauksessa päätuotteeseen kuuluvat tuotevariantit yhdistetään tuotevariantin numeroihin ja nimiin nimikkeistöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="22cae-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="22cae-139">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="22cae-139">Example</span></span>

<span data-ttu-id="22cae-140">T-paitaa (TS1234) valmistetaan kolme eri kokoa (S, M, L), neljä eri väriä (punainen, vihreä, sininen, keltainen) ja kaksi mallia (poolo, V).</span><span class="sxs-lookup"><span data-stu-id="22cae-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="22cae-141">Mahdollisia tuotevariantteja on siis 24 (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="22cae-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="22cae-142">Voit luoda tuotevariantin numeron nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="22cae-143">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="22cae-143">Product master number</span></span>
2.  <span data-ttu-id="22cae-144">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="22cae-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="22cae-145">Väri</span><span class="sxs-lookup"><span data-stu-id="22cae-145">Color</span></span>
4.  <span data-ttu-id="22cae-146">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="22cae-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="22cae-147">Koko</span><span class="sxs-lookup"><span data-stu-id="22cae-147">Size</span></span>
6.  <span data-ttu-id="22cae-148">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="22cae-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="22cae-149">Tyyli</span><span class="sxs-lookup"><span data-stu-id="22cae-149">Style</span></span>

<span data-ttu-id="22cae-150">Tässä tapauksessa tuotevariantin numero ominaisuuksille punainen, S, poolo, T-paita TS1234-punainen-S-poolo.</span><span class="sxs-lookup"><span data-stu-id="22cae-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="22cae-151">Poissulkeva konfiguraationimikkeistö</span><span class="sxs-lookup"><span data-stu-id="22cae-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="22cae-152">Poissulkeville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="22cae-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="22cae-153">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="22cae-154">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="22cae-154">Number sequence value</span></span>
-   <span data-ttu-id="22cae-155">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="22cae-155">Text constant</span></span>
-   <span data-ttu-id="22cae-156">Määritteen arvo</span><span class="sxs-lookup"><span data-stu-id="22cae-156">Attribute value</span></span>

<span data-ttu-id="22cae-157">Jokaisella tuotemääritysmallin komponentilla voi olla oma konfiguraationimikkeistö.</span><span class="sxs-lookup"><span data-stu-id="22cae-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="22cae-158">Vain komponenttiin kuuluvia määritteitä saa käyttää.</span><span class="sxs-lookup"><span data-stu-id="22cae-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="22cae-159">Alikomponenttien tai käyttäjävaatimuksien määritteitä ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="22cae-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="22cae-160">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="22cae-160">Example</span></span>

<span data-ttu-id="22cae-161">Tuotemääritysmallin juurikomponentissa on seuraavat kaksi määritettä:</span><span class="sxs-lookup"><span data-stu-id="22cae-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="22cae-162">Materiaali (muovi, puu, teräs)</span><span class="sxs-lookup"><span data-stu-id="22cae-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="22cae-163">Pituus (10... 100)</span><span class="sxs-lookup"><span data-stu-id="22cae-163">Length (10...100)</span></span>

<span data-ttu-id="22cae-164">Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="22cae-165">Määritteen arvo: materiaali</span><span class="sxs-lookup"><span data-stu-id="22cae-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="22cae-166">Tekstivakio: AAA</span><span class="sxs-lookup"><span data-stu-id="22cae-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="22cae-167">Määritteen arvo: pituus</span><span class="sxs-lookup"><span data-stu-id="22cae-167">Attribute value: Length</span></span>

<span data-ttu-id="22cae-168">Tässä tapauksessa puumateriaalin konfiguraatiotunnus, jonka pituus on, on WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="22cae-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="22cae-169">Dimensioihin perustuva konfiguraationimikkeistö</span><span class="sxs-lookup"><span data-stu-id="22cae-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="22cae-170">Dimensioihin perustuville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="22cae-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="22cae-171">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="22cae-172">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="22cae-172">Number sequence value</span></span>
-   <span data-ttu-id="22cae-173">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="22cae-173">Text constant</span></span>
-   <span data-ttu-id="22cae-174">Konfiguraatioryhmän nimike</span><span class="sxs-lookup"><span data-stu-id="22cae-174">Configuration group item</span></span>

<span data-ttu-id="22cae-175">Konfiguraationimikkeistö voidaan määrittää tuoterakenteelle.</span><span class="sxs-lookup"><span data-stu-id="22cae-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="22cae-176">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="22cae-176">Example</span></span>

<span data-ttu-id="22cae-177">Tuoterakenne sisältää neljä tuoterakenteen riviä, jotka on jaettu kahteen konfiguraatioryhmään:</span><span class="sxs-lookup"><span data-stu-id="22cae-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="22cae-178">Tuoterakennerivi: M0007, vakiokaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="22cae-179">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="22cae-180">Tuoterakennerivi: M0008, korkealuokkainen kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="22cae-181">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="22cae-182">Tuoterakennerivi: M0021, kaiuttimen etukangas</span><span class="sxs-lookup"><span data-stu-id="22cae-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="22cae-183">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="22cae-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="22cae-184">Tuoterakennerivi: M0022, kaiuttimen teräsverkko</span><span class="sxs-lookup"><span data-stu-id="22cae-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="22cae-185">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="22cae-185">Configuration group: Front grill</span></span>

<span data-ttu-id="22cae-186">Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="22cae-187">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="22cae-188">Tekstivakio: &</span><span class="sxs-lookup"><span data-stu-id="22cae-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="22cae-189">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="22cae-189">Configuration group: Front grill</span></span>

<span data-ttu-id="22cae-190">Tässä tapauksessa etukankaalla varustetun vakiokaiutinkotelon konfiguraatiotunnus on M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="22cae-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="22cae-191">Tuotevarianttien ja konfiguraatioiden yhdistelmän nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="22cae-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="22cae-192">Jos käytät poissulkevaa tai dimensioihin perustuvaa määritysmenetelmää päätuotteen tuotevarianttien määritykseen, tuotevarianttien numerot voivat sisältää konfigurointidimension nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="22cae-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="22cae-193">Jos haluat konfiguroida variantit, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="22cae-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="22cae-194">Määritä **Tuotenimikkeistö**-sivulla tuotevariantin numeron nimikkeistö, joka sisältää konfigurointidimension.</span><span class="sxs-lookup"><span data-stu-id="22cae-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="22cae-195">Määritä nimikkeistö tuotedimensioryhmälle, jolla on konfigurointidimensio.</span><span class="sxs-lookup"><span data-stu-id="22cae-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="22cae-196">Määritä konfiguraationimikkeistö komponenteille tai tuoterakenteille, jota käytetään tuotevarianttien konfiguroimisessa.</span><span class="sxs-lookup"><span data-stu-id="22cae-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="22cae-197">Myös tuotevariantin nimille voi luoda nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="22cae-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="22cae-198">Tuotevariantin nimet voidaan konfiguroida niin, että ne sisältävät konfiguraation tunnuksen tai nimen.</span><span class="sxs-lookup"><span data-stu-id="22cae-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="22cae-199">Esimerkki poissulkevasta konfiguraatiosta</span><span class="sxs-lookup"><span data-stu-id="22cae-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="22cae-200">Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="22cae-201">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="22cae-201">Product master number</span></span>
2.  <span data-ttu-id="22cae-202">Tekstivakio \_</span><span class="sxs-lookup"><span data-stu-id="22cae-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="22cae-203">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="22cae-203">Configuration</span></span>

<span data-ttu-id="22cae-204">Konfiguraationimikkeistö sisältää seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="22cae-205">Määritteen arvo: materiaali</span><span class="sxs-lookup"><span data-stu-id="22cae-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="22cae-206">Tekstivakio: AAA</span><span class="sxs-lookup"><span data-stu-id="22cae-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="22cae-207">Määritteen arvo: pituus</span><span class="sxs-lookup"><span data-stu-id="22cae-207">Attribute value: Length</span></span>

<span data-ttu-id="22cae-208">Syötä segmenteille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="22cae-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="22cae-209">Päätuotteen numero = **M0099**</span><span class="sxs-lookup"><span data-stu-id="22cae-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="22cae-210">Materiaali = **muovi**</span><span class="sxs-lookup"><span data-stu-id="22cae-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="22cae-211">Pituus = **12**</span><span class="sxs-lookup"><span data-stu-id="22cae-211">Length = **12**</span></span>

<span data-ttu-id="22cae-212">Tässä tapauksessa tuotevariantin numero on M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="22cae-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="22cae-213">Esimerkki dimensioihin perustuvasta konfiguraatiosta</span><span class="sxs-lookup"><span data-stu-id="22cae-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="22cae-214">Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="22cae-215">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="22cae-215">Product master number</span></span>
2.  <span data-ttu-id="22cae-216">Tekstivakio //</span><span class="sxs-lookup"><span data-stu-id="22cae-216">Text constant "//"</span></span>
3.  <span data-ttu-id="22cae-217">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="22cae-217">Configuration</span></span>

<span data-ttu-id="22cae-218">Konfiguraationimikkeistö sisältää seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="22cae-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="22cae-219">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="22cae-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="22cae-220">Tekstivakio: &</span><span class="sxs-lookup"><span data-stu-id="22cae-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="22cae-221">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="22cae-221">Configuration group: Front grill</span></span>

<span data-ttu-id="22cae-222">Syötä segmenteille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="22cae-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="22cae-223">Päätuotteen numero = **D0123**</span><span class="sxs-lookup"><span data-stu-id="22cae-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="22cae-224">Kaiutinkaappi = **M0008**</span><span class="sxs-lookup"><span data-stu-id="22cae-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="22cae-225">Etusäleikkö = **M0022**</span><span class="sxs-lookup"><span data-stu-id="22cae-225">Front grill = **M0022**</span></span>

<span data-ttu-id="22cae-226">Tässä tapauksessa tuotevariantin numero on D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="22cae-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="22cae-227">Numerointiristiriidat</span><span class="sxs-lookup"><span data-stu-id="22cae-227">Numbering conflicts</span></span>
<span data-ttu-id="22cae-228">Joissakin tapauksissa tuotevariantin numeron määritetty nimikkeistö ei tuota yksilöiviä tuotevariantin numeroita.</span><span class="sxs-lookup"><span data-stu-id="22cae-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="22cae-229">Esimerkiksi tuotevariantin numerot eivät ole yksilöiviä, jos yksi aktiivinen tuotedimensio ei sisälly päätuotteen nimikkeistöön, joka käyttää esimääritettyä variantin määritysmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="22cae-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="22cae-230">Ristiriitatilanteiden käsittelytapa vaihtelee määritysmenetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="22cae-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="22cae-231">Ennalta määritetyt variantit</span><span class="sxs-lookup"><span data-stu-id="22cae-231">Predefined variants</span></span>

<span data-ttu-id="22cae-232">Jos yrität luoda manuaalisesti tai automaattisesti tuotevariantteja, joista vähintään yksi päättyy samaan tuotevariantin numeroon, tapahtuu virhe.</span><span class="sxs-lookup"><span data-stu-id="22cae-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="22cae-233">Voit välttää tämän käyttämällä tuotedimensioryhmässä kaikkia aktiivisia tuotedimensioita.</span><span class="sxs-lookup"><span data-stu-id="22cae-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="22cae-234">Vaihtoehtoisesti voit ottaa mukaan numerosarjat, joiden avulla varmistetaan, että tuotevariantin numerot ovat yksilöiviä.</span><span class="sxs-lookup"><span data-stu-id="22cae-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="22cae-235">Poissulkevat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="22cae-235">Constraint-based configurations</span></span>

<span data-ttu-id="22cae-236">Nimikkeistön mukaan järjestelmä yrittää määrittää ei-yksilöivän tuotevariantin numeron konfiguraatioon.</span><span class="sxs-lookup"><span data-stu-id="22cae-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="22cae-237">Tällöin järjestelmä käyttää sen sijaan konfigurointidimension numerosarjaa tuotevariantin numerona, ja näyttöön tulee varoitus.</span><span class="sxs-lookup"><span data-stu-id="22cae-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="22cae-238">Voit välttää tämän, kun nimikkeistössä on riittävästi määritteitä. Tällöin yksilöivien tuotevariantin numeroiden varmistaminen on helpompaa.</span><span class="sxs-lookup"><span data-stu-id="22cae-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="22cae-239">Varmista myös, että komponentin **Käytä uudelleen** -vaihtoehto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="22cae-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="22cae-240">Dimensioihin perustuvat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="22cae-240">Dimension-based configurations</span></span>

<span data-ttu-id="22cae-241">Konfigurointiprosessin yhden vaiheen aikana järjestelmä ehdottaa konfiguraatioarvoa nimikkeistön mukaan.</span><span class="sxs-lookup"><span data-stu-id="22cae-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="22cae-242">Et voi muuttaa konfigurointiarvoa manuaalisesti tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="22cae-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="22cae-243">Kun konfiguraatio tallennetaan, järjestelmä tarkistaa, onko konfiguraation arvo yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="22cae-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="22cae-244">Jos syötetty arvo ei ole yksilöivä, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="22cae-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="22cae-245">Voit tallentaa konfiguraation syöttämällä yksilöivän konfiguraatioarvon.</span><span class="sxs-lookup"><span data-stu-id="22cae-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="22cae-246">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="22cae-246">See also</span></span>
--------

[<span data-ttu-id="22cae-247">Tuotenumeroiden nimikkeistön luominen esimääritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="22cae-247">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="22cae-248">Tuotenumeroiden nimikkeistön luominen konfiguroiduille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="22cae-248">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)


