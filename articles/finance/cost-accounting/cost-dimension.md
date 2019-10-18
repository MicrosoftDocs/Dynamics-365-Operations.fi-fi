---
title: Dimensioiden luonti ja dimensiojäsenten tuonti
description: Kustannuslaskenta on riippumaton moduuli, joka edellyttää muiden moduulien päätietoja.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a7db93e1877034051b6add4c11ddfe7cd7d17e0b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187909"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="4feea-103">Dimensioiden luonti ja dimensiojäsenten tuonti</span><span class="sxs-lookup"><span data-stu-id="4feea-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4feea-104">Kustannuslaskenta on riippumaton moduuli, joka edellyttää muiden moduulien tietoja.</span><span class="sxs-lookup"><span data-stu-id="4feea-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="4feea-105">Nämä tiedot luokitellaan seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="4feea-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="4feea-106">Kustannustasot</span><span class="sxs-lookup"><span data-stu-id="4feea-106">Cost elements</span></span>
-  <span data-ttu-id="4feea-107">Kustannusobjektit</span><span class="sxs-lookup"><span data-stu-id="4feea-107">Cost objects</span></span>
-  <span data-ttu-id="4feea-108">Tilastodimensiot</span><span class="sxs-lookup"><span data-stu-id="4feea-108">Statistical dimensions</span></span>

<span data-ttu-id="4feea-109">**Kustannustaso** vastaa kustannusten kannalta merkittävää nimikettä tilikartassa.</span><span class="sxs-lookup"><span data-stu-id="4feea-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="4feea-110">**Kustannusobjekti** voi olla mikä tahansa taloushallinnon dimensio, kuten tuote, kustannuspaikka, tai projekti, jota haluat arvioida tai mitata tai kohdistaa siihen kustannuksia suoraan.</span><span class="sxs-lookup"><span data-stu-id="4feea-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="4feea-111">**Tilastodimensiota** ja sen jäseniä käytetään rekisteröitäessä ei-rahallisia merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="4feea-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="4feea-112">Tilastodimension jäseniä voidaan käyttää kohdistusperusteena esimerkiksi kustannusten jaossa ja kohdistuksessa.</span><span class="sxs-lookup"><span data-stu-id="4feea-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="4feea-113">Seuraavassa kaaviossa kuvataan kustannuslaskennassa käytettävät dimensiot.</span><span class="sxs-lookup"><span data-stu-id="4feea-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="4feea-114">[![Kustannuslaskennan dimensiot](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="4feea-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="4feea-115">Kun tiedot tuodaan kustannuslaskentaan, voit luoda sen avulla eri näkökulmia, jotka avustavat organisaation kaikkien tasojen johtajia.</span><span class="sxs-lookup"><span data-stu-id="4feea-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="4feea-116">Seuraavissa ohjeaiheissa on tietoja dimensioiden luomisesta ja dimension jäsenten tuonnista.</span><span class="sxs-lookup"><span data-stu-id="4feea-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="4feea-117">Kustannustason dimensiot</span><span class="sxs-lookup"><span data-stu-id="4feea-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="4feea-118">Kustannustasojen luonti (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="4feea-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="4feea-119">Kustannusobjektin dimensiot</span><span class="sxs-lookup"><span data-stu-id="4feea-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="4feea-120">Kustannustasojen luonti (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="4feea-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="4feea-121">Kustannustasodimension jäsenten yhdistäminen yhteiseen dimension jäsenten joukkoon</span><span class="sxs-lookup"><span data-stu-id="4feea-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="4feea-122">Kustannustason dimension määritys (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="4feea-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="4feea-123">Tilastodimension jäsenet ja tilastomittauksen lähdemallit</span><span class="sxs-lookup"><span data-stu-id="4feea-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






