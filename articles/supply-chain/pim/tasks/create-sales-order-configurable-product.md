---
title: Myyntitilauksen luominen määritettävälle tuotteelle
description: Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, PCRuntimeConfigurator, PCTemplateConfigurationSelection
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e69fd2aa04a65d64db4d34f1839a01fb0f8e018
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213190"
---
# <a name="create-a-sales-order-for-a-configurable-product"></a><span data-ttu-id="4e2e1-103">Myyntitilauksen luominen määritettävälle tuotteelle</span><span class="sxs-lookup"><span data-stu-id="4e2e1-103">Create a sales order for a configurable product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e2e1-104">Tämä menettely osoittaa, miten konfiguraatiomallia käytetään myyntitilauksen tuotteeseen.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-104">This procedure shows how to apply a configuration template to a product on a sales order.</span></span> <span data-ttu-id="4e2e1-105">Tämä esimerkki käyttää USMF-yrityksen demotietojen kaiutinmallia D0006.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-105">This example uses the D0006 speaker model in the USMF demo data company.</span></span> <span data-ttu-id="4e2e1-106">Nämä toimet suorittaa yleensä myyntitilausten käsittelijä.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-106">Typically, a sales order processor uses this procedure.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="4e2e1-107">Luo myyntitilaus</span><span class="sxs-lookup"><span data-stu-id="4e2e1-107">Create a sales order</span></span>
1. <span data-ttu-id="4e2e1-108">Valitse Myyntitilausten käsittely ja kysely.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-108">Click Sales order processing and inquiry.</span></span>
2. <span data-ttu-id="4e2e1-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-109">Click New.</span></span>
3. <span data-ttu-id="4e2e1-110">Valitse Myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-110">Click Sales order.</span></span>
4. <span data-ttu-id="4e2e1-111">Valitse Asiakastili-kentässä US-001.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-111">In the Customer account field, select US-001.</span></span> 
5. <span data-ttu-id="4e2e1-112">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-112">Click OK.</span></span>
6. <span data-ttu-id="4e2e1-113">Valitse Nimiketunnus-kenttään D0006.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-113">In the Item number field, select D0006.</span></span>
    * <span data-ttu-id="4e2e1-114">Tätä tehtävää varten on valittava määritettävissä oleva tuote.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-114">For this task, you must select a configurable product.</span></span>  
7. <span data-ttu-id="4e2e1-115">Valitse Tuote ja toimitus.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-115">Click Product and supply.</span></span>
8. <span data-ttu-id="4e2e1-116">Napsauta Konfiguroi rivi.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-116">Click Configure line.</span></span>
    * <span data-ttu-id="4e2e1-117">Huomaa, että hinta on muuttunut valitun konfiguraation perusteella, ja Kaapeli mukana -kenttä on nyt arvoltaan Tosi.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-117">Note that the price has changed, based on the configuration that was selected, and that the Include cable field is now set to True.</span></span>  
    * <span data-ttu-id="4e2e1-118">Pidä mielessä oletushinta ja kaapelille valitut asetukset.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-118">Note the default price and the settings that are selected for the cable.</span></span>  
9. <span data-ttu-id="4e2e1-119">Valitse Lataa malli.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-119">Click Load template.</span></span>
    * <span data-ttu-id="4e2e1-120">Tässä esimerkissä näytetään, miten voit käyttää mallia esimääritetyn konfiguraation valinnassa.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-120">This example shows how you can apply a template to select a predefined configuration.</span></span> <span data-ttu-id="4e2e1-121">Jos käytät tätä menettelyä tehtäväoppaana ja haluat nähdä käytettävissä olevat määritearvot, paina Poista lukitus -painiketta.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-121">If you're using this procedure as a task guide and want to see the other attribute values that are available, you must click the Unlock button.</span></span>  
10. <span data-ttu-id="4e2e1-122">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-122">Click OK.</span></span>
11. <span data-ttu-id="4e2e1-123">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-123">Click OK.</span></span>
12. <span data-ttu-id="4e2e1-124">Laajenna Rivin erittely -osa.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-124">Expand the Line details section.</span></span>
13. <span data-ttu-id="4e2e1-125">Valitse Tuote-välilehti.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-125">Click the Product tab.</span></span>
    * <span data-ttu-id="4e2e1-126">Nimikkeen konfigurointi näytetään nyt tuotedimensioissa.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-126">The configuration of the item is now listed under the product dimensions.</span></span>  
14. <span data-ttu-id="4e2e1-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-127">Close the page.</span></span>

## <a name="select-the-product-configuration"></a><span data-ttu-id="4e2e1-128">Valitse tuotteen konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="4e2e1-128">Select the product configuration</span></span>

