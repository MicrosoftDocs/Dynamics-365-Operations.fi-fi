---
title: Toimittajan maksut osasummalla
description: Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi. Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89e025977a0dcd40e35f17448a7b0ebde08cb6c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177597"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="c17f6-104">Toimittajan maksut osasummalle</span><span class="sxs-lookup"><span data-stu-id="c17f6-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c17f6-105">Joskus toimittajalle saatetaan luoda maksu, jonka summa on laskun summaa pienempi.</span><span class="sxs-lookup"><span data-stu-id="c17f6-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="c17f6-106">Tässä artikkelissa on kuvaus erilaisista toimintavaihtoehdoista tällaisessa tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="c17f6-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="c17f6-107">Käytettävissä olevat vaihtoehdot määräytyvät liiketoiminnan vaatimusten ja konfiguraation mukaan.</span><span class="sxs-lookup"><span data-stu-id="c17f6-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="c17f6-108">Käteisalennussummat</span><span class="sxs-lookup"><span data-stu-id="c17f6-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="c17f6-109">Toimittaja voi tarjota yrityksellesi käteisalennuksen, jos maksat laskun ennen eräpäivää.</span><span class="sxs-lookup"><span data-stu-id="c17f6-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="c17f6-110">Voit syöttää esimerkiksi laskun summaksi 100,00, jolle määritetään 2 prosentin käteisalennus, jos lasku maksetaan 10 päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="c17f6-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="c17f6-111">Maksuehto on 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="c17f6-111">The due date terms are 30 days.</span></span> <span data-ttu-id="c17f6-112">Jos maksuehdotuksessa käytetään käteisalennusta ehtona laskun valinnalle, ja jos ehdotus ajetaan käteisalennuspäivämääränä tai sitä ennen, lasku valitaan maksettavaksi ja maksu luodaan arvolle 98,00.</span><span class="sxs-lookup"><span data-stu-id="c17f6-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="c17f6-113">Käteisalennusta voi myös käyttää yksittäiselle, manuaalisesti luodulle maksulle.</span><span class="sxs-lookup"><span data-stu-id="c17f6-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="c17f6-114">Osamaksut käteisalennuksella</span><span class="sxs-lookup"><span data-stu-id="c17f6-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="c17f6-115">Kun suoritat osamaksun, suunnitelmana voi olla suorittaa toinen osamaksu laskun loppuun maksamiseksi.</span><span class="sxs-lookup"><span data-stu-id="c17f6-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="c17f6-116">Jos haluat käyttää käteisalennusta osittaismaksussa, sinun on määritettävä **Laske käteisalennukset osamaksuille** -asetukseksi **Kyllä** **Ostoreskontran parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="c17f6-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="c17f6-117">Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista.</span><span class="sxs-lookup"><span data-stu-id="c17f6-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="c17f6-118">Laskun arvoksi on kirjattu 100,00.</span><span class="sxs-lookup"><span data-stu-id="c17f6-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="c17f6-119">Jos suoritat maksun summalla 49,00 10 päivän kuluessa, kirjaat maksuksi 49,00 maksujen kirjauskansioon.</span><span class="sxs-lookup"><span data-stu-id="c17f6-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="c17f6-120">Kun täsmäytät osamaksun **Selvitä avoimet tapahtumat** -sivulla, **1,00** näkyy **Käytettävä käteisalennussumma** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c17f6-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c17f6-121">Jos kirjaat osamaksun ja jätät koko laskusumman **Täsmäytettävä summa** -kenttään, **Käytettävä käteisalennussumma** -kenttä lasketaan uudelleen automaattisesti, kun kirjaat tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="c17f6-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="c17f6-122">Hyvityslaskut ja käteisalennukset</span><span class="sxs-lookup"><span data-stu-id="c17f6-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="c17f6-123">Saatat palauttaa laskulla olevia nimikkeitä ja saada niistä hyvityslaskun.</span><span class="sxs-lookup"><span data-stu-id="c17f6-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="c17f6-124">Jos käteisalennusta oli käytetty alkuperäisellä laskulla, voit vähentää alennuksen arvon ja saada palautuksen oikealle summalle.</span><span class="sxs-lookup"><span data-stu-id="c17f6-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="c17f6-125">Jos **Laske käteisalennukset hyvityslaskuille** -asetukseksi on määritetty **Kyllä** **Ostoreskontran parametrit** -sivulla, alennus lasketaan automaattisesti hyvityslaskulle.</span><span class="sxs-lookup"><span data-stu-id="c17f6-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="c17f6-126">Saat esimerkin mukaisesti 2 prosentin käteisalennuksen, jos lasku maksetaan 10 päivän kuluessa sen luonnista.</span><span class="sxs-lookup"><span data-stu-id="c17f6-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="c17f6-127">Laskun kirjataan arvolla 100,00.</span><span class="sxs-lookup"><span data-stu-id="c17f6-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="c17f6-128">Jos palautat tavarat ja vastaanotat hyvityslaskun, voit syöttää hyvityslaskun kokonaisuudessaan alkuperäisen laskun summalle, 100,00, mukaan lukien 2 prosentin käteisalennus, joka on myös määritetty hyvityslaskulla.</span><span class="sxs-lookup"><span data-stu-id="c17f6-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="c17f6-129">Kun tarkastelet hyvityslaskua **Tilitä tapahtumat** -sivulla, **98,00** näkyy **Tilitettävä summa** -kentässä ja **-2,00** näkyy **Käteisalennuksen summa** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="c17f6-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="c17f6-130">Alennussumma kirjataan käteisalennustilille.</span><span class="sxs-lookup"><span data-stu-id="c17f6-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="c17f6-131">Liika-/alisuorituksen summat</span><span class="sxs-lookup"><span data-stu-id="c17f6-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="c17f6-132">Voit suorittaa osamaksun, jonka jälkeen tilitettäväksi voi jäädä hyvin pieni summa.</span><span class="sxs-lookup"><span data-stu-id="c17f6-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="c17f6-133">Toimittajan laskun summa on esimerkiksi 1 000,00 ja suoritat maksun summalle 999,90.</span><span class="sxs-lookup"><span data-stu-id="c17f6-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="c17f6-134">Jos jäljelle jäävä summa on pienempi kuin liika-/alisuorituksen summa, joka on määritetty **Ostoreskontran parametrit** -sivulla, erotus kirjataan automaattisesti liika-/alisuorituksien kirjanpitotilille.</span><span class="sxs-lookup"><span data-stu-id="c17f6-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="c17f6-135">Lisätietoja on ohjeaiheessa [Toimittajan maksujen yleiskatsaus](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c17f6-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>
