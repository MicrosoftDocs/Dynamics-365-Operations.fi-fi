---
title: Käänteinen kirjauskansion kirjaus
description: Tässä aiheessa kuvataan ominaisuuksia, joiden avulla voit muuttaa tositteita käänteisiksi tositetapahtumien luettelosta tai talouskirjauskansioista.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 586c0f807cf45908bacd88ff4e4d5793db054e4d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815401"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="b33f1-103">Käänteinen kirjauskansion kirjaus</span><span class="sxs-lookup"><span data-stu-id="b33f1-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b33f1-104">Tässä aiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, joiden avulla voit muuttaa koko kirjauskansion tai yhden tai useamman tositteen käänteiseksi tositetapahtumien luettelosta riippumatta niiden alkuperästä.</span><span class="sxs-lookup"><span data-stu-id="b33f1-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="b33f1-105">Kirjauskansioiden muuttaminen käänteiseksi</span><span class="sxs-lookup"><span data-stu-id="b33f1-105">Reversing journals</span></span>

<span data-ttu-id="b33f1-106">Voit muuttaa kirjauskansion rivejä käänteisiksi yksittäin.</span><span class="sxs-lookup"><span data-stu-id="b33f1-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="b33f1-107">Käänteisen kirjauskansion kirjauksen avulla voit myös muuttaa koko talouskirjauskansion käänteiseksi.</span><span class="sxs-lookup"><span data-stu-id="b33f1-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="b33f1-108">Kirjauskansion muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="b33f1-108">To reverse a journal:</span></span> 

- <span data-ttu-id="b33f1-109">Avaa talouskirjauskansio ja suodata kirjattujen kirjauskansioiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="b33f1-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="b33f1-110">Valitse **Käänteinen**-valikko sivun ylälaidasta.</span><span class="sxs-lookup"><span data-stu-id="b33f1-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="b33f1-111">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="b33f1-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="b33f1-112">Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="b33f1-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b33f1-113">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="b33f1-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="b33f1-114">Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="b33f1-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b33f1-115">Kirjoita kommentti, jonka haluat lisätä käänteiseksi muuttamisen tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="b33f1-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="b33f1-116">Valitse **Käänteinen**-painike.</span><span class="sxs-lookup"><span data-stu-id="b33f1-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="b33f1-117">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="b33f1-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="b33f1-118">Jos tositteessa on yli 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="b33f1-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b33f1-119">Voit tarkistaa tulokset lukemalla erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="b33f1-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b33f1-120">Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.</span><span class="sxs-lookup"><span data-stu-id="b33f1-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="b33f1-121">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="b33f1-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b33f1-122">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voi muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="b33f1-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="b33f1-123">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33f1-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="b33f1-124">Tositteiden muuttaminen käänteiseksi tositetapahtumien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b33f1-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="b33f1-125">Voit muuttaa tositteita käänteisiksi myös minkä tahansa alareskontran **tositetapahtumien luettelosta**.</span><span class="sxs-lookup"><span data-stu-id="b33f1-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="b33f1-126">Lisäksi voit muuntaa useita tositteita käänteisiksi kerralla.</span><span class="sxs-lookup"><span data-stu-id="b33f1-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="b33f1-127">Yhden tai usean tositteen muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="b33f1-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="b33f1-128">Valitse **Käänteinen**-valikko sivun ylälaidasta</span><span class="sxs-lookup"><span data-stu-id="b33f1-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="b33f1-129">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="b33f1-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="b33f1-130">Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="b33f1-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="b33f1-131">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="b33f1-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="b33f1-132">Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="b33f1-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="b33f1-133">Kirjoita kommentti kuvaamaan käänteiseksi muuttamisen tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="b33f1-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="b33f1-134">Valitse **Käänteinen**-painike.</span><span class="sxs-lookup"><span data-stu-id="b33f1-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="b33f1-135">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="b33f1-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="b33f1-136">Jos tositerivejä on yli 100, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="b33f1-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="b33f1-137">Voit tarkistaa tulokset lukemalla erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="b33f1-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="b33f1-138">Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.</span><span class="sxs-lookup"><span data-stu-id="b33f1-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="b33f1-139">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="b33f1-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="b33f1-140">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voitu muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="b33f1-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="b33f1-141">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="b33f1-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="b33f1-142">Tapahtumia voidaan muuttaa käänteiseksi vain, jos ne täyttävät käänteiseksi muuttamisen liiketoimintasäännöt.</span><span class="sxs-lookup"><span data-stu-id="b33f1-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="b33f1-143">Toimittajamaksuja ei voida muuttaa käänteiseksi tässä aiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="b33f1-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="b33f1-144">Toimittajamaksut on muutettava käänteiseksi kohdassa [Toimittajamaksun käänteiseksi muuttaminen](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="b33f1-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]