---
title: Verkkotoimintoprofiilin luominen
description: Tässä ohjeaiheessa käsitellään verkkotoimintoprofiilin luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477729"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="e480a-103">Luo online-toimintoprofiili</span><span class="sxs-lookup"><span data-stu-id="e480a-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e480a-104">Tässä ohjeaiheessa on yleiskatsaus Microsoft Dynamics 365 Commercen online-toimintoprofiilin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="e480a-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e480a-105">Online-toimintojen profiilissa on erilaisia online-kanavien asetuksia.</span><span class="sxs-lookup"><span data-stu-id="e480a-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="e480a-106">Kunkin online-kanavan on määritettävä online-toimintoprofiili.</span><span class="sxs-lookup"><span data-stu-id="e480a-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="e480a-107">Verkkotoimintoprofiilin luominen</span><span class="sxs-lookup"><span data-stu-id="e480a-107">Create an online functionality profile</span></span>

<span data-ttu-id="e480a-108">Seuraavassa kuvataan, miten online-toimintoprofiili luodaan Commerce Headquarters -sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="e480a-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="e480a-109">Siirry siirtymisruudussa kohtaan **Moduulit \> Kanavan määritys \> Verkkokaupan määritys \> Toimintoprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="e480a-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="e480a-110">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="e480a-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="e480a-111">Kirjoita **Profiili**-kenttään nimi profiilille.</span><span class="sxs-lookup"><span data-stu-id="e480a-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="e480a-112">Kirjoita **Kuvaus**-kenttään arvo (Adventure Works -profiili alla olevaan esimerkkikuvaan).</span><span class="sxs-lookup"><span data-stu-id="e480a-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="e480a-113">Muokkaa **Toiminnot**-osassa **OSTOSKÄRRYÄ**, **VÄHITTÄISMYYNTIASIAKKAITA** tai **KASSALLE**-asetuksia tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e480a-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="e480a-114">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e480a-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="e480a-115">Seuraavassa kuvassa on esimerkki verkkotoimintoprofiilista.</span><span class="sxs-lookup"><span data-stu-id="e480a-115">The following image shows an example online functionality profile.</span></span>
  
![Verkon toimintoprofiiliesimerkki](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="e480a-117">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="e480a-117">Functions</span></span>

- <span data-ttu-id="e480a-118">**Koostetuotteet**: Kun tämä toiminto on käytössä, ostoskärry voi päivittää määrän, kun sama nimike lisätään useita kertoja.</span><span class="sxs-lookup"><span data-stu-id="e480a-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="e480a-119">**Salli uloskuittaus ilman maksuja**: Kun tämä toiminto on käytössä, se käsittelee skenaarion, kun ostoskärryyn lisätyistä nimikkeistä veloitetaan hinta 0,00 $.</span><span class="sxs-lookup"><span data-stu-id="e480a-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="e480a-120">**Luo asiakas asynkronisessa tilassa**: Tämä on kolmannen osapuolen sähköisen kaupankäynnin kanaviin sovellettava perintöasetus, eikä se koske Dynamics 365 -verkkokauppasivustoa.</span><span class="sxs-lookup"><span data-stu-id="e480a-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e480a-121">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e480a-121">Additional resources</span></span>

[<span data-ttu-id="e480a-122">Kanavien yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e480a-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="e480a-123">Kanava-asetusten edellytykset</span><span class="sxs-lookup"><span data-stu-id="e480a-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="e480a-124">Verkkokanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e480a-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="e480a-125">Vähittäismyyntikanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e480a-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="e480a-126">Puhelinkeskuskanavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e480a-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
