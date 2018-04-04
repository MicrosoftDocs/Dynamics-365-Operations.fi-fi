---
title: "Projektin aikamerkintöjen mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja projektin aikamerkintöjen mobiilityötilasta. Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella."
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 9bf79af6eea6f899158fc3c8d523587cb11c90ad
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="7387e-104">Projektin aikamerkintöjen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="7387e-104">Project time entry mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7387e-105">Tässä ohjeaiheessa on tietoja **projektin aikamerkintöjen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="7387e-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="7387e-106">Työtilan avulla käyttäjät voivat syöttää ja tallentaa projektin aikakirjauksia mobiililaittella.</span><span class="sxs-lookup"><span data-stu-id="7387e-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="7387e-107">Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="7387e-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="7387e-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="7387e-108">Overview</span></span>
<span data-ttu-id="7387e-109">Projektiresurssit ovat kohteessa tai liikkeellä osana päivittäistä työtään.</span><span class="sxs-lookup"><span data-stu-id="7387e-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="7387e-110">**Projektin aikamerkinnät** -mobiilityötilan avulla käyttäjät voivat syöttää laskutettavan tai ei-laskutettavan aikansa projektiin valitsemallaan mobiililaitteella.</span><span class="sxs-lookup"><span data-stu-id="7387e-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="7387e-111">Tämän ansiosta projektiresurssit voivat tehdä aikakirjauksia missä ja milloin tahansa.</span><span class="sxs-lookup"><span data-stu-id="7387e-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="7387e-112">He voivat myös tarkastella aiemmin kirjattuja merkintöjä.</span><span class="sxs-lookup"><span data-stu-id="7387e-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="7387e-113">Käyttäjät voivat suorittaa seuraavat tehtävät **projektin aikamerkintöjen** mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="7387e-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="7387e-114">Anna valitulle päivämäärällä tuntien määrä, jonka olet käyttänyt tietyn tehtävän suorittamiseen.</span><span class="sxs-lookup"><span data-stu-id="7387e-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="7387e-115">Hae projekti, jolle haluat kirjata tunteja projektin tai asiakkaan nimellä .</span><span class="sxs-lookup"><span data-stu-id="7387e-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="7387e-116">Määritä käyttämällesi ajalle luokka ja tehtävä.</span><span class="sxs-lookup"><span data-stu-id="7387e-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="7387e-117">Kirjaa aika projektiin laskutettavaksi tai ei-laskutettavaksi.</span><span class="sxs-lookup"><span data-stu-id="7387e-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="7387e-118">Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="7387e-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7387e-119">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="7387e-119">Prerequisites</span></span>
<span data-ttu-id="7387e-120">Edellytykset vaihtelevat sen mukaan, mikä Microsoft Dynamics 365 -versio on otettu käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="7387e-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="7387e-121">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7387e-121">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="7387e-122">Jos Microsoft Dynamics 365 for Finance and Operations on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Projektin aikamerkintä** -mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="7387e-122">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="7387e-123">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="7387e-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="7387e-124">Edellytykset, jos käytössä on Microsoft Dynamics 365 for Operations -versio 1611, johon on asennettu vähintään ympäristöpäivitys 3.</span><span class="sxs-lookup"><span data-stu-id="7387e-124">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="7387e-125">Jos organisaatiossa on otettu käyttöön Microsoft Dynamics 365 for Operations -versio 1611, jossa on vähintään ympäristöpäivitys 3, järjestelmänvalvojan on toteutettava seuraavat edellytykset.</span><span class="sxs-lookup"><span data-stu-id="7387e-125">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7387e-126">Edellytys</span><span class="sxs-lookup"><span data-stu-id="7387e-126">Prerequisite</span></span></th>
<th><span data-ttu-id="7387e-127">Rooli</span><span class="sxs-lookup"><span data-stu-id="7387e-127">Role</span></span></th>
<th><span data-ttu-id="7387e-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7387e-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="7387e-129">KB 4018050 -käyttöönotto.</span><span class="sxs-lookup"><span data-stu-id="7387e-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="7387e-130">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="7387e-130">System administrator</span></span></td>
<td><span data-ttu-id="7387e-131">KB 4018050 on X++-päivitys tai metatietojen korjaus, joka sisältää <strong>projektin aikakirjausten</strong> mobiilityötilan.</span><span class="sxs-lookup"><span data-stu-id="7387e-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="7387e-132">Järjestelmänvalvojan on toimittava seuraavasti asentaakseen KB 4018050 -päivityksen.</span><span class="sxs-lookup"><span data-stu-id="7387e-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="7387e-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Lataa metatietojen hotfix-korjaus Microsoft Dynamics Lifecycle Servicesistä (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="7387e-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="7387e-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Asenna metatietojen korjaustiedosto</a>.</span><span class="sxs-lookup"><span data-stu-id="7387e-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="7387e-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Luo käyttöön otettava paketti</a>, joka sisältää <strong>ApplicationSuite</strong>- ja <strong>ProjectMobile</strong>-mallit ja lataa sitten käyttöön otettava paketti elinkaaripalveluihin.</span><span class="sxs-lookup"><span data-stu-id="7387e-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="7387e-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Ota käyttöönotettava paketti käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="7387e-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7387e-137">Julkaise <strong>projektin aikamerkintöjen</strong> mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="7387e-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="7387e-138">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="7387e-138">System administrator</span></span></td>
<td><span data-ttu-id="7387e-139">Lisätietoja on ohjeaiheessa <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="7387e-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="7387e-140">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="7387e-140">Download and install the mobile app</span></span>

<span data-ttu-id="7387e-141">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="7387e-141">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="7387e-142">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="7387e-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="7387e-143">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="7387e-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="7387e-144">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="7387e-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="7387e-145">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="7387e-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="7387e-146">Anna Dynamics 365 -URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="7387e-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="7387e-147">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="7387e-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="7387e-148">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="7387e-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="7387e-149">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="7387e-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="7387e-150">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="7387e-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="7387e-151">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="7387e-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="7387e-152">Aikakirjausten syöttäminen Projektin aikakirjausten mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="7387e-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="7387e-153">Valitse mobiililaitteessasi **Projektin aikakirjausten** työtila.</span><span class="sxs-lookup"><span data-stu-id="7387e-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="7387e-154">Valitse **Aikamerkintä**.</span><span class="sxs-lookup"><span data-stu-id="7387e-154">Select **Time entry**.</span></span> <span data-ttu-id="7387e-155">Kuluvan viikon kalenteripäivät näytetään.</span><span class="sxs-lookup"><span data-stu-id="7387e-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="7387e-156">Napsauta valitun päivän kohdalla **Toiminnot** &gt; **Uusi kirjaus**.</span><span class="sxs-lookup"><span data-stu-id="7387e-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="7387e-157">Anna kirjattava tuntien määrä.</span><span class="sxs-lookup"><span data-stu-id="7387e-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="7387e-158">Valitse aikakirjauksen kohdeprojekti.</span><span class="sxs-lookup"><span data-stu-id="7387e-158">Select the project for the time entry.</span></span> <span data-ttu-id="7387e-159">Luettelo koostuu projekteista, jotka on ladattu sovellukseen offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7387e-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="7387e-160">Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7387e-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7387e-161">Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="7387e-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="7387e-162">Jos projekti ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7387e-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="7387e-163">Voit hakea nimen, projektin nimen tai asiakkaan perusteella.</span><span class="sxs-lookup"><span data-stu-id="7387e-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="7387e-164">Valitse luokka.</span><span class="sxs-lookup"><span data-stu-id="7387e-164">Select a category.</span></span> <span data-ttu-id="7387e-165">Luettelo koostuu luokista, jotka on ladattu sovellukseen offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7387e-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="7387e-166">Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7387e-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7387e-167">Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="7387e-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="7387e-168">Jos luokka ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7387e-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="7387e-169">Etsi luokan tai luokan nimen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7387e-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="7387e-170">Valitse tehtävä.</span><span class="sxs-lookup"><span data-stu-id="7387e-170">Select an activity.</span></span> <span data-ttu-id="7387e-171">Luettelo koostuu tehtävistä, jotka on ladattu sovellukseen offline-käyttöä varten.</span><span class="sxs-lookup"><span data-stu-id="7387e-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="7387e-172">Oletusarvon mukaan ladataan 50 nimikettä, mutta sovelluskehittäjä voi muuttaa tätä määrää.</span><span class="sxs-lookup"><span data-stu-id="7387e-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="7387e-173">Lisätietoja on ohjeaiheessa [Mobiiliympäristö](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="7387e-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="7387e-174">Jos tehtävä ei ole luettelossa, valitse **Hae**.</span><span class="sxs-lookup"><span data-stu-id="7387e-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="7387e-175">Etsi tehtävän numeron tai tarkoituksen mukaan.</span><span class="sxs-lookup"><span data-stu-id="7387e-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="7387e-176">Valitse rivin ominaisuus.</span><span class="sxs-lookup"><span data-stu-id="7387e-176">Select the line property.</span></span>
12. <span data-ttu-id="7387e-177">Voit myös kirjoittaa ulkoisia tai sisäisiä kommentteja.</span><span class="sxs-lookup"><span data-stu-id="7387e-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="7387e-178">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="7387e-178">Select **Done**.</span></span>

