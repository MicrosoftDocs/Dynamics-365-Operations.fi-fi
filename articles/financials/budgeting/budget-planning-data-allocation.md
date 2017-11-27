---
title: Budjettisuunnittelun tietojen kohdistus
description: "Tässä artikkelissa on tietoja Microsoft Dynamics 365 for Finance and Operationsin, Enterprise Editionin käytettävissä olevista kohdistustavoista ja niiden käyttämisestä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c12b46ea68edd3d58c5b9abbc20a6ee6948b44f2
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="21c89-103">Budjettisuunnittelun tietojen kohdistus</span><span class="sxs-lookup"><span data-stu-id="21c89-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="21c89-104">Tässä artikkelissa on tietoja Microsoft Dynamics 365 for Finance and Operationsin, Enterprise Editionin käytettävissä olevista kohdistustavoista ja niiden käyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="21c89-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="21c89-105">Voit jakaa tiedot budjettisuunnitelmaan useilla eri tavoilla arvioitujen summien kuvaamista varten.</span><span class="sxs-lookup"><span data-stu-id="21c89-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="21c89-106">Kohdistusmenetelmät</span><span class="sxs-lookup"><span data-stu-id="21c89-106">Allocation methods</span></span>
<span data-ttu-id="21c89-107">Kolme kohdistusmenetelmää (Kohdista kausille, Kohdista dimensioille ja Käytä kirjanpidon kohdistussääntöjä) voivat luoda budjettisuunnitelman rivejä, jotka perustuvat saman budjettisuunnitelman riveihin.</span><span class="sxs-lookup"><span data-stu-id="21c89-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="21c89-108">Kolme muuta menetelmään (Yhdistä, Jaa ja Kopioi budjettisuunnitelmasta) voivat luoda budjettisuunnitelman rivejä muissa budjettisuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="21c89-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="21c89-109">Jokaiselle kuudelle kohdistusmenetelmälle voi määrittää kohdeskenaarion.</span><span class="sxs-lookup"><span data-stu-id="21c89-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="21c89-110">Kohdeskenaario voi olla sama kuin lähdeskenaario, mutta se voi olla myös erilainen.</span><span class="sxs-lookup"><span data-stu-id="21c89-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="21c89-111">Lisäksi voit määrittää, lisätäänkö uudet rivit budjettisuunnitelmaan vai korvataanko budjettisuunnitelman nykyiset rivit.</span><span class="sxs-lookup"><span data-stu-id="21c89-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="21c89-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Kohdista kausille** – Kaudenkohdistusluokkaa voi käyttää kohdistettaessa lähdebudjettiskenaarion budjettisuunnitelman rivit kohdeskenaarion kausiin.</span><span class="sxs-lookup"><span data-stu-id="21c89-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="21c89-113">Lähdesumma liitetään kohdeskenaarion useisiin riveihin kaudenkohdistusluokassa määritetyn prosenttiosuuden ja päivämäärän perusteella.</span><span class="sxs-lookup"><span data-stu-id="21c89-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="21c89-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Kohdista dimensioille** – Budjettisuunnitelman rivit kohdistetaan lähdebudjettisuunnittelun skenaariosta kohdeskenaarion yhteen tai useaan riviin valitussa budjetin kohdistusehdossa määritettyjen prosenttiosuuksien ja taloushallinnon dimensioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="21c89-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="21c89-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Yhdistä** – Budjettisuunnitelman rivit yhdistetään liittyvien (alitason) budjettisuunnitelmien lähdebudjettiskenaariosta päätason budjettisuunnitelman kohdeskenaarioon.</span><span class="sxs-lookup"><span data-stu-id="21c89-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="21c89-116">Tämän menetelmän avulla organisaation alemmalla tasolla valmistellut budjettisummat voidaan konsolidoida korkeammalla tasolla.</span><span class="sxs-lookup"><span data-stu-id="21c89-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="21c89-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Jaa** – Budjettisuunnitelman rivit jaetaan päätason budjettisuunnitelman lähdebudjettisuunnittelun skenaariosta liittyvän (alitason) budjettisuunnitelmien kohdeskenaarioon liittyvien suunnitelmien organisaatioyksiköiden taloushallinnon dimensioiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="21c89-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="21c89-118">Tämän menetelmän avulla organisaation korkeammalla tasolla valmistellut budjettisummat voidaan jakaa paikallisesti tarkastelua varten.</span><span class="sxs-lookup"><span data-stu-id="21c89-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="21c89-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Käytä kirjanpidon kohdistussääntöjä** – Budjettisuunnitelman rivit jaetaan lähdebudjettisuunnittelun skenaariosta kohdebudjettiskenaarioon valitun kirjanpidon kohdistussäännön perusteella.</span><span class="sxs-lookup"><span data-stu-id="21c89-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="21c89-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopioi budjettisuunnitelmasta** – Budjettirivit luodaan jaon kohdistusmenetelmän tapaan kohteessa liittyvän budjettisuunnitelman rivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="21c89-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="21c89-121">Tässä menetelmässä lähdebudjettisuunnitelman ei kuitenkaan tarvitse olla päätaso, mutta se voi olla mikä tahansa budjettisuunnitelman hierarkian korkeampi taso.</span><span class="sxs-lookup"><span data-stu-id="21c89-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="21c89-122">Tämä kohdistusmenetelmä on hyödyllinen, jos konsolidoidut summat on alun perin budjetoitu paljon korkeammalla tasolla, mutta jotka on siirrettävä organisaation alemmalle tasolle yksityiskohtaista tarkastelua ja oikaisua varten ennen ylemmän tason hyväksynnän saavuttamista.</span><span class="sxs-lookup"><span data-stu-id="21c89-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="21c89-123">Kohdistusmenetelmien käyttäminen budjettisuunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="21c89-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="21c89-124">Voit suorittaa kohdistuksia budjettisuunnitelman sivulla, kun valitset kohdistettavat rivit ja valitset sitten **Kohdista budjetti**.</span><span class="sxs-lookup"><span data-stu-id="21c89-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="21c89-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="21c89-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="21c89-126">Valitse seuraavaksi kohdistusmenetelmä.</span><span class="sxs-lookup"><span data-stu-id="21c89-126">Next, select an allocation method.</span></span> <span data-ttu-id="21c89-127">Tämän jälkeen määritetään jäljellä olevat kentät valitun menetelmän mukaan.</span><span class="sxs-lookup"><span data-stu-id="21c89-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="21c89-128">Nämä kentät sisältävät budjettisuunnitelman tietojen lähteen ja kohteen sekä vaihtoehdon, joka mahdollistaa lähteen kertomisen määritetyllä kertoimella kohdesummien luomisen yhteydessä. Tämä yksinkertaistaa joukko-oikaisua.</span><span class="sxs-lookup"><span data-stu-id="21c89-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="21c89-129">Voit määrittää myös **Liitä suunnitelmaan** -vaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="21c89-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="21c89-130">Korvaa aiemmin luodut budjettisuunnitelman rivit valitsemalla **Ei** tai säilytä aiemmin luodut budjettisuunnitelman rivit ja lisää uusia rivejä kohdistetuille summille valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="21c89-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="21c89-131">Kohdistusten automatisointi työnkulun aikana</span><span class="sxs-lookup"><span data-stu-id="21c89-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="21c89-132">Kohdistukset voidaan suorittaa erään tehokkaan toiminnon avulla automaattisesti budjettisuunnittelun työnkulun osana.</span><span class="sxs-lookup"><span data-stu-id="21c89-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="21c89-133">Budjettisuunnitelman siirtyessä työnkulussa, automaattiset tehtävät voivat käynnistää kohdistuksen tietyssä budjettisuunnittelun vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="21c89-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="21c89-134">Voit määrittää automaattisen kohdistuksen luomalla ensin kohdistusaikataulun **Budjettisuunnittelun konfigurointi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="21c89-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="21c89-135">Kohdistusaikataulu määrittää kohdistusmenetelmä, jota käytetään automaattisen kohdistuksen suorituksen aikana, sekä eri kohdistusvaihtoehtojen arvot (kuvaukset löytyvät edellisestä osasta).</span><span class="sxs-lookup"><span data-stu-id="21c89-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="21c89-136">Seuraavaksi luodaan vaiheen kohdistus **Budjettisuunnittelun konfigurointi** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="21c89-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="21c89-137">Vaiheen kohdistuksen liittää kohdistusaikataulun budjettisuunnittelun työnkulkuun ja vaiheeseen.</span><span class="sxs-lookup"><span data-stu-id="21c89-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="21c89-138">Lopuksi lisätään budjettisuunnittelun vaiheen kohdistuksen haluttuun työnkulun vaiheeseen automaattinen tehtävä.</span><span class="sxs-lookup"><span data-stu-id="21c89-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="21c89-139">Seuraavassa esimerkissä työnkulkuun on lisätty kaksi budjettisuunnittelun vaiheen kohdistusta (näkyvät punaisina).</span><span class="sxs-lookup"><span data-stu-id="21c89-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="21c89-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="21c89-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




