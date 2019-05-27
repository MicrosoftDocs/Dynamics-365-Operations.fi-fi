---
title: Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille
description: Tässä ohjeaiheessa kerrotaan, miten voit Dynamics 365 for Talent - Attractista julkaista töitä ulkoisille työhönoton sivustoille.
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
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
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517905"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="24255-103">Työpaikkailmoitusten julkaiseminen Attractista ulkoisille urasivustoille</span><span class="sxs-lookup"><span data-stu-id="24255-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24255-104">Haluat saada työpaikkailmoituksesi mahdollisimman monen pätevän ehdokkaan näkyville kuin mahdollista.</span><span class="sxs-lookup"><span data-stu-id="24255-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="24255-105">Työhönoton sivustot, kuten Broadbean, voi auttaa saavuttamaan tämän tavoitteen.</span><span class="sxs-lookup"><span data-stu-id="24255-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="24255-106">Microsoft Dynamics 365 Talent: Attractin avulla voit nyt julkaista työpaikkoja Broadbeanissa, ja Microsoft tarjoaa koko ajan uusia mahdollisuuksia tällä alueella.</span><span class="sxs-lookup"><span data-stu-id="24255-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="24255-107">Työpaikkojen julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="24255-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="24255-108">Ennen kuin voit julkaista töitä Broadbeaniin, sinun on määritettävä Broadbean-integrointi.</span><span class="sxs-lookup"><span data-stu-id="24255-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="24255-109">Voit julkaista töitä ulkoisille sivustoille vain jos sinulla on [kattava työhönottolaajennus](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="24255-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="24255-110">Tämä ominaisuus on tällä hetkellä vain esiversiossa.</span><span class="sxs-lookup"><span data-stu-id="24255-110">This feature is currently in preview.</span></span> <span data-ttu-id="24255-111">Voit halutessasi kokeilla sitä [ottamalla sen käyttöön Attractin järjestelmänvalvojan asetuksissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="24255-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="24255-112">Broadbean-integroinnin määritys</span><span class="sxs-lookup"><span data-stu-id="24255-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="24255-113">Kirjaudu Attractiin järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="24255-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="24255-114">Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa ja valitse sitten **Hallintakeskus**.</span><span class="sxs-lookup"><span data-stu-id="24255-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="24255-115">Ota integraatio käyttöön **Työpaikkailmoitussivun asetukset** -välilehden **Ota Broadbean-integrointi käyttöön** -osassa.</span><span class="sxs-lookup"><span data-stu-id="24255-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="24255-116">Muodosta yhteys Broadbeaniin ja anna tietosi kohdassa **Käyttäjätunnus, Asiakastunnus, Salaustunnus**.</span><span class="sxs-lookup"><span data-stu-id="24255-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="24255-117">Broadbean-tunnistetietosi ovat luottamuksellisia.</span><span class="sxs-lookup"><span data-stu-id="24255-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="24255-118">Siksi tallenna ja jaa niitä vastuuntuntoisesti.</span><span class="sxs-lookup"><span data-stu-id="24255-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="24255-119">Kaikki käyttäjät, joilla on järjestelmänvalvojan rooli Attractissa, voivat tarkastella näitä tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="24255-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="24255-120">Microsoft ja Attract eivät ole mukana luomassa ja ylläpitämässä näitä arvoja.</span><span class="sxs-lookup"><span data-stu-id="24255-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="24255-121">On omalla vastuullasi pitää ne ajan tasalla Attractissa ja selvittää mahdolliset ongelmat Broadbeanin kanssa.</span><span class="sxs-lookup"><span data-stu-id="24255-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="24255-122">Työpaikan julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="24255-122">Post a job to Broadbean</span></span>

<span data-ttu-id="24255-123">Kun Broadbean on otettu käyttöön, rekrytoijat ja järjestelmänvalvojat voivat julkaista sinne työpaikkailmoituksen.</span><span class="sxs-lookup"><span data-stu-id="24255-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="24255-124">Ilmoituksessa on oltava URL-osoite työn hakemista varten.</span><span class="sxs-lookup"><span data-stu-id="24255-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="24255-125">Avaa Attractissa työ, jonka haluat julkaista Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="24255-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="24255-126">Valitse **Ilmoitukset**-osassa **Julkaise nyt** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="24255-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="24255-127">Noudata Broadbean-ikkunan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="24255-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="24255-128">Attract välittää Broadbeaniin seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="24255-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="24255-129">Pyynnön tunnus</span><span class="sxs-lookup"><span data-stu-id="24255-129">Request ID</span></span>
- <span data-ttu-id="24255-130">Ammattinimike</span><span class="sxs-lookup"><span data-stu-id="24255-130">Job title</span></span>
- <span data-ttu-id="24255-131">Työn kuvaus</span><span class="sxs-lookup"><span data-stu-id="24255-131">Job description</span></span>
- <span data-ttu-id="24255-132">Työn sijainti</span><span class="sxs-lookup"><span data-stu-id="24255-132">Job location</span></span>
- <span data-ttu-id="24255-133">Hakemuksen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="24255-133">Apply URL</span></span>
- <span data-ttu-id="24255-134">Työhönottajan tiedot</span><span class="sxs-lookup"><span data-stu-id="24255-134">Recruiter information</span></span>

<span data-ttu-id="24255-135">Kun Broadbean on suorittanut julkaisun, työn **Ilmoitukset**-osio Attractissa näyttää Broadbean-tilana **Julkaistu**.</span><span class="sxs-lookup"><span data-stu-id="24255-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="24255-136">Broadbean edellyttää **Toimiala**-kentän.</span><span class="sxs-lookup"><span data-stu-id="24255-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="24255-137">Tämän kentän oletusarvo on tällä hetkellä **IT**.</span><span class="sxs-lookup"><span data-stu-id="24255-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="24255-138">Voit kuitenkin muuttaa arvoa oikeaan toimialaan Broadbean-työpaikkailmoituksen ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="24255-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="24255-139">Kestää jonkin aikaa, kun Broadbean viimeistelee työn julkaisun kaikkiin valitsemiisi työpaikkailmoitussivustoihin.</span><span class="sxs-lookup"><span data-stu-id="24255-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="24255-140">Näin voi olla vähäinen viive ennen kuin Attract näyttää työn tilan päivityksen.</span><span class="sxs-lookup"><span data-stu-id="24255-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="24255-141">Tarkastele Broadbean-työpaikkailmoitusta</span><span class="sxs-lookup"><span data-stu-id="24255-141">View a Broadbean job posting</span></span>

<span data-ttu-id="24255-142">Kun olet julkaissut työn Broadbeaniin, voit tarkastella sitä Attractista.</span><span class="sxs-lookup"><span data-stu-id="24255-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="24255-143">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="24255-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="24255-144">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="24255-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="24255-145">Broadbean-työpaikkailmoitus näkyy uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="24255-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="24255-146">Päivitä Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="24255-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="24255-147">Voit päivittää Broadbean-työpaikkailmoituksen kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="24255-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="24255-148">Avaa Attractissa työ, jota haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="24255-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="24255-149">Valitse **Ilmoitukset**-osassa **Päivitä julkaisu** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="24255-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="24255-150">Muokkaa ilmoitusta Broadbean-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="24255-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="24255-151">–TAI–</span><span class="sxs-lookup"><span data-stu-id="24255-151">–or–</span></span>

1. <span data-ttu-id="24255-152">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="24255-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="24255-153">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="24255-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="24255-154">Muokkaa työn tietoja Broadbean-ikkunassa ja julkaise sitten työ uudelleen.</span><span class="sxs-lookup"><span data-stu-id="24255-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="24255-155">Työn tietoja Attractissa ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="24255-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="24255-156">Poista Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="24255-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="24255-157">Voit poistaa työpaikkailmoituksen Broadbeanista tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="24255-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="24255-158">Avaa Attractissa työ, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="24255-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="24255-159">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Poista julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="24255-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="24255-160">Sen jälkeen, kun Broadbean poistaa työn, Broadbean-kohteessa Attractissa on **Julkaise nyt** -painike.</span><span class="sxs-lookup"><span data-stu-id="24255-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="24255-161">Tämä painike ilmaisee, että työ on poistettu ja se voidaan julkaista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="24255-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="24255-162">Broadbean-integroinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="24255-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="24255-163">Jos sinulla on vaikeuksia julkaista työ Broadbeanissa, yritä seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="24255-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="24255-164">Varmista, että Broadbean-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeelliset.</span><span class="sxs-lookup"><span data-stu-id="24255-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="24255-165">Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [Broadbeanin tukeen](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="24255-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="24255-166">Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="24255-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
