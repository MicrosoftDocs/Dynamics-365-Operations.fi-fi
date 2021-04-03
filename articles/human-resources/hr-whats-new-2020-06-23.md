---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (25. kesäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 23. kesäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f767ad634a37b7231a7998184ef130668c8a8dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463619"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="b3b94-103">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. kesäkuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="b3b94-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b3b94-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="b3b94-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b3b94-105">Muutokset koskevat koontiversion numeroa 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="b3b94-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="b3b94-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="b3b94-107">Kun poistetun työntekijän rekisteröityminen vanhenee, loman tyyppi, saldo ja määrä nollataan loman rekisteröintilomakkeessa (444867)</span><span class="sxs-lookup"><span data-stu-id="b3b94-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="b3b94-108">**Lomatyyppi**, **Saldo** ja **Määrä** säilyvät nyt nollaamiseen sijaan, kun teet tämän valinnan.</span><span class="sxs-lookup"><span data-stu-id="b3b94-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="b3b94-109">Virheellinen ennustettu saldo, kun uusi ominaisuus (loman jaksotus yksittäisessä yrityksessä tai yksittäisessä suunnitelmassa) (456553)</span><span class="sxs-lookup"><span data-stu-id="b3b94-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="b3b94-110">Oikea ennustettu saldo näkyy nyt, kun yksittäisen yrityksen tai yksittäisen suunnitelman loman jaksotus on otettu käyttöön.</span><span class="sxs-lookup"><span data-stu-id="b3b94-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="b3b94-111">Yksiköt, joilla on suhteita, jotka aiheuttavat kaksinkertaisia navigointiominaisuuksia (456486)</span><span class="sxs-lookup"><span data-stu-id="b3b94-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="b3b94-112">Tämä versio korjaa ongelman, joka liittyy useiden yksiköiden navigointiominaisuuksiin (suhteeseen).</span><span class="sxs-lookup"><span data-stu-id="b3b94-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="b3b94-113">Kaksinkertaisia suhteita havaitaan.</span><span class="sxs-lookup"><span data-stu-id="b3b94-113">Duplicate relations are detected.</span></span> <span data-ttu-id="b3b94-114">Kaikki nämä tapaukset on korjattu.</span><span class="sxs-lookup"><span data-stu-id="b3b94-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="b3b94-115">Yritysten väliset kommentit suorituskykyarviossa (455536)</span><span class="sxs-lookup"><span data-stu-id="b3b94-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="b3b94-116">Yritysten väliset kommentit näkyvät nyt suorituskykyarvioissa tämän korjauksen myötä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="b3b94-117">Tämä muutos korjaa niiden arvioijan kommenttien näkymän, jotka syötettiin eri yrityksissä samaan suorituskykyarvioon.</span><span class="sxs-lookup"><span data-stu-id="b3b94-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="b3b94-118">Epäjohdonmukaisuus kompensaationhallintatietojen näyttämisessä (432562)</span><span class="sxs-lookup"><span data-stu-id="b3b94-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="b3b94-119">Kompensaatiotietojen johdonmukainen näkymä säilyy nyt esimiehen itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="b3b94-120">Sen mukaan, miten siirryt työntekijän **kompensaatiotietoihin**, kompensaatiotiedot näkyvät nyt johdonmukaisesti esimiehille.</span><span class="sxs-lookup"><span data-stu-id="b3b94-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="b3b94-121">Korjatun kompensaatiosuunnitelman voimaantulopäivä on oletusarvoisesti kuluva päivä (411994)</span><span class="sxs-lookup"><span data-stu-id="b3b94-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="b3b94-122">Kompensaation alkamispäivä perustuu nyt työntekijälle määritetyn aseman alkamispäivään.</span><span class="sxs-lookup"><span data-stu-id="b3b94-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="b3b94-123">Loma- ja poissaololomakkeen Ota käyttöön puolipäiväiset määritykset on pois käytöstä, kun lomake avautuu (452607)</span><span class="sxs-lookup"><span data-stu-id="b3b94-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="b3b94-124">Tämän muutoksen myötä **Ota käyttöön puolipäiväiset määritykset** on käytössä, kunnes uusi lomatapahtuma on olemassa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="b3b94-125">HcmDiscussionEntity-arvoa ei voida julkaista Excelissä; TotalRatingScore-kenttävirhe (453899)</span><span class="sxs-lookup"><span data-stu-id="b3b94-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="b3b94-126">Nyt voit päivittää **TotalRatingScore**-kentän käyttämällä **HCMDiscussionEntity**-arvoa Excel-työkirjan suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b3b94-127">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="b3b94-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="b3b94-128">Tietokannan lokiinkirjaus</span><span class="sxs-lookup"><span data-stu-id="b3b94-128">Database logging</span></span>

<span data-ttu-id="b3b94-129">Tietokantakirjauksen avulla voit määrittää, mitä taulukoita ja kenttiä seurataan.</span><span class="sxs-lookup"><span data-stu-id="b3b94-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="b3b94-130">Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan.</span><span class="sxs-lookup"><span data-stu-id="b3b94-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="b3b94-131">Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="b3b94-132">Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="b3b94-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="b3b94-133">Pakolliset kentät</span><span class="sxs-lookup"><span data-stu-id="b3b94-133">Mandatory fields</span></span> 

<span data-ttu-id="b3b94-134">Nyt voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="b3b94-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="b3b94-135">Tämä toiminto edellyttää **tallennettuja näkymiä**.</span><span class="sxs-lookup"><span data-stu-id="b3b94-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="b3b94-136">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="b3b94-136">Human Resources application in Teams</span></span>

<span data-ttu-id="b3b94-137">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b3b94-138">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b3b94-139">Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="b3b94-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="b3b94-140">Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="b3b94-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="b3b94-141">Etujen hallintayksiköt julkaisevat.</span><span class="sxs-lookup"><span data-stu-id="b3b94-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="b3b94-142">DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="b3b94-143">Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli.</span><span class="sxs-lookup"><span data-stu-id="b3b94-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="b3b94-144">Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.</span><span class="sxs-lookup"><span data-stu-id="b3b94-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="b3b94-145">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="b3b94-145">Buy and sell leave</span></span> 

<span data-ttu-id="b3b94-146">Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi.</span><span class="sxs-lookup"><span data-stu-id="b3b94-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="b3b94-147">Tätä prosessia hallitaan usein manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b3b94-147">This process is often managed manually.</span></span> <span data-ttu-id="b3b94-148">Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan.</span><span class="sxs-lookup"><span data-stu-id="b3b94-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="b3b94-149">Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="b3b94-150">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="b3b94-150">For more information, see:</span></span>

- [<span data-ttu-id="b3b94-151">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="b3b94-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="b3b94-152">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="b3b94-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="b3b94-153">Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus</span><span class="sxs-lookup"><span data-stu-id="b3b94-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="b3b94-154">Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="b3b94-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="b3b94-155">Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="b3b94-156">Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="b3b94-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="b3b94-157">Liitteiden lisääminen poissaolopyyntöihin</span><span class="sxs-lookup"><span data-stu-id="b3b94-157">Add attachments to time off requests</span></span>

<span data-ttu-id="b3b94-158">Mahdollisuus lisätä liitteitä hyväksyttyihin lomapyyntöihin on tärkeää nykyisessä COVID-19-tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="b3b94-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="b3b94-159">Työntekijät voivat nyt lisätä nämä liitteet.</span><span class="sxs-lookup"><span data-stu-id="b3b94-159">Employees can now add these attachments.</span></span> <span data-ttu-id="b3b94-160">He saavat lisää merkityksellisiä tietoja lomapyyntöihin tehtävistä päivityksistä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="b3b94-161">Lisätietoja on kohdassa [Liitteen lisääminen aiemmin luotuun pyyntöön](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="b3b94-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="b3b94-162">Syykoodin lisääminen jaksotuskeskeytyksiin</span><span class="sxs-lookup"><span data-stu-id="b3b94-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="b3b94-163">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="b3b94-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="b3b94-164">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="b3b94-164">Carry forward rules</span></span> 

<span data-ttu-id="b3b94-165">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="b3b94-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b3b94-166">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="b3b94-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b3b94-167">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b3b94-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="b3b94-168">Valittujen lomatyyppien jaksotuksen keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="b3b94-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="b3b94-169">Voit luoda säännön, joka keskeyttää työntekijöiden lomaa ja palkatonta lomaa varten annettujen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="b3b94-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b3b94-170">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="b3b94-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b3b94-171">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="b3b94-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="b3b94-172">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten</span><span class="sxs-lookup"><span data-stu-id="b3b94-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="b3b94-173">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="b3b94-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b3b94-174">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="b3b94-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="b3b94-175">Työntekijän itsepalvelun nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b3b94-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="b3b94-176">**Henkilöstöhallintoparametreissa** on uusi vaihtoehto, jolla voi päivittää Työntekijän itsepalvelu -työtilan nimen itsepalveluksi.</span><span class="sxs-lookup"><span data-stu-id="b3b94-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="b3b94-177">Dataverseen sisältyvät tarkistusluettelokohdat</span><span class="sxs-lookup"><span data-stu-id="b3b94-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="b3b94-178">Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="b3b94-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3b94-179">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="b3b94-179">See also</span></span>

[<span data-ttu-id="b3b94-180">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b3b94-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="b3b94-181">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="b3b94-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="b3b94-182">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="b3b94-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="b3b94-183">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="b3b94-183">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]