---
title: Yrityksen hakemiston mobiilityötila
description: Tässä ohjeaiheessa on tietoja yrityshakemiston mobiilityötilasta, jossa käyttäjät voivat tarkastella organisaation muita työntekijöitä ja ottaa heihin yhteyttä.
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 37b338d5971395264bd2ff673ee7892814859846
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741156"
---
# <a name="company-directory-mobile-workspace"></a><span data-ttu-id="68046-103">Yrityksen hakemiston mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="68046-103">Company directory mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68046-104">Tässä ohjeaiheessa on tietoja **Yrityksen hakemisto** -mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="68046-104">This topic provides information about the **Company directory** mobile workspace.</span></span> <span data-ttu-id="68046-105">Käyttäjät voivat tarkastella tässä työtilassa organisaation muita työntekijöitä ja ottaa heihin yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="68046-105">This workspace lets users view and contact other employees in their organization.</span></span>

<span data-ttu-id="68046-106">Tätä mobiilityötilaa voi käyttää Microsoft Dynamics 365 for Unified Operations Mobile -sovelluksella.</span><span class="sxs-lookup"><span data-stu-id="68046-106">This mobile workspace can be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="68046-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="68046-107">Overview</span></span>
<span data-ttu-id="68046-108">Käyttäjät voivat tehdä seuraavia tehtäviä **Yrityksen hakemisto** -mobiilityötilassa:</span><span class="sxs-lookup"><span data-stu-id="68046-108">The **Company directory** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="68046-109">tarkastella organisaation työntekijäluetteloa</span><span class="sxs-lookup"><span data-stu-id="68046-109">View a list of employees in the organization.</span></span>
- <span data-ttu-id="68046-110">hakea organisaation työntekijöitä</span><span class="sxs-lookup"><span data-stu-id="68046-110">Search for employees in the organization.</span></span>
- <span data-ttu-id="68046-111">tarkastella työntekijöiden yhteystietoja</span><span class="sxs-lookup"><span data-stu-id="68046-111">View contact information for employees.</span></span>
- <span data-ttu-id="68046-112">ottaa yhteyttä työntekijöihin profiilitiedoista.</span><span class="sxs-lookup"><span data-stu-id="68046-112">Contact employees from the profile information.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="68046-113">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="68046-113">Prerequisites</span></span>
<span data-ttu-id="68046-114">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="68046-114">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="68046-115">Edellytys</span><span class="sxs-lookup"><span data-stu-id="68046-115">Prerequisite</span></span></th>
<th><span data-ttu-id="68046-116">Rooli</span><span class="sxs-lookup"><span data-stu-id="68046-116">Role</span></span></th>
<th><span data-ttu-id="68046-117">kuvaus</span><span class="sxs-lookup"><span data-stu-id="68046-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68046-118">Organisaatiossa on oltava käytössä jokin seuraavista tuotteista:</span><span class="sxs-lookup"><span data-stu-id="68046-118">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="68046-119">Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68046-119">Microsoft Dynamics 365 for Finance and Operations</span></span></li>
<li><span data-ttu-id="68046-120">Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="68046-120">Microsoft Dynamics 365 for Talent</span></span></li>
</ul>
</td>
<td><span data-ttu-id="68046-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="68046-121">System administrator</span></span></td>
<td><span data-ttu-id="68046-122">Jos Finance and Operationsia ei ole vielä otettu organisaatiossa käyttöön, lisätietoja on kohdassa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön ottaminen käyttöön</a>.</span><span class="sxs-lookup"><span data-stu-id="68046-122">If you don&#39;t already have Finance and Operations deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="68046-123">Jos Talentia ei ole vielä otettu organisaatiossa käyttöön, järjestelmänvalvoja voi hakea kokeiluversion <a href="https://www.microsoft.com/dynamics365/talent">Talent-sivulta</a>.</span><span class="sxs-lookup"><span data-stu-id="68046-123">If you don&#39;t already have Talent deployed in your organization, the system administrator can access a trial version from the <a href="https://www.microsoft.com/dynamics365/talent">Talent webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="68046-124"><strong>Yrityksen hakemisto</strong> -mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="68046-124">The <strong>Company directory</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="68046-125">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="68046-125">System administrator</span></span></td>
<td><span data-ttu-id="68046-126">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="68046-126">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="68046-127">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="68046-127">Download and install the mobile app</span></span>
<span data-ttu-id="68046-128">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="68046-128">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="68046-129">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="68046-129">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="68046-130">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="68046-130">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="68046-131">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="68046-131">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="68046-132">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="68046-132">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="68046-133">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="68046-133">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="68046-134">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="68046-134">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="68046-135">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="68046-135">Enter your credentials.</span></span>
4.  <span data-ttu-id="68046-136">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="68046-136">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="68046-137">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="68046-137">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="68046-138">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="68046-138">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="68046-139">Yrityksen hakemiston tarkastelu mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="68046-139">View the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="68046-140">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="68046-140">In the mobile app, select the **Company directory** workspace.</span></span> <span data-ttu-id="68046-141">Näkyvissä on työntekijäluettelo.</span><span class="sxs-lookup"><span data-stu-id="68046-141">A list of employees is shown.</span></span>
3.  <span data-ttu-id="68046-142">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="68046-142">Select an employee.</span></span> <span data-ttu-id="68046-143">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="68046-143">The **Employee profile** page appears.</span></span> <span data-ttu-id="68046-144">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="68046-144">The information on this page includes the employee's first name, last name, title, and department.</span></span>

## <a name="search-the-company-directory-by-using-the-mobile-workspace"></a><span data-ttu-id="68046-145">Haku yrityksen hakemistossa mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="68046-145">Search the company directory by using the mobile workspace</span></span>
1.  <span data-ttu-id="68046-146">Valitse mobiilisovelluksessa **Yrityksen hakemisto** -työtila.</span><span class="sxs-lookup"><span data-stu-id="68046-146">In the mobile app, select the **Company directory** workspace.</span></span>
2.  <span data-ttu-id="68046-147">Aloita haku kirjoittamalla **Haku**-kenttään työntekijän etunimi, sukunimi, nimike tai osasto.</span><span class="sxs-lookup"><span data-stu-id="68046-147">In the **Search** field, enter an employee's first name, last name, title, or department to start the search.</span></span>
3.  <span data-ttu-id="68046-148">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="68046-148">Select an employee.</span></span> <span data-ttu-id="68046-149">**Työntekijän profiili** -sivu avautuu.</span><span class="sxs-lookup"><span data-stu-id="68046-149">The **Employee profile** page appears.</span></span> <span data-ttu-id="68046-150">Tällä sivulla on näkyvissä muun muassa työntekijän etunimi, sukunimi, nimike ja osasto.</span><span class="sxs-lookup"><span data-stu-id="68046-150">The information on this page includes the employee's first name, last name, title, and department.</span></span>
