---
title: Kirjausmääritysesimerkkejä
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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 301f15f1d7d8f0e10bbaf2546fcf727aff284624
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552299"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="74794-103">Kirjausmääritysten esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="74794-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74794-104">Tässä artikkelissa on esimerkkejä, jotka osoittavat, miten kirjausmäärityksiä käytetään ostotilausten varauksiin ja budjettivarauksiin.</span><span class="sxs-lookup"><span data-stu-id="74794-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="74794-105">Tutustu kirjausmäärityksiin ja tapahtuman kirjausmäärityksiin ennen tämän aiheen lukemista.</span><span class="sxs-lookup"><span data-stu-id="74794-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="74794-106">Tietoja on aiheessa [Kirjausmääritykset](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="74794-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="74794-107">Seuraavat esimerkit voidaan määrittää **Kirjausmääritykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74794-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="74794-108">Kussakin esimerkissä on nämä skenaariot:</span><span class="sxs-lookup"><span data-stu-id="74794-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="74794-109">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="74794-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="74794-110">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="74794-111">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="74794-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="74794-112">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="74794-113">Kun kirjausmäärityksen **Vastaavuusehdot**-ruudun tilien ja dimensioarvojen sekä tapahtuman tilien ja dimensioarvojen välillä on vastaavuus, kirjanpitomerkinnät luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudun perusteella.</span><span class="sxs-lookup"><span data-stu-id="74794-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="74794-114">Liitä kirjausmääritykset tapahtumatyyppeihin **Tapahtuman kirjausmääritykset** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="74794-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="74794-115">Kun kirjausmääritys on liitetty tapahtumatyyppiin ja **Kirjanpitoparametrit**-sivulla on valittu **Käytä kirjausmäärityksiä** -vaihtoehto, kaikki valitun tapahtumatyypin tapahtumien on käytettävä kirjausmäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="74794-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="74794-116">Esimerkki: Ostotilauksen varaukset</span><span class="sxs-lookup"><span data-stu-id="74794-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="74794-117">Kun otat varauksen käsittelyyn käyttöön valitsemalla **Ota varausprosessi käyttöön** -vaihtoehdon **Kirjanpitoparametrit**-sivulta, varaukset on kirjattava kirjanpitoon kirjausmääritysten avulla kaikilla tileillä, joilla varaus on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="74794-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="74794-118">Useimmissa tapauksissa taseessa varataan kaikki kulutilit.</span><span class="sxs-lookup"><span data-stu-id="74794-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="74794-119">Varausten kirjausmääritykset määritetään **Osto**-moduulissa **Kirjausmääritykset**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="74794-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="74794-120">Sen jälkeen voit valita **Tapahtuman kirjausmääritykset**-sivun **Osto**-alueesta **Ostotilaus**-tapahtumatyypin, jotta voit liittää kirjausmäärityksen ostotilauksiin.</span><span class="sxs-lookup"><span data-stu-id="74794-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="74794-121">Kaikkien ostotilauksen varausten tositetapahtumien (eli debet- ja kredit-puolen) on täsmättävä tositteen kussakin yksilöllisessä dimensiossa.</span><span class="sxs-lookup"><span data-stu-id="74794-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="74794-122">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="74794-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="74794-123">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-123">Account structure</span></span>       | <span data-ttu-id="74794-124">Vastaava tilinumero</span><span class="sxs-lookup"><span data-stu-id="74794-124">Match account number</span></span> | <span data-ttu-id="74794-125">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="74794-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="74794-126">Tilirakenne – Tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="74794-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="74794-127">1</span><span class="sxs-lookup"><span data-stu-id="74794-127">1</span></span>        |

<span data-ttu-id="74794-128"><em>\**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.</span><span class="sxs-lookup"><span data-stu-id="74794-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="74794-129">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="74794-130">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-130">Account structure</span></span> | <span data-ttu-id="74794-131">Luotu tilinumero</span><span class="sxs-lookup"><span data-stu-id="74794-131">Generated account number</span></span>                    | <span data-ttu-id="74794-132">Luotu debet/kredit</span><span class="sxs-lookup"><span data-stu-id="74794-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="74794-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="74794-133">Balance</span></span>           | <span data-ttu-id="74794-134">300143 - -(Varaustili)</span><span class="sxs-lookup"><span data-stu-id="74794-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="74794-135">Sama</span><span class="sxs-lookup"><span data-stu-id="74794-135">Same</span></span>                   |
| <span data-ttu-id="74794-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="74794-136">Balance</span></span>           | <span data-ttu-id="74794-137">300144 - -(Varaus varaustilille)</span><span class="sxs-lookup"><span data-stu-id="74794-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="74794-138">Tasapainottelu</span><span class="sxs-lookup"><span data-stu-id="74794-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="74794-139">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="74794-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="74794-140">Tilit ja dimensioarvot tulevat joko ostotilausriville syötetyistä kirjanpidollisista jaoista tai tileistä ja dimensioista, jotka luodaan automaattisesti toimittajien, nimikkeiden, kategorioiden ja dimensiomallien perusteella.</span><span class="sxs-lookup"><span data-stu-id="74794-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="74794-141">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="74794-141">Account + dimensions</span></span>           | <span data-ttu-id="74794-142">Veloitus</span><span class="sxs-lookup"><span data-stu-id="74794-142">Debit</span></span>  | <span data-ttu-id="74794-143">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="74794-143">Credit</span></span> | <span data-ttu-id="74794-144">Kommentti</span><span class="sxs-lookup"><span data-stu-id="74794-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="74794-145">606400-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="74794-146">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="74794-147">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="74794-148">Varausten kirjaamiseksi luodaan kirjanpitomerkinnät.</span><span class="sxs-lookup"><span data-stu-id="74794-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="74794-149">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="74794-149">Account + dimensions</span></span>           | <span data-ttu-id="74794-150">Veloitus</span><span class="sxs-lookup"><span data-stu-id="74794-150">Debit</span></span>  | <span data-ttu-id="74794-151">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="74794-151">Credit</span></span> | <span data-ttu-id="74794-152">Kommentti</span><span class="sxs-lookup"><span data-stu-id="74794-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="74794-153">300143-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="74794-154">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-154">250.00</span></span> |        |         |
| <span data-ttu-id="74794-155">300144-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="74794-156">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-156">250.00</span></span> |         |

<span data-ttu-id="74794-157">Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="74794-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="74794-158">Siten kun 606500-OU\_1-OU\_3566-Koulutus arvioidaan, kirjaukset luodaan kirjausmäärityksen **Luodut kirjaukset** -ruudussa määritellyille tileille.</span><span class="sxs-lookup"><span data-stu-id="74794-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="74794-159">Esimerkki: Budjettivaraukset</span><span class="sxs-lookup"><span data-stu-id="74794-159">Example: Budget appropriations</span></span>
<span data-ttu-id="74794-160">Kun otat budjettivarauksen käyttöön valitsemalla **Kirjanpitoparametrit**-sivulta **Ota käyttöön budjettivaraus** -vaihtoehdon, budjettitapahtumat on kirjattava kirjanpitoon käyttämällä kirjausmäärityksiä.</span><span class="sxs-lookup"><span data-stu-id="74794-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="74794-161">Jos budjetin hallinnan konfiguraatio on aktiivinen ja otettu käyttöön, kirjausmäärityksillä ja tapahtumakirjauksen määrityksillä voidaan tukea varausten, tarkistusten, siirtojen, projektien, käyttöomaisuuden ja tarjonta- sekä kysyntäennusteiden tapahtumien kirjaamista kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="74794-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="74794-162">Jos haluat määrittää kirjausmäärityksen budjettitapahtumille, joiden budjettityyppi on **Alkuperäinen budjetti** ja joissa on varaukset käytössä, valitse **Kirjausmääritykset**-sivulta **Budjetti**-moduuli.</span><span class="sxs-lookup"><span data-stu-id="74794-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="74794-163">Tämän jälkeen voit **Tapahtuman kirjausmääritykset** -sivun **Budjetti**-alueessa budjettikoodien avulla liittää kirjausmäärityksen budjettitapahtumiin, joiden budjettityyppi on **Alkuperäinen budjetti**.</span><span class="sxs-lookup"><span data-stu-id="74794-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="74794-164">Kun budjettivarauksia ja kirjausmäärityksiä otetaan käyttöön, budjettitapahtumat kirjataan budjetin hallintaan ja kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="74794-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="74794-165">Kirjausmääritys – Vastaavuusehdot</span><span class="sxs-lookup"><span data-stu-id="74794-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="74794-166">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-166">Account structure</span></span>       | <span data-ttu-id="74794-167">Vastaava tilinumero</span><span class="sxs-lookup"><span data-stu-id="74794-167">Match account number</span></span> | <span data-ttu-id="74794-168">Prioriteetti </span><span class="sxs-lookup"><span data-stu-id="74794-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="74794-169">Tilirakenne – Tuloslaskelma</span><span class="sxs-lookup"><span data-stu-id="74794-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="74794-170">1</span><span class="sxs-lookup"><span data-stu-id="74794-170">1</span></span>        |

<span data-ttu-id="74794-171"><em>\**Vastaava tilinumero</em> -kentän tyhjä arvo* tarkoittaa, että kaikki määritetyn tilirakenteen vastaavat tilit kuuluvat täsmäytyssääntöön.</span><span class="sxs-lookup"><span data-stu-id="74794-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="74794-172">Kirjausmääritys – Luodut merkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="74794-173">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-173">Account structure</span></span> | <span data-ttu-id="74794-174">Luotu tilinumero</span><span class="sxs-lookup"><span data-stu-id="74794-174">Generated account number</span></span>              | <span data-ttu-id="74794-175">Luotu debet/kredit</span><span class="sxs-lookup"><span data-stu-id="74794-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="74794-176">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-176">Account structure</span></span> | <span data-ttu-id="74794-177">300145 - -(Arvioidun tuoton tili)</span><span class="sxs-lookup"><span data-stu-id="74794-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="74794-178">Sama</span><span class="sxs-lookup"><span data-stu-id="74794-178">Same</span></span>                   |
| <span data-ttu-id="74794-179">Tilirakenne</span><span class="sxs-lookup"><span data-stu-id="74794-179">Account structure</span></span> | <span data-ttu-id="74794-180">300146 - -(Tilinpäätössiirtojen tili)</span><span class="sxs-lookup"><span data-stu-id="74794-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="74794-181">Tasapainottelu</span><span class="sxs-lookup"><span data-stu-id="74794-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="74794-182">Tapahtumat ja tilit, dimensioarvot ja määrät</span><span class="sxs-lookup"><span data-stu-id="74794-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="74794-183">Voit lisätä budjettitiliviennin tilit, dimensioarvot ja summat **Budjettitapahtuma**-sivulle.</span><span class="sxs-lookup"><span data-stu-id="74794-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="74794-184">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="74794-184">Account + dimensions</span></span>           | <span data-ttu-id="74794-185">Veloitus</span><span class="sxs-lookup"><span data-stu-id="74794-185">Debit</span></span> | <span data-ttu-id="74794-186">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="74794-186">Credit</span></span> | <span data-ttu-id="74794-187">Kommentti</span><span class="sxs-lookup"><span data-stu-id="74794-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="74794-188">606400-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="74794-189">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="74794-190">Kirjausmäärityksestä luodut kirjanpitomerkinnät</span><span class="sxs-lookup"><span data-stu-id="74794-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="74794-191">Kirjanpitotapahtumat luodaan, jotta alkuperäinen budjetti voidaan kirjata kuhunkin dimensioon.</span><span class="sxs-lookup"><span data-stu-id="74794-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="74794-192">Tili + dimensiot</span><span class="sxs-lookup"><span data-stu-id="74794-192">Account + dimensions</span></span>           | <span data-ttu-id="74794-193">Veloitus</span><span class="sxs-lookup"><span data-stu-id="74794-193">Debit</span></span>  | <span data-ttu-id="74794-194">Hyvitys</span><span class="sxs-lookup"><span data-stu-id="74794-194">Credit</span></span> | <span data-ttu-id="74794-195">Kommentti</span><span class="sxs-lookup"><span data-stu-id="74794-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="74794-196">300145-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="74794-197">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-197">250.00</span></span> |         |
| <span data-ttu-id="74794-198">300146-OU\_1-OU\_3566-Koulutus</span><span class="sxs-lookup"><span data-stu-id="74794-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="74794-199">250,00</span><span class="sxs-lookup"><span data-stu-id="74794-199">250.00</span></span> |        |         |

<span data-ttu-id="74794-200">Tässä esimerkissä kaikki Tilirakenne – Tuloslaskelma -skenaarioon kuuluvat tilit vastaavat kirjausmäärityksen ehtoja.</span><span class="sxs-lookup"><span data-stu-id="74794-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="74794-201">Niinpä kun 606400-OU\_1-OU\_3566-Koulutus arvioidaan, kirjanpitotapahtumat luodaan.</span><span class="sxs-lookup"><span data-stu-id="74794-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





