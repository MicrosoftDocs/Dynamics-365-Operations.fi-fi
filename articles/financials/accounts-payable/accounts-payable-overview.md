---
title: "Ostoreskontran määrittäminen"
description: "Tässä artikkelissa kuvataan sivut, joiden avulla määritetään perus- ja valinnaiset toiminnot Microsoft Dynamics 365 for Finance and Operationsin ostoreskontrassa. Artikkelissa kerrotaan myös ennen ostoreskontran määrittämisen aloittamista suoritettavat asetusvaiheet."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6a832a30870f77578503bae6eea17ad1d0881d91
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="configure-accounts-payable"></a><span data-ttu-id="b21cf-104">Ostoreskontran määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b21cf-104">Configure Accounts payable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b21cf-105">Tässä artikkelissa kuvataan sivut, joiden avulla määritetään perus- ja valinnaiset toiminnot Microsoft Dynamics 365 for Finance and Operationsin ostoreskontrassa.</span><span class="sxs-lookup"><span data-stu-id="b21cf-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b21cf-106">Artikkelissa kerrotaan myös ennen ostoreskontran määrittämisen aloittamista suoritettavat asetusvaiheet.</span><span class="sxs-lookup"><span data-stu-id="b21cf-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="b21cf-107">Ostoreskontra-määrityksen edellytykset</span><span class="sxs-lookup"><span data-stu-id="b21cf-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="b21cf-108">Ennen ostoreskontran määrittämäistä, seuraavat asetukset on määritettävä:</span><span class="sxs-lookup"><span data-stu-id="b21cf-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="b21cf-109">Kirjanpito:</span><span class="sxs-lookup"><span data-stu-id="b21cf-109">In General ledger:</span></span>
    -   <span data-ttu-id="b21cf-110">Jos aiot käyttää maksukirjauskansioita, ne on ensin määritettävä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="b21cf-111">Jos aiot suorittaa valuuttakurssioikaisuja, määritä valuuttakoodit Valuutat-sivulla, vaihtokurssin tyypit Vaihtokurssin tyypit -sivulla ja valuutan vaihtokurssit Valuutan vaihtokurssit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b21cf-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="b21cf-112">Määritä Maksuliikenteen hallinta -kohdassa pankkitilit, joita käytetään maksutapojen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="b21cf-113">Ostoreskontra-asetusten sivut</span><span class="sxs-lookup"><span data-stu-id="b21cf-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="b21cf-114">Voit määrittää seuraavilla sivuilla ostoreskontran perustoiminnot kullekin yritykselle.</span><span class="sxs-lookup"><span data-stu-id="b21cf-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="b21cf-115">Sivut mainitaan suositeltavassa määritysjärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="b21cf-116">Voit helpottaa määritysprosessia luomalla ensimmäisistä tietueista malleja.</span><span class="sxs-lookup"><span data-stu-id="b21cf-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="b21cf-117">Mallissa arvot yleensä annetaan useisiin sellaisiin kenttiin, joiden ominaisuuksia organisaatio haluaa käyttää tietyn toimittajatyypin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="b21cf-118">Määritä Maksuehdot-sivulla maksuehdot, jotka haluat määrittää myyntitilauksiin, ostotilauksiin, asiakkaisiin ja toimittajiin ja joiden mukaan laskujen eräpäivät määräytyvät.</span><span class="sxs-lookup"><span data-stu-id="b21cf-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="b21cf-119">Lisätietoja on ohjeaiheessa [Toimittajan toimitusmaksujen määrittäminen](tasks/define-vendor-payment-fees.md).</span><span class="sxs-lookup"><span data-stu-id="b21cf-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="b21cf-120">Luo ja ylläpidä Maksutapa - Toimittajat -sivulla tiedot tavoista, joilla organisaatio maksaa toimittajille.</span><span class="sxs-lookup"><span data-stu-id="b21cf-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="b21cf-121">Luo ja ylläpidä Toimittajaryhmät-sivulla toimittajaryhmiä, joilla on samat tärkeät kirjaus-, tilitys-, maksu-, raportointi- ja ennusteparametrit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="b21cf-122">Määritä Toimittajan kirjausprofiilit -sivulla kirjausprofiilit, jotka määrittävät, miten toimittajatapahtumat kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="b21cf-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="b21cf-123">Määritä Ostoreskontran parametrit -sivulla oletusasetukset, joita käytetään, jos tarkempaa asetusta ei ole määritetty, erilaisten toimintojen parametrit ja ostoreskontran erilaiset numerosarjat.</span><span class="sxs-lookup"><span data-stu-id="b21cf-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="b21cf-124">Määritä Lomakeasetukset-sivulla niiden erilaisten toimittajiin liittyvien asiakirjojen muoto, joilla organisaatio seuraa toimittajien vastaanottoja ja antaa syyt toimittajille maksettaville suorituksille.</span><span class="sxs-lookup"><span data-stu-id="b21cf-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="b21cf-125">Luo ja ylläpidä Toimittajat-sivulla toimittajatilejä sekä veroviranomaisia, joille organisaatio ilmoittaa arvonlisäveron.</span><span class="sxs-lookup"><span data-stu-id="b21cf-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="b21cf-126">Ostoreskontran valinnaiset asetussivut</span><span class="sxs-lookup"><span data-stu-id="b21cf-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="b21cf-127">Perustoimintojen lisäksi ostoreskontrassa voi määrittää muita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="b21cf-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="b21cf-128">Lisäasetusten sivut on järjestetty toiminnon mukaan.</span><span class="sxs-lookup"><span data-stu-id="b21cf-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="b21cf-129">**Käytännöt**</span><span class="sxs-lookup"><span data-stu-id="b21cf-129">**Policies**</span></span>
-   <span data-ttu-id="b21cf-130">Määritä Toimittajan laskukäytäntö -sivulla toimittajan laskukäytännöt.</span><span class="sxs-lookup"><span data-stu-id="b21cf-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="b21cf-131">**Laskun täsmäytys**</span><span class="sxs-lookup"><span data-stu-id="b21cf-131">**Invoice matching**</span></span>

-   <span data-ttu-id="b21cf-132">Määritä Laskusummien toleranssit -sivulla laskusummien toleranssit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="b21cf-133">Määriä Täsmäytyskäytäntö-sivulla kaksi- ja kolmisuuntaiset vastaavuuskäytännöt.</span><span class="sxs-lookup"><span data-stu-id="b21cf-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="b21cf-134">Määritä Hintatoleranssit-sivulla yksikköhintojen toleranssit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="b21cf-135">Määritä Nimikkeiden hintatoleranssiryhmät -sivulla nimikehintojen toleranssiryhmät.</span><span class="sxs-lookup"><span data-stu-id="b21cf-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="b21cf-136">Määritä Toimittajan hintatoleranssiryhmät -sivulla toimittajan hintojen toleranssiryhmät.</span><span class="sxs-lookup"><span data-stu-id="b21cf-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="b21cf-137">Määritä Kulutoleranssit-sivulla kulujen toleranssit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="b21cf-138">**Työnkulku**</span><span class="sxs-lookup"><span data-stu-id="b21cf-138">**Workflow**</span></span>

-   <span data-ttu-id="b21cf-139">Määritä Ostoreskontran työnkulut -sivulla kirjauskansioiden hyväksyntä- ja ostoehdotustyönkulkujen määritykset.</span><span class="sxs-lookup"><span data-stu-id="b21cf-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="b21cf-140">**Syyt**</span><span class="sxs-lookup"><span data-stu-id="b21cf-140">**Reasons**</span></span>

-   <span data-ttu-id="b21cf-141">Määritä syykoodit Toimittajan syyt -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b21cf-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="b21cf-142">**Kulut**</span><span class="sxs-lookup"><span data-stu-id="b21cf-142">**Charges**</span></span>

-   <span data-ttu-id="b21cf-143">Määritä Kulujen koodi -sivulla ostotilauksessa käytettyjen kulujen koodit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="b21cf-144">Luo ja ylläpidä Toimittajan kulujen ryhmä -sivulla toimittajien kulujen ryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="b21cf-145">Luo ja ylläpidä Nimikkeen kuluryhmät -sivulla nimikkeiden kuluryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="b21cf-146">Määritä Automaattiset kulut -sivulla tilauksiin automaattisesti määritettävät kulut.</span><span class="sxs-lookup"><span data-stu-id="b21cf-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="b21cf-147">**Lisänimikkeet**</span><span class="sxs-lookup"><span data-stu-id="b21cf-147">**Supplementary items**</span></span>

-   <span data-ttu-id="b21cf-148">Luo ja ylläpidä Täydennysnimikeryhmät - Toimittaja -sivulla toimittajien täydennysnimikeryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="b21cf-149">Luo ja ylläpidä Täydennysnimikeryhmät - Varasto -sivulla nimikkeiden täydennysnimikeryhmiä.</span><span class="sxs-lookup"><span data-stu-id="b21cf-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="b21cf-150">**Toimitukset**</span><span class="sxs-lookup"><span data-stu-id="b21cf-150">**Distribution**</span></span>

-   <span data-ttu-id="b21cf-151">Luo ja ylläpidä Toimitusehdot-sivullaehtoja, joiden mukaisesti nimike siirretään myyjältä ostajalle.</span><span class="sxs-lookup"><span data-stu-id="b21cf-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="b21cf-152">Luo ja ylläpidä Toimitustavat-sivulla kuljetustavat, joilla tilaus toimitetaan myyjältä ostajalle.</span><span class="sxs-lookup"><span data-stu-id="b21cf-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="b21cf-153">Luo ja ylläpidä Kohdekoodit-sivulla toimituskohteiden tunnuksia ja kuvauksia.</span><span class="sxs-lookup"><span data-stu-id="b21cf-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="b21cf-154">**Lomakkeet**</span><span class="sxs-lookup"><span data-stu-id="b21cf-154">**Forms**</span></span>

-   <span data-ttu-id="b21cf-155">Luo Lomakehuomautukset-sivulla eri sivulla näkyvä vakioteksti.</span><span class="sxs-lookup"><span data-stu-id="b21cf-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="b21cf-156">Määritä Lomakkeen lajitteluparametrit -sivulla ehdotusten, vastaanottoluetteloiden, pakkausluetteloiden ja laskujen lajittelujärjestys.</span><span class="sxs-lookup"><span data-stu-id="b21cf-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="b21cf-157">Määritä Tulostuksenhallinnan asetukset -sivulla alkuperäisten ja kopioitujen sivujen tulostuksenhallinnan tiedot.</span><span class="sxs-lookup"><span data-stu-id="b21cf-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="b21cf-158">**Maksut**</span><span class="sxs-lookup"><span data-stu-id="b21cf-158">**Payments**</span></span>

-   <span data-ttu-id="b21cf-159">Määritä käteisalennusten saantiehdot ja niitä Käteisalennukset-sivulla.</span><span class="sxs-lookup"><span data-stu-id="b21cf-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="b21cf-160">Käteisalennuskoodit liitetään toimittajiin ja niitä käytetään ostotilauksissa.</span><span class="sxs-lookup"><span data-stu-id="b21cf-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="b21cf-161">Määritä Maksusuunnitelmat-sivulla maksusuunnitelmat, joilla hallitaan toimittajille maksettavia maksuerämaksuja.</span><span class="sxs-lookup"><span data-stu-id="b21cf-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="b21cf-162">Määritä Maksupäivät-sivulla eräpäivien laskennassa käytettävät maksupäivät ja määritä maksupäivät viikon tai kuukauden tietylle päivälle.</span><span class="sxs-lookup"><span data-stu-id="b21cf-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="b21cf-163">Luo ja ylläpidä Toimitusmaksu-sivulla toimittajiin liittyviä toimitusmaksuja.</span><span class="sxs-lookup"><span data-stu-id="b21cf-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="b21cf-164">Luo ja ylläpidä Maksuohje-sivulla maksuohjeita.</span><span class="sxs-lookup"><span data-stu-id="b21cf-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="b21cf-165">**Tilastotiedot**</span><span class="sxs-lookup"><span data-stu-id="b21cf-165">**Statistics**</span></span>

-   <span data-ttu-id="b21cf-166">Määritä Erääntymiskausien määritykset -sivulla käyttäjän määrittämiä välejä toimittajatilien erääntymisjakauman analysointia varten.</span><span class="sxs-lookup"><span data-stu-id="b21cf-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="b21cf-167">Luo Toimiala-sivulla toimittajille määritettäviä toimialakoodeja.</span><span class="sxs-lookup"><span data-stu-id="b21cf-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="b21cf-168">**Vero 1099**</span><span class="sxs-lookup"><span data-stu-id="b21cf-168">**Tax 1099**</span></span>

-   <span data-ttu-id="b21cf-169">Vahvista ja päivitä **1099-kentät** -sivulla vähimmäissummat, jotka on ilmoitettava Yhdysvaltain veroviranomaiselle (IRS) uusimpien IRS-vaatimusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="b21cf-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="b21cf-170">**Muiden moduulien valinnaiset asetukset**</span><span class="sxs-lookup"><span data-stu-id="b21cf-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="b21cf-171">**Organisaation hallinto**</span><span class="sxs-lookup"><span data-stu-id="b21cf-171">**Organization administration**</span></span>

-   <span data-ttu-id="b21cf-172">Määritä Numerosarjat-sivulla laskunumeroiden numerosarjaryhmät.</span><span class="sxs-lookup"><span data-stu-id="b21cf-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="b21cf-173">Määritä osoitetiedot seuraavilla sivuilla:</span><span class="sxs-lookup"><span data-stu-id="b21cf-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="b21cf-174">Osoitemääritys</span><span class="sxs-lookup"><span data-stu-id="b21cf-174">Address setup</span></span>
    -   <span data-ttu-id="b21cf-175">NAF-koodit</span><span class="sxs-lookup"><span data-stu-id="b21cf-175">NAF codes</span></span>
    -   <span data-ttu-id="b21cf-176">Tuo postinumerot</span><span class="sxs-lookup"><span data-stu-id="b21cf-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="b21cf-177">**Kirjanpito**</span><span class="sxs-lookup"><span data-stu-id="b21cf-177">**General ledger**</span></span>

-   <span data-ttu-id="b21cf-178">Määritä taloushallinnon dimensiot Taloushallinnon dimensiot -sivulla.</span><span class="sxs-lookup"><span data-stu-id="b21cf-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="b21cf-179">Määritä verotiedot seuraavilla sivulla:</span><span class="sxs-lookup"><span data-stu-id="b21cf-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="b21cf-180">Arvonlisäverokoodit</span><span class="sxs-lookup"><span data-stu-id="b21cf-180">Sales tax codes</span></span>
    -   <span data-ttu-id="b21cf-181">Arvonlisäveroryhmät</span><span class="sxs-lookup"><span data-stu-id="b21cf-181">Sales tax groups</span></span>
    -   <span data-ttu-id="b21cf-182">Nimikkeiden arvonlisäveroryhmät</span><span class="sxs-lookup"><span data-stu-id="b21cf-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="b21cf-183">Tiliryhmä</span><span class="sxs-lookup"><span data-stu-id="b21cf-183">Account group</span></span>
    -   <span data-ttu-id="b21cf-184">Verottomuuskoodit</span><span class="sxs-lookup"><span data-stu-id="b21cf-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="b21cf-185">Arvonlisäveroviranomaiset</span><span class="sxs-lookup"><span data-stu-id="b21cf-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="b21cf-186">Alv-viranomaiset</span><span class="sxs-lookup"><span data-stu-id="b21cf-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="b21cf-187">Arvonlisäveron tilityskaudet</span><span class="sxs-lookup"><span data-stu-id="b21cf-187">Sales tax settlement periods</span></span>

<span data-ttu-id="b21cf-188">**Maksuliikenteen hallinta**</span><span class="sxs-lookup"><span data-stu-id="b21cf-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="b21cf-189">Määritä Maksun tarkoituskoodit -sivulla keskuspankin maksun tarkoituskoodit.</span><span class="sxs-lookup"><span data-stu-id="b21cf-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






