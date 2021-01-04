---
title: Mobiilisovelluksen aloitussivu
description: Tässä ohjeaiheessa käsitellään Finance and Operations (Dynamics 365) -mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.
author: ChrisGarty
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: e4a9d6424e2d214624c148c0565c88ea4cf4ccf9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683455"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="e3487-103">Mobiilisovelluksen aloitussivu</span><span class="sxs-lookup"><span data-stu-id="e3487-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3487-104">Tässä ohjeaiheessa käsitellään **Finance and Operations (Dynamics 365)** -mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="e3487-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="e3487-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e3487-105">Overview</span></span>
--------

<span data-ttu-id="e3487-106">Mobiilisovelluksen avulla organisaatiosi liiketoimintaprosesseja voi käyttää mobiililaitteilla.</span><span class="sxs-lookup"><span data-stu-id="e3487-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="e3487-107">Kun IT-järjestelmänvalvoja ottaa mobiilityötilat käyttöön organisaatiossa, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan.</span><span class="sxs-lookup"><span data-stu-id="e3487-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="e3487-108">Mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="e3487-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="e3487-109">Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="e3487-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="e3487-110">Kun laitteen verkkoyhteys on jälleen käytössä, offline-tilassa tehdyt toimet synkronoidaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="e3487-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="e3487-111">IT-järjestelmänvalvojat tai sovelluskehittäjät voivat julkaista organisaatiolleen räätälöityjä mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="e3487-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="e3487-112">Sovellus käyttää olemassa olevia koodiresursseja.</span><span class="sxs-lookup"><span data-stu-id="e3487-112">The app uses your existing code assets.</span></span> <span data-ttu-id="e3487-113">Sinun ei siis täydy luoda tarkistusmenettelyitä, liiketoimintalogiikkaa tai suojausmäärittelyitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e3487-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="e3487-114">IT-järjestelmänvalvoja tai sovelluskehittäjät voivat suunnitella mobiilityötiloja helposti verkkoasiakasohjelman työtilojen helppokäyttöisellä suunnitteluohjelmalla.</span><span class="sxs-lookup"><span data-stu-id="e3487-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="e3487-115">IT-järjestelmävalvojat voivat halutessaan optimoida työtilojen offline-ominaisuuksia liiketoimintalogiikan laajennuskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="e3487-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="e3487-116">Koska tietojen käsittely ei keskeydy laitteen ollessa offline-tilassa, mobiiliskenaariosi säilyvät mukautuvina, vaikka laitteilla ei olisikaan jatkuvaa verkkoyhteyttä.</span><span class="sxs-lookup"><span data-stu-id="e3487-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="e3487-117">Mobiilisovelluksen osat</span><span class="sxs-lookup"><span data-stu-id="e3487-117">Elements of the mobile app</span></span>
<span data-ttu-id="e3487-118">Mobiilisovelluksen käyttö koostuu neljästä, perusosasta: koontinäyttö, työtilat, sivut ja toiminnot.</span><span class="sxs-lookup"><span data-stu-id="e3487-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="e3487-119">[![Mobiilisovelluksen siirtymiskonseptit](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="e3487-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="e3487-120">**Koontinäyttö** aukea, kun sovellus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="e3487-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="e3487-121">Koontinäytössä on luettelo julkaistuista **työtiloista**.</span><span class="sxs-lookup"><span data-stu-id="e3487-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="e3487-122">Kussakin työtilassa näet luettelon **sivuista**, jotka ovat saatavilla kyseisessä työtilassa.</span><span class="sxs-lookup"><span data-stu-id="e3487-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="e3487-123">Kun olet sivulla, voit suorittaa siellä useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e3487-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="e3487-124">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="e3487-124">Here are some examples:</span></span>

    - <span data-ttu-id="e3487-125">Yksityiskohtaisten tietojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="e3487-125">View detailed data.</span></span>
    - <span data-ttu-id="e3487-126">Siirtyminen muille sivuille, joilla on liittyviä tietoja, kuten yksikön tietoja tai rivejä.</span><span class="sxs-lookup"><span data-stu-id="e3487-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="e3487-127">Tutustu luetteloon **toiminnoista**, jotka ovat käytettävissä kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="e3487-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="e3487-128">Toimintojen avulla voit luoda tai muokata tietoja.</span><span class="sxs-lookup"><span data-stu-id="e3487-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="e3487-129">Käyttöönottoprosessi</span><span class="sxs-lookup"><span data-stu-id="e3487-129">Implementation process</span></span>
<span data-ttu-id="e3487-130">Seuraavassa kuvassa on esitys Microsoftin toimittamien mobiilityötilojen ja mukautettujen mobiilityötilojen käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="e3487-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="e3487-131">[![Mobiilisovellusten käyttöönottoprosessi](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="e3487-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="e3487-132">Seuraavassa taulukossa on linkkejä resursseihin, jotka auttavat ottamaan käyttöön sekä Microsoftin tarjoamia mobiilityötiloja että mukautettuja mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="e3487-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="e3487-133">Ensimmäisen sarakkeen numerot vastaavat edellisessä kuvassa esitettyjä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e3487-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3487-134">Vaihe</span><span class="sxs-lookup"><span data-stu-id="e3487-134">Step</span></span></th>
<th><span data-ttu-id="e3487-135">Rooli</span><span class="sxs-lookup"><span data-stu-id="e3487-135">Role</span></span></th>
<th><span data-ttu-id="e3487-136">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="e3487-136">Action</span></span></th>
<th><span data-ttu-id="e3487-137">Resursseja, jotka auttavat suorittamaan toiminnon</span><span class="sxs-lookup"><span data-stu-id="e3487-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3487-138">1</span><span class="sxs-lookup"><span data-stu-id="e3487-138">1</span></span></td>
<td><span data-ttu-id="e3487-139">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e3487-139">System administrator</span></span></td>
<td><span data-ttu-id="e3487-140">Ota Finance and Operations -sovellus käyttöön organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="e3487-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="e3487-141">Jos et ole vielä ottanut&#39; Microsoft Dynamics 365 -versiota käyttöön, lisätietoja on kohdassa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="e3487-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="e3487-142">Jos haluat tutustua käytettävissä oleviin mobiilityötilaluetteloihin, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="e3487-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3487-143">2</span><span class="sxs-lookup"><span data-stu-id="e3487-143">2</span></span></td>
<td><span data-ttu-id="e3487-144">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e3487-144">System administrator</span></span></td>
<td><span data-ttu-id="e3487-145"><strong>Jos käytössä&#39; on Microsoft Dynamics 365 for Operationsin versio 1611:</strong> Lataa ja asenna paketit, jotka mahdollistavat Microsoftin tarjoamien mobiilityötilojen käytön.</span><span class="sxs-lookup"><span data-stu-id="e3487-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e3487-146">Lisätietoja on seuraavissa ohjeaiheissa:</span><span class="sxs-lookup"><span data-stu-id="e3487-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="e3487-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Kustannusseurannan mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="e3487-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e3487-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Käytettävissä olevan varaston mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="e3487-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="e3487-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Myyntitilausten mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="e3487-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e3487-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Toimittajayhteistyön mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="e3487-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="e3487-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Projektin aikamerkintöjen mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="e3487-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="e3487-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Kulujen hallinnan mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="e3487-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3487-153">3</span><span class="sxs-lookup"><span data-stu-id="e3487-153">3</span></span></td>
<td><span data-ttu-id="e3487-154">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e3487-154">System administrator</span></span></td>
<td><span data-ttu-id="e3487-155">Julkaise Microsoftin tarjoamat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="e3487-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e3487-156"><a href="publish-mobile-workspace.md">Julkaise mobiilityötila</a>
</span><span class="sxs-lookup"><span data-stu-id="e3487-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3487-157">4</span><span class="sxs-lookup"><span data-stu-id="e3487-157">4</span></span></td>
<td><span data-ttu-id="e3487-158">Kehittäjä tai riippumaton ohjelmistotoimittaja (ISV)</span><span class="sxs-lookup"><span data-stu-id="e3487-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="e3487-159">Luo mukautettuja mobiilityötiloja mobiiliympäristön avulla.</span><span class="sxs-lookup"><span data-stu-id="e3487-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="e3487-160"><a href="platform/mobile-platform-home-page.md">Mobiiliympäristö</a></span><span class="sxs-lookup"><span data-stu-id="e3487-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3487-161">5</span><span class="sxs-lookup"><span data-stu-id="e3487-161">5</span></span></td>
<td><span data-ttu-id="e3487-162">riippumaton ohjelmistotoimittaja</span><span class="sxs-lookup"><span data-stu-id="e3487-162">ISV</span></span></td>
<td><span data-ttu-id="e3487-163">Luo käyttöön otettava paketti, joka sisältää mukautettuja mobiilityötiloja ja lataa paketti Microsoft Dynamics Lifecycle Services (LCS) -palveluun.</span><span class="sxs-lookup"><span data-stu-id="e3487-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="e3487-164"><a href="../deployment/create-apply-deployable-package.md">Käyttöönotettavan paketin luominen</a></span><span class="sxs-lookup"><span data-stu-id="e3487-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3487-165">6</span><span class="sxs-lookup"><span data-stu-id="e3487-165">6</span></span></td>
<td><span data-ttu-id="e3487-166">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e3487-166">System administrator</span></span></td>
<td><span data-ttu-id="e3487-167">Avaa riippumattoman ohjelmistotoimittajan tarjoamat mukautetut työtilat sisältävä paketti.</span><span class="sxs-lookup"><span data-stu-id="e3487-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="e3487-168"><a href="../deployment/apply-deployable-package-system.md">Käyttöönotettavan paketin käyttäminen</a></span><span class="sxs-lookup"><span data-stu-id="e3487-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3487-169">7</span><span class="sxs-lookup"><span data-stu-id="e3487-169">7</span></span></td>
<td><span data-ttu-id="e3487-170">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="e3487-170">System administrator</span></span></td>
<td><span data-ttu-id="e3487-171">Julkaise ohjelmistotoimittajan tarjoamat, mukautetut mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="e3487-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="e3487-172"><a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a></span><span class="sxs-lookup"><span data-stu-id="e3487-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3487-173">8</span><span class="sxs-lookup"><span data-stu-id="e3487-173">8</span></span></td>
<td><span data-ttu-id="e3487-174">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="e3487-174">User</span></span></td>
<td><span data-ttu-id="e3487-175">Lataa ja asenna mobiilisovellus.</span><span class="sxs-lookup"><span data-stu-id="e3487-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="e3487-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations -sovellus Androidille</a></span><span class="sxs-lookup"><span data-stu-id="e3487-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="e3487-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations -sovellus iOSille</a></span><span class="sxs-lookup"><span data-stu-id="e3487-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="e3487-178">(Windows Phonea ei tueta)</span><span class="sxs-lookup"><span data-stu-id="e3487-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3487-179">9</span><span class="sxs-lookup"><span data-stu-id="e3487-179">9</span></span></td>
<td><span data-ttu-id="e3487-180">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="e3487-180">User</span></span></td>
<td><span data-ttu-id="e3487-181">Kirjaudu mobiilisovellukseen ja käytä sitä.</span><span class="sxs-lookup"><span data-stu-id="e3487-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="e3487-182">Sovellus sisältää järjestelmänvalvojan julkaisemat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="e3487-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="e3487-183">Jos haluat tutustua Microsoftin toimittamaan mobiilityötilaluetteloon, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="e3487-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="e3487-184">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e3487-184">Troubleshooting</span></span>
[<span data-ttu-id="e3487-185">Mobiiliympäristön resurssit</span><span class="sxs-lookup"><span data-stu-id="e3487-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)
