---
title: "Kontin painon ja tilavuuden sisällyttäminen kuormaan"
description: "Tässä aiheessa käsitellään kuormaan konttipainon- ja tilavuuden lisäämistoiminnon määrittämistä ja käyttöä."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: adbaa379889d373d597b2f6882b78f82bd71ae57
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---

# <a name="include-container-weight-and-volume-on-load"></a><span data-ttu-id="e70e5-103">Kontin painon ja tilavuuden sisällyttäminen kuormaan</span><span class="sxs-lookup"><span data-stu-id="e70e5-103">Include container weight and volume on load</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e70e5-104">Toiminnallisuus, jolla lisätään konttipaino- ja tilavuus kuormaan antaa selkeän kuvan kuormaan lastattavien konttien ja nimikkeiden kokonaispainosta- ja tilavuudesta.</span><span class="sxs-lookup"><span data-stu-id="e70e5-104">The functionality for including the container weight and volume on a load gives a clear representation of the total weight and volume of containers and items that are going on a load.</span></span>

<span data-ttu-id="e70e5-105">Kuorma voi sisältää yhden tai useampia lähetyksiä, ja nämä lähetykset sisältävät erilaisia nimikkeitä, jotka voivat kuulua yhteen tai useampaan myyntitilaukseen.</span><span class="sxs-lookup"><span data-stu-id="e70e5-105">A load contains a single shipment or multiple shipments, and these shipments contain distinct items that belong to a single sales order or multiple sales orders.</span></span> <span data-ttu-id="e70e5-106">Nimikkeet on tallennettu konttiin, ja kontit kuormataan kuormaan.</span><span class="sxs-lookup"><span data-stu-id="e70e5-106">The items are stored inside a container, and containers are loaded on a load.</span></span> <span data-ttu-id="e70e5-107">Kuormassa voi olla myös kontin ulkopuolisia nimikkeitä.</span><span class="sxs-lookup"><span data-stu-id="e70e5-107">Items that are outside a container can also be part of a load.</span></span> <span data-ttu-id="e70e5-108">Järjestelmä laskee näiden ehtojen perusteella arvon kuorman painolle ja tilavuudelle ottamalla huomioon sekä konttien että nimikkeiden painot.</span><span class="sxs-lookup"><span data-stu-id="e70e5-108">Based on these conditions, the system calculates values for the weight and volume on the load by considering the weight and volume of both containers and items.</span></span>

<span data-ttu-id="e70e5-109">Jos lasketut arvot eivät ole tarkkoja, voit muokata niitä syöttämällä todelliset paino- ja tilavuusarvot kuormaan.</span><span class="sxs-lookup"><span data-stu-id="e70e5-109">If the calculated values aren’t precise, you can adjust them by entering the actual values for the weight and volume on the load.</span></span> <span data-ttu-id="e70e5-110">Paino- ja tilavuusarvoja käytetään kuljetusten hallintaprosessissa.</span><span class="sxs-lookup"><span data-stu-id="e70e5-110">The values for the weight and volume are used in transportation management processes.</span></span> <span data-ttu-id="e70e5-111">Arvoja käytetään esimerkiksi hinnan ja reitin työtilassa, jossa niillä määritetään kuormien hintaa ja reittiä; niitä käytetään myös kuljetustarjouksissa ja kuljettajan sisäänkuittauksessa.</span><span class="sxs-lookup"><span data-stu-id="e70e5-111">For example, the values are used in the rate route workbench, where they help define the rate and route for loads, and they are also used for transportation tenders and driver check-in.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e70e5-112">Käyttö</span><span class="sxs-lookup"><span data-stu-id="e70e5-112">Where it applies</span></span>

<span data-ttu-id="e70e5-113">Kontin painon ja tilavuuden lisäämistoimintoa käytetään kuljetuksenhallintaprosesseissa, kuten hinnan ja reitin työtilassa, kuljetustarjouksissa ja kuljettajan sisäänkuittauksessa.</span><span class="sxs-lookup"><span data-stu-id="e70e5-113">The functionality for including the container weight and volume on a load applies in transportation management processes, such as the rate route workbench, transportation tenders, and driver check-in.</span></span>

## <a name="how-it-is-set-up"></a><span data-ttu-id="e70e5-114">Määritysohjeet</span><span class="sxs-lookup"><span data-stu-id="e70e5-114">How it is set up</span></span>

<span data-ttu-id="e70e5-115">Konttien määrä, joka tulisi ottaa huomioon kuormassa lasketaan kontin painon ja tilavuuden sekä kontin käyttöasteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e70e5-115">The number of containers that should be considered for a load is calculated based on the weight and volume of the container, and on the percentage of the container is used.</span></span>

-   <span data-ttu-id="e70e5-116">Kontin painon ja tilavuuden voi määrittää kohdassa **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttityypit**.</span><span class="sxs-lookup"><span data-stu-id="e70e5-116">To set the weight and volume for a container, click **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>

-   <span data-ttu-id="e70e5-117">Kontin käyttöaste valitsemalla asetetaan kohdassa **Varastonhallinta** \> **Asetukset** \> **Kontit** \> **Konttiryhmät** kirjoittamalla arvo **Kontin käyttöaste** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="e70e5-117">To set the container utilization percentage, click **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**, and then enter a value in the **Container utilization percentage** field.</span></span>

