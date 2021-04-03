---
title: Rekisteröintikelpoisuuden käsittely
description: Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 25699d643b3e74fe7118884457ab17314d1f9132
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466299"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="eb263-103">Rekisteröintikelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="eb263-103">Process enrollment eligibility</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eb263-104">Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="eb263-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="eb263-105">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Rekisteröintikelpoisuuden käsittely**.</span><span class="sxs-lookup"><span data-stu-id="eb263-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="eb263-106">Määritä **Suorita edun rekisteröintikelpoisuusprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="eb263-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="eb263-107">Kenttä</span><span class="sxs-lookup"><span data-stu-id="eb263-107">Field</span></span> | <span data-ttu-id="eb263-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="eb263-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="eb263-109">**Rekisteröitymiskausi**</span><span class="sxs-lookup"><span data-stu-id="eb263-109">**Enrollment period**</span></span> | <span data-ttu-id="eb263-110">Rekisteröintijakso, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="eb263-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="eb263-111">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="eb263-111">**Legal entity**</span></span> | <span data-ttu-id="eb263-112">Yritys, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="eb263-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="eb263-113">**Työntekijä**</span><span class="sxs-lookup"><span data-stu-id="eb263-113">**Worker**</span></span> | <span data-ttu-id="eb263-114">Työntekijä, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="eb263-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="eb263-115">Jos jätät tämän kentän tyhjäksi, käsitellään kaikkien työntekijöiden rekisteröintikelpoisuus.</span><span class="sxs-lookup"><span data-stu-id="eb263-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="eb263-116">**Etuussuunnitelma**</span><span class="sxs-lookup"><span data-stu-id="eb263-116">**Benefit plan**</span></span> | <span data-ttu-id="eb263-117">Etuussuunnitelma, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="eb263-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="eb263-118">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="eb263-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="eb263-119">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="eb263-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="eb263-120">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb263-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="eb263-121">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb263-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="eb263-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb263-122">Select **OK**.</span></span> <span data-ttu-id="eb263-123">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="eb263-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="eb263-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="eb263-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="eb263-125">Näytä prosessitulokset</span><span class="sxs-lookup"><span data-stu-id="eb263-125">View Process Results</span></span>

<span data-ttu-id="eb263-126">Tässä artikkelissa kerrotaan, miten kelpoisuusprosessitulokset näytetään.</span><span class="sxs-lookup"><span data-stu-id="eb263-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="eb263-127">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Prosessitulokset**.</span><span class="sxs-lookup"><span data-stu-id="eb263-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="eb263-128">**Prosessitulokset**-lomakkeessa määritetään seuraavat kentät:</span><span class="sxs-lookup"><span data-stu-id="eb263-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="eb263-129">Kenttä</span><span class="sxs-lookup"><span data-stu-id="eb263-129">Field</span></span> | <span data-ttu-id="eb263-130">kuvaus</span><span class="sxs-lookup"><span data-stu-id="eb263-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="eb263-131">**Prosessitunnus**</span><span class="sxs-lookup"><span data-stu-id="eb263-131">**Process ID**</span></span> | <span data-ttu-id="eb263-132">Työntekijän, yrityksen ja prosessiajon yksilöivä tunnus.</span><span class="sxs-lookup"><span data-stu-id="eb263-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="eb263-133">**Prosessityyppi**</span><span class="sxs-lookup"><span data-stu-id="eb263-133">**Process type**</span></span> | <span data-ttu-id="eb263-134">Tämä määrittää suoritettavan prosessin.</span><span class="sxs-lookup"><span data-stu-id="eb263-134">This identifies the process that was run.</span></span> <span data-ttu-id="eb263-135">Esimerkiksi: Ilmoittautuminen.</span><span class="sxs-lookup"><span data-stu-id="eb263-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="eb263-136">**Aikaleima**</span><span class="sxs-lookup"><span data-stu-id="eb263-136">**Time stamp**</span></span> | <span data-ttu-id="eb263-137">Kelpoisuusprosessin suoritusaika.</span><span class="sxs-lookup"><span data-stu-id="eb263-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="eb263-138">**Yritys**</span><span class="sxs-lookup"><span data-stu-id="eb263-138">**Legal entity**</span></span> | <span data-ttu-id="eb263-139">Rekisteröintiprosessin aikana määritetty yritys.</span><span class="sxs-lookup"><span data-stu-id="eb263-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="eb263-140">**Työntekijä**</span><span class="sxs-lookup"><span data-stu-id="eb263-140">**Worker**</span></span> | <span data-ttu-id="eb263-141">Käsitelty työntekijä.</span><span class="sxs-lookup"><span data-stu-id="eb263-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="eb263-142">\*\*Suunnitelma</span><span class="sxs-lookup"><span data-stu-id="eb263-142">\*\*Plan</span></span> | <span data-ttu-id="eb263-143">Etuussuunnitelma, johon rekisteröintiä yritettiin.</span><span class="sxs-lookup"><span data-stu-id="eb263-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="eb263-144">**Kelpoisuussääntö**</span><span class="sxs-lookup"><span data-stu-id="eb263-144">**Eligibility rule**</span></span> | <span data-ttu-id="eb263-145">Käsiteltävä oikeutussääntö.</span><span class="sxs-lookup"><span data-stu-id="eb263-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="eb263-146">Jos virhe ilmeni ennen tukikelpoisuuden suorittamista, se on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="eb263-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="eb263-147">Esimerkki: Jos kompensaatiota ei ole määritetty työntekijälle, oikeutusprosessia ei suoriteta, ja tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="eb263-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="eb263-148">**Tuloksen tila**</span><span class="sxs-lookup"><span data-stu-id="eb263-148">**Result status**</span></span> | <span data-ttu-id="eb263-149">Tämä on kelvollinen tai kelpaamaton.</span><span class="sxs-lookup"><span data-stu-id="eb263-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="eb263-150">Tulostila ei ole käytettävissä, jos työntekijä ei täytä kelpoisuussäännön ehtoja, jos työntekijästä puuttuu pakollisia tietoja, kuten maksutiheys tai kiinteämääräinen kompensaatio, tai jos etuussuunnitelmasta puuttuu tietoja, jotka estävät työntekijöitä ilmoittautumasta.</span><span class="sxs-lookup"><span data-stu-id="eb263-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="eb263-151">**Tulossanoma**</span><span class="sxs-lookup"><span data-stu-id="eb263-151">**Result message**</span></span> | <span data-ttu-id="eb263-152">Ilmaisee, miksi työntekijä ei ole oikeutettu etuusjärjestelyyn tai jos oikeutussääntö on kulunut.</span><span class="sxs-lookup"><span data-stu-id="eb263-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |



[!INCLUDE[footer-include](../includes/footer-banner.md)]