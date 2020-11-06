---
title: Saman erän varaaminen myyntitilausta varten
description: Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce750745d6f094a296b43827568ee1745179de2d
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017273"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="04e14-103">Saman erän varaaminen myyntitilausta varten</span><span class="sxs-lookup"><span data-stu-id="04e14-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04e14-104">Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.</span><span class="sxs-lookup"><span data-stu-id="04e14-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="04e14-105">Saman erän varaamisen avulla voit varata myyntitilausriville varaston yhden varastoerän mukaan.</span><span class="sxs-lookup"><span data-stu-id="04e14-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="04e14-106">Tapettia tilaava asiakas voi esimerkiksi pyytää koko tilauksen samasta erästä saadakseen keskenään samanlaisia tapettirullia.</span><span class="sxs-lookup"><span data-stu-id="04e14-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="04e14-107">Voit määrittää tuotteen käyttämään saman erän varausta ottamalla käyttöön seuraavat asetukset tuotteeseen liitetyssä nimikemalli-, seurantadimensio- ja varastodimensioryhmässä:</span><span class="sxs-lookup"><span data-stu-id="04e14-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="04e14-108">**Nimikemalliryhmät** – Nimikemalliryhmässä on valittava varastokäytäntöjen **Varaus** -kenttäryhmän **Saman erän valinta** - ja **Konsolidoi tarve** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="04e14-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="04e14-109">**Seurantadimensioryhmät** – Seurantadimensioryhmässä on valittava eränumeron **Kattavuussuunnitelma dimension mukaan** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="04e14-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="04e14-110">**Varastodimensioryhmät** – Varastodimensioryhmässä on valittava **Toimipaikka** - ja **Varasto** -kohdassa **Kattavuussuunnitelma dimension mukaan** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="04e14-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="04e14-111">Kun varaat myyntitilausrivin tuotteelle varaston, jolla on määritetty saman erän valinta, järjestelmä yrittää varata tilatun määrän yhdestä varastoerästä.</span><span class="sxs-lookup"><span data-stu-id="04e14-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="04e14-112">Myös muut erämääritteen vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="04e14-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="04e14-113">Jos määrää ei voida täyttää yhdestä erästä, **Saman erävarauksen ristiriita** -sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="04e14-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="04e14-114">Sivulla kerrotaan ongelmista ja toimenpiteistä, joiden avulla varauksen tekemistä voi jatkaa.</span><span class="sxs-lookup"><span data-stu-id="04e14-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="04e14-115">Seuraavat tilanteet saattavat estää erän varaamisen:</span><span class="sxs-lookup"><span data-stu-id="04e14-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="04e14-116">Myynnin erän käsittelykoodin **Estä varaaminen** -kohdan arvoksi on merkitty **Estetty**.</span><span class="sxs-lookup"><span data-stu-id="04e14-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="04e14-117">Erä on vanhentunut vanhentumispäivän ja mahdollisten käytettävissä olevien asiakkaan myyntipäivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="04e14-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="04e14-118">Nimikkeen varausta voidaan silti harkita, jos kyseessä on päivämäärän mukaan ohjatun FEFO-nimikkeen nimikemalliryhmä ja parasta ennen -päivä on valittu keräysehdoksi.</span><span class="sxs-lookup"><span data-stu-id="04e14-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="04e14-119">Erällä ei ole jäljellä riittävästi varastointiaikaa vanhentumispäivän ja parasta ennen -päivän sekä mahdollisten asiakkaan myyntipäivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="04e14-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="04e14-120">Jos nimike liittyy varastodimensioryhmään, jossa on otettu käyttöön **Käytä varastonhallintaprosesseja** , voit varata tiettyjä eränumeroita käyttämällä varaushierarkiaa, jossa on sijaintidimension yläpuolella määritetty eränumeron varastodimensio.</span><span class="sxs-lookup"><span data-stu-id="04e14-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="04e14-121">Myynti- ja siirtotilausrivien **Erän varaus** -sivulla voit myös valita ja varata useita rivejä käytettävissä olevien eränumeroiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="04e14-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="04e14-122">Katso lisätietoja siitä, mitä tehdä, jos käytät varaushierarkiaa, jolla on varastopaikan alapuolella eränumerodimensio kohdasta [Joustava varastotason dimension varauskäytäntö](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="04e14-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
