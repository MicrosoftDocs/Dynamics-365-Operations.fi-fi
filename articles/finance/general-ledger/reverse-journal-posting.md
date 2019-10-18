---
title: Käänteinen kirjauskansion kirjaus
description: Tässä aiheessa kuvataan ominaisuuksia, joiden avulla voit muuttaa tositteita käänteisiksi tositetapahtumien luettelosta tai talouskirjauskansioista.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248582"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="4ad59-103">Käänteinen kirjauskansion kirjaus</span><span class="sxs-lookup"><span data-stu-id="4ad59-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ad59-104">Tässä aiheessa kuvataan Microsoft Dynamics 365 Finance -ominaisuuksia, joiden avulla voit muuttaa koko kirjauskansion tai yhden tai useamman tositteen käänteiseksi tositetapahtumien luettelosta riippumatta niiden alkuperästä.</span><span class="sxs-lookup"><span data-stu-id="4ad59-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="4ad59-105">Kirjauskansioiden muuttaminen käänteiseksi</span><span class="sxs-lookup"><span data-stu-id="4ad59-105">Reversing journals</span></span>

<span data-ttu-id="4ad59-106">Voit muuttaa kirjauskansion rivejä käänteisiksi yksittäin.</span><span class="sxs-lookup"><span data-stu-id="4ad59-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="4ad59-107">Käänteisen kirjauskansion kirjauksen avulla voit myös muuttaa koko talouskirjauskansion käänteiseksi.</span><span class="sxs-lookup"><span data-stu-id="4ad59-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="4ad59-108">Kirjauskansion muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="4ad59-108">To reverse a journal:</span></span> 
- <span data-ttu-id="4ad59-109">Avaa talouskirjauskansio ja suodata kirjattujen kirjauskansioiden mukaan</span><span class="sxs-lookup"><span data-stu-id="4ad59-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="4ad59-110">Valitse Käänteinen-valikko sivun ylälaidasta.</span><span class="sxs-lookup"><span data-stu-id="4ad59-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="4ad59-111">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="4ad59-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="4ad59-112">Valitse Kyllä käyttääksesi olemassa olevia tapahtumapäiviä tai Ei luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="4ad59-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="4ad59-113">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja haluat syöttää uuden tapahtumapäivän käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="4ad59-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="4ad59-114">Jos valitsit Ei, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="4ad59-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="4ad59-115">Kirjoita kommentti, jonka haluat lisätä käänteiseksi muuttamisen tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="4ad59-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="4ad59-116">Napsauta Käänteinen-painiketta</span><span class="sxs-lookup"><span data-stu-id="4ad59-116">Click the Reverse button</span></span>

<span data-ttu-id="4ad59-117">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="4ad59-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="4ad59-118">Jos tositteessa on yli 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="4ad59-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="4ad59-119">Voit tarkistaa käänteiseksi muuttamisen tulokset lukemalla suoritetun erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="4ad59-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="4ad59-120">Kaikki virheet kirjataan erätyöhistoriaan.</span><span class="sxs-lookup"><span data-stu-id="4ad59-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="4ad59-121">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="4ad59-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="4ad59-122">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voi muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="4ad59-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="4ad59-123">Sulje valintaikkuna valitsemalla Ok.</span><span class="sxs-lookup"><span data-stu-id="4ad59-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="4ad59-124">Tositteiden muuttaminen käänteiseksi tositetapahtumien luettelosta.</span><span class="sxs-lookup"><span data-stu-id="4ad59-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="4ad59-125">Voit muuttaa tositteita käänteisiksi myös minkä tahansa alareskontran **tositetapahtumien luettelosta**.</span><span class="sxs-lookup"><span data-stu-id="4ad59-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="4ad59-126">Lisäksi voit muuntaa useita tositteita käänteisiksi kerralla.</span><span class="sxs-lookup"><span data-stu-id="4ad59-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="4ad59-127">Yhden tai usean tositteen muuttaminen käänteiseksi:</span><span class="sxs-lookup"><span data-stu-id="4ad59-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="4ad59-128">Valitse Käänteinen-valikko sivun ylälaidasta.</span><span class="sxs-lookup"><span data-stu-id="4ad59-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="4ad59-129">Näet tositteiden ja tositerivien kokonaismäärän sekä käänteiseksi muunnettavien rivien kokonaissumman.</span><span class="sxs-lookup"><span data-stu-id="4ad59-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="4ad59-130">Valitse Kyllä käyttääksesi olemassa olevia tapahtumapäiviä tai Ei luodaksesi uuden.</span><span class="sxs-lookup"><span data-stu-id="4ad59-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="4ad59-131">Joissakin tapauksissa alkuperäisen tapahtuman ajanjakso voi olla suljettu, ja haluat syöttää uuden tapahtumapäivän käänteiseksi muuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="4ad59-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="4ad59-132">Jos valitsit Ei, syötä tapahtumapäivä käänteiseksi muutamista varten.</span><span class="sxs-lookup"><span data-stu-id="4ad59-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="4ad59-133">Kirjoita kommentti, jonka haluat lisätä käänteiseksi muuttamisen tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="4ad59-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="4ad59-134">Napsauta Käänteinen-painiketta</span><span class="sxs-lookup"><span data-stu-id="4ad59-134">Click the Reverse button</span></span>

<span data-ttu-id="4ad59-135">Tapahtumat muutetaan käänteisiksi.</span><span class="sxs-lookup"><span data-stu-id="4ad59-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="4ad59-136">Jos tositteessa on yli 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan eräkäsittelyn avulla.</span><span class="sxs-lookup"><span data-stu-id="4ad59-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="4ad59-137">Voit tarkistaa käänteiseksi muuttamisen tulokset lukemalla suoritetun erätyön kommentit.</span><span class="sxs-lookup"><span data-stu-id="4ad59-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="4ad59-138">Kaikki virheet kirjataan erätyöhistoriaan.</span><span class="sxs-lookup"><span data-stu-id="4ad59-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="4ad59-139">Jos tositteessa on enintään 100 riviä, käänteiseksi muuttamisen prosessi suoritetaan heti.</span><span class="sxs-lookup"><span data-stu-id="4ad59-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="4ad59-140">Tulokset esitetään valintaikkunassa. Näet kaikki tositteet, joita ei voi muuttaa käänteiseksi, sekä epäonnistumisen syyn.</span><span class="sxs-lookup"><span data-stu-id="4ad59-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="4ad59-141">Sulje valintaikkuna valitsemalla Ok.</span><span class="sxs-lookup"><span data-stu-id="4ad59-141">Click on Ok to close the dialog.</span></span>

