---
title: Tuotteiden vastaanottojen ja laskutuksen vianmääritys
description: Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteiden vastaanottamisessa ja laskutuksessa voi esiintyä.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d86fa3df1de13cc0e0fb94449207a326069da25b
ms.sourcegitcommit: 91e101d7a51a8b63bd196ec80e9224e5e6e6fc95
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3834352"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="50595-103">Tuotteiden vastaanottojen ja laskutuksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="50595-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="50595-104">Tässä ohjeaiheessa käsitellään sellaisten ongelmien korjaamista, joita tuotteiden vastaanottamisessa ja laskutuksessa voi esiintyä.</span><span class="sxs-lookup"><span data-stu-id="50595-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="50595-105">Voin kirjata vain yhden laskun ostotilausriville, jolla on luokkaperusteisia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="50595-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="50595-106">Määrä on pakollinen, jos haluat kirjata laskuja.</span><span class="sxs-lookup"><span data-stu-id="50595-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="50595-107">Siten, jos rivin kokonaismäärä on laskutettu vain osittaisen summan osalta, et voi laskuttaa jäljellä olevaa summaa toisella laskulla.</span><span class="sxs-lookup"><span data-stu-id="50595-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="50595-108">Saan "Kohdeviitettä ei määritetty" -virheen ostotilauksen vahvistuksen aikana tai "Kutsun kohde on aiheuttanut poikkeuksen" -poikkeus esiintyy toimittajan laskun julkaisemisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="50595-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="50595-109">Tämä ongelma voi esiintyä, kun ostotilausten jaoissa on epäjohdonmukaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="50595-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="50595-110">Voit poistaa tämän ongelman eston ja palauttaa ostotilauksen *Luonnos* siirtymällä kohtaan **Ostot ja hankinnat \> Säännölliset tehtävät \> Tyhjennys \> Ostotilauksen jaon palautus**.</span><span class="sxs-lookup"><span data-stu-id="50595-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="50595-111">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostotilausten jakovirheiden korjaaminen Dynamics 365 Supply Chain Managementissa](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="50595-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="50595-112">En saa yhdistettyä useita tuotteiden vastaanottoja yhdeksi ostotilaukseksi.</span><span class="sxs-lookup"><span data-stu-id="50595-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="50595-113">Useita tuotteiden vastaanottoja ei voi yhdistää yhdeksi ostotilaukseksi, jos eri tuotteiden vastaanottojen riveillä on eri kirjanpitopäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="50595-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="50595-114">Aiemmissa Microsoft Dynamics 365 Supply Chain Managementin versioissa yhdistäminen sallittiin tässä tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="50595-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="50595-115">Käytäntö on kuitenkin altis virheille.</span><span class="sxs-lookup"><span data-stu-id="50595-115">However, the practice is prone to error.</span></span> <span data-ttu-id="50595-116">Luotujen ostotilausrivien kirjanpitopäivämäärän ei pitäisi poiketa niiden tuotteen vastaanoton rivien kirjanpitopäivämäärästä, joiden perusteella ostotilausrivit luotiin.</span><span class="sxs-lookup"><span data-stu-id="50595-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="50595-117">(Osto tilausrivien kirjanpitopäivämäärä vastaa ostotilauksen otsikon kirjanpitopäivämäärää.) Tämän vuoksi useiden tuotteiden vastaanottojen yhdistäminen yhdeksi ostotilaukseksi ei ole enää sallittua.</span><span class="sxs-lookup"><span data-stu-id="50595-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="50595-118">Kirjanpitopäivämäärää käytetään esimerkiksi budjettivarausten ja varausten osalta.</span><span class="sxs-lookup"><span data-stu-id="50595-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="50595-119">Siksi se on säilytettävä siirryttäessä tuotteen vastaanotosta ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="50595-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="50595-120">Kun tuotteen vastaanotot peruutetaan, tapahtumat voidaan kirjata keskeytetylle kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="50595-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="50595-121">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="50595-121">Issue description</span></span>

<span data-ttu-id="50595-122">Jos tuotteen vastaanotto peruutetaan, järjestelmä sallii tapahtumien kirjaamisen keskeytetyille kirjanpitotileille, vaikka päätilit olisivat keskeytettynä.</span><span class="sxs-lookup"><span data-stu-id="50595-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="50595-123">Ongelman toistaminen</span><span class="sxs-lookup"><span data-stu-id="50595-123">Reproduce the issue</span></span>

<span data-ttu-id="50595-124">Seuraavassa esitetään yksi tapa ongelman toistamiseen.</span><span class="sxs-lookup"><span data-stu-id="50595-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="50595-125">Varmista **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdessä, että **Kirjaa vastaanotto kirjanpitoon** -asetuksen arvona on *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="50595-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="50595-126">Luo ostotilaus ja lisää tilausrivi, jossa tietyn tuotteen määrä on *1 000*.</span><span class="sxs-lookup"><span data-stu-id="50595-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="50595-127">Vahvista ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="50595-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="50595-128">Kirjaa tuotteen vastaanotto ja tarkista tositteet.</span><span class="sxs-lookup"><span data-stu-id="50595-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="50595-129">Keskeytä tarvittavat päätilit eli *200140* ja *140200*.</span><span class="sxs-lookup"><span data-stu-id="50595-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="50595-130">Peruuta kirjattu tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="50595-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="50595-131">Huomaa, että tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille.</span><span class="sxs-lookup"><span data-stu-id="50595-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="50595-132">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="50595-132">Issue resolution</span></span>

<span data-ttu-id="50595-133">Tapahtumat voidaan kirjata keskeytetyille kirjanpitotileille, kun tuotteiden vastaanotot peruutetaan, koska tämä toimintatapa mahdollistaa oikeelliset kirjaukset.</span><span class="sxs-lookup"><span data-stu-id="50595-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="50595-134">Tuotteen vastaanoton tositenumero käytettään, vaikka tuotteen vastaanoton aikana ei luotaisi rahoitustositetta.</span><span class="sxs-lookup"><span data-stu-id="50595-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="50595-135">Jos **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi on määritetty *Ei* nimikemalliryhmän osalta, kirjanpitoon ei tehdä kirjauksia.</span><span class="sxs-lookup"><span data-stu-id="50595-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="50595-136">Fyysinen tapahtuma kirjataan kuitenkin kirjanpitotarkoituksia varten alikirjanpitoon, ja tapahtuma vaatii tositenumeron.</span><span class="sxs-lookup"><span data-stu-id="50595-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="50595-137">Tämä tositenumero on se tositenumero, johon viitataan varastotapahtumissa.</span><span class="sxs-lookup"><span data-stu-id="50595-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="50595-138">On suositeltavaa määrittää **Jaksota ostovelka tuotteen vastaanotossa** -asetuksen arvoksi *Kyllä*, kuten seuraavassa blogikirjoituksessa kuvataan: [Muiden kulujen kirjaaminen tuotteen vastaanoton hetkellä](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="50595-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="50595-139">Kirjaa kirjanpidon veloitustilille -asetus ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="50595-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="50595-140">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="50595-140">Issue description</span></span>

<span data-ttu-id="50595-141">Tämä ongelma ilmenee, kun ostotilaus laskutetaan ja **Kirjaa kirjanpidon veloitustilille** -asetuksen arvona on *Kyllä* **Ostoreskontran parametrit** -sivun **Lasku**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="50595-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="50595-142">Ongelman toistaminen</span><span class="sxs-lookup"><span data-stu-id="50595-142">Reproduce the issue</span></span>

<span data-ttu-id="50595-143">Seuraavassa esitetään yksi tapa ongelman toistamiseen.</span><span class="sxs-lookup"><span data-stu-id="50595-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="50595-144">Valitse **Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**.</span><span class="sxs-lookup"><span data-stu-id="50595-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="50595-145">Määritä **Lasku**-välilehden **Kirjaa kirjanpidon veloitustilille** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="50595-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="50595-146">Siirry kohtaan **Varastonhallinta \> Määritys \> Kirjaus \> Kirjaus**.</span><span class="sxs-lookup"><span data-stu-id="50595-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="50595-147">Varmista **Ostotilaus**-välilehdellä, että olet poistanut kaikki tuotteen ostomenojen rivit.</span><span class="sxs-lookup"><span data-stu-id="50595-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="50595-148">Valitse **Ostoreskontra \> Ostotilaukset \> Kaikki ostotilaukset**.</span><span class="sxs-lookup"><span data-stu-id="50595-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="50595-149">Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="50595-149">Create a purchase order.</span></span> <span data-ttu-id="50595-150">Valitse **Toimittajatili**-kentässä *1001 Acme-toimistotarviketta*.</span><span class="sxs-lookup"><span data-stu-id="50595-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="50595-151">Lisää ostotilausrivi, jossa on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="50595-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="50595-152">**Nimikenumero:** *D0011 Laserprojektori*</span><span class="sxs-lookup"><span data-stu-id="50595-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="50595-153">**Toimipaikka:** *1*</span><span class="sxs-lookup"><span data-stu-id="50595-153">**Site:** *1*</span></span>
    - <span data-ttu-id="50595-154">**Varasto**: *11*</span><span class="sxs-lookup"><span data-stu-id="50595-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="50595-155">**Määrä** *4*</span><span class="sxs-lookup"><span data-stu-id="50595-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="50595-156">Valitse toimintoruudun **osta**-välilehden **Toimi**-ryhmässä **Vahvista**.</span><span class="sxs-lookup"><span data-stu-id="50595-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="50595-157">Valitse toimintoruudun **Vastaanota**-välilehden **Luo**-ryhmässä **Tuotteen vastaanotto**.</span><span class="sxs-lookup"><span data-stu-id="50595-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="50595-158">Syötä **Tuotteen vastaanottokirjaus** -valintaikkunan **Tuotteen vastaanotto** -kenttään satunnainen numero ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="50595-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="50595-159">Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.</span><span class="sxs-lookup"><span data-stu-id="50595-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="50595-160">Syötä **Numero**-kenttään satunnainen numero laskunumeroksi.</span><span class="sxs-lookup"><span data-stu-id="50595-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="50595-161">Päivitä täsmäytyksen tila ja kirjaa.</span><span class="sxs-lookup"><span data-stu-id="50595-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="50595-162">Huomaa, näkyviin tulee nyt seuraava virhe, kun luot laskun ostotilauksesta: "Tuotteen ostomenot -tapahtumatyypin tilinumeroa ei ole olemassa".</span><span class="sxs-lookup"><span data-stu-id="50595-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="50595-163">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="50595-163">Issue resolution</span></span>

<span data-ttu-id="50595-164">Tämä määräytyy laskujen ja laskuryhmien parametriasetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="50595-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="50595-165">Lisä tietoja on seuraavassa blogikirjoituksessa: [Ostomenojen kirjaaminen ja varastotilanteen vaihtelut](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="50595-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
