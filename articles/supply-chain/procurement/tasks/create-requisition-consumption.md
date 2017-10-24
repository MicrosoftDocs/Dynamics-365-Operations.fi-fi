--- 
title: Luo kulutusehdotus
description: "Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="9f7ee-103">Luo kulutusehdotus</span><span class="sxs-lookup"><span data-stu-id="9f7ee-103">Create a requisition for consumption</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f7ee-104">Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="9f7ee-105">Siinä näytetään erilaisia tapoja hakea tuotteiden hankintaluettelon tuotteita sekä millä tavoin lisätään tuote, jota ei ole luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-105">It shows you different ways to search for products in your procurement catalogue and how to add a product that isn’t in your catalogue.</span></span> <span data-ttu-id="9f7ee-106">Varmista ennen menettelyn aloittamista, että ostokäytäntö on määritetty siten, että ehdotuksen oletustyyppi on Kulutus.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="9f7ee-107">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="9f7ee-108">Menettelyn voi suorittaa vain käyttäjäprofiili, joka on määritetty työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="9f7ee-109">Työntekijä suorittaa yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="9f7ee-110">Työntekijän käyttöoikeusroolin ansiosta voit suorittaa tehtävät. Jos käytössä on USMF, voit kirjautua sisään tunnuksella Alicia.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="9f7ee-111">Luo uusi ehdotus</span><span class="sxs-lookup"><span data-stu-id="9f7ee-111">Create a new requisition</span></span>
1. <span data-ttu-id="9f7ee-112">Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="9f7ee-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-113">Click New.</span></span>
3. <span data-ttu-id="9f7ee-114">Kirjoita Nimi-kenttään ehdotuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="9f7ee-115">Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="9f7ee-116">Pyyntöpäivämäärä ja kirjauspäivä kopioidaan oletusarvoisesti ostoehdotusriveille.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="9f7ee-117">Niitä voidaan muuttaa rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-117">They can be changed at the line level.</span></span> <span data-ttu-id="9f7ee-118">Pyydetty päivämäärä on pyydetty toimituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="9f7ee-119">Kirjoita päivämäärä Kirjauspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="9f7ee-120">Kirjauspäivämäärää käytetään tiliviennin kirjaamiseen kirjanpitoon ja vahvistamaan, onko budjettirahoitus käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="9f7ee-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-121">Click OK.</span></span>
7. <span data-ttu-id="9f7ee-122">Avaa haku napsauttamalla Syy-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f7ee-123">Oletusarvon mukaan liiketoimintaperusteet, jotka olet valinnut, ilmestyvät ostoehdotusriveille, mutta voit muuttaa niitä rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="9f7ee-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="9f7ee-125">Valitse syy</span><span class="sxs-lookup"><span data-stu-id="9f7ee-125">Select the reason</span></span>
10. <span data-ttu-id="9f7ee-126">Kirjoita tietokenttään ehdotuksen peruste</span><span class="sxs-lookup"><span data-stu-id="9f7ee-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="9f7ee-127">Lisää rivi ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="9f7ee-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="9f7ee-128">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-128">Click Add line.</span></span>
    * <span data-ttu-id="9f7ee-129">Ostoehdotukseen voi lisätä rivejä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="9f7ee-130">Jos tiedät tuotenumeron tai tiedät, ettei pyytämäsi tuotetta ole tuoteluettelossa, voit lisätä rivin suoraan valitsemalla Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalogueue, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="9f7ee-131">Vaihtoehtoisesti voit Lisää tuotteet -asetusta, jota voi käyttää nimikkeiden etsimiseen ja suodattamiseen tuoteluettelossa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalogueue.</span></span>    
2. <span data-ttu-id="9f7ee-132">Napsauta juuri luotua riviä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="9f7ee-133">Pyynnön lähettäjä on työntekijä, joka on pyytänyt ehdotusta.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="9f7ee-134">Oletusarvoisesti työntekijä, joka on pyytänyt varasto-ottoehdotuksen, valmistelee sen.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="9f7ee-135">Varasto-ottoehdotusrivin valmisteluun toisen työntekijän puolesta tarvitaan lupa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="9f7ee-136">Jos sinulla on tämä käyttöoikeus, toiset työntekijät näkyvät tässä haussa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="9f7ee-137">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9f7ee-138">Ostavan yrityksen luokan käyttöoikeuskäytäntö ja tuotteiden hankintaluettelo rajoittavat, mitä vaihtoehtoja sinulla on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-138">The items that are available for you to choose are limited by the category access policy and the procurement catalogue for the buying legal entity.</span></span>   
4. <span data-ttu-id="9f7ee-139">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="9f7ee-140">Lisää muita tuotteita ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="9f7ee-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="9f7ee-141">Valitse Lisää tuotteet.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-141">Click Add products.</span></span>
    * <span data-ttu-id="9f7ee-142">Voit hakea tällä asetuksella tuoteluettelon tuotteita.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-142">This is the option where you can search for products in the product catalogueue.</span></span>    
2. <span data-ttu-id="9f7ee-143">Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="9f7ee-144">Kirjoita esimerkiksi tiet.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-144">For example, type comput.</span></span>  
3. <span data-ttu-id="9f7ee-145">Käytä InvokeDefaultButton-pikavalintaa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="9f7ee-146">Voit suodattaa valitun luokan tuoteluetteloa suodattimella.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="9f7ee-147">Valitse ehdotukseen lisättävä tuotekortti.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="9f7ee-148">Valitse Lisää riveihin.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-148">Click Add to lines.</span></span>
7. <span data-ttu-id="9f7ee-149">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="9f7ee-150">Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="9f7ee-151">Kirjoita esimerkiksi alle (alleviivauskynät).</span><span class="sxs-lookup"><span data-stu-id="9f7ee-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="9f7ee-152">Käytä InvokeDefaultButton-pikavalintaa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="9f7ee-153">Lisää tuote, joka ei ole tuotteiden hankintaluettelossa, valitsemalla Lisää listaamaton tuote riveille.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalogue.</span></span>
11. <span data-ttu-id="9f7ee-154">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="9f7ee-155">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="9f7ee-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-156">Click OK.</span></span>
14. <span data-ttu-id="9f7ee-157">Lisää tuotekuvaus Nimikkeen kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="9f7ee-158">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="9f7ee-159">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="9f7ee-160">Jos tiedät tietyn (toimittajan tilikentässä valitun) toimittajan hinta, kyseinen hinta voidaan ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="9f7ee-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="9f7ee-161">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9f7ee-162">Tästä kentästä valittavat vaihtoehdot määräytyvät hankintakäytäntöjen ja toimittajan nykyisen hankintaluokan tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="9f7ee-163">Sen sijaan että toimittaja valittaisiin tässä, voit napsauttaa toimittajan ehdotuspainiketta.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="9f7ee-164">Valitse luettelosta toimittaja, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="9f7ee-165">Kirjoita Ulkoinen nimiketunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="9f7ee-166">Tämä on tuotteen viitenumero, jonka toimittaja tietää.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="9f7ee-167">Se voi olla esimerkiksi tuotteen nimiketunnus toimittajan omassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-167">For example, this could be the item number of the product in the vendor's own catalogue.</span></span>  
20. <span data-ttu-id="9f7ee-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="9f7ee-169">Jaa summat</span><span class="sxs-lookup"><span data-stu-id="9f7ee-169">Distribute amounts</span></span>
1. <span data-ttu-id="9f7ee-170">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-170">Click Financials.</span></span>
2. <span data-ttu-id="9f7ee-171">Valitse Jaa summat.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="9f7ee-172">Tämä prosessi osoittaa, miten ensimmäisen rivin kustannus jaetaan kahden tilin välillä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="9f7ee-173">Se voidaan tehdä myös myöhemmin, kun varasto-ottoehdotusta arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="9f7ee-174">Luo uusi jakorivi valitsemalla Jako.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="9f7ee-175">Valitse Kirjanpitotili-kentässä ensimmäinen kustannuspaikka, johon osa kustannuksesta siirretään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-175">In the Ledger account field select the first cost centre that should take part of the cost.</span></span>
5. <span data-ttu-id="9f7ee-176">Valitse toinen jakorivi.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="9f7ee-177">Määritä toinen kustannuspaikka Kirjanpitotili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-177">In the Ledger account field specify the other cost centre.</span></span>
7. <span data-ttu-id="9f7ee-178">Valitse Jaa tasaisesti.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="9f7ee-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="9f7ee-180">Näytä rivin tiedot</span><span class="sxs-lookup"><span data-stu-id="9f7ee-180">View line details</span></span>
1. <span data-ttu-id="9f7ee-181">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="9f7ee-182">Lähetä ehdotus</span><span class="sxs-lookup"><span data-stu-id="9f7ee-182">Submit the requisition</span></span>
1. <span data-ttu-id="9f7ee-183">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="9f7ee-184">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-184">Click Submit.</span></span>
3. <span data-ttu-id="9f7ee-185">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-185">Close the page.</span></span>
4. <span data-ttu-id="9f7ee-186">Kirjoita ehdotuksen hyväksyjälle huomautus Kommentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="9f7ee-187">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-187">Click Submit.</span></span>
6. <span data-ttu-id="9f7ee-188">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-188">Close the page.</span></span>
7. <span data-ttu-id="9f7ee-189">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="9f7ee-189">Refresh the page.</span></span>


