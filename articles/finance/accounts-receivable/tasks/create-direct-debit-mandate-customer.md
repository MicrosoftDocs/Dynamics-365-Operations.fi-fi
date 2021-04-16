---
title: Luo suoraveloitusvaltakirja asiakkaalle
description: Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bbf3703941255dfd82b8fb501ba8a9d1f3a2ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835073"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="a661d-103">Luo suoraveloitusvaltakirja asiakkaalle</span><span class="sxs-lookup"><span data-stu-id="a661d-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a661d-104">Tässä tehtävän ohjauksessa kerrotaan, miten suoraveloitusvaltakirja luodaan ja miten sitä käytetään laskuissa.</span><span class="sxs-lookup"><span data-stu-id="a661d-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="a661d-105">Pankkitilin luominen</span><span class="sxs-lookup"><span data-stu-id="a661d-105">Create a bank account</span></span>
1. <span data-ttu-id="a661d-106">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="a661d-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a661d-107">Valitse luettelosta tietue.</span><span class="sxs-lookup"><span data-stu-id="a661d-107">In the list, select a record.</span></span> <span data-ttu-id="a661d-108">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="a661d-108">For example, select US-001</span></span>
3. <span data-ttu-id="a661d-109">Valitse toimintoruudussa **Asiakas**.</span><span class="sxs-lookup"><span data-stu-id="a661d-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="a661d-110">Valitse **Pankkitilit**.</span><span class="sxs-lookup"><span data-stu-id="a661d-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="a661d-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a661d-111">Click **New**.</span></span>
6. <span data-ttu-id="a661d-112">Kirjoita arvo **Pankkitili**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="a661d-113">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="a661d-114">Syötä arvon **IBAN**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="a661d-115">Kirjoita arvo **Valuutta**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="a661d-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a661d-116">Click **Save**.</span></span>
11. <span data-ttu-id="a661d-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-117">Close the page.</span></span>
12. <span data-ttu-id="a661d-118">Siirry **siirtymisruudussa** kohtaan **Moduulit > Maksuliikenteen hallinta > pankkitilit > pankkitilit.**</span><span class="sxs-lookup"><span data-stu-id="a661d-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="a661d-119">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="a661d-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a661d-120">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="a661d-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="a661d-121">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="a661d-121">Click **Edit**.</span></span>
16. <span data-ttu-id="a661d-122">Laajenna **Lisätunnus**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a661d-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="a661d-123">Syötä **Suoraveloitustunnus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a661d-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="a661d-124">Syötä arvon **IBAN**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="a661d-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-125">Close the page.</span></span>
20. <span data-ttu-id="a661d-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="a661d-127">Sähköisen maksutavan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a661d-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="a661d-128">Siirry kohtaan **Siirtymisruutu** **> Moduulit > Myyntireskontra >Maksujen asetukset > Maksutavat**.</span><span class="sxs-lookup"><span data-stu-id="a661d-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="a661d-129">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a661d-129">Click **New**.</span></span>
3. <span data-ttu-id="a661d-130">Syötä arvo **Maksutapa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="a661d-131">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="a661d-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a661d-132">Valitse **Maksutyyppi**-kentässä Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="a661d-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="a661d-133">Suoraveloitusvaltakirjan maksutavan maksutyypin on oltava Sähköinen maksu.</span><span class="sxs-lookup"><span data-stu-id="a661d-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="a661d-134">Valitse **Vaadi valtakirjaa** -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="a661d-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="a661d-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="a661d-136">Lisää suoraveloitusvaltakirja asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="a661d-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="a661d-137">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Asiakkaat > Kaikki asiakkaat**.</span><span class="sxs-lookup"><span data-stu-id="a661d-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="a661d-138">Valitse luettelosta tietue.</span><span class="sxs-lookup"><span data-stu-id="a661d-138">In the list, select a record.</span></span> <span data-ttu-id="a661d-139">Voit valita esimerkiksi arvon US-001</span><span class="sxs-lookup"><span data-stu-id="a661d-139">For example, select US-001</span></span>
3. <span data-ttu-id="a661d-140">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="a661d-140">Click **Edit**.</span></span>
4. <span data-ttu-id="a661d-141">Laajenna **Oletusmaksut**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a661d-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="a661d-142">Anna tai valitse arvo **Maksutapa**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a661d-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="a661d-143">Laajenna **Oletusmaksut**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a661d-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="a661d-144">Laajenna **Suoraveloitusvaltakirjat**-pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="a661d-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="a661d-145">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a661d-145">Click **Add**.</span></span>
9. <span data-ttu-id="a661d-146">Anna tai valitse arvo **Pankkitili**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="a661d-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="a661d-147">Syötä tai valitse arvo **Laskuttajan pankkitili** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="a661d-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="a661d-148">Syötä **Maksun toistuvuus** -kenttään niiden maksujen määrä, jotka odotat käsiteltäväksi tämän valtakirjan osalta.</span><span class="sxs-lookup"><span data-stu-id="a661d-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="a661d-149">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a661d-149">Click **OK**.</span></span>
13. <span data-ttu-id="a661d-150">Valitse **Tulosta**.</span><span class="sxs-lookup"><span data-stu-id="a661d-150">Click **Print**.</span></span>
14. <span data-ttu-id="a661d-151">Valitse **Valtakirjaraportti**.</span><span class="sxs-lookup"><span data-stu-id="a661d-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="a661d-152">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-152">Close the page.</span></span>
16. <span data-ttu-id="a661d-153">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="a661d-153">Click **Edit**.</span></span>
17. <span data-ttu-id="a661d-154">Syötä päivämäärä **Allekirjoituksen päivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="a661d-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="a661d-155">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a661d-155">Click **Yes**.</span></span>
19. <span data-ttu-id="a661d-156">Syötä paikka, jossa valtakirja on allekirjoitettu.</span><span class="sxs-lookup"><span data-stu-id="a661d-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="a661d-157">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="a661d-157">Click **OK**.</span></span>
21. <span data-ttu-id="a661d-158">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a661d-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="a661d-159">Vapaatekstilaskun ja valtakirjan luominen</span><span class="sxs-lookup"><span data-stu-id="a661d-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="a661d-160">Siirry **siirtymisruudussa** kohtaan **Moduulit > Myyntireskontra > Laskut > Kaikki vapaamuotoiset laskut**.</span><span class="sxs-lookup"><span data-stu-id="a661d-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="a661d-161">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a661d-161">Click **New**.</span></span>
3. <span data-ttu-id="a661d-162">Valitse asiakas, jolle valtakirja lisättiin.</span><span class="sxs-lookup"><span data-stu-id="a661d-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="a661d-163">Anna tai valitse **Suoraveloitusvaltakirjan tunnus** -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="a661d-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]