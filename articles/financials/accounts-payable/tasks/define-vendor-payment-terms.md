---
title: Toimittajan maksuehtojen määrittäminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajalaskujen maksuehdot.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843190"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="b8746-103">Toimittajan maksuehtojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b8746-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8746-104">Tässä ohjeaiheessa kerrotaan, kuinka voit määrittää toimittajalaskujen maksuehdot.</span><span class="sxs-lookup"><span data-stu-id="b8746-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="b8746-105">Tässä tehtävässä käytetään esittely-yritystä USMF.</span><span class="sxs-lookup"><span data-stu-id="b8746-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b8746-106">Siirry kohtaan **Siirtymisruutu > Moduulit > Ostoreskontra > Maksun asetukset > Maksuehdot**.</span><span class="sxs-lookup"><span data-stu-id="b8746-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="b8746-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8746-107">Select **New**.</span></span> <span data-ttu-id="b8746-108">Maksuehdot-sivulla määritetään, miten eräpäivä lasketaan.</span><span class="sxs-lookup"><span data-stu-id="b8746-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="b8746-109">Sivulla ei määritetä, miten käteisalennuksen päivämäärä lasketaan.</span><span class="sxs-lookup"><span data-stu-id="b8746-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="b8746-110">Syötä **Maksuehdot**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8746-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="b8746-111">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8746-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="b8746-112">Syötä **Päivää**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b8746-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="b8746-113">Tähän syötetty luku lisätään maksutavan määrittämään eräpäivään tai kauden loppuun.</span><span class="sxs-lookup"><span data-stu-id="b8746-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="b8746-114">Jos valitset esimerkiksi **Netto**, luku lisätään eräpäivään.</span><span class="sxs-lookup"><span data-stu-id="b8746-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="b8746-115">Jos valitset **Nykyinen kuukausi**, luku lisätään nykyisen kuukauden viimeiseen päivään eräpäivän laskemiseksi.</span><span class="sxs-lookup"><span data-stu-id="b8746-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="b8746-116">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8746-116">Select **Save**.</span></span>
7. <span data-ttu-id="b8746-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8746-117">Close the page.</span></span>
8. <span data-ttu-id="b8746-118">Siirry kohtaan **Ostoreskontra > Maksun asetukset > Käteisalennukset**.</span><span class="sxs-lookup"><span data-stu-id="b8746-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="b8746-119">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="b8746-119">Select **New**.</span></span>
10. <span data-ttu-id="b8746-120">Kirjoita **Käteisalennus**-kenttään tunnus.</span><span class="sxs-lookup"><span data-stu-id="b8746-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="b8746-121">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="b8746-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="b8746-122">Jos toimittaja tarjoaa alennustasoja, valitse seuraava käteisalennus nykyisen vanhennuttua.</span><span class="sxs-lookup"><span data-stu-id="b8746-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="b8746-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b8746-123">Close the page.</span></span>
14. <span data-ttu-id="b8746-124">Syötä **Päivää**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="b8746-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="b8746-125">**Päivät**-kenttään syötettyä määrää käytetään käteisalennuksen päivämäärän laskemiseen **Netto-/Nykyinen**-kentässä valitun vaihtoehdon mukaan.</span><span class="sxs-lookup"><span data-stu-id="b8746-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="b8746-126">Jos valittuna on **Netto**, määrä lisätään laskun päivämäärään käteisalennuksen päivämäärän määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="b8746-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="b8746-127">Jos valittuna on **Nykyinen kuukausi**, määrä lisätään nykyisen kuukauden loppuun käteisalennuksen päivämäärän määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="b8746-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="b8746-128">Syötä **Alennus**-kenttään käteisalennuksen prosentti.</span><span class="sxs-lookup"><span data-stu-id="b8746-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="b8746-129">Syötä päätili, jolle käteisalennus kirjataan myyntilaskuille, ja syötä päätili, jolle käteisalennus kirjataan toimittajalaskuille.</span><span class="sxs-lookup"><span data-stu-id="b8746-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="b8746-130">Päätiliä käytetään, jos **Käytä toimittajan alennusten päätiliä** -kohtaan on valittu **Alennuksen vastatilit**.</span><span class="sxs-lookup"><span data-stu-id="b8746-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="b8746-131">Jos asetukseksi on valittu **Laskurivien tilit**, käteisalennus kirjataan laskurivien resurssin/kulujen tileille.</span><span class="sxs-lookup"><span data-stu-id="b8746-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="b8746-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b8746-132">Select **Save**.</span></span>

