---
title: Pääkirjan talousraportit
description: Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a9902471101b752c4b09d8ae28eb673743b7a53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816928"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="10e77-104">Pääkirjan talousraportit</span><span class="sxs-lookup"><span data-stu-id="10e77-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10e77-105">Tässä artikkelissa kuvataan pääkirjojen oletusraportteja.</span><span class="sxs-lookup"><span data-stu-id="10e77-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="10e77-106">Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="10e77-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="10e77-107">Pääkirjan oletusraportit</span><span class="sxs-lookup"><span data-stu-id="10e77-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="10e77-108">Talousraportointi sisältää kolme pääkirjaraporttia.</span><span class="sxs-lookup"><span data-stu-id="10e77-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="10e77-109">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="10e77-109">Default report</span></span>                                 | <span data-ttu-id="10e77-110">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="10e77-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10e77-111">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="10e77-112">Määrittää kaikkien tilien saldotiedot ja sisältää debet- ja kreditsaldot ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="10e77-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="10e77-113">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="10e77-114">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="10e77-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="10e77-115">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="10e77-116">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="10e77-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="10e77-117">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="10e77-117">Building blocks</span></span>
<span data-ttu-id="10e77-118">Pääkirjan talousraporteissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="10e77-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="10e77-119">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="10e77-119">Default report</span></span>                                 | <span data-ttu-id="10e77-120">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="10e77-120">Row definition</span></span>          | <span data-ttu-id="10e77-121">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="10e77-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="10e77-122">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="10e77-123">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="10e77-123">Trial Balance - Default</span></span> | <span data-ttu-id="10e77-124">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="10e77-125">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="10e77-126">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="10e77-126">Trial Balance - Default</span></span> | <span data-ttu-id="10e77-127">Pääkirjan yhteenveto - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="10e77-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="10e77-128">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="10e77-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="10e77-129">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="10e77-129">Trial Balance - Default</span></span> | <span data-ttu-id="10e77-130">Pääkirjan yhteenveto vuosittain - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="10e77-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="10e77-131">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="10e77-131">Row definition</span></span>

<span data-ttu-id="10e77-132">Rivimääritys, Pääkirja – Oletusarvo, sisältää yhden rivin, joka hakee kaikki päätilit.</span><span class="sxs-lookup"><span data-stu-id="10e77-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="10e77-133">Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="10e77-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="10e77-134">Voit siirtyä raporttia tarkastellessasi yhdelle riville, kun haluat nähdä kunkin tilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="10e77-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="10e77-135">Voit muokata rivimääritystä niin, että se sisältää enemmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="10e77-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="10e77-136">Pääkirjan muokkaaminen - oletusrivimääritys, joka sisältää kaikkien tilien rivit. Noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="10e77-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="10e77-137">Valitse **Muokkaa** ja valitse sitten **Lisää rivejä dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="10e77-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="10e77-138">**Lisää rivejä dimensioista** -komennon avulla voit valita rivimääritykseen haluamasi dimensiot.</span><span class="sxs-lookup"><span data-stu-id="10e77-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="10e77-139">Tässä rivimäärityksessä käytetään **päätiliä**.</span><span class="sxs-lookup"><span data-stu-id="10e77-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="10e77-140">Varmista, että **päätili** sisältää kaikki et-merkit (&) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="10e77-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="10e77-141">Rivimääritys sisältää nyt kaikki oletusyrityksen päätilit.</span><span class="sxs-lookup"><span data-stu-id="10e77-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="10e77-142">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="10e77-142">Column definition</span></span>

<span data-ttu-id="10e77-143">Jokaisessa pääkirjan raportissa käytetään eri sarakemääritystä.</span><span class="sxs-lookup"><span data-stu-id="10e77-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="10e77-144">Nämä sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="10e77-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="10e77-145">**Yksityiskohtainen pääkirja – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="10e77-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="10e77-146">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="10e77-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="10e77-147">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="10e77-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="10e77-148">**ATTR (3)** – määritteet:</span><span class="sxs-lookup"><span data-stu-id="10e77-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="10e77-149">Tapahtumapäivä</span><span class="sxs-lookup"><span data-stu-id="10e77-149">Transaction Date</span></span>
        -   <span data-ttu-id="10e77-150">Tosite</span><span class="sxs-lookup"><span data-stu-id="10e77-150">Voucher</span></span>
        -   <span data-ttu-id="10e77-151">Kirjauskansion kuvaus</span><span class="sxs-lookup"><span data-stu-id="10e77-151">Journal Description</span></span>
    -   <span data-ttu-id="10e77-152">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="10e77-153">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="10e77-154">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="10e77-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="10e77-155">**Pääkirjan yhteenveto – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="10e77-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="10e77-156">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="10e77-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="10e77-157">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="10e77-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="10e77-158">**ATTR** – määrite:</span><span class="sxs-lookup"><span data-stu-id="10e77-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="10e77-159">Tosite</span><span class="sxs-lookup"><span data-stu-id="10e77-159">Voucher</span></span>
    -   <span data-ttu-id="10e77-160">**FD** – alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="10e77-161">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="10e77-162">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="10e77-163">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="10e77-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="10e77-164">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="10e77-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="10e77-165">**Pääkirjan yhteenveto vuosittain – oletusarvo**</span><span class="sxs-lookup"><span data-stu-id="10e77-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="10e77-166">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="10e77-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="10e77-167">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="10e77-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="10e77-168">**ATTR** – määrite</span><span class="sxs-lookup"><span data-stu-id="10e77-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="10e77-169">Tosite</span><span class="sxs-lookup"><span data-stu-id="10e77-169">Voucher</span></span>
    -   <span data-ttu-id="10e77-170">**FD** – kuluvan vuoden alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="10e77-171">**FD** – vain kuluvan vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="10e77-172">**FD** – vain kuluvan vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="10e77-173">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="10e77-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="10e77-174">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="10e77-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="10e77-175">**FD** – vain edellisen vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="10e77-176">**FD** – vain edellisen vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="10e77-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="10e77-177">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="10e77-177">Additional resources</span></span>
--------

[<span data-ttu-id="10e77-178">Taloushallinnon raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="10e77-178">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="10e77-179">Raporttien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="10e77-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="10e77-180">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="10e77-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]