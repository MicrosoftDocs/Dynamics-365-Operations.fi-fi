---
title: Vähittäismyyntikanavien määrittäminen ja ylläpitäminen
description: Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Dynamics 365 Commerceissa myymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen myymälän määrittämistä ja sen jälkeen.
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTableListPagePreviewPane
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16481
ms.assetid: 14496d96-1c72-43ce-a2e7-8467bab4ae46
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0fbca2c9178cd372653287afdf72deaf75442604
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411888"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="1e46f-104">Vähittäismyyntikanavien määrittäminen ja ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="1e46f-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e46f-105">Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Dynamics 365 Commerceissa myymälöiksi.</span><span class="sxs-lookup"><span data-stu-id="1e46f-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as stores in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1e46f-106">Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen myymälän määrittämistä ja sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="1e46f-106">It includes information about the tasks that you must complete both before and after you set up a store.</span></span>

<span data-ttu-id="1e46f-107">Commerce tukee useita kanavia, kuten verkkokauppoja, verkkokauppoja, puhelinkeskuksia ja perinteisiä myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="1e46f-107">Commerce supports multiple channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="1e46f-108">Perinteistä myymälöitä kutsutaan myymäläksi.</span><span class="sxs-lookup"><span data-stu-id="1e46f-108">A brick-and-mortar store is called a store.</span></span> <span data-ttu-id="1e46f-109">Jokaisella myymälällä voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta.</span><span class="sxs-lookup"><span data-stu-id="1e46f-109">Each store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="1e46f-110">Myymälälle on määritettävä kaikki edellä luetellut elementit, ennen kuin se voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="1e46f-110">You must set up all these elements for a store before you create it.</span></span> <span data-ttu-id="1e46f-111">Kun olet luonut myymälän, voit määrittää myymälän tuotteet.</span><span class="sxs-lookup"><span data-stu-id="1e46f-111">After you create the store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="1e46f-112">Voit myös liittää työntekijät, kassapäätteet ja asiakkaat myymälään.</span><span class="sxs-lookup"><span data-stu-id="1e46f-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="1e46f-113">Lopuksi lisäät uuden myymälän organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="1e46f-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-stores"></a><span data-ttu-id="1e46f-114">Myymälöiden määritys</span><span class="sxs-lookup"><span data-stu-id="1e46f-114">Setting up stores</span></span>

<span data-ttu-id="1e46f-115">Ennen kuin voit määrittää myymälän Commercessä, sinun on suoritettava edellytettäviä toimia.</span><span class="sxs-lookup"><span data-stu-id="1e46f-115">Before you can set up a store in Commerce, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="1e46f-116">Tämän jälkeen voit luoda myymälän ja lisätä tiedot.</span><span class="sxs-lookup"><span data-stu-id="1e46f-116">You can then create the store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="1e46f-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="1e46f-117">Prerequisites</span></span>

<span data-ttu-id="1e46f-118">Ennen kuin voit määrittää myymälän, sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="1e46f-118">You must complete the following tasks before you can set up a store:</span></span>

1. <span data-ttu-id="1e46f-119">Määritä organisaatiorakenne ja organisaation hierarkiat vähittäismyynnin valikoimille, täydennyksille ja raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="1e46f-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="1e46f-120">Määritä varasto, joka vastaa myymälää.</span><span class="sxs-lookup"><span data-stu-id="1e46f-120">Set up a warehouse that represents the store.</span></span>
3. <span data-ttu-id="1e46f-121">Myymälöiden numerosarjojen, myymälän laskelmien ja laskelman tositteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="1e46f-121">Set up number sequences for stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="1e46f-122">Commercen parametrien määritys.</span><span class="sxs-lookup"><span data-stu-id="1e46f-122">Configure parameters for Commerce.</span></span>
5. <span data-ttu-id="1e46f-123">Määritä maksutapoja, jotka myymälä hyväksyy.</span><span class="sxs-lookup"><span data-stu-id="1e46f-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="1e46f-124">Voit myös määrittää maksupalvelut prosessoimaan luottokorttitapahtumat myyntipisteen kassakoneissa.</span><span class="sxs-lookup"><span data-stu-id="1e46f-124">To process credit card transactions at POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="1e46f-125">Määritä arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="1e46f-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="1e46f-126">Määritä tuotteet.</span><span class="sxs-lookup"><span data-stu-id="1e46f-126">Set up products.</span></span> <span data-ttu-id="1e46f-127">Tässä tehtävässä määritetään myös tuotteiden hierarkiat, tuotevariantit ja tuotevalikoimat.</span><span class="sxs-lookup"><span data-stu-id="1e46f-127">As part of this task, you also set up product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="1e46f-128">Voit määrittää tuotehintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="1e46f-128">Set up product price groups.</span></span>
10. <span data-ttu-id="1e46f-129">Tuotehinnoittelujen määritys.</span><span class="sxs-lookup"><span data-stu-id="1e46f-129">Set up product pricing.</span></span> <span data-ttu-id="1e46f-130">Tässä tehtävässä määritetään myös hinnanoikaisut, alennukset ja alennuskaudet.</span><span class="sxs-lookup"><span data-stu-id="1e46f-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="1e46f-131">Henkilökunnan jäsenten määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="1e46f-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1e46f-132">Määritä myös työntekijöille soveltuvat käyttöoikeudet, joiden avulla he voivat kirjautua POS-järjestelmään ja suorittaa siellä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="1e46f-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the POS system.</span></span>

12. <span data-ttu-id="1e46f-133">Määritä myymälään liitettävät POS-profiilit.</span><span class="sxs-lookup"><span data-stu-id="1e46f-133">Configure the POS profiles to assign to the store.</span></span> <span data-ttu-id="1e46f-134">Tämä tehtävä sisältää useita tehtäviä, kuten kassapäätteiden määrittäminen, offline profiilien määrittäminen ja kuitin muodon ja profiilien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="1e46f-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="1e46f-135">Tarkastele kaikkia näihin edellytyksiin sisältyviä tehtäviä ja suorita vain tehtävät, jotka koskevat sinua.</span><span class="sxs-lookup"><span data-stu-id="1e46f-135">Review all the tasks that are included in the prerequisites, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-store"></a><span data-ttu-id="1e46f-136">Määritä myymälä</span><span class="sxs-lookup"><span data-stu-id="1e46f-136">Set up a store</span></span>

<span data-ttu-id="1e46f-137">Kun olet tehnyt edellytettävät toimet, määritä myymälän tiedot suorittamalla nämä tehtävät:</span><span class="sxs-lookup"><span data-stu-id="1e46f-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the store:</span></span>

1. <span data-ttu-id="1e46f-138">Luo myymälä.</span><span class="sxs-lookup"><span data-stu-id="1e46f-138">Create a store.</span></span>
2. <span data-ttu-id="1e46f-139">Määritä arvonlisäveroryhmä myymälälle.</span><span class="sxs-lookup"><span data-stu-id="1e46f-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="1e46f-140">Määritä hyväksytyt maksutavat myymälälle.</span><span class="sxs-lookup"><span data-stu-id="1e46f-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="1e46f-141">Lisää tietoja niiden tuotteiden tuotekuvauksiin, joita myyt myymälöissäsi.</span><span class="sxs-lookup"><span data-stu-id="1e46f-141">Add details to the product descriptions for products that you offer in your stores.</span></span> <span data-ttu-id="1e46f-142">Voit esimerkiksi lisätä rtf-tekstiä ja kuvia.</span><span class="sxs-lookup"><span data-stu-id="1e46f-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="1e46f-143">Nämä tuotetiedot näkyvät useissa paikoissa, kuten myyntipisteen kassakoneella ja tulostetuissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="1e46f-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="1e46f-144">Lisää myymälä oletusorganisaatiohierarkiaan, joka on liitetty **vähittäismyyntivalikoimaan**, **vähittäismyynnin täydennykseen** tai **vähittäismyynnin raportointiin**.</span><span class="sxs-lookup"><span data-stu-id="1e46f-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-store"></a><span data-ttu-id="1e46f-145">Kun olet määrittänyt myymälän</span><span class="sxs-lookup"><span data-stu-id="1e46f-145">After you set up a store</span></span>

<span data-ttu-id="1e46f-146">Kun olet lisännyt myymälälle tietoja, päätä tehtävät lähettämällä uudet vähittäismyymälän tiedot POS-järjestelmään:</span><span class="sxs-lookup"><span data-stu-id="1e46f-146">After you enter the details for the store, complete these tasks to send the new store data to POS:</span></span>

1. <span data-ttu-id="1e46f-147">Määritä myymälän myyntipisteiden kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="1e46f-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="1e46f-148">Määritä tuotevalikoimia myymälään.</span><span class="sxs-lookup"><span data-stu-id="1e46f-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="1e46f-149">Käsittele valikoimat luodaksesi luettelo tuotteista, jotka sisältyvät valikoimaan ja tehdäksesi tuotteet saataviksi myymälässä.</span><span class="sxs-lookup"><span data-stu-id="1e46f-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the store.</span></span>
4. <span data-ttu-id="1e46f-150">Lähetä POS-sovelluksen kassakoneille tietoja, kuten numerosarjat, laitteistojen laiteprofiilit ja myyntipisteen näytön asettelut.</span><span class="sxs-lookup"><span data-stu-id="1e46f-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the POS registers.</span></span>
5. <span data-ttu-id="1e46f-151">Julkaise myymälän tietojen lähettämiseksi POS-järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="1e46f-151">Publish the store to send store data to POS.</span></span>
6. <span data-ttu-id="1e46f-152">Suorita työt lähettääksesi myymälän tiedot POS-järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="1e46f-152">Run the jobs to send the store data to POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="1e46f-153">Organisaatiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="1e46f-153">Organization hierarchies</span></span>

<span data-ttu-id="1e46f-154">Commerce käyttää organisaatiohierarkioita määrittämään vähittäismyynnin kanavien rakenteen.</span><span class="sxs-lookup"><span data-stu-id="1e46f-154">Commerce uses organization hierarchies to structure channels.</span></span> <span data-ttu-id="1e46f-155">Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.</span><span class="sxs-lookup"><span data-stu-id="1e46f-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="1e46f-156">Kun perustat kauppoja, voit lisätä ne organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="1e46f-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="1e46f-157">Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="1e46f-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>

> [!NOTE]
> <span data-ttu-id="1e46f-158">Jos haluat käyttää Commercen myyntitoimintoa, **usean toimitusasiakkaan** konfigurointiavain on otettava käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1e46f-158">To use Commerce sales functionality, the configuration key for **Multiple ship-to** must be enabled.</span></span> <span data-ttu-id="1e46f-159">Tämä konfigurointiavain löytyy **Kaupan määritysavaimet** -osiosta kohdasta **Järjestelmänhallinta**\> **Asetukset** \> **Käyttöoikeuden määritys**.</span><span class="sxs-lookup"><span data-stu-id="1e46f-159">This configuration key can be found in the **Trade configuration** keys under **System Administration**\> **Setup** \> **License Configuration**.</span></span> <span data-ttu-id="1e46f-160">Tämä vaaditaan, koska myyntitilauksen rivitasolla määritettyjen toimitusosoitteiden perusteella suoritetaan erilaisia tarkistuksia.</span><span class="sxs-lookup"><span data-stu-id="1e46f-160">This is required due to various validations based on the delivery address configured at the sales order line level.</span></span>

