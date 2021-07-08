---
title: Taloushallinnon raportoinnin usein kysytyt kysymykset
description: Tämä ohjeaihe sisältää vastauksia eräisiin usein kysyttyihin talousraportoinnin kysymyksiin.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266630"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="b9a11-103">Taloushallinnon raportoinnin usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="b9a11-103">Financial reporting FAQ</span></span>

<span data-ttu-id="b9a11-104">Tämä ohjeaihe sisältää vastauksia usein kysyttyihin talousraportoinnin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="b9a11-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="b9a11-105">Miten rajoitan raportin käyttöoikeuksia puurakenteen suojauksen avulla?</span><span class="sxs-lookup"><span data-stu-id="b9a11-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="b9a11-106">Seuraavassa esimerkissä kerrotaan, miten raportin käyttöoikeuksia rajoitetaan puurakenteen suojauksen avulla.</span><span class="sxs-lookup"><span data-stu-id="b9a11-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="b9a11-107">USMF-esittely-yrityksellä on **taseraportti**, johon kaikilla taloushallinnon raportoinnin käyttäjillä ei pitäisi olla käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="b9a11-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="b9a11-108">Voit rajoittaa yksittäisen raportin käyttöoikeutta puurakenteen suojauksen avulla siten, että vain tietyt käyttäjät voivat käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="b9a11-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="b9a11-109">Kirjaudu Financial Reporter Report Designer -palveluun.</span><span class="sxs-lookup"><span data-stu-id="b9a11-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="b9a11-110">Luo uusi puumääritys valitsemalla **Tiedosto \> Uusi \> Puumäritys**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="b9a11-111">Kaksoisnapauta (tai kaksoisnapsauta) **Yhteenveto**-riviä **Yksikkösuojaus**-sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="b9a11-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="b9a11-112">Valitse **Käyttäjät ja ryhmät**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="b9a11-113">Valitse käyttäjät tai ryhmät, joiden on voitava käyttää tätä raporttia.</span><span class="sxs-lookup"><span data-stu-id="b9a11-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="b9a11-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-114">Select **Save**.</span></span>
7. <span data-ttu-id="b9a11-115">Lisää uusi puumäärityksesi raportin määritykseen.</span><span class="sxs-lookup"><span data-stu-id="b9a11-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="b9a11-116">Valitse puumäärityksessä **Asetus**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="b9a11-117">Valitse sitten **Raportointiyksikön valinta** -kohdassa **Sisällytä kaikki yksiköt**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="b9a11-118">Miten tunnistan tilit, jotka eivät täsmää saldojeni kanssa?</span><span class="sxs-lookup"><span data-stu-id="b9a11-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="b9a11-119">Jos sinulla on raportti, jossa ei ole täsmääviä saldoja, käytä seuraavia toimia tilien ja niiden varianssien tunnistamiseksi.</span><span class="sxs-lookup"><span data-stu-id="b9a11-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="b9a11-120">Financial Reporter Report Designer -palvelussa</span><span class="sxs-lookup"><span data-stu-id="b9a11-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="b9a11-121">Luo uusi rivimääritys.</span><span class="sxs-lookup"><span data-stu-id="b9a11-121">Create a new row definition.</span></span>
2. <span data-ttu-id="b9a11-122">Valitse **Muokkaa \> Lisää rivit dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="b9a11-123">Valitse **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="b9a11-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-124">Select **OK**.</span></span>
5. <span data-ttu-id="b9a11-125">Tallenna rivimääritys.</span><span class="sxs-lookup"><span data-stu-id="b9a11-125">Save the row definition.</span></span>
6. <span data-ttu-id="b9a11-126">Luo uusi sarakemääritys.</span><span class="sxs-lookup"><span data-stu-id="b9a11-126">Create a new column definition.</span></span>
7. <span data-ttu-id="b9a11-127">Luo uusi raportin määritys.</span><span class="sxs-lookup"><span data-stu-id="b9a11-127">Create a new report definition.</span></span>
8. <span data-ttu-id="b9a11-128">Valitse **Asetukset** ja poista tämän vaihtoehdon valinta.</span><span class="sxs-lookup"><span data-stu-id="b9a11-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="b9a11-129">Luo raportti.</span><span class="sxs-lookup"><span data-stu-id="b9a11-129">Generate the report.</span></span> 
10. <span data-ttu-id="b9a11-130">Vie raportti Microsoft Exceliin.</span><span class="sxs-lookup"><span data-stu-id="b9a11-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="b9a11-131">Dynamics 365 Financessa</span><span class="sxs-lookup"><span data-stu-id="b9a11-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="b9a11-132">Mene kohtaan **Pääkirja \> Kyselyt ja raportit \> Pääkirja**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="b9a11-133">Määritä seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="b9a11-133">Set the following fields:</span></span>

    - <span data-ttu-id="b9a11-134">**Aloituspäivä** – syötä tilikauden alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="b9a11-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="b9a11-135">**Päättymispäivämäärä** – syötä päivämäärä, jolle raportti luodaan.</span><span class="sxs-lookup"><span data-stu-id="b9a11-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="b9a11-136">**Taloushallinnon dimensio** – aseta tämän kentän arvoksi **Asetettu päätili**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="b9a11-137">Valitse **Laske**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="b9a11-138">Vie raportti Exceliin.</span><span class="sxs-lookup"><span data-stu-id="b9a11-138">Export the report to Excel.</span></span>

<span data-ttu-id="b9a11-139">Nyt sinun pitäisi pystyä kopioimaan tiedot Financial Reporterin Excel-raportista **Pääkirja**-raporttiin, jotta voit verrata **Loppusaldo**-sarakkeita.</span><span class="sxs-lookup"><span data-stu-id="b9a11-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="b9a11-140">Kun suunnittelen raportin Report Designerissa tai kun luon talousraportin, näyttöön tulee seuraava sanoma: "Työvaihetta ei voitu suorittaa loppuun tietopalvelun kehikossa olevan ongelman vuoksi."</span><span class="sxs-lookup"><span data-stu-id="b9a11-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="b9a11-141">Miten reagoin?</span><span class="sxs-lookup"><span data-stu-id="b9a11-141">How should I respond?</span></span>

<span data-ttu-id="b9a11-142">Sanoma ilmaisee, että virhe tapahtui, kun järjestelmä yritti hakea taloushallinnon metatietoja tietovaraston osajoukosta käyttäessäsi talousraportointia.</span><span class="sxs-lookup"><span data-stu-id="b9a11-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="b9a11-143">Tähän ongelmaan voi reagoida kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="b9a11-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="b9a11-144">Tarkista tietojen integroinnin tila menemällä Report Designerin kohtaan **Työkalut \> Integroinnin tila**.</span><span class="sxs-lookup"><span data-stu-id="b9a11-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="b9a11-145">Jos integrointi on kesken, odota sen valmistumista.</span><span class="sxs-lookup"><span data-stu-id="b9a11-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="b9a11-146">Yritä sen jälkeen uudelleen sitä, mitä teit saadessasi sanoman.</span><span class="sxs-lookup"><span data-stu-id="b9a11-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="b9a11-147">Ota yhteyttä tukeen, jotta ongelma voidaan tunnistaa ja käsitellä.</span><span class="sxs-lookup"><span data-stu-id="b9a11-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="b9a11-148">Järjestelmässä saattaa olla epäyhtenäisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="b9a11-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="b9a11-149">Tuki-insinöörit auttavat palvelimella olevan ongelman tunnistamisessa ja etsivät erityiset tiedot, jotka saattavat vaatia päivittämistä.</span><span class="sxs-lookup"><span data-stu-id="b9a11-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
