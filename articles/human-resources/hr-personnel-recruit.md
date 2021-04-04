---
title: Ehdokkaiden työhönotto
description: Tässä aiheessa kerrotaan, miten ehdokkaiden työhönotto tehdään Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478281"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="3454c-103">Ehdokkaiden työhönotto</span><span class="sxs-lookup"><span data-stu-id="3454c-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3454c-104">Dynamics 365 Human Resources auttaa työhönottopyyntöjen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="3454c-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="3454c-105">Sen avulla myös ehdokkaiden siirtäminen työntenkijöiksi sujuu saumattomasti.</span><span class="sxs-lookup"><span data-stu-id="3454c-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="3454c-106">Jos organisaatiossa käytetään erillistä työhönottosovellusta, työhönottoprosessissa saatetaan suorittaa seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="3454c-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="3454c-107">Syötä rekrytointipyyntö Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3454c-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="3454c-108">Vastaanota ehdokkaiden suositukset työhönottosovelluksesta Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="3454c-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="3454c-109">Tee ehdokkaan hyväksymisprosessi valmiiksi Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="3454c-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="3454c-110">Jos käytössä ei ole erillistä työhönottosovellusta, voit hallinnoida ehdokkaita Human Resourcesissa myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="3454c-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="3454c-111">Jos olet järjestelmänvalvoja tai kehittäjä ja haluat integroida Human Resourcen kolmannen osapuolen työhönottosovellukseen, katso lisätietoja kohdasta [Dataverse -integroinnin määrittäminen](hr-admin-integration-common-data-service.md) ja [Dataversen virtuaalitaulukoiden määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="3454c-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="3454c-112">Voit myös etsiä työhönoton integrointisovelluksia [AppSourcesta](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="3454c-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="3454c-113">Saat lisätietoja LinkedIn Talent Hub -integroinnin esiversiotoiminnosta kohdasta [LinkedIn Talent Hub -integrointi](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="3454c-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="3454c-114">Ota työhönottopyynnöt käyttöön</span><span class="sxs-lookup"><span data-stu-id="3454c-114">Enable recruiting requests</span></span>

<span data-ttu-id="3454c-115">Jos haluat lähettää työhönottopyyntöjä Human Resourcesissa, ota ensin toiminto käyttöön kohdassa **Human Resourcesin jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3454c-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="3454c-116">Valitse **Henkilöstön hallinta** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="3454c-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="3454c-117">Valitse **Määritys**-kohdasta **Human resourcesin jaetut parametrit**.</span><span class="sxs-lookup"><span data-stu-id="3454c-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="3454c-118">Määritä **Työhönotto**-välilehden **TYÖHÖNOTTO**-kohdan **Ota työhönottopyynnöt käyttöön** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="3454c-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="3454c-119">Työhönottopyynnön sijainnin lisääminen</span><span class="sxs-lookup"><span data-stu-id="3454c-119">Add a recruiting request location</span></span>

<span data-ttu-id="3454c-120">Voit lisätä organisaation mahdolliset useat sijainnit, jotta pyytäjät voivat uuden valita rekrytoitavan henkilön työskentelysijainnin.</span><span class="sxs-lookup"><span data-stu-id="3454c-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="3454c-121">Sijainti sisällytetään työpaikkailmoitukseen.</span><span class="sxs-lookup"><span data-stu-id="3454c-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="3454c-122">Syötä hakupalkkiin **työhönottopyynnön sijainti**.</span><span class="sxs-lookup"><span data-stu-id="3454c-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="3454c-123">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3454c-123">Select **New**.</span></span>

3. <span data-ttu-id="3454c-124">Syötä **Työhönottopyynnön sijainti** -kenttään sijainnin nimi.</span><span class="sxs-lookup"><span data-stu-id="3454c-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Työhönottopyynnön sijainnin lisääminen](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="3454c-126">Syötä **Kuvaus**-kohtaan sijainnin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3454c-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="3454c-127">Valitse **Sijainti**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="3454c-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="3454c-128">Jos **Uusi osoite** -ponnahdusikkuna tulee näkyviin, syötä sijainnin osoite.</span><span class="sxs-lookup"><span data-stu-id="3454c-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Anna osoite](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="3454c-130">Syötä **Yhteyshenkilön tiedot** -kohtaan sijainnin yhtyshenkilön tiedot.</span><span class="sxs-lookup"><span data-stu-id="3454c-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="3454c-131">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3454c-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="3454c-132">Työhönottopyynnön lisääminen</span><span class="sxs-lookup"><span data-stu-id="3454c-132">Add a recruiting request</span></span>

<span data-ttu-id="3454c-133">Esimiehet voivat lähettää työhönottopyyntöjä Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="3454c-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="3454c-134">Jos käytät erillistä työhönottosovellusta, näiden vaiheiden suorittaminen lähettää työhönottopyynnön ja aloittaa työhönottoprosessin kyseisessä sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="3454c-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="3454c-135">Muussa tapauksessa voit aloittaa oman sisäisen työhönotoprosessin työnkulun tämän menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="3454c-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="3454c-136">Valitse **Työntekijän itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="3454c-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="3454c-137">Valitse **Oma ryhmä** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="3454c-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="3454c-138">Valitse **Työhönottopyyntö**.</span><span class="sxs-lookup"><span data-stu-id="3454c-138">Select  **Request to recruit**.</span></span>

   ![Työhönottopyynnön aloittaminen](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="3454c-140">Täytä **Kuvaus**-, **Työ**- ja **Arvioitu alkamispäivämäärä** -kentät.</span><span class="sxs-lookup"><span data-stu-id="3454c-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Työhönottopyynnön suorittaminen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="3454c-142">Valitse **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="3454c-142">Select **Continue**.</span></span> <span data-ttu-id="3454c-143">Sijainnin työhönottopyyntö tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="3454c-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="3454c-144">Valitse **Yleistiedot**-kohtaan työhönottaja avattavasta **Työhönottaja**-luettelosta. Valitse sitten sijainti avattavasta **Työhönottopyynnön sijainti** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="3454c-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="3454c-145">Muuta **Työ**-kohdassa tarvittavat tiedot ja valitse **Luo tiedot työstä**.</span><span class="sxs-lookup"><span data-stu-id="3454c-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Luo tiedot työstä](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="3454c-147">Muut työhönottopyynnön kentät täytetään käyttämällä annetun työn oletustietoja.</span><span class="sxs-lookup"><span data-stu-id="3454c-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="3454c-148">Syötä **Ulkoinen kuvaus** -kenttään ulkoisen työn kuvaus.</span><span class="sxs-lookup"><span data-stu-id="3454c-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="3454c-149">Valitse **Toimet**-kohdassa **Lisää** ja valitse tämän työhönottopyynnön toimi.</span><span class="sxs-lookup"><span data-stu-id="3454c-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Toimen lisääminen](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="3454c-151">Valitse **Taidot**-kentässä **Lisää** ja valitse sitten taito.</span><span class="sxs-lookup"><span data-stu-id="3454c-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="3454c-152">Valitse **Koulutusvaatimukset** -kohdassa **Lisää** ja valitse sitten avattavat **Koulutus**- ja **Koulutustaso**-luettelot.</span><span class="sxs-lookup"><span data-stu-id="3454c-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Lisävaatimusten lisääminen](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="3454c-154">Lisää **Kommentti**-kohtaan tarvittavat kommentit.</span><span class="sxs-lookup"><span data-stu-id="3454c-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="3454c-155">Valitse **Kompensaatio**-kohdassa taso avattavasta **Taso**-luettelosta. Muuta sitten tarvittaessa **Alaraja**-, **Tarkistuspiste**- ja **Yläraja**-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="3454c-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="3454c-156">Kun työhönottopyyntö on valmis ja haluat aloittaa työhönottoprosessin, valitse valikkorivillä **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="3454c-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Työhönottopyynnön aktivoiminen](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="3454c-158">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3454c-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="3454c-159">Työhönottopyyntöjen tarkasteleminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="3454c-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="3454c-160">Tee seuraavasti, jos olet esimies ja haluat tarkastella omia pyyntöäsi:</span><span class="sxs-lookup"><span data-stu-id="3454c-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="3454c-161">Valitse **Työntekijän itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="3454c-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="3454c-162">Valitse **Oma ryhmä** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="3454c-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="3454c-163">Valitse **Oman ryhmän tiedot** -kohdan **Työhönottopyynnöt**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3454c-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Valitse Työhönottopyynnöt-välilehti](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="3454c-165">Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="3454c-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="3454c-166">Tee seuraavasti, jos olet HR-ammattilainen ja haluat tarkastella kaikkia työhönottopyyntöjä:</span><span class="sxs-lookup"><span data-stu-id="3454c-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="3454c-167">Valitse **Henkilöstöhallinto**.</span><span class="sxs-lookup"><span data-stu-id="3454c-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="3454c-168">Valitse **Työhönottopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="3454c-168">Select **Recruiting requests**.</span></span>

   ![Työhönottopyyntöjen tarkasteleminen henkilöstöhallinnossa](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="3454c-170">Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="3454c-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="3454c-171">Ehdokasprofiilin lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="3454c-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="3454c-172">Jos organisaatio on integroitu toiseen sovellukseen työhönottopyyntöjen hallintaa varten, työhönottopyynnöt lähetetään edelleen tähän sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="3454c-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="3454c-173">Työhönottosovellus lähettää tämän jälkeen ehdokkaan tiedot takaisin Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="3454c-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="3454c-174">Muussa tapauksessa voit seurata omia sisäisiä työhönottoprosesseja ja syöttää ehdokkaan tiedot manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="3454c-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="3454c-175">Valitse **Henkilöstöhallinto**.</span><span class="sxs-lookup"><span data-stu-id="3454c-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="3454c-176">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="3454c-176">Select **Links**.</span></span>

3. <span data-ttu-id="3454c-177">Valitse **Työhönotto**-kohdassa **Ehdokkaat**.</span><span class="sxs-lookup"><span data-stu-id="3454c-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![Ehdokkaiden tarkasteleminen](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="3454c-179">Voit lisätä ehdokkaan valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="3454c-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="3454c-180">Jos haluat muokata aiemmin luotua ehdokasta, valitse ehdokas luettelosta ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="3454c-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="3454c-181">Ehdokasprofiili tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="3454c-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="3454c-182">Syötä **Ehdokkaan yhteenveto** -kohtaan ehdokkaan tiedot tai muokkaa niitä.</span><span class="sxs-lookup"><span data-stu-id="3454c-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="3454c-183">**Valitse työhönottopyyntö** -kohdassa työhönottopyyntö, johon ehdokas linkitetään.</span><span class="sxs-lookup"><span data-stu-id="3454c-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="3454c-184">Täytä sitten soveltuvat **Arvioitu aloituspäivämäärä**-, **Työhön ottava esimies**-, **Toimi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="3454c-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Työhönottopyynnön linkki](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="3454c-186">Täytä kaikki ne seuraavien alueiden tiedot, jotka haluat sisällyttää ehdokkaan tietueeseen:</span><span class="sxs-lookup"><span data-stu-id="3454c-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="3454c-187">**Huomautukset**</span><span class="sxs-lookup"><span data-stu-id="3454c-187">**Comments**</span></span>
   - <span data-ttu-id="3454c-188">**Ammattikokemus**</span><span class="sxs-lookup"><span data-stu-id="3454c-188">**Professional experience**</span></span>
   - <span data-ttu-id="3454c-189">**Yhteystiedot**</span><span class="sxs-lookup"><span data-stu-id="3454c-189">**Contact information**</span></span>
   - <span data-ttu-id="3454c-190">**Koulutus**</span><span class="sxs-lookup"><span data-stu-id="3454c-190">**Education**</span></span>
   - <span data-ttu-id="3454c-191">**Osaamisalueet**</span><span class="sxs-lookup"><span data-stu-id="3454c-191">**Skills**</span></span>
   - <span data-ttu-id="3454c-192">**Todistukset**</span><span class="sxs-lookup"><span data-stu-id="3454c-192">**Certificates**</span></span>
   - <span data-ttu-id="3454c-193">**Seulonnat**</span><span class="sxs-lookup"><span data-stu-id="3454c-193">**Screenings**</span></span>

8. <span data-ttu-id="3454c-194">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="3454c-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="3454c-195">Ehdokkaan työhönotto</span><span class="sxs-lookup"><span data-stu-id="3454c-195">Hire a candidate</span></span>

<span data-ttu-id="3454c-196">Kun olet valmis ehdokkaan työhönottoa varten, siirrä ehdokas työntekijäksi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="3454c-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="3454c-197">Valitse ehdokkaan lomakkeesta **Työhönotto**.</span><span class="sxs-lookup"><span data-stu-id="3454c-197">On the candidate form, select **Hire**.</span></span>

   ![Ehdokkaan työhönotto](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="3454c-199">Täytä kaikki kentät **Palkkaa uusi työntekijä** -lomakkeen **Tiedot**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="3454c-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Uuden työntekijän tietojen syöttäminen](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="3454c-201">Tarkista **Position tiedot** -kohdan tiedot ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="3454c-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="3454c-202">Valitse **Perehdytyksen tarkistusluettelot** -kohdassa kyseisen työntekijän asiaankuuluvat perehdytyksen tarkistusluettelot.</span><span class="sxs-lookup"><span data-stu-id="3454c-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="3454c-203">Valitse **Jatka**, jos haluat luoda työntekijätietueen.</span><span class="sxs-lookup"><span data-stu-id="3454c-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="3454c-204">Organisaation työnkuluista riippuen ehdokkaan tietue voi siirtyä lisähyväksyntävaiheisiin ennen työntekijätietueeksi muuttamista.</span><span class="sxs-lookup"><span data-stu-id="3454c-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="3454c-205">Päätös olla ottamatta ehdokasta töihin</span><span class="sxs-lookup"><span data-stu-id="3454c-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="3454c-206">Jos päätät olla ottamatta ehdokasta töihin, noudata näitä toimintoja ja poista tämä ennakkotarkistusprosessista.</span><span class="sxs-lookup"><span data-stu-id="3454c-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="3454c-207">Valitse ehdokkaan lomakkeessa **Älä ota töihin** -kohta.</span><span class="sxs-lookup"><span data-stu-id="3454c-207">On the candidate form, select **Do not hire**.</span></span>

   ![Ehdokkaan työhönoton peruminen](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="3454c-209">Valitse **Syykoodi** ja lisää mahdolliset kommentit.</span><span class="sxs-lookup"><span data-stu-id="3454c-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="3454c-210">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="3454c-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="3454c-211">Ehdokkaan hylkääminen</span><span class="sxs-lookup"><span data-stu-id="3454c-211">Dismiss a candidate</span></span>

<span data-ttu-id="3454c-212">Tarvittaessa voit hylätä ehdokkaan työhönoton jälkeen.</span><span class="sxs-lookup"><span data-stu-id="3454c-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="3454c-213">Ehdokas voi esimerkiksi hylätä tarjouksen tai jättää tulematta töihin ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="3454c-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="3454c-214">Valitse ehdokkaan lomakkeessa **Hylkää ehdokas** -kohta.</span><span class="sxs-lookup"><span data-stu-id="3454c-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Hylkää ehdokas](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="3454c-216">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3454c-216">See also</span></span>

[<span data-ttu-id="3454c-217">Määritä Dataverse -virtuaalitaulukot</span><span class="sxs-lookup"><span data-stu-id="3454c-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="3454c-218">Työvoimasi organisointi</span><span class="sxs-lookup"><span data-stu-id="3454c-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="3454c-219">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="3454c-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
