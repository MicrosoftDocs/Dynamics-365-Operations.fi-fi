---
title: Palkanlaskennan integroinnin ohjelmointirajapinnan esittely
description: Tässä aiheessa kuvataan Dynamics 365 Human Resources -palkanlaskenta-integroinnin sovellusliittymää.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a7be5ad42642de48ffdb2731a1300a953c5ede4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022760"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="3e0c9-103">Palkanlaskennan integroinnin ohjelmointirajapinnan esittely</span><span class="sxs-lookup"><span data-stu-id="3e0c9-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3e0c9-104">Tässä ohjeessa kuvataan Dynamics 365 Human Resources -palkanlaskenta-integroinnin sovellusliittymää.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="3e0c9-105">Ohjelmointirajapinta mahdollistaa virtaviivaisen päästä päähän -integraation henkilöstöhallinnon ja kumppanuuspalkkajärjestelmien välillä.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="3e0c9-106">Integroitu kokemus alkaa henkilöstöhallinnosta työntekijän profiili-, palkka- ja vähennystieto- ja osallistumistiedoilla.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="3e0c9-107">Kun työntekijä palkataan ja tarvittavat profiilitiedot ja palkkatiedot otetaan henkilöstöhallintoon, palkanlaskentajärjestelmä ottaa käyttöön nämä tiedot, joita käytetään palkanlaskentaa käsiteltäessä.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="3e0c9-108">Työntekijään tehdyt tai maksutiedot päivitetään myös käytettäväksi myöhemmin maksuajoissa.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Palkanlaskennan integroinnin työnkulku](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="3e0c9-110">Integroinnin mahdollistamiseksi Human Resourcesiin kuuluvat seuraavat komponentit:</span><span class="sxs-lookup"><span data-stu-id="3e0c9-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="3e0c9-111">Toiminto, jonka avulla voidaan merkitä, että työntekijälle voidaan maksaa</span><span class="sxs-lookup"><span data-stu-id="3e0c9-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="3e0c9-112">Integroinnin API-sovellusliittymä, joka avaa uudet toiminnot integroiduille sovelluksille</span><span class="sxs-lookup"><span data-stu-id="3e0c9-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="3e0c9-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="3e0c9-113">Microsoft Dataverse</span></span>

<span data-ttu-id="3e0c9-114">Tämä sovellusliittymä perustuu Microsoft Dataverseen (aiemmin Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="3e0c9-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="3e0c9-115">Kaikki RESTful-vuorovaikutus tämän sovellusliittymän kanssa tapahtuu ODataa käyttävän Microsoft Dataverse -verkkoliittymän kautta.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="3e0c9-116">Tämä sovellusliittymä on Dataverse-verkkoliittymän osajoukko.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="3e0c9-117">Dataverse-verkkoliittymä määrittää ominaisuuksia, kuten todennuksen, SLA-sopimukset, erän, samanaikaisuustarkistuksen ja virheiden käsittelyn.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="3e0c9-118">Yleisiä tietoja Microsoft Dataverse -verkkoliittymästä:</span><span class="sxs-lookup"><span data-stu-id="3e0c9-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="3e0c9-119">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3e0c9-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="3e0c9-120">Microsoft Dataverse -verkkoliittymän käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3e0c9-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="3e0c9-121">Microsoft Dataversen kehittäjäopas</span><span class="sxs-lookup"><span data-stu-id="3e0c9-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="3e0c9-122">Tämä dokumentaatio sisältää Dataversen Web-ohjelmointirajapinnan käytön yksityiskohtaisia tietoja ja kehittäjän ohjeita, joita ovat muun muassa seuraavat aiheet:</span><span class="sxs-lookup"><span data-stu-id="3e0c9-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="3e0c9-123">Todenna Microsoft Dataverse www-ohjelmointirajapinnan avulla</span><span class="sxs-lookup"><span data-stu-id="3e0c9-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="3e0c9-124">Toimintojen suorittamiseen www-ohjelmointirajapinnan avulla</span><span class="sxs-lookup"><span data-stu-id="3e0c9-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="3e0c9-125">Postmanin käyttäminen www-ohjelmointirajapinnan kanssa</span><span class="sxs-lookup"><span data-stu-id="3e0c9-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="3e0c9-126">Muutosten seurannan avulla voit synkronoida tiedot ulkoisten järjestelmien kanssa</span><span class="sxs-lookup"><span data-stu-id="3e0c9-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="3e0c9-127">Human Resourcesin virtuaalitaulut Dataversessa</span><span class="sxs-lookup"><span data-stu-id="3e0c9-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="3e0c9-128">Palkanlaskentaintegroinnin API:n päätepisteet käyttävät Microsoft Dataversen virtuaalitaulujen ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="3e0c9-129">Oletusarvon mukaan virtuaalitauluja ja niihin liittyviä API-päätepisteitä ei ole otettu käyttöön Human Resources -ympäristöissä, minkä ansiosta organisaatiot voivat määrittää, mitkä OData-päätepisteet julkistetaan ympäristölle.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="3e0c9-130">Jotta sovellusliittymää voidaan käyttää, Human Resourcesin yksiköiden virtuaalitaulut on luotava ympäristöä varten.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="3e0c9-131">Lisätietoja virtuaalitaulujen luomisesta liittymää varten on kohdassa [Dataverse-virtuaalitaulujen konfiguroiminen](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="3e0c9-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="3e0c9-132">Tietomalli</span><span class="sxs-lookup"><span data-stu-id="3e0c9-132">Data model</span></span>

<span data-ttu-id="3e0c9-133">Seuraava kaavio kuvaa suhteita API:n sisällä.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="3e0c9-134">Useilla tyypeillä on viiteavaimet muihin Human Resourcesin aiemmin luotuihin yksiköihin, joita ei ole kuvattu tässä.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="3e0c9-135">Tässä asiakirjassa on tietoja yksiköistä, jotka liittyvät erityisesti palkanlaskennan integrointiskenaarioihin.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="3e0c9-136">Dataverse-www-ohjelmointirajapinnassa on kuitenkin useita muita yksiköitä henkilöstöhallinnolle, jotka voivat myös olla oleellisia integrointisi kannalta.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="3e0c9-137">Joihinkin näistä yksiköistä viitataan viiteavainsuhteissa tai siirtymisominaisuuksissa.</span><span class="sxs-lookup"><span data-stu-id="3e0c9-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Palkanlaskennan integroinnin API-tietomalli](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="3e0c9-139">Palkanlaskennan työntekijä ja liittyvät entiteetit</span><span class="sxs-lookup"><span data-stu-id="3e0c9-139">Payroll employee and related entities</span></span>

<span data-ttu-id="3e0c9-140">Yksiköt:</span><span class="sxs-lookup"><span data-stu-id="3e0c9-140">Entities:</span></span>

- [<span data-ttu-id="3e0c9-141">Palkanlaskennan työntekijä</span><span class="sxs-lookup"><span data-stu-id="3e0c9-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="3e0c9-142">Palkanlaskennan työntekijän osoite</span><span class="sxs-lookup"><span data-stu-id="3e0c9-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="3e0c9-143">Palkanlaskennan kiinteän kompensaation suunnitelma</span><span class="sxs-lookup"><span data-stu-id="3e0c9-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="3e0c9-144">Palkanlaskennan työ</span><span class="sxs-lookup"><span data-stu-id="3e0c9-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="3e0c9-145">Palkanlaskennan toimi</span><span class="sxs-lookup"><span data-stu-id="3e0c9-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="3e0c9-146">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3e0c9-146">See also</span></span>

[<span data-ttu-id="3e0c9-147">Luo ja arvostele palkanlaskennan yksiköitä</span><span class="sxs-lookup"><span data-stu-id="3e0c9-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="3e0c9-148">Määritä Human Resourcesin parametrit</span><span class="sxs-lookup"><span data-stu-id="3e0c9-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="3e0c9-149">Määritä jaetut henkilöstöhallinnon parametrit</span><span class="sxs-lookup"><span data-stu-id="3e0c9-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="3e0c9-150">Mikä on Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="3e0c9-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="3e0c9-151">Microsoft Dataverse -verkkoliittymän käyttäminen</span><span class="sxs-lookup"><span data-stu-id="3e0c9-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]