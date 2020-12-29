---
title: Kuormituksen mallipohjat
description: Tässä aiheessa käsitellään kuormamallien määrittämistä ja kuormamallin liittämistä uuteen kuormaan.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1ea7f5244b483a1b9d6c55227c676a3878a71d83
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646384"
---
# <a name="load-templates"></a><span data-ttu-id="836d8-103">Kuormituksen mallipohjat</span><span class="sxs-lookup"><span data-stu-id="836d8-103">Load templates</span></span>

<span data-ttu-id="836d8-104">Kun luot uuden kuorman, voi määrittää kuormamallin.</span><span class="sxs-lookup"><span data-stu-id="836d8-104">When you create a new load, you can assign a load template.</span></span> <span data-ttu-id="836d8-105">Kuormamallissa on tietoja välineistä ja mitoista, kuten kuorman korkeudesta, leveydestä, syvyydestä ja tilavuudesta.</span><span class="sxs-lookup"><span data-stu-id="836d8-105">The load template contains information about equipment, and about measures such as the height, width, depth, and volume of the load.</span></span>

<span data-ttu-id="836d8-106">Tässä aiheessa käsitellään kuormamallien määrittämistä ja kuormamallin liittämistä uuteen kuormaan.</span><span class="sxs-lookup"><span data-stu-id="836d8-106">This topic describes how to set up load templates, and how to associate a load template with a new load.</span></span>

## <a name="set-up-a-load-template"></a><span data-ttu-id="836d8-107">Kuormamallien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="836d8-107">Set up a load template</span></span>

1. <span data-ttu-id="836d8-108">Valitse **Kuljetustenhallinta \> Määritys \> Kuormituksen luonti \> Kuormamalli**.</span><span class="sxs-lookup"><span data-stu-id="836d8-108">Go to **Transportation management \> Setup \> Load Building \> Load template**.</span></span>
1. <span data-ttu-id="836d8-109">Lisää uusi malli valitsemalla toimintoruudussa **Uusi** tai muokkaa aiemmin luotua mallia valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="836d8-109">On the Action Pane, select **New** to add a new template or **Edit** to edit an existing template.</span></span>
1. <span data-ttu-id="836d8-110">Määritä seuraavat kentät uuden tai aiemmin luodun mallin rivillä:</span><span class="sxs-lookup"><span data-stu-id="836d8-110">In the row for the new or existing template, set the following fields:</span></span>

    - <span data-ttu-id="836d8-111">**Kuorman mallitunnus** – anna kuormamallin yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="836d8-111">**Load template ID** – Enter a unique identifier (ID) for the load template.</span></span>
    - <span data-ttu-id="836d8-112">**Laite** – valitse laite, jota käytetään kuorman lähettämiseen.</span><span class="sxs-lookup"><span data-stu-id="836d8-112">**Equipment** – Select the equipment that should be used to ship the load.</span></span>
    - <span data-ttu-id="836d8-113">**Kuorman korkeus**, **Kuorman leveys** ja **Kuorman syvyys** – anna kuorman dimensiot.</span><span class="sxs-lookup"><span data-stu-id="836d8-113">**Load height**, **Load width**, and **Load depth** – Enter the dimensions of the load.</span></span>
    - <span data-ttu-id="836d8-114">**Kuorman suurin sallittu tilavuus** ja **Suurin sallittu kuorman paino** – anna kuorman suurin sallittu tilavuus ja paino.</span><span class="sxs-lookup"><span data-stu-id="836d8-114">**Max. allowed load volume** and **Max. allowed load weight** – Enter the maximum allowed volume and weight of the load.</span></span>
    - <span data-ttu-id="836d8-115">**Suurin sallittu bruttopaino** – Anna kuorman suurin sallittu bruttopaino.</span><span class="sxs-lookup"><span data-stu-id="836d8-115">**Maximum allowed gross weight** – Enter the maximum allowed gross weight of the load.</span></span> <span data-ttu-id="836d8-116">Kuorman bruttopaino sisältää sekä sen taarapainon että sen kuormauspainon.</span><span class="sxs-lookup"><span data-stu-id="836d8-116">A load's gross weight includes both its tare weight and its loading weight.</span></span>
    - <span data-ttu-id="836d8-117">**Suurin sallittu rahdin osien määrä** – anna suurin sallittu rahdin osien määrä, joka kuormassa voi olla.</span><span class="sxs-lookup"><span data-stu-id="836d8-117">**Maximum number of freight pieces allowed** – Enter the maximum number of freight pieces that the load can contain.</span></span>
    - <span data-ttu-id="836d8-118">**Pinoa kuorma lattialle** – Valitse tämä valintaruutu lattiakuormitusta varten</span><span class="sxs-lookup"><span data-stu-id="836d8-118">**Stack load on floor** – Select this check box to use floor loading.</span></span> <span data-ttu-id="836d8-119">Lattiakuormaskenaariossa laatikot ovat pinossa lattiasta kattoon ja seinästä seinään konttien kapasiteetin maksimoimiseksi.</span><span class="sxs-lookup"><span data-stu-id="836d8-119">In a floor loading scenario, boxes are stacked floor to ceiling and wall to wall inside the container, to maximize capacity.</span></span>

1. <span data-ttu-id="836d8-120">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="836d8-120">On the Action Pane, select **Save**.</span></span>

## <a name="associate-a-load-template-with-a-new-load"></a><span data-ttu-id="836d8-121">Kuormamallin liittäminen uuteen kuormaan</span><span class="sxs-lookup"><span data-stu-id="836d8-121">Associate a load template with a new load</span></span>

1. <span data-ttu-id="836d8-122">Valitse **Kuljetustenhallinta \> Suunnittelu \> Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="836d8-122">Go to **Transportation management \> Planning \> Load planning workbench**.</span></span>
1. <span data-ttu-id="836d8-123">Valitse sivun yläosassa jokin seuraavista välilehdistä sen perusteella, minkälaiselle lähdeasiakirjatyypille luodaan kuorma: **lähetykset**, **myyntirivit**, **siirtorivit** tai **ostotilausrivit**.</span><span class="sxs-lookup"><span data-stu-id="836d8-123">In the upper part of the page, select one of the following tabs, depending on the type of source document that you're creating a load for: **Shipments**, **Sales lines**, **Transfer lines**, or **Purchase order lines**.</span></span> 
1. <span data-ttu-id="836d8-124">Valitse tietty asiakirja, jolle kuorma suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="836d8-124">Select the specific document to plan the load for.</span></span>
1. <span data-ttu-id="836d8-125">Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="836d8-125">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span>
1. <span data-ttu-id="836d8-126">Valitse **Kuormamalli**-valintaikkunan **Kuorman mallitunnus** -kentässä käytettävä malli.</span><span class="sxs-lookup"><span data-stu-id="836d8-126">In the **Load template** dialog box, in the **Load template ID** field, select the template to apply.</span></span>
1. <span data-ttu-id="836d8-127">Käytä mallia valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="836d8-127">Select **OK** to apply the template.</span></span>
