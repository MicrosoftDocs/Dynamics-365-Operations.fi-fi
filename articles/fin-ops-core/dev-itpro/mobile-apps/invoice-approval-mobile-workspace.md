---
title: Laskujen hyväksyntöjen mobiilityötila
description: Tässä ohjeaiheessa on tietoja laskujen hyväksyntöjen mobiilityötilasta.
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
ms.openlocfilehash: 1a7aa1a03791b8ccb7050389097d1272f5930a49
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127566"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="fea09-103">Laskujen hyväksyntöjen mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="fea09-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fea09-104">Tässä ohjeaiheessa on tietoja **laskujen hyväksyntöjen** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="fea09-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="fea09-105">Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="fea09-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="fea09-106">Tämä mobiilityötila on tarkoitettu käytettäväksi Finance and Operations -mobiilisovelluksen kanssa.</span><span class="sxs-lookup"><span data-stu-id="fea09-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="fea09-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="fea09-107">Overview</span></span>

<span data-ttu-id="fea09-108">**Laskun hyväksyntöjen** mobiilityötilan avulla ostoreskontran käsittelijät ja esimiehet voivat tarkastella laskuja, jotka on määritetty heille toimittajan laskun otsikon työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="fea09-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="fea09-109">Voit tarkastella laskun tietoja sekä rivi- ja jakelutietoja, mikä parantaa hyväksyntäpäätöksiä.</span><span class="sxs-lookup"><span data-stu-id="fea09-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="fea09-110">Voit valita työtilassa toiminnon, jolla lasku siirtyy työnkulussa.</span><span class="sxs-lookup"><span data-stu-id="fea09-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="fea09-111">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="fea09-111">Prerequisites</span></span>

<span data-ttu-id="fea09-112">Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.</span><span class="sxs-lookup"><span data-stu-id="fea09-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="fea09-113">Edellytys</span><span class="sxs-lookup"><span data-stu-id="fea09-113">Prerequisite</span></span></th>
<th><span data-ttu-id="fea09-114">Rooli</span><span class="sxs-lookup"><span data-stu-id="fea09-114">Role</span></span></th>
<th><span data-ttu-id="fea09-115">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="fea09-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fea09-116">Microsoft Dynamics 365 Finance on otettava käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="fea09-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="fea09-117">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="fea09-117">System administrator</span></span></td>
<td><span data-ttu-id="fea09-118">Katso <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</span><span class="sxs-lookup"><span data-stu-id="fea09-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="fea09-119"><strong>Laskun hyväksyntöjen</strong> mobiilityötila on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="fea09-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="fea09-120">Järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="fea09-120">System administrator</span></span></td>
<td><span data-ttu-id="fea09-121">Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</span><span class="sxs-lookup"><span data-stu-id="fea09-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="fea09-122">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="fea09-122">Download and install the mobile app</span></span>

<span data-ttu-id="fea09-123">Finance and Operations -mobiilisovelluksen lataaminen ja asentaminen:</span><span class="sxs-lookup"><span data-stu-id="fea09-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="fea09-124">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="fea09-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="fea09-125">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="fea09-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="fea09-126">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="fea09-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="fea09-127">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="fea09-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="fea09-128">Anna Microsoft Dynamics 365:n URL-osoite.</span><span class="sxs-lookup"><span data-stu-id="fea09-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="fea09-129">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="fea09-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="fea09-130">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="fea09-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="fea09-131">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="fea09-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="fea09-132">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="fea09-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="fea09-133">[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="fea09-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="fea09-134">Laskun hyväksyminen laskun hyväksyntöjen mobiilityötilassa</span><span class="sxs-lookup"><span data-stu-id="fea09-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="fea09-135">Valitse mobiililaitteessasi **laskun hyväksyntöjen** työtila.</span><span class="sxs-lookup"><span data-stu-id="fea09-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="fea09-136">Valitse toimittajan laskun otsikon työnkulussa sinulle määritetty lasku.</span><span class="sxs-lookup"><span data-stu-id="fea09-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="fea09-137">Tarkista **Laskun tiedot** -sivulla laskun otsikon tiedot, kuten toimittaja ja päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="fea09-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="fea09-138">Valitse laskurivi ja tarkastele sen yksityiskohtaisia tietoja **Laskurivin tiedot** -tietoja.</span><span class="sxs-lookup"><span data-stu-id="fea09-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="fea09-139">Näytä rivijakelut valitsemalla **Laskurivin tiedot** -näkymässä **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="fea09-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="fea09-140">Voit tarkastella täällä laskurivin kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="fea09-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="fea09-141">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätili.</span><span class="sxs-lookup"><span data-stu-id="fea09-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="fea09-142">Näytä kaikki jakelut valitsemalla **Laskun tiedot** -sivulla **Jakelut**.</span><span class="sxs-lookup"><span data-stu-id="fea09-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="fea09-143">Voit tarkastella täällä koko lasku kirjanpitoa.</span><span class="sxs-lookup"><span data-stu-id="fea09-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="fea09-144">Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätilit.</span><span class="sxs-lookup"><span data-stu-id="fea09-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="fea09-145">Voit tarkastella laskuun liitettyjä huomautuksia tai tiedostoja valitsemalla **Liitteet**.</span><span class="sxs-lookup"><span data-stu-id="fea09-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="fea09-146">Viimeistele tarkasteluprosessi valitsemalla **Laskun tiedot** -sivulla soveltuva työkulkutoiminto.</span><span class="sxs-lookup"><span data-stu-id="fea09-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="fea09-147">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="fea09-147">Select **Done**.</span></span>
