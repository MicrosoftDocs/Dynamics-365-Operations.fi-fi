---
title: Ylläpitopyynnöt
description: Tässä aiheessa on yleiskatsaus ylläpitopyyntöjen hallintaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7038269c66092367a0faf147766cb45eb5364e1b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427133"
---
# <a name="maintenance-requests"></a><span data-ttu-id="a9ad9-103">Ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="a9ad9-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a9ad9-104">Ylläpitopyynnöt ovat muistiinpanoja tai ilmoituksia, jotka on luotu ilmoittamaan esimiehlle tai suunnittelijalle, että resurssi voi edellyttää huolto- tai korjaustyötä, mutta luomatta työtilausta.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="a9ad9-105">Jos ylläpitopyynnön sisältö katsotaan kelvolliseksi, työtilaus voidaan luoda ylläpitopyynnön perusteella.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="a9ad9-106">Ylläpitopyyntöjä voi luoda mille tahansa resurssille resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="a9ad9-107">Erilaisia ylläpitopyyntöjä voidaan luoda sen mukaan, miten yrityksesi käyttää ylläpitopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="a9ad9-108">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="a9ad9-108">Here are some examples:</span></span>

- <span data-ttu-id="a9ad9-109">Ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="a9ad9-109">Maintenance requests</span></span>
- <span data-ttu-id="a9ad9-110">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="a9ad9-110">Notes</span></span>
- <span data-ttu-id="a9ad9-111">Korjaukset tai parannukset</span><span class="sxs-lookup"><span data-stu-id="a9ad9-111">Corrections or enhancements</span></span>
- <span data-ttu-id="a9ad9-112">Investoinnit</span><span class="sxs-lookup"><span data-stu-id="a9ad9-112">Investments</span></span>
- <span data-ttu-id="a9ad9-113">Varastokorjaus (tätä tyyppiä käytetään, kun vastaanotat resursseja toisesta sijainnista, jotta voit tehdä huolto- tai korjaus työn, ja palautat sitten resurssin sen jälkeen, kun työ on suoritettu loppuun.)</span><span class="sxs-lookup"><span data-stu-id="a9ad9-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="a9ad9-114">Näytä ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="a9ad9-114">View maintenance requests</span></span>

<span data-ttu-id="a9ad9-115">Näet ylläpitopyynnöt valitsemalla **resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="a9ad9-116">Kullakin luettelosivulla näkyy joitakin ylläpitopyyntöön liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Ylläpitopyyntöjen katselu](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="a9ad9-118">Käytä **Omat toiminnallisen sijainnin ylläpitopyynnöt** -luettelosivua, kun haluat tarkastella luetteloa ylläpitopyynnöistä, jotka sisältävät joko toiminnallisia sijainteja, joihin olet yhteydessä työntekijänä tai resursseja, jotka on asennettu toiminnallisiin sijainteihin, joihin olet liittynyt työntekijänä.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="a9ad9-119">(Lisätietoja toiminnalisten sijainiten määrittämisestä kunnossapitotyöntekijöille on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="a9ad9-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="a9ad9-120">Vaikka asiakastilin tiedot ovat käytettävissä resurssien palvelujen hallinnassa (ulkoinen kunnossapito), se ei ole käytettävissä resurssien hallinnassa (sisäinen kunnossapito).</span><span class="sxs-lookup"><span data-stu-id="a9ad9-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="a9ad9-121">Voit avata tietueen tietonäkymän valitsemalla **Kaikki ylläpitopyynnöt** -luettelosivun ruudukkonäkymässä **Ylläpitopyyntö**-sarakkeesta linkin.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Ylläpitopyynnön tietojen avaaminen](media/02-manage-maintenance-requests.png)

<span data-ttu-id="a9ad9-123">Toimintoruudun painikkeet on järjestetty välilehtiin.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="a9ad9-124">Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="a9ad9-125">Painikkeen nimi</span><span class="sxs-lookup"><span data-stu-id="a9ad9-125">Button name</span></span>                      | <span data-ttu-id="a9ad9-126">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a9ad9-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="a9ad9-127">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="a9ad9-127">Edit</span></span>                             | <span data-ttu-id="a9ad9-128">Muokkaa valittua ylläpitopyyntöä.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-129">Uusi</span><span class="sxs-lookup"><span data-stu-id="a9ad9-129">New</span></span>                              | <span data-ttu-id="a9ad9-130">luo uusi ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-131">Poista</span><span class="sxs-lookup"><span data-stu-id="a9ad9-131">Delete</span></span>                           | <span data-ttu-id="a9ad9-132">Poista valittu ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-133">Työtilauspooli</span><span class="sxs-lookup"><span data-stu-id="a9ad9-133">Work order pool</span></span>                  | <span data-ttu-id="a9ad9-134">Yhdistä valittu huoltopyyntö työtilauspooliin.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="a9ad9-135">Työtilaus</span><span class="sxs-lookup"><span data-stu-id="a9ad9-135">Work order</span></span>                       | <span data-ttu-id="a9ad9-136">Luo työtilaus valitun huoltopyynnön perusteella.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-137">Resurssin vika</span><span class="sxs-lookup"><span data-stu-id="a9ad9-137">Asset fault</span></span>                      | <span data-ttu-id="a9ad9-138">Valitse **Resurssin viat**, jossa voit luoda vikarekisteröinnin valittuun ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-139">Työtilaukset</span><span class="sxs-lookup"><span data-stu-id="a9ad9-139">Work orders</span></span>                      | <span data-ttu-id="a9ad9-140">Näytä luettelo kaikista työtilauksista, jotka on yhdistetty valittuun ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-141">Päivitä ylläpitopyynnön tila.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-141">Update maintenance request state</span></span> | <span data-ttu-id="a9ad9-142">Päivitä ylläpitopyynnön tila.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="a9ad9-143">Elinkaaren tilan loki</span><span class="sxs-lookup"><span data-stu-id="a9ad9-143">Lifecycle state log</span></span>              | <span data-ttu-id="a9ad9-144">Tarkastele lokia, joka näyttää valitun ylläpitopyynnön elinkaaritilat.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-145">Ylläpitopyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="a9ad9-145">Maintenance request details</span></span>      | <span data-ttu-id="a9ad9-146">Tulosta raportti, joka sisältää valitun ylläpitopyynnön tiedot.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-147">Lähetä lainattu resurssi</span><span class="sxs-lookup"><span data-stu-id="a9ad9-147">Send loan asset</span></span>                  | <span data-ttu-id="a9ad9-148">Valitse lainaresurssi, jonka pitäisi olla väliaikainen korvaava resurssi, joka on valittu valitulle ylläpitopyynnölle.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="a9ad9-149">Palauta lainaresurssi</span><span class="sxs-lookup"><span data-stu-id="a9ad9-149">Return loan asset</span></span>                | <span data-ttu-id="a9ad9-150">Rekisteröi lainaresurssi palautetuksi.</span><span class="sxs-lookup"><span data-stu-id="a9ad9-150">Register the loan asset as returned.</span></span> |

