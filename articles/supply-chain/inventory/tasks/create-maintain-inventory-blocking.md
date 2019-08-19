---
title: Luo ja ylläpidä varastoesto
description: Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 845d517ad10245df3b208874df61e235c199c7fe
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836395"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="48ddb-103">Luo ja ylläpidä varastoesto</span><span class="sxs-lookup"><span data-stu-id="48ddb-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48ddb-104">Tässä menettelyssä kerrotaan, miten fyysisen käytettävissä olevan varaston varaaminen estetään muiden lähtevien asiakirjojen tai varastoeston avulla.</span><span class="sxs-lookup"><span data-stu-id="48ddb-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="48ddb-105">Voit suorittaa menettelyn esittelytietojen USMF-yrityksen avulla näkyvillä olevilla esimerkkiarvoilla.</span><span class="sxs-lookup"><span data-stu-id="48ddb-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="48ddb-106">Aloita tämä menettely vasta, kun käytettävissä on fyysistä käytettävissä olevaa varastoa omaava nimike.</span><span class="sxs-lookup"><span data-stu-id="48ddb-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="48ddb-107">Varastoeston luominen</span><span class="sxs-lookup"><span data-stu-id="48ddb-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="48ddb-108">Valitse Inventoinnin- ja varastonhallinta > Kausittaiset tehtävät > Varastoesto.</span><span class="sxs-lookup"><span data-stu-id="48ddb-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="48ddb-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="48ddb-109">Click New.</span></span>
3. <span data-ttu-id="48ddb-110">Avaa haku valitsemalla Nimiketunnus-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="48ddb-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="48ddb-111">Valitse luettelosta nimike.</span><span class="sxs-lookup"><span data-stu-id="48ddb-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="48ddb-112">Määritä estettävä nimiketunnus, jolla on fyysistä käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="48ddb-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="48ddb-113">Jos käytössä on USMF, voit valita nimikkeen M9201.</span><span class="sxs-lookup"><span data-stu-id="48ddb-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="48ddb-114">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="48ddb-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="48ddb-115">Jos käytössä on nimike M9201, määritä arvo, joka on pienempi kuin 200.</span><span class="sxs-lookup"><span data-stu-id="48ddb-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="48ddb-116">Ota käyttöön Varastodimensiot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="48ddb-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="48ddb-117">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="48ddb-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="48ddb-118">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="48ddb-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48ddb-119">Jos käytössä on nimike M9201, voit valita varaston 51.</span><span class="sxs-lookup"><span data-stu-id="48ddb-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="48ddb-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="48ddb-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="48ddb-121">Varastoeston ehtojen päivittäminen</span><span class="sxs-lookup"><span data-stu-id="48ddb-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="48ddb-122">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="48ddb-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="48ddb-123">Päivitä Varastomäärä-kenttä vastaamaan estettävää määrää.</span><span class="sxs-lookup"><span data-stu-id="48ddb-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="48ddb-124">Kirjoita päivämäärä Odotettu päivämäärä -kenttään.</span><span class="sxs-lookup"><span data-stu-id="48ddb-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="48ddb-125">Haluat ehkä määrittää, milloin estetyn varaston odotetaan olevan varattavissa. Voit määrittää tätä varten odotetun päivämäärän.</span><span class="sxs-lookup"><span data-stu-id="48ddb-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="48ddb-126">Jos varastoestolle on valittu Odotetut vastaanotot -asetus, kuten oletusarvoisesti on, voit luoda eston manuaalisesti. Tämä päivä näkyy odotetun tapahtuman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="48ddb-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="48ddb-127">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="48ddb-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="48ddb-128">Varastoeston poistaminen</span><span class="sxs-lookup"><span data-stu-id="48ddb-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="48ddb-129">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="48ddb-129">Click Delete.</span></span>
2. <span data-ttu-id="48ddb-130">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="48ddb-130">Click Yes.</span></span>
3. <span data-ttu-id="48ddb-131">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="48ddb-131">Close the page.</span></span>

