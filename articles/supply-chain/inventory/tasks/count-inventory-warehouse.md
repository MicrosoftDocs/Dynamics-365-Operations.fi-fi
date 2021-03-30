---
title: Varaston kokonaismäärän laskeminen
description: Tässä aiheessa kuvataan varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 452822eaf26c26e4c9e00f909dbd18127f6fc781
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230101"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="1425b-103">Varaston kokonaismäärän laskeminen</span><span class="sxs-lookup"><span data-stu-id="1425b-103">Count inventory in a warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1425b-104">Tässä aiheessa kuvataan varaston inventointikirjauskansion luonti- ja kirjausprosessi, jolla voidaan inventoida tietty nimike varastosijainnissa.</span><span class="sxs-lookup"><span data-stu-id="1425b-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="1425b-105">Menettely koskee Inventoinnin- ja varastonhallinta -moduulin varastoinnin perustoimintoja. Se ei koske Varastonhallinta-moduulin varastointitoimintoja.</span><span class="sxs-lookup"><span data-stu-id="1425b-105">The procedure applies to "basic warehousing" functionality, available in the Inventory management module, not to the warehousing functionality that's available in the Warehouse management module.</span></span> <span data-ttu-id="1425b-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="1425b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="1425b-107">Jos käytät omia tietoja, varmista, että olet määrittänyt tuotteita ja sijainteja ja että olet luonut inventointikirjauskansioille varastokirjauskansion.</span><span class="sxs-lookup"><span data-stu-id="1425b-107">If you're using your own data, make sure that you have products and locations set up, and that you've created an inventory journal name for counting journals.</span></span> <span data-ttu-id="1425b-108">Varastoinventoinnin suorittaa tavallisesti varastotyöntekijä.</span><span class="sxs-lookup"><span data-stu-id="1425b-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="1425b-109">Luo varaston inventointikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="1425b-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="1425b-110">Valitse **Siirtymisruutu > Moduulit > Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Inventointi > Inventointi**.</span><span class="sxs-lookup"><span data-stu-id="1425b-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="1425b-111">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1425b-111">Select **New**.</span></span>
3. <span data-ttu-id="1425b-112">Valitse **Nimi**-kentässä avattavasta luettelosta varastoinventoinnin kirjauskansion nimi, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="1425b-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="1425b-113">Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston inventointikirjauskansion asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="1425b-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="1425b-114">Avaa haku valitsemalla **Työntekijä**-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="1425b-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="1425b-115">**Valitse** luettelosta työntekijä, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="1425b-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="1425b-116">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1425b-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="1425b-117">Luo kirjauskansion rivejä</span><span class="sxs-lookup"><span data-stu-id="1425b-117">Create journal lines</span></span>
1. <span data-ttu-id="1425b-118">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="1425b-118">Select **New**.</span></span>
2. <span data-ttu-id="1425b-119">Valitse **Nimiketunnus**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="1425b-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="1425b-120">Jos käytät USMF-yrityksen demotietoja, valitse **A0001**.</span><span class="sxs-lookup"><span data-stu-id="1425b-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="1425b-121">Valitse **Toimipaikka**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="1425b-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="1425b-122">Jos käytät USMF-yrityksen demotietoja, valitse toimipaikka **2**.</span><span class="sxs-lookup"><span data-stu-id="1425b-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="1425b-123">Valitse **Varasto**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="1425b-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="1425b-124">Jos käytät USMF-yrityksen demotietoja, valitse varasto **24**.</span><span class="sxs-lookup"><span data-stu-id="1425b-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="1425b-125">Valitse **Sijainti**-kentässä avattavasta valikosta haluttu tietue.</span><span class="sxs-lookup"><span data-stu-id="1425b-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="1425b-126">Jos käytät USMF-yrityksen demotietoja, valitse sijainti **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="1425b-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="1425b-127">Lisää Inventoitu-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1425b-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="1425b-128">Jos annat inventoitu määrä, joka poikkeaa **Varastosaldo**-kentässä olevasta numerosta, **Määrä**-kenttä päivitetään näyttämään ristiriita.</span><span class="sxs-lookup"><span data-stu-id="1425b-128">If you enter a counted number that's different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="1425b-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="1425b-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="1425b-130">Kirjaa varaston inventointikirjauskansio</span><span class="sxs-lookup"><span data-stu-id="1425b-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="1425b-131">Valitse **Kirjaa**.</span><span class="sxs-lookup"><span data-stu-id="1425b-131">Select **Post**.</span></span> <span data-ttu-id="1425b-132">Jos varaston inventointikirjauskansiota kirjatessa kirjataan varastovastaanoton **Varastosaldo**-kentässä tai varasto-otossa olevasta määrästä eroava inventoitu määrä, varastotaso ja arvo muuttuvat ja kirjanpitotapahtumat muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="1425b-132">When you post an inventory counting journal, if the counted amount differs from amount that's reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="1425b-133">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="1425b-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="1425b-134">Näytä varastotapahtumat</span><span class="sxs-lookup"><span data-stu-id="1425b-134">View inventory transactions</span></span>
1. <span data-ttu-id="1425b-135">Valitse **Varasto**.</span><span class="sxs-lookup"><span data-stu-id="1425b-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="1425b-136">Valitse **Tapahtumat**.</span><span class="sxs-lookup"><span data-stu-id="1425b-136">Select **Transactions**.</span></span> <span data-ttu-id="1425b-137">Tässä näkyvät kaikki liittyvät tapahtumat, jotka luodaan, kun varaston inventointikirjauskansioon kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1425b-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]