---
title: Kanava-asetusten edellytykset
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 8a0927f6ee9b2d5bed1327bb223ceca85ecc16a0
ms.sourcegitcommit: 161e85eb0a6b772b60ba8b2578a3de149ce5bfd7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/22/2020
ms.locfileid: "3081312"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="69b13-103">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="69b13-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="69b13-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.</span><span class="sxs-lookup"><span data-stu-id="69b13-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="69b13-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="69b13-105">Overview</span></span>

<span data-ttu-id="69b13-106">Ennen Dynamics 365 Commerce -kanavan luontia on suoritettava useita ennakkoedellytystehtäviä.</span><span class="sxs-lookup"><span data-stu-id="69b13-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="69b13-107">Seuraava edellytysten tehtäväluettelo on organisoitu kanavatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="69b13-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="69b13-108">Osaa ohjeistuksesta kirjoitetaan edelleen ja linkit päivitetään, kun uutta sisältöä julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="69b13-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="69b13-109">Alustus</span><span class="sxs-lookup"><span data-stu-id="69b13-109">Initialization</span></span>

- [<span data-ttu-id="69b13-110">Alkutietojen alustaminen</span><span class="sxs-lookup"><span data-stu-id="69b13-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="69b13-111">Kaikissa kanavatyypeissä tarvittavat yleiset edellytykset</span><span class="sxs-lookup"><span data-stu-id="69b13-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="69b13-112">Yrityksen rakenteen määrittäminen ja asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="69b13-113">Organisaatiohierarkian asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="69b13-114">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="69b13-115">Arvonlisäveron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-115">Configure sales tax</span></span>](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="69b13-116">Sähköpostin ilmoitusprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="69b13-117">Numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-117">Set up number sequences</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="69b13-118">Oletusasiakkaan ja -osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="69b13-119">Vähittäismyyntikanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="69b13-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="69b13-120">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="69b13-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="69b13-121">Vähittäismyynnin toimintoprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="69b13-122">Työntekijän osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="69b13-123">Aseta näyttöpohja</span><span class="sxs-lookup"><span data-stu-id="69b13-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="69b13-124">Laiteaseman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="69b13-125">Puhelinkeskuskanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="69b13-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="69b13-126">Puhelinkeskuksen parametrit</span><span class="sxs-lookup"><span data-stu-id="69b13-126">Call center parameters</span></span>
- [<span data-ttu-id="69b13-127">Puhelinkeskuksen tilaus- ja maksunpalautusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="69b13-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="69b13-128">Puhelinkeskuksen toimitustilat ja kulut</span><span class="sxs-lookup"><span data-stu-id="69b13-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="69b13-129">Online-kanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="69b13-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="69b13-130">Luo online-toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="69b13-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="69b13-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="69b13-131">Additional resources</span></span>

[<span data-ttu-id="69b13-132">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="69b13-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="69b13-133">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="69b13-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="69b13-134">Organisaatiohierarkioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="69b13-135">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="69b13-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="69b13-136">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="69b13-137">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="69b13-137">Set up an online channel</span></span>](channel-setup-online.md)
