---
title: Kyselylomakkeiden jakelu ja aikataulutus
description: Tässä artikkelissa kerrotaan, miten suunnittelemasi kyselylomakkeet jaetaan niin, että ne ovat oikean henkilön tai henkilöryhmän täytettävissä.
author: andreabichsel
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0329b80615eed6efcc22bb0b140970988f5c306a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429503"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="ccf75-103">Kyselylomakkeiden jakelu ja aikataulutus</span><span class="sxs-lookup"><span data-stu-id="ccf75-103">Distribute and schedule questionnaires</span></span>

<span data-ttu-id="ccf75-104">Tässä artikkelissa kerrotaan, miten suunnittelemasi kyselylomakkeet jaetaan niin, että ne ovat oikean henkilön tai henkilöryhmän täytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-104">This article explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="ccf75-105">Kyselylomakkeen voi jakaa seuraavilla tavoilla:</span><span class="sxs-lookup"><span data-stu-id="ccf75-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="ccf75-106">Merkitse kyselylomake aktiiviseksi.</span><span class="sxs-lookup"><span data-stu-id="ccf75-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="ccf75-107">Tämän jälkeen kyselylomake on kaikkien työntekijöiden käytettävässä, jos kyselylomakeryhmän määrityksissä ei ole valittu toisin.</span><span class="sxs-lookup"><span data-stu-id="ccf75-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="ccf75-108">Liitä käyttöoikeudet kyselylomakeryhmään.</span><span class="sxs-lookup"><span data-stu-id="ccf75-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="ccf75-109">Tämän jälkeen kyselylomake on valitun ryhmän jokaisen jäsenen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="ccf75-110">Luo suunniteltuja vastausistuntoja.</span><span class="sxs-lookup"><span data-stu-id="ccf75-110">Create planned answer sessions.</span></span> <span data-ttu-id="ccf75-111">Näin kyselylomake on vain tietyn henkilön käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="ccf75-112">Luo aikataulu.</span><span class="sxs-lookup"><span data-stu-id="ccf75-112">Create a schedule.</span></span> <span data-ttu-id="ccf75-113">Näin kyselylomake voi olla useiden henkilöiden käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="ccf75-114">Kyselylomakkeen merkitseminen aktiiviseksi</span><span class="sxs-lookup"><span data-stu-id="ccf75-114">Marking a questionnaire as active</span></span>

<span data-ttu-id="ccf75-115">Kun määrität **Aktiivinen**-kentän arvoksi **Kyllä** **Kyselylomakkeet**-sivulla, voit määrittää kyselylomakkeen kaikkien työntekijöiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ccf75-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="ccf75-116">Vastaajat voivat täyttää kyselylomakkeen useita kertoja.</span><span class="sxs-lookup"><span data-stu-id="ccf75-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="ccf75-117">Tämä toiminto on hyödyllinen, jos haluat kerätä palautetta koko vuoden ajan.</span><span class="sxs-lookup"><span data-stu-id="ccf75-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="ccf75-118">Voit luoda esimerkiksi kyselylomakkeen, jonka avulla työntekijät voivat antaa palautetta kahvilan lounaspalvelusta.</span><span class="sxs-lookup"><span data-stu-id="ccf75-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="ccf75-119">Kyselylomakeryhmät</span><span class="sxs-lookup"><span data-stu-id="ccf75-119">Questionnaire groups</span></span>

<span data-ttu-id="ccf75-120">Voit määrittää kyselylomakeryhmät ja lisätä vastaajat, joille kyselylomake jaetaan.</span><span class="sxs-lookup"><span data-stu-id="ccf75-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="ccf75-121">Voit luoda kyselylomakeryhmiä seuraavilta sivuilta:</span><span class="sxs-lookup"><span data-stu-id="ccf75-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="ccf75-122">**Kyselylomakeryhmät**– Vain kyselylomakeryhmään kuuluvat henkilöt voivat täyttää valitun kyselylomakkeen.</span><span class="sxs-lookup"><span data-stu-id="ccf75-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="ccf75-123">Jos kohdeyleisöksi on määritetty esimerkiksi alihankkijat, voit luoda juuri heille määritetyn kyselylomakeryhmän.</span><span class="sxs-lookup"><span data-stu-id="ccf75-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="ccf75-124">**Kyselylomakeryhmän jäsenet** – Voit lisätä kyselylomakeryhmiin henkilöitä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="ccf75-125">Liitä kyselylomakeryhmä kyselylomakkeeseen valitsemalla **Kyselylomakkeet**-sivulla **Käyttöoikeudet**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="ccf75-126">Kun kyselylomake on tallennettu aktiiviseksi, kyselylomakeryhmän jäsenet voivat täyttää kyselylomakkeen.</span><span class="sxs-lookup"><span data-stu-id="ccf75-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="ccf75-127">Tämä toiminto on hyödyllinen, jos haluat testata kyselylomakkeen valitulla ryhmällä henkilöitä, ennen kuin se lähetetään suuremmalle ryhmälle, tai jos haluat kohdistaa kyselylomakkeen tietylle yleisölle.</span><span class="sxs-lookup"><span data-stu-id="ccf75-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="ccf75-128">Kyselylomakkeen suunnitellut vastausistunnot</span><span class="sxs-lookup"><span data-stu-id="ccf75-128">Planned answer sessions in a questionnaire</span></span>

<span data-ttu-id="ccf75-129">Suunnitellut vastausistunnot ovat vastaajille suunniteltuja ja valittuja kyselylomakkeita.</span><span class="sxs-lookup"><span data-stu-id="ccf75-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> [!NOTE]
> <span data-ttu-id="ccf75-130">Kyselylomake on määritettävä ennen suunniteltujen vastausistuntojen määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-130">Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="ccf75-131">Luo suunniteltu vastausistunto yksittäiselle työntekijälle **Suunniteltu vastausistunto** -sivulla</span><span class="sxs-lookup"><span data-stu-id="ccf75-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="ccf75-132">Sivulla oleva luettelo sisältää kaikki suunnitellut kyselylomakkeet.</span><span class="sxs-lookup"><span data-stu-id="ccf75-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="ccf75-133">Suunniteltuja vastausistuntoja käytetään myös **Kyselylomakkeiden aikataulut** -sivulla, jolla voit suunnitella kyselylomakkeita useille ihmisille. Heitä ovat:</span><span class="sxs-lookup"><span data-stu-id="ccf75-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="ccf75-134">Työntekijät</span><span class="sxs-lookup"><span data-stu-id="ccf75-134">Employees</span></span>
-   <span data-ttu-id="ccf75-135">Kurssin osallistujat</span><span class="sxs-lookup"><span data-stu-id="ccf75-135">Course participants</span></span>
-   <span data-ttu-id="ccf75-136">organisaatioyksiköt</span><span class="sxs-lookup"><span data-stu-id="ccf75-136">Organizational units</span></span>

<span data-ttu-id="ccf75-137">Kukin henkilö voi vastata kyselylomakkeeseen vain kerran.</span><span class="sxs-lookup"><span data-stu-id="ccf75-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="ccf75-138">Kyselylomakkeen ajoittaminen</span><span class="sxs-lookup"><span data-stu-id="ccf75-138">Scheduling a questionnaire</span></span>

<span data-ttu-id="ccf75-139">Halutessasi voit aikatauluttaa kyselylomakkeen useille vastaajille.</span><span class="sxs-lookup"><span data-stu-id="ccf75-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="ccf75-140">Suunnittelutyypit</span><span class="sxs-lookup"><span data-stu-id="ccf75-140">Planning types</span></span>

<span data-ttu-id="ccf75-141">Suunnittelutyypit ovat pakollisia, jos haluat ajoittaa suunnitellut vastausistunnot useille vastaajille.</span><span class="sxs-lookup"><span data-stu-id="ccf75-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="ccf75-142">Suunnittelutyyppejä käytetään kyselylomakkeiden aikataulujen luokittelussa.</span><span class="sxs-lookup"><span data-stu-id="ccf75-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="ccf75-143">Voit ajoittaa kyselylomakkeita esimerkiksi seuraavia tarkoituksia varten:</span><span class="sxs-lookup"><span data-stu-id="ccf75-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="ccf75-144">Arviointi</span><span class="sxs-lookup"><span data-stu-id="ccf75-144">Evaluation</span></span>
-   <span data-ttu-id="ccf75-145">Kysely</span><span class="sxs-lookup"><span data-stu-id="ccf75-145">Survey</span></span>
-   <span data-ttu-id="ccf75-146">Testaaminen</span><span class="sxs-lookup"><span data-stu-id="ccf75-146">Testing</span></span>

<span data-ttu-id="ccf75-147">Voit määrittää kyselylomakkeen aikataulun suunnittelutyypit **Kyselylomakkeiden aikataulut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ccf75-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="ccf75-148">Kyselylomakkeen viitetyypit</span><span class="sxs-lookup"><span data-stu-id="ccf75-148">Reference types for questionnaire</span></span>

<span data-ttu-id="ccf75-149">Viitetyyppien avulla voit syöttää vastaajille ehdot, jotka valitsisit kyselylomakkeen ajoittamisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="ccf75-150">Määritä kyselylomakkeen viitetyypit **Viitetyypit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="ccf75-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="ccf75-151">Kukin viitetyyppi vastaa Microsoft Dynamics 365 Financen taulua.</span><span class="sxs-lookup"><span data-stu-id="ccf75-151">Each reference type corresponds to a table in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="ccf75-152">Voit määrittää kyselylomakkeen aikataulujen luomisen yhteydessä yksittäisiä tietueita tauluun tai tietuealueen. Tietueet tai tietuealue liitetään kyselylomakkeeseen.</span><span class="sxs-lookup"><span data-stu-id="ccf75-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="ccf75-153">Esimerkiksi Kurssit-taulussa voit määrittää kurssin, jota kyselylomake koskee.</span><span class="sxs-lookup"><span data-stu-id="ccf75-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="ccf75-154">Kun määrität Kurssit-taulun viitteen, osa **Kurssit**-sivun kentistä ja painikkeista ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="ccf75-155">Kyselylomakkeiden aikataulut</span><span class="sxs-lookup"><span data-stu-id="ccf75-155">Questionnaire schedules</span></span>

<span data-ttu-id="ccf75-156">Voit käyttää kyselylomakkeen ajoituksia luodessasi useita suunniteltuja vastausistuntoja käyttäjäryhmälle viitetyypin perusteella.</span><span class="sxs-lookup"><span data-stu-id="ccf75-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="ccf75-157">Luo aikataulu **Kyselylomakkeiden aikataulut** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="ccf75-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="ccf75-158">Luokittele aikataulu valitsemalla suunnittelutyyppi ja valitse myös viitetyyppi, jota käytetään suoritettaessa järjestelmäkysely tiettyjen käyttäjien osalta.</span><span class="sxs-lookup"><span data-stu-id="ccf75-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="ccf75-159">Jos määrität Kurssit-taulun arvoksi Viitetyyppi, voit valita tietyn kurssin **Viite**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="ccf75-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="ccf75-160">Valitse kyselylomake ja muut ehdot valitsemalla **Asetuksen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="ccf75-161">Määritä ehdoksi esimerkiksi opettajan nimi, jos kyselylomake koskee opettajan arviointia.</span><span class="sxs-lookup"><span data-stu-id="ccf75-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="ccf75-162">Kun asetuksen tiedot on syötetty, järjestelmä luo kyselyyn kuuluville käyttäjille suunnitellut vastausistunnot.</span><span class="sxs-lookup"><span data-stu-id="ccf75-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="ccf75-163">Voit tarkastella aikataulun vastausistuntoja **Suunnitellut vastausistunnot** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="ccf75-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="ccf75-164">Tämän jälkeen voit luoda lisää suunniteltuja vastausistuntoja manuaalisesti tai poistaa istuntoja, joihin ei ole vastattu.</span><span class="sxs-lookup"><span data-stu-id="ccf75-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="ccf75-165">Ota kyselylomake käyttöön liittyvien suunniteltujen vastausistuntojen käyttäjille valitsemalla **Toiminnot** &gt; **Käynnistä**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="ccf75-166">Voit tarkastella kyselylomakkeen vastauksia **Vastaukset**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="ccf75-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="ccf75-167">Voit myös kopioida kyselylomakkeen aikataulun asetuksia, suunniteltuja vastausistuntoja ja vastauksia uutta kyselylomakkeen aikataulua varten.</span><span class="sxs-lookup"><span data-stu-id="ccf75-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="ccf75-168">Käytettävissä olevista kyselylomakkeista ilmoittaminen vastaajille</span><span class="sxs-lookup"><span data-stu-id="ccf75-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="ccf75-169">Kun jaat kyselylomakkeen, sinun on ilmoitettava vastaajille, että kyselylomakkeet ovat heidän saatavillaan.</span><span class="sxs-lookup"><span data-stu-id="ccf75-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="ccf75-170">Suunnitellusta vastausistunnosta ilmoittaminen vastaajille</span><span class="sxs-lookup"><span data-stu-id="ccf75-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="ccf75-171">Jos käytössä on suunniteltu vastausistunto, henkilölle on ilmoitettava suoraan esimerkiksi puhelimitse tai sähköpostitse.</span><span class="sxs-lookup"><span data-stu-id="ccf75-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="ccf75-172">Aikataulusta ilmoittaminen vastaajille</span><span class="sxs-lookup"><span data-stu-id="ccf75-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="ccf75-173">**Kyselylomakkeiden aikataulut** -sivulla voidaan luoda ja lähettää sähköpostiviesti kaikille kyselylomakkeen vastaajille.</span><span class="sxs-lookup"><span data-stu-id="ccf75-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="ccf75-174">Syötä sähköpostiviestin teksti **Työntekijän itsepalvelun sähköpostiosoite** -välilehdessä. Kun ajoitus on aloitettu, luo ja lähetä sähköposti vastaajille valitsemalla **Toiminnot** &gt; **Lähetä sähköposti**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="ccf75-175">Vastaajat voivat sitten kirjautua sivustoon ja täyttää kyselylomakkeen.</span><span class="sxs-lookup"><span data-stu-id="ccf75-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> [!NOTE]
> <span data-ttu-id="ccf75-176">IT-järjestelmänvalvojan on annettava sähköpostiasetukset **Sähköpostiparametrit**-sivulla, ennen kuin tämä toiminto otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ccf75-176">Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="ccf75-177">Ajoitetun kyselyn päättäminen</span><span class="sxs-lookup"><span data-stu-id="ccf75-177">Ending a scheduled questionnaire</span></span>

<span data-ttu-id="ccf75-178">Voit lopettaa aikataulutetun kyselylomakkeen, kun kaikki vastaajat ovat tehneet vastausistuntonsa loppuun.</span><span class="sxs-lookup"><span data-stu-id="ccf75-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="ccf75-179">Kun ajoitettu kyselylomake lopetetaan, asetuksia ei enää voi kopioida uuteen aikatauluun.</span><span class="sxs-lookup"><span data-stu-id="ccf75-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> [!NOTE]
>   <span data-ttu-id="ccf75-180">Jos vähintään yksi vastaaja ei ole täyttänyt vastauslomaketta, mutta haluat siitä huolimatta lopettaa aikataulutuksen, poista vastaajat **Suunniteltu vastausistunto** -sivun luettelosta.</span><span class="sxs-lookup"><span data-stu-id="ccf75-180">If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="ccf75-181">Sen jälkeen voit lopettaa aikataulun.</span><span class="sxs-lookup"><span data-stu-id="ccf75-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="ccf75-182">Kyselylomakkeiden täyttäminen</span><span class="sxs-lookup"><span data-stu-id="ccf75-182">Completing questionnaires</span></span>

<span data-ttu-id="ccf75-183">Kun kyselylomake on suunniteltu ja jaettu, valitut vastaajat voivat täyttää sen.</span><span class="sxs-lookup"><span data-stu-id="ccf75-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="ccf75-184">Voit täyttää kyselylomakkeita kahdesta käytettävissäsi olevasta sijainnista:</span><span class="sxs-lookup"><span data-stu-id="ccf75-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="ccf75-185">Valitse siirtymisruudussa **Kyselylomakkeet** &gt; **Jaa** &gt; **Täydennä kyselylomake**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="ccf75-186">Valitse työntekijän itsepalvelussa **Täytettävät kyselylomakkeet**.</span><span class="sxs-lookup"><span data-stu-id="ccf75-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="ccf75-187">Kyselylomakkeet voidaan määrittää tietyille käyttäjille tai käyttäjäryhmille tai kaikille verkon käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="ccf75-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>


