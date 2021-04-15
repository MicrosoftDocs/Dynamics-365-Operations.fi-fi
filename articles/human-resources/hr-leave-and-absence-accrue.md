---
title: Jaksota loma- ja poissaolosuunnitelmat
description: Voit jaksottaa lomaa ja poissaoloa Dynamics 365 Human Resourcesissa useille työntekijöille tai yksittäisille henkilöille.
author: andreabichsel
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 53c089da64f6b5f950a92afb9246454fb9a9686d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800258"
---
# <a name="accrue-leave-and-absence-plans"></a><span data-ttu-id="7fa3d-103">Jaksota loma- ja poissaolosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="7fa3d-103">Accrue leave and absence plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7fa3d-104">Voit jaksottaa lomaa ja poissaoloa Dynamics 365 Human Resourcesissa useille työntekijöille tai yksittäisille henkilöille.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-104">You can accrue leave and absence in Dynamics 365 Human Resources for multiple employees or for an individual.</span></span>

## <a name="accrue-leave-and-absence-for-multiple-employees"></a><span data-ttu-id="7fa3d-105">Useiden työntekijöiden kertyneet lomat ja poissaolot</span><span class="sxs-lookup"><span data-stu-id="7fa3d-105">Accrue leave and absence for multiple employees</span></span>

1. <span data-ttu-id="7fa3d-106">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-106">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7fa3d-107">Valitse **Hallitse lomia** -kohdassa **Jaksota loma- ja poissaolosuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-107">Under **Manage leave**, select **Accrue leave and absence plans**.</span></span>

3. <span data-ttu-id="7fa3d-108">**Kertyneiden lomien ja poissaolojen suunnitelmat** -valintaikkuna tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-108">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="7fa3d-109">Valitse **Kertymä**-kohdasta joko **Kuluvan päivän päivämäärä** tai valitse **Mukautettu päivämäärä** ja syötä mukautettu päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-109">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="7fa3d-110">Jos haluat suorittaa jaksotukset kaikissa yrityksissä, valitse **Kaikki yritykset**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-110">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="7fa3d-111">Jos haluat käsitellä yhden lomasuunnitelman jaksotukset, valitse **Kaikki suunnitelmat** -asetukseksi **Ei** ja valitse sitten **Lomasuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-111">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="7fa3d-112">Jos valitset kaikki yritykset, et voi valita yksittäistä lomasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-112">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="7fa3d-113">Jos haluat suorittaa jaksotusprosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="7fa3d-113">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="7fa3d-114">Määritä jaksotusprosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-114">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="7fa3d-115">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-115">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="7fa3d-116">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-116">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="7fa3d-117">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-117">Select **OK**.</span></span> <span data-ttu-id="7fa3d-118">Jaksotusprosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-118">The accrual process will run with the parameters you set.</span></span>

## <a name="accrue-leave-and-absence-for-an-employee"></a><span data-ttu-id="7fa3d-119">Työntekijän kertyneet lomat ja poissaolot</span><span class="sxs-lookup"><span data-stu-id="7fa3d-119">Accrue leave and absence for an employee</span></span>

1. <span data-ttu-id="7fa3d-120">Valitse työntekijän tietueesta **Loma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-120">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="7fa3d-121">Valitse **Jaksota lomat ja poissaolot**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-121">Select **Accrue leave and absence**.</span></span>

3. <span data-ttu-id="7fa3d-122">**Kertyneiden lomien ja poissaolojen suunnitelmat** -valintaikkuna tulee näyttöön.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-122">The **Accrue leave and absence plans** dialog box appears.</span></span> <span data-ttu-id="7fa3d-123">Valitse **Kertymä**-kohdasta joko **Kuluvan päivän päivämäärä** tai valitse **Mukautettu päivämäärä** ja syötä mukautettu päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-123">In **Accrue as of**, either select **Today's date** or select **Custom date** and enter a custom date.</span></span>

4. <span data-ttu-id="7fa3d-124">Jos haluat suorittaa jaksotukset kaikissa yrityksissä, valitse **Kaikki yritykset**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-124">If you want to run accruals for all companies, select **All companies**.</span></span> <span data-ttu-id="7fa3d-125">Jos haluat käsitellä yhden lomasuunnitelman jaksotukset, valitse **Kaikki suunnitelmat** -asetukseksi **Ei** ja valitse sitten **Lomasuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-125">If you want to process accruals for a single leave plan, select **No** for **All plans**, and then select a **Leave plan**.</span></span> <span data-ttu-id="7fa3d-126">Jos valitset kaikki yritykset, et voi valita yksittäistä lomasuunnitelmaa.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-126">If you select all companies, you can't select an individual leave plan.</span></span> 

5. <span data-ttu-id="7fa3d-127">Jos haluat suorittaa jaksotusprosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="7fa3d-127">If you want to run the accrual process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="7fa3d-128">Määritä jaksotusprosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-128">Enter information for the accrual process.</span></span>

   2. <span data-ttu-id="7fa3d-129">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-129">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="7fa3d-130">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-130">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="7fa3d-131">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-131">Select **OK**.</span></span> <span data-ttu-id="7fa3d-132">Jaksotusprosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-132">The accrual process will run with the parameters you set.</span></span>

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a><span data-ttu-id="7fa3d-133">Poista useiden työntekijöiden kertyneet lomat ja poissaolot</span><span class="sxs-lookup"><span data-stu-id="7fa3d-133">Delete leave and absence accruals for multiple employees</span></span>

<span data-ttu-id="7fa3d-134">Poista tietyn suunnitelman ja päivämäärävälin jaksotustiedot.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-134">Delete accrual records for a specific plan and date range.</span></span> <span data-ttu-id="7fa3d-135">Jaksotuspäivämäärät on päivättävä tälle päivälle tai tulevaisuuteen.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-135">Accrual dates must be dated today or in the future.</span></span>

1. <span data-ttu-id="7fa3d-136">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-136">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7fa3d-137">Valitse **Hallitse lomia** -kohdassa **Poista loma- ja poissaolosuunnitelmien kertymät**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-137">Under **Manage leave**, select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="7fa3d-138">Valitse **Poista loma- ja poissaolosuunnitelman kertymät** -valintaikkunasta **Lomasuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-138">In the **Delete leave and absence plan accruals** dialog box, select the **Leave plan**.</span></span> 

4. <span data-ttu-id="7fa3d-139">Valitse tarvittaessa **Poista saldo-oikaisut**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-139">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="7fa3d-140">Kirjoita tai valitse **Loman jaksotuspäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-140">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="7fa3d-141">Tämän päivän on oltava joko tänään tai tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-141">This date has to be either today or in the future.</span></span> 

6. <span data-ttu-id="7fa3d-142">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-142">Select **OK**.</span></span> <span data-ttu-id="7fa3d-143">Jaksotusprosessi poistaa kertymät määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-143">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a><span data-ttu-id="7fa3d-144">Poista yhden työntekijän kertyneet lomat ja poissaolot</span><span class="sxs-lookup"><span data-stu-id="7fa3d-144">Delete leave and absence accruals for a single employee</span></span>

1. <span data-ttu-id="7fa3d-145">Valitse työntekijän tietueesta **Loma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-145">On the employee's record, select **Leave**.</span></span>

2. <span data-ttu-id="7fa3d-146">Valitse **Poista loma- ja poissaolosuunnitelman jaksotukset**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-146">Select **Delete leave and absence plan accruals**.</span></span>

3. <span data-ttu-id="7fa3d-147">Valitse **Poista loma- ja poissaolosuunnitelman kertymät** -valintaikkunasta **Lomasuunnitelma**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-147">In the **Delete leave and absence plan accruals** dialog box, select **Leave plan**.</span></span> 

4. <span data-ttu-id="7fa3d-148">Valitse tarvittaessa **Poista saldo-oikaisut**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-148">If applicable, choose **Delete balance adjustments**.</span></span>

5. <span data-ttu-id="7fa3d-149">Kirjoita tai valitse **Loman jaksotuspäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-149">Enter or select a **Leave accrual date**.</span></span> <span data-ttu-id="7fa3d-150">Tämän päivän on oltava joko tänään tai tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-150">This date must be either today or in the future.</span></span> 

6. <span data-ttu-id="7fa3d-151">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-151">Select **OK**.</span></span> <span data-ttu-id="7fa3d-152">Jaksotusprosessi poistaa kertymät määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-152">The accrual process will delete accruals with the parameters you set.</span></span> 

## <a name="review-leave-accrual-and-deletion-processes"></a><span data-ttu-id="7fa3d-153">Loman kertymä- ja poistoprosessien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="7fa3d-153">Review leave accrual and deletion processes</span></span>

<span data-ttu-id="7fa3d-154">**Lomakertymän valvonta** näyttää aina, kun suoritat tai poistat yhden tai kaikkien työntekijöiden kertymän.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-154">**Leave accrual audit** displays each time you run or delete an accrual for one or all employees.</span></span> <span data-ttu-id="7fa3d-155">Myös toimenpiteen päiväys ja suorittanut henkilö näytetään.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-155">The date and person who performed the action also displays.</span></span>

1. <span data-ttu-id="7fa3d-156">Valitse **Lomat ja poissaolot** -sivulla **Linkit**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-156">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7fa3d-157">Valitse **Hallitse lomia** -kohdassa **Poista lomakertymien valvonta**.</span><span class="sxs-lookup"><span data-stu-id="7fa3d-157">Under **Manage leave**, select **Delete leave accrual audit**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7fa3d-158">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="7fa3d-158">See also</span></span>

[<span data-ttu-id="7fa3d-159">Lomien ja poissaolojen yhteenveto</span><span class="sxs-lookup"><span data-stu-id="7fa3d-159">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)</br>
[<span data-ttu-id="7fa3d-160">Loma- ja poissaolosuunnitelman luominen</span><span class="sxs-lookup"><span data-stu-id="7fa3d-160">Create a leave and absence plan</span></span>](hr-leave-and-absence-plans.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]