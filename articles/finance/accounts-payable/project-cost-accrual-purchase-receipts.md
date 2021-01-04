---
title: Projektikustannusten jaksottaminen ostojen vastaanotoissa
description: Tässä aiheessa kerrotaan, miten ostojen vastaanottojen jaksotettuja projektikustannuksia voidaan seurata Microsoft Dynamics 365 Financessa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0a930b4921a29d5ce561ce0e958733f0c3261b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442725"
---
# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="90b52-103">Projektikustannusten jaksottaminen ostojen vastaanotoissa</span><span class="sxs-lookup"><span data-stu-id="90b52-103">Project cost accrual on purchase receipts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90b52-104">Tässä aiheessa kerrotaan, miten ostojen vastaanottojen jaksotettuja projektikustannuksia voidaan seurata Microsoft Dynamics 365 Financessa.</span><span class="sxs-lookup"><span data-stu-id="90b52-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 Finance.</span></span> 

<span data-ttu-id="90b52-105">Projektin laskut saapuvat usein tavaroiden ja palveluiden toimituksen jälkeen. Tällä saattaa olla merkittävä vaikutus projektin suorituskykyilmaisimiin.</span><span class="sxs-lookup"><span data-stu-id="90b52-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="90b52-106">On tärkeää, että näitä tapahtumia pystytään seuraamaan sekä tilinpäätöksissä että projektiraporteissa.</span><span class="sxs-lookup"><span data-stu-id="90b52-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="90b52-107">Seuraava esimerkki havainnollistaa tätä.</span><span class="sxs-lookup"><span data-stu-id="90b52-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="90b52-108">Contoso Consulting on aloittanut uuden pilvikehitysprojektin.</span><span class="sxs-lookup"><span data-stu-id="90b52-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="90b52-109">Luodaan ostotilaus tietokoneen ostamiseksi projektia varten.</span><span class="sxs-lookup"><span data-stu-id="90b52-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="90b52-110">Tietokone maksaa 1 500 euroa ja asennuspalvelut 150 euroa.</span><span class="sxs-lookup"><span data-stu-id="90b52-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="90b52-111">Toimittaja on toimittanut ja asentanut tietokoneen, mutta Contoso Consulting ei ole vielä saanut laskua.</span><span class="sxs-lookup"><span data-stu-id="90b52-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="90b52-112">Projektipäällikkö haluaa tarkastella projektikustannusten 1 650 euron jaksottamista ennen laskun toimitusta.</span><span class="sxs-lookup"><span data-stu-id="90b52-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="90b52-113">Kustannusten tulee vastata yrityksen kuukauden lopun tilinpäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="90b52-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="90b52-114">Jaksotettu kustannus on tallennettava raportoinnissa sekä taloushallinnon tasolla että projektitasolla.</span><span class="sxs-lookup"><span data-stu-id="90b52-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="90b52-115">Tuotteen vastaanoton nimike- ja hankintaluokkien maksupäivitystä voidaan seurata.</span><span class="sxs-lookup"><span data-stu-id="90b52-115">The financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="90b52-116">Valitse nimikkeille **Ostoreskontran parametrit** -sivulla **Kirjaa tuotteen vastaanotot kirjanpitoon** -vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="90b52-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="90b52-117">[![Ostoreskontran parametrit -sivu](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-117">[![Accounts payable parameters page](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="90b52-118">Valitse hankintaluokille **Luokan käytäntösääntö** -sivulla **ostokäytännöt** ja valitse sitten jokaiselle hankintaluokalle **Jaksota ostokulut vastaanoton yhteydessä** -kohta.</span><span class="sxs-lookup"><span data-stu-id="90b52-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="90b52-119">[![Luokan käytäntösääntö -sivu](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-119">[![Category policy rule page](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="90b52-120">**Kirjausasetukset**-kohdassa olevia **Ostomeno, laskuttamaton**- ja **Osto, jaksotus** -tilejä käytetään, kun tuotteen vastaanottoon liittyvät tositteen kirjataan.</span><span class="sxs-lookup"><span data-stu-id="90b52-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>

<span data-ttu-id="90b52-121">Käytetään samaa skenaariota ja tarkastellaan, miten tuotteen vastaanotto vaikuttaa kirjanpitoon ja projektin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="90b52-121">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="90b52-122">**Vaihe 1:** Luodaan ja vahvistetaan projektille uusi ostotilaus 1 500 euroa maksaneen tietokoneen ja 150 euroa maksaneiden asennuspalveluiden oston tallentamista varten.</span><span class="sxs-lookup"><span data-stu-id="90b52-122">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="90b52-123">[![Uuden ostotilauksen luominen](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-123">[![Create new purchase order](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="90b52-124">Kun ostotilaus vahvistetaan, projektille luodaan sidotun kustannuksen tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="90b52-124">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="90b52-125">[![Luodut tapahtumat](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-125">[![Transactions created](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="90b52-126">Sidotun kustannuksen tapahtumien **Tapahtuman alkuperä** -kentän arvoksi on määritetty **Ostotilaus**.</span><span class="sxs-lookup"><span data-stu-id="90b52-126">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="90b52-127">Projektille ei luoda tapahtumia ostotilauksen luomisen ja vahvistamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="90b52-127">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="90b52-128">**Vaihe 2:** Tavarat ja palvelut toimitetaan ja tuotteen vastaanotto rekisteröidään.</span><span class="sxs-lookup"><span data-stu-id="90b52-128">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="90b52-129">Tuotteen vastaanoton kirjaamisen yhteydessä luodaan tosite ja kirjataan se kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="90b52-129">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="90b52-130">Tosite veloittaa ostomenoa, laskuttamatonta tiliä, ja hyvittää jaksotusmenetelmän tiliä.</span><span class="sxs-lookup"><span data-stu-id="90b52-130">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="90b52-131">[![Tositetapahtumat](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-131">[![Voucher transactions](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="90b52-132">Tuotteen vastaanoton kirjaamisessa käytetään hankintaluokkien ja tuotteiden kirjausasetuksia projektiluokkien kirjausasetusten sijaan.</span><span class="sxs-lookup"><span data-stu-id="90b52-132">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="90b52-133">Nämä asetukset on kohdistettava, jotta taloudellinen vaikutus ostojen jaksotukseen on oikea.</span><span class="sxs-lookup"><span data-stu-id="90b52-133">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="90b52-134">Hankintaluokat on mahdollista yhdistää projektiluokkiin **Hankintaluokka**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="90b52-134">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="90b52-135">[![Hankintaluokan nimi -sivu](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-135">[![Procurement category page](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="90b52-136">**Vaihe 3:** Luo toimittajan laskuluonnos.</span><span class="sxs-lookup"><span data-stu-id="90b52-136">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="90b52-137">Tuotteen kirjaaminen ei vaikuta projektin tietoihin.</span><span class="sxs-lookup"><span data-stu-id="90b52-137">Posting a product receipt does not impact project information.</span></span> <span data-ttu-id="90b52-138">Voit välttää ongelman luomalla toimittajan luonnoslaskun myös heti oston vastaanoton kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="90b52-138">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="90b52-139">Siirry kohtaan **Ostolasku**-sivu &gt; **Lasku-välilehti** &gt; **Luo** &gt; **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="90b52-139">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="90b52-140">Tämä luo odottavan laskuasiakirjan, joka päivittää projektin tiedot.</span><span class="sxs-lookup"><span data-stu-id="90b52-140">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="90b52-141">Toimittajan laskuluonnoksen luominen luo odottavia projektitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="90b52-141">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="90b52-142">[![Odottavat projektitapahtumat](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-142">[![Pending project transactions](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="90b52-143">**Sidottu kustannus** -sivulla vaiheessa 1 luodut tietueet suljetaan. Tämän jälkeen luodaan uudet tietueet, jotka vastaavat odottavista toimittajan laskuista saatavia kustannussitoumuksia.</span><span class="sxs-lookup"><span data-stu-id="90b52-143">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="90b52-144">Sidotun kustannuksen **Tapahtuman alkuperä** -kentän arvoksi määritetään **Toimittajan lasku**.</span><span class="sxs-lookup"><span data-stu-id="90b52-144">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="90b52-145">[![Sidotut kustannukset -sivu](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="90b52-145">[![Commited costs page](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="90b52-146">Toimittajan laskun tila on Odottaa niin kauan, kunnes todellinen toimittajan lasku saapuu.</span><span class="sxs-lookup"><span data-stu-id="90b52-146">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>



