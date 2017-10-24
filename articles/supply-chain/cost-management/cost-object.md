---
title: Kustannusobjektit
description: "Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 13efb284c24c20cf4115ce2dd50be31dd3e5543e
ms.contentlocale: fi-fi
ms.lasthandoff: 10/13/2017

---

# <a name="cost-objects"></a><span data-ttu-id="9b10f-105">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="9b10f-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9b10f-106">Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään.</span><span class="sxs-lookup"><span data-stu-id="9b10f-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="9b10f-107">Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään.</span><span class="sxs-lookup"><span data-stu-id="9b10f-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="9b10f-108">Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.</span><span class="sxs-lookup"><span data-stu-id="9b10f-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="9b10f-109">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="9b10f-109">Cost objects</span></span>

<span data-ttu-id="9b10f-110">**Kustannuskohde**-sivulla eritellään kaikki kustannuskohteet, jotka on rekisteröity tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="9b10f-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="9b10f-111">Kustannuskohteet määritetään seuraavista lähteistä saaduilla tiedoilla:</span><span class="sxs-lookup"><span data-stu-id="9b10f-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="9b10f-112">Tuote</span><span class="sxs-lookup"><span data-stu-id="9b10f-112">Product</span></span>
-   <span data-ttu-id="9b10f-113">Tuotedimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-113">Product dimension group</span></span>
-   <span data-ttu-id="9b10f-114">Varastodimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-114">Storage dimension group</span></span>
-   <span data-ttu-id="9b10f-115">Seurantadimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-115">Tracking dimension group</span></span>

<span data-ttu-id="9b10f-116">**Huomautus:** Kustannuskohde edustaa vain **Suorat Materiaalit** -tyypin kustannusryhmää.</span><span class="sxs-lookup"><span data-stu-id="9b10f-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="9b10f-117">Kustannuskohde ja varastokohde eroavat sillä tavalla, että kustannuskohde määritetään varastodimensioiden mukaan, jotka valitaan taloudellista varastoa varten.</span><span class="sxs-lookup"><span data-stu-id="9b10f-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="9b10f-118">Esimerkiksi, nimikkeellä on seuraava rakenne:</span><span class="sxs-lookup"><span data-stu-id="9b10f-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="9b10f-119">**Toimipaikka:** varastonmääritys = Kyllä, taloudellinen varasto = Kyllä</span><span class="sxs-lookup"><span data-stu-id="9b10f-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="9b10f-120">**Varasto:** varastonmääritys = Kyllä, taloudellinen varasto = Ei</span><span class="sxs-lookup"><span data-stu-id="9b10f-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="9b10f-121">**Eränumero:** varastonmääritys = Kyllä, taloudellinen varasto = Ei</span><span class="sxs-lookup"><span data-stu-id="9b10f-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="9b10f-122">Seuraavassa taulukossa näkyy mikä on kustannuskohde ja mikä on varastokohde.</span><span class="sxs-lookup"><span data-stu-id="9b10f-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="9b10f-123">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="9b10f-123">Object type</span></span>      | <span data-ttu-id="9b10f-124">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="9b10f-124">Item number</span></span> | <span data-ttu-id="9b10f-125">Sivusto</span><span class="sxs-lookup"><span data-stu-id="9b10f-125">Site</span></span> | <span data-ttu-id="9b10f-126">Varasto</span><span class="sxs-lookup"><span data-stu-id="9b10f-126">Warehouse</span></span> | <span data-ttu-id="9b10f-127">Eränumero.</span><span class="sxs-lookup"><span data-stu-id="9b10f-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="9b10f-128">Kustannuskohde</span><span class="sxs-lookup"><span data-stu-id="9b10f-128">Cost object</span></span>      | <span data-ttu-id="9b10f-129">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-129">x</span></span>           | <span data-ttu-id="9b10f-130">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-130">x</span></span>    |           |           |
| <span data-ttu-id="9b10f-131">Varastokohde</span><span class="sxs-lookup"><span data-stu-id="9b10f-131">Inventory object</span></span> | <span data-ttu-id="9b10f-132">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-132">x</span></span>           | <span data-ttu-id="9b10f-133">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-133">x</span></span>    |  <span data-ttu-id="9b10f-134">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-134">x</span></span>        | <span data-ttu-id="9b10f-135">x</span><span class="sxs-lookup"><span data-stu-id="9b10f-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="9b10f-136">Kustannusten ja määrien kasvu</span><span class="sxs-lookup"><span data-stu-id="9b10f-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="9b10f-137">Arvo **Arvo**-kentässä on seuraavien arvojen summa:</span><span class="sxs-lookup"><span data-stu-id="9b10f-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="9b10f-138">Fyysinen kustannus</span><span class="sxs-lookup"><span data-stu-id="9b10f-138">Physical cost amount</span></span>
    -   <span data-ttu-id="9b10f-139">Rahoituksellinen kustannus</span><span class="sxs-lookup"><span data-stu-id="9b10f-139">Financial cost amount</span></span>
    -   <span data-ttu-id="9b10f-140">Oikaisut</span><span class="sxs-lookup"><span data-stu-id="9b10f-140">Adjustments</span></span>
-   <span data-ttu-id="9b10f-141">Arvo **Määrä**-kentässä on seuraavien arvojen summa:</span><span class="sxs-lookup"><span data-stu-id="9b10f-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="9b10f-142">Vastaanotettu</span><span class="sxs-lookup"><span data-stu-id="9b10f-142">Received</span></span>
    -   <span data-ttu-id="9b10f-143">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="9b10f-143">Deducted</span></span>
    -   <span data-ttu-id="9b10f-144">Kirjattu määrä</span><span class="sxs-lookup"><span data-stu-id="9b10f-144">Posted quantity</span></span>
-   <span data-ttu-id="9b10f-145">**Keskimääräinen yksikkökustannus**-kenttä on laskettu kenttä.</span><span class="sxs-lookup"><span data-stu-id="9b10f-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="9b10f-146">Arvo lasketaan jakamalla **Arvo**-arvo **Määrä**-arvolla.</span><span class="sxs-lookup"><span data-stu-id="9b10f-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="9b10f-147">**Huomautus:** **Sisällytä fyysinen arvo** -parametri ei vaikuta edellisiin laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="9b10f-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="9b10f-148">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="9b10f-148">See also</span></span>
--------

[<span data-ttu-id="9b10f-149">Tuotedimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="9b10f-150">Varastodimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="9b10f-151">Seurantadimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="9b10f-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="9b10f-152">Uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="9b10f-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="9b10f-153">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="9b10f-153">Cost entries</span></span>](cost-entries.md)




