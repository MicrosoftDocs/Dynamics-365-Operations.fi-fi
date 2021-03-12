---
title: Tuoterakenteen luominen dimensioperustaiselle päätuotteelle
description: Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ffe30f1b5aae3e954b527e84648f4dbb4b181513
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986901"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="b30cc-103">Tuoterakenteen luominen dimensioperustaiselle päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="b30cc-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b30cc-104">Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="b30cc-105">Ensimmäiset 4 tallennetta määrittävät tiedot, jotka tarvitaan tämän menettelyn suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="b30cc-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="b30cc-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b30cc-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b30cc-107">Tästä tehtävästä vastaa yleensä tuotesuunnittelija.</span><span class="sxs-lookup"><span data-stu-id="b30cc-107">This task is typically handled by the product designer.</span></span>


## <a name="select-the-product"></a><span data-ttu-id="b30cc-108">Valitse tuote</span><span class="sxs-lookup"><span data-stu-id="b30cc-108">Select the product</span></span>
1. <span data-ttu-id="b30cc-109">Valitse Vapautetun tuotteen ylläpito.</span><span class="sxs-lookup"><span data-stu-id="b30cc-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="b30cc-110">Valitse Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="b30cc-110">Click Released products.</span></span>
3. <span data-ttu-id="b30cc-111">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b30cc-112">Paikanna tämän tehtäväoppaan ensimmäisessä vaiheessa luomasi julkaistu päätuote, jolla on dimensioihin perustuva konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="b30cc-112">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
4. <span data-ttu-id="b30cc-113">Valitse toimintoruudussa Suunnittele.</span><span class="sxs-lookup"><span data-stu-id="b30cc-113">On the Action Pane, click Engineer.</span></span>
5. <span data-ttu-id="b30cc-114">Valitse Tuoterakenneversiot.</span><span class="sxs-lookup"><span data-stu-id="b30cc-114">Click BOM versions.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="b30cc-115">Luo uusi tuoterakenne ja tuoterakenneversio</span><span class="sxs-lookup"><span data-stu-id="b30cc-115">Create new BOM and BOM version</span></span>
1. <span data-ttu-id="b30cc-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-116">Click New.</span></span>
2. <span data-ttu-id="b30cc-117">Napsauta kohtia Tuoterakenne ja Tuoterakenneversio.</span><span class="sxs-lookup"><span data-stu-id="b30cc-117">Click BOM and BOM version.</span></span>
3. <span data-ttu-id="b30cc-118">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30cc-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b30cc-119">Toimipaikan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b30cc-119">Setting a site</span></span>  
    * <span data-ttu-id="b30cc-120">Näissä toimintaohjeissa ei määritetä tuoterakenteelle tiettyä toimipaikkaa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-120">In this procedure we don't set a specific site for the BOM.</span></span>  
4. <span data-ttu-id="b30cc-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b30cc-121">Click OK.</span></span>
5. <span data-ttu-id="b30cc-122">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-122">Click New.</span></span>
    * <span data-ttu-id="b30cc-123">Näissä toimintaohjeissa lisätään neljä riviä tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="b30cc-123">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="b30cc-124">Kaksi riviä edustavat kaapelivaihtoehtoja ja toisen kaksi riviä kabinettivaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="b30cc-124">Two lines represent cable options and two lines represent cabinet options.</span></span>  
6. <span data-ttu-id="b30cc-125">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-125">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b30cc-126">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b30cc-126">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-127">Valitse nimiketunnus A0001, HDMI 6' kaapelit.</span><span class="sxs-lookup"><span data-stu-id="b30cc-127">Select item number A0001, HDMI 6' Cables.</span></span>  
8. <span data-ttu-id="b30cc-128">Anna tai valitse arvo Konfiguraatioryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30cc-128">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-129">Valitse kaapelin konfiguraatioryhmä, joka luotiin oppaan vaiheessa 4.</span><span class="sxs-lookup"><span data-stu-id="b30cc-129">Select the Cable configuration group created in guide 4 in this sequence.</span></span>  
9. <span data-ttu-id="b30cc-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-130">Click New.</span></span>
    * <span data-ttu-id="b30cc-131">Valitse nimiketunnus A0002, HDMI 12' kaapelit.</span><span class="sxs-lookup"><span data-stu-id="b30cc-131">Select item number A0002, HDMI 12' Cables.</span></span>  
10. <span data-ttu-id="b30cc-132">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-132">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="b30cc-133">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b30cc-133">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="b30cc-134">Anna tai valitse arvo Konfiguraatioryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30cc-134">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-135">Valitse kaapelin konfiguraatioryhmä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="b30cc-135">Select the Cable configuration group again.</span></span>  
13. <span data-ttu-id="b30cc-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-136">Click New.</span></span>
14. <span data-ttu-id="b30cc-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-137">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="b30cc-138">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b30cc-138">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-139">Valitse nimiketunnus D0002 Kabinetti.</span><span class="sxs-lookup"><span data-stu-id="b30cc-139">Select item number D0002 Cabinet.</span></span>  
16. <span data-ttu-id="b30cc-140">Anna tai valitse arvo Konfiguraatioryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30cc-140">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-141">Valitse kabinetin konfiguraatioryhmä tälle tuoterakenteen riville.</span><span class="sxs-lookup"><span data-stu-id="b30cc-141">Select the Cabinet configuration group for this BOM line.</span></span>  
17. <span data-ttu-id="b30cc-142">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-142">Click New.</span></span>
18. <span data-ttu-id="b30cc-143">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b30cc-143">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="b30cc-144">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b30cc-144">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-145">Valitse nimiketunnus M0007 Vakiokabinetti viimeiseksi tuoterakenteen riviksi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-145">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
20. <span data-ttu-id="b30cc-146">Anna tai valitse arvo Konfiguraatioryhmä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="b30cc-146">In the Configuration group field, enter or select a value.</span></span>
    * <span data-ttu-id="b30cc-147">Valitse kabinetin konfiguraatioryhmä viimeiselle tuoterakenteen riville.</span><span class="sxs-lookup"><span data-stu-id="b30cc-147">Select the Cabinet configuration group for the laste BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="b30cc-148">Hyväksy ja aktivoi</span><span class="sxs-lookup"><span data-stu-id="b30cc-148">Approve and activate</span></span>
1. <span data-ttu-id="b30cc-149">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b30cc-149">Close the page.</span></span>
2. <span data-ttu-id="b30cc-150">Valitse Hyväksy.</span><span class="sxs-lookup"><span data-stu-id="b30cc-150">Click Approve.</span></span>
3. <span data-ttu-id="b30cc-151">Anna tai valitse Hyväksyjä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="b30cc-151">In the Approved by field, enter or select a value.</span></span>
4. <span data-ttu-id="b30cc-152">Vastaa kyllä kysymykseen "Haluatko myös hyväksyä tuoterakenteen?" avulla.</span><span class="sxs-lookup"><span data-stu-id="b30cc-152">Select Yes in the Do you also want to approve the bill of materials? field.</span></span>
5. <span data-ttu-id="b30cc-153">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="b30cc-153">Click OK.</span></span>
6. <span data-ttu-id="b30cc-154">Valitse Aktivoi.</span><span class="sxs-lookup"><span data-stu-id="b30cc-154">Click Activate.</span></span>

