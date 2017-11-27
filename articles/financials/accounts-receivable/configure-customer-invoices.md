---
title: Myyntilaskun luominen
description: "**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0e5605b65b6203a50ef2fef81d032a887da32bf9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="a22a7-103">Myyntilaskun luominen</span><span class="sxs-lookup"><span data-stu-id="a22a7-103">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a22a7-104">**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="a22a7-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="a22a7-105">Tämän tyyppinen myyntilasku luonti perustuu myyntitilaukseen, jossa on tilausrivit ja nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="a22a7-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="a22a7-106">Nimiketunnukset määritetään ja kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="a22a7-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="a22a7-107">Alareskontran kirjauskansioviennit eivät ole käytettävissä myyntitilauksen asiakaslaskulle.</span><span class="sxs-lookup"><span data-stu-id="a22a7-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="a22a7-108">Lisätietoja on ohjeaiheessa [Myyntitilauksen laskujen luominen](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="a22a7-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="a22a7-109">**Vapaatekstilasku** ei liity myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="a22a7-110">Sen tilausriveillä on antamasi kirjanpitotilit, vapaatekstikuvaukset ja myyntisumma.</span><span class="sxs-lookup"><span data-stu-id="a22a7-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="a22a7-111">Tällaiseen laskuun ei voi kirjoittaa nimiketunnusta.</span><span class="sxs-lookup"><span data-stu-id="a22a7-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="a22a7-112">Arvonlisäverotiedot on kirjoitettava.</span><span class="sxs-lookup"><span data-stu-id="a22a7-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="a22a7-113">Myynnin päätili ilmaistaan jokaisella laskurivillä, ja voit jakaa sen useille kirjanpitotileille valitsemalla **Jaa summat** **Vapaatekstilasku**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="a22a7-114">Myös asiakkaan saldo kirjataan vapaatekstilaskussa käytetystä kirjausprofiilista yhteenvetotilille.</span><span class="sxs-lookup"><span data-stu-id="a22a7-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="a22a7-115">Lisätietoja on kohdassa </span><span class="sxs-lookup"><span data-stu-id="a22a7-115">For more information see:</span></span>

[<span data-ttu-id="a22a7-116">Luo vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="a22a7-116">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="a22a7-117">Vapaatekstilaskumallin luominen</span><span class="sxs-lookup"><span data-stu-id="a22a7-117">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="a22a7-118">Vapaatekstilaskumallin määrittäminen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="a22a7-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="a22a7-119">Luo ja kirjaa toistuvat vapaatekstilaskut</span><span class="sxs-lookup"><span data-stu-id="a22a7-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="a22a7-120">**Proformalasku** on lasku, joka laaditaan todellisten laskusummien ennusteena ennen laskun kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="a22a7-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="a22a7-121">Proformalaskun voi tulostaa joko myyntilauksen myyntilaskulle tai vapaatekstilaskulle.</span><span class="sxs-lookup"><span data-stu-id="a22a7-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="a22a7-122">Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat myyntitilauksiin</span><span class="sxs-lookup"><span data-stu-id="a22a7-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="a22a7-123">Voit tämän prosessin avulla myyntitilaukseen perustuvan laskun.</span><span class="sxs-lookup"><span data-stu-id="a22a7-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="a22a7-124">Tämä voi olla kätevää, jos päätät laskuttaa asiakasta ennen tavaroiden tai palvelujen toimittamista.</span><span class="sxs-lookup"><span data-stu-id="a22a7-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="a22a7-125">Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen myyntitilausten laskujen kokonaismäärän mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="a22a7-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="a22a7-126">Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="a22a7-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="a22a7-127">Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.</span><span class="sxs-lookup"><span data-stu-id="a22a7-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="a22a7-128">Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="a22a7-129">Voit tarkastella kirjattuja laskuja **Avoimet asiakaslaskut** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="a22a7-130">Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat pakkausluetteloihin ja päivämäärään</span><span class="sxs-lookup"><span data-stu-id="a22a7-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="a22a7-131">Käytä tätä prosessia, kun myyntitilaukselle on kirjattu vähintään yksi pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="a22a7-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="a22a7-132">Myyntilasku perustuu näiden tuotteiden pakkausluetteloihin ja vastaa niiden määriä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="a22a7-133">Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="a22a7-134">Voit luoda myyntilaskun niiden pakkausluettelon rivinimikkeiden perusteella, jotka on toimitettu tähän mennessä, vaikka kaikkia tietyn myyntitilauksen nimikkeitä ei olisi vielä toimitettu.</span><span class="sxs-lookup"><span data-stu-id="a22a7-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="a22a7-135">Näin kannattaa tehdä esimerkiksi silloin, kun yritys lähettää asiakkaalle kuukaudessa yhden laskun, joka sisältää kaikki kuukauden aikana tehdyt toimitukset.</span><span class="sxs-lookup"><span data-stu-id="a22a7-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="a22a7-136">Jokainen pakkausluettelo edustaa myyntitilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta.</span><span class="sxs-lookup"><span data-stu-id="a22a7-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="a22a7-137">Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen pakkausluetteloiden toimitusten kokonaismäärällä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="a22a7-138">Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="a22a7-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="a22a7-139">Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.</span><span class="sxs-lookup"><span data-stu-id="a22a7-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="a22a7-140">Varastotapahtumat päivitetään laskun numerolla ja myyntitilauksen **Rivin tila** -kentän tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="a22a7-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="a22a7-141">Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="a22a7-142">Konsolidoi kirjattavat myyntitilaukset tai pakkausluettelot</span><span class="sxs-lookup"><span data-stu-id="a22a7-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="a22a7-143">Käytä tätä prosessia, kun vähintään yksi myyntitilaus on valmis laskutettavaksi ja haluat konsolidoida ne yhteen laskuun.</span><span class="sxs-lookup"><span data-stu-id="a22a7-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="a22a7-144">Voit valita **Myyntitilaus**-luettelosivulla useita laskuja ja konsolidoida ne sitten **Luo laskuja** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="a22a7-145">Voit muuttaa **Laskun kirjaus** -sivulla **Yhteenvetotilaus**-asetuksen muodostamaan yhteenvedon tilausnumeron mukaan (jossa yhdelle myyntitilaukselle on useita pakkausluetteloita) tai laskutustilin mukaan (jossa yhdellä laskutustilillä on useita myyntitilauksia).</span><span class="sxs-lookup"><span data-stu-id="a22a7-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="a22a7-146">Konsolidoi myyntitilaukset yhdeksi laskuksi **Järjestä**-painikkeella **Yhteenvetotilaus**-asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="a22a7-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="a22a7-147">Kirjaustoimintoa muuttavat lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="a22a7-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="a22a7-148">Seuraavat kentät muuttaa kirjausprosessin toimintaa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a22a7-149">Kenttä</span><span class="sxs-lookup"><span data-stu-id="a22a7-149">Field</span></span></th>
<th><span data-ttu-id="a22a7-150">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a22a7-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a22a7-151">Määrä</span><span class="sxs-lookup"><span data-stu-id="a22a7-151">Quantity</span></span></td>
<td><span data-ttu-id="a22a7-152">Valitse määrät, joihin asiakirjan kirjaaminen perustuu.</span><span class="sxs-lookup"><span data-stu-id="a22a7-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="a22a7-153">Kentän vaihtoehdot vaihtelevat ja määräytyvät kirjattavan asiakirjan tyypin mukaan. Asiakirja voi olla esimerkiksi pakkausluettelo tai lasku.</span><span class="sxs-lookup"><span data-stu-id="a22a7-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="a22a7-154"><strong>Toimita nyt</strong> – Valitse kaikki <strong>Toimita nyt</strong> -kenttään annetut määrät.</span><span class="sxs-lookup"><span data-stu-id="a22a7-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="a22a7-155">Tällä vaihtoehdolla voit tehdä osittaisen tilausvahvistuksen tai toimituksen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="a22a7-156"><strong>Keräilty</strong> – valitse kaikki kerätyt määrät.</span><span class="sxs-lookup"><span data-stu-id="a22a7-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="a22a7-157"><strong>Kaikki</strong> – valitse kaikki myyntitilausmäärät, joita ei ole vielä päivitetty nykyisellä asiakirjatyypillä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-157"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="a22a7-158"><strong>Pakkausluettelo</strong> – valitse kaikki määrät, jotka on päivitetty pakkausluettelolla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="a22a7-159"><strong>Kerätty määrä ja muut kuin varastoidut tuotteet</strong> – valitse kaikki kerätyt määrät ja kaikki tuotemäärät, joita ei ole varastoitu.</span><span class="sxs-lookup"><span data-stu-id="a22a7-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-160">Kirjaus</span><span class="sxs-lookup"><span data-stu-id="a22a7-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="a22a7-161">Valitse tämä vaihtoehto, jos haluat kirjata myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="a22a7-162">Poista tämän vaihtoehdon valinta, jos haluat tulostaa proformamyyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="a22a7-163"><strong>Huomautus:</strong> Jos sovit maksusuunnitelman, maksusuunnitelma ei näy proformamyyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="a22a7-164">Maksusuunnitelmat näkyvät vain varsinaisessa myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a22a7-165">Myöhäinen valinta</span><span class="sxs-lookup"><span data-stu-id="a22a7-165">Late selection</span></span></td>
<td><span data-ttu-id="a22a7-166">Valitse tämä vaihtoehto, jos haluat käyttää valittua kyselyä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="a22a7-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="a22a7-167">Tätä vaihtoehtoa käytetään komentojonotöissä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-167">This option is used for batch jobs.</span></span> <span data-ttu-id="a22a7-168">Kysely suoritetaan, kun komentojonotyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="a22a7-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-169">Vähennä määrää</span><span class="sxs-lookup"><span data-stu-id="a22a7-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="a22a7-170">Valitse tämä vaihtoehto, jos haluat automaattisesti vähentää toimitettua määrää tiedostoa kirjatessa, jotta toimitettu määrä vastaisi käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a22a7-171">Tulosta</span><span class="sxs-lookup"><span data-stu-id="a22a7-171">Print</span></span></td>
<td><span data-ttu-id="a22a7-172">Valitse, milloin asiakirjat tulostetaan:</span><span class="sxs-lookup"><span data-stu-id="a22a7-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="a22a7-173"><strong>Valittu</strong> – tulosta asiakirjat, kun lasku on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="a22a7-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="a22a7-174"><strong>Jälkeen</strong> – tulosta asiakirjat, kun kaikki laskut on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="a22a7-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="a22a7-175">
<strong>Huomautus:</strong> <strong>Tulosta</strong>-kenttä on käytettävissä vain, jos <strong>Tulosta lasku</strong>-, <strong>Tulosta vahvistus</strong>-, <strong>Tulosta keräysluettelo</strong>- tai <strong>Tulosta pakkausluettelo</strong> -vaihtoehto on valittu.</span><span class="sxs-lookup"><span data-stu-id="a22a7-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="a22a7-176">Voit esimerkiksi määrittää <strong>Lomakkeen lajittelu</strong> -sivulla järjestelmän lajittelemaan tiedot laskutustilin perusteella.</span><span class="sxs-lookup"><span data-stu-id="a22a7-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="a22a7-177">Voit sitten valita <strong>Jälkeen</strong>, jos haluat tulostaa asiakirjat laskutilin mukaan lajitelluissa erissä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="a22a7-178">Muussa tapauksessa asiakirjat tulostetaan ennen kuin niiden käsittely on valmis, eikä asiakirjoja lajitella <strong>Lomakkeen lajittelu</strong> -sivulla määritetyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-178">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-179">Tulosta lasku</span><span class="sxs-lookup"><span data-stu-id="a22a7-179">Print invoice</span></span></td>
<td><span data-ttu-id="a22a7-180">Valitse tämä vaihtoehto, kun haluat tulostaa laskun.</span><span class="sxs-lookup"><span data-stu-id="a22a7-180">Select this option to print the invoice.</span></span> <span data-ttu-id="a22a7-181">Jos tämä vaihtoehto on poistettu käytöstä, voit kirjata laskun sitä tulostamatta.</span><span class="sxs-lookup"><span data-stu-id="a22a7-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a22a7-182">Lähetä sähköposti</span><span class="sxs-lookup"><span data-stu-id="a22a7-182">Send e-mail</span></span></td>
<td><span data-ttu-id="a22a7-183">Valitsemalla tämän voit lähettää myyntitilauksen laskun asiakkaalle sähköpostin liitteenä laskun kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="a22a7-184">Liitteet lähetetään PDF- ja XML-tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="a22a7-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="a22a7-185">Tämä vaihtoehto on käytettävissä vain, jos valitset <strong>Ota CFD käyttöön (sähköiset laskut)</strong> -vaihtoehdon <strong>Sähköisten laskujen parametrit</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="a22a7-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="a22a7-186"><strong>Huomautus:</strong> (MEX) Tämä ohjausobjekti on vain niiden yritysten käytettävissä, joiden ensisijainen osoite on Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-187">Käytä tulostuksenhallinnan kohdetta</span><span class="sxs-lookup"><span data-stu-id="a22a7-187">Use print management destination</span></span></td>
<td><span data-ttu-id="a22a7-188">Valitsemalla tämän vaihtoehdon voit käyttää tapahtumalle, asiakirjalle tai moduulille <strong>Tulostuksenhallinnan asetukset</strong> -sivulla määritettyjä tulostusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="a22a7-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a22a7-189">Tarkista luottoraja</span><span class="sxs-lookup"><span data-stu-id="a22a7-189">Check credit limit</span></span></td>
<td><span data-ttu-id="a22a7-190">Valitse, mitä luottorajan tarkistuksessa analysoidaan.</span><span class="sxs-lookup"><span data-stu-id="a22a7-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="a22a7-191"><strong>Ei mitään</strong> – Luottorajatarkistusta ei tarvitse tehdä.</span><span class="sxs-lookup"><span data-stu-id="a22a7-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="a22a7-192"><strong>Saldo</strong> – Luottorajaa verrataan asiakkaan saldoon.</span><span class="sxs-lookup"><span data-stu-id="a22a7-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="a22a7-193"><strong>Saldo + pakkausluettelo tai tuotteen vastaanotto</strong> – luottorajaa verrataan asiakkaan saldoon ja toimituksiin.</span><span class="sxs-lookup"><span data-stu-id="a22a7-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="a22a7-194"><strong>Saldo+Kaikki</strong> – Luottorajaa verrataan asiakkaan saldoon, toimituksiin ja avoimiin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="a22a7-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-195">Hyvityksen oikaisu</span><span class="sxs-lookup"><span data-stu-id="a22a7-195">Credit correction</span></span></td>
<td><span data-ttu-id="a22a7-196">Valitse tämä vaihtoehto, jos haluat näyttää hyvityslaskun veloituksena tositetapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a22a7-197">Jäljelle jäävän luoton määrä</span><span class="sxs-lookup"><span data-stu-id="a22a7-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="a22a7-198">Valitse tämä vaihtoehto, jos kirjaat hyvityslaskua ja haluat säilyttää jäljelle jäävän määrän tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-198">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="a22a7-199">Jos tämän vaihtoehdon valinta poistetaan, jäljelle jääväksi määräksi määritetään 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="a22a7-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a22a7-200">Päivitysyhteenveto mille:</span><span class="sxs-lookup"><span data-stu-id="a22a7-200">Summary update for</span></span></td>
<td><span data-ttu-id="a22a7-201">Valitse, miten useista myyntitilauksista luodaan yhteenveto:</span><span class="sxs-lookup"><span data-stu-id="a22a7-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="a22a7-202"><strong>Ei mitään</strong> – Älä luo myyntitilauksista yhteenvetoa.</span><span class="sxs-lookup"><span data-stu-id="a22a7-202"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="a22a7-203">Kutakin myyntitilausta varten luodaan esimerkiksi erillinen lasku.</span><span class="sxs-lookup"><span data-stu-id="a22a7-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="a22a7-204"><strong>Laskutustili</strong> – tee yhteenveto kaikista valituista tilauksista <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a22a7-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="a22a7-205"><strong>Tilaus</strong> – Luo valitusta tilausvalikoimasta yhteenveto yhdeksi määrittämäksesi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="a22a7-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="a22a7-206">Tilauksista luodaan yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="a22a7-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="a22a7-207">Jos valitset tämän vaihtoehdon, myös <strong>Myyntitilaus</strong>-kentästä on valittava arvo.</span><span class="sxs-lookup"><span data-stu-id="a22a7-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="a22a7-208"><strong>Automaattinen yhteenveto</strong> – Jos yhteenvetopäivitykset on määritetty <strong>Yhteenvedon päivitys</strong> -sivulla, luo kaikista valituista tilauksista yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a22a7-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="a22a7-209">Jos yhteenvetopäivityksiä ei ole määritetty, tilaus kirjataan erikseen.</span><span class="sxs-lookup"><span data-stu-id="a22a7-209">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="a22a7-210"><strong>Pakkausluettelo</strong> – Luo valitusta tilausvalikoimasta yksi yhteenvetolasku pakkausluetteloa kohden.</span><span class="sxs-lookup"><span data-stu-id="a22a7-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="a22a7-211">Tämä vaihtoehto on käytettävissä vain, jos <strong>Määrä</strong>-kentästä on valittu <strong>Pakkausluettelo</strong>.</span><span class="sxs-lookup"><span data-stu-id="a22a7-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






