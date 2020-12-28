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
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669165"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="7d02f-103">Ehdokkaiden työhönotto</span><span class="sxs-lookup"><span data-stu-id="7d02f-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="7d02f-104">Dynamics 365 Human Resources auttaa työhönottopyyntöjen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="7d02f-105">Sen avulla myös ehdokkaiden siirtäminen työntenkijöiksi sujuu saumattomasti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="7d02f-106">Jos organisaatiossa käytetään erillistä työhönottosovellusta, työhönottoprosessissa saatetaan suorittaa seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="7d02f-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="7d02f-107">Syötä rekrytointipyyntö Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="7d02f-108">Vastaanota ehdokkaiden suositukset työhönottosovelluksesta Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="7d02f-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="7d02f-109">Tee ehdokkaan hyväksymisprosessi valmiiksi Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="7d02f-110">Jos käytössä ei ole erillistä työhönottosovellusta, voit hallinnoida ehdokkaita Human Resourcesissa myös manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="7d02f-111">Jos olet järjestelmänvalvoja tai kehittäjä ja haluat integroida Human Resourcen kolmannen osapuolen työhönottosovellukseen, katso lisätietoja kohdasta [Common Data Service -integroinnin määrittäminen](hr-admin-integration-common-data-service.md) ja [Common Data Servicen virtuaalientiteettien määrittäminen](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="7d02f-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="7d02f-112">Voit myös etsiä työhönoton integrointisovelluksia [AppSourcesta](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="7d02f-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="7d02f-113">Saat lisätietoja LinkedIn Talent Hub -integroinnin esiversiotoiminnosta kohdasta [LinkedIn Talent Hub -integrointi](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="7d02f-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="7d02f-114">Ota työhönottopyynnöt käyttöön</span><span class="sxs-lookup"><span data-stu-id="7d02f-114">Enable recruiting requests</span></span>

<span data-ttu-id="7d02f-115">Jos hlauat lähettää työhönottopyyntöjä Human Resourcesissa, ota ensin toiminto käyttöön **Human resources -parametreissa**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="7d02f-116">Valitse **Henkilöstön hallinta** -työtilassa **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="7d02f-117">Valitse **Määritys**-kohdasta **Henkilöstöparametrit**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7d02f-118">Määritä **Yleistiedot**-välilehden **TYÖHÖNOTTO**-kohdan **Ota työhönottopyynnöt käyttöön** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![Ota työhönottopyynnöt käyttöön](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="7d02f-120">Työhönottopyynnön sijainnin lisääminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-120">Add a recruiting request location</span></span>

<span data-ttu-id="7d02f-121">Voit lisätä organisaation mahdolliset useat sijainnit, jotta pyytäjät voivat uuden valita rekrytoitavan henkilön työskentelysijainnin.</span><span class="sxs-lookup"><span data-stu-id="7d02f-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="7d02f-122">Sijainti sisällytetään työpaikkailmoitukseen.</span><span class="sxs-lookup"><span data-stu-id="7d02f-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="7d02f-123">Syötä hakupalkkiin **työhönottopyynnön sijainti**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="7d02f-124">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-124">Select **New**.</span></span>

3. <span data-ttu-id="7d02f-125">Syötä **Työhönottopyynnön sijainti** -kenttään sijainnin nimi.</span><span class="sxs-lookup"><span data-stu-id="7d02f-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![Työhönottopyynnön sijainnin lisääminen](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="7d02f-127">Syötä **Kuvaus**-kohtaan sijainnin kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7d02f-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="7d02f-128">Valitse **Sijainti**-kohdassa **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="7d02f-129">Jos **Uusi osoite** -ponnahdusikkuna tulee näkyviin, syötä sijainnin osoite.</span><span class="sxs-lookup"><span data-stu-id="7d02f-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![Anna osoite](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="7d02f-131">Syötä **Yhteyshenkilön tiedot** -kohtaan sijainnin yhtyshenkilön tiedot.</span><span class="sxs-lookup"><span data-stu-id="7d02f-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="7d02f-132">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="7d02f-133">Työhönottopyynnön lisääminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-133">Add a recruiting request</span></span>

<span data-ttu-id="7d02f-134">Esimiehet voivat lähettää työhönottopyyntöjä Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="7d02f-135">Jos käytät erillistä työhönottosovellusta, näiden vaiheiden suorittaminen lähettää työhönottopyynnön ja aloittaa työhönottoprosessin kyseisessä sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="7d02f-136">Muussa tapauksessa voit aloittaa oman sisäisen työhönotoprosessin työnkulun tämän menetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="7d02f-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="7d02f-137">Valitse **Työntekijän itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7d02f-138">Valitse **Oma ryhmä** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7d02f-139">Valitse **Työhönottopyyntö**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-139">Select  **Request to recruit**.</span></span>

   ![Työhönottopyynnön aloittaminen](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="7d02f-141">Täytä **Kuvaus**-, **Työ**- ja **Arvioitu alkamispäivämäärä** -kentät.</span><span class="sxs-lookup"><span data-stu-id="7d02f-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![Työhönottopyynnön suorittaminen](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="7d02f-143">Valitse **Jatka**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-143">Select **Continue**.</span></span> <span data-ttu-id="7d02f-144">Sijainnin työhönottopyyntö tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="7d02f-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="7d02f-145">Valitse **Yleistiedot**-kohtaan työhönottaja avattavasta **Työhönottaja**-luettelosta. Valitse sitten sijainti avattavasta **Työhönottopyynnön sijainti** -luettelosta.</span><span class="sxs-lookup"><span data-stu-id="7d02f-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="7d02f-146">Muuta **Työ**-kohdassa tarvittavat tiedot ja valitse **Luo tiedot työstä**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![Luo tiedot työstä](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="7d02f-148">Muut työhönottopyynnön kentät täytetään käyttämällä annetun työn oletustietoja.</span><span class="sxs-lookup"><span data-stu-id="7d02f-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="7d02f-149">Syötä **Ulkoinen kuvaus** -kenttään ulkoisen työn kuvaus.</span><span class="sxs-lookup"><span data-stu-id="7d02f-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="7d02f-150">Valitse **Toimet**-kohdassa **Lisää** ja valitse tämän työhönottopyynnön toimi.</span><span class="sxs-lookup"><span data-stu-id="7d02f-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![Toimen lisääminen](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="7d02f-152">Valitse **Taidot**-kentässä **Lisää** ja valitse sitten taito.</span><span class="sxs-lookup"><span data-stu-id="7d02f-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="7d02f-153">Valitse **Koulutusvaatimukset** -kohdassa **Lisää** ja valitse sitten avattavat **Koulutus**- ja **Koulutustaso**-luettelot.</span><span class="sxs-lookup"><span data-stu-id="7d02f-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![Lisävaatimusten lisääminen](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="7d02f-155">Lisää **Kommentti**-kohtaan tarvittavat kommentit.</span><span class="sxs-lookup"><span data-stu-id="7d02f-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="7d02f-156">Valitse **Kompensaatio**-kohdassa taso avattavasta **Taso**-luettelosta. Muuta sitten tarvittaessa **Alaraja**-, **Tarkistuspiste**- ja **Yläraja**-kohtaa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="7d02f-157">Kun työhönottopyyntö on valmis ja haluat aloittaa työhönottoprosessin, valitse valikkorivillä **Aktivoi**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![Työhönottopyynnön aktivoiminen](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="7d02f-159">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="7d02f-160">Työhönottopyyntöjen tarkasteleminen ja muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="7d02f-161">Tee seuraavasti, jos olet esimies ja haluat tarkastella omia pyyntöäsi:</span><span class="sxs-lookup"><span data-stu-id="7d02f-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="7d02f-162">Valitse **Työntekijän itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="7d02f-163">Valitse **Oma ryhmä** -välilehti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="7d02f-164">Valitse **Oman ryhmän tiedot** -kohdan **Työhönottopyynnöt**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![Valitse Työhönottopyynnöt-välilehti](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="7d02f-166">Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="7d02f-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="7d02f-167">Tee seuraavasti, jos olet HR-ammattilainen ja haluat tarkastella kaikkia työhönottopyyntöjä:</span><span class="sxs-lookup"><span data-stu-id="7d02f-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="7d02f-168">Valitse **Henkilöstöhallinto**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7d02f-169">Valitse **Työhönottopyynnöt**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-169">Select **Recruiting requests**.</span></span>

   ![Työhönottopyyntöjen tarkasteleminen henkilöstöhallinnossa](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="7d02f-171">Voit tarkastella tai muokata työhönottopyyntöä valitsemalla sen ruudukosta.</span><span class="sxs-lookup"><span data-stu-id="7d02f-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="7d02f-172">Ehdokasprofiilin lisääminen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="7d02f-173">Jos organisaatio on integroitu toiseen sovellukseen työhönottopyyntöjen hallintaa varten, työhönottopyynnöt lähetetään edelleen tähän sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="7d02f-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="7d02f-174">Työhönottosovellus lähettää tämän jälkeen ehdokkaan tiedot takaisin Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="7d02f-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="7d02f-175">Muussa tapauksessa voit seurata omia sisäisiä työhönottoprosesseja ja syöttää ehdokkaan tiedot manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="7d02f-176">Valitse **Henkilöstöhallinto**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="7d02f-177">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-177">Select **Links**.</span></span>

3. <span data-ttu-id="7d02f-178">Valitse **Työhönotto**-kohdassa **Ehdokkaat**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![Ehdokkaiden tarkasteleminen](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="7d02f-180">Voit lisätä ehdokkaan valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="7d02f-181">Jos haluat muokata aiemmin luotua ehdokasta, valitse ehdokas luettelosta ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="7d02f-182">Ehdokasprofiili tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="7d02f-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="7d02f-183">Syötä **Ehdokkaan yhteenveto** -kohtaan ehdokkaan tiedot tai muokkaa niitä.</span><span class="sxs-lookup"><span data-stu-id="7d02f-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="7d02f-184">**Valitse työhönottopyyntö** -kohdassa työhönottopyyntö, johon ehdokas linkitetään.</span><span class="sxs-lookup"><span data-stu-id="7d02f-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="7d02f-185">Täytä sitten soveltuvat **Arvioitu aloituspäivämäärä**-, **Työhön ottava esimies**-, **Toimi**- ja **Kuvaus**-kentät.</span><span class="sxs-lookup"><span data-stu-id="7d02f-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![Työhönottopyynnön linkki](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="7d02f-187">Täytä kaikki ne seuraavien alueiden tiedot, jotka haluat sisällyttää ehdokkaan tietueeseen:</span><span class="sxs-lookup"><span data-stu-id="7d02f-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="7d02f-188">**Huomautukset**</span><span class="sxs-lookup"><span data-stu-id="7d02f-188">**Comments**</span></span>
   - <span data-ttu-id="7d02f-189">**Ammattikokemus**</span><span class="sxs-lookup"><span data-stu-id="7d02f-189">**Professional experience**</span></span>
   - <span data-ttu-id="7d02f-190">**Yhteystiedot**</span><span class="sxs-lookup"><span data-stu-id="7d02f-190">**Contact information**</span></span>
   - <span data-ttu-id="7d02f-191">**Koulutus**</span><span class="sxs-lookup"><span data-stu-id="7d02f-191">**Education**</span></span>
   - <span data-ttu-id="7d02f-192">**Osaamisalueet**</span><span class="sxs-lookup"><span data-stu-id="7d02f-192">**Skills**</span></span>
   - <span data-ttu-id="7d02f-193">**Todistukset**</span><span class="sxs-lookup"><span data-stu-id="7d02f-193">**Certificates**</span></span>
   - <span data-ttu-id="7d02f-194">**Seulonnat**</span><span class="sxs-lookup"><span data-stu-id="7d02f-194">**Screenings**</span></span>

8. <span data-ttu-id="7d02f-195">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="7d02f-196">Ehdokkaan työhönotto</span><span class="sxs-lookup"><span data-stu-id="7d02f-196">Hire a candidate</span></span>

<span data-ttu-id="7d02f-197">Kun olet valmis ehdokkaan työhönottoa varten, siirrä ehdokas työntekijäksi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7d02f-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="7d02f-198">Valitse ehdokkaan lomakkeesta **Työhönotto**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-198">On the candidate form, select **Hire**.</span></span>

   ![Ehdokkaan työhönotto](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="7d02f-200">Täytä kaikki kentät **Palkkaa uusi työntekijä** -lomakkeen **Tiedot**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![Uuden työntekijän tietojen syöttäminen](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="7d02f-202">Tarkista **Position tiedot** -kohdan tiedot ja muuta niitä tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="7d02f-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="7d02f-203">Valitse **Perehdytyksen tarkistusluettelot** -kohdassa kyseisen työntekijän asiaankuuluvat perehdytyksen tarkistusluettelot.</span><span class="sxs-lookup"><span data-stu-id="7d02f-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="7d02f-204">Valitse **Jatka**, jos haluat luoda työntekijätietueen.</span><span class="sxs-lookup"><span data-stu-id="7d02f-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="7d02f-205">Organisaation työnkuluista riippuen ehdokkaan tietue voi siirtyä lisähyväksyntävaiheisiin ennen työntekijätietueeksi muuttamista.</span><span class="sxs-lookup"><span data-stu-id="7d02f-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="7d02f-206">Päätös olla ottamatta ehdokasta töihin</span><span class="sxs-lookup"><span data-stu-id="7d02f-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="7d02f-207">Jos päätät olla ottamatta ehdokasta töihin, noudata näitä toimintoja ja poista tämä ennakkotarkistusprosessista.</span><span class="sxs-lookup"><span data-stu-id="7d02f-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="7d02f-208">Valitse ehdokkaan lomakkeessa **Älä ota töihin** -kohta.</span><span class="sxs-lookup"><span data-stu-id="7d02f-208">On the candidate form, select **Do not hire**.</span></span>

   ![Ehdokkaan työhönoton peruminen](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="7d02f-210">Valitse **Syykoodi** ja lisää mahdolliset kommentit.</span><span class="sxs-lookup"><span data-stu-id="7d02f-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="7d02f-211">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d02f-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="7d02f-212">Ehdokkaan hylkääminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-212">Dismiss a candidate</span></span>

<span data-ttu-id="7d02f-213">Tarvittaessa voit hylätä ehdokkaan työhönoton jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7d02f-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="7d02f-214">Ehdokas voi esimerkiksi hylätä tarjouksen tai jättää tulematta töihin ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="7d02f-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="7d02f-215">Valitse ehdokkaan lomakkeessa **Hylkää ehdokas** -kohta.</span><span class="sxs-lookup"><span data-stu-id="7d02f-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![Hylkää ehdokas](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="7d02f-217">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="7d02f-217">See also</span></span>

[<span data-ttu-id="7d02f-218">Common Data Service -virtuaaliyksiköiden määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="7d02f-219">Työvoimasi organisointi</span><span class="sxs-lookup"><span data-stu-id="7d02f-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="7d02f-220">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7d02f-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)