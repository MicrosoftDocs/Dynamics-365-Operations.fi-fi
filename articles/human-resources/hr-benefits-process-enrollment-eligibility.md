---
title: Rekisteröintikelpoisuuden käsittely
description: Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008829"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="789a5-103">Rekisteröintikelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="789a5-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="789a5-104">Tässä artikkelissa kerrotaan, miten rekisteröintikelpoisuusprosessi suoritetaan.</span><span class="sxs-lookup"><span data-stu-id="789a5-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="789a5-105">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Rekisteröintikelpoisuuden käsittely**.</span><span class="sxs-lookup"><span data-stu-id="789a5-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="789a5-106">Määritä **Suorita edun rekisteröintikelpoisuusprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="789a5-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="789a5-107">Kenttä</span><span class="sxs-lookup"><span data-stu-id="789a5-107">Field</span></span> | <span data-ttu-id="789a5-108">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="789a5-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="789a5-109">Rekisteröitymiskausi</span><span class="sxs-lookup"><span data-stu-id="789a5-109">Enrollment period</span></span> | <span data-ttu-id="789a5-110">Rekisteröintijakso, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="789a5-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="789a5-111">Oikeushenkilö</span><span class="sxs-lookup"><span data-stu-id="789a5-111">Legal entity</span></span> | <span data-ttu-id="789a5-112">Yritys, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="789a5-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="789a5-113">Työntekijä</span><span class="sxs-lookup"><span data-stu-id="789a5-113">Worker</span></span> | <span data-ttu-id="789a5-114">Työntekijä, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="789a5-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="789a5-115">Jos jätät tämän kentän tyhjäksi, käsitellään kaikkien työntekijöiden rekisteröintikelpoisuus.</span><span class="sxs-lookup"><span data-stu-id="789a5-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="789a5-116">Etuussuunnitelma</span><span class="sxs-lookup"><span data-stu-id="789a5-116">Benefit plan</span></span> | <span data-ttu-id="789a5-117">Etuussuunnitelma, jonka rekisteröintikelpoisuus käsitellään.</span><span class="sxs-lookup"><span data-stu-id="789a5-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="789a5-118">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="789a5-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="789a5-119">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="789a5-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="789a5-120">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="789a5-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="789a5-121">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="789a5-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="789a5-122">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="789a5-122">Select **OK**.</span></span> <span data-ttu-id="789a5-123">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="789a5-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="789a5-124">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="789a5-124">Select **OK**.</span></span>
