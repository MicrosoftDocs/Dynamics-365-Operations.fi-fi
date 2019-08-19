---
title: Lisää laskelma tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39450b5aef2fb7b57492a52011f4b0db9dc8ff2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845038"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="1d0cc-103">Lisää laskelma tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="1d0cc-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d0cc-104">Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="1d0cc-105">Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="1d0cc-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="1d0cc-107">Lisää laskelma</span><span class="sxs-lookup"><span data-stu-id="1d0cc-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="1d0cc-108">Luo laskelmalauseke</span><span class="sxs-lookup"><span data-stu-id="1d0cc-108">Create calculation expression</span></span>
1. <span data-ttu-id="1d0cc-109">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-109">Click Edit expression.</span></span>
2. <span data-ttu-id="1d0cc-110">Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="1d0cc-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="1d0cc-111">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-111">Click Validate.</span></span>
4. <span data-ttu-id="1d0cc-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-112">Click Close.</span></span>
5. <span data-ttu-id="1d0cc-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-113">Click OK.</span></span>

