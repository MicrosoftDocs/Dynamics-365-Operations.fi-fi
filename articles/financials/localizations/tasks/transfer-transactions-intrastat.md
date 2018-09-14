--- 
title: "Siirrä tapahtumat Intrastatiin"
description: "Tämä menettely opastaa Intrastat-parametrien asetuksen ja tapahtumien siirron Intrastatiin."
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13cc9dc2119ad3dc85d580e92edee7bb9ef2075c
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2018

---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="0b94b-103">Siirrä tapahtumat Intrastatiin</span><span class="sxs-lookup"><span data-stu-id="0b94b-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b94b-104">Tämä menettely opastaa Intrastat-parametrien asetuksen ja tapahtumien siirron Intrastatiin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="0b94b-105">Tämä menettelyn luomisessa käytettiin DEMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="0b94b-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="0b94b-106">Luo uusia kauppatavarakoodeja ja päivitä olemassa olevia koodeja</span><span class="sxs-lookup"><span data-stu-id="0b94b-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="0b94b-107">Valitse Tuotetietojen hallinta > Asetukset > Luokat ja määritteet > Luokkahierarkiat.</span><span class="sxs-lookup"><span data-stu-id="0b94b-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="0b94b-108">Etsi tai valitse luettelosta tietue "Intrastat-kauppatavarakoodit".</span><span class="sxs-lookup"><span data-stu-id="0b94b-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="0b94b-109">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0b94b-110">Valitse puussa tietue.</span><span class="sxs-lookup"><span data-stu-id="0b94b-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="0b94b-111">Valitse esimerkiksi Intrastat\Speaker.</span><span class="sxs-lookup"><span data-stu-id="0b94b-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="0b94b-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-112">Click Edit.</span></span>
6. <span data-ttu-id="0b94b-113">Laajenna Ulkomaankauppa-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="0b94b-114">Syötä tai valitse Lisäyksiköt-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="0b94b-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-115">Valitse esimerkiksi pcs.</span><span class="sxs-lookup"><span data-stu-id="0b94b-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="0b94b-116">Valitse Paino ei käytössä -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="0b94b-117">Valitse puussa Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0b94b-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="0b94b-118">Valitse Uusi luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-118">Click New category node.</span></span>
11. <span data-ttu-id="0b94b-119">Kirjoita Nimi-kenttään kauppatavaran nimi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="0b94b-120">Kirjoita esimerkiksi Muu kauppatavara.</span><span class="sxs-lookup"><span data-stu-id="0b94b-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="0b94b-121">Kirjoita Koodi-kenttään kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="0b94b-122">Kirjoita esimerkiksi 995 00 00.</span><span class="sxs-lookup"><span data-stu-id="0b94b-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="0b94b-123">Kirjoita Kutsumanimi-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0b94b-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="0b94b-124">Kirjoita esimerkiksi Muu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="0b94b-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0b94b-125">Click Save.</span></span>
15. <span data-ttu-id="0b94b-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="0b94b-127">Määritä kauppatavarakoodi tuotehierarkialle ja vapautetulle tuotteelle</span><span class="sxs-lookup"><span data-stu-id="0b94b-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="0b94b-128">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="0b94b-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0b94b-129">Voit esimerkiksi suodattaa Nimi-kenttää arvolla myynti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="0b94b-130">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="0b94b-131">Laajenna puussa luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="0b94b-132">Laajenna esimerkiksi Myyntihierarkia\Kodin äänentoisto.</span><span class="sxs-lookup"><span data-stu-id="0b94b-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="0b94b-133">Valitse puussa kauppatavarakoodille määritettävä luokka.</span><span class="sxs-lookup"><span data-stu-id="0b94b-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="0b94b-134">Valitse esimerkiksi Myyntihierarkia\Kodin äänentoisto\Kaiuttimet.</span><span class="sxs-lookup"><span data-stu-id="0b94b-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="0b94b-135">Laajenna Kauppatavarakoodit-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="0b94b-136">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0b94b-136">Click Add.</span></span>
7. <span data-ttu-id="0b94b-137">Valitse Valitse hierarkia -kentästä Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0b94b-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="0b94b-138">Etsi kauppatavarakoodi luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0b94b-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="0b94b-139">Valitse esimerkiksi 920 20 34 Kaiutin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="0b94b-140">Valitse SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="0b94b-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="0b94b-141">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-141">Click OK.</span></span>
11. <span data-ttu-id="0b94b-142">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="0b94b-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="0b94b-143">Valitse luettelosta vapautettu tuote, joka liitetään kauppatavarakoodiin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="0b94b-144">Valitse esimerkiksi D0001.</span><span class="sxs-lookup"><span data-stu-id="0b94b-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="0b94b-145">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-145">Click Edit.</span></span>
14. <span data-ttu-id="0b94b-146">Laajenna Ulkomaankauppa-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="0b94b-147">Kirjoita Kauppatavara-kenttään kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="0b94b-148">Valitse esimerkiksi arvo 920 20 34 Kaiutin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="0b94b-149">Syötä Kuluprosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0b94b-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="0b94b-150">Kirjoita esimerkiksi 3.</span><span class="sxs-lookup"><span data-stu-id="0b94b-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="0b94b-151">Kirjoita tai valitse Maa/alue-kenttään alkuperämaa/-alue</span><span class="sxs-lookup"><span data-stu-id="0b94b-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="0b94b-152">Valitse esimerkiksi AUT.</span><span class="sxs-lookup"><span data-stu-id="0b94b-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="0b94b-153">Laajenna Varastonhallinta-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="0b94b-154">Syötä Nettopaino-kenttään paino kilogrammoina.</span><span class="sxs-lookup"><span data-stu-id="0b94b-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="0b94b-155">Kirjoita esimerkiksi 2.5.</span><span class="sxs-lookup"><span data-stu-id="0b94b-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="0b94b-156">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0b94b-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="0b94b-157">Määritä Intrastat-tapahtumakoodit ja ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="0b94b-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="0b94b-158">Valitse Vero > Asetukset > Ulkomaankauppa > Tapahtumakoodit</span><span class="sxs-lookup"><span data-stu-id="0b94b-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="0b94b-159">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-159">Click New.</span></span>
3. <span data-ttu-id="0b94b-160">Kirjoita arvo Tapahtumakoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="0b94b-161">Kirjoita esimerkiksi "21" palautuksessa käytettäväksi tapahtumakoodiksi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="0b94b-162">Kirjoita tapahtumakoodin nimi Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="0b94b-163">Syötä kenttään esimerkiksi Palautus.</span><span class="sxs-lookup"><span data-stu-id="0b94b-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="0b94b-164">Valitse Tilastosumma-kentästä haluamasi vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="0b94b-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="0b94b-165">Valitse esimerkiksi "Tyhjä", joka ilmaisee, että tapahtumien, joiden koodi on "21", ilmoitettu tilastollinen arvo on aina nolla.</span><span class="sxs-lookup"><span data-stu-id="0b94b-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="0b94b-166">Valitse Vero > Asetukset > Ulkomaankauppa > Ulkomaankaupan parametrit</span><span class="sxs-lookup"><span data-stu-id="0b94b-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="0b94b-167">Syötä tai valitse arvo Tapahtumakoodi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-168">Valitse esimerkiksi 11.</span><span class="sxs-lookup"><span data-stu-id="0b94b-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="0b94b-169">Anna tai valitse Hyvityslasku-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0b94b-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-170">Tämä arvo tunnistaa myös fyysisen palautuksen.</span><span class="sxs-lookup"><span data-stu-id="0b94b-170">This value also identifies the physical return.</span></span> <span data-ttu-id="0b94b-171">Fyysisen palautuksen hyvityslasku siirretään Intrastat-kirjauskansioon päinvastaisen suuntaiseksi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="0b94b-172">Esimerkiksi saapumisen palautus siirretään lähetyksenä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="0b94b-173">Muussa tapauksessa hyvityslasku käsitellään korjauksena ja siirretään samansuuntaisena ja vastakkaisella merkillä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="0b94b-174">Esimerkiksi saapumisen korjaus siirretään saapumisena, jolla on negatiivinen summa ja aktiiviseksi merkinnäksi asetetaan "Korjaus".</span><span class="sxs-lookup"><span data-stu-id="0b94b-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="0b94b-175">Laajenna Varastosiirto-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="0b94b-176">Valitse Kyllä Nimikkeet, joilla on kauppatavarakoodi -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="0b94b-177">Valitse tämä vaihtoehto siirtääksesi ainoastaan tapahtumat, joille on määritetty kauppatavarakoodi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="0b94b-178">Tapahtumia, joilla ei ole kauppatavarakoodia ei siirretä Intrastatiin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="0b94b-179">Valitse Siirrä, kun nämä kriteerit täyttyvät -kenttään vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="0b94b-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="0b94b-180">Valitse esimerkiksi "Yksi valituista".</span><span class="sxs-lookup"><span data-stu-id="0b94b-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="0b94b-181">Laajenna Kauppatavarakoodihierarkia-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="0b94b-182">Valitse Maan tai alueen ominaisuudet -välilehti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="0b94b-183">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-183">Click New.</span></span>
15. <span data-ttu-id="0b94b-184">Syötä tai valitse arvo Maa/alue-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-185">Valitse esimerkiksi arvo FRA.</span><span class="sxs-lookup"><span data-stu-id="0b94b-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="0b94b-186">Kirjoita Intrastat-koodi-kenttään maan ISO-koodi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="0b94b-187">Kirjoita esimerkiksi FR.</span><span class="sxs-lookup"><span data-stu-id="0b94b-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="0b94b-188">Valitse Maa-/aluetyyppi-kentässä EU.</span><span class="sxs-lookup"><span data-stu-id="0b94b-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="0b94b-189">Valitse Numerojärjestykset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="0b94b-190">Määritä toimitustavat ja kulujen sisällyttämissäännöt Intrastatissa</span><span class="sxs-lookup"><span data-stu-id="0b94b-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="0b94b-191">Valitse Myynti ja markkinointi > Asetukset > Jakelu > Toimitustavat</span><span class="sxs-lookup"><span data-stu-id="0b94b-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="0b94b-192">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0b94b-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0b94b-193">Valitse esimerkiksi 20 Air.</span><span class="sxs-lookup"><span data-stu-id="0b94b-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="0b94b-194">Laajenna Ulkomaankauppa-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="0b94b-195">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-195">Click Edit.</span></span>
5. <span data-ttu-id="0b94b-196">Syötä tai valitse arvo Kuljetus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-197">Valitse esimerkiksi 02.</span><span class="sxs-lookup"><span data-stu-id="0b94b-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="0b94b-198">Valitse Myyntireskontra > Kulujen määritys > Kulujen koodi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="0b94b-199">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="0b94b-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0b94b-200">Voit esimerkiksi suodattaa Kulujen koodi -kenttää arvolla rahti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="0b94b-201">Laajenna Ulkomaankauppa-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="0b94b-202">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-202">Click Edit.</span></span>
10. <span data-ttu-id="0b94b-203">Valitse Intrastat-laskun arvo -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="0b94b-204">Summa siirretään Laskun kulut -kenttään ja lasketaan yhteen Laskun summa -kenttään siirretyn summan kanssa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="0b94b-205">Valitse Kyllä Tilastollinen Intrastat-arvo -kentässä jos muutosten määrä on siirrettävä Tilastolliset maksut -kenttään ja laskettava yhteen tilastollisen summan kanssa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="0b94b-206">Tuotteiden myynti EU-asiakkaille</span><span class="sxs-lookup"><span data-stu-id="0b94b-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="0b94b-207">Siirry kohtaan Myyntireskontra > Tilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="0b94b-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="0b94b-208">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-208">Click New.</span></span>
3. <span data-ttu-id="0b94b-209">Valitse Asiakastili-kentässä EU-asiakas</span><span class="sxs-lookup"><span data-stu-id="0b94b-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="0b94b-210">Valitse esimerkiksi "DE-012 Litware Retail".</span><span class="sxs-lookup"><span data-stu-id="0b94b-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="0b94b-211">Laajenna Toimitus-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="0b94b-212">Syötä tai valitse arvo Toimitustapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-213">Valitse esimerkiksi 20 Air.</span><span class="sxs-lookup"><span data-stu-id="0b94b-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="0b94b-214">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-214">Click OK.</span></span>
7. <span data-ttu-id="0b94b-215">Siirrä kohdistin myyntitilausrivien ensimmäiselle riville.</span><span class="sxs-lookup"><span data-stu-id="0b94b-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="0b94b-216">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-217">Valitse esimerkiksi D001.</span><span class="sxs-lookup"><span data-stu-id="0b94b-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="0b94b-218">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="0b94b-219">Valitse Ulkomaankauppa-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="0b94b-220">Kuljetus täytetään automaattisesti valitusta toimitustavasta.</span><span class="sxs-lookup"><span data-stu-id="0b94b-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="0b94b-221">Syötä tai valitse arvo Portti-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="0b94b-222">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="0b94b-222">Click Financials.</span></span>
    * <span data-ttu-id="0b94b-223">Asetusten mukaan, tämä summa sisältyy Intrastat-laskutusarvoon.</span><span class="sxs-lookup"><span data-stu-id="0b94b-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="0b94b-224">Valitse Kulujen ylläpito.</span><span class="sxs-lookup"><span data-stu-id="0b94b-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="0b94b-225">Syötä tai valitse arvo Kulujen koodi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-226">Valitse esimerkiksi RAHTI.</span><span class="sxs-lookup"><span data-stu-id="0b94b-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="0b94b-227">Merkitse Säilytä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="0b94b-228">Syötä Kulujen arvo -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="0b94b-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="0b94b-229">Kirjoita esimerkiksi 10.</span><span class="sxs-lookup"><span data-stu-id="0b94b-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="0b94b-230">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0b94b-230">Click Save.</span></span>
18. <span data-ttu-id="0b94b-231">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-231">Close the page.</span></span>
19. <span data-ttu-id="0b94b-232">Valitse toimintoruudussa Lasku.</span><span class="sxs-lookup"><span data-stu-id="0b94b-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="0b94b-233">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="0b94b-233">Click Invoice.</span></span>
21. <span data-ttu-id="0b94b-234">Laajenna Parametrit-osa.</span><span class="sxs-lookup"><span data-stu-id="0b94b-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="0b94b-235">Valitse Määrä-kentässä Kaikki.</span><span class="sxs-lookup"><span data-stu-id="0b94b-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="0b94b-236">Laajenna osa Asetukset.</span><span class="sxs-lookup"><span data-stu-id="0b94b-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="0b94b-237">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="0b94b-238">Kirjoita esimerkiksi 2015-01-31.</span><span class="sxs-lookup"><span data-stu-id="0b94b-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="0b94b-239">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-239">Click OK.</span></span>
26. <span data-ttu-id="0b94b-240">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-240">Click OK.</span></span>
27. <span data-ttu-id="0b94b-241">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b94b-241">Close the page.</span></span>
28. <span data-ttu-id="0b94b-242">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="0b94b-242">Click New.</span></span>
29. <span data-ttu-id="0b94b-243">Valitse Asiakastili-kentässä EU-asiakas.</span><span class="sxs-lookup"><span data-stu-id="0b94b-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="0b94b-244">Valitse esimerkiksi DE-013 Trey Wholesales.</span><span class="sxs-lookup"><span data-stu-id="0b94b-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="0b94b-245">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-245">Click OK.</span></span>
31. <span data-ttu-id="0b94b-246">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="0b94b-247">Valitse esimerkiksi D0001.</span><span class="sxs-lookup"><span data-stu-id="0b94b-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="0b94b-248">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0b94b-248">Click Save.</span></span>
33. <span data-ttu-id="0b94b-249">Valitse Lasku.</span><span class="sxs-lookup"><span data-stu-id="0b94b-249">Click Invoice.</span></span>
34. <span data-ttu-id="0b94b-250">Kirjoita päivämäärä Laskun päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="0b94b-251">Syötä esimerkiksi päivämäärä "2015-01-31".</span><span class="sxs-lookup"><span data-stu-id="0b94b-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="0b94b-252">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-252">Click OK.</span></span>
36. <span data-ttu-id="0b94b-253">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="0b94b-254">Siirrä tapahtumat Intrastatiin</span><span class="sxs-lookup"><span data-stu-id="0b94b-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="0b94b-255">Valitse Vero > Ilmoitukset > Ulkomaankauppa > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="0b94b-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="0b94b-256">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-256">Click Transfer.</span></span>
3. <span data-ttu-id="0b94b-257">Valitse Myyntilasku-kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="0b94b-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="0b94b-258">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="0b94b-258">Click Filter.</span></span>
5. <span data-ttu-id="0b94b-259">Merkitse Päivämäärä-rivi luettelossa</span><span class="sxs-lookup"><span data-stu-id="0b94b-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="0b94b-260">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b94b-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0b94b-261">Kirjoita esimerkiksi suodatin kaudelle tammikuu 2015 (tarkka arvo riippuu päivämäärämuodosta): 1/1/2015..31/1/2015</span><span class="sxs-lookup"><span data-stu-id="0b94b-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="0b94b-262">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-262">Click OK.</span></span>
8. <span data-ttu-id="0b94b-263">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0b94b-263">Click OK.</span></span>
9. <span data-ttu-id="0b94b-264">Etsi siirretty tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="0b94b-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="0b94b-265">Valitse Yleiset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0b94b-265">Click the General tab.</span></span>
    * <span data-ttu-id="0b94b-266">Tarkista siirretyt tiedot, mukaan lukien kohde- tai lähetysmaa tai -alue, alkuperämaa, paino, määrä, määrä lisäyksiköinä, kauppatavara, tapahtumakoodi, laskutusmäärät ja tilastolliset määrät.</span><span class="sxs-lookup"><span data-stu-id="0b94b-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="0b94b-267">Voit muokata tietoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0b94b-267">You can modify data if necessary.</span></span>  


