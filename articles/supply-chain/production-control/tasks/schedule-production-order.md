--- 
title: Ajoita tuotantotilaus
description: "Tässä menettelyssä selvitetään, miten tuotantotilaus ajoitetaan."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4aeb51fd2d9e916d5838b47c4a6b74800572a9ca
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="a693c-103">Ajoita tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="a693c-103">Schedule a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a693c-104">Tässä menettelyssä selvitetään, miten tuotantotilaus ajoitetaan.</span><span class="sxs-lookup"><span data-stu-id="a693c-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="a693c-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="a693c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a693c-106">Tämä on kolmas seitsemästä tuotantotilauksen elinkaaresta kertovasta menettelystä.</span><span class="sxs-lookup"><span data-stu-id="a693c-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="a693c-107">Ajoita tuotantotilaus</span><span class="sxs-lookup"><span data-stu-id="a693c-107">Schedule a production order</span></span>
1. <span data-ttu-id="a693c-108">Siirry kohtaan Tuotannonhallinta > Tuotantotilaukset > Kaikki tuotantotilaukset.</span><span class="sxs-lookup"><span data-stu-id="a693c-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="a693c-109">Valitse tuotantotilaus, jonka tila on Arvioitu.</span><span class="sxs-lookup"><span data-stu-id="a693c-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="a693c-110">Valitse toimintoruudussa Aikataulu.</span><span class="sxs-lookup"><span data-stu-id="a693c-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="a693c-111">Valitse Ajoita työt.</span><span class="sxs-lookup"><span data-stu-id="a693c-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="a693c-112">Ajoituksen parametrit määritetään tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="a693c-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="a693c-113">Voit määrittää parametrit tietyille käyttäjille tai kaikille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="a693c-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="a693c-114">Valitse Ajoituksen suunta -kentässä Tästä päivästä eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="a693c-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="a693c-115">Anna Ajoituspäivämäärä-kentässä päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a693c-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="a693c-116">Valitse Rajallinen kapasiteetti -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a693c-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="a693c-117">Valitse Rajallinen materiaali -valintaruutu tai poista sen valinta.</span><span class="sxs-lookup"><span data-stu-id="a693c-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="a693c-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a693c-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="a693c-119">Näytä ajoituksen tulokset</span><span class="sxs-lookup"><span data-stu-id="a693c-119">View the scheduling results</span></span>
1. <span data-ttu-id="a693c-120">Valitse toimintoruudussa Tuotantotilaus.</span><span class="sxs-lookup"><span data-stu-id="a693c-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="a693c-121">Valitse Kaikki työt.</span><span class="sxs-lookup"><span data-stu-id="a693c-121">Click All jobs.</span></span>
    * <span data-ttu-id="a693c-122">Juuri luodut ajoitetut työt näkyvät tällä sivulla.</span><span class="sxs-lookup"><span data-stu-id="a693c-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="a693c-123">Laajenna tai tiivistä Aikataulutus-osa.</span><span class="sxs-lookup"><span data-stu-id="a693c-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="a693c-124">Voit tarkastella ajoituksen pikavälilehdessä ajoitettua päivämäärää ja aikaa.</span><span class="sxs-lookup"><span data-stu-id="a693c-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="a693c-125">Valitse Kyselyt.</span><span class="sxs-lookup"><span data-stu-id="a693c-125">Click Inquiries.</span></span>
5. <span data-ttu-id="a693c-126">Valitse Kapasiteetin kuormitus.</span><span class="sxs-lookup"><span data-stu-id="a693c-126">Click Capacity load.</span></span>
    * <span data-ttu-id="a693c-127">Kapasiteetin kuormitus -sivulla näkyy töiden ajoittamisella varattu kapasiteetti, resurssiin tällä hetkellä varattujen tuntien kokonaismäärä ja resurssissa jäljellä olevat tunnit, joille voidaan ajoittaa töitä.</span><span class="sxs-lookup"><span data-stu-id="a693c-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="a693c-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a693c-128">Close the page.</span></span>
7. <span data-ttu-id="a693c-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="a693c-129">Close the page.</span></span>


