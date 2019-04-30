---
title: Virkavapaan hallinta
description: Tässä menettelyssä esitellään työntekijän lomatietueiden luominen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, HcmEmploymentLeave
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ce57495be4ae601d6ac06bb4780a2e1192dfcc5
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "859341"
---
# <a name="manage-leave-of-absence"></a><span data-ttu-id="b2aa2-103">Virkavapaan hallinta</span><span class="sxs-lookup"><span data-stu-id="b2aa2-103">Manage leave of absence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b2aa2-104">Tässä menettelyssä esitellään työntekijän lomatietueiden luominen.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-104">This procedure walks through the creation of employee leave records.</span></span> <span data-ttu-id="b2aa2-105">Voit seurata loma-aikaa, jos syy liittyy terveyteen, koulutukseen tai vanhemmuuteen.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-105">You can track leave time for reasons that include medical, educational, or parental activities.</span></span> <span data-ttu-id="b2aa2-106">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b2aa2-107">Siirry kohtaan Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-107">Go to Human resources > Workers > Employees.</span></span>
2. <span data-ttu-id="b2aa2-108">Valitse luettelosta työntekijä.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-108">In the list, select an employee.</span></span>
3. <span data-ttu-id="b2aa2-109">Näytä valitun työntekijän yksityiskohtaiset tiedot valitsemalla työntekijän nimi.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-109">Display detailed information for the selected employee by selecting the employee's name.</span></span>
4. <span data-ttu-id="b2aa2-110">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-110">Click the Employment tab.</span></span>
5. <span data-ttu-id="b2aa2-111">Valitse Loma.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-111">Click Leave.</span></span>
6. <span data-ttu-id="b2aa2-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-112">Click New.</span></span>
7. <span data-ttu-id="b2aa2-113">Avaa haku valitsemalla Lomatyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-113">In the Leave type field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b2aa2-114">Lomatyypit-lomakkeessa voit liittää lomatyypin ansiokoodiin.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-114">You can associate a leave type to an earning code in the Leave types form.</span></span> <span data-ttu-id="b2aa2-115">Jos lomatyyppi on liitetty ansiokoodiin, ansiorivi luodaan liittyvän ansiokoodin kanssa syöttämäsi lomakauden aikana.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-115">If a leave type is associated with an earning code, an earning line will be generated with the associated earning code during the leave period that you enter.</span></span>  
8. <span data-ttu-id="b2aa2-116">Valitse lomatyyppi luettelosta.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-116">In the list, select a leave type.</span></span> 
    * <span data-ttu-id="b2aa2-117">Esimerkki: Adoptio</span><span class="sxs-lookup"><span data-stu-id="b2aa2-117">For example: Adoption</span></span>  
9. <span data-ttu-id="b2aa2-118">Syötä loman alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-118">Enter the date that the leave will start.</span></span> <span data-ttu-id="b2aa2-119">Esimerkki: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="b2aa2-119">Example: '2015-10-26'</span></span>
    * <span data-ttu-id="b2aa2-120">Esimerkki: 26.10.2015</span><span class="sxs-lookup"><span data-stu-id="b2aa2-120">For example:  2015-10-26</span></span>  
10. <span data-ttu-id="b2aa2-121">Syötä loman alkamispäivä.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-121">Enter the date that the leave will start.</span></span> 
    * <span data-ttu-id="b2aa2-122">Esimerkki: 20.11.2015</span><span class="sxs-lookup"><span data-stu-id="b2aa2-122">For example:  2015-11-20</span></span>  
11. <span data-ttu-id="b2aa2-123">Syötä huomautuskenttään kuvaus.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-123">In the note field, enter a description.</span></span>
    * <span data-ttu-id="b2aa2-124">Esimerkki: Adoptioloma</span><span class="sxs-lookup"><span data-stu-id="b2aa2-124">For example: Leave for adoption</span></span>  
12. <span data-ttu-id="b2aa2-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="b2aa2-125">Click Save.</span></span>

