---
title: "Kustannusseurannan mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja kustannusseurannan mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6019634c47bd97fb16ea8aaf029ea176f095b8b6
ms.contentlocale: fi-fi
ms.lasthandoff: 08/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="859ca-104">Kustannusseurannan mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="859ca-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="859ca-105">Tässä ohjeaiheessa on tietoja **Kustannusseuranta**-mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="859ca-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="859ca-106">Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="859ca-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="859ca-107">Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="859ca-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="859ca-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="859ca-108">Overview</span></span>
<span data-ttu-id="859ca-109">**Kustannusten hallinnan** mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="859ca-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="859ca-110">Voit porautua yksittäisten kustannuselementtien tilaan.</span><span class="sxs-lookup"><span data-stu-id="859ca-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="859ca-111">Työntekijä voi esimerkiksi saada kutsun kansainväliseen konferenssiin, mutta organisaation on katettava kaikki matkakulut.</span><span class="sxs-lookup"><span data-stu-id="859ca-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="859ca-112">Työntekijä kysyy esimieheltään, voiko hän osallistua kokoukseen.</span><span class="sxs-lookup"><span data-stu-id="859ca-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="859ca-113">Esimies avaa nopeasti **kustannusten hallinnan** mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.</span><span class="sxs-lookup"><span data-stu-id="859ca-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="859ca-114">Tietoturva</span><span class="sxs-lookup"><span data-stu-id="859ca-114">Data security</span></span>
<span data-ttu-id="859ca-115">**Kustannusten hallinnan** mobiilityötilan tiedot suojataan käyttäjän tunnistetietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="859ca-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="859ca-116">Kustannuspaikan johtajan on sallittu nähdä vain tiedot omasta kustannuspaikastaan.</span><span class="sxs-lookup"><span data-stu-id="859ca-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="859ca-117">Käyttöoikeustason tietoturva on hallittu **Kustannuslaskenta**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="859ca-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="859ca-118">Kustannusten kirjanpitäjät määrittävät **kustannusten hallinnan** mobiilityötilan **Kustannuslaskenta**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="859ca-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="859ca-119">Työtila on käytettävissä sovelluksessa, kun se on julkaistu mobiilisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="859ca-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="859ca-120">Näin varmistetaan, että kaikkien kustannuspaikkojen johtajat organisaatiossa näkevät tiedot samassa muodossa.</span><span class="sxs-lookup"><span data-stu-id="859ca-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="859ca-121">Toiminnot, näkymät ja linkit</span><span class="sxs-lookup"><span data-stu-id="859ca-121">Actions, views, and links</span></span>
<span data-ttu-id="859ca-122">Seuraavat toiminnot, näkymät ja linkit sisältyvät **Kustannusseuranta**-mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="859ca-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="859ca-123">**Toiminnot:**</span><span class="sxs-lookup"><span data-stu-id="859ca-123">**Actions:**</span></span>

    -   <span data-ttu-id="859ca-124">Valitse asettelu **Valitse konfiguraatio** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="859ca-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="859ca-125">Valitse kustannuspaikat, joiden tiedot suodatetaan **Valitse kustannusobjekti** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="859ca-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="859ca-126">Luettelossa näytettävät kustannuspaikat riippuvat **Kustannuslaskenta**-moduulissa annetuista käyttöoikeuksista.</span><span class="sxs-lookup"><span data-stu-id="859ca-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="859ca-127">**Näkymät:** voit tarkastella korteissa valittujen toimintojen sekä **Kustannuslaskenta**-moduulissa valitun konfiguraation perusteella seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="859ca-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="859ca-128">Todellinen vs. budjetti (kuluva kausi)</span><span class="sxs-lookup"><span data-stu-id="859ca-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="859ca-129">Todellinen vs. muutettu budjetti (kuluva kausi)</span><span class="sxs-lookup"><span data-stu-id="859ca-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="859ca-130">Todellinen vs. budjetti (edellinen kausi)</span><span class="sxs-lookup"><span data-stu-id="859ca-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="859ca-131">Todellinen vs tarkistettu budjetti (edellinen kausi)</span><span class="sxs-lookup"><span data-stu-id="859ca-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="859ca-132">Todellinen vs. budjetti (vuoden alusta)</span><span class="sxs-lookup"><span data-stu-id="859ca-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="859ca-133">Todellinen vs tarkistettu budjetti (vuoden alusta)</span><span class="sxs-lookup"><span data-stu-id="859ca-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="859ca-134">Jokaisella kortilla näytetään seuraavat summat: Todellinen, Budjetti, Varianssi ja Varianssi-%.</span><span class="sxs-lookup"><span data-stu-id="859ca-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="859ca-135">**Linkit:**</span><span class="sxs-lookup"><span data-stu-id="859ca-135">**Links:**</span></span>

    -   <span data-ttu-id="859ca-136">Kuluvan kauden tiedot</span><span class="sxs-lookup"><span data-stu-id="859ca-136">Details for current period</span></span>
    -   <span data-ttu-id="859ca-137">Edellisen kauden tiedot</span><span class="sxs-lookup"><span data-stu-id="859ca-137">Details for previous period</span></span>
    -   <span data-ttu-id="859ca-138">Kuluvan vuoden tiedot</span><span class="sxs-lookup"><span data-stu-id="859ca-138">Details for year to date</span></span>

    <span data-ttu-id="859ca-139">Kun valitset linkin, kullekin kustannuselementille näytetään kortti.</span><span class="sxs-lookup"><span data-stu-id="859ca-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="859ca-140">Kullakin kortilla näytetään seuraavat summat: Todellinen, budjetti, budjetin varianssi, budjetin varianssi %, muokattu budjetti, muokattu budjetin varianssi ja muokattu budjetin varianssi %.</span><span class="sxs-lookup"><span data-stu-id="859ca-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="859ca-141">[![Kustannuselementin kortti ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="859ca-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="859ca-142">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="859ca-142">Prerequisites</span></span>
<span data-ttu-id="859ca-143">Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="859ca-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="859ca-144">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys</span><span class="sxs-lookup"><span data-stu-id="859ca-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span>
<span data-ttu-id="859ca-145">Jos Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on otettu organisaatiossa käyttöön, järjestelmänvalvojan on julkaistava **Kustannusseuranta**-mobiilityötilassa.</span><span class="sxs-lookup"><span data-stu-id="859ca-145">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="859ca-146">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span><span class="sxs-lookup"><span data-stu-id="859ca-146">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="859ca-147">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operations -versio 1611, johon on asennettu vähintään ympäristöpäivitys 3.</span><span class="sxs-lookup"><span data-stu-id="859ca-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="859ca-148">Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operations -versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="859ca-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="859ca-149">Edellytys</span><span class="sxs-lookup"><span data-stu-id="859ca-149">Prerequisite</span></span></th>
<th><span data-ttu-id="859ca-150">Rooli</span><span class="sxs-lookup"><span data-stu-id="859ca-150">Role</span></span></th>
<th><span data-ttu-id="859ca-151">kuvaus</span><span class="sxs-lookup"><span data-stu-id="859ca-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="859ca-152">Ota KB 4013633 käyttöön.</span><span class="sxs-lookup"><span data-stu-id="859ca-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="859ca-153">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="859ca-153">System administrator</span></span></td>

<td><span data-ttu-id="859ca-154">KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Kustannusseuranta</strong>-mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="859ca-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="859ca-155">Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.</span><span class="sxs-lookup"><span data-stu-id="859ca-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="859ca-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="859ca-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="859ca-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Asenna metatietojen korjaustiedosto</a>.</span><span class="sxs-lookup"><span data-stu-id="859ca-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="859ca-158"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</span><span class="sxs-lookup"><span data-stu-id="859ca-158"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="859ca-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Ota käyttöönotettava paketti käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="859ca-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="859ca-160">Julkaise <strong>Kustannusseuranta</strong>-mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="859ca-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="859ca-161">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="859ca-161">System administrator</span></span></td>
<td><span data-ttu-id="859ca-162">Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="859ca-162">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="859ca-163">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="859ca-163">Download and install the mobile app</span></span>
<span data-ttu-id="859ca-164">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="859ca-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="859ca-165">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="859ca-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="859ca-166">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="859ca-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="859ca-167">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="859ca-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="859ca-168">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="859ca-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="859ca-169">Anna Dynamics 365 -URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="859ca-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="859ca-170">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="859ca-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="859ca-171">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="859ca-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="859ca-172">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="859ca-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="859ca-173">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="859ca-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="859ca-174">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="859ca-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="859ca-175">Tarkastele kustannuspaikkasi suorituskykyä kustannusten hallinnan mobiilissa työtilassa</span><span class="sxs-lookup"><span data-stu-id="859ca-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="859ca-176">Valitse mobiililaitteessasi **Kustannusten hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="859ca-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="859ca-177">Valitse **Kustannusobjektin hallinta**.</span><span class="sxs-lookup"><span data-stu-id="859ca-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="859ca-178">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="859ca-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="859ca-179">Valitse **Valitse konfigurointi** valitaksesi kustannusten hallinnan asettelun.</span><span class="sxs-lookup"><span data-stu-id="859ca-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="859ca-180">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="859ca-180">Select **Done**.</span></span>
6.  <span data-ttu-id="859ca-181">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="859ca-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="859ca-182">Valitse **Valitse kustannusobjekti** valitaksesi kustannuspaikat, joihin sinulla on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="859ca-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="859ca-183">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="859ca-183">Select **Done**.</span></span>
9.  <span data-ttu-id="859ca-184">Kustannuspaikan yleisen suorituskyvyn tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="859ca-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="859ca-185">Napsauta **Kuluvan kauden tiedot** -linkkiä.</span><span class="sxs-lookup"><span data-stu-id="859ca-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="859ca-186">Yksittäisten kustannuselementtien suorituskyvyn tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="859ca-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="859ca-187">Voit myös etsiä tiettyjä kustannuselementtejä.</span><span class="sxs-lookup"><span data-stu-id="859ca-187">You can also search for specific cost elements.</span></span>


