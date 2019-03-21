---
title: Attractin urasivuston toiminnot
description: Tässä ohjeaineessa on Attractin ehdokkaalle tarkoitetun urasivustotoimintojen yleiskatsaus.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/13/2019
ms.locfileid: "389960"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="0fb4e-103">Attractin urasivuston toiminnot</span><span class="sxs-lookup"><span data-stu-id="0fb4e-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0fb4e-104">Tässä ohjeaineessa on Microsoft Dynamics 365 for Talent: Attractin ehdokkaalle tarkoitetun urasivustotoimintojen yleiskatsaus.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="0fb4e-105">Siinä käsitellään myös toiminnon määrittäminen.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="0fb4e-106">Attractissa on yksi urasivusto vuokraajan kullekin ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="0fb4e-107">Jos organisaatiossa on esimerkiksi kehitysympäristö ja testiympäristö, sekä kehitys- että testiympäristölle valmistellaan oma urasivusto.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="0fb4e-108">Kumpikin urasivusto on täysin eristetty ja kummassakin oma todennusmekanismi.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="0fb4e-109">Urasivustot eivät jaa töitä eivätkä hakijaprofiileja keskenään.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="0fb4e-110">Urasivusto on oletusarvoisesti julkinen.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-110">By default, the career site is public.</span></span> <span data-ttu-id="0fb4e-111">Niinpä hakijat voivat tarkastella kaikki ulkoiseksi merkittyjä töitä ilman kirjautumista.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="0fb4e-112">Kaikkia muita toimintoja varten hakijoiden on kuitenkin kirjauduttava sisään.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="0fb4e-113">Urasivuston hallinta</span><span class="sxs-lookup"><span data-stu-id="0fb4e-113">Career site management</span></span>

<span data-ttu-id="0fb4e-114">Voit määrittää seuraavat kohdat kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa (hammasrataskuvake) **Hallintakeskus** ja sitten **Yrityksen tiedot** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="0fb4e-115">**Organisaation nimi** – Organisaation nimi näkyy siirtymispalkissa urasivuston yläosassa.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="0fb4e-116">Valitsemalla organisaation nimet hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="0fb4e-117">**Organisaation logo** – Organisaation logo näkyy urasivuston vasemmassa yläkulmassa.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="0fb4e-118">Valitsemalla organisaation logon hakijat voivat siirtyä sivulle, jossa on luettelo avoimista työpaikoista.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="0fb4e-119">Urasivustossa näkyvän logon korkeus on aina 20 kuvapistettä (px).</span><span class="sxs-lookup"><span data-stu-id="0fb4e-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="0fb4e-120">Hallintakeskukseen lisätty kuva sovitetaan oikean kokoiseksi.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="0fb4e-121">Tämän vuoksi kuvan leveys voi muuttua.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="0fb4e-122">Voit määrittää seuraavat kohdat kirjautumalla järjestelmänvalvojana Attractiin ja valitsemalla ensin **Asetukset**-valikossa **Hallintakeskus** ja sitten **Urasivuston hallinta** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="0fb4e-123">**Hakukoneoptimointi** – Kun otettu käyttöön, kaikkia Attractin urasivustossa julkaistuja julkisia työpaikkoja voi hakea hakukoneilla, kuten Bingillä ja Googlella.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="0fb4e-124">Tämän asetuksen käyttöönottamisessa ja hakutulosten näkymisessä voi olla viive, joka määräytyy käytetyn hakukoneen mukaan.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="0fb4e-125">Urasivuston URL-osoitteet</span><span class="sxs-lookup"><span data-stu-id="0fb4e-125">Career site URLs</span></span>

<span data-ttu-id="0fb4e-126">Seuraavassa luettelossa on yleisesti käytettyjen urasivustojen URL-osoitteita ja ohjeita niiden käyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="0fb4e-127">**Urasivuston aloitussivun URL-osoite** – voit tarkastella urasivuston aloitussivun URL-osoitetta kirjautumalla Attractiin järjestelmänvalvojana, valitsemalla **Hallintakeskus** **Asetukset**-valikossa ja valitsemalla sitten **Urasivuston hallinta** -välilehden.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="0fb4e-128">**Yksittäisen työpaikkailmoituksen käyttämisen URL-osoite** – Kun [teet ulkoisen työpaikkailmoituksen](Creating-jobs-Attract.md#postings) ensimmäisen kerran, voit kopioida **Käytä**-linkin Attract-sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="0fb4e-129">Tämän linkin URL-osoitteen muoto on seuraavanlainen: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="0fb4e-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="0fb4e-130">**Yksittäisen työpaikkailmoituksen URL-osoite** – Työpaikkailmoituksen URL-osoite on käytön URL-osoitteen alimerkkijono.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="0fb4e-131">Se sisältää työnumerosta oikealle kaikki merkkijonon tiedot.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="0fb4e-132">Niinpä edellisessä Käytä-linkin URL-osoitteessa työpaikkailmoituksen URL-osoite on [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e).</span><span class="sxs-lookup"><span data-stu-id="0fb4e-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="0fb4e-133">Todennusasetukset</span><span class="sxs-lookup"><span data-stu-id="0fb4e-133">Authentication options</span></span>

<span data-ttu-id="0fb4e-134">Hakijat voivat kirjautua Attract-urasivustoon seuraavin tavoin:</span><span class="sxs-lookup"><span data-stu-id="0fb4e-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="0fb4e-135">Henkilökohtainen tili:</span><span class="sxs-lookup"><span data-stu-id="0fb4e-135">Personal account:</span></span>

    -   <span data-ttu-id="0fb4e-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="0fb4e-136">LinkedIn</span></span>

    -   <span data-ttu-id="0fb4e-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="0fb4e-137">Microsoft</span></span>

    -   <span data-ttu-id="0fb4e-138">Google</span><span class="sxs-lookup"><span data-stu-id="0fb4e-138">Google</span></span>

    -   <span data-ttu-id="0fb4e-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="0fb4e-139">Facebook</span></span>

-   <span data-ttu-id="0fb4e-140">Työ- tai opiskelijatili:</span><span class="sxs-lookup"><span data-stu-id="0fb4e-140">Work or school account:</span></span>

    -   <span data-ttu-id="0fb4e-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="0fb4e-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="0fb4e-142">Azure AD -kirjautuminen on tarkoitettu vain sisäisille hakijoille.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="0fb4e-143">Tämän vuoksi vain yrityksen Azure AD -tunnistetietoja käyttävät sisäiset hakijat voivat käyttää tätä vaihtoehtoa.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="0fb4e-144">Esimerkiksi hakija, joka on tällä hetkellä Contoso Ltd:n työntekijä, halua hakea töitä Alpine Ski Housesta, joka on erillinen yritys.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="0fb4e-145">Kirjautuminen ei tässä tapauksessa onnistu, jos työntekijä yrittää käyttää Contoso Ltd:n Azure AD -tunnistetietoja.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="0fb4e-146">Profiilin luominen ja ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="0fb4e-146">Create and maintain a profile</span></span>

<span data-ttu-id="0fb4e-147">Kun hakijat ovat kirjautuneet urasivustoon, he voivat luoda profiilin ja ylläpitää sitä valitsemalla sivun yläosan siirtymispalkissa **Oma profiili**.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="0fb4e-148">Profiili sisältää henkilötiedot, tietoja työkokemuksesta ja koulutuksesta sekä asiakirjoja, linkkejä ja tietoja osaamisalueista.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="0fb4e-149">Kun profiili on luotu, sen avulla voi hakea työpaikkoja, joista hakija on kiinnostunut.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="0fb4e-150">Lisäksi Attract voi suositella profiilien avulla hakijoille sopivia työpaikkoja.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="0fb4e-151">Jos hakija kirjautuu johonkin edellä mainittuun todennuspalveluun sähköpostitunnuksella, kyseinen sähköpostitunnus muuttuu oletusarvoisesti profiiliin liitetyksi yhteyshenkilön sähköpostitunnukseksi.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="0fb4e-152">Jälkimmäinen voidaan kuitenkin muuttaa ja on täysin erillinen edellisestä.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="0fb4e-153">Attract liittää aina profiilin kaikkeen sähköpostiviestintään yhteyshenkilön sähköpostitunnuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="0fb4e-154">Oikean työpaikan etsiminen</span><span class="sxs-lookup"><span data-stu-id="0fb4e-154">Find the right job</span></span>

<span data-ttu-id="0fb4e-155">Hakijat voivat hakea tiettyä työpaikkaa työluettelosivulla hakuehtojen avulla.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="0fb4e-156">Hakutoiminto hakee tiettyjä sanoja työnimikkeistä ja työnkuvauksista sekä näyttää sopivat työpaikat tuloksina.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="0fb4e-157">Hakijat voivat suodattaa tuloksia koska tahansa työn sijainnin tai työtehtävän perusteella.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="0fb4e-158">Hakijat voivat tarkastella urasivustossa myös suositeltuja työpaikkoja.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="0fb4e-159">Hakijalle suositellaan työpaikkoja hakijan aiempien hakemusten, profiilin ja ansioluetteloiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="0fb4e-160">Työpaikkasuositukset näytetään vain, jos urasivustossa on julkaista vähintään 10 työpaikkaa ja jos hakija on täyttänyt profiilitiedot.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="0fb4e-161">Työpaikkojen hakeminen</span><span class="sxs-lookup"><span data-stu-id="0fb4e-161">Apply for jobs</span></span>

<span data-ttu-id="0fb4e-162">Kun hakija löytää oikean työpaikan, sitä voi hakea **Työn tiedot** -sivun **Käytä**-painikkeella.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="0fb4e-163">Hakijat voivat tässä vaiheessa joko luoda uuden profiilin tai tarkistaa aiemmin luodun profiilin tiedot.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="0fb4e-164">Hakija voi myös tarvittaessa ladata ansioluettelon ja lähettää sitten työhakemuksen.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="0fb4e-165">Hakemuksen tilan tarkistaminen</span><span class="sxs-lookup"><span data-stu-id="0fb4e-165">Check application status</span></span>

<span data-ttu-id="0fb4e-166">Kun hakija on hakenut yhtä tai useaa työpaikkaa, hän voi tarkastella avoimia ja suljettuja hakemuksia valitsemalla sivun yläosan siirtymispalkissa **Hakemukset**.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="0fb4e-167">Kun hakija avaa jonkin hakemuksensa, näkyviin tulee hakemuksen nykyinen tila ja mahdolliset odottavat toiminnot, jotka hakijan on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="0fb4e-168">Jos hakijan on esimerkiksi annettava mahdolliset päivämäärät henkilökohtaista haastattelua varten, käytettävissä olevat vaihtoehdot näkyvät sivulla.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="0fb4e-169">Sisäiset työpaikat</span><span class="sxs-lookup"><span data-stu-id="0fb4e-169">Internal jobs</span></span>

<span data-ttu-id="0fb4e-170">Tällä hetkellä sisäisiksi merkityt Attractin urasivustoon julkaistut työt eivät näy urasivustossa.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="0fb4e-171">Niitä voi käyttää vain avaamalla suoran **Käytä**-linkin URL-osoitteen, joka voidaan kopioida Attract-sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="0fb4e-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
