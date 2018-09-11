--- 
title: "Määritä laatutilaukset"
description: "Seuraavissa vaiheissa kerrotaan, miten laadunhallintaprosessi otetaan käyttöön, kun saapuva varasto on tarkistettava heti saapumisen yhteydessä tehtävän rekisteröinnin jälkeen."
author: perlynne
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c36e35f45709d32db7bc1a625d4bcc30cf543fb0
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="807e9-103">Määritä laatutilaukset</span><span class="sxs-lookup"><span data-stu-id="807e9-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="807e9-104">Seuraavissa vaiheissa kerrotaan, miten laadunhallintaprosessi otetaan käyttöön, kun saapuva varasto on tarkistettava heti saapumisen yhteydessä tehtävän rekisteröinnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="807e9-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="807e9-105">Laatupäällikkö tekee yleensä tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="807e9-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="807e9-106">Prosessi sisältää laaturyhmän luomisen, kerättävien nimikkeiden määrittämisen ja testiryhmän, jonne kerätään laaturyhmän nimikkeille suoritettavat testit.</span><span class="sxs-lookup"><span data-stu-id="807e9-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="807e9-107">Voit suorittaa tämän ohjauksen esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="807e9-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="807e9-108">Laadunhallinnan ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="807e9-108">Enable quality management</span></span>
1. <span data-ttu-id="807e9-109">Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="807e9-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="807e9-110">Valitse Laadunhallinta-välilehti.</span><span class="sxs-lookup"><span data-stu-id="807e9-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="807e9-111">Määritä Käytä laadunhallintaa -vaihtoehdon arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="807e9-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="807e9-112">Valitse Raportin asetukset.</span><span class="sxs-lookup"><span data-stu-id="807e9-112">Click Report setup.</span></span>
    * <span data-ttu-id="807e9-113">Laadunhallinnan raportin määritys on jo määritetty USMF-yritykselle.</span><span class="sxs-lookup"><span data-stu-id="807e9-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="807e9-114">Jos tätä ei ole tehty, lisäät uusia rivejä tässä erityyppisille raporttityypeille ja valitset kullakin raportilla käytettävän asiakirjan tyypin.</span><span class="sxs-lookup"><span data-stu-id="807e9-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="807e9-115">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-115">Close the page.</span></span>
6. <span data-ttu-id="807e9-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="807e9-117">Testin luominen</span><span class="sxs-lookup"><span data-stu-id="807e9-117">Create a test</span></span>
1. <span data-ttu-id="807e9-118">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testit.</span><span class="sxs-lookup"><span data-stu-id="807e9-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="807e9-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-119">Click New.</span></span>
3. <span data-ttu-id="807e9-120">Kirjoita arvo Testi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="807e9-121">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="807e9-122">Valitse Tyyppi-kentässä Asetus.</span><span class="sxs-lookup"><span data-stu-id="807e9-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="807e9-123">Tässä esimerkissä valitaan Asetus-kohta, jolloin testitulokset on mahdollista liittää ennalta määrättyjen arvojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="807e9-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="807e9-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-124">Click Save.</span></span>
7. <span data-ttu-id="807e9-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="807e9-126">Testimuuttujien luominen ja testitulosten tallennustavan määrittämisen</span><span class="sxs-lookup"><span data-stu-id="807e9-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="807e9-127">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testimuuttujat.</span><span class="sxs-lookup"><span data-stu-id="807e9-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="807e9-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-128">Click New.</span></span>
3. <span data-ttu-id="807e9-129">Kirjoita arvo Muuttuja-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="807e9-130">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="807e9-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-131">Click Save.</span></span>
6. <span data-ttu-id="807e9-132">Valitse Tulokset.</span><span class="sxs-lookup"><span data-stu-id="807e9-132">Click Outcomes.</span></span>
7. <span data-ttu-id="807e9-133">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-133">Click New.</span></span>
8. <span data-ttu-id="807e9-134">Kirjoita arvo Tulos-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="807e9-135">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="807e9-136">Valitse Tuloksen tila -kentässä Hyväksytty.</span><span class="sxs-lookup"><span data-stu-id="807e9-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="807e9-137">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-137">Click Save.</span></span>
12. <span data-ttu-id="807e9-138">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-138">Click New.</span></span>
13. <span data-ttu-id="807e9-139">Kirjoita arvo Tulos-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="807e9-140">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="807e9-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-141">Click Save.</span></span>
16. <span data-ttu-id="807e9-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-142">Close the page.</span></span>
17. <span data-ttu-id="807e9-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="807e9-144">Nimikeotannan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="807e9-144">Set up item sampling</span></span>
1. <span data-ttu-id="807e9-145">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Nimikeotanta.</span><span class="sxs-lookup"><span data-stu-id="807e9-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="807e9-146">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-146">Click New.</span></span>
3. <span data-ttu-id="807e9-147">Kirjoita arvo Nimikeotanta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="807e9-148">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="807e9-149">Kirjoita numero Arvo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="807e9-150">Tämä arvo liittyy määrän määritykseen, joka valitaan viereisessä kentässä.</span><span class="sxs-lookup"><span data-stu-id="807e9-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="807e9-151">Laajenna tai tiivistä Prosessi-osa.</span><span class="sxs-lookup"><span data-stu-id="807e9-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="807e9-152">Valitse Täysi esto -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="807e9-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="807e9-153">Jos valitset tämän asetuksen, koko erä tai tilausrivin määrä estetään, jos testi epäonnistuu.</span><span class="sxs-lookup"><span data-stu-id="807e9-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="807e9-154">Jos tätä ei valita, vain laatutilauksen nimikkeet estetään.</span><span class="sxs-lookup"><span data-stu-id="807e9-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="807e9-155">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-155">Click Save.</span></span>
9. <span data-ttu-id="807e9-156">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="807e9-157">Laaturyhmän luominen</span><span class="sxs-lookup"><span data-stu-id="807e9-157">Create a quality group</span></span>
1. <span data-ttu-id="807e9-158">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Laaturyhmät.</span><span class="sxs-lookup"><span data-stu-id="807e9-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="807e9-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-159">Click New.</span></span>
3. <span data-ttu-id="807e9-160">Kirjoita arvo Laaturyhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="807e9-161">Käytä kuvaavaa nimeä, jonka avulla tunnistat, minkä tyyppisiä nimikkeitä ryhmä sisältää (otannan ehdot).</span><span class="sxs-lookup"><span data-stu-id="807e9-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="807e9-162">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="807e9-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-163">Click Save.</span></span>
6. <span data-ttu-id="807e9-164">Valitse Lisää nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="807e9-164">Click Add items.</span></span>
7. <span data-ttu-id="807e9-165">Nimiketunnuksen rivin valitseminen</span><span class="sxs-lookup"><span data-stu-id="807e9-165">Select the Item number row</span></span>
    * <span data-ttu-id="807e9-166">Tässä esimerkissä suodatus suoritetaan nimiketunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="807e9-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="807e9-167">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="807e9-168">Kirjoita esimerkiksi T\*, kun haluat suodattaa T-kirjaimella alkavien nimiketunnusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="807e9-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="807e9-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="807e9-169">Click OK.</span></span>
10. <span data-ttu-id="807e9-170">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="807e9-170">Click OK.</span></span>
11. <span data-ttu-id="807e9-171">Valitse Nimikkeen laaturyhmät.</span><span class="sxs-lookup"><span data-stu-id="807e9-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="807e9-172">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-172">Close the page.</span></span>
13. <span data-ttu-id="807e9-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="807e9-174">Testiryhmän luominen</span><span class="sxs-lookup"><span data-stu-id="807e9-174">Create a test group</span></span>
1. <span data-ttu-id="807e9-175">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Testiryhmät.</span><span class="sxs-lookup"><span data-stu-id="807e9-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="807e9-176">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-176">Click New.</span></span>
3. <span data-ttu-id="807e9-177">Kirjoita Testiryhmä-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="807e9-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="807e9-178">Anna testiryhmälle nimi, jonka avulla muistat suoritettavien testien tyypin ja sen, mihin laaturyhmään liitos tehdään.</span><span class="sxs-lookup"><span data-stu-id="807e9-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="807e9-179">Jos sitä käytetään esimerkiksi sellaisen laaturyhmän kanssa, joka valitsee T-kirjaimella alkavat nimikkeet, voit antaa nimeksi T-nimikkeen testit.</span><span class="sxs-lookup"><span data-stu-id="807e9-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="807e9-180">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="807e9-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="807e9-181">Valitse Nimikeotanta-kentässä aiemmin luomasi nimikeotantarivi.</span><span class="sxs-lookup"><span data-stu-id="807e9-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="807e9-182">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="807e9-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="807e9-183">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="807e9-183">Click Add.</span></span>
8. <span data-ttu-id="807e9-184">Syötä Järjestysnumero-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="807e9-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="807e9-185">Valitse Testi-kentässä aiemmin luomasi testi.</span><span class="sxs-lookup"><span data-stu-id="807e9-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="807e9-186">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="807e9-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="807e9-187">Valitse Testi-välilehti.</span><span class="sxs-lookup"><span data-stu-id="807e9-187">Click the Test tab.</span></span>
12. <span data-ttu-id="807e9-188">Valitse Muuttuja-kentässä aiemmin luomasi muuttuja</span><span class="sxs-lookup"><span data-stu-id="807e9-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="807e9-189">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="807e9-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="807e9-190">Avaa haku valitsemalla Oletustulos-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="807e9-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="807e9-191">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="807e9-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="807e9-192">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-192">Click Save.</span></span>
17. <span data-ttu-id="807e9-193">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="807e9-194">Laatutilausten luomisajankohdan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="807e9-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="807e9-195">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Laadunvalvonta > Laatuliitokset.</span><span class="sxs-lookup"><span data-stu-id="807e9-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="807e9-196">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="807e9-196">Click New.</span></span>
3. <span data-ttu-id="807e9-197">Valitse Viitetyyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="807e9-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="807e9-198">Valitse Nimikekoodi-kentässä Ryhmä.</span><span class="sxs-lookup"><span data-stu-id="807e9-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="807e9-199">Tässä esimerkissä arvoksi valitaan Ryhmä ja käytetään aiemmin luotua laaturyhmää.</span><span class="sxs-lookup"><span data-stu-id="807e9-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="807e9-200">Arvoksi voi määrittää myös Taulu, jos haluat määrittää nimikkeen manuaalisesti, tai Kaikki, jos haluat lisätä kaikki nimikkeet laatutilaukseen.</span><span class="sxs-lookup"><span data-stu-id="807e9-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="807e9-201">Valitse Nimike-kentässä aiemmin luomasi laaturyhmä.</span><span class="sxs-lookup"><span data-stu-id="807e9-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="807e9-202">Nimike-kentän käytettävissä olevat vaihtoehdot riippuvat Nimikekoodi-kentän määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="807e9-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="807e9-203">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="807e9-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="807e9-204">Laajenna tai tiivistä Prosessi-osa.</span><span class="sxs-lookup"><span data-stu-id="807e9-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="807e9-205">Valitse Tapahtumatyyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="807e9-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="807e9-206">Tämä on testin käynnistävä tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="807e9-206">This is the event that triggers the test.</span></span> <span data-ttu-id="807e9-207">Tässä käytettävissä olevat vaihtoehdot riippuvat Viitetyyppi-kentässä valitusta prosessista.</span><span class="sxs-lookup"><span data-stu-id="807e9-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="807e9-208">Valitse Suoritus-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="807e9-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="807e9-209">Laajenna tai tiivistä Laatutilausprosessi-osa.</span><span class="sxs-lookup"><span data-stu-id="807e9-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="807e9-210">Avaa haku valitsemalla Tapahtuman esto -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="807e9-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="807e9-211">Tässä kentässä on niiden prosessien luettelo, joita voidaan estää, jos laatutilaus on yhä avoin.</span><span class="sxs-lookup"><span data-stu-id="807e9-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="807e9-212">Vaihtoehdot riippuvat Tapahtumatyyppi-kentässä valitusta arvosta.</span><span class="sxs-lookup"><span data-stu-id="807e9-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="807e9-213">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="807e9-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="807e9-214">Tämä riippuu aiemmin valituista arvoista.</span><span class="sxs-lookup"><span data-stu-id="807e9-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="807e9-215">Määritä, onko seuraavat prosessit estettävä, kun lähdeasiakirjariviin on linkitettynä avoimia laatutilauksia.</span><span class="sxs-lookup"><span data-stu-id="807e9-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="807e9-216">Laajenna tai tiivistä Määritykset-osa.</span><span class="sxs-lookup"><span data-stu-id="807e9-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="807e9-217">Valitse Testiryhmä-kentässä aiemmin luomasi testiryhmä.</span><span class="sxs-lookup"><span data-stu-id="807e9-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="807e9-218">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="807e9-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="807e9-219">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="807e9-219">Click Save.</span></span>
17. <span data-ttu-id="807e9-220">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="807e9-220">Close the page.</span></span>


