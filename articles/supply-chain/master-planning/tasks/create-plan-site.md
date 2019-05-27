---
title: Luo toimipaikan suunnitelma
description: Tuotannon suunnittelija laskee materiaali- ja kapasiteettivaatimukset, jotka koskevat tietyn nimikkeen tuotantoa.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560321"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="162b0-103">Luo toimipaikan suunnitelma</span><span class="sxs-lookup"><span data-stu-id="162b0-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="162b0-104">Tuotannon suunnittelija laskee materiaali- ja kapasiteettivaatimukset, jotka koskevat tietyn nimikkeen tuotantoa.</span><span class="sxs-lookup"><span data-stu-id="162b0-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="162b0-105">Kun hankintaehdotukset on luotu, suunnittelija löytää tilaukset suunnittelemaltaan toimipaikalta ja vahvistaa tilaukset, aloittaen tärkeämmästä.</span><span class="sxs-lookup"><span data-stu-id="162b0-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="162b0-106">Kiireisimpiä tilauksia ovat ne, jotka on vahvistettava samana päivänä.</span><span class="sxs-lookup"><span data-stu-id="162b0-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="162b0-107">Käytä esittelyversion yritystä, USMF:ää, näiden tehtävien suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="162b0-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="162b0-108">Luo nimikkeen materiaali- ja kapasiteettisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="162b0-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="162b0-109">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="162b0-109">Click Master planning.</span></span>
    * <span data-ttu-id="162b0-110">Sinun on siirryttävä oletuskoontinäytölle.</span><span class="sxs-lookup"><span data-stu-id="162b0-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="162b0-111">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="162b0-111">Click Run.</span></span>
3. <span data-ttu-id="162b0-112">Laajenna Tietueet-kohta ja sisällytä osaan.</span><span class="sxs-lookup"><span data-stu-id="162b0-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="162b0-113">Valitse Suodatin.</span><span class="sxs-lookup"><span data-stu-id="162b0-113">Click Filter.</span></span>
5. <span data-ttu-id="162b0-114">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="162b0-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="162b0-115">Kirjoita arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="162b0-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="162b0-116">Esimerkki: D0001</span><span class="sxs-lookup"><span data-stu-id="162b0-116">Example: D0001</span></span>  
7. <span data-ttu-id="162b0-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="162b0-117">Click OK.</span></span>
8. <span data-ttu-id="162b0-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="162b0-118">Click OK.</span></span>
    * <span data-ttu-id="162b0-119">Tämä voi kestää muutamia minuutteja.</span><span class="sxs-lookup"><span data-stu-id="162b0-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="162b0-120">Päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="162b0-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="162b0-121">Tunnista nimikkeen suunnitellut tilaukset, jotka ovat kiireisiä</span><span class="sxs-lookup"><span data-stu-id="162b0-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="162b0-122">Avaa nimiketunnuksen sarakkeen suodatin.</span><span class="sxs-lookup"><span data-stu-id="162b0-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="162b0-123">Käytä suodatinta Nimiketunnus-kentässä niin, että arvo on D0001 ja suodatinoperaattori Alkaa.</span><span class="sxs-lookup"><span data-stu-id="162b0-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="162b0-124">Avaa sarakkeen Tilauspvm.-suodatin.</span><span class="sxs-lookup"><span data-stu-id="162b0-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="162b0-125">Käytä suodatinta "Tilauspäivä"-kentässä käyttäen arvona nykyistä päivämäärää ja "on täsmälleen" -suodatinoperaattoria.</span><span class="sxs-lookup"><span data-stu-id="162b0-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="162b0-126">Vahvista kaikki nimikkeen suunnitellut tilaukset, jotka ovat kiireisiä</span><span class="sxs-lookup"><span data-stu-id="162b0-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="162b0-127">Merkitse kaikki rivit tai poista kaikkien rivien merkinnät luettelossa.</span><span class="sxs-lookup"><span data-stu-id="162b0-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="162b0-128">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="162b0-128">Click Firm.</span></span>
3. <span data-ttu-id="162b0-129">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="162b0-129">Click OK.</span></span>

