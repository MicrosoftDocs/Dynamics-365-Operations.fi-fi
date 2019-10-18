---
title: Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 2 – asiakirjojen luominen) -menettely on suoritettu.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5df6128228b9ff620c606c550c5eb7a6039b915
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182298"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="727f8-103">Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="727f8-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="727f8-104">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (osa 2: asiakirjojen luominen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="727f8-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="727f8-105">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="727f8-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="727f8-106">Tässä menettelyssä muokataan ER-konfiguraatioita ja aloitetaan niiden käyttäminen sähköisten asiakirjojen luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="727f8-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="727f8-107">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="727f8-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="727f8-108">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="727f8-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="727f8-109">Tietomallin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="727f8-109">Modify data model</span></span>
1. <span data-ttu-id="727f8-110">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="727f8-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="727f8-111">Valitse puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="727f8-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="727f8-112">Voit laajentaa tietomallin käyttötapaa.</span><span class="sxs-lookup"><span data-stu-id="727f8-112">You will extend how you use the data model.</span></span> <span data-ttu-id="727f8-113">Tietomallia käytetään Intrastat-raportin luonnissa käytettävänä tietolähteenä sekä Intrastat-raportointiprosessin tietojen keräämisessä.</span><span class="sxs-lookup"><span data-stu-id="727f8-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="727f8-114">Tietoja käytetään tämän jälkeen sovellustietojen päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="727f8-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="727f8-115">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="727f8-115">Click Designer.</span></span>
4. <span data-ttu-id="727f8-116">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="727f8-117">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="727f8-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="727f8-118">Kirjoita Nimi-kenttään Sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="727f8-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="727f8-119">Sovellustietojen päivitystä varten</span><span class="sxs-lookup"><span data-stu-id="727f8-119">For application data update</span></span>  
7. <span data-ttu-id="727f8-120">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-120">Click Add.</span></span>
8. <span data-ttu-id="727f8-121">Valitse puussa For application data update.</span><span class="sxs-lookup"><span data-stu-id="727f8-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="727f8-122">Tämä uusi juurinimike lisätään määrittämään tietovirta, jota käytetään (tietolähteenä käytettävän) Intrastar-raportin tietojen siirtämiseen sovellustauluihin (päivityskohde).</span><span class="sxs-lookup"><span data-stu-id="727f8-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="727f8-123">Huomaa, että lähtevään asiakirjaan kirjattujen tietojen ja sovellustietojen päivityksessä käytettävän asiakirjan tietojen haussa on käytettävä eri juurinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="727f8-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="727f8-124">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="727f8-125">Syötä Nimi-kenttään Arkiston otsikko.</span><span class="sxs-lookup"><span data-stu-id="727f8-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="727f8-126">Arkiston otsikko</span><span class="sxs-lookup"><span data-stu-id="727f8-126">Archive header</span></span>  
11. <span data-ttu-id="727f8-127">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="727f8-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="727f8-128">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-128">Click Add.</span></span>
    * <span data-ttu-id="727f8-129">Koska luot jokaiselle luodulle Intrastat-raportille tietueen, raportille on luotava uusi nimike.</span><span class="sxs-lookup"><span data-stu-id="727f8-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="727f8-130">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="727f8-131">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="727f8-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="727f8-132">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="727f8-132">File name</span></span>  
15. <span data-ttu-id="727f8-133">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="727f8-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="727f8-134">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-134">Click Add.</span></span>
17. <span data-ttu-id="727f8-135">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="727f8-136">Syötä Nimi-kenttään Rivien määrä.</span><span class="sxs-lookup"><span data-stu-id="727f8-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="727f8-137">Rivien määrä</span><span class="sxs-lookup"><span data-stu-id="727f8-137">Number of lines</span></span>  
19. <span data-ttu-id="727f8-138">Valitse Nimiketyyppi-kentässä Kokonaisluku.</span><span class="sxs-lookup"><span data-stu-id="727f8-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="727f8-139">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-139">Click Add.</span></span>
    * <span data-ttu-id="727f8-140">Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien määrää.</span><span class="sxs-lookup"><span data-stu-id="727f8-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="727f8-141">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="727f8-142">Syötä Nimi-kenttään Arkiston rivit.</span><span class="sxs-lookup"><span data-stu-id="727f8-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="727f8-143">Arkiston rivit</span><span class="sxs-lookup"><span data-stu-id="727f8-143">Archive lines</span></span>  
23. <span data-ttu-id="727f8-144">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="727f8-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="727f8-145">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-145">Click Add.</span></span>
    * <span data-ttu-id="727f8-146">Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="727f8-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="727f8-147">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="727f8-148">Syötä Nimi-kenttään Summa.</span><span class="sxs-lookup"><span data-stu-id="727f8-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="727f8-149">Määrä</span><span class="sxs-lookup"><span data-stu-id="727f8-149">Amount</span></span>  
27. <span data-ttu-id="727f8-150">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="727f8-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="727f8-151">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-151">Click Add.</span></span>
29. <span data-ttu-id="727f8-152">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="727f8-153">Kirjoita Nimi-kenttään Kauppatavaratietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="727f8-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="727f8-154">Kauppatavaratietueen tunnus</span><span class="sxs-lookup"><span data-stu-id="727f8-154">Commodity rec id</span></span>  
31. <span data-ttu-id="727f8-155">Valitse Nimiketyyppi-kentässä Int64.</span><span class="sxs-lookup"><span data-stu-id="727f8-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="727f8-156">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-156">Click Add.</span></span>
33. <span data-ttu-id="727f8-157">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="727f8-158">Syötä Nimi-kenttään Nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="727f8-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="727f8-159">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="727f8-159">Item number</span></span>  
35. <span data-ttu-id="727f8-160">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="727f8-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="727f8-161">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-161">Click Add.</span></span>
37. <span data-ttu-id="727f8-162">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="727f8-162">Click Save.</span></span>
38. <span data-ttu-id="727f8-163">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="727f8-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="727f8-164">Mallin yhdistämismäärityksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="727f8-164">Modify model mapping</span></span>
1. <span data-ttu-id="727f8-165">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="727f8-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="727f8-166">Valitse puussa Intrastat (model)\Intrastat (mapping).</span><span class="sxs-lookup"><span data-stu-id="727f8-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="727f8-167">Muokkaa aiemmin määritettyä mallin yhdistämismääritystä, kun haluat aloittaa sen käytön sovellustietojen päivityksessä ja Intrastat-raportoinnin tietojen arkistoinnissa.</span><span class="sxs-lookup"><span data-stu-id="727f8-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="727f8-168">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="727f8-168">Click Designer.</span></span>
4. <span data-ttu-id="727f8-169">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="727f8-169">Click New.</span></span>
5. <span data-ttu-id="727f8-170">Syötä Nimi-kenttään Päivitä arkisto.</span><span class="sxs-lookup"><span data-stu-id="727f8-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="727f8-171">Arkiston päivittäminen</span><span class="sxs-lookup"><span data-stu-id="727f8-171">Update archive</span></span>  
6. <span data-ttu-id="727f8-172">Valitse Suunta-kentässä Kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="727f8-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="727f8-173">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="727f8-173">Click Save.</span></span>
    * <span data-ttu-id="727f8-174">Tämä uusi yhdistämismääritys määrittää tietovirran, jota käytetään tietojen (Intrastat-raportoinnin tietojen) siirtämisessä tietomallista sovellustauluihin (päivityskohde).</span><span class="sxs-lookup"><span data-stu-id="727f8-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="727f8-175">Ota huomioon, että raportointiprosessin sovelluksen tietojen haussa ja sovellustietojen päivityksen tietomallin tietojen käytössä on käytettävä eri mallin juurinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="727f8-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="727f8-176">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="727f8-176">Click Designer.</span></span>
9. <span data-ttu-id="727f8-177">Valitse puussa Data model\Data model.</span><span class="sxs-lookup"><span data-stu-id="727f8-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="727f8-178">Lisää vaadittu tietolähde.</span><span class="sxs-lookup"><span data-stu-id="727f8-178">Add the required data source.</span></span> <span data-ttu-id="727f8-179">Tämä on tietomalli, joka sisältää raportoitujen ja arkistoitavien Intrastat-tapahtumien tiedot.</span><span class="sxs-lookup"><span data-stu-id="727f8-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="727f8-180">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="727f8-180">Click Add root.</span></span>
11. <span data-ttu-id="727f8-181">Kirjoita Nimi-kenttään malli.</span><span class="sxs-lookup"><span data-stu-id="727f8-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="727f8-182">malli</span><span class="sxs-lookup"><span data-stu-id="727f8-182">model</span></span>  
12. <span data-ttu-id="727f8-183">Syötä tai valitse Määritelmä-kenttään Sovellustietojen päivitystä varten -arvo.</span><span class="sxs-lookup"><span data-stu-id="727f8-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="727f8-184">Sovellustietojen päivitystä varten</span><span class="sxs-lookup"><span data-stu-id="727f8-184">For application data update</span></span>  
13. <span data-ttu-id="727f8-185">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="727f8-185">Click OK.</span></span>
14. <span data-ttu-id="727f8-186">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="727f8-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="727f8-187">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="727f8-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="727f8-188">Valitse puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="727f8-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="727f8-189">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="727f8-189">Click Add.</span></span>
    * <span data-ttu-id="727f8-190">Koska haluat luetteloida raportoidut Intrastat-tapahtumat arkistointia varten, soveltuva tietolähde on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="727f8-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="727f8-191">Syötä Nimi-kenttään Luetteloidut rivit.</span><span class="sxs-lookup"><span data-stu-id="727f8-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="727f8-192">Luetteloidut rivit</span><span class="sxs-lookup"><span data-stu-id="727f8-192">Enumerated lines</span></span>  
19. <span data-ttu-id="727f8-193">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="727f8-193">Click Edit formula.</span></span>
20. <span data-ttu-id="727f8-194">Valitse puussa List\ENUMERATE.</span><span class="sxs-lookup"><span data-stu-id="727f8-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="727f8-195">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="727f8-195">Click Add function.</span></span>
22. <span data-ttu-id="727f8-196">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="727f8-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="727f8-197">Laajenna puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="727f8-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="727f8-198">Valitse puussa model\Archive header\Archive lines.</span><span class="sxs-lookup"><span data-stu-id="727f8-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="727f8-199">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="727f8-199">Click Add data source.</span></span>
26. <span data-ttu-id="727f8-200">Syötä Kaava-kenttään ENUMERATE(model.'Archive header'.'Archive lines').</span><span class="sxs-lookup"><span data-stu-id="727f8-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="727f8-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="727f8-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="727f8-202">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="727f8-202">Click Save.</span></span>
28. <span data-ttu-id="727f8-203">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="727f8-203">Close the page.</span></span>
29. <span data-ttu-id="727f8-204">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="727f8-204">Click OK.</span></span>
30. <span data-ttu-id="727f8-205">Valitse Lisää kohde.</span><span class="sxs-lookup"><span data-stu-id="727f8-205">Click Add destination.</span></span>
    * <span data-ttu-id="727f8-206">Lisää sovellustaulut pakollisina kohteina, jotka vaativat päivitykset raportoitujen Intrastat-tapahtumien tietojen arkistointia varten.</span><span class="sxs-lookup"><span data-stu-id="727f8-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="727f8-207">Kirjoita Nimi-kenttään Arkisto.</span><span class="sxs-lookup"><span data-stu-id="727f8-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="727f8-208">Arkistoi</span><span class="sxs-lookup"><span data-stu-id="727f8-208">Archive</span></span>  
32. <span data-ttu-id="727f8-209">Kirjoita Taulun nimi -kenttään IntrastatArchiveGeneral.</span><span class="sxs-lookup"><span data-stu-id="727f8-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="727f8-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="727f8-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="727f8-211">Säilytä tietueen lisäystoiminto, jotta voit lisätä tietueita kunkin Intrastat-raportointiprosessin tietojen arkistoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="727f8-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="727f8-212">Valitse Tietueen infoloki -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="727f8-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="727f8-213">Valitse Kyllä, kun haluat hakea sovellustietojen päivityksen ongelmien tiedot.</span><span class="sxs-lookup"><span data-stu-id="727f8-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="727f8-214">Valitse Ohita tietueen toiminnon tarkistus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="727f8-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="727f8-215">Valitse Kyllä, jos haluat piilottaa tyhjän Intrastat-arkiston tunnus -kentän tarkistusvirheet.</span><span class="sxs-lookup"><span data-stu-id="727f8-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="727f8-216">Tämä tehdään tietueiden lisäämisen jälkeen tälle taululle ulkomaankaupan parametrilomakkeessa määritettyjen järjestysnumeroiden asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="727f8-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="727f8-217">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="727f8-217">Click OK.</span></span>
    * <span data-ttu-id="727f8-218">Sido lisätyn tietolähteen (suodatettu malli, joka perustuu valittuun juurinimikkeeseen) elementit lisätyn kohteen elementtien kanssa.</span><span class="sxs-lookup"><span data-stu-id="727f8-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="727f8-219">Laajenna puussa Archive.</span><span class="sxs-lookup"><span data-stu-id="727f8-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="727f8-220">Laajenna puussa Archive\<Relations.</span><span class="sxs-lookup"><span data-stu-id="727f8-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="727f8-221">Laajenna puussa Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="727f8-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="727f8-222">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="727f8-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="727f8-223">Laajenna puussa model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="727f8-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="727f8-224">Laajenna puussa model\Archive header\Enumerated lines\Value.</span><span class="sxs-lookup"><span data-stu-id="727f8-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="727f8-225">Valitse puussa model\Archive header\Enumerated lines\Value\Amount.</span><span class="sxs-lookup"><span data-stu-id="727f8-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="727f8-226">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-226">Click Bind.</span></span>
44. <span data-ttu-id="727f8-227">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="727f8-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="727f8-228">Valitse puussa model\Archive header\Enumerated lines\Value\Commodity rec id.</span><span class="sxs-lookup"><span data-stu-id="727f8-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="727f8-229">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-229">Click Bind.</span></span>
47. <span data-ttu-id="727f8-230">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).</span><span class="sxs-lookup"><span data-stu-id="727f8-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="727f8-231">Valitse puussa model\Archive header\Enumerated lines\Value\Item number.</span><span class="sxs-lookup"><span data-stu-id="727f8-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="727f8-232">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-232">Click Bind.</span></span>
50. <span data-ttu-id="727f8-233">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).</span><span class="sxs-lookup"><span data-stu-id="727f8-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="727f8-234">Valitse puussa model\Archive header\Enumerated lines\Number.</span><span class="sxs-lookup"><span data-stu-id="727f8-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="727f8-235">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-235">Click Bind.</span></span>
53. <span data-ttu-id="727f8-236">Valitse puussa Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="727f8-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="727f8-237">Valitse puussa model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="727f8-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="727f8-238">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-238">Click Bind.</span></span>
56. <span data-ttu-id="727f8-239">Valitse puussa Archive\File name(FileName).</span><span class="sxs-lookup"><span data-stu-id="727f8-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="727f8-240">Valitse puussa model\Archive header\File name.</span><span class="sxs-lookup"><span data-stu-id="727f8-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="727f8-241">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-241">Click Bind.</span></span>
59. <span data-ttu-id="727f8-242">Valitse puussa Archive\Number of lines(NumberOfLines).</span><span class="sxs-lookup"><span data-stu-id="727f8-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="727f8-243">Valitse puussa model\Archive header\Number of lines.</span><span class="sxs-lookup"><span data-stu-id="727f8-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="727f8-244">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-244">Click Bind.</span></span>
62. <span data-ttu-id="727f8-245">Valitse puussa Archive.</span><span class="sxs-lookup"><span data-stu-id="727f8-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="727f8-246">Valitse puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="727f8-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="727f8-247">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="727f8-247">Click Bind.</span></span>
65. <span data-ttu-id="727f8-248">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="727f8-248">Click Save.</span></span>
66. <span data-ttu-id="727f8-249">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="727f8-249">Close the page.</span></span>
67. <span data-ttu-id="727f8-250">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="727f8-250">Close the page.</span></span>
