---
title: Oikeat varaston seurantatiedot
description: Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a8a488d4c30923445b3ebc2626a79b8fa45012c7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427341"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="38949-103">Oikeat varaston seurantatiedot</span><span class="sxs-lookup"><span data-stu-id="38949-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38949-104">Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen.</span><span class="sxs-lookup"><span data-stu-id="38949-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="38949-105">Tässä esimerkissä päivitetään eräohjatun nimikkeen tiedot muuttamalla virheellisesti rekisteröity erä toiseksi eräksi.</span><span class="sxs-lookup"><span data-stu-id="38949-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="38949-106">Tämä käyttää tässä menettelyssä USPI-yrityksen demotietoja tai omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="38949-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="38949-107">Jos käytät omia tietoja, tarvitset nimikkeen, jossa erätoiminnot on otettu käyttöön ja joka ei ole sijaintiohjattu.</span><span class="sxs-lookup"><span data-stu-id="38949-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="38949-108">Lisäksi varastosiirroille on oltava määritettynä varastokirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="38949-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="38949-109">Yleensä varastotyöntekijä tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="38949-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="38949-110">Luo varastosiirtokirjauskansio</span><span class="sxs-lookup"><span data-stu-id="38949-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="38949-111">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="38949-111">Go to Transfer.</span></span>
2. <span data-ttu-id="38949-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="38949-112">Click New.</span></span>
3. <span data-ttu-id="38949-113">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38949-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="38949-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38949-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="38949-115">Tämän kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="38949-115">Create journal lines</span></span>
1. <span data-ttu-id="38949-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="38949-116">Click New.</span></span>
2. <span data-ttu-id="38949-117">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="38949-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="38949-118">Jos käytössä on USPI, valitse nimike M5003.</span><span class="sxs-lookup"><span data-stu-id="38949-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="38949-119">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38949-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="38949-120">Valitse Varastodimensiot-välilehti.</span><span class="sxs-lookup"><span data-stu-id="38949-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="38949-121">Anna tai valitse Erätunnus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="38949-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="38949-122">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="38949-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="38949-123">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="38949-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="38949-124">Anna tai valitse Erätunnus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="38949-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="38949-125">Kirjaa kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="38949-125">Post the journal</span></span>
1. <span data-ttu-id="38949-126">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="38949-126">Click Post.</span></span>
2. <span data-ttu-id="38949-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38949-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="38949-128">Tarkista jäljitystiedot</span><span class="sxs-lookup"><span data-stu-id="38949-128">Check tracing information</span></span>
1. <span data-ttu-id="38949-129">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="38949-129">Click Inventory.</span></span>
2. <span data-ttu-id="38949-130">Valitse Jäljitys.</span><span class="sxs-lookup"><span data-stu-id="38949-130">Click Trace.</span></span>
3. <span data-ttu-id="38949-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="38949-131">Click OK.</span></span>
    * <span data-ttu-id="38949-132">Käyttämällä näitä jäljitystietoja, voit jäljittää taaksepäin, mistä erästä korjasit varaston.</span><span class="sxs-lookup"><span data-stu-id="38949-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="38949-133">Nämä tiedot ovat nähtävissä myös Nimikkeen seuranta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="38949-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="38949-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="38949-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="38949-135">Tarkista varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="38949-135">Check inventory transactions</span></span>
1. <span data-ttu-id="38949-136">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="38949-136">Click Inventory.</span></span>
2. <span data-ttu-id="38949-137">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="38949-137">Click Transactions.</span></span>
    * <span data-ttu-id="38949-138">Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.</span><span class="sxs-lookup"><span data-stu-id="38949-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

