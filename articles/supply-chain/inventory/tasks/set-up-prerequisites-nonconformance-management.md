---
title: "Määritä hallinnan esivaatimukset"
description: "Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 842a9441158defca74d1b203a1b2509773ba8919
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="82ff9-103">Määritä hallinnan esivaatimukset</span><span class="sxs-lookup"><span data-stu-id="82ff9-103">Set up prerequisites for management</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82ff9-104">Näitä toimintaohjeita noudattamalla voit ottaa käyttöön määrityksistä poikkeamisen hallintaprosessit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="82ff9-105">Määrityksistä poikkeaminen tarkoittaa menettelyä tai nimikettä, jolla on laatuongelma, jossa kuvaavat tiedot sisältävät ongelman lähteen ja tyypin.</span><span class="sxs-lookup"><span data-stu-id="82ff9-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="82ff9-106">Menettely käyttää USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="82ff9-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="82ff9-107">Tämän menettelyn suorittaa yleensä laatupäällikkö.</span><span class="sxs-lookup"><span data-stu-id="82ff9-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="82ff9-108">Ota laadunvalvontaprosessit käyttöön yrityksessä</span><span class="sxs-lookup"><span data-stu-id="82ff9-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="82ff9-109">Siirry kohtaan Varastonhallinta > Asetukset > Varasto ja varastonhallinnan parametrit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="82ff9-110">Valitse Laadunhallinta-välilehti.</span><span class="sxs-lookup"><span data-stu-id="82ff9-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="82ff9-111">Valitse Käytä laadunhallintaa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="82ff9-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="82ff9-112">Valitse tämä parametri ottaaksesi käyttöön yrityksen laadunhallintaprosessit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="82ff9-113">Syötä Tuntihinta-kenttään haluamasi luku.</span><span class="sxs-lookup"><span data-stu-id="82ff9-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="82ff9-114">Syötä työn hinta paikallisena valuuttana Tuntihinta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="82ff9-115">Tuntihintaa käytetään määrityksistä poikkeavien toimintojen kustannusten laskentaan.</span><span class="sxs-lookup"><span data-stu-id="82ff9-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="82ff9-116">Tuntihinta ja lasketut kustannukset ovat poikkeaman viitetietoja, eivätkä ne vaikuta muihin toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="82ff9-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="82ff9-117">Valitse Raportin asetukset.</span><span class="sxs-lookup"><span data-stu-id="82ff9-117">Click Report setup.</span></span>
    * <span data-ttu-id="82ff9-118">Tällä sivulla voit määrittää erityyppisissä laadunhallintaraporteissa käytettävät laaturaporttien huomautustyypit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="82ff9-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-119">Close the page.</span></span>
7. <span data-ttu-id="82ff9-120">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="82ff9-121">Salli käyttäjälle määrityksistä poikkeamisen käsittely</span><span class="sxs-lookup"><span data-stu-id="82ff9-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-122">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="82ff9-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="82ff9-123">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="82ff9-124">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="82ff9-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="82ff9-125">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="82ff9-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="82ff9-126">Voit esimerkiksi suodattaa Nimi-kenttää arvolla "Riku".</span><span class="sxs-lookup"><span data-stu-id="82ff9-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="82ff9-127">Paikanna määrityksistä poikkeamiset hyväksyvä tai hylkäävä käyttäjä suodattimen avulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="82ff9-128">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="82ff9-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="82ff9-129">Määrityksistä poikkeamisen hyväksymisen käsittely edellyttää, että määrityksistä poikkeamisten hyväksynnän tai hylkäyksen suorittajalle on määritetty Nimi-arvo Käyttäjät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="82ff9-130">Napsauta Käyttäjän asetukset.</span><span class="sxs-lookup"><span data-stu-id="82ff9-130">Click User options.</span></span>
5. <span data-ttu-id="82ff9-131">Napsauta Asetukset-välilehteä.</span><span class="sxs-lookup"><span data-stu-id="82ff9-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="82ff9-132">Valitse Ota tiedoston käsittely käyttöön -kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="82ff9-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="82ff9-133">Asiakirjojen huomautusten käyttö taas edellyttää, että tiedoston käsittely on aktivoitu käyttäjäasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="82ff9-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="82ff9-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-134">Close the page.</span></span>
8. <span data-ttu-id="82ff9-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-135">Close the page.</span></span>
9. <span data-ttu-id="82ff9-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="82ff9-137">Määritä määrityksistä poikkeamisen käsittelyn diagnostiikkatyypit</span><span class="sxs-lookup"><span data-stu-id="82ff9-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-138">Valitse Varastonhallinta > Asetukset > Laadunhallintaa > Diagnostiikan tyypit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="82ff9-139">Määritä vianmääritystoimenpiteiden luokitus Vianmääritystyypit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="82ff9-140">Korjaus ilmaisee hyväksytyn poikkeaman vianmääritystoimenpiteen, sen tekijän sekä halutun ja suunnitellun valmistumispäivämäärän.</span><span class="sxs-lookup"><span data-stu-id="82ff9-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="82ff9-141">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-141">Click New.</span></span>
3. <span data-ttu-id="82ff9-142">Kirjoita arvo Diagnostiikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="82ff9-143">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ff9-144">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="82ff9-145">Määritä määrityksistä poikkeamisen käsittelyn laadun kulut</span><span class="sxs-lookup"><span data-stu-id="82ff9-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-146">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Laadun kulut.</span><span class="sxs-lookup"><span data-stu-id="82ff9-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="82ff9-147">Määritä määrityksistä poikkeamiseen liittyvien toimintojen kulujen luokittelu Laadun kulut -sivulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="82ff9-148">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-148">Click New.</span></span>
3. <span data-ttu-id="82ff9-149">Kirjoita Kulujen koodi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="82ff9-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="82ff9-150">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ff9-151">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="82ff9-152">Määritä määrityksistä poikkeamisen käsittelyn toiminnot</span><span class="sxs-lookup"><span data-stu-id="82ff9-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-153">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="82ff9-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="82ff9-154">Määritä Toiminnot-sivulla avulla luokitus hyväksytyn määrityksistä poikkeamisen käsittelyä varten.</span><span class="sxs-lookup"><span data-stu-id="82ff9-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="82ff9-155">Kun liität poikkeamaan toiminnon, voit määrittää tietoja liittyvästä materiaalista, työtunneista ja erilaisista toiminnon tekemiseen tarvittavista kuluista.</span><span class="sxs-lookup"><span data-stu-id="82ff9-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="82ff9-156">Näitä tietoja käytetään perustana laskettaessa toiminnon arvioituja kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="82ff9-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="82ff9-157">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-157">Click New.</span></span>
3. <span data-ttu-id="82ff9-158">Kirjoita arvo Toiminto-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="82ff9-159">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ff9-160">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="82ff9-161">Määritä määrityksistä poikkeamisen käsittelyn ongelmatyypit</span><span class="sxs-lookup"><span data-stu-id="82ff9-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-162">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Ongelmatyypit.</span><span class="sxs-lookup"><span data-stu-id="82ff9-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="82ff9-163">Määritä Ongelmatyypit-sivulla luokitus laatuongelmille, joita kohdataan erityyppisissä määrityksistä poikkeamisen tyypeissä.</span><span class="sxs-lookup"><span data-stu-id="82ff9-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="82ff9-164">Määrityksistä poikkeamisen tyypit ovat: Sisäinen, Asiakas, Toimittaja, Palvelupyyntö, Tuotanto ja Oheistuotteen tuotanto.</span><span class="sxs-lookup"><span data-stu-id="82ff9-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="82ff9-165">Yksittäisen ongelmatyypin voi liittää useampaan määrityksistä poikkeamisen tyyppiin.</span><span class="sxs-lookup"><span data-stu-id="82ff9-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="82ff9-166">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-166">Click New.</span></span>
3. <span data-ttu-id="82ff9-167">Kirjoita arvo Ongelman tyyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="82ff9-168">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ff9-169">Napsauta Määrityksistä poikkeamisen tyypit -kohtaa.</span><span class="sxs-lookup"><span data-stu-id="82ff9-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="82ff9-170">Hyväksy yhdessä tai useassa määrityksistä poikkeamisen tyypissä käytettävä ongelmatyyppi Määrityksistä poikkeamisen tyypit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="82ff9-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="82ff9-171">Vikakoodia koskeva ongelmatyyppi voi esimerkiksi liittyä kaikkiin poikkeamatyyppeihin, kun taas asiakasvalituksia koskeva ongelmatyyppi voi liittyä vain asiakkaan ja huoltopyynnön poikkeamatyyppeihin.</span><span class="sxs-lookup"><span data-stu-id="82ff9-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="82ff9-172">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-172">Click New.</span></span>
7. <span data-ttu-id="82ff9-173">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="82ff9-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="82ff9-174">Valitse Määrityksistä poikkeamisen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="82ff9-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="82ff9-175">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-175">Close the page.</span></span>
10. <span data-ttu-id="82ff9-176">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="82ff9-177">Määritä määrityksistä poikkeamisen käsittelyn karanteenivyöhykkeet</span><span class="sxs-lookup"><span data-stu-id="82ff9-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="82ff9-178">Valitse Varastonhallinta > Asetukset > Laadunhallinta > Karanteenivyöhykkeet.</span><span class="sxs-lookup"><span data-stu-id="82ff9-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="82ff9-179">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="82ff9-179">Click New.</span></span>
3. <span data-ttu-id="82ff9-180">Kirjoita Karanteenivyöhyke-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="82ff9-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="82ff9-181">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="82ff9-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="82ff9-182">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="82ff9-182">Close the page.</span></span>

