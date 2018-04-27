---
title: Toimittajan maksut osasummalla
description: "Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa. Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aeef806980665c523f10b373f7662ecf509a8172
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="e86dd-105">Toimittajan maksut osasummalla</span><span class="sxs-lookup"><span data-stu-id="e86dd-105">Vendor payments for a partial amount</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e86dd-106">Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi.</span><span class="sxs-lookup"><span data-stu-id="e86dd-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="e86dd-107">Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="e86dd-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="e86dd-108">Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan.</span><span class="sxs-lookup"><span data-stu-id="e86dd-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="e86dd-109">Käteisalennussummat</span><span class="sxs-lookup"><span data-stu-id="e86dd-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="e86dd-110">Toimittaja voi tarjota yrityksellesi käteisalennuksen, jos maksat laskun ennen eräpäivää.</span><span class="sxs-lookup"><span data-stu-id="e86dd-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="e86dd-111">Voit syöttää esimerkiksi laskun summaksi 100,00, jolle määritetään 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="e86dd-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="e86dd-112">Maksuehto on 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="e86dd-112">The due date terms are 30 days.</span></span> <span data-ttu-id="e86dd-113">Jos maksuehdotuksessa käytetään käteisalennusta ehtona laskun valinnalle, ja jos ehdotus ajetaan käteisalennuspäivämääränä tai sitä ennen, lasku valitaan maksettavaksi ja maksu luodaan arvolle 98,00.</span><span class="sxs-lookup"><span data-stu-id="e86dd-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="e86dd-114">Käteisalennusta voi myös käyttää yksittäiselle, manuaalisesti luodulle maksulle.</span><span class="sxs-lookup"><span data-stu-id="e86dd-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="e86dd-115">Osamaksut käteisalennuksella</span><span class="sxs-lookup"><span data-stu-id="e86dd-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="e86dd-116">Kun suoritat osamaksun, suunnitelmana voi olla suorittaa toinen osamaksu laskun loppuun maksamiseksi.</span><span class="sxs-lookup"><span data-stu-id="e86dd-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="e86dd-117">Jos haluat käyttää käteisalennusta osittaismaksussa, sinun on määritettävä <strong>Laske käteisalennukset osamaksuille **-asetukseksi **Kyllä</strong> <strong>Ostoreskontran parametrit</strong> -sivulla.</span><span class="sxs-lookup"><span data-stu-id="e86dd-117">To take a cash discount for a partial payment, you must set the <strong>Calculate cash discounts for partial payments **option to **Yes</strong> on the <strong>Account payable parameters</strong> page.</span></span> 

<span data-ttu-id="e86dd-118">Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista.</span><span class="sxs-lookup"><span data-stu-id="e86dd-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="e86dd-119">Laskun arvoksi on kirjattu 100,00.</span><span class="sxs-lookup"><span data-stu-id="e86dd-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="e86dd-120">Jos suoritat maksun summalla 49,00 10 päivän kuluessa, kirjaat maksuksi 49,00 maksujen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="e86dd-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="e86dd-121">Kun täsmäytät osamaksun **Selvitä avoimet tapahtumat** -sivulla, **1,00** näkyy **Käytettävä käteisalennussumma** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e86dd-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="e86dd-122">Jos kirjaat osamaksun ja jätät koko laskusumman **Täsmäytettävä summa** -kenttään, **Käytettävä käteisalennussumma** -kenttä lasketaan uudelleen automaattisesti, kun kirjaat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="e86dd-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="e86dd-123">Hyvityslaskut ja käteisalennukset</span><span class="sxs-lookup"><span data-stu-id="e86dd-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="e86dd-124">Saatat palauttaa laskulla olevia nimikkeitä ja saada niistä hyvityslaskun.</span><span class="sxs-lookup"><span data-stu-id="e86dd-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="e86dd-125">Jos käteisalennusta oli käytetty alkuperäisellä laskulla, voit vähentää alennuksen arvon ja saada palautuksen oikealle summalle.</span><span class="sxs-lookup"><span data-stu-id="e86dd-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="e86dd-126">Jos <strong>Laske käteisalennukset hyvityslaskuille **-asetukseksi on määritetty **Kyllä</strong> <strong>Ostoreskontran parametrit</strong> -sivulla, alennus lasketaan automaattisesti hyvityslaskulle.</span><span class="sxs-lookup"><span data-stu-id="e86dd-126">If the <strong>Calculate cash discounts for credit notes **option is set to **Yes</strong> on the <strong>Accounts payable parameters</strong> page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="e86dd-127">Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista.</span><span class="sxs-lookup"><span data-stu-id="e86dd-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="e86dd-128">Laskun kirjataan arvolla 100,00.</span><span class="sxs-lookup"><span data-stu-id="e86dd-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="e86dd-129">Jos palautat tavarat ja vastaanotat hyvityslaskun, voit syöttää hyvityslaskun kokonaisuudessaan alkuperäisen laskun summalle, 100,00, mukaan lukien 2 prosentin käteisalennus, joka on myös määritetty hyvityslaskulla.</span><span class="sxs-lookup"><span data-stu-id="e86dd-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="e86dd-130">Kun tarkastelet hyvityslaskua **Tilitä tapahtumat** -sivulla, **98,00** näkyy **Tilitettävä summa** -kentässä ja **-2,00** näkyy **Käteisalennuksen summa** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="e86dd-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="e86dd-131">Alennussumma kirjataan käteisalennustilille.</span><span class="sxs-lookup"><span data-stu-id="e86dd-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="e86dd-132">Liika-/alisuorituksen summat</span><span class="sxs-lookup"><span data-stu-id="e86dd-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="e86dd-133">Voit suorittaa osamaksun, jonka jälkeen tilitettäväksi voi jäädä hyvin pieni summa.</span><span class="sxs-lookup"><span data-stu-id="e86dd-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="e86dd-134">Toimittajan laskun summa on esimerkiksi 1 000,00 ja suoritat maksun summalle 999,90.</span><span class="sxs-lookup"><span data-stu-id="e86dd-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="e86dd-135">Jos jäljelle jäävä summa on pienempi kuin liika-/alisuorituksen summa, joka on määritetty **Ostoreskontran parametrit** -sivulla, erotus kirjataan automaattisesti liika-/alisuorituksien kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="e86dd-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="e86dd-136">Lisätietoja on ohjeaiheessa [Toimittajan maksujen yleiskatsaus](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e86dd-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

