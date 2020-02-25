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
ms.openlocfilehash: 3fe08b30977b8515ffd8d0acc1fd8f4b3085de93
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026083"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="312df-103">ER Suunnittele toimialueen erityistietomalli</span><span class="sxs-lookup"><span data-stu-id="312df-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="312df-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin.</span><span class="sxs-lookup"><span data-stu-id="312df-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="312df-105">Tietomallia käytetään myöhemmin tietolähteenä, kun maksuasiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="312df-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="312df-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="312df-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="312df-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="312df-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="312df-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="312df-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="312df-109">Valitse malliyrityksen Litware, Inc:n konfiguraation lähde.</span><span class="sxs-lookup"><span data-stu-id="312df-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="312df-110">Jos lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="312df-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="312df-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="312df-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="312df-112">Luodaan konfiguraatio, joka sisältää tietomallin sähköisen maksun asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="312df-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="312df-113">Tietomallia käytetään myöhemmin tietolähteenä, kun maksujen asiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="312df-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="312df-114">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="312df-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="312df-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="312df-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="312df-116">Syötä Nimi-kenttään Maksut (yksinkertaistettu malli).</span><span class="sxs-lookup"><span data-stu-id="312df-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="312df-117">Maksut (yksinkertaistettu malli)</span><span class="sxs-lookup"><span data-stu-id="312df-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="312df-118">Syötä Kuvaus-kenttään Maksumallin konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="312df-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="312df-119">Maksumallin konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="312df-119">Payment model configuration</span></span>  
    * <span data-ttu-id="312df-120">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="312df-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="312df-121">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="312df-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="312df-122">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="312df-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="312df-123">Suorita konfiguraation luontitehtävä valitsemalla Luo konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="312df-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="312df-124">Tietomallin luominen</span><span class="sxs-lookup"><span data-stu-id="312df-124">Create a data model</span></span>
<span data-ttu-id="312df-125">Olet luomassa valitulle määritykselle uutta tietomallia.</span><span class="sxs-lookup"><span data-stu-id="312df-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="312df-126">Konfiguraation version tilaksi tulee Luonnos.</span><span class="sxs-lookup"><span data-stu-id="312df-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="312df-127">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="312df-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="312df-128">Maksuprosessiin osallistuvan osapuolen rakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="312df-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="312df-129">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="312df-130">Kirjoita Nimi-kenttään Osapuoli.</span><span class="sxs-lookup"><span data-stu-id="312df-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="312df-131">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="312df-131">Party</span></span>  
3. <span data-ttu-id="312df-132">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-132">Click Add.</span></span>
4. <span data-ttu-id="312df-133">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="312df-134">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="312df-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="312df-135">Nimi</span><span class="sxs-lookup"><span data-stu-id="312df-135">Name</span></span>  
6. <span data-ttu-id="312df-136">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="312df-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="312df-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-137">Click Add.</span></span>
8. <span data-ttu-id="312df-138">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="312df-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="312df-139">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="312df-139">Party</span></span>  
9. <span data-ttu-id="312df-140">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="312df-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="312df-141">Pankkirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="312df-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="312df-142">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="312df-143">Syötä Nimi-kenttään Agentti.</span><span class="sxs-lookup"><span data-stu-id="312df-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="312df-144">Edustaja</span><span class="sxs-lookup"><span data-stu-id="312df-144">Agent</span></span>  
3. <span data-ttu-id="312df-145">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="312df-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="312df-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-146">Click Add.</span></span>
5. <span data-ttu-id="312df-147">Kirjoita Kuvaus-kenttään "Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä".</span><span class="sxs-lookup"><span data-stu-id="312df-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="312df-148">Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä.</span><span class="sxs-lookup"><span data-stu-id="312df-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="312df-149">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="312df-150">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="312df-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="312df-151">Nimi</span><span class="sxs-lookup"><span data-stu-id="312df-151">Name</span></span>  
8. <span data-ttu-id="312df-152">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="312df-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="312df-153">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-153">Click Add.</span></span>
10. <span data-ttu-id="312df-154">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="312df-155">Syötä Nimi-kenttään SWIFT.</span><span class="sxs-lookup"><span data-stu-id="312df-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="312df-156">SWIFT-koodi</span><span class="sxs-lookup"><span data-stu-id="312df-156">SWIFT</span></span>  
12. <span data-ttu-id="312df-157">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-157">Click Add.</span></span>
13. <span data-ttu-id="312df-158">Kirjoita Kuvaus-kenttään "BIC-koodi".</span><span class="sxs-lookup"><span data-stu-id="312df-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="312df-159">BIC-koodi</span><span class="sxs-lookup"><span data-stu-id="312df-159">Bank identification code</span></span>  
14. <span data-ttu-id="312df-160">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="312df-161">Syötä Nimi-kenttään RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="312df-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="312df-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="312df-162">RoutingNumber</span></span>  
16. <span data-ttu-id="312df-163">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-163">Click Add.</span></span>
17. <span data-ttu-id="312df-164">Kirjoita Kuvaus-kenttään "Pankkikoodi".</span><span class="sxs-lookup"><span data-stu-id="312df-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="312df-165">Pankkikoodi</span><span class="sxs-lookup"><span data-stu-id="312df-165">Routing number</span></span>  
18. <span data-ttu-id="312df-166">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="312df-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="312df-167">Pankkitilirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="312df-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="312df-168">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="312df-169">Syötä Nimi-kenttään Tili.</span><span class="sxs-lookup"><span data-stu-id="312df-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="312df-170">Tili</span><span class="sxs-lookup"><span data-stu-id="312df-170">Account</span></span>  
3. <span data-ttu-id="312df-171">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="312df-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="312df-172">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-172">Click Add.</span></span>
5. <span data-ttu-id="312df-173">Kirjoita Kuvaus-kenttään "Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa)".</span><span class="sxs-lookup"><span data-stu-id="312df-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="312df-174">Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa).</span><span class="sxs-lookup"><span data-stu-id="312df-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="312df-175">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="312df-176">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="312df-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="312df-177">Valuutta</span><span class="sxs-lookup"><span data-stu-id="312df-177">Currency</span></span>  
8. <span data-ttu-id="312df-178">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="312df-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="312df-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-179">Click Add.</span></span>
10. <span data-ttu-id="312df-180">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="312df-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="312df-181">Valuuttakoodi</span><span class="sxs-lookup"><span data-stu-id="312df-181">Currency code</span></span>  
11. <span data-ttu-id="312df-182">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="312df-183">Syötä Nimi-kenttään Numero.</span><span class="sxs-lookup"><span data-stu-id="312df-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="312df-184">Numero</span><span class="sxs-lookup"><span data-stu-id="312df-184">Number</span></span>  
13. <span data-ttu-id="312df-185">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-185">Click Add.</span></span>
14. <span data-ttu-id="312df-186">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="312df-187">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="312df-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="312df-188">IBAN-tilinumero</span><span class="sxs-lookup"><span data-stu-id="312df-188">IBAN</span></span>  
16. <span data-ttu-id="312df-189">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-189">Click Add.</span></span>
17. <span data-ttu-id="312df-190">Kirjoita Kuvaus-kenttään "Kansainvälinen tilinumero (IBAN)".</span><span class="sxs-lookup"><span data-stu-id="312df-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="312df-191">Kansainvälinen tilinumero (IBAN)</span><span class="sxs-lookup"><span data-stu-id="312df-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="312df-192">Tilisiirtomaksun tyypin maksuviestirakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="312df-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="312df-193">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="312df-194">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="312df-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="312df-195">Syötä Nimi-kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="312df-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="312df-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="312df-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="312df-197">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-197">Click Add.</span></span>
5. <span data-ttu-id="312df-198">Kirjoita Etsi--kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="312df-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="312df-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="312df-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="312df-200">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="312df-200">Click Find previous.</span></span>
7. <span data-ttu-id="312df-201">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="312df-202">Syötä Nimi-kenttään MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="312df-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="312df-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="312df-203">MessageIdentification</span></span>  
9. <span data-ttu-id="312df-204">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-204">Click Add.</span></span>
10. <span data-ttu-id="312df-205">Kirjoita Kuvaus-kenttään "Osoitetaan pisteviitteeseen ohjaavan osapuolen määrityksen mukaisesti (ja lähetetään seuraavalle osapuolelle) viestin tunnistamista varten".</span><span class="sxs-lookup"><span data-stu-id="312df-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="312df-206">Pisteestä pisteeseen -viite, jonka ohjaava osapuoli on määrittänyt (ja lähettänyt seuraavalle osapuolelle) viestin tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="312df-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="312df-207">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="312df-208">Syötä Nimi-kenttään ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="312df-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="312df-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="312df-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="312df-210">Valitse Nimiketyyppi-kentässä DateTime.</span><span class="sxs-lookup"><span data-stu-id="312df-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="312df-211">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-211">Click Add.</span></span>
15. <span data-ttu-id="312df-212">Kirjoita Kuvaus-kenttään "Päivämäärä ja kellonaika, jolloin maksun viesti luotiin".</span><span class="sxs-lookup"><span data-stu-id="312df-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="312df-213">Päivämäärä ja kellonaika, jolloin maksun viesti luotiin.</span><span class="sxs-lookup"><span data-stu-id="312df-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="312df-214">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="312df-215">Pankkitapahtumarakenteen määrittäminen tälle mallille.</span><span class="sxs-lookup"><span data-stu-id="312df-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="312df-216">Syötä Nimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="312df-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="312df-217">Maksut</span><span class="sxs-lookup"><span data-stu-id="312df-217">Payments</span></span>  
18. <span data-ttu-id="312df-218">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="312df-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="312df-219">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-219">Click Add.</span></span>
20. <span data-ttu-id="312df-220">Syötä Kuvaus-kenttään Nykyisen viestin maksurivi.</span><span class="sxs-lookup"><span data-stu-id="312df-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="312df-221">Nykyisen viestin maksurivit</span><span class="sxs-lookup"><span data-stu-id="312df-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="312df-222">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="312df-223">Syötä Nimi-kenttään Laskuttaja.</span><span class="sxs-lookup"><span data-stu-id="312df-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="312df-224">Laskuttaja</span><span class="sxs-lookup"><span data-stu-id="312df-224">Creditor</span></span>  
23. <span data-ttu-id="312df-225">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="312df-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="312df-226">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-226">Click Add.</span></span>
25. <span data-ttu-id="312df-227">Kirjoita Kuvaus-kenttään "Osapuoli, jolle rahasumma on maksettava".</span><span class="sxs-lookup"><span data-stu-id="312df-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="312df-228">Osapuoli, jolle rahasumma on maksettava.</span><span class="sxs-lookup"><span data-stu-id="312df-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="312df-229">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="312df-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="312df-230">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="312df-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="312df-231">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="312df-231">Party</span></span>  
28. <span data-ttu-id="312df-232">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="312df-232">Click Find next.</span></span>
29. <span data-ttu-id="312df-233">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="312df-233">Click OK.</span></span>
30. <span data-ttu-id="312df-234">Kirjoita Etsi-kenttään "Maksut".</span><span class="sxs-lookup"><span data-stu-id="312df-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="312df-235">Maksut</span><span class="sxs-lookup"><span data-stu-id="312df-235">Payments</span></span>  
31. <span data-ttu-id="312df-236">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="312df-236">Click Find next.</span></span>
32. <span data-ttu-id="312df-237">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="312df-238">Syötä Nimi-kenttään Maksaja.</span><span class="sxs-lookup"><span data-stu-id="312df-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="312df-239">Maksaja</span><span class="sxs-lookup"><span data-stu-id="312df-239">Debtor</span></span>  
34. <span data-ttu-id="312df-240">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-240">Click Add.</span></span>
35. <span data-ttu-id="312df-241">Kirjoita Kuvaus-kenttään "Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle".</span><span class="sxs-lookup"><span data-stu-id="312df-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="312df-242">Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle.</span><span class="sxs-lookup"><span data-stu-id="312df-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="312df-243">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="312df-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="312df-244">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="312df-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="312df-245">Osapuoli</span><span class="sxs-lookup"><span data-stu-id="312df-245">Party</span></span>  
38. <span data-ttu-id="312df-246">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="312df-246">Click Find next.</span></span>
39. <span data-ttu-id="312df-247">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="312df-247">Click OK.</span></span>
40. <span data-ttu-id="312df-248">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="312df-248">Click Find next.</span></span>
41. <span data-ttu-id="312df-249">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="312df-250">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="312df-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="312df-251">kuvaus</span><span class="sxs-lookup"><span data-stu-id="312df-251">Description</span></span>  
43. <span data-ttu-id="312df-252">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="312df-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="312df-253">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-253">Click Add.</span></span>
45. <span data-ttu-id="312df-254">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="312df-255">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="312df-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="312df-256">Valuutta</span><span class="sxs-lookup"><span data-stu-id="312df-256">Currency</span></span>  
47. <span data-ttu-id="312df-257">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-257">Click Add.</span></span>
48. <span data-ttu-id="312df-258">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="312df-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="312df-259">Valuuttakoodi</span><span class="sxs-lookup"><span data-stu-id="312df-259">Currency code</span></span>  
49. <span data-ttu-id="312df-260">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="312df-261">Syötä Nimi-kenttään TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="312df-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="312df-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="312df-262">TransactionDate</span></span>  
51. <span data-ttu-id="312df-263">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="312df-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="312df-264">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-264">Click Add.</span></span>
53. <span data-ttu-id="312df-265">Kirjoita Kuvaus-kenttään "Tapahtumapäivä".</span><span class="sxs-lookup"><span data-stu-id="312df-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="312df-266">Tapahtuman päivämäärä</span><span class="sxs-lookup"><span data-stu-id="312df-266">Transaction date</span></span>  
54. <span data-ttu-id="312df-267">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="312df-268">Syötä Nimi-kenttään InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="312df-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="312df-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="312df-269">InstructedAmount</span></span>  
56. <span data-ttu-id="312df-270">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="312df-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="312df-271">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-271">Click Add.</span></span>
58. <span data-ttu-id="312df-272">Kirjoita Kuvaus-kenttään "Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="312df-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="312df-273">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="312df-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="312df-274">Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="312df-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="312df-275">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="312df-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="312df-276">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="312df-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="312df-277">Syötä Nimi-kenttään End2EndID.</span><span class="sxs-lookup"><span data-stu-id="312df-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="312df-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="312df-278">End2EndID</span></span>  
61. <span data-ttu-id="312df-279">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="312df-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="312df-280">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="312df-280">Click Add.</span></span>
63. <span data-ttu-id="312df-281">Kirjoita Kuvaus-kenttään "Aloittavan osapuolen määrittämä yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="312df-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="312df-282">Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.</span><span class="sxs-lookup"><span data-stu-id="312df-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="312df-283">Aloittavan osapuolen määrittämä yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="312df-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="312df-284">Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.</span><span class="sxs-lookup"><span data-stu-id="312df-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="312df-285">Syötä Nimi-kenttään PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="312df-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="312df-286">PaymentModel-nimi on linjassa maksulomakkeiden ennalta määritettyjen käyttöliittymien kanssa.</span><span class="sxs-lookup"><span data-stu-id="312df-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="312df-287">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="312df-287">Click Save.</span></span>
66. <span data-ttu-id="312df-288">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="312df-288">Close the page.</span></span>

