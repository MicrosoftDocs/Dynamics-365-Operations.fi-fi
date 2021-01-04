---
title: Kustannusseurannan mobiilityötila
description: Tässä ohjeaiheessa on tietoja kustannusseurannan mobiilityötilasta. Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4fc35feb4f3a67ba9c8c70c2d2f8c07cb944b0f6
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/03/2020
ms.locfileid: "4442991"
---
# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="1a641-104">Kustannusseurannan mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="1a641-104">Cost controlling mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a641-105">Tässä ohjeaiheessa on tietoja **Kustannusseuranta**-mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="1a641-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="1a641-106">Kustannuspaikan johtajat voivat käyttää työtilaa tarkastellakseen kustannuspaikan suorituskykytietoja milloin ja missä tahansa.</span><span class="sxs-lookup"><span data-stu-id="1a641-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="1a641-107">Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="1a641-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="1a641-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="1a641-108">Overview</span></span>
<span data-ttu-id="1a641-109">**Kustannusten hallinnan** mobiilityötila sisältää kustannuspaikkojen nykyisen suorituskyvyn välittömän näkymän vertaamalla toteutuneita kustannuksia budjetoituihin kustannuksiin.</span><span class="sxs-lookup"><span data-stu-id="1a641-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="1a641-110">Voit porautua yksittäisten kustannuselementtien tilaan.</span><span class="sxs-lookup"><span data-stu-id="1a641-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="1a641-111">Työntekijä voi esimerkiksi saada kutsun kansainväliseen konferenssiin, mutta organisaation on katettava kaikki matkakulut.</span><span class="sxs-lookup"><span data-stu-id="1a641-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="1a641-112">Työntekijä pyytää esimieheltä lupaa osallistua konferenssiin.</span><span class="sxs-lookup"><span data-stu-id="1a641-112">The employee asks their manager whether they can attend the conference.</span></span> <span data-ttu-id="1a641-113">Esimies avaa nopeasti **kustannusten hallinnan** mobiilityötilan puhelimessaan nähdäkseen, onko budjetissa varaa työntekijän osallistumiseen kokoukseen.</span><span class="sxs-lookup"><span data-stu-id="1a641-113">The manager opens the **Cost controlling** mobile workspace on their mobile device to see whether there is budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="1a641-114">Tietoturva</span><span class="sxs-lookup"><span data-stu-id="1a641-114">Data security</span></span>
<span data-ttu-id="1a641-115">**Kustannusten hallinnan** mobiilityötilan tiedot suojataan käyttäjän tunnistetietojen mukaan.</span><span class="sxs-lookup"><span data-stu-id="1a641-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="1a641-116">Kustannuspaikan johtajan on sallittu nähdä vain tiedot omasta kustannuspaikastaan.</span><span class="sxs-lookup"><span data-stu-id="1a641-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="1a641-117">Käyttöoikeustason tietoturva on hallittu **Kustannuslaskenta**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="1a641-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="1a641-118">Kustannusten kirjanpitäjät määrittävät **kustannusten hallinnan** mobiilityötilan **Kustannuslaskenta**-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="1a641-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="1a641-119">Työtila on käytettävissä sovelluksessa, kun se on julkaistu mobiilisovellukseen.</span><span class="sxs-lookup"><span data-stu-id="1a641-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="1a641-120">Näin varmistetaan, että kaikkien kustannuspaikkojen johtajat organisaatiossa näkevät tiedot samassa muodossa.</span><span class="sxs-lookup"><span data-stu-id="1a641-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="1a641-121">Toiminnot, näkymät ja linkit</span><span class="sxs-lookup"><span data-stu-id="1a641-121">Actions, views, and links</span></span>
<span data-ttu-id="1a641-122">Seuraavat toiminnot, näkymät ja linkit sisältyvät **Kustannusseuranta**-mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="1a641-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="1a641-123">**Toiminnot:**</span><span class="sxs-lookup"><span data-stu-id="1a641-123">**Actions:**</span></span>

    -   <span data-ttu-id="1a641-124">Valitse asettelu **Valitse konfiguraatio** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1a641-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="1a641-125">Valitse kustannuspaikat, joiden tiedot suodatetaan **Valitse kustannusobjekti** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="1a641-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="1a641-126">Luettelossa näytettävät kustannuspaikat riippuvat **Kustannuslaskenta**-moduulissa annetuista käyttöoikeuksista.</span><span class="sxs-lookup"><span data-stu-id="1a641-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="1a641-127">**Näkymät:** voit tarkastella korteissa valittujen toimintojen sekä **Kustannuslaskenta**-moduulissa valitun konfiguraation perusteella seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="1a641-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="1a641-128">Todellinen vs. budjetti (kuluva kausi)</span><span class="sxs-lookup"><span data-stu-id="1a641-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="1a641-129">Todellinen vs. muutettu budjetti (kuluva kausi)</span><span class="sxs-lookup"><span data-stu-id="1a641-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="1a641-130">Todellinen vs. budjetti (edellinen kausi)</span><span class="sxs-lookup"><span data-stu-id="1a641-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="1a641-131">Todellinen vs tarkistettu budjetti (edellinen kausi)</span><span class="sxs-lookup"><span data-stu-id="1a641-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="1a641-132">Todellinen vs. budjetti (vuoden alusta)</span><span class="sxs-lookup"><span data-stu-id="1a641-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="1a641-133">Todellinen vs tarkistettu budjetti (vuoden alusta)</span><span class="sxs-lookup"><span data-stu-id="1a641-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="1a641-134">Jokaisella kortilla näytetään seuraavat summat: Todellinen, Budjetti, Varianssi ja Varianssi-%.</span><span class="sxs-lookup"><span data-stu-id="1a641-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="1a641-135">**Linkit:**</span><span class="sxs-lookup"><span data-stu-id="1a641-135">**Links:**</span></span>

    -   <span data-ttu-id="1a641-136">Kuluvan kauden tiedot</span><span class="sxs-lookup"><span data-stu-id="1a641-136">Details for current period</span></span>
    -   <span data-ttu-id="1a641-137">Edellisen kauden tiedot</span><span class="sxs-lookup"><span data-stu-id="1a641-137">Details for previous period</span></span>
    -   <span data-ttu-id="1a641-138">Kuluvan vuoden tiedot</span><span class="sxs-lookup"><span data-stu-id="1a641-138">Details for year to date</span></span>

    <span data-ttu-id="1a641-139">Kun valitset linkin, kullekin kustannuselementille näytetään kortti.</span><span class="sxs-lookup"><span data-stu-id="1a641-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="1a641-140">Kullakin kortilla näytetään seuraavat summat: Todellinen, budjetti, budjetin varianssi, budjetin varianssi-%, muokattu budjetti, muokattu budjetin varianssi ja muokattu budjetin varianssi-%.</span><span class="sxs-lookup"><span data-stu-id="1a641-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="1a641-141">[![Kustannuselementin kortti ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="1a641-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a641-142">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="1a641-142">Prerequisites</span></span>
<span data-ttu-id="1a641-143">Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="1a641-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a><span data-ttu-id="1a641-144">Edellytykset, jos käytössä on Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1a641-144">Prerequisites if you use Microsoft Dynamics 365 Finance</span></span>
<span data-ttu-id="1a641-145">Jos Finance on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Kustannusten hallinta** -mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="1a641-145">If Finance has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="1a641-146">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="1a641-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="1a641-147">Edellytykset, jos käytössä on versio 1611 ja Platform update 3 tai uudempi</span><span class="sxs-lookup"><span data-stu-id="1a641-147">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="1a641-148">Jos organisaatiossa on otettu käyttöön versio 1611 ja Platform update 3 tai uudempi, järjestelmänvalvojan on toteutettava seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="1a641-148">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1a641-149">Edellytys</span><span class="sxs-lookup"><span data-stu-id="1a641-149">Prerequisite</span></span></th>
<th><span data-ttu-id="1a641-150">Rooli</span><span class="sxs-lookup"><span data-stu-id="1a641-150">Role</span></span></th>
<th><span data-ttu-id="1a641-151">kuvaus</span><span class="sxs-lookup"><span data-stu-id="1a641-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1a641-152">Ota KB 4013633 käyttöön.</span><span class="sxs-lookup"><span data-stu-id="1a641-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="1a641-153">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="1a641-153">System administrator</span></span></td>

<td><span data-ttu-id="1a641-154">KB 4013633 on X++-päivitys tai metatietojen hotfix-korjaus, joka sisältää <strong>Kustannusseuranta</strong>-mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="1a641-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="1a641-155">Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4013633 -päivityksen.</span><span class="sxs-lookup"><span data-stu-id="1a641-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="1a641-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metatietojen hotfix-korjauksen lataaminen Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="1a641-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="1a641-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</span><span class="sxs-lookup"><span data-stu-id="1a641-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="1a641-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>SCMMobile</strong>-mallin ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</span><span class="sxs-lookup"><span data-stu-id="1a641-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="1a641-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="1a641-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1a641-160">Julkaise <strong>Kustannusseuranta</strong>-mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="1a641-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="1a641-161">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="1a641-161">System administrator</span></span></td>
<td><span data-ttu-id="1a641-162">Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="1a641-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="1a641-163">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="1a641-163">Download and install the mobile app</span></span>
<span data-ttu-id="1a641-164">Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:</span><span class="sxs-lookup"><span data-stu-id="1a641-164">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="1a641-165">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="1a641-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="1a641-166">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="1a641-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="1a641-167">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="1a641-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="1a641-168">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="1a641-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="1a641-169">Anna Dynamics 365 -URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="1a641-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="1a641-170">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="1a641-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="1a641-171">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="1a641-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="1a641-172">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="1a641-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="1a641-173">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="1a641-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="1a641-174">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="1a641-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="1a641-175">Tarkastele kustannuspaikkasi suorituskykyä kustannusten hallinnan mobiilissa työtilassa</span><span class="sxs-lookup"><span data-stu-id="1a641-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="1a641-176">Valitse mobiililaitteessasi **Kustannusten hallinta** -työtila.</span><span class="sxs-lookup"><span data-stu-id="1a641-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="1a641-177">Valitse **Kustannusobjektin hallinta**.</span><span class="sxs-lookup"><span data-stu-id="1a641-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="1a641-178">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="1a641-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="1a641-179">Valitse **Valitse konfigurointi** valitaksesi kustannusten hallinnan asettelun.</span><span class="sxs-lookup"><span data-stu-id="1a641-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="1a641-180">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="1a641-180">Select **Done**.</span></span>
6.  <span data-ttu-id="1a641-181">Valitse **Toiminnot**.</span><span class="sxs-lookup"><span data-stu-id="1a641-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="1a641-182">Valitse **Valitse kustannusobjekti** valitaksesi kustannuspaikat, joihin sinulla on käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="1a641-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="1a641-183">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="1a641-183">Select **Done**.</span></span>
9.  <span data-ttu-id="1a641-184">Kustannuspaikan yleisen suorituskyvyn tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="1a641-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="1a641-185">Napsauta **Kuluvan kauden tiedot** -linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1a641-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="1a641-186">Yksittäisten kustannuselementtien suorituskyvyn tarkasteleminen.</span><span class="sxs-lookup"><span data-stu-id="1a641-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="1a641-187">Voit myös etsiä tiettyjä kustannuselementtejä.</span><span class="sxs-lookup"><span data-stu-id="1a641-187">You can also search for specific cost elements.</span></span>

