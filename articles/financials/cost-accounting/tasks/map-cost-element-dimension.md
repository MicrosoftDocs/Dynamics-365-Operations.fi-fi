--- 
title: "Määritä kustannustason dimensio"
description: "Kustannusten vastuuhenkilö voi käyttää tätä menettelyä kustannustason dimension vastaavuuden määrityksessä MXMF-yrityksen kustannustason dimensioon."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cfad9c5c02f5002f075e2de99eaf407b4c75f596
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="1836f-103">Määritä kustannustason dimensio</span><span class="sxs-lookup"><span data-stu-id="1836f-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1836f-104">Kustannusten vastuuhenkilö voi käyttää tätä menettelyä kustannustason dimension vastaavuuden määrityksessä MXMF-yrityksen kustannustason dimensioon.</span><span class="sxs-lookup"><span data-stu-id="1836f-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="1836f-105">Tämä tallenne käyttää esittelytietojen USP2-yritystä.</span><span class="sxs-lookup"><span data-stu-id="1836f-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="1836f-106">Valitse Kustannuslaskenta > Dimensiot > Kustannuselementin dimensiot.</span><span class="sxs-lookup"><span data-stu-id="1836f-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="1836f-107">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="1836f-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1836f-108">Valitse tässä esimerkissä Kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="1836f-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="1836f-109">Valitse Dimension yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="1836f-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="1836f-110">Valitse Määritä yhdistämismääritykset tästä dimensiosta.</span><span class="sxs-lookup"><span data-stu-id="1836f-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="1836f-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1836f-111">Click New.</span></span>
6. <span data-ttu-id="1836f-112">Syötä tai valitse arvo Dimensioon-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1836f-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="1836f-113">Valitse tässä esimerkissä MXMF-kustannustasot.</span><span class="sxs-lookup"><span data-stu-id="1836f-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="1836f-114">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1836f-114">Click New.</span></span>
8. <span data-ttu-id="1836f-115">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1836f-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1836f-116">Syötä tai valitse arvo Lähtödimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1836f-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1836f-117">Valitse tässä esimerkissä dimension jäsen 606400 Puhelinnumero- ja faksikulut.</span><span class="sxs-lookup"><span data-stu-id="1836f-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="1836f-118">Syötä tai valitse arvo Kohdedimension jäsen -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1836f-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="1836f-119">Valitse tässä esimerkissä dimension jäsen 6001004 Telefono.</span><span class="sxs-lookup"><span data-stu-id="1836f-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="1836f-120">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1836f-120">Click Save.</span></span>


