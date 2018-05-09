--- 
title: Virkavapaan hallinta
description: "Tässä menettelyssä esitellään työntekijän lomatietueiden luominen."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dda5b8e1f970a0de4c362cb825947f0fde4f41d9
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="7f8c8-103">Virkavapaan hallinta</span><span class="sxs-lookup"><span data-stu-id="7f8c8-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f8c8-104">Tässä menettelyssä esitellään työntekijän lomatietueiden luominen.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="7f8c8-105">Voit seurata loma-aikaa, jos syy liittyy terveyteen, koulutukseen tai vanhemmuuteen.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="7f8c8-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="7f8c8-107">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="7f8c8-108">Valitse luettelosta työntekijä.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="7f8c8-109">Näytä valitun työntekijän yksityiskohtaiset tiedot valitsemalla työntekijän nimi.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="7f8c8-110">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="7f8c8-111">Valitse Loma.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-111">Click Leave.</span></span>
6. <span data-ttu-id="7f8c8-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-112">Click New.</span></span>
7. <span data-ttu-id="7f8c8-113">Avaa haku valitsemalla Lomatyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7f8c8-114">Lomatyypit-lomakkeessa voit liittää lomatyypin ansiokoodiin.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="7f8c8-115">Jos lomatyyppi on liitetty ansiokoodiin, ansiorivi luodaan liittyvän ansiokoodin kanssa syöttämäsi lomakauden aikana.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="7f8c8-116">Valitse lomatyyppi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="7f8c8-117">Esimerkki: Adoptio</span><span class="sxs-lookup"><span data-stu-id="7f8c8-117">For example: Adoption</span></span>  
9. <span data-ttu-id="7f8c8-118">Syötä loman alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="7f8c8-119">Esimerkki: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="7f8c8-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="7f8c8-120">Esimerkki: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="7f8c8-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="7f8c8-121">Syötä loman alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="7f8c8-122">Esimerkki: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="7f8c8-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="7f8c8-123">Syötä huomautuskenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="7f8c8-124">Esimerkki: Adoptioloma</span><span class="sxs-lookup"><span data-stu-id="7f8c8-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="7f8c8-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7f8c8-125">Click Save.</span></span>


