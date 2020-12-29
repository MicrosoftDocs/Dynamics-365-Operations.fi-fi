---
title: Luo toimipisteelle aikataulu
description: Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9059080fcd77a5317ce4226de6aad38b0066500
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427092"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="e62f0-103">Luo toimipisteelle aikataulu</span><span class="sxs-lookup"><span data-stu-id="e62f0-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e62f0-104">Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="e62f0-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="e62f0-105">Tämän menettelyn täytössä on käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="e62f0-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="e62f0-106">Tunnista aloittamattomat tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="e62f0-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="e62f0-107">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="e62f0-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e62f0-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="e62f0-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e62f0-109">Voit esimerkiksi suodattaa Toimipaikka-kenttää arvolla 1.</span><span class="sxs-lookup"><span data-stu-id="e62f0-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="e62f0-110">1 edustaa USMF:n toimipistettä.</span><span class="sxs-lookup"><span data-stu-id="e62f0-110">1 represents a site in USMF.</span></span> <span data-ttu-id="e62f0-111">Jos et käytä USMF:ää, valitse oman yrityksesi toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="e62f0-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="e62f0-112">Avaa Tila-sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="e62f0-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="e62f0-113">Suodattimen operaattorin "on täsmälleen" avulla voit käyttää suodatinta kentässä "Tila", jonka arvo on "Ajoitettu".</span><span class="sxs-lookup"><span data-stu-id="e62f0-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="e62f0-114">Luo aikataulu</span><span class="sxs-lookup"><span data-stu-id="e62f0-114">Create a schedule</span></span>
1. <span data-ttu-id="e62f0-115">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e62f0-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="e62f0-116">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="e62f0-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="e62f0-117">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="e62f0-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="e62f0-118">Valitse Ajoituksen suunta -kentässä Toimituspäivästä taaksepäin.</span><span class="sxs-lookup"><span data-stu-id="e62f0-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="e62f0-119">Valitse Rajallinen kapasiteetti -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="e62f0-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="e62f0-120">Valitse Rajallinen materiaali -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="e62f0-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="e62f0-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="e62f0-121">Click OK.</span></span>
    * <span data-ttu-id="e62f0-122">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="e62f0-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="e62f0-123">Katso ajoitettujen tuotantotilauksien tulos</span><span class="sxs-lookup"><span data-stu-id="e62f0-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="e62f0-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e62f0-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e62f0-125">Voit merkitä minkä tahansa rivin.</span><span class="sxs-lookup"><span data-stu-id="e62f0-125">You can mark any row.</span></span>  
2. <span data-ttu-id="e62f0-126">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="e62f0-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e62f0-127">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="e62f0-127">Click All jobs.</span></span>
    * <span data-ttu-id="e62f0-128">Tällä sivulla voit tarkastella työluetteloa.</span><span class="sxs-lookup"><span data-stu-id="e62f0-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="e62f0-129">Aikataulutus-välilehdessä näet projektin alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="e62f0-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="e62f0-130">Napsauta kohtaa Materiaalit.</span><span class="sxs-lookup"><span data-stu-id="e62f0-130">Click Materials.</span></span>
    * <span data-ttu-id="e62f0-131">Tällä sivulla voit tarkastella tuotantotilauksen toimintojen arvioitua materiaalinkulutusta ja käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="e62f0-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

