---
title: Tuoterakenteen luominen dimensioperustaiselle päätuotteelle
description: Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventItemIdLookupSimple, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13053dd87242963586678b46c64493feb3383c4c
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920702"
---
# <a name="create-a-bill-of-materials-for-a-dimension-based-product-master"></a><span data-ttu-id="0b0ed-103">Tuoterakenteen luominen dimensioperustaiselle päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="0b0ed-103">Create a bill of materials for a dimension-based product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0b0ed-104">Tätä menettelyä varten sinun tulisi olla suorittanut edelliset 4 opasta tässä neljän tallenteen sarjassa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-104">For this procedure you should have completed the previous 4 guides in this sequence of eight recordings.</span></span> <span data-ttu-id="0b0ed-105">Ensimmäiset 4 tallennetta määrittävät tiedot, jotka tarvitaan tämän menettelyn suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-105">The first 4 recordings set up data that is required to complete this procedure.</span></span> <span data-ttu-id="0b0ed-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0b0ed-107">Tästä tehtävästä vastaa yleensä tuotesuunnittelija.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-107">This task is typically handled by the product designer.</span></span>

## <a name="select-the-product"></a><span data-ttu-id="0b0ed-108">Valitse tuote</span><span class="sxs-lookup"><span data-stu-id="0b0ed-108">Select the product</span></span>

1. <span data-ttu-id="0b0ed-109">Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-109">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="0b0ed-110">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-110">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0b0ed-111">Paikanna tämän tehtäväoppaan ensimmäisessä vaiheessa luomasi julkaistu päätuote, jolla on dimensioihin perustuva konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-111">Find the released product master with dimension-based configuration technology that you created in the first task guide in this sequence.</span></span>  
1. <span data-ttu-id="0b0ed-112">Valitse toimintoruudussa **Kehittäjä**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-112">On the Action Pane, select **Engineer**.</span></span>
1. <span data-ttu-id="0b0ed-113">Valitse **Tuoterakenneversiot**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-113">Select **BOM versions**.</span></span>

## <a name="create-new-bom-and-bom-version"></a><span data-ttu-id="0b0ed-114">Luo uusi tuoterakenne ja tuoterakenneversio</span><span class="sxs-lookup"><span data-stu-id="0b0ed-114">Create new BOM and BOM version</span></span>

1. <span data-ttu-id="0b0ed-115">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-115">Select **New**.</span></span>
1. <span data-ttu-id="0b0ed-116">Valitse **Tuoterakenne ja tuoterakenneversio**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-116">Select **BOM and BOM version**.</span></span>
1. <span data-ttu-id="0b0ed-117">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-117">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="0b0ed-118">Toimipaikan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0b0ed-118">Setting a site</span></span>  
    * <span data-ttu-id="0b0ed-119">Näissä toimintaohjeissa ei määritetä tuoterakenteelle tiettyä toimipaikkaa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-119">In this procedure we don't set a specific site for the BOM.</span></span>  
1. <span data-ttu-id="0b0ed-120">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-120">Select **OK**.</span></span>
1. <span data-ttu-id="0b0ed-121">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-121">Select **New**.</span></span>
    * <span data-ttu-id="0b0ed-122">Näissä toimintaohjeissa lisätään neljä riviä tuoterakenteeseen.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-122">In this procedure we will add four lines to the BOM.</span></span> <span data-ttu-id="0b0ed-123">Kaksi riviä edustavat kaapelivaihtoehtoja ja toisen kaksi riviä kabinettivaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-123">Two lines represent cable options and two lines represent cabinet options.</span></span>  
1. <span data-ttu-id="0b0ed-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-124">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b0ed-125">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-125">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-126">Valitse nimiketunnus A0001, HDMI 6' kaapelit.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-126">Select item number A0001, HDMI 6' Cables.</span></span>  
1. <span data-ttu-id="0b0ed-127">Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-127">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-128">Valitse kaapelin konfiguraatioryhmä, joka luotiin oppaan vaiheessa 4.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-128">Select the cable configuration group created in guide 4 in this sequence.</span></span>  
1. <span data-ttu-id="0b0ed-129">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-129">Select **New**.</span></span>
    * <span data-ttu-id="0b0ed-130">Valitse nimiketunnus A0002, HDMI 12' kaapelit.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-130">Select item number A0002, HDMI 12' Cables.</span></span>  
1. <span data-ttu-id="0b0ed-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-131">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b0ed-132">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-132">In the **Item number** field, enter or select a value.</span></span>
1. <span data-ttu-id="0b0ed-133">Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-133">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-134">Valitse kaapelin konfiguraatioryhmä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-134">Select the cable configuration group again.</span></span>  
1. <span data-ttu-id="0b0ed-135">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-135">Select **New**.</span></span>
1. <span data-ttu-id="0b0ed-136">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-136">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b0ed-137">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-137">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-138">Valitse nimiketunnus D0002 Kabinetti.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-138">Select item number D0002 Cabinet.</span></span>  
1. <span data-ttu-id="0b0ed-139">Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-139">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-140">Valitse kabinetin konfiguraatioryhmä tälle tuoterakenteen riville.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-140">Select the cabinet configuration group for this BOM line.</span></span>  
1. <span data-ttu-id="0b0ed-141">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-141">Select **New**.</span></span>
1. <span data-ttu-id="0b0ed-142">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-142">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="0b0ed-143">Syötä tai valitse arvo **Nimiketunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-143">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-144">Valitse nimiketunnus M0007 Vakiokabinetti viimeiseksi tuoterakenteen riviksi.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-144">Select Item number M0007 StandardCabinet as the last BOM line.</span></span>  
1. <span data-ttu-id="0b0ed-145">Anna tai valitse arvo **Konfiguraatioryhmä**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-145">In the **Configuration group** field, enter or select a value.</span></span>
    * <span data-ttu-id="0b0ed-146">Valitse kabinetin konfiguraatioryhmä viimeiselle tuoterakenteen riville.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-146">Select the Cabinet configuration group for the last BOM line.</span></span>  

## <a name="approve-and-activate"></a><span data-ttu-id="0b0ed-147">Hyväksy ja aktivoi</span><span class="sxs-lookup"><span data-stu-id="0b0ed-147">Approve and activate</span></span>

1. <span data-ttu-id="0b0ed-148">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-148">Close the page.</span></span>
1. <span data-ttu-id="0b0ed-149">Valitse **Hyväksy**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-149">Select **Approve**.</span></span>
1. <span data-ttu-id="0b0ed-150">Anna tai valitse **Hyväksyjä**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-150">In the **Approved by** field, enter or select a value.</span></span>
1. <span data-ttu-id="0b0ed-151">Vastaa *Kyllä* **Haluatko myös hyväksyä tuoterakenteen?** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-151">Select *Yes* in the **Do you also want to approve the bill of materials?** field.</span></span>
1. <span data-ttu-id="0b0ed-152">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-152">Select **OK**.</span></span>
1. <span data-ttu-id="0b0ed-153">Valitse **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="0b0ed-153">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]