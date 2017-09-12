--- 
title: "Myyntitilauksen luominen määritettävälle tuotteelle"
description: "Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen."
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7084c3749f18e4fbe90fe4e04bdeac320cefeafa
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="ea5cc-103">Myyntitilauksen luominen määritettävälle tuotteelle</span><span class="sxs-lookup"><span data-stu-id="ea5cc-103">Create a sales order for a configurable product</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea5cc-104">Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="ea5cc-105">Tämä esimerkki käyttää USMF-yrityksen demotietojen kaiutinmallia D0006.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="ea5cc-106">Nämä toimet suorittaa yleensä myyntitilausten käsittelijä.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="ea5cc-107">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="ea5cc-107">Create a sales order</span></span>
1. <span data-ttu-id="ea5cc-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="ea5cc-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-109">Click New.</span></span>
3. <span data-ttu-id="ea5cc-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-110">Click Sales order.</span></span>
4. <span data-ttu-id="ea5cc-111">Valitse Asiakastili-kentässä US-001.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="ea5cc-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-112">Click OK.</span></span>
6. <span data-ttu-id="ea5cc-113">Valitse Nimiketunnus-kenttään D0006.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="ea5cc-114">Tätä tehtävää varten on valittava määritettävissä oleva tuote.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="ea5cc-115">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-115">Click Product and supply.</span></span>
8. <span data-ttu-id="ea5cc-116">Napsauta Konfiguroi rivi.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-116">Click Configure line.</span></span>
    * <span data-ttu-id="ea5cc-117">Huomaa, että hinta on muuttunut valitun konfiguraation perusteella, ja Kaapeli mukana -kenttä on nyt arvoltaan Tosi.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="ea5cc-118">Pidä mielessä oletushinta ja kaapelille valitut asetukset.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="ea5cc-119">Valitse Lataa malli.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-119">Click Load template.</span></span>
    * <span data-ttu-id="ea5cc-120">Tässä esimerkissä näytetään, miten voit käyttää mallia esimääritetyn konfiguraation valinnassa.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="ea5cc-121">Jos käytät tätä menettelyä tehtäväoppaana ja haluat nähdä käytettävissä olevat määritearvot, paina Poista lukitus -painiketta.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-121">If you’re using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="ea5cc-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-122">Click OK.</span></span>
11. <span data-ttu-id="ea5cc-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-123">Click OK.</span></span>
12. <span data-ttu-id="ea5cc-124">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="ea5cc-125">Valitse Tuote-välilehti.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-125">Click the Product tab.</span></span>
    * <span data-ttu-id="ea5cc-126">Nimikkeen konfigurointi näytetään nyt tuotedimensioissa.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="ea5cc-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="ea5cc-128">Valitse tuotteen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="ea5cc-128">Select the product configuration</span></span>


