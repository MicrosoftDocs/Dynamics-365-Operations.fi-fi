--- 
title: "Lisää laskelma tuotemääritysmalliin"
description: "Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 01434e8dbd1e66ae04d0b7910ef2be582297ac84
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="85a96-103">Lisää laskelma tuotemääritysmalliin</span><span class="sxs-lookup"><span data-stu-id="85a96-103">Add a calculation to a product configuration model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85a96-104">Tässä menettelyssä käsitellään, miten uusi laskelma lisätään tuotemääritysmalliin.</span><span class="sxs-lookup"><span data-stu-id="85a96-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="85a96-105">Siinä näytetään, miten voit luoda loogisen lausekkeen käyttämällä jos-operaattoria määrittämään kaiutinkorkeudeksi 10 valkoisille kaiuttimille ja 15 muille kotelon pintakäsittelyille.</span><span class="sxs-lookup"><span data-stu-id="85a96-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="85a96-106">Menettely käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -komponenttia.</span><span class="sxs-lookup"><span data-stu-id="85a96-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="85a96-107">Lisää laskelma</span><span class="sxs-lookup"><span data-stu-id="85a96-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="85a96-108">Luo laskelmalauseke</span><span class="sxs-lookup"><span data-stu-id="85a96-108">Create calculation expression</span></span>
1. <span data-ttu-id="85a96-109">Valitse Muokkaa lauseketta.</span><span class="sxs-lookup"><span data-stu-id="85a96-109">Click Edit expression.</span></span>
2. <span data-ttu-id="85a96-110">Lisää ConstraintBody-kenttään If[CabinetFinish=="White", 10, 15].</span><span class="sxs-lookup"><span data-stu-id="85a96-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="85a96-111">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="85a96-111">Click Validate.</span></span>
4. <span data-ttu-id="85a96-112">Valitse Sulje.</span><span class="sxs-lookup"><span data-stu-id="85a96-112">Click Close.</span></span>
5. <span data-ttu-id="85a96-113">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="85a96-113">Click OK.</span></span>


