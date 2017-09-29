--- 
title: "Työaikamallien luominen"
description: "Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle."
author: sorenva
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
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="c4b8b-103">Työaikamallien luominen</span><span class="sxs-lookup"><span data-stu-id="c4b8b-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4b8b-104">Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="c4b8b-105">Tässä menettelyssä käsitellään, miten työaikamalli määritetään käyttämällä työaikojen aikavälien luokittelun ajoitusominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="c4b8b-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="c4b8b-107">Siirry kohtaan Kaikki työtilat > Resurssin elinkaaren hallinta.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="c4b8b-108">Valitse Työaikamallit.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="c4b8b-109">Luo työaikamalli</span><span class="sxs-lookup"><span data-stu-id="c4b8b-109">Create working time template</span></span>
1. <span data-ttu-id="c4b8b-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-110">Click New.</span></span>
2. <span data-ttu-id="c4b8b-111">Kirjoita Työaikamalli-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="c4b8b-112">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c4b8b-113">Laajenna Maanantai-osa.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="c4b8b-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-114">Click Add.</span></span>
6. <span data-ttu-id="c4b8b-115">Anna aika Alkaen-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="c4b8b-116">Määritä aika, jolloin työ alkaa aamulla.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="c4b8b-117">Anna aika Asti-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="c4b8b-118">Määritä työntekijöiden lounastauon aika.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="c4b8b-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-119">Click Add.</span></span>
9. <span data-ttu-id="c4b8b-120">Anna aika Alkaen-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="c4b8b-121">Määritä aika, jolloin työ jatkuu lounaan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="c4b8b-122">Anna aika Asti-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="c4b8b-123">Määritä, milloin työpäivä päättyy.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="c4b8b-124">Replikoi työajat kaikkiin viikonpäiviin</span><span class="sxs-lookup"><span data-stu-id="c4b8b-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="c4b8b-125">Valitse Kopioi päivä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-125">Click Copy day.</span></span>
    * <span data-ttu-id="c4b8b-126">Kopioi työaikojen määritykset maanantaista tiistaille.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="c4b8b-127">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-127">Click OK.</span></span>
3. <span data-ttu-id="c4b8b-128">Valitse Kopioi päivä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-128">Click Copy day.</span></span>
    * <span data-ttu-id="c4b8b-129">Kopioi työaikojen määritykset maanantaista keskiviikolle.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="c4b8b-130">Valitse vaihtoehto Arkipäivään-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="c4b8b-131">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-131">Click OK.</span></span>
6. <span data-ttu-id="c4b8b-132">Valitse Kopioi päivä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-132">Click Copy day.</span></span>
    * <span data-ttu-id="c4b8b-133">Kopioi työaikojen määritykset maanantaista torstaille.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="c4b8b-134">Valitse vaihtoehto Arkipäivään-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="c4b8b-135">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-135">Click OK.</span></span>
9. <span data-ttu-id="c4b8b-136">Valitse Kopioi päivä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-136">Click Copy day.</span></span>
    * <span data-ttu-id="c4b8b-137">Kopioi työaikojen määritykset maanantaista perjantaille.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="c4b8b-138">Valitse vaihtoehto Arkipäivään-kentässä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="c4b8b-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="c4b8b-140">Määritä erityistyövaiheiden ajankohdat</span><span class="sxs-lookup"><span data-stu-id="c4b8b-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="c4b8b-141">Laajenna Perjantai-osa.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="c4b8b-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c4b8b-143">Anna tai valitse Ominaisuus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="c4b8b-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c4b8b-145">Anna tai valitse Ominaisuus-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="c4b8b-146">Merkitse viikonlopun päivät noudolta suljetuksi</span><span class="sxs-lookup"><span data-stu-id="c4b8b-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="c4b8b-147">Laajenna Lauantai-osa.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="c4b8b-148">Valitse Suljettu noudolta -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="c4b8b-149">Laajenna Sunnuntai-osa.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="c4b8b-150">Valitse Suljettu noudolta -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="c4b8b-150">Select Yes in the Closed for pickup field.</span></span>


