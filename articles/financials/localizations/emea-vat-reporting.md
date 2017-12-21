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
ms.sourcegitcommit: 7ce3c0397986ba2281aae7b71d579f3fe5f488ae
ms.openlocfilehash: 415e23190c6d7d12e824a42dec3916a4c3f5bc92
ms.contentlocale: fi-fi
ms.lasthandoff: 12/21/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="96766-103">ALV-raportointi Euroopassa</span><span class="sxs-lookup"><span data-stu-id="96766-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="96766-104">Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.</span><span class="sxs-lookup"><span data-stu-id="96766-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="96766-105">Tämä ohjeaihe sisältää yleisen lähestymistavan ALV-ilmoituksen määrittämiseen ja luomiseen.</span><span class="sxs-lookup"><span data-stu-id="96766-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="96766-106">Tämä lähestymistapa on yhteinen yrityksille seuraavissa maissa/alueilla:</span><span class="sxs-lookup"><span data-stu-id="96766-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="96766-107">Itävalta</span><span class="sxs-lookup"><span data-stu-id="96766-107">Austria</span></span>
-   <span data-ttu-id="96766-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="96766-108">Belgium</span></span>
-   <span data-ttu-id="96766-109">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="96766-109">Czech Republic</span></span>
-   <span data-ttu-id="96766-110">Viro</span><span class="sxs-lookup"><span data-stu-id="96766-110">Estonia</span></span>
-   <span data-ttu-id="96766-111">Suomi</span><span class="sxs-lookup"><span data-stu-id="96766-111">Finland</span></span>
-   <span data-ttu-id="96766-112">Saksa</span><span class="sxs-lookup"><span data-stu-id="96766-112">Germany</span></span>
-   <span data-ttu-id="96766-113">Latvia</span><span class="sxs-lookup"><span data-stu-id="96766-113">Latvia</span></span>
-   <span data-ttu-id="96766-114">Liettua</span><span class="sxs-lookup"><span data-stu-id="96766-114">Lithuania</span></span>
-   <span data-ttu-id="96766-115">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="96766-115">Netherlands</span></span>
-   <span data-ttu-id="96766-116">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="96766-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="96766-117">ALV-ilmoituksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="96766-117">VAT statement overview</span></span>
<span data-ttu-id="96766-118">ALV-ilmoitus perustuu verotapahtumien summiin.</span><span class="sxs-lookup"><span data-stu-id="96766-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="96766-119">ALV-ilmoituksen luomisprosessi kuuluu arvonlisäveron maksamisen prosessiin, joka toteutetaan Tilitä ja kirjaa arvonlisävero -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="96766-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="96766-120">Tämä toiminto laskee arvonlisäveron, joka erääntyy tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="96766-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="96766-121">Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta verotapahtumille.</span><span class="sxs-lookup"><span data-stu-id="96766-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="96766-122">ALV-ilmoituksen tietojen laskentaprosessi perustuu arvonlisäverokoodien ja arvonlisäveroilmoituksen koodien suhteeseen, jossa ALV-raporttikoodit vastaavat ALV-ilmoitusten ruutuja (tai XML-tunnisteita).</span><span class="sxs-lookup"><span data-stu-id="96766-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="96766-123">Kullekin arvonlisäverokoodille arvonlisäveron raportointikoodit pitäisi määrittää kunkin tyyppiselle tapahtumalle, kuten verolliselle myynnille, verollisille ostoille tai verolliselle tuonnille.</span><span class="sxs-lookup"><span data-stu-id="96766-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="96766-124">Näiden tapahtumien tyyppi on kuvattu Arvonlisäverokoodit ALV-raportoinnissa -osassa jäljempänä tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="96766-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="96766-125">Jokaiselle arvonlisäveroilmoituksen koodille olisi määritettävä tietty raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="96766-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="96766-126">Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn arvonlisäveroviranomaiseen arvonlisäveron tilityskausien kautta.</span><span class="sxs-lookup"><span data-stu-id="96766-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="96766-127">Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="96766-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="96766-128">Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, joka on määritetty ALV-viranomaiselle arvonlisäverokoodin arvonlisäveron tilityskausissa, voidaan valita arvonlisäverokoodin raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="96766-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="96766-129">Arvonlisäverotapahtuma, joka luodaan kirjatessa tilauksen tai päiväkirjan, sisältää arvonlisäverokoodin, arvonlisäveron lähteen, arvonlisäveron suunnan ja tapahtumasummat (veron peruste ja verosumma kirjanpitovaluuttana, ALV-valuutta ja tapahtumavaluutta).</span><span class="sxs-lookup"><span data-stu-id="96766-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="96766-130">Perustuen verotapahtuman määritteiden yhdistelmään, tapahtumasummat koostavat kokonaissummat arvonlisäverokoodeille määritetyille arvonlisäveroilmoituksen koodeille.</span><span class="sxs-lookup"><span data-stu-id="96766-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="96766-131">Seuraavassa on kuvattu tietojen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="96766-131">The following illustration shows the data relationship.</span></span>

![Kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="96766-133">ALV-ilmoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="96766-133">VAT statement setup</span></span>
<span data-ttu-id="96766-134">Voit luoda ALV-ilmoituksen määrittämällä seuraavat.</span><span class="sxs-lookup"><span data-stu-id="96766-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="96766-135">Veroviranomaiset ALV-raportointia varten</span><span class="sxs-lookup"><span data-stu-id="96766-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="96766-136">Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea raporttiasettelu arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="96766-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="96766-137">Valitse **Arvonlisäveroviranomaiset**-sivulla **Yleiset**-osassa **Raportin asettelu**.</span><span class="sxs-lookup"><span data-stu-id="96766-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="96766-138">Tätä asettelua käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.</span><span class="sxs-lookup"><span data-stu-id="96766-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="96766-139">Arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="96766-139">Sales tax reporting codes</span></span>

<span data-ttu-id="96766-140">ALV-ilmoituskoodit ovat ruutukoodeja ALV-ilmoituksessa tai tunnisteen nimiä XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="96766-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="96766-141">Näitä koodeja käytetään keräämään ja valmistelemaan raportin summat.</span><span class="sxs-lookup"><span data-stu-id="96766-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="96766-142">ALV-ilmoituksen sähköisen raportoinnin muotoa määrittäessäsi käytetään tulossummien nimiä.</span><span class="sxs-lookup"><span data-stu-id="96766-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="96766-143">Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodeja **Arvonlisäveroilmoituksen koodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="96766-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="96766-144">Jokaiselle koodille tulee määrittää raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="96766-144">You must assign each code a report layout.</span></span> <span data-ttu-id="96766-145">Kun olet luonut arvonlisäveroraportin koodit, voit valita koodeja **Arvonlisäverokoodit**-sivun **Raportin asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="96766-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="96766-146">ALV-ilmoituksen arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="96766-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="96766-147"><strong>Tapahtumatyyppi</strong></span><span class="sxs-lookup"><span data-stu-id="96766-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="96766-148"><strong>Tapahtumien kuvaus ja tapahtumatyypille laskettavat summat</strong></span><span class="sxs-lookup"><span data-stu-id="96766-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-149"><strong>Verollinen myynti</strong></span><span class="sxs-lookup"><span data-stu-id="96766-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="96766-150">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-151">Tapahtumapäivä on valitussa kaudessa/</span><span class="sxs-lookup"><span data-stu-id="96766-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="96766-152">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="96766-153">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-154"><strong>Verovapaa myynti</strong></span><span class="sxs-lookup"><span data-stu-id="96766-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="96766-155">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-156">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-157">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="96766-158">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-159"><strong>Maksettava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="96766-160">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-161">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-162">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="96766-163">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-164"><strong>Verollinen hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="96766-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="96766-165">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-166">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-167">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="96766-168">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-169"><strong>Verovapaa hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="96766-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="96766-170">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-171">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-172">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="96766-173">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-174"><strong>Myyntihyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="96766-175">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-176">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-177">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="96766-178">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-179"><strong>Verollinen osto</strong></span><span class="sxs-lookup"><span data-stu-id="96766-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="96766-180">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-181">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-182">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="96766-183">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-184"><strong>Verovapaa osto</strong></span><span class="sxs-lookup"><span data-stu-id="96766-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="96766-185">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-186">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-187">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="96766-188">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-189"><strong>Saatava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="96766-190">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-191">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-192">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="96766-193">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-194"><strong>Verollinen ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="96766-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="96766-195">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-196">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-197">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="96766-198">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-199"><strong>Verovapaa ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="96766-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="96766-200">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-201">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-202">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="96766-203">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-204"><strong>Ostohyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="96766-205">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-206">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-207">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="96766-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="96766-208">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-209"><strong>Verollinen tuonti</strong></span><span class="sxs-lookup"><span data-stu-id="96766-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="96766-210">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-211">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-212"><strong>Veron suunta</strong> on <strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="96766-213">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-214"><strong>Verollinen tuonti vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="96766-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="96766-215">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-216">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-217"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="96766-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="96766-218">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-219"><strong>Verollinen tuontihyvitysmaksu</strong></span><span class="sxs-lookup"><span data-stu-id="96766-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="96766-220">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-221">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="96766-222">e</span><span class="sxs-lookup"><span data-stu-id="96766-222">e</span></span><li><span data-ttu-id="96766-223"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="96766-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="96766-224">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-225"><strong>Verollinen tuontihyvityslasku vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="96766-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="96766-226">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-227">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-228">Veron suunta on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="96766-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="96766-229">d</span><span class="sxs-lookup"><span data-stu-id="96766-229">d</span></span><li><span data-ttu-id="96766-230">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="96766-231"><strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="96766-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="96766-232">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-233">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-234"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="96766-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="96766-235">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="96766-236"><strong>Käyttöveron vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="96766-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="96766-237">Verotapahtumien <strong>Verosummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="96766-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="96766-238">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="96766-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="96766-239"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="96766-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="96766-240">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="96766-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="96766-241">Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="96766-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="96766-242">Veron perustesumma on tapahtumasumma **Alkuperäinen summa kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="96766-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="96766-243">Veron summa on tapahtumasumma **Toteutunut arvonlisäverosumma kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="96766-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="96766-244">Raportin ER-mallin ja muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="96766-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="96766-245">Voit käyttää sähköistä raportointia (ER) määrittääksesi ilmoituksia ja raportteja sekä viedäksesi tietoja eri sähköisissä muodoissa muuttamatta X++ -koodia.</span><span class="sxs-lookup"><span data-stu-id="96766-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="96766-246">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="96766-246">For additional information:</span></span>

-   [<span data-ttu-id="96766-247">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="96766-247">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="96766-248">Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Servicesista</span><span class="sxs-lookup"><span data-stu-id="96766-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="96766-249">Lokalisoinnin vaatimukset – GER-konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="96766-249">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="96766-250">ALV-ilmoitusten maakohtaiset resurssit</span><span class="sxs-lookup"><span data-stu-id="96766-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="96766-251">Kunkin maan ALV-ilmoituksen on täytettävä sen maan lainsäädännön vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="96766-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="96766-252">On olemassa ennalta määritetyt mallit ja muodot ALV-ilmoituksille seuraavassa taulukossa luetelluissa maissa.</span><span class="sxs-lookup"><span data-stu-id="96766-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="96766-253">Maa tai alue</span><span class="sxs-lookup"><span data-stu-id="96766-253">Country</span></span>        | <span data-ttu-id="96766-254">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="96766-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="96766-255">Itävalta</span><span class="sxs-lookup"><span data-stu-id="96766-255">Austria</span></span>        |  [<span data-ttu-id="96766-256">ALV-ilmoituksen erittely, Itävalta</span><span class="sxs-lookup"><span data-stu-id="96766-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="96766-257">Belgia</span><span class="sxs-lookup"><span data-stu-id="96766-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="96766-258">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="96766-258">Czech Republic</span></span> |  [<span data-ttu-id="96766-259">ALV-ilmoituksen tiedot, Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="96766-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="96766-260">Viro</span><span class="sxs-lookup"><span data-stu-id="96766-260">Estonia</span></span>        |  [<span data-ttu-id="96766-261">ALV-ilmoituksen erittely, Viro</span><span class="sxs-lookup"><span data-stu-id="96766-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="96766-262">Suomi</span><span class="sxs-lookup"><span data-stu-id="96766-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="96766-263">Saksa</span><span class="sxs-lookup"><span data-stu-id="96766-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="96766-264">Italia</span><span class="sxs-lookup"><span data-stu-id="96766-264">Italy</span></span>          | [<span data-ttu-id="96766-265">ALV-ilmoituksen erittely, Italia</span><span class="sxs-lookup"><span data-stu-id="96766-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="96766-266">Latvia</span><span class="sxs-lookup"><span data-stu-id="96766-266">Latvia</span></span>         | [<span data-ttu-id="96766-267">ALV-ilmoituksen erittely, Latvia</span><span class="sxs-lookup"><span data-stu-id="96766-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="96766-268">Liettua</span><span class="sxs-lookup"><span data-stu-id="96766-268">Lithuania</span></span>      | [<span data-ttu-id="96766-269">ALV-ilmoituksen erittely, Liettua</span><span class="sxs-lookup"><span data-stu-id="96766-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="96766-270">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="96766-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="96766-271">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="96766-271">Sweden</span></span>         |                                                                                 |






