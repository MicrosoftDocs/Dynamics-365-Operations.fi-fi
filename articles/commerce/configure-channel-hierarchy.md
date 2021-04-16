---
title: Kanavan määrittäminen kanavan siirtymishierarkian käyttämistä varten
description: Tässä aiheessa kuvataan, miten kanava määritetään kanavahierarkian käyttöä varten Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 94d38c5c3a091263b310f346f839e1a67d6c0609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796121"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="e694c-103">Kanavan määrittäminen kanavan siirtymishierarkian käyttämistä varten</span><span class="sxs-lookup"><span data-stu-id="e694c-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e694c-104">Tässä aiheessa kuvataan, miten kanava määritetään kanavahierarkian käyttöä varten Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e694c-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e694c-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e694c-105">Overview</span></span>

<span data-ttu-id="e694c-106">Kanavien siirtymishierarkiat järjestävät tuotteet luokkiin, jotta tuotteita voi selata verkkokauppasivustolla tai myyntipisteissä.</span><span class="sxs-lookup"><span data-stu-id="e694c-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="e694c-107">Vähittäismyynti- ja verkkokanavat on määritettävä kanavan siirtymishierarkioilla.</span><span class="sxs-lookup"><span data-stu-id="e694c-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="e694c-108">Kanavan määritys</span><span class="sxs-lookup"><span data-stu-id="e694c-108">Configure the channel</span></span>

<span data-ttu-id="e694c-109">Voit määrittää kanavan kanavan siirtymishierarkian käyttöä varten noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e694c-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="e694c-110">Siirry siirtymisruudussa kohtaan **Moduulit \> Vähittäismyynti ja kauppa \> Kanavan määritys \> Kanavaluokat ja tuotemääritteet**.</span><span class="sxs-lookup"><span data-stu-id="e694c-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="e694c-111">Valitse määritettävä kanava.</span><span class="sxs-lookup"><span data-stu-id="e694c-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="e694c-112">Valitse toimintoruudussa **Määritä määritteen metatiedot**.</span><span class="sxs-lookup"><span data-stu-id="e694c-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="e694c-113">Valitse avattavassa **Luokkahierarkia**-luettelossa asianmukainen kanavan siirtymishierarkia.</span><span class="sxs-lookup"><span data-stu-id="e694c-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="e694c-114">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e694c-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="e694c-115">Lisää **Määriteryhmä**-kohtaan määriteryhmiä, joita käytetään yleisinä määritteinä kaikille solmuille.</span><span class="sxs-lookup"><span data-stu-id="e694c-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="e694c-116">Seuraavassa kuvassa esitetään, miten kanava määritetään kanavan siirtymishierarkian käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="e694c-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Kanavan esimerkkimääritys](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="e694c-118">Määritä määritteen metatiedot</span><span class="sxs-lookup"><span data-stu-id="e694c-118">Set attribute metadata</span></span>

<span data-ttu-id="e694c-119">Määritteen metatietojen määrittäminen mahdollistaa kunkin solmun määritteiden määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="e694c-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="e694c-120">Määritä määritteen metatiedot seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e694c-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="e694c-121">Valitse toimintoruudussa **Määritä määritteen metatiedot**.</span><span class="sxs-lookup"><span data-stu-id="e694c-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="e694c-122">Valitse kullekin solmulle **Kanavan tuotemääritteet**.</span><span class="sxs-lookup"><span data-stu-id="e694c-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="e694c-123">Asta **Näytä määrite kanavassa**-asetuksen arvoksi **Kyllä** ja **Voidaan tarkistaa**-asetuksen arvoksi **Kyllä**, jotta kyseisessä kanavassa voidaan käyttää tarkentajia.</span><span class="sxs-lookup"><span data-stu-id="e694c-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="e694c-124">Kun olet määrittänyt kunkin solmun haluamallasi tavalla, tallenna määritykset valitsemalla **Toimintoruudussa** **Tallenna**-painike.</span><span class="sxs-lookup"><span data-stu-id="e694c-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="e694c-125">Poistu tästä ruudusta takaisin **Kanavaluokat ja tuotemääritteet** -sivulle valitsemalla oikean yläkulman **X**.</span><span class="sxs-lookup"><span data-stu-id="e694c-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="e694c-126">Seuraavassa kuvassa näkyy esimerkkijoukko kanavan tuotemääritteitä, jotka on määritetty kanavan luokkasolmussa.</span><span class="sxs-lookup"><span data-stu-id="e694c-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Kanavamääritteet kanavaluokkasolmussa](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="e694c-128">Julkaise muutokset</span><span class="sxs-lookup"><span data-stu-id="e694c-128">Publish changes</span></span>

<span data-ttu-id="e694c-129">Sinun on julkaistava muutokset, jotta ne tulevat voimaan.</span><span class="sxs-lookup"><span data-stu-id="e694c-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="e694c-130">Julkaise muutokset seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="e694c-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="e694c-131">Valitse toimintoruudussa **Julkaise kanavapäivitykset**.</span><span class="sxs-lookup"><span data-stu-id="e694c-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="e694c-132">Valitse **Julkaise kanavapäivitykset** -ruudussa **OK**.</span><span class="sxs-lookup"><span data-stu-id="e694c-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="e694c-133">Seuraavassa kuvassa näkyy, miten kanavapäivitykset julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="e694c-133">The following image shows how to publish channel updates.</span></span>

![Julkaise kanavan päivitykset](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="e694c-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e694c-135">Additional resources</span></span>

[<span data-ttu-id="e694c-136">Luo kanavan siirtymishierarkia</span><span class="sxs-lookup"><span data-stu-id="e694c-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]