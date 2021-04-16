---
title: Ylläpitopyynnöt
description: Tässä aiheessa on yleiskatsaus ylläpitopyyntöjen hallintaan resurssien hallinnassa.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestTable, EntAssetRequestWorkspace, EntAssetRequestActivePart, EntAssetRequestWorkOrderActive, EntAssetRequestType, EntAssetRequestTableCreateWO, EntAssetRequestTableLookup, EntAssetRequestTableActivePart, EntAssetMobileRequestDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dceb179d0a17d8025d88c5945b9571de65c86449
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838607"
---
# <a name="maintenance-requests"></a><span data-ttu-id="68e5a-103">Ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="68e5a-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="68e5a-104">Ylläpitopyynnöt ovat muistiinpanoja tai ilmoituksia, jotka on luotu ilmoittamaan esimiehlle tai suunnittelijalle, että resurssi voi edellyttää huolto- tai korjaustyötä, mutta luomatta työtilausta.</span><span class="sxs-lookup"><span data-stu-id="68e5a-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="68e5a-105">Jos ylläpitopyynnön sisältö katsotaan kelvolliseksi, työtilaus voidaan luoda ylläpitopyynnön perusteella.</span><span class="sxs-lookup"><span data-stu-id="68e5a-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="68e5a-106">Ylläpitopyyntöjä voi luoda mille tahansa resurssille resurssien hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="68e5a-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="68e5a-107">Erilaisia ylläpitopyyntöjä voidaan luoda sen mukaan, miten yrityksesi käyttää ylläpitopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="68e5a-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="68e5a-108">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="68e5a-108">Here are some examples:</span></span>

- <span data-ttu-id="68e5a-109">Ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="68e5a-109">Maintenance requests</span></span>
- <span data-ttu-id="68e5a-110">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="68e5a-110">Notes</span></span>
- <span data-ttu-id="68e5a-111">Korjaukset tai parannukset</span><span class="sxs-lookup"><span data-stu-id="68e5a-111">Corrections or enhancements</span></span>
- <span data-ttu-id="68e5a-112">Investoinnit</span><span class="sxs-lookup"><span data-stu-id="68e5a-112">Investments</span></span>
- <span data-ttu-id="68e5a-113">Varastokorjaus (tätä tyyppiä käytetään, kun vastaanotat resursseja toisesta sijainnista, jotta voit tehdä huolto- tai korjaus työn, ja palautat sitten resurssin sen jälkeen, kun työ on suoritettu loppuun.)</span><span class="sxs-lookup"><span data-stu-id="68e5a-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="68e5a-114">Näytä ylläpitopyynnöt</span><span class="sxs-lookup"><span data-stu-id="68e5a-114">View maintenance requests</span></span>

<span data-ttu-id="68e5a-115">Näet ylläpitopyynnöt valitsemalla **resurssien hallinta** \> **Yhteiset** \> **Ylläpitopyynnöt** \> **Kaikki ylläpitopyynnöt**, **Aktiiviset ylläpitopyynnöt** tai **Omat toiminnallisen sijainnin ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="68e5a-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="68e5a-116">Kullakin luettelosivulla näkyy joitakin ylläpitopyyntöön liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="68e5a-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Ylläpitopyyntöjen katselu](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="68e5a-118">Käytä **Omat toiminnallisen sijainnin ylläpitopyynnöt** -luettelosivua, kun haluat tarkastella luetteloa ylläpitopyynnöistä, jotka sisältävät joko toiminnallisia sijainteja, joihin olet yhteydessä työntekijänä tai resursseja, jotka on asennettu toiminnallisiin sijainteihin, joihin olet liittynyt työntekijänä.</span><span class="sxs-lookup"><span data-stu-id="68e5a-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="68e5a-119">(Lisätietoja toiminnalisten sijainiten määrittämisestä kunnossapitotyöntekijöille on kohdassa [huoltotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="68e5a-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="68e5a-120">Vaikka asiakastilin tiedot ovat käytettävissä resurssien palvelujen hallinnassa (ulkoinen kunnossapito), se ei ole käytettävissä resurssien hallinnassa (sisäinen kunnossapito).</span><span class="sxs-lookup"><span data-stu-id="68e5a-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="68e5a-121">Voit avata tietueen tietonäkymän valitsemalla **Kaikki ylläpitopyynnöt** -luettelosivun ruudukkonäkymässä **Ylläpitopyyntö**-sarakkeesta linkin.</span><span class="sxs-lookup"><span data-stu-id="68e5a-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Ylläpitopyynnön tietojen avaaminen](media/02-manage-maintenance-requests.png)

<span data-ttu-id="68e5a-123">Toimintoruudun painikkeet on järjestetty välilehtiin.</span><span class="sxs-lookup"><span data-stu-id="68e5a-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="68e5a-124">Seuraavassa taulukossa kuvataan lyhyesti resurssien hallintaan liittyvät painikkeet.</span><span class="sxs-lookup"><span data-stu-id="68e5a-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="68e5a-125">Painikkeen nimi</span><span class="sxs-lookup"><span data-stu-id="68e5a-125">Button name</span></span>                      | <span data-ttu-id="68e5a-126">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="68e5a-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="68e5a-127">Muokkaa</span><span class="sxs-lookup"><span data-stu-id="68e5a-127">Edit</span></span>                             | <span data-ttu-id="68e5a-128">Muokkaa valittua ylläpitopyyntöä.</span><span class="sxs-lookup"><span data-stu-id="68e5a-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-129">Uusi</span><span class="sxs-lookup"><span data-stu-id="68e5a-129">New</span></span>                              | <span data-ttu-id="68e5a-130">luo uusi ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="68e5a-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="68e5a-131">Poista</span><span class="sxs-lookup"><span data-stu-id="68e5a-131">Delete</span></span>                           | <span data-ttu-id="68e5a-132">Poista valittu ylläpitopyyntö.</span><span class="sxs-lookup"><span data-stu-id="68e5a-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-133">Työtilauspooli</span><span class="sxs-lookup"><span data-stu-id="68e5a-133">Work order pool</span></span>                  | <span data-ttu-id="68e5a-134">Yhdistä valittu huoltopyyntö työtilauspooliin.</span><span class="sxs-lookup"><span data-stu-id="68e5a-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="68e5a-135">Työtilaus</span><span class="sxs-lookup"><span data-stu-id="68e5a-135">Work order</span></span>                       | <span data-ttu-id="68e5a-136">Luo työtilaus valitun huoltopyynnön perusteella.</span><span class="sxs-lookup"><span data-stu-id="68e5a-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-137">Resurssin vika</span><span class="sxs-lookup"><span data-stu-id="68e5a-137">Asset fault</span></span>                      | <span data-ttu-id="68e5a-138">Valitse **Resurssin viat**, jossa voit luoda vikarekisteröinnin valittuun ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="68e5a-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-139">Työtilaukset</span><span class="sxs-lookup"><span data-stu-id="68e5a-139">Work orders</span></span>                      | <span data-ttu-id="68e5a-140">Näytä luettelo kaikista työtilauksista, jotka on yhdistetty valittuun ylläpitopyyntöön.</span><span class="sxs-lookup"><span data-stu-id="68e5a-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-141">Päivitä ylläpitopyynnön tila.</span><span class="sxs-lookup"><span data-stu-id="68e5a-141">Update maintenance request state</span></span> | <span data-ttu-id="68e5a-142">Päivitä ylläpitopyynnön tila.</span><span class="sxs-lookup"><span data-stu-id="68e5a-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="68e5a-143">Elinkaaren tilan loki</span><span class="sxs-lookup"><span data-stu-id="68e5a-143">Lifecycle state log</span></span>              | <span data-ttu-id="68e5a-144">Tarkastele lokia, joka näyttää valitun ylläpitopyynnön elinkaaritilat.</span><span class="sxs-lookup"><span data-stu-id="68e5a-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-145">Ylläpitopyynnön tiedot</span><span class="sxs-lookup"><span data-stu-id="68e5a-145">Maintenance request details</span></span>      | <span data-ttu-id="68e5a-146">Tulosta raportti, joka sisältää valitun ylläpitopyynnön tiedot.</span><span class="sxs-lookup"><span data-stu-id="68e5a-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-147">Lähetä lainattu resurssi</span><span class="sxs-lookup"><span data-stu-id="68e5a-147">Send loan asset</span></span>                  | <span data-ttu-id="68e5a-148">Valitse lainaresurssi, jonka pitäisi olla väliaikainen korvaava resurssi, joka on valittu valitulle ylläpitopyynnölle.</span><span class="sxs-lookup"><span data-stu-id="68e5a-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="68e5a-149">Palauta lainaresurssi</span><span class="sxs-lookup"><span data-stu-id="68e5a-149">Return loan asset</span></span>                | <span data-ttu-id="68e5a-150">Rekisteröi lainaresurssi palautetuksi.</span><span class="sxs-lookup"><span data-stu-id="68e5a-150">Register the loan asset as returned.</span></span> |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]