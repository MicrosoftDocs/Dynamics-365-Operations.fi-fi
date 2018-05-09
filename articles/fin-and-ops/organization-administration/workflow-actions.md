---
title: "Työnkulkutehtävät"
description: "Tässä artikkelissa kuvataan toimenpiteet, jotka kukin työnkulun hyväksyntäprosessin osallistuja voi suorittaa."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2dd9520d16f6cc136ee1b3fae084170cbcee7c34
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---

# <a name="workflow-actions"></a><span data-ttu-id="3fde0-103">Työnkulkutehtävät</span><span class="sxs-lookup"><span data-stu-id="3fde0-103">Workflow actions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fde0-104">Tässä artikkelissa kuvataan toimenpiteet, jotka kukin työnkulun hyväksyntäprosessin osallistuja voi suorittaa.</span><span class="sxs-lookup"><span data-stu-id="3fde0-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="3fde0-105">Työnkulkuun voi liittyä useita käyttäjäryhmiä: aloittaja, tehtävän osallistuja, päätöksentekijät ja hyväksyjät.</span><span class="sxs-lookup"><span data-stu-id="3fde0-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="3fde0-106">Esimerkiksi seuraavassa kuluraportin työnkulussa Sam on aloittaja, jonon jäsenet ovat tehtävän osallistujia, John on päätöksentekijä sekä Frank, Sue sekä Ann ovat hyväksyjiä.</span><span class="sxs-lookup"><span data-stu-id="3fde0-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>   

<span data-ttu-id="3fde0-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="3fde0-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span> 

<span data-ttu-id="3fde0-108">Seuraavissa kappaleissa kuvataan kunkin ryhmän mahdolliset toimenpiteet.</span><span class="sxs-lookup"><span data-stu-id="3fde0-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="3fde0-109">Toiminnot, joita aloittaja voi suorittaa</span><span class="sxs-lookup"><span data-stu-id="3fde0-109">Actions that an originator can perform</span></span>
<span data-ttu-id="3fde0-110">Aloittaja käynnistää työnkulkuesiintymän lähettämällä tiedoston käsiteltäväksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="3fde0-111">Sam voi esimerkiksi lähettää kuluraporttinsa napsauttamalla **Lähetä**-painiketta **Kuluraportti**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3fde0-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="3fde0-112">Toiminnot, joita tehtävän osallistuja voi suorittaa</span><span class="sxs-lookup"><span data-stu-id="3fde0-112">Actions that a task assignee can perform</span></span>
<span data-ttu-id="3fde0-113">Tehtävä voidaan määrittää useille henkilöille tai useiden henkilöiden seuraamalle työnimikejonolle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="3fde0-114">Kuitenkin vain yksi henkilö voi suorittaa tehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-114">However, only one person can complete a task.</span></span> <span data-ttu-id="3fde0-115">Sam on esimerkiksi lähettänyt kuluraportin ja reitittänyt kuittinsa organisaationsa kuluraporttiosastolle tarkistusta varten.</span><span class="sxs-lookup"><span data-stu-id="3fde0-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span> 

<span data-ttu-id="3fde0-116">Adventure Worksin kuluraporttiosaston jäsenet seuraavat jonoa.</span><span class="sxs-lookup"><span data-stu-id="3fde0-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="3fde0-117">Tämän osaston jäsen, Julie, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3fde0-118">Julie voi suorittaa jonkin seuraavista toiminnoista: valmis, hylkää, delegointi, pyydä muutosta, määritä uudelleen tai vapauta.</span><span class="sxs-lookup"><span data-stu-id="3fde0-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span> 

<span data-ttu-id="3fde0-119">**Huomautus.** Käytettävissä olevat toiminnot vaihtelevat sen mukaan, miten ohjelmistokehittäjä on suunnitellut tehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-119">**Note:** The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="3fde0-120">Valmis</span><span class="sxs-lookup"><span data-stu-id="3fde0-120">Complete</span></span>

<span data-ttu-id="3fde0-121">Kun käyttäjä suorittaa tehtävän loppuun, käsiteltäväksi lähetetty tiedosto lähetetään työnkulussa mahdollisesti seuraavaksi määritetylle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="3fde0-122">Jos lisäkäsittelyä ei tarvita, työnkulkuprosessi päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-122">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-123">Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="3fde0-124">Kun Julie on suorittanut tarkistuksen, asiakirja määritetään Johnille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="3fde0-125">Hylkää</span><span class="sxs-lookup"><span data-stu-id="3fde0-125">Reject</span></span>

<span data-ttu-id="3fde0-126">Jos käyttäjä hylkää tiedoston, työnkulku päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-126">When a user rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-127">Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam’s expense report and receipts.</span></span> <span data-ttu-id="3fde0-128">Jos Julie hylkää kuluraportin, työnkulkuprosessi päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-128">If Julie rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-129">San voi sitten lähettää kuluraportin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="3fde0-130">Hän voi tehdä siihen ensin muutoksia tai lähettää alkuperäisen version uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="3fde0-131">Jos Sam lähettää kuluraportin uudelleen, työnkulkuprosessi käynnistyy manuaalisesta tarkistustehtävästä.</span><span class="sxs-lookup"><span data-stu-id="3fde0-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="3fde0-132">Delegointi</span><span class="sxs-lookup"><span data-stu-id="3fde0-132">Delegate</span></span>

<span data-ttu-id="3fde0-133">Jos käyttäjä delegoi tehtävän, se määritetään toisen käyttäjän suoritettavaksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-133">When a user delegates a task, the task is assigned to another user.</span></span> 

<span data-ttu-id="3fde0-134">Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3fde0-135">Julie delegoi tehtävän Timille, joka on hänen avustajansa.</span><span class="sxs-lookup"><span data-stu-id="3fde0-135">Julie delegates this task to Tim, who is her assistant.</span></span> 

<span data-ttu-id="3fde0-136">Tim toimii sitten Julien puolesta.</span><span class="sxs-lookup"><span data-stu-id="3fde0-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="3fde0-137">Kun Tim sitten päättää tarkistuksensa, kuluraportti määritetään Johnille aivan kuten, jos Julie olisi suorittanut tehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="3fde0-138">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="3fde0-138">Request change</span></span>

<span data-ttu-id="3fde0-139">Jos käyttäjä tekee muutospyynnön, tiedosto palautetaan sen lähettäneelle aloittajalle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span> 

<span data-ttu-id="3fde0-140">Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3fde0-141">Julie huomaa kuluraportissa virheitä ja pyytää muutoksia.</span><span class="sxs-lookup"><span data-stu-id="3fde0-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="3fde0-142">Kuluraportti lähetetään takaisin Samille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-142">The expense report is sent back to Sam.</span></span> 

<span data-ttu-id="3fde0-143">Sam voi lähettää kuluraportin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3fde0-144">Hän voi tehdä siihen ensin pyydetyt muutokset tai lähettää alkuperäisen version.</span><span class="sxs-lookup"><span data-stu-id="3fde0-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="3fde0-145">Jos Sam lähettää kuluraportin uudelleen, työnimikejonon jäsenen on tarkistettava kuluraportti ja kuitit uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="3fde0-146">Määritä uudelleen</span><span class="sxs-lookup"><span data-stu-id="3fde0-146">Reassign</span></span>

<span data-ttu-id="3fde0-147">Työnimijonon jäsenet voivat määrittää jonossa olevat asiakirjat toiseen jonoon.</span><span class="sxs-lookup"><span data-stu-id="3fde0-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span> 

<span data-ttu-id="3fde0-148">Esimerkiksi Julie, Adventure Worksin kuluraporttiosaston jäsen, seuraa jonoa.</span><span class="sxs-lookup"><span data-stu-id="3fde0-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="3fde0-149">Julie voi tasapainottaa kuormitusta määrittämällä kuluraportin ja siihen sisältyvät kuitit uudelleen toiseen jonoon.</span><span class="sxs-lookup"><span data-stu-id="3fde0-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="3fde0-150">Vapauta</span><span class="sxs-lookup"><span data-stu-id="3fde0-150">Release</span></span>

<span data-ttu-id="3fde0-151">Työnimikejonon jäsen voi joskus hyväksyä tehtävän mutta päättää myöhemmin, ettei hän voikaan suorittaa tehtävää.</span><span class="sxs-lookup"><span data-stu-id="3fde0-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="3fde0-152">Siinä tapauksessa tehtävän hyväksynyt henkilö vapauttaa asiakirjan takaisin työnimikejonoon.</span><span class="sxs-lookup"><span data-stu-id="3fde0-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span> 

<span data-ttu-id="3fde0-153">Esimerkiksi Julie, joka on Adventure Worksin kuluraporttiosaston jäsen, on hyväksynyt Samin kuluraportin ja kuittien tarkistustehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="3fde0-154">Jos Julie päättää, ettei hän voi suorittaa tehtävää, hän vapauttaa asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="3fde0-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="3fde0-155">Kuluraportti palautetaan jonoon, jolloin Adventure Worksin kuluraporttiosaston muut jäsenet voivat suorittaa tehtävän.</span><span class="sxs-lookup"><span data-stu-id="3fde0-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="3fde0-156">Toiminnot, joita päätöksentekijä voi suorittaa</span><span class="sxs-lookup"><span data-stu-id="3fde0-156">Actions that a decision maker can perform</span></span>
<span data-ttu-id="3fde0-157">Asiakirja määritetään yleensä päätöksentekijälle siksi, että siihen sisältyy kysymys, johon päätöksentekijän on vastattava.</span><span class="sxs-lookup"><span data-stu-id="3fde0-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="3fde0-158">Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="3fde0-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="3fde0-159">Jos päätöksentekijä ei valitse yhtä näistä vaihtoehdoista, hän delegoida päätöksen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="3fde0-160">\[Vaihtoehto 1\] tai \[Vaihtoehto 2\]</span><span class="sxs-lookup"><span data-stu-id="3fde0-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="3fde0-161">Päätöksentekijän on vastattava asiakirjaan liittyvään kysymykseen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="3fde0-162">Kysymyksen vastaus on yleensä **Kyllä** tai **Ei** tai **Tosi** tai **Epätosi**.</span><span class="sxs-lookup"><span data-stu-id="3fde0-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="3fde0-163">Päätöksentekijän valitsema vastaus määrittää työnkulun haaran, jossa asiakirja käsitellään.</span><span class="sxs-lookup"><span data-stu-id="3fde0-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span> 

<span data-ttu-id="3fde0-164">Samin kuluraportti on esimerkiksi määritetty Johnille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="3fde0-165">Johnin on päätettävä, onko hänen soitettava Samin esimiehelle asiakirjan tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3fde0-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="3fde0-166">John päättää, että puhelu on välttämätön, kuluraportti määritetään Arethalla, jonka on sitten soitettava Samin esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="3fde0-167">Jos John päättää, että puhelua ei tarvita, kuluraportti määritetään Frankille hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="3fde0-168">Delegointi</span><span class="sxs-lookup"><span data-stu-id="3fde0-168">Delegate</span></span>

<span data-ttu-id="3fde0-169">Kun päätöksentekijä delegoi päätöksen, asiakirja määritetään toiselle käyttäjälle, jonka on tehtävä päätös.</span><span class="sxs-lookup"><span data-stu-id="3fde0-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span> 

<span data-ttu-id="3fde0-170">Samin kuluraportti on esimerkiksi määritetty Johnille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="3fde0-171">John delegoi päätöksen Maria, joka on hänen avustajansa.</span><span class="sxs-lookup"><span data-stu-id="3fde0-171">John delegates the decision to Maria, who is his assistant.</span></span> 

<span data-ttu-id="3fde0-172">Maria toimii sitten Johnin puolesta.</span><span class="sxs-lookup"><span data-stu-id="3fde0-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="3fde0-173">Jos Maria päättää, että puhelu on Samin esimiehelle on välttämätön, kuluraportti määritetään Arethalla, jonka on sitten soitettava Samin esimiehelle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="3fde0-174">Jos Maria päättää, että puhelua ei tarvita, kuluraportti määritetään Frankille hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="3fde0-175">Toiminnot, joita aloittaja voi suorittaa</span><span class="sxs-lookup"><span data-stu-id="3fde0-175">Actions that an approver can perform</span></span>
<span data-ttu-id="3fde0-176">Kun tiedosto määritetään hyväksyjälle, hän voi suorittaa jonkin seuraavista toiminnoista: hyväksyntä, hylkäys, delegointi, pyydä muutosta.</span><span class="sxs-lookup"><span data-stu-id="3fde0-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="3fde0-177">Hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="3fde0-177">Approve</span></span>

<span data-ttu-id="3fde0-178">Jos hyväksyjä hyväksyy asiakirjan, se lähetetään työnkulussa mahdolliselle seuraavaksi määritetylle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="3fde0-179">Jos lisäkäsittelyä ei tarvita, työnkulkuprosessi päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-179">If no additional processing is required, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-180">Sam on esimerkiksi lähettänyt 6 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Frankille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="3fde0-181">Kun Frank hyväksyy raportin, se määritetään Suelle hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="3fde0-182">Kun Sue hyväksyy kuluraportin, työnkulkuprosessi päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="3fde0-183">Hylkää</span><span class="sxs-lookup"><span data-stu-id="3fde0-183">Reject</span></span>

<span data-ttu-id="3fde0-184">Jos hyväksyjä hylkää tiedoston, työnkulku päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-184">When an approver rejects a document, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-185">Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Suelle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="3fde0-186">Jos Sue hylkää kuluraportin, työnkulkuprosessi päättyy.</span><span class="sxs-lookup"><span data-stu-id="3fde0-186">If Sue rejects the expense report, the workflow process ends.</span></span> 

<span data-ttu-id="3fde0-187">Sam voi lähettää kuluraportin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3fde0-188">Hän voi tehdä siihen ensin muutoksia tai lähettää kuluraportin alkuperäisen version uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="3fde0-189">Jos Sam lähettää kuluraportin uudelleen, työnkulkuprosessi käynnistyy hyväksyntäprosessista.</span><span class="sxs-lookup"><span data-stu-id="3fde0-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="3fde0-190">Delegointi</span><span class="sxs-lookup"><span data-stu-id="3fde0-190">Delegate</span></span>

<span data-ttu-id="3fde0-191">Jos hyväksyjä delegoi tiedoston, se lähetetään hyväksyttäväksi toiselle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span> 

<span data-ttu-id="3fde0-192">Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Frankille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="3fde0-193">Frank delegoi kuluraportin Annille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-193">Frank delegates the expense report to Ann.</span></span> 

<span data-ttu-id="3fde0-194">Ann toimii sitten Frankin puolesta.</span><span class="sxs-lookup"><span data-stu-id="3fde0-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="3fde0-195">Kun Ann sitten hyväksyy asiakirjan, se määritetään Suelle hyväksyttäväksi, aivan kuten jos Frank olisi hyväksynyt asiakirjan.</span><span class="sxs-lookup"><span data-stu-id="3fde0-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="3fde0-196">Kun Sue hyväksyy asiakirjan, se lähetetään Annille hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="3fde0-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="3fde0-197">Pyydä muutosta</span><span class="sxs-lookup"><span data-stu-id="3fde0-197">Request change</span></span>

<span data-ttu-id="3fde0-198">Jos hyväksyjä tekee muutospyynnön, tiedosto palautetaan sen lähettäneelle aloittajalle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span> 

<span data-ttu-id="3fde0-199">Sam on esimerkiksi lähettänyt 12 000 dollarin arvoisen kuluraportin ja asiakirja on määritetty Suelle.</span><span class="sxs-lookup"><span data-stu-id="3fde0-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="3fde0-200">Jos Sue pyytää muutosta, kuluraportti lähetetään takaisin Samille.</span><span class="sxs-lookup"><span data-stu-id="3fde0-200">If Sue requests a change, the expense report is sent back to Sam.</span></span> 

<span data-ttu-id="3fde0-201">Sam voi lähettää kuluraportin uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="3fde0-202">Hän voi tehdä siihen ensin pyydetyt muutokset tai lähettää kuluraportin alkuperäisen version uudelleen.</span><span class="sxs-lookup"><span data-stu-id="3fde0-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="3fde0-203">Jos Sam lähettää kuluraportin uudelleen, se lähetetään Frankille hyväksyttäväksi, koska Frank on hyväksyntäprosessin ensimmäinen hyväksyjä.</span><span class="sxs-lookup"><span data-stu-id="3fde0-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>




