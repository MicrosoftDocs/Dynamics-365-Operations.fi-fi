--- 
title: "Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa"
description: "Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään."
author: rubencdelgado
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailBuyersPush, InventLocationIdLookup, InventItemIdLookupSimple, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3337241f8b0e3b30a3382a402257844e7438477a
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="330b7-103">Siirrä tuotteita jakelukeskuksesta myymälään käyttäen ostotarjontaa</span><span class="sxs-lookup"><span data-stu-id="330b7-103">Push products from distribution center to store using buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="330b7-104">Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään.</span><span class="sxs-lookup"><span data-stu-id="330b7-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="330b7-105">Käyttäjä voi määrittää useita konfiguraatioita. Järjestelmä voi ehdottaa, miten tuotteet jaellaan, tai käyttäjä voi syöttää manuaalisesti, minne tuotteet jaellaan ja miten paljon kuhunkin myymälään tuotteita siirtyy.</span><span class="sxs-lookup"><span data-stu-id="330b7-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="330b7-106">Menettely ei sisällä tietojen asetuksia, joita ostovaatimuksessa voi käyttää, kuten täydennyssääntöjä, organisaatiohierarkioita ja myymälän painoja.</span><span class="sxs-lookup"><span data-stu-id="330b7-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="330b7-107">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="330b7-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="330b7-108">Siirry Ostovaatimus-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="330b7-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="330b7-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="330b7-109">Click New.</span></span>
3. <span data-ttu-id="330b7-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="330b7-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="330b7-111">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="330b7-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="330b7-112">Syötä tai valitse Varasto-kenttään varasto, joka sisältää tuotteita, joilla on käytettävissä olevia määriä.</span><span class="sxs-lookup"><span data-stu-id="330b7-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="330b7-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="330b7-113">Click Add.</span></span>
7. <span data-ttu-id="330b7-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="330b7-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="330b7-115">Syötä tai valitse tuote Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="330b7-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="330b7-116">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="330b7-116">Click Add.</span></span>
10. <span data-ttu-id="330b7-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="330b7-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="330b7-118">Syötä tai valitse tuotevariantti Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="330b7-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="330b7-119">Kun tuotevariantti syötetään, jokaiselle variantille luodaan rivit.</span><span class="sxs-lookup"><span data-stu-id="330b7-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="330b7-120">Merkitse rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="330b7-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="330b7-121">Määritä Siirretty määrä -kenttään, miten monta valittua tuotetta haluat jaella.</span><span class="sxs-lookup"><span data-stu-id="330b7-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="330b7-122">Syötä Siirrettävä lisämäärä -kenttään niiden tuotteiden määrä, joilla on jaettavaa käytettävissä olevaa määrää.</span><span class="sxs-lookup"><span data-stu-id="330b7-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="330b7-123">Syötä Jakelu-kenttään Sijaintipaino.</span><span class="sxs-lookup"><span data-stu-id="330b7-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="330b7-124">Voit valita muita tyyppejä jakelun eri säännöille.</span><span class="sxs-lookup"><span data-stu-id="330b7-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="330b7-125">Syötä tai valitse arvo Täydennyshierarkia-kentässä.</span><span class="sxs-lookup"><span data-stu-id="330b7-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="330b7-126">Valitse Ota valikoimat huomioon -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="330b7-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="330b7-127">Valitse Laske määrät ja tarkista, että määrät on lisätty Varasto-osan riveille.</span><span class="sxs-lookup"><span data-stu-id="330b7-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="330b7-128">Valitse Luo tilaus.</span><span class="sxs-lookup"><span data-stu-id="330b7-128">Click Create order.</span></span>
20. <span data-ttu-id="330b7-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="330b7-129">Click Yes.</span></span>


