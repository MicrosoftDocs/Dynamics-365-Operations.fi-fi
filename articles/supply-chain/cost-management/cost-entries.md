---
title: Kustannusmerkinnät
description: Tässä artikkelissa on tietoja kustannusmerkinnöistä ja siitä, milloin niitä luodaan. Kustannusmerkintä on tietue, joka rekisteröi tietyn tapahtuman määrän ja kustannukset.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3116f9fd2d1fe6a0967b114a069f495cea6217a1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426740"
---
# <a name="cost-entries"></a><span data-ttu-id="501b2-104">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="501b2-104">Cost entries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="501b2-105">Tässä artikkelissa on tietoja kustannusmerkinnöistä ja siitä, milloin niitä luodaan.</span><span class="sxs-lookup"><span data-stu-id="501b2-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="501b2-106">Kustannusmerkintä on tietue, joka rekisteröi tietyn tapahtuman määrän ja kustannukset.</span><span class="sxs-lookup"><span data-stu-id="501b2-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="501b2-107">Kustannustapahtumat ovat koosteita varastotapahtumista, jotka on tallennettu aktiivisiin taloushallinnon varastodimensioihin.</span><span class="sxs-lookup"><span data-stu-id="501b2-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="501b2-108">Esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="501b2-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="501b2-109">Esimerkki 1: Kustannustapahtumia ei luoda</span><span class="sxs-lookup"><span data-stu-id="501b2-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="501b2-110">Kirjauskansion siirtotapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="501b2-110">A transfer journal event is registered.</span></span> <span data-ttu-id="501b2-111">Tapahtuma siirtää yhden nimikkeen A sijainnista A kohteeseen B. Varastodimension sijainnin ei katsota kuuluvan osaksi kustannuskohdetta.</span><span class="sxs-lookup"><span data-stu-id="501b2-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="501b2-112">Joten, tapauksessa on kaksi varastotapahtumaa eikä yhtäään kustannusmerkintää.</span><span class="sxs-lookup"><span data-stu-id="501b2-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="501b2-113">Esimerkki 2: Kustannustapahtumia luodaan</span><span class="sxs-lookup"><span data-stu-id="501b2-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="501b2-114">Kirjauskansion siirtotapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="501b2-114">A transfer journal event is registered.</span></span> <span data-ttu-id="501b2-115">Tapahtuma siirtää yhden nimikeyksikön A toimipaikasta 1 toimipaikkaan 2.</span><span class="sxs-lookup"><span data-stu-id="501b2-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="501b2-116">Toimipaikan varastodimensiota pidetään osana kustannusobjektia.</span><span class="sxs-lookup"><span data-stu-id="501b2-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="501b2-117">Joten, tapauksessa on kaksi varastotapahtumaa ja kaksi kustannusmerkintää.</span><span class="sxs-lookup"><span data-stu-id="501b2-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="501b2-118">Esimerkki 3: Yksi kustannustapahtuma luodaan</span><span class="sxs-lookup"><span data-stu-id="501b2-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="501b2-119">Ostotilauksen tuotteen vastaanottotapahtuma on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="501b2-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="501b2-120">Tapahtuma rekisteröi 100 kappaletta nimikettä A, yksikkökustannuksen ollessa 10,00 Yhdysvaltain dollaria (USD).</span><span class="sxs-lookup"><span data-stu-id="501b2-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="501b2-121">Koska kohde A käyttää sarjanumeroja seuratakseen varastonhallinnan päämäärää, ainutkertainen sarjanumero luodaan kullekin nimikkeelle, joka on vastaanotettu.</span><span class="sxs-lookup"><span data-stu-id="501b2-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="501b2-122">Joten, tapauksessa on 100 varastotapahtumaa ja yksi kustannusmerkintä.</span><span class="sxs-lookup"><span data-stu-id="501b2-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="501b2-123">Kustannusmerkintäsivu</span><span class="sxs-lookup"><span data-stu-id="501b2-123">Cost entries page</span></span>
<span data-ttu-id="501b2-124">Uuden **Kustannustapahtuma**-sivun avulla voit tarkastella ja hallita määrien ja kustannuksien rekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="501b2-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="501b2-125">Tämä sivu täydentää **Varastotapahtuma-** ja **Varastotilitys** sivuja.</span><span class="sxs-lookup"><span data-stu-id="501b2-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="501b2-126">Tapahtuman tietueet ovat rekisteröityjä aikajärjestyksessä.</span><span class="sxs-lookup"><span data-stu-id="501b2-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="501b2-127">Siksi voit nopeasti etsiä ja kontrolloida tietyn tapahtuman kumulatiiviset kustannukset tai kaikki tapahtumat, jotka liittyvät asiakirjaan.</span><span class="sxs-lookup"><span data-stu-id="501b2-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="501b2-128">Tässä on esimerkki:</span><span class="sxs-lookup"><span data-stu-id="501b2-128">Here is an example:</span></span>

-   <span data-ttu-id="501b2-129">Tuotteen vastaanottotapahtuma on rekisteröity nimikkeelle A. Sata kappaletta vastaanotetaan yksikkökustannuksin 10,00 USD.</span><span class="sxs-lookup"><span data-stu-id="501b2-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="501b2-130">Muutaman päivän kuluttua laskutapahtuman kirjaamisesta, kustannukset nousevat 11,00 dollariin (USD).</span><span class="sxs-lookup"><span data-stu-id="501b2-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="501b2-131">Joten, kokonaissumma on 1,100 euroa.</span><span class="sxs-lookup"><span data-stu-id="501b2-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="501b2-132">Toinen tosite luodaan kattamaan 100 dollarin (USD) ero myyntihintaan.</span><span class="sxs-lookup"><span data-stu-id="501b2-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="501b2-133">Muutaman päivän kuluttua luokittelematon 15.00 dollarin (USD) kulu rekisteröidään kuljetuskuluina ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="501b2-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="501b2-134">Tosite</span><span class="sxs-lookup"><span data-stu-id="501b2-134">Voucher</span></span> | <span data-ttu-id="501b2-135">Päivämäärä</span><span class="sxs-lookup"><span data-stu-id="501b2-135">Date</span></span>       | <span data-ttu-id="501b2-136">Viite</span><span class="sxs-lookup"><span data-stu-id="501b2-136">Reference</span></span>      | <span data-ttu-id="501b2-137">Numero</span><span class="sxs-lookup"><span data-stu-id="501b2-137">Number</span></span> | <span data-ttu-id="501b2-138">Erätunnus</span><span class="sxs-lookup"><span data-stu-id="501b2-138">Lot ID</span></span>  | <span data-ttu-id="501b2-139">Määrä</span><span class="sxs-lookup"><span data-stu-id="501b2-139">Quantity</span></span> | <span data-ttu-id="501b2-140">Summa</span><span class="sxs-lookup"><span data-stu-id="501b2-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="501b2-141">00001</span><span class="sxs-lookup"><span data-stu-id="501b2-141">00001</span></span>   | <span data-ttu-id="501b2-142">01.01.2015</span><span class="sxs-lookup"><span data-stu-id="501b2-142">01-01-2015</span></span> | <span data-ttu-id="501b2-143">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="501b2-143">Purchase order</span></span> | <span data-ttu-id="501b2-144">100001</span><span class="sxs-lookup"><span data-stu-id="501b2-144">100001</span></span> | <span data-ttu-id="501b2-145">0000101</span><span class="sxs-lookup"><span data-stu-id="501b2-145">0000101</span></span> | <span data-ttu-id="501b2-146">100,00</span><span class="sxs-lookup"><span data-stu-id="501b2-146">100.00</span></span>   | <span data-ttu-id="501b2-147">1000.00</span><span class="sxs-lookup"><span data-stu-id="501b2-147">1000.00</span></span> |
| <span data-ttu-id="501b2-148">00002</span><span class="sxs-lookup"><span data-stu-id="501b2-148">00002</span></span>   | <span data-ttu-id="501b2-149">20.01.2015</span><span class="sxs-lookup"><span data-stu-id="501b2-149">20-01-2015</span></span> | <span data-ttu-id="501b2-150">Ostotilaus</span><span class="sxs-lookup"><span data-stu-id="501b2-150">Purchase order</span></span> | <span data-ttu-id="501b2-151">100001</span><span class="sxs-lookup"><span data-stu-id="501b2-151">100001</span></span> | <span data-ttu-id="501b2-152">0000101</span><span class="sxs-lookup"><span data-stu-id="501b2-152">0000101</span></span> |          | <span data-ttu-id="501b2-153">100,00</span><span class="sxs-lookup"><span data-stu-id="501b2-153">100.00</span></span>  |
| <span data-ttu-id="501b2-154">00003</span><span class="sxs-lookup"><span data-stu-id="501b2-154">00003</span></span>   | <span data-ttu-id="501b2-155">31.01.2015</span><span class="sxs-lookup"><span data-stu-id="501b2-155">31-01-2015</span></span> | <span data-ttu-id="501b2-156">Oikaisu</span><span class="sxs-lookup"><span data-stu-id="501b2-156">Adjustment</span></span>     | <span data-ttu-id="501b2-157">100001</span><span class="sxs-lookup"><span data-stu-id="501b2-157">100001</span></span> | <span data-ttu-id="501b2-158">0000101</span><span class="sxs-lookup"><span data-stu-id="501b2-158">0000101</span></span> |          | <span data-ttu-id="501b2-159">15,00</span><span class="sxs-lookup"><span data-stu-id="501b2-159">15.00</span></span>   |

<span data-ttu-id="501b2-160">**Kustannustapahtumat**-sivun avulla voidaan suodattaa asiakirjan tunnuksella ja asiakirjan päivämäärällä.</span><span class="sxs-lookup"><span data-stu-id="501b2-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="501b2-161">Huomautus: Kustannustapahtumat käytettävissä vain [kustannusobjekteja](cost-object.md) tai vapautettuja tuotteita varten.</span><span class="sxs-lookup"><span data-stu-id="501b2-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="additional-resources"></a><span data-ttu-id="501b2-162">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="501b2-162">Additional resources</span></span>
--------

[<span data-ttu-id="501b2-163">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="501b2-163">Cost objects</span></span>](cost-object.md)



