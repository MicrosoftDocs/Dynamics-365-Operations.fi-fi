---
title: Luo suoraveloitusvaltakirja asiakkaalle
description: Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ca5ff2290df2179004ca1cebd11f67fbb7a724e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177580"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="13a2a-103">Luo suoraveloitusvaltakirja asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="13a2a-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13a2a-104">Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.</span><span class="sxs-lookup"><span data-stu-id="13a2a-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="13a2a-105">Pankkitilin luominen</span><span class="sxs-lookup"><span data-stu-id="13a2a-105">Create a bank account</span></span>
1. <span data-ttu-id="13a2a-106">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="13a2a-107">Valitse luettelosta tietue.</span><span class="sxs-lookup"><span data-stu-id="13a2a-107">In the list, select a record.</span></span> <span data-ttu-id="13a2a-108">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="13a2a-108">For example, select US-001</span></span>
3. <span data-ttu-id="13a2a-109">Valitse toimintoruudussa **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="13a2a-110">Valitse **Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="13a2a-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-111">Click **New**.</span></span>
6. <span data-ttu-id="13a2a-112">Kirjoita arvo **Pankkitili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="13a2a-113">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="13a2a-114">Syötä arvon **IBAN**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="13a2a-115">Kirjoita arvo **Valuutta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="13a2a-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-116">Click **Save**.</span></span>
11. <span data-ttu-id="13a2a-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-117">Close the page.</span></span>
12. <span data-ttu-id="13a2a-118">Siirry **siirtymisruudussa**kohtaan **Moduulit > Maksuliikenteen hallinta > pankkitilit > pankkitilit.**</span><span class="sxs-lookup"><span data-stu-id="13a2a-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="13a2a-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="13a2a-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="13a2a-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="13a2a-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="13a2a-121">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-121">Click **Edit**.</span></span>
16. <span data-ttu-id="13a2a-122">Laajenna **Lisätunnus**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="13a2a-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="13a2a-123">Syötä **Suoraveloitustunnus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="13a2a-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="13a2a-124">Syötä arvon **IBAN**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="13a2a-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-125">Close the page.</span></span>
20. <span data-ttu-id="13a2a-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="13a2a-127">Sähköisen maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="13a2a-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="13a2a-128">Siirry kohtaan **Siirtymisruutu** **> Moduulit > Myyntireskontra >Maksujen asetukset > Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="13a2a-129">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-129">Click **New**.</span></span>
3. <span data-ttu-id="13a2a-130">Syötä arvo **Maksutapa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="13a2a-131">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="13a2a-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="13a2a-132">Valitse **Maksutyyppi**-kentässä Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="13a2a-133">Suoraveloitusvaltakirjan maksutavan maksutyypin on oltava Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="13a2a-134">Valitse **Vaadi valtakirjaa** -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="13a2a-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="13a2a-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="13a2a-136">Lisää suoraveloitusvaltakirja asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="13a2a-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="13a2a-137">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="13a2a-138">Valitse luettelosta tietue.</span><span class="sxs-lookup"><span data-stu-id="13a2a-138">In the list, select a record.</span></span> <span data-ttu-id="13a2a-139">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="13a2a-139">For example, select US-001</span></span>
3. <span data-ttu-id="13a2a-140">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-140">Click **Edit**.</span></span>
4. <span data-ttu-id="13a2a-141">Laajenna **Oletusmaksut**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="13a2a-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="13a2a-142">Anna tai valitse arvo **Maksutapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="13a2a-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="13a2a-143">Laajenna **Oletusmaksut**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="13a2a-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="13a2a-144">Laajenna **Suoraveloitusvaltakirjat**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="13a2a-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="13a2a-145">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-145">Click **Add**.</span></span>
9. <span data-ttu-id="13a2a-146">Anna tai valitse arvo **Pankkitili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="13a2a-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="13a2a-147">Syötä tai valitse arvo **Laskuttajan pankkitili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="13a2a-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="13a2a-148">Syötä **Maksun toistuvuus** -kenttään niiden maksujen määrä, jotka odotat käsiteltäväksi tämän valtakirjan osalta.</span><span class="sxs-lookup"><span data-stu-id="13a2a-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="13a2a-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-149">Click **OK**.</span></span>
13. <span data-ttu-id="13a2a-150">Valitse **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-150">Click **Print**.</span></span>
14. <span data-ttu-id="13a2a-151">Valitse **Valtakirjaraportti**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="13a2a-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-152">Close the page.</span></span>
16. <span data-ttu-id="13a2a-153">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-153">Click **Edit**.</span></span>
17. <span data-ttu-id="13a2a-154">Syötä päivämäärä **Allekirjoituksen päivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="13a2a-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="13a2a-155">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-155">Click **Yes**.</span></span>
19. <span data-ttu-id="13a2a-156">Syötä paikka, jossa valtakirja on allekirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="13a2a-157">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-157">Click **OK**.</span></span>
21. <span data-ttu-id="13a2a-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="13a2a-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="13a2a-159">Vapaatekstilaskun ja valtakirjan luominen</span><span class="sxs-lookup"><span data-stu-id="13a2a-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="13a2a-160">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Laskut > Kaikki vapaamuotoiset laskut**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="13a2a-161">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="13a2a-161">Click **New**.</span></span>
3. <span data-ttu-id="13a2a-162">Valitse asiakas, jolle valtakirja lisättiin.</span><span class="sxs-lookup"><span data-stu-id="13a2a-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="13a2a-163">Anna tai valitse **Suoraveloitusvaltakirjan tunnus** -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="13a2a-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

