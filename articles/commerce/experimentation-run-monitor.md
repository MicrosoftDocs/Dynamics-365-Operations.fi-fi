---
title: Kokeen suorittaminen ja seuranta
description: Tässä ohjeaiheessa käsitellään kokeen suorittamista ja seurantaa kolmannen osapuolen palvelussa. Siinä käsitellään muutosten tekemistä variaatioihin kokeen aloittamisen jälkeen.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 4afc19ed103f204fec61ab20b88f767ad5f05b38
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792532"
---
# <a name="run-and-monitor-an-experiment"></a><span data-ttu-id="bb951-104">Kokeen suorittaminen ja seuranta</span><span class="sxs-lookup"><span data-stu-id="bb951-104">Run and monitor an experiment</span></span>

<span data-ttu-id="bb951-105">Tässä ohjeaiheessa käsitellään kokeen suorittamista ja seuraamista kolmannen osapuolen sovelluksessa sekä mahdollisia variaatioiden muutoksia.</span><span class="sxs-lookup"><span data-stu-id="bb951-105">This topic describes how to run and monitor your experiment in a third-party app, and change variations if needed.</span></span> <span data-ttu-id="bb951-106">Koe on ensin [julkaistava](experimentation-preview-publish.md) Commercessa, ennen kuin tässä ohjeaiheessa olevat vaiheet voidaan suorittaa.</span><span class="sxs-lookup"><span data-stu-id="bb951-106">Before you complete the steps in this topic, you'll first need to [publish](experimentation-preview-publish.md) your experiment in Commerce.</span></span> 

<span data-ttu-id="bb951-107">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="bb951-107">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bb951-108">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="bb951-108">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="bb951-109">[ ![Kokeilun käyttäjän siirtymä – suorittaminen ja seuranta](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="bb951-109">[ ![Experimentation user journey - Run & Monitor](./media/experimentation_run_monitor.svg) ](./media/experimentation_run_monitor.svg#lightbox)</span></span>

<span data-ttu-id="bb951-110">Kun variaatiot on julkaistu, kaikki Commercessa tehtävät kokeen suorittamiseen tarvittavat vaiheet on tehty.</span><span class="sxs-lookup"><span data-stu-id="bb951-110">After you publish your variations, all of the steps you need to do in Commerce to run your experiment are complete.</span></span> <span data-ttu-id="bb951-111">Seuraavassa vaiheessa määritetään, mikä variaatio näytetään kullekin käyttäjälle, kun he pyytävät sivua.</span><span class="sxs-lookup"><span data-stu-id="bb951-111">The next step is determining which variation to show to each user when they request a page.</span></span> <span data-ttu-id="bb951-112">Kolmannen osapuolen palvelu tekee tämän päätöksen, mutta ennen sitä koe on aktivoitava kyseisessä palvelussa.</span><span class="sxs-lookup"><span data-stu-id="bb951-112">The third-party service makes that determination, but first you have to activate the experiment within the service.</span></span> <span data-ttu-id="bb951-113">Koska kokeen aktivointivaiheet ovat palvelukohtaisia, palvelun antamien ohjeiden noudattaminen on välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="bb951-113">Since the steps for activating an experiment vary from service to service, you'll need to follow the instructions included with your service or provider.</span></span> <span data-ttu-id="bb951-114">Jos koetta ei aktivoida, käyttäjät näkevät vain sivun oletusversion (yksikään variaatio ei ole näkyvissä).</span><span class="sxs-lookup"><span data-stu-id="bb951-114">If the experiment is not activated, users will only see the default version of the page (no variations will be displayed).</span></span>

<span data-ttu-id="bb951-115">Koetta on jatkettava niin kauan, että kerätyistä tiedoista voidaan muodostaa tilastollisesti kelvolliset tulokset.</span><span class="sxs-lookup"><span data-stu-id="bb951-115">You'll need to keep the experiment running long enough to gather data for statistically valid results.</span></span> <span data-ttu-id="bb951-116">Kokeeseen liittyviä tietoja voi seurata ja analysoida kokeen aikana kolmannen osapuolen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="bb951-116">Use the third-party service to monitor the experiment-related data and analytics while the experiment is running.</span></span>

## <a name="adjust-your-variations"></a><span data-ttu-id="bb951-117">Variaatioiden säätäminen</span><span class="sxs-lookup"><span data-stu-id="bb951-117">Adjust your variations</span></span>
<span data-ttu-id="bb951-118">Jos variaatioita on jostain syystä muokattava, voit tehdä sen seuraavien ohjeiden avulla.</span><span class="sxs-lookup"><span data-stu-id="bb951-118">If for any reason you need to modify your variations, follow the steps below.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bb951-119">Jos live-kokeiluun tehdään muutoksia Commercessa tai kolmannen osapuolen palvelussa, niillä voi olla merkittäviä vaikutuksia tuloksiin.</span><span class="sxs-lookup"><span data-stu-id="bb951-119">If you make changes to a live experiment in Commerce or the third-party service, your results may be significantly impacted.</span></span> <span data-ttu-id="bb951-120">Jos muutokset ovat merkittäviä, kannattaakin harkita kokeen jatkamista loppuun saakka ja uuden kokeen luomista.</span><span class="sxs-lookup"><span data-stu-id="bb951-120">Consider letting the experiment run its course and then creating a new experiment for major changes.</span></span>

1. <span data-ttu-id="bb951-121">Valitse Commercen sivustonmuodostimen vasemmassa siirtymisruudussa ensin **Kokeet** ja sitten koe.</span><span class="sxs-lookup"><span data-stu-id="bb951-121">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
1. <span data-ttu-id="bb951-122">Valitse päivitettävä variaatio avattavassa valikossa.</span><span class="sxs-lookup"><span data-stu-id="bb951-122">Select the variation you want to update from the drop-down menu.</span></span>
1. <span data-ttu-id="bb951-123">Tee tarvittavat muutokset ja esikatsele ja julkaise variaatiot sen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="bb951-123">Make any needed changes, and then preview and publish the variations.</span></span> <span data-ttu-id="bb951-124">Lisätietoja on kohdassa [Kokeen esikatseleminen ja julkaiseminen](experimentation-preview-publish.md).</span><span class="sxs-lookup"><span data-stu-id="bb951-124">For more information, see [Preview and publish an experiment](experimentation-preview-publish.md).</span></span>
1. <span data-ttu-id="bb951-125">Jos muutokset liittyvät kokeen asetuksiin, siirry kolmannen osapuolen palveluun.</span><span class="sxs-lookup"><span data-stu-id="bb951-125">Go to the third-party service to make any experiment setup-related changes.</span></span>
    
## <a name="previous-step"></a><span data-ttu-id="bb951-126">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="bb951-126">Previous step</span></span>
[<span data-ttu-id="bb951-127">Kokeen esikatseleminen ja julkaiseminen</span><span class="sxs-lookup"><span data-stu-id="bb951-127">Preview and publish an experiment</span></span>](experimentation-preview-publish.md)

## <a name="next-step"></a><span data-ttu-id="bb951-128">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="bb951-128">Next step</span></span>
[<span data-ttu-id="bb951-129">Variaation korottaminen ja kokeen päättäminen</span><span class="sxs-lookup"><span data-stu-id="bb951-129">Promote a variation and complete an experiment</span></span>](experimentation-review-complete.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]