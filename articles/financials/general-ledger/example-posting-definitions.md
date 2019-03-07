---
title: Kirjausmääritykset
description: Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten kirjausmäärityksiä käytetään ostotilausten varauksiin ja budjettivarauksiin.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5fb08a86639e9a9a79dca5fc1200e73e5870432
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310251"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="84013-103">Kirjausmääritysten esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="84013-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84013-104">Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten kirjausmäärityksiä käytetään ostotilausten varauksiin ja budjettivarauksiin.</span><span class="sxs-lookup"><span data-stu-id="84013-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="84013-105">Tutustu kirjausmäärityksiin ja tapahtuman kirjausmäärityksiin ennen tämän aiheen lukemista.</span><span class="sxs-lookup"><span data-stu-id="84013-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="84013-106">Tietoja on aiheessa [Kirjausmääritykset](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="84013-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="84013-107">Seuraavat esimerkit voidaan määrittää **Kirjausmääritykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="84013-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="84013-108">Kussakin esimerkissä on nämä skenaariot:</span><span class="sxs-lookup"><span data-stu-id="84013-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="84013-109">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="84013-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="84013-110">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="84013-111">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="84013-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="84013-112">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="84013-113">Kun kirjausmäärityksen **Vastaavuusehdot**-ruudun tilien ja dimensioarvojen sekä tapahtuman tilien ja dimensioarvojen välillä on vastaavuus, kirjanpitomerkinnät luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudun perusteella.</span><span class="sxs-lookup"><span data-stu-id="84013-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="84013-114">Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="84013-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="84013-115">Kun kirjausmääritys on liitetty tapahtumatyyppiin ja **Kirjanpitoparametrit**-sivulla on valittu **Käytä kirjausmäärityksiä** -vaihtoehto, kaikki valitun tapahtumatyypin tapahtumien on käytettävä kirjausmäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="84013-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="84013-116">Esimerkki: Ostotilauksen varaukset</span><span class="sxs-lookup"><span data-stu-id="84013-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="84013-117">Kun otat varauksen käsittelyyn käyttöön valitsemalla **Ota varausprosessi käyttöön** -vaihtoehdon **Kirjanpitoparametrit**-sivulta, varaukset on kirjattava kirjanpitoon kirjausmääritysten avulla kaikilla tileillä, joilla varaus on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="84013-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="84013-118">Useimmissa tapauksissa taseessa varataan kaikki kulutilit.</span><span class="sxs-lookup"><span data-stu-id="84013-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="84013-119">Varausten kirjausmääritykset määritetään **Osto**-moduulissa **Kirjausmääritykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="84013-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="84013-120">Sen jälkeen voit valita **Tapahtuman kirjausmääritykset**-sivun **Osto**-alueesta **Ostotilaus**-tapahtumatyypin, jotta voit liittää kirjausmäärityksen ostotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="84013-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="84013-121">Kaikkien ostotilauksen varausten tositetapahtumien (eli debet- ja kredit-puolen) on täsmättävä tositteen kussakin yksilöllisessä dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="84013-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="84013-122">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="84013-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="84013-123">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-123">Account structure</span></span>       | <span data-ttu-id="84013-124">Vastaava tilinumero</span><span class="sxs-lookup"><span data-stu-id="84013-124">Match account number</span></span> | <span data-ttu-id="84013-125">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="84013-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="84013-126">Tilirakenne – Tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="84013-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="84013-127">1</span><span class="sxs-lookup"><span data-stu-id="84013-127">1</span></span>        |

<span data-ttu-id="84013-128"><em>\**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.</span><span class="sxs-lookup"><span data-stu-id="84013-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="84013-129">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="84013-130">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-130">Account structure</span></span> | <span data-ttu-id="84013-131">Luotu tilinumero</span><span class="sxs-lookup"><span data-stu-id="84013-131">Generated account number</span></span>                    | <span data-ttu-id="84013-132">Luotu debet/kredit</span><span class="sxs-lookup"><span data-stu-id="84013-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="84013-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="84013-133">Balance</span></span>           | <span data-ttu-id="84013-134">300143 - -(Varaustili)</span><span class="sxs-lookup"><span data-stu-id="84013-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="84013-135">Sama</span><span class="sxs-lookup"><span data-stu-id="84013-135">Same</span></span>                   |
| <span data-ttu-id="84013-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="84013-136">Balance</span></span>           | <span data-ttu-id="84013-137">300144 - -(Varaus varaustilille)</span><span class="sxs-lookup"><span data-stu-id="84013-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="84013-138">Tasapainottelu</span><span class="sxs-lookup"><span data-stu-id="84013-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="84013-139">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="84013-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="84013-140">Tilit ja dimensioarvot tulevat joko ostotilausriville syötetyistä kirjanpidollisista jaoista tai tileistä ja dimensioista, jotka luodaan automaattisesti toimittajien, nimikkeiden, kategorioiden ja dimensiomallien perusteella.</span><span class="sxs-lookup"><span data-stu-id="84013-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="84013-141">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="84013-141">Account + dimensions</span></span>           | <span data-ttu-id="84013-142">Veloitus</span><span class="sxs-lookup"><span data-stu-id="84013-142">Debit</span></span>  | <span data-ttu-id="84013-143">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="84013-143">Credit</span></span> | <span data-ttu-id="84013-144">Kommentti</span><span class="sxs-lookup"><span data-stu-id="84013-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="84013-145">606400-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="84013-146">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="84013-147">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="84013-148">Varausten kirjaamiseksi luodaan kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="84013-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="84013-149">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="84013-149">Account + dimensions</span></span>           | <span data-ttu-id="84013-150">Veloitus</span><span class="sxs-lookup"><span data-stu-id="84013-150">Debit</span></span>  | <span data-ttu-id="84013-151">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="84013-151">Credit</span></span> | <span data-ttu-id="84013-152">Kommentti</span><span class="sxs-lookup"><span data-stu-id="84013-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="84013-153">300143-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="84013-154">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-154">250.00</span></span> |        |         |
| <span data-ttu-id="84013-155">300144-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="84013-156">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-156">250.00</span></span> |         |

<span data-ttu-id="84013-157">Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="84013-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="84013-158">Siten kun 606500-OU\_1-OU\_3566-Koulutus arvioidaan, kirjaukset luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudussa määritellyille tileille.</span><span class="sxs-lookup"><span data-stu-id="84013-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="84013-159">Esimerkki: Budjettivaraukset</span><span class="sxs-lookup"><span data-stu-id="84013-159">Example: Budget appropriations</span></span>
<span data-ttu-id="84013-160">Kun otat budjettivarauksen käyttöön valitsemalla **Kirjanpitoparametrit**-sivulta **Ota käyttöön budjettivaraus** -vaihtoehdon, budjettitapahtumat on kirjattava kirjanpitoon käyttämällä kirjausmäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="84013-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="84013-161">Jos budjetin hallinnan konfiguraatio on aktiivinen ja otettu käyttöön, kirjausmäärityksillä ja tapahtumakirjauksen määrityksillä voidaan tukea varausten, tarkistusten, siirtojen, projektien, käyttöomaisuuden ja tarjonta- sekä kysyntäennusteiden tapahtumien kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="84013-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="84013-162">Jos haluat määrittää kirjausmäärityksen budjettitapahtumille, joiden budjettityyppi on **Alkuperäinen budjetti** ja joissa on varaukset käytössä, valitse **Kirjausmääritykset**-sivulta **Budjetti**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="84013-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="84013-163">Tämän jälkeen voit **Tapahtuman kirjausmääritykset** -sivun **Budjetti**-alueessa budjettikoodien avulla liittää kirjausmäärityksen budjettitapahtumiin, joiden budjettityyppi on **Alkuperäinen budjetti**.</span><span class="sxs-lookup"><span data-stu-id="84013-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="84013-164">Kun budjettivarauksia ja kirjausmäärityksiä otetaan käyttöön, budjettitapahtumat kirjataan budjetin hallintaan ja kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="84013-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="84013-165">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="84013-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="84013-166">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-166">Account structure</span></span>       | <span data-ttu-id="84013-167">Vastaava tilinumero</span><span class="sxs-lookup"><span data-stu-id="84013-167">Match account number</span></span> | <span data-ttu-id="84013-168">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="84013-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="84013-169">Tilirakenne – Tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="84013-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="84013-170">1</span><span class="sxs-lookup"><span data-stu-id="84013-170">1</span></span>        |

<span data-ttu-id="84013-171"><em>\**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.</span><span class="sxs-lookup"><span data-stu-id="84013-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="84013-172">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="84013-173">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-173">Account structure</span></span> | <span data-ttu-id="84013-174">Luotu tilinumero</span><span class="sxs-lookup"><span data-stu-id="84013-174">Generated account number</span></span>              | <span data-ttu-id="84013-175">Luotu debet/kredit</span><span class="sxs-lookup"><span data-stu-id="84013-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="84013-176">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-176">Account structure</span></span> | <span data-ttu-id="84013-177">300145 - -(Arvioidun tuoton tili)</span><span class="sxs-lookup"><span data-stu-id="84013-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="84013-178">Sama</span><span class="sxs-lookup"><span data-stu-id="84013-178">Same</span></span>                   |
| <span data-ttu-id="84013-179">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="84013-179">Account structure</span></span> | <span data-ttu-id="84013-180">300146 - -(Tilinpäätössiirtojen tili)</span><span class="sxs-lookup"><span data-stu-id="84013-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="84013-181">Tasapainottelu</span><span class="sxs-lookup"><span data-stu-id="84013-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="84013-182">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="84013-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="84013-183">Voit lisätä budjettitiliviennin tilit, dimensioarvot ja summat **Budjettitapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="84013-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="84013-184">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="84013-184">Account + dimensions</span></span>           | <span data-ttu-id="84013-185">Veloitus</span><span class="sxs-lookup"><span data-stu-id="84013-185">Debit</span></span> | <span data-ttu-id="84013-186">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="84013-186">Credit</span></span> | <span data-ttu-id="84013-187">Kommentti</span><span class="sxs-lookup"><span data-stu-id="84013-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="84013-188">606400-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="84013-189">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="84013-190">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="84013-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="84013-191">Kirjanpitotapahtumat luodaan, jotta alkuperäinen budjetti voidaan kirjata kuhunkin dimensioon.</span><span class="sxs-lookup"><span data-stu-id="84013-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="84013-192">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="84013-192">Account + dimensions</span></span>           | <span data-ttu-id="84013-193">Veloitus</span><span class="sxs-lookup"><span data-stu-id="84013-193">Debit</span></span>  | <span data-ttu-id="84013-194">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="84013-194">Credit</span></span> | <span data-ttu-id="84013-195">Kommentti</span><span class="sxs-lookup"><span data-stu-id="84013-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="84013-196">300145-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="84013-197">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-197">250.00</span></span> |         |
| <span data-ttu-id="84013-198">300146-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="84013-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="84013-199">250,00</span><span class="sxs-lookup"><span data-stu-id="84013-199">250.00</span></span> |        |         |

<span data-ttu-id="84013-200">Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="84013-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="84013-201">Niinpä kun 606400-OU\_1-OU\_3566-Koulutus arvioidaan, kirjanpitotapahtumat luodaan.</span><span class="sxs-lookup"><span data-stu-id="84013-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





