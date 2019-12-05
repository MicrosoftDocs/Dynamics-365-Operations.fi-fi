---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773947"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="e93d9-103">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="e93d9-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="e93d9-104">Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Microsoft Dynamics 365 Supply Chain Managementin sisäisessä suunnittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e93d9-105">Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="e93d9-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="e93d9-106">Suunnittelun optimointitoimintoa ei ole oletusarvoisesti otettu käyttöön Dynamics Lifecycle Servicesissa (LCS).</span><span class="sxs-lookup"><span data-stu-id="e93d9-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="e93d9-107">Niinpä arvioinnin voi tehdä, ennen kuin toiminto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e93d9-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="e93d9-108">Suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen suunnittelumoduulin.</span><span class="sxs-lookup"><span data-stu-id="e93d9-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="e93d9-109">Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset.</span><span class="sxs-lookup"><span data-stu-id="e93d9-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="e93d9-110">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="e93d9-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="e93d9-111">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="e93d9-111">Licensing</span></span>

<span data-ttu-id="e93d9-112">Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="e93d9-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="e93d9-113">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="e93d9-113">Install the add-in</span></span>

<span data-ttu-id="e93d9-114">Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e93d9-115">Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="e93d9-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="e93d9-116">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="e93d9-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="e93d9-117">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e93d9-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="e93d9-118">Valitse **Ylläpito** tai selaa alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="e93d9-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="e93d9-119">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="e93d9-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="e93d9-120">Valitse **Suunnittelun optimointi**.</span><span class="sxs-lookup"><span data-stu-id="e93d9-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="e93d9-121">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="e93d9-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="e93d9-122">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="e93d9-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="e93d9-123">Suunnittelun optimoinnin integrointi</span><span class="sxs-lookup"><span data-stu-id="e93d9-123">Planning Optimization integration</span></span>

<span data-ttu-id="e93d9-124">Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin integrointi** \> **Integrointiparametrit**.</span><span class="sxs-lookup"><span data-stu-id="e93d9-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="e93d9-125">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="e93d9-125">Connection status</span></span>

<span data-ttu-id="e93d9-126">Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan.</span><span class="sxs-lookup"><span data-stu-id="e93d9-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="e93d9-127">Mahdolliset arvot ovat seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="e93d9-128">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="e93d9-128">Connection status</span></span> | <span data-ttu-id="e93d9-129">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="e93d9-129">Description</span></span> | <span data-ttu-id="e93d9-130">Voiko suunnittelun optimointia käyttää?</span><span class="sxs-lookup"><span data-stu-id="e93d9-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="e93d9-131">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="e93d9-131">Connected</span></span> | <span data-ttu-id="e93d9-132">Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys.</span><span class="sxs-lookup"><span data-stu-id="e93d9-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="e93d9-133">Kyllä</span><span class="sxs-lookup"><span data-stu-id="e93d9-133">Yes</span></span> |
| <span data-ttu-id="e93d9-134">Otetaan yhteyttä käyttöön</span><span class="sxs-lookup"><span data-stu-id="e93d9-134">Enabling connection</span></span> | <span data-ttu-id="e93d9-135">Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="e93d9-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e93d9-136">Ei</span><span class="sxs-lookup"><span data-stu-id="e93d9-136">No</span></span> |
| <span data-ttu-id="e93d9-137">Yhteys katkaistu</span><span class="sxs-lookup"><span data-stu-id="e93d9-137">Disconnected</span></span> | <span data-ttu-id="e93d9-138">Suunnittelun optimointipalveluun ei ole yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="e93d9-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="e93d9-139">Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="e93d9-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="e93d9-140">Ei</span><span class="sxs-lookup"><span data-stu-id="e93d9-140">No</span></span> |
| <span data-ttu-id="e93d9-141">Poistettaan yhteyttä käytöstä</span><span class="sxs-lookup"><span data-stu-id="e93d9-141">Disabling connection</span></span> | <span data-ttu-id="e93d9-142">Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="e93d9-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="e93d9-143">Ei</span><span class="sxs-lookup"><span data-stu-id="e93d9-143">No</span></span> |
| <span data-ttu-id="e93d9-144">Tilan saaminen</span><span class="sxs-lookup"><span data-stu-id="e93d9-144">Getting status</span></span> | <span data-ttu-id="e93d9-145">Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta.</span><span class="sxs-lookup"><span data-stu-id="e93d9-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="e93d9-146">Ei</span><span class="sxs-lookup"><span data-stu-id="e93d9-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="e93d9-147">Käytä suunnittelun optimointia -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="e93d9-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="e93d9-148">**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:</span><span class="sxs-lookup"><span data-stu-id="e93d9-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="e93d9-149">**Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="e93d9-150">**Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="e93d9-151">Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="e93d9-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="e93d9-152">Integrointi määrityksiin</span><span class="sxs-lookup"><span data-stu-id="e93d9-152">Integration with the setup</span></span>

<span data-ttu-id="e93d9-153">Jos suunnittelun optimoinnin esiversio on otettu käyttöön, suunnittelun optimoinnin lisäosaa käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="e93d9-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="e93d9-154">Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="e93d9-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e93d9-155">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="e93d9-155">Related resources</span></span>

[<span data-ttu-id="e93d9-156">Esiversion ehdot</span><span class="sxs-lookup"><span data-stu-id="e93d9-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="e93d9-157">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e93d9-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="e93d9-158">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="e93d9-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="e93d9-159">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e93d9-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="e93d9-160">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="e93d9-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="e93d9-161">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="e93d9-161">Cancel a planning job</span></span>](cancel-planning-job.md)
