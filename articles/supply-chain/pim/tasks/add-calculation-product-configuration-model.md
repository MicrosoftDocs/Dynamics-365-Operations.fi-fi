---
title: Lisää laskelma tuotemääritysmalliin
description: Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 268baa4b518f6df52d4393f7278a79cbe1733844
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812668"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="520f9-103">Lisää laskelma tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="520f9-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="520f9-104">Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="520f9-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="520f9-105">Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille.</span><span class="sxs-lookup"><span data-stu-id="520f9-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="520f9-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="520f9-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="520f9-107">Lisää laskelma</span><span class="sxs-lookup"><span data-stu-id="520f9-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="520f9-108">Luo laskelmalauseke</span><span class="sxs-lookup"><span data-stu-id="520f9-108">Create calculation expression</span></span>
1. <span data-ttu-id="520f9-109">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="520f9-109">Click Edit expression.</span></span>
2. <span data-ttu-id="520f9-110">Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="520f9-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="520f9-111">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="520f9-111">Click Validate.</span></span>
4. <span data-ttu-id="520f9-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="520f9-112">Click Close.</span></span>
5. <span data-ttu-id="520f9-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="520f9-113">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]