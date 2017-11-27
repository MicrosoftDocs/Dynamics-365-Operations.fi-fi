---
title: "Hankinnan työnkulut"
description: "Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3bf244786e308ebcaee27a16fae378f41086f963
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="ec5dd-104">Hankinnan työnkulut</span><span class="sxs-lookup"><span data-stu-id="ec5dd-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ec5dd-105">Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="ec5dd-106">Voit määrittää hyväksymisprosessin luomalla työnkulun.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="ec5dd-107">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-107">A workflow represents a business process.</span></span> <span data-ttu-id="ec5dd-108">Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="ec5dd-109">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="ec5dd-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="ec5dd-110">**Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="ec5dd-111">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="ec5dd-112">**Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="ec5dd-113">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="ec5dd-114">**Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitetyssä työluettelossa olevia työnkulkutehtäviä ja niille annettuja hyväksyntöjä kaikissa työnkuluissa, joissa he ovat osallisina.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="ec5dd-115">Tämän voi tehdä Työnimikkeet-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="ec5dd-116"> Luotavissa olevat työnkulkutyypit</span><span class="sxs-lookup"><span data-stu-id="ec5dd-116">The types of workflows that you can create</span></span>
<span data-ttu-id="ec5dd-117">Hankinnoissa voi käyttää seuraavia työnkulkutyyppejä.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ec5dd-118">**Tyyppi**</span><span class="sxs-lookup"><span data-stu-id="ec5dd-118">**Type**</span></span>                         | <span data-ttu-id="ec5dd-119">**Käytä tätä tyyppiä**</span><span class="sxs-lookup"><span data-stu-id="ec5dd-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="ec5dd-120">Ostoehdotuksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="ec5dd-120">Purchase requisition review</span></span>      | <span data-ttu-id="ec5dd-121">Luo ostoehdotuksille tarkistustyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="ec5dd-122">Ostoehdotusrivin tarkistus</span><span class="sxs-lookup"><span data-stu-id="ec5dd-122">Purchase requisition line review</span></span> | <span data-ttu-id="ec5dd-123">Luo ostoehdotuksen riveille tarkistustyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="ec5dd-124">Ostotilaustyönkulku</span><span class="sxs-lookup"><span data-stu-id="ec5dd-124">Purchase order workflow</span></span>          | <span data-ttu-id="ec5dd-125">Luo ostotilauksille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="ec5dd-126">Ostotilausrivin työnkulku</span><span class="sxs-lookup"><span data-stu-id="ec5dd-126">Purchase order line workflow</span></span>     | <span data-ttu-id="ec5dd-127">Luo ostotilauksen riveille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="ec5dd-128">Työnkulun luominen</span><span class="sxs-lookup"><span data-stu-id="ec5dd-128">Creating a workflow</span></span>
<span data-ttu-id="ec5dd-129">Jos haluat luoda työnkulun, valitse Hankinta &gt; Asetukset &gt; Hankinnan työnkulut ja luo uusi työnkulku valitsemalla haluamasi työnkulkutyyppi.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="ec5dd-130">Voit vetää työnkulkualustassa työnkulun elementit suunnitteluun ja linkittää ne työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="ec5dd-131">Työnkulun elementtien asetukset täytyy määrittää.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-131">The workflow elements should be configured.</span></span> <span data-ttu-id="ec5dd-132">Hyväksynnän ja tehtävän työnkulun elementeille voit määrittää, kenen osallistujan tulee tehdä niille toimia.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="ec5dd-133">Osallistujien tyypit</span><span class="sxs-lookup"><span data-stu-id="ec5dd-133">Types of participants</span></span>
----------------------

<span data-ttu-id="ec5dd-134">Voit määrittää hyväksyntävaiheen seuraaville osallistujaryhmille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="ec5dd-135">Käyttäjäryhmä</span><span class="sxs-lookup"><span data-stu-id="ec5dd-135">User group</span></span>    | <span data-ttu-id="ec5dd-136">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ec5dd-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="ec5dd-137">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="ec5dd-137">Participant</span></span>   | <span data-ttu-id="ec5dd-138">Määritä hyväksyntävaihe ryhmän tai roolin jäsenille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="ec5dd-139">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="ec5dd-139">Hierarchy</span></span>     | <span data-ttu-id="ec5dd-140">Määritä hyväksyntävaihe tietyssä organisaatiohierarkiassa oleville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="ec5dd-141">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="ec5dd-141">Workflow user</span></span> | <span data-ttu-id="ec5dd-142">Määritä hyväksyntävaihe tämän työnkulun käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="ec5dd-143">Jono</span><span class="sxs-lookup"><span data-stu-id="ec5dd-143">Queue</span></span>         | <span data-ttu-id="ec5dd-144">Määritä hyväksyntävaihe työnimikejonolle.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="ec5dd-145">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="ec5dd-145">User</span></span>          | <span data-ttu-id="ec5dd-146">Määritä hyväksyntävaihe tietyille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="ec5dd-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="ec5dd-147">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ec5dd-147">See also</span></span>
--------

<span data-ttu-id="ec5dd-148">[Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions) (raportti)</span><span class="sxs-lookup"><span data-stu-id="ec5dd-148">[Defining business process workflows for purchase requisitions](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)</span></span>

[<span data-ttu-id="ec5dd-149">Ostoehdotuksen työnkulku</span><span class="sxs-lookup"><span data-stu-id="ec5dd-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




