---
title: ALV-raportointi Euroopassa
description: "Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c5cd61c45eb7cbc6f040f054a99d9a54e1ee854
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="07be7-103">ALV-raportointi Euroopassa</span><span class="sxs-lookup"><span data-stu-id="07be7-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07be7-104">Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.</span><span class="sxs-lookup"><span data-stu-id="07be7-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="07be7-105">Tämä ohjeaihe sisältää yleisen lähestymistavan ALV-ilmoituksen määrittämiseen ja luomiseen.</span><span class="sxs-lookup"><span data-stu-id="07be7-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="07be7-106">Tämä lähestymistapa on yhteinen yrityksille seuraavissa maissa/alueilla:</span><span class="sxs-lookup"><span data-stu-id="07be7-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="07be7-107">Itävalta</span><span class="sxs-lookup"><span data-stu-id="07be7-107">Austria</span></span>
-   <span data-ttu-id="07be7-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="07be7-108">Belgium</span></span>
-   <span data-ttu-id="07be7-109">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="07be7-109">Czech Republic</span></span>
-   <span data-ttu-id="07be7-110">Viro</span><span class="sxs-lookup"><span data-stu-id="07be7-110">Estonia</span></span>
-   <span data-ttu-id="07be7-111">Suomi</span><span class="sxs-lookup"><span data-stu-id="07be7-111">Finland</span></span>
-   <span data-ttu-id="07be7-112">Saksa</span><span class="sxs-lookup"><span data-stu-id="07be7-112">Germany</span></span>
-   <span data-ttu-id="07be7-113">Latvia</span><span class="sxs-lookup"><span data-stu-id="07be7-113">Latvia</span></span>
-   <span data-ttu-id="07be7-114">Liettua</span><span class="sxs-lookup"><span data-stu-id="07be7-114">Lithuania</span></span>
-   <span data-ttu-id="07be7-115">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="07be7-115">Netherlands</span></span>
-   <span data-ttu-id="07be7-116">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="07be7-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="07be7-117">ALV-ilmoituksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="07be7-117">VAT statement overview</span></span>
<span data-ttu-id="07be7-118">ALV-ilmoitus perustuu verotapahtumien summiin.</span><span class="sxs-lookup"><span data-stu-id="07be7-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="07be7-119">ALV-ilmoituksen luomisprosessi kuuluu arvonlisäveron maksamisen prosessiin, joka toteutetaan Tilitä ja kirjaa arvonlisävero -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="07be7-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="07be7-120">Tämä toiminto laskee arvonlisäveron, joka erääntyy tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="07be7-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="07be7-121">Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta verotapahtumille.</span><span class="sxs-lookup"><span data-stu-id="07be7-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="07be7-122">ALV-ilmoituksen tietojen laskentaprosessi perustuu arvonlisäverokoodien ja arvonlisäveroilmoituksen koodien suhteeseen, jossa ALV-raporttikoodit vastaavat ALV-ilmoitusten ruutuja (tai XML-tunnisteita).</span><span class="sxs-lookup"><span data-stu-id="07be7-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="07be7-123">Kullekin arvonlisäverokoodille arvonlisäveron raportointikoodit pitäisi määrittää kunkin tyyppiselle tapahtumalle, kuten verolliselle myynnille, verollisille ostoille tai verolliselle tuonnille.</span><span class="sxs-lookup"><span data-stu-id="07be7-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="07be7-124">Näiden tapahtumien tyyppi on kuvattu Arvonlisäverokoodit ALV-raportoinnissa -osassa jäljempänä tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="07be7-125">Jokaiselle arvonlisäveroilmoituksen koodille olisi määritettävä tietty raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="07be7-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="07be7-126">Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn arvonlisäveroviranomaiseen arvonlisäveron tilityskausien kautta.</span><span class="sxs-lookup"><span data-stu-id="07be7-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="07be7-127">Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="07be7-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="07be7-128">Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, joka on määritetty ALV-viranomaiselle arvonlisäverokoodin arvonlisäveron tilityskausissa, voidaan valita arvonlisäverokoodin raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="07be7-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="07be7-129">Arvonlisäverotapahtuma, joka luodaan kirjatessa tilauksen tai päiväkirjan, sisältää arvonlisäverokoodin, arvonlisäveron lähteen, arvonlisäveron suunnan ja tapahtumasummat (veron peruste ja verosumma kirjanpitovaluuttana, ALV-valuutta ja tapahtumavaluutta).</span><span class="sxs-lookup"><span data-stu-id="07be7-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="07be7-130">Perustuen verotapahtuman määritteiden yhdistelmään, tapahtumasummat koostavat kokonaissummat arvonlisäverokoodeille määritetyille arvonlisäveroilmoituksen koodeille.</span><span class="sxs-lookup"><span data-stu-id="07be7-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="07be7-131">Seuraavassa on kuvattu tietojen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="07be7-131">The following illustration shows the data relationship.</span></span>

![Kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="07be7-133">ALV-ilmoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="07be7-133">VAT statement setup</span></span>
<span data-ttu-id="07be7-134">Voit luoda ALV-ilmoituksen määrittämällä seuraavat.</span><span class="sxs-lookup"><span data-stu-id="07be7-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="07be7-135">Veroviranomaiset ALV-raportointia varten</span><span class="sxs-lookup"><span data-stu-id="07be7-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="07be7-136">Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea raporttiasettelu arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="07be7-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="07be7-137">Valitse **Arvonlisäveroviranomaiset**-sivulla **Yleiset**-osassa **Raportin asettelu**.</span><span class="sxs-lookup"><span data-stu-id="07be7-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="07be7-138">Tätä asettelua käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.</span><span class="sxs-lookup"><span data-stu-id="07be7-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="07be7-139">Arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="07be7-139">Sales tax reporting codes</span></span>

<span data-ttu-id="07be7-140">ALV-ilmoituskoodit ovat ruutukoodeja ALV-ilmoituksessa tai tunnisteen nimiä XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="07be7-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="07be7-141">Näitä koodeja käytetään keräämään ja valmistelemaan raportin summat.</span><span class="sxs-lookup"><span data-stu-id="07be7-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="07be7-142">ALV-ilmoituksen sähköisen raportoinnin muotoa määrittäessäsi käytetään tulossummien nimiä.</span><span class="sxs-lookup"><span data-stu-id="07be7-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="07be7-143">Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodeja **Arvonlisäveroilmoituksen koodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="07be7-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="07be7-144">Jokaiselle koodille tulee määrittää raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="07be7-144">You must assign each code a report layout.</span></span> <span data-ttu-id="07be7-145">Kun olet luonut arvonlisäveroraportin koodit, voit valita koodeja **Arvonlisäverokoodit**-sivun **Raportin asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="07be7-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="07be7-146">ALV-ilmoituksen arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="07be7-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="07be7-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Arvonlisäverotapahtumien perussummat ja verosummat voidaan koostaa ALV-ilmoituksen raportointikoodeista (XML-tunnisteista tai ilmoitusruuduista).</span><span class="sxs-lookup"><span data-stu-id="07be7-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="07be7-148">Voit määrittää tämän liittämällä arvonlisäveroilmoituksen koodit arvonlisäverokoodien eri tapahtumalajeille <strong>Arvonlisäverokoodit</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="07be7-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="07be7-149">Seuraavassa taulukossa kuvataan tapahtumatyypit arvonlisäverokoodien raporttiasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="07be7-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="07be7-150">Laskenta sisältää tapahtumia kaiken tyyppisille lähteille lukuun ottamatta arvonlisäveroa.</span><span class="sxs-lookup"><span data-stu-id="07be7-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07be7-151"><strong>Tapahtumalaji</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="07be7-152"><strong>Tapahtumien kuvaus ja tapahtumatyypille laskettavat summat</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-153"><strong>Verollinen myynti</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="07be7-154">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-155">Tapahtumapäivä on valitussa kaudessa/</span><span class="sxs-lookup"><span data-stu-id="07be7-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="07be7-156">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-157">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-158"><strong>Verovapaa myynti</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="07be7-159">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-160">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-161">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="07be7-162">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-163"><strong>Maksettava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="07be7-164">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-165">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-166">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-167">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-168"><strong>Verollinen hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-169">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-170">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-171">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-172">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-173"><strong>Verovapaa hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-174">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-175">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-176">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="07be7-177">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-178"><strong>Myyntihyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-179">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-180">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-181">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-182">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-183"><strong>Verollinen osto</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="07be7-184">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-185">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-186">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-187">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-188"><strong>Verovapaa osto</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="07be7-189">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-190">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-191">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="07be7-192">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-193"><strong>Saatava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="07be7-194">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-195">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-196">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-197">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-198"><strong>Verollinen ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-199">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-200">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-201">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-202">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-203"><strong>Verovapaa ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-204">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-205">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-206">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="07be7-207">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-208"><strong>Ostohyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-209">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-210">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-211">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="07be7-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="07be7-212">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-213"><strong>Verollinen tuonti</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="07be7-214">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-215">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-216"><strong>Veron suunta</strong> on <strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="07be7-217">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-218"><strong>Verollinen tuonti vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="07be7-219">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-220">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-221"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="07be7-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="07be7-222">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-223"><strong>Verollinen tuontihyvitysmaksu</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-224">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-225">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="07be7-226">e</span><span class="sxs-lookup"><span data-stu-id="07be7-226">e</span></span><li><span data-ttu-id="07be7-227"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="07be7-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="07be7-228">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-229"><strong>Verollinen tuontihyvityslasku vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="07be7-230">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-231">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-232">Veron suunta on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="07be7-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="07be7-233">d</span><span class="sxs-lookup"><span data-stu-id="07be7-233">d</span></span><li><span data-ttu-id="07be7-234">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07be7-235"><strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="07be7-236">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-237">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-238"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="07be7-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="07be7-239">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07be7-240"><strong>Käyttöveron vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="07be7-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="07be7-241">Verotapahtumien <strong>Verosummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="07be7-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="07be7-242">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="07be7-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="07be7-243"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="07be7-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="07be7-244">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="07be7-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="07be7-245">Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="07be7-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="07be7-246">Veron perustesumma on tapahtumasumma **Alkuperäinen summa kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="07be7-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="07be7-247">Veron summa on tapahtumasumma **Toteutunut arvonlisäverosumma kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="07be7-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="07be7-248">Raportin ER-mallin ja muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="07be7-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="07be7-249">Voit käyttää sähköistä raportointia (ER) määrittääksesi ilmoituksia ja raportteja sekä viedäksesi tietoja eri sähköisissä muodoissa muuttamatta X++ -koodia.</span><span class="sxs-lookup"><span data-stu-id="07be7-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="07be7-250">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="07be7-250">For additional information:</span></span>

-   [<span data-ttu-id="07be7-251">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="07be7-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="07be7-252">Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Servicesista</span><span class="sxs-lookup"><span data-stu-id="07be7-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="07be7-253">Lokalisoinnin vaatimukset – GER-konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="07be7-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="07be7-254">ALV-ilmoitusten maakohtaiset resurssit</span><span class="sxs-lookup"><span data-stu-id="07be7-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="07be7-255">Kunkin maan ALV-ilmoituksen on täytettävä sen maan lainsäädännön vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="07be7-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="07be7-256">On olemassa ennalta määritetyt mallit ja muodot ALV-ilmoituksille seuraavassa taulukossa luetelluissa maissa.</span><span class="sxs-lookup"><span data-stu-id="07be7-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="07be7-257">Maa tai alue</span><span class="sxs-lookup"><span data-stu-id="07be7-257">Country</span></span>        | <span data-ttu-id="07be7-258">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="07be7-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="07be7-259">Itävalta</span><span class="sxs-lookup"><span data-stu-id="07be7-259">Austria</span></span>        |  [<span data-ttu-id="07be7-260">ALV-ilmoituksen erittely, Itävalta</span><span class="sxs-lookup"><span data-stu-id="07be7-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="07be7-261">Belgia</span><span class="sxs-lookup"><span data-stu-id="07be7-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="07be7-262">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="07be7-262">Czech Republic</span></span> |  [<span data-ttu-id="07be7-263">ALV-ilmoituksen tiedot, Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="07be7-263">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="07be7-264">Viro</span><span class="sxs-lookup"><span data-stu-id="07be7-264">Estonia</span></span>        |  [<span data-ttu-id="07be7-265">ALV-ilmoituksen erittely, Viro</span><span class="sxs-lookup"><span data-stu-id="07be7-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="07be7-266">Suomi</span><span class="sxs-lookup"><span data-stu-id="07be7-266">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="07be7-267">Saksa</span><span class="sxs-lookup"><span data-stu-id="07be7-267">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="07be7-268">Italia</span><span class="sxs-lookup"><span data-stu-id="07be7-268">Italy</span></span>          | [<span data-ttu-id="07be7-269">ALV-ilmoituksen erittely, Italia</span><span class="sxs-lookup"><span data-stu-id="07be7-269">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="07be7-270">Latvia</span><span class="sxs-lookup"><span data-stu-id="07be7-270">Latvia</span></span>         | [<span data-ttu-id="07be7-271">ALV-ilmoituksen erittely, Latvia</span><span class="sxs-lookup"><span data-stu-id="07be7-271">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="07be7-272">Liettua</span><span class="sxs-lookup"><span data-stu-id="07be7-272">Lithuania</span></span>      | [<span data-ttu-id="07be7-273">ALV-ilmoituksen erittely, Liettua</span><span class="sxs-lookup"><span data-stu-id="07be7-273">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="07be7-274">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="07be7-274">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="07be7-275">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="07be7-275">Sweden</span></span>         |                                                                                 |






