---
title: Dynamics 365 Talentin integrointia Dynamics 365 Financeiin koskevat usein kysytyt kysymykset
description: Tässä ohjeaiheessa selvitetään, mitkä tiedot synkronoidaan Talentin ja Financen integroinnissa.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251011"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="284d7-103">Dynamics 365 Talentin integrointia Dynamics 365 Financeiin koskevat usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="284d7-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="284d7-104">Tässä ohjeaiheessa vastaan yleisiin kysymyksiin, jotka koskevat Dynamics 365 Talentista synkronoitavia tietoja, kun Talent integroidaan Dynamics 365 Financein kanssa.</span><span class="sxs-lookup"><span data-stu-id="284d7-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="284d7-105">Synkronoidaanko kaikki tiedot vai vain tietyt tietoyksiköt?</span><span class="sxs-lookup"><span data-stu-id="284d7-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="284d7-106">Core HR:n tiedoista synkronoidaan tietojen alijoukko.</span><span class="sxs-lookup"><span data-stu-id="284d7-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="284d7-107">Kaikki yksiköt sisältävä luettelo on kohdassa [Integrointi Dynamics 365 Talentista Dynamics 365 Financeiin](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="284d7-108">Attractin ja Onboardin osalta kaikki tiedot ovat alkuperäisiä Common Data Servicen tietoja.</span><span class="sxs-lookup"><span data-stu-id="284d7-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="284d7-109">Voinko luoda uuden yhdistämismäärityksen ilman mallia?</span><span class="sxs-lookup"><span data-stu-id="284d7-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="284d7-110">Mallien avulla pääsee alkuun.</span><span class="sxs-lookup"><span data-stu-id="284d7-110">Templates are the starting point.</span></span> <span data-ttu-id="284d7-111">Voit luoda oman mallin, mutta integrointiprojektia luotaessa tarvitaan aina malli.</span><span class="sxs-lookup"><span data-stu-id="284d7-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="284d7-112">Lisätietoja tietojen integrointiohjelmasta, malleista ja projekteista on kohdassa [Tietojen integrointi Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator) -ratkaisuun.</span><span class="sxs-lookup"><span data-stu-id="284d7-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="284d7-113">Voinko määrittää taloushallinnon dimensiot siirtymään Talentin ja Financen välillä?</span><span class="sxs-lookup"><span data-stu-id="284d7-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="284d7-114">Common Data Service -ratkaisussa ei ole tällä hetkellä taloushallinnon dimensioita, joten ne eivät sisälly oletusmalliin.</span><span class="sxs-lookup"><span data-stu-id="284d7-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="284d7-115">Tätä yksikköä suunnitellaan, mutta julkaisuajankohta ei ole tällä hetkellä tiedossa.</span><span class="sxs-lookup"><span data-stu-id="284d7-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="284d7-116">Jos Financessa on sellaisia tietoja, joita ei ole Talentissa, voit linkittää järjestelmät yhteen Talentin **Määritä linkit** -toiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="284d7-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="284d7-117">Lisätietoja Talentin ja Financen välisten linkkien määrittämisestä on kohdassa [Dynamics 365 Talent: Core HR:n uudet tai muuttuneet ominaisuudet (31. lokakuuta 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="284d7-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Määritä taloushallinnon dimensiot](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="284d7-119">Kun tuon työntekijöitä, ne päätyvät joskus Financen passiivisiin työntekijöihin.</span><span class="sxs-lookup"><span data-stu-id="284d7-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="284d7-120">Miksi?</span><span class="sxs-lookup"><span data-stu-id="284d7-120">Why?</span></span>

<span data-ttu-id="284d7-121">Tämä virhe voi esiintyä, jos työntekijöillä ei ole aktiivista työntekijän tietojen tietuetta Talentissa.</span><span class="sxs-lookup"><span data-stu-id="284d7-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="284d7-122">Voit ratkaista tämän ongelman valitsemalla **Henkilöstön hallinta \> Työntekijät \> Työhistoria \> Päivämäärän hallinta** ja varmistamalla, että työntekijätietojen tietue on aktiivinen.</span><span class="sxs-lookup"><span data-stu-id="284d7-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="284d7-123">Jos valitsen vain yhden kentän alijoukon yhdistämisen, käynnistävätkö yhdistämättömiin kenttiin tehdyt muutokset synkronoinnin?</span><span class="sxs-lookup"><span data-stu-id="284d7-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="284d7-124">Tietojen synkronointi noudattaa suoritusaikataulua.</span><span class="sxs-lookup"><span data-stu-id="284d7-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="284d7-125">Integrointi noutaa tietueen, jos jokin tietuen kenttä muuttuu, riippumatta siitä, onko kenttä osa integraation yhdistämismääritystä.</span><span class="sxs-lookup"><span data-stu-id="284d7-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="284d7-126">Miten voin lähettää vain aktiiviset työntekijän muutokset mutta ei päätettyjä tietueita?</span><span class="sxs-lookup"><span data-stu-id="284d7-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="284d7-127">Kyselyn lisäasetusten avulla voit suodattaa ja muokata lähdetietoja, ennen kuin ne siirretään kohteeseen.</span><span class="sxs-lookup"><span data-stu-id="284d7-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Aktiivisten työntekijöiden tarkennettu kysely](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="284d7-129">Voinko määrittää, mitkä tietyn yksikön kentät lähetetään Financeen?</span><span class="sxs-lookup"><span data-stu-id="284d7-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="284d7-130">Kenttiä voi lisätä integrointitehtävään tai poistaa niitä siitä.</span><span class="sxs-lookup"><span data-stu-id="284d7-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="284d7-131">Kaikkia Common Data Service -yksikössä olevia tietokenttiä ei täytetä Core HR:stä.</span><span class="sxs-lookup"><span data-stu-id="284d7-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="284d7-132">Lisätiedot voidaan täyttää PowerAppsin kautta.</span><span class="sxs-lookup"><span data-stu-id="284d7-132">Additional data can be populated via PowerApps.</span></span>

![Lisää tai poista kenttiä integrointitehtävään tai -tehtävästä](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="284d7-134">Määritän integroinnin erätyönä, mutta Talentin yhteys kohdejärjestelmään katkesi.</span><span class="sxs-lookup"><span data-stu-id="284d7-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="284d7-135">Miten voi lähettää saman muutosjoukon kohdejärjestelmään?</span><span class="sxs-lookup"><span data-stu-id="284d7-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="284d7-136">Poikkeuksen käsittelyyn ei tarvita mitään erityisiä asetuksia.</span><span class="sxs-lookup"><span data-stu-id="284d7-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="284d7-137">Tietojen integrointiohjelma havaitsee ja raportoi automaattisesti lähteessä ja kohteessa tapahtumat sekä sallii manuaaliset uudelleenyritykset.</span><span class="sxs-lookup"><span data-stu-id="284d7-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="284d7-138">Tietoja ei kuitenkaan voi korjata manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="284d7-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="284d7-139">Jos tietoja on päivitettävä, ne on tehtävä joko lähteessä tai kohteessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="284d7-140">Voinko määrittää kaksisuuntaisen integroinnin?</span><span class="sxs-lookup"><span data-stu-id="284d7-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="284d7-141">Ei, sillä tällä hetkellä integrointi on yksisuuntaista (Talentista Finance and Operationsiin).</span><span class="sxs-lookup"><span data-stu-id="284d7-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="284d7-142">Käytettävissä on kuitenkin oletusmalli, jolla tietoja voi lähettää Talentista Financeen.</span><span class="sxs-lookup"><span data-stu-id="284d7-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="284d7-143">Voinko sallia tietueiden poiston integroinnin osana?</span><span class="sxs-lookup"><span data-stu-id="284d7-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="284d7-144">Ei, sillä tietojen integrointiohjelma ei taltioi poistettuja tietueita tietojen siirtoon.</span><span class="sxs-lookup"><span data-stu-id="284d7-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="284d7-145">Tällä hetkellä vain tietojen luonti ja päivitykset (UPSERT) sisällytetään.</span><span class="sxs-lookup"><span data-stu-id="284d7-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="284d7-146">Voinko suorittaa virheellisen suorituksen uudelleen?</span><span class="sxs-lookup"><span data-stu-id="284d7-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="284d7-147">Ja lähetetäänkö siinä tapauksessa koko tiedosto vai vain muutokset?</span><span class="sxs-lookup"><span data-stu-id="284d7-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="284d7-148">Tietojen integrointiohjelman ensimmäinen ajo on täydellinen ajo.</span><span class="sxs-lookup"><span data-stu-id="284d7-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="284d7-149">Seuraavat ajot perustuvat muutosten seurantaan.</span><span class="sxs-lookup"><span data-stu-id="284d7-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="284d7-150">Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset Common Data Servicestä.</span><span class="sxs-lookup"><span data-stu-id="284d7-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="284d7-151">Saan projektia tallentaessani virheen, jonka mukaan projektissa on yhdistämisvirheitä.</span><span class="sxs-lookup"><span data-stu-id="284d7-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="284d7-152">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="284d7-152">What do I do?</span></span>

<span data-ttu-id="284d7-153">Tarkista integrointiavainten asetukset, tee asetuksiin tarvittavat muutokset ja päivitä sitten projektin yksiköt.</span><span class="sxs-lookup"><span data-stu-id="284d7-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="284d7-154">Oletusmallia käytettäessä integrointiavaimet tuodaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="284d7-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="284d7-155">Tämä ongelma voi esiintyä, kun uusia tehtäviä lisätään nykyiseen malliin.</span><span class="sxs-lookup"><span data-stu-id="284d7-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="284d7-156">Jos minulla on N yritystä, joissa työntekijöillä on työpaikat, onko minun luotava yhdistämismääritys heille kaikille?</span><span class="sxs-lookup"><span data-stu-id="284d7-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="284d7-157">Kyllä. Jokaiselle Financen yksikölle on luotava erillinen integrointiprojekti tietojen integroinnissa.</span><span class="sxs-lookup"><span data-stu-id="284d7-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="284d7-158">Minun on siirrettävä tietoja, jotka eivät sisälly Microsoftin oletusmalliin.</span><span class="sxs-lookup"><span data-stu-id="284d7-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="284d7-159">Onko se mahdollista?</span><span class="sxs-lookup"><span data-stu-id="284d7-159">Can I do this?</span></span>

<span data-ttu-id="284d7-160">Kyllä. Nykyisiin malleihin voi lisätä kenttiä, ja niitä voidaan myös poistaa siitä.</span><span class="sxs-lookup"><span data-stu-id="284d7-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="284d7-161">Kun virheajo suoritetaan, se poistaa tietueet ajosta ja lähettää viimeisimmät muutokset muista Common Data Service -yksiköistä.</span><span class="sxs-lookup"><span data-stu-id="284d7-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="284d7-162">Yksikön on oltava Common Data Service -ratkaisussa, jotta sen voi sisällyttää malliin.</span><span class="sxs-lookup"><span data-stu-id="284d7-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="284d7-163">Olen juuri luonut uudet Finance- ja Talent-ympäristöt ja saan virheilmoituksen, jonka mukaan tietoarvo rikkoo yhtenäisyysehtoja.</span><span class="sxs-lookup"><span data-stu-id="284d7-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="284d7-164">Miksi?</span><span class="sxs-lookup"><span data-stu-id="284d7-164">Why?</span></span>

<span data-ttu-id="284d7-165">Tämän virheen syy voi olla jokin seuraavista:</span><span class="sxs-lookup"><span data-stu-id="284d7-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="284d7-166">Tiedonsiirto aiheutti sen, että tietueet noudettiin lähteestä (Common Data Service) kahdesti.</span><span class="sxs-lookup"><span data-stu-id="284d7-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="284d7-167">Tiedonsiirrossa Finance and Operationsin pakollisilla kentillä on tyhjäarvo.</span><span class="sxs-lookup"><span data-stu-id="284d7-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="284d7-168">Tarkista, että tiedot ovat Common Data Servicessä ja että ne vastaavat Finance and Operationsin vaatimuksia.</span><span class="sxs-lookup"><span data-stu-id="284d7-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="284d7-169">Jos tapahtuu suoritusvirheitä eikä työntekijätunnus synkronoitunut, miten löydän työhistoria, joka sisältää epäonnistuneen työntekijätietueen?</span><span class="sxs-lookup"><span data-stu-id="284d7-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="284d7-170">Tietojen integrointiohjelma luo useita projekteja Financessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="284d7-171">Tietojen integrointiohjelman tehtävän ja Financen projektin välinen suhde on yksi yhteen.</span><span class="sxs-lookup"><span data-stu-id="284d7-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="284d7-172">Jäljitä aika tietojen integrointiohjelman suoritushistoriasta ja etsi Financen indeksi -1 -projekti.</span><span class="sxs-lookup"><span data-stu-id="284d7-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="284d7-173">Jos tehtävän numero on tietojen integrointiohjelmassa 9, Financen indeksi on 8.</span><span class="sxs-lookup"><span data-stu-id="284d7-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="284d7-174">Taltioi tehtäväindeksi tietojen integrointiohjelmasta (tässä esimerkissä se on 9).</span><span class="sxs-lookup"><span data-stu-id="284d7-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Tehtäväindeksin taltiointi tietojen integrointiohjelmasta](media/CaptureTaskIndex.png)

2. <span data-ttu-id="284d7-176">Jäljitä projektin suoritusaika.</span><span class="sxs-lookup"><span data-stu-id="284d7-176">Track the execution time of the project.</span></span>

![Projektin suoritusajan jäljitys](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="284d7-178">Etsi Financesta indeksi -1.</span><span class="sxs-lookup"><span data-stu-id="284d7-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="284d7-179">Tässä esimerkissä projekti, jonka jälkiliite on 8, ja projekti, jonka indeksin suoritusaika on 0, vastaa vaiheen 2 suoritusaikaa.</span><span class="sxs-lookup"><span data-stu-id="284d7-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Indeksin tunnistaminen](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="284d7-181">Talentin tiedot eivät näy Financessa sen jälkeen, kun Talent ja Finance on integroitu.</span><span class="sxs-lookup"><span data-stu-id="284d7-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="284d7-182">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="284d7-182">What do I do?</span></span>

<span data-ttu-id="284d7-183">Integrointi Financeen tapahtuu kahdessa vaiheessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="284d7-184">Tarkista ensin, että Talentin tiedot on päivitetty ja käytettävissä Common Data Servicessä.</span><span class="sxs-lookup"><span data-stu-id="284d7-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="284d7-185">Tämä synkronointi tapahtuu lähes reaaliaikaisesti, ja se voidaan tarkistaa PowerAppsissa katsomalla tietoyksiköiden tietoja.</span><span class="sxs-lookup"><span data-stu-id="284d7-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Tiedot Common Data Servicessä](media/DataInCDS.png)

<span data-ttu-id="284d7-187">Jos tiedot eivät näy odotetusti Common Data Servicessä, tarkista, että yksikön integrointia tuetaan.</span><span class="sxs-lookup"><span data-stu-id="284d7-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="284d7-188">Jos Common Data Serviceen halutaan sisällyttää lisätietoja, se edellyttää muutosta Microsoftin puolella.</span><span class="sxs-lookup"><span data-stu-id="284d7-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="284d7-189">Jos yksikköä tuetaan ja tiedot ovat käytettävissä Common Data Servicessä, tarkista, että yhdistämismääritys on oikein tietojen integrointiohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="284d7-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="284d7-190">Jos integrointiohjelman yhdistämismääritys näyttää olevan kunnossa, varmista seuraavaksi, että tietojen hallintatyöt on suoritettu.</span><span class="sxs-lookup"><span data-stu-id="284d7-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="284d7-191">Erätöitä suoritettaessa voi tapahtua virheitä.</span><span class="sxs-lookup"><span data-stu-id="284d7-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="284d7-192">Lisätietoja tietojen hallinnasta on kohdassa [Tietojen hallinta](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="284d7-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="284d7-193">Työntekijöiden osoitteet ovat virheellisiä Financeen tuonnin jälkeen.</span><span class="sxs-lookup"><span data-stu-id="284d7-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="284d7-194">Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="284d7-194">What should I do?</span></span>

<span data-ttu-id="284d7-195">**Sijainnin tunnus** -asetuksen numerosarja käyttää samaa mallia sekä Talentissa että Financessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="284d7-196">Kummallakin puolella on oltava yksilöllinen numerosarja, jotta osoiteongelmia ei tule, kun tiedot integroidaan Common Data Servicestä Finance and Operationsiin.</span><span class="sxs-lookup"><span data-stu-id="284d7-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="284d7-197">Tarkista Talentin toteutuksen aikana, että Talentissa ja Financessa ei käytetä samaa numerosarjaa.</span><span class="sxs-lookup"><span data-stu-id="284d7-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="284d7-198">Tarkista, että kaikki numerosarjat eivät ole samanlaisia siellä, missä tietoja ehkä ylläpidetään molemmissa järjestelmissä.</span><span class="sxs-lookup"><span data-stu-id="284d7-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="284d7-199">Kun yhteysjoukkoa luotiin, en nähnyt yhteyttä avattavassa Yhteys-luettelossa.</span><span class="sxs-lookup"><span data-stu-id="284d7-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="284d7-200">Mitä teen seuraavaksi?</span><span class="sxs-lookup"><span data-stu-id="284d7-200">What do I do?</span></span>

<span data-ttu-id="284d7-201">Varmista, että valitset yhteyksiä luotaessa Dynamics 365 Financen ja Common Data Servicen.</span><span class="sxs-lookup"><span data-stu-id="284d7-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="284d7-202">Saan työsuhteita synkronoitaessa virheen, jonka mukaan CompanyInfo_FK ei ole olemassa tai kentän Työsuhteen päättymispäivämäärä arvoa 31.12.2154 23:59:59 ei löydy liittyvästä taulusta Työsuhde. Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="284d7-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="284d7-203">Varmista, että yhdistämismääritys tehdään oikeisiin yrityksiin.</span><span class="sxs-lookup"><span data-stu-id="284d7-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="284d7-204">Yrityksen synkronointi ei sisälly oletusmalliin, joten oletuksena on, että jokainen Talentissa ja Common Data Servicessa oleva yritys on myös Financessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="284d7-205">Varmista myös, että valitset liitetylle yhteysjoukolle oikeat yritykset.</span><span class="sxs-lookup"><span data-stu-id="284d7-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="284d7-206">Financen kenttämääritys näyttää olevan tyhjä projektin määrittämisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="284d7-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="284d7-207">Mitä minun pitäisi tehdä?</span><span class="sxs-lookup"><span data-stu-id="284d7-207">What should I do?</span></span>

<span data-ttu-id="284d7-208">Päivitä Financen tietoyksiköt valitsemalla **Tietojen hallinta \> Kehikkoparametrit \> Yksikön asetukset \> Päivitä yksikköluettelo.**</span><span class="sxs-lookup"><span data-stu-id="284d7-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="284d7-209">Tämä voi kestää muutaman minuutin, jonka jälkeen yhdistämismääritysten pitäisi olla näkyvissä.</span><span class="sxs-lookup"><span data-stu-id="284d7-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="284d7-210">Tämä ongelma ilmenee uusia projekteja luotaessa.</span><span class="sxs-lookup"><span data-stu-id="284d7-210">This issue occurs when new projects are created.</span></span>

![Puuttuva kenttämääritys](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="284d7-212">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="284d7-212">Additional resources</span></span>

- <span data-ttu-id="284d7-213">Tietojen integrointiohjelma:</span><span class="sxs-lookup"><span data-stu-id="284d7-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="284d7-214">Integroi tiedot kohteeseen Common Data Service</span><span class="sxs-lookup"><span data-stu-id="284d7-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="284d7-215">Tietojen integrointiohjelman virheiden hallinta ja vianmääritys</span><span class="sxs-lookup"><span data-stu-id="284d7-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="284d7-216">Järjestelmän muodostamien lokien DSR-pyyntöihin vastaaminen PowerAppsissa, Microsoft Flow'ssa ja Common Data Servicessa</span><span class="sxs-lookup"><span data-stu-id="284d7-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="284d7-217">Tietojen hallinta:</span><span class="sxs-lookup"><span data-stu-id="284d7-217">Data Management:</span></span>

  - [<span data-ttu-id="284d7-218">Tietojen hallinta</span><span class="sxs-lookup"><span data-stu-id="284d7-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
