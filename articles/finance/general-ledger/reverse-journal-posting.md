---
title: Käänteinen kirjauskansion kirjaus
description: Tässä aiheessa kuvataan ominaisuuksia, joiden avulla voit muuttaa tositteita käänteisiksi tositetapahtumien luettelosta tai talouskirjauskansioista.
author: MikeFalkner
manager: AnnBe
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3244d857a9135249130672501f8b766ff9a0680
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442778"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="85225-103">Käänteinen kirjauskansion kirjaus</span><span class="sxs-lookup"><span data-stu-id="85225-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85225-104">Tässä aiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, joiden avulla voit muuttaa koko kirjauskansion tai yhden tai useamman tositteen käänteiseksi tositetapahtumien luettelosta riippumatta niiden alkuperästä.</span><span class="sxs-lookup"><span data-stu-id="85225-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="85225-105">Kirjauskansioiden muuttaminen käänteiseksi</span><span class="sxs-lookup"><span data-stu-id="85225-105">Reversing journals</span></span>

<span data-ttu-id="85225-106">Voit muuttaa kirjauskansion rivejä käänteisiksi yksittäin.</span><span class="sxs-lookup"><span data-stu-id="85225-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="85225-107">Käänteisen kirjauskansion kirjauksen avulla voit myös muuttaa koko talouskirjauskansion käänteiseksi.</span><span class="sxs-lookup"><span data-stu-id="85225-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="85225-108">Kirjauskansion muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="85225-108">To reverse a journal:</span></span> 

- <span data-ttu-id="85225-109">Avaa talouskirjauskansio ja suodata kirjattujen kirjauskansioiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="85225-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="85225-110">Valitse **Käänteinen**-valikko sivun ylälaidasta.</span><span class="sxs-lookup"><span data-stu-id="85225-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="85225-111">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="85225-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="85225-112">Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="85225-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="85225-113">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="85225-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="85225-114">Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="85225-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="85225-115">Kirjoita kommentti, jonka haluat lisätä käänteiseksi muuttamisen tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="85225-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="85225-116">Valitse **Käänteinen**-painike.</span><span class="sxs-lookup"><span data-stu-id="85225-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="85225-117">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="85225-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="85225-118">Jos tositteessa on yli 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="85225-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="85225-119">Voit tarkistaa tulokset lukemalla erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="85225-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="85225-120">Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.</span><span class="sxs-lookup"><span data-stu-id="85225-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="85225-121">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="85225-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="85225-122">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voi muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="85225-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="85225-123">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="85225-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="85225-124">Tositteiden muuttaminen käänteiseksi tositetapahtumien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="85225-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="85225-125">Voit muuttaa tositteita käänteisiksi myös minkä tahansa alareskontran **tositetapahtumien luettelosta**.</span><span class="sxs-lookup"><span data-stu-id="85225-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="85225-126">Lisäksi voit muuntaa useita tositteita käänteisiksi kerralla.</span><span class="sxs-lookup"><span data-stu-id="85225-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="85225-127">Yhden tai usean tositteen muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="85225-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="85225-128">Valitse **Käänteinen**-valikko sivun ylälaidasta</span><span class="sxs-lookup"><span data-stu-id="85225-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="85225-129">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="85225-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="85225-130">Valitse **Kyllä** käyttääksesi olemassa olevia tapahtumapäiviä tai **Ei** luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="85225-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="85225-131">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja sinun on syötettävä uusi tapahtumapäivä käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="85225-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="85225-132">Jos valitsit **Ei**, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="85225-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="85225-133">Kirjoita kommentti kuvaamaan käänteiseksi muuttamisen tapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="85225-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="85225-134">Valitse **Käänteinen**-painike.</span><span class="sxs-lookup"><span data-stu-id="85225-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="85225-135">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="85225-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="85225-136">Jos tositerivejä on yli 100, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="85225-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="85225-137">Voit tarkistaa tulokset lukemalla erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="85225-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="85225-138">Tapahtumat, joita ei voitu muuttaa käänteiseksi, luetellaan erätyön historiassa.</span><span class="sxs-lookup"><span data-stu-id="85225-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="85225-139">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="85225-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="85225-140">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voitu muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="85225-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="85225-141">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="85225-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="85225-142">Tapahtumia voidaan muuttaa käänteiseksi vain, jos ne täyttävät käänteiseksi muuttamisen liiketoimintasäännöt.</span><span class="sxs-lookup"><span data-stu-id="85225-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="85225-143">Toimittajamaksuja ei voida muuttaa käänteiseksi tässä aiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="85225-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="85225-144">Toimittajamaksut on muutettava käänteiseksi kohdassa [Toimittajamaksun käänteiseksi muuttaminen](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment) esitetyllä tavalla.</span><span class="sxs-lookup"><span data-stu-id="85225-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](https://docs.microsoft.com/dynamics365/finance/accounts-payable/reverse-vendor-payment).</span></span>

