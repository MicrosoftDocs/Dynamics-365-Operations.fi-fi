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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993650"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="45f5e-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-103">Warehouse set up</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="45f5e-104">Tässä ohjeaiheessa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="45f5e-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="45f5e-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="45f5e-105">Overview</span></span>

<span data-ttu-id="45f5e-106">Jokaiseen Commerce-kanavaan on liitettävä määritetty varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-106">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="45f5e-107">Seuraavilla menetelmillä tehdään määritykset, jotka vähintään tarvitaan Commerce-kanavan varaston määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="45f5e-107">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="45f5e-108">Lisätietoja varaston määrittämisestä on kohdassa [Varastonhallinnan yleiskatsaus](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="45f5e-108">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="45f5e-109">Varaston toimipaikan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-109">Configure a warehouse site</span></span>

<span data-ttu-id="45f5e-110">Ennen varaston määrittämistä on määritettävä varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="45f5e-110">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="45f5e-111">Varaston toimipaikka määritetään noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="45f5e-111">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="45f5e-112">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Toimipaikat**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-112">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="45f5e-113">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="45f5e-114">Anna **Toimipaikka**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="45f5e-114">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="45f5e-115">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="45f5e-115">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="45f5e-116">Määritä **Yleiset**-osassa sopiva **Aikavyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-116">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="45f5e-117">Anna osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="45f5e-117">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="45f5e-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="45f5e-119">Seuraavassa kuvassa on esimerkki varaston toimipaikasta.</span><span class="sxs-lookup"><span data-stu-id="45f5e-119">The following image shows an example warehouse site.</span></span>

![Esimerkki varaston toimipaikasta](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="45f5e-121">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-121">Set up a warehouse</span></span>

<span data-ttu-id="45f5e-122">Voit määrittää varaston seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-122">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="45f5e-123">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-123">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="45f5e-124">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-124">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="45f5e-125">Anna **Varasto**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="45f5e-125">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="45f5e-126">Jos tämä on myymälän 1:1-vastaavuus, voit käyttää myymälän nimeä tai alueellisen jakelukeskuksen nimeä.</span><span class="sxs-lookup"><span data-stu-id="45f5e-126">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="45f5e-127">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="45f5e-127">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="45f5e-128">Valitse avattavassa **Toimipaikka**-luettelossa aiemmin luotu varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="45f5e-128">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="45f5e-129">Valitse **Tyyppi**-kentässä **Oletus**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-129">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="45f5e-130">Jos haluat määrittää **karanteenivaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Karanteeni**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-130">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="45f5e-131">Jos haluat määrittää **siirtovaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Siirto**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-131">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="45f5e-132">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-132">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="45f5e-133">Määritä varastokäytävät</span><span class="sxs-lookup"><span data-stu-id="45f5e-133">Set up inventory aisles</span></span>

<span data-ttu-id="45f5e-134">Voit määrittää varastokäytävät noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="45f5e-134">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="45f5e-135">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Sijainnin asetukset \> Varastokäytävät**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-135">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="45f5e-136">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="45f5e-137">Valitse avattavassa **Varasto**-luettelossa aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-137">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="45f5e-138">Anna **Käytävä**-kentässä nimi (kuten Olet).</span><span class="sxs-lookup"><span data-stu-id="45f5e-138">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="45f5e-139">Anna **Nimi**-kentässä nimi (kuten Oletuskäytävä).</span><span class="sxs-lookup"><span data-stu-id="45f5e-139">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="45f5e-140">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-140">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="45f5e-141">Määritä varaston varastosijainnit</span><span class="sxs-lookup"><span data-stu-id="45f5e-141">Set up warehouse inventory locations</span></span>

<span data-ttu-id="45f5e-142">Voit määrittää varaston varastosijainnit standardivarastolle, vaurioituneelle varastolle ja palautetulle varastolle seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-142">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="45f5e-143">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-143">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="45f5e-144">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-144">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="45f5e-145">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-145">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="45f5e-146">Valitse toimintoruudussa **Varasto** ja valitse sitten **Varastosijainti**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-146">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="45f5e-147">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-147">On the action pane, select **New**.</span></span> <span data-ttu-id="45f5e-148">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-148">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="45f5e-149">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="45f5e-149">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="45f5e-150">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="45f5e-150">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="45f5e-151">Anna **Sijainti**-ruudussa varaston nimi.</span><span class="sxs-lookup"><span data-stu-id="45f5e-151">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="45f5e-152">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-152">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="45f5e-153">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-153">On the action pane, select **New**.</span></span>  <span data-ttu-id="45f5e-154">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-154">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="45f5e-155">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="45f5e-155">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="45f5e-156">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="45f5e-156">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="45f5e-157">Kirjoita **Sijainti**-ruutuun Vaurioitunut.</span><span class="sxs-lookup"><span data-stu-id="45f5e-157">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="45f5e-158">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-158">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="45f5e-159">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-159">On the action pane, select **New**.</span></span>  <span data-ttu-id="45f5e-160">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-160">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="45f5e-161">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="45f5e-161">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="45f5e-162">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="45f5e-162">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="45f5e-163">Kirjoita **Sijainti**-ruutuun Palautukset.</span><span class="sxs-lookup"><span data-stu-id="45f5e-163">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="45f5e-164">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-164">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="45f5e-165">Seuraavassa kuvassa on San Franciscon varaston varastosijaintiasetukset.</span><span class="sxs-lookup"><span data-stu-id="45f5e-165">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Esimerkki varastosijainnin asetuksista](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="45f5e-167">Varaston määrityksen viimeistely</span><span class="sxs-lookup"><span data-stu-id="45f5e-167">Complete warehouse setup</span></span>

<span data-ttu-id="45f5e-168">Viimeiste varaston määritys noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="45f5e-168">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="45f5e-169">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-169">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="45f5e-170">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="45f5e-170">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="45f5e-171">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-171">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="45f5e-172">**Varastonhallinta**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="45f5e-172">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="45f5e-173">Määritä **Oletusvastaanottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-173">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="45f5e-174">Määritä **Oletusvarasto-ottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-174">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="45f5e-175">Anna varaston osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="45f5e-175">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="45f5e-176">**Vähittäismyynti**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="45f5e-176">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="45f5e-177">Anna **Oletuspalautussijainti**-ruudussa aiemmin luotu palautussijainti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-177">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="45f5e-178">Määritä **Myymälä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-178">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="45f5e-179">Määritä **Paino**-asetukseksi **1,00**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-179">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="45f5e-180">Anna **Varastodimensiot**-ruudussa aiemmin luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="45f5e-180">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="45f5e-181">Määritä **Varasto**-osassa **Fyysinen negatiivinen varasto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-181">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="45f5e-182">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="45f5e-182">On the action pane, select **Save**.</span></span>

<span data-ttu-id="45f5e-183">Seuraavassa kuvassa on määritetyn varaston tiedot.</span><span class="sxs-lookup"><span data-stu-id="45f5e-183">The following image shows details for a configured warehouse.</span></span>

![Esimerkki määritetystä varastosta](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="45f5e-185">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="45f5e-185">Additional resources</span></span>

[<span data-ttu-id="45f5e-186">Varastonhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="45f5e-186">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="45f5e-187">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="45f5e-187">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="45f5e-188">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="45f5e-188">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="45f5e-189">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-189">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="45f5e-190">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-190">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="45f5e-191">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="45f5e-191">Set up a call center channel</span></span>](channel-setup-callcenter.md)





