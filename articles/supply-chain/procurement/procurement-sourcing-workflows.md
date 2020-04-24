---
title: Hankinnan työnkulut
description: Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a20be4730189f1f81a08b5dda21e97aaedd7d3b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209234"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="0c298-104">Hankinnan työnkulut</span><span class="sxs-lookup"><span data-stu-id="0c298-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c298-105">Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="0c298-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="0c298-106">Voit määrittää hyväksymisprosessin luomalla työnkulun.</span><span class="sxs-lookup"><span data-stu-id="0c298-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="0c298-107">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="0c298-107">A workflow represents a business process.</span></span> <span data-ttu-id="0c298-108">Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="0c298-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="0c298-109">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="0c298-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="0c298-110">**Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="0c298-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="0c298-111">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="0c298-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="0c298-112">**Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="0c298-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="0c298-113">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="0c298-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="0c298-114">**Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitetyssä työluettelossa olevia työnkulkutehtäviä ja niille annettuja hyväksyntöjä kaikissa työnkuluissa, joissa he ovat osallisina.</span><span class="sxs-lookup"><span data-stu-id="0c298-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="0c298-115">Tämän voi tehdä Työnimikkeet-sivulla.</span><span class="sxs-lookup"><span data-stu-id="0c298-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="0c298-116"> Luotavissa olevat työnkulkutyypit</span><span class="sxs-lookup"><span data-stu-id="0c298-116">The types of workflows that you can create</span></span>
<span data-ttu-id="0c298-117">Hankinnoissa voi käyttää seuraavia työnkulkutyyppejä.</span><span class="sxs-lookup"><span data-stu-id="0c298-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0c298-118">**Tyyppi**</span><span class="sxs-lookup"><span data-stu-id="0c298-118">**Type**</span></span>                         | <span data-ttu-id="0c298-119">**Käytä tätä tyyppiä**</span><span class="sxs-lookup"><span data-stu-id="0c298-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="0c298-120">Ostoehdotuksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="0c298-120">Purchase requisition review</span></span>      | <span data-ttu-id="0c298-121">Luo ostoehdotusten tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="0c298-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="0c298-122">Ostoehdotusrivin tarkistus</span><span class="sxs-lookup"><span data-stu-id="0c298-122">Purchase requisition line review</span></span> | <span data-ttu-id="0c298-123">Luo ostoehdotusrivien tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="0c298-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="0c298-124">Ostotilaustyönkulku</span><span class="sxs-lookup"><span data-stu-id="0c298-124">Purchase order workflow</span></span>          | <span data-ttu-id="0c298-125">Luo ostotilauksille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="0c298-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="0c298-126">Ostotilausrivin työnkulku</span><span class="sxs-lookup"><span data-stu-id="0c298-126">Purchase order line workflow</span></span>     | <span data-ttu-id="0c298-127">Luo ostotilauksen riveille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="0c298-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="0c298-128">Toimittajan sovelluksen lisäystyönkulku</span><span class="sxs-lookup"><span data-stu-id="0c298-128">Vendor add application workflow</span></span>  | <span data-ttu-id="0c298-129">Luo toimittajapyyntöjen kautta lisättävien uusien toimittajien tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="0c298-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="0c298-130">Työnkulun luominen</span><span class="sxs-lookup"><span data-stu-id="0c298-130">Creating a workflow</span></span>

<span data-ttu-id="0c298-131">Jos haluat luoda työnkulun, valitse Hankinta &gt; Asetukset &gt; Hankinnan työnkulut ja luo uusi työnkulku valitsemalla haluamasi työnkulkutyyppi.</span><span class="sxs-lookup"><span data-stu-id="0c298-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="0c298-132">Voit vetää työnkulkualustassa työnkulun elementit suunnitteluun ja linkittää ne työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="0c298-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="0c298-133">Työnkulun elementtien asetukset täytyy määrittää.</span><span class="sxs-lookup"><span data-stu-id="0c298-133">The workflow elements should be configured.</span></span> <span data-ttu-id="0c298-134">Hyväksynnän ja tehtävän työnkulun elementeille voit määrittää, kenen osallistujan tulee tehdä niille toimia.</span><span class="sxs-lookup"><span data-stu-id="0c298-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="0c298-135">Osallistujien tyypit</span><span class="sxs-lookup"><span data-stu-id="0c298-135">Types of participants</span></span>

<span data-ttu-id="0c298-136">Voit määrittää hyväksyntävaiheen seuraaville osallistujaryhmille.</span><span class="sxs-lookup"><span data-stu-id="0c298-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="0c298-137">Käyttäjäryhmä</span><span class="sxs-lookup"><span data-stu-id="0c298-137">User group</span></span>    | <span data-ttu-id="0c298-138">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0c298-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0c298-139">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="0c298-139">Participant</span></span>   | <span data-ttu-id="0c298-140">Määritä hyväksyntävaihe ryhmän tai roolin jäsenille.</span><span class="sxs-lookup"><span data-stu-id="0c298-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="0c298-141">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="0c298-141">Hierarchy</span></span>     | <span data-ttu-id="0c298-142">Määritä hyväksyntävaihe tietyssä organisaatiohierarkiassa oleville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="0c298-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="0c298-143">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="0c298-143">Workflow user</span></span> | <span data-ttu-id="0c298-144">Määritä hyväksyntävaihe tämän työnkulun käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="0c298-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="0c298-145">Jono</span><span class="sxs-lookup"><span data-stu-id="0c298-145">Queue</span></span>         | <span data-ttu-id="0c298-146">Määritä hyväksyntävaihe työnimikejonolle.</span><span class="sxs-lookup"><span data-stu-id="0c298-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="0c298-147">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="0c298-147">User</span></span>          | <span data-ttu-id="0c298-148">Määritä hyväksyntävaihe tietyille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="0c298-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="0c298-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0c298-149">Additional resources</span></span>

- [<span data-ttu-id="0c298-150">Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen (raportti)</span><span class="sxs-lookup"><span data-stu-id="0c298-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="0c298-151">Ostoehdotuksen työnkulku</span><span class="sxs-lookup"><span data-stu-id="0c298-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="0c298-152">Toimittajien aktivointi</span><span class="sxs-lookup"><span data-stu-id="0c298-152">Onboard vendors</span></span>](vendor-onboarding.md)

