---
title: Määritä määrityksistä poikkeamisen hallinnan edellytykset
description: Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "337667"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="b90df-103">Määritä määrityksistä poikkeamisen hallinnan edellytykset</span><span class="sxs-lookup"><span data-stu-id="b90df-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b90df-104">Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit.</span><span class="sxs-lookup"><span data-stu-id="b90df-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="b90df-105">Määrityksistä poikkeaminen tarkoittaa menettelyä tai nimikettä, jolla on laatuongelma, jossa kuvaavat tiedot sisältävät ongelman lähteen ja tyypin.</span><span class="sxs-lookup"><span data-stu-id="b90df-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="b90df-106">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b90df-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="b90df-107">Tämän menettelyn suorittaa yleensä laatupäällikkö.</span><span class="sxs-lookup"><span data-stu-id="b90df-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="b90df-108">Ota laadunvalvontaprosessit käyttöön yrityksessä</span><span class="sxs-lookup"><span data-stu-id="b90df-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="b90df-109">Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="b90df-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="b90df-110">Valitse Laadunhallinta-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b90df-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="b90df-111">Valitse Käytä laadunhallintaa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b90df-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="b90df-112">Valitse tämä parametri ottaaksesi käyttöön yrityksen laadunhallintaprosessit.</span><span class="sxs-lookup"><span data-stu-id="b90df-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="b90df-113">Syötä Tuntihinta-kenttään haluamasi luku.</span><span class="sxs-lookup"><span data-stu-id="b90df-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="b90df-114">Syötä työn hinta paikallisena valuuttana Tuntihinta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="b90df-115">Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan.</span><span class="sxs-lookup"><span data-stu-id="b90df-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="b90df-116">Tuntihinta ja lasketut kustannukset ovat poikkeaman viitetietoja, eivätkä ne vaikuta muihin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="b90df-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="b90df-117">Valitse Raportin asetukset.</span><span class="sxs-lookup"><span data-stu-id="b90df-117">Click Report setup.</span></span>
    * <span data-ttu-id="b90df-118">Tällä sivulla voit määrittää erityyppisissä laadunhallintaraporteissa käytettävät laaturaporttien huomautustyypit.</span><span class="sxs-lookup"><span data-stu-id="b90df-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="b90df-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-119">Close the page.</span></span>
7. <span data-ttu-id="b90df-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="b90df-121">Salli käyttäjälle määrityksistä poikkeamisen käsittely</span><span class="sxs-lookup"><span data-stu-id="b90df-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-122">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="b90df-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="b90df-123">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="b90df-124">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="b90df-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="b90df-125">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="b90df-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b90df-126">Voit esimerkiksi suodattaa Nimi-kenttää arvolla "Riku".</span><span class="sxs-lookup"><span data-stu-id="b90df-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="b90df-127">Paikanna määrityksistä poikkeamiset hyväksyvä tai hylkäävä käyttäjä suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="b90df-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="b90df-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b90df-129">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="b90df-130">Napsauta Käyttäjän asetukset.</span><span class="sxs-lookup"><span data-stu-id="b90df-130">Click User options.</span></span>
5. <span data-ttu-id="b90df-131">Napsauta Asetukset-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="b90df-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="b90df-132">Valitse Ota tiedoston käsittely käyttöön -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="b90df-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="b90df-133">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="b90df-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="b90df-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-134">Close the page.</span></span>
8. <span data-ttu-id="b90df-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-135">Close the page.</span></span>
9. <span data-ttu-id="b90df-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="b90df-137">Määritä määrityksistä poikkeamisen käsittelyn diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="b90df-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-138">Valitse Varastonhallinta > Asetukset > Laadunhallintaa > Diagnostiikan tyypit.</span><span class="sxs-lookup"><span data-stu-id="b90df-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="b90df-139">Määritä vianmääritystoimenpiteiden luokitus Vianmääritystyypit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="b90df-140">Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen, sen tekijän sekä halutun ja suunnitellun valmistumispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="b90df-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="b90df-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-141">Click New.</span></span>
3. <span data-ttu-id="b90df-142">Kirjoita arvo Diagnostiikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="b90df-143">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b90df-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="b90df-145">Määritä määrityksistä poikkeamisen käsittelyn laadun kulut</span><span class="sxs-lookup"><span data-stu-id="b90df-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-146">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Laadun kulut.</span><span class="sxs-lookup"><span data-stu-id="b90df-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="b90df-147">Määritä määrityksistä poikkeamiseen liittyvien toimintojen kulujen luokittelu Laadun kulut -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="b90df-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-148">Click New.</span></span>
3. <span data-ttu-id="b90df-149">Kirjoita Kulujen koodi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b90df-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="b90df-150">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b90df-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="b90df-152">Määritä määrityksistä poikkeamisen käsittelyn toiminnot</span><span class="sxs-lookup"><span data-stu-id="b90df-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-153">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="b90df-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="b90df-154">Määritä Toiminnot-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="b90df-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="b90df-155">Kun liität poikkeamaan toiminnon, voit määrittää tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista.</span><span class="sxs-lookup"><span data-stu-id="b90df-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="b90df-156">Näitä tietoja käytetään perustana laskettaessa toiminnon arvioituja kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="b90df-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="b90df-157">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-157">Click New.</span></span>
3. <span data-ttu-id="b90df-158">Kirjoita arvo Toiminto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="b90df-159">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b90df-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="b90df-161">Määritä määrityksistä poikkeamisen käsittelyn ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="b90df-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-162">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Ongelmatyypit.</span><span class="sxs-lookup"><span data-stu-id="b90df-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="b90df-163">Määritä Ongelmatyypit-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä.</span><span class="sxs-lookup"><span data-stu-id="b90df-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="b90df-164">Määrityksistä poikkeamisen tyypit ovat: Sisäinen, Asiakas, Toimittaja, Palvelupyyntö, Tuotanto ja Oheistuotteen tuotanto.</span><span class="sxs-lookup"><span data-stu-id="b90df-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="b90df-165">Yksittäisen ongelmatyypin voi liittää useampaan määrityksistä poikkeamisen tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="b90df-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="b90df-166">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-166">Click New.</span></span>
3. <span data-ttu-id="b90df-167">Kirjoita arvo Ongelman tyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="b90df-168">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b90df-169">Napsauta Määrityksistä poikkeamisen tyypit -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="b90df-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="b90df-170">Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi Määrityksistä poikkeamisen tyypit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b90df-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="b90df-171">Vikakoodia koskeva ongelmatyyppi voi esimerkiksi liittyä kaikkiin poikkeamatyyppeihin, kun taas asiakasvalituksia koskeva ongelmatyyppi voi liittyä vain asiakkaan ja huoltopyynnön poikkeamatyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="b90df-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="b90df-172">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-172">Click New.</span></span>
7. <span data-ttu-id="b90df-173">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b90df-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="b90df-174">Valitse Määrityksistä poikkeamisen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="b90df-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="b90df-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-175">Close the page.</span></span>
10. <span data-ttu-id="b90df-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="b90df-177">Määritä määrityksistä poikkeamisen käsittelyn karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="b90df-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="b90df-178">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Karanteenivyöhykkeet.</span><span class="sxs-lookup"><span data-stu-id="b90df-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="b90df-179">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b90df-179">Click New.</span></span>
3. <span data-ttu-id="b90df-180">Kirjoita Karanteenivyöhyke-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b90df-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="b90df-181">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b90df-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b90df-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b90df-182">Close the page.</span></span>

