---
title: Saman erän varaaminen myyntitilausta varten
description: Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 067dd6d3c337378a610ee1fcf6a7812716813bab
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251727"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="28499-103">Saman erän varaaminen myyntitilausta varten</span><span class="sxs-lookup"><span data-stu-id="28499-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28499-104">Tässä artikkelissa kerrotaan, miten tuote määritetään, kun varastovaraus sallitaan yhden varastoerän mukaan.</span><span class="sxs-lookup"><span data-stu-id="28499-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="28499-105">Saman erän varaamisen avulla voit varata myyntitilausriville varaston yhden varastoerän mukaan.</span><span class="sxs-lookup"><span data-stu-id="28499-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="28499-106">Tapettia tilaava asiakas voi esimerkiksi pyytää koko tilauksen samasta erästä saadakseen keskenään samanlaisia tapettirullia.</span><span class="sxs-lookup"><span data-stu-id="28499-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="28499-107">Voit määrittää tuotteen käyttämään saman erän varausta ottamalla käyttöön seuraavat asetukset tuotteeseen liitetyssä nimikemalli-, seurantadimensio- ja varastodimensioryhmässä:</span><span class="sxs-lookup"><span data-stu-id="28499-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="28499-108">**Nimikemalliryhmät** – Nimikemalliryhmässä on valittava varastokäytäntöjen **Varaus**-kenttäryhmän **Saman erän valinta**- ja **Konsolidoi tarve** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="28499-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="28499-109">**Seurantadimensioryhmät** – Seurantadimensioryhmässä on valittava eränumeron **Kattavuussuunnitelma dimension mukaan** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="28499-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="28499-110">**Varastodimensioryhmät** – Varastodimensioryhmässä on valittava **Toimipaikka**- ja **Varasto**-kohdassa **Kattavuussuunnitelma dimension mukaan** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="28499-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="28499-111">Kun varaat myyntitilausrivin tuotteelle varaston, jolla on määritetty saman erän valinta, järjestelmä yrittää varata tilatun määrän yhdestä varastoerästä.</span><span class="sxs-lookup"><span data-stu-id="28499-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="28499-112">Myös muut erämääritteen vaatimukset otetaan huomioon.</span><span class="sxs-lookup"><span data-stu-id="28499-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="28499-113">Jos määrää ei voida täyttää yhdestä erästä, **Saman erävarauksen ristiriita** -sivu aukeaa.</span><span class="sxs-lookup"><span data-stu-id="28499-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="28499-114">Sivulla kerrotaan ongelmista ja toimenpiteistä, joiden avulla varauksen tekemistä voi jatkaa.</span><span class="sxs-lookup"><span data-stu-id="28499-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="28499-115">Seuraavat tilanteet saattavat estää erän varaamisen:</span><span class="sxs-lookup"><span data-stu-id="28499-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="28499-116">Myynnin erän käsittelykoodin **Estä varaaminen** -kohdan arvoksi on merkitty **Estetty**.</span><span class="sxs-lookup"><span data-stu-id="28499-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="28499-117">Erä on vanhentunut vanhentumispäivän ja mahdollisten käytettävissä olevien asiakkaan myyntipäivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="28499-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="28499-118">Nimikkeen varausta voidaan silti harkita, jos kyseessä on päivämäärän mukaan ohjatun FEFO-nimikkeen nimikemalliryhmä ja parasta ennen -päivä on valittu keräysehdoksi.</span><span class="sxs-lookup"><span data-stu-id="28499-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="28499-119">Erällä ei ole jäljellä riittävästi varastointiaikaa vanhentumispäivän ja parasta ennen -päivän sekä mahdollisten asiakkaan myyntipäivien perusteella.</span><span class="sxs-lookup"><span data-stu-id="28499-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>




