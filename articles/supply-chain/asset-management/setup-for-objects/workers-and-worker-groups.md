---
title: Ylläpitotyöntekijät ja -työntekijäryhmät
description: Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitotyöntekijät ja -työntekijäryhmät määritetään resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0a8fcf26da02bd42f6ee45687c585091e3b945e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570975"
---
# <a name="maintenance-workers-and-worker-groups"></a><span data-ttu-id="b3fca-103">Ylläpitotyöntekijät ja -työntekijäryhmät</span><span class="sxs-lookup"><span data-stu-id="b3fca-103">Maintenance workers and worker groups</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="b3fca-104">Tässä ohjeaiheessa kerrotaan, kuinka ylläpitopitotyöntekijät ja -työntekijäryhmät määritetään resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="b3fca-104">This topic explains maintenance workers and worker groups in Asset Management.</span></span> <span data-ttu-id="b3fca-105">Resurssien hallinnassa voit liittää kunnossapitotyöntekijöitä toiminnallisiin sijainteihin.</span><span class="sxs-lookup"><span data-stu-id="b3fca-105">In Asset Management, you can connect maintenance workers to functional locations.</span></span> <span data-ttu-id="b3fca-106">(Lisätietoja toiminnallisista sijainneista on kohdassa [luo toiminnallisia sijainteja](../functional-locations/create-functional-locations.md).) Tämä toiminto voi olla hyödyllinen esimerkiksi silloin, kun olet aikatauluttamasta kunnossapitotyötä koneelle, joka sijaitsee toiminnallisessa sijainnissa 01, ja haluat kohdistaa ylläpitotyöntekijät samasta sijainnista, jotta työ voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="b3fca-106">(For more information about functional locations, see [Create functional locations](../functional-locations/create-functional-locations.md).) This functionality might be useful if, for example, you're scheduling a maintenance job on a machine that is located in functional location 01, and you want to allocate maintenance workers from the same location to perform the job.</span></span>

<span data-ttu-id="b3fca-107">Voit myös luoda kunnossapitotyöntekijäryhmiä ja liittää niitä kunnosapitotyöntekijöihin.</span><span class="sxs-lookup"><span data-stu-id="b3fca-107">You can also create maintenance worker groups and associate maintenance workers with them.</span></span> <span data-ttu-id="b3fca-108">Tästä toiminnosta on hyötyä, kun teet yksinkertaisia työtilausten ajoituksia ja haluat ajoittaa huoltotyöntekijäryhmän työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="b3fca-108">This functionality is useful when you do simple work order scheduling, and you want to schedule a group of maintenance workers on a work order.</span></span> <span data-ttu-id="b3fca-109">Kunnossapitotyöntekijöiden ja kunnossapitotyöntekijäryhmien avulla voit määrittää ensisijaisia huoltotyöntekijöitä ja vastuuvelvollisia huoltotyöntekijöitä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-109">You can use maintenance workers and maintenance worker groups to set up preferred maintenance workers and responsible maintenance workers.</span></span> 


## <a name="create-workers"></a><span data-ttu-id="b3fca-110">Luo työntekijöitä</span><span class="sxs-lookup"><span data-stu-id="b3fca-110">Create workers</span></span>

1. <span data-ttu-id="b3fca-111">Valitse **Resurssien hallinta** \> **Asetukset** \> **työntekijät** \> **työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-111">Select **Asset management** \> **Setup** \> **Workers** \> **Workers**.</span></span>
2. <span data-ttu-id="b3fca-112">Lisää uusi työntekijä luetteloon valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-112">Select **New** to add a worker to the list.</span></span>
3. <span data-ttu-id="b3fca-113">Valitse **Työntekijä**-kentässä työntekijä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-113">In the **Worker** field, select the worker.</span></span>
4. <span data-ttu-id="b3fca-114">Määritä **Aktiivinen**-asetukseksi **Kyllä**, jos haluat ajoittaa työtilaukseen työntekijän.</span><span class="sxs-lookup"><span data-stu-id="b3fca-114">Set the **Active** option to **Yes** to schedule the worker on work orders.</span></span>

    <span data-ttu-id="b3fca-115">**Yleiset**-pikavälilehdessä **Resurssi**- ja **Kuvaus**-kentät täytetään automaattisesti, jos työntekijälle on valittu resurssi.</span><span class="sxs-lookup"><span data-stu-id="b3fca-115">On the **General** FastTab, the **Resource** and **Description** fields are automatically filled in if a resource has been selected for the worker.</span></span> <span data-ttu-id="b3fca-116">**Kalenteri**-kenttä täytetään myös automaattisesti, jos olet määrittänyt työntekijän resurssiksi ja osoittanut sille kalenterin **Resurssit**-sivulla (**Organisaation hallinta** \> **Resurssit** \> **Resurssit**).</span><span class="sxs-lookup"><span data-stu-id="b3fca-116">The **Calendar** field is also automatically filled in, provided that you've set up the worker as a resource and allocated a calendar to that resource on the **Resources** page (**Organization administration** \> **Resources** \> **Resources**).</span></span>

5. <span data-ttu-id="b3fca-117">Valitse **Ryhmät**-pikavälilehdessä **Lisää** ja valitse työntekijälle kunnossapitotyöntekijäryhmä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-117">On the **Groups** FastTab, select **Add**, and then select a maintenance worker group for the worker.</span></span> <span data-ttu-id="b3fca-118">Työntekijä voidaan liittää useampaan kuin yhteen ryhmään.</span><span class="sxs-lookup"><span data-stu-id="b3fca-118">A worker can be affiliated with more than one group.</span></span>
6. <span data-ttu-id="b3fca-119">Vakiomäärityksissä työntekijän kuuluminen ryhmään on voimassa päivämäärästä, kun lisäät hänet ryhmään, eikä se vanhene koskaan.</span><span class="sxs-lookup"><span data-stu-id="b3fca-119">In the standard setup, a worker's affiliation with a group is effective from the date when you add the group, and it never expires.</span></span> <span data-ttu-id="b3fca-120">Tämä päivämäärä näkyy **Voimassa** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-120">This date is shown in the **Effective** field.</span></span> <span data-ttu-id="b3fca-121">Jos haluat nähdä **Voimassa**-kentän valitse **Näytä** \> **Kaikki**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-121">To see the **Effective** field, select **View** \> **All**.</span></span> <span data-ttu-id="b3fca-122">Jos työntekijän kuuluminen ryhmään tulisi rajoittaa tietylle kaudelle, määritä kausi käyttämällä **Voimassa**- ja **Vanhentuminen**-kenttiä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-122">If the worker's affiliation with a group should be limited to a specific period, use the **Effective** and **Expiration** fields to define the period.</span></span>
7. <span data-ttu-id="b3fca-123">Valitse **Toiminnalliset sijainnit**-pikavälilehdessä **Lisää** ja valitse ylläpitotyöntekijälle toiminnallinen sijainti.</span><span class="sxs-lookup"><span data-stu-id="b3fca-123">On the **Functional locations** FastTab, select **Add**, and then select a functional location for the maintenance worker.</span></span> <span data-ttu-id="b3fca-124">Määritä myös, mikä sijainti on työntekijän ensisijainen toiminnallinen sijainti.</span><span class="sxs-lookup"><span data-stu-id="b3fca-124">Also specify which location is the primary functional location for the worker.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b3fca-125">Kun lisäät toiminnallisia sijainteja työntekijälle, kaikki näihin toiminnallisiin sijainteihin liittyvät aktiiviset resurssit näkyvät eri valikkokohteissa, kuten **Omat aktiiviset resurssit** ja **Omat aktiiviset toiminnalliset sijainnit**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-125">When you add functional locations to a worker, all active assets that are related to those functional locations appear on various menu items, such as **My active assets** and **My active functional locations**.</span></span> <span data-ttu-id="b3fca-126">Ne näkyvät myös resurssihauissa, jotka näytetään, kun luot uuden resurssin, kunnossapitopyynnön tai työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="b3fca-126">They also appear in the asset lookups that are shown when you create a new asset, maintenance request, or work order.</span></span>

    <span data-ttu-id="b3fca-127">**Tiedot**-pikavälilehden kentissä näkyy niiden kunnossapitotyöntekijäryhmien ja toiminnallisten sijaintien määrä, joihin valittu kunnossapitotyöntekijä liittyy.</span><span class="sxs-lookup"><span data-stu-id="b3fca-127">The fields on the **Details** FastTab show the number of maintenance worker groups and functional locations that the selected maintenance worker is related to.</span></span>

## <a name="create-worker-groups"></a><span data-ttu-id="b3fca-128">Luo työntekijäryhmät</span><span class="sxs-lookup"><span data-stu-id="b3fca-128">Create worker groups</span></span>

1. <span data-ttu-id="b3fca-129">Valitse **Resurssien hallinta** \> **Asetukset** \> **Työntekijät** \> **Ylläpitotyöntekijäryhmät**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-129">Select **Asset management** \> **Setup** \> **Workers** \> **Maintenance worker groups**.</span></span>
2. <span data-ttu-id="b3fca-130">Lisää uusi työntekijäryhmä luetteloon valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-130">Select **New** to add a worker group to the list.</span></span>
3. <span data-ttu-id="b3fca-131">Kirjoita ryhmän tunnus **Ylläpitotyöntekijäryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b3fca-131">In the **Maintenance worker group** field, enter a group ID.</span></span>
4. <span data-ttu-id="b3fca-132">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b3fca-132">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="b3fca-133">Valitse **Työntekijät**-pikavälilehdessä **Lisää** ja valitse kunnossapitotyöntekijäryhmälle työntekijä.</span><span class="sxs-lookup"><span data-stu-id="b3fca-133">On the **Workers** FastTab, select **Add**, and then select a maintenance worker for the worker group.</span></span> <span data-ttu-id="b3fca-134">Lisätietoja **Voimassa**- ja **Vanheneminen**-kentistä on edellisen toimenpiteen kohdassa 6.</span><span class="sxs-lookup"><span data-stu-id="b3fca-134">For information about the **Effective** and **Expiration** fields, see step 6 in the previous procedure.</span></span>
6. <span data-ttu-id="b3fca-135">Jos resurssiryhmä liittyy valittuun kunnossapitotyöntekijäryhmään, valitse **Kopioi resurssiryhmästä**.</span><span class="sxs-lookup"><span data-stu-id="b3fca-135">If a resource group should be related to the selected maintenance worker group, select **Copy from resource group**.</span></span> <span data-ttu-id="b3fca-136">Valitse **Ryhmä**-kentässä resurssiryhmä, josta kalenteriasetukset kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="b3fca-136">In the **Group** field, select the resource group to copy calendar settings from.</span></span> <span data-ttu-id="b3fca-137">Valitse sitten **Työntekijäryhmä**-kentästä työntekijäryhmä, johon resurssiryhmän kalenteriasetukset kopioidaan.</span><span class="sxs-lookup"><span data-stu-id="b3fca-137">Then, in the **Worker group** field, select the worker group to copy the resource group's calendar settings to.</span></span> <span data-ttu-id="b3fca-138">Tämä vaihe on merkityksellinen vain, jos haluat, että kunnossapitotyöntekijät voivat käyttää resurssiin (kuormituspaikkaan) liittyvää kalenteria työtilauksen ajoittamisen aikana.</span><span class="sxs-lookup"><span data-stu-id="b3fca-138">This step is relevant only if you want maintenance workers to use the calendar that is related to a resource (work center) during work order scheduling.</span></span>

    <span data-ttu-id="b3fca-139">**Tiedot**-pikavälilehden kentissä näkyy niiden kunnossapitotyöntekijöiden määrä, jotka on määritetty valitulle kunnossapitotyöntekijäryhmälle.</span><span class="sxs-lookup"><span data-stu-id="b3fca-139">The field on the **Details** FastTab shows the number of maintenance workers that have been set up on the selected maintenance worker group.</span></span>
