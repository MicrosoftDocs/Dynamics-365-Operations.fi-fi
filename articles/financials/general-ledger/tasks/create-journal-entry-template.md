---
title: Kirjauskansioviennin luonti mallin avulla
description: Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a749740b62e39202d502a112f947679f85ca085
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562495"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="055cd-103">Kirjauskansioviennin luonti mallin avulla</span><span class="sxs-lookup"><span data-stu-id="055cd-103">Create a journal entry using template</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="055cd-104">Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen.</span><span class="sxs-lookup"><span data-stu-id="055cd-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="055cd-105">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="055cd-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="055cd-106">Kirjanpito > Kirjauskansioviennit > Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="055cd-106">General ledger > Journal entries > General journals.</span></span> <span data-ttu-id="055cd-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="055cd-107">Click New.</span></span>
    * <span data-ttu-id="055cd-108">Tämä menettely käynnistyy kirjauskansion tositteen luomisella ja kirjaamisella. Myös aiemmin kirjattu kirjauskansion tosite voidaan tallentaa mallina.</span><span class="sxs-lookup"><span data-stu-id="055cd-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
2. <span data-ttu-id="055cd-109">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="055cd-109">In the Name field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="055cd-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="055cd-110">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="055cd-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="055cd-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="055cd-112">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="055cd-112">Click Lines.</span></span>
6. <span data-ttu-id="055cd-113">Syötä tilityypin tili.</span><span class="sxs-lookup"><span data-stu-id="055cd-113">Enter an account for the Account type.</span></span>
7. <span data-ttu-id="055cd-114">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="055cd-114">In the Description field, type a value.</span></span>
8. <span data-ttu-id="055cd-115">Syötä summa Debet-kenttään.</span><span class="sxs-lookup"><span data-stu-id="055cd-115">Enter an amount in the Debit field.</span></span>
9. <span data-ttu-id="055cd-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="055cd-116">Click New.</span></span>
10. <span data-ttu-id="055cd-117">Syötä tilityypille toinen tili.</span><span class="sxs-lookup"><span data-stu-id="055cd-117">Enter a different account for the Account type.</span></span>
11. <span data-ttu-id="055cd-118">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="055cd-118">In the Description field, type a value.</span></span>
12. <span data-ttu-id="055cd-119">Syötä summa Debet-kenttään.</span><span class="sxs-lookup"><span data-stu-id="055cd-119">Enter an amount in the Debit field.</span></span>
13. <span data-ttu-id="055cd-120">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="055cd-120">Click New.</span></span>
14. <span data-ttu-id="055cd-121">Määritä Tili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="055cd-121">In the Account field, specify the desired values.</span></span>
15. <span data-ttu-id="055cd-122">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="055cd-122">In the Description field, type a value.</span></span>
16. <span data-ttu-id="055cd-123">Oikaise tositteen saldo syöttämällä summa Kredit-kenttään.</span><span class="sxs-lookup"><span data-stu-id="055cd-123">Enter an amount in the Credit field to balance the voucher.</span></span>
17. <span data-ttu-id="055cd-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="055cd-124">Click Post.</span></span>
18. <span data-ttu-id="055cd-125">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="055cd-125">Click Functions.</span></span>
19. <span data-ttu-id="055cd-126">Valitse Tallenna tositemalli.</span><span class="sxs-lookup"><span data-stu-id="055cd-126">Click Save voucher template.</span></span>
20. <span data-ttu-id="055cd-127">Tässä menettelyssä oletetaan, että tyyppi on Prosenttimalli.</span><span class="sxs-lookup"><span data-stu-id="055cd-127">This procedure assumes a Percent Template type.</span></span> <span data-ttu-id="055cd-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="055cd-128">Click OK.</span></span>
    * <span data-ttu-id="055cd-129">• Prosentti: Tositteen summat muunnetaan prosenttikertoimiksi. Näin mikä tahansa summa voidaan kohdistaa, kun tositemalli valitaan.</span><span class="sxs-lookup"><span data-stu-id="055cd-129">• Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>  <span data-ttu-id="055cd-130">• Summa: Toteutuneet summat tallennetaan ja kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="055cd-130">• Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="055cd-131">Valitse Yleiset kirjauskansiot.</span><span class="sxs-lookup"><span data-stu-id="055cd-131">Click General journals.</span></span>
22. <span data-ttu-id="055cd-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="055cd-132">Click New.</span></span>
23. <span data-ttu-id="055cd-133">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="055cd-133">In the Name field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="055cd-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="055cd-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="055cd-135">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="055cd-135">Click Lines.</span></span>
26. <span data-ttu-id="055cd-136">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="055cd-136">Click Functions.</span></span>
27. <span data-ttu-id="055cd-137">Valitse Valitse tositemalli.</span><span class="sxs-lookup"><span data-stu-id="055cd-137">Click Select voucher template.</span></span>
28. <span data-ttu-id="055cd-138">Etsi aiemmin luomasi malli.</span><span class="sxs-lookup"><span data-stu-id="055cd-138">Find the template that you created earlier.</span></span> <span data-ttu-id="055cd-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="055cd-139">Click OK.</span></span>
    * <span data-ttu-id="055cd-140">Sinun on ehkä valittava Edellinen vaihe ja valittava sitten oikea malli, jos muita malleja on olemassa.</span><span class="sxs-lookup"><span data-stu-id="055cd-140">You may need to click Previous step and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="055cd-141">Syötä Summa-kenttään tositteeseen kohdistettava summa.</span><span class="sxs-lookup"><span data-stu-id="055cd-141">In the Amount field, enter the amount to be applied to the voucher.</span></span>
    * <span data-ttu-id="055cd-142">Summakenttä näytetään vain, jos tositemallin tyyppi on Prosentti.</span><span class="sxs-lookup"><span data-stu-id="055cd-142">The amount field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="055cd-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="055cd-143">Click OK.</span></span>

