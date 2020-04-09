---
title: Hallitse ER-mallien kartoitusta erillisissä ER-konfiguraatioissa
description: Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi hallita sähköisen raportoinnin (ER) mallin yhdistämismäärityksiä erillisissä ER-konfiguraatioissa.
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
ms.openlocfilehash: b8ff3b419caafec626497c65ea18ca24ca95cb5d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143050"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="02b71-103">Hallitse ER-mallien kartoitusta erillisissä ER-konfiguraatioissa</span><span class="sxs-lookup"><span data-stu-id="02b71-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02b71-104">Seuraavissa vaiheissa kerrotaan, miten käyttäjä, jolla on järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli, voi hallita sähköisen raportoinnin (ER) mallin yhdistämismäärityksiä erillisissä ER-konfiguraatioissa.</span><span class="sxs-lookup"><span data-stu-id="02b71-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="02b71-105">Tässä tehtäväoppaassa luodaan pakollisia ER-määrityksiä malliyritykselle Litware, Inc. Tätä tehtäväopastaa varten on suoritettava ensin ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="02b71-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="02b71-106">Voit suorittaa tämän tehtäväoppaan valitsemasi yrityksen tietojoukon avulla, koska yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="02b71-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="02b71-107">Tässä oppaassa tehtävä toiminto on käytettävissä, jos olet asentanut jonkin seuraavista hotfix-korjauksista: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 Dynamics AX 7.0 -versiolle tai https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 Dynamics 365 for Operations -versiolle.</span><span class="sxs-lookup"><span data-stu-id="02b71-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="02b71-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="02b71-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="02b71-109">Tarkista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja onko se merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="02b71-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="02b71-110">Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -tehtäväoppaan vaiheet.</span><span class="sxs-lookup"><span data-stu-id="02b71-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="02b71-111">Uuden ER-mallimäärityksen lisääminen</span><span class="sxs-lookup"><span data-stu-id="02b71-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="02b71-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="02b71-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="02b71-113">Luo uusi mallin konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="02b71-113">Add a new model configuration.</span></span> <span data-ttu-id="02b71-114">Konfiguraatioiden puurakenteen nimen on oltava yksilöivä.</span><span class="sxs-lookup"><span data-stu-id="02b71-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="02b71-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="02b71-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="02b71-116">Syötä Nimi-kenttään Tietomallin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="02b71-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="02b71-117">Tietomallin esimerkki</span><span class="sxs-lookup"><span data-stu-id="02b71-117">Sample data model</span></span>  
4. <span data-ttu-id="02b71-118">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="02b71-118">Click Create configuration.</span></span>
5. <span data-ttu-id="02b71-119">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-119">Click Designer.</span></span>
6. <span data-ttu-id="02b71-120">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="02b71-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="02b71-121">Kirjoita Nimi-kenttään "Juuri".</span><span class="sxs-lookup"><span data-stu-id="02b71-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="02b71-122">Juuri</span><span class="sxs-lookup"><span data-stu-id="02b71-122">Root</span></span>  
8. <span data-ttu-id="02b71-123">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="02b71-123">Click Add.</span></span>
9. <span data-ttu-id="02b71-124">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="02b71-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="02b71-125">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="02b71-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="02b71-126">Yritys </span><span class="sxs-lookup"><span data-stu-id="02b71-126">Company</span></span>  
11. <span data-ttu-id="02b71-127">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="02b71-127">Click Add.</span></span>
12. <span data-ttu-id="02b71-128">Syötä Kuvaus-kenttään teksti, yrityksen kuvaus tai yritys, johon käyttäjä oli kirjautuneena suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="02b71-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="02b71-129">Sen yrityksen kuvaus, johon käyttäjä on kirjautuneena suorituksen aikana.</span><span class="sxs-lookup"><span data-stu-id="02b71-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="02b71-130">Valitse Juuriviite.</span><span class="sxs-lookup"><span data-stu-id="02b71-130">Click Root reference.</span></span>
14. <span data-ttu-id="02b71-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-131">Click OK.</span></span>
15. <span data-ttu-id="02b71-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="02b71-132">Click Save.</span></span>
16. <span data-ttu-id="02b71-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-133">Close the page.</span></span>
17. <span data-ttu-id="02b71-134">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="02b71-134">Click Change status.</span></span>
18. <span data-ttu-id="02b71-135">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="02b71-135">Click Complete.</span></span>
19. <span data-ttu-id="02b71-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="02b71-137">Uuden ER-mallin yhdistämismäärityksen konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="02b71-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="02b71-138">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="02b71-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="02b71-139">Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Tietomallin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="02b71-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="02b71-140">Syötä Nimi-kenttään Esimerkkiyhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="02b71-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="02b71-141">Esimerkkiyhdistämismääritys</span><span class="sxs-lookup"><span data-stu-id="02b71-141">Sample mapping</span></span>  
4. <span data-ttu-id="02b71-142">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="02b71-142">Click Create configuration.</span></span>
5. <span data-ttu-id="02b71-143">Laajenna Edellytykset-osa.</span><span class="sxs-lookup"><span data-stu-id="02b71-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="02b71-144">Huomaa, että toteutusten edellytysten ryhmä on lisätty automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="02b71-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="02b71-145">Ryhmä sisältää edellytetyn komponentin, joka viittaa päätietomallin konfiguraatioon ja jossa käytetään Toteutus-merkintää.</span><span class="sxs-lookup"><span data-stu-id="02b71-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="02b71-146">Merkintä tarkoittaa, että Esimerkkiyhdistämismääritys-yhdistämismäärityksen konfiguraatiota pidetään Esimerkki-tietomallin toteutuksena.</span><span class="sxs-lookup"><span data-stu-id="02b71-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="02b71-147">Tämä vuoksi tämä komponentti pakottaa sähköisen raportoinnin lataamaan mallin yhdistämismäärityksen konfiguraation (Esimerkkiyhdistämismääritys) sähköisen raportoinnin säilöstä, kun mallin konfiguraatio, Esimerkkitietomalli, ladataan.</span><span class="sxs-lookup"><span data-stu-id="02b71-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="02b71-148">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-148">Click Designer.</span></span>
    * <span data-ttu-id="02b71-149">Ota huomioon, että luotu mallin yhdistämismäärityksen kokoonpano sisältää uuden tyhjän yhdistämismäärityksen, jolla on sama nimi kuin luodulla konfiguraatiolla.</span><span class="sxs-lookup"><span data-stu-id="02b71-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="02b71-150">Huomioi, että kun valittu päämallin konfiguraatio sisältää mallin yhdistämismäärityksiä, ne kopioidaan uuteen mallin yhdistämismäärityksen konfiguraatioon.</span><span class="sxs-lookup"><span data-stu-id="02b71-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="02b71-151">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-151">Click Designer.</span></span>
8. <span data-ttu-id="02b71-152">Valitse puussa Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="02b71-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="02b71-153">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="02b71-153">Click Add root.</span></span>
10. <span data-ttu-id="02b71-154">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="02b71-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="02b71-155">Yritys </span><span class="sxs-lookup"><span data-stu-id="02b71-155">Company</span></span>  
11. <span data-ttu-id="02b71-156">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="02b71-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="02b71-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="02b71-157">CompanyInfo</span></span>  
12. <span data-ttu-id="02b71-158">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-158">Click OK.</span></span>
13. <span data-ttu-id="02b71-159">Laajenna puussa Company.</span><span class="sxs-lookup"><span data-stu-id="02b71-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="02b71-160">Laajenna puussa Company\find().</span><span class="sxs-lookup"><span data-stu-id="02b71-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="02b71-161">Valitse puussa Company\find()\Name.</span><span class="sxs-lookup"><span data-stu-id="02b71-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="02b71-162">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="02b71-162">Click Bind.</span></span>
17. <span data-ttu-id="02b71-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="02b71-163">Click Save.</span></span>
18. <span data-ttu-id="02b71-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-164">Close the page.</span></span>
19. <span data-ttu-id="02b71-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-165">Close the page.</span></span>
20. <span data-ttu-id="02b71-166">Valitse toimintoruudussa Konfiguroinnit.</span><span class="sxs-lookup"><span data-stu-id="02b71-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="02b71-167">Valitse Käyttäjän parametrit.</span><span class="sxs-lookup"><span data-stu-id="02b71-167">Click User parameters.</span></span>
22. <span data-ttu-id="02b71-168">Valitse Suorita asetukset -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="02b71-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="02b71-169">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-169">Click OK.</span></span>
24. <span data-ttu-id="02b71-170">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="02b71-170">Click Edit.</span></span>
25. <span data-ttu-id="02b71-171">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="02b71-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="02b71-172">Uuden ER-muotokonfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="02b71-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="02b71-173">Valitse puussa Sample data model.</span><span class="sxs-lookup"><span data-stu-id="02b71-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="02b71-174">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="02b71-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="02b71-175">Anna Uusi-kenttään Muoto perustuu tietomalliin Tietomallin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="02b71-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="02b71-176">Syötä Nimi-kenttään Esimerkkimuoto.</span><span class="sxs-lookup"><span data-stu-id="02b71-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="02b71-177">Esimerkkimuoto</span><span class="sxs-lookup"><span data-stu-id="02b71-177">Sample format</span></span>  
5. <span data-ttu-id="02b71-178">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="02b71-178">Click Create configuration.</span></span>
6. <span data-ttu-id="02b71-179">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-179">Click Designer.</span></span>
7. <span data-ttu-id="02b71-180">Avaa valintaikkuna valitsemalla Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="02b71-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="02b71-181">Valitse puussa solmu Text\String.</span><span class="sxs-lookup"><span data-stu-id="02b71-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="02b71-182">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-182">Click OK.</span></span>
10. <span data-ttu-id="02b71-183">Valitse Yhdistämismääritys-välilehti.</span><span class="sxs-lookup"><span data-stu-id="02b71-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="02b71-184">Laajenna puussa solmu model.</span><span class="sxs-lookup"><span data-stu-id="02b71-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="02b71-185">Valitse puussa model\Company.</span><span class="sxs-lookup"><span data-stu-id="02b71-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="02b71-186">Valitse Sido.</span><span class="sxs-lookup"><span data-stu-id="02b71-186">Click Bind.</span></span>
14. <span data-ttu-id="02b71-187">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="02b71-187">Click Save.</span></span>
15. <span data-ttu-id="02b71-188">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-188">Close the page.</span></span>
    * <span data-ttu-id="02b71-189">Suorita luodun muodon luonnosversio testausta varten.</span><span class="sxs-lookup"><span data-stu-id="02b71-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="02b71-190">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="02b71-190">Click Run.</span></span>
    * <span data-ttu-id="02b71-191">Valitse Versiot-pikavälilehdessä Suorita.</span><span class="sxs-lookup"><span data-stu-id="02b71-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="02b71-192">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-192">Click OK.</span></span>
    * <span data-ttu-id="02b71-193">Tarkista tulos, joka sisältää sen yrityksen nimen, johon tämän muotokonfiguraation suorittava käyttäjä on kirjautunut.</span><span class="sxs-lookup"><span data-stu-id="02b71-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="02b71-194">Ota huomioon, että tämä muotokonfiguraatio käyttää tätä mallin yhdistämismäärityksen konfiguraatiota, koska vaaditut mallin yhdistämismääritykset sisältäviä konfiguraatioita on vain yksi.</span><span class="sxs-lookup"><span data-stu-id="02b71-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="02b71-195">Vaihtoehtoisen ER-mallin yhdistämismäärityksen konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="02b71-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="02b71-196">Valitse puussa Sample data model.</span><span class="sxs-lookup"><span data-stu-id="02b71-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="02b71-197">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="02b71-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="02b71-198">Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomalliin Tietomallin esimerkki.</span><span class="sxs-lookup"><span data-stu-id="02b71-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="02b71-199">Syötä Nimi-kenttään Esimerkkiyhdistämismääritys (vaihtoehto).</span><span class="sxs-lookup"><span data-stu-id="02b71-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="02b71-200">Esimerkkiyhdistämismääritys (vaihtoehto)</span><span class="sxs-lookup"><span data-stu-id="02b71-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="02b71-201">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="02b71-201">Click Create configuration.</span></span>
6. <span data-ttu-id="02b71-202">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-202">Click Designer.</span></span>
7. <span data-ttu-id="02b71-203">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-203">Click Designer.</span></span>
8. <span data-ttu-id="02b71-204">Valitse puussa Dynamics 365 for Operations\Table.</span><span class="sxs-lookup"><span data-stu-id="02b71-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="02b71-205">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="02b71-205">Click Add root.</span></span>
10. <span data-ttu-id="02b71-206">Syötä Nimi-kenttään Yritys.</span><span class="sxs-lookup"><span data-stu-id="02b71-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="02b71-207">Yritys </span><span class="sxs-lookup"><span data-stu-id="02b71-207">Company</span></span>  
11. <span data-ttu-id="02b71-208">Syötä Taulu-kenttään CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="02b71-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="02b71-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="02b71-209">CompanyInfo</span></span>  
12. <span data-ttu-id="02b71-210">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-210">Click OK.</span></span>
13. <span data-ttu-id="02b71-211">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="02b71-211">Click Edit.</span></span>
14. <span data-ttu-id="02b71-212">Valitse puussa solmu String\CONCATENATE.</span><span class="sxs-lookup"><span data-stu-id="02b71-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="02b71-213">Valitse Lisää toiminto.</span><span class="sxs-lookup"><span data-stu-id="02b71-213">Click Add function.</span></span>
16. <span data-ttu-id="02b71-214">Laajenna puussa Company.</span><span class="sxs-lookup"><span data-stu-id="02b71-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="02b71-215">Laajenna puussa Company\find().</span><span class="sxs-lookup"><span data-stu-id="02b71-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="02b71-216">Valitse puussa Company\find()\Name.</span><span class="sxs-lookup"><span data-stu-id="02b71-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="02b71-217">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="02b71-217">Click Add data source.</span></span>
20. <span data-ttu-id="02b71-218">Kirjoita arvo Resepti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="02b71-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="02b71-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="02b71-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="02b71-220">Valitse puussa Company\find()\Company(DataArea).</span><span class="sxs-lookup"><span data-stu-id="02b71-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="02b71-221">Valitse Lisää tietolähde.</span><span class="sxs-lookup"><span data-stu-id="02b71-221">Click Add data source.</span></span>
23. <span data-ttu-id="02b71-222">Kirjoita arvo Resepti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="02b71-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="02b71-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="02b71-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="02b71-224">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="02b71-224">Click Save.</span></span>
25. <span data-ttu-id="02b71-225">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-225">Close the page.</span></span>
26. <span data-ttu-id="02b71-226">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="02b71-226">Click Save.</span></span>
27. <span data-ttu-id="02b71-227">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-227">Close the page.</span></span>
28. <span data-ttu-id="02b71-228">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="02b71-228">Close the page.</span></span>
29. <span data-ttu-id="02b71-229">Valitse Suorita luonnos -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="02b71-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="02b71-230">Aiemmin määritetyn ER-mallin yhdistämismäärityksen konfiguraation käyttäminen</span><span class="sxs-lookup"><span data-stu-id="02b71-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="02b71-231">Valitse puussa Sample data model\Sample format.</span><span class="sxs-lookup"><span data-stu-id="02b71-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="02b71-232">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="02b71-232">Click Run.</span></span>
    * <span data-ttu-id="02b71-233">Ota huomioon, että ER-muotokonfiguraation luonnosversiota ei voi suorittaa, koska suoritettavan ER-muodon tietolähteeksi valitulla määrittämättömällä tietomallilla on käytettävissä useita mallin yhdistämismäärityksen konfiguraatioita.</span><span class="sxs-lookup"><span data-stu-id="02b71-233">Note that the selected draft version of the ER format configuration can't be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="02b71-234">Seuraavaksi määritetään vaihtoehtoinen mallin yhdistämismäärityksen konfiguraatio, josta mallin yhdistämismäärityksiä käytetään tietolähteinä ER-muodon suorituksessa.</span><span class="sxs-lookup"><span data-stu-id="02b71-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="02b71-235">Valitse puussa Sample data model\Sample mapping (alternative).</span><span class="sxs-lookup"><span data-stu-id="02b71-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="02b71-236">Valitse Mallin määrityksen oletusarvo -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="02b71-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="02b71-237">Valitse puussa Sample data model\Sample format.</span><span class="sxs-lookup"><span data-stu-id="02b71-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="02b71-238">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="02b71-238">Click Run.</span></span>
7. <span data-ttu-id="02b71-239">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02b71-239">Click OK.</span></span>
    * <span data-ttu-id="02b71-240">Ota huomioon, että tämä muotokonfiguraatio käyttää mallin yhdistämismäärityksen oletuskonfiguraatiota sähköisen asiakirjan (luotu tuloste sisältää yrityskoodin) luomiseen.</span><span class="sxs-lookup"><span data-stu-id="02b71-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

