---
title: Luo kanban-sääntö käyttäen vähimmäisvarastotapahtumaa
description: Tämä menettely keskittyy asetuksiin, jotka tarvitaan kanban-säännön luomiseen vähimmäisvarastotapahtuman perusteella sen varmistamiseksi, että tiettyä tuotetta on aina saatavilla tietyssä paikassa.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 297ee73daf10dffd027dadec11725ae6f0408d4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255154"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="02195-103">Luo kanban-sääntö käyttäen vähimmäisvarastotapahtumaa</span><span class="sxs-lookup"><span data-stu-id="02195-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02195-104">Tämä menettely keskittyy asetuksiin, jotka tarvitaan kanban-säännön luomiseen vähimmäisvarastotapahtuman perusteella sen varmistamiseksi, että tiettyä tuotetta on aina saatavilla tietyssä paikassa.</span><span class="sxs-lookup"><span data-stu-id="02195-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="02195-105">Kanban-sääntö luodaan materiaalin siirtämiselle sijaintiin, kun varaston taso laskee alle 200 kappaleen.</span><span class="sxs-lookup"><span data-stu-id="02195-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="02195-106">Tarvittavat kanbanit luodaan ajamalla tarvekohdistustapahtuman käsittely.</span><span class="sxs-lookup"><span data-stu-id="02195-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="02195-107">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="02195-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="02195-108">Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="02195-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="02195-109">Luo uusi kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="02195-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="02195-110">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="02195-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="02195-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="02195-111">Click New.</span></span>
3. <span data-ttu-id="02195-112">Valitse Tyyppi-kentän arvoksi "Otto".</span><span class="sxs-lookup"><span data-stu-id="02195-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="02195-113">Tätä tyyppiä käytetään siirtokanbanien luomiseen.</span><span class="sxs-lookup"><span data-stu-id="02195-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="02195-114">Valitse Täydennysstrategia-kentässä Tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="02195-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="02195-115">Tapahtumastategiaa käytetään, jotta kanbanien siirto voidaan tehdä tapahtuman perusteella.</span><span class="sxs-lookup"><span data-stu-id="02195-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="02195-116">Jäljempänä menettelyssä siirtokanbanit käynnistetään varaston täydennyksen kautta.</span><span class="sxs-lookup"><span data-stu-id="02195-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="02195-117">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="02195-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="02195-118">Anna tai valitse ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="02195-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="02195-119">Siirtotehtävällä on vastaanottava (tulos-)varasto ja toimipaikka 12, minkä vuoksi materiaalit siirretään varaston 12 toimipaikkaan 12.</span><span class="sxs-lookup"><span data-stu-id="02195-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="02195-120">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="02195-120">Expand the Details section.</span></span>
7. <span data-ttu-id="02195-121">Anna tai valitse Tuote-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="02195-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="02195-122">Valitse M0007.</span><span class="sxs-lookup"><span data-stu-id="02195-122">Select M0007.</span></span>  
8. <span data-ttu-id="02195-123">Laajenna Tapahtumat-osa.</span><span class="sxs-lookup"><span data-stu-id="02195-123">Expand the Events section.</span></span>
9. <span data-ttu-id="02195-124">Valitse Varaston täydennystapahtuma -kentässä Erä.</span><span class="sxs-lookup"><span data-stu-id="02195-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="02195-125">Tämä luo kanbanit materiaalitarpeen täyttämisellä liittyvässä sijainnissa tarvekohdistustapahtuman käsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="02195-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="02195-126">Aseta nimikkeen vähimmäismäärä</span><span class="sxs-lookup"><span data-stu-id="02195-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="02195-127">Napsauta Tuote-kentän linkkiä.</span><span class="sxs-lookup"><span data-stu-id="02195-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="02195-128">Käytä Nimiketunnus-kentän linkkiä napsauttamalla.</span><span class="sxs-lookup"><span data-stu-id="02195-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="02195-129">Laajenna tuotekuvan tietoruutu.</span><span class="sxs-lookup"><span data-stu-id="02195-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="02195-130">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="02195-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="02195-131">Valitse Nimikekattavuus.</span><span class="sxs-lookup"><span data-stu-id="02195-131">Click Item coverage.</span></span>
6. <span data-ttu-id="02195-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="02195-132">Click New.</span></span>
7. <span data-ttu-id="02195-133">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="02195-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="02195-134">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="02195-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="02195-135">Määritä Varasto-arvoksi 12.</span><span class="sxs-lookup"><span data-stu-id="02195-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="02195-136">Määritä vähimmäisarvoksi "200".</span><span class="sxs-lookup"><span data-stu-id="02195-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="02195-137">Suorita tapahtumien luonnin erätyö</span><span class="sxs-lookup"><span data-stu-id="02195-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="02195-138">Valitse Laadunvalvonta > Kausittaiset tehtävät > Kanban-työn eräkäsittely > Tarvekohdistustapahtuman käsittely.</span><span class="sxs-lookup"><span data-stu-id="02195-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="02195-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="02195-139">Click OK.</span></span>
3. <span data-ttu-id="02195-140">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="02195-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="02195-141">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="02195-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="02195-142">Valitse aiemmin luomasi kanban-sääntö.</span><span class="sxs-lookup"><span data-stu-id="02195-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="02195-143">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="02195-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="02195-144">Huomaa, että kanban luotiin siirtämään tarvittava materiaalin varastoon 12.</span><span class="sxs-lookup"><span data-stu-id="02195-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]