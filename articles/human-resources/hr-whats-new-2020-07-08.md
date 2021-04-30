---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (8. heinäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 8. heinäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b277333ea37c2b6157ae9befc9d94f0e35ff97be
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891886"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="4aa08-103">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (8. heinäkuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="4aa08-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4aa08-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="4aa08-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="4aa08-105">Muutokset koskevat koontiversion numeroa 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="4aa08-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="4aa08-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="4aa08-107">Tietokannan lokiinkirjaus</span><span class="sxs-lookup"><span data-stu-id="4aa08-107">Database logging</span></span>

<span data-ttu-id="4aa08-108">Tietokantakirjauksen avulla voit määrittää, mitä taulukoita ja kenttiä seurataan.</span><span class="sxs-lookup"><span data-stu-id="4aa08-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="4aa08-109">Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan.</span><span class="sxs-lookup"><span data-stu-id="4aa08-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="4aa08-110">Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="4aa08-111">Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="4aa08-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="4aa08-112">Työntekijän itsepalvelun nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="4aa08-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="4aa08-113">**Työntekijän itsepalvelu** -työntilan nimen voi nyt vaihtaa **Henkilöstöhallinnon parametrit** -kohdassa muotoon **Itsepalvelu**.</span><span class="sxs-lookup"><span data-stu-id="4aa08-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="4aa08-114">Lisätietoja on kohdassa [Työntekijän itsepalvelutyötilan nimen muuttaminen](hr-employee-self-service-workspace-name.md).</span><span class="sxs-lookup"><span data-stu-id="4aa08-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="4aa08-115">Etuuksien hallinnan avoimen ilmoittautumisen käyttäminen kauden ulkopuolella</span><span class="sxs-lookup"><span data-stu-id="4aa08-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="4aa08-116">Tämä versio korjaa virheen, jonka vuoksi työntekijät pystyivät käyttämään etuuksien avointa ilmoittautumista ilmoittautumiskauden ulkopuolella tai ilman elämäntapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="4aa08-117">Tämän vuoksi avoimen ilmoittautumisen esittelyä varten työntekijän itsepalvelussa on muokattava avoimen ilmoittautumisen päivämäärät kuluvalle päivälle (tai sitä aikaisemmaksi), jotta toimintoa voi käyttää.</span><span class="sxs-lookup"><span data-stu-id="4aa08-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="4aa08-118">Tätä asetusta voi muuttaa valitsemalla **Etujen hallinta > Sääntö- ja asetuskaudet**.</span><span class="sxs-lookup"><span data-stu-id="4aa08-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="4aa08-119">Työntekijän ilmoittautumisen vahvistussähköposti</span><span class="sxs-lookup"><span data-stu-id="4aa08-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="4aa08-120">Voit nyt lähettää työntekijöille sähköpostiviestejä, kun he ovat tehneet etuusvalinnat.</span><span class="sxs-lookup"><span data-stu-id="4aa08-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="4aa08-121">Voit lähettää joko oletusviestin tai käyttää organisaation sähköpostimallia.</span><span class="sxs-lookup"><span data-stu-id="4aa08-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="4aa08-122">Nämä asetukset ovat kohdassa **Henkilöstöhallinnan parametrit > Etujen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="4aa08-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="4aa08-123">Peruutettu loma näkyy edelleen tulevana poissaolona Henkilöt-työtilassa (441358)</span><span class="sxs-lookup"><span data-stu-id="4aa08-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="4aa08-124">Peruutettu loma ei enää näy tulevana poissaolona **Henkilöt**-työtilan poissaolokorteissa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="4aa08-125">Osastoentiteetin ominaisuutta ei voi käyttää PositionV2-entiteetissä (456486)</span><span class="sxs-lookup"><span data-stu-id="4aa08-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="4aa08-126">Voit nyt lisätä osaston ilman, että näin luotaisiin suhteen kaksoiskappale.</span><span class="sxs-lookup"><span data-stu-id="4aa08-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="4aa08-127">PayrollWorkerEnrolledBenefitDetailEntity-entiteetin on käytettävä vain laskettua kenttää eläkepaketeissa (459779)</span><span class="sxs-lookup"><span data-stu-id="4aa08-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="4aa08-128">Kun **PayrollWorkerEnrolledBenefitDetailEntity**-entiteetti viedään, vienti määrittää, käyttääkö se laskettua kenttää palkkataulukon perusteella vai käyttääkö se **ContributionAmountCur**-kenttää varmuuskopiotaulussa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="4aa08-129">Tietoentiteetin käyttämä logiikka käyttää palkkataulua tilanteissa, joissa sovellus ei sitä yleensä tee.</span><span class="sxs-lookup"><span data-stu-id="4aa08-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="4aa08-130">Tämän logiikan vuoksi entiteettiviennit palauttavat sarakkeelle nolla-arvon, koska laskennan palkkataulukkoa ei ole eikä tuote anna asiakkaalle mahdollisuutta sen määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="4aa08-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="4aa08-131">Epäselvät tšekinkieliset käännökset henkilöstöhallinnassa ja työntekijän itsepalvelussa (400276)</span><span class="sxs-lookup"><span data-stu-id="4aa08-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="4aa08-132">Tämä versio korjaa käännökset sanoille **yrityksen hakemisto**, **seuraava rekisteröity kurssi**, **työ** ja **paikka**.</span><span class="sxs-lookup"><span data-stu-id="4aa08-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="4aa08-133">WorkCalendarEmployment-taulu ei ole luonut ja muokannut käyttöönotettuja järjestelmäkenttiä (460171)</span><span class="sxs-lookup"><span data-stu-id="4aa08-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="4aa08-134">Luodut ja muokatut järjestelmäkentät on nyt otettu käyttöön Human Resourcen **WorkCalendarEmployment**-taulussa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="4aa08-135">Työhönoton tyhjäarvoviittaus tulevan työntekijän Työhönotto ja tietojen lisääminen -toiminnossa (455475)</span><span class="sxs-lookup"><span data-stu-id="4aa08-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="4aa08-136">Tämä versio korjaa virheen (tyhjäarvoviittaus) sujuvoitetussa työntekijämerkinnässä, kun työntekijän työhönottoon käytetään **Työhönotto ja tietojen lisääminen** -toimintoa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="4aa08-137">Dataversen työntekijäentiteettiin tehdyt muutokset eivät siirry Human Resourcesiin (455652)</span><span class="sxs-lookup"><span data-stu-id="4aa08-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="4aa08-138">Seuraaviin Dataversen **Työntekijä**-entiteettiin tehdyt muutokset näkyvät nyt Human Resourcesissa:</span><span class="sxs-lookup"><span data-stu-id="4aa08-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="4aa08-139">**Työskentelee kotoa käsin**</span><span class="sxs-lookup"><span data-stu-id="4aa08-139">**Works from home**</span></span>
- <span data-ttu-id="4aa08-140">**Ikälisäpäivä**</span><span class="sxs-lookup"><span data-stu-id="4aa08-140">**Seniority date**</span></span>
- <span data-ttu-id="4aa08-141">**Vuosipäivän päivämäärä**</span><span class="sxs-lookup"><span data-stu-id="4aa08-141">**Anniversary date**</span></span>
- <span data-ttu-id="4aa08-142">**Alkuperäinen työsuhteen alkamispäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="4aa08-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="4aa08-143">Oikea kompensaatiotaso ei palaa oletusarvoon toimeen määritetyn työn perusteella (394136)</span><span class="sxs-lookup"><span data-stu-id="4aa08-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="4aa08-144">Tämän muutoksen myötä kompensaatiotaso palaa oikein oletusarvoon **Toimen tiedot** -kohdan **Voimassaolotietueet**-tietueiden ja **Kompensaatiopaketin määritys** -kohdan **alkamispäivän** perusteella.</span><span class="sxs-lookup"><span data-stu-id="4aa08-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="4aa08-145">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="4aa08-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="4aa08-146">Pakolliset kentät</span><span class="sxs-lookup"><span data-stu-id="4aa08-146">Mandatory fields</span></span> 

<span data-ttu-id="4aa08-147">Nyt voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="4aa08-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="4aa08-148">Tämä toiminto edellyttää **tallennettuja näkymiä**.</span><span class="sxs-lookup"><span data-stu-id="4aa08-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="4aa08-149">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="4aa08-149">Human Resources application in Teams</span></span>

<span data-ttu-id="4aa08-150">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="4aa08-151">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="4aa08-152">Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="4aa08-152">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="4aa08-153">Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="4aa08-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="4aa08-154">Etujen hallintayksiköt julkaisevat.</span><span class="sxs-lookup"><span data-stu-id="4aa08-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="4aa08-155">DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="4aa08-156">Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli.</span><span class="sxs-lookup"><span data-stu-id="4aa08-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="4aa08-157">Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.</span><span class="sxs-lookup"><span data-stu-id="4aa08-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="4aa08-158">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="4aa08-158">Buy and sell leave</span></span> 

<span data-ttu-id="4aa08-159">Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi.</span><span class="sxs-lookup"><span data-stu-id="4aa08-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="4aa08-160">Tätä prosessia hallitaan usein manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="4aa08-160">This process is often managed manually.</span></span> <span data-ttu-id="4aa08-161">Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan.</span><span class="sxs-lookup"><span data-stu-id="4aa08-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="4aa08-162">Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="4aa08-163">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="4aa08-163">For more information, see:</span></span>

- [<span data-ttu-id="4aa08-164">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="4aa08-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="4aa08-165">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="4aa08-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="4aa08-166">Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus</span><span class="sxs-lookup"><span data-stu-id="4aa08-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="4aa08-167">Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="4aa08-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="4aa08-168">Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="4aa08-169">Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="4aa08-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="4aa08-170">Liitteiden lisääminen poissaolopyyntöihin</span><span class="sxs-lookup"><span data-stu-id="4aa08-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="4aa08-171">Mahdollisuus lisätä liitteitä hyväksyttyihin lomapyyntöihin on tärkeää nykyisessä COVID-19-tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="4aa08-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="4aa08-172">Työntekijät voivat nyt lisätä nämä liitteet.</span><span class="sxs-lookup"><span data-stu-id="4aa08-172">Employees can now add these attachments.</span></span> <span data-ttu-id="4aa08-173">He saavat lisää merkityksellisiä tietoja lomapyyntöihin tehtävistä päivityksistä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="4aa08-174">Lisätietoja on kohdassa [Liitteen lisääminen aiemmin luotuun pyyntöön](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="4aa08-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="4aa08-175">Syykoodin lisääminen jaksotuskeskeytyksiin</span><span class="sxs-lookup"><span data-stu-id="4aa08-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="4aa08-176">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="4aa08-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="4aa08-177">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="4aa08-177">Carry forward rules</span></span> 

<span data-ttu-id="4aa08-178">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="4aa08-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="4aa08-179">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="4aa08-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="4aa08-180">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="4aa08-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="4aa08-181">Valittujen lomatyyppien jaksotuksen keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="4aa08-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="4aa08-182">Voit luoda säännön, joka keskeyttää työntekijöiden lomaa ja palkatonta lomaa varten annettujen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="4aa08-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="4aa08-183">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="4aa08-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="4aa08-184">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="4aa08-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="4aa08-185">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten</span><span class="sxs-lookup"><span data-stu-id="4aa08-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="4aa08-186">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="4aa08-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="4aa08-187">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="4aa08-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="4aa08-188">Dataverseen sisältyvät tarkistusluettelokohdat</span><span class="sxs-lookup"><span data-stu-id="4aa08-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="4aa08-189">Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="4aa08-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="4aa08-190">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="4aa08-190">See also</span></span>

[<span data-ttu-id="4aa08-191">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="4aa08-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="4aa08-192">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="4aa08-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="4aa08-193">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="4aa08-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="4aa08-194">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="4aa08-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]