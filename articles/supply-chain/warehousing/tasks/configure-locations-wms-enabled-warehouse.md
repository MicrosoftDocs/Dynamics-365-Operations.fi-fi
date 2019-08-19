---
title: Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa
description: Tässä opastuksessa selvitetään, miten voit määrittää sijaintiasetuset varastoon, jossa uusi varastonhallintajärjestelmä on otettu käyttöön. (Kyse on varastosta, jossa käytetään varastonhallinnan lisäprosesseja.)
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5df88f9ae7b07835db2911d55fae87f282826243
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847372"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="379a7-103">Sijaintien määrittäminen varastonhallintajärjestelmää käyttävässä varastossa</span><span class="sxs-lookup"><span data-stu-id="379a7-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="379a7-104">Tässä opastuksessa selvitetään, miten voit määrittää sijaintiasetuset varastoon, jossa uusi varastonhallintajärjestelmä on otettu käyttöön. (Kyse on varastosta, jossa käytetään varastonhallinnan lisäprosesseja.)</span><span class="sxs-lookup"><span data-stu-id="379a7-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="379a7-105">Yleensä tämän prosessin tekee varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="379a7-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="379a7-106">Voit suorittaa opastuksen USMF-demoyrityksen tiedoilla tai käyttää omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="379a7-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="379a7-107">Edellytyksenä on, että vähintään yksi toimipaikka on määritetty.</span><span class="sxs-lookup"><span data-stu-id="379a7-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="379a7-108">Luo uusi varasto</span><span class="sxs-lookup"><span data-stu-id="379a7-108">Create a new warehouse</span></span>
1. <span data-ttu-id="379a7-109">Valitse Varastot.</span><span class="sxs-lookup"><span data-stu-id="379a7-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="379a7-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-110">Click New.</span></span>
3. <span data-ttu-id="379a7-111">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="379a7-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="379a7-113">Kirjoita arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="379a7-114">Laajenna tai tiivistä Varasto-osa.</span><span class="sxs-lookup"><span data-stu-id="379a7-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="379a7-115">Valitse Käyttäjän varastonhallintaprosessien virheloki -asetukseksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="379a7-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="379a7-116">Voit suorittaa tällä asetuksella varastoinnin lisäprosesseja varastotyön ja mobiililaitteiden avulla.</span><span class="sxs-lookup"><span data-stu-id="379a7-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="379a7-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="379a7-118">Määritä sijainnin muoto</span><span class="sxs-lookup"><span data-stu-id="379a7-118">Define a location format</span></span>
1. <span data-ttu-id="379a7-119">Valitse Sijainnin muodot.</span><span class="sxs-lookup"><span data-stu-id="379a7-119">Go to Location formats.</span></span>
    * <span data-ttu-id="379a7-120">Sijainnin muodot ovat nimeämisjärjestelmä, jolla luodaan yksilölliset ja yhtenäiset nimet varastossa käytettäville eri sijaintien lokeropaikoille.</span><span class="sxs-lookup"><span data-stu-id="379a7-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="379a7-121">Erottimien käyttö sijaintimuodon osana voi helpottaa sijainnin osien, kuten käytävänumeron, tunnistamista.</span><span class="sxs-lookup"><span data-stu-id="379a7-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="379a7-122">Tässä esimerkissä luotavassa nimessä on neljä osaa.</span><span class="sxs-lookup"><span data-stu-id="379a7-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="379a7-123">Ne voivat olla esimerkiksi käytävä, teline, hylly ja lokero.</span><span class="sxs-lookup"><span data-stu-id="379a7-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="379a7-124">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-124">Click New.</span></span>
3. <span data-ttu-id="379a7-125">Kirjoita Sijainnin muoto -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="379a7-126">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="379a7-127">Kirjoita Segmentin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="379a7-128">Tämä kuvaa, mihin sijainnin nimen ensimmäinen osa viittaa.</span><span class="sxs-lookup"><span data-stu-id="379a7-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="379a7-129">Se voi olla esimerkiksi käytävä.</span><span class="sxs-lookup"><span data-stu-id="379a7-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="379a7-130">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="379a7-131">Tämä määrittää, kuinka monta merkkiä sijainnin nimen tässä osassa on oltava.</span><span class="sxs-lookup"><span data-stu-id="379a7-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="379a7-132">Huomaa, että kaikki osat, myös erottimet, sisältävän nimen enimmäispituus on 10 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="379a7-133">Kirjoita Erotin-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="379a7-134">Tämä määrittää, mitä merkkiä tai symbolia käytetään nimen ensimmäisen ja toisen osan välissä.</span><span class="sxs-lookup"><span data-stu-id="379a7-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="379a7-135">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-135">Click New.</span></span>
9. <span data-ttu-id="379a7-136">Kirjoita Segmentin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="379a7-137">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="379a7-138">Kirjoita Erotin-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="379a7-139">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-139">Click New.</span></span>
13. <span data-ttu-id="379a7-140">Kirjoita Segmentin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="379a7-141">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="379a7-142">Kirjoita Erotin-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="379a7-143">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-143">Click New.</span></span>
17. <span data-ttu-id="379a7-144">Kirjoita Segmentin kuvaus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="379a7-145">Lisää Pituus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="379a7-146">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="379a7-146">Click Save.</span></span>
20. <span data-ttu-id="379a7-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="379a7-148">Määritä sijaintityypit</span><span class="sxs-lookup"><span data-stu-id="379a7-148">Define location types</span></span>
1. <span data-ttu-id="379a7-149">Valitse Sijainnin tyypit.</span><span class="sxs-lookup"><span data-stu-id="379a7-149">Go to Location types.</span></span>
    * <span data-ttu-id="379a7-150">Sijainnin tyyppejä voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="379a7-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="379a7-151">Ainakin väliaikaiset ja lopulliset lähetyssijainnit on luotava, jotta lähtevä varastonhallintaprosessi voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="379a7-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="379a7-152">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-152">Click New.</span></span>
3. <span data-ttu-id="379a7-153">Kirjoita arvo Sijainnin tyyppi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="379a7-154">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="379a7-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="379a7-156">Määritä sijaintiprofiili</span><span class="sxs-lookup"><span data-stu-id="379a7-156">Define location profile</span></span>
1. <span data-ttu-id="379a7-157">Valitse Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="379a7-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="379a7-158">Sijaintiprofiilien määritys on erittäin tärkeä.</span><span class="sxs-lookup"><span data-stu-id="379a7-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="379a7-159">Ryhmiteltyjä sijaintien kapasiteettia voidaan hallita täällä. Lisäksi vodaan hallita käytäntöjä, jotka liittyvät varastoitavan varaston valitsemiseen ja varastointitapaan.</span><span class="sxs-lookup"><span data-stu-id="379a7-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="379a7-160">Sijaintiprofiileja voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="379a7-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="379a7-161">Ainakin käyttäjän sijaintiprofiili on luotava, jotta varastonhallintaprosessit voidaan ottaa käyttöön.</span><span class="sxs-lookup"><span data-stu-id="379a7-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="379a7-162">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-162">Click New.</span></span>
3. <span data-ttu-id="379a7-163">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="379a7-164">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="379a7-165">Avaa haku napsauttamalla Sijainnin muoto -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="379a7-166">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="379a7-167">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="379a7-168">Avaa haku napsauttamalla Sijainnin tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="379a7-169">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="379a7-170">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="379a7-171">Valitse Salli yhdistetyt varastotilat -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="379a7-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="379a7-172">Ota tämä asetus käyttöön, jos haluat sallia yhdistetyt varastotila-arvot sijainneissa, jotka ryhmitetään tällä sijaintiprofiililla.</span><span class="sxs-lookup"><span data-stu-id="379a7-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="379a7-173">Valitse Erän käsittelypäivien ohitussäännöt -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="379a7-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="379a7-174">Ota tämä asetus käyttöön, jos haluat ohittaa säännön päivistä, jonka varastoerän vanhentumispäivämäärät voivat erota. Tällä tavoin voidaan yhdistää varastoeriä, joissa tätä sääntöä ei noudateta.</span><span class="sxs-lookup"><span data-stu-id="379a7-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="379a7-175">Valitse Salli inventointi -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="379a7-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="379a7-176">Ottamalla tämän asetuksen käyttöön sallit inventoinnin käsittelyn kaikissa sijainneissa, jotka tullaan ryhmittelemään tällä sijaintiprofiililla.</span><span class="sxs-lookup"><span data-stu-id="379a7-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="379a7-177">Laajenna tai tiivistä Dimensiot-osa.</span><span class="sxs-lookup"><span data-stu-id="379a7-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="379a7-178">Dimensiot-välilehden avulla voit määrittää parametrit ja menetelmät, joilla voidaan laskea kuorman kapasiteetti tarkasti kussakin sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="379a7-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="379a7-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="379a7-180">Ota varastonhallinnan parametrit käyttöön</span><span class="sxs-lookup"><span data-stu-id="379a7-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="379a7-181">Valitse Varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="379a7-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="379a7-182">Varastontyön käsittely edellyttää, että käyttäjän profiilityypin, väliaikaissijainnin tyypin ja lopullisen toimitussijainnin tyypin parametrit määritetään. Heti kun lähtevä prosessi päättyy määrittämässäsi lopullisen toimitussijainnin tyypissä, liittyvien lähtevien tapahtumien tilaksi päivittyy Keräilty.</span><span class="sxs-lookup"><span data-stu-id="379a7-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="379a7-183">Laajenna tai tiivistä Sijaintiprofiilit-osa.</span><span class="sxs-lookup"><span data-stu-id="379a7-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="379a7-184">Avaa haku napsauttamalla Käyttäjän sijainti -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="379a7-185">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="379a7-186">Laajenna tai tiivistä Sijaintityypit-osa.</span><span class="sxs-lookup"><span data-stu-id="379a7-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="379a7-187">Avaa haku napsauttamalla Vaiheistussijainnin tyyppi -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="379a7-188">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="379a7-189">Avaa haku napsauttamalla Lopullinen lähetyssijainti -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="379a7-190">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="379a7-191">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="379a7-192">Määritä varastovyöhykeryhmät</span><span class="sxs-lookup"><span data-stu-id="379a7-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="379a7-193">Valitse Varastovyöhykeryhmät.</span><span class="sxs-lookup"><span data-stu-id="379a7-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="379a7-194">Varastovyöhykkeitä voidaan käyttää suodatusasetuksina, joilla voi ohjata erilaisia varastonhallintaprosesseja.</span><span class="sxs-lookup"><span data-stu-id="379a7-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="379a7-195">Vyöhykeryhmä on luotava ennen vyöhykkeen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="379a7-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="379a7-196">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-196">Click New.</span></span>
3. <span data-ttu-id="379a7-197">Kirjoita Vyöhykeryhmän tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="379a7-198">Kirjoita Vyöhykeryhmän nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="379a7-199">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="379a7-200">Määritä varastovyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="379a7-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="379a7-201">Valitse Vyöhykkeet.</span><span class="sxs-lookup"><span data-stu-id="379a7-201">Go to Zones.</span></span>
2. <span data-ttu-id="379a7-202">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-202">Click New.</span></span>
3. <span data-ttu-id="379a7-203">Kirjoita Vyöhyketunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="379a7-204">Kirjoita Vyöhykkeen nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="379a7-205">Avaa haku napsauttamalla Vyöhykeryhmän tunnus -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="379a7-206">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="379a7-207">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="379a7-208">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="379a7-209">Luo sijainnit ohjatulla sijaintien asennustoiminnolla</span><span class="sxs-lookup"><span data-stu-id="379a7-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="379a7-210">Valitse Ohjattu sijaintien asennustoiminto.</span><span class="sxs-lookup"><span data-stu-id="379a7-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="379a7-211">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="379a7-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="379a7-212">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="379a7-213">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="379a7-214">Avaa haku napsauttamalla Vyöhyketunnus-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="379a7-215">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="379a7-216">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="379a7-217">Avaa haku napsauttamalla Sijainnin profiilitunnus -kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="379a7-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="379a7-218">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="379a7-219">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="379a7-220">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="379a7-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="379a7-221">Lisää Ensimmäinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="379a7-222">Ensimmäinen numero- ja Viimeinen numero -kentät määrittävät, kuinka monta sijaintia luodaan.</span><span class="sxs-lookup"><span data-stu-id="379a7-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="379a7-223">Jos esimerkiksi sijainnin muodon kaikkien neljän rivin Ensimmäinen numero -arvoksi on määritetty 1 ja Viimeinen numero -arvoksi 3, luodaan 81 sijaintia (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="379a7-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="379a7-224">Lisää Viimeinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="379a7-225">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="379a7-226">Lisää Ensimmäinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="379a7-227">Lisää Viimeinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="379a7-228">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="379a7-229">Lisää Ensimmäinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="379a7-230">Lisää Viimeinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="379a7-231">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="379a7-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="379a7-232">Lisää Ensimmäinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="379a7-233">Lisää Viimeinen numero -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="379a7-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="379a7-234">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="379a7-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="379a7-235">Luo sijainnit manuaalisesti</span><span class="sxs-lookup"><span data-stu-id="379a7-235">Create locations manually</span></span>
1. <span data-ttu-id="379a7-236">Valitse Sijainnit.</span><span class="sxs-lookup"><span data-stu-id="379a7-236">Go to Locations.</span></span>
    * <span data-ttu-id="379a7-237">Sijaintien luonti varastoon manuaalisesti on helppoa.</span><span class="sxs-lookup"><span data-stu-id="379a7-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="379a7-238">Sijainnin nimi ja profiilitunnus ovat pakollisia arvoja.</span><span class="sxs-lookup"><span data-stu-id="379a7-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="379a7-239">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-239">Click New.</span></span>
3. <span data-ttu-id="379a7-240">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="379a7-241">Kirjoita arvo kenttään Sijainti.</span><span class="sxs-lookup"><span data-stu-id="379a7-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="379a7-242">Huomaa, että olet luomassa uutta sijaintia, joten sinun on kirjoitettava uusi yksilöllinen nimi. Et siis voi valita aiemmin luotua nimeä.</span><span class="sxs-lookup"><span data-stu-id="379a7-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="379a7-243">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="379a7-244">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="379a7-245">Määritä pakkauskokoluokat</span><span class="sxs-lookup"><span data-stu-id="379a7-245">Define Pack size categories</span></span>
1. <span data-ttu-id="379a7-246">Valitse Pakkauskokoluokat.</span><span class="sxs-lookup"><span data-stu-id="379a7-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="379a7-247">Pakkauskokoluokkia voidaan käyttää ryhmittämään nimikkeitä, joiden fyysinen pakkauskoko on lähellä toisiaan.</span><span class="sxs-lookup"><span data-stu-id="379a7-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="379a7-248">Tässä esimerkissä pakkauskokoluokan avulla hallitaan keräilysijaintien kapasiteettia tietyllä varastovyöhykkeellä.</span><span class="sxs-lookup"><span data-stu-id="379a7-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="379a7-249">Huomaa, että vapautetulle tuoteyksikölle on määritettävä pakkauskokoluokan tunnus, jotta sitä voi käyttää osana varastointirajoitusten käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="379a7-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="379a7-250">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-250">Click New.</span></span>
3. <span data-ttu-id="379a7-251">Kirjoita Pakkauskokoluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="379a7-252">Kirjoita Pakkauskokoluokan nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="379a7-253">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="379a7-254">Määritä toimipaikan varastointirajoitukset</span><span class="sxs-lookup"><span data-stu-id="379a7-254">Define location stocking limits</span></span>
1. <span data-ttu-id="379a7-255">Valitse Sijainnin varastointirajoitukset.</span><span class="sxs-lookup"><span data-stu-id="379a7-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="379a7-256">Sijainnin varastointirajoitukset auttavat varmistamaan, että ei luoda työtä, jossa varasto pyydetään sijoittamaan sijaintiin, jonka fyysinen kapasiteetti ei ole riittävä.</span><span class="sxs-lookup"><span data-stu-id="379a7-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="379a7-257">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-257">Click New.</span></span>
3. <span data-ttu-id="379a7-258">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="379a7-259">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="379a7-260">Kirjoita Pakkauskokoluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="379a7-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="379a7-261">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="379a7-262">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="379a7-262">Click Save.</span></span>
8. <span data-ttu-id="379a7-263">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="379a7-264">Määritä kiinteät keräilysijainnit</span><span class="sxs-lookup"><span data-stu-id="379a7-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="379a7-265">Valitse Kiinteät sijainnit.</span><span class="sxs-lookup"><span data-stu-id="379a7-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="379a7-266">Voit määrittää sijaintien käytön tuotteen tai tuotevariantin mukaan.</span><span class="sxs-lookup"><span data-stu-id="379a7-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="379a7-267">Samalle tuotteelle voi luoda samaan varastoon useita kiinteitä sijainteja.</span><span class="sxs-lookup"><span data-stu-id="379a7-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="379a7-268">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="379a7-268">Click New.</span></span>
3. <span data-ttu-id="379a7-269">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="379a7-270">Kirjoita arvo Varasto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="379a7-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="379a7-271">Avaa haku valitsemalla Sijainnit-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="379a7-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="379a7-272">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="379a7-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="379a7-273">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="379a7-273">Close the page.</span></span>

