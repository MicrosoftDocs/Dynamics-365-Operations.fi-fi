--- 
title: "Määritä toimittajan maksuehdot"
description: "Määritä toimittajan laskujen maksuehdot."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="76087-103">Määritä toimittajan maksuehdot</span><span class="sxs-lookup"><span data-stu-id="76087-103">Define vendor payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="76087-104">Määritä toimittajan laskujen maksuehdot.</span><span class="sxs-lookup"><span data-stu-id="76087-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="76087-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="76087-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="76087-106">Siirry kohtaan Ostoreskontra > Maksun asetukset > Maksuehdot.</span><span class="sxs-lookup"><span data-stu-id="76087-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="76087-107">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76087-107">Click New.</span></span>
    * <span data-ttu-id="76087-108">Maksuehdot-sivulla määritetään, miten eräpäivä lasketaan.</span><span class="sxs-lookup"><span data-stu-id="76087-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="76087-109">Sivulla ei määritetä, miten käteisalennuksen päivämäärä lasketaan.</span><span class="sxs-lookup"><span data-stu-id="76087-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="76087-110">Syötä Maksuehdot-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="76087-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="76087-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="76087-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="76087-112">Syötä Päivät-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="76087-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="76087-113">Tähän syötetty luku lisätään maksutavan määrittämään eräpäivään tai kauden loppuun.</span><span class="sxs-lookup"><span data-stu-id="76087-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="76087-114">Jos valitset esimerkiksi Netto, luku lisätään eräpäivään.</span><span class="sxs-lookup"><span data-stu-id="76087-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="76087-115">Jos valitset Nykyinen kuukausi, luku lisätään nykyisen kuukauden viimeiseen päivään eräpäivän laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="76087-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="76087-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="76087-116">Click Save.</span></span>
7. <span data-ttu-id="76087-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="76087-117">Close the page.</span></span>
8. <span data-ttu-id="76087-118">Siirry kohtaan Ostoreskontra > Maksun asetukset > Käteisalennukset.</span><span class="sxs-lookup"><span data-stu-id="76087-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="76087-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="76087-119">Click New.</span></span>
10. <span data-ttu-id="76087-120">Kirjoita Käteisalennus-kenttään tunnus.</span><span class="sxs-lookup"><span data-stu-id="76087-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="76087-121">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="76087-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="76087-122">Jos toimittaja tarjoaa alennustasoja, valitse seuraava käteisalennus nykyisen vanhennuttua.</span><span class="sxs-lookup"><span data-stu-id="76087-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="76087-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="76087-123">Close the page.</span></span>
14. <span data-ttu-id="76087-124">Syötä Päivät-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="76087-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="76087-125">Päivät-kenttään syötettyä määrää käytetään käteisalennuksen päivämäärän laskemiseen Netto-/Nykyinen-kentässä valitun vaihtoehdon mukaan.</span><span class="sxs-lookup"><span data-stu-id="76087-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="76087-126">Jos valittuna on Netto, määrä lisätään laskun päivämäärään käteisalennuksen päivämäärän määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="76087-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="76087-127">Jos valittuna on Nykyinen kuukausi, määrä lisätään nykyisen kuukauden loppuun käteisalennuksen päivämäärän määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="76087-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="76087-128">Syötä Alennus-kenttään käteisalennuksen prosentti.</span><span class="sxs-lookup"><span data-stu-id="76087-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="76087-129">Syötä päätili, jolle myyntilaskujen käteisalennus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="76087-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="76087-130">Syötä päätili, jolle toimittajan laskujen käteisalennus kirjataan.</span><span class="sxs-lookup"><span data-stu-id="76087-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="76087-131">Päätiliä käytetään, jos Käytä toimittajan alennusten päätiliä -kohtaan on valittu Alennuksen vastatilit.</span><span class="sxs-lookup"><span data-stu-id="76087-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="76087-132">Jos asetukseksi on valittu Laskurivien tilit, käteisalennus kirjataan laskurivien käyttöomaisuuserän/kulujen tileille.</span><span class="sxs-lookup"><span data-stu-id="76087-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="76087-133">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="76087-133">Click Save.</span></span>


