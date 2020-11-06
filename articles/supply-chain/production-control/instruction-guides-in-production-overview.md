---
title: Yhdistetyn todellisuuden oppaiden tuottaminen tuotannon työntekijöille
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Supply Chain Managementin tuotannon hallintamoduulin ja Dynamics 365 Guidesin integrointia.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000975"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="af1bb-103">Yhdistetyn todellisuuden oppaiden tuottaminen tuotannon työntekijöille</span><span class="sxs-lookup"><span data-stu-id="af1bb-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="af1bb-104">Tuotantoprosesseissa työskenteleville työntekijöille on apua oikea-aikaisesti toimitetuista työtilanteeseen liittyvistä ohjeista.</span><span class="sxs-lookup"><span data-stu-id="af1bb-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="af1bb-105">*Ohjeet* koskevat monia työalueita, kuten kokoonpanoa, huoltoa, työvaiheita, sertifiointia ja turvallisuutta.</span><span class="sxs-lookup"><span data-stu-id="af1bb-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="af1bb-106">Näitä liiketoiminnan perustoimintoja koskevat jatkuvasti kehittyvät koulutusohjeet auttavat työntekijöitä toimimaan tehokkaammin ja paremmin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="af1bb-107">Johdanto</span><span class="sxs-lookup"><span data-stu-id="af1bb-107">Introduction</span></span>

<span data-ttu-id="af1bb-108">Ohjeita voidaan antaa eri tavoin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="af1bb-109">Yksi tehokas, heti käyttövalmis järjestelmä käyttää [Dynamics 365 Guidesia](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="af1bb-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="af1bb-110">Dynamics 365 Guidesin avulla työntekijöille voidaan antaa käytännön opastusta.</span><span class="sxs-lookup"><span data-stu-id="af1bb-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="af1bb-111">Voit määrittää standardoidut prosessit vaiheittaisilla ohjeilla, jotka opastavat työntekijöitä valitsemaan tarvittavat työkalut ja osat. Lisäksi nämä oppaat näyttävät työntekijöille, miten kyseisiä työkaluja käytetään todellisissa työtilanteissa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="af1bb-112">Oppaita voi liittää esimerkiksi seuraaviin tuotannonhallinnan osiin:</span><span class="sxs-lookup"><span data-stu-id="af1bb-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="af1bb-113">Resurssit</span><span class="sxs-lookup"><span data-stu-id="af1bb-113">Resources</span></span>](#resources)
- [<span data-ttu-id="af1bb-114">Resurssiryhmät</span><span class="sxs-lookup"><span data-stu-id="af1bb-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="af1bb-115">Vapautetut tuotteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="af1bb-116">Reseptit</span><span class="sxs-lookup"><span data-stu-id="af1bb-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="af1bb-117">Kaavaversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="af1bb-118">Tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="af1bb-119">Tuoterakenneversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="af1bb-120">Reititykset</span><span class="sxs-lookup"><span data-stu-id="af1bb-120">Routes</span></span>](#routes)
- [<span data-ttu-id="af1bb-121">Reititysversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="af1bb-122">Reitityksen työvaihesuhteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="af1bb-123">Oppaita voi liittää myös käyttöomaisuuden hallinnan avulla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="af1bb-124">Lisätietoja tästä vaihtoehdosta on kohdassa [Dynamics 365 Supply Chain Managementin (Käyttöomaisuuden hallinta) ja Dynamics 365 Guidesin integrointi](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="af1bb-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="af1bb-125">Kun tuotannon työntekijä valitsee työn tuotannossa Supply Chain Managementissa, työntekijä näkee työkortissa olevat työhön [liittyvät oppaat](#logic).</span><span class="sxs-lookup"><span data-stu-id="af1bb-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="af1bb-126">Kun työntekijä valitsee tietyn oppaan, näyttöön tulee kyseisen oppaan QR-koodi.</span><span class="sxs-lookup"><span data-stu-id="af1bb-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="af1bb-127">Työntekijä käynnistää sitten oppaat skannaamalla sitten QR-koodin HoloLens-laitteella, jolloin liittyvät ohjeet tulevat näkyviin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="af1bb-128">Seuraavissa alaosioissa käsitellään joitakin skenaarioita, joissa eri toimialojen yrityksille on eniten hyötyä tuotannon ohjeiden esittämisestä oppaiden avulla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="af1bb-129">Kokoonpano</span><span class="sxs-lookup"><span data-stu-id="af1bb-129">Assembly</span></span>

<span data-ttu-id="af1bb-130">![Oppaiden käyttäminen kokoonpanotehtävissä](media/instruction-guides-hero-assembly.png "Oppaiden käyttäminen huoltotehtävissä")</span><span class="sxs-lookup"><span data-stu-id="af1bb-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="af1bb-131">Kokoonpanotoimintojen ohjeet näyttävät työntekijöille, mitä työkaluja ja osia he tarvitsevat ja miten niitä käytetään käytännössä käytetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="af1bb-132">Tuotantopäälliköt voivat luoda ja määrittää oppaita esimerkiksi [tuotantoreittejä](routes-operations.md), [työvaiheiden suhteita](routes-operations.md#operation-relations) tai [tuoterakennetta](bill-of-material-bom.md) varten.</span><span class="sxs-lookup"><span data-stu-id="af1bb-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="af1bb-133">Työntekijät saavat käyttöönsä tuotannon työvaihetta koskevat ohjeet.</span><span class="sxs-lookup"><span data-stu-id="af1bb-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="af1bb-134">Huolto</span><span class="sxs-lookup"><span data-stu-id="af1bb-134">Service</span></span>

<span data-ttu-id="af1bb-135">![Oppaiden käyttäminen huoltotehtävissä](media/instruction-guides-hero-service.png "Oppaiden käyttäminen huoltotehtävissä")</span><span class="sxs-lookup"><span data-stu-id="af1bb-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="af1bb-136">Teknikoille voidaan antaa opastetut ohjeet työkohteessa, joten lisäkäyntejä ei tarvitse aikatauluttaa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="af1bb-137">Huoltopäälliköt voivat määrittää esimerkiksi tietyille [tuotteille](../../commerce/product.md) oppaita, joissa käydään läpi kaikki laadunarviointitoimet.</span><span class="sxs-lookup"><span data-stu-id="af1bb-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="af1bb-138">Laatu</span><span class="sxs-lookup"><span data-stu-id="af1bb-138">Quality</span></span>

<span data-ttu-id="af1bb-139">![Oppaiden käyttäminen laadunvalvontatehtävissä](media/instruction-guides-hero-quality.png "Oppaiden käyttäminen laadunvalvontatehtävissä")</span><span class="sxs-lookup"><span data-stu-id="af1bb-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="af1bb-140">Uusien prosessien käyttöönottaminen ja yhdenmukaisuuden paranemisen varmistaminen muuttamalla työntekijöiden tietämyksen toistettavaksi työkaluksi.</span><span class="sxs-lookup"><span data-stu-id="af1bb-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="af1bb-141">Laadunvalvontapäälliköt voivat määrittää esimerkiksi [tuotteille](../../commerce/product.md) oppaita, joissa käydään läpi kaikki laadunarviointitoimet.</span><span class="sxs-lookup"><span data-stu-id="af1bb-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="af1bb-142">Varmenteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-142">Certifications</span></span>

<span data-ttu-id="af1bb-143">![Oppaiden käyttäminen sertifiointiin liittyvissä tehtävissä](media/instruction-guides-hero-certification.png "Oppaiden käyttäminen sertifiointiin liittyvissä tehtävissä")</span><span class="sxs-lookup"><span data-stu-id="af1bb-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="af1bb-144">Tunnistamalla nopeasti, ketkä työntekijät tarvitsevat apua ja missä apua tarvitaan, voidaan varmistaa, että kaikki työntekijät ovat korkeiden standardien mukaisia.</span><span class="sxs-lookup"><span data-stu-id="af1bb-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="af1bb-145">Turvallisuus</span><span class="sxs-lookup"><span data-stu-id="af1bb-145">Safety</span></span>

<span data-ttu-id="af1bb-146">![Oppaiden käyttäminen työturvallisuusohjeistuksessa](media/instruction-guides-hero-safety.png "Oppaiden käyttäminen työturvallisuusohjeistuksessa")</span><span class="sxs-lookup"><span data-stu-id="af1bb-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="af1bb-147">Vaarallisten toimenpiteiden käyminen läpi virtuaalisesti ohjeiden avulla ennen niiden suorittamista fyysisessä ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="af1bb-148">Yhdistetyn todellisuuden avulla työntekijät voivat kokeilla vaarallisia toimenpiteitä virtuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="af1bb-149">Tuotantopäälliköt voivat antaa tarkkoja vaarallisten materiaalien tai helposti särkyvien tuotteiden käsittelyohjeita määrittämällä ohjeet [tuotenimikkeille](../../commerce/product.md), [reiteille](routes-operations.md) ja [työvaiheille](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="af1bb-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="af1bb-150">Ohjeiden ja oppaiden käytön aloittaminen</span><span class="sxs-lookup"><span data-stu-id="af1bb-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="af1bb-151">Dynamics 365 Guides voidaan integroida heti Supply Chain Managementiin, mikä mahdollistaa ohjeiden antamisen tuotantoprosesseissa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="af1bb-152">Tuotannon resursseja ja töitä koskevien yhdistetyn todellisuuden ohjeiden muodostaminen, ylläpitäminen ja määrittäminen edellyttää käyttöoikeudellista asennettua Guidesin sovellusesiintymää.</span><span class="sxs-lookup"><span data-stu-id="af1bb-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="af1bb-153">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="af1bb-153">Prerequisites</span></span>

<span data-ttu-id="af1bb-154">Tämän toiminnon käyttö edellyttää, että järjestelmä sisältää seuraavat:</span><span class="sxs-lookup"><span data-stu-id="af1bb-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="af1bb-155">Dynamics 365 Supply Chain Management versio 10.0.15 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="af1bb-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="af1bb-156">Supply Chain Management -sovellusten [kaksoiskirjoitus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write)</span><span class="sxs-lookup"><span data-stu-id="af1bb-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="af1bb-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) -versio 400.0.1.48 tai sitä uudempi</span><span class="sxs-lookup"><span data-stu-id="af1bb-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="af1bb-158">Toiminnon ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="af1bb-158">Turn on the feature</span></span>

<span data-ttu-id="af1bb-159">Toiminnon käyttäminen järjestelmässä edellyttää, että sen määritysavaimet on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="af1bb-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="af1bb-160">Se on tehtävä vain kerran.</span><span class="sxs-lookup"><span data-stu-id="af1bb-160">You only need to do this once.</span></span> <span data-ttu-id="af1bb-161">Järjestelmänvalvojan on tehtävä sitä varten seuraavat toimet:</span><span class="sxs-lookup"><span data-stu-id="af1bb-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="af1bb-162">Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="af1bb-163">Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="af1bb-164">Laajenna **Yhdistetty todellisuus** -osa ja valitse sitten **Yhdistetyn todellisuus opas** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="af1bb-165">Laajenna **Tuotannon hallinta** -osa ja valitse sitten **Tuotanto-ohjeet** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="af1bb-166">Poista järjestelmä ylläpitotila käytöstä kohdassa [Ylläpitotila](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="af1bb-167">Oppaiden näkymisen määrittäminen tuotantoon</span><span class="sxs-lookup"><span data-stu-id="af1bb-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="af1bb-168">Määritä tapa, jolla oppat näkyvät tuotannossa, valitsemalla **Yhdistetty todellisuus \> Dynamics 365 Guides \> Määritä oppaiden integrointi**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="af1bb-169">![Oppaan integroinnin määrittäminen tuotantoa varten](media/instruction-guides-configure-integration.png "Oppaan integroinnin määrittäminen tuotantoa varten")</span><span class="sxs-lookup"><span data-stu-id="af1bb-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="af1bb-170">Määritä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="af1bb-170">Set the following fields:</span></span>

- <span data-ttu-id="af1bb-171">**Common Data Service -alitoimialue** – Tässä kentässä on oltava aina arvo.</span><span class="sxs-lookup"><span data-stu-id="af1bb-171">**Common Data Service subdomain** - This field should already show a value.</span></span> <span data-ttu-id="af1bb-172">Tämä kenttä sisältää sen Common Data Service -ympäristön alitoimialueen, jossa oppaat luodaan.</span><span class="sxs-lookup"><span data-stu-id="af1bb-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="af1bb-173">Alitoimialue on URL-osoitteen ensimmäinen osa, joka yleensä nimetään organisaation mukaan.</span><span class="sxs-lookup"><span data-stu-id="af1bb-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="af1bb-174">Jos esimerkiksi Common Data Servicen URL-osoite on contoso.crm4.dynamics.com, annan tässä kohdassa *contoso*.</span><span class="sxs-lookup"><span data-stu-id="af1bb-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="af1bb-175">Tätä arvoa käytetään oppaisen osoitteiden laatimiseen, ja se koodataan QR-koodeihin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="af1bb-176">**QR-koodin koko** – Määritä hahmonnetun QR-koodin koko.</span><span class="sxs-lookup"><span data-stu-id="af1bb-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="af1bb-177">Järkevintä on valita koko, joka täyttää suurimman osan näytöstä mutta ei enemmän.</span><span class="sxs-lookup"><span data-stu-id="af1bb-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="af1bb-178">*15* on yleensä hyvä arvo.</span><span class="sxs-lookup"><span data-stu-id="af1bb-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="af1bb-179">**QR-koodin virheen korjaustaso** – Määritä QR-koodin tarkkuus.</span><span class="sxs-lookup"><span data-stu-id="af1bb-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="af1bb-180">Mitä tarkempi koodi on, sitä luotettavampi se on. **QR-koodin koon** on kuitenkin oltava riittävän suuri, jotta se tukee valitun korjaustason mukaista tietojen tasoa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="af1bb-181">Näyttöön liian suurien QR-koodien kokojen hahmontaminen kestää kauemmin, ja ne on sitten pienennettävä näyttöön sopivaksi.</span><span class="sxs-lookup"><span data-stu-id="af1bb-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="af1bb-182">Tästä ei ole mitään hyötyä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="af1bb-183">Jos QR-koodin koko on taas liian pieni, on mahdollista, että HoloLens ei lue koodia oikein joissakin ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="af1bb-184">Tämä asetus kannattaakin testata jokaisessa laitteessa, jolla QR-koodi näytetään HoloLens-käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="af1bb-185">Valitse asetukset, joilla saadaan riittävän hyvä luettavuus tuotantoympäristössä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="af1bb-186">Kaikkien oppaan tehtävien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="af1bb-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="af1bb-187">Valitsemalla **Kaikki oppaat** -sivun näet luettelon kaikista organisaatiossa käytettävissä olevista oppaista sekä kaikista tuotannon prosessien ja resurssien tehtävistä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="af1bb-188">Avaa se valitsemalla **Yhdistetty todellisuus \> Oppaat \> Kaikki oppaat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="af1bb-189">Yläosassa on kaikki käytettävissä olevat oppaat sisältävä luettelo, ja voit suodattaa luetteloa suodatuskentän avulla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="af1bb-190">Alaosassa on kaikki oppaan tehtävät sisältävä luettelo sekä työkalurivi, jolla niitä voi hallita.</span><span class="sxs-lookup"><span data-stu-id="af1bb-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="af1bb-191">![Oppaiden hallinta](media/instruction-guides-allguides.png "Oppaiden hallinta")</span><span class="sxs-lookup"><span data-stu-id="af1bb-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="af1bb-192">Seuraavissa osissa käsitellään objektityyppejä, joille voidaan määrittää oppaita.</span><span class="sxs-lookup"><span data-stu-id="af1bb-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="af1bb-193">Kukin määritetty ohje sisältää ohjeet, jotka liitetään automaattisesti kyseisiin tuotantotöihin ja joita voi käyttää tuotannossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="af1bb-194">Oppaan liittäminen resurssiin</span><span class="sxs-lookup"><span data-stu-id="af1bb-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="af1bb-195">Kun opas liitetään [resurssiin](operations-resources.md), kyseistä opasta voi käyttää soveltuvan tuotantotyön yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="af1bb-196">Tyypillinen resursseja käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-196">Typical scenario using resources</span></span>

<span data-ttu-id="af1bb-197">Voit liittää oppaan esimerkiksi konetyyppisen resurssin yleisiin turvallisuusohjeisiin tai käsittelyohjeisiin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="af1bb-198">Tämän jälkeen opas on käytettävissä jokaisessa kyseisessä laitteessa tehtävässä työssä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="af1bb-199">Oppaan liittäminen resurssiin</span><span class="sxs-lookup"><span data-stu-id="af1bb-199">Add a Guide to a resource</span></span>

<span data-ttu-id="af1bb-200">Oppaan liittäminen resurssiin:</span><span class="sxs-lookup"><span data-stu-id="af1bb-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="af1bb-201">Valitse **Tuotannonhallinta \> Asetukset \> Resurssit \> Resurssit**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="af1bb-202">Valitse luetteloruudussa resurssi, johon haluat määrittää oppaan.</span><span class="sxs-lookup"><span data-stu-id="af1bb-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-203">Laajenna **Liitetyt oppaat** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="af1bb-204">Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="af1bb-205">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="af1bb-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="af1bb-206">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="af1bb-207">Jos oppaita on paljon, oikean oppaan voi etsiä luetteloa suodattamalla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="af1bb-208">![Oppaiden hallinta](media/instruction-guides-allguides.png "Oppaiden hallinta")</span><span class="sxs-lookup"><span data-stu-id="af1bb-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="af1bb-209">Oppaan liittäminen resurssiryhmään</span><span class="sxs-lookup"><span data-stu-id="af1bb-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="af1bb-210">Oppaan voi lisätä [resurssiryhmiin](tasks/define-discrete-manufacturing-resource-group.md), jos niillä hallitaan koneiden, tuotantolinjojen ja työsolujen ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="af1bb-211">Tyypillisiä resurssiryhmiä käyttäviä skenaariota</span><span class="sxs-lookup"><span data-stu-id="af1bb-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="af1bb-212">**Esimerkki 1:** Resurssiryhmä on määritetty useille saman mallin koneille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="af1bb-213">Sen sijaan että konemallin käsittelyohjeiden opas määritettäisiin jokaiselle kyseiselle resurssille, opas voidaan määrittää resurssiryhmälle, joka vastaa kyseistä konemallia.</span><span class="sxs-lookup"><span data-stu-id="af1bb-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="af1bb-214">**Esimerkki 2:** Resurssiryhmä on määritetty erilaisia koneita sisältävälle työsolulle ja käytössä on opas, jossa on työsolun ylläpidon yleiset ohjeet.</span><span class="sxs-lookup"><span data-stu-id="af1bb-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="af1bb-215">Opas koskee kaikkia tämän työsolun tuotantotehtäviä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="af1bb-216">Oppaan liittäminen resurssiryhmään</span><span class="sxs-lookup"><span data-stu-id="af1bb-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="af1bb-217">Oppaan liittäminen resurssiryhmään:</span><span class="sxs-lookup"><span data-stu-id="af1bb-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="af1bb-218">Valitse **Tuotannonhallinta \> Asetukset \> Resurssit \> Resurssiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="af1bb-219">Valitse luetteloruudussa resurssiryhmä, johon haluat määrittää oppaan.</span><span class="sxs-lookup"><span data-stu-id="af1bb-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-220">Laajenna **Liitetyt oppaat** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="af1bb-221">Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="af1bb-222">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="af1bb-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="af1bb-223">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="af1bb-224">Jos oppaita on paljon, oikean oppaan voi etsiä luetteloa suodattamalla.</span><span class="sxs-lookup"><span data-stu-id="af1bb-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="af1bb-225">![Oppaan lisääminen resurssiryhmään](media/instruction-guides-resourcegroup.png "Oppaan lisääminen resurssiryhmään")</span><span class="sxs-lookup"><span data-stu-id="af1bb-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="af1bb-226">Oppaan liittäminen vapautettuun tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="af1bb-227">Opas voidaan lisätä mihin tahansa [vapautettuun tuotteeseen](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="af1bb-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="af1bb-228">Tyypillinen vapautettuja tuotteita käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-228">Typical scenario using released products</span></span>

<span data-ttu-id="af1bb-229">Tuotantotason oppaissa on tuotannon työntekijöiden apuna ohjeita, jotka liittyvät tietyn vapautetun tuotteen tai nimikkeen käyttämiseen tai käsittelemiseen.</span><span class="sxs-lookup"><span data-stu-id="af1bb-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="af1bb-230">Oppaan lisääminen vapautettuun tuotteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-230">Add a Guide to a released product</span></span>

<span data-ttu-id="af1bb-231">Oppaan lisääminen vapautettuun tuotteeseen:</span><span class="sxs-lookup"><span data-stu-id="af1bb-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="af1bb-232">Mene **Tuotantotietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="af1bb-233">Avaa tuote, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-234">Avaa toimintoruudussa **Suunnittele** -välilehti ja valitse **Näytä** -ryhmässä **Liitetyt oppaat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="af1bb-235">Valitun tuotteen **Liitetyt oppaat** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="af1bb-236">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="af1bb-237">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-238">![Oppaan lisääminen vapautettuun tuotteeseen](media/instruction-guides-ReleasedProduct-AddGuides.png "Oppaan lisääminen vapautettuun tuotteeseen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="af1bb-239">Oppaan liittäminen kaavaan</span><span class="sxs-lookup"><span data-stu-id="af1bb-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="af1bb-240">Opas voidaan lisätä mihin tahansa [kaavaan](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="af1bb-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="af1bb-241">Tyypillinen kaavoja käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="af1bb-242">Kaavatason oppaista tuotannon työtekijät saavat opastetut käsittelyohjeet kaavojen tai reseptien yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="af1bb-243">Oppaat voidaan määrittää kaavan versioille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="af1bb-244">Kaavaan perustuvan tuotantoprosesseihin liittyvän opastuksen voi määrittää reitille, reittiversioon tai reitin työvaihesuhteisiin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="af1bb-245">Oppaita ei voi tällä hetkellä liittää yksittäisille kaavariveille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="af1bb-246">Oppaan lisääminen kaavaan</span><span class="sxs-lookup"><span data-stu-id="af1bb-246">Add a Guide to a formula</span></span>

<span data-ttu-id="af1bb-247">Oppaan lisääminen kaavaan:</span><span class="sxs-lookup"><span data-stu-id="af1bb-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="af1bb-248">Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="af1bb-249">Avaa kaava, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-250">Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="af1bb-251">Laajenna **Liitetyt oppaat** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="af1bb-252">Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="af1bb-253">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="af1bb-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="af1bb-254">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-255">![Oppaan lisääminen kaavaan](media/instruction-guides-Formula.png "Oppaan lisääminen kaavaan")</span><span class="sxs-lookup"><span data-stu-id="af1bb-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="af1bb-256">Oppaan liittäminen kaavaversioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="af1bb-257">Opas voidaan lisätä mihin tahansa [kaavaversioon](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="af1bb-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="af1bb-258">Tyypillinen kaavaversioita käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="af1bb-259">Kaavan yksittäiseen versioon liitetyt oppaat antavat tuotannon työntekijöille ohjeita, joissa käydään läpi kaavan kyseisen version tuotanto.</span><span class="sxs-lookup"><span data-stu-id="af1bb-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="af1bb-260">Kaavan tähän versioon perustuvan tuotantoprosesseihin liittyvän opastuksen voi määrittää reitille, reittiversioon tai reitin työvaihesuhteisiin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="af1bb-261">Oppaita ei voi tällä hetkellä liittää yksittäisille kaavariveille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="af1bb-262">Oppaan lisääminen kaavaversioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="af1bb-263">Oppaan lisääminen kaavaversioon:</span><span class="sxs-lookup"><span data-stu-id="af1bb-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="af1bb-264">Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Kaavat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="af1bb-265">Avaa sen version sisältävä kaava, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-266">Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="af1bb-267">Valitse **Kaavaversiot** -pikavälilehdessä versio, jolla opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-268">Valitse **Kaavaversiot** -työkalurivillä **Liitetyt oppaat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="af1bb-269">![Valittuun kaavaversioon liittyvien oppaiden avaaminen](media/instruction-guides-FormulaVersion.png "Valittuun kaavaversioon liittyvien oppaiden avaaminen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="af1bb-270">Kaavaversion **Liitetyt oppaat** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="af1bb-271">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="af1bb-272">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-273">![Oppaan lisääminen kaavaversioon](media/instruction-guides-FormulaVersionAddGuide.png "Oppaan lisääminen kaavaversioon")</span><span class="sxs-lookup"><span data-stu-id="af1bb-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="af1bb-274">Oppaan liittäminen tuoterakenteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="af1bb-275">Oppaan voi lisätä mihin tahansa [tuoterakenteeseen](bill-of-material-bom.md).</span><span class="sxs-lookup"><span data-stu-id="af1bb-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="af1bb-276">Tyypillinen tuoterakennetta käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="af1bb-277">Tuoterakenteeseen liitetyissä oppaissa on tuotannon työntekijöille ohjeita tuoterakenteen materiaalin valmisteluun ja käsittelyyn.</span><span class="sxs-lookup"><span data-stu-id="af1bb-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="af1bb-278">Oppaat voidaan määrittää tuoterakenteen versioille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="af1bb-279">Oppaita ei voi tällä hetkellä liittää yksittäisille tuoterakenteen riveille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="af1bb-280">Oppaan lisääminen tuoterakenteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="af1bb-281">Oppaan lisääminen tuoterakenteeseen:</span><span class="sxs-lookup"><span data-stu-id="af1bb-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="af1bb-282">Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Tuoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="af1bb-283">Avaa tuoterakenne, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-284">Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="af1bb-285">Laajenna **Liitetyt oppaat** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="af1bb-286">Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="af1bb-287">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="af1bb-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="af1bb-288">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-289">![Oppaan lisääminen tuoterakenteeseen](media/instruction-guides-BOM.png "Oppaan lisääminen tuoterakenteeseen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="af1bb-290">Oppaan liittäminen tuoterakenteen versioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="af1bb-291">Oppaan voi lisätä mihin tahansa [tuoterakenteen versioon](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="af1bb-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="af1bb-292">Tyypillinen tuoterakenteen versioita käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="af1bb-293">Yksittäiseen tuoterakenteen versioon liitetyissä oppaissa on tuotannon työntekijöille ohjeita, jotka selittävät yleisestä tuoterakenteesta tai sen muista versioista poikkeavan tuoterakenteen version materiaalien valmistelua ja käsittelyä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="af1bb-294">Oppaita ei voi tällä hetkellä liittää yksittäisille tuoterakenteen riveille.</span><span class="sxs-lookup"><span data-stu-id="af1bb-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="af1bb-295">Oppaan lisääminen tuoterakenteen versioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="af1bb-296">Oppaan lisääminen tuoterakenteen versioon:</span><span class="sxs-lookup"><span data-stu-id="af1bb-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="af1bb-297">Valitse **Tuotantotietojen hallinta \> Tuoterakenteet ja kaavat \> Tuoterakenteet**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="af1bb-298">Avaa sen version sisältävä tuoterakenne, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-299">Avaa ylemmän pikavälilehden yläpuolella oleva **Otsikko** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="af1bb-300">Valitse **Tuoterakenteen versiot** -pikavälilehdessä versio, jolla opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-301">Valitse **Tuoterakenteen versiot** -työkalurivillä **Liitetyt oppaat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="af1bb-302">![Valittuun tuoterakenteen versioon liittyvien oppaiden avaaminen](media/instruction-guides-BOMVersion.png "Valittuun tuoterakenteen versioon liittyvien oppaiden avaaminen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="af1bb-303">Tuoterakenteen version **Liitetyt oppaat** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="af1bb-304">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="af1bb-305">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-306">![Oppaan lisääminen tuoterakenteen versioon](media/instruction-guides-BOMVersionAddGuide.png "Oppaan lisääminen tuoterakenteen versioon")</span><span class="sxs-lookup"><span data-stu-id="af1bb-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="af1bb-307">Oppaan liittäminen reittiin</span><span class="sxs-lookup"><span data-stu-id="af1bb-307">Associate a Guide to a route</span></span>

<span data-ttu-id="af1bb-308">Opas voidaan lisätä mihin tahansa [reittiin](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="af1bb-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="af1bb-309">Tyypillinen reittejä käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-309">Typical scenario using routes</span></span>

<span data-ttu-id="af1bb-310">Reittejä käytetään tyypillisesti määrittämään, miten tietty vapautettu tuote tuotetaan tuoterakenteen tai tuoterakenteen version ja resurssijoukon tai resurssiryhmien perusteella.</span><span class="sxs-lookup"><span data-stu-id="af1bb-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="af1bb-311">Opas määritetään reittiin antamaan kyseisen tuotantoprosessin vaiheittaiset ohjeet.</span><span class="sxs-lookup"><span data-stu-id="af1bb-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="af1bb-312">Oppaan lisääminen reittiin</span><span class="sxs-lookup"><span data-stu-id="af1bb-312">Add a Guide to a route</span></span>

<span data-ttu-id="af1bb-313">Oppaan lisääminen reittiin:</span><span class="sxs-lookup"><span data-stu-id="af1bb-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="af1bb-314">Valitse **Tuotannonhallinta \> Kaikki reitit**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="af1bb-315">Avaa reitti, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-316">Laajenna **Liitetyt oppaat** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="af1bb-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="af1bb-317">Valitse **Lisää** **Liittyvät oppaat** -työkalurivillä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="af1bb-318">Uusi rivi lisätään ruudukkoon.</span><span class="sxs-lookup"><span data-stu-id="af1bb-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="af1bb-319">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-320">![Oppaan lisääminen reittiin](media/instruction-guides-Route.png "Oppaan lisääminen reittiin")</span><span class="sxs-lookup"><span data-stu-id="af1bb-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="af1bb-321">Oppaan liittäminen reitin versioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="af1bb-322">Opas voidaan lisätä mihin tahansa [reitin versioon](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="af1bb-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="af1bb-323">Tyypillinen reitin versioita käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-323">Typical scenario using route versions</span></span>

<span data-ttu-id="af1bb-324">Reitin versioita käytetään tyypillisesti määrittämään tuotantoprosessien variantteja aiemmin luodun reitin perusteella.</span><span class="sxs-lookup"><span data-stu-id="af1bb-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="af1bb-325">Kullekin reitin versiolle voi määrittää eri oppaat.</span><span class="sxs-lookup"><span data-stu-id="af1bb-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="af1bb-326">Oppaan lisääminen reitin versioon</span><span class="sxs-lookup"><span data-stu-id="af1bb-326">Add a Guide to a route version</span></span>

<span data-ttu-id="af1bb-327">Oppaan lisääminen reitin versioon:</span><span class="sxs-lookup"><span data-stu-id="af1bb-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="af1bb-328">Valitse **Tuotannonhallinta \> Kaikki reitit**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="af1bb-329">Avaa reitti, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-330">Valitse **Versiot** -pikavälilehdessä versio, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-331">Valitse **Versiot** -työkalurivillä **Liitetyt oppaat**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="af1bb-332">![Valittuun reitin versioon liittyvien oppaiden avaaminen](media/instruction-guides-RouteVersion.png "Valittuun reitin versioon liittyvien oppaiden avaaminen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="af1bb-333">Tuoterakenteen version **Liitetyt oppaat** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="af1bb-334">Lisää ruudukkoon uusi rivi valitsemalla toimintoruudussa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="af1bb-335">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="af1bb-336">![Oppaan lisääminen reitin versioon](media/instruction-guides-RouteVersionAddGuide.png "Oppaan lisääminen reitin versioon")</span><span class="sxs-lookup"><span data-stu-id="af1bb-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="af1bb-337">Oppaan liittäminen reitin työvaihesuhteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="af1bb-338">Opas voidaan lisätä mihin tahansa [reitin työvaihesuhteeseen](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="af1bb-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="af1bb-339">Tyypillinen reitin työvaihesuhteita käyttävä skenaario</span><span class="sxs-lookup"><span data-stu-id="af1bb-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="af1bb-340">Työvaihesuhteet ovat tarkoin tapa lisätä ohjeita tuoteprosessin ja siihen liittyviin työvaiheisiin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="af1bb-341">Reitin kullekin työvaiheelle voidaan määrittää ohje, ja määritetty ohje voi vaihdella reitille määritetyn suhteen tyypin mukaan. Ohje voi siis olla erilainen esimerkiksi sen mukaan, mikä nimike tai määritys on kyseessä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="af1bb-342">Lisäksi voidaan määrittää, mitä työvaiheen osavaiheetta (kuten määritystä, jonoon asettamista, käsittelyä tai kuljetusta) ohjeet koskevat.</span><span class="sxs-lookup"><span data-stu-id="af1bb-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="af1bb-343">Jos reitin useille työvaihesuhteille määritetään oppaita, näistä oppaista vain tarkimmin suhdetta vastaava opas näytetään luodulle työlle tuotannossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="af1bb-344">Oppaan lisääminen reitin työvaihesuhteeseen</span><span class="sxs-lookup"><span data-stu-id="af1bb-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="af1bb-345">Oppaan lisääminen reitin työvaihesuhteeseen:</span><span class="sxs-lookup"><span data-stu-id="af1bb-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="af1bb-346">Valitse **Tuotannonhallinta \> Kaikki reitit**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="af1bb-347">Avaa reitti, jolle opas määritetään.</span><span class="sxs-lookup"><span data-stu-id="af1bb-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="af1bb-348">Avaa toimintoruudussa **Reitti** -välilehti ja valitse **Ylläpito** -ryhmässä **Reititystiedot**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="af1bb-349">Valitun reitin **Reititystiedot** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="af1bb-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="af1bb-350">Valitse yläruudukosta työvaihe, jolle ohjeet annetaan.</span><span class="sxs-lookup"><span data-stu-id="af1bb-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="af1bb-351">Valitse alaruudukossa tietty suhde (tai yleinen **Kaikki** -suhde).</span><span class="sxs-lookup"><span data-stu-id="af1bb-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="af1bb-352">![Työvaiheen ja sen jälkeen suhteen valitseminen](media/instruction-guides-RouteOperationRelation.png "Työvaiheen ja sen jälkeen suhteen valitseminen")</span><span class="sxs-lookup"><span data-stu-id="af1bb-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="af1bb-353">Avaa alaruudukon yläpuolella **Liitetyt oppaat** -välilehti. ![Liitetyt oppaat -välilehti](media/instruction-guides-RouteOperationRelation-AddGuide.png "Liitetyt oppaat -välilehti")</span><span class="sxs-lookup"><span data-stu-id="af1bb-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="af1bb-354">Lisää ruudukkoon uusi rivi valitsemalla alaruudukon yläosan työkalurivillä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="af1bb-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="af1bb-355">Valitse uudelle riville määritettävä opas **Nimi** -sarakkeen avattavassa luettelossa.</span><span class="sxs-lookup"><span data-stu-id="af1bb-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="af1bb-356">Valitse rivin muilta osin valintaruutu jokaiselle tilanteelle, jossa valittu opas on oltava käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="af1bb-357">Kunkin työvaiheen kuhunkin osavaiheeseen voi lisätä useita oppaita.</span><span class="sxs-lookup"><span data-stu-id="af1bb-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="af1bb-358">Oppaiden valitseminen tuotannon käyttöliittymässä</span><span class="sxs-lookup"><span data-stu-id="af1bb-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="af1bb-359">Kun työntekijä avaa työluettelon tuotannon käyttöliittymässä, Supply Chain Management etsii näkyvissä olevia töitä koskevat oppaat.</span><span class="sxs-lookup"><span data-stu-id="af1bb-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="af1bb-360">Voit tarkastella liittyviä oppaita **Oppaat** -painikkeella.</span><span class="sxs-lookup"><span data-stu-id="af1bb-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="af1bb-361">![Oppaat-painike tuotannon käyttöliittymässä](media/instruction-guides-Shopfloor1.png "Oppaat-painike tuotannon käyttöliittymässä")</span><span class="sxs-lookup"><span data-stu-id="af1bb-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="af1bb-362">Aseta HoloLens sitten paikalleen ja siirry soveltuvaan oppaaseen vilkaisemalla QR-koodia ja aktivoimalla opas tällä tavoin.</span><span class="sxs-lookup"><span data-stu-id="af1bb-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="af1bb-363">![QR-koodi oppaiden käyttämiseen HoloLensin avulla](media/instruction-guides-Shopfloor2.png "QR-koodi oppaiden käyttämiseen HoloLensin avulla")</span><span class="sxs-lookup"><span data-stu-id="af1bb-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="af1bb-364">Oppaiden valintalogiikan ratkaiseminen</span><span class="sxs-lookup"><span data-stu-id="af1bb-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="af1bb-365">Oppaita voi lisätä seuraaviin tuotantotietoihin:</span><span class="sxs-lookup"><span data-stu-id="af1bb-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="af1bb-366">Resurssit</span><span class="sxs-lookup"><span data-stu-id="af1bb-366">Resources</span></span>](#resources)
- [<span data-ttu-id="af1bb-367">Resurssiryhmät</span><span class="sxs-lookup"><span data-stu-id="af1bb-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="af1bb-368">Vapautetut tuotteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="af1bb-369">Reseptit</span><span class="sxs-lookup"><span data-stu-id="af1bb-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="af1bb-370">Kaavaversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="af1bb-371">Tuoterakenteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="af1bb-372">Tuoterakenneversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="af1bb-373">Reititykset</span><span class="sxs-lookup"><span data-stu-id="af1bb-373">Routes</span></span>](#routes)
- [<span data-ttu-id="af1bb-374">Reititysversiot</span><span class="sxs-lookup"><span data-stu-id="af1bb-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="af1bb-375">Reitityksen työvaihesuhteet</span><span class="sxs-lookup"><span data-stu-id="af1bb-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="af1bb-376">Kun Supply Chain Management luo tuotannon töitä, se kerää liittyvät oppaat kyseisistä lähteistä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="af1bb-377">Ota huomioon seuraavat tärkeät säännöt.</span><span class="sxs-lookup"><span data-stu-id="af1bb-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="af1bb-378">Jos liität tuoterakenteen tai kaavan version reittiin tai tuotantotilaukseen, niin kyseiseen versioon ja myös sen päätuoterakenteeseen tai -kaavaan liitetyt oppaat näytetään työssä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="af1bb-379">Jos liität reitin version tuotantotilaukseen, niin kyseiseen versioon ja myös sen pääreittiin liitetyt oppaat näytetään työssä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="af1bb-380">Jos määrität useita reitityksen työvaiheita, jotka sisältävät *Kaikki* -suhteen, ja määrität niille oppaita, vain tarkimman suhteen oppaat näytetään työssä.</span><span class="sxs-lookup"><span data-stu-id="af1bb-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="af1bb-381">![Kaavio oppaiden soveltuvuuden ratkaisemisesta](media/instruction-guides-Resolve.png "Kaavio oppaiden soveltuvuuden ratkaisemisesta")</span><span class="sxs-lookup"><span data-stu-id="af1bb-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
