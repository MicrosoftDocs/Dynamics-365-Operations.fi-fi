---
title: Varaston varastotasojen oikaisu (perusvarastointi)
description: Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja.
author: MarkusFogelberg
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d91c8901a4ff7df8ae6c3d9b98024db57e29f15b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209536"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="6420c-103">Varaston varastotasojen oikaisu (perusvarastointi)</span><span class="sxs-lookup"><span data-stu-id="6420c-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6420c-104">Tässä menettelyssä selvitetään varaston oikaisun kirjauskansion luonti- ja kirjausprosessi, jolla voidaan oikaista varastossa olevien tuotteiden varastotasoja.</span><span class="sxs-lookup"><span data-stu-id="6420c-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="6420c-105">Ennen aloittamista varasto-oikaisuille on oltava määritettynä varaston oikaisun kirjauskansio.</span><span class="sxs-lookup"><span data-stu-id="6420c-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="6420c-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="6420c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="6420c-107">Yleensä varastotyöntekijä tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="6420c-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="6420c-108">Luo varaston oikaisun kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="6420c-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="6420c-109">Valitse Inventoinnin- ja varastonhallinta > Kirjauskansioviennit > Nimikkeet > Varaston oikaisu.</span><span class="sxs-lookup"><span data-stu-id="6420c-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="6420c-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6420c-110">Click New.</span></span>
3. <span data-ttu-id="6420c-111">Avaa haku valitsemalla Nimi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6420c-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6420c-112">Valitse luettelosta varaston oikaisun kirjauskansio, jota haluat käyttää.</span><span class="sxs-lookup"><span data-stu-id="6420c-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="6420c-113">Joidenkin kenttien tiedot voidaan lisätä valitsemasi varaston oikaisun kirjauskansion asetusten perusteella.</span><span class="sxs-lookup"><span data-stu-id="6420c-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="6420c-114">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6420c-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="6420c-115">Tämän kirjauskansion rivit</span><span class="sxs-lookup"><span data-stu-id="6420c-115">Create journal lines</span></span>
1. <span data-ttu-id="6420c-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="6420c-116">Click New.</span></span>
2. <span data-ttu-id="6420c-117">Merkitse luettelossa nimiketunnuskenttä.</span><span class="sxs-lookup"><span data-stu-id="6420c-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="6420c-118">Valitse Nimiketunnus-kentässä nimike.</span><span class="sxs-lookup"><span data-stu-id="6420c-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="6420c-119">Jos käytät USMF-yrityksen demotietoja, kirjoita D0001.</span><span class="sxs-lookup"><span data-stu-id="6420c-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="6420c-120">Avaa haku napsauttamalla Toimipaikka-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="6420c-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="6420c-121">Valitse luettelosta toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="6420c-121">In the list, select a site.</span></span>
6. <span data-ttu-id="6420c-122">Avaa haku valitsemalla Varasto-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="6420c-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6420c-123">Valitse luettelosta varasto.</span><span class="sxs-lookup"><span data-stu-id="6420c-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="6420c-124">Jos olet valinnut nimikkeen, jossa sijainti on pakollinen dimensio, sijainti on määritettävä tässä.</span><span class="sxs-lookup"><span data-stu-id="6420c-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="6420c-125">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6420c-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6420c-126">Kustannushinnan kenttä määrittää varastovastaanottojen yksikkökohtaisen kustannuksen.</span><span class="sxs-lookup"><span data-stu-id="6420c-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="6420c-127">Jos nimiketunnukselle ei ole määritetty kustannusta tai haluat muuttaa sitä manuaalisesti, voit tehdä sen tässä.</span><span class="sxs-lookup"><span data-stu-id="6420c-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="6420c-128">Vahvista ja kirjaa varaston oikaisun kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="6420c-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="6420c-129">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="6420c-129">Click Validate.</span></span>
2. <span data-ttu-id="6420c-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6420c-130">Click OK.</span></span>
3. <span data-ttu-id="6420c-131">Valitse Kirjaa.</span><span class="sxs-lookup"><span data-stu-id="6420c-131">Click Post.</span></span>
    * <span data-ttu-id="6420c-132">Kun kirjaat tämäntyyppisen kirjauskansion, järjestelmä kirjaa varastovastaanoton tai varasto-oton, muuttaa varastotason ja -arvon sekä luo kirjanpitotapahtumat.</span><span class="sxs-lookup"><span data-stu-id="6420c-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="6420c-133">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6420c-133">Click OK.</span></span>
5. <span data-ttu-id="6420c-134">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="6420c-134">Close the form.</span></span>
6. <span data-ttu-id="6420c-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="6420c-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]