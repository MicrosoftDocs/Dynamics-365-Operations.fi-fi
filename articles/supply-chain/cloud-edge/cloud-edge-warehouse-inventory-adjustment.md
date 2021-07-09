---
title: Varasto-oikaisu
description: Tässä aiheessa on tietoja varaston oikaisun kirjauskansiosta ja käsittelystä, kun käytät scale uniteja.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1bf147ce430d84980516d8d4824081ee2a9321a2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271229"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="2508f-103">Varasto-oikaisu</span><span class="sxs-lookup"><span data-stu-id="2508f-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2508f-104">Varaston oikaisuominaisuutta käytetään, kun suoritetaan pilvi- ja reunapalvelujen scale uniteja [valmistuksen kuormituksille](cloud-edge-workload-manufacturing.md) ja [varaston hallinnan kuormituksille](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="2508f-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="2508f-105">Kun työntekijä tekee varaston oikaisun varastosovelluksen avulla scale unitin varastonhallinnan kuormitusta vasten, fyysisen käytettävissä olevan päivityksen käsittelee **Varaston oikaisun kirjauskansio** -erätyö, joka suoritetaan ja ajoitetaan valitsemalla **Varastonhallinta > Kausittaiset tehtävät > Varaston oikaisun kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="2508f-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="2508f-106">Seuraavissa varastosovellusten työprosesseissa käytetään tällä hetkellä **Varaston oikaisun kirjauskansiota** scale unit -kuormituksissa:</span><span class="sxs-lookup"><span data-stu-id="2508f-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="2508f-107">Oikaisu sisään/ulos</span><span class="sxs-lookup"><span data-stu-id="2508f-107">Adjustment in/out</span></span>
- <span data-ttu-id="2508f-108">Inventointi</span><span class="sxs-lookup"><span data-stu-id="2508f-108">Cycle counting</span></span>
- <span data-ttu-id="2508f-109">Rekisterikilven lataus</span><span class="sxs-lookup"><span data-stu-id="2508f-109">License plate loading</span></span>

<span data-ttu-id="2508f-110">Useita varaston tapahtumia luodaan osana kutakin varaston oikaisuprosessia, koska keskuksen ja scale unitin käyttöönotot jakavat varastotietueet.</span><span class="sxs-lookup"><span data-stu-id="2508f-110">Several inventory transactions are created as part of each inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="2508f-111">Varaston oikaisun esimerkki</span><span class="sxs-lookup"><span data-stu-id="2508f-111">Inventory adjustment example</span></span>

<span data-ttu-id="2508f-112">Tässä esimerkissä varastotyöntekijä on rekisteröinyt varastosovelluksen avulla käytettävissä olevan varaston lisäämisen.</span><span class="sxs-lookup"><span data-stu-id="2508f-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="2508f-113">Ensin scale unitin kuormitus luo positiiviselle fyysiselle oikaisulle varaston oikaisutapahtuman, joka tämän jälkeen synkronoidaan keskukseen ja mikä johtaa keskuksen käytettävissä olevan varaston suurenemiseen.</span><span class="sxs-lookup"><span data-stu-id="2508f-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="2508f-114">Laji</span><span class="sxs-lookup"><span data-stu-id="2508f-114">Type</span></span>                                    | <span data-ttu-id="2508f-115">Skaalausyksikkö</span><span class="sxs-lookup"><span data-stu-id="2508f-115">Scale unit</span></span> | <span data-ttu-id="2508f-116">Siirtosuunta</span><span class="sxs-lookup"><span data-stu-id="2508f-116">Direction</span></span> | <span data-ttu-id="2508f-117">Keskus</span><span class="sxs-lookup"><span data-stu-id="2508f-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="2508f-118">Varasto-oikaisu</span><span class="sxs-lookup"><span data-stu-id="2508f-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="2508f-119">+1</span><span class="sxs-lookup"><span data-stu-id="2508f-119">+1</span></span>         | ->        | <span data-ttu-id="2508f-120">+1</span><span class="sxs-lookup"><span data-stu-id="2508f-120">+1</span></span>  |

<span data-ttu-id="2508f-121">Tämän jälkeen keskus käsittelee inventoinnin kirjauskansion kirjauksen, joka vastaanotetaan [sanoman käsittelijän sanomien](cloud-edge-message-processor-messages.md) kautta.</span><span class="sxs-lookup"><span data-stu-id="2508f-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="2508f-122">Tämä päivittää käytettävissä olevan lisävaraston.</span><span class="sxs-lookup"><span data-stu-id="2508f-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="2508f-123">Jotta käytettävissä ei olisi kaksinkertaista varastoa, keskus luo vastatapahtuman prosessin osana ja poistaa varaston oikaisuun liittyvän aiemmin tallennetun käytettävissä olevan varaston.</span><span class="sxs-lookup"><span data-stu-id="2508f-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="2508f-124">Laji</span><span class="sxs-lookup"><span data-stu-id="2508f-124">Type</span></span>                                    | <span data-ttu-id="2508f-125">Skaalausyksikkö</span><span class="sxs-lookup"><span data-stu-id="2508f-125">Scale unit</span></span> | <span data-ttu-id="2508f-126">Siirtosuunta</span><span class="sxs-lookup"><span data-stu-id="2508f-126">Direction</span></span> | <span data-ttu-id="2508f-127">Keskus</span><span class="sxs-lookup"><span data-stu-id="2508f-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="2508f-128">Inventointi</span><span class="sxs-lookup"><span data-stu-id="2508f-128">Counting</span></span>                                | <span data-ttu-id="2508f-129">+1</span><span class="sxs-lookup"><span data-stu-id="2508f-129">+1</span></span>         | <-        | <span data-ttu-id="2508f-130">+1</span><span class="sxs-lookup"><span data-stu-id="2508f-130">+1</span></span>  |
| <span data-ttu-id="2508f-131">Varaston oikaisu (vastakirjaus)</span><span class="sxs-lookup"><span data-stu-id="2508f-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="2508f-132">-1</span><span class="sxs-lookup"><span data-stu-id="2508f-132">-1</span></span>         | <-        | <span data-ttu-id="2508f-133">-1</span><span class="sxs-lookup"><span data-stu-id="2508f-133">-1</span></span>  |

<span data-ttu-id="2508f-134">Kun asteikkoyksikkö on luonut **Varaston oikaisun kirjauskansion** keskuksessa, näkyvissä on sekä **Inventointikirjauskansio** että **Vastakirjauskansio**, jotka keskus luo osana oikaisuprosessia.</span><span class="sxs-lookup"><span data-stu-id="2508f-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="2508f-135">Noudattamalla seuraavia ohjeita voit tarkastella kaikkia näitä kirjauskansiomerkintöjä ja tapahtumia Supply Chain Managementissa:</span><span class="sxs-lookup"><span data-stu-id="2508f-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="2508f-136">Kirjautuu scale unitiin.</span><span class="sxs-lookup"><span data-stu-id="2508f-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="2508f-137">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Varaston oikaisun kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="2508f-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="2508f-138">**Varaston oikaisun kirjauskansio** -sivulla etsi ja avaa kirjauskansio, joka kirjasi käytettävissä olevan varaston muutoksen.</span><span class="sxs-lookup"><span data-stu-id="2508f-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="2508f-139">**Kirjauskansion rivit** -osassa näkyvät kaikki tämän kirjauskansion kirjaamat oikaisut.</span><span class="sxs-lookup"><span data-stu-id="2508f-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="2508f-140">Kirjaudu sisään keskukseen.</span><span class="sxs-lookup"><span data-stu-id="2508f-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="2508f-141">Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Varaston oikaisun kirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="2508f-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="2508f-142">**Varaston oikaisun kirjauskansio** -sivulla pitäisi näkyä sama kirjauskasio, jos keskus ja scale unit on synkronoitu.</span><span class="sxs-lookup"><span data-stu-id="2508f-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="2508f-143">Avaa kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="2508f-143">Open the journal.</span></span> <span data-ttu-id="2508f-144">Jos [sanoman käsittelijän sanomat](cloud-edge-message-processor-messages.md) on käsitelty, näkyvissä ovat linkit otsikon kohtiin **Inventointikirjauskansio** ja **Vastakirjauskansio**.</span><span class="sxs-lookup"><span data-stu-id="2508f-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="2508f-145">**Inventointikirjauskansiossa** tulisi näkyä samat dimensioarvot kuin kirjauskansion riveillä.</span><span class="sxs-lookup"><span data-stu-id="2508f-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="2508f-146">**Vastakirjauskansiossa** tulisi näkyä vastakirjaus, joka poistaa kaksoisvarasto-oikaisun.</span><span class="sxs-lookup"><span data-stu-id="2508f-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="2508f-147">Kun kaikki synkronointi ja käsittely on tehty, **Inventointikirjauskansio** ja **Vastakirjauskansio** synkronoidaan takaisin skaalausyksikköön.</span><span class="sxs-lookup"><span data-stu-id="2508f-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="2508f-148">Voit tarkastella niitä myös asianmukaisella **Varaston oikaisun kirjauskansio** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2508f-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
