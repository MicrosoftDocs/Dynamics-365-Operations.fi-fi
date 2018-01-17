---
title: "Kulunhallinnan työnkulkujen määrittäminen"
description: "Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: fi-fi
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="46ebb-103">Kulunhallinnan työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46ebb-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="46ebb-104"> Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="46ebb-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="46ebb-105">Asiakirjat, joille työnkulun voi määrittää, ovat muun muassa kuluraportteja, matkustusehdotuksia ja käteisennakkopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="46ebb-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="46ebb-106">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="46ebb-106">A workflow represents a business process.</span></span> <span data-ttu-id="46ebb-107">Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="46ebb-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="46ebb-108">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="46ebb-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="46ebb-109">**Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="46ebb-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="46ebb-110">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="46ebb-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="46ebb-111">Prosessin näkyvyys — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="46ebb-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="46ebb-112">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="46ebb-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="46ebb-113">Keskitetty työluettelo — Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät.</span><span class="sxs-lookup"><span data-stu-id="46ebb-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="46ebb-114">**Voit luoda seuraavat työnkulkutyypit**</span><span class="sxs-lookup"><span data-stu-id="46ebb-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="46ebb-115">Seuraavassa taulukossa on esitetty erityyppisiä työnkulkuja, joita voit luoda **kulunhallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="46ebb-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="46ebb-116">**Tyyppi**</span><span class="sxs-lookup"><span data-stu-id="46ebb-116">**Type**</span></span>                           | <span data-ttu-id="46ebb-117">**Käytä tätä tyyppiä**</span><span class="sxs-lookup"><span data-stu-id="46ebb-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="46ebb-118">**Kuluraportti**</span><span class="sxs-lookup"><span data-stu-id="46ebb-118">**Expense report**</span></span>                 | <span data-ttu-id="46ebb-119">Kuluraporttien hyväksyntätyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="46ebb-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="46ebb-120">**Kuluraportin automaattinen kirjaaminen**</span><span class="sxs-lookup"><span data-stu-id="46ebb-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="46ebb-121">Luo automaattisen kirjaamisen työnkulut kuluraportteja varten.</span><span class="sxs-lookup"><span data-stu-id="46ebb-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="46ebb-122">**Kulurivin nimike**</span><span class="sxs-lookup"><span data-stu-id="46ebb-122">**Expense line item**</span></span>              | <span data-ttu-id="46ebb-123">Kuluraporttien rivinimikkeiden hyväksyntätyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="46ebb-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="46ebb-124">**Kulurivinimikkeen automaattinen kirjaaminen**</span><span class="sxs-lookup"><span data-stu-id="46ebb-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="46ebb-125">Kuluraporttien rivinimikkeiden automaattisten kirjaustyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="46ebb-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="46ebb-126">**Matkahankinta**</span><span class="sxs-lookup"><span data-stu-id="46ebb-126">**Travel requisition**</span></span>             | <span data-ttu-id="46ebb-127">Luo matkustusehdotusten hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="46ebb-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="46ebb-128">**Käteisennakkopyyntö**</span><span class="sxs-lookup"><span data-stu-id="46ebb-128">**Cash advance request**</span></span>           | <span data-ttu-id="46ebb-129">Luo hyväksyntätyönkulkuja käteisennakkopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="46ebb-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="46ebb-130">**Arvonlisäveron palautus**</span><span class="sxs-lookup"><span data-stu-id="46ebb-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="46ebb-131">Luo arvonlisäveron (ALV) palautuksen hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="46ebb-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

