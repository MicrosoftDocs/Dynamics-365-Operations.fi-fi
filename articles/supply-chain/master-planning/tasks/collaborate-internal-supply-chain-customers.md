---
title: Yhteistyö sisäisen toimitusketjun asiakkaiden kanssa
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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2746534cc808dc61e54aa55c1030422bb37e8984
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148144"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="8f3cc-103">Yhteistyö sisäisen toimitusketjun asiakkaiden kanssa</span><span class="sxs-lookup"><span data-stu-id="8f3cc-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f3cc-104">Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="8f3cc-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="8f3cc-106">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-106">Click Master planning.</span></span>
2. <span data-ttu-id="8f3cc-107">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="8f3cc-108">Valitse suunnitelma 10 Suunitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="8f3cc-109">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-109">Click Run.</span></span>
4. <span data-ttu-id="8f3cc-110">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="8f3cc-111">Tämä vastaa pääsuunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="8f3cc-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-112">Click OK.</span></span>
    * <span data-ttu-id="8f3cc-113">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-113">This may take a while.</span></span>  
6. <span data-ttu-id="8f3cc-114">Valitse Suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="8f3cc-115">Valitse Lähtevä suunniteltu konserniyritysten välinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="8f3cc-116">Tällä sivulla on yleiskuvaus suunnitellusta kysynnästä, jonka täyttää sisäisen toimitusketjun toimittaja.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="8f3cc-117">Laajenna Ylöspäin suuntautuvan kysynnän tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="8f3cc-118">Tässä osassa näytetään tietoja kysynnän täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="8f3cc-119">Voit joutua odottamaan pääsuunnittelun valmistumista toimittajayrityksessä, ennen kuin näet lisätietoja tässä.</span><span class="sxs-lookup"><span data-stu-id="8f3cc-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

