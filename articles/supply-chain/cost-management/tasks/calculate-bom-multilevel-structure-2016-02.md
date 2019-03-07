---
title: Tuoterakenteen laskeminen käyttämällä monitasoista rakennetta (helmikuu 2016)
description: Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa monitasoista hajotusta.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcc1248d64145c10f1c67bfac49c053e99dc1598
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "323361"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a><span data-ttu-id="236d1-103">Tuoterakenteen laskeminen käyttämällä monitasoista rakennetta (helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="236d1-103">Calculate a BOM by using a multilevel structure (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="236d1-104">Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa monitasoista hajotusta.</span><span class="sxs-lookup"><span data-stu-id="236d1-104">This procedure shows how to calculate the cost of a finished product by using multilevel explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="236d1-105">Se on tuoterakenteen laskentasarjan seitsemäs tehtävä.</span><span class="sxs-lookup"><span data-stu-id="236d1-105">It is the seventh task in the BOM calculation series.</span></span> <span data-ttu-id="236d1-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="236d1-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="236d1-107">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="236d1-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="236d1-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="236d1-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="236d1-109">Valitse tuotteen BOM_1.</span><span class="sxs-lookup"><span data-stu-id="236d1-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="236d1-110">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="236d1-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="236d1-111">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="236d1-111">Click Item price.</span></span>
5. <span data-ttu-id="236d1-112">Valitse Laske nimikekustannus.</span><span class="sxs-lookup"><span data-stu-id="236d1-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="236d1-113">Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.</span><span class="sxs-lookup"><span data-stu-id="236d1-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="236d1-114">Anna tai valitse Kustannuslaskentaversio-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="236d1-114">In the Costing version field, enter or select a value.</span></span>
    * <span data-ttu-id="236d1-115">Valitse Kustannusversio 20, koska se on suunniteltu kustannustyyppi ja hajotustila on monitasoinen.</span><span class="sxs-lookup"><span data-stu-id="236d1-115">Select Costing version 20, because it's Planned cost type and Explosion mode is Multilevel.</span></span>   <span data-ttu-id="236d1-116">Monitasoinen hajotustila on tarkoitettu suunnitelluille kustannuksille ja simulaatioille.</span><span class="sxs-lookup"><span data-stu-id="236d1-116">The Multilevel explosion mode is for planned costs and simulations.</span></span> <span data-ttu-id="236d1-117">Sitä ei käytetä standardikustannuksille.</span><span class="sxs-lookup"><span data-stu-id="236d1-117">It is not used for standard cost.</span></span>  
7. <span data-ttu-id="236d1-118">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="236d1-118">Click OK.</span></span>
8. <span data-ttu-id="236d1-119">Valitse Näytä laskennan tiedot.</span><span class="sxs-lookup"><span data-stu-id="236d1-119">Click View calculation details.</span></span>
    * <span data-ttu-id="236d1-120">Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.</span><span class="sxs-lookup"><span data-stu-id="236d1-120">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  <span data-ttu-id="236d1-121">Huomaa tässä tapauksessa, että BOM_2 on laskettu ottamalla huomioon raaka-aine, prosessi ja yleiskustannus, joiden yhteissumma on 29,40, eikä standardikustannuksella 10, joka aktivoitiin tämän sarjan alkuperäisessä tehtäväoppaassa.</span><span class="sxs-lookup"><span data-stu-id="236d1-121">In this case, notice how BOM_2 has been calculated taking into account the raw material, process, and overhead with a total of 29,40 instead of the standard cost of 10 that was activated in the initial task guide in this series.</span></span>  
9. <span data-ttu-id="236d1-122">Valitse Kustannuslaskentalomake-välilehti.</span><span class="sxs-lookup"><span data-stu-id="236d1-122">Click the Costing sheet tab.</span></span>
    * <span data-ttu-id="236d1-123">Kun siirrytään Kustannuslaskentalomake-välilehteen kustannusryhmäkohtaiset yhteissummat poikkeavat edellisessä tehtäväoppaassa tehdyistä laskelmista.</span><span class="sxs-lookup"><span data-stu-id="236d1-123">Moving to the Costing sheet tab, the totals per cost group are different compared to the calculation done in previous task guide.</span></span>  
10. <span data-ttu-id="236d1-124">Valitse Taso-kentässä Monitasoinen.</span><span class="sxs-lookup"><span data-stu-id="236d1-124">In the Level field, select 'Multi'.</span></span>
    * <span data-ttu-id="236d1-125">Kun Monitasoinen valitaan, kustannukset luokitellaan BOM_2-kokoonpanon mukaan, jolloin 10 johdetaan M1-kustannusryhmästä (ITEM_C) ja 15,60 johdetaan sen tuotannosta, jossa kustannusryhmä on L2.</span><span class="sxs-lookup"><span data-stu-id="236d1-125">When selecting Multi, the costs are classified according to the composition of BOM_2, where 10 is derived from the M1 cost group (ITEM_C), and 15,60 is derived from its manufacturing where the cost group is L2.</span></span> <span data-ttu-id="236d1-126">Myös epäsuorat kustannukset vaihtelevat.</span><span class="sxs-lookup"><span data-stu-id="236d1-126">Indirect costs also vary.</span></span>  
11. <span data-ttu-id="236d1-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="236d1-127">Close the page.</span></span>
12. <span data-ttu-id="236d1-128">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="236d1-128">Close the page.</span></span>

