---
title: Kuormien suunnittelu keskusten konsolidoinnin avulla – yleiskatsaus
description: Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d61527113746e76889d097e963f70ced24fd241
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016421"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a><span data-ttu-id="5afcf-103">Kuormien suunnittelu keskusten konsolidoinnin avulla – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5afcf-103">Plan loads using hub consolidation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5afcf-104">Tässä artikkelissa käsitellään lähetysten konsolidointia keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun vastaanotat hyödykkeitä useilta toimittajilta samaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="5afcf-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="5afcf-105">Lähetykset kannattaa ehkä konsolidoida keskukseen, kun toimitat hyödykkeitä eri varastoista samalle asiakkaalle tai kun useat toimittajat toimittavat hyödykkeitä samaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="5afcf-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="5afcf-106">Kuormien muodostaminen</span><span class="sxs-lookup"><span data-stu-id="5afcf-106">Building loads</span></span>
<span data-ttu-id="5afcf-107">Ennen konsolidointia keskukseen **Kuljetussuunnittelu** -vaihtoehto on otettava käyttöön **Kuljetustenhallintaparametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5afcf-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="5afcf-108">Sinun on myös luotava keskukset, joissa konsolidointi tapahtuu.</span><span class="sxs-lookup"><span data-stu-id="5afcf-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="5afcf-109">Seuraavassa kaaviossa on esimerkki konsolidoinnista keskukseen.</span><span class="sxs-lookup"><span data-stu-id="5afcf-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="5afcf-110">Tässä tapauksessa eri varastoista tulevilla myyntitilauksilla on sama asiakas.</span><span class="sxs-lookup"><span data-stu-id="5afcf-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="5afcf-111">Peruskuormat luodaan myyntitilausten perusteella tavalliseen tapaan **Kuormasuunnittelun työtila** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="5afcf-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="5afcf-112">Voit konsolidoida kaksi kuormaa keskuksessa ennen niiden toimittamista asiakkaalle valitsemalla **Kuormasuunnittelun työtila** -sivun **Kuljetus** -kentässä **Keskusten konsolidointi**.</span><span class="sxs-lookup"><span data-stu-id="5afcf-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="5afcf-113">Kun valitset kullekin kuormalle oikean keskuksen, keskus on kuormien jättökohde.</span><span class="sxs-lookup"><span data-stu-id="5afcf-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="5afcf-114">Lisäksi **Kuormasuunnittelun työtila** -sivun **Tarjonta ja kysyntä** -osassa on kaksi kuljetuspyynnön riviä.</span><span class="sxs-lookup"><span data-stu-id="5afcf-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="5afcf-115">Voit sitten lisätä nämä kaksi riviä uuteen kuormaan.</span><span class="sxs-lookup"><span data-stu-id="5afcf-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="5afcf-116">Tässä uudessa kuormassa on molemmat myyntitilausrivit. Lisäksi keskus on keräilyosoitteena ja asiakas A jättökohteena.</span><span class="sxs-lookup"><span data-stu-id="5afcf-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="5afcf-117">Kolme kuormaa ovat sitten valmiita hinnoittelua ja reititystä varten muiden kuormien tavoin.</span><span class="sxs-lookup"><span data-stu-id="5afcf-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="5afcf-118">Voit valita kullekin kuormalle järjestelmän ehdottaman lähetyksen rahdinkuljettajan.</span><span class="sxs-lookup"><span data-stu-id="5afcf-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="5afcf-119">[![Keskusten konsolidointi](./media/hubconsol.jpg)](./media/hubconsol.jpg) Voit konsolidoida kuormia samalla menetelmällä useille siirtotilauksille.</span><span class="sxs-lookup"><span data-stu-id="5afcf-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="5afcf-120">Tässä tapauksessa edellisen kaavion asiakas A on varasto.</span><span class="sxs-lookup"><span data-stu-id="5afcf-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="5afcf-121">Voit vaihtoehtoisesti konsolidoida useiden ostotilausten kuormat tilanteessa, jossa eri toimittajat toimittavat kuormat samaan varastoon.</span><span class="sxs-lookup"><span data-stu-id="5afcf-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="5afcf-122">Sinulla on useita konsolidointikeskuksia ja voit konsolidoida eri varastoita tulevia kuormia useissa keskuksissa.</span><span class="sxs-lookup"><span data-stu-id="5afcf-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="5afcf-123">Kun olet muodostanut peruskuormat ja käytät keskuksen konsolidointiasetusta, voit muodostaa uusia kuormia konsolidoimalla kuljetuspyynnön rivit.</span><span class="sxs-lookup"><span data-stu-id="5afcf-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="5afcf-124">Voit sitten hinnoitella ja reitittää kuormat.</span><span class="sxs-lookup"><span data-stu-id="5afcf-124">You then rate and route your loads.</span></span>



