---
title: Luo kanavan siirtymishierarkia
description: Tässä ohjeaiheessa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 04/27/2021
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
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951905"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="5194c-103">Vähittäismyyntikanavan siirtymishierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="5194c-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5194c-104">Tässä ohjeaiheessa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="5194c-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5194c-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="5194c-105">Overview</span></span>

<span data-ttu-id="5194c-106">Kanavan siirtymishierarkiaa käytetään tuotteiden luokkiin ryhmittelemiseen ja järjestämiseen, jotta niitä voidaan selata verkossa tai myyntipisteessä (POS).</span><span class="sxs-lookup"><span data-stu-id="5194c-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="5194c-107">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="5194c-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="5194c-108">Voit luoda kanavan siirtymishierarkian seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5194c-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="5194c-109">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.</span><span class="sxs-lookup"><span data-stu-id="5194c-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="5194c-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5194c-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="5194c-111">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="5194c-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5194c-112">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5194c-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5194c-113">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="5194c-113">Select **Create**.</span></span>
1. <span data-ttu-id="5194c-114">Valitse toimintoruudussa **Uusi luokkasolmu** luodaksesi pääsolmun.</span><span class="sxs-lookup"><span data-stu-id="5194c-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="5194c-115">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="5194c-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5194c-116">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5194c-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5194c-117">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="5194c-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="5194c-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5194c-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5194c-119">Seuraavassa kuvassa näkyy esimerkki pääsolmusta.</span><span class="sxs-lookup"><span data-stu-id="5194c-119">The following image shows a example root node.</span></span>

![Pääsolmun esimerkki](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="5194c-121">Siirtymisluokkasolmujen luominen</span><span class="sxs-lookup"><span data-stu-id="5194c-121">Create navigation category nodes</span></span>

<span data-ttu-id="5194c-122">Seuraavien ohjeiden avulla voit luoda lisää siirtymisluokkasolmuja edustamaan tuoteluokkia kanavalla.</span><span class="sxs-lookup"><span data-stu-id="5194c-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="5194c-123">Valitse siirtymisruudussa se pääsolmu, johon luokka lisätään.</span><span class="sxs-lookup"><span data-stu-id="5194c-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="5194c-124">Valitse toimintoruudusta **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="5194c-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="5194c-125">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="5194c-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="5194c-126">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5194c-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="5194c-127">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="5194c-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="5194c-128">Syötä **Näyttöjärjestys**-ruutuun näyttöjärjestys (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="5194c-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="5194c-129">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5194c-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5194c-130">Seuraavassa kuvassa näkyy esimerkki valmiista kanavan siirtymishierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="5194c-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanavan hierarkian esimerkki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="5194c-132">Lisää tuotteita luokkasolmuihin</span><span class="sxs-lookup"><span data-stu-id="5194c-132">Add products to category nodes</span></span>

<span data-ttu-id="5194c-133">Voit lisätä tuotteita luokkasolmuihin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="5194c-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="5194c-134">Valitse luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="5194c-134">Select a category node.</span></span>
1. <span data-ttu-id="5194c-135">Valitse **Tuotteet**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5194c-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="5194c-136">Etsi uudet tuotteet, jotka haluat lisätä tuotenumeron tai tuotteen nimen avulla, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="5194c-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="5194c-137">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5194c-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="5194c-138">Tuotteiden lisääminen kanavan siirtymishierarkiassa olevaan solmuun ei riitä siihen, että näkyisivät valitussa kanavassa, sillä tuotteet on myös lajiteltava kanavaan.</span><span class="sxs-lookup"><span data-stu-id="5194c-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="5194c-139">Lisätietoa valikoimista on kohdassa [Valikoiman hallinta](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="5194c-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="5194c-140">Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotteita.</span><span class="sxs-lookup"><span data-stu-id="5194c-140">The following image shows an example node with products added.</span></span>

![Luokkasolmuun lisätyt tuotteet](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="5194c-142">Tuotemääriteryhmien lisääminen luokkasolmuihin</span><span class="sxs-lookup"><span data-stu-id="5194c-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="5194c-143">Määriteryhmät on luotava ennen kuin voit lisätä ne solmuun kanavan siirtymishierarkian sisällä.</span><span class="sxs-lookup"><span data-stu-id="5194c-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="5194c-144">Voit lisätä tuotteen määriteryhmän luokkasolmuun seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="5194c-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="5194c-145">Valitse luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="5194c-145">Select a category node.</span></span>
1. <span data-ttu-id="5194c-146">Valitse **Tuotteen määriteryhmä**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5194c-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="5194c-147">Etsi lisättävät määriteryhmät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5194c-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="5194c-148">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5194c-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="5194c-149">Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotemääriteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="5194c-149">The following image shows a sample node with product attribute groups added.</span></span>

![Tuotemääriteryhmiä solmussa](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="5194c-151">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5194c-151">Additional resources</span></span>

[<span data-ttu-id="5194c-152">Valikoimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5194c-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="5194c-153">Määritteiden ja määriteryhmien hallinta</span><span class="sxs-lookup"><span data-stu-id="5194c-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
