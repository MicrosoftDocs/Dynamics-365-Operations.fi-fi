---
title: ALV-raportointi Euroopassa
description: Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efa9be4a5243444c2bf0b154836efbf8cfa76de9
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894667"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="2a95e-103">ALV-raportointi Euroopassa</span><span class="sxs-lookup"><span data-stu-id="2a95e-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a95e-104">Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="2a95e-105">Tämä ohjeaihe sisältää yleisen lähestymistavan ALV-ilmoituksen määrittämiseen ja luomiseen.</span><span class="sxs-lookup"><span data-stu-id="2a95e-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="2a95e-106">Tämä lähestymistapa on yhteinen yrityksille seuraavissa maissa/alueilla:</span><span class="sxs-lookup"><span data-stu-id="2a95e-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="2a95e-107">Itävalta</span><span class="sxs-lookup"><span data-stu-id="2a95e-107">Austria</span></span>
-   <span data-ttu-id="2a95e-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="2a95e-108">Belgium</span></span>
-   <span data-ttu-id="2a95e-109">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="2a95e-109">Czech Republic</span></span>
-   <span data-ttu-id="2a95e-110">Viro</span><span class="sxs-lookup"><span data-stu-id="2a95e-110">Estonia</span></span>
-   <span data-ttu-id="2a95e-111">Suomi</span><span class="sxs-lookup"><span data-stu-id="2a95e-111">Finland</span></span>
-   <span data-ttu-id="2a95e-112">Saksa</span><span class="sxs-lookup"><span data-stu-id="2a95e-112">Germany</span></span>
-   <span data-ttu-id="2a95e-113">Latvia</span><span class="sxs-lookup"><span data-stu-id="2a95e-113">Latvia</span></span>
-   <span data-ttu-id="2a95e-114">Liettua</span><span class="sxs-lookup"><span data-stu-id="2a95e-114">Lithuania</span></span>
-   <span data-ttu-id="2a95e-115">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="2a95e-115">Netherlands</span></span>
-   <span data-ttu-id="2a95e-116">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="2a95e-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="2a95e-117">ALV-ilmoituksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="2a95e-117">VAT statement overview</span></span>
<span data-ttu-id="2a95e-118">ALV-ilmoitus perustuu verotapahtumien summiin.</span><span class="sxs-lookup"><span data-stu-id="2a95e-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="2a95e-119">ALV-ilmoituksen luomisprosessi kuuluu arvonlisäveron maksamisen prosessiin, joka toteutetaan Tilitä ja kirjaa arvonlisävero -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="2a95e-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="2a95e-120">Tämä toiminto laskee arvonlisäveron, joka erääntyy tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="2a95e-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="2a95e-121">Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta verotapahtumille.</span><span class="sxs-lookup"><span data-stu-id="2a95e-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="2a95e-122">ALV-ilmoituksen tietojen laskentaprosessi perustuu arvonlisäverokoodien ja arvonlisäveroilmoituksen koodien suhteeseen, jossa ALV-raporttikoodit vastaavat ALV-ilmoitusten ruutuja (tai XML-tunnisteita).</span><span class="sxs-lookup"><span data-stu-id="2a95e-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="2a95e-123">Kullekin arvonlisäverokoodille arvonlisäveron raportointikoodit pitäisi määrittää kunkin tyyppiselle tapahtumalle, kuten verolliselle myynnille, verollisille ostoille tai verolliselle tuonnille.</span><span class="sxs-lookup"><span data-stu-id="2a95e-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="2a95e-124">Näiden tapahtumien tyyppi on kuvattu Arvonlisäverokoodit ALV-raportoinnissa -osassa jäljempänä tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="2a95e-125">Jokaiselle arvonlisäveroilmoituksen koodille olisi määritettävä tietty raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="2a95e-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="2a95e-126">Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn arvonlisäveroviranomaiseen arvonlisäveron tilityskausien kautta.</span><span class="sxs-lookup"><span data-stu-id="2a95e-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="2a95e-127">Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="2a95e-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="2a95e-128">Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, joka on määritetty ALV-viranomaiselle arvonlisäverokoodin arvonlisäveron tilityskausissa, voidaan valita arvonlisäverokoodin raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="2a95e-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="2a95e-129">Arvonlisäverotapahtuma, joka luodaan kirjatessa tilauksen tai päiväkirjan, sisältää arvonlisäverokoodin, arvonlisäveron lähteen, arvonlisäveron suunnan ja tapahtumasummat (veron peruste ja verosumma kirjanpitovaluuttana, ALV-valuutta ja tapahtumavaluutta).</span><span class="sxs-lookup"><span data-stu-id="2a95e-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="2a95e-130">Perustuen verotapahtuman määritteiden yhdistelmään, tapahtumasummat koostavat kokonaissummat arvonlisäverokoodeille määritetyille arvonlisäveroilmoituksen koodeille.</span><span class="sxs-lookup"><span data-stu-id="2a95e-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="2a95e-131">Seuraavassa on kuvattu tietojen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="2a95e-131">The following illustration shows the data relationship.</span></span>

![Kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="2a95e-133">ALV-ilmoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="2a95e-133">VAT statement setup</span></span>
<span data-ttu-id="2a95e-134">Voit luoda ALV-ilmoituksen määrittämällä seuraavat.</span><span class="sxs-lookup"><span data-stu-id="2a95e-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="2a95e-135">Veroviranomaiset ALV-raportointia varten</span><span class="sxs-lookup"><span data-stu-id="2a95e-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="2a95e-136">Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea raporttiasettelu arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="2a95e-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="2a95e-137">Valitse **Arvonlisäveroviranomaiset**-sivulla **Yleiset**-osassa **Raportin asettelu**.</span><span class="sxs-lookup"><span data-stu-id="2a95e-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="2a95e-138">Tätä asettelua käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.</span><span class="sxs-lookup"><span data-stu-id="2a95e-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="2a95e-139">Arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="2a95e-139">Sales tax reporting codes</span></span>

<span data-ttu-id="2a95e-140">ALV-ilmoituskoodit ovat ruutukoodeja ALV-ilmoituksessa tai tunnisteen nimiä XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="2a95e-141">Näitä koodeja käytetään keräämään ja valmistelemaan raportin summat.</span><span class="sxs-lookup"><span data-stu-id="2a95e-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="2a95e-142">ALV-ilmoituksen sähköisen raportoinnin muotoa määrittäessäsi käytetään tulossummien nimiä.</span><span class="sxs-lookup"><span data-stu-id="2a95e-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="2a95e-143">Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodeja **Arvonlisäveroilmoituksen koodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2a95e-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="2a95e-144">Jokaiselle koodille tulee määrittää raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="2a95e-144">You must assign each code a report layout.</span></span> <span data-ttu-id="2a95e-145">Kun olet luonut arvonlisäveroraportin koodit, voit valita koodeja **Arvonlisäverokoodit**-sivun **Raportin asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="2a95e-146">ALV-ilmoituksen arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="2a95e-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="2a95e-147"> Arvonlisäverotapahtumien perussummat ja verosummat voidaan koostaa ALV-ilmoituksen raportointikoodeista (XML-tunnisteista tai ilmoitusruuduista).</span><span class="sxs-lookup"><span data-stu-id="2a95e-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="2a95e-148">Voit määrittää tämän liittämällä arvonlisäveroilmoituksen koodit arvonlisäverokoodien eri tapahtumalajeille <strong>Arvonlisäverokoodit</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2a95e-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="2a95e-149">Seuraavassa taulukossa kuvataan tapahtumatyypit arvonlisäverokoodien raporttiasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="2a95e-150">Laskenta sisältää tapahtumia kaiken tyyppisille lähteille lukuun ottamatta arvonlisäveroa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2a95e-151"><strong>Tapahtumalaji</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="2a95e-152"><strong>Tapahtumien kuvaus ja tapahtumatyypille laskettavat summat</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-153"><strong>Verollinen myynti</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="2a95e-154">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-155">Tapahtumapäivä on valitussa kaudessa/</span><span class="sxs-lookup"><span data-stu-id="2a95e-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="2a95e-156">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-157">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-158"><strong>Verovapaa myynti</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="2a95e-159">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-160">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-161">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-162">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-163"><strong>Maksettava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="2a95e-164">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-165">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-166">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-167">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-168"><strong>Verollinen hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-169">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-170">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-171">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-172">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-173"><strong>Verovapaa hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-174">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-175">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-176">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-177">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-178"><strong>Myyntihyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-179">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-180">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-181">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-182">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-183"><strong>Verollinen osto</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="2a95e-184">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-185">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-186">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-187">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-188"><strong>Verovapaa osto</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="2a95e-189">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-190">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-191">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-192">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-193"><strong>Saatava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="2a95e-194">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-195">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-196">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-197">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-198"><strong>Verollinen ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-199">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-200">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-201">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-202">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-203"><strong>Verovapaa ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-204">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-205">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-206">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-207">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-208"><strong>Ostohyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-209">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-210">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-211">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="2a95e-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="2a95e-212">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-213"><strong>Verollinen tuonti</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="2a95e-214">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-215">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-216"><strong>Veron suunta</strong> on <strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="2a95e-217">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-218"><strong>Verollinen tuonti vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="2a95e-219">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-220">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-221"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a95e-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="2a95e-222">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-223"><strong>Verollinen tuontihyvitysmaksu</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-224">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-225">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="2a95e-226">e</span><span class="sxs-lookup"><span data-stu-id="2a95e-226">e</span></span><li><span data-ttu-id="2a95e-227"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a95e-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="2a95e-228">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-229"><strong>Verollinen tuontihyvityslasku vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="2a95e-230">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-231">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-232">Veron suunta on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a95e-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="2a95e-233">d</span><span class="sxs-lookup"><span data-stu-id="2a95e-233">d</span></span><li><span data-ttu-id="2a95e-234">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2a95e-235"><strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="2a95e-236">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-237">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-238"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a95e-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="2a95e-239">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2a95e-240"><strong>Käyttöveron vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="2a95e-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="2a95e-241">Verotapahtumien <strong>Verosummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="2a95e-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="2a95e-242">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="2a95e-243"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="2a95e-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="2a95e-244">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="2a95e-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2a95e-245">Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="2a95e-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="2a95e-246">Veron perustesumma on tapahtumasumma **Alkuperäinen summa kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="2a95e-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="2a95e-247">Veron summa on tapahtumasumma **Toteutunut arvonlisäverosumma kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="2a95e-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="2a95e-248">Raportin ER-mallin ja muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2a95e-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="2a95e-249">Voit käyttää sähköistä raportointia (ER) määrittääksesi ilmoituksia ja raportteja sekä viedäksesi tietoja eri sähköisissä muodoissa muuttamatta X++ -koodia.</span><span class="sxs-lookup"><span data-stu-id="2a95e-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="2a95e-250">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="2a95e-250">For additional information:</span></span>

-   [<span data-ttu-id="2a95e-251">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="2a95e-251">Electronic reporting overview</span></span>](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="2a95e-252">Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Servicesista</span><span class="sxs-lookup"><span data-stu-id="2a95e-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="2a95e-253">Lokalisoinnin vaatimukset – GER-konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="2a95e-253">Localization requirements – Create a GER configuration</span></span>](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="2a95e-254">ALV-ilmoitusten maakohtaiset resurssit</span><span class="sxs-lookup"><span data-stu-id="2a95e-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="2a95e-255">Kunkin maan ALV-ilmoituksen on täytettävä sen maan lainsäädännön vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="2a95e-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="2a95e-256">On olemassa ennalta määritetyt mallit ja muodot ALV-ilmoituksille seuraavassa taulukossa luetelluissa maissa.</span><span class="sxs-lookup"><span data-stu-id="2a95e-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="2a95e-257">Maa tai alue</span><span class="sxs-lookup"><span data-stu-id="2a95e-257">Country</span></span>        | <span data-ttu-id="2a95e-258">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="2a95e-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2a95e-259">Itävalta</span><span class="sxs-lookup"><span data-stu-id="2a95e-259">Austria</span></span>        |  [<span data-ttu-id="2a95e-260">ALV-ilmoituksen erittely, Itävalta</span><span class="sxs-lookup"><span data-stu-id="2a95e-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="2a95e-261">Belgia</span><span class="sxs-lookup"><span data-stu-id="2a95e-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="2a95e-262">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="2a95e-262">Czech Republic</span></span> |  [<span data-ttu-id="2a95e-263">Tšekin tasavallan ALV-ilmoitus</span><span class="sxs-lookup"><span data-stu-id="2a95e-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="2a95e-264">Viro</span><span class="sxs-lookup"><span data-stu-id="2a95e-264">Estonia</span></span>        |  [<span data-ttu-id="2a95e-265">ALV-ilmoituksen erittely, Viro</span><span class="sxs-lookup"><span data-stu-id="2a95e-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="2a95e-266">Suomi</span><span class="sxs-lookup"><span data-stu-id="2a95e-266">Finland</span></span>        | [<span data-ttu-id="2a95e-267">Suomen arvonlisäveroraportti</span><span class="sxs-lookup"><span data-stu-id="2a95e-267">Sales tax report for Finland</span></span>](emea-fin-sales-tax-payment-report-finland.md)          |
| <span data-ttu-id="2a95e-268">Saksa</span><span class="sxs-lookup"><span data-stu-id="2a95e-268">Germany</span></span>        | [<span data-ttu-id="2a95e-269">Saksan ALV-ilmoitus</span><span class="sxs-lookup"><span data-stu-id="2a95e-269">VAT declaration for Germany</span></span>](emea-de-vat-declaration.md)                       |
| <span data-ttu-id="2a95e-270">Italia</span><span class="sxs-lookup"><span data-stu-id="2a95e-270">Italy</span></span>          | [<span data-ttu-id="2a95e-271">ALV-ilmoituksen erittely, Italia</span><span class="sxs-lookup"><span data-stu-id="2a95e-271">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="2a95e-272">Latvia</span><span class="sxs-lookup"><span data-stu-id="2a95e-272">Latvia</span></span>         | [<span data-ttu-id="2a95e-273">ALV-ilmoituksen erittely, Latvia</span><span class="sxs-lookup"><span data-stu-id="2a95e-273">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="2a95e-274">Liettua</span><span class="sxs-lookup"><span data-stu-id="2a95e-274">Lithuania</span></span>      | [<span data-ttu-id="2a95e-275">ALV-ilmoituksen erittely, Liettua</span><span class="sxs-lookup"><span data-stu-id="2a95e-275">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="2a95e-276">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="2a95e-276">Netherlands</span></span>    | [<span data-ttu-id="2a95e-277">Alankomaiden ALV-ilmoitus</span><span class="sxs-lookup"><span data-stu-id="2a95e-277">VAT declaration for the Netherlands</span></span>](emea-nl-vat-declaration.md)           |
| <span data-ttu-id="2a95e-278">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="2a95e-278">Sweden</span></span>         | [<span data-ttu-id="2a95e-279">Ruotsin arvonlisäveroraportti</span><span class="sxs-lookup"><span data-stu-id="2a95e-279">Sales tax report for Sweden</span></span>](emea-swe-sales-tax-payment-report-sweden.md)          |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]