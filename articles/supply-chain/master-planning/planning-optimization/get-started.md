---
title: Suunnittelun optimoinnin aloittaminen
description: Tässä ohjeaiheessa käsitellään suunnittelun optimointitoiminnon käytön aloittamisesta.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427519"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="04a60-103">Suunnittelun optimoinnin aloittaminen</span><span class="sxs-lookup"><span data-stu-id="04a60-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04a60-104">Kuten [aiemmin ilmoitettiin](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), suunnittelun optimointi on aikataulutettu korvaamaan nykyinen sisäinen pääsuunnittelumoduuli.</span><span class="sxs-lookup"><span data-stu-id="04a60-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="04a60-105">Jos sisäinen pääsuunnittelumoduuli on tällä hetkellä käytössä, suunnittelun optimointiin siirtymisen suunnittelu on syytä aloittaa nyt.</span><span class="sxs-lookup"><span data-stu-id="04a60-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="04a60-106">Siirtoprosessi on tärkeää aloittaa heti, koska toiminnot voivat häiriintyä, kun vanhentumista ei voi estää.</span><span class="sxs-lookup"><span data-stu-id="04a60-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="04a60-107">Siirtyminen kannattaa toteuttaa 1. joulukuuta 2020 mennessä, jotta vanhentumisesta aiheutuvat viime hetken ongelmat voidaan välttää.</span><span class="sxs-lookup"><span data-stu-id="04a60-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="04a60-108">Suunnittelun optimointitoiminto ei tällä hetkellä tue kaikki niitä toimintoja, joita on Supply Chain Managementin sisäisessä suunnittelumoduulissa.</span><span class="sxs-lookup"><span data-stu-id="04a60-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="04a60-109">Tämän vuoksi on tärkeää arvioida, vastaako suunnittelun optimoinnissa tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.</span><span class="sxs-lookup"><span data-stu-id="04a60-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="04a60-110">Suunnittelun optimointi ei ole tällä hetkellä oletusarvoisesti otettuna käyttöön Dynamics Lifecycle Servicesissä (LCS), joten arvionti on mahdollista tehdä ennen ominaisuuden ottamista käyttöön.</span><span class="sxs-lookup"><span data-stu-id="04a60-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="04a60-111">Poikkeusta suunnittelun optimointiin siirtymiseen on pyydettävä, jos pääsuunnitteluprosessi ei sisällä tuotantoa (pääsuunnittelun luomia suunniteltuja tuotantotilauksia) ja tarvitset sisäistä pääsuunnittelumoduulia version 10.0.15 jälkeen.</span><span class="sxs-lookup"><span data-stu-id="04a60-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="04a60-112">Versiosta 10.0.16 alkaen ympäristöissä näytetään virhe, jos sisäinen pääsuunnittelu suoritetaan ilman suunniteltujen tuotantotilausten luontia.</span><span class="sxs-lookup"><span data-stu-id="04a60-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="04a60-113">Suunnittelun optimointia on käytettävä kaikissa uusissa käyttöönotoissa, joissa ei luoda suunniteltuja tuotantotilauksia pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="04a60-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="04a60-114">Aiemmin luotujen ympäristöjen omistajat, jotka käyttävät sisäistä pääsuunnittelumoduulia suunniteltuja tuotantotilauksia luomatta, saavat poikkeusprosessia koskevan sähköpostin.</span><span class="sxs-lookup"><span data-stu-id="04a60-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="04a60-115">Siirtyminen suunnittelun optimointiin kannattaa arvioida ja suunnitella yhteistyössä kumppanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="04a60-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="04a60-116">Ennen suunnittelun optimoinnin ottamista käyttöön on syytä arvioida suunnittelun optimoinnin sopivuusanalyysin tulokset.</span><span class="sxs-lookup"><span data-stu-id="04a60-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="04a60-117">Lisätietoja on kohdassa [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="04a60-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="04a60-118">Saatavuus</span><span class="sxs-lookup"><span data-stu-id="04a60-118">Availability</span></span>
<span data-ttu-id="04a60-119">Suunnittelun optimointi on tällä hetkellä käytettävissä seuraavilla Azure-maantieteellisillä alueilla: Yhdysvallat, Kanada, Eurooppa, Iso-Britannia ja Australia.</span><span class="sxs-lookup"><span data-stu-id="04a60-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="04a60-120">Jos yrität asentaa apuohjelman toiselta maantieteelliseltä alueelta, LCS näyttää sanoman, jonka mukaan tätä maantieteellistä aluetta ei tueta.</span><span class="sxs-lookup"><span data-stu-id="04a60-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="04a60-121">Huomaa, että suunnittelun optimointi ei tue Dynamics 365 Supply Chain Management -järjestelmän paikallisia käyttöönottoja.</span><span class="sxs-lookup"><span data-stu-id="04a60-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="04a60-122">Käyttöoikeudet</span><span class="sxs-lookup"><span data-stu-id="04a60-122">Licensing</span></span>

<span data-ttu-id="04a60-123">Jos voit suorittaa pääsuunnittelua nykyisellä käyttöoikeudella, suunnittelun optimoinnin käytön aloittamista varten ei tarvitse ostaa käyttöoikeutta.</span><span class="sxs-lookup"><span data-stu-id="04a60-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="04a60-124">Lisäosan asentaminen</span><span class="sxs-lookup"><span data-stu-id="04a60-124">Install the add-in</span></span>

<span data-ttu-id="04a60-125">Suunnittelun optimoinnin käyttöä varten on asennettava Dynamics 365 Supply Chain Managementin suunnittelun optimoinnin lisäosa.</span><span class="sxs-lookup"><span data-stu-id="04a60-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="04a60-126">Voit käyttää lisäosaa LCS-projektista ja ottaa suunnittelun optimointitoiminnon käyttöön Supply Chain Management -käyttöliittymässä.</span><span class="sxs-lookup"><span data-stu-id="04a60-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="04a60-127">Suunnittelun optimoinnin vaatimus on korkean käytettävyyden ympäristö, jossa LCS on käytössä, taso 2 tai korkeampi (ei OneBox-ympäristö). Käytössä on Dynamics 365 Supply Chain Management -sovelluksen versio 10.0.7 tai uudempi versio.</span><span class="sxs-lookup"><span data-stu-id="04a60-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="04a60-128">Jos yrität asentaa apuohjelman OneBox-ympäristöön, asennus ei ole valmis ja sinun on peruutettava asennus.</span><span class="sxs-lookup"><span data-stu-id="04a60-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="04a60-129">Kirjaudu sisään LCS:ään ja avaa sopiva ympäristö.</span><span class="sxs-lookup"><span data-stu-id="04a60-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="04a60-130">Valitse **Kaikki tiedot**.</span><span class="sxs-lookup"><span data-stu-id="04a60-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="04a60-131">Vieritä alas **Ympäristön lisäosat** -pikavälilehteen.</span><span class="sxs-lookup"><span data-stu-id="04a60-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="04a60-132">Valitse **Asenna uusi lisäosa**.</span><span class="sxs-lookup"><span data-stu-id="04a60-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="04a60-133">Valitse **Suunnittelun optimointi**.</span><span class="sxs-lookup"><span data-stu-id="04a60-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="04a60-134">Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.</span><span class="sxs-lookup"><span data-stu-id="04a60-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="04a60-135">Valitse **Asenna**.</span><span class="sxs-lookup"><span data-stu-id="04a60-135">Select **Install**.</span></span>
1. <span data-ttu-id="04a60-136">**Ympäristön lisäosat** -pikavälilehdessä pitäisi näkyä, että suunnittelun optimointia asennetaan.</span><span class="sxs-lookup"><span data-stu-id="04a60-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="04a60-137">Muutaman minuutin kuluttua arvon **Asennettaan** pitäisi muuttua arvoksi **Asennettu** (voi vaatia sivun päivityksen).</span><span class="sxs-lookup"><span data-stu-id="04a60-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="04a60-138">Kun asennus on valmis, voit aktivoida suunnittelun optimoinnin Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="04a60-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="04a60-139">Suunnittelun optimoinnin apuohjelman asennuksen päätarkoitus on yhdistää palvelu ja ympäristö.</span><span class="sxs-lookup"><span data-stu-id="04a60-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="04a60-140">Tämän vuoksi apuohjelma on asennettava erikseen jokaiseen ympäristöön, jossa suunnittelun optimointia käytetään, riippumatta ympäristöjen välillä siirrettävästä koodista riippumatta.</span><span class="sxs-lookup"><span data-stu-id="04a60-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="04a60-141">Suunnittelun optimoinnin integrointi</span><span class="sxs-lookup"><span data-stu-id="04a60-141">Planning Optimization integration</span></span>

<span data-ttu-id="04a60-142">Voit määrittää, käytetäänkö suunnittelun optimoinnin lisää pääsuunnittelussa valitsemalla **Pääsuunnittelu** \> **Asetukset** \> **Suunnittelun optimoinnin parametrit**.</span><span class="sxs-lookup"><span data-stu-id="04a60-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="04a60-143">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="04a60-143">Connection status</span></span>

<span data-ttu-id="04a60-144">Yhteyden tila ilmaisee Supply Chain Managementin ja suunnittelun optimointipalvelun välisen yhteyden nykyisen tilan.</span><span class="sxs-lookup"><span data-stu-id="04a60-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="04a60-145">Mahdolliset arvot ovat seuraavassa taulukossa.</span><span class="sxs-lookup"><span data-stu-id="04a60-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="04a60-146">Yhteyden tila</span><span class="sxs-lookup"><span data-stu-id="04a60-146">Connection status</span></span> | <span data-ttu-id="04a60-147">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="04a60-147">Description</span></span> | <span data-ttu-id="04a60-148">Voiko suunnittelun optimointia käyttää?</span><span class="sxs-lookup"><span data-stu-id="04a60-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="04a60-149">Yhdistetty</span><span class="sxs-lookup"><span data-stu-id="04a60-149">Connected</span></span> | <span data-ttu-id="04a60-150">Suunnittelun optimointipalvelun ja Supply Chain Managementin välille on muodostettu yhteys.</span><span class="sxs-lookup"><span data-stu-id="04a60-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="04a60-151">Kyllä</span><span class="sxs-lookup"><span data-stu-id="04a60-151">Yes</span></span> |
| <span data-ttu-id="04a60-152">Otetaan yhteyttä käyttöön</span><span class="sxs-lookup"><span data-stu-id="04a60-152">Enabling connection</span></span> | <span data-ttu-id="04a60-153">Pyyntöä ottaa yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="04a60-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="04a60-154">Ei</span><span class="sxs-lookup"><span data-stu-id="04a60-154">No</span></span> |
| <span data-ttu-id="04a60-155">Yhteys katkaistu</span><span class="sxs-lookup"><span data-stu-id="04a60-155">Disconnected</span></span> | <span data-ttu-id="04a60-156">Suunnittelun optimointipalveluun ei ole yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="04a60-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="04a60-157">Yhteys voidaan ottaa käyttöön LCS:ssä aiemmin tässä ohjeaiheessa kuvatulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="04a60-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="04a60-158">Ei</span><span class="sxs-lookup"><span data-stu-id="04a60-158">No</span></span> |
| <span data-ttu-id="04a60-159">Poistettaan yhteyttä käytöstä</span><span class="sxs-lookup"><span data-stu-id="04a60-159">Disabling connection</span></span> | <span data-ttu-id="04a60-160">Pyyntöä katkaista yhteys suunnittelun optimointipalveluun käsitellään.</span><span class="sxs-lookup"><span data-stu-id="04a60-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="04a60-161">Ei</span><span class="sxs-lookup"><span data-stu-id="04a60-161">No</span></span> |
| <span data-ttu-id="04a60-162">Tilan saaminen</span><span class="sxs-lookup"><span data-stu-id="04a60-162">Getting status</span></span> | <span data-ttu-id="04a60-163">Järjestelmä odottaa tilatietoja suunnittelun optimointipalvelusta.</span><span class="sxs-lookup"><span data-stu-id="04a60-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="04a60-164">Ei</span><span class="sxs-lookup"><span data-stu-id="04a60-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="04a60-165">Käytä suunnittelun optimointia -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="04a60-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="04a60-166">**Käytä suunnittelun optimointia** -vaihtoehdossa valittu asetus määrittää, mitä suunnittelumoduulia pääsuunnittelussa käytetään:</span><span class="sxs-lookup"><span data-stu-id="04a60-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="04a60-167">**Kyllä** – suunnittelun optimointia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="04a60-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="04a60-168">**Ei** – Supply Chain Managementin sisäistä suunnittelumoduulia käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="04a60-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="04a60-169">Jos Supply Chain Managementin sisäiselle suunnittelumoduulille aiemmin luodut suunnittelun erätyöt käynnistyvät, kun **Käytä suunnittelun optimointia** -asetuksena on **Kyllä**, kyseiset työt epäonnistuvat.</span><span class="sxs-lookup"><span data-stu-id="04a60-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="04a60-170">Integrointi määrityksiin</span><span class="sxs-lookup"><span data-stu-id="04a60-170">Integration with the setup</span></span>

<span data-ttu-id="04a60-171">Jos suunnittelun optimointi on otettu käyttöön, suunnittelun optimoinnin apuohjelmaa käytetään pääsuunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="04a60-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="04a60-172">Tällä on vaikutusta pääsuunnittelun tuloksiin ja toimintoihin.</span><span class="sxs-lookup"><span data-stu-id="04a60-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04a60-173">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="04a60-173">Additional resources</span></span>

[<span data-ttu-id="04a60-174">Esiversion ehdot</span><span class="sxs-lookup"><span data-stu-id="04a60-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="04a60-175">Suunnittelun optimoinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="04a60-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="04a60-176">Suunnittelun optimoinnin sopivuusanalyysi</span><span class="sxs-lookup"><span data-stu-id="04a60-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="04a60-177">Suunnitelman historia- ja suunnittelulokien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="04a60-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="04a60-178">Suodattimien käyttäminen suunnitelmaan</span><span class="sxs-lookup"><span data-stu-id="04a60-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="04a60-179">Suunnittelutyön peruuttaminen</span><span class="sxs-lookup"><span data-stu-id="04a60-179">Cancel a planning job</span></span>](cancel-planning-job.md)
