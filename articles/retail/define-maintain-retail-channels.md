---
title: Vähittäismyyntikanavien määrittäminen ja ylläpitäminen
description: Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Microsoft Dynamics 365 for Retailissa vähittäismyymälöiksi. Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen vähittäismyymälän määrittämistä ja sen jälkeen.
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: 53ba6cdb2378ce9011c6e7e3ce4e67c789adb1e6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "318623"
---
# <a name="define-and-maintain-retail-channels"></a><span data-ttu-id="43058-104">Vähittäismyyntikanavien määrittäminen ja ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="43058-104">Define and maintain retail channels</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43058-105">Tämä ohjeaihe sisältää perinteisten myymälöiden määrittämisprosessin yleiskatsauksen. Perinteisiä myymälöitä kutsutaan Microsoft Dynamics 365 for Retailissa vähittäismyymälöiksi.</span><span class="sxs-lookup"><span data-stu-id="43058-105">This topic provides an overview of the process for setting up brick-and-mortar stores, which are referred to as retail stores in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="43058-106">Artikkeli sisältää myös tietoja tehtävistä, jotka on suoritettava ennen vähittäismyymälän määrittämistä ja sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="43058-106">It includes information about the tasks that you must complete both before and after you set up a retail store.</span></span>

<span data-ttu-id="43058-107">Dynamics 365 for Retail tukee useita vähittäismyynnin kanavia, kuten verkkokauppoja, verkkokauppoja, puhelinkeskuksia ja perinteisiä myymälöitä.</span><span class="sxs-lookup"><span data-stu-id="43058-107">Dynamics 365 for Retail supports multiple retail channels, such as online stores, call centers, and brick-and-mortar stores.</span></span> <span data-ttu-id="43058-108">Perinteistä myymälöitä kutsutaan vähittäismyymäläksi.</span><span class="sxs-lookup"><span data-stu-id="43058-108">A brick-and-mortar store is called a retail store.</span></span> <span data-ttu-id="43058-109">Jokaisella vähittäismyymälällä voi olla omat maksuvälineet, hintaryhmät, kassakoneet, tulo- ja kulutilit sekä oma henkilökunta.</span><span class="sxs-lookup"><span data-stu-id="43058-109">Each retail store can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="43058-110">Vähittäismyymälälle on määritettävä kaikki edellä luetellut elementit, ennen kuin se voidaan luoda.</span><span class="sxs-lookup"><span data-stu-id="43058-110">You must set up all these elements for a retail store before you create it.</span></span> <span data-ttu-id="43058-111">Kun olet luonut vähittäismyymälän, voit määrittää myymälän tuotteet.</span><span class="sxs-lookup"><span data-stu-id="43058-111">After you create the retail store, you assign the products that you want it to carry.</span></span> <span data-ttu-id="43058-112">Voit myös liittää työntekijät, kassapäätteet ja asiakkaat myymälään.</span><span class="sxs-lookup"><span data-stu-id="43058-112">You also assign employees, registers, and customers to the store.</span></span> <span data-ttu-id="43058-113">Lopuksi lisäät uuden myymälän organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="43058-113">Finally, you add the new store to an organization hierarchy.</span></span>

## <a name="setting-up-retail-stores"></a><span data-ttu-id="43058-114">Vähittäismyynnin varastojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="43058-114">Setting up retail stores</span></span>

<span data-ttu-id="43058-115">Ennen kuin voit määrittää vähittäismyymälän Dynamics 365 for Retailissa, sinun on suoritettava edellytettäviä toimia.</span><span class="sxs-lookup"><span data-stu-id="43058-115">Before you can set up a retail store in Dynamics 365 for Retail, you must complete some prerequisite tasks.</span></span> <span data-ttu-id="43058-116">Tämän jälkeen voit luoda vähittäismyymälän ja lisätä tiedot.</span><span class="sxs-lookup"><span data-stu-id="43058-116">You can then create the retail store and add details.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="43058-117">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="43058-117">Prerequisites</span></span>

<span data-ttu-id="43058-118">Ennen kuin voit määrittää vähittäismyymälän, sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="43058-118">You must complete the following tasks before you can set up a retail store:</span></span>

1. <span data-ttu-id="43058-119">Määritä organisaatiorakenne ja organisaation hierarkiat vähittäismyynnin valikoimille, täydennyksille ja raportointia varten.</span><span class="sxs-lookup"><span data-stu-id="43058-119">Configure your organization structure, and set up organization hierarchies for retail assortments, replenishment, and reporting.</span></span>
2. <span data-ttu-id="43058-120">Määritä varasto, joka vastaa vähittäismyyntiliikettä.</span><span class="sxs-lookup"><span data-stu-id="43058-120">Set up a warehouse that represents the retail store.</span></span>
3. <span data-ttu-id="43058-121">Vähittäismyynnin myymälöiden numerosarjojen, myymälän laskelmien ja laskelman tositteiden määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="43058-121">Set up number sequences for retail stores, store statements, and statement vouchers.</span></span>
4. <span data-ttu-id="43058-122">Määritä Retail-parametrit.</span><span class="sxs-lookup"><span data-stu-id="43058-122">Configure parameters for Retail.</span></span>
5. <span data-ttu-id="43058-123">Määritä maksutapoja, jotka myymälä hyväksyy.</span><span class="sxs-lookup"><span data-stu-id="43058-123">Set up the methods of payment that the store accepts.</span></span>
6. <span data-ttu-id="43058-124">Voit myös määrittää maksupalvelut prosessoimaan luottokorttitapahtumat Retail POS -kassakoneissa.</span><span class="sxs-lookup"><span data-stu-id="43058-124">To process credit card transactions at retail POS registers, you can also set up payment services.</span></span>
7. <span data-ttu-id="43058-125">Määritä arvonlisäveroryhmät.</span><span class="sxs-lookup"><span data-stu-id="43058-125">Set up sales tax groups.</span></span>
8. <span data-ttu-id="43058-126">Aseta vähittäismyyntituotteet.</span><span class="sxs-lookup"><span data-stu-id="43058-126">Set up retail products.</span></span> <span data-ttu-id="43058-127">Tässä tehtävässä määritetään myös vähittäismyyntituotteiden hierarkiat, tuotevariantit ja tuotevalikoimat.</span><span class="sxs-lookup"><span data-stu-id="43058-127">As part of this task, you also set up retail product hierarchies, product variants, and product assortments.</span></span>
9. <span data-ttu-id="43058-128">Voit määrittää tuotehintaryhmät.</span><span class="sxs-lookup"><span data-stu-id="43058-128">Set up product price groups.</span></span>
10. <span data-ttu-id="43058-129">Määritä vähittäismyynnin tuotteiden hinnoittelu.</span><span class="sxs-lookup"><span data-stu-id="43058-129">Set up retail product pricing.</span></span> <span data-ttu-id="43058-130">Tässä tehtävässä määritetään myös hinnanoikaisut, alennukset ja alennuskaudet.</span><span class="sxs-lookup"><span data-stu-id="43058-130">As part of this task, you also set up price adjustments, discounts, and discount periods.</span></span>
11. <span data-ttu-id="43058-131">Henkilökunnan jäsenten määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="43058-131">Set up staff members.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43058-132">Määritä myös työntekijöille soveltuvat käyttöoikeudet, joiden avulla he voivat kirjautua Dynamics 365 for Retail for Retail POS -järjestelmään ja suorittaa siellä tehtäviä.</span><span class="sxs-lookup"><span data-stu-id="43058-132">You must also assign appropriate permissions to the workers, so that they can sign in and perform tasks by using the Dynamics 365 for Retail for Retail POS system.</span></span>

12. <span data-ttu-id="43058-133">Määritä myymälään liitettävät Retail POS -profiilit.</span><span class="sxs-lookup"><span data-stu-id="43058-133">Configure the Retail POS profiles to assign to the store.</span></span> <span data-ttu-id="43058-134">Tämä tehtävä sisältää useita tehtäviä, kuten kassapäätteiden määrittäminen, offline profiilien määrittäminen ja kuitin muodon ja profiilien määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="43058-134">This task includes many other tasks, such as setting up registers, setting up offline profiles, and setting up receipt formats and profiles.</span></span>

<span data-ttu-id="43058-135">Tarkastele kaikkia näihin edellytyksiin sisältyviä tehtäviä ja suorita vain tehtävät, jotka koskevat sinua.</span><span class="sxs-lookup"><span data-stu-id="43058-135">Review all the tasks that are included in the prerequisite, and complete only the tasks that apply to you.</span></span>

### <a name="set-up-a-retail-store"></a><span data-ttu-id="43058-136">Aseta vähittäismyyntiliike</span><span class="sxs-lookup"><span data-stu-id="43058-136">Set up a retail store</span></span>

<span data-ttu-id="43058-137">Kun olet tehnyt edellytettävät toimet, määritä vähittäismyymälän tiedot suorittamalla nämä tehtävät:</span><span class="sxs-lookup"><span data-stu-id="43058-137">After you complete the prerequisite tasks, complete these tasks to set up the details for the retail store:</span></span>

1. <span data-ttu-id="43058-138">Luo vähittäismyymälä.</span><span class="sxs-lookup"><span data-stu-id="43058-138">Create a retail store.</span></span>
2. <span data-ttu-id="43058-139">Määritä arvonlisäveroryhmä myymälälle.</span><span class="sxs-lookup"><span data-stu-id="43058-139">Assign a sales tax group to the store.</span></span>
3. <span data-ttu-id="43058-140">Määritä hyväksytyt maksutavat myymälälle.</span><span class="sxs-lookup"><span data-stu-id="43058-140">Assign the accepted payment methods to the store.</span></span>
4. <span data-ttu-id="43058-141">Lisää tietoja niiden tuotteiden tuotekuvauksiin, joita myyt myymälöissäsi.</span><span class="sxs-lookup"><span data-stu-id="43058-141">Add details to the product descriptions for products that you offer in your retail stores.</span></span> <span data-ttu-id="43058-142">Voit esimerkiksi lisätä rtf-tekstiä ja kuvia.</span><span class="sxs-lookup"><span data-stu-id="43058-142">For example, you can add rich text and images.</span></span> <span data-ttu-id="43058-143">Nämä tuotetiedot näkyvät useissa paikoissa, kuten myyntipisteen kassakoneella ja tulostetuissa etiketeissä.</span><span class="sxs-lookup"><span data-stu-id="43058-143">These product details appear in various contexts, such as on the POS register or on printed labels.</span></span>
5. <span data-ttu-id="43058-144">Lisää myymälä oletusorganisaatiohierarkiaan, joka on liitetty **vähittäismyyntivalikoimaan**, **vähittäismyynnin täydennykseen** tai **vähittäismyynnin raportointiin**.</span><span class="sxs-lookup"><span data-stu-id="43058-144">Add the store to the default organization hierarchy that is assigned to a purpose of **Retail assortment**, **Retail replenishment**, or **Retail reporting**.</span></span>

### <a name="after-you-set-up-a-retail-store"></a><span data-ttu-id="43058-145">Kun olet määrittänyt myymälän</span><span class="sxs-lookup"><span data-stu-id="43058-145">After you set up a retail store</span></span>

<span data-ttu-id="43058-146">Kun olet lisännyt vähittäismyymälälle tietoja, päätä tehtävät lähettämällä uudet vähittäismyymälän tiedot Retail POS -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="43058-146">After you enter the details for the retail store, complete these tasks to send the new retail store data to Retail POS:</span></span>

1. <span data-ttu-id="43058-147">Määritä myymälän myyntipisteiden kassakoneet.</span><span class="sxs-lookup"><span data-stu-id="43058-147">Configure the POS registers for the store.</span></span>
2. <span data-ttu-id="43058-148">Määritä tuotevalikoimia myymälään.</span><span class="sxs-lookup"><span data-stu-id="43058-148">Assign product assortments to the store.</span></span>
3. <span data-ttu-id="43058-149">Käsittele valikoimat luodaksesi luettelo tuotteista, jotka sisältyvät valikoimaan ja tehdäksesi tuotteet saataviksi vähittäismyymälässä.</span><span class="sxs-lookup"><span data-stu-id="43058-149">Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store.</span></span>
4. <span data-ttu-id="43058-150">Lähetä Retail POS -sovelluksen kassakoneille tietoja, kuten numerosarjat, laitteistojen laiteprofiilit ja myyntipisteen näytön asettelut.</span><span class="sxs-lookup"><span data-stu-id="43058-150">Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.</span></span>
5. <span data-ttu-id="43058-151">Julkaise vähittäismyymälä lähettääksesi myymälän tietoja Retail POS -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="43058-151">Publish the retail store to send store data to Retail POS.</span></span>
6. <span data-ttu-id="43058-152">Suorita työt lähettääksesi myymälän Retail POS -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="43058-152">Run the jobs to send the store data to Retail POS.</span></span>

## <a name="organization-hierarchies"></a><span data-ttu-id="43058-153">Organisaatiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="43058-153">Organization hierarchies</span></span>

<span data-ttu-id="43058-154">Retail määrittää vähittäismyyntikanavien rakenteen organisaatiohierarkioiden avulla.</span><span class="sxs-lookup"><span data-stu-id="43058-154">Retail uses organization hierarchies to structure retail channels.</span></span> <span data-ttu-id="43058-155">Organisaatiohierarkiat edustavat liiketoimintasi muodostavien organisaatioiden välisiä suhteita.</span><span class="sxs-lookup"><span data-stu-id="43058-155">Organization hierarchies represent the relationships between the organizations that make up your business.</span></span> <span data-ttu-id="43058-156">Kun perustat kauppoja, voit lisätä ne organisaatiohierarkiaan.</span><span class="sxs-lookup"><span data-stu-id="43058-156">When you set up stores, you can add them to an organization hierarchy.</span></span> <span data-ttu-id="43058-157">Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot.</span><span class="sxs-lookup"><span data-stu-id="43058-157">The stores then share data that is used for assortments, replenishment, and reporting.</span></span>
