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
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8d4b40c7ce8939248e85b6b6f3d359bd16e35b0d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683405"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="ba52e-104">Laskujen hyväksyntöjen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="ba52e-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba52e-105">Tässä ohjeaiheessa on tietoja **laskujen hyväksyntöjen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="ba52e-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="ba52e-106">Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="ba52e-107">Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="ba52e-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ba52e-108">Overview</span></span>

<span data-ttu-id="ba52e-109">**Laskun hyväksyntöjen** mobiilityötilan avulla ostoreskontran käsittelijät ja esimiehet voivat tarkastella laskuja, jotka on määritetty heille toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="ba52e-110">Voit tarkastella laskun tietoja sekä rivi- ja jakelutietoja, mikä parantaa hyväksyntäpäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="ba52e-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="ba52e-111">Voit valita työtilassa toiminnon, jolla lasku siirtyy työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ba52e-112">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="ba52e-112">Prerequisites</span></span>

<span data-ttu-id="ba52e-113">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ba52e-114">Edellytys</span><span class="sxs-lookup"><span data-stu-id="ba52e-114">Prerequisite</span></span></th>
<th><span data-ttu-id="ba52e-115">Rooli</span><span class="sxs-lookup"><span data-stu-id="ba52e-115">Role</span></span></th>
<th><span data-ttu-id="ba52e-116">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="ba52e-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba52e-117">Microsoft Dynamics 365 Finance on otettava käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-117">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="ba52e-118">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ba52e-118">System administrator</span></span></td>
<td><span data-ttu-id="ba52e-119">Katso <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="ba52e-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba52e-120"><strong>Laskun hyväksyntöjen</strong> mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="ba52e-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="ba52e-121">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="ba52e-121">System administrator</span></span></td>
<td><span data-ttu-id="ba52e-122">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="ba52e-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="ba52e-123">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="ba52e-123">Download and install the mobile app</span></span>

<span data-ttu-id="ba52e-124">Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:</span><span class="sxs-lookup"><span data-stu-id="ba52e-124">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="ba52e-125">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="ba52e-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="ba52e-126">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="ba52e-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="ba52e-127">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="ba52e-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="ba52e-128">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="ba52e-129">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="ba52e-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="ba52e-130">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="ba52e-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="ba52e-131">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="ba52e-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="ba52e-132">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="ba52e-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="ba52e-133">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="ba52e-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="ba52e-134">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="ba52e-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="ba52e-135">Laskun hyväksyminen laskun hyväksyntöjen mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="ba52e-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="ba52e-136">Valitse mobiililaitteessasi **laskun hyväksyntöjen** työtila.</span><span class="sxs-lookup"><span data-stu-id="ba52e-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="ba52e-137">Valitse toimittajan laskun otsikon työnkulussa sinulle määritetty lasku.</span><span class="sxs-lookup"><span data-stu-id="ba52e-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="ba52e-138">Tarkista **Laskun tiedot** -sivulla laskun otsikon tiedot, kuten toimittaja ja päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="ba52e-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="ba52e-139">Valitse laskurivi ja tarkastele sen yksityiskohtaisia tietoja **Laskurivin tiedot** -tietoja.</span><span class="sxs-lookup"><span data-stu-id="ba52e-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="ba52e-140">Näytä rivijakelut valitsemalla **Laskurivin tiedot** -näkymässä **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="ba52e-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="ba52e-141">Voit tarkastella täällä laskurivin kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="ba52e-142">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätili.</span><span class="sxs-lookup"><span data-stu-id="ba52e-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="ba52e-143">Näytä kaikki jakelut valitsemalla **Laskun tiedot** -sivulla **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="ba52e-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="ba52e-144">Voit tarkastella täällä koko lasku kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="ba52e-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="ba52e-145">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätilit.</span><span class="sxs-lookup"><span data-stu-id="ba52e-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="ba52e-146">Voit tarkastella laskuun liitettyjä huomautuksia tai tiedostoja valitsemalla **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="ba52e-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="ba52e-147">Viimeistele tarkasteluprosessi valitsemalla **Laskun tiedot** -sivulla soveltuva työkulkutoiminto.</span><span class="sxs-lookup"><span data-stu-id="ba52e-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="ba52e-148">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="ba52e-148">Select **Done**.</span></span>
