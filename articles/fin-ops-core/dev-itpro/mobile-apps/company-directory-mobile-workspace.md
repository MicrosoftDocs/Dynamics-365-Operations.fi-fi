---
title: Yrityksen hakemiston mobiilityötila
description: Tässä ohjeaiheessa on tietoja yrityshakemiston mobiilityötilasta, jossa käyttäjät voivat tarkastella organisaation muita työntekijöitä ja ottaa heihin yhteyttä.
author: jcart1106
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3193fbc4d4b3492960c7c13dc24b41bb920e7d23
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683428"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="23bf5-103">Yrityksen hakemiston mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="23bf5-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23bf5-104">Tässä ohjeaiheessa on tietoja **Yrityksen hakemisto** -mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="23bf5-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="23bf5-105">Käyttäjät voivat tarkastella tässä työtilassa organisaation muita työntekijöitä ja ottaa heihin yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="23bf5-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="23bf5-106">Tätä mobiilityötilaa voi käyttää Finance and Operations -mobiilisovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="23bf5-106">This mobile workspace can be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="23bf5-107">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="23bf5-107">Overview</span></span>
<span data-ttu-id="23bf5-108">Käyttäjät voivat tehdä seuraavia tehtäviä **Yrityksen hakemisto** -mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="23bf5-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="23bf5-109">tarkastella organisaation työntekijäluetteloa</span><span class="sxs-lookup"><span data-stu-id="23bf5-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="23bf5-110">hakea organisaation työntekijöitä</span><span class="sxs-lookup"><span data-stu-id="23bf5-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="23bf5-111">tarkastella työntekijöiden yhteystietoja</span><span class="sxs-lookup"><span data-stu-id="23bf5-111">View contact information for employees.</span></span>
- <span data-ttu-id="23bf5-112">ottaa yhteyttä työntekijöihin profiilitiedoista.</span><span class="sxs-lookup"><span data-stu-id="23bf5-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="23bf5-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="23bf5-113">Prerequisites</span></span>
<span data-ttu-id="23bf5-114">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="23bf5-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="23bf5-115">Edellytys</span><span class="sxs-lookup"><span data-stu-id="23bf5-115">Prerequisite</span></span></th>
<th><span data-ttu-id="23bf5-116">Rooli</span><span class="sxs-lookup"><span data-stu-id="23bf5-116">Role</span></span></th>
<th><span data-ttu-id="23bf5-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="23bf5-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="23bf5-118">Organisaatiossa on oltava käytössä jokin seuraavista tuotteista:</span><span class="sxs-lookup"><span data-stu-id="23bf5-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="23bf5-119">Finance and Operations -sovellus</span><span class="sxs-lookup"><span data-stu-id="23bf5-119">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="23bf5-120">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="23bf5-120">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="23bf5-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="23bf5-121">System administrator</span></span></td>
<td><span data-ttu-id="23bf5-122">Jos Finance and Operations -sovellusta ei ole vielä otettu&#39; organisaatiossa käyttöön, lisätietoja on kohdassa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="23bf5-122">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="23bf5-123">Jos Human Resourcesia ei ole vielä otettu&#39; organisaatiossa käyttöön, järjestelmänvalvoja voi hakea kokeiluversion <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources -sivulta</a>.</span><span class="sxs-lookup"><span data-stu-id="23bf5-123">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="23bf5-124"><strong>Yrityksen hakemisto</strong> -mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="23bf5-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="23bf5-125">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="23bf5-125">System administrator</span></span></td>
<td><span data-ttu-id="23bf5-126">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="23bf5-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="23bf5-127">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="23bf5-127">Download and install the mobile app</span></span>
<span data-ttu-id="23bf5-128">Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:</span><span class="sxs-lookup"><span data-stu-id="23bf5-128">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="23bf5-129">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="23bf5-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="23bf5-130">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="23bf5-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="23bf5-131">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="23bf5-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="23bf5-132">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="23bf5-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="23bf5-133">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="23bf5-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="23bf5-134">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="23bf5-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="23bf5-135">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="23bf5-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="23bf5-136">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="23bf5-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="23bf5-137">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="23bf5-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="23bf5-138">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="23bf5-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="23bf5-139">Yrityksen hakemiston tarkastelu mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="23bf5-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="23bf5-140">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="23bf5-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="23bf5-141">Näkyvissä on työntekijäluettelo.</span><span class="sxs-lookup"><span data-stu-id="23bf5-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="23bf5-142">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="23bf5-142">Select an employee.</span></span> <span data-ttu-id="23bf5-143">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="23bf5-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="23bf5-144">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="23bf5-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="23bf5-145">Haku yrityksen hakemistossa mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="23bf5-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="23bf5-146">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="23bf5-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="23bf5-147">Aloita haku kirjoittamalla **Haku**-kenttään työntekijän etunimi, sukunimi, nimike tai osasto.</span><span class="sxs-lookup"><span data-stu-id="23bf5-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="23bf5-148">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="23bf5-148">Select an employee.</span></span> <span data-ttu-id="23bf5-149">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="23bf5-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="23bf5-150">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="23bf5-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
