---
title: Tuotteiden cross-docking vastaanottaessa varastosta myymälöihin
description: Tässä menettelyssä esitellään, miten cross docking luodaan ja miten sitä käsitellään jaettaessa tuotteita ostotilauksen vastaanottosijainnista yhteen tai useaan myymälään.
author: ShylaThompson
manager: tfehr
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9bf53ba136c446df61893f4703e5951e42ae605d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217077"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="dc07d-103">Tuotteiden cross-docking vastaanottaessa varastosta myymälöihin</span><span class="sxs-lookup"><span data-stu-id="dc07d-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc07d-104">Tässä menettelyssä esitellään, miten cross docking luodaan ja miten sitä käsitellään jaettaessa tuotteita ostotilauksen vastaanottosijainnista yhteen tai useaan myymälään.</span><span class="sxs-lookup"><span data-stu-id="dc07d-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="dc07d-105">Käyttäjä voi määrittää useita konfiguraatioita. Järjestelmä voi ehdottaa, miten tuotteet jaellaan, tai käyttäjä voi syöttää manuaalisesti, minne tuotteet jaellaan ja miten paljon kuhunkin myymälään tuotteita siirtyy.</span><span class="sxs-lookup"><span data-stu-id="dc07d-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="dc07d-106">Menettely ei sisällä tietojen asetuksia, joita cross dockingissa voi käyttää, kuten täydennyssääntöjä, organisaatiohierarkioita ja myymälän painoja.</span><span class="sxs-lookup"><span data-stu-id="dc07d-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="dc07d-107">Menettelyssä käytetään esittely-yritystä USRT.</span><span class="sxs-lookup"><span data-stu-id="dc07d-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="dc07d-108">Siirry Kaikki ostotilaukset -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="dc07d-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="dc07d-109">Valitse luettelosta ostotilaus ja avaa sitten tilaus valitsemalla linkki.</span><span class="sxs-lookup"><span data-stu-id="dc07d-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="dc07d-110">Valitse toimintoruudussa Retail ja Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc07d-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="dc07d-111">Valitse Cross docking.</span><span class="sxs-lookup"><span data-stu-id="dc07d-111">Click Cross docking.</span></span>
5. <span data-ttu-id="dc07d-112">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="dc07d-112">Click Edit.</span></span>
    * <span data-ttu-id="dc07d-113">Luokkaa voidaan käyttää Rivit-osan nimikkeiden suodattamisessa.</span><span class="sxs-lookup"><span data-stu-id="dc07d-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="dc07d-114">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dc07d-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="dc07d-115">Syötä Cross docking -määrä -kenttään arvo, joka määrittää, miten suuri osa valitun tuotteen ostetusta määrästä jaellaan.</span><span class="sxs-lookup"><span data-stu-id="dc07d-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="dc07d-116">Syötä Cross docking -lisämäärä -kenttään arvo, joka määrittää käytettävissä olevien ostettavien tuotteiden jaettavan määrän</span><span class="sxs-lookup"><span data-stu-id="dc07d-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="dc07d-117">Syötä Jakelu-kenttään Sijaintipaino.</span><span class="sxs-lookup"><span data-stu-id="dc07d-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="dc07d-118">Voit valita muita tyyppejä jakelun eri säännöille.</span><span class="sxs-lookup"><span data-stu-id="dc07d-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="dc07d-119">Syötä tai valitse arvo Täydennyshierarkia-kentässä.</span><span class="sxs-lookup"><span data-stu-id="dc07d-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="dc07d-120">Valitse Ota valikoimat huomioon -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dc07d-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="dc07d-121">Valitse Laske määrät.</span><span class="sxs-lookup"><span data-stu-id="dc07d-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="dc07d-122">Valitse Luo tilaus.</span><span class="sxs-lookup"><span data-stu-id="dc07d-122">Click Create order.</span></span>
14. <span data-ttu-id="dc07d-123">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="dc07d-123">Click Yes.</span></span>
15. <span data-ttu-id="dc07d-124">Etsi ja valitse luettelosta tuotteet vastaanottava varasto</span><span class="sxs-lookup"><span data-stu-id="dc07d-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="dc07d-125">Valitse Tilaus, kun haluat tarkastella valitussa varastossa luotuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="dc07d-125">Click Order to view the orders that got created for the selected warehouse</span></span>

