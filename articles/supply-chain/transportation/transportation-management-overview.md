---
title: Kuljetustenhallinnan yleiskatsaus
description: Tässä ohjeaiheessa on Supply Chain Managementin kuljetustenhallinnan toimintojen yleiskatsaus.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4affc5846ee329a4571d6fb3e0c42873387241ad
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427441"
---
# <a name="transportation-management-overview"></a><span data-ttu-id="98a3b-103">Kuljetustenhallinnan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="98a3b-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a3b-104">Tässä ohjeaiheessa on Supply Chain Managementin kuljetustenhallinnan toimintojen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="98a3b-104">This topic gives an overview of the transportation management functionality in Supply Chain Management.</span></span>

<span data-ttu-id="98a3b-105">Kuljetustenhallinnan avulla voit hallita yrityksen kuljetuksia sekä määrittää toimittajan ja reititysratkaisut lähteville ja saapuville tilauksille.</span><span class="sxs-lookup"><span data-stu-id="98a3b-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="98a3b-106">Voit esimerkiksi tunnistaa nopeimman reitin tai edullisimman hinnan lähetykselle.</span><span class="sxs-lookup"><span data-stu-id="98a3b-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="98a3b-107">Seuraavassa taulukossa kuvataan kuljetustenhallinnan tärkeimmät käyttöskenaariot.</span><span class="sxs-lookup"><span data-stu-id="98a3b-107">The following table describes the main scenarios for using Transportation management.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98a3b-108">Skenaario</span><span class="sxs-lookup"><span data-stu-id="98a3b-108">Scenario</span></span></th>
<th><span data-ttu-id="98a3b-109">Missä kuljetustenhallinnasta on apua</span><span class="sxs-lookup"><span data-stu-id="98a3b-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98a3b-110">Ulkoisten logistiikkatoimittajien käyttö kuljetustehtävissä.</span><span class="sxs-lookup"><span data-stu-id="98a3b-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="98a3b-111">Kuljetustenhallinnan käyttö saapuvissa ja lähtevissä kuljetuksissa.</span><span class="sxs-lookup"><span data-stu-id="98a3b-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98a3b-112">Yrityksen omaa kalustoa voidaan käyttää toimituksissa ja noudoissa, ja toimituskulut siirretään asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="98a3b-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="98a3b-113">Lähtevissä prosesseissa voit kuljetustenhallinnan avulla määrittää kuljetuskulut ja siirtää ne asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="98a3b-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="98a3b-114">Rahdinkuljettajan laskun täsmäytysprosessia ei kuitenkaan tarvita.</span><span class="sxs-lookup"><span data-stu-id="98a3b-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98a3b-115">Yrityksen omaa kalustoa voidaan käyttää toimituksissa ja noudoissa, mutta toimituskulut eivät siirry asiakkaille, koska kuljetus sisältyy tuotehintoihin.</span><span class="sxs-lookup"><span data-stu-id="98a3b-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="98a3b-116">Läheskään kaikki kuljetustenhallinnan toiminnot eivät ole pakollisia.</span><span class="sxs-lookup"><span data-stu-id="98a3b-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="98a3b-117">Kuljetustenhallinnan avulla voit kuitenkin määrittää kuljetushinnat ja tarkistaa myyntihintoja niiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="98a3b-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98a3b-118">Logistiikkapalvelua tarjoaa toinen samaan yhtiöön kuuluva yritys.</span><span class="sxs-lookup"><span data-stu-id="98a3b-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="98a3b-119">Kuljetustenhallinnan avulla voit käsitellä toista yritystä kuin mitä tahansa muuta rahdinkuljettajaa.</span><span class="sxs-lookup"><span data-stu-id="98a3b-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="98a3b-120">Yritysten välisiä taloudellisia tapahtumia ei voi automatisoida.</span><span class="sxs-lookup"><span data-stu-id="98a3b-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="98a3b-121">Siksi nämä tapahtumat on käsiteltävä manuaalisesti (esimerkiksi luomalla ostotilaus).</span><span class="sxs-lookup"><span data-stu-id="98a3b-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="98a3b-122">Yritys, joka tarjoaa logistiikkapalveluja, voi käyttää kuljetustenhallintaa kuljetushintojen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="98a3b-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a><span data-ttu-id="98a3b-123">Kuljetusten suunnittelu Supply Chain Managementissa</span><span class="sxs-lookup"><span data-stu-id="98a3b-123">Planning transportation in Supply Chain Management</span></span>
<span data-ttu-id="98a3b-124">Kuljetustenhallinnassa kuljetusten suunnittelu voidaan tehdä joko tilausten tai niistä luotujen lähetysten perusteella.</span><span class="sxs-lookup"><span data-stu-id="98a3b-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="98a3b-125">Lähetykset tapahtuvat aina jossakin vaiheessa, mutta niitä ei tarvita kuljetusten suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="98a3b-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="98a3b-126">Siirtotilaukset kuuluvat lähtevien tilausten skenaarioon, ja ne voidaan suunnitella yhdessä myyntitilausten kanssa.</span><span class="sxs-lookup"><span data-stu-id="98a3b-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![Kuormapiirustus](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="98a3b-128">Saapuva kuljetus</span><span class="sxs-lookup"><span data-stu-id="98a3b-128">Inbound transportation</span></span>
<span data-ttu-id="98a3b-129">Kun tilaat nimikkeitä toimittajalta, ja nimikkeet on toimitettava varastoosi, haluat ehkä järjestää nimikkeiden kuljetuksen itse.</span><span class="sxs-lookup"><span data-stu-id="98a3b-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="98a3b-130">Supply Chain Management -ohjelmassa voit suunnitella saapuvan kuorman kuljetuksen ja vastaanoton.</span><span class="sxs-lookup"><span data-stu-id="98a3b-130">You can use Supply Chain Management to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="98a3b-131">Seuraavat kuvat esittävät liiketoimintaprosessin kulkua saapuvan kuorman kuljetuksen suunnittelulle.</span><span class="sxs-lookup"><span data-stu-id="98a3b-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![Saapuvien kuormakuljetusten liiketoimintaprosessin työnkulku](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="98a3b-133">Lähtevä kuljetus</span><span class="sxs-lookup"><span data-stu-id="98a3b-133">Outbound transportation</span></span>
<span data-ttu-id="98a3b-134">Voit suunnitella ja käsitellä lähtevän kuorman tiettyjen nimikkeiden toimittamiseksi yrityksen varastosta asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="98a3b-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="98a3b-135">Supply Chain Management -ohjelmassa voit suunnitella lähtevän kuorman kuljetuksen ja toimituksen.</span><span class="sxs-lookup"><span data-stu-id="98a3b-135">You can use Supply Chain Management to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="98a3b-136">Seuraavassa kuvassa on esitetty liiketoiminnan prosessin kulku lähtevien kuormien suunnittelemiseksi ja käsittelemiseksi lähetystä varten.</span><span class="sxs-lookup"><span data-stu-id="98a3b-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![Lähtevien kuormien suunnittelu ja käsittely](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="98a3b-138">Kuormituksen luonti</span><span class="sxs-lookup"><span data-stu-id="98a3b-138">Load building</span></span>
<span data-ttu-id="98a3b-139">Supply Chain Management sisältää Tilavuuteen perustuva kuormituksen luontistrategia -nimisen kuorman luontistrategian.</span><span class="sxs-lookup"><span data-stu-id="98a3b-139">Supply Chain Management provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="98a3b-140">Sen avulla voit käyttää kuormamallissa määritettyjä suurimpia korkeus- ja painoarvoja tai korvata asetukset syöttämällä uudet arvot.</span><span class="sxs-lookup"><span data-stu-id="98a3b-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="98a3b-141">Jos haluat käyttää tätä strategiaa, valitse se **Kuormituksen luontistrategia** -kentässä **Asetukset**-pikavälilehdessä **Kuormituksen luonnin työtila** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="98a3b-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="98a3b-142">Voit lisätä myös oman kuormituksen rakennuksen strategioita luomalla uuden luokan sovellusobjektipuussa (AOT).</span><span class="sxs-lookup"><span data-stu-id="98a3b-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>



