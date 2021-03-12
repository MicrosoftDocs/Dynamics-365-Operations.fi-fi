---
title: Maksujen luominen asiakkaalle, jolla on suoraveloitusvaltakirjoja
description: Näiden ohjeiden avulla voit luoda ISO20022-suoraveloituksen maksutiedoston asiakkaalle, jolle on määritetty suoraveloitus ja jolla on maksettava lasku.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 934d086661dbbf1c7ba1d868f90caafe5b0bebf2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964563"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="01613-103">Maksujen luominen asiakkaalle, jolla on suoraveloitusvaltakirjoja</span><span class="sxs-lookup"><span data-stu-id="01613-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="01613-104">Näiden ohjeiden avulla voit luoda ISO20022-suoraveloituksen maksutiedoston asiakkaalle, jolle on määritetty suoraveloitus ja jolla on maksettava lasku.</span><span class="sxs-lookup"><span data-stu-id="01613-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="01613-105">Laskun luominen ja kirjaaminen on vapaaehtoista.</span><span class="sxs-lookup"><span data-stu-id="01613-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="01613-106">Sen sijaan, että lasku maksettaisiin, voit valita valtakirjan kirjauskansiossa ennen maksutiedoston luomista, jos haluat tukea asiakkaan ennakkomaksuja.</span><span class="sxs-lookup"><span data-stu-id="01613-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="01613-107">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="01613-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="01613-108">Tämä on viimeinen viidestä tehtävästä, joilla esitellään asiakasmaksujen prosessi, jossa käytetään sähköisen raportoinnin määrityksiä.</span><span class="sxs-lookup"><span data-stu-id="01613-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="01613-109">Edelliset tehtävät on suoritettava ennen tätä tehtävää.</span><span class="sxs-lookup"><span data-stu-id="01613-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="01613-110">Sinun on ensiksi tuotava asiakkaan maksun sähköiset raportointimääritykset, määritettävä maksutavat sekä määritettävä yrityksen ja asiakkaan tiedot.</span><span class="sxs-lookup"><span data-stu-id="01613-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="01613-111">Kirjaa vapaatekstilasku suoraveloitustietoineen</span><span class="sxs-lookup"><span data-stu-id="01613-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="01613-112">Siirry kohtaan Myyntireskontra > Laskut > Kaikki vapaatekstilaskut.</span><span class="sxs-lookup"><span data-stu-id="01613-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="01613-113">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="01613-113">Click New.</span></span>
3. <span data-ttu-id="01613-114">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="01613-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="01613-115">Valitse esimerkiksi arvo DE-010.</span><span class="sxs-lookup"><span data-stu-id="01613-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="01613-116">Anna tai valitse arvo Maksutapa-kentässä.</span><span class="sxs-lookup"><span data-stu-id="01613-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="01613-117">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="01613-117">For example.</span></span> <span data-ttu-id="01613-118">valitse Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="01613-118">select Electronic.</span></span>  
5. <span data-ttu-id="01613-119">Anna tai valitse Suoraveloitusvaltakirjan tunnus -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="01613-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="01613-120">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="01613-120">Click Add line.</span></span>
7. <span data-ttu-id="01613-121">Kirjoita Kuvaus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="01613-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="01613-122">Määritä Päätili-kenttään haluamasi arvot.</span><span class="sxs-lookup"><span data-stu-id="01613-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="01613-123">Syötä Yksikköhinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="01613-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="01613-124">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="01613-124">Click Post.</span></span>
11. <span data-ttu-id="01613-125">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="01613-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="01613-126">Luo maksu</span><span class="sxs-lookup"><span data-stu-id="01613-126">Create a payment</span></span>
1. <span data-ttu-id="01613-127">Siirry kohtaan Myyntireskontra > Maksut > Maksukirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="01613-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="01613-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="01613-128">Click New.</span></span>
3. <span data-ttu-id="01613-129">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="01613-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="01613-130">Valitse Rivit.</span><span class="sxs-lookup"><span data-stu-id="01613-130">Click Lines.</span></span>
5. <span data-ttu-id="01613-131">Valitse Maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="01613-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="01613-132">Valitse Luo maksuehdotus.</span><span class="sxs-lookup"><span data-stu-id="01613-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="01613-133">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="01613-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="01613-134">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="01613-134">Click Filter.</span></span>
9. <span data-ttu-id="01613-135">Valitse luettelosta Asiakastapahtumat-taulukon ja Maksutapa-kentän rivi.</span><span class="sxs-lookup"><span data-stu-id="01613-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="01613-136">Voit käyttää mitä tahansa ehtoja maksettavien asiakastapahtumien valinnassa.</span><span class="sxs-lookup"><span data-stu-id="01613-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="01613-137">Tässä esimerkissä käytetään tapahtumien suodattamiseen maksutapaa Sähköinen.</span><span class="sxs-lookup"><span data-stu-id="01613-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="01613-138">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="01613-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="01613-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="01613-139">Click OK.</span></span>
12. <span data-ttu-id="01613-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="01613-140">Click OK.</span></span>
13. <span data-ttu-id="01613-141">Valitse Luo maksut.</span><span class="sxs-lookup"><span data-stu-id="01613-141">Click Create payments.</span></span>
