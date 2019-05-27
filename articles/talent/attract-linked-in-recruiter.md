---
title: Hankinta LinkedIn Recruiterin avulla
description: Tässä ohjeaiheessa käsitellään koneoppimisen käyttöä työpaikkojen ja niiden ehdokassuositusten hankkimisessa.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517860"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="e50a5-103">Hankinta LinkedIn Recruiterin avulla</span><span class="sxs-lookup"><span data-stu-id="e50a5-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="e50a5-104">LinkedIn on maailman suurin kykytietokanta. Se on myös usein ensisijainen järjestelmä, jonka avulla työhönottajat etsivät ehdokkaita, viestivät heidän kanssaan ja hankkivat ehdokkaita työpaikkoihin, joihin työhönottajat etsivät työntekijää.</span><span class="sxs-lookup"><span data-stu-id="e50a5-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="e50a5-105">LinkedIn Recruiterin ja Dynamics 365 for Talentin välinen integrointi: Attract helpottaa työhönottoa ja tietojen pitämistä synkronoituna kahden järjestelmän välillä.</span><span class="sxs-lookup"><span data-stu-id="e50a5-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="e50a5-106">LinkedIn Recruiterin ja Attractin väliseen integraatioon tarvitaan kattavan työhönottolaajennuksen ja LinkedIn Recruiterin käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="e50a5-107">LinkedIn Recruiterin määrittäminen Attractin kanssa</span><span class="sxs-lookup"><span data-stu-id="e50a5-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="e50a5-108">LinkedIn Recruiter -toimintojen käyttö edellyttää, että Attract-esiintymään on määritetty sopimus- tai yritystasoiset käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="e50a5-109">Määritysprosessin suorittamista varten on tehtävät yhteistyötä sen käyttäjän kanssa, joka on LinkedIn Recruiter -sopimuksen järjestelmänvalvoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="e50a5-110">Määritä LinkedIn Recruiterin ja Attractin yhteiskäyttö seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e50a5-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="e50a5-111">Kirjaudu Attractiin järjestelmänvalvoja ja valitse **Järjestelmänvalvojan asetukset**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="e50a5-112">Valitse vasemmassa ruudussa **LinkedIn-integrointi**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e50a5-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="e50a5-113">[![LinkedIn Recruiter -integroinnin aloittaminen Attractin hallintanäkymässä](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="e50a5-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="e50a5-114">Aloita asennus valitsemalla **Muodosta yhteys**. Noudata opastettua LinkedIn-kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="e50a5-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="e50a5-115">Jos käytössä on paikkoja useissa LinkedIn-sopimuksissa, valitse sopimus, jonka haluat yhdistää Attract-järjestelmään.</span><span class="sxs-lookup"><span data-stu-id="e50a5-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="e50a5-116">Jos käytössä on paikka vain yhdessä LinkedIn-sopimuksessa, tämä vaihe on tarpeeton.</span><span class="sxs-lookup"><span data-stu-id="e50a5-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="e50a5-117">LinkedIn-pienoisohjelma latautuu nyt järjestelmänvalvojan asetuksiin, ja siinä on kuvassa näkyvät integraatiot.</span><span class="sxs-lookup"><span data-stu-id="e50a5-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="e50a5-118">Valitse **Recruiter System Connect** -kohdassa **Pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="e50a5-119">[![LinkedIn Recruiter -integroinnin pyytäminen Attractin hallintanäkymässä](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e50a5-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="e50a5-120">Kun integrointia on pyydetty Attractista, näkyviin tulee, että **kumppani on valmis** ja että integrointi voidaan ottaa käyttöön **Recruiterin järjestelmänvalvojan asetuksissa**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="e50a5-121">Jos sivulla näkyy ilmoitus, jossa pyydetään **ilmoittamaan kumppanille**, odota muutama sekunti, valitse sitten **kumppanille ilmoittaminen** ja päivitä sivu.</span><span class="sxs-lookup"><span data-stu-id="e50a5-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="e50a5-122">Näkyvissä pitäisi nyt olla, että **kumppani on valmis**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="e50a5-123">[![Attractin hallintanäkymä ilmaisee, että Attractin pyynnöt on tehty](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e50a5-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="e50a5-124">Seuraavaa vaihetta varten tarvitaan LinkedIn Recruiter -sopimuksen järjestelmänvalvojan oikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="e50a5-125">Kirjaudu LinkedIniin järjestelmänvalvojan tilillä ja valitse oikeassa yläkulmassa LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="e50a5-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="e50a5-126">Valitse näytön yläosan **Lisää**-valikossa **Järjestelmänvalvojan asetukset** ja valitse sitten **ATS**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e50a5-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="e50a5-127">Attract-järjestelmä on näkyvissä muutaman muun käyttöönotettavan vaihtoehdon ohella.</span><span class="sxs-lookup"><span data-stu-id="e50a5-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="e50a5-128">Jos haluat ottaa käyttöön vain yhden napsautuksen viennin **ATS:n ilmaisin**- tai **ATS:n profiilin pienoisohjelma** -kohdassa, valitse **Yritystason käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="e50a5-129">Jos haluat ottaa käyttöön kaikki yritystason käyttöoikeudet sekä InMail -historiatietojen, huomautusten historiatietojen ja InMail tynkäprofiilin käyttöoikeudet, valitse **Sopimustason käyttöoikeus**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="e50a5-130">Ota valittu käyttöoikeustaso käyttöön LinkedIn Recruiterin **Järjestelmänvalvoja-ATS**-asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="e50a5-131">[![Attract-integroinnin käyttöönotto LinkedIn Recruiterin hallintanäkymässä](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="e50a5-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="e50a5-132">Palaa Attractin järjestelmänvalvojan asetuksiin Attractin järjestelmänvalvojana ja valitse **LinkedIn-integrointi**-välilehti. LinkedIn-pienoisohjelmalataus pitäisi nyt näkyä siten, että **Käytössä**-tilassa on valittu käyttöoikeustaso käyttöönotettuna.</span><span class="sxs-lookup"><span data-stu-id="e50a5-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="e50a5-133">[![LinkedIn Recruiterin integrointi valmis](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="e50a5-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="e50a5-134">Käytetään LinkedIn Recruiterin ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="e50a5-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="e50a5-135">Kun Attractin järjestelmänvalvoja on ottanut LinkedIn Recruiterin toiminnot käyttöön, työhön ottavat esimiehet ja työhönottajat voivat käyttää sitä.</span><span class="sxs-lookup"><span data-stu-id="e50a5-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="e50a5-136">Voit ottaa nämä toiminnot käyttöön, muodostamalla yhteyden LinkedIn-tiliin **käyttäjäasetuksissa**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="e50a5-137">Sen jälkeen kun sekä järjestelmänvalvojan että käyttäjän asetukset on yhdistetty, käytössä on useita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="e50a5-138">ATS:n profiilin pienoisohjelma</span><span class="sxs-lookup"><span data-stu-id="e50a5-138">In-ATS profile widget</span></span>

<span data-ttu-id="e50a5-139">Voit tarkastella ehdokkaan LinkedIn-profiilia Attractissa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="e50a5-140">LinkedIn-pienoisohjelma näyttää hakijan profiilin, kun ATS-tiedot vastaavat käyttäjien LinkedIn-tietoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="e50a5-141">Voit tarkastella profiilia valitsemalla profiilin joko työstä tai kykypoolista.</span><span class="sxs-lookup"><span data-stu-id="e50a5-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="e50a5-142">Valitse ehdokkaan profiilissa **LinkedIn**-välilehti, jolloin pienoisohjelma latautuu.</span><span class="sxs-lookup"><span data-stu-id="e50a5-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="e50a5-143">Voit myös tallentaa ehdokkaan tällä sivulla LinkedIn Recruiter -projekteihin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="e50a5-144">Jos LinkedIn löysi vastineen sähköpostin ja LinkedInin jäsentunnuksen perusteella (tarkka vastine), ehdokkaan profiili näytetään.</span><span class="sxs-lookup"><span data-stu-id="e50a5-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="e50a5-145">Käyttäjällä on edelleen mahdollisuus linkittää profiili tai poistaa profiilin linkitys.</span><span class="sxs-lookup"><span data-stu-id="e50a5-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="e50a5-146">Jos LinkedIn ei löydä ehdokasta sähköpostiosoitteen tai jäsentunnuksen perusteella, se näyttää luettelon mahdollisista ehdokkaista ehdokkaan nimen perusteella. Käyttäjä voi sitten valita heistä yhden ja linkittää profiilin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="e50a5-147">Jos LinkedIn ei löydä yhtään hakijaa nimen perusteella, se ilmoittaa, että yhtään vastinetta ei löytynyt.</span><span class="sxs-lookup"><span data-stu-id="e50a5-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="e50a5-148">Yhden napsautuksen vienti</span><span class="sxs-lookup"><span data-stu-id="e50a5-148">1-click export</span></span> 

<span data-ttu-id="e50a5-149">Kun ehdokkaita haetaan LinkedInissä, voit viedä ehdokkaan yhdellä napsautuksella avoimiin työpaikkoihin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="e50a5-150">Tee vienti yhdellä napsautuksella seuraavien ohjeiden mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e50a5-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="e50a5-151">Varmista ennen näiden vaiheiden suorittamista, että sinulle on määritetty työpaikan työhön ottavan esimiehen tai työhönottajan rooli ja että työpaikassa on **Potentiaalinen ehdokas** -vaihe.</span><span class="sxs-lookup"><span data-stu-id="e50a5-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="e50a5-152">Luo työpaikka, määritä soveltuvat roolit ja aktivoi työpaikka.</span><span class="sxs-lookup"><span data-stu-id="e50a5-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="e50a5-153">Kun työpaikka on aktivoitu, siirry LinkedIn Recruiteriin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="e50a5-154">Etsi sopiva ehdokas ja siirry tämän profiiliin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="e50a5-155">Etsi yhteyshenkilökortin työpaikan hakuruudun avulla työpaikka nimikkeen tai Attractissa aktivoidun työpaikan tunnuksen perusteella.</span><span class="sxs-lookup"><span data-stu-id="e50a5-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="e50a5-156">Jos et löydä työpaikkaa, etsi oikea Attract-esiintymä valitsemalla **Vaihda ATS**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="e50a5-157">Kun työpaikka on valittu, valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="e50a5-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="e50a5-158">Attract noutaa nyt ehdokkaan.</span><span class="sxs-lookup"><span data-stu-id="e50a5-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="e50a5-159">Siirry Attractiin ja avaa vastaava työpaikka.</span><span class="sxs-lookup"><span data-stu-id="e50a5-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="e50a5-160">Juuri viety ehdokas löytyy nyt työpaikan **Potentiaalinen ehdokas** -vaiheesta.</span><span class="sxs-lookup"><span data-stu-id="e50a5-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="e50a5-161">ATS:n ilmaisin</span><span class="sxs-lookup"><span data-stu-id="e50a5-161">In-ATS indicator</span></span> 

<span data-ttu-id="e50a5-162">Voit seurata LinkedIn Recruiterin avulla, onko ehdokas hakenut organisaatiossa muita työpaikkoja, tarkastella, missä työhakemusten vaiheessa ehdokas on, sekä tarkastella Attractin palautetta ja kommentteja LinkedIn Recruiterissa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="e50a5-163">Avaa LinkedIn Recruiter ja etsi ehdokasprofiili.</span><span class="sxs-lookup"><span data-stu-id="e50a5-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="e50a5-164">Selaa hakijan profiilissa **ATS:ssä**-osaan.</span><span class="sxs-lookup"><span data-stu-id="e50a5-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="e50a5-165">Voit tarkastella pienoisohjelmalla kaikki ehdokkaan Attractissa olevia tietoja LinkedIn Recruiter -näkymässä.</span><span class="sxs-lookup"><span data-stu-id="e50a5-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="e50a5-166">Valitse **Työpaikat ja tilat** -välilehti, jos haluat nähdä ehdokkaaseen liittyvät työpaikat, viimeisimmät tilat ja siirtymisen kussakin työpaikassa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="e50a5-167">Valitse **Haastattelun palaute** -välilehti, jos haluat nähdä palautteen, jonka haastattelijat ovat lähettäneet Attractissa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="e50a5-168">Valitse **Huomautukset**-välilehti, jos haluat nähdä kyseisestä hakijasta Attractissa olevat muistiinpanot.</span><span class="sxs-lookup"><span data-stu-id="e50a5-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="e50a5-169">Ehdokkaan ja hakemuksen tietoja ei synkronoida LinkedIn Recruiteriin, jos ehdokas ei ole siirtynyt prospektivaiheesta eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="e50a5-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="e50a5-170">InMailin historiatiedot</span><span class="sxs-lookup"><span data-stu-id="e50a5-170">InMail history</span></span>

<span data-ttu-id="e50a5-171">LinkedIn InMailin historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e50a5-172">Kun vaihtoehto on otettu käyttöön, voit tarkastella koko ehdokkaaseen liittyviä InMail-historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="e50a5-173">Voit tarkastella myös, kenellä muulla organisaatiossa on InMail-viestintää ehdokkaan kanssa. Et kuitenkaan voi tarkastella itse viestejä.</span><span class="sxs-lookup"><span data-stu-id="e50a5-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="e50a5-174">Voit tarkastella InMail-historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="e50a5-175">Voit tarkastella InMail-historiatietoja, jos olet käynyt keskustelun ehdokkaan kanssa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="e50a5-176">InMail-viestit synkronoidaan Attractin kanssa parin tunnin välein.</span><span class="sxs-lookup"><span data-stu-id="e50a5-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="e50a5-177">Huomautusten historiatiedot</span><span class="sxs-lookup"><span data-stu-id="e50a5-177">Notes history</span></span> 

<span data-ttu-id="e50a5-178">LinkedInin huomautusten historiatiedot ovat käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e50a5-179">Kun tämä vaihtoehto on otettu käyttöön, voit tarkastella organisaation työhönottajien ehdokkaasta tekemiä huomautuksia.</span><span class="sxs-lookup"><span data-stu-id="e50a5-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="e50a5-180">Voit tarkastella huomautusten historiatietoja valitsemalla ehdokkaan profiilissa **LinkedIn**-välilehden ja selaamalla sivun alareunaan tarkastelemaan historiatietoja.</span><span class="sxs-lookup"><span data-stu-id="e50a5-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="e50a5-181">Voit tarkastella kaikkia ehdokasta koskevia huomautuksia LinkedIn Recruiterista.</span><span class="sxs-lookup"><span data-stu-id="e50a5-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="e50a5-182">InMailin tynkäprofiili</span><span class="sxs-lookup"><span data-stu-id="e50a5-182">InMail stub profile</span></span>

<span data-ttu-id="e50a5-183">InMailin tynkäprofiili on käytettävissä, kun LinkedIn Recruiterissa on sopimustason käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="e50a5-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="e50a5-184">Jos ehdokkaat suostuvat jakamaan LinkedIn-profiilin kaikkien organisaation käyttäjien kanssa, voit seurata ehdokkaita Attractissa ja kullekin ehdokkaalle luodaan uusi ehdokastietue.</span><span class="sxs-lookup"><span data-stu-id="e50a5-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="e50a5-185">Voit tarkastella ehdokkaan sähköpostiosoitetta, jos ehdokkaalla on jo järjestelmässä sähköpostiosoite tai jos hän on jakanut osoitteensa työhönottajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="e50a5-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="e50a5-186">Voit tarkastella ehdokasluetteloa valitsemalla **Kykypoolit**. Näkyvissä on nyt järjestelmän luoma LinkedIn-kykypooli.</span><span class="sxs-lookup"><span data-stu-id="e50a5-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="e50a5-187">Kykypoolissa on luettelo ehdokkaista ja heidän LinkedInista vastaanotetut tynkäprofiilit, joissa näkyy ehdokkaan etu- ja sukunimi.</span><span class="sxs-lookup"><span data-stu-id="e50a5-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="e50a5-188">Ehdokkaan sähköpostitunnus on näkyvissä, jos ehdokas on valinnat sähköpostiosoitteen jakamisen.</span><span class="sxs-lookup"><span data-stu-id="e50a5-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
