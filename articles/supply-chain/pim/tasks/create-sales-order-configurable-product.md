--- 
title: "Myyntitilauksen luominen määritettävälle tuotteelle"
description: "Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen."
author: ShylaThompson
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: f00eb49a7f4c664a523f0646d0c9fc56625e10a6
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="3db1f-103">Myyntitilauksen luominen määritettävälle tuotteelle</span><span class="sxs-lookup"><span data-stu-id="3db1f-103">Create a sales order for a configurable product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3db1f-104">Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="3db1f-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="3db1f-105">Tämä esimerkki käyttää USMF-yrityksen demotietojen kaiutinmallia D0006.</span><span class="sxs-lookup"><span data-stu-id="3db1f-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="3db1f-106">Nämä toimet suorittaa yleensä myyntitilausten käsittelijä.</span><span class="sxs-lookup"><span data-stu-id="3db1f-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="3db1f-107">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="3db1f-107">Create a sales order</span></span>
1. <span data-ttu-id="3db1f-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="3db1f-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="3db1f-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="3db1f-109">Click New.</span></span>
3. <span data-ttu-id="3db1f-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="3db1f-110">Click Sales order.</span></span>
4. <span data-ttu-id="3db1f-111">Valitse Asiakastili-kentässä US-001.</span><span class="sxs-lookup"><span data-stu-id="3db1f-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="3db1f-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3db1f-112">Click OK.</span></span>
6. <span data-ttu-id="3db1f-113">Valitse Nimiketunnus-kenttään D0006.</span><span class="sxs-lookup"><span data-stu-id="3db1f-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="3db1f-114">Tätä tehtävää varten on valittava määritettävissä oleva tuote.</span><span class="sxs-lookup"><span data-stu-id="3db1f-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="3db1f-115">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="3db1f-115">Click Product and supply.</span></span>
8. <span data-ttu-id="3db1f-116">Napsauta Konfiguroi rivi.</span><span class="sxs-lookup"><span data-stu-id="3db1f-116">Click Configure line.</span></span>
    * <span data-ttu-id="3db1f-117">Huomaa, että hinta on muuttunut valitun konfiguraation perusteella, ja Kaapeli mukana -kenttä on nyt arvoltaan Tosi.</span><span class="sxs-lookup"><span data-stu-id="3db1f-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="3db1f-118">Pidä mielessä oletushinta ja kaapelille valitut asetukset.</span><span class="sxs-lookup"><span data-stu-id="3db1f-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="3db1f-119">Valitse Lataa malli.</span><span class="sxs-lookup"><span data-stu-id="3db1f-119">Click Load template.</span></span>
    * <span data-ttu-id="3db1f-120">Tässä esimerkissä näytetään, miten voit käyttää mallia esimääritetyn konfiguraation valinnassa.</span><span class="sxs-lookup"><span data-stu-id="3db1f-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="3db1f-121">Jos käytät tätä menettelyä tehtäväoppaana ja haluat nähdä käytettävissä olevat määritearvot, paina Poista lukitus -painiketta.</span><span class="sxs-lookup"><span data-stu-id="3db1f-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="3db1f-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3db1f-122">Click OK.</span></span>
11. <span data-ttu-id="3db1f-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="3db1f-123">Click OK.</span></span>
12. <span data-ttu-id="3db1f-124">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="3db1f-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="3db1f-125">Valitse Tuote-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3db1f-125">Click the Product tab.</span></span>
    * <span data-ttu-id="3db1f-126">Nimikkeen konfigurointi näytetään nyt tuotedimensioissa.</span><span class="sxs-lookup"><span data-stu-id="3db1f-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="3db1f-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="3db1f-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="3db1f-128">Valitse tuotteen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="3db1f-128">Select the product configuration</span></span>


