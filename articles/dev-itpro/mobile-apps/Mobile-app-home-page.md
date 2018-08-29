---
title: Dynamics 365 for Unified Operations -mobiilisovelluksen kotisivu
description: "Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Unified Operationsin mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b9cdb2b2c2b5aaf7743cd2cd0dbfee6c602a5a46
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="dynamics-365-for-unified-operations-mobile-app-home-page"></a><span data-ttu-id="db77c-103">Dynamics 365 for Unified Operations -mobiilisovelluksen kotisivu</span><span class="sxs-lookup"><span data-stu-id="db77c-103">Dynamics 365 for Unified Operations mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db77c-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Unified Operationsin mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="db77c-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="db77c-105">Mobiilisovelluksen nimi oli aiemmin *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="db77c-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="db77c-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="db77c-106">Overview</span></span>
--------

<span data-ttu-id="db77c-107">Mobiilisovelluksen avulla organisaatiosi liiketoimintaprosesseja voi käyttää mobiililaitteilla.</span><span class="sxs-lookup"><span data-stu-id="db77c-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="db77c-108">Kun IT-järjestelmänvalvoja ottaa mobiilityötilat käyttöön organisaatiossa, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan.</span><span class="sxs-lookup"><span data-stu-id="db77c-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="db77c-109">Mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="db77c-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="db77c-110">Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="db77c-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="db77c-111">Kun laitteen verkkoyhteys on jälleen käytössä, offline-tilassa tehdyt toimet synkronoidaan automaattisesti Dynamics 365 for Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="db77c-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="db77c-112">IT-järjestelmänvalvojat tai sovelluskehittäjät voivat julkaista organisaatiolleen räätälöityjä mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="db77c-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="db77c-113">Sovellus käyttää olemassa olevia koodiresursseja.</span><span class="sxs-lookup"><span data-stu-id="db77c-113">The app uses your existing code assets.</span></span> <span data-ttu-id="db77c-114">Sinun ei siis täydy luoda tarkistusmenettelyitä, liiketoimintalogiikkaa tai suojausmäärittelyitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="db77c-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="db77c-115">IT-järjestelmänvalvoja tai sovelluskehittäjät voivat suunnitella mobiilityötiloja helposti verkkoasiakasohjelman työtilojen helppokäyttöisellä suunnitteluohjelmalla.</span><span class="sxs-lookup"><span data-stu-id="db77c-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="db77c-116">IT-järjestelmävalvojat voivat halutessaan optimoida työtilojen offline-ominaisuuksia liiketoimintalogiikan laajennuskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="db77c-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="db77c-117">Koska tietojen käsittely ei keskeydy laitteen ollessa offline-tilassa, mobiiliskenaariosi säilyvät mukautuvina, vaikka laitteilla ei olisikaan jatkuvaa verkkoyhteyttä.</span><span class="sxs-lookup"><span data-stu-id="db77c-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="db77c-118">Mobiilisovelluksen osat</span><span class="sxs-lookup"><span data-stu-id="db77c-118">Elements of the mobile app</span></span>
<span data-ttu-id="db77c-119">Mobiilisovelluksen käyttö koostuu neljästä, perusosasta: koontinäyttö, työtilat, sivut ja toiminnot.</span><span class="sxs-lookup"><span data-stu-id="db77c-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="db77c-120">[![Mobiilisovelluksen siirtymiskonseptit](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="db77c-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="db77c-121">**Koontinäyttö** aukea, kun sovellus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="db77c-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="db77c-122">Koontinäytössä on luettelo julkaistuista **työtiloista**.</span><span class="sxs-lookup"><span data-stu-id="db77c-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="db77c-123">Kussakin työtilassa näet luettelon **sivuista**, jotka ovat saatavilla kyseisessä työtilassa.</span><span class="sxs-lookup"><span data-stu-id="db77c-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="db77c-124">Kun olet sivulla, voit suorittaa siellä useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="db77c-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="db77c-125">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="db77c-125">Here are some examples:</span></span>

    - <span data-ttu-id="db77c-126">Yksityiskohtaisten tietojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="db77c-126">View detailed data.</span></span>
    - <span data-ttu-id="db77c-127">Siirtyminen muille sivuille, joilla on liittyviä tietoja, kuten yksikön tietoja tai rivejä.</span><span class="sxs-lookup"><span data-stu-id="db77c-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="db77c-128">Tutustu luetteloon **toiminnoista**, jotka ovat käytettävissä kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="db77c-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="db77c-129">Toimintojen avulla voit luoda tai muokata tietoja.</span><span class="sxs-lookup"><span data-stu-id="db77c-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="db77c-130">Käyttöönottoprosessi</span><span class="sxs-lookup"><span data-stu-id="db77c-130">Implementation process</span></span>
<span data-ttu-id="db77c-131">Seuraavassa kuvassa on esitys Microsoftin toimittamien mobiilityötilojen ja mukautettujen mobiilityötilojen käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="db77c-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Mobiilisovellusten käyttöönottoprosessi](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="db77c-133">Seuraavassa taulukossa on linkkejä resursseihin, jotka auttavat ottamaan käyttöön sekä Microsoftin tarjoamia mobiilityötiloja että mukautettuja mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="db77c-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="db77c-134">Ensimmäisen sarakkeen numerot vastaavat edellisessä kuvassa esitettyjä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="db77c-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="db77c-135">Vaihe</span><span class="sxs-lookup"><span data-stu-id="db77c-135">Step</span></span></th>
<th><span data-ttu-id="db77c-136">Rooli</span><span class="sxs-lookup"><span data-stu-id="db77c-136">Role</span></span></th>
<th><span data-ttu-id="db77c-137">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="db77c-137">Action</span></span></th>
<th><span data-ttu-id="db77c-138">Resursseja, jotka auttavat suorittamaan toiminnon</span><span class="sxs-lookup"><span data-stu-id="db77c-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="db77c-139">1</span><span class="sxs-lookup"><span data-stu-id="db77c-139">1</span></span></td>
<td><span data-ttu-id="db77c-140">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db77c-140">System administrator</span></span></td>
<td><span data-ttu-id="db77c-141">Ota Finance and Operations käyttöön organisaatiossasi</span><span class="sxs-lookup"><span data-stu-id="db77c-141">Implement Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="db77c-142">Jos et ole vielä ottanut Microsoft Dynamics 365 -versiota käyttöön, lisätietoja on kohdassa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="db77c-142">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="db77c-143">Jos haluat tutustua käytettävissä oleviin mobiilityötilaluetteloihin, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="db77c-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db77c-144">2</span><span class="sxs-lookup"><span data-stu-id="db77c-144">2</span></span></td>
<td><span data-ttu-id="db77c-145">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db77c-145">System administrator</span></span></td>
<td><span data-ttu-id="db77c-146"><strong>Jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611:</strong> Lataa ja asenna KB:t, joilla otetaan Microsoftin mobiilityötilat käyttöön.</span><span class="sxs-lookup"><span data-stu-id="db77c-146"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="db77c-147">Lisätietoja on seuraavissa ohjeaiheissa:</span><span class="sxs-lookup"><span data-stu-id="db77c-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="db77c-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Kustannusseurannan mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="db77c-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="db77c-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Käytettävissä olevan varaston mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="db77c-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="db77c-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Myyntitilausten mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="db77c-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="db77c-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Toimittajayhteistyön mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="db77c-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="db77c-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projektin aikamerkintöjen mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="db77c-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="db77c-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Kulujen hallinnan mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="db77c-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db77c-154">3</span><span class="sxs-lookup"><span data-stu-id="db77c-154">3</span></span></td>
<td><span data-ttu-id="db77c-155">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db77c-155">System administrator</span></span></td>
<td><span data-ttu-id="db77c-156">Julkaise Microsoftin tarjoamat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="db77c-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="db77c-157"><a href="publish-mobile-workspace.md">Julkaise mobiilityötila</a>
</span><span class="sxs-lookup"><span data-stu-id="db77c-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db77c-158">4</span><span class="sxs-lookup"><span data-stu-id="db77c-158">4</span></span></td>
<td><span data-ttu-id="db77c-159">Kehittäjä tai riippumaton ohjelmistotoimittaja (ISV)</span><span class="sxs-lookup"><span data-stu-id="db77c-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="db77c-160">Luo mukautettuja mobiilityötiloja mobiiliympäristön avulla.</span><span class="sxs-lookup"><span data-stu-id="db77c-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="db77c-161"><a href="platform/mobile-platform-home-page.md">Mobiiliympäristö</a></span><span class="sxs-lookup"><span data-stu-id="db77c-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db77c-162">5</span><span class="sxs-lookup"><span data-stu-id="db77c-162">5</span></span></td>
<td><span data-ttu-id="db77c-163">riippumaton ohjelmistotoimittaja</span><span class="sxs-lookup"><span data-stu-id="db77c-163">ISV</span></span></td>
<td><span data-ttu-id="db77c-164">Luo käyttöön otettava paketti, joka sisältää mukautettuja mobiilityötiloja ja lataa paketti Microsoft Dynamics Lifecycle Services (LCS) -palveluun.</span><span class="sxs-lookup"><span data-stu-id="db77c-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="db77c-165"><a href="../deployment/create-apply-deployable-package.md">Käyttöön otettavan paketin luominen</a></span><span class="sxs-lookup"><span data-stu-id="db77c-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db77c-166">6</span><span class="sxs-lookup"><span data-stu-id="db77c-166">6</span></span></td>
<td><span data-ttu-id="db77c-167">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db77c-167">System administrator</span></span></td>
<td><span data-ttu-id="db77c-168">Avaa riippumattoman ohjelmistotoimittajan tarjoamat mukautetut työtilat sisältävä paketti.</span><span class="sxs-lookup"><span data-stu-id="db77c-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="db77c-169"><a href="../deployment/apply-deployable-package-system.md">Käyttöönotettavan paketin käyttäminen</a></span><span class="sxs-lookup"><span data-stu-id="db77c-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db77c-170">7</span><span class="sxs-lookup"><span data-stu-id="db77c-170">7</span></span></td>
<td><span data-ttu-id="db77c-171">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="db77c-171">System administrator</span></span></td>
<td><span data-ttu-id="db77c-172">Julkaise ohjelmistotoimittajan tarjoamat, mukautetut mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="db77c-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="db77c-173"><a href="publish-mobile-workspace.md">Mobiilityötilan julkaisu</a></span><span class="sxs-lookup"><span data-stu-id="db77c-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="db77c-174">8</span><span class="sxs-lookup"><span data-stu-id="db77c-174">8</span></span></td>
<td><span data-ttu-id="db77c-175">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="db77c-175">User</span></span></td>
<td><span data-ttu-id="db77c-176">Lataa ja asenna mobiilisovellus.</span><span class="sxs-lookup"><span data-stu-id="db77c-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="db77c-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android-puhelimet</a></span><span class="sxs-lookup"><span data-stu-id="db77c-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="db77c-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">IPhone-puhelimet</a></span><span class="sxs-lookup"><span data-stu-id="db77c-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="db77c-179">9</span><span class="sxs-lookup"><span data-stu-id="db77c-179">9</span></span></td>
<td><span data-ttu-id="db77c-180">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="db77c-180">User</span></span></td>
<td><span data-ttu-id="db77c-181">Kirjaudu mobiilisovellukseen ja käytä sitä.</span><span class="sxs-lookup"><span data-stu-id="db77c-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="db77c-182">Sovellus sisältää järjestelmänvalvojan julkaisemat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="db77c-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="db77c-183">Jos haluat tutustua Microsoftin toimittamaan mobiilityötilaluetteloon, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="db77c-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

