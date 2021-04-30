---
title: Financeen integroinnin usein kysytyt kysymykset
description: Tässä artikkelissa selitetään, mitkä tiedot synkronoidaan Human Resourcesin ja Financen integroinnissa.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5befac6c72153332319eefc1aaeab30c33f4c69
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892248"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="b326d-103">Financeen integroinnin usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="b326d-103">Integration with Finance FAQ</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b326d-104">Tässä ohjeaiheessa vastaan yleisiin kysymyksiin, jotka koskevat Dynamics 365 Human Resourcesista synkronoitavia tietoja, kun Talent integroidaan Dynamics 365 Financein kanssa.</span><span class="sxs-lookup"><span data-stu-id="b326d-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="can-i-edit-the-dynamics-365-talent-application-user-in-power-apps"></a><span data-ttu-id="b326d-105">Voinko muokata Dynamics 365 Talent -sovelluksen käyttäjää Power Appsissa?</span><span class="sxs-lookup"><span data-stu-id="b326d-105">Can I edit the Dynamics 365 Talent application user in Power Apps?</span></span>

<span data-ttu-id="b326d-106">Nro</span><span class="sxs-lookup"><span data-stu-id="b326d-106">No.</span></span> <span data-ttu-id="b326d-107">Jos muokkaat Human Resourcesin sovelluskäyttäjää, Human Resourcesin ja Dataversen välinen integrointi voi epäonnistua.</span><span class="sxs-lookup"><span data-stu-id="b326d-107">If you edit the Human Resources application user, the integration between Human Resources and Dataverse might fail.</span></span> <span data-ttu-id="b326d-108">Seuraavassa taulukossa näkyvät Talentin sovelluskäyttäjän oletusasetukset.</span><span class="sxs-lookup"><span data-stu-id="b326d-108">The following table shows the default settings for the Talent application user.</span></span>

| <span data-ttu-id="b326d-109">Koko nimi</span><span class="sxs-lookup"><span data-stu-id="b326d-109">Full Name</span></span> | <span data-ttu-id="b326d-110">Sovelluksen tunnus</span><span class="sxs-lookup"><span data-stu-id="b326d-110">Application ID</span></span> | <span data-ttu-id="b326d-111">Azure AD -objektin tunnus</span><span class="sxs-lookup"><span data-stu-id="b326d-111">Azure AD Object ID</span></span> | <span data-ttu-id="b326d-112">Sovelluksen tunnuksen URI</span><span class="sxs-lookup"><span data-stu-id="b326d-112">Application ID URI</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="b326d-113">Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="b326d-113">Dynamics365 for Talent</span></span> | <span data-ttu-id="b326d-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="b326d-114">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> | <span data-ttu-id="b326d-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span><span class="sxs-lookup"><span data-stu-id="b326d-115">27fd8129-4b3c-43f7-b1bf-47495d3a049b</span></span> | <span data-ttu-id="b326d-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span><span class="sxs-lookup"><span data-stu-id="b326d-116">f9be0c49-aa22-4ec6-911a-c5da515226ff</span></span> |

![Talentin sovelluskäyttäjän oletusasetukset](media/DynamicsApplicationUser.png)

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="b326d-118">Synkronoidaanko kaikki tiedot vai vain tietyt tietoyksiköt?</span><span class="sxs-lookup"><span data-stu-id="b326d-118">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="b326d-119">Tiedoista synkronoidaan tietojen alijoukko.</span><span class="sxs-lookup"><span data-stu-id="b326d-119">A subset of the data is synchronized.</span></span> <span data-ttu-id="b326d-120">Kaikki yksiköt sisältävä luettelo on kohdassa [Integrointi Dynamics 365 Financeen](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="b326d-120">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-dataverse"></a><span data-ttu-id="b326d-121">Miksi en nää, että Dataverseen synkronoidaan tietoja?</span><span class="sxs-lookup"><span data-stu-id="b326d-121">Why don't I see any data synced to Dataverse?</span></span>

<span data-ttu-id="b326d-122">Dataverse -integrointi on oletusarvoisesti pois käytöstä uudessa ympäristössä, joka ei sisällä toimitettuja demotietoja.</span><span class="sxs-lookup"><span data-stu-id="b326d-122">By default, the Dataverse integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="b326d-123">Se on oletusarvoisesti käytössä ympäristöissä, jotka sisältävät demotietoja, ja tietojen synkronointi alkaa, kun ympäristö on provisioitu.</span><span class="sxs-lookup"><span data-stu-id="b326d-123">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="b326d-124">Kyn ympäristö on valmis synkronoimaan tietoja, voit ottaa integroinnin käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b326d-124">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="b326d-125">Lisätietoja on kohdassa [Dataverse -integroinnin määritys](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="b326d-125">For more information, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="b326d-126">Voinko luoda uuden yhdistämismäärityksen ilman mallia?</span><span class="sxs-lookup"><span data-stu-id="b326d-126">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="b326d-127">Mallien avulla pääsee alkuun.</span><span class="sxs-lookup"><span data-stu-id="b326d-127">Templates are the starting point.</span></span> <span data-ttu-id="b326d-128">Voit luoda oman mallin, mutta integrointiprojektia luotaessa tarvitaan aina malli.</span><span class="sxs-lookup"><span data-stu-id="b326d-128">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="b326d-129">Lisätietoja tietojen integrointiohjelmasta, malleista ja projekteista on kohdassa [Tietojen integrointi Microsoft Dataverse](/powerapps/administrator/data-integrator) -ratkaisuun.</span><span class="sxs-lookup"><span data-stu-id="b326d-129">For more information about data integrator (DI), templates, and projects, see [Integrate data into Microsoft Dataverse](/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="b326d-130">Voinko määrittää taloushallinnon dimensiot siirtymään Human Resourcesin ja Financen välillä?</span><span class="sxs-lookup"><span data-stu-id="b326d-130">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="b326d-131">Dataverse -ratkaisussa ei ole tällä hetkellä taloushallinnon dimensioita, joten ne eivät sisälly oletusmalliin.</span><span class="sxs-lookup"><span data-stu-id="b326d-131">Financial dimensions aren’t currently in Dataverse and as a result aren’t part of the default template.</span></span> <span data-ttu-id="b326d-132">Tätä yksikköä suunnitellaan, mutta julkaisuajankohta ei ole tällä hetkellä tiedossa.</span><span class="sxs-lookup"><span data-stu-id="b326d-132">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="b326d-133">Jos Financessa on sellaisia tietoja, joita ei ole Human Resourcesissa, voit linkittää järjestelmät yhteen Human Resourcesin **linkkien määrittämisen** avulla.</span><span class="sxs-lookup"><span data-stu-id="b326d-133">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Määritä taloushallinnon dimensiot](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="b326d-135">Kun tuon työntekijöitä, ne päätyvät joskus Financen passiivisiin työntekijöihin.</span><span class="sxs-lookup"><span data-stu-id="b326d-135">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="b326d-136">Miksi?</span><span class="sxs-lookup"><span data-stu-id="b326d-136">Why?</span></span>

<span data-ttu-id="b326d-137">Tämä virhe voi esiintyä, jos työntekijöillä ei ole aktiivista työntekijän tietojen tietuetta Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="b326d-137">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="b326d-138">Voit ratkaista tämän ongelman valitsemalla **Henkilöstön hallinta \> Työntekijät \> Työhistoria \> Päivämäärän hallinta** ja varmistamalla, että työntekijätietojen tietue on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="b326d-138">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="b326d-139">Jos valitsen vain yhden kentän alijoukon yhdistämisen, käynnistävätkö yhdistämättömiin kenttiin tehdyt muutokset synkronoinnin?</span><span class="sxs-lookup"><span data-stu-id="b326d-139">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="b326d-140">Tietojen synkronointi noudattaa suoritusaikataulua.</span><span class="sxs-lookup"><span data-stu-id="b326d-140">Data sync follows the execution schedule.</span></span> <span data-ttu-id="b326d-141">Integrointi noutaa tietueen, jos jokin tietuen kenttä muuttuu, riippumatta siitä, onko kenttä osa integraation yhdistämismääritystä.</span><span class="sxs-lookup"><span data-stu-id="b326d-141">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="b326d-142">Miten voin lähettää vain aktiiviset työntekijän muutokset mutta ei päätettyjä tietueita?</span><span class="sxs-lookup"><span data-stu-id="b326d-142">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="b326d-143">Kyselyn lisäasetusten avulla voit suodattaa ja muokata lähdetietoja, ennen kuin ne siirretään kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="b326d-143">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Aktiivisten työntekijöiden tarkennettu kysely](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="b326d-145">Voinko määrittää, mitkä tietyn yksikön kentät lähetetään Financeen?</span><span class="sxs-lookup"><span data-stu-id="b326d-145">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="b326d-146">Kenttiä voi lisätä integrointitehtävään tai poistaa niitä siitä.</span><span class="sxs-lookup"><span data-stu-id="b326d-146">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="b326d-147">Kaikkia Dataverse-taulukossa olevia tietokenttiä ei täytetä Human Resourcesista.</span><span class="sxs-lookup"><span data-stu-id="b326d-147">Not all data fields that exist on the Dataverse table will be populated from Human Resources.</span></span>
<span data-ttu-id="b326d-148">Lisätiedot voidaan täyttää Power Appsin kautta.</span><span class="sxs-lookup"><span data-stu-id="b326d-148">Additional data can be populated via Power Apps.</span></span>

![Lisää tai poista kenttiä integrointitehtävään tai -tehtävästä](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="b326d-150">Määritän integroinnin erätyönä, mutta Human Resourcesin yhteys kohdejärjestelmään katkesi.</span><span class="sxs-lookup"><span data-stu-id="b326d-150">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="b326d-151">Miten voi lähettää saman muutosjoukon kohdejärjestelmään?</span><span class="sxs-lookup"><span data-stu-id="b326d-151">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="b326d-152">Poikkeuksen käsittelyyn ei tarvita mitään erityisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="b326d-152">No special setup is required for exception handling.</span></span> <span data-ttu-id="b326d-153">Tietojen integrointiohjelma havaitsee ja raportoi automaattisesti lähteessä ja kohteessa tapahtumat sekä sallii manuaaliset uudelleenyritykset.</span><span class="sxs-lookup"><span data-stu-id="b326d-153">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="b326d-154">Tietoja ei kuitenkaan voi korjata manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b326d-154">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="b326d-155">Jos tietoja on päivitettävä, ne on tehtävä joko lähteessä tai kohteessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-155">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="b326d-156">Voinko määrittää kaksisuuntaisen integroinnin?</span><span class="sxs-lookup"><span data-stu-id="b326d-156">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="b326d-157">Ei, integraatio on tällä hetkellä yksisuuntaista (Human Resourcesista Finance and Operationsiin).</span><span class="sxs-lookup"><span data-stu-id="b326d-157">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="b326d-158">Käytettävissä on kuitenkin oletusmalli, jolla tietoja voi lähettää Human Resourcesista Financeen.</span><span class="sxs-lookup"><span data-stu-id="b326d-158">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="b326d-159">Voinko sallia tietueiden poiston integroinnin osana?</span><span class="sxs-lookup"><span data-stu-id="b326d-159">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="b326d-160">Ei, sillä tietojen integrointiohjelma ei taltioi poistettuja tietueita tietojen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="b326d-160">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="b326d-161">Tällä hetkellä vain tietojen luonti ja päivitykset (UPSERT) sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="b326d-161">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="b326d-162">Voinko suorittaa virheellisen suorituksen uudelleen?</span><span class="sxs-lookup"><span data-stu-id="b326d-162">Can I rerun the errored execution?</span></span> <span data-ttu-id="b326d-163">Ja lähetetäänkö siinä tapauksessa koko tiedosto vai vain muutokset?</span><span class="sxs-lookup"><span data-stu-id="b326d-163">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="b326d-164">Tietojen integrointiohjelman ensimmäinen ajo on täydellinen ajo.</span><span class="sxs-lookup"><span data-stu-id="b326d-164">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="b326d-165">Seuraavat ajot perustuvat muutosten seurantaan.</span><span class="sxs-lookup"><span data-stu-id="b326d-165">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="b326d-166">Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset Dataversestä.</span><span class="sxs-lookup"><span data-stu-id="b326d-166">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Dataverse.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="b326d-167">Saan projektia tallentaessani virheen, jonka mukaan projektissa on yhdistämisvirheitä.</span><span class="sxs-lookup"><span data-stu-id="b326d-167">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="b326d-168">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="b326d-168">What do I do?</span></span>

<span data-ttu-id="b326d-169">Tarkista integrointiavainten asetukset, tee asetuksiin tarvittavat muutokset ja päivitä sitten projektin yksiköt.</span><span class="sxs-lookup"><span data-stu-id="b326d-169">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="b326d-170">Oletusmallia käytettäessä integrointiavaimet tuodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="b326d-170">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="b326d-171">Tämä ongelma voi esiintyä, kun uusia tehtäviä lisätään nykyiseen malliin.</span><span class="sxs-lookup"><span data-stu-id="b326d-171">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="b326d-172">Jos minulla on N yritystä, joissa työntekijöillä on työpaikat, onko minun luotava yhdistämismääritys heille kaikille?</span><span class="sxs-lookup"><span data-stu-id="b326d-172">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="b326d-173">Kyllä. Jokaiselle Financen yksikölle on luotava erillinen integrointiprojekti tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="b326d-173">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="b326d-174">Minun on siirrettävä tietoja, jotka eivät sisälly Microsoftin oletusmalliin.</span><span class="sxs-lookup"><span data-stu-id="b326d-174">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="b326d-175">Onko se mahdollista?</span><span class="sxs-lookup"><span data-stu-id="b326d-175">Can I do this?</span></span>

<span data-ttu-id="b326d-176">Kyllä. Nykyisiin malleihin voi lisätä kenttiä, ja niitä voidaan myös poistaa siitä.</span><span class="sxs-lookup"><span data-stu-id="b326d-176">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="b326d-177">Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset muista Dataverse-taulukoista.</span><span class="sxs-lookup"><span data-stu-id="b326d-177">The template can be modified to include additional data from other Dataverse tables.</span></span> <span data-ttu-id="b326d-178">Yksikön on oltava Dataverse -ratkaisussa, jotta sen voi sisällyttää malliin.</span><span class="sxs-lookup"><span data-stu-id="b326d-178">The entity must be in Dataverse for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="b326d-179">Olen juuri luonut uudet Finance- ja Human Resources -ympäristöt ja saan virheilmoituksen, jonka mukaan tietoarvo rikkoo yhtenäisyysehtoja.</span><span class="sxs-lookup"><span data-stu-id="b326d-179">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="b326d-180">Miksi?</span><span class="sxs-lookup"><span data-stu-id="b326d-180">Why?</span></span>

<span data-ttu-id="b326d-181">Tämän virheen syy voi olla jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="b326d-181">Reasons for this error can include:</span></span>

- <span data-ttu-id="b326d-182">Tiedonsiirto aiheutti sen, että tietueet noudettiin lähteestä (Dataverse) kahdesti.</span><span class="sxs-lookup"><span data-stu-id="b326d-182">The data transfer resulted in duplicate records extraction at the source (Dataverse).</span></span>

- <span data-ttu-id="b326d-183">Tiedonsiirrossa Finance and Operationsin pakollisilla kentillä on tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="b326d-183">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="b326d-184">Tarkista, että tiedot ovat Dataversessä ja että ne vastaavat Finance and Operationsin vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="b326d-184">Verify the data that is in Dataverse and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="b326d-185">Jos tapahtuu suoritusvirheitä eikä työntekijätunnus synkronoitunut, miten löydän työhistoria, joka sisältää epäonnistuneen työntekijätietueen?</span><span class="sxs-lookup"><span data-stu-id="b326d-185">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="b326d-186">Tietojen integrointiohjelma luo useita projekteja Financessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-186">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="b326d-187">Tietojen integrointiohjelman tehtävän ja Financen projektin välinen suhde on yksi yhteen.</span><span class="sxs-lookup"><span data-stu-id="b326d-187">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="b326d-188">Jäljitä aika tietojen integrointiohjelman suoritushistoriasta ja etsi Financen indeksi -1 -projekti.</span><span class="sxs-lookup"><span data-stu-id="b326d-188">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="b326d-189">Jos tehtävän numero on tietojen integrointiohjelmassa 9, Financen indeksi on 8.</span><span class="sxs-lookup"><span data-stu-id="b326d-189">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="b326d-190">Taltioi tehtäväindeksi tietojen integrointiohjelmasta (tässä esimerkissä se on 9).</span><span class="sxs-lookup"><span data-stu-id="b326d-190">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Tehtäväindeksin taltiointi tietojen integrointiohjelmasta](media/CaptureTaskIndex.png)

2. <span data-ttu-id="b326d-192">Jäljitä projektin suoritusaika.</span><span class="sxs-lookup"><span data-stu-id="b326d-192">Track the execution time of the project.</span></span>

    ![Projektin suoritusajan jäljitys](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="b326d-194">Etsi Financesta indeksi -1.</span><span class="sxs-lookup"><span data-stu-id="b326d-194">In Finance, identify index - 1.</span></span> <span data-ttu-id="b326d-195">Tässä esimerkissä projekti, jonka jälkiliite on 8, ja projekti, jonka indeksin suoritusaika on 0, vastaa vaiheen 2 suoritusaikaa.</span><span class="sxs-lookup"><span data-stu-id="b326d-195">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Indeksin tunnistaminen](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="b326d-197">Kun olen integroinut Human Resourcesin ja Financen, en näe Human Resources -tietojani Financessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-197">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="b326d-198">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="b326d-198">What do I do?</span></span>

<span data-ttu-id="b326d-199">Integrointi Financeen tapahtuu kahdessa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-199">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="b326d-200">Tarkista ensin, että Human Resourcesin tiedot on päivitetty ja käytettävissä Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="b326d-200">First, verify that the Human Resources data is updated and available in Dataverse.</span></span> <span data-ttu-id="b326d-201">Tämä synkronointi tapahtuu lähes reaaliaikaisesti, ja se voidaan tarkistaa Power Appsissa katsomalla tietotaulukoiden tietoja.</span><span class="sxs-lookup"><span data-stu-id="b326d-201">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data tables.</span></span>

![Tiedot Dataversessä](media/DataInCDS.png)

<span data-ttu-id="b326d-203">Jos tiedot eivät näy odotetusti Dataversessä, tarkista, että yksikön integrointia tuetaan.</span><span class="sxs-lookup"><span data-stu-id="b326d-203">If the data is not appearing as expected in Dataverse, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="b326d-204">Jos Dataverseen halutaan sisällyttää lisätietoja, se edellyttää muutosta Microsoftin puolella.</span><span class="sxs-lookup"><span data-stu-id="b326d-204">To include additional data in Dataverse, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="b326d-205">Jos yksikköä tuetaan ja tiedot ovat käytettävissä Dataversessä, tarkista, että yhdistämismääritys on oikein tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="b326d-205">If the entity is supported and the data is available in Dataverse, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="b326d-206">Jos integrointiohjelman yhdistämismääritys näyttää olevan kunnossa, varmista seuraavaksi, että tietojen hallintatyöt on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="b326d-206">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="b326d-207">Erätöitä suoritettaessa voi tapahtua virheitä.</span><span class="sxs-lookup"><span data-stu-id="b326d-207">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="b326d-208">Lisätietoja tietojen hallinnasta on kohdassa [Tietojen hallinta](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="b326d-208">For more information about Data Management, see [Data management](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="b326d-209">Työntekijöiden osoitteet ovat virheellisiä Financeen tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b326d-209">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="b326d-210">Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="b326d-210">What should I do?</span></span>

<span data-ttu-id="b326d-211">**Sijainnin tunnus** -asetuksen numerosarja käyttää samaa mallia sekä Human Resourcesissa että Financessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-211">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="b326d-212">Kummallakin puolella on oltava yksilöllinen numerosarja, jotta osoiteongelmia ei tule, kun tiedot integroidaan Dataversestä Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="b326d-212">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Dataverse to Finance and Operations.</span></span>

<span data-ttu-id="b326d-213">Tarkista Human Resourcesin toteutuksen aikana, että Human Resourcesissa ja Financessa ei käytetä samaa numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="b326d-213">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="b326d-214">Tarkista, että kaikki numerosarjat eivät ole samanlaisia siellä, missä tietoja ehkä ylläpidetään molemmissa järjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="b326d-214">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="b326d-215">Kun yhteysjoukkoa luotiin, en nähnyt yhteyttä avattavassa Yhteys-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="b326d-215">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="b326d-216">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="b326d-216">What do I do?</span></span>

<span data-ttu-id="b326d-217">Varmista, että valitset yhteyksiä luotaessa Dynamics 365 Financen ja Dataversen.</span><span class="sxs-lookup"><span data-stu-id="b326d-217">Make sure when creating your connections, you choose Dynamics 365 Finance and Dataverse.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="b326d-218">Saan työsuhteita synkronoitaessa virheen, jonka mukaan CompanyInfo_FK ei ole olemassa tai kentän Työsuhteen päättymispäivämäärä arvoa 31.12.2154 23:59:59 ei löydy liittyvästä taulusta Työsuhde. Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="b326d-218">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="b326d-219">Varmista, että yhdistämismääritys tehdään oikeisiin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="b326d-219">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="b326d-220">Yrityksen synkronointi ei sisälly oletusmalliin, joten oletuksena on, että jokainen Human Resourcesissa ja Dataversessä oleva yritys on myös Financessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-220">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Dataverse is also present in Finance.</span></span>
<span data-ttu-id="b326d-221">Varmista myös, että valitset liitetylle yhteysjoukolle oikeat yritykset.</span><span class="sxs-lookup"><span data-stu-id="b326d-221">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="b326d-222">Financen kenttämääritys näyttää olevan tyhjä projektin määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="b326d-222">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="b326d-223">Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="b326d-223">What should I do?</span></span>

<span data-ttu-id="b326d-224">Päivitä Financen tietoyksiköt valitsemalla **Tietojen hallinta \> Kehikkoparametrit \> Yksikön asetukset \> Päivitä yksikköluettelo.**</span><span class="sxs-lookup"><span data-stu-id="b326d-224">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="b326d-225">Tämä voi kestää muutaman minuutin, jonka jälkeen yhdistämismääritysten pitäisi olla näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="b326d-225">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="b326d-226">Tämä ongelma ilmenee uusia projekteja luotaessa.</span><span class="sxs-lookup"><span data-stu-id="b326d-226">This issue occurs when new projects are created.</span></span>

![Puuttuva kenttämääritys](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="b326d-228">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b326d-228">Additional resources</span></span>

- <span data-ttu-id="b326d-229">Tietojen integrointiohjelma:</span><span class="sxs-lookup"><span data-stu-id="b326d-229">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="b326d-230">Integroi tiedot kohteeseen Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="b326d-230">Integrate data into Microsoft Dataverse</span></span>](/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="b326d-231">Tietojen integrointiohjelman virheiden hallinta ja vianmääritys</span><span class="sxs-lookup"><span data-stu-id="b326d-231">Data Integrator error management and troubleshooting</span></span>](/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="b326d-232">Järjestelmän muodostamien lokien DSR-pyyntöihin vastaaminen Power Appsissa, Microsoft Power Automate'ssa ja Dataversessa</span><span class="sxs-lookup"><span data-stu-id="b326d-232">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Dataverse</span></span>](/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="b326d-233">Tietojen hallinta:</span><span class="sxs-lookup"><span data-stu-id="b326d-233">Data Management:</span></span>

  - [<span data-ttu-id="b326d-234">Tietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="b326d-234">Data management</span></span>](/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=%2ffin-and-ops%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]