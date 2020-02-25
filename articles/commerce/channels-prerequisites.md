---
title: Kanava-asetusten edellytykset
description: Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.
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
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002286"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="86efd-103">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="86efd-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="86efd-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanava-asetusten edellytyksistä.</span><span class="sxs-lookup"><span data-stu-id="86efd-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="86efd-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="86efd-105">Overview</span></span>

<span data-ttu-id="86efd-106">Ennen Dynamics 365 Commerce -kanavan luontia on suoritettava useita ennakkoedellytystehtäviä.</span><span class="sxs-lookup"><span data-stu-id="86efd-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="86efd-107">Seuraava edellytysten tehtäväluettelo on organisoitu kanavatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="86efd-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="86efd-108">Osaa ohjeistuksesta kirjoitetaan edelleen ja linkit päivitetään, kun uutta sisältöä julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="86efd-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="86efd-109">Alustus</span><span class="sxs-lookup"><span data-stu-id="86efd-109">Initialization</span></span>

- [<span data-ttu-id="86efd-110">Alkutietojen alustaminen</span><span class="sxs-lookup"><span data-stu-id="86efd-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="86efd-111">Kaikissa kanavatyypeissä tarvittavat yleiset edellytykset</span><span class="sxs-lookup"><span data-stu-id="86efd-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="86efd-112">Yrityksen rakenteen määrittäminen ja asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="86efd-113">Organisaatiohierarkian asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="86efd-114">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="86efd-115">Arvonlisäveron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="86efd-116">Sähköpostin ilmoitusprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="86efd-117">Numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="86efd-118">Oletusasiakkaan ja -osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="86efd-119">Vähittäismyyntikanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="86efd-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="86efd-120">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="86efd-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="86efd-121">Vähittäismyynnin toimintoprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="86efd-122">Työntekijän osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="86efd-123">Aseta näyttöpohja</span><span class="sxs-lookup"><span data-stu-id="86efd-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="86efd-124">Laiteaseman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="86efd-125">Puhelinkeskuskanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="86efd-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="86efd-126">Puhelinkeskuksen parametrit</span><span class="sxs-lookup"><span data-stu-id="86efd-126">Call center parameters</span></span>
- <span data-ttu-id="86efd-127">Puhelinkeskuksen palautusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="86efd-127">Call center refund methods</span></span>
- <span data-ttu-id="86efd-128">Vuokratyypit</span><span class="sxs-lookup"><span data-stu-id="86efd-128">Rental types</span></span>
- <span data-ttu-id="86efd-129">Maksupalvelut</span><span class="sxs-lookup"><span data-stu-id="86efd-129">Payment services</span></span>
- <span data-ttu-id="86efd-130">Tilauksen pitokoodit</span><span class="sxs-lookup"><span data-stu-id="86efd-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="86efd-131">Verkkokanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="86efd-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="86efd-132">Verkkotoimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="86efd-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="86efd-133">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="86efd-133">Additional resources</span></span>

[<span data-ttu-id="86efd-134">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="86efd-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="86efd-135">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="86efd-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="86efd-136">Organisaatiohierarkioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="86efd-137">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="86efd-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="86efd-138">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="86efd-139">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86efd-139">Set up an online channel</span></span>](channel-setup-online.md)
