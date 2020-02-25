---
title: Kanavan lisääminen organisaatiohierarkiaan
description: Tässä ohjeaiheessa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.
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
ms.openlocfilehash: 701c90e8e28b4419422cddde698e9c9862a588a2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002470"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="27739-103">Kanavan lisääminen organisaatiohierarkiaan</span><span class="sxs-lookup"><span data-stu-id="27739-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="27739-104">Tässä ohjeaiheessa käsitellään kanavan lisäämistä organisaatiohierarkiaan Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="27739-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27739-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="27739-105">Overview</span></span>

<span data-ttu-id="27739-106">Kanavat on liitettävä vähintään yhteen organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="27739-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="27739-107">Ennen kanavien luontia on varmistettava, että organisaatiohierarkiat on määritetty.</span><span class="sxs-lookup"><span data-stu-id="27739-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="27739-108">Kohdassa [Organisaatiohierarkiat](channels-org-hierarchies.md) on lisätietoja organisaatiohierarkioiden luomisesta.</span><span class="sxs-lookup"><span data-stu-id="27739-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="27739-109">Hierarkian valinta</span><span class="sxs-lookup"><span data-stu-id="27739-109">Select a hierarchy</span></span>

<span data-ttu-id="27739-110">Valitse hierarkia seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="27739-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="27739-111">Valitse siirtymisruudussa **Moduulit \> Retail ja Commerce \> Kanavan asetukset \> Organisaatiohierarkiat**.</span><span class="sxs-lookup"><span data-stu-id="27739-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="27739-112">Valitse luettelosta organisaatiohierarkia, johon kanava lisätään.</span><span class="sxs-lookup"><span data-stu-id="27739-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="27739-113">Näytä hierarkian tiedot valitsemalla toimintoruudussa **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="27739-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="27739-114">Seuraavassa kuvassa on valitun hierarkian organisaatiohierarkian tiedot.</span><span class="sxs-lookup"><span data-stu-id="27739-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Valitun hierarkian organisaatiohierarkian tiedot](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="27739-116">Kanavan lisääminen hierarkiasolmuun</span><span class="sxs-lookup"><span data-stu-id="27739-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="27739-117">Voit lisätä kanavan hierarkiasolmuun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="27739-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="27739-118">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="27739-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="27739-119">Valitse hierarkiasolmu, johon kanava lisätään, ja valitse sitten avattavasta **Lisää**-luettelosta **Vähittäismyyntikanava**.</span><span class="sxs-lookup"><span data-stu-id="27739-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="27739-120">Valitse lisättävä kanava ja valitse sitten **OK**-painike.</span><span class="sxs-lookup"><span data-stu-id="27739-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="27739-121">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="27739-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="27739-122">Valitse toimintoruudussa **Julkaise** ja anna sitten menneisyydessä oleva **Voimaantulopäivä**, jotta toiminto otetaan heti käyttöön.</span><span class="sxs-lookup"><span data-stu-id="27739-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="27739-123">Seuraava kuva osoittaa, miten hierarkiasolmuun lisättävä kanava valitaan.</span><span class="sxs-lookup"><span data-stu-id="27739-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Hierarkiasolmuun lisättävän kanavan valitseminen](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="27739-125">Seuraavassa kuvassa on hierarkia, johon on lisätty useita kanavia.</span><span class="sxs-lookup"><span data-stu-id="27739-125">The following image shows a hierarchy with various channels added.</span></span>

![Hierarkia, johon on lisätty erilaisia kanavia](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="27739-127">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="27739-127">Additional resources</span></span>

[<span data-ttu-id="27739-128">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="27739-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="27739-129">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="27739-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="27739-130">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="27739-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="27739-131">Organisaatiohierarkian suunnitteleminen</span><span class="sxs-lookup"><span data-stu-id="27739-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="27739-132">Organisaatiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="27739-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="27739-133">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="27739-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="27739-134">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="27739-134">Set up an online channel</span></span>](channel-setup-online.md)
