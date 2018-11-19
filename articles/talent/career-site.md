---
title: Attractin urasivuston toiminnot
description: "Tässä artikkelissa on Microsoft Dynamics 365 for Talent - Attractin hakijalle suunnatun urasivuston toimintojen yleiskatsaus. Siinä käsitellään myös toiminnon määrittäminen."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: fi-fi
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="63e7b-104">Attractin urasivuston toiminnot</span><span class="sxs-lookup"><span data-stu-id="63e7b-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="63e7b-105">Tässä artikkelissa on Microsoft Dynamics 365 for Talent: Attractin hakijalle suunnatun urasivuston toimintojen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="63e7b-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="63e7b-106">Siinä käsitellään myös toiminnon määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="63e7b-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="63e7b-107">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="63e7b-107">Overview</span></span>

<span data-ttu-id="63e7b-108">Attractissa on yksi urasivusto vuokraajan kullekin ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="63e7b-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="63e7b-109">Jos organisaatiossa on esimerkiksi kehitysympäristö ja testiympäristö, sekä kehitys- että testiympäristölle valmistellaan oma urasivusto.</span><span class="sxs-lookup"><span data-stu-id="63e7b-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="63e7b-110">Kumpikin urasivusto on **täysin eristetty** ja kummassakin oma todennusmekanismi.</span><span class="sxs-lookup"><span data-stu-id="63e7b-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="63e7b-111">Urasivustot eivät jaa töitä ja hakijaprofiileja keskenään.</span><span class="sxs-lookup"><span data-stu-id="63e7b-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="63e7b-112">Urasivusto on oletusarvoisesti julkinen.</span><span class="sxs-lookup"><span data-stu-id="63e7b-112">By default, the career site is public.</span></span> <span data-ttu-id="63e7b-113">Niinpä hakijat voivat tarkastella kaikki ulkoiseksi merkittyjä töitä ilman kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="63e7b-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="63e7b-114">Kaikkia muita toimintoja varten hakijoiden on kuitenkin kirjauduttava sisään.</span><span class="sxs-lookup"><span data-stu-id="63e7b-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="63e7b-115">Urasivuston hallinta</span><span class="sxs-lookup"><span data-stu-id="63e7b-115">Career site management</span></span>

<span data-ttu-id="63e7b-116">Asetuksilla hallitaan seuraavia urasivuston kohteita:</span><span class="sxs-lookup"><span data-stu-id="63e7b-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="63e7b-117">**Organisaation nimi:** Organisaation nimi näkyy siirtymispalkissa urasivuston yläosassa.</span><span class="sxs-lookup"><span data-stu-id="63e7b-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="63e7b-118">Valitsemalla organisaation nimet hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.</span><span class="sxs-lookup"><span data-stu-id="63e7b-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="63e7b-119">**Organisaation logo:** Organisaation logo näkyy urasivuston vasemmassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="63e7b-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="63e7b-120">Valitsemalla organisaation logon hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.</span><span class="sxs-lookup"><span data-stu-id="63e7b-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="63e7b-121">Voit määrittää organisaation nimen ja logon arvot kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa (hammasrataskuvake) **Hallintakeskus** ja sitten **Yrityksen tiedot** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="63e7b-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="63e7b-122">Urasivustossa näkyvän logon korkeus on aina 20 kuvapistettä (px).</span><span class="sxs-lookup"><span data-stu-id="63e7b-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="63e7b-123">Hallintakeskukseen lisätty kuva sovitetaan oikean kokoiseksi.</span><span class="sxs-lookup"><span data-stu-id="63e7b-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="63e7b-124">Tämän vuoksi kuvan leveys voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="63e7b-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="63e7b-125">Urasivuston URL-osoite</span><span class="sxs-lookup"><span data-stu-id="63e7b-125">Career site URL</span></span>

<span data-ttu-id="63e7b-126">Kun [teet ulkoisen työpaikkailmoituksen](./Creating-jobs-Attract.md#postings) ensimmäisen kerran, voit kopioida **Käytä**-linkin Attract-sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="63e7b-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="63e7b-127">Tämän linkin URL-osoitteen muoto on seuraavanlainen: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="63e7b-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="63e7b-128">Urasivuston URL-osoite on **Käytä**-linkin URL-osoitteen alimerkkijono.</span><span class="sxs-lookup"><span data-stu-id="63e7b-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="63e7b-129">Se sisältää yrityksen nimestä oikealle kaikki merkkijonon tiedot.</span><span class="sxs-lookup"><span data-stu-id="63e7b-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="63e7b-130">Niinpä edellisessä **Käytä**-linkin URL-osoitteessa urasivuston URL-osoite on `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="63e7b-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="63e7b-131">Todennusasetukset</span><span class="sxs-lookup"><span data-stu-id="63e7b-131">Authentication options</span></span>

<span data-ttu-id="63e7b-132">Hakijat voivat kirjautua Attract-urasivustoon seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="63e7b-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="63e7b-133">Henkilökohtainen tili:</span><span class="sxs-lookup"><span data-stu-id="63e7b-133">Personal account:</span></span>

    - <span data-ttu-id="63e7b-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="63e7b-134">LinkedIn</span></span>
    - <span data-ttu-id="63e7b-135">Microsoft </span><span class="sxs-lookup"><span data-stu-id="63e7b-135">Microsoft</span></span>
    - <span data-ttu-id="63e7b-136">Google</span><span class="sxs-lookup"><span data-stu-id="63e7b-136">Google</span></span>
    - <span data-ttu-id="63e7b-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="63e7b-137">Facebook</span></span>

- <span data-ttu-id="63e7b-138">Työ- tai opiskelijatili:</span><span class="sxs-lookup"><span data-stu-id="63e7b-138">Work or school account:</span></span>

    - <span data-ttu-id="63e7b-139">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="63e7b-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="63e7b-140">Azure AD -kirjautuminen on tarkoitettu vain sisäisille hakijoille.</span><span class="sxs-lookup"><span data-stu-id="63e7b-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="63e7b-141">Tämän vuoksi vain yrityksen Azure AD -tunnistetietoja käyttävät sisäiset hakijat voivat käyttää tätä vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="63e7b-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="63e7b-142">Esimerkiksi hakija, joka on tällä hetkellä Contoso Ltd:n työntekijä, halua hakea töitä Alpine Ski Housesta, joka on erillinen yritys.</span><span class="sxs-lookup"><span data-stu-id="63e7b-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="63e7b-143">Kirjautuminen ei tässä tapauksessa onnistu, jos työntekijä yrittää käyttää Contoso Ltd:n Azure AD -tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="63e7b-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="63e7b-144">Profiilin luominen ja ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="63e7b-144">Create and maintain a profile</span></span>

<span data-ttu-id="63e7b-145">Kun hakijat ovat kirjautuneet urasivustoon, he voivat luoda profiilin ja ylläpitää sitä valitsemalla sivun yläosan siirtymispalkissa **Oma profiili**.</span><span class="sxs-lookup"><span data-stu-id="63e7b-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="63e7b-146">Profiili sisältää henkilötiedot, tietoja työkokemuksesta ja koulutuksesta sekä asiakirjoja, linkkejä ja tietoja osaamisalueista.</span><span class="sxs-lookup"><span data-stu-id="63e7b-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="63e7b-147">Kun profiili on luotu, sen avulla voi hakea työpaikkoja, joista hakija on kiinnostunut.</span><span class="sxs-lookup"><span data-stu-id="63e7b-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="63e7b-148">Lisäksi Attract voi suositella profiilien avulla hakijoille sopivia työpaikkoja.</span><span class="sxs-lookup"><span data-stu-id="63e7b-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="63e7b-149">Oikean työpaikan etsiminen</span><span class="sxs-lookup"><span data-stu-id="63e7b-149">Find the right job</span></span>

<span data-ttu-id="63e7b-150">Hakijat voivat hakea tiettyä työpaikkaa työluettelosivulla hakuehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="63e7b-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="63e7b-151">Hakutoiminto hakee tiettyjä sanoja työnimikkeistä ja työnkuvauksista sekä näyttää sopivat työpaikat tuloksina.</span><span class="sxs-lookup"><span data-stu-id="63e7b-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="63e7b-152">Hakijat voivat suodattaa tuloksia koska tahansa työn sijainnin tai työtehtävän perusteella.</span><span class="sxs-lookup"><span data-stu-id="63e7b-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="63e7b-153">Hakijat voivat tarkastella urasivustossa myös suositeltuja työpaikkoja.</span><span class="sxs-lookup"><span data-stu-id="63e7b-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="63e7b-154">Hakijalle suositellaan työpaikkoja hakijan aiempien hakemusten, profiilin ja ansioluetteloiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="63e7b-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="63e7b-155">Työpaikkasuositukset näytetään vain, jos urasivustossa on julkaista vähintään 10 työpaikkaa ja jos hakija on täyttänyt profiilitiedot.</span><span class="sxs-lookup"><span data-stu-id="63e7b-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="63e7b-156">Hae työtä</span><span class="sxs-lookup"><span data-stu-id="63e7b-156">Apply for jobs</span></span>

<span data-ttu-id="63e7b-157">Kun hakija löytää oikean työpaikan, sitä voi hakea työn tietosivun **Käytä**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="63e7b-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="63e7b-158">Hakijat voivat tässä vaiheessa joko luoda uuden profiilin tai tarkistaa aiemmin luodun profiilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="63e7b-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="63e7b-159">Hakija voi myös tarvittaessa ladata ansioluettelon ja lähettää sitten työhakemuksen.</span><span class="sxs-lookup"><span data-stu-id="63e7b-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="63e7b-160">Hakemuksen tilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="63e7b-160">Check application status</span></span>

<span data-ttu-id="63e7b-161">Kun hakija on hakenut yhtä tai useaa työpaikkaa, hän voi tarkastella avoimia ja suljettuja hakemuksia valitsemalla sivun yläosan siirtymispalkissa **Hakemukset**.</span><span class="sxs-lookup"><span data-stu-id="63e7b-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="63e7b-162">Kun hakija avaa jonkin hakemuksensa, näkyviin tulee hakemuksen nykyinen tila ja mahdolliset odottavat toiminnot, jotka hakijan on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="63e7b-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="63e7b-163">Jos hakijan on esimerkiksi annettava mahdolliset päivämäärät henkilökohtaista haastattelua varten, käytettävissä olevat vaihtoehdot näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="63e7b-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="63e7b-164">Sisäiset työpaikat</span><span class="sxs-lookup"><span data-stu-id="63e7b-164">Internal jobs</span></span>

<span data-ttu-id="63e7b-165">Tällä hetkellä sisäisiksi merkityt Attractin urasivustoon julkaistut työt eivät näy urasivustossa.</span><span class="sxs-lookup"><span data-stu-id="63e7b-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="63e7b-166">Niitä voi käyttää vain avaamalla suoran **Käytä**-linkin URL-osoitteen, joka voidaan kopioida Attract-sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="63e7b-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

