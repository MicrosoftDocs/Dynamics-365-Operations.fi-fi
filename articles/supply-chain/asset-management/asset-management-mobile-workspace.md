---
title: Resurssien hallinnan mobiilityötilan käyttäminen
description: Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 98f935a11ad8a5272cde0270f9ae0471411b914a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837942"
---
# <a name="use-the-asset-management-mobile-workspace"></a><span data-ttu-id="aca77-103">Resurssien hallinnan mobiilityötilan käyttäminen</span><span class="sxs-lookup"><span data-stu-id="aca77-103">Use the Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aca77-104">Tässä aiheessa on tietoja **resurssien hallinnan** mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="aca77-104">This topic provides information about the **Asset management** mobile workspace.</span></span> <span data-ttu-id="aca77-105">Tämä työtila antaa käyttäjien tarkastella ja luoda ylläpitopyyntöjä ja työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="aca77-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="aca77-106">Käyttäjät voivat myös tarkastella määritettyjä työtilaustöitä kalenteri- tai luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="aca77-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="aca77-107">Myös käyttökohteita ja toiminnallisia sijainteja voidaan tarkastella ja etsiä.</span><span class="sxs-lookup"><span data-stu-id="aca77-107">Assets and functional locations can also be viewed and searched for.</span></span>

## <a name="overview"></a><span data-ttu-id="aca77-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="aca77-108">Overview</span></span>

<span data-ttu-id="aca77-109">Resurssien hallinta on kehittynyt moduuli resurssien ja työtilausten hallintaan Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="aca77-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="aca77-110">**Resurssien hallinnan** mobiilityötilassa käyttäjät voivat nopeasti tarkastella heille määritettyjä työtilaustöitä valitsemassaan mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="aca77-111">Käyttäjät voivat myös luoda ja hallita ylläpitopyyntöjä, päivittää elinkaaren tilan sekä tarkastella resurssien ja toiminnallisen sijainnin tietoja omassa mobiililaitteeseen.</span><span class="sxs-lookup"><span data-stu-id="aca77-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="aca77-112">Käyttäjät voivat tehdä **resurssien hallinnan** mobiilityötilassa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="aca77-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="aca77-113">Ylläpitopyyntöjen luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen ylläpitopyyntöön ja ylläpitopyynnön elinkaaren tilan muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="aca77-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="aca77-114">Työtilausten luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen työtilaukseen, työtilauksen elinkaaren tilan muuttaminen ja työtilauksen töiden tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="aca77-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="aca77-115">Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="aca77-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="aca77-116">Työtilauksen työn luonti, tarkastelu ja muokkaus, resurssilaskurien päivitys, ylläpidon tarkastuslistan tarkastelu, työtilauksen työn huomausten tarkastelu ja muokkaus sekä työtilauksen työssä tarvittavien työkalujen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="aca77-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="aca77-117">Tietyn resurssin tai toiminnallisen sijainnin tarkastelu tai haku.</span><span class="sxs-lookup"><span data-stu-id="aca77-117">View or search for a specific asset or functional location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="aca77-118">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="aca77-118">Prerequisites</span></span>

<span data-ttu-id="aca77-119">**Resurssien hallinnan** mobiilityötilaa ei voi käyttää, ennen kuin järjestelmänvalvoja on määrittävät tarvittavat käyttäjä- ja työntekijätilit sekä julkaissut työtilan.</span><span class="sxs-lookup"><span data-stu-id="aca77-119">Before you can use the **Asset management** mobile workspace, your admin must set up the required user and worker accounts, and publish the workspace.</span></span> <span data-ttu-id="aca77-120">Lisätietoja on kohdassa [Resurssien hallinnan mobiilityötilan määrittäminen](set-up-asset-management-mobile.md).</span><span class="sxs-lookup"><span data-stu-id="aca77-120">For more information, see [Set up the Asset management mobile workspace](set-up-asset-management-mobile.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="aca77-121">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="aca77-121">Download and install the mobile app</span></span>

<span data-ttu-id="aca77-122">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="aca77-122">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="aca77-123">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="aca77-123">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="aca77-124">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="aca77-124">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="aca77-125">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="aca77-125">Sign in to the mobile app</span></span>

1. <span data-ttu-id="aca77-126">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-126">Start the app on your mobile device.</span></span>

1. <span data-ttu-id="aca77-127">Anna Dynamics 365 -URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="aca77-127">Enter your Dynamics 365 URL.</span></span>

1. <span data-ttu-id="aca77-128">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="aca77-128">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="aca77-129">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="aca77-129">Enter your credentials.</span></span>

1. <span data-ttu-id="aca77-130">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="aca77-130">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="aca77-131">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="aca77-131">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="aca77-132">![Työtilan valitseminen](media/am-mobile-01.png "Työtilan valitseminen")</span><span class="sxs-lookup"><span data-stu-id="aca77-132">![Select a workspace](media/am-mobile-01.png "Select a workspace")</span></span>

## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="aca77-133">Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä</span><span class="sxs-lookup"><span data-stu-id="aca77-133">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="aca77-134">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-134">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-135">Valitse **Oman työtilauksen töiden kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="aca77-135">Select **My work order jobs calendar**.</span></span>

1. <span data-ttu-id="aca77-136">Valitse päivämäärä, jona haluat tarkastella työtilauksen töitä.</span><span class="sxs-lookup"><span data-stu-id="aca77-136">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="aca77-137">Luettelossa on näkyvissä kunkin työtilauksen työn resurssin tunnus ja toiminnallisen sijainnin tunnus.</span><span class="sxs-lookup"><span data-stu-id="aca77-137">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

1. <span data-ttu-id="aca77-138">Saat työn tiedot näkyviin valitsemalla työtilauksen työn luettelossa: resurssin ja toiminnallisen sijainnin tiedot sekä muut siirtymislinkit, joilla voi avata seuraavat kohdat: **Liitteet**, **Tarkistusluettelot**, **Työkalut**, **Resurssilaskurit**, **Huomautukset** ja **Kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="aca77-138">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

    <span data-ttu-id="aca77-139">![Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä](media/am-mobile-02.png "Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä")</span><span class="sxs-lookup"><span data-stu-id="aca77-139">![View assigned work order jobs in calendar view](media/am-mobile-02.png "View assigned work order jobs in calendar view")</span></span>

## <a name="create-a-work-order-job"></a><span data-ttu-id="aca77-140">Työtilauksen työn luominen</span><span class="sxs-lookup"><span data-stu-id="aca77-140">Create a work order job</span></span>

1. <span data-ttu-id="aca77-141">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-141">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-142">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-142">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-143">Valitse työtilaus, jolle haluat luoda uuden työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="aca77-143">Select the work order you want to create a new work order job for.</span></span>

1. <span data-ttu-id="aca77-144">Valitse **Lisää rivi** -painike.</span><span class="sxs-lookup"><span data-stu-id="aca77-144">Select the **Add line** button.</span></span>

1. <span data-ttu-id="aca77-145">Valitse **Resurssi**, jolle haluat luoda työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="aca77-145">Select the **Asset** you want to create a work order job for.</span></span>

1. <span data-ttu-id="aca77-146">Valitse **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.</span><span class="sxs-lookup"><span data-stu-id="aca77-146">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

1. <span data-ttu-id="aca77-147">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-147">Select **Done**.</span></span>

    <span data-ttu-id="aca77-148">![Rivin lisäysnäyttö](media/am-mobile-03.png "Rivin lisäysnäyttö")</span><span class="sxs-lookup"><span data-stu-id="aca77-148">![The Add line screen](media/am-mobile-03.png "The Add line screen")</span></span>


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="aca77-149">Liitteen lisääminen työtilauksen työhön</span><span class="sxs-lookup"><span data-stu-id="aca77-149">Add attachment to a work order job</span></span>

1. <span data-ttu-id="aca77-150">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-150">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-151">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-151">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-152">Valitse työtilaus > työtilauksen työ, johon haluat lisätä liitteen.</span><span class="sxs-lookup"><span data-stu-id="aca77-152">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="aca77-153">Vaihtoehtoisesti voit valita myös aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="aca77-153">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

1. <span data-ttu-id="aca77-154">Valitse **Liitteet** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aca77-154">Select **Attachments** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="aca77-155">Näkyvissä on työtilauksen työssä jo olevat liitteet.</span><span class="sxs-lookup"><span data-stu-id="aca77-155">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="aca77-156">Valitse **Lisää liite**.</span><span class="sxs-lookup"><span data-stu-id="aca77-156">Select **Add attachment**.</span></span>

1. <span data-ttu-id="aca77-157">Anna liitteelle **nimi** ja lisää **huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-157">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="aca77-158">Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.</span><span class="sxs-lookup"><span data-stu-id="aca77-158">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="aca77-159">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-159">Select **Done**.</span></span>

    <span data-ttu-id="aca77-160">![Työtilauksen työn liitteiden näyttäminen ja lisääminen](media/am-mobile-04.png "Työtilauksen työn liitteiden näyttäminen ja lisääminen")</span><span class="sxs-lookup"><span data-stu-id="aca77-160">![View and add attachments for a work order job](media/am-mobile-04.png "View and add attachments for a work order job")</span></span>

## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="aca77-161">Työtilauksen työn ylläpidon tarkistuslistan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="aca77-161">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="aca77-162">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-162">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-163">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-163">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-164">Valitse työtilaus > työtilauksen työ, jonka tarkistusluetteloita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="aca77-164">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="aca77-165">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="aca77-165">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="aca77-166">Valitse **Tarkistusluettelot** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aca77-166">Select **Checklists** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="aca77-167">Näkyviin tulee luettelo työtilauksen työhön liittyviä tarkistusluettelon rivejä.</span><span class="sxs-lookup"><span data-stu-id="aca77-167">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="aca77-168">Avaa **Ohjeet** valitsemalla tarkistusluettelossa rivi ja lisää **Huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-168">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

1. <span data-ttu-id="aca77-169">Palaa edelliselle sivulle valitsemalla Edellinen (**<**) -painike.</span><span class="sxs-lookup"><span data-stu-id="aca77-169">Select the back button (**<**) to return to the previous page.</span></span>

    <span data-ttu-id="aca77-170">![Ylläpidon tarkistuslista ja rivin tiedot](media/am-mobile-05.png "Ylläpidon tarkistuslista ja rivin tiedot")</span><span class="sxs-lookup"><span data-stu-id="aca77-170">![Maintenance checklist and line details](media/am-mobile-05.png "Maintenance checklist and line details")</span></span>

## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="aca77-171">Resurssilaskurien näyttäminen ja päivittäminen työtilauksen työssä</span><span class="sxs-lookup"><span data-stu-id="aca77-171">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="aca77-172">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-172">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-173">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-173">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-174">Valitse työtilaus > työtilauksen työ, jonka resurssilaskureita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="aca77-174">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="aca77-175">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="aca77-175">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="aca77-176">Valitse **Resurssilaskurit** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aca77-176">Select **Asset counters** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="aca77-177">Näkyviin tulee luettelo työtilauksen työhön liittyviä resurssilaskureita.</span><span class="sxs-lookup"><span data-stu-id="aca77-177">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="aca77-178">Päivitä laskurin arvo valitsemalla kynäkuvake resurssilaskurin rivillä.</span><span class="sxs-lookup"><span data-stu-id="aca77-178">Select the pencil icon on an asset counter line to update the counter value.</span></span>

1. <span data-ttu-id="aca77-179">Anna laskurin uusi arvo ja valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-179">Enter a new counter value, and select **Done**.</span></span>

    <span data-ttu-id="aca77-180">![Resurssilaskureiden näyttäminen ja päivittäminen](media/am-mobile-06.png "Resurssilaskureiden näyttäminen ja päivittäminen")</span><span class="sxs-lookup"><span data-stu-id="aca77-180">![View and update asset counters](media/am-mobile-06.png "View and update asset counters")</span></span>

## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="aca77-181">Kulutuksen rekisteröinti työtilaus työssä</span><span class="sxs-lookup"><span data-stu-id="aca77-181">Register consumption on a work order job</span></span>

1. <span data-ttu-id="aca77-182">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-182">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-183">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-183">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-184">Valitse työtilaus > työtilauksen työ, johon kulutuksen rekisteröinnit halutaan lisätä.</span><span class="sxs-lookup"><span data-stu-id="aca77-184">Select the work order > work order job you want to add consumption registrations for.</span></span>
    - <span data-ttu-id="aca77-185">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="aca77-185">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

1. <span data-ttu-id="aca77-186">Valitse **Kirjauskansiot** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="aca77-186">Select **Journals** on the **Work order job details** page.</span></span>

1. <span data-ttu-id="aca77-187">Luo työtunnin rekisteröinnit valitsemalla **Lisää tunnit**.</span><span class="sxs-lookup"><span data-stu-id="aca77-187">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="aca77-188">Valitse haussa **Luokka**.</span><span class="sxs-lookup"><span data-stu-id="aca77-188">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="aca77-189">Anna **Tunnit**-kenttään työtilauksen työhön käytetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="aca77-189">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    1. <span data-ttu-id="aca77-190">Valitse sopiva **Rivin ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="aca77-190">Select the appropriate **Line property**.</span></span>
    1. <span data-ttu-id="aca77-191">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-191">Select **Done**.</span></span>

1. <span data-ttu-id="aca77-192">Luo nimikerekisteröinnit valitsemalla **Lisää nimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="aca77-192">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="aca77-193">Valitse haussa **Nimiketunnus**.</span><span class="sxs-lookup"><span data-stu-id="aca77-193">Select the **Item number** from the lookup.</span></span>
    1. <span data-ttu-id="aca77-194">Valitse haussa **Toimipaikka**.</span><span class="sxs-lookup"><span data-stu-id="aca77-194">Select the **Site** from the lookup.</span></span>
    1. <span data-ttu-id="aca77-195">Anna kulutettujen nimikkeiden **Määrä**.</span><span class="sxs-lookup"><span data-stu-id="aca77-195">Enter the **Quantity** of items consumed.</span></span>
    1. <span data-ttu-id="aca77-196">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-196">Select **Done**.</span></span>

1. <span data-ttu-id="aca77-197">Luo kulurekisteröinnit valitsemalla **Lisää kulu**.</span><span class="sxs-lookup"><span data-stu-id="aca77-197">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="aca77-198">Valitse haussa **Luokka**.</span><span class="sxs-lookup"><span data-stu-id="aca77-198">Select the **Category** from the lookup.</span></span>
    1. <span data-ttu-id="aca77-199">Anna kulurekisteröintien määrä.</span><span class="sxs-lookup"><span data-stu-id="aca77-199">Enter the quantity for the expense registration.</span></span>
    1. <span data-ttu-id="aca77-200">Valitse haussa **Myyntivaluutta**.</span><span class="sxs-lookup"><span data-stu-id="aca77-200">Select the **Sales currency** from the lookup.</span></span>
    1. <span data-ttu-id="aca77-201">Anna kulurekisteröintien **Kustannushinta**.</span><span class="sxs-lookup"><span data-stu-id="aca77-201">Enter the **Cost price** for the expense registration.</span></span>
    1. <span data-ttu-id="aca77-202">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-202">Select **Done**.</span></span>

    <span data-ttu-id="aca77-203">![Työtilauksen kirjauskansion päivittäminen](media/am-mobile-07.png "Työtilauksen kirjauskansion päivittäminen")</span><span class="sxs-lookup"><span data-stu-id="aca77-203">![Update a work order journal](media/am-mobile-07.png "Update a work order journal")</span></span>

## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="aca77-204">Työtilauksen elinkaaren tilan päivittäminen</span><span class="sxs-lookup"><span data-stu-id="aca77-204">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="aca77-205">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-205">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-206">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-206">Select **All maintenance work orders**.</span></span>

1. <span data-ttu-id="aca77-207">Valitse työtilaus, jonka elinkaaren tilan haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="aca77-207">Select the work order you want to update lifecycle state for.</span></span>

1. <span data-ttu-id="aca77-208">Valitse **Päivitä tila** -painike näytön alareunassa.</span><span class="sxs-lookup"><span data-stu-id="aca77-208">Select the **Update state** button at the bottom of the screen.</span></span>

1. <span data-ttu-id="aca77-209">Valitse luettelossa uusi elinkaaren tila.</span><span class="sxs-lookup"><span data-stu-id="aca77-209">Select a new lifecycle state from the list.</span></span>

1. <span data-ttu-id="aca77-210">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-210">Select **Done**.</span></span>

    <span data-ttu-id="aca77-211">![Työtilauksen elinkaaren tilan päivittäminen](media/am-mobile-08.png "Työtilauksen elinkaaren tilan päivittäminen")</span><span class="sxs-lookup"><span data-stu-id="aca77-211">![Update lifecycle state on a work order](media/am-mobile-08.png "Update lifecycle state on a work order")</span></span>

## <a name="create-a-maintenance-request"></a><span data-ttu-id="aca77-212">Luo ylläpitopyyntö</span><span class="sxs-lookup"><span data-stu-id="aca77-212">Create a maintenance request</span></span>

1. <span data-ttu-id="aca77-213">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-213">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-214">Valitse **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="aca77-214">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="aca77-215">Valitse näytön alareunassa ensin **Toiminnot** ja sitten **Luo ylläpitopyyntö**.</span><span class="sxs-lookup"><span data-stu-id="aca77-215">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

1. <span data-ttu-id="aca77-216">Jos huoltopyyntöjen numerosarja otetaan käyttöön **resurssin hallinnassa**, **Ylläpitopyyntö**-kenttä piilotetaan, koska se täytetään automaattisesti. Jos **Ylläpitopyyntö**-kenttä on näkyvissä, anna ylläpitopyynnön tunnus.</span><span class="sxs-lookup"><span data-stu-id="aca77-216">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

1. <span data-ttu-id="aca77-217">Valitse **Ylläpitopyynnön tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="aca77-217">Select a **Maintenance request type**.</span></span>

1. <span data-ttu-id="aca77-218">Lisää ylläpitopyynnön **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="aca77-218">Enter a **Description** for the maintenance request.</span></span>

1. <span data-ttu-id="aca77-219">Valitse **Resurssi**, jolle pyyntö luodaan.</span><span class="sxs-lookup"><span data-stu-id="aca77-219">Select the **Asset** you want to create the request for.</span></span>

1. <span data-ttu-id="aca77-220">Valitse ylläpitopyynnön **Palvelutaso**.</span><span class="sxs-lookup"><span data-stu-id="aca77-220">Select the **Service level** for the maintenance request.</span></span>

1. <span data-ttu-id="aca77-221">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-221">Select **Done**.</span></span>

    <span data-ttu-id="aca77-222">![Luo ylläpitopyyntö](media/am-mobile-09.png "Luo ylläpitopyyntö")</span><span class="sxs-lookup"><span data-stu-id="aca77-222">![Create a maintenance request](media/am-mobile-09.png "Create a maintenance request")</span></span>

## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="aca77-223">Liitteen lisääminen ylläpitopyyntöön</span><span class="sxs-lookup"><span data-stu-id="aca77-223">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="aca77-224">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="aca77-224">On your mobile device, open the **Asset management** workspace.</span></span>

1. <span data-ttu-id="aca77-225">Valitse **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="aca77-225">Select **All maintenance requests**.</span></span>

1. <span data-ttu-id="aca77-226">Valitse ylläpitopyyntö, johon liite lisätään.</span><span class="sxs-lookup"><span data-stu-id="aca77-226">Select the maintenance request you want to add an attachment to.</span></span>

1. <span data-ttu-id="aca77-227">Valitse **Liitteet** näytön alareunassa.</span><span class="sxs-lookup"><span data-stu-id="aca77-227">Select **Attachments** at the bottom of the screen.</span></span>

1. <span data-ttu-id="aca77-228">Valitse **Lisää liitteet**.</span><span class="sxs-lookup"><span data-stu-id="aca77-228">Select **Add attachments**.</span></span>

1. <span data-ttu-id="aca77-229">Anna liitteelle **nimi** ja lisää **huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="aca77-229">Enter **Name** and **Notes** for the attachment.</span></span>

1. <span data-ttu-id="aca77-230">Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.</span><span class="sxs-lookup"><span data-stu-id="aca77-230">Select **Choose image** to select a photo from the mobile gallery or **Take photo** to take a photo.</span></span>

1. <span data-ttu-id="aca77-231">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="aca77-231">Select **Done**.</span></span>

    <span data-ttu-id="aca77-232">![Liitteen lisääminen ylläpitopyyntöön](media/am-mobile-10.png "Liitteen lisääminen ylläpitopyyntöön")</span><span class="sxs-lookup"><span data-stu-id="aca77-232">![Add an attachment to a maintenance request](media/am-mobile-10.png "Add an attachment to a maintenance request")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]