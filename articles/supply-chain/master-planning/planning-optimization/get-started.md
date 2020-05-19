---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ce1bbb18e9a448e84d001a4195421d2b0e4af5be
ms.sourcegitcommit: c0d37fdd70f3dec4605fdee6f981f84a49be9b9e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/06/2020
ms.locfileid: "3339875"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="6ca8b-103">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ca8b-104">Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Microsoft Dynamics 365 Supply Chain Managementin sisäisessä suunnittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6ca8b-105">Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="6ca8b-106">Suunnittelun optimointitoimintoa ei ole oletusarvoisesti otettu käyttöön Dynamics Lifecycle Servicesissa (LCS).</span><span class="sxs-lookup"><span data-stu-id="6ca8b-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="6ca8b-107">Niinpä arvioinnin voi tehdä, ennen kuin toiminto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="6ca8b-108">Suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen suunnittelumoduulin.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="6ca8b-109">Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="6ca8b-110">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="6ca8b-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="6ca8b-111">Saatavuus</span><span class="sxs-lookup"><span data-stu-id="6ca8b-111">Availability</span></span>
<span data-ttu-id="6ca8b-112">Suunnittelun optimointi on tällä hetkellä käytettävissä seuraavilla Azure-maantieteellisillä alueilla: Yhdysvallat, Kanada, Eurooppa, Iso-Britannia ja Australia.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="6ca8b-113">Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, LCS näyttää sanoman, jonka mukaan tätä maantieteellistä aluetta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="6ca8b-114">Huomaa, että suunnittelun optimointi ei tue Dynamics 365 Supply Chain Management -järjestelmän paikallisia käyttöönottoja.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="6ca8b-115">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="6ca8b-115">Licensing</span></span>

<span data-ttu-id="6ca8b-116">Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="6ca8b-117">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-117">Install the add-in</span></span>

<span data-ttu-id="6ca8b-118">Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="6ca8b-119">Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="6ca8b-120">Suunnittelun optimoinnin vaatimus on korkean käytettävyyden ympäristö, jossa LCS on käytössä, taso 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on Dynamics 365 Supply Chain Management -sovelluksen versio 10.0.7 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="6ca8b-121">Jos yrität asentaa apuohjelman OneBox-ympäristöön, asennus ei ole valmis ja sinun on peruutettava asennus.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="6ca8b-122">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="6ca8b-123">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="6ca8b-124">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="6ca8b-125">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="6ca8b-126">Valitse **Suunnittelun optimointi**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="6ca8b-127">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="6ca8b-128">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-128">Select **Install**.</span></span>
1. <span data-ttu-id="6ca8b-129">**Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="6ca8b-130">Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi vaatia sivun päivityksen).</span><span class="sxs-lookup"><span data-stu-id="6ca8b-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="6ca8b-131">Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="6ca8b-132">Suunnittelun optimoinnin integrointi</span><span class="sxs-lookup"><span data-stu-id="6ca8b-132">Planning Optimization integration</span></span>

<span data-ttu-id="6ca8b-133">Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="6ca8b-134">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="6ca8b-134">Connection status</span></span>

<span data-ttu-id="6ca8b-135">Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="6ca8b-136">Mahdolliset arvot ovat seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="6ca8b-137">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="6ca8b-137">Connection status</span></span> | <span data-ttu-id="6ca8b-138">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6ca8b-138">Description</span></span> | <span data-ttu-id="6ca8b-139">Voiko suunnittelun optimointia käyttää?</span><span class="sxs-lookup"><span data-stu-id="6ca8b-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="6ca8b-140">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="6ca8b-140">Connected</span></span> | <span data-ttu-id="6ca8b-141">Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="6ca8b-142">Kyllä</span><span class="sxs-lookup"><span data-stu-id="6ca8b-142">Yes</span></span> |
| <span data-ttu-id="6ca8b-143">Otetaan yhteyttä käyttöön</span><span class="sxs-lookup"><span data-stu-id="6ca8b-143">Enabling connection</span></span> | <span data-ttu-id="6ca8b-144">Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6ca8b-145">Ei</span><span class="sxs-lookup"><span data-stu-id="6ca8b-145">No</span></span> |
| <span data-ttu-id="6ca8b-146">Yhteys katkaistu</span><span class="sxs-lookup"><span data-stu-id="6ca8b-146">Disconnected</span></span> | <span data-ttu-id="6ca8b-147">Suunnittelun optimointipalveluun ei ole yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="6ca8b-148">Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="6ca8b-149">Ei</span><span class="sxs-lookup"><span data-stu-id="6ca8b-149">No</span></span> |
| <span data-ttu-id="6ca8b-150">Poistettaan yhteyttä käytöstä</span><span class="sxs-lookup"><span data-stu-id="6ca8b-150">Disabling connection</span></span> | <span data-ttu-id="6ca8b-151">Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="6ca8b-152">Ei</span><span class="sxs-lookup"><span data-stu-id="6ca8b-152">No</span></span> |
| <span data-ttu-id="6ca8b-153">Tilan saaminen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-153">Getting status</span></span> | <span data-ttu-id="6ca8b-154">Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="6ca8b-155">Ei</span><span class="sxs-lookup"><span data-stu-id="6ca8b-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="6ca8b-156">Käytä suunnittelun optimointia -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="6ca8b-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="6ca8b-157">**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:</span><span class="sxs-lookup"><span data-stu-id="6ca8b-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="6ca8b-158">**Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="6ca8b-159">**Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="6ca8b-160">Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="6ca8b-161">Integrointi määrityksiin</span><span class="sxs-lookup"><span data-stu-id="6ca8b-161">Integration with the setup</span></span>

<span data-ttu-id="6ca8b-162">Jos suunnittelun optimoinnin esiversio on otettu käyttöön, suunnittelun optimoinnin lisäosaa käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="6ca8b-163">Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="6ca8b-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ca8b-164">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="6ca8b-164">Additional resources</span></span>

[<span data-ttu-id="6ca8b-165">Esiversion ehdot</span><span class="sxs-lookup"><span data-stu-id="6ca8b-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="6ca8b-166">Suunnittelun optimoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="6ca8b-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="6ca8b-167">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="6ca8b-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="6ca8b-168">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="6ca8b-169">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="6ca8b-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="6ca8b-170">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="6ca8b-170">Cancel a planning job</span></span>](cancel-planning-job.md)
