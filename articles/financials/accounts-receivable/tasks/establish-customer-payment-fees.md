---
title: Määritä asiakkaan maksulisät
description: Luo asiakkaan toimitusmaksut.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5acb202d46ef39376a01ca592f60926786d11186
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "354825"
---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="37874-103">Määritä asiakkaan maksulisät</span><span class="sxs-lookup"><span data-stu-id="37874-103">Establish customer payment fees</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37874-104">Luo asiakkaan toimitusmaksut.</span><span class="sxs-lookup"><span data-stu-id="37874-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="37874-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="37874-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="37874-106">Siirry kohtaan Myyntireskontra > Maksujen asetukset > Toimitusmaksu.</span><span class="sxs-lookup"><span data-stu-id="37874-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="37874-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="37874-107">Click New.</span></span>
3. <span data-ttu-id="37874-108">Syötä Lisämaksun tunnus -kenttään lisämaksun tunnus.</span><span class="sxs-lookup"><span data-stu-id="37874-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="37874-109">Lisämaksun tunnus näkyy maksukirjauskansioissa, joten määritä käsiteltävää lisämaksua kuvaava tunnus.</span><span class="sxs-lookup"><span data-stu-id="37874-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="37874-110">Syötä Nimi-kenttään lisämaksun nimi.</span><span class="sxs-lookup"><span data-stu-id="37874-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="37874-111">Syötä Lisämaksun kuvaus -kenttään lisämaksun kuvaus.</span><span class="sxs-lookup"><span data-stu-id="37874-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="37874-112">Määritä, veloitetaanko lisämaksu asiakkaalta vai kirjanpitotililtä.</span><span class="sxs-lookup"><span data-stu-id="37874-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="37874-113">Jos lisämaksu koskee asiakasta, valitse Asiakas.</span><span class="sxs-lookup"><span data-stu-id="37874-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="37874-114">Jos organisaatio käsittelee lisämaksun kuluna, valitse Kirjanpito.</span><span class="sxs-lookup"><span data-stu-id="37874-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="37874-115">Tässä tehtävässä valitaan Asiakas.</span><span class="sxs-lookup"><span data-stu-id="37874-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="37874-116">Valitse sen kirjauskansion tyyppi, joka voi käyttää tätä toimitusmaksua.</span><span class="sxs-lookup"><span data-stu-id="37874-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="37874-117">Jos näitä lisämaksuja käytetään asiakkaan maksuissa, kirjauskansion tyypiksi määritetään todennäköisesti Asiakkaan maksu.</span><span class="sxs-lookup"><span data-stu-id="37874-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="37874-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="37874-118">Click Save.</span></span>
9. <span data-ttu-id="37874-119">Valitse Toimittajan toimitusmaksun asetukset.</span><span class="sxs-lookup"><span data-stu-id="37874-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="37874-120">Toimitusmaksun asetuksissa määritetään toimitusmaksun käsittelyajankohdan ehdot.</span><span class="sxs-lookup"><span data-stu-id="37874-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="37874-121">Voit esimerkiksi määrittää, että lisämaksu lasketaan, jos pankkitili on USMF OPER ja maksutapa on sekki.</span><span class="sxs-lookup"><span data-stu-id="37874-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="37874-122">Valitse joko Taulu, Ryhmä tai Kaikki, kun määrität tätä lisämaksua käyttävät pankkitilit.</span><span class="sxs-lookup"><span data-stu-id="37874-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="37874-123">Jos valitset Kaikki, tämä lisämaksu koskee kaikkia pankkitilejä.</span><span class="sxs-lookup"><span data-stu-id="37874-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="37874-124">Jos valitset Taulu, tämä lisämaksu koskee vain valitsemaasi pankkitiliä.</span><span class="sxs-lookup"><span data-stu-id="37874-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="37874-125">Jos valitset Ryhmä, tämä lisämaksu koskee vain valitsemasi pankkiryhmän pankkitilejä.</span><span class="sxs-lookup"><span data-stu-id="37874-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="37874-126">Valitse pankkiryhmä tai pankkitili.</span><span class="sxs-lookup"><span data-stu-id="37874-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="37874-127">Jos valitset Taulu, pankkitilit näkyvät haussa.</span><span class="sxs-lookup"><span data-stu-id="37874-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="37874-128">Jos valitset Ryhmä, pankkiryhmät näkyvät haussa.</span><span class="sxs-lookup"><span data-stu-id="37874-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="37874-129">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="37874-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="37874-130">Valitse maksutapa, jossa tätä lisämaksua käytetään.</span><span class="sxs-lookup"><span data-stu-id="37874-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="37874-131">Voit määrittää lisämaksun asiakkaille esimerkiksi silloin, kun he lähettävät maksut sekkeinä sähköisten maksujen sijaan.</span><span class="sxs-lookup"><span data-stu-id="37874-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="37874-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="37874-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="37874-133">Syötä tarvittaessa maksun valuutta.</span><span class="sxs-lookup"><span data-stu-id="37874-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="37874-134">Maksun valuuttaa käytetään lisäehtona lisämaksun määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="37874-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="37874-135">Pankki voi veloittaa lisämaksun esimerkiksi Yhdysvaltojen dollareina saapuneista maksuista, koska yleensä maksutapahtumat suoritetaan euroina.</span><span class="sxs-lookup"><span data-stu-id="37874-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="37874-136">Määritä, esitetäänkö lisämaksu prosenttina, summana vai välinä.</span><span class="sxs-lookup"><span data-stu-id="37874-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="37874-137">Syötä lisämaksun prosentti tai summa.</span><span class="sxs-lookup"><span data-stu-id="37874-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="37874-138">Jos Prosentti/summa-kentän arvo on Prosentti, tähän syötetään prosenttiluku.</span><span class="sxs-lookup"><span data-stu-id="37874-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="37874-139">Jos Prosentti/summa-kentän arvo on Summa, tähän syötetään summa.</span><span class="sxs-lookup"><span data-stu-id="37874-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="37874-140">Jos Prosentti/summa-kenttä on Väli, määritä tasot Väli-välilehden avulla.</span><span class="sxs-lookup"><span data-stu-id="37874-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="37874-141">Valitse Lisämaksun valuutta -kentässä lisämaksun valuutta.</span><span class="sxs-lookup"><span data-stu-id="37874-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="37874-142">Tämä on valuutta, jossa lisämaksu luodaan.</span><span class="sxs-lookup"><span data-stu-id="37874-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="37874-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="37874-143">Click Save.</span></span>

