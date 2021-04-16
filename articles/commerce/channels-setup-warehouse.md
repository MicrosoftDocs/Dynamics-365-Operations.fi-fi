---
title: Varaston määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 154ec719e16e4826b0e24deb5ecadf587d938e3c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800492"
---
# <a name="warehouse-set-up"></a><span data-ttu-id="dbe69-103">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-103">Warehouse set up</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dbe69-104">Tässä ohjeaiheessa käsitellään uuden kanavan kanssa käytettävän varaston määrittämistä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="dbe69-104">This topic describes how to set up a warehouse to be used with a new channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dbe69-105">Jokaiseen Commerce-kanavaan on liitettävä määritetty varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-105">Each Commerce channel requires a configured warehouse to be associated with it.</span></span> <span data-ttu-id="dbe69-106">Seuraavilla menetelmillä tehdään määritykset, jotka vähintään tarvitaan Commerce-kanavan varaston määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="dbe69-106">The following procedures provide the minimum configuration required to set up a warehouse for a Commerce channel.</span></span> <span data-ttu-id="dbe69-107">Lisätietoja varaston määrittämisestä on kohdassa [Varastonhallinnan yleiskatsaus](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="dbe69-107">For more information regarding warehouse setup, please see the [Warehouse management overview](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="configure-a-warehouse-site"></a><span data-ttu-id="dbe69-108">Varaston toimipaikan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-108">Configure a warehouse site</span></span>

<span data-ttu-id="dbe69-109">Ennen varaston määrittämistä on määritettävä varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="dbe69-109">Before setting up a warehouse, you need to configure a warehouse site.</span></span>

<span data-ttu-id="dbe69-110">Varaston toimipaikka määritetään noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="dbe69-110">To configure a warehouse site, follow these steps.</span></span>

1. <span data-ttu-id="dbe69-111">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Toimipaikat**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Sites**.</span></span>
1. <span data-ttu-id="dbe69-112">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dbe69-113">Anna **Toimipaikka**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dbe69-113">In the **Site** field, enter a value.</span></span>
1. <span data-ttu-id="dbe69-114">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="dbe69-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="dbe69-115">Määritä **Yleiset**-osassa sopiva **Aikavyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-115">In the **General** section, set the appropriate **Time zone**.</span></span>
1. <span data-ttu-id="dbe69-116">Anna osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="dbe69-116">In the **Addresses** section, enter an address.</span></span>
1. <span data-ttu-id="dbe69-117">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-117">On the action pane, select **Save**.</span></span>

<span data-ttu-id="dbe69-118">Seuraavassa kuvassa on esimerkki varaston toimipaikasta.</span><span class="sxs-lookup"><span data-stu-id="dbe69-118">The following image shows an example warehouse site.</span></span>

![Esimerkki varaston toimipaikasta](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a><span data-ttu-id="dbe69-120">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-120">Set up a warehouse</span></span>

<span data-ttu-id="dbe69-121">Voit määrittää varaston seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-121">To set up a warehouse, follow these steps.</span></span>

1. <span data-ttu-id="dbe69-122">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-122">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="dbe69-123">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-123">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dbe69-124">Anna **Varasto**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="dbe69-124">In the **Warehouse** field, enter a value.</span></span>  <span data-ttu-id="dbe69-125">Jos tämä on myymälän 1:1-vastaavuus, voit käyttää myymälän nimeä tai alueellisen jakelukeskuksen nimeä.</span><span class="sxs-lookup"><span data-stu-id="dbe69-125">If this is a 1:1 mapping to a store, consider using the store name or the name of a regional distribution center.</span></span>
1. <span data-ttu-id="dbe69-126">Anna **Nimi**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="dbe69-126">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="dbe69-127">Valitse avattavassa **Toimipaikka**-luettelossa aiemmin luotu varaston toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="dbe69-127">In the **Site** drop-down list, select the warehouse site created previously.</span></span>
1. <span data-ttu-id="dbe69-128">Valitse **Tyyppi**-kentässä **Oletus**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-128">In the **Type** field, select **Default**.</span></span>
    - <span data-ttu-id="dbe69-129">Jos haluat määrittää **karanteenivaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Karanteeni**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-129">If you want to set a **Quarantine warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Quarantine**.</span></span>
    - <span data-ttu-id="dbe69-130">Jos haluat määrittää **siirtovaraston**, ensin on luotava näiden ohjeiden mukaan lisävarasto, jossa **Tyyppi**-asetuksena on **Siirto**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-130">If you want to set a **Transit warehouse**, first you'll need to follow these steps to create an additional warehouse where the **Type** is set to **Transit**.</span></span>
1. <span data-ttu-id="dbe69-131">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-131">On the action pane, select **Save**.</span></span>

## <a name="set-up-inventory-aisles"></a><span data-ttu-id="dbe69-132">Määritä varastokäytävät</span><span class="sxs-lookup"><span data-stu-id="dbe69-132">Set up inventory aisles</span></span>

<span data-ttu-id="dbe69-133">Voit määrittää varastokäytävät noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="dbe69-133">To set up inventory aisles, follow these steps.</span></span>

1. <span data-ttu-id="dbe69-134">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Sijainnin asetukset \> Varastokäytävät**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-134">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Location setup \> Inventory aisles**.</span></span>
1. <span data-ttu-id="dbe69-135">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-135">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dbe69-136">Valitse avattavassa **Varasto**-luettelossa aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-136">In the **Warehouse** drop-down list, select the warehouse created previously.</span></span>
1. <span data-ttu-id="dbe69-137">Anna **Käytävä**-kentässä nimi (kuten Olet).</span><span class="sxs-lookup"><span data-stu-id="dbe69-137">In the **Aisle** field, enter a name (for example, "Def").</span></span>
1. <span data-ttu-id="dbe69-138">Anna **Nimi**-kentässä nimi (kuten Oletuskäytävä).</span><span class="sxs-lookup"><span data-stu-id="dbe69-138">In the **Name** field, enter a name (for example, "Default aisle").</span></span>
1. <span data-ttu-id="dbe69-139">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-139">On the action pane, select **Save**.</span></span>

## <a name="set-up-warehouse-inventory-locations"></a><span data-ttu-id="dbe69-140">Määritä varaston varastosijainnit</span><span class="sxs-lookup"><span data-stu-id="dbe69-140">Set up warehouse inventory locations</span></span>

<span data-ttu-id="dbe69-141">Voit määrittää varaston varastosijainnit standardivarastolle, vaurioituneelle varastolle ja palautetulle varastolle seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-141">To set up warehouse inventory locations for standard, damaged, and returned inventory, follow these steps.</span></span>

1. <span data-ttu-id="dbe69-142">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-142">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="dbe69-143">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-143">Select the warehouse you created previously.</span></span>
1. <span data-ttu-id="dbe69-144">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-144">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="dbe69-145">Valitse toimintoruudussa **Varasto** ja valitse sitten **Varastosijainti**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-145">On the action pane, select **Warehouse**, and then select **Inventory location**.</span></span>
1. <span data-ttu-id="dbe69-146">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-146">On the action pane, select **New**.</span></span> <span data-ttu-id="dbe69-147">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-147">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="dbe69-148">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="dbe69-148">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="dbe69-149">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="dbe69-149">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="dbe69-150">Anna **Sijainti**-ruudussa varaston nimi.</span><span class="sxs-lookup"><span data-stu-id="dbe69-150">In the **Location** box, enter the name of the warehouse.</span></span>
    1. <span data-ttu-id="dbe69-151">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-151">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="dbe69-152">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-152">On the action pane, select **New**.</span></span>  <span data-ttu-id="dbe69-153">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-153">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="dbe69-154">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="dbe69-154">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span>  
    1. <span data-ttu-id="dbe69-155">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="dbe69-155">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="dbe69-156">Kirjoita **Sijainti**-ruutuun Vaurioitunut.</span><span class="sxs-lookup"><span data-stu-id="dbe69-156">In the **Location** box, enter "Damaged".</span></span>
    1. <span data-ttu-id="dbe69-157">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-157">On the action pane, select **Save**.</span></span>
 1. <span data-ttu-id="dbe69-158">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-158">On the action pane, select **New**.</span></span>  <span data-ttu-id="dbe69-159">Avattavan **Varasto**-luettelon oletusarvona pitäisi olla uusi varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-159">The **Warehouse** drop-down list should default to your new warehouse.</span></span>
    1. <span data-ttu-id="dbe69-160">Anna **Käytävä**-ruutuun aiemmin määritetyn käytävän nimi.</span><span class="sxs-lookup"><span data-stu-id="dbe69-160">In the **Aisle** box, enter the name of the aisle you specified earlier.</span></span> 
    1. <span data-ttu-id="dbe69-161">Määritä **Manuaalinen päivitys** -asetukseksi **Kyllä**</span><span class="sxs-lookup"><span data-stu-id="dbe69-161">Set **Manual update** to **Yes**</span></span>
    1. <span data-ttu-id="dbe69-162">Kirjoita **Sijainti**-ruutuun Palautukset.</span><span class="sxs-lookup"><span data-stu-id="dbe69-162">In the **Location** box, enter "Returns".</span></span>
    1. <span data-ttu-id="dbe69-163">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-163">On the action pane, select **Save**.</span></span>
    
<span data-ttu-id="dbe69-164">Seuraavassa kuvassa on San Franciscon varaston varastosijaintiasetukset.</span><span class="sxs-lookup"><span data-stu-id="dbe69-164">The following image shows a San Francisco warehouse inventory location setup.</span></span>

![Esimerkki varastosijainnin asetuksista](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a><span data-ttu-id="dbe69-166">Varaston määrityksen viimeistely</span><span class="sxs-lookup"><span data-stu-id="dbe69-166">Complete warehouse setup</span></span>

<span data-ttu-id="dbe69-167">Viimeiste varaston määritys noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="dbe69-167">To complete warehouse setup, follow these steps.</span></span>

1. <span data-ttu-id="dbe69-168">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan määritys \> Varastot**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-168">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Warehouses**.</span></span>
1. <span data-ttu-id="dbe69-169">Valitse aiemmin luotu varasto.</span><span class="sxs-lookup"><span data-stu-id="dbe69-169">Select the warehouse you previously created.</span></span>
1. <span data-ttu-id="dbe69-170">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-170">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="dbe69-171">**Varastonhallinta**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="dbe69-171">Under **Inventory and warehouse management**:</span></span>
    1. <span data-ttu-id="dbe69-172">Määritä **Oletusvastaanottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-172">Set **Default receipt location** to the default location created above.</span></span>
    1. <span data-ttu-id="dbe69-173">Määritä **Oletusvarasto-ottosijainti**-asetukseksi edellä luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-173">Select **Default issue location** to the default location created above.</span></span>
1. <span data-ttu-id="dbe69-174">Anna varaston osoite **Osoitteet**-osassa.</span><span class="sxs-lookup"><span data-stu-id="dbe69-174">Under the **Addresses** section, enter a warehouse address.</span></span>
1. <span data-ttu-id="dbe69-175">**Vähittäismyynti**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="dbe69-175">Under the **Retail** section:</span></span> 
    1. <span data-ttu-id="dbe69-176">Anna **Oletuspalautussijainti**-ruudussa aiemmin luotu palautussijainti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-176">In the **Default return location** box, enter the returns location created previously.</span></span>
    1. <span data-ttu-id="dbe69-177">Määritä **Myymälä**-asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-177">Set **Store** to **Yes**.</span></span>
    1. <span data-ttu-id="dbe69-178">Määritä **Paino**-asetukseksi **1,00**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-178">Set **Weight** to **1.00**.</span></span> 
    1. <span data-ttu-id="dbe69-179">Anna **Varastodimensiot**-ruudussa aiemmin luotu oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="dbe69-179">In the **Storage Dimensions** box, enter the default location created previously.</span></span>
1. <span data-ttu-id="dbe69-180">Määritä **Varasto**-osassa **Fyysinen negatiivinen varasto** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-180">Under the **Warehouse** section, set **Physical negative inventory** to **Yes**.</span></span>
1. <span data-ttu-id="dbe69-181">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dbe69-181">On the action pane, select **Save**.</span></span>

<span data-ttu-id="dbe69-182">Seuraavassa kuvassa on määritetyn varaston tiedot.</span><span class="sxs-lookup"><span data-stu-id="dbe69-182">The following image shows details for a configured warehouse.</span></span>

![Esimerkki määritetystä varastosta](media/warehouse-sample.png)

## <a name="additional-resources"></a><span data-ttu-id="dbe69-184">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="dbe69-184">Additional resources</span></span>

[<span data-ttu-id="dbe69-185">Varastonhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dbe69-185">Warehouse management overview</span></span>](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="dbe69-186">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="dbe69-186">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="dbe69-187">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="dbe69-187">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="dbe69-188">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-188">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="dbe69-189">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-189">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="dbe69-190">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="dbe69-190">Set up a call center channel</span></span>](channel-setup-callcenter.md)







[!INCLUDE[footer-include](../includes/footer-banner.md)]
