---
title: Konsernin sisäinen suunnittelu
description: Tässä aiheessa käsitellään konsernin sisäistä suunnittelua ja konsernin sisäisen suunnittelun määrittämistä Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin avulla.
author: ChristianRytt
manager: tfehr
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25c80ce27498131c6eb92174ab14a592bfa9915a
ms.sourcegitcommit: fe21a3a98dcf6fe4eb9351941493f2c0443d8696
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672182"
---
# <a name="intercompany-planning"></a><span data-ttu-id="e6e7f-103">Konsernin sisäinen suunnittelu</span><span class="sxs-lookup"><span data-stu-id="e6e7f-103">Intercompany planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6e7f-104">Joissakin organisaatioissa logistiikkatoiminnot ovat riippuvaisia organisaation muista yrityksistä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-104">For some organizations, logistics operations depend on other legal entities (companies) in the organization.</span></span> <span data-ttu-id="e6e7f-105">Näitä toimintoja käsitellään konsernin sisäisten myyntien ja ostojen avulla, koska kullakin yrityksellä on erillinen tilikartta.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-105">These operations are handled by using intercompany sales and purchases, because each legal entity has a separate chart of accounts.</span></span>

<span data-ttu-id="e6e7f-106">Tässä aiheessa käsitellään konsernin sisäistä suunnittelua ja konsernin sisäisen suunnittelun määrittämistä Microsoft Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin avulla.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-106">This topic describes intercompany planning and explains how to configure intercompany planning with Planning Optimization in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e6e7f-107">Tässä aiheessa käytetään seuraavia tärkeitä konsernin sisäisiä käsitteitä:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-107">This topic uses the following important intercompany terms:</span></span>

- <span data-ttu-id="e6e7f-108">**Yläpuolinen** – Suhteellinen viittaus vahvistus- tai toimitusketjussa.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-108">**Upstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="e6e7f-109">Se ilmaisee raaka-aineen toimittajaan päin suuntautuvaa liikettä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-109">It indicates movement in the direction of the raw material supplier.</span></span>
- <span data-ttu-id="e6e7f-110">**Alapuolinen** – Suhteellinen viittaus vahvistus- tai toimitusketjussa.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-110">**Downstream** – A relative reference in a firm or supply chain.</span></span> <span data-ttu-id="e6e7f-111">Se ilmaisee asiakkaaseen päin suuntautuvaa liikettä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-111">It indicates movement in the direction of the customer.</span></span>
- <span data-ttu-id="e6e7f-112">**Suunniteltu konsernin sisäinen kysyntä** – tuotteen suunniteltu kysyntä yrityksessä sen perusteella, mikä on tuotteen suunniteltu kysyntä alapuolisessa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-112">**Planned intercompany demand** – Planned demand for a product in a company, based on planned demand for the product from a downstream company.</span></span>

<span data-ttu-id="e6e7f-113">Pääsuunnittelussa yhden yrityksen suunnitelma voi sisältää suunnitellun konsernin sisäisen kysynnän, joka liittyy suunniteltuihin tilaukseen toisen yrityksen suunnitelmasta:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-113">In master planning, a plan in one company can include planned intercompany demand that is related to planned orders from a plan in another company.</span></span> <span data-ttu-id="e6e7f-114">Tämä ominaisuus on kätevä, sillä sen avulla saada täysi näkyvyys eri yritysten suunniteltuihin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-114">This capability is useful, because it provides full visibility into planned orders across companies.</span></span> <span data-ttu-id="e6e7f-115">Se myös varmistaa, että kaikki tarvittavat suunnittelut toimitustilaukset luodaan ilman, että kyseiset suunnitellut tilaukset olisi vahvistettava konsernin sisäistä kysyntää varten.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-115">It also ensures that all required planned supply orders are created, but without requiring that planned orders be firmed for the intercompany demand.</span></span>

<span data-ttu-id="e6e7f-116">Jos pääsuunnittelu suoritetaan pääsuunnitelmasta, joka sisältää suunnitellun alapuolisen kysynnän, liittyvien konsernin sisäisten toimittajien suunnitellut ostotilaukset sisällytetään suunnitelmaan kysyntänä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-116">If you run master planning from a master plan that includes planned downstream demand, planned purchase orders from the related intercompany vendors will be included in the plan as demand.</span></span>

## <a name="required-setup"></a><span data-ttu-id="e6e7f-117">Tarvittavat määritykset</span><span class="sxs-lookup"><span data-stu-id="e6e7f-117">Required setup</span></span>

<span data-ttu-id="e6e7f-118">Järjestelmä on valmisteltava konsernin sisäisen suunnittelun käyttöä varten seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-118">To use intercompany planning, you must prepare your system in the following way:</span></span>

1. <span data-ttu-id="e6e7f-119">Tarvittavat tuotteet on vapautettava kaikkiin tarvittaviin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-119">The relevant products must be released in all the relevant companies.</span></span> <span data-ttu-id="e6e7f-120">Lisätietoja on Microsoft Learnissa kohdassa [Konsernin sisäisen kaupan määrittäminen ja käyttäminen Dynamics 365 Supply Chain Managementissa](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).</span><span class="sxs-lookup"><span data-stu-id="e6e7f-120">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="e6e7f-121">Alapuolinen kysyntä on katettava ostoilla sellaiselta toimittajalta, jolla on konsernin sisäinen suhde yläpuoliseen yritykseen ja tarvittaviin oletusvarastodimensioihin (toimipaikka ja varasto) asiakkaalla.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-121">Downstream demand must be covered by purchases from a vendor that has an intercompany relation to the upstream company and relevant default inventory dimensions (site and warehouse) on the customer.</span></span> <span data-ttu-id="e6e7f-122">Lisätietoja on Microsoft Learnissa kohdassa [Konsernin sisäisen kaupan määrittäminen ja käyttäminen Dynamics 365 Supply Chain Managementissa](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/).</span><span class="sxs-lookup"><span data-stu-id="e6e7f-122">For more information, see [Configure and use intercompany trade in Dynamics 365 Supply Chain Management ](https://docs.microsoft.com/learn/modules/configure-use-intercompany-trade-dyn365-supply-chain-mgmt/) on Microsoft Learn.</span></span>
1. <span data-ttu-id="e6e7f-123">Yläpuolisen yrityksen pääsuunnitelman on sisällettävä suunniteltu alapuolinen kysyntä. Alapuolisissa suunnitelmissa on myös määritettävä tarvittava yritys ja pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-123">The master plan in the upstream company must include planned downstream demand, and the relevant company and master plan must be specified in the downstream plans.</span></span>

## <a name="include-planned-downstream-demand"></a><span data-ttu-id="e6e7f-124">Sisällytä suunniteltu tuotantovirran kysyntä</span><span class="sxs-lookup"><span data-stu-id="e6e7f-124">Include planned downstream demand</span></span>

<span data-ttu-id="e6e7f-125">Pääsuunnitelma määritetään sisältämään suunniteltu alapuolinen kysyntä seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-125">Follow these steps to configure your master plan so that it includes planned downstream demand.</span></span>

1. <span data-ttu-id="e6e7f-126">Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-126">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="e6e7f-127">Valitse tai luo pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-127">Select or create a master plan.</span></span>
1. <span data-ttu-id="e6e7f-128">Määritä **Konsernin sisäinen suunnittelu** -pikavälilehdessä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-128">On the **Intercompany planning** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="e6e7f-129">**Sisällytä suunniteltu alapuolinen kysyntä** – määritä asetukseksi *Kyllä*, jolloin konsernin sisäinen suunnittelu on käytössä pääsuunnitelmassa:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-129">**Include planned downstream demand** – Set this option to *Yes* to enable intercompany planning for the master plan.</span></span>
    - <span data-ttu-id="e6e7f-130">**Alapuoliset suunnitelmat** – jos **Sisällytä suunniteltu alapuolinen kysyntä** -asetukseksi on määritetty *Kyllä*, lisää muiden yritysten pääsuunnitelmia työkalurivin ja ruudukon avulla.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-130">**Downstream plans** – If you set the **Include planned downstream demand** option to *Yes*, use the toolbar and grid to add the desired master plans from other companies.</span></span>

## <a name="peg-across-companies-by-using-multilevel-pegging"></a><span data-ttu-id="e6e7f-131">Yritysten välinen tarvekohdistus monitasoisen tarvekohdistuksen avulla</span><span class="sxs-lookup"><span data-stu-id="e6e7f-131">Peg across companies by using multilevel pegging</span></span>

<span data-ttu-id="e6e7f-132">Monitasoisessa tarvekohdistuksessa yritysten välistä tarvekohdistusta tarkastelemalla nähdään toimituksen kattaman kysynnän alkuperäinen lähde:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-132">In multilevel pegging, you can view pegging across companies to see the initial source of demand that is being covered by a supply.</span></span>

<span data-ttu-id="e6e7f-133">Monitasoisen tarvekohdistuksen tietoja voi tarkastella seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e6e7f-133">To view multilevel pegging information, follow these steps.</span></span>

1. <span data-ttu-id="e6e7f-134">Valitse **Pääsuunnittelu \> Pääsuunnittelu \> Suunnitellut tilaukset**.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-134">Go to **Master planning \> Master planning \> Planned orders**.</span></span>
1. <span data-ttu-id="e6e7f-135">Valitse tai avaa suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-135">Select or open a planned order.</span></span>
1. <span data-ttu-id="e6e7f-136">Valitse sitten toimintoruudussa **Näytä**-välilehden **Tarpeet**-ryhmässä **Monitasoinen tarvekohdistus**.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-136">On the Action Pane, on the **View** tab, in the **Requirements** group, select **Multilevel pegging**.</span></span>

### <a name="intercompany-example-that-involves-two-companies"></a><span data-ttu-id="e6e7f-137">Kaksi konsernin sisäistä yritystä sisältävä esimerkki</span><span class="sxs-lookup"><span data-stu-id="e6e7f-137">Intercompany example that involves two companies</span></span>

<span data-ttu-id="e6e7f-138">Tässä esimerkissä suunniteltu tuotantotilaus luodaan USMF-yrityksessä kattamaan myyntitilaus DEMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-138">For this example, a planned production order is created in the USMF company to cover a sales order in the DEMF company.</span></span> <span data-ttu-id="e6e7f-139">USMF-yrityksessä suora kysyntä on suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-139">In USMF, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="e6e7f-140">Jotta tämä kysyntä näkyisi USMF-yrityksessä, pääsuunnittelu suoritetaan ensin DEMF- ja sitten USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-140">To make this demand appear in USMF, master planning is run first in DEMF and then in USMF.</span></span>

<span data-ttu-id="e6e7f-141">Seuraavassa kuvassa näkyy, miltä tämä esimerkki näyttäisi suunnittelun tuotantotilauksen **Monitasoinen tarvekohdistus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-141">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Kaksi konsernin sisäistä yritystä sisältävä esimerkki](media/IntercompanyPlanning1.png)

### <a name="intercompany-example-that-involves-three-companies"></a><span data-ttu-id="e6e7f-143">Kolme konsernin sisäistä yritystä sisältävä esimerkki</span><span class="sxs-lookup"><span data-stu-id="e6e7f-143">Intercompany example that involves three companies</span></span>

<span data-ttu-id="e6e7f-144">Tässä esimerkissä suunniteltu ostotilaus luodaan USMF-yrityksessä kattamaan myyntitilaus FRRT-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-144">For this example, a planned purchase order is created in the USMF company to cover a sales order in the FRRT company.</span></span> <span data-ttu-id="e6e7f-145">DEMF- ja USMF-yrityksissä suora kysyntä on suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-145">In the DEMF and USMF companies, the direct demand is planned intercompany demand.</span></span> <span data-ttu-id="e6e7f-146">Jotta tämä kysyntä näkyisi USMF-yrityksessä, pääsuunnittelu suoritetaan ensin FRRT-, sitten DEMF- ja lopulta USMF-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-146">To make this demand appear in USMF, master planning is run first in FRRT, then in DEMF, and finally in USMF.</span></span>

<span data-ttu-id="e6e7f-147">Seuraavassa kuvassa näkyy, miltä tämä esimerkki näyttäisi suunnittelun tuotantotilauksen **Monitasoinen tarvekohdistus** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e6e7f-147">The following illustration shows how this example might appear on the **Multilevel pegging** page for the planned production order.</span></span>

![Kolme konsernin sisäistä yritystä sisältävä esimerkki](media/IntercompanyPlanning2.png)
