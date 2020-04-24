---
title: Näytä lähtevä suunniteltu konserniyritysten välinen kysyntä
description: Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bd24e2e19e3e7257f37ebc0becb8af2fdf82b546
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208590"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="c8e57-103">Näytä lähtevä suunniteltu konserniyritysten välinen kysyntä</span><span class="sxs-lookup"><span data-stu-id="c8e57-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8e57-104">Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.</span><span class="sxs-lookup"><span data-stu-id="c8e57-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="c8e57-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="c8e57-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="c8e57-106">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="c8e57-106">Click Master planning.</span></span>
2. <span data-ttu-id="c8e57-107">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c8e57-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="c8e57-108">Valitse suunnitelma 10 Suunitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c8e57-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="c8e57-109">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="c8e57-109">Click Run.</span></span>
4. <span data-ttu-id="c8e57-110">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="c8e57-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="c8e57-111">Tämä vastaa pääsuunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="c8e57-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="c8e57-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c8e57-112">Click OK.</span></span>
    * <span data-ttu-id="c8e57-113">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="c8e57-113">This may take a while.</span></span>  
6. <span data-ttu-id="c8e57-114">Valitse Suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="c8e57-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="c8e57-115">Valitse Lähtevä suunniteltu konserniyritysten välinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="c8e57-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="c8e57-116">Tällä sivulla on yleiskuvaus suunnitellusta kysynnästä, jonka täyttää sisäisen toimitusketjun toimittaja.</span><span class="sxs-lookup"><span data-stu-id="c8e57-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="c8e57-117">Laajenna Ylöspäin suuntautuvan kysynnän tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="c8e57-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="c8e57-118">Tässä osassa näytetään tietoja kysynnän täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="c8e57-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="c8e57-119">Voit joutua odottamaan pääsuunnittelun valmistumista toimittajayrityksessä, ennen kuin näet lisätietoja tässä.</span><span class="sxs-lookup"><span data-stu-id="c8e57-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

