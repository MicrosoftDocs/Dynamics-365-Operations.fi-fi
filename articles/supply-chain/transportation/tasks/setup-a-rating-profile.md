---
title: Hinnoitteluprofiilit
description: Tässä aiheessa käsitellään hinnoitteluprofiilien tietojen määrittämisestä.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ceb2b7a5edcee6e248798a6bee114c7da7ecb18a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973957"
---
# <a name="rating-profiles"></a><span data-ttu-id="c7be3-103">Hinnoitteluprofiilit</span><span class="sxs-lookup"><span data-stu-id="c7be3-103">Rating profiles</span></span>

<span data-ttu-id="c7be3-104">Hinnoitteluprofiili muistuttaa logistista sopimusta (mutta ei juridista sopimusta).</span><span class="sxs-lookup"><span data-stu-id="c7be3-104">A rating profile resembles a logistics contract (but not a legal contract).</span></span> <span data-ttu-id="c7be3-105">Sitä käytetään määrittämään kuormien kuljetusmaksut.</span><span class="sxs-lookup"><span data-stu-id="c7be3-105">It's used to determine transportation tariffs for loads.</span></span> 

<span data-ttu-id="c7be3-106">Hinnoitteluprofiilit ovat rahdinkuljettajakohtaisia.</span><span class="sxs-lookup"><span data-stu-id="c7be3-106">Each rating profile is unique to a shipping carrier.</span></span> <span data-ttu-id="c7be3-107">Hinnoitteluprofiilissa rahdinkuljettaja liitetään hinnoittelun perustietoihin.</span><span class="sxs-lookup"><span data-stu-id="c7be3-107">In the profile, you associate the shipping carrier with a rate master.</span></span> <span data-ttu-id="c7be3-108">Hinnan päätiedot määrittävät hintaperusteen määritykset ja hintaperusteen</span><span class="sxs-lookup"><span data-stu-id="c7be3-108">The rate master defines the rate base assignment and the rate base.</span></span> <span data-ttu-id="c7be3-109">Hintaperuste määrittää rahdinkuljettajan hinnan.</span><span class="sxs-lookup"><span data-stu-id="c7be3-109">The rate base determines the rate of the carrier.</span></span>

<span data-ttu-id="c7be3-110">Voit määrittää hinnoitteluprofiilin käyttämällä yleistä sivua, jossa on yhteenveto kaikista aiemmista luokituksen profiileista.</span><span class="sxs-lookup"><span data-stu-id="c7be3-110">You can set up a rating profile by using a generic page that shows an overview of all existing rating profiles.</span></span> <span data-ttu-id="c7be3-111">Vaihtoehtoisesti voit määrittää hinnoittelun profiilin suoraan lähetyksen rahdinkuljettajalta.</span><span class="sxs-lookup"><span data-stu-id="c7be3-111">Alternatively, you can set up a rating profile directly from the shipping carrier.</span></span> <span data-ttu-id="c7be3-112">Molemmissa tapauksissa hinnoitteluprofiilille määritetyt tiedot ovat samat.</span><span class="sxs-lookup"><span data-stu-id="c7be3-112">In both cases, the information that you set up for the rating profile is the same.</span></span>

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a><span data-ttu-id="c7be3-113">Hinnoitteluprofiilin luominen tai muokkaaminen Hinnoitteluprofiilit-sivulla</span><span class="sxs-lookup"><span data-stu-id="c7be3-113">Create or edit a rating profile on the Rating profiles page</span></span>

<span data-ttu-id="c7be3-114">Voit tarkastella kaikkia käytettävissä olevia hinnoitteluprofiileja **Hinnoitteluprofiilit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c7be3-114">On the **Rating profiles** page, you can review all available rating profiles.</span></span> <span data-ttu-id="c7be3-115">Voit myös muokata aiemmin luotuja profiileja ja luoda uusia profiileja.</span><span class="sxs-lookup"><span data-stu-id="c7be3-115">You can also edit existing profiles and create new profiles.</span></span>

1. <span data-ttu-id="c7be3-116">Valitse **Kuljetustenhallinta \> Määritys \> Luokitus \> Hinnoitteluprofiili**.</span><span class="sxs-lookup"><span data-stu-id="c7be3-116">Go to **Transportation management \> Setup \> Rating \> Rating profile**.</span></span>
1. <span data-ttu-id="c7be3-117">Lisää uusi hinnoitteluprofiili ruudukkoon valitsemalla toimintoruudussa **Uusi** tai muokkaa aiemmin luotua profiilia valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="c7be3-117">On the Action Pane, select **New** to add a new rating profile to the grid, or select **Edit** to edit an existing profile.</span></span>
1. <span data-ttu-id="c7be3-118">Määritä seuraavat kentät uuden tai aiemmin luodun hinnoitteluprofiilin rivillä:</span><span class="sxs-lookup"><span data-stu-id="c7be3-118">In the row for the new or existing rating profile, set the following fields:</span></span>

    - <span data-ttu-id="c7be3-119">**Hinnoitteluprofiili** – anna hinnoitteluprofiilin yksilöivä tunniste.</span><span class="sxs-lookup"><span data-stu-id="c7be3-119">**Rating profile** – Enter a unique identifier (ID) for the rating profile.</span></span>
    - <span data-ttu-id="c7be3-120">**Nimi** – anna hinnoitteluprofiilin kuvaava nimi.</span><span class="sxs-lookup"><span data-stu-id="c7be3-120">**Name** – Enter a descriptive name for the rating profile.</span></span>
    - <span data-ttu-id="c7be3-121">**Rahdinkuljettaja** – Valitse rahdinkuljettaja.</span><span class="sxs-lookup"><span data-stu-id="c7be3-121">**Shipping carrier** – Select a shipping carrier.</span></span> <span data-ttu-id="c7be3-122">Määritettävä hinnoitteluprofiili näkyy myös valitun rahdinkuljettajan **Rahdinkuljettajat**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c7be3-122">The rating profile that you're setting up will also be shown on the **Shipping carriers** page for the selected carrier.</span></span>
    - <span data-ttu-id="c7be3-123">**Toimipaikka** ja **Varasto** – valitse toimipaikka ja varasto.</span><span class="sxs-lookup"><span data-stu-id="c7be3-123">**Site** and **Warehouse** – Select a site and warehouse.</span></span>
    - <span data-ttu-id="c7be3-124">**Hinnan laskenta** – valitse hinnoitteluprofiilin hinnan laskenta.</span><span class="sxs-lookup"><span data-stu-id="c7be3-124">**Rate engine** – Select the rate engine for the rating profile.</span></span>
    - <span data-ttu-id="c7be3-125">**Hinnan päätiedot** – Valitse hinnoitteluprofiilin hinnan päätiedot.</span><span class="sxs-lookup"><span data-stu-id="c7be3-125">**Rate master** – Select the rate master for the rating profile.</span></span> <span data-ttu-id="c7be3-126">Voit käyttää hinnan päätietoja hintaperusteen tyypin ja hintaperusteen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="c7be3-126">You can use the rate master to define a rate base type and a rate base.</span></span> <span data-ttu-id="c7be3-127">Lisätietoja on kohdassa [Hinnan päätietojen määrittäminen](set-up-rate-masters.md).</span><span class="sxs-lookup"><span data-stu-id="c7be3-127">For more information, see [Set up rate masters](set-up-rate-masters.md).</span></span>
    - <span data-ttu-id="c7be3-128">**Siirtoajan laskenta** – valitse hinnoitteluprofiilin siirtoajan laskenta.</span><span class="sxs-lookup"><span data-stu-id="c7be3-128">**Transit time engine** – Select the transit time engine for the rating profile.</span></span>
    - <span data-ttu-id="c7be3-129">**Rahdinkuljettajan polttoaineindeksi** – valitse hinnoitteluprofiilin rahdinkuljettajan polttoaineindeksi.</span><span class="sxs-lookup"><span data-stu-id="c7be3-129">**Carrier fuel index** – Select the carrier fuel index for the rating profile.</span></span>
    - <span data-ttu-id="c7be3-130">**Voimaantulon aloituspäivä ja -aika** ja **Voimaantulon päättymispäivä ja -aika** – määritä jakso, jolloin hinnoitteluprofiilin on oltava aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="c7be3-130">**Effect start date and time** and **Effective end date and time** – Define the period when the rating profile should be active.</span></span>

1. <span data-ttu-id="c7be3-131">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="c7be3-131">On the Action Pane, select **Save**.</span></span>

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a><span data-ttu-id="c7be3-132">Hinnoitteluprofiilin luominen suoraan Rahdinkuljettajat-sivulla</span><span class="sxs-lookup"><span data-stu-id="c7be3-132">Create a rating profile directly on the Shipping carriers page</span></span>

1. <span data-ttu-id="c7be3-133">Valitse **Kuljetustenhallinta \> Asetukset \> Rahdinkuljettajat \> Lähetyksen rahdinkuljettajat**.</span><span class="sxs-lookup"><span data-stu-id="c7be3-133">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="c7be3-134">Valitse rahdinkuljettaja luettelossa.</span><span class="sxs-lookup"><span data-stu-id="c7be3-134">Select a shipping carrier in the list.</span></span>
1. <span data-ttu-id="c7be3-135">Luo hinnoitteluprofiili valitsemalla **Hinnoitteluprofiilit**-pikavälilehdessä **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="c7be3-135">On the **Rating profiles** FastTab, select **New** to create a rating profile.</span></span>
1. <span data-ttu-id="c7be3-136">Määritä uuden hinnoitteluprofiilin kentät.</span><span class="sxs-lookup"><span data-stu-id="c7be3-136">Set the fields for the new rating profile.</span></span> <span data-ttu-id="c7be3-137">Nämä kentät vastaavat **Hinnoitteluprofiilit**-sivun kenttiä tämän aiheen edellisessä osassa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c7be3-137">These fields correspond to the fields on the **Rating profiles** page, as described in previous section of this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="c7be3-138">**Rahdinkuljettajat**-sivulla luodut profiilit näkyvät myös **Hinnoitteluprofiilit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="c7be3-138">Profiles that are created on the **Shipping carriers** page are also shown on the **Rating profiles** page.</span></span>
