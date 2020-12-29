---
title: Varastonhallinnan varausten vianmääritys
description: Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645116"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="2bc98-103">Varastonhallinnan varausten vianmääritys</span><span class="sxs-lookup"><span data-stu-id="2bc98-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bc98-104">Tässä aiheessa käsitellään yleisiä ongelmia, joita voi esiintyä, kun varastovarauksia käytetään Microsoft Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="2bc98-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="2bc98-105">Seuraava virhesanoma avautuu: Varauksia ei voi poistaa, koska on luotu töitä, jotka ovat riippuvaisia niistä.</span><span class="sxs-lookup"><span data-stu-id="2bc98-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bc98-106">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="2bc98-106">Issue description</span></span>

<span data-ttu-id="2bc98-107">Myyntirivin varastoin varausta ei voi poistaa, koska rivillä on avoin työ.</span><span class="sxs-lookup"><span data-stu-id="2bc98-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bc98-108">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="2bc98-108">Issue resolution</span></span>

<span data-ttu-id="2bc98-109">Selvitä, onko kyse avoimesta pakkausryhmän työstä ja siirrä nimike pakkausasemalta toiseen sijaintiin (kuten *lastausovelle*).</span><span class="sxs-lookup"><span data-stu-id="2bc98-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="2bc98-110">Selvitä **Työn luontihistorian loki**- ja **Työn tiedot** -sivuilta, mikä fyysisesti varaa varastoa, ja vapauta varaus sitten suorittamalla tai poistamalla työ.</span><span class="sxs-lookup"><span data-stu-id="2bc98-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="2bc98-111">Näytössä on seuraava virhesanoma: Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2....</span><span class="sxs-lookup"><span data-stu-id="2bc98-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bc98-112">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="2bc98-112">Issue description</span></span>

<span data-ttu-id="2bc98-113">Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi.</span><span class="sxs-lookup"><span data-stu-id="2bc98-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="2bc98-114">Virhesanoman koko teksti:</span><span class="sxs-lookup"><span data-stu-id="2bc98-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="2bc98-115">Varastomäärää -%1 ei voi päivittää, sillä varastotapahtumia on liian vähän nimikkeelle %2 dimensioilla Koko=%3, Väri=%4, Lisäykset=%5, Toimipaikka=%6, Varasto=%7, Varasto=%8, Varaston tila=Käytettävissä, Rekisterikilpi=%9, Eränumero=%10 viitetunnusta %11 varten erätunnuksessa %12.</span><span class="sxs-lookup"><span data-stu-id="2bc98-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bc98-116">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="2bc98-116">Issue resolution</span></span>

<span data-ttu-id="2bc98-117">Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="2bc98-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="2bc98-118">Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.</span><span class="sxs-lookup"><span data-stu-id="2bc98-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="2bc98-119">Seuraava virhesanoma avautuu: Fyysinen varastosaldo...ei voi varata, koska varastossa on vain 0,00 saatavana.</span><span class="sxs-lookup"><span data-stu-id="2bc98-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bc98-120">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="2bc98-120">Issue description</span></span>

<span data-ttu-id="2bc98-121">Tämä ongelma voi esiintyä, jos järjestelmä ei voi päivittää varastomäärää, koska varastotapahtumia, joilla on määritetyt dimensiot, ei ole tarpeeksi.</span><span class="sxs-lookup"><span data-stu-id="2bc98-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="2bc98-122">Virhesanoman koko teksti:</span><span class="sxs-lookup"><span data-stu-id="2bc98-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="2bc98-123">Fyysinen varastosaldo Toimipaikka=%1, Varasto=%2, Varaston tila=käytettävissä, Eränumero=%3, Omistaja=%4: %5 ei voi varata, koska varastossa on vain 0,00 saatavana.</span><span class="sxs-lookup"><span data-stu-id="2bc98-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bc98-124">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="2bc98-124">Issue resolution</span></span>

<span data-ttu-id="2bc98-125">Tämä ongelman syy on todennäköisesti avoin työ.</span><span class="sxs-lookup"><span data-stu-id="2bc98-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="2bc98-126">Voit joko suorittaa työn tai vastaanottaa ilman työn luontia.</span><span class="sxs-lookup"><span data-stu-id="2bc98-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="2bc98-127">Varmista, että määrää ei ole varattu fyysisesti millään varastotapahtumalla.</span><span class="sxs-lookup"><span data-stu-id="2bc98-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="2bc98-128">Nämä tapahtumat voivat esimerkiksi avata laatutilauksia, varastoestotilauksia tai toimitustilauksia.</span><span class="sxs-lookup"><span data-stu-id="2bc98-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="2bc98-129">Seuraava virhesanoma avautuu: Jotta kuormituksen rivit voidaan määrittää aaltoon, niiden on määritettävä dimensiot sijainnin yläpuolelle.</span><span class="sxs-lookup"><span data-stu-id="2bc98-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="2bc98-130">Voit määrittää nämä dimensiot varaamalla kuormituksen rivin ja luomalla sen uudelleen.</span><span class="sxs-lookup"><span data-stu-id="2bc98-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="2bc98-131">Ongelman kuvaus</span><span class="sxs-lookup"><span data-stu-id="2bc98-131">Issue description</span></span>

<span data-ttu-id="2bc98-132">Jos käytät nimikettä, jossa käytetään erän yläpuolella olevaa varaushierarkiaa (eli **Eränumero**-dimensio on sijoitettu **Sijainti**-dimension *yläpuolelle*), osittaisen määrän **Kuormasuunnittelun työtila** -sivun **Vapauta varastoon** -komento ei toimi.</span><span class="sxs-lookup"><span data-stu-id="2bc98-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="2bc98-133">Sait tämän virhesanoma eikä osittaiselle määrälle luoda yhtään työtä.</span><span class="sxs-lookup"><span data-stu-id="2bc98-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="2bc98-134">Jos käytät kuitenkin nimikettä, jossa käytetään erän alapuolella olevaa varaushierarkiaa (eli **Eränumero**-dimensio on sijoitettu **Sijainti**-dimension *alapuolelle*), voit vapauttaa kuorman osittaisen määrän **Kuormasuunnittelun työtila** -sivulta.</span><span class="sxs-lookup"><span data-stu-id="2bc98-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2bc98-135">Ongelman ratkaisu</span><span class="sxs-lookup"><span data-stu-id="2bc98-135">Issue resolution</span></span>

<span data-ttu-id="2bc98-136">Tämä on suunniteltu ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="2bc98-136">This behavior is by design.</span></span> <span data-ttu-id="2bc98-137">Jos sijoitat dimension **Sijainti**-dimension yläpuolelle varaushierarkiassa, se on määritettävä ennen vapautusta varastoon.</span><span class="sxs-lookup"><span data-stu-id="2bc98-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="2bc98-138">Microsoft on arvioinut tämän ongelman ja määrittänyt sen toimintorajoitukseksi, joka koskee vapautuksia varastoon kuormasuunnittelun työtilasta.</span><span class="sxs-lookup"><span data-stu-id="2bc98-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="2bc98-139">Osittaisia määriä ei voi vapauttaa, jos vähintään yhtä **Sijainti**-dimension yläpuolella olevaa dimensiota ei ole määritetty.</span><span class="sxs-lookup"><span data-stu-id="2bc98-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="2bc98-140">Lisätietoja on kohdassa [Joustava varastotason dimensioiden varauskäytäntö](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="2bc98-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
