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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b5fb3c7fc5dbeb6263357113d2a9348afc5b1ac9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212744"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="ccc13-103">Luo ja ylläpidä varastoesto</span><span class="sxs-lookup"><span data-stu-id="ccc13-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccc13-104">Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.</span><span class="sxs-lookup"><span data-stu-id="ccc13-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="ccc13-105">Voit suorittaa menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla.</span><span class="sxs-lookup"><span data-stu-id="ccc13-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="ccc13-106">Aloita tämä menettely vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.</span><span class="sxs-lookup"><span data-stu-id="ccc13-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="ccc13-107">Varastoeston luominen</span><span class="sxs-lookup"><span data-stu-id="ccc13-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="ccc13-108">Valitse **siirtymisruudussa** **Moduulit > Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Varastoesto**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-108">In the **Navigation pane**, go to **Modules > Inventory management > Periodic tasks > Inventory blocking**.</span></span>
2. <span data-ttu-id="ccc13-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-109">Click **New**.</span></span>
3. <span data-ttu-id="ccc13-110">Avaa haku valitsemalla **Nimiketunnus**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ccc13-110">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ccc13-111">Valitse luettelosta nimike.</span><span class="sxs-lookup"><span data-stu-id="ccc13-111">In the list, select the item you want to choose.</span></span> <span data-ttu-id="ccc13-112">Määritä estettävä nimiketunnus, jolla on fyysistä käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="ccc13-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="ccc13-113">Jos käytössä on USMF, voit valita nimikkeen M9201.</span><span class="sxs-lookup"><span data-stu-id="ccc13-113">If you're using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="ccc13-114">Anna **Määrä**-kentässä numero.</span><span class="sxs-lookup"><span data-stu-id="ccc13-114">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="ccc13-115">Jos käytössä on nimike M9201, määritä arvo, joka on pienempi kuin 200.</span><span class="sxs-lookup"><span data-stu-id="ccc13-115">If you're using item M9201, you need to select less than 200.</span></span>
6. <span data-ttu-id="ccc13-116">Laajenna **Varaston dimensiot** -pikavälilehti.</span><span class="sxs-lookup"><span data-stu-id="ccc13-116">Expand the **Inventory dimensions** fastTab.</span></span>
7. <span data-ttu-id="ccc13-117">Avaa haku valitsemalla **Varasto**-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ccc13-117">In the **Warehouse** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ccc13-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ccc13-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="ccc13-119">Jos käytössä on nimike M9201, voit valita varaston 51.</span><span class="sxs-lookup"><span data-stu-id="ccc13-119">If you're using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="ccc13-120">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-120">Click **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="ccc13-121">Varastoeston ehtojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ccc13-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="ccc13-122">Kirjoita numero **Yleiset** -pikavälilehden **Määrä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ccc13-122">In the **General** fastTab, in the **Quantity** field, enter a number.</span></span> <span data-ttu-id="ccc13-123">Päivitä Varastomäärä-kenttä vastaamaan estettävää määrää.</span><span class="sxs-lookup"><span data-stu-id="ccc13-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="ccc13-124">Kirjoita päivämäärä **Odotettu päivämäärä** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ccc13-124">In the **Expected date** field, enter a date.</span></span> <span data-ttu-id="ccc13-125">Haluat ehkä määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Voit määrittää tätä varten odotetun päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="ccc13-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="ccc13-126">Jos varastoestolle on valittu Odotetut vastaanotot -asetus, kuten oletusarvoisesti on, voit luoda eston manuaalisesti. Tämä päivä näkyy odotetun tapahtuman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="ccc13-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="ccc13-127">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-127">Click **Save**.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="ccc13-128">Varastoeston poistaminen</span><span class="sxs-lookup"><span data-stu-id="ccc13-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="ccc13-129">Valitse **toimintoruudussa** **Poista**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-129">On the **Action Pane**, click **Delete**.</span></span>
2. <span data-ttu-id="ccc13-130">Valitse **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="ccc13-130">Click **Yes**.</span></span>
3. <span data-ttu-id="ccc13-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ccc13-131">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]