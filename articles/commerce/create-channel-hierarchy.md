---
title: Luo kanavan siirtymishierarkia
description: Tässä ohjeaiheessa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: e83860667f142adcc85cd8542d521e18f16dbc2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411867"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ca0d5-103">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="ca0d5-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ca0d5-104">Tässä ohjeaiheessa käsitellään kanavan siirtymishierarkian luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ca0d5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ca0d5-105">Overview</span></span>

<span data-ttu-id="ca0d5-106">Kanavan siirtymishierarkiaa käytetään tuotteiden luokkiin ryhmittelemiseen ja järjestämiseen, jotta niitä voidaan selata verkossa tai myyntipisteessä (POS).</span><span class="sxs-lookup"><span data-stu-id="ca0d5-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ca0d5-107">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="ca0d5-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="ca0d5-108">Voit luoda kanavan siirtymishierarkian seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ca0d5-109">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="ca0d5-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ca0d5-111">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ca0d5-112">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ca0d5-113">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-113">Select **Create**.</span></span>
1. <span data-ttu-id="ca0d5-114">Valitse toimintoruudussa **Uusi luokkasolmu** luodaksesi pääsolmun.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="ca0d5-115">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ca0d5-116">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ca0d5-117">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ca0d5-118">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ca0d5-119">Seuraavassa kuvassa näkyy esimerkki pääsolmusta.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-119">The following image shows a example root node.</span></span>

![Pääsolmun esimerkki](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="ca0d5-121">Siirtymisluokkasolmujen luominen</span><span class="sxs-lookup"><span data-stu-id="ca0d5-121">Create navigation category nodes</span></span>

<span data-ttu-id="ca0d5-122">Seuraavien ohjeiden avulla voit luoda lisää siirtymisluokkasolmuja edustamaan tuoteluokkia kanavalla.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="ca0d5-123">Valitse siirtymisruudussa se pääsolmu, johon luokka lisätään.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="ca0d5-124">Valitse toimintoruudusta **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="ca0d5-125">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ca0d5-126">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ca0d5-127">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ca0d5-128">Syötä **Näyttöjärjestys**-ruutuun näyttöjärjestys (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="ca0d5-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="ca0d5-129">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ca0d5-130">Seuraavassa kuvassa näkyy esimerkki valmiista kanavan siirtymishierarkiasta.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Kanavan hierarkian esimerkki](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="ca0d5-132">Lisää tuotteita luokkasolmuihin</span><span class="sxs-lookup"><span data-stu-id="ca0d5-132">Add products to category nodes</span></span>

<span data-ttu-id="ca0d5-133">Voit lisätä tuotteita luokkasolmuihin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="ca0d5-134">Valitse luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-134">Select a category node.</span></span>
1. <span data-ttu-id="ca0d5-135">Valitse **Tuotteet**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="ca0d5-136">Etsi uudet tuotteet, jotka haluat lisätä tuotenumeron tai tuotteen nimen avulla, ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="ca0d5-137">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ca0d5-138">Tuotteiden lisääminen kanavan siirtymishierarkiassa olevaan solmuun ei riitä siihen, että näkyisivät valitussa kanavassa, sillä tuotteet on myös lajiteltava tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="ca0d5-139">Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotteita.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-139">The following image shows an example node with products added.</span></span>

![Luokkasolmuun lisätyt tuotteet](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="ca0d5-141">Tuotemääriteryhmien lisääminen luokkasolmuihin</span><span class="sxs-lookup"><span data-stu-id="ca0d5-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="ca0d5-142">Määriteryhmät on luotava ennen kuin voit lisätä ne solmuun kanavan siirtymishierarkian sisällä.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="ca0d5-143">Voit lisätä tuotteen määriteryhmän luokkasolmuun seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="ca0d5-144">Valitse luokkasolmu.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-144">Select a category node.</span></span>
1. <span data-ttu-id="ca0d5-145">Valitse **Tuotteen määriteryhmä**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="ca0d5-146">Etsi lisättävät määriteryhmät ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="ca0d5-147">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ca0d5-148">Seuraavassa kuvassa näkyy esimerkkisolmu, johon on lisätty tuotemääriteryhmiä.</span><span class="sxs-lookup"><span data-stu-id="ca0d5-148">The following image shows a sample node with product attribute groups added.</span></span>

![Tuotemääriteryhmiä solmussa](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="ca0d5-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ca0d5-150">Additional resources</span></span>

[<span data-ttu-id="ca0d5-151">Valikoimien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ca0d5-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="ca0d5-152">Määritteiden ja määriteryhmien hallinta</span><span class="sxs-lookup"><span data-stu-id="ca0d5-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)
