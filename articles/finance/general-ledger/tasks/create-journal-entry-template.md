---
title: Kirjauskansioviennin luonti mallin avulla
description: Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6a3ec1d04515106d7e391834ec646f957cbc03b0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837030"
---
# <a name="create-a-journal-entry-using-template"></a><span data-ttu-id="6bb4d-103">Kirjauskansioviennin luonti mallin avulla</span><span class="sxs-lookup"><span data-stu-id="6bb4d-103">Create a journal entry using template</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6bb4d-104">Kirjatut kirjauskansion tositteet voidaan tallentaa tositemalleina. Ne voidaan kohdistaa uuteen kirjauskansion tositteeseen.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-104">Posted journal vouchers can be saved as Voucher templates and applied in a new journal voucher.</span></span> <span data-ttu-id="6bb4d-105">Näissä toimintaohjeissa käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="6bb4d-106">Siirry kohtaan **Siirtymisruutu > Moduulit > kirjanpito > kirjauskansioviennit > Yleiset kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-106">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
2. <span data-ttu-id="6bb4d-107">Napsauta **Toimintoruudussa** **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-107">On the **Action pane**, click **New**.</span></span> <span data-ttu-id="6bb4d-108">Tämä menettely käynnistyy kirjauskansion tositteen luomisella ja kirjaamisella. Myös aiemmin kirjattu kirjauskansion tosite voidaan tallentaa mallina.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-108">This procedure starts by creating and posting a journal voucher, but any previously posted journal voucher can be saved as a template.</span></span>  
3. <span data-ttu-id="6bb4d-109">Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-109">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6bb4d-110">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6bb4d-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6bb4d-112">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-112">Click **Lines**.</span></span>
7. <span data-ttu-id="6bb4d-113">Kirjoita arvo **Tilityyppi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-113">In the **Account type** field, type a value.</span></span>
8. <span data-ttu-id="6bb4d-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-114">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="6bb4d-115">Kirjoita arvo kenttään **Debet**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-115">In the **Debit** field, type a value.</span></span>
10. <span data-ttu-id="6bb4d-116">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-116">Click **New**.</span></span>
11. <span data-ttu-id="6bb4d-117">Kirjoita arvo **Tilityyppi** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-117">In the **Account type** field, type a value.</span></span>
12. <span data-ttu-id="6bb4d-118">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-118">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="6bb4d-119">Kirjoita arvo kenttään **Debet**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-119">In the **Debit** field, type a value.</span></span>
14. <span data-ttu-id="6bb4d-120">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-120">Click **New**.</span></span>
14. <span data-ttu-id="6bb4d-121">Määritä **Tili**-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-121">In the **Account** field, specify the desired values.</span></span>
15. <span data-ttu-id="6bb4d-122">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-122">In the **Description** field, type a value.</span></span>
16. <span data-ttu-id="6bb4d-123">Oikaise tositteen saldo syöttämällä arvo **Kredit**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-123">In the **Credit** field, type a value to balance the voucher.</span></span>
17. <span data-ttu-id="6bb4d-124">Valitse **toimintoruudussa** **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-124">On the **Action pane**, click **Post**.</span></span>
18. <span data-ttu-id="6bb4d-125">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-125">Click **Functions**.</span></span>
19. <span data-ttu-id="6bb4d-126">Valitse **Tallenna tosite** -malli.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-126">Click **Save voucher** template.</span></span>
20. <span data-ttu-id="6bb4d-127">Tässä menettelyssä oletetaan, että tyyppi on **Prosenttimalli**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-127">This procedure assumes a **Percent Template** type.</span></span> <span data-ttu-id="6bb4d-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-128">Click OK.</span></span>
    - <span data-ttu-id="6bb4d-129">Prosentti: Tositteen summat muunnetaan prosenttikertoimiksi. Näin mikä tahansa summa voidaan kohdistaa, kun tositemalli valitaan.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-129">Percent: The amounts in the voucher are converted into percentage factors, which allows any amount to be applied when the Voucher template is selected.</span></span>
    - <span data-ttu-id="6bb4d-130">Summa: Toteutuneet summat tallennetaan ja kohdistetaan.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-130">Amount: The actual amounts will be stored and applied.</span></span>  
21. <span data-ttu-id="6bb4d-131">Valitse **Yleiset kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-131">Click **General journals**.</span></span>
22. <span data-ttu-id="6bb4d-132">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-132">Click **New**.</span></span>
23. <span data-ttu-id="6bb4d-133">Avaa haku valitsemalla **Nimi**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-133">In the **Name** field, click the drop-down button to open the lookup.</span></span>
24. <span data-ttu-id="6bb4d-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-134">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="6bb4d-135">Valitse **Rivit**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-135">Click **Lines**.</span></span>
26. <span data-ttu-id="6bb4d-136">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-136">Click **Functions**.</span></span>
27. <span data-ttu-id="6bb4d-137">Valitse **Valitse tositemalli**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-137">Click **Select voucher template**.</span></span>
28. <span data-ttu-id="6bb4d-138">Etsi aiemmin luomasi malli.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-138">Find the template that you created earlier.</span></span> <span data-ttu-id="6bb4d-139">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-139">Click **OK**.</span></span> <span data-ttu-id="6bb4d-140">Sinun on ehkä valittava **Edellinen vaihe** ja valittava sitten oikea malli, jos muita malleja on olemassa.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-140">You may need to click **Previous step** and then select the correct template if other templates exist.</span></span>  
29. <span data-ttu-id="6bb4d-141">Syötä **Summa**-kenttään tositteeseen kohdistettava summa.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-141">In the **Amount** field, enter the amount to be applied to the voucher.</span></span> <span data-ttu-id="6bb4d-142">**Summa**-kenttä näytetään vain, jos tositemallin tyyppi on Prosentti.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-142">The **Amount** field is only displayed if the voucher template is of type Percent.</span></span>  
30. <span data-ttu-id="6bb4d-143">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="6bb4d-143">Click **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]