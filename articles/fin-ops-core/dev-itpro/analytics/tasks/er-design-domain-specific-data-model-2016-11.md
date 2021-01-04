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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268f661079b80551b36ad2e1877615d878350051
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681946"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="e974c-103">ER Suunnittele toimialueen erityistietomalli</span><span class="sxs-lookup"><span data-stu-id="e974c-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e974c-104">Seuraavissa vaiheissa kerrotaan, miten järjestelmänvalvojan tai sähköisen raportoinnin kehittäjän roolin omaava käyttäjä voi luoda uuden sähköiselle raportoinnin (ER) konfiguraation lähteen, joka sisältää sähköisen maksun asiakirjojen tietomallin.</span><span class="sxs-lookup"><span data-stu-id="e974c-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e974c-105">Tietomallia käytetään myöhemmin tietolähteenä, kun maksuasiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="e974c-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="e974c-106">Tässä esimerkissä luodaan konfiguraatio malliyritykselle Litware, Inc. Nämä vaiheet voidaan suorittaa mille tahansa yritykselle, koska kaikki yritykset jakavat ER-konfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="e974c-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="e974c-107">Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet on suoritettava ennen näiden vaiheiden suorittamista.</span><span class="sxs-lookup"><span data-stu-id="e974c-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="e974c-108">Siirry kohtaan Organisaation hallinto > Työtilat > Sähköinen raportointi.</span><span class="sxs-lookup"><span data-stu-id="e974c-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="e974c-109">Valitse malliyrityksen Litware, Inc:n konfiguraation lähde.</span><span class="sxs-lookup"><span data-stu-id="e974c-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="e974c-110">Jos konfiguraation lähde ei ole näkyvissä, suorita ensin Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi -menettelyn vaiheet.</span><span class="sxs-lookup"><span data-stu-id="e974c-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="e974c-111">Valitse Raportointikonfiguraatiot.</span><span class="sxs-lookup"><span data-stu-id="e974c-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="e974c-112">Luodaan konfiguraatio, joka sisältää tietomallin sähköisen maksun asiakirjoja varten.</span><span class="sxs-lookup"><span data-stu-id="e974c-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="e974c-113">Tietomallia käytetään myöhemmin tietolähteenä, kun maksujen asiakirjojen muoto määritetään.</span><span class="sxs-lookup"><span data-stu-id="e974c-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="e974c-114">Uuden tietomallin konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="e974c-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="e974c-115">Avaa valintaikkuna napsauttamalla Luo konfigurointi.</span><span class="sxs-lookup"><span data-stu-id="e974c-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="e974c-116">Syötä Nimi-kenttään Maksut (yksinkertaistettu malli).</span><span class="sxs-lookup"><span data-stu-id="e974c-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="e974c-117">Syötä Kuvaus-kenttään Maksumallin konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="e974c-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="e974c-118">Aktiivinen konfiguraation lähde syötetään tässä automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e974c-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e974c-119">Tämä lähde voi ylläpitää tätä konfiguraatiota.</span><span class="sxs-lookup"><span data-stu-id="e974c-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e974c-120">Muut lähteet voivat käyttää tätä konfiguraatiota, mutta eivät ylläpitää sitä.</span><span class="sxs-lookup"><span data-stu-id="e974c-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="e974c-121">Suorita konfiguraation luontitehtävä valitsemalla Luo konfiguraatio</span><span class="sxs-lookup"><span data-stu-id="e974c-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="e974c-122">Tietomallin luominen</span><span class="sxs-lookup"><span data-stu-id="e974c-122">Create a data model</span></span>
<span data-ttu-id="e974c-123">Olet luomassa valitulle määritykselle uutta tietomallia.</span><span class="sxs-lookup"><span data-stu-id="e974c-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="e974c-124">Konfiguraation version tilaksi tulee Luonnos.</span><span class="sxs-lookup"><span data-stu-id="e974c-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="e974c-125">Valitse Suunnittelutoiminto.</span><span class="sxs-lookup"><span data-stu-id="e974c-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="e974c-126">Maksuprosessiin osallistuvan osapuolen rakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e974c-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="e974c-127">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e974c-128">Kirjoita Nimi-kenttään Osapuoli.</span><span class="sxs-lookup"><span data-stu-id="e974c-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="e974c-129">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-129">Click Add.</span></span>
4. <span data-ttu-id="e974c-130">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e974c-131">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="e974c-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="e974c-132">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e974c-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="e974c-133">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-133">Click Add.</span></span>
8. <span data-ttu-id="e974c-134">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="e974c-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="e974c-135">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="e974c-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="e974c-136">Pankkirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="e974c-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="e974c-137">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e974c-138">Syötä Nimi-kenttään Agentti.</span><span class="sxs-lookup"><span data-stu-id="e974c-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="e974c-139">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="e974c-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e974c-140">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-140">Click Add.</span></span>
5. <span data-ttu-id="e974c-141">Kirjoita Kuvaus-kenttään "Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä".</span><span class="sxs-lookup"><span data-stu-id="e974c-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="e974c-142">Rahoituslaitos (esimerkiksi pankki), joka hoitaa osapuolen (maksajan tai laskuttajan) tiliä.</span><span class="sxs-lookup"><span data-stu-id="e974c-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="e974c-143">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e974c-144">Syötä Nimi-kenttään Nimi.</span><span class="sxs-lookup"><span data-stu-id="e974c-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="e974c-145">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e974c-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e974c-146">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-146">Click Add.</span></span>
10. <span data-ttu-id="e974c-147">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="e974c-148">Syötä Nimi-kenttään SWIFT.</span><span class="sxs-lookup"><span data-stu-id="e974c-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="e974c-149">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-149">Click Add.</span></span>
13. <span data-ttu-id="e974c-150">Kirjoita Kuvaus-kenttään "BIC-koodi".</span><span class="sxs-lookup"><span data-stu-id="e974c-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="e974c-151">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e974c-152">Syötä Nimi-kenttään RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="e974c-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="e974c-153">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-153">Click Add.</span></span>
17. <span data-ttu-id="e974c-154">Kirjoita Kuvaus-kenttään "Pankkikoodi".</span><span class="sxs-lookup"><span data-stu-id="e974c-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="e974c-155">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="e974c-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="e974c-156">Pankkitilirakenteen määrittäminen tälle mallille</span><span class="sxs-lookup"><span data-stu-id="e974c-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="e974c-157">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e974c-158">Syötä Nimi-kenttään Tili.</span><span class="sxs-lookup"><span data-stu-id="e974c-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="e974c-159">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="e974c-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="e974c-160">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-160">Click Add.</span></span>
5. <span data-ttu-id="e974c-161">Kirjoita Kuvaus-kenttään "Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa)".</span><span class="sxs-lookup"><span data-stu-id="e974c-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="e974c-162">Osapuolen tilin tunnus rahoituslaitoksessa (kuten pankissa).</span><span class="sxs-lookup"><span data-stu-id="e974c-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="e974c-163">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="e974c-164">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="e974c-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="e974c-165">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e974c-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="e974c-166">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-166">Click Add.</span></span>
10. <span data-ttu-id="e974c-167">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="e974c-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="e974c-168">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e974c-169">Syötä Nimi-kenttään Numero.</span><span class="sxs-lookup"><span data-stu-id="e974c-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="e974c-170">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-170">Click Add.</span></span>
14. <span data-ttu-id="e974c-171">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="e974c-172">Syötä Nimi-kenttään IBAN.</span><span class="sxs-lookup"><span data-stu-id="e974c-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="e974c-173">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-173">Click Add.</span></span>
17. <span data-ttu-id="e974c-174">Kirjoita Kuvaus-kenttään "Kansainvälinen tilinumero (IBAN)".</span><span class="sxs-lookup"><span data-stu-id="e974c-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="e974c-175">Tilisiirtomaksun tyypin maksuviestirakenteen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e974c-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="e974c-176">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="e974c-177">Kirjoita Uusi solmu muodossa -kenttään "Mallin juuri".</span><span class="sxs-lookup"><span data-stu-id="e974c-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="e974c-178">Syötä Nimi-kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="e974c-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="e974c-179">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-179">Click Add.</span></span>
5. <span data-ttu-id="e974c-180">Kirjoita Etsi--kenttään CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="e974c-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="e974c-181">Valitse Etsi edellinen.</span><span class="sxs-lookup"><span data-stu-id="e974c-181">Click Find previous.</span></span>
7. <span data-ttu-id="e974c-182">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="e974c-183">Syötä Nimi-kenttään MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="e974c-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="e974c-184">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-184">Click Add.</span></span>
10. <span data-ttu-id="e974c-185">Kirjoita Kuvaus-kenttään "Osoitetaan pisteviitteeseen ohjaavan osapuolen määrityksen mukaisesti (ja lähetetään seuraavalle osapuolelle) viestin tunnistamista varten".</span><span class="sxs-lookup"><span data-stu-id="e974c-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="e974c-186">Pisteestä pisteeseen -viite, jonka ohjaava osapuoli on määrittänyt (ja lähettänyt seuraavalle osapuolelle) viestin tunnistamista varten.</span><span class="sxs-lookup"><span data-stu-id="e974c-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="e974c-187">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="e974c-188">Syötä Nimi-kenttään ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="e974c-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="e974c-189">Valitse Nimiketyyppi-kentässä DateTime.</span><span class="sxs-lookup"><span data-stu-id="e974c-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="e974c-190">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-190">Click Add.</span></span>
15. <span data-ttu-id="e974c-191">Kirjoita Kuvaus-kenttään "Päivämäärä ja kellonaika, jolloin maksun viesti luotiin".</span><span class="sxs-lookup"><span data-stu-id="e974c-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="e974c-192">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="e974c-193">Pankkitapahtumarakenteen määrittäminen tälle mallille.</span><span class="sxs-lookup"><span data-stu-id="e974c-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="e974c-194">Syötä Nimi-kenttään Maksut.</span><span class="sxs-lookup"><span data-stu-id="e974c-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="e974c-195">Valitse Nimiketyyppi-kentässä Tietueluettelo.</span><span class="sxs-lookup"><span data-stu-id="e974c-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="e974c-196">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-196">Click Add.</span></span>
20. <span data-ttu-id="e974c-197">Syötä Kuvaus-kenttään Nykyisen viestin maksurivi.</span><span class="sxs-lookup"><span data-stu-id="e974c-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="e974c-198">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e974c-199">Syötä Nimi-kenttään Laskuttaja.</span><span class="sxs-lookup"><span data-stu-id="e974c-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="e974c-200">Valitse Nimiketyyppi-kentässä Tietue.</span><span class="sxs-lookup"><span data-stu-id="e974c-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="e974c-201">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-201">Click Add.</span></span>
25. <span data-ttu-id="e974c-202">Kirjoita Kuvaus-kenttään "Osapuoli, jolle rahasumma on maksettava".</span><span class="sxs-lookup"><span data-stu-id="e974c-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="e974c-203">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="e974c-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="e974c-204">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="e974c-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="e974c-205">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="e974c-205">Click Find next.</span></span>
29. <span data-ttu-id="e974c-206">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e974c-206">Click OK.</span></span>
30. <span data-ttu-id="e974c-207">Kirjoita Etsi-kenttään "Maksut".</span><span class="sxs-lookup"><span data-stu-id="e974c-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="e974c-208">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="e974c-208">Click Find next.</span></span>
32. <span data-ttu-id="e974c-209">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="e974c-210">Syötä Nimi-kenttään Maksaja.</span><span class="sxs-lookup"><span data-stu-id="e974c-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="e974c-211">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-211">Click Add.</span></span>
35. <span data-ttu-id="e974c-212">Kirjoita Kuvaus-kenttään "Osapuoli, joka on rahasumman velkaa (lopulliselle) laskuttajalle".</span><span class="sxs-lookup"><span data-stu-id="e974c-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="e974c-213">Valitse Muuta nimikkeen viitettä.</span><span class="sxs-lookup"><span data-stu-id="e974c-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="e974c-214">Kirjoita Etsi-kenttään "Osapuoli".</span><span class="sxs-lookup"><span data-stu-id="e974c-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="e974c-215">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="e974c-215">Click Find next.</span></span>
39. <span data-ttu-id="e974c-216">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e974c-216">Click OK.</span></span>
40. <span data-ttu-id="e974c-217">Valitse Etsi seuraava.</span><span class="sxs-lookup"><span data-stu-id="e974c-217">Click Find next.</span></span>
41. <span data-ttu-id="e974c-218">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="e974c-219">Syötä Nimi-kenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e974c-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="e974c-220">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e974c-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="e974c-221">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-221">Click Add.</span></span>
45. <span data-ttu-id="e974c-222">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="e974c-223">Syötä Nimi-kenttään Valuutta.</span><span class="sxs-lookup"><span data-stu-id="e974c-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="e974c-224">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-224">Click Add.</span></span>
48. <span data-ttu-id="e974c-225">Kirjoita Kuvaus-kenttään "Valuuttakoodi".</span><span class="sxs-lookup"><span data-stu-id="e974c-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="e974c-226">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="e974c-227">Syötä Nimi-kenttään TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="e974c-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="e974c-228">Valitse Nimiketyyppi-kentässä Päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="e974c-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="e974c-229">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-229">Click Add.</span></span>
53. <span data-ttu-id="e974c-230">Kirjoita Kuvaus-kenttään "Tapahtumapäivä".</span><span class="sxs-lookup"><span data-stu-id="e974c-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="e974c-231">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="e974c-232">Syötä Nimi-kenttään InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="e974c-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="e974c-233">Valitse Nimiketyyppi-kentässä Reaaliluku.</span><span class="sxs-lookup"><span data-stu-id="e974c-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="e974c-234">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-234">Click Add.</span></span>
58. <span data-ttu-id="e974c-235">Kirjoita Kuvaus-kenttään "Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="e974c-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e974c-236">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="e974c-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="e974c-237">Maksajan ja laskuttajan välillä siirrettävä rahasumma ennen maksupidätyksiä.</span><span class="sxs-lookup"><span data-stu-id="e974c-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="e974c-238">Summa ilmaistaan aloittavan osapuolen määrittämänä valuuttana.</span><span class="sxs-lookup"><span data-stu-id="e974c-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="e974c-239">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="e974c-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="e974c-240">Syötä Nimi-kenttään End2EndID.</span><span class="sxs-lookup"><span data-stu-id="e974c-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="e974c-241">Valitse Nimiketyyppi-kentässä Merkkijono.</span><span class="sxs-lookup"><span data-stu-id="e974c-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="e974c-242">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="e974c-242">Click Add.</span></span>
63. <span data-ttu-id="e974c-243">Kirjoita Kuvaus-kenttään "Aloittavan osapuolen määrittämä yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="e974c-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="e974c-244">Tunnus välitetään muuttumattomana koko päästä päähän -ketjun läpi.</span><span class="sxs-lookup"><span data-stu-id="e974c-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="e974c-245">Syötä Nimi-kenttään PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="e974c-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="e974c-246">PaymentModel-nimi on linjassa maksulomakkeiden ennalta määritettyjen käyttöliittymien kanssa.</span><span class="sxs-lookup"><span data-stu-id="e974c-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="e974c-247">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="e974c-247">Click Save.</span></span>
66. <span data-ttu-id="e974c-248">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="e974c-248">Close the page.</span></span>

