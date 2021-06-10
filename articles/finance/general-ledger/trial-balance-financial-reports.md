---
title: Pääkirjan talousraportit
description: Tässä artikkelissa kuvataan pääkirjojen oletusraportteja. Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.
author: jinniew
ms.date: 05/26/2021
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
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103655"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="d3634-104">Pääkirjan talousraportit</span><span class="sxs-lookup"><span data-stu-id="d3634-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3634-105">Tässä artikkelissa kuvataan pääkirjojen oletusraportteja.</span><span class="sxs-lookup"><span data-stu-id="d3634-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="d3634-106">Siinä myös kuvataan rakenneosat, jotka liittyvät näihin raportteihin sekä niiden muokkaaminen liiketoimintasi tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="d3634-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="d3634-107">Pääkirjan oletusraportit</span><span class="sxs-lookup"><span data-stu-id="d3634-107">Default trial balance reports</span></span>

<span data-ttu-id="d3634-108">Talousraportointi sisältää kolme pääkirjaraporttia.</span><span class="sxs-lookup"><span data-stu-id="d3634-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="d3634-109">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="d3634-109">Default report</span></span>                                 | <span data-ttu-id="d3634-110">Toiminnot</span><span class="sxs-lookup"><span data-stu-id="d3634-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3634-111">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d3634-112">Määrittää kaikkien tilien saldotiedot ja sisältää debet- ja kreditsaldot ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.</span><span class="sxs-lookup"><span data-stu-id="d3634-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="d3634-113">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d3634-114">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="d3634-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="d3634-115">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d3634-116">Määrittää kaikkien tilien saldotiedot ja sisältää alku- ja loppusaldot, debet- ja kreditsaldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.</span><span class="sxs-lookup"><span data-stu-id="d3634-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d3634-117">Rakenneosat</span><span class="sxs-lookup"><span data-stu-id="d3634-117">Building blocks</span></span>
<span data-ttu-id="d3634-118">Pääkirjan talousraporteissa käytetään seuraavia rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="d3634-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="d3634-119">Oletusraportti</span><span class="sxs-lookup"><span data-stu-id="d3634-119">Default report</span></span>                                 | <span data-ttu-id="d3634-120">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="d3634-120">Row definition</span></span>          | <span data-ttu-id="d3634-121">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="d3634-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="d3634-122">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="d3634-123">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="d3634-123">Trial Balance - Default</span></span> | <span data-ttu-id="d3634-124">Yksityiskohtainen pääkirja – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="d3634-125">Pääkirjan yhteenveto – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="d3634-126">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="d3634-126">Trial Balance - Default</span></span> | <span data-ttu-id="d3634-127">Pääkirjan yhteenveto - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="d3634-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="d3634-128">Pääkirjan yhteenveto vuosittain – oletus</span><span class="sxs-lookup"><span data-stu-id="d3634-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="d3634-129">Pääkirja - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="d3634-129">Trial Balance - Default</span></span> | <span data-ttu-id="d3634-130">Pääkirjan yhteenveto vuosittain - oletusarvo</span><span class="sxs-lookup"><span data-stu-id="d3634-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="d3634-131">Kun suoritetaan talousraportoinnin **Pääkirjasaldo**-raportti, valitse valintaruutuja, jotka koskevat **Näytä rivit, joilla ei ole summia**, ja **näytä raportit, joilla ei ole aktiivisia rivejä** **Asetukset**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="d3634-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="d3634-132">Rivimääritys</span><span class="sxs-lookup"><span data-stu-id="d3634-132">Row definition</span></span>

<span data-ttu-id="d3634-133">Rivimääritys, Pääkirja – Oletusarvo, sisältää yhden rivin, joka hakee kaikki päätilit.</span><span class="sxs-lookup"><span data-stu-id="d3634-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="d3634-134">Tämän vuoksi kuka tahansa voi luoda raportin ilman muutosten tekemistä.</span><span class="sxs-lookup"><span data-stu-id="d3634-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="d3634-135">Voit siirtyä raporttia tarkastellessasi yhdelle riville, kun haluat nähdä kunkin tilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="d3634-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="d3634-136">Voit muokata rivimääritystä niin, että se sisältää enemmän tietoja.</span><span class="sxs-lookup"><span data-stu-id="d3634-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="d3634-137">Pääkirjan muokkaaminen - oletusrivimääritys, joka sisältää kaikkien tilien rivit. Noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="d3634-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="d3634-138">Valitse **Muokkaa** ja valitse sitten **Lisää rivejä dimensioista**.</span><span class="sxs-lookup"><span data-stu-id="d3634-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="d3634-139">**Lisää rivejä dimensioista** -komennon avulla voit valita rivimääritykseen haluamasi dimensiot.</span><span class="sxs-lookup"><span data-stu-id="d3634-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="d3634-140">Tässä rivimäärityksessä käytetään **päätiliä**.</span><span class="sxs-lookup"><span data-stu-id="d3634-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="d3634-141">Varmista, että **päätili** sisältää kaikki et-merkit (&) ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3634-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="d3634-142">Rivimääritys sisältää nyt kaikki oletusyrityksen päätilit.</span><span class="sxs-lookup"><span data-stu-id="d3634-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d3634-143">Sarakemääritys</span><span class="sxs-lookup"><span data-stu-id="d3634-143">Column definition</span></span>

<span data-ttu-id="d3634-144">Jokaisessa pääkirjan raportissa käytetään eri sarakemääritystä.</span><span class="sxs-lookup"><span data-stu-id="d3634-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="d3634-145">Nämä sarakemääritykset sisältävät erityppisiä sarakkeita, joissa on useita yksityiskohtaisia tasoja ja taloushallinnon tietoja.</span><span class="sxs-lookup"><span data-stu-id="d3634-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d3634-146">**Yksityiskohtainen pääkirja – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="d3634-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="d3634-147">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3634-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3634-148">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="d3634-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3634-149">**ATTR (3)** – määritteet:</span><span class="sxs-lookup"><span data-stu-id="d3634-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="d3634-150">Tapahtumapäivä</span><span class="sxs-lookup"><span data-stu-id="d3634-150">Transaction Date</span></span>
        -   <span data-ttu-id="d3634-151">Tosite</span><span class="sxs-lookup"><span data-stu-id="d3634-151">Voucher</span></span>
        -   <span data-ttu-id="d3634-152">Kirjauskansion kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3634-152">Journal Description</span></span>
    -   <span data-ttu-id="d3634-153">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d3634-154">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d3634-155">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="d3634-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="d3634-156">**Pääkirjan yhteenveto – oletussaraketyypit:**</span><span class="sxs-lookup"><span data-stu-id="d3634-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="d3634-157">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="d3634-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3634-158">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3634-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3634-159">**ATTR** – määrite:</span><span class="sxs-lookup"><span data-stu-id="d3634-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="d3634-160">Tosite</span><span class="sxs-lookup"><span data-stu-id="d3634-160">Voucher</span></span>
    -   <span data-ttu-id="d3634-161">**FD** – alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="d3634-162">**FD** – vain debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="d3634-163">**FD** – vain kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="d3634-164">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="d3634-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d3634-165">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="d3634-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="d3634-166">**Pääkirjan yhteenveto vuosittain – oletusarvo**</span><span class="sxs-lookup"><span data-stu-id="d3634-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="d3634-167">**ACCT** – tilikoodit</span><span class="sxs-lookup"><span data-stu-id="d3634-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="d3634-168">**DESC** – rivimäärityksen kuvaus</span><span class="sxs-lookup"><span data-stu-id="d3634-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d3634-169">**ATTR** – määrite</span><span class="sxs-lookup"><span data-stu-id="d3634-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="d3634-170">Tosite</span><span class="sxs-lookup"><span data-stu-id="d3634-170">Voucher</span></span>
    -   <span data-ttu-id="d3634-171">**FD** – kuluvan vuoden alkusaldon taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="d3634-172">**FD** – vain kuluvan vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="d3634-173">**FD** – vain kuluvan vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="d3634-174">**CALC** – nettoerotus</span><span class="sxs-lookup"><span data-stu-id="d3634-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="d3634-175">**CALC** – loppusaldo</span><span class="sxs-lookup"><span data-stu-id="d3634-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="d3634-176">**FD** – vain edellisen vuoden debet-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="d3634-177">**FD** – vain edellisen vuoden kredit-tiedot sisältävät taloushallinnon tiedot</span><span class="sxs-lookup"><span data-stu-id="d3634-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3634-178">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="d3634-178">Additional resources</span></span>

[<span data-ttu-id="d3634-179">Taloushallinnon raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="d3634-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d3634-180">Raporttien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="d3634-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d3634-181">Dynamicsin talousraportointi -blogi</span><span class="sxs-lookup"><span data-stu-id="d3634-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
