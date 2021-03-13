---
title: Hypoteesin ja kokeen mittareiden määrittäminen
description: Tässä ohjeaiheessa käsitellään hypoteesin ja sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa suorittavan kokeen onnistumismittareiden määrittämistä.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5594b81d09eade263487244a14c0305d589ff94e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009996"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="340c2-103">Hypoteesin ja kokeen onnistumismittareiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="340c2-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="340c2-104">Kokeen elinkaaren ensimmäinen vaihe sisältää kokeen hypoteesin ja onnistumisen arvioinnissa käytettävien mittareiden määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="340c2-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="340c2-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät [kokeen määrittämiseen ja suorittamiseen ](experimentation-overview.md) sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="340c2-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="340c2-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="340c2-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="340c2-107">[ ![Kokeilun käyttäjän siirtymä – määrittäminen](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="340c2-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="340c2-108">Hypoteesi on väite, joka ennakoi kokeen tuloksen.</span><span class="sxs-lookup"><span data-stu-id="340c2-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="340c2-109">Hypoteesin määrittämisessä on monia vaiheita, kuten käyttäjien toiminnasta ja sivustosta kerättyihin tietoihin tutustuminen.</span><span class="sxs-lookup"><span data-stu-id="340c2-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="340c2-110">Hypoteesin avulla määritetään oletus tai teoria, joka halutaan vahvistaa kokeen avulla.</span><span class="sxs-lookup"><span data-stu-id="340c2-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="340c2-111">Kokeen hypoteesi voi olla esimerkiksi seuraava: *aloitussivulla oleva kuva valkoisesta teepaidasta tuottaa kesäkuukausina enemmän mainoslinkin napsautuksia kuin tummansininen neule, koska ihmiset haluat käyttää ohuita ja vaaleita vaatteita kesällä*.</span><span class="sxs-lookup"><span data-stu-id="340c2-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="340c2-112">Tässä tapauksessa luodaan variaatiot, joissa käytetään valkoista teepaitaa ja tummansinistä neuletta, ja molemmat julkaistaan samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="340c2-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="340c2-113">Hypoteesin vahvistamista varten kokeen onnistuminen tai epäonnistuminen on sidottava suoraan käyttäjän toimintoihin, kuten siihen, napsauttaako sivuston käyttäjä linkkiä tai painiketta.</span><span class="sxs-lookup"><span data-stu-id="340c2-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="340c2-114">Näiden toimintojen on sitten vastattava tapahtumia, jotka ilmoitetaan koetta seuraavalle kolmannen osapuolen palvelulle.</span><span class="sxs-lookup"><span data-stu-id="340c2-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="340c2-115">Toiminnon ajan mittaan suorittavien käyttäjien prosenttiosuus lasketaan yhteen mittarina, jolla voi luoda raportteja ja tehdä analyyseja.</span><span class="sxs-lookup"><span data-stu-id="340c2-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="340c2-116">Lisätietoja kaikkien käytettävissä olevien tapahtumien ja määritteiden tarkistamisesta on kohdassa [Commerce-komponenttien diagnostiikka- ja vianmääritystapahtumat](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="340c2-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="340c2-117">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="340c2-117">Previous step</span></span>
[<span data-ttu-id="340c2-118">Kokeilu Dynamics 365 Commercessa</span><span class="sxs-lookup"><span data-stu-id="340c2-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="340c2-119">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="340c2-119">Next step</span></span>
[<span data-ttu-id="340c2-120">Kokeilun määrittäminen</span><span class="sxs-lookup"><span data-stu-id="340c2-120">Set up an experiment</span></span>](experimentation-setup.md)
