---
title: Eliminointisäännöt
description: Tässä artikkelissa on tietoja eliminointisäännöistä ja eliminointien eri vaihtoehdoista.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0736d63c9a582948d197dc267f9941cbbd3e3c6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "333090"
---
# <a name="elimination-rules"></a><span data-ttu-id="d9b62-103">Eliminointisäännöt</span><span class="sxs-lookup"><span data-stu-id="d9b62-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9b62-104">Tässä artikkelissa on tietoja eliminointisäännöistä ja eliminointien eri vaihtoehdoista.</span><span class="sxs-lookup"><span data-stu-id="d9b62-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="d9b62-105">Eliminointitapahtumia tarvitaan, kun emoyritys suorittaa liiketoimia vähintään yhden tytäryhtiön kanssa ja käyttää konsolidoituja raportteja.</span><span class="sxs-lookup"><span data-stu-id="d9b62-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="d9b62-106">Konsolidoiduissa raporteissa voi olla vain konsolidointiorganisaation ja kyseisten organisaatioiden muiden ulkopuolisten entiteettien välisiä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d9b62-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="d9b62-107">Tämän vuoksi samaan organisaatioon kuuluvien yritysten välillä tapahtuvat tapahtumat on poistettava tai eliminoitava kirjanpidosta, jotta ne eivät näy raporteissa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="d9b62-108">Eliminoinnin voi tehdä useilla eri tavoilla.</span><span class="sxs-lookup"><span data-stu-id="d9b62-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="d9b62-109">Eliminointisääntö voidaan luoda ja käsitellä konsolidointi- tai eliminointiyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="d9b62-110">Talousraportoinnin avulla voidaan näyttää tietyn rivin tai sarakkeen eliminoinnin tilit ja dimensiot.</span><span class="sxs-lookup"><span data-stu-id="d9b62-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="d9b62-111">Eliminointien seuraamisessa käytettävien manuaalisten tapahtumakirjausten kirjaamisessa voidaan käyttää erillistä yritystä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="d9b62-112">Tässä ohjeaiheessa keskitytään konsolidointi- tai eliminointiyrityksessä käsiteltäviin eliminointisääntöihin.</span><span class="sxs-lookup"><span data-stu-id="d9b62-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="d9b62-113">Määrittämällä eliminointisääntöjä voit luoda eliminointitapahtumia yritykseen, joka on määritetty eliminointien kohdeyritykseksi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="d9b62-114">Kohdetyritys tunnetaan nimellä eliminointiyritys.</span><span class="sxs-lookup"><span data-stu-id="d9b62-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="d9b62-115">Eliminointikirjauskansioita voi muodostaa joko konsolidoinnin aikana tai eliminointikirjauskansion ehdotuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="d9b62-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="d9b62-116">Tutustu seuraaviin termeihin, ennen kuin määrität eliminointisääntöjä:</span><span class="sxs-lookup"><span data-stu-id="d9b62-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="d9b62-117">**Lähdeyritys** – Yritys, johon eliminoitavat summat kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d9b62-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="d9b62-118">**Kohdeyritys** – Yritys, johon eliminointisäännöt kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d9b62-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="d9b62-119">**Eliminoinnin kohdeyritys** – Yritys, joka määritetään eliminointien kohdeyritykseksi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="d9b62-120">**Konsolidoitu yritys** – Yritys, joka luodaan ilmoittamaan taloudelliset tulokset yritysten ryhmälle.</span><span class="sxs-lookup"><span data-stu-id="d9b62-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="d9b62-121">Yritysten taloushallinnon tiedot konsolidoidaan tähän yritykseen, ja raportti luodaan yhdistettyjen tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="d9b62-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="d9b62-122">Seuraavassa taulukossa on esitetty tapahtumatyypit, jotka on ehkä eliminoitava.</span><span class="sxs-lookup"><span data-stu-id="d9b62-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9b62-123">Tapahtumatyyppi</span><span class="sxs-lookup"><span data-stu-id="d9b62-123">Transaction type</span></span></th>
<th><span data-ttu-id="d9b62-124">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d9b62-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9b62-125">Myyntitilausten käsittely ja laskutus (keskitetty käsittely)</span><span class="sxs-lookup"><span data-stu-id="d9b62-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="d9b62-126">Myyt tuotteen asiakkaalle toisen organisaatiosi yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-127">Myyntitilauksen käsittely (konserniyritysten välinen / yrityksen sisäinen) ja laskutus</span><span class="sxs-lookup"><span data-stu-id="d9b62-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="d9b62-128">Myyt tuotteet yritysten välillä organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b62-129">Ostotilaukset (keskitetty käsittely)</span><span class="sxs-lookup"><span data-stu-id="d9b62-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="d9b62-130">Ostat varastoa, toimituksia, palveluita, käyttöomaisuuseriä ja muita tuotteita toimittajalta toisen organisaatiosi yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-131">Varastonhallinta (konserniyritysten välinen / yrityksen sisäinen)</span><span class="sxs-lookup"><span data-stu-id="d9b62-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9b62-132">Siirrät yhden yrityksen varaston toisen yrityksen käyttöomaisuuteen organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="d9b62-133">Siirrät yhden yrityksen varaston toisen yrityksen varastoon organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b62-134">Kuljetettavan varaston seuranta</span><span class="sxs-lookup"><span data-stu-id="d9b62-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="d9b62-135">Siirrät nimikkeitä varastojen välillä samassa yrityksessä mutta maantieteellisesti eri toimipaikoissa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-136">Ostoreskontran keskitetty laskujen käsittely</span><span class="sxs-lookup"><span data-stu-id="d9b62-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="d9b62-137">Tallennat laskun toisen organisaatiosi yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b62-138">Ostoreskontran keskitetty maksujen käsittely</span><span class="sxs-lookup"><span data-stu-id="d9b62-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="d9b62-139">Voit maksaa laskun toisen organisaatiosi yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-140">Kassanhallinta / rahasto (keskitetty käsittely)</span><span class="sxs-lookup"><span data-stu-id="d9b62-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9b62-141">Käsittelet maksetut verot, veronpalautukset, korkokulut, lainat, ennakot, osinkomaksut ja ennalta maksetut palkkiot tai provisiot.</span><span class="sxs-lookup"><span data-stu-id="d9b62-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="d9b62-142">Voit maksaa kulun toisen organisaatiosi yrityksen puolesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="d9b62-143">Lasku syötetään kohdeyrityksen kirjoihin, ja sinun on suoritettava yritysten välinen selvitys.</span><span class="sxs-lookup"><span data-stu-id="d9b62-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="d9b62-144">Esimerkiksi yksi yritys maksaa toisessa yrityksessä olevan työntekijän kuluraportin.</span><span class="sxs-lookup"><span data-stu-id="d9b62-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="d9b62-145">Tässä tapauksessa työntekijän kuluraportissa on kuluja, jotka liittyvät toiseen yritykseen.</span><span class="sxs-lookup"><span data-stu-id="d9b62-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="d9b62-146">Siirrät käteisvaroja yhdestä yrityksestä toiseen organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b62-147">Myyntireskontra (keskitetty käsittely)</span><span class="sxs-lookup"><span data-stu-id="d9b62-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="d9b62-148">Vastaanotat käteisvaroja toisen yrityksen myyntilaskua varten ja tallennat sekin kyseisen yrityksen pankkitilille.</span><span class="sxs-lookup"><span data-stu-id="d9b62-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-149">Palkanlaskenta (keskitetty käsittely, konserniyritysten välinen / yrityksen sisäinen)</span><span class="sxs-lookup"><span data-stu-id="d9b62-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="d9b62-150">Voit maksaa toisen yrityksen palkanlaskennan.</span><span class="sxs-lookup"><span data-stu-id="d9b62-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="d9b62-151">Yritys esimerkiksi maksaa omien työntekijöidensä palkkamenot, mutta veloittaa takaisin kyseisen palkka-ajon aikaisen työn, jonka työntekijä on tehnyt toisessa yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="d9b62-152">Jos työntekijä on työskennellyt puolipäiväisesti yritykselle A ja puolipäiväisesti yritykselle B ja edut jakautuvat koko palkan ajalle</span><span class="sxs-lookup"><span data-stu-id="d9b62-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="d9b62-153">Näissä tapauksissa työntekijän palkka sisältää palkan molemmilta yrityksiltä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="d9b62-154">Paitsi palkat myös palkkojen verot, edut, vähennykset ja siirtosaamiset kirjataan.</span><span class="sxs-lookup"><span data-stu-id="d9b62-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="d9b62-155">Siirrä työvoimaa yhdestä osastosta tai jaostosta toiseen.</span><span class="sxs-lookup"><span data-stu-id="d9b62-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9b62-156">Käyttöomaisuuserät (konserniyritysten välinen / yrityksen sisäinen)</span><span class="sxs-lookup"><span data-stu-id="d9b62-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="d9b62-157">Siirrät käyttöomaisuutta toisen yrityksen käyttöomaisuuteen tai varastoon.</span><span class="sxs-lookup"><span data-stu-id="d9b62-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9b62-158">Kohdistukset (konserniyritysten välinen / yrityksen sisäinen)</span><span class="sxs-lookup"><span data-stu-id="d9b62-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="d9b62-159">Käsittelet yrityksen kohdistukset.</span><span class="sxs-lookup"><span data-stu-id="d9b62-159">You process corporate allocations.</span></span> <span data-ttu-id="d9b62-160">Kohdistukset ovat mihin tahansa kohdistettuun tiliin kohdistuvia toimia alkuperäisestä moduulista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="d9b62-161">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="d9b62-161">Example</span></span>
<span data-ttu-id="d9b62-162">Yrityksesi nimeltä yritys A myy pienoisohjelmia toiselle organisaatiosi yritykselle nimeltä yritys B. Seuraava esimerkki kuvaa, kuinka kahden yrityksen väliset tapahtumat on ehkä eliminoitava:</span><span class="sxs-lookup"><span data-stu-id="d9b62-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="d9b62-163">Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 10,00 euroa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="d9b62-164">Yritys A myy 10,00 euroa maksavan pienoisohjelmanyritykselle B hintaan 10,00 euroa ja laskuttaa 2,00 euroa todellisia toimituskuluja.</span><span class="sxs-lookup"><span data-stu-id="d9b62-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="d9b62-165">Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 15,00 euroa ja tunnustaa myynnin katteen.</span><span class="sxs-lookup"><span data-stu-id="d9b62-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="d9b62-166">Yritys A myy 10,00 euroa maksavan pienoisohjelman yritykselle B hintaan 15,00 euroa ja tunnustaa puolet myynnin katteesta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="d9b62-167">Yritys B tunnustaa toisen puoliskon myynnin marginaalista.</span><span class="sxs-lookup"><span data-stu-id="d9b62-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="d9b62-168">Tämän vuoksi tuotto jaetaan.</span><span class="sxs-lookup"><span data-stu-id="d9b62-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="d9b62-169">Jaettu tuotto tarjoaa mahdollisuuden tilata toiselta organisaation yritykseltä ulkoisen organisaation sijasta.</span><span class="sxs-lookup"><span data-stu-id="d9b62-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="d9b62-170">Kaikki nämä tapahtumat luovat konsernin sisäisiä tapahtumia, jotka kirjataan erääntymiskohteen ja -lähteen tileihin.</span><span class="sxs-lookup"><span data-stu-id="d9b62-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="d9b62-171">Näissä tapahtumissa voi olla myös summien korotuksia ja alennuksia tilanteissa, joissa konserniyritysten välisen myynnin ja myytyjen tuotteiden kustannusten summat eivät täsmää.</span><span class="sxs-lookup"><span data-stu-id="d9b62-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="d9b62-172">Määritä eliminointisääntöjä</span><span class="sxs-lookup"><span data-stu-id="d9b62-172">Set up elimination rules</span></span>
<span data-ttu-id="d9b62-173">Kun Microsoft Dynamics 365 for Finance and Operationsissa määritetään eliminointisääntöjä, on suositeltavaa luoda taloushallinnon dimensio erityisesti eliminointitarkoituksia varten.</span><span class="sxs-lookup"><span data-stu-id="d9b62-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="d9b62-174">Useimmat asiakkaat nimeävät sen Kaupankäynnin kumppaniksi tai jotain vastaavaa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="d9b62-175">Jos et halua käyttää taloushallinnon dimensiota, muista varmistaa, että sinulla on päätilit, jotka koskevat vain konserniyritysten välisiä tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="d9b62-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="d9b62-176">Konsolidoinnit-moduulin Asetukset-alueelta löytyy eliminoinnin asetukset.</span><span class="sxs-lookup"><span data-stu-id="d9b62-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="d9b62-177">Kun kirjoitat säännön kuvauksen, sinun on valittava yritys, johon eliminoinnin kirjauskansio kirjaa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="d9b62-178">Tämän tulisi olla yritys, jonka asetuksissa on valittu **Käytetään taloushallinnon eliminointiprosessissa**.</span><span class="sxs-lookup"><span data-stu-id="d9b62-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="d9b62-179">Voit määrittää päivämäärän, jolloin eliminointisääntö tulee voimaan ja (tarvittaessa) milloin se vanhentuu.</span><span class="sxs-lookup"><span data-stu-id="d9b62-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="d9b62-180">On määritettävä **Aktiivinen** arvoksi **Kyllä**, jos haluat sen olevan saatavilla eliminoinnin ehdotusprosessissa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="d9b62-181">Valitse kirjauskansio, jonka tyyppi on **Eliminointi**.</span><span class="sxs-lookup"><span data-stu-id="d9b62-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="d9b62-182">Kun olet määritellyt perusteet, voit määrittää todelliset käsittelysäännöt valitsemalla **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="d9b62-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="d9b62-183">Vaihtoehtoja on kaksi eliminoinneissa: nettomuutossumman eliminointi tai kiinteän summan määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="d9b62-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="d9b62-184">Valitse lähdetili.</span><span class="sxs-lookup"><span data-stu-id="d9b62-184">Select your source account.</span></span> <span data-ttu-id="d9b62-185">Voit käyttää tähteä (\*) yleismerkkinä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="d9b62-186">Esimerkiksi 1\* valitsisi kaikki 1-alkuiset tilit kohdistuksen tietolähteenä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="d9b62-187">Kun olet valinnut lähdetilisi **Tilin määrittely** määrittää käytettävän tilin kohdeyrityksestä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="d9b62-188">Valitse **Lähde**, jos haluat käyttää samaa päätiliä, joka on määritelty **Lähde**-tilissä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="d9b62-189">Jos valitset **Käyttäjän määrittämä**, sinun on määritettävä kohdetili.</span><span class="sxs-lookup"><span data-stu-id="d9b62-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="d9b62-190">Dimension määrittely toimii samalla tavalla.</span><span class="sxs-lookup"><span data-stu-id="d9b62-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="d9b62-191">Jos valitset **Lähde**, se käyttää kohdeyrityksessä samoja dimensioita kuin lähdeyrityksessä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="d9b62-192">Jos valitset **Käyttäjän määrittämä**, sinun täytyy määrittää kohdeyrityksen dimensiot valitsemalla **Kohdedimensiot**-valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="d9b62-193">Valitse lähdedimensiot ja taloushallinnon dimensiot ja eliminoinnin lähteenä käytettävät arvot.</span><span class="sxs-lookup"><span data-stu-id="d9b62-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="d9b62-194">Käsittele eliminointitapahtumia</span><span class="sxs-lookup"><span data-stu-id="d9b62-194">Process elimination transactions</span></span>
<span data-ttu-id="d9b62-195">On kaksi tapaa käsitellä eliminoinnin tapahtumia kokoa: konsolidoinnin online-prosessin aikana tai luomalla eliminoinnin kirjauskansio ja suorittamalla eliminoinnin ehdotusprosessi.</span><span class="sxs-lookup"><span data-stu-id="d9b62-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="d9b62-196">Tässä osassa keskitytään kirjauskansion luomiseen ja eliminointiprosessin suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="d9b62-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="d9b62-197">Valitse eliminointiyritykseksi määritellyssä yrityksessä **Eliminoinnin kirjauskansio** Konsolidoinnit-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="d9b62-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="d9b62-198">Kun olet valinnut kirjauskansion nimen, valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="d9b62-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="d9b62-199">Valitsemalla voit suorittaa ehdotuksen valitsemalla **Ehdotukset**-valikon ja sitten **Eliminointiehdotus**.</span><span class="sxs-lookup"><span data-stu-id="d9b62-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="d9b62-200">Valitse yritys, joka on koottujen tietojen lähde ja valitse sääntö, jota haluat käsitellä.</span><span class="sxs-lookup"><span data-stu-id="d9b62-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="d9b62-201">Anna aloituspäivämäärä käynnistääksesi eliminoinnin summien haun ja päättymispäivä eliminoinnin summien haun päivämäärävälin loppuun.</span><span class="sxs-lookup"><span data-stu-id="d9b62-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="d9b62-202">**Kirjanpidon kirjauspäivä** -kenttä on päivämäärä, jolloin eliminointikirjauskansio kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="d9b62-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="d9b62-203">Kun olet valinnut **OK**, voit tarkistaa määrät ja kirjata kirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="d9b62-203">After you click **OK**, you can review the amounts and post the journal.</span></span>



