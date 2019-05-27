---
title: Näytä lähtevä suunniteltu konserniyritysten välinen kysyntä
description: Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e0e3a4613e5598e725c475c7dff7662bf4169a7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565612"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="cab0d-103">Näytä lähtevä suunniteltu konserniyritysten välinen kysyntä</span><span class="sxs-lookup"><span data-stu-id="cab0d-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cab0d-104">Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.</span><span class="sxs-lookup"><span data-stu-id="cab0d-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="cab0d-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="cab0d-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="cab0d-106">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="cab0d-106">Click Master planning.</span></span>
2. <span data-ttu-id="cab0d-107">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="cab0d-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="cab0d-108">Valitse suunnitelma 10 Suunitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="cab0d-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="cab0d-109">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="cab0d-109">Click Run.</span></span>
4. <span data-ttu-id="cab0d-110">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="cab0d-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="cab0d-111">Tämä vastaa pääsuunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="cab0d-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="cab0d-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="cab0d-112">Click OK.</span></span>
    * <span data-ttu-id="cab0d-113">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="cab0d-113">This may take a while.</span></span>  
6. <span data-ttu-id="cab0d-114">Valitse Suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="cab0d-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="cab0d-115">Valitse Lähtevä suunniteltu konserniyritysten välinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="cab0d-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="cab0d-116">Tällä sivulla on yleiskuvaus suunnitellusta kysynnästä, jonka täyttää sisäisen toimitusketjun toimittaja.</span><span class="sxs-lookup"><span data-stu-id="cab0d-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="cab0d-117">Laajenna Ylöspäin suuntautuvan kysynnän tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="cab0d-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="cab0d-118">Tässä osassa näytetään tietoja kysynnän täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="cab0d-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="cab0d-119">Voit joutua odottamaan pääsuunnittelun valmistumista toimittajayrityksessä, ennen kuin näet lisätietoja tässä.</span><span class="sxs-lookup"><span data-stu-id="cab0d-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

