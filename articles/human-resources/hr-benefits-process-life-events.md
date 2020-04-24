---
title: Elämäntapahtumien käsittely
description: Microsoft Dynamics 365 Human Resourcesin työntekijäelinkaaren aikana kukin työntekijä voi kohdata erilaisia elämäntapahtumamuutoksia.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: ba8d21482a18c6baa93437fc65c165907bdb515d
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229923"
---
# <a name="process-life-events"></a><span data-ttu-id="f18fd-103">Elämäntapahtumien käsittely</span><span class="sxs-lookup"><span data-stu-id="f18fd-103">Process life events</span></span>

<span data-ttu-id="f18fd-104">Microsoft Dynamics 365 Human Resourcesin työntekijäelinkaaren aikana kukin työntekijä voi kohdata erilaisia elämäntapahtumamuutoksia.</span><span class="sxs-lookup"><span data-stu-id="f18fd-104">During the employee lifecycle in Microsoft Dynamics 365 Human Resources, each employee may encounter various life event changes.</span></span> <span data-ttu-id="f18fd-105">Esimerkiksi avioliitto, muutos työsuhteessa tai huollettavan/edunsaajan muutos.</span><span class="sxs-lookup"><span data-stu-id="f18fd-105">For example, marriage, change in employment, or dependent/beneficiary change.</span></span> <span data-ttu-id="f18fd-106">Jos haluat käyttää elämäntapahtumia, sinun on otettava elämäntapahtumat käyttöön etuusparametrien lomakkeessa, määritettävä elämäntapahtumatyyppejä ja määritettävä elämäntapahtuma-asetuksia suunnitelmatyypeille.</span><span class="sxs-lookup"><span data-stu-id="f18fd-106">To use life events, you must enable life events in the benefits parameters form, set up life event types, and set up life event options for plan types.</span></span>

<span data-ttu-id="f18fd-107">Ennen kuin voit käsitellä elämäntapahtumia, avoin rekisteröinti on suoritettava vähintään kerran palkkausjakson aikana.</span><span class="sxs-lookup"><span data-stu-id="f18fd-107">Before you can process life events, you must have already run open enrollment at least once during a hiring time frame.</span></span> <span data-ttu-id="f18fd-108">Yhdysvalloissa avoin rekisteröityminen järjestetään tyypillisesti kerran vuodessa.</span><span class="sxs-lookup"><span data-stu-id="f18fd-108">In the United States, open enrollment is typically once per year.</span></span> <span data-ttu-id="f18fd-109">Yhdysvaltojen ulkopuolella avoin rekisteröityminen saatetaan suorittaa palkkauksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="f18fd-109">Outside the United States, open enrollment may be run at the time of hire.</span></span> <span data-ttu-id="f18fd-110">Työn tekijän ei tarvitse valita etuussuunnitelmaa, jotta elämäntapahtumia voidaan käsitellä, mutta heidän on oltava olleita mukana avoimen rekisteröitymisen käsittelyssä.</span><span class="sxs-lookup"><span data-stu-id="f18fd-110">A worker does not need to select a benefit plan in order for life events to be processed, but they need to have been included in open enrollment processing.</span></span> 

<span data-ttu-id="f18fd-111">Käytä elämäntapahtumien käsittelyä, kun sinulla on työntekijöitä, joilla on tulevaisuudessa toteutuvia elämäntapahtumia.</span><span class="sxs-lookup"><span data-stu-id="f18fd-111">Use life event processing when you have workers who have life events that take place on a future date.</span></span> <span data-ttu-id="f18fd-112">Tämä tapahtuma käsittelee kaikki elämäntapahtumat, joita ei ole käsitelty (kuten tulevat elämäntapahtumat tai lisätyt elämäntapahtumat, jotka eivät ole työntekijäkohtaisia – esimerkki tästä on uusi etu).</span><span class="sxs-lookup"><span data-stu-id="f18fd-112">This event will process all life events that have not been processed (like future life events, or life events that have been added that are not specific to any one worker – one example is a new benefit).</span></span> <span data-ttu-id="f18fd-113">Reaaliaikaiset elämäntapahtumat ovat piilotettuja.</span><span class="sxs-lookup"><span data-stu-id="f18fd-113">Real-time life events are hidden.</span></span>

<span data-ttu-id="f18fd-114">Jos esimerkiksi tänään on 1. helmikuuta ja työntekijä Joe Smithin on tarkoitus vaihtaa yritystä 14. helmikuuta, järjestelmä käsittelee kaikki tapahtumat 15. helmikuuta saakka, jos suoritat elämäntapahtumien käsittelyn 15. helmikuuta osalta.</span><span class="sxs-lookup"><span data-stu-id="f18fd-114">For example, if today is February 1, and on February 14 worker Joe Smith is scheduled to change legal entities, if you run life event processing for February 15, the system processes all events up until February 15.</span></span> 

1. <span data-ttu-id="f18fd-115">Valitse **Etujen hallinta** -työtilassa **Käsittely**-kohdasta **Elämäntapahtumien käsittely**.</span><span class="sxs-lookup"><span data-stu-id="f18fd-115">In the **Benefits management** workspace, under **Processing**, select **Life event processing**.</span></span>

2. <span data-ttu-id="f18fd-116">Määritä **Suorita elämäntapahtumaprosessi** -valintaruudussa arvot seuraaville kentille:</span><span class="sxs-lookup"><span data-stu-id="f18fd-116">In the **Run life event process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="f18fd-117">Kenttä</span><span class="sxs-lookup"><span data-stu-id="f18fd-117">Field</span></span> | <span data-ttu-id="f18fd-118">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="f18fd-118">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f18fd-119">**Rekisteröitymiskausi**</span><span class="sxs-lookup"><span data-stu-id="f18fd-119">**Enrollment period**</span></span> | <span data-ttu-id="f18fd-120">Rekisteröintijakso, jonka elämäntapahtumat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f18fd-120">The enrollment period to process life events for.</span></span> |
   | <span data-ttu-id="f18fd-121">**Oikeushenkilö**</span><span class="sxs-lookup"><span data-stu-id="f18fd-121">**Legal entity**</span></span> | <span data-ttu-id="f18fd-122">Yritys, jonka elämäntapahtumat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f18fd-122">The legal entity to process life events for.</span></span> |
   | <span data-ttu-id="f18fd-123">**Elinkaaritapahtuman päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="f18fd-123">**Life event date**</span></span> | <span data-ttu-id="f18fd-124">Järjestelmä käsittelee kaikki rekisteröintijakson aikana tähän päivämäärään mennessä toteutuneet tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f18fd-124">The system processes all events during the enrollment period that occur up until this date.</span></span> |
   | <span data-ttu-id="f18fd-125">**Työntekijä**</span><span class="sxs-lookup"><span data-stu-id="f18fd-125">**Worker**</span></span> | <span data-ttu-id="f18fd-126">Työntekijä, jonka elämäntapahtumat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f18fd-126">The worker to process life events for.</span></span> <span data-ttu-id="f18fd-127">Jos jätät tämän kentän tyhjäksi, käsitellään kaikkien työntekijöiden elämäntapahtumat.</span><span class="sxs-lookup"><span data-stu-id="f18fd-127">If you leave this field blank, life events will be processed for all workers.</span></span> |

3. <span data-ttu-id="f18fd-128">Jos haluat suorittaa prosessin taustalla, valitse **Suorita taustalla** ja tee seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="f18fd-128">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="f18fd-129">Määritä prosessin tiedot.</span><span class="sxs-lookup"><span data-stu-id="f18fd-129">Enter information for the process.</span></span>

   2. <span data-ttu-id="f18fd-130">Jos haluat määrittää toistuvan työn, valitse **Toistuminen**, kirjoita toistuvuustiedot ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f18fd-130">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="f18fd-131">Jos haluat määrittää työpaikkahälytyksen, valitse **Hälytykset**, valitse vastaanotettavat hälytykset ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="f18fd-131">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="f18fd-132">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f18fd-132">Select **OK**.</span></span> <span data-ttu-id="f18fd-133">Prosessi suoritetaan määrittämilläsi parametreilla.</span><span class="sxs-lookup"><span data-stu-id="f18fd-133">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="f18fd-134">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="f18fd-134">Select **OK**.</span></span>
