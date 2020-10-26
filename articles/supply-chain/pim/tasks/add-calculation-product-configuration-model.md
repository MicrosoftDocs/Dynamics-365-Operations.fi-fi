---
title: Lisää laskelma tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e703c6d505f1e2e77f454732301de7a6c130c58a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986500"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="a5c3e-103">Lisää laskelma tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="a5c3e-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5c3e-104">Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="a5c3e-105">Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="a5c3e-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="a5c3e-107">Lisää laskelma</span><span class="sxs-lookup"><span data-stu-id="a5c3e-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="a5c3e-108">Luo laskelmalauseke</span><span class="sxs-lookup"><span data-stu-id="a5c3e-108">Create calculation expression</span></span>
1. <span data-ttu-id="a5c3e-109">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-109">Click Edit expression.</span></span>
2. <span data-ttu-id="a5c3e-110">Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="a5c3e-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="a5c3e-111">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-111">Click Validate.</span></span>
4. <span data-ttu-id="a5c3e-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-112">Click Close.</span></span>
5. <span data-ttu-id="a5c3e-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="a5c3e-113">Click OK.</span></span>

