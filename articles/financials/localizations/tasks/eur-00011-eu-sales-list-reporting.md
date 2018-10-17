--- 
title: "EUR-00011 EU-myyntiluetteloraportoinnin määrittäminen"
description: "Tässä tehtävässä käsitellään yleisesti EU-myyntiluettelon raportoinnin edellytyksiä."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: aef1d19aabb7937fcd961a9657b8ca65c064b0b1
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-103">EUR-00011 EU-myyntiluetteloraportoinnin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b4f6e-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4f6e-104">Tässä tehtävässä käsitellään yleisesti EU-myyntiluettelon raportoinnin edellytyksiä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="b4f6e-105">Lisätietoja EU:n myyntiluettelon raportoinnista ja edellytyksistä on Dynamics 365 for Finance and Operationsin ohjeissa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-105">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="b4f6e-106">Tämä tehtävä koskee kaikkia Euroopan maita/alueita.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="b4f6e-107">Opastuksessa on käytetty DEMF-demotietoyritystä ja Saksaa kotimaa-/alue-esimerkkinä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="b4f6e-108">Opastuksessa käytetään myös Portugalia EU-esimerkkimaana/-alueena.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="b4f6e-109">Nämä tehtävät on tarkoitettu järjestelmänvalvojille.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-110">Tuo EU-myyntiluettelon raportoinnin sähköisen raportoinnin konfiguraatiot</span><span class="sxs-lookup"><span data-stu-id="b4f6e-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="b4f6e-111">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b4f6e-112">Valitse Aseta aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-112">Click Set active.</span></span>
3. <span data-ttu-id="b4f6e-113">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-113">Click Repositories.</span></span>
4. <span data-ttu-id="b4f6e-114">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-114">Click Open.</span></span>
5. <span data-ttu-id="b4f6e-115">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="b4f6e-116">Valitse Lisäsuodatin/-lajittelu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="b4f6e-117">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-117">Click Add.</span></span>
8. <span data-ttu-id="b4f6e-118">Valitse Kenttä-kentässä Konfiguroinnin nimi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="b4f6e-119">Kirjoita Ehdot-kenttään EU-myyntiluettelo (DE).</span><span class="sxs-lookup"><span data-stu-id="b4f6e-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="b4f6e-120">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-120">Click OK.</span></span>
11. <span data-ttu-id="b4f6e-121">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-121">Click Import.</span></span>
12. <span data-ttu-id="b4f6e-122">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-122">Click Yes.</span></span>
13. <span data-ttu-id="b4f6e-123">Valitse toimintoruudussa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="b4f6e-124">Valitse Lisäsuodatin/-lajittelu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="b4f6e-125">Valitse Palauta.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-125">Click Reset.</span></span>
16. <span data-ttu-id="b4f6e-126">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-126">Click Add.</span></span>
17. <span data-ttu-id="b4f6e-127">Valitse Kenttä-kentässä Konfiguroinnin nimi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="b4f6e-128">Kirjoita Ehdot-kenttään EU-myyntiluettelo riviraportti.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="b4f6e-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-129">Click OK.</span></span>
20. <span data-ttu-id="b4f6e-130">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-130">Click Import.</span></span>
21. <span data-ttu-id="b4f6e-131">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-132">Määritä EU-myyntiluetteloraportoinnin alv-koodit</span><span class="sxs-lookup"><span data-stu-id="b4f6e-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="b4f6e-133">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäverokoodit.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="b4f6e-134">Suodata pikasuodattimella Arvonlisäverokoodi-kenttä arvolla ALV19.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="b4f6e-135">Laajenna Raportin asetukset -osa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="b4f6e-136">Tarkista, että Poissuljettu-valintana on Ei.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="b4f6e-137">Tehtäväopastuksen lukitus on ehkä avattava, jotta asetusta voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-138">Määritä EU-myyntiluetteloraportoinnin alv-ryhmät</span><span class="sxs-lookup"><span data-stu-id="b4f6e-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="b4f6e-139">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="b4f6e-140">Suodata pikasuodattimella Arvonlisäveroryhmä-kenttä arvolla MR-KOT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="b4f6e-141">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-141">Click Edit.</span></span>
4. <span data-ttu-id="b4f6e-142">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="b4f6e-143">Valitse luettelon ensimmäinen rivi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="b4f6e-144">Valitse Vapautus-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="b4f6e-145">Valitse luettelon toinen rivi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="b4f6e-146">Valitse Vapautus-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="b4f6e-147">Valitse luettelon kolmas rivi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="b4f6e-148">Valitse Vapautus-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-149">Määritä EU-myyntiluetteloraportoinnin nimikkeiden alv-ryhmät</span><span class="sxs-lookup"><span data-stu-id="b4f6e-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="b4f6e-150">Siirry kohtaan Vero > Välilliset verot > Arvonlisävero > Arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="b4f6e-151">Suodata pikasuodattimella Nimikkeen arvonlisäveroryhmä -kenttä arvolla TÄYSI.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="b4f6e-152">Tarkista, että Raportointityyppi-valintana on Nimike.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="b4f6e-153">Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="b4f6e-154">Suodata pikasuodattimella Nimikkeen arvonlisäveroryhmä -kenttä arvolla PUN.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="b4f6e-155">Tarkista, että Raportointityyppi-valintana on Palvelu.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="b4f6e-156">Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="b4f6e-157">Määritä EU-myyntiluetteloraportoinnin maa- tai alueparametrit</span><span class="sxs-lookup"><span data-stu-id="b4f6e-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="b4f6e-158">Valitse Vero > Asetukset > Arvonlisävero > Maan/alueen parametrit.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="b4f6e-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-159">Click New.</span></span>
3. <span data-ttu-id="b4f6e-160">Kirjoita Maa/alue-kenttään PRT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="b4f6e-161">Kirjoita Arvonlisävero -kenttään PT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="b4f6e-162">Luo ALV-tunnukset</span><span class="sxs-lookup"><span data-stu-id="b4f6e-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="b4f6e-163">Valitse Vero > Asetukset > Arvonlisävero > ALV-tunnukset.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="b4f6e-164">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-164">Click New.</span></span>
3. <span data-ttu-id="b4f6e-165">Kirjoita Maa/alue-kenttään PRT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="b4f6e-166">Kirjoita ALV-tunnus-kenttään PT12345.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="b4f6e-167">Määritä EU-myyntiluettelon raportointiparametrit</span><span class="sxs-lookup"><span data-stu-id="b4f6e-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="b4f6e-168">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="b4f6e-169">Valitse EU-myyntiluettelo-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="b4f6e-170">Valitse Ostojen siirto -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="b4f6e-171">Laajenna Pyöristyssäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="b4f6e-172">Määritä pyöristyssäännöksi 0,1</span><span class="sxs-lookup"><span data-stu-id="b4f6e-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="b4f6e-173">Valitse Käytä vähimmäisarvoa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="b4f6e-174">Anna Desimaalien määrä -kentässä 2.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="b4f6e-175">Laajenna Sähköinen raportointi -osa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="b4f6e-176">Valitse Tiedostomuodon yhdistäminen -kentässä EU-myyntiluettelo (DE).</span><span class="sxs-lookup"><span data-stu-id="b4f6e-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="b4f6e-177">Valitse Raporttimuodon yhdistäminen -kenttään EU-myyntiluettelon riviraportti.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="b4f6e-178">Valitse Maan tai alueen ominaisuudet -välilehti.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="b4f6e-179">Tarkista, että Maa-/aluetyyppi-kentän Maa/alue DEU -asetuksena on Kotimaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="b4f6e-180">Tehtäväopastuksen lukitus on ehkä avattava, jotta tämän kentän arvoa voi muuttaa.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="b4f6e-181">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-181">Click New.</span></span>
13. <span data-ttu-id="b4f6e-182">Kirjoita Maa/alue-kenttään PRT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="b4f6e-183">Kirjoita Intrastat-koodi-kenttään PT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="b4f6e-184">Valitse Maa-/aluetyyppi-kentässä EU.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="b4f6e-185">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="b4f6e-186">Tarkista, että Numerojärjestyskoodi on määritetty viitteelle EU-myyntiluettelo.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="b4f6e-187">Luo asiakas EU-myyntiluetteloraportoinnin esittelyä varten</span><span class="sxs-lookup"><span data-stu-id="b4f6e-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="b4f6e-188">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="b4f6e-189">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-189">Click New.</span></span>
3. <span data-ttu-id="b4f6e-190">Kirjoita Asiakastili-kenttään PRT-001.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="b4f6e-191">Kirjoita Nimi-kenttään Portugalilainen asiakas.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="b4f6e-192">Valitse Asiakasryhmä-kentässä 10.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="b4f6e-193">Valitse Arvonlisäveroryhmä-kentässä MR-KOT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="b4f6e-194">Valitse ALV-tunnus-kentässä PT12345.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="b4f6e-195">Kirjoita Maa/alue-kenttään PRT.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="b4f6e-196">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b4f6e-196">Click Save.</span></span>


