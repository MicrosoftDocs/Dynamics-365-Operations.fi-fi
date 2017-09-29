---
title: "Järjestelmän ryhmittely avoimessa työluettelossa"
description: "Tässä aiheessa kuvataan avoimen työluettelon suodattamista mobiililaitteella."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="2a020-103">Järjestelmän ryhmittely avoimessa työluettelossa</span><span class="sxs-lookup"><span data-stu-id="2a020-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2a020-104">Järjestelmän ryhmittelykentän avulla voit suodattaa avoimen työluettelon muokkaamatta mobiililaitteen valikkovaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="2a020-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="2a020-105">Järjestelmän ryhmittelyä voidaan käyttää työluettelon suodattamisessa yhden työn otsikkokentässä.</span><span class="sxs-lookup"><span data-stu-id="2a020-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="2a020-106">Et voi käyttää järjestelmän ryhmittelyä online-tason kentissä.</span><span class="sxs-lookup"><span data-stu-id="2a020-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="2a020-107">Järjestelmän ryhmittelyn määrittely avoimessa työluettelossa</span><span class="sxs-lookup"><span data-stu-id="2a020-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="2a020-108">Suorita seuraavat vaiheet järjestelmän ryhmittelyn määrittelemiseksi avoimessa työluettelossa.</span><span class="sxs-lookup"><span data-stu-id="2a020-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="2a020-109">Valitse mobiililaitteen valikkovaihtoehdoista **Tila: epäsuora** ja **Tehtävän koodi: Näytä avoin työluettelo**.</span><span class="sxs-lookup"><span data-stu-id="2a020-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="2a020-110">Valittaviksi tulevat seuraavat vaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="2a020-110">The following options become available.</span></span> <span data-ttu-id="2a020-111">Nämä asetukset ovat pakollisia järjestelmän ryhmittelemiseksi avoimessa työluettelossa.</span><span class="sxs-lookup"><span data-stu-id="2a020-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="2a020-112">Vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="2a020-112">Option</span></span>        | <span data-ttu-id="2a020-113">kuvaus</span><span class="sxs-lookup"><span data-stu-id="2a020-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="2a020-114">Salli järjestelmän ryhmittely</span><span class="sxs-lookup"><span data-stu-id="2a020-114">Allow system grouping</span></span>   | <span data-ttu-id="2a020-115">Mahdollistaa järjestelmän ryhmittelyn valitun työluettelon valikon kohteelle.</span><span class="sxs-lookup"><span data-stu-id="2a020-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="2a020-116">Järjestelmän ryhmittelykenttä</span><span class="sxs-lookup"><span data-stu-id="2a020-116">System grouping field</span></span>   | <span data-ttu-id="2a020-117">Käytettävissä vain, jos **Järjestelmän työn salliminen** on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2a020-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="2a020-118">Valitse kenttä, joka määrittää, miten poimintatyö ryhmitellään työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="2a020-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="2a020-119">Esimerkiksi jos valitset **ShipmentId**-kentän, työntekijä skannaa lähetystunnuksen keräilytyön ryhmittelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="2a020-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="2a020-120">Tämän jälkeen kaikki lähetyksen työt on määritetty työntekijälle.</span><span class="sxs-lookup"><span data-stu-id="2a020-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="2a020-121">Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä.</span><span class="sxs-lookup"><span data-stu-id="2a020-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="2a020-122">Ilmoita työntekijälle skannattavat kohteet **Järjestelmän ryhmittelyotsikko** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2a020-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="2a020-123">Järjestelmän ryhmittelyotsikko</span><span class="sxs-lookup"><span data-stu-id="2a020-123">System grouping label</span></span>   | <span data-ttu-id="2a020-124">Käytettävissä vain, jos **Järjestelmän työn salliminen** on määritetty **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="2a020-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="2a020-125">Kirjoita tiedot työntekijälle siitä, mitä tulisi skannata, kun poimintatyö ryhmitellään.</span><span class="sxs-lookup"><span data-stu-id="2a020-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="2a020-126">Jos esimerkiksi käytät **ShipmentId**-kenttää keräilytöiden ryhmittelemiseen lähetyksen mukaan, voit kirjoittaa kenttään Lähetyksen tunnus.</span><span class="sxs-lookup"><span data-stu-id="2a020-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="2a020-127">Tämä kenttä edellyttää, että luot valikkovaihtoehdon, jolla voi käyttää aiemmin luotua järjestelmän ryhmittelemää työtä.</span><span class="sxs-lookup"><span data-stu-id="2a020-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="2a020-128">Sinun on myös valittava ryhmiteltävä kenttä **Järjestelmän ryhmittely** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="2a020-128">You must also select the field to group by in the **System grouping** field.</span></span>|

