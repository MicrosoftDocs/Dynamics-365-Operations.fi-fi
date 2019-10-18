---
title: ER Suunnittele toimialueen erityistietomalli
description: Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d66cc69da08478ceb931fab594da51bafcacc38
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185080"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="4d727-103">ER Suunnittele toimialueen erityistietomalli</span><span class="sxs-lookup"><span data-stu-id="4d727-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d727-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin.</span><span class="sxs-lookup"><span data-stu-id="4d727-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="4d727-105">Tietomallia käytetään myöhemmin tietolähteenä, kun maksuasiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="4d727-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="4d727-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4d727-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="4d727-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="4d727-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="4d727-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="4d727-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="4d727-109">Valitse malliyrityksen Litware, Inc:n konfiguraation lähde.</span><span class="sxs-lookup"><span data-stu-id="4d727-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="4d727-110">Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="4d727-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="4d727-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="4d727-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="4d727-112">Luodaan konfiguraatio, joka sisältää tietomallin sähköisen maksun asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="4d727-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="4d727-113">Tietomallia käytetään myöhemmin tietolähteenä, kun maksujen asiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="4d727-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="4d727-114">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="4d727-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="4d727-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="4d727-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="4d727-116">Syötä Nimi-kenttään Maksut (yksinkertaistettu malli).</span><span class="sxs-lookup"><span data-stu-id="4d727-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="4d727-117">Maksut (yksinkertaistettu malli)</span><span class="sxs-lookup"><span data-stu-id="4d727-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="4d727-118">Syötä Kuvaus-kenttään Maksumallin konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="4d727-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="4d727-119">Maksumallin konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="4d727-119">Payment model configuration</span></span>  
    * <span data-ttu-id="4d727-120">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="4d727-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="4d727-121">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="4d727-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="4d727-122">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="4d727-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="4d727-123">Suorita konfiguraation luontitehtävä valitsemalla Luo konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="4d727-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="4d727-124">Tietomallin luominen</span><span class="sxs-lookup"><span data-stu-id="4d727-124">Create a data model</span></span>
    * <span data-ttu-id="4d727-125">Olet luomassa valitulle määritykselle uutta tietomallia.</span><span class="sxs-lookup"><span data-stu-id="4d727-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="4d727-126">Konfiguraation version tilaksi tulee Luonnos.</span><span class="sxs-lookup"><span data-stu-id="4d727-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="4d727-127">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="4d727-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="4d727-128">Maksuprosessiin osallistuvan osapuolen rakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d727-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="4d727-129">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4d727-130">Kirjoita Nimi-kenttään Osapuoli.</span><span class="sxs-lookup"><span data-stu-id="4d727-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="4d727-131">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="4d727-131">Party</span></span>  
3. <span data-ttu-id="4d727-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-132">Click Add.</span></span>
4. <span data-ttu-id="4d727-133">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="4d727-134">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="4d727-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="4d727-135">Nimi</span><span class="sxs-lookup"><span data-stu-id="4d727-135">Name</span></span>  
6. <span data-ttu-id="4d727-136">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d727-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="4d727-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-137">Click Add.</span></span>
8. <span data-ttu-id="4d727-138">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="4d727-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="4d727-139">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="4d727-139">Party</span></span>  
9. <span data-ttu-id="4d727-140">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="4d727-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="4d727-141">Pankkirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="4d727-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="4d727-142">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4d727-143">Syötä Nimi-kenttään Agentti.</span><span class="sxs-lookup"><span data-stu-id="4d727-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="4d727-144">Edustaja</span><span class="sxs-lookup"><span data-stu-id="4d727-144">Agent</span></span>  
3. <span data-ttu-id="4d727-145">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="4d727-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="4d727-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-146">Click Add.</span></span>
5. <span data-ttu-id="4d727-147">Kirjoita Kuvaus-kenttään "Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä".</span><span class="sxs-lookup"><span data-stu-id="4d727-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="4d727-148">Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä.</span><span class="sxs-lookup"><span data-stu-id="4d727-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="4d727-149">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="4d727-150">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="4d727-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="4d727-151">Nimi</span><span class="sxs-lookup"><span data-stu-id="4d727-151">Name</span></span>  
8. <span data-ttu-id="4d727-152">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d727-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="4d727-153">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-153">Click Add.</span></span>
10. <span data-ttu-id="4d727-154">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="4d727-155">Syötä Nimi-kenttään SWIFT.</span><span class="sxs-lookup"><span data-stu-id="4d727-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="4d727-156">SWIFT-koodi</span><span class="sxs-lookup"><span data-stu-id="4d727-156">SWIFT</span></span>  
12. <span data-ttu-id="4d727-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-157">Click Add.</span></span>
13. <span data-ttu-id="4d727-158">Kirjoita Kuvaus-kenttään "BIC-koodi".</span><span class="sxs-lookup"><span data-stu-id="4d727-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="4d727-159">BIC-koodi</span><span class="sxs-lookup"><span data-stu-id="4d727-159">Bank identification code</span></span>  
14. <span data-ttu-id="4d727-160">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="4d727-161">Syötä Nimi-kenttään RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="4d727-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="4d727-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="4d727-162">RoutingNumber</span></span>  
16. <span data-ttu-id="4d727-163">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-163">Click Add.</span></span>
17. <span data-ttu-id="4d727-164">Kirjoita Kuvaus-kenttään "Pankkikoodi".</span><span class="sxs-lookup"><span data-stu-id="4d727-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="4d727-165">Pankkikoodi</span><span class="sxs-lookup"><span data-stu-id="4d727-165">Routing number</span></span>  
18. <span data-ttu-id="4d727-166">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="4d727-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="4d727-167">Pankkitilirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="4d727-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="4d727-168">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4d727-169">Syötä Nimi-kenttään Tili.</span><span class="sxs-lookup"><span data-stu-id="4d727-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="4d727-170">Tili</span><span class="sxs-lookup"><span data-stu-id="4d727-170">Account</span></span>  
3. <span data-ttu-id="4d727-171">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="4d727-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="4d727-172">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-172">Click Add.</span></span>
5. <span data-ttu-id="4d727-173">Kirjoita Kuvaus-kenttään "Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa)".</span><span class="sxs-lookup"><span data-stu-id="4d727-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="4d727-174">Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa).</span><span class="sxs-lookup"><span data-stu-id="4d727-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="4d727-175">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="4d727-176">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="4d727-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="4d727-177">Valuutta</span><span class="sxs-lookup"><span data-stu-id="4d727-177">Currency</span></span>  
8. <span data-ttu-id="4d727-178">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d727-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="4d727-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-179">Click Add.</span></span>
10. <span data-ttu-id="4d727-180">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="4d727-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="4d727-181">Valuuttakoodi</span><span class="sxs-lookup"><span data-stu-id="4d727-181">Currency code</span></span>  
11. <span data-ttu-id="4d727-182">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="4d727-183">Syötä Nimi-kenttään Numero.</span><span class="sxs-lookup"><span data-stu-id="4d727-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="4d727-184">Numero</span><span class="sxs-lookup"><span data-stu-id="4d727-184">Number</span></span>  
13. <span data-ttu-id="4d727-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-185">Click Add.</span></span>
14. <span data-ttu-id="4d727-186">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="4d727-187">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="4d727-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="4d727-188">IBAN-tilinumero</span><span class="sxs-lookup"><span data-stu-id="4d727-188">IBAN</span></span>  
16. <span data-ttu-id="4d727-189">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-189">Click Add.</span></span>
17. <span data-ttu-id="4d727-190">Kirjoita Kuvaus-kenttään "Kansainvälinen tilinumero (IBAN)".</span><span class="sxs-lookup"><span data-stu-id="4d727-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="4d727-191">Kansainvälinen tilinumero (IBAN)</span><span class="sxs-lookup"><span data-stu-id="4d727-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="4d727-192">Tilisiirtomaksun tyypin maksuviestirakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4d727-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="4d727-193">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="4d727-194">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="4d727-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="4d727-195">Syötä Nimi-kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="4d727-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="4d727-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="4d727-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="4d727-197">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-197">Click Add.</span></span>
5. <span data-ttu-id="4d727-198">Kirjoita Etsi--kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="4d727-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="4d727-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="4d727-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="4d727-200">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="4d727-200">Click Find previous.</span></span>
7. <span data-ttu-id="4d727-201">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="4d727-202">Syötä Nimi-kenttään MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="4d727-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="4d727-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="4d727-203">MessageIdentification</span></span>  
9. <span data-ttu-id="4d727-204">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-204">Click Add.</span></span>
10. <span data-ttu-id="4d727-205">Kirjoita Kuvaus-kenttään "Osoitetaan pisteviitteeseen ohjaavan osapuolen määrityksen mukaisesti (ja lähetetään seuraavalle osapuolelle) viestin tunnistamista varten".</span><span class="sxs-lookup"><span data-stu-id="4d727-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="4d727-206">Pisteestä pisteeseen -viite, jonka ohjaava osapuoli on määrittänyt (ja lähettänyt seuraavalle osapuolelle) viestin tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="4d727-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="4d727-207">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="4d727-208">Syötä Nimi-kenttään ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="4d727-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="4d727-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="4d727-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="4d727-210">Valitse Nimiketyyppi-kentässä DateTime.</span><span class="sxs-lookup"><span data-stu-id="4d727-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="4d727-211">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-211">Click Add.</span></span>
15. <span data-ttu-id="4d727-212">Kirjoita Kuvaus-kenttään "Päivämäärä ja kellonaika, jolloin maksun viesti luotiin".</span><span class="sxs-lookup"><span data-stu-id="4d727-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="4d727-213">Päivämäärä ja kellonaika, jolloin maksun viesti luotiin.</span><span class="sxs-lookup"><span data-stu-id="4d727-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="4d727-214">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="4d727-215">Pankkitapahtumarakenteen määrittäminen tälle mallille.</span><span class="sxs-lookup"><span data-stu-id="4d727-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="4d727-216">Syötä Nimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="4d727-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="4d727-217">Maksut</span><span class="sxs-lookup"><span data-stu-id="4d727-217">Payments</span></span>  
18. <span data-ttu-id="4d727-218">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="4d727-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="4d727-219">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-219">Click Add.</span></span>
20. <span data-ttu-id="4d727-220">Syötä Kuvaus-kenttään Nykyisen viestin maksurivi.</span><span class="sxs-lookup"><span data-stu-id="4d727-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="4d727-221">Nykyisen viestin maksurivit</span><span class="sxs-lookup"><span data-stu-id="4d727-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="4d727-222">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4d727-223">Syötä Nimi-kenttään Laskuttaja.</span><span class="sxs-lookup"><span data-stu-id="4d727-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="4d727-224">Laskuttaja</span><span class="sxs-lookup"><span data-stu-id="4d727-224">Creditor</span></span>  
23. <span data-ttu-id="4d727-225">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="4d727-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="4d727-226">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-226">Click Add.</span></span>
25. <span data-ttu-id="4d727-227">Kirjoita Kuvaus-kenttään "Osapuoli, jolle rahasumma on maksettava".</span><span class="sxs-lookup"><span data-stu-id="4d727-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="4d727-228">Osapuoli, jolle rahasumma on maksettava.</span><span class="sxs-lookup"><span data-stu-id="4d727-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="4d727-229">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="4d727-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="4d727-230">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="4d727-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="4d727-231">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="4d727-231">Party</span></span>  
28. <span data-ttu-id="4d727-232">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="4d727-232">Click Find next.</span></span>
29. <span data-ttu-id="4d727-233">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4d727-233">Click OK.</span></span>
30. <span data-ttu-id="4d727-234">Kirjoita Etsi-kenttään "Maksut".</span><span class="sxs-lookup"><span data-stu-id="4d727-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="4d727-235">Maksut</span><span class="sxs-lookup"><span data-stu-id="4d727-235">Payments</span></span>  
31. <span data-ttu-id="4d727-236">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="4d727-236">Click Find next.</span></span>
32. <span data-ttu-id="4d727-237">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="4d727-238">Syötä Nimi-kenttään Maksaja.</span><span class="sxs-lookup"><span data-stu-id="4d727-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="4d727-239">Maksaja</span><span class="sxs-lookup"><span data-stu-id="4d727-239">Debtor</span></span>  
34. <span data-ttu-id="4d727-240">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-240">Click Add.</span></span>
35. <span data-ttu-id="4d727-241">Kirjoita Kuvaus-kenttään "Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle".</span><span class="sxs-lookup"><span data-stu-id="4d727-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="4d727-242">Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle.</span><span class="sxs-lookup"><span data-stu-id="4d727-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="4d727-243">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="4d727-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="4d727-244">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="4d727-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="4d727-245">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="4d727-245">Party</span></span>  
38. <span data-ttu-id="4d727-246">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="4d727-246">Click Find next.</span></span>
39. <span data-ttu-id="4d727-247">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4d727-247">Click OK.</span></span>
40. <span data-ttu-id="4d727-248">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="4d727-248">Click Find next.</span></span>
41. <span data-ttu-id="4d727-249">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="4d727-250">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="4d727-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="4d727-251">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4d727-251">Description</span></span>  
43. <span data-ttu-id="4d727-252">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d727-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="4d727-253">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-253">Click Add.</span></span>
45. <span data-ttu-id="4d727-254">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="4d727-255">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="4d727-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="4d727-256">Valuutta</span><span class="sxs-lookup"><span data-stu-id="4d727-256">Currency</span></span>  
47. <span data-ttu-id="4d727-257">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-257">Click Add.</span></span>
48. <span data-ttu-id="4d727-258">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="4d727-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="4d727-259">Valuuttakoodi</span><span class="sxs-lookup"><span data-stu-id="4d727-259">Currency code</span></span>  
49. <span data-ttu-id="4d727-260">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="4d727-261">Syötä Nimi-kenttään TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="4d727-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="4d727-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="4d727-262">TransactionDate</span></span>  
51. <span data-ttu-id="4d727-263">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="4d727-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="4d727-264">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-264">Click Add.</span></span>
53. <span data-ttu-id="4d727-265">Kirjoita Kuvaus-kenttään "Tapahtumapäivä".</span><span class="sxs-lookup"><span data-stu-id="4d727-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="4d727-266">Tapahtuman päivämäärä</span><span class="sxs-lookup"><span data-stu-id="4d727-266">Transaction date</span></span>  
54. <span data-ttu-id="4d727-267">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="4d727-268">Syötä Nimi-kenttään InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="4d727-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="4d727-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="4d727-269">InstructedAmount</span></span>  
56. <span data-ttu-id="4d727-270">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="4d727-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="4d727-271">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-271">Click Add.</span></span>
58. <span data-ttu-id="4d727-272">Kirjoita Kuvaus-kenttään "Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="4d727-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="4d727-273">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="4d727-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="4d727-274">Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="4d727-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="4d727-275">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="4d727-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="4d727-276">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="4d727-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="4d727-277">Syötä Nimi-kenttään End2EndID.</span><span class="sxs-lookup"><span data-stu-id="4d727-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="4d727-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="4d727-278">End2EndID</span></span>  
61. <span data-ttu-id="4d727-279">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="4d727-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="4d727-280">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4d727-280">Click Add.</span></span>
63. <span data-ttu-id="4d727-281">Kirjoita Kuvaus-kenttään "Aloittavan osapuolen määrittämä yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="4d727-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="4d727-282">Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.</span><span class="sxs-lookup"><span data-stu-id="4d727-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="4d727-283">Aloittavan osapuolen määrittämä yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="4d727-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="4d727-284">Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.</span><span class="sxs-lookup"><span data-stu-id="4d727-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="4d727-285">Syötä Nimi-kenttään PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="4d727-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="4d727-286">PaymentModel-nimi on linjassa maksulomakkeiden ennalta määritettyjen käyttöliittymien kanssa.</span><span class="sxs-lookup"><span data-stu-id="4d727-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="4d727-287">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4d727-287">Click Save.</span></span>
66. <span data-ttu-id="4d727-288">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4d727-288">Close the page.</span></span>

