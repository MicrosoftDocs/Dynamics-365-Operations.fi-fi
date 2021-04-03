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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477921"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="c8e03-103">Kanavan määrittämisen edellytykset</span><span class="sxs-lookup"><span data-stu-id="c8e03-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8e03-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen kanavien asetusten edellytyksistä.</span><span class="sxs-lookup"><span data-stu-id="c8e03-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c8e03-105">Ennen Dynamics 365 Commerce -kanavan luontia on suoritettava useita ennakkoedellytystehtäviä.</span><span class="sxs-lookup"><span data-stu-id="c8e03-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="c8e03-106">Seuraava edellytysten tehtäväluettelo on organisoitu kanavatyypin mukaan.</span><span class="sxs-lookup"><span data-stu-id="c8e03-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="c8e03-107">Osaa ohjeistuksesta kirjoitetaan edelleen ja linkit päivitetään, kun uutta sisältöä julkaistaan.</span><span class="sxs-lookup"><span data-stu-id="c8e03-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="c8e03-108">Alustus</span><span class="sxs-lookup"><span data-stu-id="c8e03-108">Initialization</span></span>

- [<span data-ttu-id="c8e03-109">Alkutietojen alustaminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="c8e03-110">Kaikissa kanavatyypeissä tarvittavat yleiset edellytykset</span><span class="sxs-lookup"><span data-stu-id="c8e03-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="c8e03-111">Yrityksen rakenteen määrittäminen ja asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="c8e03-112">Organisaatiohierarkian asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="c8e03-113">Varaston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="c8e03-114">Arvonlisäveron määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c8e03-115">Sähköpostin ilmoitusprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="c8e03-116">Numerosarjojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="c8e03-117">Oletusasiakkaan ja -osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="c8e03-118">Vähittäismyyntikanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="c8e03-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="c8e03-119">Tietokoodit ja tietokoodiryhmät</span><span class="sxs-lookup"><span data-stu-id="c8e03-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="c8e03-120">Vähittäismyynnin toimintoprofiilin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="c8e03-121">Työntekijän osoitekirjan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="c8e03-122">Aseta näyttöpohja</span><span class="sxs-lookup"><span data-stu-id="c8e03-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="c8e03-123">Laiteaseman määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="c8e03-124">Puhelinkeskuskanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="c8e03-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="c8e03-125">Puhelinkeskuksen parametrit</span><span class="sxs-lookup"><span data-stu-id="c8e03-125">Call center parameters</span></span>
- [<span data-ttu-id="c8e03-126">Puhelinkeskuksen tilaus- ja maksunpalautusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="c8e03-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="c8e03-127">Puhelinkeskuksen toimitustilat ja kulut</span><span class="sxs-lookup"><span data-stu-id="c8e03-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="c8e03-128">Online-kanavan edellytykset</span><span class="sxs-lookup"><span data-stu-id="c8e03-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="c8e03-129">Luo online-toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="c8e03-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="c8e03-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c8e03-130">Additional resources</span></span>

[<span data-ttu-id="c8e03-131">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c8e03-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="c8e03-132">Organisaatiot ja organisaatiohierarkiat – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c8e03-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="c8e03-133">Organisaatiohierarkioiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="c8e03-134">Yritysten luominen</span><span class="sxs-lookup"><span data-stu-id="c8e03-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="c8e03-135">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="c8e03-136">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c8e03-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
