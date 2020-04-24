---
title: Tuotevariantin numeroiden ja nimien nimikkeistö
description: Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli].
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 1acdd51645fad3bf0d6bb484afc24675f144b1d9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208544"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="46dbf-103">Tuotevariantin numeroiden ja nimien nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="46dbf-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46dbf-104">Tässä aiheessa kuvataan, miten tuotenumeroiden nimikkeistö määritetään korvaamaan kiinteän muodon [päätuotteen numero - konfiguraatio - koko - väri - malli].</span><span class="sxs-lookup"><span data-stu-id="46dbf-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="46dbf-105">Uusi nimikkeistö sisältää kohdennetun muodon, joka sisältää päätuotteen numeron, aktiiviset tuotedimensiot ja haluamasi tekstierottimet.</span><span class="sxs-lookup"><span data-stu-id="46dbf-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="46dbf-106">Myös tuotenimille voi luoda nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="46dbf-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="46dbf-107">Voit myös luoda nimikkeistön konfiguraatioiden tunnistamiseksi, jotka on luotu poissulkevan tuotekonfiguraattorin avulla.</span><span class="sxs-lookup"><span data-stu-id="46dbf-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="46dbf-108">Nämä nimikkeistöt voivat sisältää valitsemiasi määritteitä.</span><span class="sxs-lookup"><span data-stu-id="46dbf-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="46dbf-109">Tuotevariantin numeroiden ja nimien uusien nimikkeistöjen avulla voi sisällyttää segmenttejä tuotevarianttien tunnuksiin.</span><span class="sxs-lookup"><span data-stu-id="46dbf-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="46dbf-110">Nämä segmentit voivat sisältää päätuotenumeron ja nimen, tuotedimensioiden tunnukset ja nimet, numerosarjat, tekstivakioita ja määritteitä.</span><span class="sxs-lookup"><span data-stu-id="46dbf-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="46dbf-111">Kun luot myyntitilauksen tai ostotilauksen, löydät nopeasti tietyt tuotevariantit tämän toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="46dbf-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="46dbf-112">Sekä tuotevariantin numeroille että nimille voi luoda nimikkeistöjä **Tuotenimikkeistö**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="46dbf-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="46dbf-113">Avaa tämä sivu valitsemalla **Tuotetietojen hallinta** &gt; **Asetukset**.</span><span class="sxs-lookup"><span data-stu-id="46dbf-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="46dbf-114">Ennalta määritettyjen tuotevarianttien nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="46dbf-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="46dbf-115">Tuotevariantit luodaan päätuotteelle jollain kolmesta määritysmenetelmästä:</span><span class="sxs-lookup"><span data-stu-id="46dbf-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="46dbf-116">Ennalta määritetyt variantit</span><span class="sxs-lookup"><span data-stu-id="46dbf-116">Predefined variants</span></span>
-   <span data-ttu-id="46dbf-117">Rajoitukseen perustuva</span><span class="sxs-lookup"><span data-stu-id="46dbf-117">Constraint-based</span></span>
-   <span data-ttu-id="46dbf-118">Dimensioon perustuva</span><span class="sxs-lookup"><span data-stu-id="46dbf-118">Dimension-based</span></span>

<span data-ttu-id="46dbf-119">Jokaisella tuotevariantilla on numero ja nimi, ja tuotevariantin numeroiden nimikkeistöjen avulla voi valita segmentit, jotka sisällytetään tuotevariantin numeroihin tai nimiin.</span><span class="sxs-lookup"><span data-stu-id="46dbf-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="46dbf-120">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="46dbf-121">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="46dbf-121">Product master number</span></span>
-   <span data-ttu-id="46dbf-122">Päätuotteen nimi</span><span class="sxs-lookup"><span data-stu-id="46dbf-122">Product master name</span></span>
-   <span data-ttu-id="46dbf-123">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="46dbf-123">Number sequence value</span></span>
-   <span data-ttu-id="46dbf-124">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="46dbf-124">Text constant</span></span>
-   <span data-ttu-id="46dbf-125">Tuotedimensiot</span><span class="sxs-lookup"><span data-stu-id="46dbf-125">Product dimensions</span></span>
    -   <span data-ttu-id="46dbf-126">Konfiguraation tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="46dbf-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="46dbf-127">Värin tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="46dbf-127">Color ID or name</span></span>
    -   <span data-ttu-id="46dbf-128">Koon tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="46dbf-128">Size ID or name</span></span>
    -   <span data-ttu-id="46dbf-129">Tyylin tunnus tai nimi</span><span class="sxs-lookup"><span data-stu-id="46dbf-129">Style ID or name</span></span>

<span data-ttu-id="46dbf-130">Kun olet määrittänyt tuotevariantin numeron nimikkeistön, voit yhdistää sen tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="46dbf-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="46dbf-131">Tämän jälkeen kaikki tähän tuotedimensioryhmään viittaavat päätuotteet määritetään tuotevariantin numeroille nimikkeistön mukaan.</span><span class="sxs-lookup"><span data-stu-id="46dbf-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="46dbf-132">Tuotevariantin nimien nimikkeistöjä ei kuitenkaan voi yhdistää tuotedimensioryhmiin.</span><span class="sxs-lookup"><span data-stu-id="46dbf-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="46dbf-133">Voit myös yhdistää tuotevariantin tunnuksen nimikkeistön suoraan päätuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="46dbf-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="46dbf-134">Tässä tapauksessa päätuotteeseen kuuluvat tuotevariantit yhdistetään tuotevariantin numeroihin ja nimiin nimikkeistöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="46dbf-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="46dbf-135">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="46dbf-135">Example</span></span>

<span data-ttu-id="46dbf-136">T-paitaa (TS1234) valmistetaan kolme eri kokoa (S, M, L), neljä eri väriä (punainen, vihreä, sininen, keltainen) ja kaksi mallia (poolo, V).</span><span class="sxs-lookup"><span data-stu-id="46dbf-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="46dbf-137">Mahdollisia tuotevariantteja on siis 24 (= 3 × 4 × 2).</span><span class="sxs-lookup"><span data-stu-id="46dbf-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="46dbf-138">Voit luoda tuotevariantin numeron nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="46dbf-139">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="46dbf-139">Product master number</span></span>
2.  <span data-ttu-id="46dbf-140">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="46dbf-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="46dbf-141">Väri</span><span class="sxs-lookup"><span data-stu-id="46dbf-141">Color</span></span>
4.  <span data-ttu-id="46dbf-142">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="46dbf-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="46dbf-143">Koko</span><span class="sxs-lookup"><span data-stu-id="46dbf-143">Size</span></span>
6.  <span data-ttu-id="46dbf-144">Tekstivakio: -</span><span class="sxs-lookup"><span data-stu-id="46dbf-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="46dbf-145">Tyyli</span><span class="sxs-lookup"><span data-stu-id="46dbf-145">Style</span></span>

<span data-ttu-id="46dbf-146">Tässä tapauksessa tuotevariantin numero ominaisuuksille punainen, S, poolo, T-paita TS1234-punainen-S-poolo.</span><span class="sxs-lookup"><span data-stu-id="46dbf-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="46dbf-147">Poissulkeva konfiguraationimikkeistö</span><span class="sxs-lookup"><span data-stu-id="46dbf-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="46dbf-148">Poissulkeville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="46dbf-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="46dbf-149">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="46dbf-150">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="46dbf-150">Number sequence value</span></span>
-   <span data-ttu-id="46dbf-151">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="46dbf-151">Text constant</span></span>
-   <span data-ttu-id="46dbf-152">Määritteen arvo</span><span class="sxs-lookup"><span data-stu-id="46dbf-152">Attribute value</span></span>

<span data-ttu-id="46dbf-153">Jokaisella tuotemääritysmallin komponentilla voi olla oma konfiguraationimikkeistö.</span><span class="sxs-lookup"><span data-stu-id="46dbf-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="46dbf-154">Vain komponenttiin kuuluvia määritteitä saa käyttää.</span><span class="sxs-lookup"><span data-stu-id="46dbf-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="46dbf-155">Alikomponenttien tai käyttäjävaatimuksien määritteitä ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="46dbf-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="46dbf-156">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="46dbf-156">Example</span></span>

<span data-ttu-id="46dbf-157">Tuotemääritysmallin juurikomponentissa on seuraavat kaksi määritettä:</span><span class="sxs-lookup"><span data-stu-id="46dbf-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="46dbf-158">Materiaali (muovi, puu, teräs)</span><span class="sxs-lookup"><span data-stu-id="46dbf-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="46dbf-159">Pituus (10... 100)</span><span class="sxs-lookup"><span data-stu-id="46dbf-159">Length (10...100)</span></span>

<span data-ttu-id="46dbf-160">Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="46dbf-161">Määritteen arvo: materiaali</span><span class="sxs-lookup"><span data-stu-id="46dbf-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="46dbf-162">Tekstivakio: AAA</span><span class="sxs-lookup"><span data-stu-id="46dbf-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="46dbf-163">Määritteen arvo: pituus</span><span class="sxs-lookup"><span data-stu-id="46dbf-163">Attribute value: Length</span></span>

<span data-ttu-id="46dbf-164">Tässä tapauksessa puumateriaalin konfiguraatiotunnus, jonka pituus on, on WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="46dbf-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="46dbf-165">Dimensioihin perustuva konfiguraationimikkeistö</span><span class="sxs-lookup"><span data-stu-id="46dbf-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="46dbf-166">Dimensioihin perustuville konfiguraatioille voi luoda konfiguraation tuotedimension kohdistetun nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="46dbf-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="46dbf-167">**Tuotenimikkeistö**-sivulla voi seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="46dbf-168">Numerosarjan arvo</span><span class="sxs-lookup"><span data-stu-id="46dbf-168">Number sequence value</span></span>
-   <span data-ttu-id="46dbf-169">Tekstivakio</span><span class="sxs-lookup"><span data-stu-id="46dbf-169">Text constant</span></span>
-   <span data-ttu-id="46dbf-170">Konfiguraatioryhmän nimike</span><span class="sxs-lookup"><span data-stu-id="46dbf-170">Configuration group item</span></span>

<span data-ttu-id="46dbf-171">Konfiguraationimikkeistö voidaan määrittää tuoterakenteelle.</span><span class="sxs-lookup"><span data-stu-id="46dbf-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="46dbf-172">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="46dbf-172">Example</span></span>

<span data-ttu-id="46dbf-173">Tuoterakenne sisältää neljä tuoterakenteen riviä, jotka on jaettu kahteen konfiguraatioryhmään:</span><span class="sxs-lookup"><span data-stu-id="46dbf-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="46dbf-174">Tuoterakennerivi: M0007, vakiokaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="46dbf-175">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="46dbf-176">Tuoterakennerivi: M0008, korkealuokkainen kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="46dbf-177">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="46dbf-178">Tuoterakennerivi: M0021, kaiuttimen etukangas</span><span class="sxs-lookup"><span data-stu-id="46dbf-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="46dbf-179">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="46dbf-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="46dbf-180">Tuoterakennerivi: M0022, kaiuttimen teräsverkko</span><span class="sxs-lookup"><span data-stu-id="46dbf-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="46dbf-181">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="46dbf-181">Configuration group: Front grill</span></span>

<span data-ttu-id="46dbf-182">Voit luoda konfiguraation nimikkeistön, jolla on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="46dbf-183">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="46dbf-184">Tekstivakio: &</span><span class="sxs-lookup"><span data-stu-id="46dbf-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="46dbf-185">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="46dbf-185">Configuration group: Front grill</span></span>

<span data-ttu-id="46dbf-186">Tässä tapauksessa etukankaalla varustetun vakiokaiutinkotelon konfiguraatiotunnus on M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="46dbf-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="46dbf-187">Tuotevarianttien ja konfiguraatioiden yhdistelmän nimikkeistö</span><span class="sxs-lookup"><span data-stu-id="46dbf-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="46dbf-188">Jos käytät poissulkevaa tai dimensioihin perustuvaa määritysmenetelmää päätuotteen tuotevarianttien määritykseen, tuotevarianttien numerot voivat sisältää konfigurointidimension nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="46dbf-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="46dbf-189">Jos haluat konfiguroida variantit, noudata seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="46dbf-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="46dbf-190">Määritä **Tuotenimikkeistö**-sivulla tuotevariantin numeron nimikkeistö, joka sisältää konfigurointidimension.</span><span class="sxs-lookup"><span data-stu-id="46dbf-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="46dbf-191">Määritä nimikkeistö tuotedimensioryhmälle, jolla on konfigurointidimensio.</span><span class="sxs-lookup"><span data-stu-id="46dbf-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="46dbf-192">Määritä konfiguraationimikkeistö komponenteille tai tuoterakenteille, jota käytetään tuotevarianttien konfiguroimisessa.</span><span class="sxs-lookup"><span data-stu-id="46dbf-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="46dbf-193">Myös tuotevariantin nimille voi luoda nimikkeistön.</span><span class="sxs-lookup"><span data-stu-id="46dbf-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="46dbf-194">Tuotevariantin nimet voidaan konfiguroida niin, että ne sisältävät konfiguraation tunnuksen tai nimen.</span><span class="sxs-lookup"><span data-stu-id="46dbf-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="46dbf-195">Esimerkki poissulkevasta konfiguraatiosta</span><span class="sxs-lookup"><span data-stu-id="46dbf-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="46dbf-196">Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="46dbf-197">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="46dbf-197">Product master number</span></span>
2.  <span data-ttu-id="46dbf-198">Tekstivakio \_</span><span class="sxs-lookup"><span data-stu-id="46dbf-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="46dbf-199">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="46dbf-199">Configuration</span></span>

<span data-ttu-id="46dbf-200">Konfiguraationimikkeistö sisältää seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="46dbf-201">Määritteen arvo: materiaali</span><span class="sxs-lookup"><span data-stu-id="46dbf-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="46dbf-202">Tekstivakio: AAA</span><span class="sxs-lookup"><span data-stu-id="46dbf-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="46dbf-203">Määritteen arvo: pituus</span><span class="sxs-lookup"><span data-stu-id="46dbf-203">Attribute value: Length</span></span>

<span data-ttu-id="46dbf-204">Syötä segmenteille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="46dbf-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="46dbf-205">Päätuotteen numero = **M0099**</span><span class="sxs-lookup"><span data-stu-id="46dbf-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="46dbf-206">Materiaali = **muovi**</span><span class="sxs-lookup"><span data-stu-id="46dbf-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="46dbf-207">Pituus = **12**</span><span class="sxs-lookup"><span data-stu-id="46dbf-207">Length = **12**</span></span>

<span data-ttu-id="46dbf-208">Tässä tapauksessa tuotevariantin numero on M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="46dbf-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="46dbf-209">Esimerkki dimensioihin perustuvasta konfiguraatiosta</span><span class="sxs-lookup"><span data-stu-id="46dbf-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="46dbf-210">Tässä esimerkissä voit käyttää tuotevariantin numeron nimikkeistöä, jossa on seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="46dbf-211">Päätuotteen numero</span><span class="sxs-lookup"><span data-stu-id="46dbf-211">Product master number</span></span>
2.  <span data-ttu-id="46dbf-212">Tekstivakio //</span><span class="sxs-lookup"><span data-stu-id="46dbf-212">Text constant "//"</span></span>
3.  <span data-ttu-id="46dbf-213">Konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="46dbf-213">Configuration</span></span>

<span data-ttu-id="46dbf-214">Konfiguraationimikkeistö sisältää seuraavat segmentit:</span><span class="sxs-lookup"><span data-stu-id="46dbf-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="46dbf-215">Konfiguraatioryhmä: kaiutinkaappi</span><span class="sxs-lookup"><span data-stu-id="46dbf-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="46dbf-216">Tekstivakio: &</span><span class="sxs-lookup"><span data-stu-id="46dbf-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="46dbf-217">Konfiguraatioryhmä: teräsverkkko</span><span class="sxs-lookup"><span data-stu-id="46dbf-217">Configuration group: Front grill</span></span>

<span data-ttu-id="46dbf-218">Syötä segmenteille seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="46dbf-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="46dbf-219">Päätuotteen numero = **D0123**</span><span class="sxs-lookup"><span data-stu-id="46dbf-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="46dbf-220">Kaiutinkaappi = **M0008**</span><span class="sxs-lookup"><span data-stu-id="46dbf-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="46dbf-221">Etusäleikkö = **M0022**</span><span class="sxs-lookup"><span data-stu-id="46dbf-221">Front grill = **M0022**</span></span>

<span data-ttu-id="46dbf-222">Tässä tapauksessa tuotevariantin numero on D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="46dbf-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="46dbf-223">Numerointiristiriidat</span><span class="sxs-lookup"><span data-stu-id="46dbf-223">Numbering conflicts</span></span>
<span data-ttu-id="46dbf-224">Joissakin tapauksissa tuotevariantin numeron määritetty nimikkeistö ei tuota yksilöiviä tuotevariantin numeroita.</span><span class="sxs-lookup"><span data-stu-id="46dbf-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="46dbf-225">Esimerkiksi tuotevariantin numerot eivät ole yksilöiviä, jos yksi aktiivinen tuotedimensio ei sisälly päätuotteen nimikkeistöön, joka käyttää esimääritettyä variantin määritysmenetelmää.</span><span class="sxs-lookup"><span data-stu-id="46dbf-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="46dbf-226">Ristiriitatilanteiden käsittelytapa vaihtelee määritysmenetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="46dbf-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="46dbf-227">Ennalta määritetyt variantit</span><span class="sxs-lookup"><span data-stu-id="46dbf-227">Predefined variants</span></span>

<span data-ttu-id="46dbf-228">Jos yrität luoda manuaalisesti tai automaattisesti tuotevariantteja, joista vähintään yksi päättyy samaan tuotevariantin numeroon, tapahtuu virhe.</span><span class="sxs-lookup"><span data-stu-id="46dbf-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="46dbf-229">Voit välttää tämän käyttämällä tuotedimensioryhmässä kaikkia aktiivisia tuotedimensioita.</span><span class="sxs-lookup"><span data-stu-id="46dbf-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="46dbf-230">Vaihtoehtoisesti voit ottaa mukaan numerosarjat, joiden avulla varmistetaan, että tuotevariantin numerot ovat yksilöiviä.</span><span class="sxs-lookup"><span data-stu-id="46dbf-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="46dbf-231">Poissulkevat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="46dbf-231">Constraint-based configurations</span></span>

<span data-ttu-id="46dbf-232">Nimikkeistön mukaan järjestelmä yrittää määrittää ei-yksilöivän tuotevariantin numeron konfiguraatioon.</span><span class="sxs-lookup"><span data-stu-id="46dbf-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="46dbf-233">Tällöin järjestelmä käyttää sen sijaan konfigurointidimension numerosarjaa tuotevariantin numerona, ja näyttöön tulee varoitus.</span><span class="sxs-lookup"><span data-stu-id="46dbf-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="46dbf-234">Voit välttää tämän, kun nimikkeistössä on riittävästi määritteitä. Tällöin yksilöivien tuotevariantin numeroiden varmistaminen on helpompaa.</span><span class="sxs-lookup"><span data-stu-id="46dbf-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="46dbf-235">Varmista myös, että komponentin **Käytä uudelleen** -vaihtoehto on käytössä.</span><span class="sxs-lookup"><span data-stu-id="46dbf-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="46dbf-236">Dimensioihin perustuvat konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="46dbf-236">Dimension-based configurations</span></span>

<span data-ttu-id="46dbf-237">Konfigurointiprosessin yhden vaiheen aikana järjestelmä ehdottaa konfiguraatioarvoa nimikkeistön mukaan.</span><span class="sxs-lookup"><span data-stu-id="46dbf-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="46dbf-238">Et voi muuttaa konfigurointiarvoa manuaalisesti tässä vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="46dbf-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="46dbf-239">Kun konfiguraatio tallennetaan, järjestelmä tarkistaa, onko konfiguraation arvo yksilöllinen.</span><span class="sxs-lookup"><span data-stu-id="46dbf-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="46dbf-240">Jos syötetty arvo ei ole yksilöivä, näyttöön tulee virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="46dbf-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="46dbf-241">Voit tallentaa konfiguraation syöttämällä yksilöivän konfiguraatioarvon.</span><span class="sxs-lookup"><span data-stu-id="46dbf-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="46dbf-242">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="46dbf-242">Additional resources</span></span>
--------

[<span data-ttu-id="46dbf-243">Luo tuotenumeroiden nimikkeistö esimääritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="46dbf-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="46dbf-244">Tuotenumeroiden nimikkeistön luominen konfiguroiduille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="46dbf-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)

