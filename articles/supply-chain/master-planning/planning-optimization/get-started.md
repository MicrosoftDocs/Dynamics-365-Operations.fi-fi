---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: AnnBe
ms.date: 01/17/2020
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
ms.openlocfilehash: 3e0371c6addc0412dc2fc105891b012941e92a06
ms.sourcegitcommit: e5a3c85a322a9216b8f176536d664fef40ae0bec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/17/2020
ms.locfileid: "2971461"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="6273a-103">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="6273a-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="6273a-104">Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Microsoft Dynamics 365 Supply Chain Managementin sisäisessä suunnittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="6273a-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6273a-105">Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="6273a-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="6273a-106">Suunnittelun optimointitoimintoa ei ole oletusarvoisesti otettu käyttöön Dynamics Lifecycle Servicesissa (LCS).</span><span class="sxs-lookup"><span data-stu-id="6273a-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="6273a-107">Niinpä arvioinnin voi tehdä, ennen kuin toiminto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6273a-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="6273a-108">Suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen suunnittelumoduulin.</span><span class="sxs-lookup"><span data-stu-id="6273a-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="6273a-109">Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset.</span><span class="sxs-lookup"><span data-stu-id="6273a-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="6273a-110">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6273a-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="6273a-111">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="6273a-111">Licensing</span></span>

<span data-ttu-id="6273a-112">Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="6273a-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="6273a-113">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="6273a-113">Install the add-in</span></span>

<span data-ttu-id="6273a-114">Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa.</span><span class="sxs-lookup"><span data-stu-id="6273a-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6273a-115">Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="6273a-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="6273a-116">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="6273a-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="6273a-117">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6273a-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="6273a-118">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="6273a-118">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="6273a-119">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="6273a-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="6273a-120">Valitse **Suunnittelun optimointi**.</span><span class="sxs-lookup"><span data-stu-id="6273a-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="6273a-121">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="6273a-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="6273a-122">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="6273a-122">Select **Install**.</span></span>
1. <span data-ttu-id="6273a-123">**Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.</span><span class="sxs-lookup"><span data-stu-id="6273a-123">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="6273a-124">Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi vaatia sivun päivityksen).</span><span class="sxs-lookup"><span data-stu-id="6273a-124">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="6273a-125">Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="6273a-125">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="6273a-126">Suunnittelun optimoinnin integrointi</span><span class="sxs-lookup"><span data-stu-id="6273a-126">Planning Optimization integration</span></span>

<span data-ttu-id="6273a-127">Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6273a-127">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="6273a-128">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="6273a-128">Connection status</span></span>

<span data-ttu-id="6273a-129">Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan.</span><span class="sxs-lookup"><span data-stu-id="6273a-129">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="6273a-130">Mahdolliset arvot ovat seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="6273a-130">The following table shows the possible values.</span></span>

| <span data-ttu-id="6273a-131">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="6273a-131">Connection status</span></span> | <span data-ttu-id="6273a-132">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6273a-132">Description</span></span> | <span data-ttu-id="6273a-133">Voiko suunnittelun optimointia käyttää?</span><span class="sxs-lookup"><span data-stu-id="6273a-133">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="6273a-134">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="6273a-134">Connected</span></span> | <span data-ttu-id="6273a-135">Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys.</span><span class="sxs-lookup"><span data-stu-id="6273a-135">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="6273a-136">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6273a-136">Yes</span></span> |
| <span data-ttu-id="6273a-137">Otetaan yhteyttä käyttöön</span><span class="sxs-lookup"><span data-stu-id="6273a-137">Enabling connection</span></span> | <span data-ttu-id="6273a-138">Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6273a-138">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6273a-139">Ei</span><span class="sxs-lookup"><span data-stu-id="6273a-139">No</span></span> |
| <span data-ttu-id="6273a-140">Yhteys katkaistu</span><span class="sxs-lookup"><span data-stu-id="6273a-140">Disconnected</span></span> | <span data-ttu-id="6273a-141">Suunnittelun optimointipalveluun ei ole yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="6273a-141">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="6273a-142">Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6273a-142">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="6273a-143">Ei</span><span class="sxs-lookup"><span data-stu-id="6273a-143">No</span></span> |
| <span data-ttu-id="6273a-144">Poistettaan yhteyttä käytöstä</span><span class="sxs-lookup"><span data-stu-id="6273a-144">Disabling connection</span></span> | <span data-ttu-id="6273a-145">Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6273a-145">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6273a-146">Ei</span><span class="sxs-lookup"><span data-stu-id="6273a-146">No</span></span> |
| <span data-ttu-id="6273a-147">Tilan saaminen</span><span class="sxs-lookup"><span data-stu-id="6273a-147">Getting status</span></span> | <span data-ttu-id="6273a-148">Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta.</span><span class="sxs-lookup"><span data-stu-id="6273a-148">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="6273a-149">Ei</span><span class="sxs-lookup"><span data-stu-id="6273a-149">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="6273a-150">Käytä suunnittelun optimointia -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6273a-150">The Use Planning Optimization option</span></span>

<span data-ttu-id="6273a-151">**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:</span><span class="sxs-lookup"><span data-stu-id="6273a-151">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="6273a-152">**Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6273a-152">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="6273a-153">**Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6273a-153">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="6273a-154">Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="6273a-154">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="6273a-155">Integrointi määrityksiin</span><span class="sxs-lookup"><span data-stu-id="6273a-155">Integration with the setup</span></span>

<span data-ttu-id="6273a-156">Jos suunnittelun optimoinnin esiversio on otettu käyttöön, suunnittelun optimoinnin lisäosaa käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6273a-156">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="6273a-157">Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="6273a-157">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="6273a-158">Liittyvät resurssit</span><span class="sxs-lookup"><span data-stu-id="6273a-158">Related resources</span></span>

[<span data-ttu-id="6273a-159">Esiversion ehdot</span><span class="sxs-lookup"><span data-stu-id="6273a-159">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="6273a-160">Suunnittelun optimoinnin yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6273a-160">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6273a-161">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="6273a-161">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="6273a-162">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="6273a-162">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6273a-163">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="6273a-163">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="6273a-164">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="6273a-164">Cancel a planning job</span></span>](cancel-planning-job.md)
