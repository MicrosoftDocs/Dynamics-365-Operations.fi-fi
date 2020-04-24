---
title: Resurssien hallinnan mobiilityötila
description: Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.dyn365.ops.version: 10.0.5
ms.search.validFrom: 2019-08-31
ms.openlocfilehash: 525f21d076027f1bf339e59fd0e346706044839c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216502"
---
# <a name="asset-management-mobile-workspace"></a><span data-ttu-id="dd7f4-103">Resurssien hallinnan mobiilityötila</span><span class="sxs-lookup"><span data-stu-id="dd7f4-103">Asset management mobile workspace</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="dd7f4-104">Tässä ohjeaiheessa on tietoja resurssien hallinnan mobiilityötilasta.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-104">This topic provides information about the Asset management mobile workspace.</span></span> <span data-ttu-id="dd7f4-105">Tämä työtila antaa käyttäjien tarkastella ja luoda ylläpitopyyntöjä ja työtilauksia.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-105">This workspace lets users view and create maintenance requests and work orders.</span></span> <span data-ttu-id="dd7f4-106">Käyttäjät voivat myös tarkastella määritettyjä työtilaustöitä kalenteri- tai luettelonäkymässä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-106">Users can also view the assigned work order jobs in a calendar or list view.</span></span> <span data-ttu-id="dd7f4-107">Myös käyttökohteita ja toiminnallisia sijainteja voidaan tarkastella ja etsiä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-107">Assets and functional locations can also be viewed and searched for.</span></span>


## <a name="overview"></a><span data-ttu-id="dd7f4-108">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="dd7f4-108">Overview</span></span>

<span data-ttu-id="dd7f4-109">Resurssien hallinta on kehittynyt moduuli resurssien ja työtilausten hallintaan Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-109">Asset Management is an advanced module for managing assets and work order jobs in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="dd7f4-110">**Resurssien hallinnan** mobiilityötilassa käyttäjät voivat nopeasti tarkastella heille määritettyjä työtilaustöitä valitsemassaan mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-110">The **Asset management** mobile workspace lets users quickly view assigned work order jobs on the mobile device of their choice.</span></span> <span data-ttu-id="dd7f4-111">Käyttäjät voivat myös luoda ja hallita ylläpitopyyntöjä, päivittää elinkaaren tilan sekä tarkastella resurssien ja toiminnallisen sijainnin tietoja omassa mobiililaitteeseen.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-111">Users can also create and manage maintenance requests, update lifecycle state, and view asset and functional location details by using their mobile device.</span></span>

<span data-ttu-id="dd7f4-112">Käyttäjät voivat tehdä **resurssien hallinnan** mobiilityötilassa seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="dd7f4-112">Specifically, the **Asset management** mobile workspace lets users perform these tasks:</span></span>

- <span data-ttu-id="dd7f4-113">Ylläpitopyyntöjen luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen ylläpitopyyntöön ja ylläpitopyynnön elinkaaren tilan muuttaminen.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-113">Create, view, and edit maintenance requests, take a photo or attach an existing image to the maintenance request, change the maintenance request lifecycle state.</span></span> 
- <span data-ttu-id="dd7f4-114">Työtilausten luonti, tarkastelu ja muokkaaminen, valokuvan ottaminen tai aiemmin otetun kuvan liittäminen työtilaukseen, työtilauksen elinkaaren tilan muuttaminen ja työtilauksen töiden tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-114">Create, view, and edit work orders, take a photo or attach an existing image to the work order, change the work order lifecycle state, view work order jobs.</span></span>
- <span data-ttu-id="dd7f4-115">Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-115">View assigned work order jobs in a calendar view.</span></span>
- <span data-ttu-id="dd7f4-116">Työtilauksen työn luonti, tarkastelu ja muokkaus, resurssilaskurien päivitys, ylläpidon tarkastuslistan tarkastelu, työtilauksen työn huomausten tarkastelu ja muokkaus sekä työtilauksen työssä tarvittavien työkalujen tarkastelu.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-116">Create, view, and edit work order job, update asset counters, view maintenance checklist, view and edit work order job notes, view the tools required for the work order job.</span></span>
- <span data-ttu-id="dd7f4-117">Tietyn resurssin tai toiminnallisen sijainnin tarkastelu tai haku.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-117">View or search for a specific asset or functional location.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="dd7f4-118">Edellytykset</span><span class="sxs-lookup"><span data-stu-id="dd7f4-118">Prerequisites</span></span>

<span data-ttu-id="dd7f4-119">Edellytykset vaihtelevat sen mukaan, mikä Dynamics 365 Supply Chain Managementin versio on otettu käyttöön organisaatiossa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-119">The prerequisites vary, based on the version of Dynamics 365 Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-supply-chain-management"></a><span data-ttu-id="dd7f4-120">Edellytykset, jos käytössä on Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="dd7f4-120">Prerequisites if you use Microsoft Dynamics 365 Supply Chain Management</span></span> 
<span data-ttu-id="dd7f4-121">Jos Microsoft Dynamics 365 Supply Chain Management on otettu käyttöön organisaatiossa, järjestelmänvalvojan on julkaistava **Resurssien hallinta** -mobiilityötila.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-121">If Microsoft Dynamics 365 Supply Chain Management has been deployed for your organization, the system administrator must publish the **Asset management** mobile workspace.</span></span> <span data-ttu-id="dd7f4-122">Ohjeet ovat ohjeaiheessa [Mobiilityötilan julkaiseminen](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="dd7f4-122">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="dd7f4-123">Mobiilisovelluksen lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="dd7f4-123">Download and install the mobile app</span></span>
<span data-ttu-id="dd7f4-124">Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:</span><span class="sxs-lookup"><span data-stu-id="dd7f4-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="dd7f4-125">Android-puhelimet</span><span class="sxs-lookup"><span data-stu-id="dd7f4-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="dd7f4-126">IPhone-puhelimet</span><span class="sxs-lookup"><span data-stu-id="dd7f4-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="dd7f4-127">Kirjautuminen mobiilisovellukseen</span><span class="sxs-lookup"><span data-stu-id="dd7f4-127">Sign in to the mobile app</span></span>
1. <span data-ttu-id="dd7f4-128">Käynnistä sovellus mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-128">Start the app on your mobile device.</span></span>

2. <span data-ttu-id="dd7f4-129">Anna Dynamics 365 -URL-osoitteesi.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-129">Enter your Dynamics 365 URL.</span></span>

3. <span data-ttu-id="dd7f4-130">Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="dd7f4-131">Kirjota tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-131">Enter your credentials.</span></span>

4. <span data-ttu-id="dd7f4-132">Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="dd7f4-133">Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-133">Note that if your system administrator publishes a new workspace later, you'll have to refresh the list of mobile workspaces.</span></span>

![Kuva 1](media/am-mobile-01.png)


## <a name="view-assigned-work-order-jobs-in-calendar-view"></a><span data-ttu-id="dd7f4-135">Määritettyjen työtilauksen töiden tarkastelu kalenterinäkymässä</span><span class="sxs-lookup"><span data-stu-id="dd7f4-135">View assigned work order jobs in calendar view</span></span>

1. <span data-ttu-id="dd7f4-136">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-136">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-137">Valitse **Oman työtilauksen töiden kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-137">Select **My work order jobs calendar**.</span></span>

3. <span data-ttu-id="dd7f4-138">Valitse päivämäärä, jona haluat tarkastella työtilauksen töitä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-138">Select the date you want to view work order jobs for.</span></span> <span data-ttu-id="dd7f4-139">Luettelossa on näkyvissä kunkin työtilauksen työn resurssin tunnus ja toiminnallisen sijainnin tunnus.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-139">In the list, you'll see the asset ID and functional location ID for each work order job.</span></span>

4. <span data-ttu-id="dd7f4-140">Saat työn tiedot näkyviin valitsemalla työtilauksen työn luettelossa: resurssin ja toiminnallisen sijainnin tiedot sekä muut siirtymislinkit, joilla voi avata seuraavat kohdat: **Liitteet**, **Tarkistusluettelot**, **Työkalut**, **Resurssilaskurit**, **Huomautukset** ja **Kirjauskansiot**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-140">Select a work order job in the list to see job details: Asset and functional location details as well as other navigation links to view **Attachments**, **Checklists**, **Tools**, **Asset counters**, **Notes**, **Journals**.</span></span>

![Kuva 2](media/am-mobile-02.png)


## <a name="create-a-work-order-job"></a><span data-ttu-id="dd7f4-142">Työtilauksen työn luominen</span><span class="sxs-lookup"><span data-stu-id="dd7f4-142">Create a work order job</span></span>

1. <span data-ttu-id="dd7f4-143">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-143">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-144">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-144">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-145">Valitse työtilaus, jolle haluat luoda uuden työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-145">Select the work order you want to create a new work order job for.</span></span>

4. <span data-ttu-id="dd7f4-146">Valitse **Lisää rivi** -painike.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-146">Select the **Add line** button.</span></span>

5. <span data-ttu-id="dd7f4-147">Valitse **Resurssi**, jolle haluat luoda työtilauksen.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-147">Select the **Asset** you want to create a work order job for.</span></span>

6. <span data-ttu-id="dd7f4-148">Valitse **Ylläpitotyön tyyppi**, **Ylläpitotyön tyypin variantti** ja **Toimiala**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-148">Select **Maintenance job type**, **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="dd7f4-149">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-149">Select **Done**.</span></span>

![Kuva 3](media/am-mobile-03.png)


## <a name="add-attachment-to-a-work-order-job"></a><span data-ttu-id="dd7f4-151">Liitteen lisääminen työtilauksen työhön</span><span class="sxs-lookup"><span data-stu-id="dd7f4-151">Add attachment to a work order job</span></span>

1. <span data-ttu-id="dd7f4-152">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-152">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-153">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-153">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-154">Valitse työtilaus > työtilauksen työ, johon haluat lisätä liitteen.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-154">Select the work order > work order job you want to add an attachment to.</span></span>
    - <span data-ttu-id="dd7f4-155">Vaihtoehtoisesti voit valita myös aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-155">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **Work order job details** page.</span></span>

4. <span data-ttu-id="dd7f4-156">Valitse **Liitteet** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-156">Select **Attachments** on the **Work order job details** page.</span></span>

5. <span data-ttu-id="dd7f4-157">Näkyvissä on työtilauksen työssä jo olevat liitteet.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-157">You'll see existing attachments on the work order job.</span></span> <span data-ttu-id="dd7f4-158">Valitse **Lisää liite**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-158">Select **Add attachment**.</span></span>

6. <span data-ttu-id="dd7f4-159">Anna liitteelle **nimi** ja lisää **huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-159">Enter **Name** and **Notes** for the attachment.</span></span>

7. <span data-ttu-id="dd7f4-160">Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-160">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

8. <span data-ttu-id="dd7f4-161">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-161">Select **Done**.</span></span>

![Kuva 4](media/am-mobile-04.png)


## <a name="view-maintenance-checklist-on-a-work-order-job"></a><span data-ttu-id="dd7f4-163">Työtilauksen työn ylläpidon tarkistuslistan tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="dd7f4-163">View maintenance checklist on a work order job</span></span>

1. <span data-ttu-id="dd7f4-164">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-164">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-165">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-165">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-166">Valitse työtilaus > työtilauksen työ, jonka tarkistusluetteloita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-166">Select the work order > work order job you want to view checklists for.</span></span>
    - <span data-ttu-id="dd7f4-167">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-167">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

4. <span data-ttu-id="dd7f4-168">Valitse **Tarkistusluettelot** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-168">Select **Checklists** on the **Work order job details** page.</span></span>

5. <span data-ttu-id="dd7f4-169">Näkyviin tulee luettelo työtilauksen työhön liittyviä tarkistusluettelon rivejä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-169">You'll see a list of checklist lines related to the work order job.</span></span> <span data-ttu-id="dd7f4-170">Avaa **Ohjeet** valitsemalla tarkistusluettelossa rivi ja lisää **Huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-170">Select a checklist line to view **Instructions** and add **Notes**.</span></span>

6. <span data-ttu-id="dd7f4-171">Palaa edelliselle sivulle valitsemalla Edellinen (**<**) -painike.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-171">Select the back button (**<**) to return to the previous page.</span></span>

![Kuva 5](media/am-mobile-05.png)


## <a name="view-and-update-asset-counters-on-a-work-order-job"></a><span data-ttu-id="dd7f4-173">Resurssilaskurien näyttäminen ja päivittäminen työtilauksen työssä</span><span class="sxs-lookup"><span data-stu-id="dd7f4-173">View and update asset counters on a work order job</span></span>

1. <span data-ttu-id="dd7f4-174">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-174">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-175">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-175">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-176">Valitse työtilaus > työtilauksen työ, jonka resurssilaskureita haluat tarkastella.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-176">Select the work order > work order job you want to view asset counters for.</span></span>
    - <span data-ttu-id="dd7f4-177">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-177">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

4. <span data-ttu-id="dd7f4-178">Valitse **Resurssilaskurit** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-178">Select **Asset counters** on the **Work order job details** page.</span></span>

5. <span data-ttu-id="dd7f4-179">Näkyviin tulee luettelo työtilauksen työhön liittyviä resurssilaskureita.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-179">You see a list of asset counters related to the work order job.</span></span> <span data-ttu-id="dd7f4-180">Päivitä laskurin arvo valitsemalla kynäkuvake resurssilaskurin rivillä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-180">Select the pencil icon on an asset counter line to update the counter value.</span></span>

6. <span data-ttu-id="dd7f4-181">Anna laskurin uusi arvo ja valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-181">Enter a new counter value, and select **Done**.</span></span>

![Kuva 6](media/am-mobile-06.png)


## <a name="register-consumption-on-a-work-order-job"></a><span data-ttu-id="dd7f4-183">Kulutuksen rekisteröinti työtilaus työssä</span><span class="sxs-lookup"><span data-stu-id="dd7f4-183">Register consumption on a work order job</span></span>

1. <span data-ttu-id="dd7f4-184">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-184">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-185">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-185">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-186">Valitse työtilaus > työtilauksen työ, johon haluat lisätä kulutuksen rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-186">Select the work order > work order job you want to add consumtion registrations for.</span></span>
    - <span data-ttu-id="dd7f4-187">Vaihtoehtoisesti voit myös valita aloitussivulla **Oman työtilauksen töiden kalenteri** tai **Oman työtilauksen töiden luettelo** ja siirtyä **Työtilauksen työn tiedot** -sivulle.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-187">Alternatively, you can also select **My work order jobs calendar** or **My work order jobs list** on the home page to navigate to the **work order job details** page.</span></span>

4. <span data-ttu-id="dd7f4-188">Valitse **Kirjauskansiot** **Työtilauksen työn tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-188">Select **Journals** on the **Work order job details** page.</span></span>

5. <span data-ttu-id="dd7f4-189">Luo työtunnin rekisteröinnit valitsemalla **Lisää tunnit**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-189">Select **Add hours** to create work hour registrations.</span></span>
    1. <span data-ttu-id="dd7f4-190">Valitse haussa **Luokka**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-190">Select the **Category** from the lookup.</span></span>
    2. <span data-ttu-id="dd7f4-191">Anna **Tunnit**-kenttään työtilauksen työhön käytetyt työtunnit.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-191">In the **Hours** field, enter the number of work hours spent on the work order job.</span></span>
    3. <span data-ttu-id="dd7f4-192">Valitse sopiva **Rivin ominaisuus**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-192">Select the appropriate **Line property**.</span></span>
    4. <span data-ttu-id="dd7f4-193">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-193">Select **Done**.</span></span>

6. <span data-ttu-id="dd7f4-194">Luo nimikerekisteröinnit valitsemalla **Lisää nimikkeitä**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-194">Select **Add items** to create item registrations.</span></span>
    1. <span data-ttu-id="dd7f4-195">Valitse haussa **Nimiketunnus**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-195">Select the **Item number** from the lookup.</span></span>
    2. <span data-ttu-id="dd7f4-196">Valitse haussa **Toimipaikka**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-196">Select the **Site** from the lookup.</span></span>
    3. <span data-ttu-id="dd7f4-197">Anna kulutettujen nimikkeiden **Määrä**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-197">Enter the **Quantity** of items consumed.</span></span>
    4. <span data-ttu-id="dd7f4-198">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-198">Select **Done**.</span></span>

7. <span data-ttu-id="dd7f4-199">Luo kulurekisteröinnit valitsemalla **Lisää kulu**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-199">Select **Add expense** to create expense registrations.</span></span>
    1. <span data-ttu-id="dd7f4-200">Valitse haussa **Luokka**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-200">Select the **Category** from the lookup.</span></span>
    2. <span data-ttu-id="dd7f4-201">Anna kulurekisteröintien määrä.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-201">Enter the quantity for the expense registration.</span></span>
    3. <span data-ttu-id="dd7f4-202">Valitse haussa **Myyntivaluutta**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-202">Select the **Sales currency** from the lookup.</span></span>
    4. <span data-ttu-id="dd7f4-203">Anna kulurekisteröintien **Kustannushinta**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-203">Enter the **Cost price** for the expense registration.</span></span>
    5. <span data-ttu-id="dd7f4-204">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-204">Select **Done**.</span></span>

![Kuva 7](media/am-mobile-07.png)


## <a name="update-lifecycle-state-on-a-work-order"></a><span data-ttu-id="dd7f4-206">Työtilauksen elinkaaren tilan päivittäminen</span><span class="sxs-lookup"><span data-stu-id="dd7f4-206">Update lifecycle state on a work order</span></span>

1. <span data-ttu-id="dd7f4-207">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-207">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-208">Valitse **Kaikki ylläpidon työtilaukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-208">Select **All maintenance work orders**.</span></span>

3. <span data-ttu-id="dd7f4-209">Valitse työtilaus, jonka elinkaaren tilan haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-209">Select the work order you want to update lifecycle state for.</span></span>

4. <span data-ttu-id="dd7f4-210">Valitse **Päivitä tila** -painike näytön alareunassa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-210">Select the **Update state** button at the bottom of the screen.</span></span>

5. <span data-ttu-id="dd7f4-211">Valitse luettelossa uusi elinkaaren tila.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-211">Select a new lifecycle state from the list.</span></span>

6. <span data-ttu-id="dd7f4-212">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-212">Select **Done**.</span></span>

![Kuva 8](media/am-mobile-08.png)


## <a name="create-a-maintenance-request"></a><span data-ttu-id="dd7f4-214">Luo ylläpitopyyntö</span><span class="sxs-lookup"><span data-stu-id="dd7f4-214">Create a maintenance request</span></span>

1. <span data-ttu-id="dd7f4-215">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-215">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-216">Valitse **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-216">Select **All maintenance requests**.</span></span>

3. <span data-ttu-id="dd7f4-217">Valitse näytön alareunassa ensin **Toiminnot** ja sitten **Luo ylläpitopyyntö**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-217">Select **Actions** at the bottom of the screen, and select **Create maintenance request**.</span></span>

4. <span data-ttu-id="dd7f4-218">Jos huoltopyyntöjen numerosarja otetaan käyttöön **resurssin hallinnassa**, **Ylläpitopyyntö**-kenttä piilotetaan, koska se täytetään automaattisesti. Jos **Ylläpitopyyntö**-kenttä on näkyvissä, anna ylläpitopyynnön tunnus.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-218">If number sequence is enabled for maintenance requests in **Asset management**, the **Maintenance request** field is hidden because it is automatically filled out. If the **Maintenance request** field is visible, enter a maintenance request ID.</span></span>

5. <span data-ttu-id="dd7f4-219">Valitse **Ylläpitopyynnön tyyppi**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-219">Select a **Maintenance request type**.</span></span>

6. <span data-ttu-id="dd7f4-220">Lisää ylläpitopyynnön **Kuvaus**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-220">Enter a **Description** for the maintenance request.</span></span>

7. <span data-ttu-id="dd7f4-221">Valitse **Resurssi**, jolle pyyntö luodaan.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-221">Select the **Asset** you want to create the request for.</span></span>

8. <span data-ttu-id="dd7f4-222">Valitse ylläpitopyynnön **Palvelutaso**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-222">Select the **Service level** for the maintenance request.</span></span>

9. <span data-ttu-id="dd7f4-223">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-223">Select **Done**.</span></span>

![Kuva 9](media/am-mobile-09.png)


## <a name="add-attachment-to-a-maintenance-request"></a><span data-ttu-id="dd7f4-225">Liitteen lisääminen ylläpitopyyntöön</span><span class="sxs-lookup"><span data-stu-id="dd7f4-225">Add attachment to a maintenance request</span></span>

1. <span data-ttu-id="dd7f4-226">Avaa **Resurssien hallinta** -työtila mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-226">On your mobile device, open the **Asset management** workspace.</span></span>

2. <span data-ttu-id="dd7f4-227">Valitse **Kaikki ylläpitopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-227">Select **All maintenance requests**.</span></span>

3. <span data-ttu-id="dd7f4-228">Valitse ylläpitopyyntö, johon liite lisätään.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-228">Select the maintenance request you want to add an attachment to.</span></span>

4. <span data-ttu-id="dd7f4-229">Valitse **Liitteet** näytön alareunassa.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-229">Select **Attachments** at the bottom of the screen.</span></span>

5. <span data-ttu-id="dd7f4-230">Valitse **Lisää liitteet**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-230">Select **Add attachments**.</span></span>

6. <span data-ttu-id="dd7f4-231">Anna liitteelle **nimi** ja lisää **huomautukset**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-231">Enter **Name** and **Notes** for the attachment.</span></span>

7. <span data-ttu-id="dd7f4-232">Valitse kuva mobiililaitteen kuvista valitsemalla **Valitse kuva** tai ota kuva valitsemalla **Ota kuva**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-232">Select **Choose image** to select a photo from the mobile gallery, or **Take photo** to take a photo.</span></span>

8. <span data-ttu-id="dd7f4-233">Valitse **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="dd7f4-233">Select **Done**.</span></span>

![Kuva 10](media/am-mobile-10.png)

