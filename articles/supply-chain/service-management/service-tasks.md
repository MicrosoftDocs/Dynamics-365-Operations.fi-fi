---
title: "Huoltotehtävät"
description: "Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän. Sekä teknikot että asiakkaat näkevät nämä tiedot."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 29b6414fe0127489a93ffe2a564e44dcb7a43b10
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="service-tasks"></a><span data-ttu-id="8c574-104">Huoltotehtävät</span><span class="sxs-lookup"><span data-stu-id="8c574-104">Service tasks</span></span>  

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="8c574-105">Huoltotehtävien avulla voit kuvata huoltotilauksen aikana suoritettavan tehtävän.</span><span class="sxs-lookup"><span data-stu-id="8c574-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="8c574-106">Sekä teknikot että asiakkaat näkevät nämä tiedot.</span><span class="sxs-lookup"><span data-stu-id="8c574-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="8c574-107">Voit luoda huoltotehtäviä **Huoltotehtävät**-sivulla ja liittää niitä tiettyyn huoltosopimukseen tai huoltotilaukseen luomalla huoltotehtävän suhteita.</span><span class="sxs-lookup"><span data-stu-id="8c574-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="8c574-108">Aina kun luot huoltotehtävän suhteen, voit luoda</span><span class="sxs-lookup"><span data-stu-id="8c574-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="8c574-109">tehtävän sisäisiä huomautuksia, esimerkiksi tehtävään liittyviä yksityiskohtaisia teknisiä pyyntöjä, jotka teknikon on tärkeä tietää</span><span class="sxs-lookup"><span data-stu-id="8c574-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="8c574-110">ulkoisia huomautuksia, jotka asiakas voi nähdä.</span><span class="sxs-lookup"><span data-stu-id="8c574-110">External notes that the customer can see.</span></span> <span data-ttu-id="8c574-111">Nämä voivat sisältää vähemmän teknistä tietoa sisältävän selvityksen tehtävästä, jota suoritetaan asiakkaan ja huoltoyhtiön välisen sopimuksen mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="8c574-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="8c574-112">Kun olet määrittänyt huoltotehtävän suhteen huoltotehtävän ja huoltotilauksen tai huoltosopimuksen välille, voit määrittää kyseisen huoltotehtävän luodessasi huoltotilauksen rivejä tai huoltosopimuksen rivejä huoltotilaukseen tai huoltosopimukseen.</span><span class="sxs-lookup"><span data-stu-id="8c574-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="8c574-113">Kun luot huoltotilauksia huoltosopimuksesta, voit ryhmitellä huoltotilauksen rivit huoltotilauksiin huoltosopimuksen riveille määritettyjen huoltotehtävien avulla.</span><span class="sxs-lookup"><span data-stu-id="8c574-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="8c574-114">Huoltotehtävän luominen</span><span class="sxs-lookup"><span data-stu-id="8c574-114">Create a service task</span></span>

1. <span data-ttu-id="8c574-115">Valitse **Huoltohallinta** \> **Asetukset** \> **Palvelutehtävät**.</span><span class="sxs-lookup"><span data-stu-id="8c574-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="8c574-116">Luo uusi rivi.</span><span class="sxs-lookup"><span data-stu-id="8c574-116">Create a new line.</span></span>
3. <span data-ttu-id="8c574-117">Anna huoltotunnus ja kuvaus.</span><span class="sxs-lookup"><span data-stu-id="8c574-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="8c574-118">Esimerkki</span><span class="sxs-lookup"><span data-stu-id="8c574-118">Example</span></span>

<span data-ttu-id="8c574-119">Teknikon on suoritettava kaksi vaihdelaatikkoa (huoltokohde GB-1234) koskevaa työtä asiakkaan toimipisteessä.</span><span class="sxs-lookup"><span data-stu-id="8c574-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="8c574-120">Asiakkaalle on luotu huoltosopimus, ja töihin liittyy useita tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="8c574-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="8c574-121">Näiden kahden työn huoltosopimus ja huoltosopimusrivit ovat seuraavat:</span><span class="sxs-lookup"><span data-stu-id="8c574-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="8c574-122">Huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="8c574-122">Service agreement</span></span>

| <span data-ttu-id="8c574-123">Project</span><span class="sxs-lookup"><span data-stu-id="8c574-123">Project</span></span> | <span data-ttu-id="8c574-124">Huoltosopimus</span><span class="sxs-lookup"><span data-stu-id="8c574-124">Service agreement</span></span> | <span data-ttu-id="8c574-125">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8c574-125">Description</span></span>                                  | <span data-ttu-id="8c574-126">Ryhmä</span><span class="sxs-lookup"><span data-stu-id="8c574-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="8c574-127">9012</span><span class="sxs-lookup"><span data-stu-id="8c574-127">9012</span></span>    | <span data-ttu-id="8c574-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="8c574-128">000008\_001</span></span>       | <span data-ttu-id="8c574-129">Tarkastus ja rutiinivaihto – GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="8c574-130">Lisä</span><span class="sxs-lookup"><span data-stu-id="8c574-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="8c574-131">Huoltosopimuksen rivit</span><span class="sxs-lookup"><span data-stu-id="8c574-131">Service agreement lines</span></span>

| <span data-ttu-id="8c574-132">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8c574-132">Description</span></span>             | <span data-ttu-id="8c574-133">Tapahtumalaji</span><span class="sxs-lookup"><span data-stu-id="8c574-133">Transaction type</span></span> | <span data-ttu-id="8c574-134">Huoltokohde</span><span class="sxs-lookup"><span data-stu-id="8c574-134">Service object</span></span> | <span data-ttu-id="8c574-135">Huoltotehtävä</span><span class="sxs-lookup"><span data-stu-id="8c574-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="8c574-136">Tarkastus ja puhdistus</span><span class="sxs-lookup"><span data-stu-id="8c574-136">Inspection and cleaning</span></span> | <span data-ttu-id="8c574-137">Tunti</span><span class="sxs-lookup"><span data-stu-id="8c574-137">Hour</span></span>             | <span data-ttu-id="8c574-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-138">GB-1234</span></span>        | <span data-ttu-id="8c574-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-139">I/C - GB1234</span></span> |
| <span data-ttu-id="8c574-140">Matkat</span><span class="sxs-lookup"><span data-stu-id="8c574-140">Travel</span></span>                  | <span data-ttu-id="8c574-141">Expense</span><span class="sxs-lookup"><span data-stu-id="8c574-141">Expense</span></span>          | <span data-ttu-id="8c574-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-142">GB-1234</span></span>        | <span data-ttu-id="8c574-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-143">I/C - GB1234</span></span> |
| <span data-ttu-id="8c574-144">Materiaalit</span><span class="sxs-lookup"><span data-stu-id="8c574-144">Materials</span></span>               | <span data-ttu-id="8c574-145">Nimike</span><span class="sxs-lookup"><span data-stu-id="8c574-145">Item</span></span>             | <span data-ttu-id="8c574-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-146">GB-1234</span></span>        | <span data-ttu-id="8c574-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-147">I/C - GB1234</span></span> |
| <span data-ttu-id="8c574-148">Rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="8c574-148">Routine replacement</span></span>     | <span data-ttu-id="8c574-149">Tunti</span><span class="sxs-lookup"><span data-stu-id="8c574-149">Hour</span></span>             | <span data-ttu-id="8c574-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-150">GB-1234</span></span>        | <span data-ttu-id="8c574-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-151">RR - GB1234</span></span>  |
| <span data-ttu-id="8c574-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="8c574-152">GR-1</span></span>                    | <span data-ttu-id="8c574-153">Nimike</span><span class="sxs-lookup"><span data-stu-id="8c574-153">Item</span></span>             | <span data-ttu-id="8c574-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-154">GB-1234</span></span>        | <span data-ttu-id="8c574-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-155">RR - GB1234</span></span>  |
| <span data-ttu-id="8c574-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="8c574-156">GR-5</span></span>                    | <span data-ttu-id="8c574-157">Nimike</span><span class="sxs-lookup"><span data-stu-id="8c574-157">Item</span></span>             | <span data-ttu-id="8c574-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="8c574-158">GB-1234</span></span>        | <span data-ttu-id="8c574-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-159">RR - GB1234</span></span>  |

<span data-ttu-id="8c574-160">Näiden kahden työn huoltosopimuksen riveihin on liitetty kaksi huoltotehtävää.</span><span class="sxs-lookup"><span data-stu-id="8c574-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="8c574-161">Huoltotehtävät määrittävät kuhunkin työhön kuuluvat tehtävät.</span><span class="sxs-lookup"><span data-stu-id="8c574-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="8c574-162">Ensimmäisessä tapauksessa huoltotehtävä I/C - GB1234 yksilöi kaikki kohteen GB-1234 tarkastamiseen ja puhdistamiseen liittyvät huoltosopimuksen rivit.</span><span class="sxs-lookup"><span data-stu-id="8c574-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="8c574-163">Toisessa tapauksessa palvelutehtävä RR - GB1234 yksilöi kaikki rutiinivaihtotyön suorittamiseen liittyvät huoltosopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="8c574-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="8c574-164">Huoltotehtävän suhteet, jotka yhdistävät huoltotehtävät tiettyyn sopimukseen, ovat seuraavanlaiset:</span><span class="sxs-lookup"><span data-stu-id="8c574-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="8c574-165">Huoltotehtävät</span><span class="sxs-lookup"><span data-stu-id="8c574-165">Service tasks</span></span>

| <span data-ttu-id="8c574-166">Huoltotehtävä</span><span class="sxs-lookup"><span data-stu-id="8c574-166">Service task</span></span> | <span data-ttu-id="8c574-167">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="8c574-167">Description</span></span>                             | <span data-ttu-id="8c574-168">Sisäinen huomautus</span><span class="sxs-lookup"><span data-stu-id="8c574-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="8c574-169">Ulkoinen huomautus</span><span class="sxs-lookup"><span data-stu-id="8c574-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="8c574-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-170">I/C - GB1234</span></span> | <span data-ttu-id="8c574-171">Vaihdelaatikon GB-1234 tarkastus</span><span class="sxs-lookup"><span data-stu-id="8c574-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="8c574-172">Vaihdelaatikon GB-1234 visuaalinen ja mekaaninen tarkastus ja puhdistus</span><span class="sxs-lookup"><span data-stu-id="8c574-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="8c574-173">Vaihdelaatikon rutiinitarkastus</span><span class="sxs-lookup"><span data-stu-id="8c574-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="8c574-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="8c574-174">RR - GB1234</span></span>  | <span data-ttu-id="8c574-175">Kohteen GB-1234 osien rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="8c574-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="8c574-176">Komponenttien GR-1 ja GR-5 vaihto osana normaalihuoltoa (ennen vuotta 2002 valmistetuista vaihdelaatikoista vaihdetaan myös komponentti GR-2)</span><span class="sxs-lookup"><span data-stu-id="8c574-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="8c574-177">Osien rutiinivaihto</span><span class="sxs-lookup"><span data-stu-id="8c574-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="8c574-178">Huoltotilausten ryhmittely</span><span class="sxs-lookup"><span data-stu-id="8c574-178">Group service orders</span></span>

<span data-ttu-id="8c574-179">Kun luot huoltotilaukset automaattisesti, voit käyttää huoltotehtäviä ryhmittelyperusteena.</span><span class="sxs-lookup"><span data-stu-id="8c574-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="8c574-180">Voit ryhmitellä huoltotilaukset huoltotehtävien perusteella määrittämällä huoltosopimuksessa, että huoltosopimukseen perustuvat huoltotilaukset ryhmitellään niin, että huoltotehtävän tunnus on ensimmäinen ryhmittelyperuste.</span><span class="sxs-lookup"><span data-stu-id="8c574-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="8c574-181">**Ryhmitteleminen huoltotehtävien perusteella**</span><span class="sxs-lookup"><span data-stu-id="8c574-181">**Group by service task**</span></span>

1. <span data-ttu-id="8c574-182">Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.</span><span class="sxs-lookup"><span data-stu-id="8c574-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="8c574-183">Valitse **Asetukset**-välilehdessä **Huoltotehtävän mukaan** **Yhdistä huoltotilaukset** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="8c574-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>



