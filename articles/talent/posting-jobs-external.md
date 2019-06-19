---
title: Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille
description: Tässä ohjeaiheessa kerrotaan, miten voit Dynamics 365 for Talent - Attractista julkaista töitä ulkoisille työhönoton sivustoille.
author: pganapmsft
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 9c27d1810a89ed7d7a7745e41c5f118dbdfe5dda
ms.sourcegitcommit: cadce85ca3004d53caf6bc49147a524c1bfd421f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/16/2019
ms.locfileid: "1590479"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="960f1-103">Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille</span><span class="sxs-lookup"><span data-stu-id="960f1-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="960f1-104">Haluat saada työpaikkailmoituksesi mahdollisimman monen pätevän ehdokkaan näkyville kuin mahdollista.</span><span class="sxs-lookup"><span data-stu-id="960f1-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="960f1-105">Työhönoton sivustot, kuten Broadbean, voi auttaa saavuttamaan tämän tavoitteen.</span><span class="sxs-lookup"><span data-stu-id="960f1-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="960f1-106">Microsoft Dynamics 365 Talent: Attractin avulla voit nyt julkaista työpaikkoja Broadbeanissa, ja Microsoft tarjoaa koko ajan uusia mahdollisuuksia tällä alueella.</span><span class="sxs-lookup"><span data-stu-id="960f1-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="960f1-107">Työpaikkojen julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="960f1-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="960f1-108">Ennen kuin voit julkaista töitä Broadbeaniin, sinun on määritettävä Broadbean-integrointi.</span><span class="sxs-lookup"><span data-stu-id="960f1-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="960f1-109">Voit julkaista töitä ulkoisille sivustoille vain jos sinulla on [kattava työhönottolaajennus](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="960f1-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="960f1-110">Jos haluat kirjata työt Broadbean-tilaan Attractilla, sinulla on oltava Broadbean-tilaus.</span><span class="sxs-lookup"><span data-stu-id="960f1-110">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="960f1-111">Tämä ominaisuus on tällä hetkellä vain esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="960f1-111">This feature is currently in preview.</span></span> <span data-ttu-id="960f1-112">Voit halutessasi kokeilla sitä [ottamalla sen käyttöön Attractin järjestelmänvalvojan asetuksissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="960f1-112">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="960f1-113">Broadbean-integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="960f1-113">Configure Broadbean integration</span></span>

1. <span data-ttu-id="960f1-114">Kirjaudu Attractiin järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="960f1-114">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="960f1-115">Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa ja valitse sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="960f1-115">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="960f1-116">Ota integraatio käyttöön **Työpaikkailmoitussivun asetukset** -välilehden **Ota Broadbean-integrointi käyttöön** -osassa.</span><span class="sxs-lookup"><span data-stu-id="960f1-116">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="960f1-117">Muodosta yhteys Broadbeaniin ja anna tietosi kohdassa **Käyttäjätunnus, Asiakastunnus, Salaustunnus**.</span><span class="sxs-lookup"><span data-stu-id="960f1-117">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="960f1-118">Broadbean-tunnistetietosi ovat luottamuksellisia.</span><span class="sxs-lookup"><span data-stu-id="960f1-118">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="960f1-119">Siksi tallenna ja jaa niitä vastuuntuntoisesti.</span><span class="sxs-lookup"><span data-stu-id="960f1-119">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="960f1-120">Kaikki käyttäjät, joilla on järjestelmänvalvojan rooli Attractissa, voivat tarkastella näitä tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="960f1-120">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="960f1-121">Microsoft ja Attract eivät ole mukana luomassa ja ylläpitämässä näitä arvoja.</span><span class="sxs-lookup"><span data-stu-id="960f1-121">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="960f1-122">On omalla vastuullasi pitää ne ajan tasalla Attractissa ja selvittää mahdolliset ongelmat Broadbeanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="960f1-122">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="960f1-123">Työpaikan julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="960f1-123">Post a job to Broadbean</span></span>

<span data-ttu-id="960f1-124">Kun Broadbean on otettu käyttöön, rekrytoijat ja järjestelmänvalvojat voivat julkaista sinne työpaikkailmoituksen.</span><span class="sxs-lookup"><span data-stu-id="960f1-124">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="960f1-125">Ilmoituksessa on oltava URL-osoite työn hakemista varten.</span><span class="sxs-lookup"><span data-stu-id="960f1-125">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="960f1-126">Avaa Attractissa työ, jonka haluat julkaista Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="960f1-126">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="960f1-127">Valitse **Ilmoitukset**-osassa **Julkaise nyt** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="960f1-127">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="960f1-128">Noudata Broadbean-ikkunan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="960f1-128">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="960f1-129">Attract välittää Broadbeaniin seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="960f1-129">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="960f1-130">Pyynnön tunnus</span><span class="sxs-lookup"><span data-stu-id="960f1-130">Request ID</span></span>
- <span data-ttu-id="960f1-131">Ammattinimike</span><span class="sxs-lookup"><span data-stu-id="960f1-131">Job title</span></span>
- <span data-ttu-id="960f1-132">Työn kuvaus</span><span class="sxs-lookup"><span data-stu-id="960f1-132">Job description</span></span>
- <span data-ttu-id="960f1-133">Työn sijainti</span><span class="sxs-lookup"><span data-stu-id="960f1-133">Job location</span></span>
- <span data-ttu-id="960f1-134">Hakemuksen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="960f1-134">Apply URL</span></span>
- <span data-ttu-id="960f1-135">Työhönottajan tiedot</span><span class="sxs-lookup"><span data-stu-id="960f1-135">Recruiter information</span></span>

<span data-ttu-id="960f1-136">Kun Broadbean on suorittanut julkaisun, työn **Ilmoitukset**-osio Attractissa näyttää Broadbean-tilana **Julkaistu**.</span><span class="sxs-lookup"><span data-stu-id="960f1-136">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="960f1-137">Broadbean edellyttää **Toimiala**-kentän.</span><span class="sxs-lookup"><span data-stu-id="960f1-137">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="960f1-138">Tämän kentän oletusarvo on tällä hetkellä **IT**.</span><span class="sxs-lookup"><span data-stu-id="960f1-138">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="960f1-139">Voit kuitenkin muuttaa arvoa oikeaan toimialaan Broadbean-työpaikkailmoituksen ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="960f1-139">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="960f1-140">Kestää jonkin aikaa, kun Broadbean viimeistelee työn julkaisun kaikkiin valitsemiisi työpaikkailmoitussivustoihin.</span><span class="sxs-lookup"><span data-stu-id="960f1-140">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="960f1-141">Näin voi olla vähäinen viive ennen kuin Attract näyttää työn tilan päivityksen.</span><span class="sxs-lookup"><span data-stu-id="960f1-141">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="960f1-142">Tarkastele Broadbean-työpaikkailmoitusta</span><span class="sxs-lookup"><span data-stu-id="960f1-142">View a Broadbean job posting</span></span>

<span data-ttu-id="960f1-143">Kun olet julkaissut työn Broadbeaniin, voit tarkastella sitä Attractista.</span><span class="sxs-lookup"><span data-stu-id="960f1-143">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="960f1-144">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="960f1-144">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="960f1-145">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="960f1-145">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="960f1-146">Broadbean-työpaikkailmoitus näkyy uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="960f1-146">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="960f1-147">Päivitä Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="960f1-147">Update a Broadbean job posting</span></span>

<span data-ttu-id="960f1-148">Voit päivittää Broadbean-työpaikkailmoituksen kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="960f1-148">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="960f1-149">Avaa Attractissa työ, jota haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="960f1-149">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="960f1-150">Valitse **Ilmoitukset**-osassa **Päivitä julkaisu** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="960f1-150">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="960f1-151">Muokkaa ilmoitusta Broadbean-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="960f1-151">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="960f1-152">–TAI–</span><span class="sxs-lookup"><span data-stu-id="960f1-152">–or–</span></span>

1. <span data-ttu-id="960f1-153">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="960f1-153">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="960f1-154">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="960f1-154">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="960f1-155">Muokkaa työn tietoja Broadbean-ikkunassa ja julkaise sitten työ uudelleen.</span><span class="sxs-lookup"><span data-stu-id="960f1-155">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="960f1-156">Työn tietoja Attractissa ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="960f1-156">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="960f1-157">Poista Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="960f1-157">Remove a Broadbean job posting</span></span>

<span data-ttu-id="960f1-158">Voit poistaa työpaikkailmoituksen Broadbeanista tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="960f1-158">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="960f1-159">Avaa Attractissa työ, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="960f1-159">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="960f1-160">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Poista julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="960f1-160">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="960f1-161">Sen jälkeen, kun Broadbean poistaa työn, Broadbean-kohteessa Attractissa on **Julkaise nyt** -painike.</span><span class="sxs-lookup"><span data-stu-id="960f1-161">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="960f1-162">Tämä painike ilmaisee, että työ on poistettu ja se voidaan julkaista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="960f1-162">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="960f1-163">Broadbean-integroinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="960f1-163">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="960f1-164">Jos sinulla on vaikeuksia julkaista työ Broadbeanissa, yritä seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="960f1-164">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="960f1-165">Varmista, että Broadbean-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeelliset.</span><span class="sxs-lookup"><span data-stu-id="960f1-165">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="960f1-166">Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [Broadbeanin tukeen](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="960f1-166">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="960f1-167">Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="960f1-167">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
