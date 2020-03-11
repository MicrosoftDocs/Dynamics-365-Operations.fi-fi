---
title: Kanavien yleiskatsaus
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanavista.
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
ms.openlocfilehash: 099ccd9f769ea5c431c1a82532d8654cbbd082b1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002355"
---
# <a name="channels-overview"></a><span data-ttu-id="6c7be-103">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6c7be-103">Channels overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6c7be-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanavista.</span><span class="sxs-lookup"><span data-stu-id="6c7be-104">This topic presents an overview of channels in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="6c7be-105">Siinä on tietoja tehtävistä, jotka on suoritettava ennen kunkin kanavan määrittämistä ja sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="6c7be-105">It includes information about the tasks that you must complete both before and after you set up each channel.</span></span>

## <a name="types-of-channels"></a><span data-ttu-id="6c7be-106">Kanavatyypit</span><span class="sxs-lookup"><span data-stu-id="6c7be-106">Types of Channels</span></span>

<span data-ttu-id="6c7be-107">Dynamics 365 Commerce tukee kolmea kanavatyyppiä: vähittäismyynti-, puhelinkeskus- ja verkkokanavaa.</span><span class="sxs-lookup"><span data-stu-id="6c7be-107">Dynamics 365 Commerce supports three different channel types: retail, call center, and online channels.</span></span>

### <a name="retail-channels"></a><span data-ttu-id="6c7be-108">Vähittäismyyntikanavat</span><span class="sxs-lookup"><span data-stu-id="6c7be-108">Retail channels</span></span>

<span data-ttu-id="6c7be-109">Vähittäismyyntikanavat tarkoittavat perinteisiä myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="6c7be-109">Retail channels represent standard brick-and-mortar stores.</span></span> <span data-ttu-id="6c7be-110">Jokaisella myymälällä voi olla omat myyntipisteiden kassakoneet, tulo- ja kulutilit sekä oma henkilökunta.</span><span class="sxs-lookup"><span data-stu-id="6c7be-110">Each store can have its own point of sale (POS) registers, income and expense accounts, and staff.</span></span> 

### <a name="call-center-channels"></a><span data-ttu-id="6c7be-111">Puhelinkeskuskanavat</span><span class="sxs-lookup"><span data-stu-id="6c7be-111">Call center channels</span></span>

<span data-ttu-id="6c7be-112">Puhelinkeskuskanavat tarkoittavat puhelinkeskustilauksia ja asiakashallintaa.</span><span class="sxs-lookup"><span data-stu-id="6c7be-112">Call center channels represent call center order and customer management.</span></span>

### <a name="online-channels"></a><span data-ttu-id="6c7be-113">Online-kanavat</span><span class="sxs-lookup"><span data-stu-id="6c7be-113">Online channels</span></span>

<span data-ttu-id="6c7be-114">Verkkokanavat tarkoittavat sähköisen kaupankäynnin verkkokauppoja.</span><span class="sxs-lookup"><span data-stu-id="6c7be-114">Online channels represent online e-Commerce storefronts.</span></span> <span data-ttu-id="6c7be-115">Kun verkkokanava luodaan, sivusto on luotava Microsoft Dynamics 365 Commercen sivuston muodostintyökalulla tai jollain kolmannen osapuolen sähköisellä kaupankäyntiratkaisulla.</span><span class="sxs-lookup"><span data-stu-id="6c7be-115">Once an online channel is created, a site must be created using the Microsoft Dynamics 365 Commerce Site Builder tool or other third-party e-Commerce solution.</span></span>

## <a name="channel-setup-basics"></a><span data-ttu-id="6c7be-116">Kanavan määritysten perusteet</span><span class="sxs-lookup"><span data-stu-id="6c7be-116">Channel setup basics</span></span>

<span data-ttu-id="6c7be-117">Kanava määritetään Commerce-työkalulla.</span><span class="sxs-lookup"><span data-stu-id="6c7be-117">Channel set up is performed in the Commerce tool.</span></span> <span data-ttu-id="6c7be-118">Kullakin kanavalla on omat maksutavat, hintaryhmät, tuotehierarkiat, valikoimat ja tuoteryhmät.</span><span class="sxs-lookup"><span data-stu-id="6c7be-118">Each channel can have its own payment methods, price groups, product hierarchies, assortments, and set of products.</span></span> <span data-ttu-id="6c7be-119">Kun kanava on luotu, kanavassa myytävät tuotteet on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="6c7be-119">After you create a channel, you assign the products that you want it to carry and sell.</span></span> <span data-ttu-id="6c7be-120">Kullakin kanavatyypillä on yksilöllinen toimintojoukko, joka on ehkä määritettävä.</span><span class="sxs-lookup"><span data-stu-id="6c7be-120">Each channel type has a unique set of features that may need to be configured.</span></span> <span data-ttu-id="6c7be-121">Esimerkiksi vähittäismyyntikanavassa on määritettävä työntekijöitä, kassakoneita ja asiakkaita.</span><span class="sxs-lookup"><span data-stu-id="6c7be-121">For example, a retail channel needs assigned employees, registers, and customers.</span></span> <span data-ttu-id="6c7be-122">Kun uusi kanava on luotu, se on määritettävä organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="6c7be-122">Once a new channel is created, it needs to be assigned to an organization hierarchy.</span></span>

## <a name="channel-setup-prerequisites"></a><span data-ttu-id="6c7be-123">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="6c7be-123">Channel setup prerequisites</span></span>

<span data-ttu-id="6c7be-124">Ennen kanavan määrittämistä on suoritettava joitakin kanavatyypin mukaisia ennakkotehtäviä.</span><span class="sxs-lookup"><span data-stu-id="6c7be-124">Before you can set up a channel, you must complete some prerequisite tasks based on the channel type.</span></span> <span data-ttu-id="6c7be-125">Lisätietoja on kohdassa [Kanava-asetusten edellytykset](channels-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="6c7be-125">For more information, see [Channel setup prerequisites](channels-prerequisites.md).</span></span>

## <a name="set-up-a-channel"></a><span data-ttu-id="6c7be-126">Kanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-126">Set up a channel</span></span>

<span data-ttu-id="6c7be-127">Kun edeltävät tehtävät on suoritettu, saat lisätietoja määrityksistä seuraavista linkeistä.</span><span class="sxs-lookup"><span data-stu-id="6c7be-127">After you complete the prerequisite tasks, for further setup instructions, use the following links.</span></span>

- [<span data-ttu-id="6c7be-128">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-128">Set up a retail channel</span></span>](channel-setup-retail.md)
- [<span data-ttu-id="6c7be-129">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-129">Set up a call center channel</span></span>](channel-setup-callcenter.md)
- [<span data-ttu-id="6c7be-130">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-130">Set up an online channel</span></span>](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a><span data-ttu-id="6c7be-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6c7be-131">Additional resources</span></span>

[<span data-ttu-id="6c7be-132">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="6c7be-132">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6c7be-133">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6c7be-134">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-134">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="6c7be-135">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-135">Set up a call center channel</span></span>](channel-setup-callcenter.md)

[<span data-ttu-id="6c7be-136">Organisaatiohierarkioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6c7be-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)