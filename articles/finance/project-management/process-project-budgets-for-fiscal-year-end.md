---
title: Projektibudjettien siirtäminen tilikauden lopussa
description: Tässä artikkelissa annetaan tietoja jäljellä olevien budjettisummien siirtämisestä tuleville vuosille ja budjettirekisteritietojen luomisesta.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172327"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="dd5ee-103">Projektibudjettien siirtäminen tilikauden lopussa</span><span class="sxs-lookup"><span data-stu-id="dd5ee-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd5ee-104">Kun työskentelet usean vuoden projektissa, sinulla voi olla jäljellä olevaa budjettia tilikauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="dd5ee-105">Voit siirtää jäljellä olevat budjettimäärät tulevaan vuoteen ja luoda budjettirekisteritiedot niihin liittyvien pääkirjatilien summille.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="dd5ee-106">Tarkista ja analysoi jäljellä olevat budjettisummat ennen jäljellä olevien summien eteenpäin suorittamista.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="dd5ee-107">Jäljellä olevien budjettisummien tarkasteleminen ja analysoiminen</span><span class="sxs-lookup"><span data-stu-id="dd5ee-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="dd5ee-108">Suorita seuraavat toimet tarkastaaksesi projektien tilinpäätöksen budjettisummat, mutta älä siirrä summia eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="dd5ee-109">Siirry kohtaan **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="dd5ee-110">Tarkista **Projektibudjetin siirtoprosessi** -sivun **Vuoden lopun asetukset** -välilehdessä, että**Siirrettävät jäljellä olevat projektibudjetin summat** -vaihtoehto ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="dd5ee-111">Valitse **Parametrit**-ryhmän **Projektin budjettivuosi** -kentästä se tilikausi, jonka projektien jäljellä olevaa budjettisummaa haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="dd5ee-112">Valitse **Avaa tilikausi** -kentästä sen tilikauden alku, jonka jäljellä olevaa budjettisummaa haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="dd5ee-113">Valitse **Ennustemallista**-kentästä **Jäljellä oleva budjetti**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="dd5ee-114">Jos haluat sisällyttää projektit, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia, valitse **Näytä nolla jäljellä**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="dd5ee-115">Valitse **Valitse budjetit** -välilehdestä**Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit, ja valitse sitten **Prosessi**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="dd5ee-116">Suunnitellaksesi tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="dd5ee-117">Lisätietoja tietystä ruudun rivistä saat valitsemalla rivin ja valitsemalla sitten **Näytä budjetin tiedot** tai **Näytä tilit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="dd5ee-118">Tee siirtokirjaus jäljellä olevista budjettisummista</span><span class="sxs-lookup"><span data-stu-id="dd5ee-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="dd5ee-119">Kun käsittelet jäljellä olevat budjettisummat, voit luoda kirjanpitoon tapahtuman siirtokirjatuista summista.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="dd5ee-120">Jos haluat luoda kirjanpidon tapahtumia, täytä osan vaiheet, [Siirrä budjettisummat ja luo kirjanpidon tapahtumat](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="dd5ee-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="dd5ee-121">Siirtokirjatut budjettisummat siirretään ennustemalliin, joka valitaan siirtokirjausmalliksi **Ennustemallit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="dd5ee-122">Budjettisummien siirtokirjaaminen ja kirjanpitotapahtumien luonti</span><span class="sxs-lookup"><span data-stu-id="dd5ee-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="dd5ee-123">Valitse **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="dd5ee-124">Valitse **projektibudjetin siirtoprosessi** -sivulla **Vuoden loppu** ja ota sitten **Siirrä jäljellä olevat projektin budjettisummat** käyttöön ja **Luo budjettirekisterimerkinnät kirjanpitoon**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="dd5ee-125">Valitse **Parametrit**-välilehden **Projektin parametrit** -kenttäryhmästä seuraavat asiat:</span><span class="sxs-lookup"><span data-stu-id="dd5ee-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="dd5ee-126">**Projektibudjetin vuosi**: Valitse sen tilikauden alku, jonka jäljellä olevia budjettisummia haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="dd5ee-127">**Voitto ja tappio**: Luo voitto- ja tappiotapahtumat kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="dd5ee-128">**KET**: Luo keskeneräisten töiden (KET) tapahtumia kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="dd5ee-129">**Palkanlaskenta**: Luo palkanlaskennan tapahtumat kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="dd5ee-130">Anna seuraavat tiedot **Kirjanpito**-kenttärymässä:</span><span class="sxs-lookup"><span data-stu-id="dd5ee-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="dd5ee-131">Valitse **Tilikauden avaus**-kentästä se tilikausi, jolle haluat siirtää projektien jäljellä olevat budjettisummat.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="dd5ee-132">Oletusarvo on vuoden kuluttua **Projektibudjetin vuosi** -kentän arvosta.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="dd5ee-133">Valitse **Siirtokirjausjakso** -kentässä ajanjakso, johon haluat luoda kirjanpidon budjettirekisteritiedot.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="dd5ee-134">Tämä on yleensä uuden tilikauden ensimmäinen jakso.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="dd5ee-135">Anna seuraavat tiedot **Kopioi jostakin/johonkin** -kenttäryhmässä:</span><span class="sxs-lookup"><span data-stu-id="dd5ee-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="dd5ee-136">Valitse **Ennustemallista** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="dd5ee-137">Valitse **Kirjanpidon budjettimalli** -kentässä kirjanpidon budjettimalli, joka liittyy jäljellä kirjanpitoon siirrettäviin budjettisummiin.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="dd5ee-138">Jos haluat käyttää projektin myyntivaluuttaa niihin kirjanpidon tapahtumiin, jotka luodaan, kun siirrät budjettisummat projekteille, valitse **Siirrä myyntivaluutta** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="dd5ee-139">Kun vaihtoehto ei ole valittuna, tapahtumat käyttävät kirjanpitovaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="dd5ee-140">Valitse **Näytä nolla jäljellä** jos haluat sisällyttää projektit, joilla ei ole jäljellä olevia budjettimääriä, mutta jotka täyttävät muut perusteet, jotka valitsit alaruudussa näkyvissä projekteissa.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="dd5ee-141">Valitse **Valitse budjetit** -välilehdestä **Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="dd5ee-142">Jos haluat suunnitella tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="dd5ee-143">Valitse kunkin haluamasi projektin kohdalla projektirivin alussa oleva vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="dd5ee-144">Jos haluat valita kaikki projektit tai useimmat niistä, valitse vasemmassa yläkulmassa oleva valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="dd5ee-145">Jos haluat jättää minkä tahansa projektin käsittelyn pois, poista kyseisen projektin valintamerkki.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="dd5ee-146">Jos haluat siirtää valittujen projektien jäljellä olevat budjettimäärät valitulle tilikaudelle ja luoda budjettirekisteritiedot pääkirjaan, valitse **Prosessi**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="dd5ee-147">Budjettisummien siirtokirjaaminen ilman kirjanpitotapahtumien luontia</span><span class="sxs-lookup"><span data-stu-id="dd5ee-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="dd5ee-148">Siirry kohtaan **Projektinhallinta- ja kirjanpito** > **Kausittainen** > **Budjetit** > **Siirrettävät budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="dd5ee-149">Valitse **Projektibudjetin siirtoprosessi** -sivun **Vuoden lopun asetukset** -välilehdessä **Siirrettävät jäljellä olevat projektibudjetin summat**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="dd5ee-150">Valitse **Parametrit**-ryhmän **Projektin budjettivuosi** -kentästä se tilikausi, jonka projektien jäljellä olevaa budjettisummaa haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="dd5ee-151">Anna seuraavat tiedot **Kopioi jostakin/johonkin** -ryhmässä:</span><span class="sxs-lookup"><span data-stu-id="dd5ee-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="dd5ee-152">Valitse **Ennustemallista** -kentässä projektibudjetin ennustemalli, joka liittyy jäljellä oleviin budjettisummiin, jotka haluat siirtää projekteille.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="dd5ee-153">Valitse **Näytä nolla jäljellä**, jos haluat sisällyttää projektit, jotka vastaavat valittuja ehtoja ja joilla ei ole jäljellä olevaa budjettia.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="dd5ee-154">Valitse **Valitse budjetit** -ryhmästä **Hae kaikki budjetit**, jos haluat ladata kaikki valittuja ehtoja vastaavat budjetit.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="dd5ee-155">Suunnitellaksesi tietokantakyselyn, joka lataa ruutuun tietyn joukon projektibudjetteja, napsauta **Hae valitut budjetit**.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="dd5ee-156">Valitse kunkin haluamasi projektin kohdalla projektirivin alussa oleva vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="dd5ee-157">Valitse **Prosessi** siirtääksesi valittujen hankkeiden jäljellä olevat budjettisummat valitulle tilikaudelle.</span><span class="sxs-lookup"><span data-stu-id="dd5ee-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

