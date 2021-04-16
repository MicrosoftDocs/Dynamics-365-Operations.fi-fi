---
title: Ostoehdotukset
description: Tässä aiheessa käsitellään ostoehdotusten tukemista suunnittelun optimoinnissa.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808037"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="7116f-103">Ostoehdotukset</span><span class="sxs-lookup"><span data-stu-id="7116f-103">Purchase requisitions</span></span>

<span data-ttu-id="7116f-104">Pääsuunnittelu voi täydentää hyväksyttyjä ostoehdotuksia.</span><span class="sxs-lookup"><span data-stu-id="7116f-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="7116f-105">Niinpä käyttäjien ei tarvitse käyttää työnkulkua ostoehdotuksia koskevien ostotilausten luontiin.</span><span class="sxs-lookup"><span data-stu-id="7116f-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="7116f-106">Ostoehdotukset voidaan siis käsitellä pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="7116f-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="7116f-107">Tämän toiminnon ansiosta ostoehdotuksesta voidaan luoda ostotilaus, siirtotilaus tai tuotantotilaus sen mukaan, mikä **Suunniteltu tilaustyyppi** -arvo on määritetty liittyvälle tuotteelle.</span><span class="sxs-lookup"><span data-stu-id="7116f-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="7116f-108">Ehdotusten sisällyttämisen ottaminen käyttöön pääsuunnitelmissa</span><span class="sxs-lookup"><span data-stu-id="7116f-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="7116f-109">Ehdotukset sisällytetään pääsuunnittelun kattavuuslaskentaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="7116f-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="7116f-110">Valitse **Pääsuunnittelu** \> **Määritykset** \> **Suunnitelmat** \> **Pääsuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="7116f-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7116f-111">Luo tai valitse pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="7116f-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="7116f-112">Määritä **Yleinen**-pikavälilehdessä **Sisällytä ehdotukset** -asetukseksi *Kyllä*.</span><span class="sxs-lookup"><span data-stu-id="7116f-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="7116f-113">Toista vaiheet 2 ja 3 jokaiselle muulle pääsuunnitelmalle, johon ehdotukset halutaan sisällyttää.</span><span class="sxs-lookup"><span data-stu-id="7116f-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="7116f-114">Hyväksyttyjen ehdotusten aikaraja</span><span class="sxs-lookup"><span data-stu-id="7116f-114">Approved requisitions time fence</span></span>

<span data-ttu-id="7116f-115">*Hyväksytty ehdotusten aikaraja* määrittää, mistä lähtien (päivinä) pääsuunnittelu sisällyttää kysynnän hyväksytyistä täydennysehdotuksista.</span><span class="sxs-lookup"><span data-stu-id="7116f-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="7116f-116">Hyväksyttyjen ehdotusten aikarajan voi määrittää sekä kattavuusryhmätasolla että pääsuunnittelutasolla.</span><span class="sxs-lookup"><span data-stu-id="7116f-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="7116f-117">Kattavuusryhmän hyväksyttyjen ehdotusten aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7116f-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="7116f-118">Valitse **Pääsuunnittelu** \> **Määritys** \> **Kattavuus** \> **Kattavuusryhmät**.</span><span class="sxs-lookup"><span data-stu-id="7116f-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="7116f-119">Luo tai valitse kattavuusryhmä.</span><span class="sxs-lookup"><span data-stu-id="7116f-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="7116f-120">Määritä **Muu**-pikavälilehden **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään aikarajaan sisällytettävien päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="7116f-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7116f-121">Toista vaiheet 2 ja 3 jokaisessa kattavuusryhmässä, jossa halutaan määrittää hyväksyttyjen ehdotusten aikaraja.</span><span class="sxs-lookup"><span data-stu-id="7116f-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="7116f-122">Yksittäisten pääsuunnitelmien hyväksyttyjen ehdotusten aikarajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7116f-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="7116f-123">Kun hyväksyttyjen ehdotusten aikaraja määritetään yksittäiselle pääsuunnitelmalle, asetus ohittaa minkä tahansa käytettävän kattavuusryhmän aikaraja-asetuksen.</span><span class="sxs-lookup"><span data-stu-id="7116f-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="7116f-124">Valitse **Pääsuunnittelu** \> **Määritykset** \> **Suunnitelmat** \> **Pääsuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="7116f-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="7116f-125">Luo tai valitse pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="7116f-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="7116f-126">Määritä **Aikarajat päivinä** -pikavälilehden **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään aikarajaan sisällytettävien päivien määrä.</span><span class="sxs-lookup"><span data-stu-id="7116f-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="7116f-127">Toista vaiheet 2 ja 3 jokaisessa pääsuunnitelmassa, jossa halutaan määrittää hyväksyttyjen ehdotusten aikaraja.</span><span class="sxs-lookup"><span data-stu-id="7116f-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7116f-128">**Tulossa pian:** Hyväksyttyjen ehdotusten aikarajoja ei tueta vielä suunnittelun optimoinnissa.</span><span class="sxs-lookup"><span data-stu-id="7116f-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="7116f-129">Niin kauan kun niitä ei tueta, kaikki **Hyväksyttyjen ehdotusten aikaraja (päivää)** -kenttään annetut arvot ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="7116f-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="7116f-130">Kattavuuskoodista riippumaton erillinen toimitus</span><span class="sxs-lookup"><span data-stu-id="7116f-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="7116f-131">Erilliset suunnitellut tilaukset kattavat aina ostoehdotukset kattavuuskoodista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="7116f-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="7116f-132">Tämä toiminta varmistaa selkeän jäljitettävyyden sekä ostoehdotusten ja täydennystilausten väliset työnkulut.</span><span class="sxs-lookup"><span data-stu-id="7116f-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="7116f-133">Esimerkki 1</span><span class="sxs-lookup"><span data-stu-id="7116f-133">Example 1</span></span>

<span data-ttu-id="7116f-134">Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="7116f-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7116f-135">Käytettävissä olevan varaston määrä = 10.</span><span class="sxs-lookup"><span data-stu-id="7116f-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="7116f-136">Varaston vähimmäismäärä = 15.</span><span class="sxs-lookup"><span data-stu-id="7116f-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7116f-137">Varaston enimmäismäärä = 20.</span><span class="sxs-lookup"><span data-stu-id="7116f-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7116f-138">Aiemmin luotu yhden kappaleen ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="7116f-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7116f-139">Sen pyydetty päivämäärä on kuluva päivä.</span><span class="sxs-lookup"><span data-stu-id="7116f-139">It has a requested date of today.</span></span>

<span data-ttu-id="7116f-140">Pääsuunnittelua suoritettaessa luodaan kaksi suunniteltua tilausta: yksi 10 kpl:n tilaus täydentämään varasto maksimimäärään ja toinen 1 kpl:n tilaus täydentämään ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="7116f-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="7116f-141">Esimerkki 2</span><span class="sxs-lookup"><span data-stu-id="7116f-141">Example 2</span></span>

<span data-ttu-id="7116f-142">Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="7116f-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="7116f-143">Käytettävissä olevan varaston määrä = 17.</span><span class="sxs-lookup"><span data-stu-id="7116f-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="7116f-144">Varaston vähimmäismäärä = 15.</span><span class="sxs-lookup"><span data-stu-id="7116f-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="7116f-145">Varaston enimmäismäärä = 20.</span><span class="sxs-lookup"><span data-stu-id="7116f-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="7116f-146">Aiemmin luotu yhden kappaleen ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="7116f-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="7116f-147">Sen pyydetty päivämäärä on kuluva päivä.</span><span class="sxs-lookup"><span data-stu-id="7116f-147">It has a requested date of today.</span></span>

<span data-ttu-id="7116f-148">Pääsuunnittelua suoritettaessa luodaan yksi yhden kappaleen tilaus täydentämään ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="7116f-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="7116f-149">Esimerkki 3</span><span class="sxs-lookup"><span data-stu-id="7116f-149">Example 3</span></span>

<span data-ttu-id="7116f-150">Tuote määritetään siten, että sen **Kattavuuskoodi**-arvo on *Kausi* ja kauden pituus on seitsemän päivää.</span><span class="sxs-lookup"><span data-stu-id="7116f-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="7116f-151">Siinä on seuraavat varaston, myyntitilauksen ja ehdotuksen tilat:</span><span class="sxs-lookup"><span data-stu-id="7116f-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="7116f-152">Käytettävissä olevan varaston määrä = 0.</span><span class="sxs-lookup"><span data-stu-id="7116f-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="7116f-153">Aiemmin luotu viiden kappaleen myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="7116f-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="7116f-154">Sen odotettu lähetyspäivä on kuluva päivä + yksi päivä.</span><span class="sxs-lookup"><span data-stu-id="7116f-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="7116f-155">Aiemmin luotu kolmen kappaleen ostoehdotus.</span><span class="sxs-lookup"><span data-stu-id="7116f-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="7116f-156">Sen pyydetty päivämäärä on kuluva päivä + kolme päivää.</span><span class="sxs-lookup"><span data-stu-id="7116f-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="7116f-157">Pääsuunnittelua suoritettaessa luodaan kaksi suunniteltua tilausta: yksi kolmen kappaleen tilaus täydentämään ostoehdotus ja yksi viiden kappaleen tilaus täydentämään myyntitilauksen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="7116f-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="7116f-158">Kun ostoehdotukseen tarvekohdistettu suunniteltu tilaus on vahvistettu, suunnittelumoduuli säilyttää tarvekohdistuksen ostoehdotukseen.</span><span class="sxs-lookup"><span data-stu-id="7116f-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="7116f-159">Jos myöhemmin huomataan, että vahvistetusta tilauksesta puuttuu jokin määrä, joka tarvitaan ostoehdotuksen täyttämiseen, järjestelmä luo eron kattavan uuden suunnitellun tilauksen.</span><span class="sxs-lookup"><span data-stu-id="7116f-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="7116f-160">Lisätietoja ostoehdotuksista on kohdassa [Ostoehdotusten yleiskatsaus](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7116f-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]