---
title: Luo kanban-sääntö käyttämällä kanban-rivitapahtumaa
description: Tämä menettely luo kanban-säännön vetämällä prosessitoiminnosta kanban-rivitapahtuman asetuksen avulla.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc838a64e74b561dd17fd2b568fa8c190a1dfcfe
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255202"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="85c5d-103">Luo kanban-sääntö käyttämällä kanban-rivitapahtumaa</span><span class="sxs-lookup"><span data-stu-id="85c5d-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="85c5d-104">Tämä menettely luo kanban-säännön vetämällä prosessitoiminnosta kanban-rivitapahtuman asetuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="85c5d-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="85c5d-105">Kanban-sääntö käynnistyy kanban-prosessitehtävästä, jonka kumpikin määrä on vähintään 25.</span><span class="sxs-lookup"><span data-stu-id="85c5d-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="85c5d-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="85c5d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="85c5d-107">Tämä tehtävä on tarkoitettu prosessiteknikolle tai arvovirtaa hallitsevalle työntekijälle uuden tai muokatun tuotteen tuotannon valmisteluun lean-ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="85c5d-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="85c5d-108">Luo kanban-sääntö</span><span class="sxs-lookup"><span data-stu-id="85c5d-108">Create a kanban rule</span></span>
1. <span data-ttu-id="85c5d-109">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="85c5d-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="85c5d-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="85c5d-110">Click New.</span></span>
3. <span data-ttu-id="85c5d-111">Valitse Täydennysstrategia-kentässä Tapahtuma.</span><span class="sxs-lookup"><span data-stu-id="85c5d-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="85c5d-112">Tämä luo kanbanit suoraan tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="85c5d-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="85c5d-113">Sitä käytetään asettamaan sääntöjä, joilla määritetään tilaukselle valmistamisen skenaario.</span><span class="sxs-lookup"><span data-stu-id="85c5d-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="85c5d-114">Anna tai valitse Ensimmäinen suunnitelman tehtävä -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="85c5d-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="85c5d-115">Anna tai valitse SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="85c5d-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="85c5d-116">Valmistuksen kanban-säännön ensimmäinen tehtävä on tuotantovirran prosessitehtävä.</span><span class="sxs-lookup"><span data-stu-id="85c5d-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="85c5d-117">Kun valitset tehtävän, tehtävän voimassaolopäivämäärät kopioidaan kanban-säännön voimassaolopäivämääriin.</span><span class="sxs-lookup"><span data-stu-id="85c5d-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="85c5d-118">Laajenna Tiedot-osa.</span><span class="sxs-lookup"><span data-stu-id="85c5d-118">Expand the Details section.</span></span>
6. <span data-ttu-id="85c5d-119">Kirjoita Tuote-kentän arvoksi L0001.</span><span class="sxs-lookup"><span data-stu-id="85c5d-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="85c5d-120">Laajenna Tapahtumat-osa.</span><span class="sxs-lookup"><span data-stu-id="85c5d-120">Expand the Events section.</span></span>
8. <span data-ttu-id="85c5d-121">Valitse Kanban-rivin tapahtuma -kentässä Automaattinen.</span><span class="sxs-lookup"><span data-stu-id="85c5d-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="85c5d-122">Järjestelmä luo tapahtuma-kanbanit tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="85c5d-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="85c5d-123">Tällä kentällä voit määrittää kanban-säännöt, jotka tarvitaan tuotantovirran alempana olevien prosessitehtävien materiaalin täydentämiseen.</span><span class="sxs-lookup"><span data-stu-id="85c5d-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="85c5d-124">Kun valinta on Automaattinen, tapahtuma-kanbanit luodaan tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="85c5d-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="85c5d-125">Tätä asetusta suositellaan, jos tuotanto on tarkoitus suorittaa samana päivänä.</span><span class="sxs-lookup"><span data-stu-id="85c5d-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="85c5d-126">Määritä tapahtuman vähimmäismääräksi 25.</span><span class="sxs-lookup"><span data-stu-id="85c5d-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="85c5d-127">Tapahtuma-kanbaneja muodostetaan, kun kysynnän määrä on yhtä suuri tai suurempi kuin tämä kenttä.</span><span class="sxs-lookup"><span data-stu-id="85c5d-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="85c5d-128">Tästä on hyötyä, jos tuotettavan tilausmäärän on oltava pienempi kuin tämä kenttä yhdellä koneella ja enemmän kuin tämä kenttä toisella koneella.</span><span class="sxs-lookup"><span data-stu-id="85c5d-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="85c5d-129">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85c5d-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="85c5d-130">Luo myyntitilaus ja käynnistä kanban-ketju</span><span class="sxs-lookup"><span data-stu-id="85c5d-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="85c5d-131">Siirry kohtaan Myynti ja markkinointi > Myyntitilaukset > Kaikki myyntitilaukset.</span><span class="sxs-lookup"><span data-stu-id="85c5d-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="85c5d-132">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="85c5d-132">Click New.</span></span>
3. <span data-ttu-id="85c5d-133">Syötä tai valitse arvo Asiakastili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="85c5d-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="85c5d-134">Valitse asiakastili US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="85c5d-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="85c5d-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85c5d-135">Click OK.</span></span>
5. <span data-ttu-id="85c5d-136">Kirjoita Nimiketunnus-kenttään L0001.</span><span class="sxs-lookup"><span data-stu-id="85c5d-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="85c5d-137">L0001 on nimike, jolle kanban-sääntö on luotu.</span><span class="sxs-lookup"><span data-stu-id="85c5d-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="85c5d-138">Valitse määräksi 27.</span><span class="sxs-lookup"><span data-stu-id="85c5d-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="85c5d-139">Koska 27 on suurempi kuin kanban-säännön vähimmäismäärä, 25, tapahtuma-kanban käynnistyy.</span><span class="sxs-lookup"><span data-stu-id="85c5d-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="85c5d-140">Kirjoita Toimipaikka-kenttään 1.</span><span class="sxs-lookup"><span data-stu-id="85c5d-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="85c5d-141">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="85c5d-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="85c5d-142">Valitse varasto 13.</span><span class="sxs-lookup"><span data-stu-id="85c5d-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="85c5d-143">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="85c5d-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="85c5d-144">Näytä kanban-säännöllä luotu kanban</span><span class="sxs-lookup"><span data-stu-id="85c5d-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="85c5d-145">Siirry kohtaan Tuotetietojen hallinta > Lean-valmistus > Kanban-säännöt.</span><span class="sxs-lookup"><span data-stu-id="85c5d-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="85c5d-146">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="85c5d-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="85c5d-147">Laajenna Kanbanit-osa.</span><span class="sxs-lookup"><span data-stu-id="85c5d-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="85c5d-148">Huomaa, että kanban 27:lle luotiin käsittelemään toiminto, joka perustuu luotuun kanban-sääntöön.</span><span class="sxs-lookup"><span data-stu-id="85c5d-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="85c5d-149">Tämä on viimeinen vaihe.</span><span class="sxs-lookup"><span data-stu-id="85c5d-149">This is the last step.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]