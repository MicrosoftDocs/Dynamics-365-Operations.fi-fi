---
title: "Fyysiset ja kirjanpidolliset päivitykset"
description: "Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e62bdbfb7b88f66ea1f6e4d57b6150c8b0bffb04
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="6002e-103">Fyysiset ja kirjanpidolliset päivitykset</span><span class="sxs-lookup"><span data-stu-id="6002e-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6002e-104">Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="6002e-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="6002e-105">Varastotapahtumia voi päivittää sekä fyysisesti että kirjanpidollisesti Microsoft Dynamics 365 for Finance and Operationsissa.</span><span class="sxs-lookup"><span data-stu-id="6002e-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="6002e-106">Tietynlaisen fyysiset ja kirjanpidolliset tapahtumat lisäävät varastomääriä, ja toisenlaiset laskevat varastomääriä.</span><span class="sxs-lookup"><span data-stu-id="6002e-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="6002e-107">Fyysisiä lisäyksiä</span><span class="sxs-lookup"><span data-stu-id="6002e-107">Physical increases</span></span>
<span data-ttu-id="6002e-108">Kun fyysinen tapahtuma kirjataan, tapahtumatietueen tila on **Vastaanotettu**.</span><span class="sxs-lookup"><span data-stu-id="6002e-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="6002e-109">Seuraavat tapahtumat ovat fyysisiä lisäyksiä:</span><span class="sxs-lookup"><span data-stu-id="6002e-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="6002e-110">ostotilauksen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="6002e-110">Purchase order receipt</span></span>
-   <span data-ttu-id="6002e-111">myyntitilauksen pakkausluettelon palautus</span><span class="sxs-lookup"><span data-stu-id="6002e-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="6002e-112">Tuotantotilauksen ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="6002e-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="6002e-113">tuotantotilauksen keräysluettelon sivutuote.</span><span class="sxs-lookup"><span data-stu-id="6002e-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="6002e-114">Taloudelliset lisäykset</span><span class="sxs-lookup"><span data-stu-id="6002e-114">Financial increases</span></span>
<span data-ttu-id="6002e-115">Kun maksuvastaanottotapahtuma kirjataan, määrää lisäävän tapahtumatietueen tila on **Ostettu**.</span><span class="sxs-lookup"><span data-stu-id="6002e-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="6002e-116">Seuraavat tapahtumat ovat kirjanpidollisia lisäyksiä:</span><span class="sxs-lookup"><span data-stu-id="6002e-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="6002e-117">Toimittajan lasku</span><span class="sxs-lookup"><span data-stu-id="6002e-117">Vendor invoice</span></span>
-   <span data-ttu-id="6002e-118">palautuksen myyntitilauslasku</span><span class="sxs-lookup"><span data-stu-id="6002e-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="6002e-119">tuotantotilauksen kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="6002e-119">Production order costing</span></span>
-   <span data-ttu-id="6002e-120">Positiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto</span><span class="sxs-lookup"><span data-stu-id="6002e-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="6002e-121">Tapahtumat, jotka lisäävät määrää.</span><span class="sxs-lookup"><span data-stu-id="6002e-121">Transactions that increase quantity</span></span>
<span data-ttu-id="6002e-122">Määrää lisäävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla.</span><span class="sxs-lookup"><span data-stu-id="6002e-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="6002e-123">Finance and Operations laskee juoksevan keskimääräisen kustannushinnan, joka perustuu kirjanpidollisesti seurattavien varastodimensioiden tapahtumien kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="6002e-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="6002e-124">Lisätietoja juoksevasta keskimääräisestä kustannushinnasta: [Juokseva keskimääräinen kustannushinta](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="6002e-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="6002e-125">Tapahtumat, jotka vähentävät määrää.</span><span class="sxs-lookup"><span data-stu-id="6002e-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="6002e-126">Finance and Operations käyttää laskettua juoksevaa kustannushintaa, kun määrää vähentävä tapahtuma kirjataan, riippumatta siitä mikä varastomalli on liitetty kyseiseen varastoon.</span><span class="sxs-lookup"><span data-stu-id="6002e-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="6002e-127">Määrää vähentävää tapahtumaa ei saa olla merkitty aiemmin toiseen tapahtumaan ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="6002e-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="6002e-128">Jos fyysinen käytettävissä oleva varasto muuttuu negatiiviseksi, Dynamics 365 for Finance and Operations käyttää nimikkeelle **Nimike**-lomakkeessa määritettyä varastokustannusta.</span><span class="sxs-lookup"><span data-stu-id="6002e-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="6002e-129">**Huomautus:** Jos multisite-toiminnot on otettu käyttöön, tätä kustannusta käytetään toimipaikan varastokustannuksena, joka on määritetty sivustolle **Tilauksen oletusasetukset** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="6002e-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="6002e-130">Kirjanpidolliset varasto-otot verrattuina fyysiseen ottoon</span><span class="sxs-lookup"><span data-stu-id="6002e-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="6002e-131">Kun fyysinen varasto-ottotapahtuma kirjataan, tapahtumatietueentila on **Toimitettu**.</span><span class="sxs-lookup"><span data-stu-id="6002e-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="6002e-132">Seuraavat tapahtumat ovat fyysisiä varasto-ottoja:</span><span class="sxs-lookup"><span data-stu-id="6002e-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="6002e-133">tuotantotilauksen keräysluettelon kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="6002e-133">Production order picking list journal</span></span>
-   <span data-ttu-id="6002e-134">myyntitilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="6002e-134">Sales order packing slip</span></span>
-   <span data-ttu-id="6002e-135">ostotilauksen pakkausluettelon palautus.</span><span class="sxs-lookup"><span data-stu-id="6002e-135">Purchase order packing slip return</span></span>

<span data-ttu-id="6002e-136">Kun kirjanpitotapahtuma kirjataan, tapahtumatietueen tila on **Myyty**.</span><span class="sxs-lookup"><span data-stu-id="6002e-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="6002e-137">Seuraavat tapahtumat ovat kirjanpidollisia varasto-ottoja:</span><span class="sxs-lookup"><span data-stu-id="6002e-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="6002e-138">Tuotantotilauksen lopetus</span><span class="sxs-lookup"><span data-stu-id="6002e-138">Ending a production order</span></span>
-   <span data-ttu-id="6002e-139">Myyntitilauslasku</span><span class="sxs-lookup"><span data-stu-id="6002e-139">Sales order invoice</span></span>
-   <span data-ttu-id="6002e-140">Toimittajalaskun palautus</span><span class="sxs-lookup"><span data-stu-id="6002e-140">Vendor invoice return</span></span>
-   <span data-ttu-id="6002e-141">Negatiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto</span><span class="sxs-lookup"><span data-stu-id="6002e-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="6002e-142">Määrää vähentävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla.</span><span class="sxs-lookup"><span data-stu-id="6002e-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="6002e-143">Tämän vuoksi varaston sulkemistoiminto vaaditaan varasto-ottotapahtumien täsmäyttämiseksi vastaanottotapahtumiksi jokaiseen nimikkeeseen määritetyn varastomallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="6002e-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




