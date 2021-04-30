---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d346251e82737624edfce88dc7b2ee10280f6877
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907664"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="0bf7d-103">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="0bf7d-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0bf7d-104">Kuten [aiemmin ilmoitettiin](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), suunnittelun optimointi on aikataulutettu korvaamaan nykyinen sisäinen pääsuunnittelumoduuli.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-104">As [previously announced](../../get-started/removed-deprecated-features-scm-updates.md#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="0bf7d-105">Jos sisäinen pääsuunnittelumoduuli on tällä hetkellä käytössä, suunnittelun optimointiin siirtymisen suunnittelu on syytä aloittaa nyt.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="0bf7d-106">Siirtoprosessi on tärkeää aloittaa heti, koska toiminnot voivat häiriintyä, kun vanhentumista ei voi estää.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="0bf7d-107">Siirtyminen kannattaa toteuttaa 1. joulukuuta 2020 mennessä, jotta vanhentumisesta aiheutuvat viime hetken ongelmat voidaan välttää.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="0bf7d-108">Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Supply Chain Managementin sisäisessä suunnittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="0bf7d-109">Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="0bf7d-110">Suunnittelun optimointi ei ole tällä hetkellä oletusarvoisesti otettuna käyttöön Dynamics Lifecycle Servicesissä (LCS), joten arvionti on mahdollista tehdä ennen ominaisuuden ottamista käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="0bf7d-111">Poikkeusta suunnittelun optimointiin siirtymiseen on pyydettävä, jos pääsuunnitteluprosessi ei sisällä tuotantoa (pääsuunnittelun luomia suunniteltuja tuotantotilauksia) ja tarvitset sisäistä pääsuunnittelumoduulia version 10.0.15 jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="0bf7d-112">Versiosta 10.0.16 alkaen ympäristöissä näytetään virhe, jos sisäinen pääsuunnittelu suoritetaan ilman suunniteltujen tuotantotilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="0bf7d-113">Suunnittelun optimointia on käytettävä kaikissa uusissa käyttöönotoissa, joissa ei luoda suunniteltuja tuotantotilauksia pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="0bf7d-114">Aiemmin luotujen ympäristöjen omistajat, jotka käyttävät sisäistä pääsuunnittelumoduulia suunniteltuja tuotantotilauksia luomatta, saavat poikkeusprosessia koskevan sähköpostin.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="0bf7d-115">Siirtyminen suunnittelun optimointiin kannattaa arvioida ja suunnitella yhteistyössä kumppanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="0bf7d-116">Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="0bf7d-117">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="0bf7d-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

## <a name="availability"></a><span data-ttu-id="0bf7d-118">Saatavuus</span><span class="sxs-lookup"><span data-stu-id="0bf7d-118">Availability</span></span>

<span data-ttu-id="0bf7d-119">Suunnittelun optimointi on tällä hetkellä käytettävissä seuraavilla Azuren maantieteellisillä alueilla: Yhdysvallat, Kanada, Eurooppa, Yhdistynyt Kuningaskunta, Australia ja Tyynenmeren Aasia.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, Australia, and Asia Pacific.</span></span> <span data-ttu-id="0bf7d-120">Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, LCS näyttää sanoman, jonka mukaan tätä maantieteellistä aluetta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="0bf7d-121">Huomaa, että suunnittelun optimointi ei tue Dynamics 365 Supply Chain Management -järjestelmän paikallisia käyttöönottoja.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

## <a name="licensing"></a><span data-ttu-id="0bf7d-122">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="0bf7d-122">Licensing</span></span>

<span data-ttu-id="0bf7d-123">Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

## <a name="install-and-enable-planning-optimization"></a><span data-ttu-id="0bf7d-124">Suunnittelun optimoinnin asentaminen ja ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="0bf7d-124">Install and enable Planning Optimization</span></span>

<span data-ttu-id="0bf7d-125">Suunnittelun optimoinnin käyttö edellyttää, että edellytykset täyttyvät järjestelmässä. Sen jälkeen käyttöoikeusavain otetaan käyttöön ja Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin apuohjelma asennetaan.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-125">To use Planning Optimization, you must make sure your system has all of the prerequisites in place and then enable its license key and install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="0bf7d-126">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="0bf7d-126">Prerequisites</span></span>

<span data-ttu-id="0bf7d-127">Ennen kuin suunnittelu optimoinnin apuohjelma voidaan asentaa, seuraavien edellytysten on toteuduttava:</span><span class="sxs-lookup"><span data-stu-id="0bf7d-127">Before you install the Planning Optimization Add-in, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="0bf7d-128">Supply Chain Managementia on käytettävä korkean käytettävyyden ympäristössä, jossa LCS on käytössä, taso 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on Dynamics 365 Supply Chain Managementin versio 10.0.7 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-128">You must be running Supply Chain Management on an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="0bf7d-129">Jos yrität asentaa apuohjelman OneBox-ympäristöön, asennus ei ole valmis ja sinun on peruutettava asennus.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-129">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

- <span data-ttu-id="0bf7d-130">Järjestelmä on määritettävä Power Platform -integrointia varten.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-130">Your system must be set up for Power Platform integration.</span></span> <span data-ttu-id="0bf7d-131">Lisätietoja on kohdissa [Apuohjelmien määrittämisen edellytykset](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) ja [Apuohjelmien määrittäminen](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span><span class="sxs-lookup"><span data-stu-id="0bf7d-131">For more information, see [Prerequisites for setting up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#prerequisites-for-setting-up-add-ins) and [Set up add-ins](../../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md#set-up-add-ins).</span></span>

### <a name="enable-the-planning-optimization-license"></a><span data-ttu-id="0bf7d-132">Suunnittelun optimoinnin käyttöoikeuden ottaminen käyttöön</span><span class="sxs-lookup"><span data-stu-id="0bf7d-132">Enable the Planning Optimization license</span></span>

<span data-ttu-id="0bf7d-133">Suunnittelun optimoinnin käyttäminen edellyttää, että sen määritysavain otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-133">To use Planning Optimization, you must enable its configuration key.</span></span> <span data-ttu-id="0bf7d-134">Toimi seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="0bf7d-134">To do so:</span></span>

1. <span data-ttu-id="0bf7d-135">Siirrä järjestelmä ylläpitotilaan kohdassa [Ylläpitotila](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-135">Put your system into maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="0bf7d-136">Valitse **Järjestelmän hallinta \> Asetukset \> Käyttöoikeuden konfiguraatio**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-136">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="0bf7d-137">Valitse **Määritysavain**-välilehdessä **Suunnittelun optimointi** -valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-137">On the **Configuration keys** tab, select the check box for **Planning Optimization**.</span></span>
1. <span data-ttu-id="0bf7d-138">Poista järjestelmän ylläpitotila käytöstä kohdassa [Ylläpitotila](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-138">Turn off maintenance mode, as described in [Maintenance mode](../../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

### <a name="install-the-planning-optimization-add-in"></a><span data-ttu-id="0bf7d-139">Suunnittelun optimoinnin apuohjelman asentaminen</span><span class="sxs-lookup"><span data-stu-id="0bf7d-139">Install the Planning Optimization Add-in</span></span>

<span data-ttu-id="0bf7d-140">LCS-projektin apuohjelma on asennettava ja suunnittelun optimointitoiminto on otettava sitten käyttöön Supply Chain Management -käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-140">You must install the add-in from your LCS project and then turn on the Planning Optimization functionality from the Supply Chain Management user interface.</span></span>

<span data-ttu-id="0bf7d-141">Suunnittelun optimoinnin apuohjelman asentaminen:</span><span class="sxs-lookup"><span data-stu-id="0bf7d-141">To install the Planning Optimization Add-in:</span></span>

1. <span data-ttu-id="0bf7d-142">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-142">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="0bf7d-143">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-143">Go to **Full details**.</span></span>
1. <span data-ttu-id="0bf7d-144">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-144">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="0bf7d-145">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-145">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="0bf7d-146">Valitse **Suunnittelun optimointi**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-146">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="0bf7d-147">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-147">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="0bf7d-148">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-148">Select **Install**.</span></span>
1. <span data-ttu-id="0bf7d-149">**Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-149">On the **Environment add-ins** FastTab, you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="0bf7d-150">Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi edellyttää sivun päivittämistä).</span><span class="sxs-lookup"><span data-stu-id="0bf7d-150">After a few minutes, **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="0bf7d-151">Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-151">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="0bf7d-152">Suunnittelun optimoinnin apuohjelman asennuksen päätarkoitus on yhdistää palvelu ja ympäristö.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-152">The main purpose of installing the Planning Optimization Add-in is to connect the service and the environment.</span></span> <span data-ttu-id="0bf7d-153">Tämän vuoksi apuohjelma on asennettava erikseen jokaiseen ympäristöön, jossa suunnittelun optimointia käytetään, riippumatta ympäristöjen välillä siirrettävästä koodista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-153">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

## <a name="integrate-planning-optimization-with-your-system"></a><span data-ttu-id="0bf7d-154">Suunnittelun optimoinnin integrointi järjestelmään</span><span class="sxs-lookup"><span data-stu-id="0bf7d-154">Integrate Planning Optimization with your system</span></span>

<span data-ttu-id="0bf7d-155">Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-155">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

### <a name="connection-status"></a><span data-ttu-id="0bf7d-156">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="0bf7d-156">Connection status</span></span>

<span data-ttu-id="0bf7d-157">Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-157">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="0bf7d-158">Mahdolliset arvot ovat seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-158">The following table shows the possible values.</span></span>

| <span data-ttu-id="0bf7d-159">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="0bf7d-159">Connection status</span></span> | <span data-ttu-id="0bf7d-160">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0bf7d-160">Description</span></span> | <span data-ttu-id="0bf7d-161">Voiko suunnittelun optimointia käyttää?</span><span class="sxs-lookup"><span data-stu-id="0bf7d-161">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="0bf7d-162">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="0bf7d-162">Connected</span></span> | <span data-ttu-id="0bf7d-163">Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-163">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="0bf7d-164">Kyllä</span><span class="sxs-lookup"><span data-stu-id="0bf7d-164">Yes</span></span> |
| <span data-ttu-id="0bf7d-165">Otetaan yhteyttä käyttöön</span><span class="sxs-lookup"><span data-stu-id="0bf7d-165">Enabling connection</span></span> | <span data-ttu-id="0bf7d-166">Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-166">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0bf7d-167">Ei</span><span class="sxs-lookup"><span data-stu-id="0bf7d-167">No</span></span> |
| <span data-ttu-id="0bf7d-168">Yhteys katkaistu</span><span class="sxs-lookup"><span data-stu-id="0bf7d-168">Disconnected</span></span> | <span data-ttu-id="0bf7d-169">Suunnittelun optimointipalveluun ei ole yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-169">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="0bf7d-170">Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-170">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="0bf7d-171">Ei</span><span class="sxs-lookup"><span data-stu-id="0bf7d-171">No</span></span> |
| <span data-ttu-id="0bf7d-172">Poistettaan yhteyttä käytöstä</span><span class="sxs-lookup"><span data-stu-id="0bf7d-172">Disabling connection</span></span> | <span data-ttu-id="0bf7d-173">Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-173">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="0bf7d-174">Ei</span><span class="sxs-lookup"><span data-stu-id="0bf7d-174">No</span></span> |
| <span data-ttu-id="0bf7d-175">Tilan saaminen</span><span class="sxs-lookup"><span data-stu-id="0bf7d-175">Getting status</span></span> | <span data-ttu-id="0bf7d-176">Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-176">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="0bf7d-177">Ei</span><span class="sxs-lookup"><span data-stu-id="0bf7d-177">No</span></span> |

### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="0bf7d-178">Käytä suunnittelun optimointia -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="0bf7d-178">The Use Planning Optimization option</span></span>

<span data-ttu-id="0bf7d-179">**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:</span><span class="sxs-lookup"><span data-stu-id="0bf7d-179">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="0bf7d-180">**Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-180">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="0bf7d-181">**Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-181">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="0bf7d-182">Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-182">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="0bf7d-183">Integrointi määrityksiin</span><span class="sxs-lookup"><span data-stu-id="0bf7d-183">Integration with the setup</span></span>

<span data-ttu-id="0bf7d-184">Jos suunnittelun optimointi on otettu käyttöön, suunnittelun optimoinnin apuohjelmaa käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-184">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="0bf7d-185">Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="0bf7d-185">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0bf7d-186">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0bf7d-186">Additional resources</span></span>

[<span data-ttu-id="0bf7d-187">Esiversion ehdot</span><span class="sxs-lookup"><span data-stu-id="0bf7d-187">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="0bf7d-188">Suunnittelun optimoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0bf7d-188">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="0bf7d-189">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="0bf7d-189">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="0bf7d-190">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="0bf7d-190">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="0bf7d-191">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="0bf7d-191">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="0bf7d-192">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="0bf7d-192">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]