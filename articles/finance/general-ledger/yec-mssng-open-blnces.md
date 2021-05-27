---
title: Alkusaldot puuttuvat tilinpäätöksestä
description: Tässä ohjeaiheessa kerrotaan, miksi alkusaldot saattavat puuttua tilinpäätöksen yhteydessä, ja miten nämä puuttuvat saldot muodostetaan uudelleen.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028561"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="ecd12-103">Alkusaldot puuttuvat tilinpäätöksestä</span><span class="sxs-lookup"><span data-stu-id="ecd12-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecd12-104">Tässä ohjeaiheessa kerrotaan, miksi alkusaldot saattavat puuttua tilinpäätöksen yhteydessä, ja miten nämä puuttuvat saldot muodostetaan uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ecd12-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="ecd12-105">Oire</span><span class="sxs-lookup"><span data-stu-id="ecd12-105">Symptom</span></span>

<span data-ttu-id="ecd12-106">Miksi alkusaldoja ei ole kirjanpidon tilinpäätöksen suorittamisen jälkeen?</span><span class="sxs-lookup"><span data-stu-id="ecd12-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="ecd12-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ecd12-107">Resolution</span></span>

<span data-ttu-id="ecd12-108">Tarkista alla olevat kohdat, jos kirjanpidon tilinpäätös on tehty ja tämän jälkeen luotu pääkirja, jossa eivät näy seuraavan tilikauden alkusaldot.</span><span class="sxs-lookup"><span data-stu-id="ecd12-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="ecd12-109">Jos **Kumoa edellinen sulkeminen** ‑kentän arvoksi on valittu **Kyllä**, edellinen saman tilikauden tilinpäätös peruutetaan.</span><span class="sxs-lookup"><span data-stu-id="ecd12-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="ecd12-110">Kun suoritetaan prosessi, joka peruuttaa tilinpäätöksen, kaikki loppusaldo- ja alkusaldomerkinnät poistetaan, ikään kuin tilinpäätöstä ei olisi missään vaiheessa suoritettu.</span><span class="sxs-lookup"><span data-stu-id="ecd12-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="ecd12-111">Tositteet poistetaan myös.</span><span class="sxs-lookup"><span data-stu-id="ecd12-111">The vouchers are also deleted.</span></span> <span data-ttu-id="ecd12-112">Tilinpäätösprosessia ei suoriteta uudelleen automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="ecd12-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="ecd12-113">Prosessi on aloitettava uudelleen siten, että **Kumoa edellinen sulkeminen** ‑asetuksen arvoksi päivitetään **Ei**.</span><span class="sxs-lookup"><span data-stu-id="ecd12-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="ecd12-114">Tämä skenaario sisältyy aiheeseen, jossa käsitellään tilinpäätöstä koskevia usein kysyttyjä kysymyksiä.</span><span class="sxs-lookup"><span data-stu-id="ecd12-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="ecd12-115">Lisätietoja on kohdassa [Vuoden lopun toimintoja koskevat usein kysytyt kysymykset](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="ecd12-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="ecd12-116">Oire</span><span class="sxs-lookup"><span data-stu-id="ecd12-116">Symptom</span></span>

<span data-ttu-id="ecd12-117">Suoritin tilinpäätöksen niin, että **Kumoa edellinen sulkeminen** -asetuksen arvo oli **Ei**. Tästä huolimatta tilikausi ei sisällä alkusaldoja.</span><span class="sxs-lookup"><span data-stu-id="ecd12-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="ecd12-118">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ecd12-118">Resolution</span></span>

<span data-ttu-id="ecd12-119">Tarkista ensin erätyön tila.</span><span class="sxs-lookup"><span data-stu-id="ecd12-119">First check the status of the batch job.</span></span> <span data-ttu-id="ecd12-120">Tilinpäätös sisältää useita yksittäisiä tehtäviä. Kriittisin tehtävä on erätehtävä, jonka tehtävän kuvaus on **Vaihe 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="ecd12-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="ecd12-121">Avaustapahtumien tai vaihtoehtoisesti päätöstapahtumien kirjaaminen kirjanpitoon tapahtuu tämän vaiheen aikana.</span><span class="sxs-lookup"><span data-stu-id="ecd12-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="ecd12-122">[![Erätyöhistorialuettelo](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="ecd12-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="ecd12-123">Jos tämän vaiheen suorittaminen onnistuu, mutta alkusaldot eivät näy **Pääkirjan kysely** -sivulla (**Kirjanpito > Kyselyt ja raportit > Pääkirja**), tarkista tilinpäätöksen erätyön tuloksista, onnistuiko Muodosta saldot uudelleen -vaiheen suorittaminen.</span><span class="sxs-lookup"><span data-stu-id="ecd12-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="ecd12-124">[![Tilinpäätöksen erätyön tulokset](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="ecd12-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="ecd12-125">Jos tämä vaihe on epäonnistunut jonkin syyn vuoksi, alkutapahtumien (tai vaihtoehtoisesti päättämistapahtumien) kirjaaminen todennäköisesti onnistui.</span><span class="sxs-lookup"><span data-stu-id="ecd12-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="ecd12-126">Tarkista, että kirjanpidon tapahtumien kirjaaminen onnistui, käyttämällä **Tositetapahtumien kysely** -sivua. Sivulla määritetään tositteen numero ja kyseisen vuoden tilinpäätösvalintaikkunassa oleva päivämäärä (**Kirjanpito > Kyselyt ja raportit > Tositetapahtumat**).</span><span class="sxs-lookup"><span data-stu-id="ecd12-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="ecd12-127">[![Tositetapahtumien kysely](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="ecd12-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="ecd12-128">Jos avaustapahtumien (tai vaihtoehtoisesti päätöstapahtumien) tositteet ovat näkyvissä, tilinpäätöstä ei tarvitse suorittaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ecd12-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="ecd12-129">Katso sen sijaan seuraavan osan ohjeita seuraavien toimintojen suorittamiseksi.</span><span class="sxs-lookup"><span data-stu-id="ecd12-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="ecd12-130">Oire</span><span class="sxs-lookup"><span data-stu-id="ecd12-130">Symptom</span></span>

<span data-ttu-id="ecd12-131">Tilinpäätöksen Muodosta saldot uudelleen -vaihe epäonnistui. Tuleeko minun suorittaa koko tilinpäätösprosessi uudelleen?</span><span class="sxs-lookup"><span data-stu-id="ecd12-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="ecd12-132">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="ecd12-132">Resolution</span></span>

<span data-ttu-id="ecd12-133">Muodosta saldot uudelleen -vaihe päivittää kirjanpidon saldot, joita käytetään pääkirjan kyselyn luomisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ecd12-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="ecd12-134">Se on tilinpäätösprosessin viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="ecd12-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="ecd12-135">Jos tämä on ainoa epäonnistunut vaihe, kirjanpitotapahtumat on kirjattu onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="ecd12-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="ecd12-136">Tilinpäätöstä ei tarvitse suorittaa uudelleen.</span><span class="sxs-lookup"><span data-stu-id="ecd12-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="ecd12-137">Voit suorittaa saldojen uudelleenmuodostusprosessin manuaalisesti **Taloushallinnon dimensioyhdistelmät** -sivulla (**Kirjanpito > Tilikartta > Dimensiot > Taloushallinnon dimensioyhdistelmät**).</span><span class="sxs-lookup"><span data-stu-id="ecd12-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="ecd12-138">[![Muodosta saldot uudelleen -painike Taloushallinnon dimensioyhdistelmät -sivulla](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="ecd12-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="ecd12-139">Jos tämän vaiheen käsittely kestää kauan, suosittelemme taloushallinnon dimensioyhdistelmien parhaiden käytäntöjen tarkastelemista kohdassa [Taloushallinnon dimensioyhdistelmien päivittämisen parhaat käytännöt](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="ecd12-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

