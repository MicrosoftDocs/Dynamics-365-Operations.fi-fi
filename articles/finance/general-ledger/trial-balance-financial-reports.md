---
title: Pääkirjan talousraportit
description: Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175395"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="68344-104">Pääkirjan talousraportit</span><span class="sxs-lookup"><span data-stu-id="68344-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68344-105">Tässä artikkelissa kuvataan pääkirjojen oletusraportteja.</span><span class="sxs-lookup"><span data-stu-id="68344-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="68344-106">Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="68344-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="68344-107">Pääkirjan oletusraportit</span><span class="sxs-lookup"><span data-stu-id="68344-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="68344-108">Talousraportointi sisältää kolme pääkirjaraporttia.</span><span class="sxs-lookup"><span data-stu-id="68344-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="68344-109">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="68344-109">Default report</span></span>                                 | <span data-ttu-id="68344-110">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="68344-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68344-111">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="68344-112">Määrittää kaikkien tilien saldotiedot ja sisältää debet- ja kreditsaldot ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="68344-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="68344-113">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="68344-114">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="68344-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="68344-115">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="68344-116">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="68344-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="68344-117">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="68344-117">Building blocks</span></span>
<span data-ttu-id="68344-118">Pääkirjan talousraporteissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="68344-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="68344-119">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="68344-119">Default report</span></span>                                 | <span data-ttu-id="68344-120">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="68344-120">Row definition</span></span>          | <span data-ttu-id="68344-121">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="68344-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="68344-122">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="68344-123">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="68344-123">Trial Balance - Default</span></span> | <span data-ttu-id="68344-124">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="68344-125">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="68344-126">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="68344-126">Trial Balance - Default</span></span> | <span data-ttu-id="68344-127">Pääkirjan yhteenveto - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="68344-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="68344-128">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="68344-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="68344-129">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="68344-129">Trial Balance - Default</span></span> | <span data-ttu-id="68344-130">Pääkirjan yhteenveto vuosittain - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="68344-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="68344-131">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="68344-131">Row definition</span></span>

<span data-ttu-id="68344-132">Rivimääritys, Pääkirja – Oletusarvo, sisältää yhden rivin, joka hakee kaikki päätilit.</span><span class="sxs-lookup"><span data-stu-id="68344-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="68344-133">Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="68344-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="68344-134">Voit siirtyä raporttia tarkastellessasi yhdelle riville, kun haluat nähdä kunkin tilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="68344-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="68344-135">Voit muokata rivimääritystä niin, että se sisältää enemmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="68344-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="68344-136">Pääkirjan muokkaaminen - oletusrivimääritys, joka sisältää kaikkien tilien rivit. Noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="68344-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="68344-137">Valitse **Muokkaa** ja valitse sitten **Lisää rivejä dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="68344-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="68344-138">**Lisää rivejä dimensioista** -komennon avulla voit valita rivimääritykseen haluamasi dimensiot.</span><span class="sxs-lookup"><span data-stu-id="68344-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="68344-139">Tässä rivimäärityksessä käytetään **päätiliä**.</span><span class="sxs-lookup"><span data-stu-id="68344-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="68344-140">Varmista, että **päätili** sisältää kaikki et-merkit (&) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="68344-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="68344-141">Rivimääritys sisältää nyt kaikki oletusyrityksen päätilit.</span><span class="sxs-lookup"><span data-stu-id="68344-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="68344-142">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="68344-142">Column definition</span></span>

<span data-ttu-id="68344-143">Jokaisessa pääkirjan raportissa käytetään eri sarakemääritystä.</span><span class="sxs-lookup"><span data-stu-id="68344-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="68344-144">Nämä sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="68344-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="68344-145">**Yksityiskohtainen pääkirja – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="68344-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="68344-146">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="68344-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="68344-147">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="68344-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="68344-148">**ATTR (3)** – määritteet:</span><span class="sxs-lookup"><span data-stu-id="68344-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="68344-149">Tapahtumapäivä</span><span class="sxs-lookup"><span data-stu-id="68344-149">Transaction Date</span></span>
        -   <span data-ttu-id="68344-150">Tosite</span><span class="sxs-lookup"><span data-stu-id="68344-150">Voucher</span></span>
        -   <span data-ttu-id="68344-151">Kirjauskansion kuvaus</span><span class="sxs-lookup"><span data-stu-id="68344-151">Journal Description</span></span>
    -   <span data-ttu-id="68344-152">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="68344-153">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="68344-154">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="68344-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="68344-155">**Pääkirjan yhteenveto – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="68344-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="68344-156">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="68344-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="68344-157">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="68344-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="68344-158">**ATTR** – määrite:</span><span class="sxs-lookup"><span data-stu-id="68344-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="68344-159">Tosite</span><span class="sxs-lookup"><span data-stu-id="68344-159">Voucher</span></span>
    -   <span data-ttu-id="68344-160">**FD** – alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="68344-161">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="68344-162">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="68344-163">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="68344-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="68344-164">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="68344-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="68344-165">**Pääkirjan yhteenveto vuosittain – oletusarvo**</span><span class="sxs-lookup"><span data-stu-id="68344-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="68344-166">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="68344-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="68344-167">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="68344-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="68344-168">**ATTR** – määrite</span><span class="sxs-lookup"><span data-stu-id="68344-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="68344-169">Tosite</span><span class="sxs-lookup"><span data-stu-id="68344-169">Voucher</span></span>
    -   <span data-ttu-id="68344-170">**FD** – kuluvan vuoden alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="68344-171">**FD** – vain kuluvan vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="68344-172">**FD** – vain kuluvan vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="68344-173">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="68344-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="68344-174">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="68344-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="68344-175">**FD** – vain edellisen vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="68344-176">**FD** – vain edellisen vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="68344-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="68344-177">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="68344-177">Additional resources</span></span>
--------

[<span data-ttu-id="68344-178">Talousraportointi</span><span class="sxs-lookup"><span data-stu-id="68344-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="68344-179">Raporttien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="68344-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="68344-180">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="68344-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



