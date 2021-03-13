---
title: Ylläpitopyynnön elinkaaren tilat
description: Tässä ohjeaiheessa kuvataan, kuinka ylläpitopitopyynnön elinkaaren tilat määritetään resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d3c2f717969b938d05e68ac775d31b6a5d5ec26a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022077"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="2186c-103">Ylläpitopyynnön elinkaaritilat</span><span class="sxs-lookup"><span data-stu-id="2186c-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="2186c-104">Huoltopyynnön elinkaaritilat määrittävät vaiheet, jotka pyyntö voi käydä läpi.</span><span class="sxs-lookup"><span data-stu-id="2186c-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="2186c-105">Esimerkkejä ovat **Luotu**, **Aktiivinen** ja **Päättynyt**.</span><span class="sxs-lookup"><span data-stu-id="2186c-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="2186c-106">Kun ylläpitopyyntö muunnetaan työtilaukseksi, kunnossapitopyynnön elinkaaren tilaksi päivitetään **Päättynyt** tai **Suljettu**, mikä osoittaa, että ylläpitopyyntö ei ole enää aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="2186c-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="2186c-107">**Kaikki ylläpitopyynnöt** -luettelosivulla näkyvät kaikki ylläpitopyynnöt niiden elinkaaritilasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="2186c-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="2186c-108">Ylläpitopyynnön elinkaaren tilojen määritys</span><span class="sxs-lookup"><span data-stu-id="2186c-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="2186c-109">Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Elinkaaren tilat**.</span><span class="sxs-lookup"><span data-stu-id="2186c-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="2186c-110">Luo ylläpitopyynnön elinkaaren tila valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2186c-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="2186c-111">Kirjoita **Elinkaaren tila** -kenttään elinkaaren tilan tunnus.</span><span class="sxs-lookup"><span data-stu-id="2186c-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="2186c-112">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2186c-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="2186c-113">**Tiedot**-pikavälilehden **Elinkaarimallit**-kentässä näkyy niiden ylläpitopyyntöjen elinkaarimallien määrä, jotka käyttävät tätä elinkaaritilaa.</span><span class="sxs-lookup"><span data-stu-id="2186c-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="2186c-114">Määritä **Yleiset**-pikavälilehdessä **Aktiivinen**-asetukseksi **Kyllä**, jos ylläpitopyynnön pitäisi olla aktiivinen, kun se on tässä elinkaaren tilassa.</span><span class="sxs-lookup"><span data-stu-id="2186c-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="2186c-115">Määritä, **Määritä todellinen lopetus** -asetukseksi **Kyllä**, jos todellinen päättymispäivä ja-aika tulee automaattisesti syöttää ylläpitopyyntöön, joka on tässä elinkaaren tilassa.</span><span class="sxs-lookup"><span data-stu-id="2186c-115">Set the **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="2186c-116">Määritä **luo työtilaus** -asetukseksi **Kyllä**, jos työtilauksen voi luoda ylläpitopyynnöstä, joka on tässä elinkaaren tilassa.</span><span class="sxs-lookup"><span data-stu-id="2186c-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="2186c-117">Määritä **Poista**-asetukseksi **Kyllä**, jos ylläpitopyyntö voidaan poistaa, kun se on tässä elinkaaren tilassa.</span><span class="sxs-lookup"><span data-stu-id="2186c-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="2186c-118">**Päivitä**-pikavälilehdessä **käyttöomaisuus**-osan **saapuvat** ja **lähtevät** asetukset ovat olennaisia, jos käytät varaston korjausta.</span><span class="sxs-lookup"><span data-stu-id="2186c-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.</span></span> <span data-ttu-id="2186c-119">Määritä sopiva vaihtoehto **Kyllä**, jos ylläpitopyynnössä valittujen käyttöomaisuuserien elinkaaren tila päivitetään automaattisesti **saapuvaan** tai **lähtevään** tilaan, kun ylläpitopyynnön elinkaaritilaksi määritetään **saapuva** tai **lähtevä**.</span><span class="sxs-lookup"><span data-stu-id="2186c-119">Set the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="2186c-120">Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön elinkaaren tilat** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="2186c-120">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Ylläpitopyynnön elinkaaritilasivu](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="2186c-122">Huoltopyynnön elinkaaritilat, elinkaaren tilaryhmät ja -tyypit liittyvät toisiinsa ja niitä käytetään samalla tavalla kuin työtilauksen elinkaaritiloja, elinkaaren tilaryhmiä ja -tyyppejä.</span><span class="sxs-lookup"><span data-stu-id="2186c-122">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="2186c-123">Ylläpitopyynnön elinkaarimallien määritys</span><span class="sxs-lookup"><span data-stu-id="2186c-123">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="2186c-124">Kun olet luonut kunnossapitopyynnöille tarvittavat elinkaaritilat, ne voidaan jakaa elinkaaren tilaryhmiin tai elinkaarimalleihin.</span><span class="sxs-lookup"><span data-stu-id="2186c-124">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="2186c-125">Huoltopyynnön elinkaarimallien avulla luodaan työnkulku, jota voidaan käyttää erityyppisissä ylläpitopyynnöissä.</span><span class="sxs-lookup"><span data-stu-id="2186c-125">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="2186c-126">Vähintään yksi ylläpitopyynnön vakioelinkaarimalli on luotava.</span><span class="sxs-lookup"><span data-stu-id="2186c-126">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="2186c-127">Valitse **Resurssien hallinta** \> **Asetukset** \> **Ylläpitopyynnöt** \> **Elinkaarimallit**.</span><span class="sxs-lookup"><span data-stu-id="2186c-127">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="2186c-128">Luo ylläpitopyynnön elinkaarimalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2186c-128">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="2186c-129">Kirjoita **Elinkaarimalli** -kenttään elinkaarimallin tunnus.</span><span class="sxs-lookup"><span data-stu-id="2186c-129">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="2186c-130">Anna nimi **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="2186c-130">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="2186c-131">**Tiedot**-välilehden **Elinkaaren tilat**-kentässä näkyy niiden elinkaaren tilojen määrä, jotka on valittu tässä elinkaarimallissa.</span><span class="sxs-lookup"><span data-stu-id="2186c-131">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="2186c-132">**Ylläpitopyynnön tyypit**-kentässä näkyy tätä elinkaarimallia käyttävien ylläpitopyynnön tyyppien määrä.</span><span class="sxs-lookup"><span data-stu-id="2186c-132">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="2186c-133">Valitse **Elinkaaren tilat** -pikavälilehdessä ne elinkaaren tilat, jotka sisällytetään elinkaarimalliin.</span><span class="sxs-lookup"><span data-stu-id="2186c-133">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="2186c-134">Jos haluat lisätä elinkaaritilan elinkaarimalliin, valitse se **Jäljellä olevat elinkaaren tilat** -osiosta ja siirrä se sitten **Valitut elinkaaren tilat** -osaan valitsemalla ![oikea nuoli](media/03-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="2186c-134">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="2186c-135">Jos haluat lisätä kaikki käytettävissä olevat elinkaaritilat elinkaarimalliin, valitse **Valitse kaikki käytettävissä olevat tilat** -painike ![Valitse kaikki käytettävissä olevat tilat](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="2186c-135">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="2186c-136">Kaikki elinkaaritilat siirretään **Valitut elinkaaren tilat** -osioon.</span><span class="sxs-lookup"><span data-stu-id="2186c-136">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="2186c-137">Jos haluat poistaa elinkaaritilan elinkaarimallista, valitse se **Valitut elinkaaren tilat** -osiosta ja siirrä se sitten **Jäljellä olevat elinkaaren tilat** -osaan valitsemalla ![vasen nuoli](media/05-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="2186c-137">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="2186c-138">**Yleiset**-pikavälilehden **Päivitykset**-osion kentät ovat merkityksellisiä, jos käytät varastokorjausta.</span><span class="sxs-lookup"><span data-stu-id="2186c-138">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="2186c-139">Valitse **Vastaanotetun resurssin elinkaaren tila** -kentässä resurssin elinkaaren tila, johon ylläpitopyynnössä valitut resurssit päivitetään automaattisesti, kun ne vastaanotetaan varastokorjausta varten.</span><span class="sxs-lookup"><span data-stu-id="2186c-139">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="2186c-140">Valitse **Toimitetun resurssin elinkaaren tila** -kentässä resurssin elinkaaren tila, johon ylläpitopyynnössä valitut resurssit päivitetään automaattisesti, kun ne palautetaan korjauksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="2186c-140">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="2186c-141">Seuraavassa kuvassa on esimerkki **Ylläpitopyynnön elinkaarimallit** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="2186c-141">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Ylläpitopyynnön elinkaarimallisivu](media/06-setup-for-requests.png)
