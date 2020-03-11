---
title: Kyselylomakkeiden jakaminen aikatauluttamalla
description: Kyselylomakkeiden ajoituksen avulla voit suunnitella ja jakaa kyselylomakkeita useille vastaajille.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0448a7ebe802a961c8c1296ef57d12ea22e4ec27
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008907"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="21207-103">Kyselylomakkeiden jakaminen aikatauluttamalla</span><span class="sxs-lookup"><span data-stu-id="21207-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="21207-104">Kyselylomakkeiden ajoituksen avulla voit suunnitella ja jakaa kyselylomakkeita useille vastaajille.</span><span class="sxs-lookup"><span data-stu-id="21207-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="21207-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="21207-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="21207-106">Kyselylomakkeen aikataulun luominen</span><span class="sxs-lookup"><span data-stu-id="21207-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="21207-107">Siirry kohtaan Kyselylomake > Jaa > Kyselylomakkeiden aikataulut.</span><span class="sxs-lookup"><span data-stu-id="21207-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="21207-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21207-108">Click New.</span></span>

3. <span data-ttu-id="21207-109">Syötä arvo Aikataulutus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21207-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="21207-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21207-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="21207-111">Määrittää aikataululle Anonyymi-arvon, jos vastaukset on kirjattava ilman niihin liittyviä nimiä.</span><span class="sxs-lookup"><span data-stu-id="21207-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="21207-112">Nimettömien tulosten käyttäminen on määritettävä ensin henkilöstöhallinnon parametreissa.</span><span class="sxs-lookup"><span data-stu-id="21207-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="21207-113">Valitse Tyyppi-kentästä suunnittelun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="21207-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="21207-114">Tässä esimerkissä käytetään Tyytyväisyys-tyyppiä.</span><span class="sxs-lookup"><span data-stu-id="21207-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="21207-115">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="21207-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="21207-116">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="21207-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="21207-117">Syötä Päivämäärään-kenttään päivämäärä.</span><span class="sxs-lookup"><span data-stu-id="21207-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="21207-118">Laajenna Työntekijän itsepalvelun sähköpostiosoite -osa.</span><span class="sxs-lookup"><span data-stu-id="21207-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="21207-119">Kirjoita arvo Aihe-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21207-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="21207-120">Esimerkki: kyselylomake käytettävissä</span><span class="sxs-lookup"><span data-stu-id="21207-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="21207-121">Kirjoita Teksti-kenttään sähköpostiviestin leipätekstissä näkyvä teksti.</span><span class="sxs-lookup"><span data-stu-id="21207-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="21207-122">Huomaa, että muuttujaa voidaan käyttää paikkamerkkinä järjestelmän arvoille.</span><span class="sxs-lookup"><span data-stu-id="21207-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="21207-123">Esimerkki: Hyvä %P%! Kirjaudu sisään työntekijän itsepalveluun ja täytä työterveyden kyselylomake.</span><span class="sxs-lookup"><span data-stu-id="21207-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="21207-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="21207-124">Contoso</span></span>  

12. <span data-ttu-id="21207-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="21207-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="21207-126">Vastattavien kyselylomakkeiden sekä valituille vastaajille käytettävien kyselyjen valitseminen asetustietojen avulla.</span><span class="sxs-lookup"><span data-stu-id="21207-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="21207-127">Valitse Asetuksen tiedot.</span><span class="sxs-lookup"><span data-stu-id="21207-127">Click Setup details.</span></span>

2. <span data-ttu-id="21207-128">Valitse luettelosta kysely, jolla etsit järjestelmästä kyselylomakkeen vastaajia.</span><span class="sxs-lookup"><span data-stu-id="21207-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="21207-129">Esimerkki: työntekijät</span><span class="sxs-lookup"><span data-stu-id="21207-129">Example: Workers</span></span>  

3. <span data-ttu-id="21207-130">Valitsemalla Tarkastele tai muokkaa kyselyä voit valita tietyt henkilöt. Muokkaamalla kyselyä voit etsiä tiettyjä ehtoja vastaavia henkilöitä.</span><span class="sxs-lookup"><span data-stu-id="21207-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="21207-131">Huomaa, että kaikkien vastaajien on oltava järjestelmän käyttäjiä.</span><span class="sxs-lookup"><span data-stu-id="21207-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="21207-132">Merkitse Henkilö-rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="21207-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="21207-133">Syötä tai valitse arvo Ehdot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="21207-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="21207-134">Valitse Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="21207-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="21207-135">Valitse luettelosta Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="21207-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="21207-136">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="21207-136">Click OK.</span></span>

8. <span data-ttu-id="21207-137">Valitse kyselyt-välilehti.</span><span class="sxs-lookup"><span data-stu-id="21207-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="21207-138">Laajenna puussa Tyytyväisyyskysely-lomaketyypin solmu -kohta.</span><span class="sxs-lookup"><span data-stu-id="21207-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="21207-139">Merkitse puussa "Työterveyden arviointi" -kohdan valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="21207-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="21207-140">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="21207-140">Click OK.</span></span>

12. <span data-ttu-id="21207-141">Valitse Suunniteltu vastausistunto.</span><span class="sxs-lookup"><span data-stu-id="21207-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="21207-142">Huomaa, että suunnitellut vastausistunnot on luotu kullekin valitulle/kysellylle käyttäjälle.</span><span class="sxs-lookup"><span data-stu-id="21207-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="21207-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21207-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="21207-144">Kyselylomakkeen ajoituksen käynnistäminen, jotta kyselylomake voidaan tarjota vastaajien täytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="21207-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="21207-145">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="21207-145">Click Functions.</span></span>

2. <span data-ttu-id="21207-146">Valitse Käynnistys.</span><span class="sxs-lookup"><span data-stu-id="21207-146">Click Start.</span></span>

3. <span data-ttu-id="21207-147">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="21207-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="21207-148">Sähköpostiviestin lähettäminen vastaajille käytettävissä olevasta kyselylomakkeesta.</span><span class="sxs-lookup"><span data-stu-id="21207-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="21207-149">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="21207-149">Click Functions.</span></span>

2. <span data-ttu-id="21207-150">Valitse Lähetä sähköposti.</span><span class="sxs-lookup"><span data-stu-id="21207-150">Click Send email.</span></span>

3. <span data-ttu-id="21207-151">Valitse Peruuta.</span><span class="sxs-lookup"><span data-stu-id="21207-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="21207-152">Kyselylomakkeen täyttäjiksi tarkoitettujen käyttäjien valvominen suunniteltujen vastausistuntojen avulla.</span><span class="sxs-lookup"><span data-stu-id="21207-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="21207-153">Valitse Suunniteltu vastausistunto.</span><span class="sxs-lookup"><span data-stu-id="21207-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="21207-154">Kun ajoitettu istunto voidaan lopettaa, poista mahdollinen jäljellä oleva suunniteltu vastausistunto.</span><span class="sxs-lookup"><span data-stu-id="21207-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="21207-155">Valitse Poista.</span><span class="sxs-lookup"><span data-stu-id="21207-155">Click Delete.</span></span>

3. <span data-ttu-id="21207-156">Valitse Kyllä.</span><span class="sxs-lookup"><span data-stu-id="21207-156">Click Yes.</span></span>

4. <span data-ttu-id="21207-157">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21207-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="21207-158">Ajoituksen voi lopettaa, kun kaikki vastaukset ovat saapuneet ja/tai kaikki jäljellä olevat suunnitellut vastausistunnot on poistettu.</span><span class="sxs-lookup"><span data-stu-id="21207-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="21207-159">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="21207-159">Click Functions.</span></span>
2. <span data-ttu-id="21207-160">Valitse Lopetus.</span><span class="sxs-lookup"><span data-stu-id="21207-160">Click End.</span></span>
3. <span data-ttu-id="21207-161">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="21207-161">Click OK.</span></span>
