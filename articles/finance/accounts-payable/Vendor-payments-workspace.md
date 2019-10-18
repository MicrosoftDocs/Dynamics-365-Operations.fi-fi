---
title: Toimittajan maksujen työtila
description: Tässä ohjeaiheessa on tietoja toimittajamaksujen työtilasta. Toimittajamaksujen työtilassa näkyy toimittajan maksujen käsittelyyn liittyviä tietoja.
author: abruer
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymentWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89ba0d68bd52413328dd583e87b09b01fd523d6f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177613"
---
# <a name="vendor-payments-workspace"></a><span data-ttu-id="57e00-104">Toimittajan maksujen työtila</span><span class="sxs-lookup"><span data-stu-id="57e00-104">Vendor payments workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57e00-105">**Toimittajamaksut** -työtilassa näkyy toimittajan maksujen käsittelyyn liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="57e00-105">The **Vendor payments** workspace shows information that is related to the processing of vendor payments.</span></span> <span data-ttu-id="57e00-106">Työtilassa on **Oma työ** -näkymä ja **Analytiikka**-sivu.</span><span class="sxs-lookup"><span data-stu-id="57e00-106">This workspace includes a **My work** view and an **Analytics** page.</span></span> <span data-ttu-id="57e00-107">**Oma työ** -näkymä näyttää yhteenvetoruudut, toimittajatapahtumaruudukot ja liittyvän toimittajan tiedot.</span><span class="sxs-lookup"><span data-stu-id="57e00-107">The **My work** view shows summary tiles, vendor transaction grids, and related vendor information.</span></span> <span data-ttu-id="57e00-108">**Analytiikka**-sivu käyttää Microsoft Power BI:n ominaisuuksien avulla toimittajan maksuihin liittyviä visuaalisia tietoja.</span><span class="sxs-lookup"><span data-stu-id="57e00-108">The **Analytics** page uses the capabilities of Microsoft Power BI to show visuals that are related to vendor payments.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="57e00-109">Power BI -sisällön tarkastelemiseen tarvittavat asetukset</span><span class="sxs-lookup"><span data-stu-id="57e00-109">Setup needed to view Power BI content</span></span>

<span data-ttu-id="57e00-110">Seuraavat asetukset on tehtävä, jotta tiedot näkyisivät Power BI -visualisoinnissa **Toimittajan maksut**.</span><span class="sxs-lookup"><span data-stu-id="57e00-110">The following setup needs to be completed for data to display in **Vendor payments** Power BI visuals.</span></span>
1. <span data-ttu-id="57e00-111">Voit määrittää **järjestelmän valuutan** ja **järjestelmän vaihtokurssin** valitsemalla **Järjestelmän hallinta > Asetukset > Järjestelmän parametrit**.</span><span class="sxs-lookup"><span data-stu-id="57e00-111">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="57e00-112">Määritä **Kirjanpitovaluutta** ja **Vaihtokurssin tyyppi** valitsemalla **Kirjanpito > Asetukset > Kirjanpito**.</span><span class="sxs-lookup"><span data-stu-id="57e00-112">Go to **General Ledger > Setup > Ledger**  to set **Accounting Currency** and **Exchange Rate Type**.</span></span> 
2. <span data-ttu-id="57e00-113">Määritä tapahtuma- ja kirjanpitovaluuttojen sekä kirjanpito- ja järjestelmävaluutan välillä.</span><span class="sxs-lookup"><span data-stu-id="57e00-113">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency.</span></span> <span data-ttu-id="57e00-114">Tee se valitsemalla **Kirjanpito > Valuutat > Valuutan vaihtokurssit**.</span><span class="sxs-lookup"><span data-stu-id="57e00-114">To do this, go to **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="57e00-115">Päivitä **VendPaymentBIMeasure**-koostemitta valitsemalla **Järjestelmän hallinta > Asetukset > Yksikkösäilö**.</span><span class="sxs-lookup"><span data-stu-id="57e00-115">Go to **System administration > Setup > Entity Store** to refresh the **VendPaymentBIMeasure** aggregate measurement.</span></span> 

## <a name="my-work-view"></a><span data-ttu-id="57e00-116">Oma työ -näkymä</span><span class="sxs-lookup"><span data-stu-id="57e00-116">My work view</span></span>

### <a name="summary-tiles"></a><span data-ttu-id="57e00-117">Yhteenvetoruudut</span><span class="sxs-lookup"><span data-stu-id="57e00-117">Summary tiles</span></span>

<span data-ttu-id="57e00-118">**Yhteenveto**-osan ruudut antavat yleiskuvan maksutietojesi tilasta.</span><span class="sxs-lookup"><span data-stu-id="57e00-118">The tiles in the **Summary** section give an overview of the state of your payment information.</span></span> <span data-ttu-id="57e00-119">Voit tarkastella maksukirjauskansioista, joita ei ole vielä kirjattu, laskuja, joiden eräpäivä on ohitettu, ja kaikki toimittajat, jotka ovat pidossa.</span><span class="sxs-lookup"><span data-stu-id="57e00-119">You can see payment journals that aren't yet posted, invoices that are past due, all vendors, and vendors that are on hold.</span></span> <span data-ttu-id="57e00-120">**Yhteenveto**-osassa voit luoda uuden maksuajon.</span><span class="sxs-lookup"><span data-stu-id="57e00-120">From the **Summary** section, you can create a new pay run.</span></span>

<span data-ttu-id="57e00-121">**Yhteenveto**-osan tiedot on tarkoitettu yritykselle, johon olet kirjautunut.</span><span class="sxs-lookup"><span data-stu-id="57e00-121">The information in the **Summary** section is for the company that you're signed in to.</span></span>

### <a name="vendor-transactions-grids"></a><span data-ttu-id="57e00-122">Toimittajatapahtumaruudukot</span><span class="sxs-lookup"><span data-stu-id="57e00-122">Vendor transactions grids</span></span>

<span data-ttu-id="57e00-123">**Toimittajatapahtumat**-osa sisältää ruudukot, joissa näkyvät laskut, jotka ovat erääntyneet, ja maksut, joita ei ole maksettu.</span><span class="sxs-lookup"><span data-stu-id="57e00-123">The **Vendor transactions** section contains grids that show the invoices that are past due and payments that aren't settled.</span></span> <span data-ttu-id="57e00-124">**Erääntyneet laskut** -ruudukossa voit tarkastella valitun laskun maksuhistoriaa.</span><span class="sxs-lookup"><span data-stu-id="57e00-124">From the **Invoices past due** grid, you can view the settlement history for a selected invoice.</span></span> <span data-ttu-id="57e00-125">**Maksamattomat laskut** -ruudukossa voit tarkastella valitun laskun maksuhistoriaa ja maksaa laskun.</span><span class="sxs-lookup"><span data-stu-id="57e00-125">From the **Payments not settled** grid, you can view the settlement history for a selected invoice and settle an invoice.</span></span>

<span data-ttu-id="57e00-126">Keskitettyjen maksujen kirjanpitäjät voivat käyttää suodatinta, joka näkyy kunkin ruudukon yläosassa, yrityksen valintaa.</span><span class="sxs-lookup"><span data-stu-id="57e00-126">Centralized payment clerks can use a filter that appears at the top of each grid to select a company.</span></span> <span data-ttu-id="57e00-127">Ruudukko suodatetaan siten, että siinä näkyy vain yrityksiä, jotka on määritetty keskitettyjen maksujen organisaatiohierarkiassa, jota keskitettyjen maksujen kirjanpitäjällä on oikeus tarkastella.</span><span class="sxs-lookup"><span data-stu-id="57e00-127">The grid is then filtered so that it shows only those companies that are defined in the centralized payment organizational hierarchy that the centralized payment clerk has rights to view.</span></span>

<span data-ttu-id="57e00-128">**Toimittajatapahtumat**-osan **Etsi tapahtumia** -välilehden avulla voit etsiä toimittajatapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="57e00-128">The **Find transactions** tab in the **Vendor transactions** section lets you search for a vendor transaction.</span></span>

### <a name="related-information"></a><span data-ttu-id="57e00-129">Aiheeseen liittyviä tietoja</span><span class="sxs-lookup"><span data-stu-id="57e00-129">Related information</span></span>

<span data-ttu-id="57e00-130">Voit tarkastella **Ostoreskontran erääntyminen** -raporttia ja **Maksuyhteenveto päivän mukaan** -raporttia työtilan **Liittyviä tietoja** linkkien avulla.</span><span class="sxs-lookup"><span data-stu-id="57e00-130">You can view the **Vendor aging** report and the **Payment summary by date** report by using the links in the **Related information** section of the workspace.</span></span>

## <a name="analytics-page"></a><span data-ttu-id="57e00-131">Analytiikka-sivu</span><span class="sxs-lookup"><span data-stu-id="57e00-131">Analytics page</span></span>

<span data-ttu-id="57e00-132">**Analytiikka**-sivulla on tärkeitä mittareita, kuten erääntyneet toimittajalaskut ja toimittajalaskuja, jotka erääntyvät myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="57e00-132">The **Analytics** page provides important metrics, such as vendor invoices that are past due and vendor invoices that are due in the future.</span></span> <span data-ttu-id="57e00-133">Tällä sivulla on yhdeksän raporttisivua.</span><span class="sxs-lookup"><span data-stu-id="57e00-133">This page contains nine report pages.</span></span> <span data-ttu-id="57e00-134">Yksi sivu sisältää yhteenvedon ja kahdeksalla muulla sivulla on tietoja ostoreskontran maksumittareista.</span><span class="sxs-lookup"><span data-stu-id="57e00-134">One page provides an overview, and the other eight pages provide details about Accounts payable payment metrics.</span></span>

<span data-ttu-id="57e00-135">Seuraavassa taulukossa on näkyvissä kullakin raporttisivulla käytettävissä olevat visualisoinnit.</span><span class="sxs-lookup"><span data-stu-id="57e00-135">The following table shows the visualizations that are available on each report page.</span></span>


|            <span data-ttu-id="57e00-136">Raporttisivu</span><span class="sxs-lookup"><span data-stu-id="57e00-136">Report page</span></span>            |                                                                                                                                                                                <span data-ttu-id="57e00-137">Visualisointi</span><span class="sxs-lookup"><span data-stu-id="57e00-137">Visualization</span></span>                                                                                                                                                                                |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     <span data-ttu-id="57e00-138">Toimittajan maksujen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="57e00-138">Vendor payments overview</span></span>      | <ul><li><span data-ttu-id="57e00-139">Erääntyneet laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-139">Invoices past due</span></span></li><li><span data-ttu-id="57e00-140">Tänään erääntyvät laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-140">Invoices due today</span></span></li><li><span data-ttu-id="57e00-141">Saadut alennukset / annetut alennukset</span><span class="sxs-lookup"><span data-stu-id="57e00-141">Discounts taken to discounts lost</span></span></li><li><span data-ttu-id="57e00-142">Tulevaisuudessa erääntyvät laskut käteisalennuspäivämäärän mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-142">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="57e00-143">Tulevaisuudessa erääntyvät laskut eräpäivämäärän mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-143">Invoices due in future by due date</span></span></li><li><span data-ttu-id="57e00-144">Myöhässä maksetut laskut / ajoissa maksetut laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-144">Invoices paid late to invoices paid on time</span></span></li><li><span data-ttu-id="57e00-145">Maksun työnkulun määritys</span><span class="sxs-lookup"><span data-stu-id="57e00-145">Payment workflow assignment</span></span></li><li><span data-ttu-id="57e00-146">Toimittaja-/asiakassaldo</span><span class="sxs-lookup"><span data-stu-id="57e00-146">Vendor to customer balance</span></span></li><li><span data-ttu-id="57e00-147">Avoimet laskut, joiden maksu on pidossa</span><span class="sxs-lookup"><span data-stu-id="57e00-147">Open invoices with payment hold</span></span></li></ul> |
|         <span data-ttu-id="57e00-148">Erääntyneet laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-148">Invoices past due</span></span>         |                                                                                             <ul><li><span data-ttu-id="57e00-149">Erääntyneet laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-149">Invoices past due</span></span></li><li><span data-ttu-id="57e00-150">Erääntyneiden laskujen tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-150">Invoices past due details</span></span></li><li><span data-ttu-id="57e00-151">Avoimien laskujen yhteissumma</span><span class="sxs-lookup"><span data-stu-id="57e00-151">Total open invoices</span></span></li><li><span data-ttu-id="57e00-152">Erääntyneet laskut toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-152">Invoices past due per vendor group</span></span></li><li><span data-ttu-id="57e00-153">Erääntyneet laskut yrityksen mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-153">Invoices past due per company</span></span></li></ul>                                                                                              |
|        <span data-ttu-id="57e00-154">Tänään erääntyvät laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-154">Invoices due today</span></span>         |                                                                                                         <ul><li><span data-ttu-id="57e00-155">Tänään erääntyvät laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-155">Invoices due today</span></span></li><li><span data-ttu-id="57e00-156">Tänään erääntyvien laskujen tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-156">Invoices due today details</span></span></li><li><span data-ttu-id="57e00-157">Tänään erääntyvät laskut yrityksen mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-157">Invoices due today per company</span></span></li><li><span data-ttu-id="57e00-158">Tänään erääntyvät laskut toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-158">Invoices due today per vendor group</span></span></li></ul>                                                                                                          |
| <span data-ttu-id="57e00-159">Saadut alennukset / annetut alennukset</span><span class="sxs-lookup"><span data-stu-id="57e00-159">Discounts taken to discounts lost</span></span> |                                                                             <ul><li><span data-ttu-id="57e00-160">Saadut alennukset / annettu alennus</span><span class="sxs-lookup"><span data-stu-id="57e00-160">Discounts taken to discount lost</span></span></li><li><span data-ttu-id="57e00-161">Saadut alennukset / annettu alennus -tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-161">Discounts taken to discount lost details</span></span></li><li><span data-ttu-id="57e00-162">Saadut alennukset / annettu alennus yrityksittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-162">Discounts taken to discount lost per company</span></span></li><li><span data-ttu-id="57e00-163">Saadut alennukset / annettu alennus toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-163">Discounts taken to discount lost per vendor group</span></span></li></ul>                                                                              |
|      <span data-ttu-id="57e00-164">Tulevaisuudessa erääntyvät laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-164">Invoices due in future</span></span>       |                                                 <ul><li><span data-ttu-id="57e00-165">Tulevaisuudessa erääntyvät laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-165">Invoices due in future</span></span></li><li><span data-ttu-id="57e00-166">Tulevaisuudessa erääntyvien laskujen tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-166">Invoices due in future details</span></span></li><li><span data-ttu-id="57e00-167">Tulevaisuudessa erääntyvät laskut yrityksittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-167">Invoices due in future per company</span></span></li><li><span data-ttu-id="57e00-168">Tulevaisuudessa erääntyvät laskut toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-168">Invoices due in future per vendor group</span></span></li><li><span data-ttu-id="57e00-169">Tulevaisuudessa erääntyvät laskut käteisalennuspäivämäärän mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-169">Invoices due in future by cash discount date</span></span></li><li><span data-ttu-id="57e00-170">Tulevaisuudessa erääntyvät laskut eräpäivämäärän mukaan</span><span class="sxs-lookup"><span data-stu-id="57e00-170">Invoices due in future by due date</span></span></li></ul>                                                  |
|        <span data-ttu-id="57e00-171">Myöhässä maksetut laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-171">Invoices paid late</span></span>         |                                                         <ul><li><span data-ttu-id="57e00-172">Eräpäivän jälkeen maksetut laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-172">Invoices paid after due date</span></span></li><li><span data-ttu-id="57e00-173">Eräpäivän jälkeen maksettujen laskujen tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-173">Invoices paid after due date details</span></span></li><li><span data-ttu-id="57e00-174">Eräpäivän jälkeen maksettujen laskujen tiedot yrityksittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-174">Invoices paid after due date per company</span></span></li><li><span data-ttu-id="57e00-175">Eräpäivän jälkeen maksettujen laskujen toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-175">Invoices paid after due date per vendor group</span></span></li><li><span data-ttu-id="57e00-176">Myöhässä maksetut laskut vs. ajoissa maksetut laskut</span><span class="sxs-lookup"><span data-stu-id="57e00-176">Invoices paid late versus invoices paid on time</span></span></li></ul>                                                          |
|         <span data-ttu-id="57e00-177">Maksun työnkulku</span><span class="sxs-lookup"><span data-stu-id="57e00-177">Payment workflow</span></span>          |                                                                                <ul><li><span data-ttu-id="57e00-178">Toimittajamaksujen työnkulkuesiintymät</span><span class="sxs-lookup"><span data-stu-id="57e00-178">Vendor payment workflow instances</span></span></li><li><span data-ttu-id="57e00-179">Toimittajamaksujen työnkulkuesiintymät / hyväksyjä</span><span class="sxs-lookup"><span data-stu-id="57e00-179">Vendor payment workflow instances per approver</span></span></li><li><span data-ttu-id="57e00-180">Toimittajamaksujen työnkulkuesiintymät / yritys</span><span class="sxs-lookup"><span data-stu-id="57e00-180">Vendor payment workflow instances per company</span></span></li><li><span data-ttu-id="57e00-181">Työnkulun keskimääräinen pituus (päiviä) / hyväksyjä</span><span class="sxs-lookup"><span data-stu-id="57e00-181">Average days in workflow by approver</span></span></li></ul>                                                                                |
|    <span data-ttu-id="57e00-182">Toimittaja-/asiakassaldo</span><span class="sxs-lookup"><span data-stu-id="57e00-182">Vendor to customer balance</span></span>     |                                                                                                                   <ul><li><span data-ttu-id="57e00-183">Toimittaja-/asiakassaldo</span><span class="sxs-lookup"><span data-stu-id="57e00-183">Vendor to customer balance</span></span></li><li><span data-ttu-id="57e00-184">Toimittaja-/asiakassaldo yrityksittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-184">Vendor to customer balance per company</span></span></li><li><span data-ttu-id="57e00-185">Toimittaja-/asiakassaldon tiedot</span><span class="sxs-lookup"><span data-stu-id="57e00-185">Vendor to customer balance details</span></span></li></ul>                                                                                                                    |
|    <span data-ttu-id="57e00-186">Laskun pidossa oleva maksu</span><span class="sxs-lookup"><span data-stu-id="57e00-186">Invoices with payment hold</span></span>     |                                                                                         <ul><li><span data-ttu-id="57e00-187">Laskun pidossa oleva maksu</span><span class="sxs-lookup"><span data-stu-id="57e00-187">Invoices with payment hold</span></span></li><li><span data-ttu-id="57e00-188">Laskun pidossa oleva maksu -yksityiskohdat</span><span class="sxs-lookup"><span data-stu-id="57e00-188">Invoices with payment hold details</span></span></li><li><span data-ttu-id="57e00-189">Laskun pidossa oleva maksu yrityksittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-189">Invoices with payment hold per company</span></span></li><li><span data-ttu-id="57e00-190">Laskun pidossa oleva maksu toimittajaryhmittäin</span><span class="sxs-lookup"><span data-stu-id="57e00-190">Invoices with payment hold per vendor group</span></span></li></ul>                                                                                          |
