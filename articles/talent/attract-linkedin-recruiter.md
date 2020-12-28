---
title: Ehdokkaiden rekrytointi LinkedIn Recruiterilla Attractissa
description: Rekrytoi ehdokkaita työpaikkaan LinkedIn Recruiterin avulla käyttämällä Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraatiota.
author: andreabichsel
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 96e4660c4958bf5f2a0910bfad770e1e713f800f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528266"
---
# <a name="source-candidates-with-linkedin-recruiter-in-attract"></a><span data-ttu-id="2b021-103">Ehdokkaiden rekrytointi LinkedIn Recruiterilla Attractissa</span><span class="sxs-lookup"><span data-stu-id="2b021-103">Source candidates with LinkedIn Recruiter in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b021-104">LinkedIn on maailman suurin verkossa toimiva asiantuntijaverkosto, jonka avulla koko maailman parhaat osaajat ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="2b021-104">LinkedIn is the world's largest online professional network, giving you access to the world's top talent.</span></span> <span data-ttu-id="2b021-105">Microsoft Dynamics 365 Talent: Attractin avulla voit rekrytoida ehdokkaita suoraan LinkedInistä.</span><span class="sxs-lookup"><span data-stu-id="2b021-105">Microsoft Dynamics 365 Talent: Attract lets you source candidates directly from LinkedIn.</span></span> <span data-ttu-id="2b021-106">Niinpä sopivien osaajien löytäminen avoimiin työpaikkoihin on helpompaa kuin koskaan.</span><span class="sxs-lookup"><span data-stu-id="2b021-106">Therefore, it's easier than ever to find the talent that you need to fill your open positions.</span></span> <span data-ttu-id="2b021-107">Kun olet muodostanut LinkedIn-yhteyden Attractin kautta, voit tarkastella työpaikkaan sopivia mahdollisia LinkedIn-ehdokkaita ja viedä heidät Attractiin yhdellä napsautuksella.</span><span class="sxs-lookup"><span data-stu-id="2b021-107">After you set up your connection with LinkedIn through Attract, you can view potential LinkedIn candidates for your positions and export them into Attract with just one click.</span></span>

<span data-ttu-id="2b021-108">Jos tämä toiminto ei näytä olevan käytössä, ota yhteys järjestelmänvalvojaan. Ennen kuin LinkedIn Recruiteria voi käyttää Attractista, järjestelmänvalvojan on [LinkedIn-integraatio](./attract-admin-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="2b021-108">If you don't seem to have this capability, contact your admin. Before you can take advantage of LinkedIn Recruiter from Attract, your admin must [set up integration with LinkedIn](./attract-admin-linkedin.md).</span></span> <span data-ttu-id="2b021-109">Voit sitten määrittää LinkedIn Recruiter -yhteyden ja aloittaa ehdokkaiden etsimisen.</span><span class="sxs-lookup"><span data-stu-id="2b021-109">You can then set up your connection with LinkedIn Recruiter and start finding candidates.</span></span>

>[!IMPORTANT]
><span data-ttu-id="2b021-110">1. heinäkuuta 2020 alkaen LinkedInissä ei enää ole Internet Explorer 11 -tukea.</span><span class="sxs-lookup"><span data-stu-id="2b021-110">As of July 1, 2020, LinkedIn no longer supports Internet Explorer 11.</span></span> <span data-ttu-id="2b021-111">Käyttäjät voivat yhä käyttää LinkedInia Internet Explorer 11:n avulla, mutta heitä kehotetaan päivittämään selain tai käyttämään toista selainta.</span><span class="sxs-lookup"><span data-stu-id="2b021-111">Users can still access LinkedIn with Internet Explorer 11, but will be prompted to upgrade or use a different browser.</span></span> <span data-ttu-id="2b021-112">Lisätietoja on kohdassa [LinkedInin tuetut internet-selaimet](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span><span class="sxs-lookup"><span data-stu-id="2b021-112">For more information, see [Supported Internet Browsers for LinkedIn](https://www.linkedin.com/help/linkedin/answer/4135/supported-internet-browsers-for-linkedin).</span></span>

## <a name="set-up-your-connection-with-linkedin-recruiter"></a><span data-ttu-id="2b021-113">LinkedIn Recruiter -yhteyden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2b021-113">Set up your connection with LinkedIn Recruiter</span></span>

<span data-ttu-id="2b021-114">LinkedIn Recruiter -yhteys on määritettävä, ennen kuin voit aloittaa LinkedIn Recruiterin käytön Attractissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-114">Before you can start working with LinkedIn Recruiter through Attract, you must set up your connection with LinkedIn Recruiter.</span></span> <span data-ttu-id="2b021-115">Tarvitset tässä vaiheessa LinkedIn Recruiter -tunnistetiedot.</span><span class="sxs-lookup"><span data-stu-id="2b021-115">For this step, you need your LinkedIn Recruiter credentials.</span></span>

1. <span data-ttu-id="2b021-116">Valitse **Asetukset**-painike (rataskuvake) sivun oikeassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="2b021-116">Select the **Settings** button (gear icon) in the upper-right corner of the page.</span></span>
2. <span data-ttu-id="2b021-117">Valitse **Käyttäjäasetukset**.</span><span class="sxs-lookup"><span data-stu-id="2b021-117">Select **User settings**.</span></span>
3. <span data-ttu-id="2b021-118">Valitse **Yhteydet**-välilehdessä **Yhdistä**-asetus **LinkedIn**-kohdan vieressä.</span><span class="sxs-lookup"><span data-stu-id="2b021-118">On the **Connections** tab, select **Connect** next to **LinkedIn**.</span></span> <span data-ttu-id="2b021-119">Noudata LinkedInin antamia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="2b021-119">Follow the instructions that are provided by LinkedIn.</span></span>

    ![[<span data-ttu-id="2b021-120">LinkedIn Recruiterin yhteyden määrittäminen Attractista</span><span class="sxs-lookup"><span data-stu-id="2b021-120">Set up connection to LinkedIn Recruiter from Attract</span></span>](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a><span data-ttu-id="2b021-121">LinkedIn-ehdokkaiden näyttäminen Attractissa</span><span class="sxs-lookup"><span data-stu-id="2b021-121">View LinkedIn candidates in Attract</span></span>

<span data-ttu-id="2b021-122">Kun olet muodostanut LinkedIn Recruiter -yhteyden, voit tarkastella ehdokkaiden LinkedIn-profiileja Attractissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-122">After you're connected to LinkedIn Recruiter, you can view candidates' LinkedIn profiles in Attract.</span></span>

>[!NOTE]
><span data-ttu-id="2b021-123">Jos sinulle on määritetty työhönottajan rooli, näet ehdokkaiden kaikki tiedot.</span><span class="sxs-lookup"><span data-stu-id="2b021-123">If you have a Recruiter seat assigned to you, you can see the candidates' full information.</span></span><br><br>
><span data-ttu-id="2b021-124">Jos sinulla on työhön ottavan esimiehen rooli tai jos sinulle ei ole määritetty roolia, muista kirjautua ulos LinkedInista tai LinkedIn Recruiterista ennen kuin siirryt Attractissa ehdokkaan LinkedIn-välilehteen.</span><span class="sxs-lookup"><span data-stu-id="2b021-124">If you have a Hiring Manager seat or no seat assigned to you, be sure to sign out of LinkedIn or LinkedIn Recruiter before navigating to the LinkedIn tab for a candidate in Attract.</span></span> <span data-ttu-id="2b021-125">Näkyvissä ovat ehdokkaan julkisen profiilin perustiedot, kuten etu- ja sukunimi.</span><span class="sxs-lookup"><span data-stu-id="2b021-125">You'll be able to see the candidate's basic public profile data, such as their first and last name.</span></span>

1. <span data-ttu-id="2b021-126">Valitse Attractissa vasemmalla **Työt** tai **Kykypoolit** ja valitse sitten hakija.</span><span class="sxs-lookup"><span data-stu-id="2b021-126">In Attract, select **Jobs** or **Talent pools** on the left, and then select an applicant.</span></span>

    ![[<span data-ttu-id="2b021-127">LinkedIn-ehdokkaiden näyttäminen Attractissa</span><span class="sxs-lookup"><span data-stu-id="2b021-127">View LinkedIn candidates in Attract</span></span>](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. <span data-ttu-id="2b021-128">Valitse ehdokkaan profiilissa **LinkedIn**-välilehti. Voit tarkastella ehdokkaan profiilia ja InMail-historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="2b021-128">In the candidate's profile, select the **LinkedIn** tab. You can view the candidate's profile and InMail history.</span></span>

   ![Ehdokkaan LinkedIn-tietojen tarkasteleminen](./media/attract-candidate-linkedin-tab.png)

<span data-ttu-id="2b021-130">Tässä voit myös tehdä seuraavia toimenpiteitä:</span><span class="sxs-lookup"><span data-stu-id="2b021-130">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="2b021-131">Valitse **Rekrytointitehtävät**-välilehti, jos haluat tarkastella seuraavia tietoja:</span><span class="sxs-lookup"><span data-stu-id="2b021-131">Select the **Recruiting activities** tab to view:</span></span>
   
   - <span data-ttu-id="2b021-132">Työhönottajan huomautukset (sekä julkiset että yksityiset).</span><span class="sxs-lookup"><span data-stu-id="2b021-132">Recruiter notes (both public and private).</span></span> <span data-ttu-id="2b021-133">Oletusarvoisest huomautukset ovat yksityisiä. Ne näkyvät vain huomautusten omistajille.</span><span class="sxs-lookup"><span data-stu-id="2b021-133">By default, notes are private and only visible to the owner of the notes.</span></span>
   - <span data-ttu-id="2b021-134">InMail-aktiviteetti (mutta ei InMail-sisältö).</span><span class="sxs-lookup"><span data-stu-id="2b021-134">InMail activity (but not the InMail content).</span></span> <span data-ttu-id="2b021-135">Siirry sivun alaosaan, jos haluat tarkastella InMail-siirtoa ja prospektia sekä organisaation muita käyttäjiä, jotka ovat yhteydessä prospektin kanssa.</span><span class="sxs-lookup"><span data-stu-id="2b021-135">Scroll to the bottom of the page to view the InMail exchange with your prospect and view other users in your organization who are interacting with your prospect.</span></span>
   - <span data-ttu-id="2b021-136">Ehdokkaan hylkäystehtävä</span><span class="sxs-lookup"><span data-stu-id="2b021-136">Candidate rejection activity</span></span>

- <span data-ttu-id="2b021-137">Valitse **Lähetä InMail**, jos haluat lähettää InMailin poistumatta Attractista.</span><span class="sxs-lookup"><span data-stu-id="2b021-137">Select **Send InMail** to send InMail without having to leave Attract.</span></span>

- <span data-ttu-id="2b021-138">Valitse **Tallenna työhön**, jos haluat tallentaa työn poistumatta Attractista.</span><span class="sxs-lookup"><span data-stu-id="2b021-138">Select **Save to a job** to save the job without leaving Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="2b021-139">Ehdokkaan LinkedIn-profiili näytetään Attractissa, kun ehdokkaan Attract-tiedot vastaavat LinkedIn-tietoja.</span><span class="sxs-lookup"><span data-stu-id="2b021-139">A candidate's LinkedIn profile will display in Attract when the candidate's Attract information matches the LinkedIn information.</span></span> <span data-ttu-id="2b021-140">Käytettävät vastaavuussäännöt:</span><span class="sxs-lookup"><span data-stu-id="2b021-140">Here are the matching rules that are used:</span></span>
> 
> 1. <span data-ttu-id="2b021-141">Jos sähköpostiosoite ja LinkedIn-jäsentunnus ovat samat Attractissa ja LinkedInissä, ehdokkaan profiili näytetään.</span><span class="sxs-lookup"><span data-stu-id="2b021-141">If the email address and LinkedIn member ID match in Attract and LinkedIn, the candidate's profile is shown.</span></span> <span data-ttu-id="2b021-142">Ehdokkaat voivat kuitenkin valita Attractissa, linkittävätkö he LinkedIn-profiilinsa vai eivät.</span><span class="sxs-lookup"><span data-stu-id="2b021-142">Candidates still have the option to link or unlink their LinkedIn profile from Attract.</span></span>
> 2. <span data-ttu-id="2b021-143">Jos sähköpostiosoite tai LinkedIn-jäsentunnus eivät vastaa toisiaan, näkyviin tulee luettelo mahdollisista ehdokkaista.</span><span class="sxs-lookup"><span data-stu-id="2b021-143">If the email address or LinkedIn member ID doesn't match, you see a list of possible candidates.</span></span> <span data-ttu-id="2b021-144">Voit sitten valita ehdokkaan luettelosta ja linkittää profiilin.</span><span class="sxs-lookup"><span data-stu-id="2b021-144">You can then select a candidate in the list and link the profile.</span></span>
> 3. <span data-ttu-id="2b021-145">Jos hyviä vastaavuuksia ei ole, saat ilmoituksen siitä, ettei vastaavuutta löytynyt.</span><span class="sxs-lookup"><span data-stu-id="2b021-145">If there are no good matches, you're notified that no match was found.</span></span>

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a><span data-ttu-id="2b021-146">LinkedIn-ehdokkaiden vienti Attractiin yhdellä napsautuksella</span><span class="sxs-lookup"><span data-stu-id="2b021-146">Export LinkedIn candidates to Attract with one click</span></span>

<span data-ttu-id="2b021-147">Samalla kun tarkastelet ehdokkaista LinkedIn Recruiterissa, voit viedä heidät Attractissa avoimina oleviin työpaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="2b021-147">While you're reviewing candidates in LinkedIn Recruiter, you can export them to jobs that you currently have open in Attract.</span></span> <span data-ttu-id="2b021-148">Tätä vaihetta varten tarvitaan Attractin työhönottajan tai työhön ottavan esimiehen käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="2b021-148">For this step, you need Recruiter or Hiring Manager permissions in Attract.</span></span> <span data-ttu-id="2b021-149">Lisätietoja näistä Attractin rooleista kohdassa [Suojaus ja roolien hallinta Attractissa](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span><span class="sxs-lookup"><span data-stu-id="2b021-149">For more information about roles in Attract, see [Security and role management in Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).</span></span>

<span data-ttu-id="2b021-150">Sinun on myös varmistettava, että työpaikassa on Prospekti-vaihe.</span><span class="sxs-lookup"><span data-stu-id="2b021-150">You must also make sure that the job has a Prospect stage.</span></span> <span data-ttu-id="2b021-151">Lisätietoja on kohdassa [Prospekti-tehtävä](./activities-attract.md#prospect-activity).</span><span class="sxs-lookup"><span data-stu-id="2b021-151">For more information, see [Prospect activity](./activities-attract.md#prospect-activity).</span></span>

1. <span data-ttu-id="2b021-152">Luo Attractissa työpaikka, määritä soveltuvat roolit ja aktivoi työpaikka.</span><span class="sxs-lookup"><span data-stu-id="2b021-152">In Attract, create a job, assign the appropriate roles, and activate the job.</span></span>
2. <span data-ttu-id="2b021-153">Etsi LinkedIn Recruiterissa työpaikkaan hyvä ehdokas ja siirry ehdokkaan profiiliin.</span><span class="sxs-lookup"><span data-stu-id="2b021-153">In LinkedIn Recruiter, find a good candidate for the job, and go to the candidate's profile.</span></span>
3. <span data-ttu-id="2b021-154">Etsi yhteyshenkilökortin työpaikan hakuruudun avulla työpaikka nimikkeen tai Attractissa aktivoidun työpaikan tunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="2b021-154">In the job search box in the contact card, find the job by using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="2b021-155">Jos et löydä työpaikkaa, etsi oikea Attract-esiintymä valitsemalla **Vaihda ATS**.</span><span class="sxs-lookup"><span data-stu-id="2b021-155">If you can't find the job, select **Change ATS** to find the correct Attract instance.</span></span>
4. <span data-ttu-id="2b021-156">Valitse ensin työpaikka ja sitten **Vie**.</span><span class="sxs-lookup"><span data-stu-id="2b021-156">Select the job, and then select **Export**.</span></span>
5. <span data-ttu-id="2b021-157">Avaa työ Attractissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-157">In Attract, open the job.</span></span> <span data-ttu-id="2b021-158">Viety ehdokas näkyy työpaikan **Prospekti**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="2b021-158">The exported candidate will appear on the **Prospect** tab of the job.</span></span>

## <a name="view-attract-information-in-linkedin-recruiter"></a><span data-ttu-id="2b021-159">Attract-tietojen näyttämine LinkedIn Recruiterissa</span><span class="sxs-lookup"><span data-stu-id="2b021-159">View Attract information in LinkedIn Recruiter</span></span>

<span data-ttu-id="2b021-160">Voit seurata LinkedIn Recruiterissa, onko ehdokas hakenut organisaatiossa muita työpaikkoja, katsoa, missä työhakemusten vaiheessa ehdokas on, ja tarkastella Attractin palautetta ja kommentteja issa.</span><span class="sxs-lookup"><span data-stu-id="2b021-160">In LinkedIn Recruiter, you can track whether a candidate applied to other jobs in your organization, see where the candidate is in the various stages for job applications, and view feedback and comments from Attract.</span></span>

1. <span data-ttu-id="2b021-161">Avaa LinkedIn Recruiter ja valitse ehdokkaan profiili.</span><span class="sxs-lookup"><span data-stu-id="2b021-161">Open LinkedIn Recruiter, and select a candidate profile.</span></span>
2. <span data-ttu-id="2b021-162">Pidä osoitinta **ATS:n**-kohdan päällä.</span><span class="sxs-lookup"><span data-stu-id="2b021-162">Hover over **In ATS**.</span></span>
3. <span data-ttu-id="2b021-163">Tarkastele ehdokkaan Attractiin tallennettuja tietoja valitsemalla jokin seuraavista vaihtoehdoista:</span><span class="sxs-lookup"><span data-stu-id="2b021-163">Select any of the following options to view the candidate information that is stored in Attract:</span></span>

    - <span data-ttu-id="2b021-164">**Työpaikat ja tilat** – voit katsoa työpaikkoja, joissa ehdokas on osallisena, viimeisintä tilaa ja ehdokkaan etenemistä kussakin työpaikassa.</span><span class="sxs-lookup"><span data-stu-id="2b021-164">**Jobs & Statuses** – See jobs that the candidate is part of, the latest status, and how the candidate is progressing for each job.</span></span>
    - <span data-ttu-id="2b021-165">**Haastattelun palaute** – katso, mitä palautetta haastattelijat ovat lähettäneet Attractissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-165">**Interview Feedback** – See feedback that interviewers have submitted in Attract.</span></span>
    - <span data-ttu-id="2b021-166">**Huomautukset** – katso, mitä tätä ehdokasta koskevia huomautuksia on annettu Attractissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-166">**Notes** – See any notes that have been entered for this candidate in Attract.</span></span>

    ![[<span data-ttu-id="2b021-167">Attract-tietojen tarkastelemien LinkedIn Recruiterissa</span><span class="sxs-lookup"><span data-stu-id="2b021-167">View Attract information from LinkedIn Recruiter</span></span>](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> <span data-ttu-id="2b021-168">Ehdokkaan ja hakemuksen tietoja ei synkronoida LinkedIn Recruiterin kanssa, jos ehdokas ei ole siirtynyt prospektivaiheesta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="2b021-168">Candidate and application data won't be synced with LinkedIn Recruiter if the candidate hasn't moved past the Prospect stage.</span></span>

## <a name="view-linkedin-talent-pools"></a><span data-ttu-id="2b021-169">LinkedInin kykypoolien näyttäminen</span><span class="sxs-lookup"><span data-stu-id="2b021-169">View LinkedIn talent pools</span></span>

<span data-ttu-id="2b021-170">Jos ehdokkaat hyväksyvät LinkedIn-profiiliinsa jakamisen organisaation käyttäjien kanssa, Attractiin luodaan uusi ehdokastietue.</span><span class="sxs-lookup"><span data-stu-id="2b021-170">If candidates agree to share their LinkedIn profiles with any user in your organization, a new candidate record is created in Attract.</span></span> <span data-ttu-id="2b021-171">Nämä ehdokkaat näkyvät sitten järjestelmän luomassa LinkedInin kykypoolissa.</span><span class="sxs-lookup"><span data-stu-id="2b021-171">These candidates then appear in a system-created LinkedIn talent pool.</span></span>

1. <span data-ttu-id="2b021-172">Valitse Attractissa vasemmalla **Kykypoolit**.</span><span class="sxs-lookup"><span data-stu-id="2b021-172">In Attract, select **Talent pools** on the left.</span></span>
2. <span data-ttu-id="2b021-173">Valitse LinkedInin kykypooli</span><span class="sxs-lookup"><span data-stu-id="2b021-173">Select the LinkedIn talent pool.</span></span> <span data-ttu-id="2b021-174">Näet luettelon ehdokkaista ja heidän LinkedInistä saadut tynkäprofiilit.</span><span class="sxs-lookup"><span data-stu-id="2b021-174">You will see a list of candidates and their stub profiles from LinkedIn.</span></span> <span data-ttu-id="2b021-175">Tynkäprofiilit sisältävät ehdokkaan etu- ja sukunimen sekä sähköpostiosoitteen, jos ehdokas on valinnut sen jakamisen.</span><span class="sxs-lookup"><span data-stu-id="2b021-175">Stub profiles contain the candidate's first and last names and email address, if the candidate chose to share it.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b021-176">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="2b021-176">See also</span></span>

[<span data-ttu-id="2b021-177">Attractin LinkedIn-integraation usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="2b021-177">Attract integration with LinkedIn FAQ</span></span>](./attract-linkedin-faq.md)

[<span data-ttu-id="2b021-178">Microsoft Dynamics 365 Talent – Attractin LinkedIn-integraation määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2b021-178">Set up integration with LinkedIn for Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-admin-linkedin.md)

[<span data-ttu-id="2b021-179">Työpaikkojen luominen, hyväksyminen ja julkaiseminen Attractissa</span><span class="sxs-lookup"><span data-stu-id="2b021-179">Create, approve, and post jobs in Attract</span></span>](./creating-jobs-attract.md)

[<span data-ttu-id="2b021-180">Työpaikkojen julkaiseminen LinkedInissä Microsoft Dynamics 365 Talent – Attractista</span><span class="sxs-lookup"><span data-stu-id="2b021-180">Post jobs to LinkedIn from Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-post-jobs-to-linkedin.md)

[<span data-ttu-id="2b021-181">LinkedInin ja Microsoft Dynamics 365 Talent – Attractin integroinnin vianmääritys</span><span class="sxs-lookup"><span data-stu-id="2b021-181">Troubleshooting integration with LinkedIn and Microsoft Dynamics 365 Talent - Attract</span></span>](./attract-troubleshoot-linkedin.md)
