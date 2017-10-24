--- 
title: Ostotilausten tuotepakkausten luominen
description: "Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a3be1e7aca7f0382aea55fa8a371c33c8b53df95
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="8be9e-103">Ostotilausten tuotepakkausten luominen</span><span class="sxs-lookup"><span data-stu-id="8be9e-103">Create product packages for purchase orders</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8be9e-104">Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="8be9e-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="8be9e-105">Ostotilausta käytetään ennalta määritetyn tuotejoukon tilauksen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="8be9e-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="8be9e-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="8be9e-107">Luo tuotepaketti</span><span class="sxs-lookup"><span data-stu-id="8be9e-107">Create a product package</span></span>
1. <span data-ttu-id="8be9e-108">Siirry kohtaan Vähittäismyynti ja kauppa > Varastonhallinta > Täydennys > Tuotepaketit.</span><span class="sxs-lookup"><span data-stu-id="8be9e-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="8be9e-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8be9e-109">Click New.</span></span>
3. <span data-ttu-id="8be9e-110">Kirjoita arvo Paketin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="8be9e-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="8be9e-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8be9e-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8be9e-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8be9e-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="8be9e-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8be9e-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8be9e-114">Click Add.</span></span>
8. <span data-ttu-id="8be9e-115">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="8be9e-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="8be9e-116">Avaa haku valitsemalla Koko-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8be9e-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8be9e-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8be9e-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8be9e-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="8be9e-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8be9e-119">Click Add.</span></span>
13. <span data-ttu-id="8be9e-120">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="8be9e-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="8be9e-121">Avaa haku valitsemalla Variantin numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8be9e-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8be9e-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8be9e-123">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8be9e-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="8be9e-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="8be9e-124">Click Add.</span></span>
18. <span data-ttu-id="8be9e-125">Kirjoita Nimiketunnus-kenttään 0175.</span><span class="sxs-lookup"><span data-stu-id="8be9e-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="8be9e-126">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8be9e-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="8be9e-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8be9e-127">Click Save.</span></span>
21. <span data-ttu-id="8be9e-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8be9e-128">Close the page.</span></span>

## <a name="add-package-to-puchase-order"></a><span data-ttu-id="8be9e-129">Lisää paketti ostotilaukseen</span><span class="sxs-lookup"><span data-stu-id="8be9e-129">Add package to puchase order</span></span>
1. <span data-ttu-id="8be9e-130">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="8be9e-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="8be9e-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8be9e-131">Click New.</span></span>
3. <span data-ttu-id="8be9e-132">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8be9e-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8be9e-133">Valitse luettelosta toimittaja, jolle aiemmin luotiin tuotepaketti, jos toimittaja valittiin luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="8be9e-134">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8be9e-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="8be9e-135">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="8be9e-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8be9e-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="8be9e-137">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="8be9e-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="8be9e-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="8be9e-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8be9e-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8be9e-139">Click OK.</span></span>
11. <span data-ttu-id="8be9e-140">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="8be9e-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="8be9e-141">Valitse Tuotepaketit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8be9e-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="8be9e-142">Valitse Ostotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="8be9e-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="8be9e-143">Valitse Luo rivit paketista.</span><span class="sxs-lookup"><span data-stu-id="8be9e-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="8be9e-144">Etsi ja valitse luettelosta edellisessä vaiheessa luotu tuotepaketti.</span><span class="sxs-lookup"><span data-stu-id="8be9e-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="8be9e-145">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8be9e-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="8be9e-146">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="8be9e-146">Click Create.</span></span>
18. <span data-ttu-id="8be9e-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="8be9e-147">Click Save.</span></span>


