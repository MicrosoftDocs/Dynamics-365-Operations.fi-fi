--- 
title: "Tuoterakenteen laskeminen käyttämällä yksitasoista rakennetta (vain helmikuu 2016)"
description: "Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa yksitasoista hajotusta."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1def2baf6a42ae4f8d117b4c06f402397b83bf88
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a><span data-ttu-id="6aacb-103">Tuoterakenteen laskeminen käyttämällä yksitasoista rakennetta (vain helmikuu 2016)</span><span class="sxs-lookup"><span data-stu-id="6aacb-103">Calculate a BOM by using a single level structure (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6aacb-104">Tämä menettely osoittaa, miten valmiin tuotteen kustannukset lasketaan käyttämällä kustannuslaskentalomakkeeseen perustuvaa yksitasoista hajotusta.</span><span class="sxs-lookup"><span data-stu-id="6aacb-104">This procedure shows how to calculate the cost of a finished product by using single level explosion that is based in the Costing sheet.</span></span> <span data-ttu-id="6aacb-105">Tämä on tuoterakenteen laskentasarjan kuudes tehtävä.</span><span class="sxs-lookup"><span data-stu-id="6aacb-105">This is the sixth task in the BOM calculation series.</span></span> <span data-ttu-id="6aacb-106">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="6aacb-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="6aacb-107">Siirry Vapautetut tuotteet -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="6aacb-107">Go to Released products.</span></span>
2. <span data-ttu-id="6aacb-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="6aacb-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6aacb-109">Valitse tuotteen BOM_1.</span><span class="sxs-lookup"><span data-stu-id="6aacb-109">Select product BOM_1.</span></span>  
3. <span data-ttu-id="6aacb-110">Valitse toimintoruudussa Hallitse kustannuksia.</span><span class="sxs-lookup"><span data-stu-id="6aacb-110">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="6aacb-111">Valitse Nimikkeen hinta.</span><span class="sxs-lookup"><span data-stu-id="6aacb-111">Click Item price.</span></span>
5. <span data-ttu-id="6aacb-112">Valitse Laske nimikekustannus.</span><span class="sxs-lookup"><span data-stu-id="6aacb-112">Click Calculate item cost.</span></span>
    * <span data-ttu-id="6aacb-113">Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.</span><span class="sxs-lookup"><span data-stu-id="6aacb-113">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>  
6. <span data-ttu-id="6aacb-114">Avaa haku napsauttamalla Kustannusversio-kentässä avattavan valikon painiketta.</span><span class="sxs-lookup"><span data-stu-id="6aacb-114">In the Costing version field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6aacb-115">Valitse tässä esimerkissä 10.</span><span class="sxs-lookup"><span data-stu-id="6aacb-115">For this demo, select 10.</span></span> <span data-ttu-id="6aacb-116">Tätä kustannuslaskentaversiosta käytetään myös kustannushinnan lisäämiseen osiin.</span><span class="sxs-lookup"><span data-stu-id="6aacb-116">This is the same costing version used for adding the cost price to the components.</span></span>  
7. <span data-ttu-id="6aacb-117">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="6aacb-117">Click OK.</span></span>
8. <span data-ttu-id="6aacb-118">Valitse Näytä laskennan tiedot.</span><span class="sxs-lookup"><span data-stu-id="6aacb-118">Click View calculation details.</span></span>
    * <span data-ttu-id="6aacb-119">Asetus ei ehkä ole päävalikossa näkyvissä, ennen kuin ellipsipainiketta (...) napsautetaan.</span><span class="sxs-lookup"><span data-stu-id="6aacb-119">You may need to click the ellipsis (...) to see this option in the top menu.</span></span>    <span data-ttu-id="6aacb-120">Kustannuksen kokoonpano:  •    10 johdetaan kohteesta ITEM_A, 10 kohteesta ITEM_B, 10 kohteesta BOM_2.</span><span class="sxs-lookup"><span data-stu-id="6aacb-120">Here's the composition of the cost:  •    10 is derived from ITEM_A, 10 from ITEM_B, 10 from BOM_2.</span></span> <span data-ttu-id="6aacb-121">Tässä tapauksessa kohteen BOM_2 tietoja ei ole, koska se annettiin standardikustannuksena 10 eikä sitä saatu laskemalla.</span><span class="sxs-lookup"><span data-stu-id="6aacb-121">In this case there are no details for BOM_2 because it was entered as a standard cost of 10 but not done through calculation.</span></span>  <span data-ttu-id="6aacb-122">•  7 johdetaan asetusajasta, joka on vakiokustannus, ja ylimääräinen 7 johdetaan ajoaikatyövaiheesta (prosessi).</span><span class="sxs-lookup"><span data-stu-id="6aacb-122">•  7 is derived from the setup time, which is a constant cost, and additional 7 is derived from the run-time operation (Process).</span></span>  <span data-ttu-id="6aacb-123">•   Lisäksi on epäsuoria kustannuksia vastaavia summia.</span><span class="sxs-lookup"><span data-stu-id="6aacb-123">•   There are also other amounts that correspond to indirect costs.</span></span>  
9. @SysTaskRecorder:_RequestClose


