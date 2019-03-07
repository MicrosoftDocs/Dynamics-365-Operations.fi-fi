---
title: Huoltotehtävät
description: Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän. Sekä teknikot että asiakkaat näkevät nämä tiedot.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "308595"
---
# <a name="service-tasks"></a><span data-ttu-id="4fb89-104">Huoltotehtävät</span><span class="sxs-lookup"><span data-stu-id="4fb89-104">Service tasks</span></span>  

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fb89-105">Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän.</span><span class="sxs-lookup"><span data-stu-id="4fb89-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="4fb89-106">Sekä teknikot että asiakkaat näkevät nämä tiedot.</span><span class="sxs-lookup"><span data-stu-id="4fb89-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="4fb89-107">Voit luoda huoltotehtäviä **Huoltotehtävät**-sivulla ja liittää niitä tiettyyn huoltosopimukseen tai huoltotilaukseen luomalla huoltotehtävän suhteita.</span><span class="sxs-lookup"><span data-stu-id="4fb89-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="4fb89-108">Aina kun luot huoltotehtävän suhteen, voit luoda</span><span class="sxs-lookup"><span data-stu-id="4fb89-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="4fb89-109">tehtävän sisäisiä huomautuksia, esimerkiksi tehtävään liittyviä yksityiskohtaisia teknisiä pyyntöjä, jotka teknikon on tärkeä tietää</span><span class="sxs-lookup"><span data-stu-id="4fb89-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="4fb89-110">ulkoisia huomautuksia, jotka asiakas voi nähdä.</span><span class="sxs-lookup"><span data-stu-id="4fb89-110">External notes that the customer can see.</span></span> <span data-ttu-id="4fb89-111">Nämä voivat sisältää vähemmän teknistä tietoa sisältävän selvityksen tehtävästä, jota suoritetaan asiakkaan ja huoltoyhtiön välisen sopimuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="4fb89-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="4fb89-112">Kun olet määrittänyt huoltotehtävän suhteen huoltotehtävän ja huoltotilauksen tai huoltosopimuksen välille, voit määrittää kyseisen huoltotehtävän luodessasi huoltotilauksen rivejä tai huoltosopimuksen rivejä huoltotilaukseen tai huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="4fb89-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="4fb89-113">Kun luot huoltotilauksia huoltosopimuksesta, voit ryhmitellä huoltotilauksen rivit huoltotilauksiin huoltosopimuksen riveille määritettyjen huoltotehtävien avulla.</span><span class="sxs-lookup"><span data-stu-id="4fb89-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="4fb89-114">Huoltotehtävän luominen</span><span class="sxs-lookup"><span data-stu-id="4fb89-114">Create a service task</span></span>

1. <span data-ttu-id="4fb89-115">Valitse **Huoltohallinta** \> **Asetukset** \> **Palvelutehtävät**.</span><span class="sxs-lookup"><span data-stu-id="4fb89-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="4fb89-116">Luo uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="4fb89-116">Create a new line.</span></span>
3. <span data-ttu-id="4fb89-117">Anna huoltotunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="4fb89-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="4fb89-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="4fb89-118">Example</span></span>

<span data-ttu-id="4fb89-119">Teknikon on suoritettava kaksi vaihdelaatikkoa (huoltokohde GB-1234) koskevaa työtä asiakkaan toimipisteessä.</span><span class="sxs-lookup"><span data-stu-id="4fb89-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="4fb89-120">Asiakkaalle on luotu huoltosopimus, ja töihin liittyy useita tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="4fb89-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="4fb89-121">Näiden kahden työn huoltosopimus ja huoltosopimusrivit ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="4fb89-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="4fb89-122">Huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="4fb89-122">Service agreement</span></span>

| <span data-ttu-id="4fb89-123">Project</span><span class="sxs-lookup"><span data-stu-id="4fb89-123">Project</span></span> | <span data-ttu-id="4fb89-124">Huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="4fb89-124">Service agreement</span></span> | <span data-ttu-id="4fb89-125">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4fb89-125">Description</span></span>                                  | <span data-ttu-id="4fb89-126">Ryhmä</span><span class="sxs-lookup"><span data-stu-id="4fb89-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="4fb89-127">9012</span><span class="sxs-lookup"><span data-stu-id="4fb89-127">9012</span></span>    | <span data-ttu-id="4fb89-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="4fb89-128">000008\_001</span></span>       | <span data-ttu-id="4fb89-129">Tarkastus ja rutiinivaihto – GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="4fb89-130">Lisä</span><span class="sxs-lookup"><span data-stu-id="4fb89-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="4fb89-131">Huoltosopimuksen rivit</span><span class="sxs-lookup"><span data-stu-id="4fb89-131">Service agreement lines</span></span>

| <span data-ttu-id="4fb89-132">kuvaus</span><span class="sxs-lookup"><span data-stu-id="4fb89-132">Description</span></span>             | <span data-ttu-id="4fb89-133">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="4fb89-133">Transaction type</span></span> | <span data-ttu-id="4fb89-134">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="4fb89-134">Service object</span></span> | <span data-ttu-id="4fb89-135">Huoltotehtävä</span><span class="sxs-lookup"><span data-stu-id="4fb89-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="4fb89-136">Tarkastus ja puhdistus</span><span class="sxs-lookup"><span data-stu-id="4fb89-136">Inspection and cleaning</span></span> | <span data-ttu-id="4fb89-137">Tunti</span><span class="sxs-lookup"><span data-stu-id="4fb89-137">Hour</span></span>             | <span data-ttu-id="4fb89-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-138">GB-1234</span></span>        | <span data-ttu-id="4fb89-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-139">I/C - GB1234</span></span> |
| <span data-ttu-id="4fb89-140">Matkat</span><span class="sxs-lookup"><span data-stu-id="4fb89-140">Travel</span></span>                  | <span data-ttu-id="4fb89-141">Expense</span><span class="sxs-lookup"><span data-stu-id="4fb89-141">Expense</span></span>          | <span data-ttu-id="4fb89-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-142">GB-1234</span></span>        | <span data-ttu-id="4fb89-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-143">I/C - GB1234</span></span> |
| <span data-ttu-id="4fb89-144">Materiaalit</span><span class="sxs-lookup"><span data-stu-id="4fb89-144">Materials</span></span>               | <span data-ttu-id="4fb89-145">Nimike</span><span class="sxs-lookup"><span data-stu-id="4fb89-145">Item</span></span>             | <span data-ttu-id="4fb89-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-146">GB-1234</span></span>        | <span data-ttu-id="4fb89-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-147">I/C - GB1234</span></span> |
| <span data-ttu-id="4fb89-148">Rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="4fb89-148">Routine replacement</span></span>     | <span data-ttu-id="4fb89-149">Tunti</span><span class="sxs-lookup"><span data-stu-id="4fb89-149">Hour</span></span>             | <span data-ttu-id="4fb89-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-150">GB-1234</span></span>        | <span data-ttu-id="4fb89-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-151">RR - GB1234</span></span>  |
| <span data-ttu-id="4fb89-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="4fb89-152">GR-1</span></span>                    | <span data-ttu-id="4fb89-153">Nimike</span><span class="sxs-lookup"><span data-stu-id="4fb89-153">Item</span></span>             | <span data-ttu-id="4fb89-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-154">GB-1234</span></span>        | <span data-ttu-id="4fb89-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-155">RR - GB1234</span></span>  |
| <span data-ttu-id="4fb89-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="4fb89-156">GR-5</span></span>                    | <span data-ttu-id="4fb89-157">Nimike</span><span class="sxs-lookup"><span data-stu-id="4fb89-157">Item</span></span>             | <span data-ttu-id="4fb89-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-158">GB-1234</span></span>        | <span data-ttu-id="4fb89-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-159">RR - GB1234</span></span>  |

<span data-ttu-id="4fb89-160">Näiden kahden työn huoltosopimuksen riveihin on liitetty kaksi huoltotehtävää.</span><span class="sxs-lookup"><span data-stu-id="4fb89-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="4fb89-161">Huoltotehtävät määrittävät kuhunkin työhön kuuluvat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="4fb89-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="4fb89-162">Ensimmäisessä tapauksessa huoltotehtävä I/C - GB1234 yksilöi kaikki kohteen GB-1234 tarkastamiseen ja puhdistamiseen liittyvät huoltosopimuksen rivit.</span><span class="sxs-lookup"><span data-stu-id="4fb89-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="4fb89-163">Toisessa tapauksessa palvelutehtävä RR - GB1234 yksilöi kaikki rutiinivaihtotyön suorittamiseen liittyvät huoltosopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="4fb89-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="4fb89-164">Huoltotehtävän suhteet, jotka yhdistävät huoltotehtävät tiettyyn sopimukseen, ovat seuraavanlaiset:</span><span class="sxs-lookup"><span data-stu-id="4fb89-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="4fb89-165">Huoltotehtävät</span><span class="sxs-lookup"><span data-stu-id="4fb89-165">Service tasks</span></span>

| <span data-ttu-id="4fb89-166">Huoltotehtävä</span><span class="sxs-lookup"><span data-stu-id="4fb89-166">Service task</span></span> | <span data-ttu-id="4fb89-167">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="4fb89-167">Description</span></span>                             | <span data-ttu-id="4fb89-168">Sisäinen huomautus</span><span class="sxs-lookup"><span data-stu-id="4fb89-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="4fb89-169">Ulkoinen huomautus</span><span class="sxs-lookup"><span data-stu-id="4fb89-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="4fb89-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-170">I/C - GB1234</span></span> | <span data-ttu-id="4fb89-171">Vaihdelaatikon GB-1234 tarkastus</span><span class="sxs-lookup"><span data-stu-id="4fb89-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="4fb89-172">Vaihdelaatikon GB-1234 visuaalinen ja mekaaninen tarkastus ja puhdistus</span><span class="sxs-lookup"><span data-stu-id="4fb89-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="4fb89-173">Vaihdelaatikon rutiinitarkastus</span><span class="sxs-lookup"><span data-stu-id="4fb89-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="4fb89-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="4fb89-174">RR - GB1234</span></span>  | <span data-ttu-id="4fb89-175">Kohteen GB-1234 osien rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="4fb89-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="4fb89-176">Komponenttien GR-1 ja GR-5 vaihto osana normaalihuoltoa (ennen vuotta 2002 valmistetuista vaihdelaatikoista vaihdetaan myös komponentti GR-2)</span><span class="sxs-lookup"><span data-stu-id="4fb89-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="4fb89-177">Osien rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="4fb89-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="4fb89-178">Huoltotilausten ryhmittely</span><span class="sxs-lookup"><span data-stu-id="4fb89-178">Group service orders</span></span>

<span data-ttu-id="4fb89-179">Kun luot huoltotilaukset automaattisesti, voit käyttää huoltotehtäviä ryhmittelyperusteena.</span><span class="sxs-lookup"><span data-stu-id="4fb89-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="4fb89-180">Voit ryhmitellä huoltotilaukset huoltotehtävien perusteella määrittämällä huoltosopimuksessa, että huoltosopimukseen perustuvat huoltotilaukset ryhmitellään niin, että huoltotehtävän tunnus on ensimmäinen ryhmittelyperuste.</span><span class="sxs-lookup"><span data-stu-id="4fb89-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="4fb89-181">**Ryhmitteleminen huoltotehtävien perusteella**</span><span class="sxs-lookup"><span data-stu-id="4fb89-181">**Group by service task**</span></span>

1. <span data-ttu-id="4fb89-182">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="4fb89-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="4fb89-183">Valitse **Asetukset**-välilehdessä **Huoltotehtävän mukaan** **Yhdistä huoltotilaukset** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="4fb89-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


