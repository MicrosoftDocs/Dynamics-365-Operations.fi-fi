---
title: Lähetyskontit
description: Tässä aiheessa kuvataan, miten kuljetuskontteja määritetään Aiheutunut kustannus -moduulia varten.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500955"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="fe7fa-103">Kuljetuskonttien määritys</span><span class="sxs-lookup"><span data-stu-id="fe7fa-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="fe7fa-104">Tässä aiheessa kuvataan, miten kuljetuskontteja määritetään **Aiheutunut kustannus** -moduulia varten.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="fe7fa-105">Kuljetuskonttityyppien määritys</span><span class="sxs-lookup"><span data-stu-id="fe7fa-105">Set up shipping container types</span></span>

<span data-ttu-id="fe7fa-106">Kuljetuskonttityypit määrittävät ne kuljetuskonttien tyypit, jotka ovat käytettävissä lähetyksissä ja matkoissa.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="fe7fa-107">Kuljetuskonttityyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Kuljetuskonttityypit**.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="fe7fa-108">Näin voit tarkastella, lisätä ja poistaa konttityyppien tietueita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="fe7fa-109">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fe7fa-110">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fe7fa-110">Field</span></span> | <span data-ttu-id="fe7fa-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-111">Description</span></span> |
|---|---|
| <span data-ttu-id="fe7fa-112">Lähetyskontin tyyppi</span><span class="sxs-lookup"><span data-stu-id="fe7fa-112">Shipping container type</span></span> | <span data-ttu-id="fe7fa-113">Syötä kuljetuskonttityypille yksilöllinen nimi/numero.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="fe7fa-114">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-114">Description</span></span> | <span data-ttu-id="fe7fa-115">Syötä kuljetuskonttityypille kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="fe7fa-116">Tilavuus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-116">Volume</span></span> | <span data-ttu-id="fe7fa-117">Syötä enimmäistilavuus, joka on sallittu tämäntyyppisille kuljetuskonteille.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fe7fa-118">Paino</span><span class="sxs-lookup"><span data-stu-id="fe7fa-118">Weight</span></span> | <span data-ttu-id="fe7fa-119">Syötä enimmäispaino, joka on sallittu tämäntyyppisille kuljetuskonteille.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="fe7fa-120">Palautettavissa</span><span class="sxs-lookup"><span data-stu-id="fe7fa-120">Returnable</span></span> | <span data-ttu-id="fe7fa-121">Määritä voidaanko tämäntyyppiset kuljetuskontit palauttaa toimittajalle, kun niitä on käytetty matkassa.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="fe7fa-122">Jos tämän asetuksen arvoksi määritetään *Kyllä*, tämäntyyppisten kuljetuskonttien lähtösatamaan palauttamiseen saatetaan soveltaa lisäkustannuksia.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="fe7fa-123">Kuljetuskonttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fe7fa-123">Set up shipping containers</span></span>

<span data-ttu-id="fe7fa-124">Kuljetuskonttien tietueilla yksilöidään kukin matkojen aikana käytettävä kontti.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="fe7fa-125">Kun luot matkan, voit valita sille tietyn kontin kaikkien täällä määrittämiesi kuljetuskonttitietueiden luettelosta.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="fe7fa-126">Tämä toiminto on erityisen hyödyllinen, jos yritys omistaa omat kuljetuskonttinsa.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="fe7fa-127">Vain kerran käytettäville kuljetuskonteille ei tarvitse syöttää kuljetuskonttinumeroita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="fe7fa-128">Sen sijaan voit lisätä kuljetuskontin numeron, kun luot matkan.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="fe7fa-129">Kuljetuskonttitietueita käytetään vain Aiheutunut kustannus -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="fe7fa-130">Ne eivät ole käytössä vakiomuotoisessa **Kuljetuksenhallinta**-moduulissa (TMS).</span><span class="sxs-lookup"><span data-stu-id="fe7fa-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="fe7fa-131">Kuljetuskontteja voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Kuljetuskontit**.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="fe7fa-132">Näin voit tarkastella, lisätä ja poistaa konttien tietueita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="fe7fa-133">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fe7fa-134">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fe7fa-134">Field</span></span> | <span data-ttu-id="fe7fa-135">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-135">Description</span></span> |
|---|---|
| <span data-ttu-id="fe7fa-136">Lähetyskontti</span><span class="sxs-lookup"><span data-stu-id="fe7fa-136">Shipping container</span></span> | <span data-ttu-id="fe7fa-137">Syötä kuljetuskontille yksilöllinen nimi/numero.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="fe7fa-138">Lähetyskontin tyyppi</span><span class="sxs-lookup"><span data-stu-id="fe7fa-138">Shipping container type</span></span> | <span data-ttu-id="fe7fa-139">Valitse kuljetuskontin tyyppi.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-139">Select the type of shipping container.</span></span> <span data-ttu-id="fe7fa-140">Lisätietoja on tämän aiheen aiemmassa kohdassa [Kuljetuskonttityyppien määrittäminen](#shipping-container-types).</span><span class="sxs-lookup"><span data-stu-id="fe7fa-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="fe7fa-141">Kuljetuskontin määrittäminen on valinnaista.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-141">The shipping container setup is optional.</span></span> <span data-ttu-id="fe7fa-142">Määritystä käytetään yleensä vain, jos yritys omistaa omat kuljetuskonttinsa tai käyttää usein uudelleen samoja kuljetuskontteja.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="fe7fa-143">Kuljetuskonttinumeroille ei lasketa tarkistusnumeroita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="fe7fa-144">Yksikkötyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="fe7fa-144">Set up unit types</span></span>

<span data-ttu-id="fe7fa-145">Yksikkötyypit tarjoavat lisää ryhmittelyjä ja yksilöintimenetelmiä kuljetuskonteille.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="fe7fa-146">Yksikkötyyppiä käytetään yleensä sen kuljetuskonttityypin yksilöimiseen, johon tuotteet on pakattu. Tällaisia ovat esimerkiksi kuormalavat tai tynnyrit.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="fe7fa-147">Voit valita yksikkötyypin, kun määrität kontin **Kaikki kuljetuskontit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fe7fa-148">Yksikkötyyppejä käytetään vain Aiheutunut kustannus -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="fe7fa-149">Ne eivät ole käytettävissä TMS:ssä.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-149">They aren't available in TMS.</span></span>

<span data-ttu-id="fe7fa-150">Yksikkötyyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Yksikkötyypit**.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="fe7fa-151">Näin voit tarkastella, lisätä ja poistaa yksikkötyyppien tietueita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="fe7fa-152">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fe7fa-153">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fe7fa-153">Field</span></span> | <span data-ttu-id="fe7fa-154">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-154">Description</span></span> |
|---|---|
| <span data-ttu-id="fe7fa-155">Yksikkötyyppi</span><span class="sxs-lookup"><span data-stu-id="fe7fa-155">Unit type</span></span> | <span data-ttu-id="fe7fa-156">Syötä yksikkötyypille yksilöllinen nimi/numero.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="fe7fa-157">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-157">Description</span></span> | <span data-ttu-id="fe7fa-158">Anna yksikkötyypin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="fe7fa-159">Jäähdytystyyppien määritys</span><span class="sxs-lookup"><span data-stu-id="fe7fa-159">Set up refrigeration types</span></span>

<span data-ttu-id="fe7fa-160">Jäähdytystyyppejä käytetään lisäryhmittelyjen ja -yksilöintimenetelmien luomiseen kuljetuskonteille (yleensä jäähdytetyille kuljetuskonteille).</span><span class="sxs-lookup"><span data-stu-id="fe7fa-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="fe7fa-161">Voit valita jäähdytystyypin, kun määrität kontin **Kaikki kuljetuskontit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="fe7fa-162">Jäähdytystyyppejä voit käsitellä valitsemalla **Aiheutunut kustannus \> Konttien määritys \> Jäähdytystyypit**.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="fe7fa-163">Näin voit tarkastella, lisätä ja poistaa jäähdytystyyppien tietueita.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="fe7fa-164">Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="fe7fa-165">Kenttä</span><span class="sxs-lookup"><span data-stu-id="fe7fa-165">Field</span></span> | <span data-ttu-id="fe7fa-166">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-166">Description</span></span> |
|---|---|
| <span data-ttu-id="fe7fa-167">Kylmäsäilytystyyppi</span><span class="sxs-lookup"><span data-stu-id="fe7fa-167">Refrigeration type</span></span> | <span data-ttu-id="fe7fa-168">Syötä jäähdytystyypille yksilöllinen nimi/numero.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="fe7fa-169">kuvaus</span><span class="sxs-lookup"><span data-stu-id="fe7fa-169">Description</span></span> | <span data-ttu-id="fe7fa-170">Kirjoita jäähdytystyypin lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="fe7fa-170">Enter a description of the refrigeration type.</span></span> |