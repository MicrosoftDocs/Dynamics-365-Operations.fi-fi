---
title: Ajoita kuormituksen käyttöaste
description: Tässä ohjeaiheessa kerrotaan, miten voit määrittää ja ajoittaa varaston kuormituksen.
author: MarkusFogelberg
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f4d259fd6c27ac96475c49c431e347ca0c03a9e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817314"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="4a563-103">Ajoita kuormituksen käyttöaste</span><span class="sxs-lookup"><span data-stu-id="4a563-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4a563-104">Voit ajoittaa valittujen sijaintityyppien kuormituksen sekä arvioida nykyistä ja tulevaa kuormitusta.</span><span class="sxs-lookup"><span data-stu-id="4a563-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="4a563-105">Voit arvioida yhden tai usean toimipaikan kuormituksen, varaston tai vyöhykkeen kuormitusyksiköt tai vyöhykkeen ja varaston yhdistetyn kuormituksen.</span><span class="sxs-lookup"><span data-stu-id="4a563-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="4a563-106">Varaston tai toimipaikan kuormituksen ajoittaminen ja tarkastelu</span><span class="sxs-lookup"><span data-stu-id="4a563-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="4a563-107">Ajoittamalla toimipaikkojen, varastojen tai vyöhykkeiden kuormituksen voit luoda tilan käytön asetukset ja liittää ne pääsuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="4a563-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="4a563-108">Tilan käytön asetuksissa voit käyttää sijaintityyppejä, kuten **Bulkkisijainti** ja **Keräilysijainti**, jotka määrittävät, miten tilan käyttö suunnitellaan.</span><span class="sxs-lookup"><span data-stu-id="4a563-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="4a563-109">Voit myös määrittää varastokuormituksen tilan, kuten **Vyöhyke**.</span><span class="sxs-lookup"><span data-stu-id="4a563-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="4a563-110">Tilan tulevan käyttöasteen projektio perustuu tietoihin, jotka on laskettu liitetyn pääsuunnitelman perusteella.</span><span class="sxs-lookup"><span data-stu-id="4a563-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="4a563-111">Pääsuunnitelmat ennakoivat tuotannon ja toimintojen saapuvien ja lähtevien tilausten resurssisuunnittelua.</span><span class="sxs-lookup"><span data-stu-id="4a563-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="4a563-112">Käytettävissä olevan tilan projektio perustuu tilan käytön asetuksen ja valitun pääsuunnitelman väliseen suhteeseen.</span><span class="sxs-lookup"><span data-stu-id="4a563-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="4a563-113">Käyttämällä tilan käytön asetuksissa kuormitustilaa voit määrittää, arvioidaanko kuormitus kullekin varastolle tai vyöhykkeelle vai sisältävätkö projektiot tietoja jokaisesta varastosta tai vyöhykkeestä vai tietoja sekä varastoista että vyöhykkeistä.</span><span class="sxs-lookup"><span data-stu-id="4a563-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="4a563-114">Voit myös määrittää, jätetäänkö estetyt sijainnit pois kuormituksen käyttölaskelmista.</span><span class="sxs-lookup"><span data-stu-id="4a563-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="4a563-115">Voit suunnitella tilan käyttöä luomalla **Varastokuormituksen käyttöaste** -raportin.</span><span class="sxs-lookup"><span data-stu-id="4a563-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="4a563-116">Kun luot tämän raportin, voit määrittää, arvioidaanko kunkin toimipaikan kuormituksen käyttöaste erikseen vai yhdessä vai arvioidaanko se valitun kuormitusyksikön, kuten vyöhykkeen tai varaston, mukaan.</span><span class="sxs-lookup"><span data-stu-id="4a563-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="4a563-117">Varaston tilan käytön asetusten luominen</span><span class="sxs-lookup"><span data-stu-id="4a563-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="4a563-118">Valitse **Varastonhallinta** \> **Asetukset** \> **Varaston valvonta** \> **Tilan käyttö**.</span><span class="sxs-lookup"><span data-stu-id="4a563-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="4a563-119">Luo tilan käytön asetukset valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="4a563-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="4a563-120">Määritä uuden asetuksen tunnus ja nimi.</span><span class="sxs-lookup"><span data-stu-id="4a563-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="4a563-121">Valitse **Varaston kuormitustila** -kentässä, näytetäänkö tilan käyttöaste varaston, vyöhykkeen vai varaston ja vyöhykkeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="4a563-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="4a563-122">Määritä **Jätä estetyt sijainnit pois** -asetukseksi **Kyllä** jättääksesi estetyt varastosijainnit pois käytettävissä olevan tilan laskennasta.</span><span class="sxs-lookup"><span data-stu-id="4a563-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="4a563-123">Voit estää saapuvien ja lähtevien varastosijainnin määrittämällä sijainnin eston syyn **Syöttö estetty**- tai **Tuloste estetty** -kentissä **Muut**-välilehdellä **Varastosijainnit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="4a563-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="4a563-124">Valitse **Sijainnin tyyppi** -pikavälilehdessä tilan käyttöastetta laskettaessa käytettävät sijaintityypit.</span><span class="sxs-lookup"><span data-stu-id="4a563-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="4a563-125">Sinun on valittava projektiolle vähintään yksi sijaintityyppi.</span><span class="sxs-lookup"><span data-stu-id="4a563-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="4a563-126">Tilan käytön asetuksen liittäminen pääsuunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="4a563-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="4a563-127">Valitse **Varastonhallinta** \> **Kausittaiset tehtävät** \> **Ajoita kuormituksen käyttöaste**.</span><span class="sxs-lookup"><span data-stu-id="4a563-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="4a563-128">Valitse **Pääsuunnitelma**-kentässä pääsuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="4a563-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="4a563-129">Määritä **Päivien määrä** -kentässä, kuinka monta päivää nykyisten ja tulevien kuormitusten projektioon sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="4a563-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="4a563-130">Valitse **Tilan käyttö** -kentässä nykyisten ja tulevien kuormitusten projektiossa käytettävät tilan käytön asetukset.</span><span class="sxs-lookup"><span data-stu-id="4a563-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="4a563-131">Kuormituksen käyttöasteprojektion määrittäminen ja tietojen näyttäminen</span><span class="sxs-lookup"><span data-stu-id="4a563-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="4a563-132">Valitse **Varastonhallinta** \> **Kyselyt ja raportit** \> **Fyysiset varastoraportit** \> **Varastokuormituksen käyttöaste**.</span><span class="sxs-lookup"><span data-stu-id="4a563-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="4a563-133">Valitse **Näyttöperuste**-kentässä tilan käyttöasteen projektio:</span><span class="sxs-lookup"><span data-stu-id="4a563-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="4a563-134">**Toimipaikka** – Arvioi kunkin toimipaikan tilan käyttöaste.</span><span class="sxs-lookup"><span data-stu-id="4a563-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="4a563-135">Tämä on kätevä projektio esimerkiksi silloin, kun haluat tarkastella toimipaikan kaikkia varastoja ja tasoittaa varastojen välistä käyttöastetta.</span><span class="sxs-lookup"><span data-stu-id="4a563-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="4a563-136">**Kuormitusyksikkö** – Arvioi vyöhykkeiden tai varastojen käyttöaste.</span><span class="sxs-lookup"><span data-stu-id="4a563-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="4a563-137">Käytettävissä oleva tila arvioidaan niiden arvojen mukaan, jotka olet valinnut **Varaston kuormitustila** -kentässä **Tilan käyttö** -sivulla tilan käytön asetusten luonnin yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="4a563-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="4a563-138">Noudata yhtä näitä vaiheita sen arvo mukaan, jonka valitsit edellisessä vaiheessa:</span><span class="sxs-lookup"><span data-stu-id="4a563-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="4a563-139">Jos valitsit **Toimipaikka**-arvon **Näyttöperuste**-kentässä, **Toimipaikka**-kenttä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4a563-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="4a563-140">Valitse vähintään yksi projektioon sisällytettävä toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="4a563-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="4a563-141">Jos valitsit **Kuormitusyksikkö**-arvon **Näyttöperuste**-kentässä, **Kuormitusyksikkö**-kenttä on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="4a563-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="4a563-142">Valitse kuormitusyksikkö.</span><span class="sxs-lookup"><span data-stu-id="4a563-142">Select the load unit.</span></span>

4. <span data-ttu-id="4a563-143">Määrittämällä **Kuormitustyyppi**-kentässä **Tilavuus** tai **Paino** osoitat, mille varastotoimintayksikölle tilaa arvioidaan.</span><span class="sxs-lookup"><span data-stu-id="4a563-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="4a563-144">Valitse **Tilan käytön asetukset** -kentässä ne tilan käytön asetukset, joihin projektio perustuu.</span><span class="sxs-lookup"><span data-stu-id="4a563-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]