---
title: Summa on suurempi kuin toimittajan maksulle laskettu alennus
description: Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa. Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7ee74bad071d546724f6ffe336bbe3bdf47e2a5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971900"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="26d86-104">Summa on suurempi kuin toimittajan maksulle laskettu alennus</span><span class="sxs-lookup"><span data-stu-id="26d86-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26d86-105">Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa.</span><span class="sxs-lookup"><span data-stu-id="26d86-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="26d86-106">Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="26d86-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="26d86-107">Toimittaja 3051 antaa Fabrikamille 4 prosentin käteisalennuksen, jos lasku maksetaan seitsemän päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="26d86-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="26d86-108">April syöttää 29. kesäkuuta 1 000,00 arvoisen laskun.</span><span class="sxs-lookup"><span data-stu-id="26d86-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="26d86-109">Toimittaja sallii Aprilin käyttää 60,00:n arvoista alennusta laskulle saatavilla olevan oletusalennuksen sijaan, joka on 40,00.</span><span class="sxs-lookup"><span data-stu-id="26d86-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="26d86-110">April kirjaa kertamaksun käyttämällä Ostoreskontran maksukirjauskansiota.</span><span class="sxs-lookup"><span data-stu-id="26d86-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="26d86-111">Hän syöttää maksulle toimittajan ja avaa sitten **Selvitä tapahtumat** -sivun.</span><span class="sxs-lookup"><span data-stu-id="26d86-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="26d86-112">Hän merkitsee laskun ja muuttaa **Käteisalennussumma**-kentän arvoksi **60,00**.</span><span class="sxs-lookup"><span data-stu-id="26d86-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="26d86-113">Merkitse</span><span class="sxs-lookup"><span data-stu-id="26d86-113">Mark</span></span>     | <span data-ttu-id="26d86-114">Käytä käteisalennusta</span><span class="sxs-lookup"><span data-stu-id="26d86-114">Use cash discount</span></span> | <span data-ttu-id="26d86-115">Tosite</span><span class="sxs-lookup"><span data-stu-id="26d86-115">Voucher</span></span>   | <span data-ttu-id="26d86-116">Tili</span><span class="sxs-lookup"><span data-stu-id="26d86-116">Account</span></span> | <span data-ttu-id="26d86-117">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="26d86-117">Date</span></span>      | <span data-ttu-id="26d86-118">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="26d86-118">Due date</span></span>  | <span data-ttu-id="26d86-119">Lasku</span><span class="sxs-lookup"><span data-stu-id="26d86-119">Invoice</span></span> | <span data-ttu-id="26d86-120">Summa tapahtuman valuuttana</span><span class="sxs-lookup"><span data-stu-id="26d86-120">Amount in transaction currency</span></span> | <span data-ttu-id="26d86-121">Valuutta</span><span class="sxs-lookup"><span data-stu-id="26d86-121">Currency</span></span> | <span data-ttu-id="26d86-122">Täsmäytettävä summa</span><span class="sxs-lookup"><span data-stu-id="26d86-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="26d86-123">Valittu</span><span class="sxs-lookup"><span data-stu-id="26d86-123">Selected</span></span> | <span data-ttu-id="26d86-124">Normaali</span><span class="sxs-lookup"><span data-stu-id="26d86-124">Normal</span></span>            | <span data-ttu-id="26d86-125">Var-10040</span><span class="sxs-lookup"><span data-stu-id="26d86-125">Inv-10040</span></span> | <span data-ttu-id="26d86-126">3051</span><span class="sxs-lookup"><span data-stu-id="26d86-126">3051</span></span>    | <span data-ttu-id="26d86-127">29.6.2015</span><span class="sxs-lookup"><span data-stu-id="26d86-127">6/29/2015</span></span> | <span data-ttu-id="26d86-128">29.7.2015</span><span class="sxs-lookup"><span data-stu-id="26d86-128">7/29/2015</span></span> | <span data-ttu-id="26d86-129">10040</span><span class="sxs-lookup"><span data-stu-id="26d86-129">10040</span></span>   | <span data-ttu-id="26d86-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="26d86-130">1,000.00</span></span>                       | <span data-ttu-id="26d86-131">USD</span><span class="sxs-lookup"><span data-stu-id="26d86-131">USD</span></span>      | <span data-ttu-id="26d86-132">940,00</span><span class="sxs-lookup"><span data-stu-id="26d86-132">940.00</span></span>           |

<span data-ttu-id="26d86-133">Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.</span><span class="sxs-lookup"><span data-stu-id="26d86-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="26d86-134">Käteisalennuksen päivämäärä</span><span class="sxs-lookup"><span data-stu-id="26d86-134">Cash discount date</span></span>           | <span data-ttu-id="26d86-135">12.7.2015</span><span class="sxs-lookup"><span data-stu-id="26d86-135">7/12/2015</span></span> |
| <span data-ttu-id="26d86-136">Käteisalennussumma</span><span class="sxs-lookup"><span data-stu-id="26d86-136">Cash discount amount</span></span>         | <span data-ttu-id="26d86-137">60,00</span><span class="sxs-lookup"><span data-stu-id="26d86-137">60.00</span></span>     |
| <span data-ttu-id="26d86-138">Käytä käteisalennusta</span><span class="sxs-lookup"><span data-stu-id="26d86-138">Use cash discount</span></span>            | <span data-ttu-id="26d86-139">Normaali</span><span class="sxs-lookup"><span data-stu-id="26d86-139">Normal</span></span>    |
| <span data-ttu-id="26d86-140">Käytetty käteisalennus</span><span class="sxs-lookup"><span data-stu-id="26d86-140">Cash discount taken</span></span>          | <span data-ttu-id="26d86-141">0,00</span><span class="sxs-lookup"><span data-stu-id="26d86-141">0.00</span></span>      |
| <span data-ttu-id="26d86-142">Käytettävä käteisalennussumma</span><span class="sxs-lookup"><span data-stu-id="26d86-142">Cash discount amount to take</span></span> | <span data-ttu-id="26d86-143">60,00</span><span class="sxs-lookup"><span data-stu-id="26d86-143">60.00</span></span>     |

<span data-ttu-id="26d86-144">April kirjaa maksukirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="26d86-144">April posts the payment journal.</span></span> <span data-ttu-id="26d86-145">Lasku selvitetään täysin käyttäen 940,00 arvoista maksua ja 60,00 arvoista alennusta.</span><span class="sxs-lookup"><span data-stu-id="26d86-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



