--- 
title: "Siirrä tuotteita jakelukeskuksista myymälöihin käyttäen ostotarjontaa"
description: "Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: ed47b4f052dab99dec058910e4b8558481b34e59
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="push-products-from-distribution-centers-to-stores-via-buyers-push"></a><span data-ttu-id="dc5be-103">Siirrä tuotteita jakelukeskuksista myymälöihin käyttäen ostotarjontaa</span><span class="sxs-lookup"><span data-stu-id="dc5be-103">Push products from distribution centers to stores via buyer's push</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="dc5be-104">Tässä menettelyssä esitellään, miten ostovaatimus luodaan ja miten sitä käsitellään jaettaessa tuotteita yhdestä sijainnista yhteen tai useaan myymälään.</span><span class="sxs-lookup"><span data-stu-id="dc5be-104">This procedure walks through the steps to create and process a Buyer's push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="dc5be-105">Käyttäjä voi määrittää useita konfiguraatioita. Järjestelmä voi ehdottaa, miten tuotteet jaellaan, tai käyttäjä voi syöttää manuaalisesti, minne tuotteet jaellaan ja miten paljon kuhunkin myymälään tuotteita siirtyy.</span><span class="sxs-lookup"><span data-stu-id="dc5be-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="dc5be-106">Menettely ei sisällä tietojen asetuksia, joita ostovaatimuksessa voi käyttää, kuten täydennyssääntöjä, organisaatiohierarkioita ja myymälän painoja.</span><span class="sxs-lookup"><span data-stu-id="dc5be-106">This procedure doesn't include setup of data that can be used in the Buyer's push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="dc5be-107">Näissä toimintaohjeissa käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="dc5be-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="dc5be-108">Siirry Ostovaatimus-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="dc5be-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="dc5be-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="dc5be-109">Click New.</span></span>
3. <span data-ttu-id="dc5be-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dc5be-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="dc5be-111">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dc5be-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="dc5be-112">Syötä tai valitse Varasto-kenttään varasto, joka sisältää tuotteita, joilla on käytettävissä olevia määriä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="dc5be-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="dc5be-113">Click Add.</span></span>
7. <span data-ttu-id="dc5be-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dc5be-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="dc5be-115">Syötä tai valitse tuote Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="dc5be-116">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="dc5be-116">Click Add.</span></span>
10. <span data-ttu-id="dc5be-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dc5be-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="dc5be-118">Syötä tai valitse tuotevariantti Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="dc5be-119">Kun tuotevariantti syötetään, jokaiselle variantille luodaan rivit.</span><span class="sxs-lookup"><span data-stu-id="dc5be-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="dc5be-120">Merkitse rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="dc5be-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="dc5be-121">Määritä Siirretty määrä -kenttään, miten monta valittua tuotetta haluat jaella.</span><span class="sxs-lookup"><span data-stu-id="dc5be-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="dc5be-122">Syötä Siirrettävä lisämäärä -kenttään niiden tuotteiden määrä, joilla on jaettavaa käytettävissä olevaa määrää.</span><span class="sxs-lookup"><span data-stu-id="dc5be-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="dc5be-123">Syötä Jakelu-kenttään Sijaintipaino.</span><span class="sxs-lookup"><span data-stu-id="dc5be-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="dc5be-124">Voit valita muita tyyppejä jakelun eri säännöille.</span><span class="sxs-lookup"><span data-stu-id="dc5be-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="dc5be-125">Syötä tai valitse arvo Täydennyshierarkia-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="dc5be-126">Valitse Ota valikoimat huomioon -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="dc5be-127">Valitse Laske määrät ja tarkista, että määrät on lisätty Varasto-osan riveille.</span><span class="sxs-lookup"><span data-stu-id="dc5be-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="dc5be-128">Valitse Luo tilaus.</span><span class="sxs-lookup"><span data-stu-id="dc5be-128">Click Create order.</span></span>
20. <span data-ttu-id="dc5be-129">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dc5be-129">Click Yes.</span></span>


