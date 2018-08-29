--- 
title: Muokkaa toimien raportointisuhteita
description: "Tässä menettelyssä näytetään, miten työntekijän raportointisuhde muutetaan."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 2e52552ec5bce957ac43c2e34ac9a0e42829accd
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---
# <a name="modify-the-reporting-relationships-for-positions"></a><span data-ttu-id="16dab-103">Muokkaa toimien raportointisuhteita</span><span class="sxs-lookup"><span data-stu-id="16dab-103">Modify the reporting relationships for positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="16dab-104">Tässä menettelyssä näytetään, miten työntekijän raportointisuhde muutetaan.</span><span class="sxs-lookup"><span data-stu-id="16dab-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="16dab-105">Asiakirjoja voi reitittää työnkulussa raportointisuhteen avulla.</span><span class="sxs-lookup"><span data-stu-id="16dab-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="16dab-106">Menettelyssä näytetään myös, miten työntekijä määritetään lisähierarkioihin.</span><span class="sxs-lookup"><span data-stu-id="16dab-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="16dab-107">Työntekijä voi esimerkiksi kuulua projektiryhmään ja hänellä voi olla epävirallinen raportointisuhde projektivastaavaan.</span><span class="sxs-lookup"><span data-stu-id="16dab-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="16dab-108">Toimelle voidaan määrittää lisäraportointisuhteita erilaisten projekti- tai matriisiskenaarioiden tarpeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="16dab-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="16dab-109">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="16dab-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="16dab-110">Valitse Henkilöstöhallinto > Toimet > Toimet.</span><span class="sxs-lookup"><span data-stu-id="16dab-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="16dab-111">Käytä pikasuodatinta tietueiden etsimiseen.</span><span class="sxs-lookup"><span data-stu-id="16dab-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="16dab-112">Voit esimerkiksi suodattaa Toimi-kenttää arvolla 000091.</span><span class="sxs-lookup"><span data-stu-id="16dab-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="16dab-113">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="16dab-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="16dab-114">Laajenna Raportoi toimelle -osa.</span><span class="sxs-lookup"><span data-stu-id="16dab-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="16dab-115">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="16dab-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="16dab-116">Anna tai valitse Raportoi:-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="16dab-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="16dab-117">Valitse Luo.</span><span class="sxs-lookup"><span data-stu-id="16dab-117">Click Create.</span></span>
8. <span data-ttu-id="16dab-118">Laajenna Suhteet-osa.</span><span class="sxs-lookup"><span data-stu-id="16dab-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="16dab-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="16dab-119">Click Add.</span></span>
10. <span data-ttu-id="16dab-120">Valitse valintaruutu ruudukossa vasemmalta.</span><span class="sxs-lookup"><span data-stu-id="16dab-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="16dab-121">Anna tai valitse Hierarkian nimi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="16dab-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="16dab-122">Esimerkki: projekti</span><span class="sxs-lookup"><span data-stu-id="16dab-122">Example: Project</span></span>  
12. <span data-ttu-id="16dab-123">Anna tai valitse Raportoi toimelle -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="16dab-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="16dab-124">Esimerkki: 000437</span><span class="sxs-lookup"><span data-stu-id="16dab-124">Example:  000437</span></span>
13. <span data-ttu-id="16dab-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="16dab-125">Click Save.</span></span>


