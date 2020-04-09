---
title: Kulujenhallinnan työnkulkujen määrittäminen
description: Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153990"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="4e056-103">Kulujenhallinnan työnkulkujen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4e056-103">Set up workflows for Expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e056-104">Voit määrittää työnkulkuprosessin, jota matka- ja kuluasiakirjojen tarkistamiseen ja hyväksyntään.</span><span class="sxs-lookup"><span data-stu-id="4e056-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="4e056-105">Asiakirjat, joille työnkulun voi määrittää, ovat muun muassa kuluraportteja, matkustusehdotuksia ja käteisennakkopyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="4e056-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="4e056-106">Työnkulku vastaa liiketoimintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="4e056-106">A workflow represents a business process.</span></span> <span data-ttu-id="4e056-107">Se määrittää, miten asiakirja "kulkee" järjestelmässä, ja osoittaa, kenen on saatettava tehtävä valmiiksi tai hyväksyttävä asiakirja.</span><span class="sxs-lookup"><span data-stu-id="4e056-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="4e056-108">Työnkulkujärjestelmän käyttö hyödyttää organisaatiotasi monin eri tavoin:</span><span class="sxs-lookup"><span data-stu-id="4e056-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="4e056-109">**Yhdenmukaiset prosessit** — Voit määrittää hyväksyntäprosessin tietyille asiakirjoille kuten ostoehdotuksille ja kuluraporteille.</span><span class="sxs-lookup"><span data-stu-id="4e056-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="4e056-110">Työnkulkujärjestelmän käyttö auttaa varmistamaan, että asiakirjat käsitellään ja hyväksytään johdonmukaisesti ja tehokkaasti.</span><span class="sxs-lookup"><span data-stu-id="4e056-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="4e056-111">Prosessin näkyvyys — Voit seurata tietyn työnkulun esiintymän tilaa, historiaa ja suorituskykyarvoja.</span><span class="sxs-lookup"><span data-stu-id="4e056-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="4e056-112">Tämä auttaa määrittämään, tarvitaanko työnkulkuun muutoksia tehokkuuden parantamiseksi.</span><span class="sxs-lookup"><span data-stu-id="4e056-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="4e056-113">Keskitetty työluettelo — Käyttäjät voivat tarkastella keskitettyä työluetteloa, joka sisältää työnkulun tehtävät ja niille annetut hyväksynnät.</span><span class="sxs-lookup"><span data-stu-id="4e056-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="4e056-114">**Voit luoda seuraavat työnkulkutyypit**</span><span class="sxs-lookup"><span data-stu-id="4e056-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="4e056-115">Seuraavassa taulukossa on esitetty erityyppisiä työnkulkuja, joita voit luoda **kulunhallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="4e056-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="4e056-116"><strong>Tyyppi</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="4e056-117"><strong>Käytä tätä tyyppiä</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="4e056-118"><strong>Kuluraportti</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="4e056-119">Kuluraporttien hyväksyntätyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="4e056-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="4e056-120"><strong>Kuluraportin automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="4e056-121">Luo automaattisen kirjaamisen työnkulut kuluraportteja varten.</span><span class="sxs-lookup"><span data-stu-id="4e056-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="4e056-122"><strong>Kulurivin nimike</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="4e056-123">Kuluraporttien rivinimikkeiden hyväksyntätyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="4e056-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="4e056-124"><strong>Kulurivinimikkeen automaattinen kirjaaminen</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="4e056-125">Kuluraporttien rivinimikkeiden automaattisten kirjaustyönkulkujen luominen.</span><span class="sxs-lookup"><span data-stu-id="4e056-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="4e056-126"><strong>Matkahankinta</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="4e056-127">Luo matkustusehdotusten hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="4e056-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="4e056-128"><strong>Käteisennakkopyyntö</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="4e056-129">Luo hyväksyntätyönkulkuja käteisennakkopyynnöille.</span><span class="sxs-lookup"><span data-stu-id="4e056-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="4e056-130"><strong>Arvonlisäveron palautus</strong></span><span class="sxs-lookup"><span data-stu-id="4e056-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="4e056-131">Luo arvonlisäveron (ALV) palautuksen hyväksyntätyönkulkuja.</span><span class="sxs-lookup"><span data-stu-id="4e056-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

