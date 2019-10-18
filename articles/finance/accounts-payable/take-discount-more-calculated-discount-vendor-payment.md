---
title: Alennuksen käyttäminen, jonka summa on suurempi kuin toimittajan maksulle laskettu alennus
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
ms.search.scope: Core, Operations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b84b3d6ef1a86d8174823345a5ee9181c701c151
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177601"
---
# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="966f7-104">Alennuksen käyttäminen, jonka summa on suurempi kuin toimittajan maksulle laskettu alennus</span><span class="sxs-lookup"><span data-stu-id="966f7-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="966f7-105">Tässä artikkelissa käydään läpi skenaario, jossa käteisalennuksen summa on suurempi kuin alennus, joka oli alunperin käytettävissä laskussa.</span><span class="sxs-lookup"><span data-stu-id="966f7-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="966f7-106">Tämä skenaario on mahdollinen, jos organisaatio sopii toimittajan kanssa laskun summaa pienemmän summan maksamisesta.</span><span class="sxs-lookup"><span data-stu-id="966f7-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="966f7-107">Toimittaja 3051 antaa Fabrikamille 4 prosentin käteisalennuksen, jos lasku maksetaan seitsemän päivän kuluessa.</span><span class="sxs-lookup"><span data-stu-id="966f7-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="966f7-108">April syöttää 29. kesäkuuta 1 000,00 arvoisen laskun.</span><span class="sxs-lookup"><span data-stu-id="966f7-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="966f7-109">Toimittaja sallii Aprilin käyttää 60,00:n arvoista alennusta laskulle saatavilla olevan oletusalennuksen sijaan, joka on 40,00.</span><span class="sxs-lookup"><span data-stu-id="966f7-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="966f7-110">April kirjaa kertamaksun käyttämällä Ostoreskontran maksukirjauskansiota.</span><span class="sxs-lookup"><span data-stu-id="966f7-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="966f7-111">Hän syöttää maksulle toimittajan ja avaa sitten **Selvitä tapahtumat** -sivun.</span><span class="sxs-lookup"><span data-stu-id="966f7-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="966f7-112">Hän merkitsee laskun ja muuttaa **Käteisalennussumma**-kentän arvoksi **60,00**.</span><span class="sxs-lookup"><span data-stu-id="966f7-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="966f7-113">Merkitse</span><span class="sxs-lookup"><span data-stu-id="966f7-113">Mark</span></span>     | <span data-ttu-id="966f7-114">Käytä käteisalennusta</span><span class="sxs-lookup"><span data-stu-id="966f7-114">Use cash discount</span></span> | <span data-ttu-id="966f7-115">Tosite</span><span class="sxs-lookup"><span data-stu-id="966f7-115">Voucher</span></span>   | <span data-ttu-id="966f7-116">Tili</span><span class="sxs-lookup"><span data-stu-id="966f7-116">Account</span></span> | <span data-ttu-id="966f7-117">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="966f7-117">Date</span></span>      | <span data-ttu-id="966f7-118">Eräpäivä</span><span class="sxs-lookup"><span data-stu-id="966f7-118">Due date</span></span>  | <span data-ttu-id="966f7-119">Lasku</span><span class="sxs-lookup"><span data-stu-id="966f7-119">Invoice</span></span> | <span data-ttu-id="966f7-120">Summa tapahtuman valuuttana</span><span class="sxs-lookup"><span data-stu-id="966f7-120">Amount in transaction currency</span></span> | <span data-ttu-id="966f7-121">Valuutta</span><span class="sxs-lookup"><span data-stu-id="966f7-121">Currency</span></span> | <span data-ttu-id="966f7-122">Täsmäytettävä summa</span><span class="sxs-lookup"><span data-stu-id="966f7-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="966f7-123">Valittu</span><span class="sxs-lookup"><span data-stu-id="966f7-123">Selected</span></span> | <span data-ttu-id="966f7-124">Normaali</span><span class="sxs-lookup"><span data-stu-id="966f7-124">Normal</span></span>            | <span data-ttu-id="966f7-125">Var-10040</span><span class="sxs-lookup"><span data-stu-id="966f7-125">Inv-10040</span></span> | <span data-ttu-id="966f7-126">3051</span><span class="sxs-lookup"><span data-stu-id="966f7-126">3051</span></span>    | <span data-ttu-id="966f7-127">29.6.2015</span><span class="sxs-lookup"><span data-stu-id="966f7-127">6/29/2015</span></span> | <span data-ttu-id="966f7-128">29.7.2015</span><span class="sxs-lookup"><span data-stu-id="966f7-128">7/29/2015</span></span> | <span data-ttu-id="966f7-129">10040</span><span class="sxs-lookup"><span data-stu-id="966f7-129">10040</span></span>   | <span data-ttu-id="966f7-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="966f7-130">1,000.00</span></span>                       | <span data-ttu-id="966f7-131">USD</span><span class="sxs-lookup"><span data-stu-id="966f7-131">USD</span></span>      | <span data-ttu-id="966f7-132">940,00</span><span class="sxs-lookup"><span data-stu-id="966f7-132">940.00</span></span>           |

<span data-ttu-id="966f7-133">Alennustiedot näkyvät **Selvitä tapahtumat** -sivun alaosassa.</span><span class="sxs-lookup"><span data-stu-id="966f7-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="966f7-134">Käteisalennuksen päivämäärä</span><span class="sxs-lookup"><span data-stu-id="966f7-134">Cash discount date</span></span>           | <span data-ttu-id="966f7-135">12.7.2015</span><span class="sxs-lookup"><span data-stu-id="966f7-135">7/12/2015</span></span> |
| <span data-ttu-id="966f7-136">Käteisalennussumma</span><span class="sxs-lookup"><span data-stu-id="966f7-136">Cash discount amount</span></span>         | <span data-ttu-id="966f7-137">60,00</span><span class="sxs-lookup"><span data-stu-id="966f7-137">60.00</span></span>     |
| <span data-ttu-id="966f7-138">Käytä käteisalennusta</span><span class="sxs-lookup"><span data-stu-id="966f7-138">Use cash discount</span></span>            | <span data-ttu-id="966f7-139">Normaali</span><span class="sxs-lookup"><span data-stu-id="966f7-139">Normal</span></span>    |
| <span data-ttu-id="966f7-140">Käytetty käteisalennus</span><span class="sxs-lookup"><span data-stu-id="966f7-140">Cash discount taken</span></span>          | <span data-ttu-id="966f7-141">0,00</span><span class="sxs-lookup"><span data-stu-id="966f7-141">0.00</span></span>      |
| <span data-ttu-id="966f7-142">Käytettävä käteisalennussumma</span><span class="sxs-lookup"><span data-stu-id="966f7-142">Cash discount amount to take</span></span> | <span data-ttu-id="966f7-143">60,00</span><span class="sxs-lookup"><span data-stu-id="966f7-143">60.00</span></span>     |

<span data-ttu-id="966f7-144">April kirjaa maksukirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="966f7-144">April posts the payment journal.</span></span> <span data-ttu-id="966f7-145">Lasku selvitetään täysin käyttäen 940,00 arvoista maksua ja 60,00 arvoista alennusta.</span><span class="sxs-lookup"><span data-stu-id="966f7-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>



