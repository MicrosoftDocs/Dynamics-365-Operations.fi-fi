---
title: Hankinnan työnkulut
description: Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman. Voit määrittää hyväksymisprosessin luomalla työnkulun.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25ca64fb6a3fa7d7898ec68568703f3de7b1595
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "330077"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="880c2-104">Hankinnan työnkulut</span><span class="sxs-lookup"><span data-stu-id="880c2-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="880c2-105">Jotkin organisaatiot edellyttävät, että ostoehdotukset ja ostotilaukset hyväksyy eri käyttäjä kuin joka on syöttänyt tapahtuman.</span><span class="sxs-lookup"><span data-stu-id="880c2-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="880c2-106">Voit määrittää hyväksymisprosessin luomalla työnkulun.</span><span class="sxs-lookup"><span data-stu-id="880c2-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="880c2-107">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="880c2-107">A workflow represents a business process.</span></span> <span data-ttu-id="880c2-108">Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="880c2-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="880c2-109">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="880c2-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="880c2-110">**Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="880c2-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="880c2-111">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="880c2-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="880c2-112">**Prosessin näkyvyys** — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="880c2-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="880c2-113">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="880c2-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="880c2-114">**Keskitetty työluettelo** – Käyttäjät voivat tarkastella keskitetyssä työluettelossa olevia työnkulkutehtäviä ja niille annettuja hyväksyntöjä kaikissa työnkuluissa, joissa he ovat osallisina.</span><span class="sxs-lookup"><span data-stu-id="880c2-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="880c2-115">Tämän voi tehdä Työnimikkeet-sivulla.</span><span class="sxs-lookup"><span data-stu-id="880c2-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="880c2-116"> Luotavissa olevat työnkulkutyypit</span><span class="sxs-lookup"><span data-stu-id="880c2-116">The types of workflows that you can create</span></span>
<span data-ttu-id="880c2-117">Hankinnoissa voi käyttää seuraavia työnkulkutyyppejä.</span><span class="sxs-lookup"><span data-stu-id="880c2-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="880c2-118">**Tyyppi**</span><span class="sxs-lookup"><span data-stu-id="880c2-118">**Type**</span></span>                         | <span data-ttu-id="880c2-119">**Käytä tätä tyyppiä**</span><span class="sxs-lookup"><span data-stu-id="880c2-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="880c2-120">Ostoehdotuksen tarkastelu</span><span class="sxs-lookup"><span data-stu-id="880c2-120">Purchase requisition review</span></span>      | <span data-ttu-id="880c2-121">Luo ostoehdotusten tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="880c2-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="880c2-122">Ostoehdotusrivin tarkistus</span><span class="sxs-lookup"><span data-stu-id="880c2-122">Purchase requisition line review</span></span> | <span data-ttu-id="880c2-123">Luo ostoehdotusrivien tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="880c2-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="880c2-124">Ostotilaustyönkulku</span><span class="sxs-lookup"><span data-stu-id="880c2-124">Purchase order workflow</span></span>          | <span data-ttu-id="880c2-125">Luo ostotilauksille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="880c2-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="880c2-126">Ostotilausrivin työnkulku</span><span class="sxs-lookup"><span data-stu-id="880c2-126">Purchase order line workflow</span></span>     | <span data-ttu-id="880c2-127">Luo ostotilauksen riveille tarkistus- ja hyväksymistyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="880c2-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="880c2-128">Toimittajan sovelluksen lisäystyönkulku</span><span class="sxs-lookup"><span data-stu-id="880c2-128">Vendor add application workflow</span></span>  | <span data-ttu-id="880c2-129">Luo toimittajapyyntöjen kautta lisättävien uusien toimittajien tarkistus- ja hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="880c2-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="880c2-130">Työnkulun luominen</span><span class="sxs-lookup"><span data-stu-id="880c2-130">Creating a workflow</span></span>

<span data-ttu-id="880c2-131">Jos haluat luoda työnkulun, valitse Hankinta &gt; Asetukset &gt; Hankinnan työnkulut ja luo uusi työnkulku valitsemalla haluamasi työnkulkutyyppi.</span><span class="sxs-lookup"><span data-stu-id="880c2-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="880c2-132">Voit vetää työnkulkualustassa työnkulun elementit suunnitteluun ja linkittää ne työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="880c2-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="880c2-133">Työnkulun elementtien asetukset täytyy määrittää.</span><span class="sxs-lookup"><span data-stu-id="880c2-133">The workflow elements should be configured.</span></span> <span data-ttu-id="880c2-134">Hyväksynnän ja tehtävän työnkulun elementeille voit määrittää, kenen osallistujan tulee tehdä niille toimia.</span><span class="sxs-lookup"><span data-stu-id="880c2-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="880c2-135">Osallistujien tyypit</span><span class="sxs-lookup"><span data-stu-id="880c2-135">Types of participants</span></span>

<span data-ttu-id="880c2-136">Voit määrittää hyväksyntävaiheen seuraaville osallistujaryhmille.</span><span class="sxs-lookup"><span data-stu-id="880c2-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="880c2-137">Käyttäjäryhmä</span><span class="sxs-lookup"><span data-stu-id="880c2-137">User group</span></span>    | <span data-ttu-id="880c2-138">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="880c2-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="880c2-139">Osallistuja</span><span class="sxs-lookup"><span data-stu-id="880c2-139">Participant</span></span>   | <span data-ttu-id="880c2-140">Määritä hyväksyntävaihe ryhmän tai roolin jäsenille.</span><span class="sxs-lookup"><span data-stu-id="880c2-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="880c2-141">Hierarkia</span><span class="sxs-lookup"><span data-stu-id="880c2-141">Hierarchy</span></span>     | <span data-ttu-id="880c2-142">Määritä hyväksyntävaihe tietyssä organisaatiohierarkiassa oleville käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="880c2-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="880c2-143">Työnkulun käyttäjä</span><span class="sxs-lookup"><span data-stu-id="880c2-143">Workflow user</span></span> | <span data-ttu-id="880c2-144">Määritä hyväksyntävaihe tämän työnkulun käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="880c2-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="880c2-145">Jono</span><span class="sxs-lookup"><span data-stu-id="880c2-145">Queue</span></span>         | <span data-ttu-id="880c2-146">Määritä hyväksyntävaihe työnimikejonolle.</span><span class="sxs-lookup"><span data-stu-id="880c2-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="880c2-147">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="880c2-147">User</span></span>          | <span data-ttu-id="880c2-148">Määritä hyväksyntävaihe tietyille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="880c2-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="880c2-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="880c2-149">Additional resources</span></span>

- <span data-ttu-id="880c2-150">[Ostoehdotusten liiketoimintaprosessien työnkulun määrittäminen](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions) (raportti)</span><span class="sxs-lookup"><span data-stu-id="880c2-150">[Defining business process workflows for purchase requisitions](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)</span></span>

- [<span data-ttu-id="880c2-151">Ostoehdotuksen työnkulku</span><span class="sxs-lookup"><span data-stu-id="880c2-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="880c2-152">Toimittajien aktivointi</span><span class="sxs-lookup"><span data-stu-id="880c2-152">Onboarding vendors</span></span>](vendor-onboarding.md)

