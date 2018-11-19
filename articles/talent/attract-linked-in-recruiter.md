---
title: "LinkedIn Recruiterin käyttö hankinnassa"
description: "Tässä ohjeaiheessa käsitellään koneoppimisen käyttöä työpaikkojen ja niiden ehdokassuositusten hankkimisessa."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: fi-fi
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="e2b33-103">LinkedIn Recruiterin käyttö hankinnassa</span><span class="sxs-lookup"><span data-stu-id="e2b33-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="e2b33-104">LinkedIn on maailman suurin kykytietokanta. Se on myös usein ensisijainen järjestelmä, jonka avulla työhönottajat etsivät ehdokkaita, viestivät heidän kanssaan ja hankkivat ehdokkaita työpaikkoihin, joihin työhönottajat etsivät työntekijää.</span><span class="sxs-lookup"><span data-stu-id="e2b33-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="e2b33-105">LinkedIn Recruiterin ja Dynamics 365 for Talent: Attractin välinen integraatio helpottaa työhönottoa ja tietojen pitämistä synkronoituna kahden järjestelmän välillä.</span><span class="sxs-lookup"><span data-stu-id="e2b33-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="e2b33-106">LinkedIn Recruiterin ja Attractin väliseen integraatioon tarvitaan kattavan työhönottolaajennuksen ja LinkedIn Recruiterin käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="e2b33-107">LinkedIn Recruiterin ja Attractin yhteiskäytön määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e2b33-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="e2b33-108">LinkedIn Recruiter -toimintojen käyttö edellyttää, että Attract-esiintymään on määritetty sopimus- tai yritystasoiset käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="e2b33-109">Määritysprosessin suorittamista varten on tehtävät yhteistyötä sen käyttäjän kanssa, joka on LinkedIn Recruiter -sopimuksen järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="e2b33-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="e2b33-110">Määritä LinkedIn Recruiterin ja Attractin yhteiskäyttö seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b33-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="e2b33-111">Kirjaudu Attractiin järjestelmänvalvoja ja valitse **Järjestelmänvalvojan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="e2b33-112">Valitse vasemmassa ruudussa **LinkedIn-integrointi**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e2b33-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="e2b33-113">[![LinkedIn Recruiter -integroinnin aloittaminen Attractin hallintanäkymässä](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="e2b33-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="e2b33-114">Aloita asennus valitsemalla **Muodosta yhteys**. Noudata opastettua LinkedIn-kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="e2b33-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="e2b33-115">Jos käytössä on paikkoja useissa LinkedIn-sopimuksissa, valitse sopimus, jonka haluat yhdistää Attract-järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="e2b33-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="e2b33-116">Jos käytössä on paikka vain yhdessä LinkedIn-sopimuksessa, tämä vaihe on tarpeeton.</span><span class="sxs-lookup"><span data-stu-id="e2b33-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="e2b33-117">LinkedIn-pienoisohjelma latautuu nyt järjestelmänvalvojan asetuksiin, ja siinä on kuvassa näkyvät integraatiot.</span><span class="sxs-lookup"><span data-stu-id="e2b33-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="e2b33-118">Valitse **Recruiter System Connect** -kohdassa **Pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="e2b33-119">[![LinkedIn Recruiter -integrointipyyntö Attractin hallintanäkymässä](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e2b33-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="e2b33-120">Kun integrointia on pyydetty Attractista, näkyviin tulee, että **kumppani on valmis** ja että integrointi voidaan ottaa käyttöön **Recruiterin järjestelmänvalvojan asetuksissa**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="e2b33-121">Jos sivulla näkyy ilmoitus, jossa pyydetään **ilmoittamaan kumppanille**, odota muutama sekunti, valitse sitten **kumppanille ilmoittaminen** ja päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="e2b33-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="e2b33-122">Näkyvissä pitäisi nyt olla, että **kumppani on valmis**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="e2b33-123">[![Attractin hallintanäkymä ilmaisee, että Attractin pyynnöt on tehty](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e2b33-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="e2b33-124">Seuraavaa vaihetta varten tarvitaan LinkedIn Recruiter -sopimuksen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="e2b33-125">Kirjaudu LinkedIniin järjestelmänvalvojan tilillä ja valitse oikeassa yläkulmassa LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="e2b33-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="e2b33-126">Valitse näytön yläosan **Lisää**-valikossa **Järjestelmänvalvojan asetukset** ja valitse sitten **ATS**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e2b33-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="e2b33-127">Attract-järjestelmä on näkyvissä muutaman muun käyttöönotettavan vaihtoehdon ohella.</span><span class="sxs-lookup"><span data-stu-id="e2b33-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="e2b33-128">Jos haluat ottaa käyttöön vain yhden napsautuksen viennin **ATS:n ilmaisin**- tai **ATS:n profiilin pienoisohjelma** -kohdassa, valitse **Yritystason käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="e2b33-129">Jos haluat ottaa käyttöön kaikki yritystason käyttöoikeudet sekä InMail-historiatietojen, huomautusten historiatietojen ja InMailin tynkäprofiilin käyttöoikeudet, valitse **Sopimustason käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="e2b33-130">Ota valittu käyttöoikeustaso käyttöön LinkedIn Recruiterin **Järjestelmänvalvoja-ATS**-setuksissa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="e2b33-131">[![Attract-integroinnin käyttöönotto LinkedIn Recruiterin hallintanäkymässä](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e2b33-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="e2b33-132">Palaa Attractin järjestelmänvalvojan asetuksiin Attractin järjestelmänvalvojana ja valitse **LinkedIn-integrointi**-välilehti. LinkedIn-pienoisohjelmalataus pitäisi nyt näkyä siten, että **Käytössä**-tilassa on valittu käyttöoikeustaso käyttöönotettuna.</span><span class="sxs-lookup"><span data-stu-id="e2b33-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="e2b33-133">[![Valmis LinkedIn Recruiter -integrointi](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="e2b33-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="e2b33-134">LinkedIn Recruiterin toimintojen käyttäminen</span><span class="sxs-lookup"><span data-stu-id="e2b33-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="e2b33-135">Kun Attractin järjestelmänvalvoja on ottanut LinkedIn Recruiterin toiminnot käyttöön, työhön ottavat esimiehet ja työhönottajat voivat käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="e2b33-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="e2b33-136">Voit ottaa nämä toiminnot käyttöön, muodostamalla yhteyden LinkedIn-tiliin **käyttäjäasetuksissa**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="e2b33-137">Sen jälkeen kun sekä järjestelmänvalvojan että käyttäjän asetukset on yhdistetty, käytössä on useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e2b33-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="e2b33-138">ATS:n profiilin pienoisohjelma</span><span class="sxs-lookup"><span data-stu-id="e2b33-138">In-ATS profile widget</span></span>

<span data-ttu-id="e2b33-139">Voit tarkastella ehdokkaan LinkedIn-profiilia Attractissa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="e2b33-140">LinkedIn-pienoisohjelma näyttää hakijan profiilin, kun ATS-tiedot vastaavat käyttäjien LinkedIn-tietoja.</span><span class="sxs-lookup"><span data-stu-id="e2b33-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="e2b33-141">Voit tarkastella profiilia valitsemalla profiilin joko työstä tai kykypoolista.</span><span class="sxs-lookup"><span data-stu-id="e2b33-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="e2b33-142">Valitse ehdokkaan profiilissa **LinkedIn**-välilehti, jolloin pienoisohjelma latautuu.</span><span class="sxs-lookup"><span data-stu-id="e2b33-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="e2b33-143">Ilmaise profiilin pienoisohjelman avulla, jos vastine sopiva.</span><span class="sxs-lookup"><span data-stu-id="e2b33-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="e2b33-144">Jos se ei ole, etsi oikea henkilö.</span><span class="sxs-lookup"><span data-stu-id="e2b33-144">If it is not, find the correct person.</span></span> <span data-ttu-id="e2b33-145">Voit myös tallentaa ehdokkaan tällä sivulla LinkedIn Recruiter -projekteihin.</span><span class="sxs-lookup"><span data-stu-id="e2b33-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="e2b33-146">Yhden napsautuksen vienti</span><span class="sxs-lookup"><span data-stu-id="e2b33-146">1-click export</span></span> 

<span data-ttu-id="e2b33-147">Kun ehdokkaita haetaan LinkedInissä, voit viedä ehdokkaan yhdellä napsautuksella avoimiin työpaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="e2b33-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="e2b33-148">Tee vienti yhdellä napsautuksella seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e2b33-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="e2b33-149">Varmista ennen näiden vaiheiden suorittamista, että sinulle on määritetty työpaikan työhön ottavan esimiehen tai työhönottajan rooli ja että työpaikassa on **Potentiaalinen ehdokas** -vaihe.</span><span class="sxs-lookup"><span data-stu-id="e2b33-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="e2b33-150">Luo työpaikka, määritä soveltuvat roolit ja aktivoi työpaikka.</span><span class="sxs-lookup"><span data-stu-id="e2b33-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="e2b33-151">Kun työpaikka on aktivoitu, siirry LinkedIn Recruiteriin.</span><span class="sxs-lookup"><span data-stu-id="e2b33-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="e2b33-152">Etsi sopiva ehdokas ja siirry tämän profiiliin.</span><span class="sxs-lookup"><span data-stu-id="e2b33-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="e2b33-153">Etsi yhteyshenkilökortin työpaikan hakuruudun avulla työpaikka nimikkeen tai Attractissa aktivoidun työpaikan tunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e2b33-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="e2b33-154">Jos et löydä työpaikkaa, etsi oikea Attract-esiintymä valitsemalla **Vaihda ATS**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="e2b33-155">Kun työpaikka on valittu, valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="e2b33-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="e2b33-156">Attract noutaa nyt ehdokkaan.</span><span class="sxs-lookup"><span data-stu-id="e2b33-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="e2b33-157">Siirry Attractiin ja avaa vastaava työpaikka.</span><span class="sxs-lookup"><span data-stu-id="e2b33-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="e2b33-158">Juuri viety ehdokas löytyy nyt työpaikan **Potentiaalinen ehdokas** -vaiheesta.</span><span class="sxs-lookup"><span data-stu-id="e2b33-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="e2b33-159">ATS:n ilmaisin</span><span class="sxs-lookup"><span data-stu-id="e2b33-159">In-ATS indicator</span></span> 

<span data-ttu-id="e2b33-160">Voit seurata LinkedIn Recruiterin avulla, onko ehdokas hakenut organisaatiossa muita työpaikkoja, tarkastella, missä työhakemusten vaiheessa ehdokas on, sekä tarkastella Attractin palautetta ja kommentteja LinkedIn Recruiterissa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="e2b33-161">Avaa LinkedIn Recruiter ja etsi ehdokasprofiili.</span><span class="sxs-lookup"><span data-stu-id="e2b33-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="e2b33-162">Selaa hakijan profiilissa **ATS:ssä**-osaan.</span><span class="sxs-lookup"><span data-stu-id="e2b33-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="e2b33-163">Voit tarkastella pienoisohjelmalla kaikki ehdokkaan Attractissa olevia tietoja LinkedIn Recruiter -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="e2b33-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="e2b33-164">Valitse **Työpaikat ja tilat** -välilehti, jos haluat nähdä ehdokkaaseen liittyvät työpaikat, viimeisimmät tilat ja siirtymisen kussakin työpaikassa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="e2b33-165">Valitse **Haastattelun palaute** -välilehti, jos haluat nähdä palautteen, jonka haastattelijat ovat lähettäneet Attractissa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="e2b33-166">Valitse **Huomautukset**-välilehti, jos haluat nähdä kyseisestä hakijasta Attractissa olevat muistiinpanot.</span><span class="sxs-lookup"><span data-stu-id="e2b33-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="e2b33-167">InMail-historiatiedot</span><span class="sxs-lookup"><span data-stu-id="e2b33-167">InMail history</span></span>

<span data-ttu-id="e2b33-168">LinkedIn InMailin historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e2b33-169">Kun vaihtoehto on otettu käyttöön, voit tarkastella koko ehdokkaaseen liittyvää InMail-historiaa.</span><span class="sxs-lookup"><span data-stu-id="e2b33-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="e2b33-170">Voit tarkastella myös, kenellä muulla organisaatiossa on InMail-viestintää ehdokkaan kanssa. Et kuitenkaan voi tarkastella itse viestejä.</span><span class="sxs-lookup"><span data-stu-id="e2b33-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="e2b33-171">Voit tarkastella InMail-historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="e2b33-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="e2b33-172">Voit tarkastella InMail-historiatietoja vain, jos ehdokas on vastannut pyyntöösi ja valinnut profiilin jakamisen kanssasi LinkedInissä.</span><span class="sxs-lookup"><span data-stu-id="e2b33-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="e2b33-173">InMail-viestit synkronoidaan Attractin kanssa parin tunnin välein.</span><span class="sxs-lookup"><span data-stu-id="e2b33-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="e2b33-174">Huomautusten historiatiedot</span><span class="sxs-lookup"><span data-stu-id="e2b33-174">Notes history</span></span> 

<span data-ttu-id="e2b33-175">LinkedInin huomautusten historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e2b33-176">Kun tämä vaihtoehto on otettu käyttöön, voit tarkastella organisaation työhönottajien ehdokkaasta tekemiä huomautuksia.</span><span class="sxs-lookup"><span data-stu-id="e2b33-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="e2b33-177">Voit tarkastella huomautusten historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="e2b33-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="e2b33-178">Voit tarkastella kaikkia ehdokasta koskevia huomautuksia LinkedIn Recruiterista.</span><span class="sxs-lookup"><span data-stu-id="e2b33-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="e2b33-179">InMailin tynkäprofiili</span><span class="sxs-lookup"><span data-stu-id="e2b33-179">InMail stub profile</span></span>

<span data-ttu-id="e2b33-180">InMailin tynkäprofiili on käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e2b33-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e2b33-181">Jos ehdokkaat suostuvat jakamaan LinkedIn-profiilin kaikkien organisaation käyttäjien kanssa, voit seurata ehdokkaita Attractissa ja kullekin ehdokkaalle luodaan uusi ehdokastietue.</span><span class="sxs-lookup"><span data-stu-id="e2b33-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="e2b33-182">Voit tarkastella ehdokasluetteloa valitsemalla **Kykypoolit**. Näkyvissä on nyt järjestelmän luoma LinkedIn-kykypooli.</span><span class="sxs-lookup"><span data-stu-id="e2b33-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="e2b33-183">Kykypoolissa on luettelo ehdokkaista ja heidän LinkedInista vastaanotetut tynkäprofiilit, joissa näkyy ehdokkaan etu- ja sukunimi.</span><span class="sxs-lookup"><span data-stu-id="e2b33-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="e2b33-184">Ehdokkaan sähköpostitunnus on näkyvissä, jos ehdokas on valinnat sähköpostiosoitteen jakamisen.</span><span class="sxs-lookup"><span data-stu-id="e2b33-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

