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
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76e73f10df5bb520b6d0d787eda08053a5e33c81
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223407"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="8b3fe-103">Oikeat varaston seurantatiedot</span><span class="sxs-lookup"><span data-stu-id="8b3fe-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b3fe-104">Tässä menettelyssä käsitellään varastosiirtokirjauskansion luonti- ja kirjausprosessia, jolla mahdollisestaan varaston seurantatietojen korjaaminen.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="8b3fe-105">Tässä esimerkissä päivitetään eräohjatun nimikkeen tiedot muuttamalla virheellisesti rekisteröity erä toiseksi eräksi.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="8b3fe-106">Tämä käyttää tässä menettelyssä USPI-yrityksen demotietoja tai omia tietoja.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="8b3fe-107">Jos käytät omia tietoja, tarvitset nimikkeen, jossa erätoiminnot on otettu käyttöön ja joka ei ole sijaintiohjattu.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="8b3fe-108">Lisäksi varastosiirroille on oltava määritettynä varastokirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="8b3fe-109">Yleensä varastotyöntekijä tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="8b3fe-110">Luo varastosiirtokirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8b3fe-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="8b3fe-111">Valitse Siirrä.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-111">Go to Transfer.</span></span>
2. <span data-ttu-id="8b3fe-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-112">Click New.</span></span>
3. <span data-ttu-id="8b3fe-113">Syötä tai valitse arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="8b3fe-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="8b3fe-115">Tämän kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="8b3fe-115">Create journal lines</span></span>
1. <span data-ttu-id="8b3fe-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-116">Click New.</span></span>
2. <span data-ttu-id="8b3fe-117">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="8b3fe-118">Jos käytössä on USPI, valitse nimike M5003.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="8b3fe-119">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="8b3fe-120">Valitse Varastodimensiot-välilehti.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="8b3fe-121">Anna tai valitse Erätunnus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="8b3fe-122">Syötä tai valitse arvo Toimipaikka-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="8b3fe-123">Anna tai valitse Varasto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="8b3fe-124">Anna tai valitse Erätunnus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="8b3fe-125">Kirjaa kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="8b3fe-125">Post the journal</span></span>
1. <span data-ttu-id="8b3fe-126">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-126">Click Post.</span></span>
2. <span data-ttu-id="8b3fe-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="8b3fe-128">Tarkista jäljitystiedot</span><span class="sxs-lookup"><span data-stu-id="8b3fe-128">Check tracing information</span></span>
1. <span data-ttu-id="8b3fe-129">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-129">Click Inventory.</span></span>
2. <span data-ttu-id="8b3fe-130">Valitse Jäljitys.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-130">Click Trace.</span></span>
3. <span data-ttu-id="8b3fe-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-131">Click OK.</span></span>
    * <span data-ttu-id="8b3fe-132">Käyttämällä näitä jäljitystietoja, voit jäljittää taaksepäin, mistä erästä korjasit varaston.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="8b3fe-133">Nämä tiedot ovat nähtävissä myös Nimikkeen seuranta -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="8b3fe-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="8b3fe-135">Tarkista varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="8b3fe-135">Check inventory transactions</span></span>
1. <span data-ttu-id="8b3fe-136">Valitse Varasto.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-136">Click Inventory.</span></span>
2. <span data-ttu-id="8b3fe-137">Valitse Tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-137">Click Transactions.</span></span>
    * <span data-ttu-id="8b3fe-138">Tässä on näkyvissä tapahtumat, jotka luotiin kirjauskansioon kirjattaessa.</span><span class="sxs-lookup"><span data-stu-id="8b3fe-138">Here you can see the transactions that were created when you posted your journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]