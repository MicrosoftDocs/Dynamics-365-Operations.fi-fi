---
title: Resurssien hallinnan integraatio käyttöomaisuuteen
description: Tässä ohjeaiheessa selitetään, miten käyttöomaisuus ja käyttöomaisuusmoduulit integroidaan toisiinsa, jotta käyttöomaisuus voidaan linkittää kunnossapitoon.
author: kamaybac
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: cdda44d361011706fe0ba170309908533aa0c2f7
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2020
ms.locfileid: "3276913"
---
# <a name="integrate-asset-management-with-fixed-assets"></a><span data-ttu-id="44cf1-103">Resurssien hallinnan integraatio käyttöomaisuuteen</span><span class="sxs-lookup"><span data-stu-id="44cf1-103">Integrate asset management with fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="44cf1-104">Integroimalla **resurssinhallinta**- ja **käyttöomaisuus**-moduulit toisiinsa käyttöomaisuus voidaan linkittää kunnossapitoon.</span><span class="sxs-lookup"><span data-stu-id="44cf1-104">By integrating the **Asset management** and **Fixed assets** modules, you can link fixed assets with maintenance assets.</span></span> <span data-ttu-id="44cf1-105">Käyttöomaisuuden käyttäjät voivat sitten luoda kunnossapitoresurssin uudesta tai aiemmin luodusta käyttöomaisuudesta, ja käyttöomaisuuden hallinnan käyttäjät voivat liittää ylläpito-omaisuuden olemassa olevaan käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="44cf1-105">Fixed assets users can then create a maintenance asset from a new or existing fixed asset, and Asset management users can associate a maintenance asset with an existing fixed asset.</span></span> <span data-ttu-id="44cf1-106">Tämän toiminnon avulla käyttöomaisuuden käyttäjät voivat myös helposti tarkastella kustannuksia, jotka kirjattiin liittyvien kunnossapitoresurssien työtilauksista.</span><span class="sxs-lookup"><span data-stu-id="44cf1-106">This feature also makes it easy for Fixed assets users to view the costs that were posted from work orders for related maintenance assets.</span></span>

> [!NOTE]
> <span data-ttu-id="44cf1-107">Tässä ohjeaiheessa *ylläpidettävät resurssit* viittaavat **resurssinhallinta**-moduulin ja *käyttöomaisuus* viittaa **käyttöomaisuus**-moduulin varoihin.</span><span class="sxs-lookup"><span data-stu-id="44cf1-107">In this topic, *maintenance assets* refer to assets from the **Asset management** module, and *fixed assets* refer to assets from the **Fixed assets** module.</span></span>

## <a name="set-a-default-location-for-new-maintenance-assets-that-are-created-from-fixed-assets-optional"></a><span data-ttu-id="44cf1-108">Käyttöomaisuuden luomien uusien kunnossapitoresurssien oletussijainnin määrittäminen (valinnainen)</span><span class="sxs-lookup"><span data-stu-id="44cf1-108">Set a default location for new maintenance assets that are created from fixed assets (optional)</span></span>

<span data-ttu-id="44cf1-109">Tämän valinnaisen kokoonpanon avulla voit asettaa oletustoiminnallisen sijainnin uusille ylläpidettäville resursseille, jotka luodaan käyttöomaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="44cf1-109">This optional configuration lets you set a default functional location for new maintenance assets that are created from fixed assets.</span></span> <span data-ttu-id="44cf1-110">Tämä konfiguraatio on tavallisesti suoritettava vain kerran, jos suoritat sen loppuun.</span><span class="sxs-lookup"><span data-stu-id="44cf1-110">You typically complete this configuration this just one time, if you complete it at all.</span></span>

<span data-ttu-id="44cf1-111">Voit tehdä määrityksen noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="44cf1-111">To complete the configuration, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-112">Siirry kohtaan **Resurssinhallinta \> Asetukset \> Resurssinhallinnan parametrit**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-112">Go to **Asset management \> Setup \> Asset management parameters**.</span></span>
1. <span data-ttu-id="44cf1-113">Valitse **Käyttöomaisuus**-välilehden **Toiminnallinen sijainti** -kentässä valmiille tuotteille käytettävä oletussijainti.</span><span class="sxs-lookup"><span data-stu-id="44cf1-113">On the **Fixed assets** tab, in the **Functional location** field, select the default location.</span></span>
1. <span data-ttu-id="44cf1-114">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-114">On the Action Pane, select **Save**.</span></span>

## <a name="work-with-integrated-maintenance-assets-and-fixed-assets"></a><span data-ttu-id="44cf1-115">Integroitujen ylläpito- ja käyttöomaisuuden käsitteleminen</span><span class="sxs-lookup"><span data-stu-id="44cf1-115">Work with integrated maintenance assets and fixed assets</span></span>

<span data-ttu-id="44cf1-116">Tässä osassa on toimintosarja, jossa on erilaisia tapoja, joilla voit käsitellä integroituja resurssinhallinta- ja käyttöomaisuustoimintoja.</span><span class="sxs-lookup"><span data-stu-id="44cf1-116">This section provides a collection of procedures that show various ways that you can work with the integrated Asset management and Fixed assets features.</span></span>

### <a name="associate-an-existing-maintenance-asset-with-a-fixed-asset"></a><span data-ttu-id="44cf1-117">Aiemmin luodun ylläpidettävän resurssin yhdistäminen käyttöomaisuuserään</span><span class="sxs-lookup"><span data-stu-id="44cf1-117">Associate an existing maintenance asset with a fixed asset</span></span>

<span data-ttu-id="44cf1-118">Seuraa näitä ohjeita yhdistääksesi aiemmin luodun ylläpidettävän resurssin käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="44cf1-118">To associate an existing maintenance asset with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-119">Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).</span><span class="sxs-lookup"><span data-stu-id="44cf1-119">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="44cf1-120">Valitse resurssi.</span><span class="sxs-lookup"><span data-stu-id="44cf1-120">Select an asset.</span></span>
1. <span data-ttu-id="44cf1-121">Valitse **Käyttöomaisuus** -pikavälilehden **Käyttöomaisuuserän numero** -kentässä aiemmin luotu käyttöomaisuuserä.</span><span class="sxs-lookup"><span data-stu-id="44cf1-121">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select an existing fixed asset.</span></span>
1. <span data-ttu-id="44cf1-122">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-122">On the Action Pane, select **Save**.</span></span>

### <a name="view-the-fixed-asset-that-is-associated-with-a-selected-maintenance-asset"></a><span data-ttu-id="44cf1-123">Näytä valittuun ylläpidettävä resurssiin liittyvä käyttöomaisuuserä</span><span class="sxs-lookup"><span data-stu-id="44cf1-123">View the fixed asset that is associated with a selected maintenance asset</span></span>

<span data-ttu-id="44cf1-124">Seuraa näitä ohjeita näyttääksesi käyttöomaisuuserän, joka liittyy valittuun ylläpidettävään resurssiin.</span><span class="sxs-lookup"><span data-stu-id="44cf1-124">To view the fixed asset that is associated with a selected maintenance asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-125">Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).</span><span class="sxs-lookup"><span data-stu-id="44cf1-125">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="44cf1-126">Valitse resurssi.</span><span class="sxs-lookup"><span data-stu-id="44cf1-126">Select an asset.</span></span>
1. <span data-ttu-id="44cf1-127">Valitse linkki **Käyttöomaisuus** -pikavälilehden **Käyttöomaisuuserän numero** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="44cf1-127">On the **Fixed asset** FastTab, in the **Fixed asset number** field, select the link.</span></span>

    <span data-ttu-id="44cf1-128">Valitun resurssin **käyttöomaisuus**-sivu avataan.</span><span class="sxs-lookup"><span data-stu-id="44cf1-128">The **Fixed assets** page for the selected asset is opened.</span></span> <span data-ttu-id="44cf1-129">( Tämä sivu löytyy yleensä kohdasta **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.)</span><span class="sxs-lookup"><span data-stu-id="44cf1-129">(Typically, this page is found at **Fixed assets \> Fixed assets \> Fixed assets**.)</span></span>

### <a name="view-the-maintenance-asset-that-is-associated-with-a-selected-fixed-asset"></a><span data-ttu-id="44cf1-130">Näytä valittuun käyttöomaisuuserään liittyvä ylläpidettävä resurssi</span><span class="sxs-lookup"><span data-stu-id="44cf1-130">View the maintenance asset that is associated with a selected fixed asset</span></span>

<span data-ttu-id="44cf1-131">Seuraa näitä ohjeita näyttääksesi ylläpidettävän resurssin, joka liittyy valittuun käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="44cf1-131">To view the maintenance asset that is associated with a selected fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-132">Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-132">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="44cf1-133">Valitse resurssi.</span><span class="sxs-lookup"><span data-stu-id="44cf1-133">Select an asset.</span></span>
1. <span data-ttu-id="44cf1-134">Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Näytä**-ryhmässä **Ylläpidettävä resurssi**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-134">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance asset**.</span></span>

    <span data-ttu-id="44cf1-135">**Ylläpidettävä resurssi** -sivu, joka liittyy valittuun käyttöomaisuuserään, avataan.</span><span class="sxs-lookup"><span data-stu-id="44cf1-135">The **Maintenance asset** page for the asset that is associated with the selected fixed asset is opened.</span></span> <span data-ttu-id="44cf1-136">(Yleensä tämä sivu löytyy kohdasta **Resurssinhallinta \> Resurssit \> Kaikki resurssit**.)</span><span class="sxs-lookup"><span data-stu-id="44cf1-136">(Typically, this page is found at **Asset management \> Assets \> All assets**.)</span></span>

### <a name="view-maintenance-costs-that-are-associated-with-a-fixed-asset"></a><span data-ttu-id="44cf1-137">Käyttöomaisuuteen liittyvien ylläpitokustannusten tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="44cf1-137">View maintenance costs that are associated with a fixed asset</span></span>

<span data-ttu-id="44cf1-138">Käyttöomaisuuden hallinnan työtilauksia voi kirjata ylläpidettävään resurssiin, ja kullakin näistä työtilauksista on yleensä kustannus.</span><span class="sxs-lookup"><span data-stu-id="44cf1-138">Asset management work orders can be posted for maintenance assets, and each of those work orders typically has a cost.</span></span> <span data-ttu-id="44cf1-139">Kun käyttöomaisuuserä liitetään ylläpidettävään resurssiin, voit tarkastella siihen liittyviä kustannuksia suoraan käyttöomaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="44cf1-139">When a fixed asset is associated with a maintenance asset, you can go directly from the fixed asset to view the related costs.</span></span>

<span data-ttu-id="44cf1-140">Seuraa näitä ohjeita näyttääksesi ylläpitokustannukset, jotka liittyvät käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="44cf1-140">To view the maintenance costs that are associated with a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-141">Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-141">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="44cf1-142">Valitse resurssi.</span><span class="sxs-lookup"><span data-stu-id="44cf1-142">Select an asset.</span></span>
1. <span data-ttu-id="44cf1-143">Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Näytä**-ryhmässä **Ylläpitokustannukset**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-143">On the Action Pane, on the **Asset management** tab, in the **View** group, select **Maintenance cost**.</span></span>

    <span data-ttu-id="44cf1-144">**Ylläpitokustannukset**-sivu avautuu ja siihen liittyvät kustannukset näkyvät.</span><span class="sxs-lookup"><span data-stu-id="44cf1-144">The **Maintenance cost** page is opened and shows the related costs.</span></span>

### <a name="create-a-new-maintenance-asset-for-an-existing-fixed-asset"></a><a name="new-maintenance-from-fixed"></a><span data-ttu-id="44cf1-145">Luo uusi ylläpidettävä resurssi olemassa olevaan käyttöomaisuuserään</span><span class="sxs-lookup"><span data-stu-id="44cf1-145">Create a new maintenance asset for an existing fixed asset</span></span>

<span data-ttu-id="44cf1-146">Seuraa näitä ohjeita yhdistääksesi uuden ylläpidettävän resurssin aiemmin luotuun käyttöomaisuuserään.</span><span class="sxs-lookup"><span data-stu-id="44cf1-146">To create a new maintenance asset for an existing fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-147">Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-147">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="44cf1-148">Valitse resurssi.</span><span class="sxs-lookup"><span data-stu-id="44cf1-148">Select an asset.</span></span>
1. <span data-ttu-id="44cf1-149">Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Uusi**-ryhmässä **Luo ylläpidettävä resurssi**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-149">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span> <span data-ttu-id="44cf1-150">(Jos tämä vaihtoehto ei ole käytettävissä, ylläpidettävä resurssi on ehkä jo liitetty valittuun käyttöomaisuuserään.)</span><span class="sxs-lookup"><span data-stu-id="44cf1-150">(If this option is unavailable, a maintenance asset might already be associated with the selected fixed asset.)</span></span>
1. <span data-ttu-id="44cf1-151">Viimeistele resurssin luominen [Luo resurssi](../objects/create-an-object.md) -kohdassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="44cf1-151">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="create-a-new-fixed-asset-and-add-a-new-maintenance-asset-for-it"></a><span data-ttu-id="44cf1-152">Luo uusi käyttöomaisuuserä ja lisää siihen olemassa oleva ylläpidettävä resurssi</span><span class="sxs-lookup"><span data-stu-id="44cf1-152">Create a new fixed asset and add a new maintenance asset for it</span></span>

<span data-ttu-id="44cf1-153">Seuraa näitä ohjeita yhdistääksesi uuden käyttöomaisuuserän uuteen ylläpidettävään resurssiin.</span><span class="sxs-lookup"><span data-stu-id="44cf1-153">To create a new fixed asset and add a new maintenance asset for it, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-154">Siirry kohtaan **Käyttöomaisuus \> Käyttöomaisuus \> Käyttöomaisuus**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-154">Go to **Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
1. <span data-ttu-id="44cf1-155">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-155">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="44cf1-156">Viimeistele käyttöomaisuuden luominen [Luo käyttöomaisuus](../../../finance/fixed-assets/tasks/create-fixed-asset.md) -kohdassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="44cf1-156">Finish creating the fixed asset as described in [Create a fixed asset](../../../finance/fixed-assets/tasks/create-fixed-asset.md).</span></span>
1. <span data-ttu-id="44cf1-157">Valitse sitten toimintoruudussa **Resurssinhallinta**-välilehden **Uusi**-ryhmässä **Luo ylläpidettävä resurssi**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-157">On the Action Pane, on the **Asset management** tab, in the **New** group, select **Create maintenance asset**.</span></span>
1. <span data-ttu-id="44cf1-158">Viimeistele resurssin luominen [Luo resurssi](../objects/create-an-object.md) -kohdassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="44cf1-158">Finish creating the asset as described in [Create an asset](../objects/create-an-object.md).</span></span>

### <a name="remove-the-association-between-two-assets"></a><span data-ttu-id="44cf1-159">Kahden käyttöomaisuuserän liitoksen poistaminen</span><span class="sxs-lookup"><span data-stu-id="44cf1-159">Remove the association between two assets</span></span>

<span data-ttu-id="44cf1-160">Joissakin tapauksissa ylläpidettävä resurssi on ehkä irrotettava käyttöomaisuudesta.</span><span class="sxs-lookup"><span data-stu-id="44cf1-160">In some cases, you might have to disassociate a maintenance asset from its fixed asset.</span></span> <span data-ttu-id="44cf1-161">Jos esimerkiksi haluat [luoda uuden ylläpidettävä resurssin](#new-maintenance-from-fixed) käyttöomaisuudesta, sinun on ensin poistettava kaikki olemassa olevat liitokset.</span><span class="sxs-lookup"><span data-stu-id="44cf1-161">For example, if you want to [create a new maintenance asset](#new-maintenance-from-fixed) from a fixed asset, you must first remove any existing association.</span></span>

<span data-ttu-id="44cf1-162">Seuraa näitä ohjeita poistaaksesi olemassa olevan liitoksen ylläpidettävän resurssin ja käyttöomaisuuserän väliltä.</span><span class="sxs-lookup"><span data-stu-id="44cf1-162">To remove an existing association between a maintenance asset and a fixed asset, follow these steps.</span></span>

1. <span data-ttu-id="44cf1-163">Mene kohtaan **Resurssien hallinta \> Resurssit \> Kaikki resurssit** (tai **Aktiiviset resurssit**).</span><span class="sxs-lookup"><span data-stu-id="44cf1-163">Go to **Asset management \> Assets \> All assets** (or **Active assets**).</span></span>
1. <span data-ttu-id="44cf1-164">Etsi ja avaa käyttöomaisuus.</span><span class="sxs-lookup"><span data-stu-id="44cf1-164">Find and open the fixed asset.</span></span>
1. <span data-ttu-id="44cf1-165">Poista **käyttöomaisuus**-pikavälilehden **toiminnallinen sijainti** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="44cf1-165">On the **Fixed asset** FastTab, clear the value from the **Functional location** field.</span></span>
1. <span data-ttu-id="44cf1-166">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="44cf1-166">On the Action Pane, select **Save**.</span></span>