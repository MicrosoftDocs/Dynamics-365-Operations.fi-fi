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
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7a7386a9be15f4eeef7aaab73cb320b71994eea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "360437"
---
# <a name="create-product-packages-for-purchase-orders"></a><span data-ttu-id="5bcb9-103">Ostotilausten tuotepakkausten luominen</span><span class="sxs-lookup"><span data-stu-id="5bcb9-103">Create product packages for purchase orders</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5bcb9-104">Tässä menettelyssä kerrotaan, miten tuotepaketti luodaan ja miten sitä käytetään ostotilauksessa.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-104">This procedure walks through creating a product package and using it on a purchase order.</span></span> <span data-ttu-id="5bcb9-105">Ostotilausta käytetään ennalta määritetyn tuotejoukon tilauksen luomisessa.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-105">The purchase order will be used to create an order for a pre-defined set of products.</span></span> <span data-ttu-id="5bcb9-106">Menettely käyttää esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-product-package"></a><span data-ttu-id="5bcb9-107">Luo tuotepaketti</span><span class="sxs-lookup"><span data-stu-id="5bcb9-107">Create a product package</span></span>
1. <span data-ttu-id="5bcb9-108">Siirry kohtaan Vähittäismyynti ja kauppa > Varastonhallinta > Täydennys > Tuotepaketit.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-108">Go to Retail and commerce > Inventory management > Replenishment > Product packages.</span></span>
2. <span data-ttu-id="5bcb9-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-109">Click New.</span></span>
3. <span data-ttu-id="5bcb9-110">Kirjoita arvo Paketin numero -kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-110">In the Package number field, type a value.</span></span>
4. <span data-ttu-id="5bcb9-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5bcb9-112">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5bcb9-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5bcb9-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-114">Click Add.</span></span>
8. <span data-ttu-id="5bcb9-115">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-115">In the Item number field, type '0160'.</span></span>
9. <span data-ttu-id="5bcb9-116">Avaa haku valitsemalla Koko-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-116">In the Size field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5bcb9-117">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="5bcb9-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="5bcb9-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-119">Click Add.</span></span>
13. <span data-ttu-id="5bcb9-120">Kirjoita Nimiketunnus-kenttään 0160.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-120">In the Item number field, type '0160'.</span></span>
14. <span data-ttu-id="5bcb9-121">Avaa haku valitsemalla Variantin numero -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-121">In the Variant number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="5bcb9-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="5bcb9-123">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-123">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5bcb9-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-124">Click Add.</span></span>
18. <span data-ttu-id="5bcb9-125">Kirjoita Nimiketunnus-kenttään 0175.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-125">In the Item number field, type '0175'.</span></span>
19. <span data-ttu-id="5bcb9-126">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-126">In the Quantity field, enter a number.</span></span>
20. <span data-ttu-id="5bcb9-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-127">Click Save.</span></span>
21. <span data-ttu-id="5bcb9-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-128">Close the page.</span></span>

## <a name="add-package-to-purchase-order"></a><span data-ttu-id="5bcb9-129">Lisää paketti ostotilaukseen</span><span class="sxs-lookup"><span data-stu-id="5bcb9-129">Add package to purchase order</span></span>
1. <span data-ttu-id="5bcb9-130">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-130">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="5bcb9-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-131">Click New.</span></span>
3. <span data-ttu-id="5bcb9-132">Avaa haku valitsemalla Toimittajan tili -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-132">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5bcb9-133">Valitse luettelosta toimittaja, jolle aiemmin luotiin tuotepaketti, jos toimittaja valittiin luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-133">In the list, select the same vendor that the product package was previously created for, if a vendor was selected.</span></span>
5. <span data-ttu-id="5bcb9-134">Ota käyttöön Yleinen-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-134">Toggle the expansion of the General section.</span></span>
6. <span data-ttu-id="5bcb9-135">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-135">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5bcb9-136">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-136">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="5bcb9-137">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-137">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="5bcb9-138">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-138">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5bcb9-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-139">Click OK.</span></span>
11. <span data-ttu-id="5bcb9-140">Ota käyttöön Rivitiedot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-140">Toggle the expansion of the Line details section.</span></span>
12. <span data-ttu-id="5bcb9-141">Valitse Tuotepaketit-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-141">Click the Product packages tab.</span></span>
13. <span data-ttu-id="5bcb9-142">Valitse Ostotilausrivi.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-142">Click Purchase order line.</span></span>
14. <span data-ttu-id="5bcb9-143">Valitse Luo rivit paketista.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-143">Click Create lines from package.</span></span>
15. <span data-ttu-id="5bcb9-144">Etsi ja valitse luettelosta edellisessä vaiheessa luotu tuotepaketti.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-144">In the list, find and select the product package created in previous step.</span></span>
16. <span data-ttu-id="5bcb9-145">Syötä Määrä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-145">In the Quantity field, enter a number.</span></span>
17. <span data-ttu-id="5bcb9-146">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-146">Click Create.</span></span>
18. <span data-ttu-id="5bcb9-147">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5bcb9-147">Click Save.</span></span>

