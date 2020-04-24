---
title: Yhteistyö sisäisen toimitusketjun asiakkaiden kanssa
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
ms.openlocfilehash: fb807a904afaba09d0dc364c06f964c135d3cfb1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208659"
---
# <a name="collaborate-with-internal-supply-chain-customers"></a><span data-ttu-id="af389-103">Yhteistyö sisäisen toimitusketjun asiakkaiden kanssa</span><span class="sxs-lookup"><span data-stu-id="af389-103">Collaborate with internal supply chain customers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af389-104">Näiden ohjeiden avulla voit tarkastella kaikkia suunniteltuja tilauksia, jotka täyttää konsernitoimittaja.</span><span class="sxs-lookup"><span data-stu-id="af389-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="af389-105">Tämän menettelyn luomisessa käytetty esittely-yritys on DEMF.</span><span class="sxs-lookup"><span data-stu-id="af389-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="af389-106">Valitse Pääsuunnittelu.</span><span class="sxs-lookup"><span data-stu-id="af389-106">Click Master planning.</span></span>
2. <span data-ttu-id="af389-107">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="af389-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="af389-108">Valitse suunnitelma 10 Suunitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="af389-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="af389-109">Valitse Suorita.</span><span class="sxs-lookup"><span data-stu-id="af389-109">Click Run.</span></span>
4. <span data-ttu-id="af389-110">Syötä Säikeiden määrä -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="af389-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="af389-111">Tämä vastaa pääsuunnittelussa käytettävien rinnakkaisten säikeiden määrää.</span><span class="sxs-lookup"><span data-stu-id="af389-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="af389-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="af389-112">Click OK.</span></span>
    * <span data-ttu-id="af389-113">Tämä saattaa kestää jonkin aikaa.</span><span class="sxs-lookup"><span data-stu-id="af389-113">This may take a while.</span></span>  
6. <span data-ttu-id="af389-114">Valitse Suunniteltu konsernin sisäinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="af389-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="af389-115">Valitse Lähtevä suunniteltu konserniyritysten välinen kysyntä.</span><span class="sxs-lookup"><span data-stu-id="af389-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="af389-116">Tällä sivulla on yleiskuvaus suunnitellusta kysynnästä, jonka täyttää sisäisen toimitusketjun toimittaja.</span><span class="sxs-lookup"><span data-stu-id="af389-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="af389-117">Laajenna Ylöspäin suuntautuvan kysynnän tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="af389-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="af389-118">Tässä osassa näytetään tietoja kysynnän täyttämisestä.</span><span class="sxs-lookup"><span data-stu-id="af389-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="af389-119">Voit joutua odottamaan pääsuunnittelun valmistumista toimittajayrityksessä, ennen kuin näet lisätietoja tässä.</span><span class="sxs-lookup"><span data-stu-id="af389-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

