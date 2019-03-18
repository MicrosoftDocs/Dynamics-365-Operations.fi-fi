---
title: Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (14. joulukuuta 2018)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talent Core HR:n uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "304136"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="43877-103">Dynamics 365 for Talent Core HR:n uudet tai muuttuneet ominaisuudet (14. joulukuuta 2018)</span><span class="sxs-lookup"><span data-stu-id="43877-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="43877-104">**Koontiversio 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="43877-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="43877-105">Tässä ohjeaiheessa käsitellään Core HR -ohjelman uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="43877-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="43877-106">Muutokset</span><span class="sxs-lookup"><span data-stu-id="43877-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="43877-107">US - ACA (Affordable Care Act) -tuki verovuoden 2018 1095-B- ja 1095-C-lomakkeille</span><span class="sxs-lookup"><span data-stu-id="43877-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="43877-108">ALE (Applicable Large Employer) -työnantajien on annetta jokaiselle kokoaikaiselle työntekijälle 1095-C-lomake.</span><span class="sxs-lookup"><span data-stu-id="43877-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="43877-109">Jos työnantaja lisäksi tarjoaa omakustanteisen vakuutuksen, työnantajan on annettava lomake 1095-C (jos ALE-työnantaja) ja 1095-B (jos pienyrittäjä) kaikille koko- ja osa-aikaisille työntekijöille, joita jokin tarjolla olevista sairausvakuutussuunnitelmista koskee.</span><span class="sxs-lookup"><span data-stu-id="43877-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="43877-110">Tämä ominaisuus sisältää tulostettavat 1095-C- ja 1095-B-lomakkeet.</span><span class="sxs-lookup"><span data-stu-id="43877-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="43877-111">SubmittedByPersonId-kenttä ohitetaan tuonnin aikana HcmPerfJournalEntity-kohdassa</span><span class="sxs-lookup"><span data-stu-id="43877-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="43877-112">Kun suorituskyvyn kirjauskansiovientejä tuodaan tai viedään, **Lähettäjä**-kenttä ohitetaan.</span><span class="sxs-lookup"><span data-stu-id="43877-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="43877-113">Tämän muutoksen myötä **tuotu tai viety** arvo vastaa taulukossa viennin aikana olevaa arvoa, kun tuotava järjestelmä päivitetään tuontitiedoston antamalla arvolla.</span><span class="sxs-lookup"><span data-stu-id="43877-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="43877-114">Loma ja poissaolo -työtilan Analytiikka-välilehdessä on OpenConnectionError-virhe, jos käytössä on jokin muu kuin järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="43877-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="43877-115">Tämän päivityksen myötä virhettä ei anneta, kun **Analytiikka**-välilehti avataan **Loma ja poissaolot** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="43877-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="43877-116">Työntekijän itsepalvelussa tehty toimihierarkiaan porautuminen ruudusta ei päädy pääsolmuun</span><span class="sxs-lookup"><span data-stu-id="43877-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="43877-117">Tehty muutos korjaa Pääsolmun hakeminen epäonnistui -virheen tilanteissa, joissa toimihierarkia on mukautettu näkymään aiemmin luodussa työtilassa ja hierarkiassa on valittu toimi.</span><span class="sxs-lookup"><span data-stu-id="43877-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="43877-118">Vain järjestelmänvalvoja näkee Toimi-sivun Palkanlaskenta-välilehden</span><span class="sxs-lookup"><span data-stu-id="43877-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="43877-119">Tehty muutos korjaa aiemmin luodun oikeuden, Ylläpidä palkanlaskennan työntekijöiden ja toimien tietoja, suojauselementit.</span><span class="sxs-lookup"><span data-stu-id="43877-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="43877-120">Tämän muutoksen myötä palkanlaskentakoordinaattorilla on oletusarvoisesti Toimi-sivun Palkanlaskenta-kenttien käyttöoikeudet.</span><span class="sxs-lookup"><span data-stu-id="43877-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="43877-121">Virhe lähetettäessä suorituskykyarviota esimiehelle ja %Reviews.PerfPeriod%-paikkamerkin käyttö lähetysohjeissa</span><span class="sxs-lookup"><span data-stu-id="43877-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="43877-122">Tehty muutos korjaa Tyhjä viittaus -virheen, kun %Reviews.PerfPeriod%-paikkamerkkiä käytetään lähetysohjeissa.</span><span class="sxs-lookup"><span data-stu-id="43877-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="43877-123">Työvoiman Power BI -raportti näyttää virheen, kun työntekijän ikälisäpäivä on karkauspäivänä.</span><span class="sxs-lookup"><span data-stu-id="43877-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="43877-124">Tämän muutoksen ansiosta Power BI tukee nyt karkauspäiviä.</span><span class="sxs-lookup"><span data-stu-id="43877-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="43877-125">Core HR:n ja Attractin välinen integraatio</span><span class="sxs-lookup"><span data-stu-id="43877-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="43877-126">Tehty muutos päivittää palkattaviin kandidaatteihin liittyvän Core HR:n ja Attractin välisen integraation.</span><span class="sxs-lookup"><span data-stu-id="43877-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="43877-127">Jos palkattavien ehdokkaiden halutaan näkyvän **Henkilöstön hallinta** -työtilassa, käytössä on seuraavat CDS for Apps (CDS 2.0) -yksiköt:</span><span class="sxs-lookup"><span data-stu-id="43877-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following CDS for Apps (CDS 2.0) entities are used:</span></span>

<span data-ttu-id="43877-128">Työhakemus</span><span class="sxs-lookup"><span data-stu-id="43877-128">Job Application</span></span>
- <span data-ttu-id="43877-129">Tilan syyksi on määritettävä Tarjous hyväksytty</span><span class="sxs-lookup"><span data-stu-id="43877-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="43877-130">Ilmaisee hakijan ja avoimen työpaikan</span><span class="sxs-lookup"><span data-stu-id="43877-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="43877-131">Ehdokas</span><span class="sxs-lookup"><span data-stu-id="43877-131">Candidate</span></span>
-   <span data-ttu-id="43877-132">Ilmaisee ehdokkaan tiedot</span><span class="sxs-lookup"><span data-stu-id="43877-132">Provides Candidate information</span></span>

<span data-ttu-id="43877-133">Avoin työpaikka</span><span class="sxs-lookup"><span data-stu-id="43877-133">Job Opening</span></span>
-   <span data-ttu-id="43877-134">Ilmaisee avoimen työpaikan tunnuksen ja avoimen työpaikan osallistujat</span><span class="sxs-lookup"><span data-stu-id="43877-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="43877-135">Avoimen työpaikan osallistujat</span><span class="sxs-lookup"><span data-stu-id="43877-135">Job Opening Participants</span></span>
-   <span data-ttu-id="43877-136">Ilmaisee työhön ottavan esimiehen</span><span class="sxs-lookup"><span data-stu-id="43877-136">Provides Hiring Manager</span></span>

<span data-ttu-id="43877-137">Kun ehdokas on lisätty henkilöstön hallintaan, kyseinen ehdokas voidaan nyt myös hylätä ehdokaskortissa olevalla uudella asetuksella.</span><span class="sxs-lookup"><span data-stu-id="43877-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="43877-138">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="43877-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="43877-139">Loma ja poissaolot: tuleva loma ja lomasaldojen ennustaminen</span><span class="sxs-lookup"><span data-stu-id="43877-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="43877-140">Koska tehtävät muutokset mahdollistavat sen, että työntekijät voivat ennustaa poissaoloja ja tehdä tulevaisuuteen sijoittuvia poissaolopyyntöjä ilman, että se vaikuttaa heidän nykyisiin poissaolosaldoihinsa, myös poissaolosaldojen näyttäminen on muuttumassa.</span><span class="sxs-lookup"><span data-stu-id="43877-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="43877-141">Tällä hetkellä näytettävä käytettävissä oleva saldo on pyyntöjen käytettävissä oleva vapaa-aikasumma, joka sisältää kertymät, kuluva päivä mukaan lukien, ja kaikki hyväksytyt lomapyynnöt ajanjakson loppuun.</span><span class="sxs-lookup"><span data-stu-id="43877-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="43877-142">Kun ennustemahdollisuus julkaistaan, saldo näyttää muutokset nykyiseen poissaolosaldoon mukaan lukien kuluvan päivän sisältävät kertymät ja pyynnöt.</span><span class="sxs-lookup"><span data-stu-id="43877-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="43877-143">Työntekijät ja esimiehet näkevät nämä päivitetyt saldot työntekijän ja esimiehen itsepalvelutoiminnossa **Poissaoloaika**-kortissa ja **Poissaolosaldot**-ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="43877-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="43877-144">Henkilöstöpäälliköt näkevät nämä päivitetyt saldot **Henkilöt**-työtilassa ja työntekijän **Määritetyt lomasuunnitelmat** -ikkunassa.</span><span class="sxs-lookup"><span data-stu-id="43877-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="43877-145">Tunnettu ongelma</span><span class="sxs-lookup"><span data-stu-id="43877-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="43877-146">Finance and Operations -integraatiossa ilmenevät määritysvirheet</span><span class="sxs-lookup"><span data-stu-id="43877-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="43877-147">Seuraavat ongelmat on havaittu nykyisessä mallissa, jolla Talent integroidaan Dynamics 365 for Finance and Operationsin kanssa.</span><span class="sxs-lookup"><span data-stu-id="43877-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="43877-148">Uusi malli julkaistaan pian, ja sitä käytetään kaikissa uusissa luotavissa integraatioprojekteissa.</span><span class="sxs-lookup"><span data-stu-id="43877-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="43877-149">Aiemmin luoduissa integraatioprojekteissa päivitetään tehtävän yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="43877-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="43877-150">Lisätietoja on seuraavassa päivitettyjen yhdistämismääritysten taulukossa.</span><span class="sxs-lookup"><span data-stu-id="43877-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="43877-151">Toimet toimien päätyöhön määrittävä tehtävä ei integroi tietoja.</span><span class="sxs-lookup"><span data-stu-id="43877-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="43877-152">Tätä ongelmaa tutkitaan parhaillaan.</span><span class="sxs-lookup"><span data-stu-id="43877-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="43877-153">Ongelmaa ei välttää nykyisessä yhdistämismäärityksessä.</span><span class="sxs-lookup"><span data-stu-id="43877-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="43877-154">Osastot toimintayksikköön -tehtävän seuraavat yhdistämismääritykset on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="43877-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="43877-155">Aiemmin luotu lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-155">Existing source field</span></span>          | <span data-ttu-id="43877-156">Uusi lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="43877-157">cdm_description (kuvaus)</span><span class="sxs-lookup"><span data-stu-id="43877-157">cdm_description (Description)</span></span>  | <span data-ttu-id="43877-158">cdm_name (nimi)</span><span class="sxs-lookup"><span data-stu-id="43877-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="43877-159">Lisäksi on lisättävä lisäyhdistämismääritys.</span><span class="sxs-lookup"><span data-stu-id="43877-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="43877-160">Lisää seuraava yhdistämismääritys valitsemalla viimeinen **Ei mitään**.</span><span class="sxs-lookup"><span data-stu-id="43877-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="43877-161">Lähdetaulu</span><span class="sxs-lookup"><span data-stu-id="43877-161">Source field</span></span>                   | <span data-ttu-id="43877-162">Kohdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="43877-163">cdm_description (kuvaus)</span><span class="sxs-lookup"><span data-stu-id="43877-163">cdm_description (Description)</span></span>  | <span data-ttu-id="43877-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="43877-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="43877-165">Päivitettyjen yhdistämismääritysten pitäisi olla seuraavassa kuvassa olevien kaltaisia.</span><span class="sxs-lookup"><span data-stu-id="43877-165">The updated mappings should look like the following image.</span></span>

![Osastot tehtäväyksiköihin -tehtävä](./media/DepartmentMapping.png)


<span data-ttu-id="43877-167">Työt työn tietoihin -tehtävän seuraavat yhdistämismääritykset on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="43877-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="43877-168">Aiemmin luotu lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-168">Existing source field</span></span>          | <span data-ttu-id="43877-169">Uusi lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="43877-170">cdm_name (nimi)</span><span class="sxs-lookup"><span data-stu-id="43877-170">cdm_name (Name)</span></span>                | <span data-ttu-id="43877-171">cdm_description (kuvaus)</span><span class="sxs-lookup"><span data-stu-id="43877-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="43877-172">cdm_name (kuvaus)</span><span class="sxs-lookup"><span data-stu-id="43877-172">cdm_name (Description)</span></span>         | <span data-ttu-id="43877-173">cdm_jobdescription (työn kuvaus)</span><span class="sxs-lookup"><span data-stu-id="43877-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="43877-174">Päivitettyjen yhdistämismääritysten pitäisi olla alla olevassa kuvassa olevien kaltaisia.</span><span class="sxs-lookup"><span data-stu-id="43877-174">The updated mappings should look like the image below.</span></span>

![Työt töiden tietoihin -tehtävä](./media/JobMapping.png)

<span data-ttu-id="43877-176">Työntekijät työhön -tehtävän seuraavat yhdistämismääritykset on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="43877-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="43877-177">Aiemmin luotu lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-177">Existing source field</span></span>                 | <span data-ttu-id="43877-178">Uusi lähdekenttä</span><span class="sxs-lookup"><span data-stu-id="43877-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="43877-179">cdm_emailaddress1 (sähköpostiosoite 1)</span><span class="sxs-lookup"><span data-stu-id="43877-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="43877-180">cdm_primaryemailaddress (ensisijainen sähköpostiosoite</span><span class="sxs-lookup"><span data-stu-id="43877-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="43877-181">cdm_telephone1 (puhelinnumero 1)</span><span class="sxs-lookup"><span data-stu-id="43877-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="43877-182">cdm_primarytelephone (ensisijainen puhelinnumero)</span><span class="sxs-lookup"><span data-stu-id="43877-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="43877-183">Myös Sukupuoli-kentän muutos on päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="43877-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="43877-184">Valitse sukupuolelle **fn** (toiminto) -määritystyyppi ja päivitä seuraavat arvon yhdistämismääritykset.</span><span class="sxs-lookup"><span data-stu-id="43877-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="43877-185">CDS-arvo</span><span class="sxs-lookup"><span data-stu-id="43877-185">CDS value</span></span>                   | <span data-ttu-id="43877-186">Finance and Operations -arvo</span><span class="sxs-lookup"><span data-stu-id="43877-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="43877-187">75440000</span><span class="sxs-lookup"><span data-stu-id="43877-187">75440000</span></span>                    | <span data-ttu-id="43877-188">Mies</span><span class="sxs-lookup"><span data-stu-id="43877-188">Male</span></span>                                             |
| <span data-ttu-id="43877-189">75440001</span><span class="sxs-lookup"><span data-stu-id="43877-189">75440001</span></span>                    | <span data-ttu-id="43877-190">Nainen</span><span class="sxs-lookup"><span data-stu-id="43877-190">Female</span></span>                                           |
| <span data-ttu-id="43877-191">75440002</span><span class="sxs-lookup"><span data-stu-id="43877-191">75440002</span></span>                    | <span data-ttu-id="43877-192">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="43877-192">None</span></span>                                             | 
| <span data-ttu-id="43877-193">75440003</span><span class="sxs-lookup"><span data-stu-id="43877-193">75440003</span></span>                    | <span data-ttu-id="43877-194">Yksilöimätön</span><span class="sxs-lookup"><span data-stu-id="43877-194">NonSpecific</span></span>                                      |

<span data-ttu-id="43877-195">Päivitettyjen yhdistämismääritysten pitäisi olla seuraavissa kuvissa olevien kaltaisia.</span><span class="sxs-lookup"><span data-stu-id="43877-195">The updated mappings should look like the following images.</span></span>

![Työntekijät työntekijään -tehtävä](./media/WorkerMapping.png)

![Sukupuoli-kentän muutos](./media/WorkerTransform.png)