---
title: Toimittajan laskujen kirjanpidolliset jaot ja kirjauskansioviennit
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
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da15f27c7fef6367eacc83271419b633c0cbb245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012285"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a><span data-ttu-id="aa602-104">Toimittajan laskujen kirjanpidolliset jaot ja kirjauskansioviennit</span><span class="sxs-lookup"><span data-stu-id="aa602-104">Accounting distributions and journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa602-105">Kirjanpidon jakoja käytetään määrittämään, miten summa käsitellään, esimerkiksi miten kulu, vara, vero tai maksu käsitellään toimittajan laskussa.</span><span class="sxs-lookup"><span data-stu-id="aa602-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="aa602-106">Jokaisella määrällä, joka on huomioitava toimittajan laskun kirjauksen yhteydessä, on yksi tai useampi kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="aa602-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="aa602-107">Kirjanpidolliset jaot</span><span class="sxs-lookup"><span data-stu-id="aa602-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="aa602-108">Seuraavilla Toimittajan lasku -sivun painikkeilla voit tarkastella ja mahdollisesti muokata kirjanpidollisia jakoja kullekin ostotilauksen summalle.</span><span class="sxs-lookup"><span data-stu-id="aa602-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="aa602-109">**Jakosummat** – Tarkastele muokkaa yksittäisen rivin ja sen alatason rivien kirjanpidollisia jakoja, kuten veroja tai maksuja.</span><span class="sxs-lookup"><span data-stu-id="aa602-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="aa602-110">Voit tarkastella ja muokata alarivin kirjanpidollisia jakoja myös suoraan Arvonlisäverotapahtumat- tai Kulutapahtumat-sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="aa602-111">Muokkaa toimittajan laskun otsikon summia, kuten kuluja tai valuutan pyöristyssummia.</span><span class="sxs-lookup"><span data-stu-id="aa602-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="aa602-112">Muokkaa toimittajalaskun rivisummia.</span><span class="sxs-lookup"><span data-stu-id="aa602-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="aa602-113">**Näytä jakaumat** – Näytä asiakirjan kaikkien rivien kirjanpidolliset jaot.</span><span class="sxs-lookup"><span data-stu-id="aa602-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="aa602-114">Et voi muokata kirjanpidollisia jakoja tästä näkymästä.</span><span class="sxs-lookup"><span data-stu-id="aa602-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="aa602-115">Näytä otsikon ja rivien summat.</span><span class="sxs-lookup"><span data-stu-id="aa602-115">View header and line amounts.</span></span>

<span data-ttu-id="aa602-116">Jos toimittajalasku viittaa ostotilaukseen, voit jakaa ja muokata kirjanpidon jaot riveille, jotka sisältävät nimikkeen, joka ei ole varastossa.</span><span class="sxs-lookup"><span data-stu-id="aa602-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="aa602-117">Jos toimittajan laskurivi viittaa ostotilausriviin, voit poistaa kirjanpitojaon.</span><span class="sxs-lookup"><span data-stu-id="aa602-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="aa602-118">Et voi jakaa tai poistaa kulujen, verojen ja rivialennusten rivejä.</span><span class="sxs-lookup"><span data-stu-id="aa602-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="aa602-119">Voi muokata kirjanpitotiliä, mutta et voi muuttaa summia tai prosentteja.</span><span class="sxs-lookup"><span data-stu-id="aa602-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="aa602-120">Jos ylätason rivillä on nimike, joka ei ole varastossa, ja kirjanpidon jaot jaetaan, rivin alempi taso jaetaan automaattisesti vastaamaan ylätason rivin taloushallinnon dimensioita.</span><span class="sxs-lookup"><span data-stu-id="aa602-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="aa602-121">Alirivin kirjanpidollisia jakoja ei voi lisäksi jakaa tai poistaa, mutta alirivin asetuksista riippuen, voit mahdollisesti muuttaa alirivin kirjanpidollisten jakojen kirjanpitotiliä.</span><span class="sxs-lookup"><span data-stu-id="aa602-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="aa602-122">Summien jakaminen</span><span class="sxs-lookup"><span data-stu-id="aa602-122">Distributing amounts</span></span>
<span data-ttu-id="aa602-123">Kun syötät toimittajan lasku, jokainen määrä jaetaan seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="aa602-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa602-124">Toimittajan laskun rivin tyyppi</span><span class="sxs-lookup"><span data-stu-id="aa602-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="aa602-125">Tärkeysjärjestys, joka määrittää, mistä päätili näkyy.</span><span class="sxs-lookup"><span data-stu-id="aa602-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="aa602-126">Tärkeysjärjestys, joka määrittää, mikä oletusarvoinen taloushallinnon dimensio tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa602-127">Varastotuote</span><span class="sxs-lookup"><span data-stu-id="aa602-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-128">Kirjanpidollinen jako ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-129">Päätili-kenttä, kun Kirjaus-sivulla on valittu Tuotteen ostomeno.</span><span class="sxs-lookup"><span data-stu-id="aa602-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-130">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-131">Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-132">Hankintaluokka tai tuote, jota ei ole varastossa</span><span class="sxs-lookup"><span data-stu-id="aa602-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-133">Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-134">Päätili-kenttä, kun Kirjaus-sivulla on valittu Kulun ostomeno.</span><span class="sxs-lookup"><span data-stu-id="aa602-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-135">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-136">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="aa602-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="aa602-137">Käytä taloushallinnon oletusdimensioarvoja toimittajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="aa602-138">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-139">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa602-140">Käyttöomaisuus</span><span class="sxs-lookup"><span data-stu-id="aa602-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-141">Kirjanpidollinen jako ostotilausriville, jos toimittajalaskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-142">Jos Toimittajan lasku -lomakkeessa Tapahtumatyyppi-kentästä on valittu Hankinta, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankinta.</span><span class="sxs-lookup"><span data-stu-id="aa602-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="aa602-143">Jos Tapahtumatyyppi-kentästä on valittu Hankintaoikaisu, Päätili-kenttä, kun Käyttöomaisuuserän kirjausprofiilit -sivulla on valittuna Hankintaoikaisu.</span><span class="sxs-lookup"><span data-stu-id="aa602-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-144">Käytä ostotilausriville tilijakoa, jos laskun rivi viittaa ostotilauksen riviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-145">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-146">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-147">Toimittajalaskurivillä määritetty projekti</span><span class="sxs-lookup"><span data-stu-id="aa602-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-148">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-149">Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Saldo, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannus.</span><span class="sxs-lookup"><span data-stu-id="aa602-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="aa602-150">Jos Projektiryhmät-sivulla Kirjaa kustannukset - Nimike -sivulta on valittu Tulos, Päätili-kenttä, kun Kirjanpidon asetukset sivulta on valittu Kustannukset - Nimike.</span><span class="sxs-lookup"><span data-stu-id="aa602-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-151">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa602-152">Rivialennus</span><span class="sxs-lookup"><span data-stu-id="aa602-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-153">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-154">Päätili-kenttä, kun Kirjaus-sivulta on valittu Alennus.</span><span class="sxs-lookup"><span data-stu-id="aa602-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="aa602-155">Jos alennuspäätiliä ei ole määritetty kirjausprofiilissa, kirjanpidon jako kokonaishinnalle tilauksen ostorivillä.</span><span class="sxs-lookup"><span data-stu-id="aa602-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-156">Jos laskurivi on viittaus ostotilausriviin, käytä kirjanpidon jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-157">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-158">Käytä toimittajan laskurivin taloushallinnon dimension arvoja.</span><span class="sxs-lookup"><span data-stu-id="aa602-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-159">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-160">Oston kulut, jotka on syötetty ostotilausrivin Hinta ja alennus -välilehteen</span><span class="sxs-lookup"><span data-stu-id="aa602-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-161">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-162">Ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="aa602-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-163">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-164">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa602-165">Rivin kulu</span><span class="sxs-lookup"><span data-stu-id="aa602-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-166">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-167">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="aa602-168">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Nimike, ostotilausrivin laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="aa602-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-169">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-170">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-171">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-172">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-173">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-174">Vero, seuraavalla ehdolla:</span><span class="sxs-lookup"><span data-stu-id="aa602-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="aa602-175">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehto valitaan Kirjanpitoparametrit-sivulta.</span><span class="sxs-lookup"><span data-stu-id="aa602-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="aa602-176">Kirjanpidollinen jako ostotilausriville, jos laskurivi viittaa ostotilausriviin.</span><span class="sxs-lookup"><span data-stu-id="aa602-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-177">Kulun tai laajennetun hinnan kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="aa602-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-178">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-179">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-180">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa602-181">Vero, seuraavilla ehdoilla:</span><span class="sxs-lookup"><span data-stu-id="aa602-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="aa602-182">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="aa602-183">Arvonlisäveroryhmän Käyttövero-kentän valinta poistetaan Arvonlisäveroryhmät-sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="aa602-184">Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="aa602-185">Jos verosummaa ei voi palauttaa, kokonaishinta tai kulun kirjanpidollinen jako.</span><span class="sxs-lookup"><span data-stu-id="aa602-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-186">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-187">Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-188">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-189">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-190">Vero, seuraavilla ehdoilla:</span><span class="sxs-lookup"><span data-stu-id="aa602-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="aa602-191">Käytä Yhdysvaltojen verotussääntöjä -vaihtoehdon valinta poistetaan Kirjanpitoparametrit-sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="aa602-192">Arvonlisäveroryhmän Käyttövero-kenttä valitaan Arvonlisäveroryhmät-sivulta.</span><span class="sxs-lookup"><span data-stu-id="aa602-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="aa602-193">Jos verosumma on palautettavissa, Kirjanpidon kirjausryhmät -sivun Saatava arvonlisävero -kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="aa602-194">Jos verosumma ei ole palautettavissa, Kirjanpidon kirjausryhmät -sivun Käyttöverokulu-kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-195">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-196">Käytä taloushallinnon dimensioita laajennetusta hinnasta tai kulun kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-197">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-198">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa602-199">Otsikkomaksu</span><span class="sxs-lookup"><span data-stu-id="aa602-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-200">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Kirjanpitotili, Kulujen koodi -sivun Debet-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="aa602-201">Jos Kulujen koodi -lomakkeen Veloituslaji-kentästä on valittu Asiakas/Toimittaja, Kulujen koodi -sivun Kredit-tili-kenttä.</span><span class="sxs-lookup"><span data-stu-id="aa602-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-202">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-203">Jos päätili on kohdistustili, käytä oletusarvoa kohdistustilin määrityksestä.</span><span class="sxs-lookup"><span data-stu-id="aa602-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="aa602-204">Käytä taloushallinnon dimension oletusmallin arvoja toimittajan laskun otsikosta.</span><span class="sxs-lookup"><span data-stu-id="aa602-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="aa602-205">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-206">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa602-207">Otsikkoalennus</span><span class="sxs-lookup"><span data-stu-id="aa602-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="aa602-208">Toimittajan laskun alennus -kirjaustyypin Päätili-kenttä Automaattisten tapahtumien tilit -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aa602-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="aa602-209">Jos laskurivi on viittaus ostotilausriviin, käytä tilin jakoa ostotilausriville.</span><span class="sxs-lookup"><span data-stu-id="aa602-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="aa602-210">Käytä taloushallinnon dimensioita laajennetun hinnan kirjanpidollisesta jaosta toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-211">Käytä taloushallinnon dimension arvoja toimittajan laskun riviltä.</span><span class="sxs-lookup"><span data-stu-id="aa602-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="aa602-212">Käytä taloushallinnon oletusdimensioarvoja Tilikartta-sivun päätililtä.</span><span class="sxs-lookup"><span data-stu-id="aa602-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="aa602-213">Verojen jakaminen</span><span class="sxs-lookup"><span data-stu-id="aa602-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="aa602-214">verojen kirjanpidollisia jakoja ei voi luoda ennen verojen laskentaa.</span><span class="sxs-lookup"><span data-stu-id="aa602-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="aa602-215">Jotta voit laskea arvonlisäverot, sinun on suoritettava jokin seuraavista Toimittajan lasku -sivun tehtävistä:</span><span class="sxs-lookup"><span data-stu-id="aa602-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="aa602-216">Näytä laskun summa.</span><span class="sxs-lookup"><span data-stu-id="aa602-216">View the invoice total.</span></span>
-   <span data-ttu-id="aa602-217">Näytä arvonlisävero.</span><span class="sxs-lookup"><span data-stu-id="aa602-217">View the sales tax.</span></span>
-   <span data-ttu-id="aa602-218">Näytä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="aa602-218">View the subledger journal.</span></span>
-   <span data-ttu-id="aa602-219">Näytä kirjanpidolliset jaot koko toimittajan laskulle.</span><span class="sxs-lookup"><span data-stu-id="aa602-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="aa602-220">Sijoita toimittajan lasku pitoon.</span><span class="sxs-lookup"><span data-stu-id="aa602-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="aa602-221">Kirjaa toimittajalasku.</span><span class="sxs-lookup"><span data-stu-id="aa602-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="aa602-222">Alareskontran kirjauskansiot toimittajalaskuille</span><span class="sxs-lookup"><span data-stu-id="aa602-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="aa602-223">Ennen kuin kirjaat toimittajalaskun, voit tarkastella laskun koko kirjanpitokirjausta, joka sisältää hyvitykset ja veloitukset, jotta voit varmistaa, että lasku kirjataan oikeille tileille.</span><span class="sxs-lookup"><span data-stu-id="aa602-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="aa602-224">Tämä kirjanpitomerkinnän koko näkymä tunnetaan nimellä alareskontran kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="aa602-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="aa602-225">Jos alareskontran kirjaus on virheellinen esikatsellessa, et voi muokata sitä ennen kuin kirjaat toimittajatilauksen.</span><span class="sxs-lookup"><span data-stu-id="aa602-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="aa602-226">Sen sijaan sinun on muokattava kirjanpidollisia jakoja tai kirjausprofiilia.</span><span class="sxs-lookup"><span data-stu-id="aa602-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="aa602-227">Kirjanpidollisia jakoja käytetään määrittämään yksi kirjanpitomerkinnän puolista, debet tai kredit.</span><span class="sxs-lookup"><span data-stu-id="aa602-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="aa602-228">Alareskontran kirjauskansion kirjanpitoviennin vastakirjaus luodaan käyttämällä kirjausprofiileja, kuten toimittajatili tai vero.</span><span class="sxs-lookup"><span data-stu-id="aa602-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





