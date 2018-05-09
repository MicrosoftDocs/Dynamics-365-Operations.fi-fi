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
ms.lasthandoff: 05/08/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="6e3c7-103">ALV-raportointi Euroopassa</span><span class="sxs-lookup"><span data-stu-id="6e3c7-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e3c7-104">Tässä aiheessa on yleistietoja (ALV)-lauseen määrittämisestä ja muodostamisesta joissakin Euroopan maissa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="6e3c7-105">Tämä ohjeaihe sisältää yleisen lähestymistavan ALV-ilmoituksen määrittämiseen ja luomiseen.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="6e3c7-106">Tämä lähestymistapa on yhteinen yrityksille seuraavissa maissa/alueilla:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="6e3c7-107">Itävalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-107">Austria</span></span>
-   <span data-ttu-id="6e3c7-108">Belgia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-108">Belgium</span></span>
-   <span data-ttu-id="6e3c7-109">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-109">Czech Republic</span></span>
-   <span data-ttu-id="6e3c7-110">Viro</span><span class="sxs-lookup"><span data-stu-id="6e3c7-110">Estonia</span></span>
-   <span data-ttu-id="6e3c7-111">Suomi</span><span class="sxs-lookup"><span data-stu-id="6e3c7-111">Finland</span></span>
-   <span data-ttu-id="6e3c7-112">Saksa</span><span class="sxs-lookup"><span data-stu-id="6e3c7-112">Germany</span></span>
-   <span data-ttu-id="6e3c7-113">Latvia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-113">Latvia</span></span>
-   <span data-ttu-id="6e3c7-114">Liettua</span><span class="sxs-lookup"><span data-stu-id="6e3c7-114">Lithuania</span></span>
-   <span data-ttu-id="6e3c7-115">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="6e3c7-115">Netherlands</span></span>
-   <span data-ttu-id="6e3c7-116">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="6e3c7-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="6e3c7-117">ALV-ilmoituksen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="6e3c7-117">VAT statement overview</span></span>
<span data-ttu-id="6e3c7-118">ALV-ilmoitus perustuu verotapahtumien summiin.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="6e3c7-119">ALV-ilmoituksen luomisprosessi kuuluu arvonlisäveron maksamisen prosessiin, joka toteutetaan Tilitä ja kirjaa arvonlisävero -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="6e3c7-120">Tämä toiminto laskee arvonlisäveron, joka erääntyy tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="6e3c7-121">Tilityksen laskenta sisältää kirjatun arvonlisäveron valitulta tilityskaudelta verotapahtumille.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="6e3c7-122">ALV-ilmoituksen tietojen laskentaprosessi perustuu arvonlisäverokoodien ja arvonlisäveroilmoituksen koodien suhteeseen, jossa ALV-raporttikoodit vastaavat ALV-ilmoitusten ruutuja (tai XML-tunnisteita).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="6e3c7-123">Kullekin arvonlisäverokoodille arvonlisäveron raportointikoodit pitäisi määrittää kunkin tyyppiselle tapahtumalle, kuten verolliselle myynnille, verollisille ostoille tai verolliselle tuonnille.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="6e3c7-124">Näiden tapahtumien tyyppi on kuvattu Arvonlisäverokoodit ALV-raportoinnissa -osassa jäljempänä tässä ohjeaiheessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="6e3c7-125">Jokaiselle arvonlisäveroilmoituksen koodille olisi määritettävä tietty raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="6e3c7-126">Samaan aikaan arvonlisäverokoodit on linkitetty tiettyyn arvonlisäveroviranomaiseen arvonlisäveron tilityskausien kautta.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="6e3c7-127">Jokaiselle arvonlisäveroviranomaiselle olisi määritettävä raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="6e3c7-128">Näin ollen ainoastaan raportointikoodeja, joilla on sama raporttiasettelu, joka on määritetty ALV-viranomaiselle arvonlisäverokoodin arvonlisäveron tilityskausissa, voidaan valita arvonlisäverokoodin raportin määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="6e3c7-129">Arvonlisäverotapahtuma, joka luodaan kirjatessa tilauksen tai päiväkirjan, sisältää arvonlisäverokoodin, arvonlisäveron lähteen, arvonlisäveron suunnan ja tapahtumasummat (veron peruste ja verosumma kirjanpitovaluuttana, ALV-valuutta ja tapahtumavaluutta).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="6e3c7-130">Perustuen verotapahtuman määritteiden yhdistelmään, tapahtumasummat koostavat kokonaissummat arvonlisäverokoodeille määritetyille arvonlisäveroilmoituksen koodeille.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="6e3c7-131">Seuraavassa on kuvattu tietojen suhdetta.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-131">The following illustration shows the data relationship.</span></span>

![Kaavio](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="6e3c7-133">ALV-ilmoituksen asetukset</span><span class="sxs-lookup"><span data-stu-id="6e3c7-133">VAT statement setup</span></span>
<span data-ttu-id="6e3c7-134">Voit luoda ALV-ilmoituksen määrittämällä seuraavat.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="6e3c7-135">Veroviranomaiset ALV-raportointia varten</span><span class="sxs-lookup"><span data-stu-id="6e3c7-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="6e3c7-136">Ennen kuin voit määrittää arvonlisäveroilmoituksen koodit, sinun on valittava oikea raporttiasettelu arvonlisäveroviranomaiselle.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="6e3c7-137">Valitse **Arvonlisäveroviranomaiset**-sivulla **Yleiset**-osassa **Raportin asettelu**.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="6e3c7-138">Tätä asettelua käytetään määrittäessäsi arvonlisäveroilmoituksen koodit.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="6e3c7-139">Arvonlisäveroilmoituksen koodit</span><span class="sxs-lookup"><span data-stu-id="6e3c7-139">Sales tax reporting codes</span></span>

<span data-ttu-id="6e3c7-140">ALV-ilmoituskoodit ovat ruutukoodeja ALV-ilmoituksessa tai tunnisteen nimiä XML-muodossa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="6e3c7-141">Näitä koodeja käytetään keräämään ja valmistelemaan raportin summat.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="6e3c7-142">ALV-ilmoituksen sähköisen raportoinnin muotoa määrittäessäsi käytetään tulossummien nimiä.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="6e3c7-143">Voit luoda ja ylläpitää arvonlisäveroilmoituksen koodeja **Arvonlisäveroilmoituksen koodit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="6e3c7-144">Jokaiselle koodille tulee määrittää raporttiasettelu.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-144">You must assign each code a report layout.</span></span> <span data-ttu-id="6e3c7-145">Kun olet luonut arvonlisäveroraportin koodit, voit valita koodeja **Arvonlisäverokoodit**-sivun **Raportin asetukset** -osassa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="6e3c7-146">ALV-ilmoituksen arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="6e3c7-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="6e3c7-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Arvonlisäverokoodit</strong>-sivu.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="6e3c7-148">Seuraavassa taulukossa kuvataan tapahtumatyypit arvonlisäverokoodien raporttiasetuksissa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="6e3c7-149">Laskenta sisältää tapahtumia kaiken tyyppisille lähteille lukuun ottamatta arvonlisäveroa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6e3c7-150"><strong>Tapahtumalaji</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="6e3c7-151"><strong>Tapahtumien kuvaus ja tapahtumatyypille laskettavat summat</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-152"><strong>Verollinen myynti</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="6e3c7-153">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-154">Tapahtumapäivä on valitussa kaudessa/</span><span class="sxs-lookup"><span data-stu-id="6e3c7-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="6e3c7-155">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-156">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-157"><strong>Verovapaa myynti</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="6e3c7-158">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-159">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-160">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-161">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-162"><strong>Maksettava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="6e3c7-163">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-164">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-165">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-166">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-167"><strong>Verollinen hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-168">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-169">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-170">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-171">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-172"><strong>Verovapaa hyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-173">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-174">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-175">Myynti on vientiä (<strong>Veron suunta</strong> on <strong>Verovapaa myynti</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-176">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-177"><strong>Myyntihyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-178">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-179">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-180">Myynti on kotimaista (<strong>Veron suunta</strong> on <strong>Maksettava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-181">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-182"><strong>Verollinen osto</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="6e3c7-183">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-184">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-185">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-186">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-187"><strong>Verovapaa osto</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="6e3c7-188">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-189">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-190">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-191">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-192"><strong>Saatava arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="6e3c7-193">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-194">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-195">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-196">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-197"><strong>Verollinen ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-198">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-199">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-200">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-201">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-202"><strong>Verovapaa ostohyvityslasku</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-203">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-204">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-205">Osto on tuontia (<strong>Veron suunta</strong> on <strong>Verovapaa osto</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-206">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-207"><strong>Ostohyvityslaskun arvonlisävero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-208">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-209">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-210">Osto on kotimaista (<strong>Veron suunta</strong> on <strong>Saatava arvonlisävero</strong>).</span><span class="sxs-lookup"><span data-stu-id="6e3c7-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="6e3c7-211">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-212"><strong>Verollinen tuonti</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="6e3c7-213">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-214">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-215"><strong>Veron suunta</strong> on <strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="6e3c7-216">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-217"><strong>Verollinen tuonti vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="6e3c7-218">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-219">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-220"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="6e3c7-221">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-222"><strong>Verollinen tuontihyvitysmaksu</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-223">Verotapahtumien <strong>Veron perustesummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-224">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="6e3c7-225">e</span><span class="sxs-lookup"><span data-stu-id="6e3c7-225">e</span></span><li><span data-ttu-id="6e3c7-226"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="6e3c7-227">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-228"><strong>Verollinen tuontihyvityslasku vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="6e3c7-229">Verotapahtumien <strong>Veron perustesummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-230">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-231">Veron suunta on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="6e3c7-232">d</span><span class="sxs-lookup"><span data-stu-id="6e3c7-232">d</span></span><li><span data-ttu-id="6e3c7-233">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&lt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6e3c7-234"><strong>Käyttövero</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="6e3c7-235">Verotapahtumien <strong>Verosummien</strong> summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-236">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-237"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="6e3c7-238">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6e3c7-239"><strong>Käyttöveron vastakirjaus</strong></span><span class="sxs-lookup"><span data-stu-id="6e3c7-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="6e3c7-240">Verotapahtumien <strong>Verosummien</strong> käänteinen summa tapahtumille, jotka täyttävät seuraavat edellytykset:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="6e3c7-241">Tapahtumapäivä on valitussa kaudessa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="6e3c7-242"><strong>Veron suunta</strong> on <strong>Käyttövero</strong>.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="6e3c7-243">Tapahtuman <strong>Veron perustesumma</strong> tai <strong>Verosumma</strong>&gt; 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="6e3c7-244">Edellä olevassa taulukossa oletetaan, että seuraavat ehdot täyttyvät:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="6e3c7-245">Veron perustesumma on tapahtumasumma **Alkuperäinen summa kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="6e3c7-246">Veron summa on tapahtumasumma **Toteutunut arvonlisäverosumma kirjanpitovaluuttana** -kentästä.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="6e3c7-247">Raportin ER-mallin ja muodon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6e3c7-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="6e3c7-248">Voit käyttää sähköistä raportointia (ER) määrittääksesi ilmoituksia ja raportteja sekä viedäksesi tietoja eri sähköisissä muodoissa muuttamatta X++ -koodia.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="6e3c7-249">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="6e3c7-249">For additional information:</span></span>

-   [<span data-ttu-id="6e3c7-250">Sähköisen raportoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6e3c7-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="6e3c7-251">Sähköisen raportoinnin konfiguraatioiden lataaminen Lifecycle Servicesista</span><span class="sxs-lookup"><span data-stu-id="6e3c7-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="6e3c7-252">Lokalisoinnin vaatimukset – GER-konfiguraation luominen</span><span class="sxs-lookup"><span data-stu-id="6e3c7-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="6e3c7-253">ALV-ilmoitusten maakohtaiset resurssit</span><span class="sxs-lookup"><span data-stu-id="6e3c7-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="6e3c7-254">Kunkin maan ALV-ilmoituksen on täytettävä sen maan lainsäädännön vaatimukset.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="6e3c7-255">On olemassa ennalta määritetyt mallit ja muodot ALV-ilmoituksille seuraavassa taulukossa luetelluissa maissa.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="6e3c7-256">Maa tai alue</span><span class="sxs-lookup"><span data-stu-id="6e3c7-256">Country</span></span>        | <span data-ttu-id="6e3c7-257">Lisätiedot</span><span class="sxs-lookup"><span data-stu-id="6e3c7-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="6e3c7-258">Itävalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-258">Austria</span></span>        |  [<span data-ttu-id="6e3c7-259">ALV-ilmoituksen erittely, Itävalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="6e3c7-260">Belgia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="6e3c7-261">Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-261">Czech Republic</span></span> |  [<span data-ttu-id="6e3c7-262">ALV-ilmoituksen tiedot, Tšekin tasavalta</span><span class="sxs-lookup"><span data-stu-id="6e3c7-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="6e3c7-263">Viro</span><span class="sxs-lookup"><span data-stu-id="6e3c7-263">Estonia</span></span>        |  [<span data-ttu-id="6e3c7-264">ALV-ilmoituksen erittely, Viro</span><span class="sxs-lookup"><span data-stu-id="6e3c7-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="6e3c7-265">Suomi</span><span class="sxs-lookup"><span data-stu-id="6e3c7-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="6e3c7-266">Saksa</span><span class="sxs-lookup"><span data-stu-id="6e3c7-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="6e3c7-267">Italia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-267">Italy</span></span>          | [<span data-ttu-id="6e3c7-268">ALV-ilmoituksen erittely, Italia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="6e3c7-269">Latvia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-269">Latvia</span></span>         | [<span data-ttu-id="6e3c7-270">ALV-ilmoituksen erittely, Latvia</span><span class="sxs-lookup"><span data-stu-id="6e3c7-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="6e3c7-271">Liettua</span><span class="sxs-lookup"><span data-stu-id="6e3c7-271">Lithuania</span></span>      | [<span data-ttu-id="6e3c7-272">ALV-ilmoituksen erittely, Liettua</span><span class="sxs-lookup"><span data-stu-id="6e3c7-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="6e3c7-273">Alankomaat</span><span class="sxs-lookup"><span data-stu-id="6e3c7-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="6e3c7-274">Ruotsi</span><span class="sxs-lookup"><span data-stu-id="6e3c7-274">Sweden</span></span>         |                                                                                 |






