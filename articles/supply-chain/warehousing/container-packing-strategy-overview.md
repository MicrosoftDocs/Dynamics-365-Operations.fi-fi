---
title: Konttien pakkausstrategiat
description: Tässä aiheessa kuvataan konttien pakkausstrategioiden eroja ja annetaan esimerkkejä.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292758"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="615b6-103">Konttien pakkausstrategiat</span><span class="sxs-lookup"><span data-stu-id="615b6-103">Container packing strategies</span></span>

<span data-ttu-id="615b6-104">*Kontin pakkausstrategia* on strategia, jonka avulla voidaan määrittää nimikkeiden kohdistukset konttien välillä.</span><span class="sxs-lookup"><span data-stu-id="615b6-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="615b6-105">Tässä aiheessa kerrotaan *Pakkaa kaikkiin avoimiin kontteihin* -strategian ja *Pakkaa vain nykyiseen konttiin* -strategian eroista.</span><span class="sxs-lookup"><span data-stu-id="615b6-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="615b6-106">**Pakkaa kaikkiin avoimiin kontteihin** - Järjestelmän on tarkistettava kaikki avoimet kontit, jotka on jo luotu konttisyklin aikana, jotta voidaan varmistaa, että nimike sopii yhteen niistä.</span><span class="sxs-lookup"><span data-stu-id="615b6-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="615b6-107">Pakkauksen aikana järjestelmä tarkistaa kunkin nimikkeen ja määrittää, sopiiko se aiemmin luotuihin kontteihin.</span><span class="sxs-lookup"><span data-stu-id="615b6-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="615b6-108">Jos nimike ei mahdu aiemmin luotuun konttiin, järjestelmä luo uuden kontin ja jatkaa sitä, kunnes koko tilaus on pakattu valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="615b6-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="615b6-109">Esimerkiksi *n* tilattua nimikettä edellyttää konttiinpakkaamista.</span><span class="sxs-lookup"><span data-stu-id="615b6-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="615b6-110">Pahimmassa tapauksessa joka kerta, kun järjestelmä käsittelee nimikkeen, joka ei sovi mihinkään konttiin, sen on arvioitava, sopiiko nimike aiemmin luotuihin kontteihin, ja tekee yhteensä (\[(*n* – 1) × (*n* + 1)\] ÷ 2) tarkistusta.</span><span class="sxs-lookup"><span data-stu-id="615b6-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="615b6-111">**Pakkaa vain nykyiseen konttiin** – Järjestelmä on tarkistettava vain, sopiiko nimike viimeksi luotuun konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="615b6-112">Pakkauksen aikana järjestelmä tarkistaa kunkin nimikkeen ja määrittää, sopiiko se viimeisimmäksi luotuun konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="615b6-113">Jos nimike ei mahdu kyseiseen konttiin, järjestelmä luo uuden kontin ja jatkaa sitä, kunnes koko tilaus on pakattu valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="615b6-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="615b6-114">Esimerkiksi *n* tilattua nimikettä edellyttää konttiinpakkaamista.</span><span class="sxs-lookup"><span data-stu-id="615b6-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="615b6-115">Pahimmassa tapauksessa järjestelmä tekee (*n* – 1) tarkistusta arvioidakseen, sopiiko nimike kontteihin.</span><span class="sxs-lookup"><span data-stu-id="615b6-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="615b6-116">Esimerkki konttien pakkausstrategioiden työnkulusta</span><span class="sxs-lookup"><span data-stu-id="615b6-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="615b6-117">Konttiinpakkaukselle määritetään seuraavat nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="615b6-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="615b6-118">Nimike</span><span class="sxs-lookup"><span data-stu-id="615b6-118">Item</span></span> | <span data-ttu-id="615b6-119">Fyysiset dimensiot (leveys × syvyys × korkeus)</span><span class="sxs-lookup"><span data-stu-id="615b6-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="615b6-120">Paino</span><span class="sxs-lookup"><span data-stu-id="615b6-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="615b6-121">HDMI-kaapeli 6'</span><span class="sxs-lookup"><span data-stu-id="615b6-121">HDMI Cable 6'</span></span> | <span data-ttu-id="615b6-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="615b6-122">1 × 1 × 1</span></span> | <span data-ttu-id="615b6-123">1</span><span class="sxs-lookup"><span data-stu-id="615b6-123">1</span></span> |
| <span data-ttu-id="615b6-124">HDMI-kaapeli 12'</span><span class="sxs-lookup"><span data-stu-id="615b6-124">HDMI Cable 12'</span></span> | <span data-ttu-id="615b6-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="615b6-125">2 × 1 × 1</span></span> | <span data-ttu-id="615b6-126">1</span><span class="sxs-lookup"><span data-stu-id="615b6-126">1</span></span> |
| <span data-ttu-id="615b6-127">HDMI-kaapeli 18'</span><span class="sxs-lookup"><span data-stu-id="615b6-127">HDMI Cable 18'</span></span> | <span data-ttu-id="615b6-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="615b6-128">3 × 1 × 1</span></span> | <span data-ttu-id="615b6-129">2</span><span class="sxs-lookup"><span data-stu-id="615b6-129">2</span></span> |

<span data-ttu-id="615b6-130">Pakkausta varten määritetään myös seuraava laatikko.</span><span class="sxs-lookup"><span data-stu-id="615b6-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="615b6-131">Säilö</span><span class="sxs-lookup"><span data-stu-id="615b6-131">Container</span></span> | <span data-ttu-id="615b6-132">Fyysiset dimensiot (pituus × leveys × korkeus)</span><span class="sxs-lookup"><span data-stu-id="615b6-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="615b6-133">Paino</span><span class="sxs-lookup"><span data-stu-id="615b6-133">Weight</span></span> | <span data-ttu-id="615b6-134">Tilavuus</span><span class="sxs-lookup"><span data-stu-id="615b6-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="615b6-135">Keskikokoinen laatikko</span><span class="sxs-lookup"><span data-stu-id="615b6-135">Medium Box</span></span> | <span data-ttu-id="615b6-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="615b6-136">6 × 3 × 2</span></span> | <span data-ttu-id="615b6-137">10</span><span class="sxs-lookup"><span data-stu-id="615b6-137">10</span></span> | <span data-ttu-id="615b6-138">100</span><span class="sxs-lookup"><span data-stu-id="615b6-138">100</span></span> |

<span data-ttu-id="615b6-139">Lopuksi määritetään tilaus, jossa on seuraavat tuotteet ja määrät.</span><span class="sxs-lookup"><span data-stu-id="615b6-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="615b6-140">Myyntitilausrivi</span><span class="sxs-lookup"><span data-stu-id="615b6-140">Sales order line</span></span> | <span data-ttu-id="615b6-141">Määrä</span><span class="sxs-lookup"><span data-stu-id="615b6-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="615b6-142">HDMI-kaapeli 12'</span><span class="sxs-lookup"><span data-stu-id="615b6-142">HDMI Cable 12'</span></span> | <span data-ttu-id="615b6-143">9</span><span class="sxs-lookup"><span data-stu-id="615b6-143">9</span></span> |
| <span data-ttu-id="615b6-144">HDMI-kaapeli 18'</span><span class="sxs-lookup"><span data-stu-id="615b6-144">HDMI Cable 18'</span></span> | <span data-ttu-id="615b6-145">8</span><span class="sxs-lookup"><span data-stu-id="615b6-145">8</span></span> |
| <span data-ttu-id="615b6-146">HDMI-kaapeli 6'</span><span class="sxs-lookup"><span data-stu-id="615b6-146">HDMI Cable 6'</span></span> | <span data-ttu-id="615b6-147">13</span><span class="sxs-lookup"><span data-stu-id="615b6-147">13</span></span> |

<span data-ttu-id="615b6-148">Seuraavassa taulukossa on yhteenveto siitä, miten konttiin pakkaaminen toimii, kun käytät *Pakkaa kaikkiin avoimiin kontteihin* -strategiaa ja kun käytät *Pakkaa vain nykyiseen konttiin* -strategiaa.</span><span class="sxs-lookup"><span data-stu-id="615b6-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="615b6-149">Pakkaa kaikkiin avoimiin kontteihin</span><span class="sxs-lookup"><span data-stu-id="615b6-149">Pack into all open containers</span></span> | <span data-ttu-id="615b6-150">Pakkaa nykyiseen konttiin</span><span class="sxs-lookup"><span data-stu-id="615b6-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="615b6-151">HDMI-kaapeli 12':</span><span class="sxs-lookup"><span data-stu-id="615b6-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="615b6-152">Luo uusi kontti, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="615b6-153">Aseta 9 kpl konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="615b6-154">HDMI-kaapeli 12':</span><span class="sxs-lookup"><span data-stu-id="615b6-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="615b6-155">Luo uusi kontti, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="615b6-156">Aseta 9 kpl konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="615b6-157">HDMI-kaapeli 18':</span><span class="sxs-lookup"><span data-stu-id="615b6-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="615b6-158">Tarkista, sopiiko nimike konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="615b6-159">Luo uusi kontti, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="615b6-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="615b6-160">Aseta 5 kpl konttiin CONT0002.</span><span class="sxs-lookup"><span data-stu-id="615b6-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="615b6-161">Luo uusi kontti, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="615b6-162">Aseta 3 kpl konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="615b6-163">HDMI-kaapeli 18':</span><span class="sxs-lookup"><span data-stu-id="615b6-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="615b6-164">Tarkista, sopiiko nimike konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="615b6-165">Luo uusi kontti, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="615b6-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="615b6-166">Aseta 5 kpl konttiin CONT0002.</span><span class="sxs-lookup"><span data-stu-id="615b6-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="615b6-167">Luo uusi kontti, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="615b6-168">Aseta 3 kpl konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="615b6-169">HDMI-kaapeli 6':</span><span class="sxs-lookup"><span data-stu-id="615b6-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="615b6-170">Tarkista, sopiiko nimike konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="615b6-171">Aseta 1 kpl konttiin CONT0001.</span><span class="sxs-lookup"><span data-stu-id="615b6-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="615b6-172">Tarkista, sopiiko nimike konttiin CONT0002.</span><span class="sxs-lookup"><span data-stu-id="615b6-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="615b6-173">Tarkista, sopiiko nimike konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="615b6-174">Aseta 4 kpl konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="615b6-175">Luo uusi kontti, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="615b6-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="615b6-176">Aseta 8 kpl konttiin CONT0004.</span><span class="sxs-lookup"><span data-stu-id="615b6-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="615b6-177">HDMI-kaapeli 6':</span><span class="sxs-lookup"><span data-stu-id="615b6-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="615b6-178">Tarkista, sopiiko nimike konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="615b6-179">Aseta 4 kpl konttiin CONT0003.</span><span class="sxs-lookup"><span data-stu-id="615b6-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="615b6-180">Luo uusi kontti, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="615b6-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="615b6-181">Aseta 9 kpl konttiin CONT0004.</span><span class="sxs-lookup"><span data-stu-id="615b6-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="615b6-182">Esimerkki: Yksittäisten tilausten pakkaaminen konttia kohden</span><span class="sxs-lookup"><span data-stu-id="615b6-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="615b6-183">Tässä osassa esitetään skenaario, jossa järjestelmä on määritetty konsolidoimaan useita tilauksia yhdeksi lähetykseksi.</span><span class="sxs-lookup"><span data-stu-id="615b6-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="615b6-184">Siksi konttiinpakkaus tehdään myyntitilauksesta, jotta jokainen useaa tuotetta sisältävä tilaus pakataan omaan konttiinsa.</span><span class="sxs-lookup"><span data-stu-id="615b6-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="615b6-185">Tämän toiminnon avulla voit käsitellä skenaarioita, joissa kuhunkin konttiin on pakattava vain yksi myyntitilaus, jotta jakelukeskus voi cross dock -käsitellä täysiä kontteja vähittäismyyntiliikkeiden välillä.</span><span class="sxs-lookup"><span data-stu-id="615b6-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="615b6-186">Vähittäismyyntiskenaarioiden (myymäläkohtainen tilaus ja cross dockingia varten jakelukeskukseen lähettäminen) lisäksi tätä menetelmää käytetään usein lean-toimitusketjuissa (myyntitilaus just-in-time -tuotantoriviä kohden).</span><span class="sxs-lookup"><span data-stu-id="615b6-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="615b6-187">Tässä skenaariossa kerrotaan, miten pakkausten aikana arvioitujen konttien määrää voidaan vähentää käyttämällä *Pakkaa vain nykyiseen konttiin* -strategiaa.</span><span class="sxs-lookup"><span data-stu-id="615b6-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="615b6-188">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="615b6-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="615b6-189">Lähetysten konsolidointiominaisuuden käyttöön ottaminen järjestelmässä</span><span class="sxs-lookup"><span data-stu-id="615b6-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="615b6-190">Tässä skenaariossa käytetään *Konsolidoi lähetykset* -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="615b6-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="615b6-191">Jos tämä toiminto ei ole vielä käytettävissä järjestelmässä, se on otettava käyttöön käyttämällä [Ominaisuuksien hallintaa](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="615b6-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="615b6-192">Demotietojen ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="615b6-192">Make demo data available</span></span>

<span data-ttu-id="615b6-193">Tässä skenaariossa viitataan arvoihin ja tietueisiin, jotka sisältyvät Microsoft Dynamics 365 Supply Chain Managementin vakiodemotietoihin.</span><span class="sxs-lookup"><span data-stu-id="615b6-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="615b6-194">Jos haluat käyttää harjoituksissa näitä annettuja arvoja, varmista, että demotiedot on asennettu työskentely-ympäristöön ja että yritykseksi on valittu **USMF** ennen aloittamista.</span><span class="sxs-lookup"><span data-stu-id="615b6-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="615b6-195">Konttityyppien tarkastaminen tai luominen</span><span class="sxs-lookup"><span data-stu-id="615b6-195">Inspect or create container types</span></span>

<span data-ttu-id="615b6-196">Noudattamalla seuraavia ohjeita voit tarkistaa konttityypit tai luoda tarvittaessa uusia konttityyppejä.</span><span class="sxs-lookup"><span data-stu-id="615b6-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="615b6-197">Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttityypit**.</span><span class="sxs-lookup"><span data-stu-id="615b6-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="615b6-198">Varmista, että esittelytiedoissa on käytettävissä kukin seuraavista konttityypeistä.</span><span class="sxs-lookup"><span data-stu-id="615b6-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="615b6-199">Muokkaa tai luo konttityyppejä tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="615b6-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="615b6-200">Konttityyppi 1:</span><span class="sxs-lookup"><span data-stu-id="615b6-200">Container type 1:</span></span>

        - <span data-ttu-id="615b6-201">**Konttityypin koodi:** *Laatikko-suuri*</span><span class="sxs-lookup"><span data-stu-id="615b6-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="615b6-202">**Kuvaus:** *Suuri laatikko*</span><span class="sxs-lookup"><span data-stu-id="615b6-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="615b6-203">**Enimmäisnettopaino:** *100*</span><span class="sxs-lookup"><span data-stu-id="615b6-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="615b6-204">**Tilavuus:** *400*</span><span class="sxs-lookup"><span data-stu-id="615b6-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="615b6-205">**Pituus:** *4*</span><span class="sxs-lookup"><span data-stu-id="615b6-205">**Length:** *4*</span></span>
        - <span data-ttu-id="615b6-206">**Leveys:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-206">**Width:** *10*</span></span>
        - <span data-ttu-id="615b6-207">**Korkeus:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-207">**Height:** *10*</span></span>

    - <span data-ttu-id="615b6-208">Konttityyppi 2:</span><span class="sxs-lookup"><span data-stu-id="615b6-208">Container type 2:</span></span>

        - <span data-ttu-id="615b6-209">**Konttityypin koodi:** *Laatikko-keskisuuri*</span><span class="sxs-lookup"><span data-stu-id="615b6-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="615b6-210">**Kuvaus:** *Keskikokoinen laatikko*</span><span class="sxs-lookup"><span data-stu-id="615b6-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="615b6-211">**Enimmäisnettopaino:** *50*</span><span class="sxs-lookup"><span data-stu-id="615b6-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="615b6-212">**Tilavuus:** *200*</span><span class="sxs-lookup"><span data-stu-id="615b6-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="615b6-213">**Pituus:** *2*</span><span class="sxs-lookup"><span data-stu-id="615b6-213">**Length:** *2*</span></span>
        - <span data-ttu-id="615b6-214">**Leveys:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-214">**Width:** *10*</span></span>
        - <span data-ttu-id="615b6-215">**Korkeus:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-215">**Height:** *10*</span></span>

    - <span data-ttu-id="615b6-216">Konttityyppi 3:</span><span class="sxs-lookup"><span data-stu-id="615b6-216">Container type 3:</span></span>

        - <span data-ttu-id="615b6-217">**Konttityypin koodi:** *Laatikko-pieni*</span><span class="sxs-lookup"><span data-stu-id="615b6-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="615b6-218">**Kuvaus:** *Pieni laatikko*</span><span class="sxs-lookup"><span data-stu-id="615b6-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="615b6-219">**Enimmäisnettopaino:** *20*</span><span class="sxs-lookup"><span data-stu-id="615b6-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="615b6-220">**Tilavuus:** *100*</span><span class="sxs-lookup"><span data-stu-id="615b6-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="615b6-221">**Pituus:** *1*</span><span class="sxs-lookup"><span data-stu-id="615b6-221">**Length:** *1*</span></span>
        - <span data-ttu-id="615b6-222">**Leveys:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-222">**Width:** *10*</span></span>
        - <span data-ttu-id="615b6-223">**Korkeus:** *10*</span><span class="sxs-lookup"><span data-stu-id="615b6-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="615b6-224">Konttiryhmien tarkastaminen tai luominen</span><span class="sxs-lookup"><span data-stu-id="615b6-224">Inspect or create container groups</span></span>

<span data-ttu-id="615b6-225">Noudattamalla seuraavia ohjeita voit tarkistaa konttiryhmät tai luoda tarvittaessa uusia konttiryhmiä.</span><span class="sxs-lookup"><span data-stu-id="615b6-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="615b6-226">Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttiryhmät**.</span><span class="sxs-lookup"><span data-stu-id="615b6-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="615b6-227">Varmista, että esittelytiedoissa on käytettävissä seuraavat konttiryhmät.</span><span class="sxs-lookup"><span data-stu-id="615b6-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="615b6-228">Jos se ei ole käytettävissä, luo se valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="615b6-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="615b6-229">**Konttiryhmän tunnus:** *Laatikot*</span><span class="sxs-lookup"><span data-stu-id="615b6-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="615b6-230">**Kuvaus:** *Laatikoiden koot*</span><span class="sxs-lookup"><span data-stu-id="615b6-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="615b6-231">Varmista *Laatikot*-konttiryhmän **Erittely**-pikavälilehdessä, että seuraavat rivit ovat olemassa.</span><span class="sxs-lookup"><span data-stu-id="615b6-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="615b6-232">Jos niitä ei ole, lisää ne valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="615b6-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="615b6-233">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="615b6-233">Line 1:</span></span>

        - <span data-ttu-id="615b6-234">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="615b6-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="615b6-235">**Kontin tyyppi:** *Laatikko-suuri*</span><span class="sxs-lookup"><span data-stu-id="615b6-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="615b6-236">**Kontin käyttöasteprosentti:** *100*</span><span class="sxs-lookup"><span data-stu-id="615b6-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="615b6-237">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="615b6-237">Line 2:</span></span>

        - <span data-ttu-id="615b6-238">**Järjestysnumero:** *2*</span><span class="sxs-lookup"><span data-stu-id="615b6-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="615b6-239">**Konttityyppi:** *Laatikko-keskisuuri*</span><span class="sxs-lookup"><span data-stu-id="615b6-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="615b6-240">**Kontin käyttöasteprosentti:** *100*</span><span class="sxs-lookup"><span data-stu-id="615b6-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="615b6-241">Rivi 3:</span><span class="sxs-lookup"><span data-stu-id="615b6-241">Line 3:</span></span>

        - <span data-ttu-id="615b6-242">**Järjestysnumero:** *3*</span><span class="sxs-lookup"><span data-stu-id="615b6-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="615b6-243">**Konttityyppi:** *Laatikko-pieni*</span><span class="sxs-lookup"><span data-stu-id="615b6-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="615b6-244">**Kontin käyttöasteprosentti:** *100*</span><span class="sxs-lookup"><span data-stu-id="615b6-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="615b6-245">Luo uusi kontin rakennusmalli</span><span class="sxs-lookup"><span data-stu-id="615b6-245">Create a new container build template</span></span>

<span data-ttu-id="615b6-246">Voit luoda uuden kontin muodostusmallin noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="615b6-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="615b6-247">Valitse **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Kontin koontimalli**.</span><span class="sxs-lookup"><span data-stu-id="615b6-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="615b6-248">Valitse **Uusi**, jos haluat luoda kontin rakennusmallin, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="615b6-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="615b6-249">**Järjestysnumero:** *1*</span><span class="sxs-lookup"><span data-stu-id="615b6-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="615b6-250">**Konttimallin tunnus:** *Laatikko*</span><span class="sxs-lookup"><span data-stu-id="615b6-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="615b6-251">**Konttiryhmän tunnus:** *Laatikot*</span><span class="sxs-lookup"><span data-stu-id="615b6-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="615b6-252">**Peruskyselytyypit:** *Myynnin kohdistusrivi*</span><span class="sxs-lookup"><span data-stu-id="615b6-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="615b6-253">**Aallon vaihekoodi:** *234*</span><span class="sxs-lookup"><span data-stu-id="615b6-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="615b6-254">**Salli jaetut valinnat:** *Kyllä*</span><span class="sxs-lookup"><span data-stu-id="615b6-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="615b6-255">**Kontin pakkausstrategia:** *Pakkaa vain nykyiseen konttiin*</span><span class="sxs-lookup"><span data-stu-id="615b6-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="615b6-256">**Pakkaaminen direktiiviyksikön mukaan:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="615b6-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="615b6-257">Kun uuden mallin rivi on vielä valittuna, valitse **Muokkaa kyselyä** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="615b6-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="615b6-258">Näyttöön tulee vakiokyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="615b6-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="615b6-259">Lisää seuraavat asetukset sisältävä rivi valitsemalla **Lajittelu**-välilehdessä **Lisää**:</span><span class="sxs-lookup"><span data-stu-id="615b6-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="615b6-260">**Taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="615b6-261">**Johdettu taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="615b6-262">**Kenttä:** *Tilausnumero*</span><span class="sxs-lookup"><span data-stu-id="615b6-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="615b6-263">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="615b6-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="615b6-264">Kun haluat välttää kierrättämisen muiden avoimien konttien kautta ja nopeuttaa prosessia tarkistamalla yhden kontin kerrallaan, käytä *Pakkaa vain nykyiseen konttiin* -strategiaa tilausnumeron mukaan lajittelun lisäksi.</span><span class="sxs-lookup"><span data-stu-id="615b6-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="615b6-265">Tämä yhdistelmä toimii kuten työmallin työtauko.</span><span class="sxs-lookup"><span data-stu-id="615b6-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="615b6-266">Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="615b6-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="615b6-267">Kun uuden mallin rivi on vielä valittuna, valitse **Kontin yhdistämisrajoitukset** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="615b6-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="615b6-268">Lisäät nyt rajoitus, joka asettaa nimikkeet yksittäisestä tilauksesta yhteen konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="615b6-269">Minkä tahansa tilauksen nimikkeet laitetaan erilliseen konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="615b6-270">Valitse **Uusi**, jos haluat luoda yhdistämisrajoituksen, jolla on seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="615b6-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="615b6-271">**Taulu:** *Myyntitilaukset*</span><span class="sxs-lookup"><span data-stu-id="615b6-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="615b6-272">**Kentän valinta:** *SalesId* (kenttä näkyy ruudukossa *myyntitilauksena*.)</span><span class="sxs-lookup"><span data-stu-id="615b6-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="615b6-273">Valitse **OK** lisätäksesi rajoituksen.</span><span class="sxs-lookup"><span data-stu-id="615b6-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="615b6-274">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="615b6-275">Aseta aaltomalli konttiinpakkausta varten</span><span class="sxs-lookup"><span data-stu-id="615b6-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="615b6-276">Määritä aaltomalli noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="615b6-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="615b6-277">Valitse **Varastonhallinta \> Asetukset \> Aallot \> Aaltomallit**.</span><span class="sxs-lookup"><span data-stu-id="615b6-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="615b6-278">Aseta luetteloruudussa **Aaltomallityyppi**-kentän arvoksi *Lähetys*.</span><span class="sxs-lookup"><span data-stu-id="615b6-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="615b6-279">Valitse luettelosta **63 - konttiinpakkaus** -malli.</span><span class="sxs-lookup"><span data-stu-id="615b6-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="615b6-280">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="615b6-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="615b6-281">Etsi **Menetelmät**-välilehden **Valitut menetelmät**-sarakkeesta seuraava rivi:</span><span class="sxs-lookup"><span data-stu-id="615b6-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="615b6-282">**Menetelmän nimi:** *konttiinpakkaus*</span><span class="sxs-lookup"><span data-stu-id="615b6-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="615b6-283">**Nimi:** *Konttiinpakkaus*</span><span class="sxs-lookup"><span data-stu-id="615b6-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="615b6-284">Määritä **Aallon vaihekoodi** -kentän arvoksi riville *234*.</span><span class="sxs-lookup"><span data-stu-id="615b6-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="615b6-285">Määritä työmalli</span><span class="sxs-lookup"><span data-stu-id="615b6-285">Set up a work template</span></span>

<span data-ttu-id="615b6-286">Määritä työmalli noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="615b6-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="615b6-287">Siirry kohtaan **Varastonhallinta \> Asetukset \> Työ \> Työmallit**.</span><span class="sxs-lookup"><span data-stu-id="615b6-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="615b6-288">Määritä **Työtilaustyyppi**-kentän arvoksi *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="615b6-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="615b6-289">Etsi ja valitse **Yleiskatsaus**-ruudukossa työmalli, jota pitää käyttää yksittäisten tilausten pakkaamiseen yhteen konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="615b6-290">Valitse tässä skenaariossa **63 – poimi konttiin** -malli.</span><span class="sxs-lookup"><span data-stu-id="615b6-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="615b6-291">Valitse toimintoruudussa **Muokkaa kyselyä**.</span><span class="sxs-lookup"><span data-stu-id="615b6-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="615b6-292">Näyttöön tulee vakiokyselyeditorin valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="615b6-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="615b6-293">Lisää **Lajittelu**-välilehdelle seuraavat rivit:</span><span class="sxs-lookup"><span data-stu-id="615b6-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="615b6-294">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="615b6-294">Line 1:</span></span>

        - <span data-ttu-id="615b6-295">**Taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-296">**Johdettu taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-297">**Kenttä:** *Lähetyksen tunnus*</span><span class="sxs-lookup"><span data-stu-id="615b6-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="615b6-298">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="615b6-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="615b6-299">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="615b6-299">Line 2:</span></span>

        - <span data-ttu-id="615b6-300">**Taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-301">**Johdettu taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-302">**Kenttä:** *Tilausnumero*</span><span class="sxs-lookup"><span data-stu-id="615b6-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="615b6-303">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="615b6-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="615b6-304">Rivi 3:</span><span class="sxs-lookup"><span data-stu-id="615b6-304">Line 3:</span></span>

        - <span data-ttu-id="615b6-305">**Taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-306">**Johdettu taulukko:** *Väliaikaiset työtapahtumat*</span><span class="sxs-lookup"><span data-stu-id="615b6-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="615b6-307">**Kenttä:** *Kontin tunnus*</span><span class="sxs-lookup"><span data-stu-id="615b6-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="615b6-308">**Hakusuunta:** *Laskeva*</span><span class="sxs-lookup"><span data-stu-id="615b6-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="615b6-309">Sulje kyselyeditorin valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="615b6-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="615b6-310">Seuraava sanoma avautuu: Ryhmittely nollataan. Haluatko jatkaa?</span><span class="sxs-lookup"><span data-stu-id="615b6-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="615b6-311">Jatka valitsemalla **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="615b6-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="615b6-312">Kun **63 – poimi konttiin** -malli on yhä valittuna, valitse **Työn otsikoiden katkaisut** toimintoruudusta.</span><span class="sxs-lookup"><span data-stu-id="615b6-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="615b6-313">Työn katkaisemiseen käytetään nyt asetuksia, jotta tilauksen kukin kontti linkitetään yhteen työtilaukseen.</span><span class="sxs-lookup"><span data-stu-id="615b6-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="615b6-314">Valitse **Työn otsikoiden katkaisut** -sivun jokaisen rivin **Ryhmittele tämän kentän mukaan** -valintaruutu (**lähetystunnus**, **tilausnumero** ja **kontin tunnus**).</span><span class="sxs-lookup"><span data-stu-id="615b6-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="615b6-315">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="615b6-316">Määritä lähetyksen konsolidoinnin käytännöt</span><span class="sxs-lookup"><span data-stu-id="615b6-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="615b6-317">Lähetyksen konsolidointikäytäntö määritetään seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="615b6-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="615b6-318">Valitse **Varastonhallinta \> Asetukset \> Vapauta varastoon \> Lähetyksen konsolidointikäytännöt**.</span><span class="sxs-lookup"><span data-stu-id="615b6-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="615b6-319">Määritä luetteloruudussa **Käytännön tyyppi**-kentän arvoksi *Myyntitilaukset*.</span><span class="sxs-lookup"><span data-stu-id="615b6-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="615b6-320">Valitse luettelosta **Oletus**-käytäntö.</span><span class="sxs-lookup"><span data-stu-id="615b6-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="615b6-321">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="615b6-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="615b6-322">Valitse **Konsolidointikentät**-pikavälilehden **Valitut kentät** -luettelossa rivi, jossa **Kentän nimi** -kentän asetuksena *Tilausnumero*.</span><span class="sxs-lookup"><span data-stu-id="615b6-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="615b6-323">Siirrä kenttä **Jäljellä olevat kentät** -luetteloon valitsemalla **Poista**-painike ![vasen nuoli](media/backward-button.png).</span><span class="sxs-lookup"><span data-stu-id="615b6-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="615b6-324">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="615b6-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="615b6-325">Määritä tuotteen fyysiset mitat</span><span class="sxs-lookup"><span data-stu-id="615b6-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="615b6-326">Noudattamalla seuraavia ohjeita voit määrittää tässä skenaariossa käytettävät tuotteiden fyysiset mitat.</span><span class="sxs-lookup"><span data-stu-id="615b6-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="615b6-327">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="615b6-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="615b6-328">Valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *A0001*.</span><span class="sxs-lookup"><span data-stu-id="615b6-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="615b6-329">Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.</span><span class="sxs-lookup"><span data-stu-id="615b6-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="615b6-330">**Fyysiset mitat** -sivulla ruudukossa on seuraava rivi:</span><span class="sxs-lookup"><span data-stu-id="615b6-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="615b6-331">**Yksikkö:** *kpl*</span><span class="sxs-lookup"><span data-stu-id="615b6-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="615b6-332">**Bruttopaino:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="615b6-333">**Leveys:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="615b6-334">**Syvyys:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="615b6-335">**Korkeus:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="615b6-336">**Tilavuus:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="615b6-337">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-337">Close the page.</span></span>
1. <span data-ttu-id="615b6-338">Valitse tuote, jossa **Nimiketunnus**-kentän arvoksi on määritetty *A0002*.</span><span class="sxs-lookup"><span data-stu-id="615b6-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="615b6-339">Valitse toimintoruudun **Varastonhallinta**-välilehden **Varasto**-ryhmässä **Fyysiset mitat**.</span><span class="sxs-lookup"><span data-stu-id="615b6-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="615b6-340">**Fyysiset mitat** -sivulla ruudukossa on seuraava rivi:</span><span class="sxs-lookup"><span data-stu-id="615b6-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="615b6-341">**Yksikkö:** *kpl*</span><span class="sxs-lookup"><span data-stu-id="615b6-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="615b6-342">**Bruttopaino:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="615b6-343">**Leveys:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="615b6-344">**Syvyys:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="615b6-345">**Korkeus:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="615b6-346">**Tilavuus:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="615b6-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="615b6-347">Luo myyntitilaus 1</span><span class="sxs-lookup"><span data-stu-id="615b6-347">Create sales order 1</span></span>

<span data-ttu-id="615b6-348">Luo myyntitilaus seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="615b6-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="615b6-349">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="615b6-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="615b6-350">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="615b6-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="615b6-351">Näyttöön tulee valintaikkuna, jossa voit luoda uuden myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="615b6-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="615b6-352">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="615b6-352">Set the following values:</span></span>

    - <span data-ttu-id="615b6-353">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="615b6-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="615b6-354">**Varasto**: *63*</span><span class="sxs-lookup"><span data-stu-id="615b6-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="615b6-355">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="615b6-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="615b6-356">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="615b6-356">The new sales order is opened.</span></span> <span data-ttu-id="615b6-357">Lisää seuraavat myyntirivit **Myyntitilausrivit**-pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="615b6-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="615b6-358">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="615b6-358">Line 1:</span></span>

        - <span data-ttu-id="615b6-359">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="615b6-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="615b6-360">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="615b6-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="615b6-361">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="615b6-361">Line 2:</span></span>

        - <span data-ttu-id="615b6-362">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="615b6-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="615b6-363">**Määrä** *2*</span><span class="sxs-lookup"><span data-stu-id="615b6-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="615b6-364">Valitse ensimmäinen rivi ja valitse sitten **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="615b6-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="615b6-365">Valitse **Varaus**-sivun kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="615b6-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="615b6-366">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-366">Then close the page.</span></span>
1. <span data-ttu-id="615b6-367">Toista kaksi edellistä vaihetta toiselle riville.</span><span class="sxs-lookup"><span data-stu-id="615b6-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="615b6-368">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="615b6-369">Luo myyntitilaus 2</span><span class="sxs-lookup"><span data-stu-id="615b6-369">Create sales order 2</span></span>

<span data-ttu-id="615b6-370">Luo toinen myyntitilaus seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="615b6-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="615b6-371">Valitse **Myynti ja markkinointi \> Myyntitilaukset \> Kaikki myyntitilaukset**.</span><span class="sxs-lookup"><span data-stu-id="615b6-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="615b6-372">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="615b6-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="615b6-373">Näyttöön tulee valintaikkuna, jossa voit luoda uuden myyntitilauksen.</span><span class="sxs-lookup"><span data-stu-id="615b6-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="615b6-374">Määritä seuraavat arvot:</span><span class="sxs-lookup"><span data-stu-id="615b6-374">Set the following values:</span></span>

    - <span data-ttu-id="615b6-375">**Asiakastili:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="615b6-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="615b6-376">**Varasto**: *63*</span><span class="sxs-lookup"><span data-stu-id="615b6-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="615b6-377">Valitse **OK** luodaksesi ostotilauksen ja sulje valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="615b6-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="615b6-378">Uusi myyntitilaus avataan.</span><span class="sxs-lookup"><span data-stu-id="615b6-378">The new sales order is opened.</span></span> <span data-ttu-id="615b6-379">Lisää seuraavat myyntirivit **Myyntitilausrivit**-pikavälilehdessä:</span><span class="sxs-lookup"><span data-stu-id="615b6-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="615b6-380">Rivi 1:</span><span class="sxs-lookup"><span data-stu-id="615b6-380">Line 1:</span></span>

        - <span data-ttu-id="615b6-381">**Nimiketunnus:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="615b6-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="615b6-382">**Määrä** *4*</span><span class="sxs-lookup"><span data-stu-id="615b6-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="615b6-383">Rivi 2:</span><span class="sxs-lookup"><span data-stu-id="615b6-383">Line 2:</span></span>

        - <span data-ttu-id="615b6-384">**Nimiketunnus:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="615b6-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="615b6-385">**Määrä** *4*</span><span class="sxs-lookup"><span data-stu-id="615b6-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="615b6-386">Valitse ensimmäinen rivi ja valitse sitten **Varasto \> Varaus**.</span><span class="sxs-lookup"><span data-stu-id="615b6-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="615b6-387">Valitse **Varaus**-sivun kohta **Varaa erä**.</span><span class="sxs-lookup"><span data-stu-id="615b6-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="615b6-388">Sulje sitten sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-388">Then close the page.</span></span>
1. <span data-ttu-id="615b6-389">Toista kaksi edellistä vaihetta toiselle riville.</span><span class="sxs-lookup"><span data-stu-id="615b6-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="615b6-390">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="615b6-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="615b6-391">Kuorman luominen</span><span class="sxs-lookup"><span data-stu-id="615b6-391">Create the load</span></span>

<span data-ttu-id="615b6-392">Luo jokaiselle tähän skenaarioon luodulle tilaukselle kuorma ja vapauta se sitten varastoon näiden ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="615b6-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="615b6-393">Valitse **Varastonhallinta \> Kuormat \> Kuormasuunnittelun työtila**.</span><span class="sxs-lookup"><span data-stu-id="615b6-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="615b6-394">Etsi ja valitse **Myyntirivit**-välilehdessä kaikki myyntitilausrivit yhdestä tätä skenaariota varten luoduista myyntitilauksista.</span><span class="sxs-lookup"><span data-stu-id="615b6-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="615b6-395">Valitse toimintoruudun **Tarjonta ja kysyntä** -välilehden **Lisää**-ryhmässä kohta **Uuteen kuormaan**.</span><span class="sxs-lookup"><span data-stu-id="615b6-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="615b6-396">Valitut tilausrivit lisätään uuteen kuormaan.</span><span class="sxs-lookup"><span data-stu-id="615b6-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="615b6-397">Valitse **Kuormamallin määritys** -valintaikkunan **Kuorman mallitunnus** -kentässä kuormamalli, kuten *40' kontti*.</span><span class="sxs-lookup"><span data-stu-id="615b6-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="615b6-398">Sulje valintaikkuna valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="615b6-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="615b6-399">Etsi ja valitse juuri luotu kuorma **Kuormat**-osassa.</span><span class="sxs-lookup"><span data-stu-id="615b6-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="615b6-400">Valitse **Vapauta \> Vapauta varastoon**.</span><span class="sxs-lookup"><span data-stu-id="615b6-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="615b6-401">Vapauta valittu kuorma varastoon valitsemalla **Vapauta varastoon** -valintaikkunassa **OK**.</span><span class="sxs-lookup"><span data-stu-id="615b6-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="615b6-402">Lähetysten ja konttien tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="615b6-402">Verify the shipments and containers</span></span>

<span data-ttu-id="615b6-403">Seuraavalla toiminnolla voit vahvistaa luodut lähetykset.</span><span class="sxs-lookup"><span data-stu-id="615b6-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="615b6-404">Tarkista sen avulla tätä skenaariota varten luomasi tilaus ja varmista, että olet saanut odotetut tulokset.</span><span class="sxs-lookup"><span data-stu-id="615b6-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="615b6-405">Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.</span><span class="sxs-lookup"><span data-stu-id="615b6-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="615b6-406">Etsi ja valitse juuri vapautetulle kuormalle luotu lähetys.</span><span class="sxs-lookup"><span data-stu-id="615b6-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="615b6-407">Valitse toimintoruudun **Kuljetus**-välilehdessä **Näytä kontit**.</span><span class="sxs-lookup"><span data-stu-id="615b6-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="615b6-408">Vahvista, että myyntitilausten nimikkeet on pakattu kahteen eri konttiin.</span><span class="sxs-lookup"><span data-stu-id="615b6-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="615b6-409">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="615b6-409">Additional resources</span></span>

- [<span data-ttu-id="615b6-410">Konttiinpakkaus</span><span class="sxs-lookup"><span data-stu-id="615b6-410">Containerization</span></span>](wave-containerization.md)
