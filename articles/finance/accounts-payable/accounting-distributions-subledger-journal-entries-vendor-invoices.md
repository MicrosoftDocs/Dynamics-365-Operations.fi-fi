---
title: Toimittajan laskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät
description: Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa. Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177615"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="7d967-104">Toimittajan laskujen kirjanpidolliset jaot ja alatason kirjauskansion merkinnät</span><span class="sxs-lookup"><span data-stu-id="7d967-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d967-105">Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa.</span><span class="sxs-lookup"><span data-stu-id="7d967-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="7d967-106">Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="7d967-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="7d967-107">Kirjanpidolliset jaot</span><span class="sxs-lookup"><span data-stu-id="7d967-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="7d967-108">Seuraavilla Toimittajan lasku -sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin ostotilauksen summalle.</span><span class="sxs-lookup"><span data-stu-id="7d967-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="7d967-109">**Jakosummat** – Tarkastele muokkaa yksittäisen rivin ja sen alatason rivien kirjanpidollisia jakoja, kuten veroja tai maksuja.</span><span class="sxs-lookup"><span data-stu-id="7d967-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="7d967-110">Voit tarkastella ja muokata alarivin kirjanpidollisia jakoja myös suoraan Arvonlisäverotapahtumat- tai Kulutapahtumat-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="7d967-111">Muokkaa toimittajan laskun otsikon summia, kuten kuluja tai valuutan pyöristyssummia.</span><span class="sxs-lookup"><span data-stu-id="7d967-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="7d967-112">Muokkaa toimittajalaskun rivisummia.</span><span class="sxs-lookup"><span data-stu-id="7d967-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="7d967-113">**Näytä jakaumat** – Näytä asiakirjan kaikkien rivien kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="7d967-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="7d967-114">Et voi muokata kirjanpidollisia jakoja tästä näkymästä.</span><span class="sxs-lookup"><span data-stu-id="7d967-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="7d967-115">Näytä otsikon ja rivien summat.</span><span class="sxs-lookup"><span data-stu-id="7d967-115">View header and line amounts.</span></span>

<span data-ttu-id="7d967-116">Jos toimittajalasku viittaa ostotilaukseen, voit jakaa ja muokata kirjanpidon jaot riveille, jotka sisältävät nimikkeen, joka ei ole varastossa.</span><span class="sxs-lookup"><span data-stu-id="7d967-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="7d967-117">Jos toimittajan laskurivi viittaa ostotilausriviin, voit poistaa kirjanpitojaon.</span><span class="sxs-lookup"><span data-stu-id="7d967-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="7d967-118">Et voi jakaa tai poistaa kulujen, verojen ja rivialennusten rivejä.</span><span class="sxs-lookup"><span data-stu-id="7d967-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="7d967-119">Voi muokata kirjanpitotiliä, mutta et voi muuttaa summia tai prosentteja.</span><span class="sxs-lookup"><span data-stu-id="7d967-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="7d967-120">Jos ylätason rivillä on nimike, joka ei ole varastossa, ja kirjanpidon jaot jaetaan, rivin alempi taso jaetaan automaattisesti vastaamaan ylätason rivin taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="7d967-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="7d967-121">Alirivin kirjanpidollisia jakoja ei voi lisäksi jakaa tai poistaa, mutta alirivin asetuksista riippuen, voit mahdollisesti muuttaa alirivin kirjanpidollisten jakojen kirjanpitotiliä.</span><span class="sxs-lookup"><span data-stu-id="7d967-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="7d967-122">Summien jakaminen</span><span class="sxs-lookup"><span data-stu-id="7d967-122">Distributing amounts</span></span>
<span data-ttu-id="7d967-123">Kun syötät toimittajan lasku, jokainen määrä jaetaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7d967-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7d967-124">Toimittajan laskun rivin tyyppi</span><span class="sxs-lookup"><span data-stu-id="7d967-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="7d967-125">Tärkeysjärjestys, joka määrittää, mistä päätili näkyy.</span><span class="sxs-lookup"><span data-stu-id="7d967-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="7d967-126">Tärkeysjärjestys, joka määrittää, mikä oletusarvoinen taloushallinnon dimensio tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7d967-127">Varastotuote</span><span class="sxs-lookup"><span data-stu-id="7d967-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-128">Kirjanpidollinen jako ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-129">Päätili-kenttä, kun Kirjaus-sivulla on valittu Tuotteen ostomeno.</span><span class="sxs-lookup"><span data-stu-id="7d967-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-130">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-131">Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-132">Hankintaluokka tai tuote, jota ei ole varastossa</span><span class="sxs-lookup"><span data-stu-id="7d967-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-133">Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-134">Päätili-kenttä, kun Kirjaus-sivulla on valittu Kulun ostomeno.</span><span class="sxs-lookup"><span data-stu-id="7d967-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-135">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-136">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="7d967-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="7d967-137">Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="7d967-138">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-139">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d967-140">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="7d967-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-141">Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-142">Jos Toimittajan lasku -lomakkeessa Tapahtumatyyppi-kentästä on valittu Hankinta, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankinta.</span><span class="sxs-lookup"><span data-stu-id="7d967-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="7d967-143">Jos Tapahtumatyyppi-kentästä on valittu Hankintaoikaisu, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankintaoikaisu.</span><span class="sxs-lookup"><span data-stu-id="7d967-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-144">Käytä ostotilausriville tilijakoa, jos laskun rivi viittaa ostotilauksen riviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-145">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-146">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-147">Toimittajalaskurivillä määritetty projekti</span><span class="sxs-lookup"><span data-stu-id="7d967-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-148">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-149">Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Saldo, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannus.</span><span class="sxs-lookup"><span data-stu-id="7d967-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="7d967-150">Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Tulos, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannukset - Nimike.</span><span class="sxs-lookup"><span data-stu-id="7d967-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-151">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d967-152">Rivialennus</span><span class="sxs-lookup"><span data-stu-id="7d967-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-153">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-154">Päätili-kenttä, kun Kirjaus-sivulta on valittu Alennus.</span><span class="sxs-lookup"><span data-stu-id="7d967-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="7d967-155">Jos alennuspäätiliä ei ole määritetty kirjausprofiilissa, kirjanpidon jako kokonaishinnalle tilauksen ostorivillä.</span><span class="sxs-lookup"><span data-stu-id="7d967-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-156">Jos laskurivi on viittaus ostotilausriviin, käytä kirjanpidon jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-157">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-158">Käytä toimittajan laskurivin taloushallinnon dimension arvoja.</span><span class="sxs-lookup"><span data-stu-id="7d967-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-159">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-160">Oston kulut, jotka on syötetty ostotilausrivin Hinta ja alennus -välilehteen</span><span class="sxs-lookup"><span data-stu-id="7d967-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-161">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-162">Ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="7d967-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-163">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-164">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d967-165">Rivin kulu</span><span class="sxs-lookup"><span data-stu-id="7d967-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-166">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-167">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="7d967-168">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Nimike, ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="7d967-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-169">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-170">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-171">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-172">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-173">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-174">Vero, seuraavalla ehdolla:</span><span class="sxs-lookup"><span data-stu-id="7d967-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="7d967-175">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehto valitaan Kirjanpitoparametrit-sivulta.</span><span class="sxs-lookup"><span data-stu-id="7d967-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="7d967-176">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="7d967-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-177">Kulun tai laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="7d967-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-178">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-179">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-180">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d967-181">Vero, seuraavilla ehdoilla:</span><span class="sxs-lookup"><span data-stu-id="7d967-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="7d967-182">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="7d967-183">Arvonlisäveroryhmän Käyttövero-kentän valinta poistetaan Arvonlisäveroryhmät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="7d967-184">Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="7d967-185">Jos verosummaa ei voi palauttaa, kokonaishinta tai kulun kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="7d967-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-186">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-187">Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-188">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-189">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-190">Vero, seuraavilla ehdoilla:</span><span class="sxs-lookup"><span data-stu-id="7d967-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="7d967-191">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="7d967-192">Arvonlisäveroryhmän Käyttövero-kenttä valitaan Arvonlisäveroryhmät-sivulta.</span><span class="sxs-lookup"><span data-stu-id="7d967-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="7d967-193">Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="7d967-194">Jos verosumma ei ole palautettavissa, Kirjanpidon kirjausryhmät -sivun Käyttöverokulu-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-195">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-196">Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-197">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-198">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7d967-199">Otsikkomaksu</span><span class="sxs-lookup"><span data-stu-id="7d967-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-200">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="7d967-201">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="7d967-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-202">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-203">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="7d967-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="7d967-204">Käytä taloushallinnon dimension oletusmallin arvoja toimittajan laskun otsikosta.</span><span class="sxs-lookup"><span data-stu-id="7d967-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="7d967-205">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-206">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7d967-207">Otsikkoalennus</span><span class="sxs-lookup"><span data-stu-id="7d967-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="7d967-208">Toimittajan laskun alennus -kirjaustyypin Päätili-kenttä Automaattisten tapahtumien tilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="7d967-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="7d967-209">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="7d967-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="7d967-210">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-211">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="7d967-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="7d967-212">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="7d967-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="7d967-213">Verojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="7d967-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="7d967-214">verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa.</span><span class="sxs-lookup"><span data-stu-id="7d967-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="7d967-215">Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista Toimittajan lasku -sivun tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="7d967-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="7d967-216">Näytä laskun summa.</span><span class="sxs-lookup"><span data-stu-id="7d967-216">View the invoice total.</span></span>
-   <span data-ttu-id="7d967-217">Näytä arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="7d967-217">View the sales tax.</span></span>
-   <span data-ttu-id="7d967-218">Näytä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="7d967-218">View the subledger journal.</span></span>
-   <span data-ttu-id="7d967-219">Näytä kirjanpidolliset jaot koko toimittajan laskulle.</span><span class="sxs-lookup"><span data-stu-id="7d967-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="7d967-220">Sijoita toimittajan lasku pitoon.</span><span class="sxs-lookup"><span data-stu-id="7d967-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="7d967-221">Kirjaa toimittajalasku.</span><span class="sxs-lookup"><span data-stu-id="7d967-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="7d967-222">Alareskontran kirjauskansiot toimittajalaskuille</span><span class="sxs-lookup"><span data-stu-id="7d967-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="7d967-223">Ennen kuin kirjaat toimittajalaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille.</span><span class="sxs-lookup"><span data-stu-id="7d967-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="7d967-224">Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="7d967-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="7d967-225">Jos alareskontran kirjaus on virheellinen esikatsellessa, et voi muokata sitä ennen kuin kirjaat toimittajatilauksen.</span><span class="sxs-lookup"><span data-stu-id="7d967-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="7d967-226">Sen sijaan sinun on muokattava kirjanpidollisia jakoja tai kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="7d967-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="7d967-227">Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit.</span><span class="sxs-lookup"><span data-stu-id="7d967-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="7d967-228">Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan käyttämällä kirjausprofiileja, kuten toimittajatili tai vero.</span><span class="sxs-lookup"><span data-stu-id="7d967-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





