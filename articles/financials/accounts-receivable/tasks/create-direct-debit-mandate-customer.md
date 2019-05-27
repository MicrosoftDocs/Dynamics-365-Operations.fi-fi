---
title: Luo suoraveloitusvaltakirja asiakkaalle
description: Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fc3052fdfc6e3dcf2826b3069f6d644201a70c3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572532"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="9cf4b-103">Luo suoraveloitusvaltakirja asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="9cf4b-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cf4b-104">Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="9cf4b-105">Pankkitilin luominen</span><span class="sxs-lookup"><span data-stu-id="9cf4b-105">Create a bank account</span></span>
1. <span data-ttu-id="9cf4b-106">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9cf4b-107">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="9cf4b-107">For example, select US-001</span></span>
3. <span data-ttu-id="9cf4b-108">Valitse toimintoruudussa Asiakas.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="9cf4b-109">Valitse Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="9cf4b-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-110">Click New.</span></span>
6. <span data-ttu-id="9cf4b-111">Kirjoita arvo Pankkitili-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="9cf4b-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="9cf4b-113">Syötä arvon IBAN-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="9cf4b-114">Kirjoita arvo Valuutta-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="9cf4b-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-115">Click Save.</span></span>
11. <span data-ttu-id="9cf4b-116">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-116">Close the page.</span></span>
12. <span data-ttu-id="9cf4b-117">Valitse Maksuliikenteen hallinta > Pankkitilit > Pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="9cf4b-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9cf4b-119">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="9cf4b-120">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-120">Click Edit.</span></span>
16. <span data-ttu-id="9cf4b-121">Laajenna Lisätunnus-osa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="9cf4b-122">Syötä Suoraveloitustunnus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="9cf4b-123">Syötä arvon IBAN-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="9cf4b-124">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-124">Close the page.</span></span>
20. <span data-ttu-id="9cf4b-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="9cf4b-126">Sähköisen maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="9cf4b-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="9cf4b-127">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Maksutavat.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="9cf4b-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-128">Click New.</span></span>
3. <span data-ttu-id="9cf4b-129">Syötä arvo Maksutapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="9cf4b-130">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9cf4b-131">Suoraveloitusvaltakirjan maksutavan maksutyypin on oltava Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="9cf4b-132">Valitse Vaadi valtakirjaa -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="9cf4b-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="9cf4b-134">Lisää suoraveloitusvaltakirja asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="9cf4b-135">Siirry kohtaan Myyntireskontra > Asiakkaat > Kaikki asiakkaat.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="9cf4b-136">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="9cf4b-136">For example, select US-001</span></span>
3. <span data-ttu-id="9cf4b-137">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-137">Click Edit.</span></span>
4. <span data-ttu-id="9cf4b-138">Laajenna Oletusmaksut-osa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="9cf4b-139">Anna tai valitse arvo Maksutapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="9cf4b-140">Laajenna Oletusmaksut-osa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="9cf4b-141">Laajenna Suoraveloitusvaltakirjat-osa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="9cf4b-142">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-142">Click Add.</span></span>
9. <span data-ttu-id="9cf4b-143">Syötä tai valitse arvo Pankkitili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="9cf4b-144">Syötä tai valitse arvo Laskuttajan pankkitili -kentässä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="9cf4b-145">Syötä niiden maksujen määrä, jotka odotat käsiteltäväksi tämän valtakirjan osalta.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="9cf4b-146">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-146">Click OK.</span></span>
13. <span data-ttu-id="9cf4b-147">Valitse Tulosta.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-147">Click Print.</span></span>
14. <span data-ttu-id="9cf4b-148">Valitse Valtakirjaraportti.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-148">Click Mandate report.</span></span>
15. <span data-ttu-id="9cf4b-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-149">Close the page.</span></span>
16. <span data-ttu-id="9cf4b-150">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-150">Click Edit.</span></span>
17. <span data-ttu-id="9cf4b-151">Syötä päivämäärä Allekirjoitus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="9cf4b-152">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-152">Click Yes.</span></span>
19. <span data-ttu-id="9cf4b-153">Syötä paikka, jossa valtakirja on allekirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="9cf4b-154">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-154">Click OK.</span></span>
21. <span data-ttu-id="9cf4b-155">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="9cf4b-156">Vapaatekstilaskun ja valtakirjan luominen</span><span class="sxs-lookup"><span data-stu-id="9cf4b-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="9cf4b-157">Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="9cf4b-158">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-158">Click New.</span></span>
3. <span data-ttu-id="9cf4b-159">Valitse asiakas, jolle valtakirja lisättiin.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="9cf4b-160">Anna tai valitse Suoraveloitusvaltakirjan tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="9cf4b-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

