---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tässä ohjeaiheessa käsitellään kysymyksiä, joita muilla käyttäjillä on ollut taloushallinnon raportoinnista.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923022"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="4b196-103">Taloushallinnon raportoinnin usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="4b196-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="4b196-104">Tämä ohjeaihe sisältää vastauksia usein kysyttyihin talousraportoinnin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="4b196-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="4b196-105">Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?</span><span class="sxs-lookup"><span data-stu-id="4b196-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="4b196-106">Seuraavassa esimerkissä kerrotaan, miten raportin käyttöoikeuksia rajoitetaan puurakenteen suojauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="4b196-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="4b196-107">USFM-esittely-yrityksellä on taseraportti, johon kaikilla taloushallinnon raportoinnin käyttäjillä ei pitäisi olla käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="4b196-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="4b196-108">Voit rajoittaa käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää raporttia.</span><span class="sxs-lookup"><span data-stu-id="4b196-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="4b196-109">Rajoita käyttöoikeuksia noudattamalla seuraavia ohjeita:</span><span class="sxs-lookup"><span data-stu-id="4b196-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="4b196-110">Kirjaudu Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="4b196-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="4b196-111">Luo uusi puumääritys.</span><span class="sxs-lookup"><span data-stu-id="4b196-111">Create a new tree definition.</span></span> <span data-ttu-id="4b196-112">Siirry kohtaan **Tiedosto > Uusi > Puumääritys**.</span><span class="sxs-lookup"><span data-stu-id="4b196-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="4b196-113">Kaksoisnapsauta **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="4b196-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="4b196-114">Valitse **Käyttäjät ja ryhmät**.</span><span class="sxs-lookup"><span data-stu-id="4b196-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="4b196-115">Valitse käyttäjät tai ryhmät, joiden on voitava käyttää tätä raporttia.</span><span class="sxs-lookup"><span data-stu-id="4b196-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="4b196-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="4b196-116">Select **Save**.</span></span>
7. <span data-ttu-id="4b196-117">Lisää uusi puumäärityksesi raportin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="4b196-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="4b196-118">Valitse puumäärityksessä **Asetus**.</span><span class="sxs-lookup"><span data-stu-id="4b196-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="4b196-119">Valitse **Raportointiyksikön valinta** -kohdassa **Sisällytä kaikki yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="4b196-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="4b196-120">Miten tunnistan tilit, jotka eivät täsmää saldojeni kanssa?</span><span class="sxs-lookup"><span data-stu-id="4b196-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="4b196-121">Jos sinulla on raportti, jossa ei ole täsmääviä saldoja, voit kokeilla seuraavia toimia tilien ja niiden varianssien tunnistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="4b196-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="4b196-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="4b196-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="4b196-123">Luo uusi rivimääritys kohteessa Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="4b196-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="4b196-124">Valitse **Muokkaa > Lisää rivit dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="4b196-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="4b196-125">Valitse **Päätili**.</span><span class="sxs-lookup"><span data-stu-id="4b196-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="4b196-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="4b196-126">Select **OK**.</span></span>
5. <span data-ttu-id="4b196-127">Tallenna rivimääritys.</span><span class="sxs-lookup"><span data-stu-id="4b196-127">Save the row definition.</span></span>
6. <span data-ttu-id="4b196-128">Luo uusi sarakemääritys.</span><span class="sxs-lookup"><span data-stu-id="4b196-128">Create a new column definition</span></span>
7. <span data-ttu-id="4b196-129">Luo uusi raportin määritys.</span><span class="sxs-lookup"><span data-stu-id="4b196-129">Create a new report definition.</span></span>
8. <span data-ttu-id="4b196-130">Valitse **Asetukset** ja poista tämän vaihtoehdon valinta.</span><span class="sxs-lookup"><span data-stu-id="4b196-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="4b196-131">Luo raportti.</span><span class="sxs-lookup"><span data-stu-id="4b196-131">Generate the report.</span></span> 
10. <span data-ttu-id="4b196-132">Vie raportti Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="4b196-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="4b196-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="4b196-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="4b196-134">Valitse Dynamics 365 Financessa **Pääkirja > Kyselyt ja raportit > Pääkirja**.</span><span class="sxs-lookup"><span data-stu-id="4b196-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="4b196-135">Määritä seuraavat parametrit:</span><span class="sxs-lookup"><span data-stu-id="4b196-135">Set the following parameters:</span></span>
   - <span data-ttu-id="4b196-136">**Aloituspäivä** - syötä tilikauden alku.</span><span class="sxs-lookup"><span data-stu-id="4b196-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="4b196-137">**Aloituspäivä** - syötä päivämäärä, jolle raportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="4b196-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="4b196-138">**Taloushallinnon dimensio** - aseta tämän kentän arvoksi **Asetettu päätili**.</span><span class="sxs-lookup"><span data-stu-id="4b196-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="4b196-139">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="4b196-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="4b196-140">Vie raportti Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="4b196-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="4b196-141">Nyt sinun pitäisi nyt pystyä kopioimaan tiedot Raporttien suunnitteluohjelman Excel-raportista Pääkirja-raporttiin, jotta voit verrata **Loppusaldo**-sarakkeita.</span><span class="sxs-lookup"><span data-stu-id="4b196-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]