---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (14. toukokuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 14. toukokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
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
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b8d65236d316035722451a871afabedc6ab73f7a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127846"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="771fc-103">Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (14. toukokuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="771fc-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="771fc-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="771fc-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="771fc-105">Muutokset koskevat koontiversion numeroa 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="771fc-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="771fc-106">Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.</span><span class="sxs-lookup"><span data-stu-id="771fc-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="771fc-107">Alustan muutokset</span><span class="sxs-lookup"><span data-stu-id="771fc-107">Platform changes</span></span>

<span data-ttu-id="771fc-108">Ympäristömuutokset sisältyvät tämän viikon julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="771fc-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="771fc-109">Lisätietoja on kohdassa [Finance and Operations -sovellusten version 10.0.10 ympäristöpäivitykset (toukokuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span><span class="sxs-lookup"><span data-stu-id="771fc-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34).</span></span> <span data-ttu-id="771fc-110">Tämä versio sisältää ohjelmakorjauksia ja tallennettujen näkymien muutoksia.</span><span class="sxs-lookup"><span data-stu-id="771fc-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="771fc-111">Dataverse -valintaluetteloiden ja lomien valintaluetteloiden yhdenmukaisuuden varmistaminen (436343)</span><span class="sxs-lookup"><span data-stu-id="771fc-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="771fc-112">Dataverse -valintaluettelot ja lomien valintaluettelot ovat nyt yhdenmukaisia.</span><span class="sxs-lookup"><span data-stu-id="771fc-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="771fc-113">Käyttäjät saavat määrittää lomapyyntötyönkulun pyydetyn määrän perusteella (300044)</span><span class="sxs-lookup"><span data-stu-id="771fc-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="771fc-114">Käyttäjät voivat määrittää lomapyyntötyönkulkuja pyydettyjen määrien perusteella.</span><span class="sxs-lookup"><span data-stu-id="771fc-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="771fc-115">Uuden työntekijän lomakkeessa tiedot tulevat näkyviin Näytä-valikossa, kun suojauksen lisäasetukset on otettu käyttöön (403185)</span><span class="sxs-lookup"><span data-stu-id="771fc-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="771fc-116">Tämä versio korjaa tavan, jolla työntekijöitä tarkastellaan yritysten toiminnoissa, kun lisäkäyttöoikeudet on otettu käyttöön ja muiden yritysten työntekijät ovat käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="771fc-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="771fc-117">Yhden suunnitelman tai yhden yrityksen loman jaksotuksen salliminen (318844)</span><span class="sxs-lookup"><span data-stu-id="771fc-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="771fc-118">Tämän muutoksen myötä jaksotuksen voi suorittaa yrityksen tai suunnitelman kohdalla.</span><span class="sxs-lookup"><span data-stu-id="771fc-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="771fc-119">Toimen kokoaikaisuuden vastaavuuden näyttäminen (FTE) Rekisteröityneet työntekijät -lomakkeessa (414658)</span><span class="sxs-lookup"><span data-stu-id="771fc-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="771fc-120">Työntekijän toimen FTE-arvo määrittää työntekijän jaksotusarvon, kun FTE-vaihtoehto on otettu käyttöön lomatyypissä.</span><span class="sxs-lookup"><span data-stu-id="771fc-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="771fc-121">Tämä kenttää sisältyy nyt **Rekisteröityneet työntekijät** -lomakkeeseen ja **Joukkorekisteröinti**-valintaikkuna.</span><span class="sxs-lookup"><span data-stu-id="771fc-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="771fc-122">Lomasaldon vanhentumisen erätyön lisääminen (431266)</span><span class="sxs-lookup"><span data-stu-id="771fc-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="771fc-123">Päivittäin suoritettava uusi erätyö on nyt saatavana.</span><span class="sxs-lookup"><span data-stu-id="771fc-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="771fc-124">Se vähentää jäljellä olevaa lomasaldoa, kun vanhentumispäivät tulevat ajankohtaisiksi.</span><span class="sxs-lookup"><span data-stu-id="771fc-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="771fc-125">Työntekijöiden omien yhteyshenkilöiden vienti työntekijän oman yhteyshenkilöentiteetin avulla ei vie omia yhteyshenkilöitä, joissa on ylätason suhdetyyppi (345893)</span><span class="sxs-lookup"><span data-stu-id="771fc-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="771fc-126">**Työntekijän oma yhteyshenkilö** -tietoyksikkö (**HcmPersonalContactPersonEntity** DMF:ssä ja **PersonalContactPerson** ODatassa) ei voinut vielä omia yhteystietoja, joiden suhdetyyppi on **Ylätaso**.</span><span class="sxs-lookup"><span data-stu-id="771fc-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="771fc-127">Tämä ongelma on korjattu omissa yhteystiedoissa, jotka on luotu tämän muutoksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="771fc-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="771fc-128">Aiemmin luodut **Ylätaso**-tyypin omat yhteystiedot korjataan myöhemmässä versiossa.</span><span class="sxs-lookup"><span data-stu-id="771fc-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="771fc-129">Syykoodit näkyvät eri skenaarioissa, kun ne on merkitty lomaksi ja poissaoloksi ja yksinkertaistettu työtekijälomake on otettu käyttöön (434163)</span><span class="sxs-lookup"><span data-stu-id="771fc-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="771fc-130">Tämä muutos rajoittaa syykoodit vain loma- ja poissaolokoodeihin, kun yksinkertaistettu työntekijämerkintä otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="771fc-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="771fc-131">Esiversiotoiminto Määritä lomasuunnitelma työntekijöille tulevaisuudessa näyttää virheen (433555)</span><span class="sxs-lookup"><span data-stu-id="771fc-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="771fc-132">Tämä muutos korjaa virheen, kun lomasuunnitelmassa on määritetty kaksi lomatyyppiä ja yrität määrittää työntekijän.</span><span class="sxs-lookup"><span data-stu-id="771fc-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="771fc-133">Aloituspalkki näytetään kaikille käyttäjille (441731)</span><span class="sxs-lookup"><span data-stu-id="771fc-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="771fc-134">Tämän muutoksen myötä Aloituspalkki piilotetaan käyttäjiltä, jotka eivät ole järjestelmänvalvojia tai tiedonhallinnan järjestelmänvalvojia.</span><span class="sxs-lookup"><span data-stu-id="771fc-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="771fc-135">Dataversen työntekijän osoite-entiteetti toimii eri tavalla kuin Human Resourcesin päivämäärän ja ajan voimassaolopäivät (425071)</span><span class="sxs-lookup"><span data-stu-id="771fc-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="771fc-136">Tämä muutos säilyttää osoitetietojen kohdistuksen tietyissä skenaarioissa osoitteen päivämäärien perusteella.</span><span class="sxs-lookup"><span data-stu-id="771fc-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="771fc-137">Liitettä ei voi lisätä hyväksyttyyn lomapyyntöön (425407)</span><span class="sxs-lookup"><span data-stu-id="771fc-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="771fc-138">Tämän viikon julkaisun myötä voi liittää liitteitä hyväksyttyihin lomapyyntöihin lomapyyntöä muuttamatta.</span><span class="sxs-lookup"><span data-stu-id="771fc-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="771fc-139">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="771fc-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="771fc-140">Loman keskeytys</span><span class="sxs-lookup"><span data-stu-id="771fc-140">Leave suspension</span></span>

<span data-ttu-id="771fc-141">Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="771fc-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="771fc-142">Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset.</span><span class="sxs-lookup"><span data-stu-id="771fc-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="771fc-143">Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon.</span><span class="sxs-lookup"><span data-stu-id="771fc-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="771fc-144">Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="771fc-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="771fc-145">Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)</span><span class="sxs-lookup"><span data-stu-id="771fc-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="771fc-146">Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.</span><span class="sxs-lookup"><span data-stu-id="771fc-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="771fc-147">Valitun lomatyypin kertymän keskeyttäminen (272447)</span><span class="sxs-lookup"><span data-stu-id="771fc-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="771fc-148">Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="771fc-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="771fc-149">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="771fc-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="771fc-150">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="771fc-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="771fc-151">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (429549)</span><span class="sxs-lookup"><span data-stu-id="771fc-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="771fc-152">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="771fc-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="771fc-153">Lisää syykoodi jaksotuskeskeytyksiin (429547)</span><span class="sxs-lookup"><span data-stu-id="771fc-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="771fc-154">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="771fc-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="771fc-155">Aloita siirryttäessä henkilöstöhallinnon parametreista loma- ja poissaoloparametreihin</span><span class="sxs-lookup"><span data-stu-id="771fc-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="771fc-156">Tämä julkaisu alkaa yhdistää henkilöstöhallinnon parametreja loma- ja poissaoloparametreihin.</span><span class="sxs-lookup"><span data-stu-id="771fc-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="771fc-157">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="771fc-157">Carry forward rules</span></span>

<span data-ttu-id="771fc-158">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="771fc-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="771fc-159">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="771fc-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="771fc-160">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="771fc-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="771fc-161">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="771fc-161">See also</span></span>

[<span data-ttu-id="771fc-162">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="771fc-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="771fc-163">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="771fc-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="771fc-164">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="771fc-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="771fc-165">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="771fc-165">Manage features</span></span>](hr-admin-manage-features.md)