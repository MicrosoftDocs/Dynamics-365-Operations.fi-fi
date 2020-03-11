---
title: Varaston määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9ba12876a8c8f841733d8ec49c33e900211c4ab4
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057853"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="f8dc2-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f8dc2-104">Tässä ohjeaiheessa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8dc2-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f8dc2-105">Overview</span></span>

<span data-ttu-id="f8dc2-106">Jokaiseen Commerce-kanavaan on liitettävä määritetty varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="f8dc2-107">Seuraavilla menetelmillä tehdään määritykset, jotka vähintään tarvitaan Commerce-kanavan varaston määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="f8dc2-108">Lisätietoja varaston määrittämisestä on kohdassa [Varastonhallinnan yleiskatsaus](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span><span class="sxs-lookup"><span data-stu-id="f8dc2-108">For more information regarding warehouse setup, please see the [Warehouse management overview](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="f8dc2-109">Varaston toimipaikan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-109">Configure a warehouse site</span></span>

<span data-ttu-id="f8dc2-110">Ennen varaston määrittämistä on määritettävä varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="f8dc2-111">Varaston toimipaikka määritetään noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="f8dc2-112">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Toimipaikat**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="f8dc2-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f8dc2-114">Anna **Toimipaikka**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="f8dc2-115">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f8dc2-116">Määritä **Yleiset**-osassa sopiva **Aikavyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="f8dc2-117">Anna osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="f8dc2-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f8dc2-119">Seuraavassa kuvassa on esimerkki varaston toimipaikasta.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-119">The following image shows an example warehouse site.</span></span>

![Esimerkki varaston toimipaikasta](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="f8dc2-121">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-121">Set up a warehouse</span></span>

<span data-ttu-id="f8dc2-122">Voit määrittää varaston seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="f8dc2-123">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="f8dc2-124">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f8dc2-125">Anna **Varasto**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="f8dc2-126">Jos tämä on myymälän 1:1-vastaavuus, voit käyttää myymälän nimeä tai alueellisen jakelukeskuksen nimeä.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="f8dc2-127">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="f8dc2-128">Valitse avattavassa **Toimipaikka**-luettelossa aiemmin luotu varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="f8dc2-129">Valitse **Tyyppi**-kentässä **Oletus**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="f8dc2-130">Jos haluat määrittää **karanteenivaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Karanteeni**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="f8dc2-131">Jos haluat määrittää **siirtovaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Siirto**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="f8dc2-132">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="f8dc2-133">Määritä varastokäytävät</span><span class="sxs-lookup"><span data-stu-id="f8dc2-133">Set up inventory aisles</span></span>

<span data-ttu-id="f8dc2-134">Voit määrittää varastokäytävät noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="f8dc2-135">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Sijainnin asetukset \> Varastokäytävät**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="f8dc2-136">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="f8dc2-137">Valitse avattavassa **Varasto**-luettelossa aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="f8dc2-138">Anna **Käytävä**-kentässä nimi (kuten Olet).</span><span class="sxs-lookup"><span data-stu-id="f8dc2-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="f8dc2-139">Anna **Nimi**-kentässä nimi (kuten Oletuskäytävä).</span><span class="sxs-lookup"><span data-stu-id="f8dc2-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="f8dc2-140">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="f8dc2-141">Määritä varaston varastosijainnit</span><span class="sxs-lookup"><span data-stu-id="f8dc2-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="f8dc2-142">Voit määrittää varaston varastosijainnit standardivarastolle, vaurioituneelle varastolle ja palautetulle varastolle seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="f8dc2-143">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="f8dc2-144">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="f8dc2-145">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="f8dc2-146">Valitse toimintoruudussa **Varasto** ja valitse sitten **Varastosijainti**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="f8dc2-147">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-147">On the action pane, select **New**.</span></span> <span data-ttu-id="f8dc2-148">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="f8dc2-149">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="f8dc2-150">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="f8dc2-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="f8dc2-151">Anna **Sijainti**-ruudussa varaston nimi.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="f8dc2-152">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="f8dc2-153">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="f8dc2-154">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="f8dc2-155">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="f8dc2-156">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="f8dc2-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="f8dc2-157">Kirjoita **Sijainti**-ruutuun Vaurioitunut.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="f8dc2-158">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="f8dc2-159">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="f8dc2-160">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="f8dc2-161">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="f8dc2-162">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="f8dc2-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="f8dc2-163">Kirjoita **Sijainti**-ruutuun Palautukset.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="f8dc2-164">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="f8dc2-165">Seuraavassa kuvassa on San Franciscon varaston varastosijaintiasetukset.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Esimerkki varastosijainnin asetuksista](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="f8dc2-167">Varaston määrityksen viimeistely</span><span class="sxs-lookup"><span data-stu-id="f8dc2-167">Complete warehouse setup</span></span>

<span data-ttu-id="f8dc2-168">Viimeiste varaston määritys noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="f8dc2-169">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="f8dc2-170">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="f8dc2-171">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="f8dc2-172">**Varastonhallinta**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="f8dc2-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="f8dc2-173">Määritä **Oletusvastaanottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="f8dc2-174">Määritä **Oletusvarasto-ottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="f8dc2-175">Anna varaston osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="f8dc2-176">**Vähittäismyynti**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="f8dc2-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="f8dc2-177">Anna **Oletuspalautussijainti**-ruudussa aiemmin luotu palautussijainti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="f8dc2-178">Määritä **Myymälä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="f8dc2-179">Määritä **Paino**-asetukseksi **1,00**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="f8dc2-180">Anna **Varastodimensiot**-ruudussa aiemmin luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="f8dc2-181">Määritä **Varasto**-osassa **Fyysinen negatiivinen varasto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="f8dc2-182">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="f8dc2-183">Seuraavassa kuvassa on määritetyn varaston tiedot.</span><span class="sxs-lookup"><span data-stu-id="f8dc2-183">The following image shows details for a configured warehouse.</span></span>

![Esimerkki määritetystä varastosta](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="f8dc2-185">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f8dc2-185">Additional resources</span></span>

[<span data-ttu-id="f8dc2-186">Varastonhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f8dc2-186">Warehouse management overview</span></span>](https://docs.microsoft.com/en-us/dynamics365/supply-chain/warehousing/warehouse-management-overview)

[<span data-ttu-id="f8dc2-187">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f8dc2-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="f8dc2-188">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="f8dc2-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="f8dc2-189">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="f8dc2-190">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="f8dc2-191">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f8dc2-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





