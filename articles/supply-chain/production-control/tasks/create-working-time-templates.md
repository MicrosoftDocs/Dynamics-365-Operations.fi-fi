---
title: Työaikamallien luominen
description: Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920926"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="5b476-103">Työaikamallien luominen</span><span class="sxs-lookup"><span data-stu-id="5b476-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b476-104">Työaikamallit määrittävät koko viikon työtunnit ja niiden avulla luodaan työajat tietylle ajanjaksolle.</span><span class="sxs-lookup"><span data-stu-id="5b476-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="5b476-105">Tässä menettelyssä käsitellään, miten työaikamalli määritetään käyttämällä työaikojen aikavälien luokittelun ajoitusominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="5b476-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="5b476-106">Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="5b476-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="5b476-107">Siirry kohtaan **Työtilat > Resurssin elinkaaren hallinta**.</span><span class="sxs-lookup"><span data-stu-id="5b476-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="5b476-108">Valitse **Työaikamallit**.</span><span class="sxs-lookup"><span data-stu-id="5b476-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="5b476-109">Luo työaikamalli</span><span class="sxs-lookup"><span data-stu-id="5b476-109">Create working time template</span></span>

1. <span data-ttu-id="5b476-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5b476-110">Select **New**.</span></span>
1. <span data-ttu-id="5b476-111">Kirjoita **Työaikamalli**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5b476-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="5b476-112">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5b476-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="5b476-113">Laajenna **Maanantai**-osa.</span><span class="sxs-lookup"><span data-stu-id="5b476-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="5b476-114">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5b476-114">Select **Add**.</span></span>
1. <span data-ttu-id="5b476-115">Anna aika **Alkaen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="5b476-116">Määritä aika, jolloin työ alkaa aamulla.</span><span class="sxs-lookup"><span data-stu-id="5b476-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="5b476-117">Anna aika **Asti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="5b476-118">Määritä työntekijöiden lounastauon aika.</span><span class="sxs-lookup"><span data-stu-id="5b476-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="5b476-119">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="5b476-119">Select **Add**.</span></span>
1. <span data-ttu-id="5b476-120">Anna aika **Alkaen**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="5b476-121">Määritä aika, jolloin työ jatkuu lounaan jälkeen.</span><span class="sxs-lookup"><span data-stu-id="5b476-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="5b476-122">Anna aika **Asti**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="5b476-123">Määritä, milloin työpäivä päättyy.</span><span class="sxs-lookup"><span data-stu-id="5b476-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="5b476-124">Replikoi työajat kaikkiin viikonpäiviin</span><span class="sxs-lookup"><span data-stu-id="5b476-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="5b476-125">Valitse **Kopioi päivä**.</span><span class="sxs-lookup"><span data-stu-id="5b476-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="5b476-126">Kopioi työaikojen määritykset maanantaista tiistaille.</span><span class="sxs-lookup"><span data-stu-id="5b476-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="5b476-127">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b476-127">Select **OK**.</span></span>
1. <span data-ttu-id="5b476-128">Valitse **Kopioi päivä**.</span><span class="sxs-lookup"><span data-stu-id="5b476-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="5b476-129">Kopioi työaikojen määritykset maanantaista keskiviikolle.</span><span class="sxs-lookup"><span data-stu-id="5b476-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="5b476-130">Valitse vaihtoehto **Arkipäivään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="5b476-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b476-131">Select **OK**.</span></span>
1. <span data-ttu-id="5b476-132">Valitse **Kopioi päivä**.</span><span class="sxs-lookup"><span data-stu-id="5b476-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="5b476-133">Kopioi työaikojen määritykset maanantaista torstaille.</span><span class="sxs-lookup"><span data-stu-id="5b476-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="5b476-134">Valitse vaihtoehto **Arkipäivään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="5b476-135">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b476-135">Select **OK**.</span></span>
1. <span data-ttu-id="5b476-136">Valitse **Kopioi päivä**.</span><span class="sxs-lookup"><span data-stu-id="5b476-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="5b476-137">Kopioi työaikojen määritykset maanantaista perjantaille.</span><span class="sxs-lookup"><span data-stu-id="5b476-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="5b476-138">Valitse vaihtoehto **Arkipäivään**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5b476-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="5b476-139">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b476-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="5b476-140">Määritä erityistyövaiheiden ajankohdat</span><span class="sxs-lookup"><span data-stu-id="5b476-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="5b476-141">Laajenna **Perjantai**-osa.</span><span class="sxs-lookup"><span data-stu-id="5b476-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="5b476-142">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5b476-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5b476-143">Anna tai valitse **Ominaisuus**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="5b476-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="5b476-144">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5b476-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="5b476-145">Anna tai valitse **Ominaisuus**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="5b476-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="5b476-146">Merkitse viikonlopun päivät noudolta suljetuksi</span><span class="sxs-lookup"><span data-stu-id="5b476-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="5b476-147">Laajenna **Lauantai**-osa.</span><span class="sxs-lookup"><span data-stu-id="5b476-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="5b476-148">Valitse **Suljettu noudolta** -kentässä *Kyllä* .</span><span class="sxs-lookup"><span data-stu-id="5b476-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="5b476-149">Laajenna **Sunnuntai**-osa.</span><span class="sxs-lookup"><span data-stu-id="5b476-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="5b476-150">Valitse **Suljettu noudolta** -kentässä *Kyllä* .</span><span class="sxs-lookup"><span data-stu-id="5b476-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]