---
title: Mobiilisovelluksen kotisivu
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
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9ee81bbdd22fed4ef6ea97080fe1f6b3d82bcaf5
ms.openlocfilehash: 88e4737bd8abf7f7dbab54fa6fb18afa525177e9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/06/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="6a211-103">Mobiilisovelluksen kotisivu</span><span class="sxs-lookup"><span data-stu-id="6a211-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6a211-104">Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Unified Operationsin mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="6a211-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="6a211-105">Mobiilisovelluksen nimi oli aiemmin *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="6a211-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="6a211-106">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="6a211-106">Overview</span></span>
--------

<span data-ttu-id="6a211-107">Mobiilisovelluksen avulla organisaatiosi liiketoimintaprosesseja voi käyttää mobiililaitteilla.</span><span class="sxs-lookup"><span data-stu-id="6a211-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="6a211-108">Kun IT-järjestelmänvalvoja ottaa mobiilityötilat käyttöön organisaatiossa, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan.</span><span class="sxs-lookup"><span data-stu-id="6a211-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="6a211-109">Mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="6a211-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="6a211-110">Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa.</span><span class="sxs-lookup"><span data-stu-id="6a211-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="6a211-111">Kun laite muodostaa verkkoyhteyden uudelleen, offline-tietotoiminnot synkronoidaan automaattisesti Dynamics 365 for Finance and Operations, Enterprise Editionin tai Microsoft Dynamics 365 for Finance and Operationsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="6a211-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="6a211-112">IT-järjestelmänvalvojat tai sovelluskehittäjät voivat julkaista organisaatiolleen räätälöityjä mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="6a211-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="6a211-113">Sovellus käyttää olemassa olevia koodiresursseja.</span><span class="sxs-lookup"><span data-stu-id="6a211-113">The app uses your existing code assets.</span></span> <span data-ttu-id="6a211-114">Sinun ei siis täydy luoda tarkistusmenettelyitä, liiketoimintalogiikkaa tai suojausmäärittelyitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="6a211-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="6a211-115">IT-järjestelmänvalvoja tai sovelluskehittäjät voivat suunnitella mobiilityötiloja helposti verkkoasiakasohjelman työtilojen helppokäyttöisellä suunnitteluohjelmalla.</span><span class="sxs-lookup"><span data-stu-id="6a211-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="6a211-116">IT-järjestelmävalvojat voivat halutessaan optimoida työtilojen offline-ominaisuuksia liiketoimintalogiikan laajennuskehyksen avulla.</span><span class="sxs-lookup"><span data-stu-id="6a211-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="6a211-117">Koska tietojen käsittely ei keskeydy laitteen ollessa offline-tilassa, mobiiliskenaariosi säilyvät mukautuvina, vaikka laitteilla ei olisikaan jatkuvaa verkkoyhteyttä.</span><span class="sxs-lookup"><span data-stu-id="6a211-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="6a211-118">Mobiilisovelluksen osat</span><span class="sxs-lookup"><span data-stu-id="6a211-118">Elements of the mobile app</span></span>
<span data-ttu-id="6a211-119">Mobiilisovelluksen käyttö koostuu neljästä, perusosasta: koontinäyttö, työtilat, sivut ja toiminnot.</span><span class="sxs-lookup"><span data-stu-id="6a211-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="6a211-120">[![Mobiilisovelluksen siirtymiskonseptit](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="6a211-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="6a211-121">**Koontinäyttö** aukea, kun sovellus käynnistetään.</span><span class="sxs-lookup"><span data-stu-id="6a211-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="6a211-122">Koontinäytössä on luettelo julkaistuista **työtiloista**.</span><span class="sxs-lookup"><span data-stu-id="6a211-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="6a211-123">Kussakin työtilassa näet luettelon **sivuista**, jotka ovat saatavilla kyseisessä työtilassa.</span><span class="sxs-lookup"><span data-stu-id="6a211-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="6a211-124">Kun olet sivulla, voit suorittaa siellä useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="6a211-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="6a211-125">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="6a211-125">Here are some examples:</span></span>

    - <span data-ttu-id="6a211-126">Yksityiskohtaisten tietojen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="6a211-126">View detailed data.</span></span>
    - <span data-ttu-id="6a211-127">Siirtyminen muille sivuille, joilla on liittyviä tietoja, kuten yksikön tietoja tai rivejä.</span><span class="sxs-lookup"><span data-stu-id="6a211-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="6a211-128">Tutustu luetteloon **toiminnoista**, jotka ovat käytettävissä kyseiseltä sivulta.</span><span class="sxs-lookup"><span data-stu-id="6a211-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="6a211-129">Toimintojen avulla voit luoda tai muokata tietoja.</span><span class="sxs-lookup"><span data-stu-id="6a211-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="6a211-130">Käyttöönottoprosessi</span><span class="sxs-lookup"><span data-stu-id="6a211-130">Implementation process</span></span>
<span data-ttu-id="6a211-131">Seuraavassa kuvassa on esitys Microsoftin toimittamien mobiilityötilojen ja mukautettujen mobiilityötilojen käyttöönottamisesta.</span><span class="sxs-lookup"><span data-stu-id="6a211-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Mobiilisovellusten käyttöönottoprosessi](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="6a211-133">Seuraavassa taulukossa on linkkejä resursseihin, jotka auttavat ottamaan käyttöön sekä Microsoftin tarjoamia mobiilityötiloja että mukautettuja mobiilityötiloja.</span><span class="sxs-lookup"><span data-stu-id="6a211-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="6a211-134">Ensimmäisen sarakkeen numerot vastaavat edellisessä kuvassa esitettyjä vaiheita.</span><span class="sxs-lookup"><span data-stu-id="6a211-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6a211-135">Vaihe</span><span class="sxs-lookup"><span data-stu-id="6a211-135">Step</span></span></th>
<th><span data-ttu-id="6a211-136">Rooli</span><span class="sxs-lookup"><span data-stu-id="6a211-136">Role</span></span></th>
<th><span data-ttu-id="6a211-137">Toimenpide</span><span class="sxs-lookup"><span data-stu-id="6a211-137">Action</span></span></th>
<th><span data-ttu-id="6a211-138">Resursseja, jotka auttavat suorittamaan toiminnon</span><span class="sxs-lookup"><span data-stu-id="6a211-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a211-139">1</span><span class="sxs-lookup"><span data-stu-id="6a211-139">1</span></span></td>
<td><span data-ttu-id="6a211-140">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6a211-140">System administrator</span></span></td>
<td><span data-ttu-id="6a211-141">Ota Finance and Operations tai Finance and Operations käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="6a211-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="6a211-142">Jos et ole vielä ottanut Microsoft Dynamics 365 -versiosta, lisätietoja on ohjeaiheessa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="6a211-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="6a211-143">Jos haluat tutustua käytettävissä oleviin mobiilityötilaluetteloihin, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="6a211-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a211-144">2</span><span class="sxs-lookup"><span data-stu-id="6a211-144">2</span></span></td>
<td><span data-ttu-id="6a211-145">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6a211-145">System administrator</span></span></td>
<td><span data-ttu-id="6a211-146"><strong>Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 1611:</strong> Lataa ja asenna KB:t, joilla otetaan Microsoftin mobiilityötilat käyttöön.</span><span class="sxs-lookup"><span data-stu-id="6a211-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="6a211-147">Lisätietoja on seuraavissa ohjeaiheissa:</span><span class="sxs-lookup"><span data-stu-id="6a211-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="6a211-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Kustannusseurannan mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="6a211-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="6a211-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Käytettävissä olevan varaston mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="6a211-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="6a211-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Myyntitilausten mobiilityötilat</a></span><span class="sxs-lookup"><span data-stu-id="6a211-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="6a211-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Toimittajayhteistyön mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="6a211-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="6a211-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projektin aikamerkintöjen mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="6a211-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="6a211-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Kulujen hallinnan mobiilityötila</a></span><span class="sxs-lookup"><span data-stu-id="6a211-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a211-154">3</span><span class="sxs-lookup"><span data-stu-id="6a211-154">3</span></span></td>
<td><span data-ttu-id="6a211-155">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6a211-155">System administrator</span></span></td>
<td><span data-ttu-id="6a211-156">Julkaise Microsoftin tarjoamat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="6a211-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="6a211-157"><a href="publish-mobile-workspace.md">Julkaise mobiilityötila</a>
</span><span class="sxs-lookup"><span data-stu-id="6a211-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a211-158">4</span><span class="sxs-lookup"><span data-stu-id="6a211-158">4</span></span></td>
<td><span data-ttu-id="6a211-159">Kehittäjä tai riippumaton ohjelmistotoimittaja (ISV)</span><span class="sxs-lookup"><span data-stu-id="6a211-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="6a211-160">Luo mukautettuja mobiilityötiloja mobiiliympäristön avulla.</span><span class="sxs-lookup"><span data-stu-id="6a211-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="6a211-161"><a href="platform/mobile-platform-home-page.md">Mobiiliympäristö</a></span><span class="sxs-lookup"><span data-stu-id="6a211-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a211-162">5</span><span class="sxs-lookup"><span data-stu-id="6a211-162">5</span></span></td>
<td><span data-ttu-id="6a211-163">riippumaton ohjelmistotoimittaja</span><span class="sxs-lookup"><span data-stu-id="6a211-163">ISV</span></span></td>
<td><span data-ttu-id="6a211-164">Luo käyttöön otettava paketti, joka sisältää mukautettuja mobiilityötiloja ja lataa paketti Microsoft Dynamicsin elinkaaripalveluihin (LCS).</span><span class="sxs-lookup"><span data-stu-id="6a211-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="6a211-165"><a href="../deployment/create-apply-deployable-package.md">Käyttöön otettavan paketin luominen</a></span><span class="sxs-lookup"><span data-stu-id="6a211-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a211-166">6</span><span class="sxs-lookup"><span data-stu-id="6a211-166">6</span></span></td>
<td><span data-ttu-id="6a211-167">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6a211-167">System administrator</span></span></td>
<td><span data-ttu-id="6a211-168">Avaa riippumattoman ohjelmistotoimittajan tarjoamat mukautetut työtilat sisältävä paketti.</span><span class="sxs-lookup"><span data-stu-id="6a211-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="6a211-169"><a href="../deployment/apply-deployable-package-system.md">Käyttöönotettavan paketin käyttäminen</a></span><span class="sxs-lookup"><span data-stu-id="6a211-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a211-170">7</span><span class="sxs-lookup"><span data-stu-id="6a211-170">7</span></span></td>
<td><span data-ttu-id="6a211-171">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="6a211-171">System administrator</span></span></td>
<td><span data-ttu-id="6a211-172">Julkaise ohjelmistotoimittajan tarjoamat, mukautetut mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="6a211-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="6a211-173"><a href="publish-mobile-workspace.md">Mobiilityötilan julkaisu</a></span><span class="sxs-lookup"><span data-stu-id="6a211-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a211-174">8</span><span class="sxs-lookup"><span data-stu-id="6a211-174">8</span></span></td>
<td><span data-ttu-id="6a211-175">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6a211-175">User</span></span></td>
<td><span data-ttu-id="6a211-176">Lataa ja asenna mobiilisovellus.</span><span class="sxs-lookup"><span data-stu-id="6a211-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="6a211-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android-puhelimet</a></span><span class="sxs-lookup"><span data-stu-id="6a211-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="6a211-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">IPhone-puhelimet</a></span><span class="sxs-lookup"><span data-stu-id="6a211-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a211-179">9</span><span class="sxs-lookup"><span data-stu-id="6a211-179">9</span></span></td>
<td><span data-ttu-id="6a211-180">Käyttäjä</span><span class="sxs-lookup"><span data-stu-id="6a211-180">User</span></span></td>
<td><span data-ttu-id="6a211-181">Kirjaudu mobiilisovellukseen ja käytä sitä.</span><span class="sxs-lookup"><span data-stu-id="6a211-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="6a211-182">Sovellus sisältää järjestelmänvalvojan julkaisemat mobiilityötilat.</span><span class="sxs-lookup"><span data-stu-id="6a211-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="6a211-183">Jos haluat tutustua Microsoftin toimittamaan mobiilityötilaluetteloon, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</span><span class="sxs-lookup"><span data-stu-id="6a211-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

