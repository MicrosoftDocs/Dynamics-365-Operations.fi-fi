---
title: Valitse tietomallin määritykset luodessasi muotoja
description: ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.
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
ms.openlocfilehash: 374c31b5ea9160fba773e82f658e8de05c67cab4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143243"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="f8189-103">Valitse tietomallin määritykset luodessasi muotoja</span><span class="sxs-lookup"><span data-stu-id="f8189-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8189-104">ER Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen tämän menettelyn vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="f8189-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="f8189-105">Tässä menettelyssä kerrotaan, miten mallin juurinimike voidaan valita tietomallin määritelmäksi, kun sähköisten asiakirjojen luomista varten suunniteltu sähköisen raportoinnin (ER) muotokonfiguraatio lisätään.</span><span class="sxs-lookup"><span data-stu-id="f8189-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="f8189-106">Tässä menettelyssä lisätään uusi ER-muotokonfiguraatio malliyritykselle Litware Inc.</span><span class="sxs-lookup"><span data-stu-id="f8189-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="f8189-107">Nämä ohjeet on tarkoitettu käyttäjille, joille on määritetty järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän rooli.</span><span class="sxs-lookup"><span data-stu-id="f8189-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="f8189-108">Vaiheet voidaan suorittaa minkä tahansa tietojoukon avulla.</span><span class="sxs-lookup"><span data-stu-id="f8189-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="f8189-109">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="f8189-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f8189-110">Varmista, onko Litware, Inc. -malliyrityksen konfiguraation lähde käytettävissä ja merkitty aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="f8189-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="f8189-111">Jos konfiguraation lähde ei ole näkyvissä, suorita Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="f8189-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="f8189-112">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="f8189-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="f8189-113">Uuden ER-tietomallin konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="f8189-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="f8189-114">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="f8189-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="f8189-115">Lisätään uusi ER-mallin konfiguraatio. Se sisältää tietomallin, joka on tarkoitettu tietolähteeksi ER-raporttien luomisessa.</span><span class="sxs-lookup"><span data-stu-id="f8189-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="f8189-116">Syötä Nimi-kenttään Maksumalli (kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="f8189-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="f8189-117">Maksumalli (kuvitteellinen)</span><span class="sxs-lookup"><span data-stu-id="f8189-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="f8189-118">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="f8189-118">Click Create configuration.</span></span>
4. <span data-ttu-id="f8189-119">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f8189-119">Click Designer.</span></span>
    * <span data-ttu-id="f8189-120">Avaa ER-suunnitteluohjelma ja määritä tämän konfiguraation tietomallin rakenne.</span><span class="sxs-lookup"><span data-stu-id="f8189-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="f8189-121">Oletetaan, että suunnittelemme maksujen liiketoimintatoimialueelle tietomallin, joka tukee kahta maksutapaa: tilisiirto ja suoraveloitus.</span><span class="sxs-lookup"><span data-stu-id="f8189-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="f8189-122">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f8189-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="f8189-123">Syötä Nimi-kenttään Maksut – tilisiirto.</span><span class="sxs-lookup"><span data-stu-id="f8189-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="f8189-124">Maksut – tilisiirto</span><span class="sxs-lookup"><span data-stu-id="f8189-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="f8189-125">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f8189-125">Click Add.</span></span>
8. <span data-ttu-id="f8189-126">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="f8189-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="f8189-127">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="f8189-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="f8189-128">Syötä Nimi-kenttään Maksut – suoraveloitus.</span><span class="sxs-lookup"><span data-stu-id="f8189-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="f8189-129">Maksut – suoraveloitus</span><span class="sxs-lookup"><span data-stu-id="f8189-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="f8189-130">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="f8189-130">Click Add.</span></span>
12. <span data-ttu-id="f8189-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f8189-131">Click Save.</span></span>
13. <span data-ttu-id="f8189-132">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8189-132">Close the page.</span></span>
14. <span data-ttu-id="f8189-133">Voit muuttaa tilaa valitsemalla Muuta.</span><span class="sxs-lookup"><span data-stu-id="f8189-133">Click Change status.</span></span>
    * <span data-ttu-id="f8189-134">Tee mallin luonnosversio valmiiksi, jotta se on uusien mallien yhdistämismääritysten ja muotojen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="f8189-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="f8189-135">Valitse Valmis.</span><span class="sxs-lookup"><span data-stu-id="f8189-135">Click Complete.</span></span>
16. <span data-ttu-id="f8189-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8189-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="f8189-137">Aloita syöttämällä uusi ER-muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="f8189-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="f8189-138">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="f8189-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f8189-139">Anna Uusi-kenttään Muoto perustuu tietomallin maksumalliin (kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="f8189-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="f8189-140">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="f8189-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f8189-141">Ota huomioon, että kaikki valitun tietomallin juurinimikkeet ovat tällä hetkellä valittavissa tietomallin määritelmäksi.</span><span class="sxs-lookup"><span data-stu-id="f8189-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="f8189-142">Voit jatkaa muodon suunnittelua käyttämällä mitä tahansa tietomallin pakollista juurinimikettä.</span><span class="sxs-lookup"><span data-stu-id="f8189-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="f8189-143">Valitun juurinimikkeen puuttuva mallin yhdistämismääritys ei estä jatkamasta.</span><span class="sxs-lookup"><span data-stu-id="f8189-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="f8189-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8189-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="f8189-145">Uuden ER-mallin yhdistämismäärityksen konfiguraation lisääminen</span><span class="sxs-lookup"><span data-stu-id="f8189-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="f8189-146">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="f8189-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="f8189-147">Anna Uusi-kenttään Mallin yhdistämismääritys perustuu tietomallin maksumalliin (kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="f8189-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="f8189-148">Syötä Nimi-kenttään Maksumallin yhdistämismääritykset (kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="f8189-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="f8189-149">Maksumallin yhdistämismääritykset (kuvitteellinen)</span><span class="sxs-lookup"><span data-stu-id="f8189-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="f8189-150">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="f8189-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="f8189-151">Valitse Luo konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="f8189-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="f8189-152">ER-mallin yhdistämismääritysten suunnittelu</span><span class="sxs-lookup"><span data-stu-id="f8189-152">Design ER model mappings</span></span>
1. <span data-ttu-id="f8189-153">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f8189-153">Click Designer.</span></span>
    * <span data-ttu-id="f8189-154">Määritä pakollisten juurinimikkeiden mallien yhdistämismääritykset ER-suunnitteluohjelman avulla.</span><span class="sxs-lookup"><span data-stu-id="f8189-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="f8189-155">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="f8189-155">Click Designer.</span></span>
    * <span data-ttu-id="f8189-156">Simuloi valitun mallin yhdistämismäärityksen asetus valitun mallin juurinimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="f8189-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="f8189-157">Valitse puussa Dynamics 365 for Operations\Table records.</span><span class="sxs-lookup"><span data-stu-id="f8189-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="f8189-158">Valitse Lisää juuri.</span><span class="sxs-lookup"><span data-stu-id="f8189-158">Click Add root.</span></span>
5. <span data-ttu-id="f8189-159">Kirjoita Nimi -kenttään Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="f8189-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="f8189-160">Syötä Taulu-kenttään LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="f8189-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="f8189-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="f8189-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="f8189-162">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f8189-162">Click OK.</span></span>
8. <span data-ttu-id="f8189-163">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f8189-163">Click Save.</span></span>
9. <span data-ttu-id="f8189-164">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8189-164">Close the page.</span></span>
10. <span data-ttu-id="f8189-165">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8189-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="f8189-166">Aloita syöttämällä toinen ER-muotokonfiguraatio</span><span class="sxs-lookup"><span data-stu-id="f8189-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="f8189-167">Valitse puussa Payment model (fictitious).</span><span class="sxs-lookup"><span data-stu-id="f8189-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="f8189-168">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="f8189-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="f8189-169">Anna Uusi-kenttään Muoto perustuu tietomallin maksumalliin (kuvitteellinen).</span><span class="sxs-lookup"><span data-stu-id="f8189-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="f8189-170">Anna tai valitse Tietomallin määritelmä -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="f8189-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="f8189-171">Ota huomioon, että nyt sovelluksen tietolähteisiin yhdistettäviä juurinimikkeitä on käytettävissä vain yksi.</span><span class="sxs-lookup"><span data-stu-id="f8189-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="f8189-172">Kun vähintään yksi mallin yhdistämismääritys on esitelty, vain sovelluksen tietolähteisiin yhdistettyjä mallin juurinimikkeitä voi valita mallin määritelmäksi ER-muodon lisäyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f8189-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="f8189-173">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f8189-173">Close the page.</span></span>

