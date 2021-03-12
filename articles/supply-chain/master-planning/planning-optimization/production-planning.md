---
title: Tuotannon suunnittelu
description: Tässä aiheessa käsitellään tuotannon suunnittelua ja suunniteltujen tuotantotilausten muokkaamista tuotannon optimoinnin avulla.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992392"
---
# <a name="production-planning"></a><span data-ttu-id="bb874-103">Tuotannon suunnittelu</span><span class="sxs-lookup"><span data-stu-id="bb874-103">Production planning</span></span>

<span data-ttu-id="bb874-104">Suunnittelun optimointi tukee useita tuotantoskenaarioita.</span><span class="sxs-lookup"><span data-stu-id="bb874-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="bb874-105">Jos siirtyminen tapahtuu nykyisestä sisäisestä pääsuunnittelumoduulista, on tärkeää ottaa huomioon tietyt toiminnasta tapahtuneet muutokset.</span><span class="sxs-lookup"><span data-stu-id="bb874-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="bb874-106">Suunnitellut tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="bb874-106">Planned production orders</span></span>

<span data-ttu-id="bb874-107">Kun pääsuunnittelu täyttää tarpeita luomalla suunniteltuja tilauksia, tilauksen tyyppi määritetään **Suunniteltu tilaustyyppi** -kentän arvon perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb874-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="bb874-108">Jos **Suunniteltu tilaustyyppi** -kentän asetuksena on *Tuotanto*, luodaan suunniteltuja tuotantotilauksia.</span><span class="sxs-lookup"><span data-stu-id="bb874-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="bb874-109">Näissä suunnitelluissa tuotantotilauksissa on tietoja aktiivisista tuoterakenteista ja liittyvän tuotantomäärityksen reititystunnus.</span><span class="sxs-lookup"><span data-stu-id="bb874-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="bb874-110">Tuoterakenteiden tarpeet</span><span class="sxs-lookup"><span data-stu-id="bb874-110">Requirements from BOMs</span></span>

<span data-ttu-id="bb874-111">Tuoterakennetiedot otetaan huomioon pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="bb874-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="bb874-112">Suunnittelutulos sisältää materiaalin oston, joka kattaa tuotantoon liittyvän materiaalin kysynnän.</span><span class="sxs-lookup"><span data-stu-id="bb874-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="bb874-113">Pääsuunnittelun aikana nykyisen aktiivisen tuoterakenteen avulla määritetään tuotantoa varten tarvittavat materiaalit.</span><span class="sxs-lookup"><span data-stu-id="bb874-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="bb874-114">Tämä vaihe tehdään kaikilla tarvittavaan tuotantotilaukseen liittyvillä tuoterakenteen tasoilla.</span><span class="sxs-lookup"><span data-stu-id="bb874-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="bb874-115">Materiaalitarve täytetään käyttämällä käytettävissä olevaa varastoa, nykyistä tilausvarastoa ja hyväksyttyjä suunniteltuja tilauksia.</span><span class="sxs-lookup"><span data-stu-id="bb874-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="bb874-116">Jos jossakin tarvitaan lisämateriaalia, kysyntää varten luodaan suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="bb874-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="bb874-117">Aikatauluttaminen vahvistuksen aikana</span><span class="sxs-lookup"><span data-stu-id="bb874-117">Scheduling during firming</span></span>

<span data-ttu-id="bb874-118">Suunnitellut tuotantotilaukset sisältävä reititystunnuksen, jota tarvitaan tuotannon aikatauluttamiseen.</span><span class="sxs-lookup"><span data-stu-id="bb874-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="bb874-119">Suunniteltujen tilausten aikataulutuksen tukea suunnitteluajon aikana odotetaan.</span><span class="sxs-lookup"><span data-stu-id="bb874-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="bb874-120">Reititystunnusta käytetään suunniteltujen tuotantotilausten aikatauluttamiseen vahvistuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="bb874-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="bb874-121">Tämän vuoksi suunniteltujen tuotantotilausten läpimenoaika voi olla erilainen kuin niistä luotujen liittyvien aikataulutettujen ja vahvistettujen tuotantotilausten läpimenoaika. Selitys:</span><span class="sxs-lookup"><span data-stu-id="bb874-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="bb874-122">**Suunniteltu tuotantotilaus** – läpimenoaika perustuu vapautetun tuotteen staattiseen läpimenoaikaan.</span><span class="sxs-lookup"><span data-stu-id="bb874-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="bb874-123">**Vahvistettu tuotantotilaus** – läpimenoaika perustuu reititystietoja ja liittyviä resurssirajoituksia käyttävään aikataulutukseen.</span><span class="sxs-lookup"><span data-stu-id="bb874-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="bb874-124">Lisätietoja toiminnon odotetusta saatavuudesta on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bb874-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="bb874-125">Jos tarvitset sellaista tuotannon toimintoa, joka ei ole vielä saatavana tuotannon optimoinnissa, voit jatkaa sisäisen pääsuunnittelumoduulin käyttöä.</span><span class="sxs-lookup"><span data-stu-id="bb874-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="bb874-126">Mitään poikkeusta ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="bb874-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="bb874-127">Viiveet</span><span class="sxs-lookup"><span data-stu-id="bb874-127">Delays</span></span>

<span data-ttu-id="bb874-128">Jos tarvittavan materiaalin läpimenoaika on pidempi kuin kuluvan päivän ja materiaalin tarvepäivän väliin jäävä jakso, tarvittavan materiaalin ja liittyvän tuotantotilauksen suunniteltu tilaus viivästyy.</span><span class="sxs-lookup"><span data-stu-id="bb874-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="bb874-129">Viive lasketaan suunnitelluissa tilauksissa vapautetun tuotteen läpimenoajan perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb874-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="bb874-130">Tämän jälkeen viivetiedot leviävät sitten kaikille tuoterakenteen tasoille.</span><span class="sxs-lookup"><span data-stu-id="bb874-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="bb874-131">Tällä tavoin viivästyneen raaka-aineen vaikutusta voidaan seurata asiakkaan myyntitilaukseen saakka.</span><span class="sxs-lookup"><span data-stu-id="bb874-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="bb874-132">Suunniteltujen tilausten muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="bb874-132">Modifying planned orders</span></span>

<span data-ttu-id="bb874-133">Suunnitellun tilauksen tietojen muuttaminen aiheuttaa seuraavan sanoman: Huomaa, että suunniteltujen tilausten manuaaliset muutokset näkyvät muualla suunnitelmassa vasta seuraavan pääsuunnitteluajon jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bb874-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="bb874-134">Suunniteltuun tilaukseen tehdyn muutoksen vaikutus liittyviin materiaalitarpeisiin saadaan näkyviin seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="bb874-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="bb874-135">Päivitä suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="bb874-135">Update the planned order.</span></span>
2. <span data-ttu-id="bb874-136">Hyväksy suunniteltu tilaus.</span><span class="sxs-lookup"><span data-stu-id="bb874-136">Approve the planned order.</span></span>
3. <span data-ttu-id="bb874-137">Suorita pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="bb874-137">Run master planning.</span></span>

<span data-ttu-id="bb874-138">Jos suunnitellut tuotantotilaukset sisältyvät suoritettavaan pääsuunnitteluun, suodattimia ei voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="bb874-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="bb874-139">Lisätietoja on myöhemmin tässä aiheessa kohdassa [Suodattimet](#filters).</span><span class="sxs-lookup"><span data-stu-id="bb874-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="bb874-140">Jos suunnitellun tilauksen toimituspäivä muutetaan myöhempään ajankohtaan, tarvekohdistus saatetaan tehdä uuden suunnitellun tilauksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="bb874-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="bb874-141">Näin tapahtuu, jos uusi tarjontapäivä viivästyttää tarvekohdistusta mutta läpimenoasetusten perusteella viive voidaan välttää.</span><span class="sxs-lookup"><span data-stu-id="bb874-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="bb874-142">Hajotussivu</span><span class="sxs-lookup"><span data-stu-id="bb874-142">Explosion page</span></span>

<span data-ttu-id="bb874-143">**Hajotus**-sivulla voidaan analysoida tietyn tuotantotilauksen tai suunnitellun tuotantotilauksen, liittyvän kattavuuden ja tarvekohdistustietojen kysyntää.</span><span class="sxs-lookup"><span data-stu-id="bb874-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="bb874-144">**Hajotus**-sivun tiedot päivitetään pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="bb874-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="bb874-145">Tietoja ei voi päivittää suoraan **Hajotus**-sivulta.</span><span class="sxs-lookup"><span data-stu-id="bb874-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="bb874-146">Suodattimet</span><span class="sxs-lookup"><span data-stu-id="bb874-146">Filters</span></span>

<span data-ttu-id="bb874-147">Tuotannon sisältävissä suunnitteluskenaarioissa ei kannata käyttää suodatettuja pääsuunnitteluajoja,</span><span class="sxs-lookup"><span data-stu-id="bb874-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="bb874-148">Jotta suunnittelun optimoinnilla on varmasti kaikki tiedot, joita tarvitaan oikean tuloksen laskemiseen, siihen on sisällyttävä kaikki tuotteet, jotka liittyvät jollain tavoin koko suunnitellun tilauksen tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="bb874-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="bb874-149">Vaikka riippuvaiset alikohteet havaitaan automaattisesti ja sisällytetään pääsuunnitteluajoihin sisäistä pääsuunnittelumoduulia käytettäessä, niin ei tapahdu suunnittelun optimoinnissa.</span><span class="sxs-lookup"><span data-stu-id="bb874-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="bb874-150">Jos esimerkiksi yhtä tuotteen A tuoterakenteen pulttia käytetään myös tuotteen B tuottamiseen, kaikkien tuotteiden A ja B tuoterakenteiden tuotteiden on sisällyttävä suodattimeen.</span><span class="sxs-lookup"><span data-stu-id="bb874-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="bb874-151">Koska voi olla erittäin monimutkaista varmistaa, että kaikki tuotteet sisältyvät suodattimeen, suodatettuja pääsuunnitteluajoja kannattaa välttää, jos kyse on tuotantotilauksesta.</span><span class="sxs-lookup"><span data-stu-id="bb874-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
