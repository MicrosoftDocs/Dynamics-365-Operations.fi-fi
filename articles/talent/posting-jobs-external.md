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
ms.openlocfilehash: 936ff85a4dabb715cb83b875a5c58c9fb7a0ac26
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739814"
---
# <a name="post-jobs-to-broadbean"></a><span data-ttu-id="99131-103">Työpaikkojen julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="99131-103">Post jobs to Broadbean</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99131-104">Microsoft Dynamics 365 for Talent: Attract auttaa palkkaamaan työntekijöitä mahdollistamalla työpaikkojen julkaisemisen suoraan Attractista Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="99131-104">Microsoft Dynamics 365 for Talent: Attract helps you get the talent you need by letting you post your jobs directly from Attract to Broadbean.</span></span> <span data-ttu-id="99131-105">Kun olet [luonut työpaikan](./creating-jobs-attract.md), sinun tarvitsee vain napsauttaa painiketta, jonka jälkeen työpaikka on työpaikan kaikkien mahdollisten ehdokkaiden nähtävillä Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="99131-105">After you [create a job](./creating-jobs-attract.md), all you have to do is click a button to put your job in front of all the potential job candidates on Broadbean.</span></span>

<span data-ttu-id="99131-106">Työpaikkojen julkaisemista varten Broadbeanissa tarvitaan soveltuva Broadbean-käyttöoikeus.</span><span class="sxs-lookup"><span data-stu-id="99131-106">Posting jobs to Broadbean requires an appropriate Broadbean license.</span></span> <span data-ttu-id="99131-107">Broadbean sisältää erilaisia tuotteita ja suunnitelmia.</span><span class="sxs-lookup"><span data-stu-id="99131-107">Broadbean offers various products and plans.</span></span> <span data-ttu-id="99131-108">Jos haluat lisätietoja Broadbeanin käyttöoikeuksista ja hinnoittelusta, [ota yhteys Broadbeaniin](https://www.broadbean.com/contact-us/).</span><span class="sxs-lookup"><span data-stu-id="99131-108">For more information about Broadbean licensing and pricing, [contact Broadbean](https://www.broadbean.com/contact-us/).</span></span>

<span data-ttu-id="99131-109">Jos olet järjestelmänvalvoja ja tarvitset lisätietoja Broadbeanin integroinnista Attractiin, katso [Ulkoisten työpaikkasivustojen asetusten määrittäminen](./attract-admin-job-board-settings.md).</span><span class="sxs-lookup"><span data-stu-id="99131-109">If you're an admin who needs more information about how to configure Broadbean integration with Attract, see [Enter settings for external job boards](./attract-admin-job-board-settings.md).</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="99131-110">Työpaikkojen julkaiseminen Broadbeaniin</span><span class="sxs-lookup"><span data-stu-id="99131-110">Post jobs to Broadbean</span></span>

<span data-ttu-id="99131-111">Kun Broadbean on otettu käyttöön, rekrytoijat ja järjestelmänvalvojat voivat julkaista sinne työpaikkailmoituksen.</span><span class="sxs-lookup"><span data-stu-id="99131-111">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="99131-112">Ilmoituksessa on oltava URL-osoite työn hakemista varten.</span><span class="sxs-lookup"><span data-stu-id="99131-112">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="99131-113">Avaa Attractissa työ, jonka haluat julkaista Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="99131-113">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="99131-114">Valitse **Ilmoitukset**-osassa **Julkaise nyt** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="99131-114">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="99131-115">Noudata Broadbean-ikkunan ohjeita.</span><span class="sxs-lookup"><span data-stu-id="99131-115">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="99131-116">Attract välittää Broadbeaniin seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="99131-116">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="99131-117">Pyynnön tunnus</span><span class="sxs-lookup"><span data-stu-id="99131-117">Request ID</span></span>
- <span data-ttu-id="99131-118">Ammattinimike</span><span class="sxs-lookup"><span data-stu-id="99131-118">Job title</span></span>
- <span data-ttu-id="99131-119">Työn kuvaus</span><span class="sxs-lookup"><span data-stu-id="99131-119">Job description</span></span>
- <span data-ttu-id="99131-120">Työn sijainti</span><span class="sxs-lookup"><span data-stu-id="99131-120">Job location</span></span>
- <span data-ttu-id="99131-121">Hakemuksen URL-osoite</span><span class="sxs-lookup"><span data-stu-id="99131-121">Apply URL</span></span>
- <span data-ttu-id="99131-122">Työhönottajan tiedot</span><span class="sxs-lookup"><span data-stu-id="99131-122">Recruiter information</span></span>

<span data-ttu-id="99131-123">Kun Broadbean on suorittanut julkaisun, työn **Ilmoitukset**-osio Attractissa näyttää Broadbean-tilana **Julkaistu**.</span><span class="sxs-lookup"><span data-stu-id="99131-123">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="99131-124">Broadbean edellyttää **Toimiala**-kentän.</span><span class="sxs-lookup"><span data-stu-id="99131-124">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="99131-125">Tämän kentän oletusarvo on tällä hetkellä **IT**.</span><span class="sxs-lookup"><span data-stu-id="99131-125">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="99131-126">Voit kuitenkin muuttaa arvoa oikeaan toimialaan Broadbean-työpaikkailmoituksen ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="99131-126">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="99131-127">Kestää jonkin aikaa, kun Broadbean viimeistelee työn julkaisun kaikkiin valitsemiisi työpaikkailmoitussivustoihin.</span><span class="sxs-lookup"><span data-stu-id="99131-127">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="99131-128">Näin voi olla vähäinen viive ennen kuin Attract näyttää työn tilan päivityksen.</span><span class="sxs-lookup"><span data-stu-id="99131-128">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="99131-129">Tarkastele Broadbean-työpaikkailmoitusta</span><span class="sxs-lookup"><span data-stu-id="99131-129">View a Broadbean job posting</span></span>

<span data-ttu-id="99131-130">Kun olet julkaissut työn Broadbeaniin, voit tarkastella sitä Attractista.</span><span class="sxs-lookup"><span data-stu-id="99131-130">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="99131-131">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="99131-131">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="99131-132">Valitse **Ilmoitukset**-välilehdessä Broadbeaniin viittaavat kolme pistettä (**...**) -painike ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="99131-132">On the **Postings** tab, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="99131-133">Broadbean-työpaikkailmoitus näkyy uudessa ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="99131-133">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="99131-134">Päivitä Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="99131-134">Update a Broadbean job posting</span></span>

<span data-ttu-id="99131-135">Voit päivittää Broadbean-työpaikkailmoituksen kahdella tavalla.</span><span class="sxs-lookup"><span data-stu-id="99131-135">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="99131-136">Avaa Attractissa työ, jota haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="99131-136">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="99131-137">Valitse **Ilmoitukset**-osassa **Päivitä julkaisu** -kuvaketta, joka lähettää tiedot Broadbeaniin.</span><span class="sxs-lookup"><span data-stu-id="99131-137">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="99131-138">Muokkaa ilmoitusta Broadbean-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="99131-138">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="99131-139">–TAI–</span><span class="sxs-lookup"><span data-stu-id="99131-139">–or–</span></span>

1. <span data-ttu-id="99131-140">Avaa Attractissa työ, jota haluat tarkastella Broadbeanissa.</span><span class="sxs-lookup"><span data-stu-id="99131-140">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="99131-141">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Näytä**.</span><span class="sxs-lookup"><span data-stu-id="99131-141">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="99131-142">Muokkaa työn tietoja Broadbean-ikkunassa ja julkaise sitten työ uudelleen.</span><span class="sxs-lookup"><span data-stu-id="99131-142">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="99131-143">Työn tietoja Attractissa ei muuteta.</span><span class="sxs-lookup"><span data-stu-id="99131-143">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="99131-144">Poista Broadbean-työpaikkailmoitus</span><span class="sxs-lookup"><span data-stu-id="99131-144">Remove a Broadbean job posting</span></span>

<span data-ttu-id="99131-145">Voit poistaa työpaikkailmoituksen Broadbeanista tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="99131-145">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="99131-146">Avaa Attractissa työ, jonka haluat poistaa.</span><span class="sxs-lookup"><span data-stu-id="99131-146">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="99131-147">Valitse **Ilmoitukset**-osasta kolme pistettä (**...**) -painike, joka vastaa Broadbeania ja valitse sitten **Poista julkaisu**.</span><span class="sxs-lookup"><span data-stu-id="99131-147">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="99131-148">Sen jälkeen, kun Broadbean poistaa työn, Broadbean-kohteessa Attractissa on **Julkaise nyt** -painike.</span><span class="sxs-lookup"><span data-stu-id="99131-148">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="99131-149">Tämä painike ilmaisee, että työ on poistettu ja se voidaan julkaista uudelleen.</span><span class="sxs-lookup"><span data-stu-id="99131-149">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-job-posting-to-broadbean"></a><span data-ttu-id="99131-150">Broadbeanissa julkaistavan työpaikkailmoituksen vianmääritys</span><span class="sxs-lookup"><span data-stu-id="99131-150">Troubleshoot job posting to Broadbean</span></span>

<span data-ttu-id="99131-151">Jos sinulla on vaikeuksia julkaista työ Broadbeanissa, yritä seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="99131-151">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="99131-152">Varmista, että Broadbean-tunnistetiedot, jotka olet määrittänyt Attractissa, ovat voimassa ja oikeelliset.</span><span class="sxs-lookup"><span data-stu-id="99131-152">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="99131-153">Jos tunnistetiedot ovat voimassa ja oikein, ota yhteyttä [Broadbeanin tukeen](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="99131-153">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="99131-154">Jos ongelma ei ratkea, ota yhteyttä [Microsoftin tukeen](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="99131-154">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="99131-155">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="99131-155">See also</span></span>

[<span data-ttu-id="99131-156">Työpaikkojen luominen</span><span class="sxs-lookup"><span data-stu-id="99131-156">Create jobs</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="99131-157">Ulkoisten työpaikkasivustojen asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="99131-157">Enter settings for external job boards</span></span>](./attract-admin-job-board-settings.md)
