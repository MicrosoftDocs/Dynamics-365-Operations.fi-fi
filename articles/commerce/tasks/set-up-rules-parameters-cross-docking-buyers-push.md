---
title: Määritä säännöt ja parametrit cross dockingille ja ostotarjonnalle
description: Tässä menettelyssä esitellään täydennyssääntöjen luontivaiheet.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141128"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="11a87-103">Määritä säännöt ja parametrit cross dockingille ja ostotarjonnalle</span><span class="sxs-lookup"><span data-stu-id="11a87-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11a87-104">Tässä menettelyssä esitellään täydennyssääntöjen luontivaiheet.</span><span class="sxs-lookup"><span data-stu-id="11a87-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="11a87-105">Täydennyssääntöjen avulla voidaan hallita tuotteiden jakelua myymälöihin, kun käytössä ovat cross docking ja ostotarjonta.</span><span class="sxs-lookup"><span data-stu-id="11a87-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="11a87-106">Täydennyssäännöt voidaan määrittää myymälöille tai myymäläryhmille.</span><span class="sxs-lookup"><span data-stu-id="11a87-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="11a87-107">Säännön kullekin riville määritetty paino määrittää, miten tuotteen määrät jaellaan myymälöihin, kun jakelumenetelmä on cross docking- tai ostotarjonta ja käytössä ovat täydennyssäännöt.</span><span class="sxs-lookup"><span data-stu-id="11a87-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="11a87-108">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="11a87-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="11a87-109">Siirry Täydennyssäännöt-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="11a87-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="11a87-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="11a87-110">Click New.</span></span>
3. <span data-ttu-id="11a87-111">Kirjoita arvo Täydennyssääntö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="11a87-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="11a87-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="11a87-113">Click Save.</span></span>
6. <span data-ttu-id="11a87-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="11a87-114">Click Add.</span></span>
7. <span data-ttu-id="11a87-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="11a87-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="11a87-116">Tyypiksi voi valita Täydennyshierarkia- tai Kanava-arvon.</span><span class="sxs-lookup"><span data-stu-id="11a87-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="11a87-117">Arvo määrittää, onko Nimi-kentän valinta kanavahierarkia tai tietty kanava.</span><span class="sxs-lookup"><span data-stu-id="11a87-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="11a87-118">Tässä esimerkissä käytetään täydennyshierarkiaa.</span><span class="sxs-lookup"><span data-stu-id="11a87-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="11a87-119">Valitse arvo Nimi-kentässä.</span><span class="sxs-lookup"><span data-stu-id="11a87-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="11a87-120">Painon oletusarvo on varastossa määritetty paino.</span><span class="sxs-lookup"><span data-stu-id="11a87-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="11a87-121">Täydennyssäännössä voidaan käyttää painoa. Voit myös syöttää uuden painon Paino-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="11a87-122">Syötä numero Paino-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="11a87-123">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="11a87-123">Click Add.</span></span>
11. <span data-ttu-id="11a87-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="11a87-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="11a87-125">Valitse Tyyppi-kentässä Kanava.</span><span class="sxs-lookup"><span data-stu-id="11a87-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="11a87-126">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="11a87-127">Syötä numero Paino-kenttään.</span><span class="sxs-lookup"><span data-stu-id="11a87-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="11a87-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="11a87-128">Click Save.</span></span>

