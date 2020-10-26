---
title: Kokeen määrittäminen
description: Tässä aiheessa käsitellään kokeen määrittämistä kolmannen osapuolen palvelussa.
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
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930188"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="737e2-103">Kokeen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="737e2-103">Set up an experiment</span></span>

<span data-ttu-id="737e2-104">Sen jälkeen kun olet [määrittänyt hypoteesin ja käytettävät onnistumismittarit](experimentation-identify.md), koe on määritettävä kolmannen osapuolen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="737e2-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="737e2-105">Seuraavassa kaaviossa on kaikki vaiheet, jotka sisältyvät kokeen määrittämiseen ja suorittamiseen sähköisessä kaupankäyntisivustossa Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="737e2-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="737e2-106">Muut vaiheet käsitellään erillisissä ohjeaiheissa.</span><span class="sxs-lookup"><span data-stu-id="737e2-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="737e2-107">[ ![Kokeilun käyttäjän siirtymä – määrittäminen](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="737e2-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="737e2-108">Kokeen määrittäminen kolmannen osapuolen palvelussa</span><span class="sxs-lookup"><span data-stu-id="737e2-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="737e2-109">Tässä vaiheessa kolmannen osapuolen palvelun pitäisi olla valittuna kokeen suorittamista ja seurantaa varten sekä kokeen yhdistämisen määrittämistä varten.</span><span class="sxs-lookup"><span data-stu-id="737e2-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="737e2-110">Nämä edellytykset on mainittu [Kokeilut Dynamics 365 Commercessa](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="737e2-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="737e2-111">Luo koe kolmannen osapuolen palvelussa noudattamalla annettuja ohjeita.</span><span class="sxs-lookup"><span data-stu-id="737e2-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="737e2-112">Jos yhdistin on määritetty oikein, täydellinen kolmannen osapuolen palvelussa määritettyjen kokeiden luettelo tulee näkyviin sivustonmuodostimeen noin 5 minuutin kuluessa.</span><span class="sxs-lookup"><span data-stu-id="737e2-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="737e2-113">Onnistumismittareiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="737e2-113">Set up your success metrics</span></span>
<span data-ttu-id="737e2-114">Kaikki kokeet tarvitsevat mittarin, jolla mitataan variaatioiden vaikutusta ja vahvistaa hypoteesi.</span><span class="sxs-lookup"><span data-stu-id="737e2-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="737e2-115">Noudata seuraavia ohjeita ja ota mittareiden laskenta käyttöön kolmannen osapuolen palvelussa käyttämällä Dynamics 365 Commercen live-telemetriatapahtumia.</span><span class="sxs-lookup"><span data-stu-id="737e2-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="737e2-116">Valitse sivustonmuodostimen vasemmassa ruudussa **Sivut**-välilehti ja valitse sitten sivu, josta haluat kerätä mittaustietoja.</span><span class="sxs-lookup"><span data-stu-id="737e2-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="737e2-117">Siirry **Seurattava tapahtumatunnukset** -osaan seurattavan sivun tai moduulin oikeassa ominaisuusruudussa.</span><span class="sxs-lookup"><span data-stu-id="737e2-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="737e2-118">Valitse **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="737e2-118">Select **View**.</span></span> <span data-ttu-id="737e2-119">Näkyvissä on kaikki tapahtumatunnukset sisältävä luettelo.</span><span class="sxs-lookup"><span data-stu-id="737e2-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="737e2-120">Kopioi seurattava tapahtuma ja liitä tapahtuma-avain sille varattuun sijaintiin kolmannen osapuolen palvelussa.</span><span class="sxs-lookup"><span data-stu-id="737e2-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="737e2-121">Jos tarvitset useita tapahtumia, kopioi avaimet yksi kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="737e2-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="737e2-122">Lisätietoja kaikkien käytettävissä olevien tapahtumien ja määritteiden, myös sivunäkymien ja tuoton seuraamisen, näyttämisestä on kohdassa [Commerce-komponenttien diagnostiikka- ja vianmääritystapahtumat](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="737e2-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="737e2-123">Suorita muut kolmannen osapuolen palvelun edellyttämät mittareiden seurantaan tarvittavat vaiheet.</span><span class="sxs-lookup"><span data-stu-id="737e2-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="737e2-124">Edellinen vaihe</span><span class="sxs-lookup"><span data-stu-id="737e2-124">Previous step</span></span>
[<span data-ttu-id="737e2-125">Kokeilun hypoteesin ja mittarien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="737e2-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="737e2-126">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="737e2-126">Next step</span></span>
[<span data-ttu-id="737e2-127">Kokeilun yhdistäminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="737e2-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
