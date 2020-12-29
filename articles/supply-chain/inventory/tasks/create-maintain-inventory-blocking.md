---
title: Luo ja ylläpidä varastoesto
description: Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12c6e047e15aaab157e6de70f4a09f500af2965f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427339"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="dcf91-103">Luo ja ylläpidä varastoesto</span><span class="sxs-lookup"><span data-stu-id="dcf91-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dcf91-104">Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.</span><span class="sxs-lookup"><span data-stu-id="dcf91-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="dcf91-105">Voit suorittaa menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla.</span><span class="sxs-lookup"><span data-stu-id="dcf91-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="dcf91-106">Aloita tämä menettely vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.</span><span class="sxs-lookup"><span data-stu-id="dcf91-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="dcf91-107">Varastoeston luominen</span><span class="sxs-lookup"><span data-stu-id="dcf91-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="dcf91-108">Valitse **siirtymisruudussa** **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Varastoesto**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="dcf91-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-109">Click **New**.</span></span>
3. <span data-ttu-id="dcf91-110">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dcf91-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="dcf91-111">Valitse luettelosta nimike.</span><span class="sxs-lookup"><span data-stu-id="dcf91-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="dcf91-112">Määritä estettävä nimiketunnus, jolla on fyysistä käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="dcf91-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="dcf91-113">Jos käytössä on USMF, voit valita nimikkeen M9201.</span><span class="sxs-lookup"><span data-stu-id="dcf91-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="dcf91-114">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="dcf91-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="dcf91-115">Jos käytössä on nimike M9201, määritä arvo, joka on pienempi kuin 200.</span><span class="sxs-lookup"><span data-stu-id="dcf91-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="dcf91-116">Laajenna **Varaston dimensiot** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="dcf91-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="dcf91-117">Avaa haku valitsemalla **Varasto**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="dcf91-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="dcf91-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="dcf91-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="dcf91-119">Jos käytössä on nimike M9201, voit valita varaston 51.</span><span class="sxs-lookup"><span data-stu-id="dcf91-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="dcf91-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="dcf91-121">Varastoeston ehtojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="dcf91-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="dcf91-122">Kirjoita numero **Yleiset** -pikavälilehden **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcf91-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="dcf91-123">Päivitä Varastomäärä-kenttä vastaamaan estettävää määrää.</span><span class="sxs-lookup"><span data-stu-id="dcf91-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="dcf91-124">Kirjoita päivämäärä **Odotettu päivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="dcf91-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="dcf91-125">Haluat ehkä määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Voit määrittää tätä varten odotetun päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="dcf91-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="dcf91-126">Jos varastoestolle on valittu Odotetut vastaanotot -asetus, kuten oletusarvoisesti on, voit luoda eston manuaalisesti. Tämä päivä näkyy odotetun tapahtuman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="dcf91-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="dcf91-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="dcf91-128">Varastoeston poistaminen</span><span class="sxs-lookup"><span data-stu-id="dcf91-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="dcf91-129">Valitse **toimintoruudussa** **Poista**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="dcf91-130">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="dcf91-130">Click **Yes**.</span></span>
3. <span data-ttu-id="dcf91-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="dcf91-131">Close the page.</span></span>

