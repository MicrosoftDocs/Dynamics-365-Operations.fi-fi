---
title: Myyntilaskun luominen
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="3ec08-102">Myyntilaskun luominen</span><span class="sxs-lookup"><span data-stu-id="3ec08-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3ec08-103">**Myyntitilauksen myyntilasku** on myyntiin liittyvä lasku, jonka organisaatio antaa asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="3ec08-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="3ec08-104">Tämän tyyppinen myyntilasku luonti perustuu myyntitilaukseen, jossa on tilausrivit ja nimiketunnukset.</span><span class="sxs-lookup"><span data-stu-id="3ec08-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="3ec08-105">Nimiketunnukset määritetään ja kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="3ec08-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="3ec08-106">Alareskontran kirjauskansioviennit eivät ole käytettävissä myyntitilauksen asiakaslaskulle.</span><span class="sxs-lookup"><span data-stu-id="3ec08-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="3ec08-107">Lisätietoja on ohjeaiheessa [Myyntitilauksen laskujen luominen](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="3ec08-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="3ec08-108">**Vapaatekstilasku** ei liity myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="3ec08-109">Sen tilausriveillä on antamasi kirjanpitotilit, vapaatekstikuvaukset ja myyntisumma.</span><span class="sxs-lookup"><span data-stu-id="3ec08-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="3ec08-110">Tällaiseen laskuun ei voi kirjoittaa nimiketunnusta.</span><span class="sxs-lookup"><span data-stu-id="3ec08-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="3ec08-111">Arvonlisäverotiedot on kirjoitettava.</span><span class="sxs-lookup"><span data-stu-id="3ec08-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="3ec08-112">Myynnin päätili ilmaistaan jokaisella laskurivillä, ja voit jakaa sen useille kirjanpitotileille valitsemalla **Jaa summat** **Vapaatekstilasku**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="3ec08-113">Myös asiakkaan saldo kirjataan vapaatekstilaskussa käytetystä kirjausprofiilista yhteenvetotilille.</span><span class="sxs-lookup"><span data-stu-id="3ec08-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="3ec08-114">Lisätietoja on kohdassa </span><span class="sxs-lookup"><span data-stu-id="3ec08-114">For more information see:</span></span>

[<span data-ttu-id="3ec08-115">Luo vapaatekstilasku</span><span class="sxs-lookup"><span data-stu-id="3ec08-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="3ec08-116">Vapaatekstilaskumallin luominen</span><span class="sxs-lookup"><span data-stu-id="3ec08-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="3ec08-117">Vapaatekstilaskumallin määrittäminen asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="3ec08-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="3ec08-118">Luo ja kirjaa toistuvat vapaatekstilaskut</span><span class="sxs-lookup"><span data-stu-id="3ec08-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="3ec08-119">**Proformalasku** on lasku, joka laaditaan todellisten laskusummien ennusteena ennen laskun kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="3ec08-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="3ec08-120">Proformalaskun voi tulostaa joko myyntilauksen myyntilaskulle tai vapaatekstilaskulle.</span><span class="sxs-lookup"><span data-stu-id="3ec08-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="3ec08-121">Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat myyntitilauksiin</span><span class="sxs-lookup"><span data-stu-id="3ec08-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="3ec08-122">Voit tämän prosessin avulla myyntitilaukseen perustuvan laskun.</span><span class="sxs-lookup"><span data-stu-id="3ec08-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="3ec08-123">Tämä voi olla kätevää, jos päätät laskuttaa asiakasta ennen tavaroiden tai palvelujen toimittamista.</span><span class="sxs-lookup"><span data-stu-id="3ec08-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="3ec08-124">Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen myyntitilausten laskujen kokonaismäärän mukaiseksi.</span><span class="sxs-lookup"><span data-stu-id="3ec08-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="3ec08-125">Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="3ec08-126">Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.</span><span class="sxs-lookup"><span data-stu-id="3ec08-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="3ec08-127">Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="3ec08-128">Voit tarkastella kirjattuja laskuja **Avoimet asiakaslaskut** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="3ec08-129">Kirjaa ja tulosta yksittäisiä myyntilaskuja, jotka perustuvat pakkausluetteloihin ja päivämäärään</span><span class="sxs-lookup"><span data-stu-id="3ec08-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="3ec08-130">Käytä tätä prosessia, kun myyntitilaukselle on kirjattu vähintään yksi pakkausluettelo.</span><span class="sxs-lookup"><span data-stu-id="3ec08-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="3ec08-131">Myyntilasku perustuu näiden tuotteiden pakkausluetteloihin ja vastaa niiden määriä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="3ec08-132">Laskun kirjanpitotiedot perustuvat tietoihin, jotka syötettiin laskujen kirjauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="3ec08-133">Voit luoda myyntilaskun niiden pakkausluettelon rivinimikkeiden perusteella, jotka on toimitettu tähän mennessä, vaikka kaikkia tietyn myyntitilauksen nimikkeitä ei olisi vielä toimitettu.</span><span class="sxs-lookup"><span data-stu-id="3ec08-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="3ec08-134">Näin kannattaa tehdä esimerkiksi silloin, kun yritys lähettää asiakkaalle kuukaudessa yhden laskun, joka sisältää kaikki kuukauden aikana tehdyt toimitukset.</span><span class="sxs-lookup"><span data-stu-id="3ec08-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="3ec08-135">Jokainen pakkausluettelo edustaa myyntitilauksen nimikkeiden osatoimitusta tai täydellistä toimitusta.</span><span class="sxs-lookup"><span data-stu-id="3ec08-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="3ec08-136">Kun kirjaat laskun, jokaisen nimikkeen **Laskuttamatta**-määrä päivitetään valittujen pakkausluetteloiden toimitusten kokonaismäärällä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="3ec08-137">Jos myyntitilauksen kaikkien nimikkeiden **Laskuttamatta**-määrä ja **Jäljellä oleva määrä** on 0 (nolla), myyntitilauksen tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="3ec08-138">Jos **Laskuttamatta**-määrä ei ole 0 (nolla), myyntitilauksen tilaa ei muuteta ja siihen voi lisätä laskuja.</span><span class="sxs-lookup"><span data-stu-id="3ec08-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="3ec08-139">Varastotapahtumat päivitetään laskun numerolla ja myyntitilauksen **Rivin tila** -kentän tilaksi muutetaan **Laskutettu**.</span><span class="sxs-lookup"><span data-stu-id="3ec08-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="3ec08-140">Voit katsoa myyntitilausten tilaa **Kaikki myyntilaukset** -luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="3ec08-141">Konsolidoi kirjattavat myyntitilaukset tai pakkausluettelot</span><span class="sxs-lookup"><span data-stu-id="3ec08-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="3ec08-142">Käytä tätä prosessia, kun vähintään yksi myyntitilaus on valmis laskutettavaksi ja haluat konsolidoida ne yhteen laskuun.</span><span class="sxs-lookup"><span data-stu-id="3ec08-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="3ec08-143">Voit valita **Myyntitilaus**-luettelosivulla useita laskuja ja konsolidoida ne sitten **Luo laskuja** -vaihtoehdolla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="3ec08-144">Voit muuttaa **Laskun kirjaus** -sivulla **Yhteenvetotilaus**-asetuksen muodostamaan yhteenvedon tilausnumeron mukaan (jossa yhdelle myyntitilaukselle on useita pakkausluetteloita) tai laskutustilin mukaan (jossa yhdellä laskutustilillä on useita myyntitilauksia).</span><span class="sxs-lookup"><span data-stu-id="3ec08-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="3ec08-145">Konsolidoi myyntitilaukset yhdeksi laskuksi **Järjestä**-painikkeella **Yhteenvetotilaus**-asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="3ec08-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="3ec08-146">Kirjaustoimintoa muuttavat lisäasetukset</span><span class="sxs-lookup"><span data-stu-id="3ec08-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="3ec08-147">Seuraavat kentät muuttaa kirjausprosessin toimintaa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ec08-148">Kenttä</span><span class="sxs-lookup"><span data-stu-id="3ec08-148">Field</span></span></th>
<th><span data-ttu-id="3ec08-149">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="3ec08-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ec08-150">Määrä</span><span class="sxs-lookup"><span data-stu-id="3ec08-150">Quantity</span></span></td>
<td><span data-ttu-id="3ec08-151">Valitse määrät, joihin asiakirjan kirjaaminen perustuu.</span><span class="sxs-lookup"><span data-stu-id="3ec08-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="3ec08-152">Kentän vaihtoehdot vaihtelevat ja määräytyvät kirjattavan asiakirjan tyypin mukaan. Asiakirja voi olla esimerkiksi pakkausluettelo tai lasku.</span><span class="sxs-lookup"><span data-stu-id="3ec08-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="3ec08-153"><strong>Toimita nyt</strong> – Valitse kaikki <strong>Toimita nyt</strong> -kenttään annetut määrät.</span><span class="sxs-lookup"><span data-stu-id="3ec08-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="3ec08-154">Tällä vaihtoehdolla voit tehdä osittaisen tilausvahvistuksen tai toimituksen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="3ec08-155"><strong>Keräilty</strong> – valitse kaikki kerätyt määrät.</span><span class="sxs-lookup"><span data-stu-id="3ec08-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="3ec08-156"><strong>Kaikki</strong> – valitse kaikki myyntitilausmäärät, joita ei ole vielä päivitetty nykyisellä asiakirjatyypillä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="3ec08-157"><strong>Pakkausluettelo</strong> – valitse kaikki määrät, jotka on päivitetty pakkausluettelolla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="3ec08-158"><strong>Kerätty määrä ja muut kuin varastoidut tuotteet</strong> – valitse kaikki kerätyt määrät ja kaikki tuotemäärät, joita ei ole varastoitu.</span><span class="sxs-lookup"><span data-stu-id="3ec08-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-159">Kirjaus</span><span class="sxs-lookup"><span data-stu-id="3ec08-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="3ec08-160">Valitse tämä vaihtoehto, jos haluat kirjata myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="3ec08-161">Poista tämän vaihtoehdon valinta, jos haluat tulostaa proformamyyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="3ec08-162"><strong>Huomautus:</strong> Jos sovit maksusuunnitelman, maksusuunnitelma ei näy proformamyyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="3ec08-163">Maksusuunnitelmat näkyvät vain varsinaisessa myyntitilauksessa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec08-164">Myöhäinen valinta</span><span class="sxs-lookup"><span data-stu-id="3ec08-164">Late selection</span></span></td>
<td><span data-ttu-id="3ec08-165">Valitse tämä vaihtoehto, jos haluat käyttää valittua kyselyä myöhemmin.</span><span class="sxs-lookup"><span data-stu-id="3ec08-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="3ec08-166">Tätä vaihtoehtoa käytetään komentojonotöissä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-166">This option is used for batch jobs.</span></span> <span data-ttu-id="3ec08-167">Kysely suoritetaan, kun komentojonotyö suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="3ec08-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-168">Vähennä määrää</span><span class="sxs-lookup"><span data-stu-id="3ec08-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="3ec08-169">Valitse tämä vaihtoehto, jos haluat automaattisesti vähentää toimitettua määrää tiedostoa kirjatessa, jotta toimitettu määrä vastaisi käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec08-170">Tulosta</span><span class="sxs-lookup"><span data-stu-id="3ec08-170">Print</span></span></td>
<td><span data-ttu-id="3ec08-171">Valitse, milloin asiakirjat tulostetaan:</span><span class="sxs-lookup"><span data-stu-id="3ec08-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="3ec08-172"><strong>Valittu</strong> – tulosta asiakirjat, kun lasku on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="3ec08-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="3ec08-173"><strong>Jälkeen</strong> – tulosta asiakirjat, kun kaikki laskut on päivitetty.</span><span class="sxs-lookup"><span data-stu-id="3ec08-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="3ec08-174">
<strong>Huomautus:</strong> <strong>Tulosta</strong>-kenttä on käytettävissä vain, jos <strong>Tulosta lasku</strong>-, <strong>Tulosta vahvistus</strong>-, <strong>Tulosta keräysluettelo</strong>- tai <strong>Tulosta pakkausluettelo</strong> -vaihtoehto on valittu.</span><span class="sxs-lookup"><span data-stu-id="3ec08-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="3ec08-175">Voit esimerkiksi määrittää <strong>Lomakkeen lajittelu</strong> -sivulla järjestelmän lajittelemaan tiedot laskutustilin perusteella.</span><span class="sxs-lookup"><span data-stu-id="3ec08-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="3ec08-176">Voit sitten valita <strong>Jälkeen</strong>, jos haluat tulostaa asiakirjat laskutilin mukaan lajitelluissa erissä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="3ec08-177">Muussa tapauksessa asiakirjat tulostetaan ennen kuin niiden käsittely on valmis, eikä asiakirjoja lajitella <strong>Lomakkeen lajittelu</strong> -sivulla määritetyssä järjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-178">Tulosta lasku</span><span class="sxs-lookup"><span data-stu-id="3ec08-178">Print invoice</span></span></td>
<td><span data-ttu-id="3ec08-179">Valitse tämä vaihtoehto, kun haluat tulostaa laskun.</span><span class="sxs-lookup"><span data-stu-id="3ec08-179">Select this option to print the invoice.</span></span> <span data-ttu-id="3ec08-180">Jos tämä vaihtoehto on poistettu käytöstä, voit kirjata laskun sitä tulostamatta.</span><span class="sxs-lookup"><span data-stu-id="3ec08-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec08-181">Lähetä sähköposti</span><span class="sxs-lookup"><span data-stu-id="3ec08-181">Send e-mail</span></span></td>
<td><span data-ttu-id="3ec08-182">Valitsemalla tämän voit lähettää myyntitilauksen laskun asiakkaalle sähköpostin liitteenä laskun kirjaamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="3ec08-183">Liitteet lähetetään PDF- ja XML-tiedostoina.</span><span class="sxs-lookup"><span data-stu-id="3ec08-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="3ec08-184">Tämä vaihtoehto on käytettävissä vain, jos valitset <strong>Ota CFD käyttöön (sähköiset laskut)</strong> -vaihtoehdon <strong>Sähköisten laskujen parametrit</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="3ec08-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="3ec08-185"><strong>Huomautus:</strong> (MEX) Tämä ohjausobjekti on vain niiden yritysten käytettävissä, joiden ensisijainen osoite on Meksikossa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-186">Käytä tulostuksenhallinnan kohdetta</span><span class="sxs-lookup"><span data-stu-id="3ec08-186">Use print management destination</span></span></td>
<td><span data-ttu-id="3ec08-187">Valitsemalla tämän vaihtoehdon voit käyttää tapahtumalle, asiakirjalle tai moduulille <strong>Tulostuksenhallinnan asetukset</strong> -sivulla määritettyjä tulostusasetuksia.</span><span class="sxs-lookup"><span data-stu-id="3ec08-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec08-188">Tarkista luottoraja</span><span class="sxs-lookup"><span data-stu-id="3ec08-188">Check credit limit</span></span></td>
<td><span data-ttu-id="3ec08-189">Valitse, mitä luottorajan tarkistuksessa analysoidaan.</span><span class="sxs-lookup"><span data-stu-id="3ec08-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="3ec08-190"><strong>Ei mitään</strong> – Luottorajatarkistusta ei tarvitse tehdä.</span><span class="sxs-lookup"><span data-stu-id="3ec08-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="3ec08-191"><strong>Saldo</strong> – Luottorajaa verrataan asiakkaan saldoon.</span><span class="sxs-lookup"><span data-stu-id="3ec08-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="3ec08-192"><strong>Saldo + pakkausluettelo tai tuotteen vastaanotto</strong> – luottorajaa verrataan asiakkaan saldoon ja toimituksiin.</span><span class="sxs-lookup"><span data-stu-id="3ec08-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="3ec08-193"><strong>Saldo+Kaikki</strong> – Luottorajaa verrataan asiakkaan saldoon, toimituksiin ja avoimiin tilauksiin.</span><span class="sxs-lookup"><span data-stu-id="3ec08-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-194">Hyvityksen oikaisu</span><span class="sxs-lookup"><span data-stu-id="3ec08-194">Credit correction</span></span></td>
<td><span data-ttu-id="3ec08-195">Valitse tämä vaihtoehto, jos haluat näyttää hyvityslaskun veloituksena tositetapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ec08-196">Jäljelle jäävän luoton määrä</span><span class="sxs-lookup"><span data-stu-id="3ec08-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="3ec08-197">Valitse tämä vaihtoehto, jos kirjaat hyvityslaskua ja haluat säilyttää jäljelle jäävän määrän tilauksessa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="3ec08-198">Jos tämän vaihtoehdon valinta poistetaan, jäljelle jääväksi määräksi määritetään 0 (nolla).</span><span class="sxs-lookup"><span data-stu-id="3ec08-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ec08-199">Päivitysyhteenveto mille:</span><span class="sxs-lookup"><span data-stu-id="3ec08-199">Summary update for</span></span></td>
<td><span data-ttu-id="3ec08-200">Valitse, miten useista myyntitilauksista luodaan yhteenveto:</span><span class="sxs-lookup"><span data-stu-id="3ec08-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="3ec08-201"><strong>Ei mitään</strong> – Älä luo myyntitilauksista yhteenvetoa.</span><span class="sxs-lookup"><span data-stu-id="3ec08-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="3ec08-202">Kutakin myyntitilausta varten luodaan esimerkiksi erillinen lasku.</span><span class="sxs-lookup"><span data-stu-id="3ec08-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="3ec08-203"><strong>Laskutustili</strong> – tee yhteenveto kaikista valituista tilauksista <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3ec08-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="3ec08-204"><strong>Tilaus</strong> – Luo valitusta tilausvalikoimasta yhteenveto yhdeksi määrittämäksesi tilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="3ec08-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="3ec08-205">Tilauksista luodaan yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="3ec08-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="3ec08-206">Jos valitset tämän vaihtoehdon, myös <strong>Myyntitilaus</strong>-kentästä on valittava arvo.</span><span class="sxs-lookup"><span data-stu-id="3ec08-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="3ec08-207"><strong>Automaattinen yhteenveto</strong> – Jos yhteenvetopäivitykset on määritetty <strong>Yhteenvedon päivitys</strong> -sivulla, luo kaikista valituista tilauksista yhteenveto <strong>Yhteenvedon päivitysparametrit</strong> -sivulla määritettyjen ehtojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="3ec08-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="3ec08-208">Jos yhteenvetopäivityksiä ei ole määritetty, tilaus kirjataan erikseen.</span><span class="sxs-lookup"><span data-stu-id="3ec08-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="3ec08-209"><strong>Pakkausluettelo</strong> – Luo valitusta tilausvalikoimasta yksi yhteenvetolasku pakkausluetteloa kohden.</span><span class="sxs-lookup"><span data-stu-id="3ec08-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="3ec08-210">Tämä vaihtoehto on käytettävissä vain, jos <strong>Määrä</strong>-kentästä on valittu <strong>Pakkausluettelo</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec08-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






