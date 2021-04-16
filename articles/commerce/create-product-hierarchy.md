---
title: Uuden tuotehierarkian luominen
description: Tässä ohjeaiheessa käsitellään uuden tuotehierarkian luontia Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 8aef33a501f43105730eaa21a9159eb1398a1b36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799562"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="3f71b-103">Uuden tuotehierarkian luominen</span><span class="sxs-lookup"><span data-stu-id="3f71b-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3f71b-104">Tässä ohjeaiheessa käsitellään uuden tuotehierarkian luontia Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="3f71b-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f71b-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="3f71b-105">Overview</span></span>

<span data-ttu-id="3f71b-106">Dynamics 365 Commerce tukee useita vähittäismyynnin kanavia.</span><span class="sxs-lookup"><span data-stu-id="3f71b-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="3f71b-107">Vähittäismyyntikanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat).</span><span class="sxs-lookup"><span data-stu-id="3f71b-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="3f71b-108">Jokaisella vähittäismyymäläkanavalla voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta.</span><span class="sxs-lookup"><span data-stu-id="3f71b-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="3f71b-109">Sinun on määritettävä kaikki nämä elementit, ennen kuin voit luoda vähittäismyymäläkanavan.</span><span class="sxs-lookup"><span data-stu-id="3f71b-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="3f71b-110">Commerce-tuotehierarkiaa käytetään organisaation yleisen tuotehierarkian määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="3f71b-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="3f71b-111">Commerce-tuotehierarkiaa voi käyttää markkinoinnissa, hinnoittelussa ja kampanjoissa, raportoinnissa sekä valikoiman suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="3f71b-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="3f71b-112">Organisaatiolle voidaan määrittää vain yksi Commerce-tuotehierarkia.</span><span class="sxs-lookup"><span data-stu-id="3f71b-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="3f71b-113">Tuotehierarkian luonti ja määritys</span><span class="sxs-lookup"><span data-stu-id="3f71b-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="3f71b-114">Voit luoda ja määrittää uuden Commerce-tuotehierarkian seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3f71b-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3f71b-115">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäiskauppa ja kauppa \> Tuotteet ja luokat \> Kanavan siirtymisluokat**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="3f71b-116">Jos hierarkiaa ei vielä ole, valitse **Toimintoruutu**-elementissä **Uusi** luodaksesi päähierarkian.</span><span class="sxs-lookup"><span data-stu-id="3f71b-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="3f71b-117">**Yleistä**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="3f71b-117">Under **General**:</span></span>
    1. <span data-ttu-id="3f71b-118">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="3f71b-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="3f71b-119">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3f71b-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="3f71b-120">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="3f71b-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="3f71b-121">Aseta **Aktiivinen**-asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="3f71b-122">Hierarkiasolmujen lisäys</span><span class="sxs-lookup"><span data-stu-id="3f71b-122">Add hierarchy nodes</span></span>

<span data-ttu-id="3f71b-123">Voit lisätä hierarkiasolmuja seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="3f71b-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="3f71b-124">Valitse toimintoruudusta **Muokkaa luokkahierarkiaa**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="3f71b-125">Valitse pääsolmu, johon haluat lisätä uuden solmun, ja valitse sitten **Uusi luokkasolmu**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="3f71b-126">Anna **Yleistä**-osassa **Nimi**, **Kuvaus**, **Kutsumanimi** ja **Avainsanat**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="3f71b-127">**Yleistä**-kohdassa:</span><span class="sxs-lookup"><span data-stu-id="3f71b-127">Under **General**:</span></span>
    1. <span data-ttu-id="3f71b-128">Anna nimi **Nimi**-ruutuun.</span><span class="sxs-lookup"><span data-stu-id="3f71b-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="3f71b-129">Syötä **Kuvaus**-ruutuun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3f71b-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="3f71b-130">Syötä **Kutsumanimi**-ruutuun kutsumanimi.</span><span class="sxs-lookup"><span data-stu-id="3f71b-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="3f71b-131">Syötä **Avainsanat**-ruutuun tarvittavat avainsanat.</span><span class="sxs-lookup"><span data-stu-id="3f71b-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="3f71b-132">Syötä **Näyttöjärjestys**-ruutuun numero, joka edustaa näyttöjärjestystä (valinnainen).</span><span class="sxs-lookup"><span data-stu-id="3f71b-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="3f71b-133">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3f71b-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="3f71b-134">Voit lisätä lisää solmuja toistamalla edellä esitetyt vaiheet.</span><span class="sxs-lookup"><span data-stu-id="3f71b-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="3f71b-135">Seuraavassa kuvassa näytetään, miten uusi tuotehierarkiasolmu luodaan.</span><span class="sxs-lookup"><span data-stu-id="3f71b-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Tuotehierarkian luominen](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="3f71b-137">Muut asetukset</span><span class="sxs-lookup"><span data-stu-id="3f71b-137">Other settings</span></span>

<span data-ttu-id="3f71b-138">Kullekin ryhmälle voi myös lisätä luokkamääriteryhmiä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="3f71b-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="3f71b-139">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3f71b-139">Additional resources</span></span>

[<span data-ttu-id="3f71b-140">Commerce-hierarkiat</span><span class="sxs-lookup"><span data-stu-id="3f71b-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="3f71b-141">Tuoteluokkien ja tuotteiden hallinta</span><span class="sxs-lookup"><span data-stu-id="3f71b-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="3f71b-142">Myynninedistämiskohteiden lajittelujärjestyksen muuttaminen</span><span class="sxs-lookup"><span data-stu-id="3f71b-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]