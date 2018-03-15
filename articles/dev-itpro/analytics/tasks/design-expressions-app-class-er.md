--- 
title: "Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)"
description: "Tässä oppaassa on tietoja aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin (ER) konfiguraatioissa kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: b0a1dba5afbd7beba45149340f637223f6ecedcf
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---
# <a name="design-expressions-to-call-application-class-methods-er"></a><span data-ttu-id="8d519-103">Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)</span><span class="sxs-lookup"><span data-stu-id="8d519-103">Design expressions to call application class methods (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d519-104">Tässä oppaassa on tietoja aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin (ER) konfiguraatioissa kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa.</span><span class="sxs-lookup"><span data-stu-id="8d519-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="8d519-105">Luokkien kutsumisen argumenttien arvot voidaan määrittää dynaamisesti suorituksen aikana esimerkiksi jäsennysasiakirjan perusteella. Näin varmistetaan tietojen oikeellisuus.</span><span class="sxs-lookup"><span data-stu-id="8d519-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="8d519-106">Tässä oppaassa luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware Inc. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="8d519-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="8d519-107">Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="8d519-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="8d519-108">Seuraava tiedosto on lisäksi ladattava ja tallennettava paikallisesti: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="8d519-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="8d519-109">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="8d519-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="8d519-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="8d519-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="8d519-111">Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="8d519-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="8d519-112">Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8d519-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="8d519-113">Oletetaan, että suunnittelet saapuvien tiliotteiden jäsennysprosessia sovellustietojen päivitys varten.</span><span class="sxs-lookup"><span data-stu-id="8d519-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="8d519-114">Saat saapuvat tiliotteet TXT-tiedostoina, joissa on IBAN-koodeja.</span><span class="sxs-lookup"><span data-stu-id="8d519-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="8d519-115">IBAN-koodit on tarkistettava tiliotteiden osana tuontiprosessia. Tähän tarkistukseen käytetään Dynamics 365 for Finance and Operations, Enterprise editioniin sisältyvää logiikkaa.</span><span class="sxs-lookup"><span data-stu-id="8d519-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="8d519-116">Uuden ER-mallimäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="8d519-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="8d519-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="8d519-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="8d519-118">Valitse Microsoft-toimittaja-ruutu.</span><span class="sxs-lookup"><span data-stu-id="8d519-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="8d519-119">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="8d519-119">Click Repositories.</span></span>
3. <span data-ttu-id="8d519-120">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="8d519-120">Click Show filters.</span></span>
4. <span data-ttu-id="8d519-121">Lisää suodattimen kenttä Tyyppinimi.</span><span class="sxs-lookup"><span data-stu-id="8d519-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="8d519-122">Anna Nimi-kentässä resurssit-arvo. Valitse ensin sisältää-suodatinoperaattori ja sitten Käytä.</span><span class="sxs-lookup"><span data-stu-id="8d519-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="8d519-123">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="8d519-123">Click Open.</span></span>
6. <span data-ttu-id="8d519-124">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="8d519-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="8d519-125">Jos Versiot-pikavälilehden Tuo-painike ei ole käytössä, olet jo tuonut version 1, joka on eräs ER-konfiguraation maksumalleista.</span><span class="sxs-lookup"><span data-stu-id="8d519-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="8d519-126">Voit ohittaa tämän alitehtävän seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="8d519-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="8d519-127">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="8d519-127">Click Import.</span></span>
8. <span data-ttu-id="8d519-128">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8d519-128">Click Yes.</span></span>
9. <span data-ttu-id="8d519-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d519-129">Close the page.</span></span>
10. <span data-ttu-id="8d519-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d519-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="8d519-131">Uuden ER-muotokonfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="8d519-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="8d519-132">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="8d519-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="8d519-133">Lisää uusi ER-muoto, jotta voit jäsentää saapuvat tiliotteet TXT-muodossa.</span><span class="sxs-lookup"><span data-stu-id="8d519-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="8d519-134">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="8d519-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="8d519-135">Avaa valintaikkunan valikko valitsemalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="8d519-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="8d519-136">Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="8d519-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="8d519-137">Kirjoita Nimi-kenttään Tiliotteen tuontimuoto (esimerkki).</span><span class="sxs-lookup"><span data-stu-id="8d519-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="8d519-138">Tiliotteen tuonnin muoto (esimerkki)</span><span class="sxs-lookup"><span data-stu-id="8d519-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="8d519-139">Valitse Tukee tietojen tuontia -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="8d519-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="8d519-140">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="8d519-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="8d519-141">ER-muotokonfiguraation suunnitteleminen - muoto</span><span class="sxs-lookup"><span data-stu-id="8d519-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="8d519-142">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="8d519-142">Click Designer.</span></span>
    * <span data-ttu-id="8d519-143">Suunniteltu muoto vastaa ulkoisen tiedoston odotettua rakennetta TXT-muodossa.</span><span class="sxs-lookup"><span data-stu-id="8d519-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="8d519-144">Avaa valintaikkunan valikko valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="8d519-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="8d519-145">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="8d519-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="8d519-146">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="8d519-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="8d519-147">Juuri</span><span class="sxs-lookup"><span data-stu-id="8d519-147">Root</span></span>  
5. <span data-ttu-id="8d519-148">Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".</span><span class="sxs-lookup"><span data-stu-id="8d519-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="8d519-149">Vaihtoehto Uusi rivi - Windows (CR LF) on valittu Erikoismerkit-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d519-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="8d519-150">Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään erillisenä tietueena.</span><span class="sxs-lookup"><span data-stu-id="8d519-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="8d519-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-151">Click OK.</span></span>
7. <span data-ttu-id="8d519-152">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d519-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="8d519-153">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="8d519-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="8d519-154">Kirjoita Nimi-kenttään Rivit.</span><span class="sxs-lookup"><span data-stu-id="8d519-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="8d519-155">Rivit</span><span class="sxs-lookup"><span data-stu-id="8d519-155">Rows</span></span>  
10. <span data-ttu-id="8d519-156">Valitse Monimuotoisuus-kentässä Yksi tai useita.</span><span class="sxs-lookup"><span data-stu-id="8d519-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="8d519-157">Vaihtoehto Yksi tai useita on valittu Monimuotoisuus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8d519-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="8d519-158">Tämän asetuksen perusteella jäsennystiedostossa odotetaan olevan vähintään yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="8d519-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="8d519-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-159">Click OK.</span></span>
12. <span data-ttu-id="8d519-160">Valitse puussa Root\Rows.</span><span class="sxs-lookup"><span data-stu-id="8d519-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="8d519-161">Valitse Lisää järjestys.</span><span class="sxs-lookup"><span data-stu-id="8d519-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="8d519-162">Kirjoita Nimi-kenttään Kentät.</span><span class="sxs-lookup"><span data-stu-id="8d519-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="8d519-163">Kentät</span><span class="sxs-lookup"><span data-stu-id="8d519-163">Fields</span></span>  
15. <span data-ttu-id="8d519-164">Valitse Monimuotoisuus-kentässä Tasan yksi.</span><span class="sxs-lookup"><span data-stu-id="8d519-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="8d519-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-165">Click OK.</span></span>
17. <span data-ttu-id="8d519-166">Valitse puussa Root\Rows\Fields.</span><span class="sxs-lookup"><span data-stu-id="8d519-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="8d519-167">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="8d519-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="8d519-168">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="8d519-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="8d519-169">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="8d519-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="8d519-170">IBAN-tilinumero</span><span class="sxs-lookup"><span data-stu-id="8d519-170">IBAN</span></span>  
21. <span data-ttu-id="8d519-171">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-171">Click OK.</span></span>
    * <span data-ttu-id="8d519-172">Jäsennystiedoston jokainen rivi sisältää vain yhden IBAN-koodin.</span><span class="sxs-lookup"><span data-stu-id="8d519-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="8d519-173">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d519-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="8d519-174">ER-muotokonfiguraation suunnitteleminen - yhdistämismääritys tietomalliin</span><span class="sxs-lookup"><span data-stu-id="8d519-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="8d519-175">Valitse Yhdistä muoto malliin.</span><span class="sxs-lookup"><span data-stu-id="8d519-175">Click Map format to model.</span></span>
2. <span data-ttu-id="8d519-176">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8d519-176">Click New.</span></span>
3. <span data-ttu-id="8d519-177">Kirjoita Määritys-kenttään BankToCustomerDebitCreditNotificationInitiation.</span><span class="sxs-lookup"><span data-stu-id="8d519-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="8d519-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="8d519-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="8d519-179">ResolveChanges, määritelmä.</span><span class="sxs-lookup"><span data-stu-id="8d519-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="8d519-180">Kirjoita Nimi-kenttään Yhdistämismääritys tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="8d519-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="8d519-181">Yhdistämismääritys tietomalliin</span><span class="sxs-lookup"><span data-stu-id="8d519-181">Mapping to data model</span></span>  
6. <span data-ttu-id="8d519-182">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d519-182">Click Save.</span></span>
7. <span data-ttu-id="8d519-183">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="8d519-183">Click Designer.</span></span>
8. <span data-ttu-id="8d519-184">Valitse puussa Dynamics 365 for Operations\Class.</span><span class="sxs-lookup"><span data-stu-id="8d519-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="8d519-185">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="8d519-185">Click Add root.</span></span>
    * <span data-ttu-id="8d519-186">Lisää uusi tietolähde, joka kutsuu aiemmin luotua sovelluslogiikkaa IBAN-koodien tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="8d519-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="8d519-187">Kirjoita Nimi-kenttään tarkista koodit.</span><span class="sxs-lookup"><span data-stu-id="8d519-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="8d519-188">tarkista koodit</span><span class="sxs-lookup"><span data-stu-id="8d519-188">check_codes</span></span>  
11. <span data-ttu-id="8d519-189">Kirjoita Luokka-kenttään ISO7064.</span><span class="sxs-lookup"><span data-stu-id="8d519-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="8d519-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="8d519-190">ISO7064</span></span>  
12. <span data-ttu-id="8d519-191">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-191">Click OK.</span></span>
13. <span data-ttu-id="8d519-192">Laajenna puussa format.</span><span class="sxs-lookup"><span data-stu-id="8d519-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="8d519-193">Laajenna puussa format\Root: Sequence(Root).</span><span class="sxs-lookup"><span data-stu-id="8d519-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="8d519-194">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="8d519-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="8d519-195">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d519-195">Click Bind.</span></span>
17. <span data-ttu-id="8d519-196">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="8d519-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="8d519-197">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields).</span><span class="sxs-lookup"><span data-stu-id="8d519-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="8d519-198">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).</span><span class="sxs-lookup"><span data-stu-id="8d519-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="8d519-199">Laajenna puussa 'Payments = format.Root.Rows'.</span><span class="sxs-lookup"><span data-stu-id="8d519-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="8d519-200">Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="8d519-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="8d519-201">Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification.</span><span class="sxs-lookup"><span data-stu-id="8d519-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="8d519-202">Valitse puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN.</span><span class="sxs-lookup"><span data-stu-id="8d519-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="8d519-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="8d519-203">Click Bind.</span></span>
25. <span data-ttu-id="8d519-204">Valitse Vahvistukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8d519-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="8d519-205">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8d519-205">Click New.</span></span>
    * <span data-ttu-id="8d519-206">Lisää uusi tarkistussääntö, joka näyttää virheen jokaisella virheellisen IBAN-koodin sisältävällä jäsennystiedoston rivillä.</span><span class="sxs-lookup"><span data-stu-id="8d519-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="8d519-207">Valitse Muokkaa ehtoa.</span><span class="sxs-lookup"><span data-stu-id="8d519-207">Click Edit condition.</span></span>
28. <span data-ttu-id="8d519-208">Laajenna puussa 'check_codes'.</span><span class="sxs-lookup"><span data-stu-id="8d519-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="8d519-209">Valitse puussa check_codes\verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="8d519-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="8d519-210">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="8d519-210">Click Add data source.</span></span>
31. <span data-ttu-id="8d519-211">Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="8d519-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="8d519-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="8d519-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="8d519-213">Laajenna puussa format.</span><span class="sxs-lookup"><span data-stu-id="8d519-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="8d519-214">Laajenna puussa format\Root: Sequence(Root).</span><span class="sxs-lookup"><span data-stu-id="8d519-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="8d519-215">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="8d519-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="8d519-216">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields).</span><span class="sxs-lookup"><span data-stu-id="8d519-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="8d519-217">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).</span><span class="sxs-lookup"><span data-stu-id="8d519-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="8d519-218">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="8d519-218">Click Add data source.</span></span>
38. <span data-ttu-id="8d519-219">Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="8d519-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="8d519-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="8d519-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="8d519-221">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d519-221">Click Save.</span></span>
40. <span data-ttu-id="8d519-222">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d519-222">Close the page.</span></span>
    * <span data-ttu-id="8d519-223">Tarkistusehto on määritetty palauttamaan FALSE jokaisen virheellisen IBAN-koodin kohdalla. Se kutsuu sovellusluokan ISO7064 olemassa olevaa menetelmää verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="8d519-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="8d519-224">Huomaa, että IBAN-koodin arvo määritetään dynaamisesti suorituksen aikana, koska kutsumenetelmän argumentti perustuu jäsennettävän TXT-tiedoston sisältöön.</span><span class="sxs-lookup"><span data-stu-id="8d519-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="8d519-225">Valitse Muokkaa sanomaa.</span><span class="sxs-lookup"><span data-stu-id="8d519-225">Click Edit message.</span></span>
42. <span data-ttu-id="8d519-226">Syötä Kaava-kenttään 'CONCATENATE("Löytyi virheellinen IBAN-kood: ", format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="8d519-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="8d519-227">CONCATENATE("Löytyi virheellinen IBAN-koodi: ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="8d519-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="8d519-228">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d519-228">Click Save.</span></span>
44. <span data-ttu-id="8d519-229">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d519-229">Close the page.</span></span>
45. <span data-ttu-id="8d519-230">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8d519-230">Click Save.</span></span>
46. <span data-ttu-id="8d519-231">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8d519-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="8d519-232">Muodon yhdistämismäärityksen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="8d519-232">Run the format mapping</span></span>
<span data-ttu-id="8d519-233">Testausta varten voit suorittaa muodon yhdistämismäärityksen käyttämällä aiemmin ladattua SampleIncomingMessage.txt-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="8d519-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="8d519-234">Luodut tiedot sisältävät tietoja, jotka tuodaan valitusta TXT-tiedostosta ja joilla täytetään mukautetun tietomallin tiedot varsinaisen tuonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8d519-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="8d519-235">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="8d519-235">Click Run.</span></span>
    * <span data-ttu-id="8d519-236">Valitse Selaa ja siirry aiemmin ladattuun SampleIncomingMessage.txt-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="8d519-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="8d519-237">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8d519-237">Click OK.</span></span>
    * <span data-ttu-id="8d519-238">Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="8d519-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="8d519-239">Huomaa, että vain 3 tuodun TXT-tiedoston riviä on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="8d519-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="8d519-240">Rivillä 4 oleva IBAN-koodi, joka ei ole sallittu, on ohitettu. Infolokissa on virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="8d519-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  


