---
title: Verolaskennan suorituskyky vaikuttaa tapahtumiin
description: Tässä aiheessa on verotuslaskennan suorituskykyyn ja tapahtumiin liittyviä vianmääritystietoja.
author: shtao
manager: beya
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ff9d9b80172c3b337737b1cd53b4c56d1befe57
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947635"
---
# <a name="tax-calculation-performance-affects-transactions"></a><span data-ttu-id="a41cb-103">Verolaskennan suorituskyky vaikuttaa tapahtumiin</span><span class="sxs-lookup"><span data-stu-id="a41cb-103">Tax calculation performance affects transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a41cb-104">Joskus verolaskennan suorituskykyyn liittyvät suorituskykyongelmat vaikuttavat tapahtumaan.</span><span class="sxs-lookup"><span data-stu-id="a41cb-104">Sometimes, a transaction is affected by performance issues that tax calculation is having.</span></span> <span data-ttu-id="a41cb-105">Voit ratkaista tämän ongelman noudattamalla seuraavien osien ohjeita tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="a41cb-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="review-the-transaction-line-count"></a><span data-ttu-id="a41cb-106">Tarkastele tapahtuman rivimäärää</span><span class="sxs-lookup"><span data-stu-id="a41cb-106">Review the transaction line count</span></span>

<span data-ttu-id="a41cb-107">Määritä, onko tapahtumalla suuri määrä rivejä (esimerkiksi enemmän kuin useita satoja).</span><span class="sxs-lookup"><span data-stu-id="a41cb-107">Determine whether the transaction has a large number of lines (for example, more than several hundred).</span></span> <span data-ttu-id="a41cb-108">Jos näin ei ole, siirry seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="a41cb-108">If it doesn't, move on to the next section.</span></span> <span data-ttu-id="a41cb-109">Jos tapahtumalla on useita satoja rivejä, viivytä veron laskentaa.</span><span class="sxs-lookup"><span data-stu-id="a41cb-109">If the transaction does have several hundred lines, delay the tax calculation.</span></span> <span data-ttu-id="a41cb-110">Lisätietoja on kohdassa [Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="a41cb-110">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span> 

<span data-ttu-id="a41cb-111">Seuraavaksi voit määrittää, täyttyykö jokin seuraavista ehdoista:</span><span class="sxs-lookup"><span data-stu-id="a41cb-111">Next, you can determine whether any of the following conditions are met:</span></span>

- <span data-ttu-id="a41cb-112">Suurista tiedostoista on tuontitapahtumia.</span><span class="sxs-lookup"><span data-stu-id="a41cb-112">There are import transactions from large files.</span></span>
- <span data-ttu-id="a41cb-113">Useat istunnot käsittelevät saman tapahtumaveron laskennan samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a41cb-113">Multiple sessions process the same transaction tax calculation at the same time.</span></span>
- <span data-ttu-id="a41cb-114">Tapahtumalla on useita rivejä, ja näkymät päivitetään reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="a41cb-114">The transaction has multiple lines, and the views are updated in real time.</span></span> <span data-ttu-id="a41cb-115">Esimerkiksi **Kirjauskansio**-sivun **Laskettu arvonlisäverosumma** -kenttä päivitetään reaaliaikaisesti, kun rivin kenttiä muutetaan.</span><span class="sxs-lookup"><span data-stu-id="a41cb-115">For example, the **Calculated sales tax amount** field on the **General journal** page is updated in real time when a line's fields are changed.</span></span>

   <span data-ttu-id="a41cb-116">[![Laskettu arvonlisäveron summa -kenttä kirjauskansion tositesivulla](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="a41cb-116">[![Calculated sales tax amount field on the Jounal voucher page](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture1.png)</span></span>

<span data-ttu-id="a41cb-117">Jos jokin näistä ehdoista täyttyy, viivytä veron laskentaa.</span><span class="sxs-lookup"><span data-stu-id="a41cb-117">If any of these conditions are met, delay the tax calculation.</span></span>

## <a name="review-the-call-stack"></a><span data-ttu-id="a41cb-118">Kutsupinon tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a41cb-118">Review the call stack</span></span>

<span data-ttu-id="a41cb-119">Tarkista kutsupino ja määritä, kutsutaanko verolaskentaa useita kertoja.</span><span class="sxs-lookup"><span data-stu-id="a41cb-119">Review the call stack to determine whether tax calculation is called multiple times.</span></span> <span data-ttu-id="a41cb-120">Jos näin ei ole, siirry seuraavaan osaan.</span><span class="sxs-lookup"><span data-stu-id="a41cb-120">If it isn't, move on to the next section.</span></span> <span data-ttu-id="a41cb-121">Jos kutsupinoa kutsutaan useita kertoja, voit vähentää veron laskenta-aikoja noudattamalla näitä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="a41cb-121">If the call stack is called multiple times, follow these steps to help reduce the tax calculation times.</span></span>

1. <span data-ttu-id="a41cb-122">Jos kirjauskansio on harkinnut tapahtumaa, viivytä veron laskentaa.</span><span class="sxs-lookup"><span data-stu-id="a41cb-122">If the journal has considered the transaction, delay the tax calculation.</span></span> <span data-ttu-id="a41cb-123">Lisätietoja on kohdassa [Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa](enable-delayed-tax-calculation.md).</span><span class="sxs-lookup"><span data-stu-id="a41cb-123">For more information, see [Enable delayed tax calculation on journals](enable-delayed-tax-calculation.md).</span></span>
2. <span data-ttu-id="a41cb-124">Jos tapahtuma on ostotilaus ja sovellusversio on uudempi kuin 10.0.15, voit viivyttää veron laskentaa lopulliseen laskentaan ottamalla käyttöön väliversiotestauksen kohteelle **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span><span class="sxs-lookup"><span data-stu-id="a41cb-124">If the transaction is a purchase order, and the application version is later than 10.0.15, you can delay the tax calculation until the final calculation by enabling the flighting for **PurchTableChangeMgmtDistributionUpdateOnToggle_KillSwitch**.</span></span>

## <a name="review-the-call-stack-timeline"></a><span data-ttu-id="a41cb-125">Kutsupinon aikajanan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a41cb-125">Review the call stack timeline</span></span>

<span data-ttu-id="a41cb-126">Tarkista kutsupinon aikajana ja määritä, esiintyykö seuraavia ongelmia.</span><span class="sxs-lookup"><span data-stu-id="a41cb-126">Review the call stack timeline to determine whether the following issues exist.</span></span> <span data-ttu-id="a41cb-127">Jos tunnukset ovat käytössä, voit korjata ongelman aktivoimalla väliversiotestauksen kohteelle **TaxUncommittedDoIsolateScopeFlighting**.</span><span class="sxs-lookup"><span data-stu-id="a41cb-127">If they do, enable the flighting for **TaxUncommittedDoIsolateScopeFlighting** to fix the issue.</span></span>

- <span data-ttu-id="a41cb-128">Tapahtuma aiheuttaa järjestelmän lopettavan vastaamisen, kunnes istunto päättyy.</span><span class="sxs-lookup"><span data-stu-id="a41cb-128">The transaction causes the system to stop responding until the session ends.</span></span> <span data-ttu-id="a41cb-129">Näin ollen tapahtuma ei voi laskea veron tulosta.</span><span class="sxs-lookup"><span data-stu-id="a41cb-129">Therefore, the transaction can't calculate the tax result.</span></span> <span data-ttu-id="a41cb-130">Seuraavassa kuvassa näkyy vastaanottamasi Istunto päättynyt -sanomaruutu.</span><span class="sxs-lookup"><span data-stu-id="a41cb-130">The following illustration shows the "Session ended" message box that you receive.</span></span>

    <span data-ttu-id="a41cb-131">[![Istunto päättynyt -sanoma](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="a41cb-131">[![Session ended message](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture2.png)</span></span>

- <span data-ttu-id="a41cb-132">**TaxUncommitted**-menetelmät vievät enemmän aikaa kuin muut menetelmät.</span><span class="sxs-lookup"><span data-stu-id="a41cb-132">The **TaxUncommitted** methods take more time than other methods.</span></span> <span data-ttu-id="a41cb-133">Esimerkiksi seuraavassa kuvassa **TaxUncommitted::updateTaxUncommitted()**-menetelmä kestää 43,347.42 sekuntia, mutta muiden menetelmien käyttö kestää 0,09 sekuntia.</span><span class="sxs-lookup"><span data-stu-id="a41cb-133">For example, in the following illustration, the **TaxUncommitted::updateTaxUncommitted()** method takes 43,347.42 seconds, but other methods take 0.09 seconds.</span></span>

    <span data-ttu-id="a41cb-134">[![Menetelmän kestot](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="a41cb-134">[![Method durations](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)](./media/tax-calculation-bad-performance-impacts-transaction-Picture3.png)</span></span>

## <a name="customizing-and-calling-tax-calculation"></a><span data-ttu-id="a41cb-135">Veron laskennan mukauttaminen ja kutsuminen</span><span class="sxs-lookup"><span data-stu-id="a41cb-135">Customizing and calling tax calculation</span></span>

<span data-ttu-id="a41cb-136">Kun muokkaat, älä kutsu veron laskentaa jokaisen rivin **lisää()**- tai **päivitä()**-menetelmässä.</span><span class="sxs-lookup"><span data-stu-id="a41cb-136">When you customize, don't call tax calculation at the **insert()** or **update()** method for each line.</span></span> <span data-ttu-id="a41cb-137">Verolaskentaa tulee kutsua tapahtumatasolla.</span><span class="sxs-lookup"><span data-stu-id="a41cb-137">Tax calculation should be called at the transaction level.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="a41cb-138">Määritä, onko mukautus olemassa</span><span class="sxs-lookup"><span data-stu-id="a41cb-138">Determine whether customization exists</span></span>

<span data-ttu-id="a41cb-139">Jos olet suorittanut edellisten osien vaiheet, mutta et ole löytänyt ongelmaa, selvitä, onko mukautus olemassa.</span><span class="sxs-lookup"><span data-stu-id="a41cb-139">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="a41cb-140">Jos mukautusta ei ole, luo Microsoftin huoltopyyntö lisätuen saamiseksi.</span><span class="sxs-lookup"><span data-stu-id="a41cb-140">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
