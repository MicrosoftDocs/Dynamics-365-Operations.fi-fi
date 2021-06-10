---
title: Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely
description: Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin hakijan seurantajärjestelmän (ATS) integraation API.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c043ac9c19a810d1718f0d4907cd5e9d651d778f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055289"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="ea585-103">Hakijan seurantajärjestelmän integroinnin sovellusliittymän esittely</span><span class="sxs-lookup"><span data-stu-id="ea585-103">Applicant Tracking System integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea585-104">Tässä aiheessa kuvataan Dynamics 365 Human Resourcesin hakijan seurantajärjestelmän (ATS) integraation API.</span><span class="sxs-lookup"><span data-stu-id="ea585-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="ea585-105">API-liittymän tarkoituksena on ottaa käyttöön tehokkaat integroinnit Dynamics 365 Human Resourcesin ja ATS-kumppanisovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="ea585-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS-integroinnin työnkulku](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="ea585-107">Integroitu kokemus alkaa Human Resourcesista, kun työhönottopäällikkö luo työhönottopyynnön.</span><span class="sxs-lookup"><span data-stu-id="ea585-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="ea585-108">Kun pyyntö aktivoidaan, ATS tuo työhönottoprojektin luontipyynnön tiedot.</span><span class="sxs-lookup"><span data-stu-id="ea585-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="ea585-109">Tämän jälkeen rekrytointiputken avulla voit valita ja palkata hakijan toimia varten.</span><span class="sxs-lookup"><span data-stu-id="ea585-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="ea585-110">Lopuksi ATS suorittaa integraaton takaisin lähettämällä valitun hakijan tietueen Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="ea585-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="ea585-111">Tämän jälkeen hakijatietue voi luoda työntekijätietueen käymällä läpi lisää rekorytoinnin oikeellisuustarkistuksia ja työnkulkuja.</span><span class="sxs-lookup"><span data-stu-id="ea585-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="ea585-112">Integroinnin mahdollistamiseksi Human Resources on lisännyt seuraavat komponentit:</span><span class="sxs-lookup"><span data-stu-id="ea585-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="ea585-113">Työhönottopyynnön luontitoiminto.</span><span class="sxs-lookup"><span data-stu-id="ea585-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="ea585-114">Laajennettu hakijan profiili ja liittyvät työnkulut.</span><span class="sxs-lookup"><span data-stu-id="ea585-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="ea585-115">Integroinnin API-sovellusliittymä, joka avaa uudet toiminnot integroiduille sovelluksille.</span><span class="sxs-lookup"><span data-stu-id="ea585-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="ea585-116">Lisätietoja työhönottopyynnön ja hakijan toimintojen määrittämisestä ja käyttämisestä on kohdassa [Ehdokkaiden työhönotto](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="ea585-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="ea585-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="ea585-117">Microsoft Dataverse</span></span>

<span data-ttu-id="ea585-118">Tämä sovellusliittymä perustuu Microsoft Dataverseen (aiemmin Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="ea585-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="ea585-119">Kaikki RESTful-vuorovaikutus tämän sovellusliittymän kanssa tapahtuu ODataa käyttävän Microsoft Dataverse -verkkoliittymän kautta.</span><span class="sxs-lookup"><span data-stu-id="ea585-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="ea585-120">Tämä sovellusliittymä on Dataverse-verkkoliittymän osajoukko.</span><span class="sxs-lookup"><span data-stu-id="ea585-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="ea585-121">Dataverse-verkkoliittymä määrittää ominaisuuksia, kuten todennuksen, SLA-sopimukset, erän, samanaikaisuustarkistuksen ja virheiden käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="ea585-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="ea585-122">Yleisiä tietoja Microsoft Dataverse -verkkoliittymästä:</span><span class="sxs-lookup"><span data-stu-id="ea585-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="ea585-123">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="ea585-123">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="ea585-124">Microsoft Dataverse -verkkoliittymän käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ea585-124">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="ea585-125">Microsoft Dataversen kehittäjäopas</span><span class="sxs-lookup"><span data-stu-id="ea585-125">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="ea585-126">Yllä olevat dokumentaatiot sisältävät yksityiskohtaisia tietoja ja kehittäjän ohjeita Dataverse-verkkoliittymän käyttämisestä. Tällaisia ohjeita ovat esimerkiksi [todennuksen hallinta](/powerapps/developer/data-platform/webapi/authenticate-web-api), [toimintojen suorittaminen](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postmanin käyttäminen API:n kanssa](/powerapps/developer/data-platform/webapi/use-postman-web-api) sekä [muutosseurannan tai delta-tunnusten käyttäminen](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) liittymän avulla.</span><span class="sxs-lookup"><span data-stu-id="ea585-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="ea585-127">Asetusjoukot</span><span class="sxs-lookup"><span data-stu-id="ea585-127">Option sets</span></span>

<span data-ttu-id="ea585-128">Tässä asiakirjassa kuvattu ATS-integroinnin API:n tietomalli sisältää asetusjoukot, joiden luettelo sisältää yksikön ominaisuuksiin liittyvät luetteloarvot.</span><span class="sxs-lookup"><span data-stu-id="ea585-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="ea585-129">Lisätietoja asetusjoukkojen käyttämisestä Dataverse-verkkoliittymässä on kohdassa [Asetusjoukkojen luominen ja päivittäminen verkkoliittymän avulla](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="ea585-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="ea585-130">Asetusjoukot määritetään kullekin Dataverse-ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="ea585-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="ea585-131">Human Resourcesin virtuaalitaulut Dataversessa</span><span class="sxs-lookup"><span data-stu-id="ea585-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="ea585-132">ATS-integroinnin API:n päätepisteet käyttävät Microsoft Dataversen virtuaalitaulujen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ea585-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="ea585-133">Oletusarvon mukaan virtuaalitauluja ja niihin liittyviä API-päätepisteitä ei ole otettu käyttöön Human Resources -ympäristöissä, minkä ansiosta organisaatiot voivat määrittää, mitkä OData-päätepisteet julkistetaan ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="ea585-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="ea585-134">Jotta sovellusliittymää voidaan käyttää, Human Resourcesin yksiköiden virtuaalitaulut on luotava ympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="ea585-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="ea585-135">Lisätietoja virtuaalitaulujen luomisesta liittymää varten on kohdassa [Dataverse-virtuaalitaulujen konfiguroiminen](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="ea585-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="ea585-136">Tietomalli</span><span class="sxs-lookup"><span data-stu-id="ea585-136">Data model</span></span>

<span data-ttu-id="ea585-137">Tietomalli on keskitetty kahden pääyksikön ympärille:</span><span class="sxs-lookup"><span data-stu-id="ea585-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="ea585-138">**RecruitingRequest** edustaa pyyntöä ATS:lle, että rekrytoidaan yhteen tai useampaan avoinna olevaan toimeen. Esimerkkikysely on kohdassa [Esimerkkikysely työhönottopyyntöä varten](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="ea585-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="ea585-139">**CandidateToHire** esittää tietoja hakijasta, joka on hyväksynyt toimen tarjouksen.</span><span class="sxs-lookup"><span data-stu-id="ea585-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="ea585-140">**Henkilö** edustaa hakijaa.</span><span class="sxs-lookup"><span data-stu-id="ea585-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="ea585-141">Henkilöllä voi olla useita rooleja yrityksessä, kuten hakija, työntekijä tai alihankkija.</span><span class="sxs-lookup"><span data-stu-id="ea585-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="ea585-142">Esimerkkikysely on kohdassa [Esimerkkikysely palkattavalle hakijalle](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="ea585-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="ea585-143">Seuraava kaavio kuvaa suhteita API:n sisällä.</span><span class="sxs-lookup"><span data-stu-id="ea585-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="ea585-144">Useilla tyypeillä on viiteavaimet muihin Human Resourcesin aiemmin luotuihin yksiköihin, joita ei ole kuvattu tässä.</span><span class="sxs-lookup"><span data-stu-id="ea585-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="ea585-145">Tässä asiakirjassa on tietoja yksiköistä, jotka liittyvät erityisesti rekrytoinnnin integrointiskenaarioihin.</span><span class="sxs-lookup"><span data-stu-id="ea585-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="ea585-146">Dataverse-verkkoliittymässä on kuitenkin useita muita yksiköitä Dynamics 365 Human Resourcesille, jotka voivat myös olla oleellisia integrointisi kannalta.</span><span class="sxs-lookup"><span data-stu-id="ea585-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="ea585-147">Voit esimerkiksi tarvita yksityiskohtaisia tietoja myös työntekijöistä, töistä, toimista tai muista yksiköistä, joita ei ole määritetty tässä.</span><span class="sxs-lookup"><span data-stu-id="ea585-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="ea585-148">Moniin näistä yksiköistä viitataan viiteavainsuhteissa tai siirtymisominaisuuksissa.</span><span class="sxs-lookup"><span data-stu-id="ea585-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integroinnin API-tietomalli](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="ea585-150">Työhönottopyyntö ja siihen liittyvät entiteetit ja asetusjoukot</span><span class="sxs-lookup"><span data-stu-id="ea585-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="ea585-151">Esimerkkikysely:</span><span class="sxs-lookup"><span data-stu-id="ea585-151">Example query:</span></span> 

- [<span data-ttu-id="ea585-152">Esimerkkikysely työhönottopyyntöä varten</span><span class="sxs-lookup"><span data-stu-id="ea585-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="ea585-153">Yksiköt:</span><span class="sxs-lookup"><span data-stu-id="ea585-153">Entities:</span></span>

- [<span data-ttu-id="ea585-154">Työhönottopyyntö</span><span class="sxs-lookup"><span data-stu-id="ea585-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="ea585-155">Työhönottopyynnön toimi</span><span class="sxs-lookup"><span data-stu-id="ea585-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="ea585-156">Työhönottopyynnön taito</span><span class="sxs-lookup"><span data-stu-id="ea585-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="ea585-157">Työhönottopyynnön koulutus</span><span class="sxs-lookup"><span data-stu-id="ea585-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="ea585-158">Työhönottopyynnön sijainti</span><span class="sxs-lookup"><span data-stu-id="ea585-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="ea585-159">Asetusjoukot:</span><span class="sxs-lookup"><span data-stu-id="ea585-159">Option sets:</span></span>

- [<span data-ttu-id="ea585-160">Työn vapautustila</span><span class="sxs-lookup"><span data-stu-id="ea585-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="ea585-161">Työhönottopyynnön toimen tila</span><span class="sxs-lookup"><span data-stu-id="ea585-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="ea585-162">Työhönottopyynnön tila</span><span class="sxs-lookup"><span data-stu-id="ea585-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="ea585-163">Säännösten mukainen tehtäväluokka</span><span class="sxs-lookup"><span data-stu-id="ea585-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="ea585-164">Palkattava hakija ja siihen liittyvät yksiköt ja asetusjoukot</span><span class="sxs-lookup"><span data-stu-id="ea585-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="ea585-165">Esimerkkikysely:</span><span class="sxs-lookup"><span data-stu-id="ea585-165">Example query:</span></span>

- [<span data-ttu-id="ea585-166">Esimerkkikysely palkattavalle hakijalle</span><span class="sxs-lookup"><span data-stu-id="ea585-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="ea585-167">Yksiköt:</span><span class="sxs-lookup"><span data-stu-id="ea585-167">Entities:</span></span>

- [<span data-ttu-id="ea585-168">Palkattava ehdokas</span><span class="sxs-lookup"><span data-stu-id="ea585-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="ea585-169">Henkilö</span><span class="sxs-lookup"><span data-stu-id="ea585-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="ea585-170">Henkilön koulutus</span><span class="sxs-lookup"><span data-stu-id="ea585-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="ea585-171">Henkilön ammattikokemus</span><span class="sxs-lookup"><span data-stu-id="ea585-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="ea585-172">Henkilön osoite</span><span class="sxs-lookup"><span data-stu-id="ea585-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="ea585-173">Osapuolen yhteyshenkilö</span><span class="sxs-lookup"><span data-stu-id="ea585-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="ea585-174">Henkilön osaamisalue</span><span class="sxs-lookup"><span data-stu-id="ea585-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="ea585-175">Luokitustaso</span><span class="sxs-lookup"><span data-stu-id="ea585-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="ea585-176">Henkilön todistus</span><span class="sxs-lookup"><span data-stu-id="ea585-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="ea585-177">Varmenteen tyyppi</span><span class="sxs-lookup"><span data-stu-id="ea585-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="ea585-178">Henkilön seulonta</span><span class="sxs-lookup"><span data-stu-id="ea585-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="ea585-179">Seulontatyypit</span><span class="sxs-lookup"><span data-stu-id="ea585-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="ea585-180">Henkilön tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="ea585-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="ea585-181">Asetusjoukot:</span><span class="sxs-lookup"><span data-stu-id="ea585-181">Option sets:</span></span>

- [<span data-ttu-id="ea585-182">Hakijatoimintojen integraation tulos</span><span class="sxs-lookup"><span data-stu-id="ea585-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="ea585-183">Tyhjä Kyllä Ei</span><span class="sxs-lookup"><span data-stu-id="ea585-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="ea585-184">Valmistumisen tila</span><span class="sxs-lookup"><span data-stu-id="ea585-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="ea585-185">Yhteyshenkilötyyppi</span><span class="sxs-lookup"><span data-stu-id="ea585-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="ea585-186">Koulutuksen hyvitysperuste</span><span class="sxs-lookup"><span data-stu-id="ea585-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="ea585-187">Sukupuoli</span><span class="sxs-lookup"><span data-stu-id="ea585-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="ea585-188">Siviilisääty</span><span class="sxs-lookup"><span data-stu-id="ea585-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="ea585-189">Vuoden kuukaudet</span><span class="sxs-lookup"><span data-stu-id="ea585-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="ea585-190">Ei Kyllä</span><span class="sxs-lookup"><span data-stu-id="ea585-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="ea585-191">Kausiyksikkö</span><span class="sxs-lookup"><span data-stu-id="ea585-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="ea585-192">Seulonnan tiheys</span><span class="sxs-lookup"><span data-stu-id="ea585-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="ea585-193">Seulonnan tiheys luo kohteesta</span><span class="sxs-lookup"><span data-stu-id="ea585-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="ea585-194">Osaamisaluetason tyyppi</span><span class="sxs-lookup"><span data-stu-id="ea585-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="ea585-195">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="ea585-195">See also</span></span>

[<span data-ttu-id="ea585-196">Ehdokkaiden työhönotto</span><span class="sxs-lookup"><span data-stu-id="ea585-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="ea585-197">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="ea585-197">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="ea585-198">Microsoft Dataverse -verkkoliittymän käyttäminen</span><span class="sxs-lookup"><span data-stu-id="ea585-198">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="ea585-199">Asetusjoukkojen luominen ja päivittäminen verkkoliittymän avulla</span><span class="sxs-lookup"><span data-stu-id="ea585-199">Create and update option sets using the Web API</span></span>](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]