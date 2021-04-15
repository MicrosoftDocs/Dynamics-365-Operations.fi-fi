---
title: Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja
description: Tässä aiheessa käsitellään sähköisen raportoinnin (ER) määritysten suunnittelua sähköisen asiakirjan luontia ja sovellustietojen päivitystä varten. (Osa 2 – Asiakirjojen luonti).
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b1771d0e01702162192ff20c03facbba4f3513
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751603"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="a0cfe-104">Muokkaa malleja ja yhdistämismäärityksiä luodaksesi sovellustietoja sisältäviä asiakirjoja</span><span class="sxs-lookup"><span data-stu-id="a0cfe-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0cfe-105">Voit suorittaa tämän menettelyn vaiheet sen jälkeen, kun ER Asiakirjojen luominen sovellustietojen päivityksen kanssa (Osa 2: asiakirjojen luominen) -menettely on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="a0cfe-106">Tämän menettelyn vaiheissa opastetaan, miten sähköisen raportoinnin (ER) konfiguraatiot suunnitellaan sähköisen asiakirjan luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="a0cfe-107">Tässä menettelyssä muokataan ER-konfiguraatioita ja aloitetaan niiden käyttäminen sähköisten asiakirjojen luomista ja sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="a0cfe-108">Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a0cfe-109">Nämä vaiheet voidaan suorittaa DEMF-tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="a0cfe-110">Tietomallin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="a0cfe-110">Modify data model</span></span>
1. <span data-ttu-id="a0cfe-111">Valitse Organisaation hallinto > Sähköinen raportointi > Konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a0cfe-112">Valitse puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="a0cfe-113">Voit laajentaa tietomallin käyttötapaa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-113">You will extend how you use the data model.</span></span> <span data-ttu-id="a0cfe-114">Tietomallia käytetään Intrastat-raportin luonnissa käytettävänä tietolähteenä sekä Intrastat-raportointiprosessin tietojen keräämisessä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="a0cfe-115">Tietoja käytetään tämän jälkeen sovellustietojen päivityksessä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="a0cfe-116">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-116">Click Designer.</span></span>
4. <span data-ttu-id="a0cfe-117">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="a0cfe-118">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="a0cfe-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="a0cfe-119">Kirjoita Nimi-kenttään Sovellustietojen päivitystä varten.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="a0cfe-120">Sovellustietojen päivitystä varten</span><span class="sxs-lookup"><span data-stu-id="a0cfe-120">For application data update</span></span>  
7. <span data-ttu-id="a0cfe-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-121">Click Add.</span></span>
8. <span data-ttu-id="a0cfe-122">Valitse puussa For application data update.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="a0cfe-123">Tämä uusi juurinimike lisätään määrittämään tietovirta, jota käytetään (tietolähteenä käytettävän) Intrastar-raportin tietojen siirtämiseen sovellustauluihin (päivityskohde).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="a0cfe-124">Huomaa, että lähtevään asiakirjaan kirjattujen tietojen ja sovellustietojen päivityksessä käytettävän asiakirjan tietojen haussa on käytettävä eri juurinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="a0cfe-125">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="a0cfe-126">Syötä Nimi-kenttään Arkiston otsikko.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="a0cfe-127">Arkiston otsikko</span><span class="sxs-lookup"><span data-stu-id="a0cfe-127">Archive header</span></span>  
11. <span data-ttu-id="a0cfe-128">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="a0cfe-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-129">Click Add.</span></span>
    * <span data-ttu-id="a0cfe-130">Koska luot jokaiselle luodulle Intrastat-raportille tietueen, raportille on luotava uusi nimike.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="a0cfe-131">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="a0cfe-132">Kirjoita Nimi-kenttään "Tiedoston nimi".</span><span class="sxs-lookup"><span data-stu-id="a0cfe-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="a0cfe-133">Tiedostonimi</span><span class="sxs-lookup"><span data-stu-id="a0cfe-133">File name</span></span>  
15. <span data-ttu-id="a0cfe-134">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="a0cfe-135">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-135">Click Add.</span></span>
17. <span data-ttu-id="a0cfe-136">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="a0cfe-137">Syötä Nimi-kenttään Rivien määrä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="a0cfe-138">Rivien määrä</span><span class="sxs-lookup"><span data-stu-id="a0cfe-138">Number of lines</span></span>  
19. <span data-ttu-id="a0cfe-139">Valitse Nimiketyyppi-kentässä Kokonaisluku.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="a0cfe-140">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-140">Click Add.</span></span>
    * <span data-ttu-id="a0cfe-141">Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien määrää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="a0cfe-142">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="a0cfe-143">Syötä Nimi-kenttään Arkiston rivit.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="a0cfe-144">Arkiston rivit</span><span class="sxs-lookup"><span data-stu-id="a0cfe-144">Archive lines</span></span>  
23. <span data-ttu-id="a0cfe-145">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="a0cfe-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-146">Click Add.</span></span>
    * <span data-ttu-id="a0cfe-147">Lisää tämä nimike osoittamaan nykyisen raportointiprosessin aikana raportoitujen Intrastat-tapahtumien luetteloa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="a0cfe-148">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="a0cfe-149">Syötä Nimi-kenttään Summa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="a0cfe-150">Määrä</span><span class="sxs-lookup"><span data-stu-id="a0cfe-150">Amount</span></span>  
27. <span data-ttu-id="a0cfe-151">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="a0cfe-152">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-152">Click Add.</span></span>
29. <span data-ttu-id="a0cfe-153">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="a0cfe-154">Kirjoita Nimi-kenttään Kauppatavaratietueen tunnus.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="a0cfe-155">Kauppatavaratietueen tunnus</span><span class="sxs-lookup"><span data-stu-id="a0cfe-155">Commodity rec id</span></span>  
31. <span data-ttu-id="a0cfe-156">Valitse Nimiketyyppi-kentässä Int64.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="a0cfe-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-157">Click Add.</span></span>
33. <span data-ttu-id="a0cfe-158">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="a0cfe-159">Syötä Nimi-kenttään Nimiketunnus.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="a0cfe-160">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="a0cfe-160">Item number</span></span>  
35. <span data-ttu-id="a0cfe-161">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="a0cfe-162">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-162">Click Add.</span></span>
37. <span data-ttu-id="a0cfe-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-163">Click Save.</span></span>
38. <span data-ttu-id="a0cfe-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="a0cfe-165">Mallin yhdistämismäärityksen muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="a0cfe-165">Modify model mapping</span></span>
1. <span data-ttu-id="a0cfe-166">Laajenna puussa Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="a0cfe-167">Valitse puussa Intrastat (model)\Intrastat (mapping).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="a0cfe-168">Muokkaa aiemmin määritettyä mallin yhdistämismääritystä, kun haluat aloittaa sen käytön sovellustietojen päivityksessä ja Intrastat-raportoinnin tietojen arkistoinnissa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="a0cfe-169">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-169">Click Designer.</span></span>
4. <span data-ttu-id="a0cfe-170">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-170">Click New.</span></span>
5. <span data-ttu-id="a0cfe-171">Syötä Nimi-kenttään Päivitä arkisto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="a0cfe-172">Arkiston päivittäminen</span><span class="sxs-lookup"><span data-stu-id="a0cfe-172">Update archive</span></span>  
6. <span data-ttu-id="a0cfe-173">Valitse Suunta-kentässä Kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="a0cfe-174">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-174">Click Save.</span></span>
    * <span data-ttu-id="a0cfe-175">Tämä uusi yhdistämismääritys määrittää tietovirran, jota käytetään tietojen (Intrastat-raportoinnin tietojen) siirtämisessä tietomallista sovellustauluihin (päivityskohde).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="a0cfe-176">Ota huomioon, että raportointiprosessin sovelluksen tietojen haussa ja sovellustietojen päivityksen tietomallin tietojen käytössä on käytettävä eri mallin juurinimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="a0cfe-177">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-177">Click Designer.</span></span>
9. <span data-ttu-id="a0cfe-178">Valitse puussa Data model\Data model.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="a0cfe-179">Lisää vaadittu tietolähde.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-179">Add the required data source.</span></span> <span data-ttu-id="a0cfe-180">Tämä on tietomalli, joka sisältää raportoitujen ja arkistoitavien Intrastat-tapahtumien tiedot.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="a0cfe-181">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-181">Click Add root.</span></span>
11. <span data-ttu-id="a0cfe-182">Kirjoita Nimi-kenttään malli.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="a0cfe-183">malli</span><span class="sxs-lookup"><span data-stu-id="a0cfe-183">model</span></span>  
12. <span data-ttu-id="a0cfe-184">Syötä tai valitse Määritelmä-kenttään Sovellustietojen päivitystä varten -arvo.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="a0cfe-185">Sovellustietojen päivitystä varten</span><span class="sxs-lookup"><span data-stu-id="a0cfe-185">For application data update</span></span>  
13. <span data-ttu-id="a0cfe-186">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-186">Click OK.</span></span>
14. <span data-ttu-id="a0cfe-187">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="a0cfe-188">Valitse puussa solmu Functions\Calculated field.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="a0cfe-189">Valitse puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="a0cfe-190">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-190">Click Add.</span></span>
    * <span data-ttu-id="a0cfe-191">Koska haluat luetteloida raportoidut Intrastat-tapahtumat arkistointia varten, soveltuva tietolähde on lisättävä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="a0cfe-192">Syötä Nimi-kenttään Luetteloidut rivit.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="a0cfe-193">Luetteloidut rivit</span><span class="sxs-lookup"><span data-stu-id="a0cfe-193">Enumerated lines</span></span>  
19. <span data-ttu-id="a0cfe-194">Valitse Muokkaa kaavaa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-194">Click Edit formula.</span></span>
20. <span data-ttu-id="a0cfe-195">Valitse puussa List\ENUMERATE.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="a0cfe-196">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-196">Click Add function.</span></span>
22. <span data-ttu-id="a0cfe-197">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="a0cfe-198">Laajenna puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="a0cfe-199">Valitse puussa model\Archive header\Archive lines.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="a0cfe-200">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-200">Click Add data source.</span></span>
26. <span data-ttu-id="a0cfe-201">Syötä Kaava-kenttään ENUMERATE(model.'Archive header'.'Archive lines').</span><span class="sxs-lookup"><span data-stu-id="a0cfe-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="a0cfe-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="a0cfe-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="a0cfe-203">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-203">Click Save.</span></span>
28. <span data-ttu-id="a0cfe-204">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-204">Close the page.</span></span>
29. <span data-ttu-id="a0cfe-205">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-205">Click OK.</span></span>
30. <span data-ttu-id="a0cfe-206">Valitse Lisää kohde.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-206">Click Add destination.</span></span>
    * <span data-ttu-id="a0cfe-207">Lisää sovellustaulut pakollisina kohteina, jotka vaativat päivitykset raportoitujen Intrastat-tapahtumien tietojen arkistointia varten.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="a0cfe-208">Kirjoita Nimi-kenttään Arkisto.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="a0cfe-209">Arkistoi</span><span class="sxs-lookup"><span data-stu-id="a0cfe-209">Archive</span></span>  
32. <span data-ttu-id="a0cfe-210">Kirjoita Taulun nimi -kenttään IntrastatArchiveGeneral.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="a0cfe-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="a0cfe-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="a0cfe-212">Säilytä tietueen lisäystoiminto, jotta voit lisätä tietueita kunkin Intrastat-raportointiprosessin tietojen arkistoinnin aikana.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="a0cfe-213">Valitse Tietueen infoloki -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="a0cfe-214">Valitse Kyllä, kun haluat hakea sovellustietojen päivityksen ongelmien tiedot.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="a0cfe-215">Valitse Ohita tietueen toiminnon tarkistus -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="a0cfe-216">Valitse Kyllä, jos haluat piilottaa tyhjän Intrastat-arkiston tunnus -kentän tarkistusvirheet.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="a0cfe-217">Tämä tehdään tietueiden lisäämisen jälkeen tälle taululle ulkomaankaupan parametrilomakkeessa määritettyjen järjestysnumeroiden asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="a0cfe-218">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-218">Click OK.</span></span>
    * <span data-ttu-id="a0cfe-219">Sido lisätyn tietolähteen (suodatettu malli, joka perustuu valittuun juurinimikkeeseen) elementit lisätyn kohteen elementtien kanssa.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="a0cfe-220">Laajenna puussa Archive.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="a0cfe-221">Laajenna puussa Archive\<Relations.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="a0cfe-222">Laajenna puussa Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="a0cfe-223">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="a0cfe-224">Laajenna puussa model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="a0cfe-225">Laajenna puussa model\Archive header\Enumerated lines\Value.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="a0cfe-226">Valitse puussa model\Archive header\Enumerated lines\Value\Amount.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="a0cfe-227">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-227">Click Bind.</span></span>
44. <span data-ttu-id="a0cfe-228">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="a0cfe-229">Valitse puussa model\Archive header\Enumerated lines\Value\Commodity rec id.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="a0cfe-230">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-230">Click Bind.</span></span>
47. <span data-ttu-id="a0cfe-231">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="a0cfe-232">Valitse puussa model\Archive header\Enumerated lines\Value\Item number.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="a0cfe-233">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-233">Click Bind.</span></span>
50. <span data-ttu-id="a0cfe-234">Valitse puussa Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="a0cfe-235">Valitse puussa model\Archive header\Enumerated lines\Number.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="a0cfe-236">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-236">Click Bind.</span></span>
53. <span data-ttu-id="a0cfe-237">Valitse puussa Archive\<Relations\IntrastatArchiveDetail.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="a0cfe-238">Valitse puussa model\Archive header\Enumerated lines.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="a0cfe-239">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-239">Click Bind.</span></span>
56. <span data-ttu-id="a0cfe-240">Valitse puussa Archive\File name(FileName).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="a0cfe-241">Valitse puussa model\Archive header\File name.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="a0cfe-242">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-242">Click Bind.</span></span>
59. <span data-ttu-id="a0cfe-243">Valitse puussa Archive\Number of lines(NumberOfLines).</span><span class="sxs-lookup"><span data-stu-id="a0cfe-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="a0cfe-244">Valitse puussa model\Archive header\Number of lines.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="a0cfe-245">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-245">Click Bind.</span></span>
62. <span data-ttu-id="a0cfe-246">Valitse puussa Archive.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="a0cfe-247">Valitse puussa model\Archive header.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="a0cfe-248">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-248">Click Bind.</span></span>
65. <span data-ttu-id="a0cfe-249">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-249">Click Save.</span></span>
66. <span data-ttu-id="a0cfe-250">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-250">Close the page.</span></span>
67. <span data-ttu-id="a0cfe-251">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a0cfe-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]