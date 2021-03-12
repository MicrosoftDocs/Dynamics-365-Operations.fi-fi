---
title: Ostotilausten tuotepakkausten luominen
description: Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa.
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 296b3fb03b20dee5b6024c182df7feb3ce280913
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964667"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="4c404-103">Ostotilausten tuotepakkausten luominen</span><span class="sxs-lookup"><span data-stu-id="4c404-103">Create product packages for purchase orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c404-104">Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="4c404-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="4c404-105">Ostotilausta käytetään ennalta määritetyn tuotejoukon tilauksen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="4c404-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="4c404-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="4c404-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="4c404-107">Luo tuotepaketti</span><span class="sxs-lookup"><span data-stu-id="4c404-107">Create a product package</span></span>
1. <span data-ttu-id="4c404-108">Siirry kohtaan Retail ja Commerce > Varastonhallinta > Täydennys > Tuotepaketit.</span><span class="sxs-lookup"><span data-stu-id="4c404-108">Go to Retail and Commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="4c404-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4c404-109">Click New.</span></span>
3. <span data-ttu-id="4c404-110">Kirjoita arvo Paketin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c404-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="4c404-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c404-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4c404-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4c404-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4c404-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4c404-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="4c404-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4c404-114">Click Add.</span></span>
8. <span data-ttu-id="4c404-115">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="4c404-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="4c404-116">Avaa haku valitsemalla Koko-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4c404-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="4c404-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4c404-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="4c404-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c404-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="4c404-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4c404-119">Click Add.</span></span>
13. <span data-ttu-id="4c404-120">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="4c404-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="4c404-121">Avaa haku valitsemalla Variantin numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4c404-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4c404-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4c404-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4c404-123">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c404-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="4c404-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="4c404-124">Click Add.</span></span>
18. <span data-ttu-id="4c404-125">Kirjoita Nimiketunnus-kenttään 0175.</span><span class="sxs-lookup"><span data-stu-id="4c404-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="4c404-126">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="4c404-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="4c404-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4c404-127">Click Save.</span></span>
21. <span data-ttu-id="4c404-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4c404-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="4c404-129">Lisää paketti ostotilaukseen</span><span class="sxs-lookup"><span data-stu-id="4c404-129">Add package to purchase order</span></span>
1. <span data-ttu-id="4c404-130">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="4c404-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="4c404-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4c404-131">Click New.</span></span>
3. <span data-ttu-id="4c404-132">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4c404-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4c404-133">Valitse luettelosta toimittaja, jolle aiemmin luotiin tuotepaketti, jos toimittaja valittiin luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="4c404-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="4c404-134">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="4c404-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="4c404-135">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="4c404-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4c404-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4c404-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4c404-137">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="4c404-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4c404-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="4c404-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4c404-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4c404-139">Click OK.</span></span>
11. <span data-ttu-id="4c404-140">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="4c404-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="4c404-141">Valitse Tuotepaketit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4c404-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="4c404-142">Valitse Ostotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="4c404-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="4c404-143">Valitse Luo rivit paketista.</span><span class="sxs-lookup"><span data-stu-id="4c404-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="4c404-144">Etsi ja valitse luettelosta edellisessä vaiheessa luotu tuotepaketti.</span><span class="sxs-lookup"><span data-stu-id="4c404-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="4c404-145">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="4c404-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="4c404-146">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="4c404-146">Click Create.</span></span>
18. <span data-ttu-id="4c404-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="4c404-147">Click Save.</span></span>

