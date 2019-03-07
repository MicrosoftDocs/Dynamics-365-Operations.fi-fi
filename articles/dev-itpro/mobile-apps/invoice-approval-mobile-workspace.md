---
title: Laskujen hyväksyntöjen mobiilityötila
description: Tässä ohjeaiheessa on tietoja laskujen hyväksyntöjen mobiilityötilasta. Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff726670e0fd7566a74e6def73555a7c53b86f97
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "326995"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="aa435-104">Laskujen hyväksyntöjen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="aa435-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa435-105">Tässä ohjeaiheessa on tietoja **laskujen hyväksyntöjen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="aa435-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="aa435-106">Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="aa435-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="aa435-107">Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations Mobile -sovelluksella.</span><span class="sxs-lookup"><span data-stu-id="aa435-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="aa435-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="aa435-108">Overview</span></span>

<span data-ttu-id="aa435-109">**Laskun hyväksyntöjen** mobiilityötilan avulla ostoreskontran käsittelijät ja esimiehet voivat tarkastella laskuja, jotka on määritetty heille toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="aa435-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="aa435-110">Voit tarkastella laskun tietoja sekä rivi- ja jakelutietoja, mikä parantaa hyväksyntäpäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="aa435-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="aa435-111">Voit valita työtilassa toiminnon, jolla lasku siirtyy työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="aa435-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="aa435-112">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="aa435-112">Prerequisites</span></span>

<span data-ttu-id="aa435-113">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="aa435-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="aa435-114">Edellytys</span><span class="sxs-lookup"><span data-stu-id="aa435-114">Prerequisite</span></span></th>
<th><span data-ttu-id="aa435-115">Rooli</span><span class="sxs-lookup"><span data-stu-id="aa435-115">Role</span></span></th>
<th><span data-ttu-id="aa435-116">kuvaus</span><span class="sxs-lookup"><span data-stu-id="aa435-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa435-117">Microsoft Dynamics 365 for Finance and Operations on otettava käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="aa435-117">Microsoft Dynamics 365 for Finance and Operations must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="aa435-118">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="aa435-118">System administrator</span></span></td>
<td><span data-ttu-id="aa435-119">Katso <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="aa435-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa435-120"><strong>Laskun hyväksyntöjen</strong> mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="aa435-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="aa435-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="aa435-121">System administrator</span></span></td>
<td><span data-ttu-id="aa435-122">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="aa435-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="aa435-123">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="aa435-123">Download and install the mobile app</span></span>

<span data-ttu-id="aa435-124">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="aa435-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="aa435-125">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="aa435-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="aa435-126">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="aa435-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="aa435-127">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="aa435-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="aa435-128">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aa435-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="aa435-129">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="aa435-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="aa435-130">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="aa435-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="aa435-131">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="aa435-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="aa435-132">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="aa435-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="aa435-133">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="aa435-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="aa435-134">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="aa435-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="aa435-135">Laskun hyväksyminen laskun hyväksyntöjen mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="aa435-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="aa435-136">Valitse mobiililaitteessasi **laskun hyväksyntöjen** työtila.</span><span class="sxs-lookup"><span data-stu-id="aa435-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="aa435-137">Valitse toimittajan laskun otsikon työnkulussa sinulle määritetty lasku.</span><span class="sxs-lookup"><span data-stu-id="aa435-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="aa435-138">Tarkista **Laskun tiedot** -sivulla laskun otsikon tiedot, kuten toimittaja ja päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="aa435-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="aa435-139">Valitse laskurivi ja tarkastele sen yksityiskohtaisia tietoja **Laskurivin tiedot** -tietoja.</span><span class="sxs-lookup"><span data-stu-id="aa435-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="aa435-140">Näytä rivijakelut valitsemalla **Laskurivin tiedot** -näkymässä **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="aa435-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="aa435-141">Voit tarkastella täällä laskurivin kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="aa435-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="aa435-142">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätili.</span><span class="sxs-lookup"><span data-stu-id="aa435-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="aa435-143">Näytä kaikki jakelut valitsemalla **Laskun tiedot** -sivulla **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="aa435-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="aa435-144">Voit tarkastella täällä koko lasku kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="aa435-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="aa435-145">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätilit.</span><span class="sxs-lookup"><span data-stu-id="aa435-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="aa435-146">Voit tarkastella laskuun liitettyjä huomautuksia tai tiedostoja valitsemalla **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="aa435-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="aa435-147">Viimeistele tarkasteluprosessi valitsemalla **Laskun tiedot** -sivulla soveltuva työkulkutoiminto.</span><span class="sxs-lookup"><span data-stu-id="aa435-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="aa435-148">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aa435-148">Select **Done**.</span></span>
