---
title: Luo toimipisteelle aikataulu
description: Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54bb2532534d5567239dad4fab7fd74fa50d2826
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549380"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="ee088-103">Luo toimipisteelle aikataulu</span><span class="sxs-lookup"><span data-stu-id="ee088-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee088-104">Seuraavassa menettelyssä kuvataan, toimipaikan aloittamattomat tuotantotilaukset ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="ee088-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="ee088-105">Tämän menettelyn täytössä on käytetty USMF-yrityksen demotietoja.</span><span class="sxs-lookup"><span data-stu-id="ee088-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="ee088-106">Tunnista aloittamattomat tuotantotilaukset</span><span class="sxs-lookup"><span data-stu-id="ee088-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="ee088-107">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="ee088-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ee088-108">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="ee088-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ee088-109">Voit esimerkiksi suodattaa Toimipaikka-kenttää arvolla 1.</span><span class="sxs-lookup"><span data-stu-id="ee088-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="ee088-110">1 edustaa USMF:n toimipistettä.</span><span class="sxs-lookup"><span data-stu-id="ee088-110">1 represents a site in USMF.</span></span> <span data-ttu-id="ee088-111">Jos et käytä USMF:ää, valitse oman yrityksesi toimipaikka.</span><span class="sxs-lookup"><span data-stu-id="ee088-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="ee088-112">Avaa Tila-sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="ee088-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="ee088-113">Suodattimen operaattorin "on täsmälleen" avulla voit käyttää suodatinta kentässä "Tila", jonka arvo on "Ajoitettu".</span><span class="sxs-lookup"><span data-stu-id="ee088-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="ee088-114">Luo aikataulu</span><span class="sxs-lookup"><span data-stu-id="ee088-114">Create a schedule</span></span>
1. <span data-ttu-id="ee088-115">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ee088-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="ee088-116">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="ee088-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="ee088-117">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="ee088-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="ee088-118">Valitse Ajoituksen suunta -kentässä Toimituspäivästä taaksepäin.</span><span class="sxs-lookup"><span data-stu-id="ee088-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="ee088-119">Valitse Rajallinen kapasiteetti -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="ee088-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="ee088-120">Valitse Rajallinen materiaali -kentässä Ei.</span><span class="sxs-lookup"><span data-stu-id="ee088-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="ee088-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ee088-121">Click OK.</span></span>
    * <span data-ttu-id="ee088-122">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="ee088-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="ee088-123">Katso ajoitettujen tuotantotilauksien tulos</span><span class="sxs-lookup"><span data-stu-id="ee088-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="ee088-124">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="ee088-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ee088-125">Voit merkitä minkä tahansa rivin.</span><span class="sxs-lookup"><span data-stu-id="ee088-125">You can mark any row.</span></span>  
2. <span data-ttu-id="ee088-126">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="ee088-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="ee088-127">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="ee088-127">Click All jobs.</span></span>
    * <span data-ttu-id="ee088-128">Tällä sivulla voit tarkastella työluetteloa.</span><span class="sxs-lookup"><span data-stu-id="ee088-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="ee088-129">Aikataulutus-välilehdessä näet projektin alkamis- ja päättymispäivämäärät.</span><span class="sxs-lookup"><span data-stu-id="ee088-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="ee088-130">Napsauta kohtaa Materiaalit.</span><span class="sxs-lookup"><span data-stu-id="ee088-130">Click Materials.</span></span>
    * <span data-ttu-id="ee088-131">Tällä sivulla voit tarkastella tuotantotilauksen toimintojen arvioitua materiaalinkulutusta ja käytettävissä olevaa varastoa.</span><span class="sxs-lookup"><span data-stu-id="ee088-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

