---
title: Lähetä ja hyväksy projektibudjetti
description: Tämä menettely osoittaa, miten voit luoda ja lähettää projektin budjetin.
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7aa7c301946b92b956f4b1b0f92985451ffe917e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149432"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="00907-103">Lähetä ja hyväksy projektibudjetti</span><span class="sxs-lookup"><span data-stu-id="00907-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="00907-104">Tämä menettely osoittaa, miten voit luoda ja lähettää projektin budjetin.</span><span class="sxs-lookup"><span data-stu-id="00907-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="00907-105">Kun luot projektibudjettia, voit antaa projektin arvioidut tuotot ja kustannukset ja hallita sitten toteutuneita projektitapahtumia niiden avulla.</span><span class="sxs-lookup"><span data-stu-id="00907-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="00907-106">Projektin budjetoinnissa kaikki alkuperäiset budjetit ja muutokset on lähettävä projektityönkulkuun hyväksyttäväksi.</span><span class="sxs-lookup"><span data-stu-id="00907-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="00907-107">Työnkulku parantaa prosessin hallintaa ja luo muutoshistoriatietueen.</span><span class="sxs-lookup"><span data-stu-id="00907-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="00907-108">Tämän tehtävä luotiin USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="00907-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="00907-109">Siirry **siirtymisruudussa** kohtaan **Moduulit > Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="00907-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="00907-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="00907-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="00907-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="00907-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="00907-112">Valitse **toimintoruudussa** **Suunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="00907-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="00907-113">Valitse **Projektibudjetti**.</span><span class="sxs-lookup"><span data-stu-id="00907-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="00907-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="00907-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="00907-115">Laajenna **Kustannukset**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="00907-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="00907-116">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="00907-116">Click **New**.</span></span>
9. <span data-ttu-id="00907-117">Valitse **Tapahtumatyyppi**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="00907-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="00907-118">Anna tai valitse **Luokka**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="00907-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="00907-119">Anna luku **Alkuperäinen budjetti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="00907-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="00907-120">Laajenna **Tuotot**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="00907-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="00907-121">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="00907-121">Click **New**.</span></span>
14. <span data-ttu-id="00907-122">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="00907-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="00907-123">Valitse **Tapahtumatyyppi**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="00907-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="00907-124">Anna tai valitse **Luokka**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="00907-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="00907-125">Anna luku **Alkuperäinen budjetti** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="00907-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="00907-126">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="00907-126">Click **Save**.</span></span>
19. <span data-ttu-id="00907-127">Valitse **Työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="00907-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="00907-128">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="00907-128">Click **Submit**.</span></span>
21. <span data-ttu-id="00907-129">Kirjoita **Kommentti**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="00907-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="00907-130">Valitse **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="00907-130">Click **Submit**.</span></span>

