---
title: Resurssin elinkaaren tilat
description: Tässä ohjeaiheessa käsitellään resurssien elinkaaren tiloja ja elinkaarimalleja resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dffedfafd9d75320accf0e27f072bab6fd51f135
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016549"
---
# <a name="asset-lifecycle-states"></a><span data-ttu-id="4fcd0-103">Resurssin elinkaaren tilat</span><span class="sxs-lookup"><span data-stu-id="4fcd0-103">Asset lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4fcd0-104">Tässä ohjeaiheessa käsitellään resurssien elinkaaren tiloja ja elinkaarimalleja resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-104">This topic explains asset lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="4fcd0-105">Resurssien elinkaaritiloja käytetään määritettäessä, onko resurssi aktiivinen vai passiivinen.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-105">Asset lifecycle states are used to define whether an asset is active or inactive.</span></span> <span data-ttu-id="4fcd0-106">Voit esimerkiksi määrittää resurssin elinkaaritilat, kuten **Luotu**, **Aktiivinen** ja **Lopetettu**.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-106">For example, you can set up asset lifecycle states such as **Created**, **Active**, and **Terminated**.</span></span>

> [!NOTE]
> - <span data-ttu-id="4fcd0-107">Pyynnön elinkaaritilat on linkitetty resurssin elinkaaritiloihin.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-107">Request lifecycle states are linked to asset lifecycle states.</span></span> <span data-ttu-id="4fcd0-108">Tämän vuoksi, kun pyyntö muutetaan uuden pyynnön elinkaaritilaan, pyyntöön liitetty resurssi muutetaan uuteen resurssin elinkaaren tilaan.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-108">Therefore, when a request is changed to a new request lifecycle state, the asset that is attached to the request is changed to a new asset lifecycle state.</span></span> <span data-ttu-id="4fcd0-109">Jos esimerkiksi pyynnön elinkaaritilaksi muutetaan **saapuva**, liittyvän resurssin elinkaaritilaksi muutetaan **Saapuva elinkaaren tila** -kentässä valittuun elinkaaren tilaan **Resurssin elinkaaren tila** -välilehdessä **Resurssin elinkaarimallit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-109">For example, if the lifecycle state of a request is changed to **Inbound**, the lifecycle state of the attached asset is changed to the lifecycle state that is selected in the **Inbound lifecycle state** field on the **Asset lifecycle state** FastTab of the **Asset lifecycle state models** page.</span></span> 


<span data-ttu-id="4fcd0-110">Resurssin elinkaaritilat voidaan määrittää resurssien elinkaarimalleissa, jossa voit määrittää erityyppisille resursseille vaaditut elinkaaritilat.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-110">Asset lifecycle states can be set up in asset lifecycle models, where you can define the required lifecycle states for various types of assets.</span></span> <span data-ttu-id="4fcd0-111">Määrität ensin elinkaaritilat.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-111">You first set up lifecycle states.</span></span> <span data-ttu-id="4fcd0-112">Luo sitten elinkaarimalli ja valitse sen elinkaaritilat.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-112">You then create a lifecycle model and select lifecycle states for it.</span></span>

1. <span data-ttu-id="4fcd0-113">Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Elinkaaren tilat**.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-113">Select **Asset management** \> **Setup** \> **Assets** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="4fcd0-114">Luo uusi resurssin elinkaaren tila valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-114">Select **New** to create a new asset lifecycle state.</span></span>
3. <span data-ttu-id="4fcd0-115">Kirjoita **elinkaaren tila** -kenttään elinkaaren tilan tunnus.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-115">In the **Lifecycle state** field, enter the lifecycle state ID.</span></span>
4. <span data-ttu-id="4fcd0-116">Anna kuvaus **nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="4fcd0-117">**Elinkaarimallit**-kentässä näkyy niiden resurssien elinkaarimallien määrä, jotka käyttävät resurssin elinkaaritilaa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-117">The **Lifecycle models** field shows the number of asset lifecycle models that use the asset lifecycle state.</span></span>

5. <span data-ttu-id="4fcd0-118">Määritä **aktiivinen**-asetukseksi **Kyllä**, jos tämän elinkaaren tilan on oltava aktiivinen elinkaaritila (toisin sanoen, jos tässä elinkaaren tilassa oleville resursseille voidaan luoda työtilauksia).</span><span class="sxs-lookup"><span data-stu-id="4fcd0-118">Set the **Active** option to **Yes** if this lifecycle state should be an active lifecycle state (in other words, if work orders can be created for assets that are in this lifecycle state).</span></span>
6. <span data-ttu-id="4fcd0-119">Määritä **Poista avoimet kalenteririvit** -asetukseksi **Kyllä**, jos avoimet resurssikalenterin rivit, joiden resurssin elinkaaren tila on **Luotu**, poistetaan, kun ne ovat tässä elinkaaren tilassa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-119">Set the **Delete open calendar lines** option to **Yes** if open asset calendar lines that have an asset lifecycle state of **Created** should be deleted when they are in this lifecycle state.</span></span> <span data-ttu-id="4fcd0-120">Tämä asetus on hyödyllinen, jos haluat puhdistaa avoimet ylläpitoaikataulut, jotka eivät enää ole olennaisia resurssin kannalta (jos esimerkiksi resurssi ei ole enää aktiivinen).</span><span class="sxs-lookup"><span data-stu-id="4fcd0-120">This setting is useful if you want to clean up any open maintenance schedules that are no longer relevant for the asset (for example, if the asset is no longer active).</span></span>

> [!NOTE]
> <span data-ttu-id="4fcd0-121">Resurssin elinkaaritilat, resurssin elinkaarimallit ja resurssityypit liittyvät toisiinsa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-121">Asset lifecycle states, asset lifecycle models, and asset types are related.</span></span> <span data-ttu-id="4fcd0-122">Niitä käytetään samalla tavalla kuin työtilauksen elinkaaritiloja, työtilauksen elinkaarimalleja ja työtilaustyyppejä.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-122">They are used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 


<span data-ttu-id="4fcd0-123">Kun olet luonut vaaditut resurssin elinkaaritilat, voit määrittää elinkaaritilat resurssien elinkaarimalleissa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-123">After you've created the required asset lifecycle states, you can set up lifecycle states in asset lifecycle models.</span></span>

1. <span data-ttu-id="4fcd0-124">Valitse **Resurssien hallinta** \> **Asetukset** \> **resurssit** \> **Elinkaarimallit**.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-124">Select **Asset management** \> **Setup** \> **assets** \> **lifecycle models**.</span></span>
2. <span data-ttu-id="4fcd0-125">Luo uusi resurssin elinkaarimalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-125">Select **New** to create a new asset lifecycle model.</span></span>
3. <span data-ttu-id="4fcd0-126">Kirjoita **Elinkaarimalli** -kenttään elinkaarimallin tunnus.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-126">In the **Lifecycle model** field, enter the lifecycle model ID.</span></span>
4. <span data-ttu-id="4fcd0-127">Anna kuvaus **nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-127">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="4fcd0-128">**Elinkaaren tilat**-kentässä näkyy niiden resurssien elinkaaren tilojen määrä, jotka on valittu resurssin elinkaarimallissa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-128">The **Lifecycle states** field shows the number of asset lifecycle states that are selected in the asset lifecycle model.</span></span> <span data-ttu-id="4fcd0-129">**Resurssityypit**-kentässä näkyy elinkaarimallia käyttävien resurssityyppien määrä.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-129">The **Asset types** field shows the number of asset types that use the lifecycle model.</span></span>

5. <span data-ttu-id="4fcd0-130">Valitse **Elinkaaren tilat** -pikavälilehdessä ne resurssin elinkaaren tilat, jotka sisällytetään resurssi elinkaarimalliin.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-130">On the **Lifecycle states** FastTab, select the asset lifecycle states that should be included in the asset lifecycle model:</span></span>

    - <span data-ttu-id="4fcd0-131">Jos haluat käyttää mallin elinkaaritilaa, valitse se **Jäljellä olevat elinkaaren tilat** -osiosta ja siirrä se sitten **Valitut elinkaaren tilat** -osaan valitsemalla ![oikea nuoli](media/15-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="4fcd0-131">To use a lifecycle state for the model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/15-setup-for-objects.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="4fcd0-132">Jos haluat käyttää mallin kaikkia käytettävissä olevia elinkaaritiloja, valitse **Kaikki käytettävissä olevat elinkaaren tilat** -painike ![Kaikki käytettävissä olevat elinkaaren tilat](media/20-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="4fcd0-132">To use all the available lifecycle states for the model, select the **All available lifecycle states** button ![All available lifecycle states](media/20-setup-for-objects.png).</span></span> <span data-ttu-id="4fcd0-133">Kaikki elinkaaritilat siirretään **Valitut elinkaaren tilat** -osioon.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-133">All lifecycle states are transferred to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="4fcd0-134">Jos haluat poistaa elinkaaritilan mallista, valitse se **Valitut elinkaaren tilat** -osiosta ja siirrä se sitten **Jäljellä olevat elinkaaren tilat** -osaan valitsemalla ![vasen nuoli](media/16-setup-for-objects.png).</span><span class="sxs-lookup"><span data-stu-id="4fcd0-134">To remove a lifecycle state from the model, select it in the **lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/16-setup-for-objects.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="4fcd0-135">Valitse **Elinkaaren tilan päivitykset** määrittääksesi, mitkä resurssin elinkaaren tilat voivat seurata valittua elinkaaren tilaa.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-135">Select **Lifecycle state updates** to define the asset lifecycle states that can follow a selected lifecycle state.</span></span>
7. <span data-ttu-id="4fcd0-136">Voit käyttää **Resurssin tila** -pikavälilehteä, jos käsittelet resursseja, jotka vastaanotat korjattavaksi.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-136">You use the **Asset state** FastTab if you handle assets that you receive for repair.</span></span> <span data-ttu-id="4fcd0-137">**Saapuva/lähtevä**-osassa voit valita resurssin elinkaaritilat ilmaisemaan korjausta varten vastaanotetun resurssin työnkulun.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-137">In the **Inbound/outbound** section, you can select asset lifecycle states to indicate the workflow of an asset that you receive for repair.</span></span> <span data-ttu-id="4fcd0-138">Jos tarjoat lainaresursseja asiakkaille tai osastoille, **Laina**-osassa voit valita elinkaaritilat lainaresursseille.</span><span class="sxs-lookup"><span data-stu-id="4fcd0-138">If you offer loan assets to customers or departments, in the **Loan** section, you can select lifecycle states for loan assets.</span></span>
