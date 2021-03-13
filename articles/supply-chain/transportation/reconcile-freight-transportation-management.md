---
title: Rahdin täsmäytys kuljetustenhallinnassa
description: Tässä aiheessa käsitellään rahdin täsmäytysprosessia.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014505"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="01aca-103">Rahdin täsmäytys kuljetustenhallinnassa</span><span class="sxs-lookup"><span data-stu-id="01aca-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01aca-104">Tässä aiheessa käsitellään rahdin täsmäytysprosessia.</span><span class="sxs-lookup"><span data-stu-id="01aca-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="01aca-105">Rahti voidaan täsmäyttää manuaalisesti tai se voidaan määrittää tapahtumaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="01aca-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="01aca-106">Jos haluat käyttää rahdin automaattista täsmäytystä, sinun on määritettävä päätarkistus, jossa voit määrittää ehdot määrittämään automaattisesti täsmäytettävät rahtilaskut.</span><span class="sxs-lookup"><span data-stu-id="01aca-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="01aca-107">Rahdin täsmäytysprosessi</span><span class="sxs-lookup"><span data-stu-id="01aca-107">The freight reconciliation process</span></span>

<span data-ttu-id="01aca-108">Kuljetusmaksut lasketaan hinnan laskennassa, joka on liitetty soveltuvaan rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="01aca-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="01aca-109">Kun kuorma on vahvistettu, rahtilasku luodaan ja rahtitaksat siirretään siihen.</span><span class="sxs-lookup"><span data-stu-id="01aca-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="01aca-110">Rahtitaksat jaetaan sekalaisina kuluina soveltuvaan lähdeasiakirjaan (ostotilaus, myyntitilaus ja/tai siirtotilaus) sen mukaan, mitä asetuksia tavallisen laskutusprosessin asetuksissa on käytetty.</span><span class="sxs-lookup"><span data-stu-id="01aca-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="01aca-111">Rahdin täsmäytysprosessi voi alkaa heti, kun rahdinkuljettajan rahtilasku saadaan.</span><span class="sxs-lookup"><span data-stu-id="01aca-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="01aca-112">Kyse voi olla sähköisestä laskusta tai paperilaskusta.</span><span class="sxs-lookup"><span data-stu-id="01aca-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="01aca-113">Jos kyse on paperilaskusta, voit luoda sähköisen laskun käyttämällä rahtilaskua mallina.</span><span class="sxs-lookup"><span data-stu-id="01aca-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="01aca-114">[![Rahdin täsmäytysprosessi](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="01aca-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="01aca-115">Manuaalinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="01aca-115">Manual reconciliation</span></span>

<span data-ttu-id="01aca-116">Jos olet täsmäyttämässä rahtia manuaalisesti, sinun on täsmäytettävä kukin laskun rivi rahtilaskun rivin tai laskutettavan kuorman rivien kanssa.</span><span class="sxs-lookup"><span data-stu-id="01aca-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="01aca-117">Tämä täsmäytys tehdään **Rahtilaskun ja laskun täsmäytys** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="01aca-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="01aca-118">Jos laskurivin summa ei täsmää rahtilaskun summan kanssa, valitse erolle täsmäytyssyy.</span><span class="sxs-lookup"><span data-stu-id="01aca-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="01aca-119">Jos täsmäytyksellä on useita syitä, voit jakaa täsmäyttämättömät summan niiden kesken.</span><span class="sxs-lookup"><span data-stu-id="01aca-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="01aca-120">Täsmäytyksen syy määrittää, miten eriävät summat kirjataan kirjanpitoon.</span><span class="sxs-lookup"><span data-stu-id="01aca-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="01aca-121">Kun koko laskutussumma on täsmäytetty, se lähetetään hyväksytyksi, jonka jälkeen kirjauskansio kirjataan.</span><span class="sxs-lookup"><span data-stu-id="01aca-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="01aca-122">Seuraavassa kuvassa on esitetty, kuinka voit luoda rahtilaskun ja suorittaa rahdin täsmäytyksen.</span><span class="sxs-lookup"><span data-stu-id="01aca-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="01aca-123">[![Rahdin täsmäytystehtävät](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="01aca-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="01aca-124">Automaattinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="01aca-124">Automatic reconciliation</span></span>

<span data-ttu-id="01aca-125">Jos haluat käyttää automaattista täsmäytystä, sinun on määritettävä täsmäytysaikataulu ja käytettävät laskut ja rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="01aca-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="01aca-126">Laskurivit ja rahtilaskut täsmäytetään päätarkistuksen ja rahtilaskun tyypin asetusten mukaan.</span><span class="sxs-lookup"><span data-stu-id="01aca-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="01aca-127">Kun olet suorittanut automaattisen täsmäytyksen, sinun on käsiteltävä kaikki laskut, joita järjestelmä ei voi täsmäyttää.</span><span class="sxs-lookup"><span data-stu-id="01aca-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="01aca-128">Nämä laskut on sitten käsiteltävä manuaalisesti ennen kaikkien laskujen kirjaamista maksettaviksi.</span><span class="sxs-lookup"><span data-stu-id="01aca-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="01aca-129">Rahtikirjojen ja rahtilaskujen täsmäyttäminen automaattisella tai manuaalisella täsmäytyksellä</span><span class="sxs-lookup"><span data-stu-id="01aca-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="01aca-130">*Täsmäytys* on prosessi, jolla etsitään kutakin rahtilaskua vastaavat rahtikirjat.</span><span class="sxs-lookup"><span data-stu-id="01aca-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="01aca-131">Se voidaan tehdä täsmäyttämällä laskurivit yksi kerrallaan (manuaalinen täsmäytys) tai täsmäyttämällä kaikki käytettävissä olevat laskut kerralla (automaattinen täsmäytys).</span><span class="sxs-lookup"><span data-stu-id="01aca-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="01aca-132">Automaattinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="01aca-132">Auto matching</span></span>

<span data-ttu-id="01aca-133">Kun useita rahtilaskuja täsmäytetään samaan rahtikirjaan, automaattinen täsmäytysprosessi toimii seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="01aca-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="01aca-134">Kaikki täsmäyttämättömät rahtilaskut lajitellaan summan perusteella suurin summa ensimmäisenä.</span><span class="sxs-lookup"><span data-stu-id="01aca-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="01aca-135">Rahtilaskut täsmäytetään yksi kerrallaan, kun rahtikirjassa ei ole jäljellä positiivista summaa.</span><span class="sxs-lookup"><span data-stu-id="01aca-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="01aca-136">Päätarkastuksen asetusten ja rahtilaskujen jäljellä olevan summan perusteella määritetään jäljellä oleva summa.</span><span class="sxs-lookup"><span data-stu-id="01aca-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="01aca-137">Manuaalinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="01aca-137">Manual matching</span></span>

<span data-ttu-id="01aca-138">Kaikki rahtikirjat, joissa on positiivinen summa, voidaan täsmäyttää.</span><span class="sxs-lookup"><span data-stu-id="01aca-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="01aca-139">Automaattisen täsmäytyksen tavoin käyttäjä voi täsmäyttää vain rahtilaskut, joissa on negatiivisia summia, rahtikirjoihin, joita ei ole kokonaisuudessaan täsmäytetty.</span><span class="sxs-lookup"><span data-stu-id="01aca-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="01aca-140">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="01aca-140">Example</span></span>

<span data-ttu-id="01aca-141">Oletetaan, että rahtikirjan summa on 1 500 ja kyseiselle rahtikirjalle on luotu kolme rahtilaskua, jossa kullekin laskulle on yksi laskurivi ja seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="01aca-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="01aca-142">Alkuperäinen rahtikirja (FB): Summa 1 500</span><span class="sxs-lookup"><span data-stu-id="01aca-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="01aca-143">Lasku 1 (Inv1): Summa 1 000</span><span class="sxs-lookup"><span data-stu-id="01aca-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="01aca-144">Lasku 2 (Inv2): Summa 600</span><span class="sxs-lookup"><span data-stu-id="01aca-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="01aca-145">Lasku 3 (Inv3): Summa -100</span><span class="sxs-lookup"><span data-stu-id="01aca-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="01aca-146">Automaattisen täsmäytyksen tulos</span><span class="sxs-lookup"><span data-stu-id="01aca-146">Automatic matching result</span></span>

<span data-ttu-id="01aca-147">Automaattinen täsmäytys suoritetaan seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="01aca-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="01aca-148">Kaikki rahtilaskut lajitellaan summan mukaiseen laskevaan järjestykseen: Lasku 1 -> Lasku 2 -> Lasku 3.</span><span class="sxs-lookup"><span data-stu-id="01aca-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="01aca-149">Lasku 1 ja rahtikirja täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="01aca-149">Match Inv1 with FB.</span></span> <span data-ttu-id="01aca-150">Laskussa 1 on täsmäytetty 1 000 ja rahtikirjassa on vielä 500 täsmäyttämättä, joten tilaksi määritetään *Osittainen vastaavuus*.</span><span class="sxs-lookup"><span data-stu-id="01aca-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="01aca-151">Lasku 2 ja rahtikirja täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="01aca-151">Match Inv2 with FB.</span></span> <span data-ttu-id="01aca-152">Laskussa 2 on täsmäytetty 500 ja rahtikirjassa on vielä 0 täsmäyttämättä, joten tilaksi määritetään *Täysi vastaavuus*.</span><span class="sxs-lookup"><span data-stu-id="01aca-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="01aca-153">Koska rahtikirja on kokonaan täsmäytetty, laskua 3 ei käsitellä.</span><span class="sxs-lookup"><span data-stu-id="01aca-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="01aca-154">Manuaalisen täsmäytyksen tulos</span><span class="sxs-lookup"><span data-stu-id="01aca-154">Manual matching result</span></span>

<span data-ttu-id="01aca-155">Manuaalisen täsmäytyksen tulokset vaihtelevat täsmäytysjärjestyksen mukaan, kuten seuraavissa esimerkkitapauksissa.</span><span class="sxs-lookup"><span data-stu-id="01aca-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="01aca-156">Manuaalinen täsmäytystapaus 1</span><span class="sxs-lookup"><span data-stu-id="01aca-156">Manual matching case 1</span></span>

<span data-ttu-id="01aca-157">Manuaalinen täsmäytys voidaan tehdä esimerkiksi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="01aca-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="01aca-158">Rahtikirja ja lasku 1 täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="01aca-158">Match FB with Inv1.</span></span> <span data-ttu-id="01aca-159">Rahtikirjassa on jäljellä summa 500, joten tilaksi määritetään *Osittainen vastaavuus*.</span><span class="sxs-lookup"><span data-stu-id="01aca-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="01aca-160">Lasku 2 ja rahtikirja täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="01aca-160">Match Inv2 with FB.</span></span> <span data-ttu-id="01aca-161">Laskussa 2 on täsmäytetty 500 ja rahtikirjassa on vielä 0 täsmäyttämättä, joten tilaksi määritetään *Täysi vastaavuus*.</span><span class="sxs-lookup"><span data-stu-id="01aca-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="01aca-162">Kun lasku 3 täsmäytetään manuaalisesti, yhtään täsmäyttämätöntä rahtikirjaa ei löydy.</span><span class="sxs-lookup"><span data-stu-id="01aca-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="01aca-163">Tämä tapaus on käytännössä sama kuin automaattinen täsmäytys</span><span class="sxs-lookup"><span data-stu-id="01aca-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="01aca-164">Manuaalinen täsmäytystapaus 2</span><span class="sxs-lookup"><span data-stu-id="01aca-164">Manual matching case 2</span></span>

<span data-ttu-id="01aca-165">Manuaalinen täsmäytys voidaan tehdä myös seuraavalla tavalla:</span><span class="sxs-lookup"><span data-stu-id="01aca-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="01aca-166">Lasku 3 ja rahtikirja täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="01aca-166">Match Inv3 with FB.</span></span> <span data-ttu-id="01aca-167">Rahtikirjan jäljellä oleva summa on nyt 1 600, joka vastaa negatiivisen 100:n vähentämistä 1 500:sta.</span><span class="sxs-lookup"><span data-stu-id="01aca-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="01aca-168">Sekä rahtikirjan että laskun 3 täsmäytetty määrä on -100.</span><span class="sxs-lookup"><span data-stu-id="01aca-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="01aca-169">Lasku 1 ja lasku 2 täsmäytetään rahtikirjaan peräkkäin.</span><span class="sxs-lookup"><span data-stu-id="01aca-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="01aca-170">Rahtikirjan on kokonaan täsmäytetty.</span><span class="sxs-lookup"><span data-stu-id="01aca-170">FB is fully matched.</span></span>

<span data-ttu-id="01aca-171">Tämä esimerkki osoittaa, että negatiivisia summia sisältävien rahtilaskujen täsmäyttäminen on tehtävä vain manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="01aca-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="01aca-172">Näin varmistetaan, että negatiivisia summia sisältävät rahtilaskut voidaan aina täsmäyttää rahtikirjaan, jota ei ole kokonaan täsmäytetty, koska tällä tavoin täsmäytysjärjestystä voidaan hallita.</span><span class="sxs-lookup"><span data-stu-id="01aca-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>
