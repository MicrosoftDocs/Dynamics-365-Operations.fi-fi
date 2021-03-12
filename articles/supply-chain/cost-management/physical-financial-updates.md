---
title: Fyysiset ja kirjanpidolliset päivitykset
description: Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b29c1c0727487992a478552d94b5bbe8684d0550
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967455"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="16133-103">Fyysiset ja kirjanpidolliset päivitykset</span><span class="sxs-lookup"><span data-stu-id="16133-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16133-104">Tämä ohjeaihe sisältää varastomääriä lisäävien tai vähentävien tapahtumatyyppien yhteenvedon.</span><span class="sxs-lookup"><span data-stu-id="16133-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="16133-105">Varastotapahtumia voi päivittää sekä fyysisesti että kirjanpidollisesti Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="16133-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="16133-106">Tietynlaisen fyysiset ja kirjanpidolliset tapahtumat lisäävät varastomääriä, ja toisenlaiset laskevat varastomääriä.</span><span class="sxs-lookup"><span data-stu-id="16133-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="16133-107">Fyysisiä lisäyksiä</span><span class="sxs-lookup"><span data-stu-id="16133-107">Physical increases</span></span>
<span data-ttu-id="16133-108">Kun fyysinen tapahtuma kirjataan, tapahtumatietueen tila on **Vastaanotettu**.</span><span class="sxs-lookup"><span data-stu-id="16133-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="16133-109">Seuraavat tapahtumat ovat fyysisiä lisäyksiä:</span><span class="sxs-lookup"><span data-stu-id="16133-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="16133-110">ostotilauksen vastaanotto</span><span class="sxs-lookup"><span data-stu-id="16133-110">Purchase order receipt</span></span>
-   <span data-ttu-id="16133-111">myyntitilauksen pakkausluettelon palautus</span><span class="sxs-lookup"><span data-stu-id="16133-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="16133-112">Tuotantotilauksen ilmoittaminen valmiiksi</span><span class="sxs-lookup"><span data-stu-id="16133-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="16133-113">tuotantotilauksen keräysluettelon sivutuote.</span><span class="sxs-lookup"><span data-stu-id="16133-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="16133-114">Taloudelliset lisäykset</span><span class="sxs-lookup"><span data-stu-id="16133-114">Financial increases</span></span>
<span data-ttu-id="16133-115">Kun maksuvastaanottotapahtuma kirjataan, määrää lisäävän tapahtumatietueen tila on **Ostettu**.</span><span class="sxs-lookup"><span data-stu-id="16133-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="16133-116">Seuraavat tapahtumat ovat kirjanpidollisia lisäyksiä:</span><span class="sxs-lookup"><span data-stu-id="16133-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="16133-117">Toimittajan lasku</span><span class="sxs-lookup"><span data-stu-id="16133-117">Vendor invoice</span></span>
-   <span data-ttu-id="16133-118">palautuksen myyntitilauslasku</span><span class="sxs-lookup"><span data-stu-id="16133-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="16133-119">tuotantotilauksen kustannuslaskenta</span><span class="sxs-lookup"><span data-stu-id="16133-119">Production order costing</span></span>
-   <span data-ttu-id="16133-120">Positiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto</span><span class="sxs-lookup"><span data-stu-id="16133-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="16133-121">Tapahtumat, jotka lisäävät määrää.</span><span class="sxs-lookup"><span data-stu-id="16133-121">Transactions that increase quantity</span></span>
<span data-ttu-id="16133-122">Määrää lisäävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla.</span><span class="sxs-lookup"><span data-stu-id="16133-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="16133-123">Laskettu juokseva keskimääräinen kustannushinta perustuu kirjanpidollisesti seurattavien varastodimensioiden tapahtumien kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="16133-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="16133-124">Lisätietoja juoksevasta keskimääräisestä kustannushinnasta: [Juokseva keskimääräinen kustannushinta](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="16133-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="16133-125">Tapahtumat, jotka vähentävät määrää.</span><span class="sxs-lookup"><span data-stu-id="16133-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="16133-126">Varastoon liittyvästä varastomallista riippumatta käytetään laskettua juoksevaa keskimääräistä kustannushintaa, kun määrää vähentävä tapahtuma kirjataan.</span><span class="sxs-lookup"><span data-stu-id="16133-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="16133-127">Määrää vähentävää tapahtumaa ei saa olla merkitty aiemmin toiseen tapahtumaan ennen kirjaamista.</span><span class="sxs-lookup"><span data-stu-id="16133-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="16133-128">Jos fyysinen käytettävissä oleva varasto muuttuu negatiiviseksi, käytetään varaston kustannusta, joka määritetään nimikkeelle **Nimike**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="16133-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="16133-129">Jos multisite-toiminnot on otettu käyttöön, tätä kustannusta käytetään toimipaikan varastokustannuksena, joka on määritetty sivustolle **Tilauksen oletusasetukset** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="16133-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="16133-130">Kirjanpidolliset varasto-otot verrattuina fyysiseen ottoon</span><span class="sxs-lookup"><span data-stu-id="16133-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="16133-131">Kun fyysinen varasto-ottotapahtuma kirjataan, tapahtumatietueentila on **Toimitettu**.</span><span class="sxs-lookup"><span data-stu-id="16133-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="16133-132">Seuraavat tapahtumat ovat fyysisiä varasto-ottoja:</span><span class="sxs-lookup"><span data-stu-id="16133-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="16133-133">tuotantotilauksen keräysluettelon kirjauskansio</span><span class="sxs-lookup"><span data-stu-id="16133-133">Production order picking list journal</span></span>
-   <span data-ttu-id="16133-134">myyntitilauksen pakkausluettelo</span><span class="sxs-lookup"><span data-stu-id="16133-134">Sales order packing slip</span></span>
-   <span data-ttu-id="16133-135">ostotilauksen pakkausluettelon palautus.</span><span class="sxs-lookup"><span data-stu-id="16133-135">Purchase order packing slip return</span></span>

<span data-ttu-id="16133-136">Kun kirjanpitotapahtuma kirjataan, tapahtumatietueen tila on **Myyty**.</span><span class="sxs-lookup"><span data-stu-id="16133-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="16133-137">Seuraavat tapahtumat ovat kirjanpidollisia varasto-ottoja:</span><span class="sxs-lookup"><span data-stu-id="16133-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="16133-138">Tuotantotilauksen lopetus</span><span class="sxs-lookup"><span data-stu-id="16133-138">Ending a production order</span></span>
-   <span data-ttu-id="16133-139">Myyntitilauslasku</span><span class="sxs-lookup"><span data-stu-id="16133-139">Sales order invoice</span></span>
-   <span data-ttu-id="16133-140">Toimittajalaskun palautus</span><span class="sxs-lookup"><span data-stu-id="16133-140">Vendor invoice return</span></span>
-   <span data-ttu-id="16133-141">Negatiivisen summan varastokirjauskansiot, kuten siirto, tulos, inventointi, tuoterakenne ja siirto</span><span class="sxs-lookup"><span data-stu-id="16133-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="16133-142">Määrää vähentävät tapahtumat kirjataan juoksevalla keskimääräisellä kustannushinnalla.</span><span class="sxs-lookup"><span data-stu-id="16133-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="16133-143">Tämän vuoksi varaston sulkemistoiminto vaaditaan varasto-ottotapahtumien täsmäyttämiseksi vastaanottotapahtumiksi jokaiseen nimikkeeseen määritetyn varastomallin perusteella.</span><span class="sxs-lookup"><span data-stu-id="16133-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>
