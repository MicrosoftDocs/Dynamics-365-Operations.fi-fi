---
title: Kustannusobjektit
description: Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään. Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään. Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85e590322c75cfb2ad21236af56656061037a4b7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427214"
---
# <a name="cost-objects"></a><span data-ttu-id="506da-105">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="506da-105">Cost objects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="506da-106">Tässä artikkelissa on tietoja kustannusobjekteista ja siitä, miten kustannukset ja määrät kerätään.</span><span class="sxs-lookup"><span data-stu-id="506da-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="506da-107">Kustannusobjekti on yksikkö, johon kustannukset ja määrät kerätään.</span><span class="sxs-lookup"><span data-stu-id="506da-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="506da-108">Kustannusobjektiyksiköt voivat olla tuotteita tai tuotevariantteja, kuten tyylin ja värin variantteja.</span><span class="sxs-lookup"><span data-stu-id="506da-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="506da-109">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="506da-109">Cost objects</span></span>

<span data-ttu-id="506da-110">**Kustannuskohde**-sivulla eritellään kaikki kustannuskohteet, jotka on rekisteröity tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="506da-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="506da-111">Kustannuskohteet määritetään seuraavista lähteistä saaduilla tiedoilla:</span><span class="sxs-lookup"><span data-stu-id="506da-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="506da-112">Tuote</span><span class="sxs-lookup"><span data-stu-id="506da-112">Product</span></span>
-   <span data-ttu-id="506da-113">Tuotedimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-113">Product dimension group</span></span>
-   <span data-ttu-id="506da-114">Varastodimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-114">Storage dimension group</span></span>
-   <span data-ttu-id="506da-115">Seurantadimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-115">Tracking dimension group</span></span>

<span data-ttu-id="506da-116">**Huomautus:** Kustannuskohde edustaa vain **Suorat Materiaalit** -tyypin kustannusryhmää.</span><span class="sxs-lookup"><span data-stu-id="506da-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="506da-117">Kustannuskohde ja varastokohde eroavat sillä tavalla, että kustannuskohde määritetään varastodimensioiden mukaan, jotka valitaan taloudellista varastoa varten.</span><span class="sxs-lookup"><span data-stu-id="506da-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="506da-118">Esimerkiksi, nimikkeellä on seuraava rakenne:</span><span class="sxs-lookup"><span data-stu-id="506da-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="506da-119">**Toimipaikka:** varastonmääritys = Kyllä, taloudellinen varasto = Kyllä</span><span class="sxs-lookup"><span data-stu-id="506da-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="506da-120">**Varasto:** varastonmääritys = Kyllä, taloudellinen varasto = Ei</span><span class="sxs-lookup"><span data-stu-id="506da-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="506da-121">**Eränumero:** varastonmääritys = Kyllä, taloudellinen varasto = Ei</span><span class="sxs-lookup"><span data-stu-id="506da-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="506da-122">Seuraavassa taulukossa näkyy mikä on kustannuskohde ja mikä on varastokohde.</span><span class="sxs-lookup"><span data-stu-id="506da-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="506da-123">Objektityyppi</span><span class="sxs-lookup"><span data-stu-id="506da-123">Object type</span></span>      | <span data-ttu-id="506da-124">Nimiketunnus</span><span class="sxs-lookup"><span data-stu-id="506da-124">Item number</span></span> | <span data-ttu-id="506da-125">Sivusto</span><span class="sxs-lookup"><span data-stu-id="506da-125">Site</span></span> | <span data-ttu-id="506da-126">Varasto</span><span class="sxs-lookup"><span data-stu-id="506da-126">Warehouse</span></span> | <span data-ttu-id="506da-127">Eränumero.</span><span class="sxs-lookup"><span data-stu-id="506da-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="506da-128">Kustannuskohde</span><span class="sxs-lookup"><span data-stu-id="506da-128">Cost object</span></span>      | <span data-ttu-id="506da-129">x</span><span class="sxs-lookup"><span data-stu-id="506da-129">x</span></span>           | <span data-ttu-id="506da-130">x</span><span class="sxs-lookup"><span data-stu-id="506da-130">x</span></span>    |           |           |
| <span data-ttu-id="506da-131">Varastokohde</span><span class="sxs-lookup"><span data-stu-id="506da-131">Inventory object</span></span> | <span data-ttu-id="506da-132">x</span><span class="sxs-lookup"><span data-stu-id="506da-132">x</span></span>           | <span data-ttu-id="506da-133">x</span><span class="sxs-lookup"><span data-stu-id="506da-133">x</span></span>    |  <span data-ttu-id="506da-134">x</span><span class="sxs-lookup"><span data-stu-id="506da-134">x</span></span>        | <span data-ttu-id="506da-135">x</span><span class="sxs-lookup"><span data-stu-id="506da-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="506da-136">Kustannusten ja määrien kasvu</span><span class="sxs-lookup"><span data-stu-id="506da-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="506da-137">Arvo **Arvo**-kentässä on seuraavien arvojen summa:</span><span class="sxs-lookup"><span data-stu-id="506da-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="506da-138">Fyysinen kustannus</span><span class="sxs-lookup"><span data-stu-id="506da-138">Physical cost amount</span></span>
    -   <span data-ttu-id="506da-139">Rahoituksellinen kustannus</span><span class="sxs-lookup"><span data-stu-id="506da-139">Financial cost amount</span></span>
    -   <span data-ttu-id="506da-140">Oikaisut</span><span class="sxs-lookup"><span data-stu-id="506da-140">Adjustments</span></span>
-   <span data-ttu-id="506da-141">Arvo **Määrä**-kentässä on seuraavien arvojen summa:</span><span class="sxs-lookup"><span data-stu-id="506da-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="506da-142">Vastaanotettu</span><span class="sxs-lookup"><span data-stu-id="506da-142">Received</span></span>
    -   <span data-ttu-id="506da-143">Toimitettu</span><span class="sxs-lookup"><span data-stu-id="506da-143">Deducted</span></span>
    -   <span data-ttu-id="506da-144">Kirjattu määrä</span><span class="sxs-lookup"><span data-stu-id="506da-144">Posted quantity</span></span>
-   <span data-ttu-id="506da-145">**Keskimääräinen yksikkökustannus**-kenttä on laskettu kenttä.</span><span class="sxs-lookup"><span data-stu-id="506da-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="506da-146">Arvo lasketaan jakamalla **Arvo**-arvo **Määrä**-arvolla.</span><span class="sxs-lookup"><span data-stu-id="506da-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="506da-147">**Huomautus:** **Sisällytä fyysinen arvo** -parametri ei vaikuta edellisiin laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="506da-147">**Note:** The \*\*Include physical value \*\*parameter has no effect on the preceding calculations.</span></span>

<a name="additional-resources"></a><span data-ttu-id="506da-148">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="506da-148">Additional resources</span></span>
--------

[<span data-ttu-id="506da-149">Tuotedimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-149">Product dimension group</span></span>](https://technet.microsoft.com/library/aa499382.aspx)

[<span data-ttu-id="506da-150">Varastodimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-150">Storage dimension group</span></span>](https://technet.microsoft.com/library/hh209317.aspx)

[<span data-ttu-id="506da-151">Seurantadimensioryhmä</span><span class="sxs-lookup"><span data-stu-id="506da-151">Tracking dimension group</span></span>](https://technet.microsoft.com/library/hh209465.aspx)

[<span data-ttu-id="506da-152">Uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="506da-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="506da-153">Kustannusmerkinnät</span><span class="sxs-lookup"><span data-stu-id="506da-153">Cost entries</span></span>](cost-entries.md)



