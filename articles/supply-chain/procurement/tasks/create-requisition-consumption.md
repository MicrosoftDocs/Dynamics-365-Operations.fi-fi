--- 
title: Luo kulutusehdotus
description: "Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi."
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bad86a4726ce69015f318d9af98992b36d34b29a
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="608c6-103">Luo kulutusehdotus</span><span class="sxs-lookup"><span data-stu-id="608c6-103">Create a requisition for consumption</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="608c6-104">Tässä menettelyssä käsitellään yksityiskohtaisesti ehdotuksen luontiprosessi.</span><span class="sxs-lookup"><span data-stu-id="608c6-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="608c6-105">Siinä näytetään erilaisia tapoja hakea tuotteiden hankintaluettelon tuotteita sekä millä tavoin lisätään tuote, jota ei ole luettelossa.</span><span class="sxs-lookup"><span data-stu-id="608c6-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="608c6-106">Varmista ennen menettelyn aloittamista, että ostokäytäntö on määritetty siten, että ehdotuksen oletustyyppi on Kulutus.</span><span class="sxs-lookup"><span data-stu-id="608c6-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="608c6-107">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="608c6-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="608c6-108">Menettelyn voi suorittaa vain käyttäjäprofiili, joka on määritetty työntekijäksi.</span><span class="sxs-lookup"><span data-stu-id="608c6-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="608c6-109">Työntekijä suorittaa yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="608c6-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="608c6-110">Työntekijän käyttöoikeusroolin ansiosta voit suorittaa tehtävät. Jos käytössä on USMF, voit kirjautua sisään tunnuksella Alicia.</span><span class="sxs-lookup"><span data-stu-id="608c6-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="608c6-111">Luo uusi ehdotus</span><span class="sxs-lookup"><span data-stu-id="608c6-111">Create a new requisition</span></span>
1. <span data-ttu-id="608c6-112">Valitse Hankinta > Ostoehdotukset > Itse luodut ostoehdotukset.</span><span class="sxs-lookup"><span data-stu-id="608c6-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="608c6-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="608c6-113">Click New.</span></span>
3. <span data-ttu-id="608c6-114">Kirjoita Nimi-kenttään ehdotuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="608c6-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="608c6-115">Kirjoita päivämäärä Vaadittu päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="608c6-116">Pyyntöpäivämäärä ja kirjauspäivä kopioidaan oletusarvoisesti ostoehdotusriveille.</span><span class="sxs-lookup"><span data-stu-id="608c6-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="608c6-117">Niitä voidaan muuttaa rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="608c6-117">They can be changed at the line level.</span></span> <span data-ttu-id="608c6-118">Pyydetty päivämäärä on pyydetty toimituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="608c6-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="608c6-119">Kirjoita päivämäärä Kirjauspäivä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="608c6-120">Kirjauspäivämäärää käytetään tiliviennin kirjaamiseen kirjanpitoon ja vahvistamaan, onko budjettirahoitus käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="608c6-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="608c6-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="608c6-121">Click OK.</span></span>
7. <span data-ttu-id="608c6-122">Avaa haku napsauttamalla Syy-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="608c6-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="608c6-123">Oletusarvon mukaan liiketoimintaperusteet, jotka olet valinnut, ilmestyvät ostoehdotusriveille, mutta voit muuttaa niitä rivitasolla.</span><span class="sxs-lookup"><span data-stu-id="608c6-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="608c6-124">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="608c6-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="608c6-125">Valitse syy</span><span class="sxs-lookup"><span data-stu-id="608c6-125">Select the reason</span></span>
10. <span data-ttu-id="608c6-126">Kirjoita tietokenttään ehdotuksen peruste</span><span class="sxs-lookup"><span data-stu-id="608c6-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="608c6-127">Lisää rivi ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="608c6-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="608c6-128">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="608c6-128">Click Add line.</span></span>
    * <span data-ttu-id="608c6-129">Ostoehdotukseen voi lisätä rivejä kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="608c6-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="608c6-130">Jos tiedät tuotenumero tai tiedät, että pyytämäsi tuote ei ole tuoteluettelossa, rivi lisätään suoraan valitsemalla Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="608c6-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="608c6-131">Vaihtoehtoisesti voit Lisää tuotteet -asetusta, jota voi käyttää nimikkeiden etsimiseen ja suodattamiseen tuoteluettelossa.</span><span class="sxs-lookup"><span data-stu-id="608c6-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="608c6-132">Napsauta juuri luotua riviä.</span><span class="sxs-lookup"><span data-stu-id="608c6-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="608c6-133">Pyynnön lähettäjä on työntekijä, joka on pyytänyt ehdotusta.</span><span class="sxs-lookup"><span data-stu-id="608c6-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="608c6-134">Oletusarvoisesti työntekijä, joka on pyytänyt varasto-ottoehdotuksen, valmistelee sen.</span><span class="sxs-lookup"><span data-stu-id="608c6-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="608c6-135">Varasto-ottoehdotusrivin valmisteluun toisen työntekijän puolesta tarvitaan lupa.</span><span class="sxs-lookup"><span data-stu-id="608c6-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="608c6-136">Jos sinulla on tämä käyttöoikeus, toiset työntekijät näkyvät tässä haussa.</span><span class="sxs-lookup"><span data-stu-id="608c6-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="608c6-137">Kirjoita arvo Nimiketunnus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="608c6-138">Ostavan yrityksen luokan käyttöoikeuskäytäntö ja tuotteiden hankintaluettelo rajoittavat, mitä vaihtoehtoja sinulla on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="608c6-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="608c6-139">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="608c6-140">Lisää muita tuotteita ehdotukseen</span><span class="sxs-lookup"><span data-stu-id="608c6-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="608c6-141">Valitse Lisää tuotteet.</span><span class="sxs-lookup"><span data-stu-id="608c6-141">Click Add products.</span></span>
    * <span data-ttu-id="608c6-142">Voit hakea tällä asetuksella tuoteluettelon tuotteita.</span><span class="sxs-lookup"><span data-stu-id="608c6-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="608c6-143">Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="608c6-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="608c6-144">Kirjoita esimerkiksi tiet.</span><span class="sxs-lookup"><span data-stu-id="608c6-144">For example, type comput.</span></span>  
3. <span data-ttu-id="608c6-145">Käytä InvokeDefaultButton-pikavalintaa.</span><span class="sxs-lookup"><span data-stu-id="608c6-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="608c6-146">Voit suodattaa valitun luokan tuoteluetteloa suodattimella.</span><span class="sxs-lookup"><span data-stu-id="608c6-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="608c6-147">Valitse ehdotukseen lisättävä tuotekortti.</span><span class="sxs-lookup"><span data-stu-id="608c6-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="608c6-148">Valitse Lisää riveihin.</span><span class="sxs-lookup"><span data-stu-id="608c6-148">Click Add to lines.</span></span>
7. <span data-ttu-id="608c6-149">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="608c6-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="608c6-150">Kirjoita Etsi hankintaluokan noodi -kenttään etsittävästä luokan nimen alkuosa ja paina sitten Enter-näppäintä.</span><span class="sxs-lookup"><span data-stu-id="608c6-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="608c6-151">Kirjoita esimerkiksi alle (alleviivauskynät).</span><span class="sxs-lookup"><span data-stu-id="608c6-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="608c6-152">Käytä InvokeDefaultButton-pikavalintaa.</span><span class="sxs-lookup"><span data-stu-id="608c6-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="608c6-153">Lisää tuote, joka ei ole tuotteiden hankintaluettelossa, valitsemalla Lisää listaamaton tuote riveille.</span><span class="sxs-lookup"><span data-stu-id="608c6-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="608c6-154">Kirjoita arvo Tuotteen nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="608c6-155">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="608c6-156">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="608c6-156">Click OK.</span></span>
14. <span data-ttu-id="608c6-157">Lisää tuotekuvaus Nimikkeen kuvaus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="608c6-158">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="608c6-159">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="608c6-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="608c6-160">Jos tiedät tietyn (toimittajan tilikentässä valitun) toimittajan hinta, kyseinen hinta voidaan ilmoittaa</span><span class="sxs-lookup"><span data-stu-id="608c6-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="608c6-161">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="608c6-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="608c6-162">Tästä kentästä valittavat vaihtoehdot määräytyvät hankintakäytäntöjen ja toimittajan nykyisen hankintaluokan tilan mukaan.</span><span class="sxs-lookup"><span data-stu-id="608c6-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="608c6-163">Sen sijaan että toimittaja valittaisiin tässä, voit napsauttaa toimittajan ehdotuspainiketta.</span><span class="sxs-lookup"><span data-stu-id="608c6-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="608c6-164">Valitse luettelosta toimittaja, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="608c6-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="608c6-165">Kirjoita Ulkoinen nimiketunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="608c6-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="608c6-166">Tämä on tuotteen viitenumero, jonka toimittaja tietää.</span><span class="sxs-lookup"><span data-stu-id="608c6-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="608c6-167">Se voi olla esimerkiksi tuotteen nimiketunnus toimittajan omassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="608c6-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="608c6-168">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="608c6-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="608c6-169">Jaa summat</span><span class="sxs-lookup"><span data-stu-id="608c6-169">Distribute amounts</span></span>
1. <span data-ttu-id="608c6-170">Valitse Myyntitiedot.</span><span class="sxs-lookup"><span data-stu-id="608c6-170">Click Financials.</span></span>
2. <span data-ttu-id="608c6-171">Valitse Jaa summat.</span><span class="sxs-lookup"><span data-stu-id="608c6-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="608c6-172">Tämä prosessi osoittaa, miten ensimmäisen rivin kustannus jaetaan kahden tilin välillä.</span><span class="sxs-lookup"><span data-stu-id="608c6-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="608c6-173">Se voidaan tehdä myös myöhemmin, kun varasto-ottoehdotusta arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="608c6-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="608c6-174">Luo uusi jakorivi valitsemalla Jako.</span><span class="sxs-lookup"><span data-stu-id="608c6-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="608c6-175">Valitse Kirjanpitotili-kentässä ensimmäinen kustannuspaikka, johon osa kustannuksesta siirretään.</span><span class="sxs-lookup"><span data-stu-id="608c6-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="608c6-176">Valitse toinen jakorivi.</span><span class="sxs-lookup"><span data-stu-id="608c6-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="608c6-177">Määritä toinen kustannuspaikka Kirjanpitotili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="608c6-178">Valitse Jaa tasaisesti.</span><span class="sxs-lookup"><span data-stu-id="608c6-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="608c6-179">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="608c6-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="608c6-180">Näytä rivin tiedot</span><span class="sxs-lookup"><span data-stu-id="608c6-180">View line details</span></span>
1. <span data-ttu-id="608c6-181">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="608c6-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="608c6-182">Lähetä ehdotus</span><span class="sxs-lookup"><span data-stu-id="608c6-182">Submit the requisition</span></span>
1. <span data-ttu-id="608c6-183">Avaa valintaikkuna valitsemalla Työnkulku.</span><span class="sxs-lookup"><span data-stu-id="608c6-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="608c6-184">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="608c6-184">Click Submit.</span></span>
3. <span data-ttu-id="608c6-185">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="608c6-185">Close the page.</span></span>
4. <span data-ttu-id="608c6-186">Kirjoita ehdotuksen hyväksyjälle huomautus Kommentti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="608c6-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="608c6-187">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="608c6-187">Click Submit.</span></span>
6. <span data-ttu-id="608c6-188">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="608c6-188">Close the page.</span></span>
7. <span data-ttu-id="608c6-189">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="608c6-189">Refresh the page.</span></span>


