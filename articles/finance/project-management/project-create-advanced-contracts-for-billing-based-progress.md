---
title: Tilaan perustuvien edistyksellisten laskutussopimusten luominen
description: Tässä ohjeaiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttiosuuden perusteella.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
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
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282823"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="04499-103">Tilaan perustuvien edistyksellisten laskutussopimusten luominen</span><span class="sxs-lookup"><span data-stu-id="04499-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="04499-104">Tässä ohjeaiheessa kerrotaan, miten projektisopimuksia luodaan, jotta asiakkaille voidaan luoda laskuja valmiin työn prosenttiosuuden perusteella.</span><span class="sxs-lookup"><span data-stu-id="04499-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="04499-105">Laskusummat lasketaan automaattisesti projektissa määritetyn työn budjettiluokkia varten.</span><span class="sxs-lookup"><span data-stu-id="04499-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="04499-106">Laskujen ajoitus määritetään, kun projektisopimus neuvotellaan asiakkaan kanssa.</span><span class="sxs-lookup"><span data-stu-id="04499-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="04499-107">Näiden ohjeaiheiden avulla voit määrittää sopimuksen, liittyvän projektin ja laskutussäännöt, joita käytetään projektia varten määritetyn työn budjettiluokkien laskujen summien laskentaan.</span><span class="sxs-lookup"><span data-stu-id="04499-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="04499-108">Kun sopimus ja projekti on luotu, voit määrittää projektin tiedot.</span><span class="sxs-lookup"><span data-stu-id="04499-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="04499-109">Voit esimerkiksi määrittää toiminnot ja projektin työntekijät.</span><span class="sxs-lookup"><span data-stu-id="04499-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="04499-110">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="04499-110">Example</span></span>

<span data-ttu-id="04499-111">Organisaatiosi on ohjelmistokehitysyritys.</span><span class="sxs-lookup"><span data-stu-id="04499-111">Your organization is a software development firm.</span></span> <span data-ttu-id="04499-112">Sitoudut kehittämään asiakkaalle palkanlaskennan kirjanpitopaketin 20 000 dollarin (USD) kokonaismaksua vastaan.</span><span class="sxs-lookup"><span data-stu-id="04499-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="04499-113">Organisaatiosi sitoutuu lähettämään asiakkaalle laskun, kun projektista on valmiina määritetty prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="04499-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="04499-114">Voit määrittää työlle seuraavat projektiluokat, jotta voit käyttää niitä laskutusprosessissa:</span><span class="sxs-lookup"><span data-stu-id="04499-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="04499-115">Konsultointi</span><span class="sxs-lookup"><span data-stu-id="04499-115">Consulting</span></span>
- <span data-ttu-id="04499-116">Suunnittelu</span><span class="sxs-lookup"><span data-stu-id="04499-116">Design</span></span>
- <span data-ttu-id="04499-117">Asentaminen</span><span class="sxs-lookup"><span data-stu-id="04499-117">Installation</span></span>

<span data-ttu-id="04499-118">Määrität myös laskutussäännöt, jotka laskevat automaattisesti laskujen summat kunkin luokan projektitöiden valmistumisprosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="04499-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="04499-119">Budjettipäällikkö luo budjetin projektiluokkia varten.</span><span class="sxs-lookup"><span data-stu-id="04499-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="04499-120">Valmiin työn määrä lasketaan automaattisesti verrattuna todellisen työn prosenttiosuutta budjetoituihin määriin.</span><span class="sxs-lookup"><span data-stu-id="04499-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="04499-121">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="04499-121">Prerequisites</span></span>

<span data-ttu-id="04499-122">Ennen kuin luot projektin, joka käyttää laskutussääntöjä, sinun on määritettävä laskutussääntöjen numerosarjat sekä maksukirjauskansio, jota käytetään edistymisen kirjaamiseen.</span><span class="sxs-lookup"><span data-stu-id="04499-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="04499-123">Valitse **Projektinhallinta ja kirjanpito** \> **Asetukset** \> **Projektinhallinnan ja kirjanpidon parametrit**.</span><span class="sxs-lookup"><span data-stu-id="04499-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="04499-124">Määritä **Projektinhallinnan ja kirjanpidon parametrit** -sivun **numerosarjat**-välilehdessä numerosarja, jota haluat käyttää laskutussääntöjen luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="04499-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="04499-125">Siirry kohtaan **Projektinhallinta ja kirjanpito** \> **Kirjauskansiot** \> **Maksu**.</span><span class="sxs-lookup"><span data-stu-id="04499-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="04499-126">Valitse **Maksukirjauskansio**-sivulla **Uusi** ja kirjoita kirjauskansion nimi.</span><span class="sxs-lookup"><span data-stu-id="04499-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="04499-127">Sopimuksen luominen edistymiseen perustuvaa laskutusta varten</span><span class="sxs-lookup"><span data-stu-id="04499-127">Create a contract for progress billings</span></span>

<span data-ttu-id="04499-128">Tämän toiminnon avulla voit luoda projektisopimuksen kiinteähintaista projektia varten.</span><span class="sxs-lookup"><span data-stu-id="04499-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="04499-129">Luot projektilaskun, kun projektin työstä valmistunut osuus saavuttaa määritetyn prosenttiosuuden.</span><span class="sxs-lookup"><span data-stu-id="04499-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="04499-130">Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Projektisopimukset**.</span><span class="sxs-lookup"><span data-stu-id="04499-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="04499-131">Valitse **Projektisopimukset**-sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="04499-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="04499-132">Määritä **Uusi projektisopimus** -valintaikkunassa seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="04499-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="04499-133">**Nimi**</span><span class="sxs-lookup"><span data-stu-id="04499-133">**Name**</span></span>
    - <span data-ttu-id="04499-134">**Rahoitustyyppi**</span><span class="sxs-lookup"><span data-stu-id="04499-134">**Funding type**</span></span>
    - <span data-ttu-id="04499-135">**Rahoituslähde**</span><span class="sxs-lookup"><span data-stu-id="04499-135">**Funding source**</span></span>
    - <span data-ttu-id="04499-136">**Myyntivaluutta** – Tätä valuuttaa käytetään oletusarvoisesti asiakkaan laskuille, jotka on liitetty projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="04499-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="04499-137">Voit kuitenkin muuttaa tietyn myyntilaskun myyntivaluuttaa.</span><span class="sxs-lookup"><span data-stu-id="04499-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="04499-138">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="04499-138">Select **OK**.</span></span> <span data-ttu-id="04499-139">Tiedot kopioidaan **Projektisopimukset**-sivun otsikkoon.</span><span class="sxs-lookup"><span data-stu-id="04499-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="04499-140">Täytä **Projektisopimukset**-sivulla loput projektin pakolliset tiedot.</span><span class="sxs-lookup"><span data-stu-id="04499-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="04499-141">Projektin luominen edistymiseen perustuvaa laskutusta varten</span><span class="sxs-lookup"><span data-stu-id="04499-141">Create a project for progress billings</span></span>

<span data-ttu-id="04499-142">Näiden ohjeiden avulla voit luoda projektin ja projektisopimukseen liittyvät aliprojektit.</span><span class="sxs-lookup"><span data-stu-id="04499-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="04499-143">Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="04499-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="04499-144">Valitse **Kaikki projektit** -sivulla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="04499-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="04499-145">Valitse **Uusi projekti** -valintaikkunan **Projektityyppi**-kentässä**Aika ja materiaali**.</span><span class="sxs-lookup"><span data-stu-id="04499-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="04499-146">Valitse projektiryhmä.</span><span class="sxs-lookup"><span data-stu-id="04499-146">Select a project group.</span></span> <span data-ttu-id="04499-147">Projektiryhmä määrittää ryhmään liitettyjen projektien kirjaustiedot.</span><span class="sxs-lookup"><span data-stu-id="04499-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="04499-148">Valitse **Luo projekti**.</span><span class="sxs-lookup"><span data-stu-id="04499-148">Select **Create project**.</span></span>
6. <span data-ttu-id="04499-149">Kun projekti on luotu, määritä projektin vaiheeksi **Käsittelyssä** .</span><span class="sxs-lookup"><span data-stu-id="04499-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="04499-150">Budjetin luominen projektia varten</span><span class="sxs-lookup"><span data-stu-id="04499-150">Create a budget for a project</span></span>

<span data-ttu-id="04499-151">Budjettiluokkien avulla lasketaan automaattisesti laskusummat, jotka laskutetaan asiakkaalta kunkin luokan valmistuneesta työstä.</span><span class="sxs-lookup"><span data-stu-id="04499-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="04499-152">Seuraavia vaiheita noudattamalla voit luoda arvioituja kustannuksia koskevia budjettiluokkia.</span><span class="sxs-lookup"><span data-stu-id="04499-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="04499-153">Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Kaikki projektit**.</span><span class="sxs-lookup"><span data-stu-id="04499-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="04499-154">Valitse ja avaa haluamasi projekti **Kaikki projektit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="04499-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="04499-155">Valitse **Projektit**-sivulla Toimintoruudun **Suunnitelma**-välilehden **Budjetti**-ryhmässä **Projektibudjetti**.</span><span class="sxs-lookup"><span data-stu-id="04499-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="04499-156">Anna **Projektibudjetti**-sivulla arvioitu kustannus projektin jokaista luokkaa varten.</span><span class="sxs-lookup"><span data-stu-id="04499-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="04499-157">Laskutussääntöjen luominen työn edistymiseen perustuvaa laskutusta varten</span><span class="sxs-lookup"><span data-stu-id="04499-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="04499-158">Valitse **Projektinhallinta ja kirjanpito** \> **Projektit** \> **Projektisopimukset**.</span><span class="sxs-lookup"><span data-stu-id="04499-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="04499-159">Valitse **Projektisopimukset** -sivulla projektisopimus ja avaa se.</span><span class="sxs-lookup"><span data-stu-id="04499-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="04499-160">Valitse projektisopimus-sivun **Laskutussäännöt**-pikavälilehdessä **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="04499-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="04499-161">Valitse **Laskutussääntö**-sivun **Rivityyppi**-kentässä **Edistyminen**.</span><span class="sxs-lookup"><span data-stu-id="04499-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="04499-162">Kirjoita sopimuksen kokonaisarvo **Laskutussäännön rivitiedot** -pikavälilehden **Sopimuksen arvo** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="04499-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="04499-163">Valitse **Luokka**-kentässä luokka, johon maksutapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="04499-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="04499-164">Valitse **Projekti**-kentässä projekti tai tehtävä, joka käyttää laskutussääntöä.</span><span class="sxs-lookup"><span data-stu-id="04499-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="04499-165">Valinnainen: Määritä laskutussääntö lisäprojekteihin.</span><span class="sxs-lookup"><span data-stu-id="04499-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="04499-166">Valitse **Projekti**-pikavälilehden **Käytettävissä olevat projektit** -osasta ja lisää sitten projekti **Valitut projektit** -osaan valitsemalla oikea nuolipainike.</span><span class="sxs-lookup"><span data-stu-id="04499-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="04499-167">Valinnainen: Laske prosenttimäärä, jonka asiakas pidättää laskun maksuista.</span><span class="sxs-lookup"><span data-stu-id="04499-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="04499-168">Valitse rahoituslähde **Maksun pidätysehto** -pikavälilehdeltä ja kirjoita sitten **Pidätysprosentti**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="04499-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="04499-169">Toista tämä vaiheet, jos haluat luoda lisää projektisopimuksen laskutussääntöjä.</span><span class="sxs-lookup"><span data-stu-id="04499-169">Repeat these steps to create additional billing rules for the project contract.</span></span>
