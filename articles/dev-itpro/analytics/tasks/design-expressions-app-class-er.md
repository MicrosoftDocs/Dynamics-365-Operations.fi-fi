---
title: Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)
description: Tässä oppaassa on tietoja aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin (ER) konfiguraatioissa kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdacd852eeed33b443a3c79b96fc4c4af04bb6b2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544883"
---
# <a name="design-er-expressions-to-call-application-class-methods"></a><span data-ttu-id="6bd09-103">Sovellusluokkamenetelmän kutsulausekkeiden suunnittelu (ER)</span><span class="sxs-lookup"><span data-stu-id="6bd09-103">Design ER expressions to call application class methods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6bd09-104">Tässä oppaassa on tietoja aiemmin luodun sovelluslogiikan käyttämisestä uudelleen sähköisen raportoinnin (ER) konfiguraatioissa kutsumalla sovellusluokkien pakollisia menetelmiä ER-lausekkeissa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-104">This guide provides information about how to reuse the existing application logic in Electronic reporting (ER) configurations by calling required methods of application classes in ER expressions.</span></span> <span data-ttu-id="6bd09-105">Luokkien kutsumisen argumenttien arvot voidaan määrittää dynaamisesti suorituksen aikana esimerkiksi jäsennysasiakirjan perusteella. Näin varmistetaan tietojen oikeellisuus.</span><span class="sxs-lookup"><span data-stu-id="6bd09-105">Values of arguments for calling classes can be defined dynamically at run-time: for example, based on information in the parsing document to ensure its correctness.</span></span> <span data-ttu-id="6bd09-106">Tässä oppaassa luodaan pakollisia ER-konfiguraatioita malliyritykselle Litware Inc. Tämä menettely on luotu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="6bd09-106">In this guide, you will create the required ER configurations for the sample company, Litware, Inc. This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="6bd09-107">Nämä vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="6bd09-107">These steps can be completed using any data set.</span></span> <span data-ttu-id="6bd09-108">Sinun on myös ladattava ja tallennettava paikallisesti seuraava tiedosto: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span><span class="sxs-lookup"><span data-stu-id="6bd09-108">You must also download and save the following file locally: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.</span></span>

<span data-ttu-id="6bd09-109">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="6bd09-109">To complete these steps, you must first complete the steps in the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="6bd09-110">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6bd09-111">Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-111">Verify that the configuration provider for sample company, Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="6bd09-112">Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6bd09-112">If you don’t see this configuration provider, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>   
    * <span data-ttu-id="6bd09-113">Oletetaan, että suunnittelet saapuvien tiliotteiden jäsennysprosessia sovellustietojen päivitys varten.</span><span class="sxs-lookup"><span data-stu-id="6bd09-113">Let’s assume that you are designing a process for parsing incoming bank statements for an application data update.</span></span> <span data-ttu-id="6bd09-114">Saat saapuvat tiliotteet TXT-tiedostoina, joissa on IBAN-koodeja.</span><span class="sxs-lookup"><span data-stu-id="6bd09-114">You will receive the incoming bank statements as TXT files that contain IBAN codes.</span></span> <span data-ttu-id="6bd09-115">IBAN-koodit on tarkistettava tiliotteiden osana tuontiprosessia. Tähän tarkistukseen käytetään Dynamics 365 for Finance and Operationsiin sisältyvää logiikkaa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-115">As part of the bank statement import process, you need to validate the correctness of this IBAN codes using the logic that is already available in Dynamics 365 for Finance and Operations.</span></span>   

## <a name="import-a-new-er-model-configuration"></a><span data-ttu-id="6bd09-116">Uuden ER-mallimäärityksen tuominen</span><span class="sxs-lookup"><span data-stu-id="6bd09-116">Import a new ER model configuration</span></span>
1. <span data-ttu-id="6bd09-117">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6bd09-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6bd09-118">Valitse Microsoft-toimittaja-ruutu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-118">Select the Microsoft provider tile.</span></span>  
2. <span data-ttu-id="6bd09-119">Valitse Säilöt.</span><span class="sxs-lookup"><span data-stu-id="6bd09-119">Click Repositories.</span></span>
3. <span data-ttu-id="6bd09-120">Valitse Näytä suodattimet.</span><span class="sxs-lookup"><span data-stu-id="6bd09-120">Click Show filters.</span></span>
4. <span data-ttu-id="6bd09-121">Lisää suodattimen kenttä Tyyppinimi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-121">Add a filter field ‘Type name’.</span></span> <span data-ttu-id="6bd09-122">Anna Nimi-kentässä resurssit-arvo. Valitse ensin sisältää-suodatinoperaattori ja sitten Käytä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-122">In the Name field, enter the value “resources”, select the “contains” filter operator, and then click Apply.</span></span>
5. <span data-ttu-id="6bd09-123">Valitse Avaa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-123">Click Open.</span></span>
6. <span data-ttu-id="6bd09-124">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="6bd09-124">In the tree, select 'Payment model'.</span></span>
    * <span data-ttu-id="6bd09-125">Jos Versiot-pikavälilehden Tuo-painike ei ole käytössä, olet jo tuonut version 1, joka on eräs ER-konfiguraation maksumalleista.</span><span class="sxs-lookup"><span data-stu-id="6bd09-125">If the Import button on the Versions FastTab is not enabled, you have already imported the version 1 one of the ER configuration ‘Payment model’.</span></span> <span data-ttu-id="6bd09-126">Voit ohittaa tämän alitehtävän seuraavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="6bd09-126">You can skip the rest steps in this sub-task.</span></span>   
7. <span data-ttu-id="6bd09-127">Valitse Tuo.</span><span class="sxs-lookup"><span data-stu-id="6bd09-127">Click Import.</span></span>
8. <span data-ttu-id="6bd09-128">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-128">Click Yes.</span></span>
9. <span data-ttu-id="6bd09-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-129">Close the page.</span></span>
10. <span data-ttu-id="6bd09-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-130">Close the page.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="6bd09-131">Uuden ER-muotokonfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="6bd09-131">Add a new ER format configuration</span></span>
1. <span data-ttu-id="6bd09-132">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="6bd09-132">Click Reporting configurations.</span></span>
    * <span data-ttu-id="6bd09-133">Lisää uusi ER-muoto, jotta voit jäsentää saapuvat tiliotteet TXT-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-133">Add a new ER format to parse incoming bank statements in TXT format.</span></span>  
2. <span data-ttu-id="6bd09-134">Valitse puussa solmu Maksumalli.</span><span class="sxs-lookup"><span data-stu-id="6bd09-134">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="6bd09-135">Avaa valintaikkunan valikko valitsemalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-135">Click Create configuration to open the dialog menu.</span></span>
4. <span data-ttu-id="6bd09-136">Syötä Uusi-kenttään Muoto perustuu tietomalliin PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="6bd09-136">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
5. <span data-ttu-id="6bd09-137">Kirjoita Nimi-kenttään Tiliotteen tuontimuoto (esimerkki).</span><span class="sxs-lookup"><span data-stu-id="6bd09-137">In the Name field, type 'Bank statement import format (sample)'.</span></span>
    * <span data-ttu-id="6bd09-138">Tiliotteen tuonnin muoto (esimerkki)</span><span class="sxs-lookup"><span data-stu-id="6bd09-138">Bank statement import format (sample)</span></span>  
6. <span data-ttu-id="6bd09-139">Valitse Tukee tietojen tuontia -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-139">Select Yes in the Supports data import field.</span></span>
7. <span data-ttu-id="6bd09-140">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="6bd09-140">Click Create configuration.</span></span>

## <a name="design-the-er-format-configuration---format"></a><span data-ttu-id="6bd09-141">ER-muotokonfiguraation suunnitteleminen - muoto</span><span class="sxs-lookup"><span data-stu-id="6bd09-141">Design the ER format configuration - format</span></span>
1. <span data-ttu-id="6bd09-142">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="6bd09-142">Click Designer.</span></span>
    * <span data-ttu-id="6bd09-143">Suunniteltu muoto vastaa ulkoisen tiedoston odotettua rakennetta TXT-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-143">The designed format represents the expected structure of the external file in TXT format.</span></span>  
2. <span data-ttu-id="6bd09-144">Avaa valintaikkunan valikko valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="6bd09-144">Click Add root to open the dialog menu.</span></span>
3. <span data-ttu-id="6bd09-145">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="6bd09-145">In the tree, select 'Text\Sequence'.</span></span>
4. <span data-ttu-id="6bd09-146">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="6bd09-146">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="6bd09-147">Juuri</span><span class="sxs-lookup"><span data-stu-id="6bd09-147">Root</span></span>  
5. <span data-ttu-id="6bd09-148">Valitse Erikoismerkit-kentässä "Uusi rivi - Windows (CR-LF)".</span><span class="sxs-lookup"><span data-stu-id="6bd09-148">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
    * <span data-ttu-id="6bd09-149">Vaihtoehto Uusi rivi - Windows (CR LF) on valittu Erikoismerkit-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-149">The option ‘New line - Windows (CR LF)’ has been selected in the ‘Special characters’ field.</span></span> <span data-ttu-id="6bd09-150">Tämän asetuksen perusteella jokaista jäsennystiedoston riviä pidetään erillisenä tietueena.</span><span class="sxs-lookup"><span data-stu-id="6bd09-150">Based on this setting, each line in the parsing file is considered a separate record.</span></span>  
6. <span data-ttu-id="6bd09-151">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-151">Click OK.</span></span>
7. <span data-ttu-id="6bd09-152">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="6bd09-152">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="6bd09-153">Valitse puussa "Text\Sequence".</span><span class="sxs-lookup"><span data-stu-id="6bd09-153">In the tree, select 'Text\Sequence'.</span></span>
9. <span data-ttu-id="6bd09-154">Kirjoita Nimi-kenttään Rivit.</span><span class="sxs-lookup"><span data-stu-id="6bd09-154">In the Name field, type 'Rows'.</span></span>
    * <span data-ttu-id="6bd09-155">Rivit</span><span class="sxs-lookup"><span data-stu-id="6bd09-155">Rows</span></span>  
10. <span data-ttu-id="6bd09-156">Valitse Monimuotoisuus-kentässä Yksi tai useita.</span><span class="sxs-lookup"><span data-stu-id="6bd09-156">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="6bd09-157">Vaihtoehto Yksi tai useita on valittu Monimuotoisuus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-157">The option ‘One many’ has been selected in the ‘Multiplicity’ field.</span></span> <span data-ttu-id="6bd09-158">Tämän asetuksen perusteella jäsennystiedostossa odotetaan olevan vähintään yksi rivi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-158">Based on this setting, it is expected that at least one line will be presented in the parsing file.</span></span>  
11. <span data-ttu-id="6bd09-159">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-159">Click OK.</span></span>
12. <span data-ttu-id="6bd09-160">Valitse puussa Root\Rows.</span><span class="sxs-lookup"><span data-stu-id="6bd09-160">In the tree, select 'Root\Rows'.</span></span>
13. <span data-ttu-id="6bd09-161">Valitse Lisää järjestys.</span><span class="sxs-lookup"><span data-stu-id="6bd09-161">Click Add Sequence.</span></span>
14. <span data-ttu-id="6bd09-162">Kirjoita Nimi-kenttään Kentät.</span><span class="sxs-lookup"><span data-stu-id="6bd09-162">In the Name field, type 'Fields'.</span></span>
    * <span data-ttu-id="6bd09-163">Kentät</span><span class="sxs-lookup"><span data-stu-id="6bd09-163">Fields</span></span>  
15. <span data-ttu-id="6bd09-164">Valitse Monimuotoisuus-kentässä Tasan yksi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-164">In the Multiplicity field, select 'Exactly one'.</span></span>
16. <span data-ttu-id="6bd09-165">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-165">Click OK.</span></span>
17. <span data-ttu-id="6bd09-166">Valitse puussa Root\Rows\Fields.</span><span class="sxs-lookup"><span data-stu-id="6bd09-166">In the tree, select 'Root\Rows\Fields'.</span></span>
18. <span data-ttu-id="6bd09-167">Avaa valintaikkuna valitsemalla Lisää.</span><span class="sxs-lookup"><span data-stu-id="6bd09-167">Click Add to open the drop dialog.</span></span>
19. <span data-ttu-id="6bd09-168">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="6bd09-168">In the tree, select 'Text\String'.</span></span>
20. <span data-ttu-id="6bd09-169">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="6bd09-169">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="6bd09-170">IBAN-tilinumero</span><span class="sxs-lookup"><span data-stu-id="6bd09-170">IBAN</span></span>  
21. <span data-ttu-id="6bd09-171">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-171">Click OK.</span></span>
    * <span data-ttu-id="6bd09-172">Jäsennystiedoston jokainen rivi sisältää vain yhden IBAN-koodin.</span><span class="sxs-lookup"><span data-stu-id="6bd09-172">It has been configured that each line in the parsing file contains the only IBAN code.</span></span>  
22. <span data-ttu-id="6bd09-173">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6bd09-173">Click Save.</span></span>

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a><span data-ttu-id="6bd09-174">ER-muotokonfiguraation suunnitteleminen - yhdistämismääritys tietomalliin</span><span class="sxs-lookup"><span data-stu-id="6bd09-174">Design the ER format configuration – mapping to data model</span></span>
1. <span data-ttu-id="6bd09-175">Valitse Yhdistä muoto malliin.</span><span class="sxs-lookup"><span data-stu-id="6bd09-175">Click Map format to model.</span></span>
2. <span data-ttu-id="6bd09-176">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-176">Click New.</span></span>
3. <span data-ttu-id="6bd09-177">Kirjoita Määritys-kenttään BankToCustomerDebitCreditNotificationInitiation.</span><span class="sxs-lookup"><span data-stu-id="6bd09-177">In the Definition field, type 'BankToCustomerDebitCreditNotificationInitiation'.</span></span>
    * <span data-ttu-id="6bd09-178">BankToCustomerDebitCreditNotificationInitiation</span><span class="sxs-lookup"><span data-stu-id="6bd09-178">BankToCustomerDebitCreditNotificationInitiation</span></span>  
4. <span data-ttu-id="6bd09-179">ResolveChanges, määritelmä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-179">ResolveChanges the Definition.</span></span>
5. <span data-ttu-id="6bd09-180">Kirjoita Nimi-kenttään Yhdistämismääritys tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="6bd09-180">In the Name field, type 'Mapping to data model'.</span></span>
    * <span data-ttu-id="6bd09-181">Yhdistämismääritys tietomalliin</span><span class="sxs-lookup"><span data-stu-id="6bd09-181">Mapping to data model</span></span>  
6. <span data-ttu-id="6bd09-182">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6bd09-182">Click Save.</span></span>
7. <span data-ttu-id="6bd09-183">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="6bd09-183">Click Designer.</span></span>
8. <span data-ttu-id="6bd09-184">Valitse puussa Dynamics 365 for Operations\Class.</span><span class="sxs-lookup"><span data-stu-id="6bd09-184">In the tree, select 'Dynamics 365 for Operations\Class'.</span></span>
9. <span data-ttu-id="6bd09-185">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="6bd09-185">Click Add root.</span></span>
    * <span data-ttu-id="6bd09-186">Lisää uusi tietolähde, joka kutsuu aiemmin luotua sovelluslogiikkaa IBAN-koodien tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="6bd09-186">Add a new data source to call the existing application logic for IBAN codes validation.</span></span>  
10. <span data-ttu-id="6bd09-187">Kirjoita Nimi-kenttään tarkista koodit.</span><span class="sxs-lookup"><span data-stu-id="6bd09-187">In the Name field, type 'check_codes'.</span></span>
    * <span data-ttu-id="6bd09-188">tarkista koodit</span><span class="sxs-lookup"><span data-stu-id="6bd09-188">check_codes</span></span>  
11. <span data-ttu-id="6bd09-189">Kirjoita Luokka-kenttään ISO7064.</span><span class="sxs-lookup"><span data-stu-id="6bd09-189">In the Class field, type 'ISO7064'.</span></span>
    * <span data-ttu-id="6bd09-190">ISO7064</span><span class="sxs-lookup"><span data-stu-id="6bd09-190">ISO7064</span></span>  
12. <span data-ttu-id="6bd09-191">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-191">Click OK.</span></span>
13. <span data-ttu-id="6bd09-192">Laajenna puussa format.</span><span class="sxs-lookup"><span data-stu-id="6bd09-192">In the tree, expand 'format'.</span></span>
14. <span data-ttu-id="6bd09-193">Laajenna puussa format\Root: Sequence(Root).</span><span class="sxs-lookup"><span data-stu-id="6bd09-193">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
15. <span data-ttu-id="6bd09-194">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="6bd09-194">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
16. <span data-ttu-id="6bd09-195">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="6bd09-195">Click Bind.</span></span>
17. <span data-ttu-id="6bd09-196">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="6bd09-196">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
18. <span data-ttu-id="6bd09-197">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields).</span><span class="sxs-lookup"><span data-stu-id="6bd09-197">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
19. <span data-ttu-id="6bd09-198">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).</span><span class="sxs-lookup"><span data-stu-id="6bd09-198">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
20. <span data-ttu-id="6bd09-199">Laajenna puussa 'Payments = format.Root.Rows'.</span><span class="sxs-lookup"><span data-stu-id="6bd09-199">In the tree, expand 'Payments = format.Root.Rows'.</span></span>
21. <span data-ttu-id="6bd09-200">Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount).</span><span class="sxs-lookup"><span data-stu-id="6bd09-200">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)'.</span></span>
22. <span data-ttu-id="6bd09-201">Laajenna puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification.</span><span class="sxs-lookup"><span data-stu-id="6bd09-201">In the tree, expand 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification'.</span></span>
23. <span data-ttu-id="6bd09-202">Valitse puussa Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN.</span><span class="sxs-lookup"><span data-stu-id="6bd09-202">In the tree, select 'Payments = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.</span></span>
24. <span data-ttu-id="6bd09-203">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="6bd09-203">Click Bind.</span></span>
25. <span data-ttu-id="6bd09-204">Valitse Vahvistukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="6bd09-204">Click the Validations tab.</span></span>
26. <span data-ttu-id="6bd09-205">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6bd09-205">Click New.</span></span>
    * <span data-ttu-id="6bd09-206">Lisää uusi tarkistussääntö, joka näyttää virheen jokaisella virheellisen IBAN-koodin sisältävällä jäsennystiedoston rivillä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-206">Add a new validation rule that displays an error for any line in the parsing file that contains invalid IBAN code.</span></span>  
27. <span data-ttu-id="6bd09-207">Valitse Muokkaa ehtoa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-207">Click Edit condition.</span></span>
28. <span data-ttu-id="6bd09-208">Laajenna puussa 'check_codes'.</span><span class="sxs-lookup"><span data-stu-id="6bd09-208">In the tree, expand 'check_codes'.</span></span>
29. <span data-ttu-id="6bd09-209">Valitse puussa check_codes\verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="6bd09-209">In the tree, select 'check_codes\verifyMOD1271_36'.</span></span>
30. <span data-ttu-id="6bd09-210">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6bd09-210">Click Add data source.</span></span>
31. <span data-ttu-id="6bd09-211">Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36('.</span><span class="sxs-lookup"><span data-stu-id="6bd09-211">In the Formula field, enter 'check_codes.verifyMOD1271_36('.</span></span>
    * <span data-ttu-id="6bd09-212">check_codes.verifyMOD1271_36(</span><span class="sxs-lookup"><span data-stu-id="6bd09-212">check_codes.verifyMOD1271_36(</span></span>  
32. <span data-ttu-id="6bd09-213">Laajenna puussa format.</span><span class="sxs-lookup"><span data-stu-id="6bd09-213">In the tree, expand 'format'.</span></span>
33. <span data-ttu-id="6bd09-214">Laajenna puussa format\Root: Sequence(Root).</span><span class="sxs-lookup"><span data-stu-id="6bd09-214">In the tree, expand 'format\Root: Sequence(Root)'.</span></span>
34. <span data-ttu-id="6bd09-215">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows).</span><span class="sxs-lookup"><span data-stu-id="6bd09-215">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)'.</span></span>
35. <span data-ttu-id="6bd09-216">Laajenna puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields).</span><span class="sxs-lookup"><span data-stu-id="6bd09-216">In the tree, expand 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)'.</span></span>
36. <span data-ttu-id="6bd09-217">Valitse puussa format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN).</span><span class="sxs-lookup"><span data-stu-id="6bd09-217">In the tree, select 'format\Root: Sequence(Root)\Rows: Sequence 1..\* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.</span></span>
37. <span data-ttu-id="6bd09-218">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="6bd09-218">Click Add data source.</span></span>
38. <span data-ttu-id="6bd09-219">Syötä Kaava-kenttään 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="6bd09-219">In the Formula field, enter 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="6bd09-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="6bd09-220">check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)</span></span>  
39. <span data-ttu-id="6bd09-221">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6bd09-221">Click Save.</span></span>
40. <span data-ttu-id="6bd09-222">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-222">Close the page.</span></span>
    * <span data-ttu-id="6bd09-223">Tarkistusehto on määritetty palauttamaan FALSE jokaisen virheellisen IBAN-koodin kohdalla. Se kutsuu sovellusluokan ISO7064 olemassa olevaa menetelmää verifyMOD1271_36.</span><span class="sxs-lookup"><span data-stu-id="6bd09-223">The validation condition has been configured to return FALSE for any invalid IBAN code by calling the existing method ‘verifyMOD1271_36’ of the application class ‘ISO7064’.</span></span> <span data-ttu-id="6bd09-224">Huomaa, että IBAN-koodin arvo määritetään dynaamisesti suorituksen aikana, koska kutsumenetelmän argumentti perustuu jäsennettävän TXT-tiedoston sisältöön.</span><span class="sxs-lookup"><span data-stu-id="6bd09-224">Note that the value of the IBAN code is defined dynamically at run-time as the argument of the calling method based on the content of the parsing TXT file.</span></span>   
41. <span data-ttu-id="6bd09-225">Valitse Muokkaa sanomaa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-225">Click Edit message.</span></span>
42. <span data-ttu-id="6bd09-226">Syötä Kaava-kenttään 'CONCATENATE("Löytyi virheellinen IBAN-kood: ", format.Root.Rows.Fields.IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="6bd09-226">In the Formula field, enter 'CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)'.</span></span>
    * <span data-ttu-id="6bd09-227">CONCATENATE("Löytyi virheellinen IBAN-koodi: ", format.Root.Rows.Fields.IBAN)</span><span class="sxs-lookup"><span data-stu-id="6bd09-227">CONCATENATE("Invalid IBAN code has been found:  ", format.Root.Rows.Fields.IBAN)</span></span>  
43. <span data-ttu-id="6bd09-228">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6bd09-228">Click Save.</span></span>
44. <span data-ttu-id="6bd09-229">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-229">Close the page.</span></span>
45. <span data-ttu-id="6bd09-230">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="6bd09-230">Click Save.</span></span>
46. <span data-ttu-id="6bd09-231">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6bd09-231">Close the page.</span></span>

## <a name="run-the-format-mapping"></a><span data-ttu-id="6bd09-232">Muodon yhdistämismäärityksen suorittaminen</span><span class="sxs-lookup"><span data-stu-id="6bd09-232">Run the format mapping</span></span>
<span data-ttu-id="6bd09-233">Testausta varten voit suorittaa muodon yhdistämismäärityksen käyttämällä aiemmin ladattua SampleIncomingMessage.txt-tiedostoa.</span><span class="sxs-lookup"><span data-stu-id="6bd09-233">For testing purposes, execute the format mapping using the SampleIncomingMessage.txt file that you downloaded.</span></span> <span data-ttu-id="6bd09-234">Luodut tiedot sisältävät tietoja, jotka tuodaan valitusta TXT-tiedostosta ja joilla täytetään mukautetun tietomallin tiedot varsinaisen tuonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="6bd09-234">The generated output includes data that will be imported from the selected TXT file and populated to the custom data model during the real import.</span></span>   
1. <span data-ttu-id="6bd09-235">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="6bd09-235">Click Run.</span></span>
    * <span data-ttu-id="6bd09-236">Valitse Selaa ja siirry aiemmin ladattuun SampleIncomingMessage.txt-tiedostoon.</span><span class="sxs-lookup"><span data-stu-id="6bd09-236">Click Browse and navigate to the SampleIncomingMessage.txt file that you previously downloaded.</span></span>  
2. <span data-ttu-id="6bd09-237">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bd09-237">Click OK.</span></span>
    * <span data-ttu-id="6bd09-238">Tarkista XML-muotoiset tiedot. Nämä tiedot on tuotu valitusta tiedostosta ja siirretty tietomalliin.</span><span class="sxs-lookup"><span data-stu-id="6bd09-238">Review the output in XML format that represents the data that has been imported from the selected file and ported to the data model.</span></span> <span data-ttu-id="6bd09-239">Huomaa, että vain 3 tuodun TXT-tiedoston riviä on käsitelty.</span><span class="sxs-lookup"><span data-stu-id="6bd09-239">Note that only 3 lines of the imported TXT file were processed.</span></span> <span data-ttu-id="6bd09-240">Rivillä 4 oleva IBAN-koodi, joka ei ole sallittu, on ohitettu. Infolokissa on virhesanoma.</span><span class="sxs-lookup"><span data-stu-id="6bd09-240">The IBAN code on line 4 that is not valid was skipped and an error message is provided in the Infolog.</span></span>  

