---
title: Kuormituskapasiteetin ajoittaminen
description: Tässä ohjeaiheessa käsitellään, miten voit määrittää ja ajoittaa kuormituskapasiteetin varaston työntekijöille tai koko varastolle.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8db243949b2aeee0a8263276234d439652905449
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965574"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="1bf02-103">Kuormituskapasiteetin ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="1bf02-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="1bf02-104">Voit ajoittaa varastojen kuormituskapasiteettia ja myös projektin nykyistä ja tulevaa kuormitusta yksittäisten varastojen työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="1bf02-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="1bf02-105">Voit suunnitella kuormituksen koko varastolle tai erikseen tuleville ja lähteville työmäärille.</span><span class="sxs-lookup"><span data-stu-id="1bf02-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="1bf02-106">Kyeisten varastojen pääajoitustiedot on oltava saatavilla lähtevän kuormituksen suunnittelemiseksi.</span><span class="sxs-lookup"><span data-stu-id="1bf02-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="1bf02-107">Lisätietoja on kohdassa [Pääsuunnitelmien yleiskatsaus](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="1bf02-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="1bf02-108">Varaston kuormituksen ajoittaminen ja tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="1bf02-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="1bf02-109">Varaston kuormituksen ajoittamiseksi on luotava kuormitusasetus vähintään yhdelle varastolle, ja liitettävä kuormitusasetus pääsuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="1bf02-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="1bf02-110">Kuormituskapasiteettiasetuksessa voit määrittää saapuvien ja lähtevien tapahtumien kuormalavoihin liittyvät rajoitteet ja painon tai tilavuuden.</span><span class="sxs-lookup"><span data-stu-id="1bf02-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="1bf02-111">Voit myös luoda useamman kuin yhden asetuksen jokaiselle varastolle ja liittää asetuksen yksittäisiin pääsuunnitelmiin.</span><span class="sxs-lookup"><span data-stu-id="1bf02-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="1bf02-112">Voi tehdä tämän esimerkiksi työvoiman kausittaisten muutosten vuoksi.</span><span class="sxs-lookup"><span data-stu-id="1bf02-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="1bf02-113">Jos varaston työntekijät työskentelevät sekä saapuvien että lähtevien kuormien tapahtumien kanssa, voit määrittää varaston kapasiteettiasetukset kuormituksen suunnittelemiseksi yhdistetyssä näkymässä.</span><span class="sxs-lookup"><span data-stu-id="1bf02-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="1bf02-114">Jotta voit ajoittaa ja tarkastella varastojen kuormituksia, sinun on suoritettava seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="1bf02-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="1bf02-115">Luo kuormituskapasiteettiasetus ja määritä kuormituskapasiteetin rajoitukset vähintään yhdelle varastolle.</span><span class="sxs-lookup"><span data-stu-id="1bf02-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="1bf02-116">Liitä kuormituskapasiteettiasetus pääsuunnitelmaan kuormitusennusteiden luomiseksi ja määrittääksesi, kuinka kauan kyseiset suunnitelmat ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="1bf02-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="1bf02-117">Kuormituskapasiteettiasetuksen luonti varastolle</span><span class="sxs-lookup"><span data-stu-id="1bf02-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="1bf02-118">Valitse **Varastonhallinta** \> **Asetukset** \> **Varastonhallinta** \> **Kuormituskapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="1bf02-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="1bf02-119">Valitse toimintoruudussa **Uusi** luodaksesi kuormituskapasiteetin asetukset.</span><span class="sxs-lookup"><span data-stu-id="1bf02-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="1bf02-120">Valitse **Varastot**-pikavälilehdessä **Uusi** ja kirjoita sitten riville arvot liittääksesi varaston kuormituskapasiteettiasetuksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="1bf02-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="1bf02-121">Valitse **Yhdistetty saapuva ja lähtevä kuormitus** -valintaruutu, jos **Kuormituskapasiteetti**-raportin tulee näyttää saapuvien ja lähtevien tapahtumien kokonaiskuormitus yhdessä näkymässä.</span><span class="sxs-lookup"><span data-stu-id="1bf02-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="1bf02-122">Valitse **Tapahtumatyypit**-pikavälilehdellä saapuvat ja lähtevät tapahtumatyypit, joihin kuormitusrajat kohdistuvat.</span><span class="sxs-lookup"><span data-stu-id="1bf02-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1bf02-123">Sinun on valittava vähintään yksi tapahtumatyyppi sekä saapuville että lähteville kuormituksille.</span><span class="sxs-lookup"><span data-stu-id="1bf02-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="1bf02-124">Määritä paino- tai tilavuusrajat</span><span class="sxs-lookup"><span data-stu-id="1bf02-124">Define limits for volume or weight</span></span>

<span data-ttu-id="1bf02-125">Voit määrittää rajoitukset tilavuudelle tai painolle riippuen siitä, mitkä rajoitukset ovat varaston työntekijöille olennaisia.</span><span class="sxs-lookup"><span data-stu-id="1bf02-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="1bf02-126">Määrittämäsi rajoitukset sisällytetään kuormituskapasiteetin suunnitelmaan, jota voit tarkastella **Kuormituskapasiteetti**-raportissa.</span><span class="sxs-lookup"><span data-stu-id="1bf02-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="1bf02-127">Jotta nimikkeiden tilavuuteen ja painoon liittyviä tietoja voidaan laskea, kaikkien tuotteiden osalta on määritettävä yhden varastonimikkeen tilavuus ja paino.</span><span class="sxs-lookup"><span data-stu-id="1bf02-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="1bf02-128">Tarvittavat kentät ovat käytettävissä seuraavissa kenttäryhmissä **Varaston hallinta**- pikavälilehdessä **Vapautetun tuotteen tiedot** -sivulla:</span><span class="sxs-lookup"><span data-stu-id="1bf02-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="1bf02-129">Käsittely</span><span class="sxs-lookup"><span data-stu-id="1bf02-129">Handling</span></span>
- <span data-ttu-id="1bf02-130">Fyysiset mitat</span><span class="sxs-lookup"><span data-stu-id="1bf02-130">Physical dimensions</span></span>
- <span data-ttu-id="1bf02-131">Painomitat</span><span class="sxs-lookup"><span data-stu-id="1bf02-131">Weight measurements</span></span>

<span data-ttu-id="1bf02-132">Jos näitä tietoja ei ole määritetty oikein, saat viestin luodessasi **Kuormituskapasiteetti**-raportin.</span><span class="sxs-lookup"><span data-stu-id="1bf02-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="1bf02-133">Raportissa saat tarkempaa tietoa tunnistaaksesi tulevan kuormituksen suunnittelusta puuttuvat tiedot.</span><span class="sxs-lookup"><span data-stu-id="1bf02-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="1bf02-134">Kuormituskapasiteettiasetuksen liittäminen pääsuunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="1bf02-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="1bf02-135">Valitse **Varastonhallinta** \> **Kausittainen** \> **Ajoita kuormitus**.</span><span class="sxs-lookup"><span data-stu-id="1bf02-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="1bf02-136">Valitse **Pääsuunnitelma**-kentässä kuormitusarvioille käytettävä pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="1bf02-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="1bf02-137">Määritä **Päivien määrä** -kentässä päivien lukumäärä, jonka kuormitusarvio kattaa.</span><span class="sxs-lookup"><span data-stu-id="1bf02-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="1bf02-138">Valitse **Kuormitus**-kentässä pääsuunnitelmaan liitettävä kuormitusasetus.</span><span class="sxs-lookup"><span data-stu-id="1bf02-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="1bf02-139">Kuormituskapasiteetin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="1bf02-139">View workload capacity</span></span>

1. <span data-ttu-id="1bf02-140">Valitse **Varastonhallinta** \> **Kyselyt ja raportit** \> **Fyysiset varastoraportit** \> **Kuormituskapasiteetti**.</span><span class="sxs-lookup"><span data-stu-id="1bf02-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="1bf02-141">Määritä **Sarakkeiden määrä** -kentässä raportissa näytettävien sarakkeiden määrä.</span><span class="sxs-lookup"><span data-stu-id="1bf02-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="1bf02-142">Valitse **Tilaustyyppi**-kentässä **Suunniteltu ja vahvistettu**, **Suunniteltu** tai **Vahvistettu** osoittaaksesi raportissa näytettävät tilaustyypit.</span><span class="sxs-lookup"><span data-stu-id="1bf02-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="1bf02-143">Valitse **Kuormatyyppi**-kentässä kuormatyyppi, joka määrittää arvioidaanko kuormituskapasiteetti tilavuuden vai painon mukaan.</span><span class="sxs-lookup"><span data-stu-id="1bf02-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="1bf02-144">Valitse kuormituskapasiteettiasetus **Kuormituskapasiteetti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="1bf02-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
