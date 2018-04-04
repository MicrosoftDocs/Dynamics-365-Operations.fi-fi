---
title: "Yrityksen hakemiston mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja yrityksen hakemiston mobiilityötilasta, jossa käyttäjät voivat tarkastella organisaation muita työntekijöitä ja ottaa heihin yhteyttä."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 77dd52848819f11a0a03eb70eebbdacdad2d1852
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="48831-103">Yrityksen hakemiston mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="48831-103">Company directory mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="48831-104">Tässä ohjeaiheessa on tietoja **Yrityksen hakemisto** -mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="48831-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="48831-105">Käyttäjät voivat tarkastella tässä työtilassa organisaation muita työntekijöitä ja ottaa heihin yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="48831-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="48831-106">Tätä mobiilityötilaa voi käyttää Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.</span><span class="sxs-lookup"><span data-stu-id="48831-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="48831-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="48831-107">Overview</span></span>
<span data-ttu-id="48831-108">Käyttäjät voivat tehdä seuraavia tehtäviä **Yrityksen hakemisto** -mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="48831-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="48831-109">tarkastella organisaation työntekijäluetteloa</span><span class="sxs-lookup"><span data-stu-id="48831-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="48831-110">hakea organisaation työntekijöitä</span><span class="sxs-lookup"><span data-stu-id="48831-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="48831-111">tarkastella työntekijöiden yhteystietoja</span><span class="sxs-lookup"><span data-stu-id="48831-111">View contact information for employees.</span></span>
- <span data-ttu-id="48831-112">ottaa yhteyttä työntekijöihin profiilitiedoista.</span><span class="sxs-lookup"><span data-stu-id="48831-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="48831-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="48831-113">Prerequisites</span></span>
<span data-ttu-id="48831-114">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="48831-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="48831-115">Edellytys</span><span class="sxs-lookup"><span data-stu-id="48831-115">Prerequisite</span></span></th>
<th><span data-ttu-id="48831-116">Rooli</span><span class="sxs-lookup"><span data-stu-id="48831-116">Role</span></span></th>
<th><span data-ttu-id="48831-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="48831-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="48831-118">Organisaatiossa on oltava käytössä jokin seuraavista tuotteista:</span><span class="sxs-lookup"><span data-stu-id="48831-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="48831-119">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="48831-119">Microsoft Dynamics 365 for Finance and Operations</span></span></li>
<li><span data-ttu-id="48831-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="48831-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="48831-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="48831-121">System administrator</span></span></td>
<td><span data-ttu-id="48831-122">Jos Finance and Operationsia ei ole vielä otettu organisaatiossa käyttöön, lisätietoja on ohjeaiheessa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön ottaminen käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="48831-122">If you don't already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="48831-123">Jos Talentia ei ole vielä otettu organisaatiossa käyttöön, järjestelmänvalvoja voi hakea kokeiluversion <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent-sivustosta</a>.</span><span class="sxs-lookup"><span data-stu-id="48831-123">If you don't already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="48831-124"><strong>Yrityksen hakemisto</strong> -mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="48831-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="48831-125">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="48831-125">System administrator</span></span></td>
<td><span data-ttu-id="48831-126">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="48831-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="48831-127">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="48831-127">Download and install the mobile app</span></span>
<span data-ttu-id="48831-128">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="48831-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="48831-129">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="48831-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="48831-130">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="48831-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="48831-131">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="48831-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="48831-132">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="48831-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="48831-133">Anna oman Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="48831-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="48831-134">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="48831-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="48831-135">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="48831-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="48831-136">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="48831-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="48831-137">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="48831-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="48831-138">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="48831-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="48831-139">Yrityksen hakemiston tarkastelu mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="48831-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="48831-140">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="48831-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="48831-141">Näkyvissä on työntekijäluettelo.</span><span class="sxs-lookup"><span data-stu-id="48831-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="48831-142">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="48831-142">Select an employee.</span></span> <span data-ttu-id="48831-143">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="48831-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="48831-144">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="48831-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="48831-145">Haku yrityksen hakemistossa mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="48831-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="48831-146">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="48831-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="48831-147">Aloita haku kirjoittamalla **Haku**-kenttään työntekijän etunimi, sukunimi, nimike tai osasto.</span><span class="sxs-lookup"><span data-stu-id="48831-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="48831-148">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="48831-148">Select an employee.</span></span> <span data-ttu-id="48831-149">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="48831-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="48831-150">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="48831-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>

