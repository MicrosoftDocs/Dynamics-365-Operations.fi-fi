---
title: Hypoteesin ja kokeen mittareiden määrittäminen
description: Tässä ohjeaiheessa käsitellään hypoteesin ja sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa suorittavan kokeen onnistumismittareiden määrittämistä.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930186"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="c7978-103">Hypoteesin ja kokeen onnistumismittareiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c7978-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="c7978-104">Kokeen elinkaaren ensimmäinen vaihe sisältää kokeen hypoteesin ja onnistumisen arvioinnissa käytettävien mittareiden määrittämisen.</span><span class="sxs-lookup"><span data-stu-id="c7978-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="c7978-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät [kokeen määrittämiseen ja suorittamiseen ](experimentation-overview.md) sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="c7978-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c7978-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="c7978-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="c7978-107">[ ![Kokeilun käyttäjän siirtymä – määrittäminen](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c7978-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="c7978-108">Hypoteesi on väite, joka ennakoi kokeen tuloksen.</span><span class="sxs-lookup"><span data-stu-id="c7978-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="c7978-109">Hypoteesin määrittämisessä on monia vaiheita, kuten käyttäjien toiminnasta ja sivustosta kerättyihin tietoihin tutustuminen.</span><span class="sxs-lookup"><span data-stu-id="c7978-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="c7978-110">Hypoteesin avulla määritetään oletus tai teoria, joka halutaan vahvistaa kokeen avulla.</span><span class="sxs-lookup"><span data-stu-id="c7978-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="c7978-111">Kokeen hypoteesi voi olla esimerkiksi seuraava: *aloitussivulla oleva kuva valkoisesta teepaidasta tuottaa kesäkuukausina enemmän mainoslinkin napsautuksia kuin tummansininen neule, koska ihmiset haluat käyttää ohuita ja vaaleita vaatteita kesällä*.</span><span class="sxs-lookup"><span data-stu-id="c7978-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="c7978-112">Tässä tapauksessa luodaan variaatiot, joissa käytetään valkoista teepaitaa ja tummansinistä neuletta, ja molemmat julkaistaan samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="c7978-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="c7978-113">Hypoteesin vahvista varten kokeen onnistuminen tai epäonnistuminen on sidottava suoraan käyttäjän toimintoihin, kuten siihen napsauttaako sivuston käyttäjä linkkiä tai painiketta.</span><span class="sxs-lookup"><span data-stu-id="c7978-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="c7978-114">Näiden toimintojen on sitten vastattava tapahtumia, jotka ilmoitetaan koetta seuraavalle kolmannen osapuolen palvelulle.</span><span class="sxs-lookup"><span data-stu-id="c7978-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="c7978-115">Toiminnon ajan mittaan suorittavien käyttäjien prosenttiosuus lasketaan yhteen mittarina, jolla voi luoda raportteja ja tehdä analyyseja.</span><span class="sxs-lookup"><span data-stu-id="c7978-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="c7978-116">Lisätietoja kaikista käytettävissä olevista tapahtumista ja määritteistä on kohdassa [Commerce-komponenttien diagnostiikka- ja vianmääritystapahtumat](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="c7978-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c7978-117">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="c7978-117">Previous step</span></span>
[<span data-ttu-id="c7978-118">Kokeilu Dynamics 365 Commercessa</span><span class="sxs-lookup"><span data-stu-id="c7978-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="c7978-119">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="c7978-119">Next step</span></span>
[<span data-ttu-id="c7978-120">Kokeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c7978-120">Set up an experiment</span></span>](experimentation-setup.md)
