---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (20. huhtikuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 20. elokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d964f9a532582b18471550a68032d00e19a065c4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467262"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="8c225-103">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (20. huhtikuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="8c225-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8c225-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8c225-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8c225-105">Muutokset koskevat koontiversion numeroa 8.1.3478.</span><span class="sxs-lookup"><span data-stu-id="8c225-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="8c225-106">Joissakin otsikoissa suluissa olevat luvut viittaavat Lifecycle Services (LCS) -palveluiden tukinumeroihin.</span><span class="sxs-lookup"><span data-stu-id="8c225-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="8c225-107">Tulevien ja odottavien poissaolotietojen näyttäminen Ihmiset-työtilan korteissa</span><span class="sxs-lookup"><span data-stu-id="8c225-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="8c225-108">Odottavat ja tulevat poissaolopyyntöjen vaihtoehdot ovat käytettävissä **Ihmiset**-työtilan loma- ja poissaolokorteissa.</span><span class="sxs-lookup"><span data-stu-id="8c225-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="8c225-109">Yksityinen-kentän asetus ei ole oletusarvoisesti Kyllä työntekijän itsepalvelun työntekijäroolissa (477106)</span><span class="sxs-lookup"><span data-stu-id="8c225-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="8c225-110">**Yksityinen**-kentän asetukseksi tulee nyt oletusarvoisesti **Kyllä**, kun työntekijät lisäävät uusia osoitetietoja työntekijän itsepalvelun **Henkilökohtaiset tiedot** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="8c225-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="8c225-111">Henkilöstöhallinnon Palkattavat ehdokkaat -pikavälilehdessä on virheellinen ehdokasmäärä (470110)</span><span class="sxs-lookup"><span data-stu-id="8c225-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="8c225-112">Palkattavien ehdokkaiden määrä näkyy nyt oikein **Henkilöstöhallinto**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="8c225-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="8c225-113">Työntekijän, jonka työsuhde on päättynyt, sairauslomaa ei voi antaa, kun jaksotukseksi on määritetty nolla (446195)</span><span class="sxs-lookup"><span data-stu-id="8c225-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="8c225-114">Poissaolotapahtumat ovat nyt mahdollisia työntekijöille, joiden työsuhde on päättynyt tulevaisuudessa, ja jaksotukseksi on määritetty nolla.</span><span class="sxs-lookup"><span data-stu-id="8c225-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="8c225-115">Poissaolotapahtumia voidaan antaa työntekijän työsuhteen päättymiseen saakka.</span><span class="sxs-lookup"><span data-stu-id="8c225-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="8c225-116">Mukautettujen kenttien lisääminen uuteen työntekijälomakkeeseen poistaa kentät käytöstä poissaolon hallinnan toimintopaneelissa (473314)</span><span class="sxs-lookup"><span data-stu-id="8c225-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="8c225-117">**Poissaolojen hallinnan** uuden **Työntekijä**-lomakkeen toimintopaneelin vaihtoehtoja ei enää poisteta käytöstä, jos uuteen **Työntekijä**-kenttään on lisätty mukautettuja kenttiä.</span><span class="sxs-lookup"><span data-stu-id="8c225-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="8c225-118">Poissaolon kommenttikentän pakollisuus sallii poissaolopyynnön lähettämisen, kun kommenttia ei lisätty (473543)</span><span class="sxs-lookup"><span data-stu-id="8c225-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="8c225-119">Kommenttikentät voivat olla nyt pakollisia, ja poissaolopyynnöt noudattavat tätä asetusta.</span><span class="sxs-lookup"><span data-stu-id="8c225-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="8c225-120">Pakolliset kentät ovat esiversiotoimintoja.</span><span class="sxs-lookup"><span data-stu-id="8c225-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="8c225-121">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten</span><span class="sxs-lookup"><span data-stu-id="8c225-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="8c225-122">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="8c225-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8c225-123">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="8c225-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="8c225-124">Pakolliset kentät</span><span class="sxs-lookup"><span data-stu-id="8c225-124">Mandatory fields</span></span>

<span data-ttu-id="8c225-125">Voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="8c225-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="8c225-126">Tämä toiminto edellyttää **tallennettuja näkymiä**.</span><span class="sxs-lookup"><span data-stu-id="8c225-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="8c225-127">Lisätietoja tallennetuista näkymistä on kohdassa:</span><span class="sxs-lookup"><span data-stu-id="8c225-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="8c225-128">[Tallennetut näkymät – yleinen käytettävyys](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020 Release Wave 2 -suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="8c225-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="8c225-129">Tallennettuja näkymiä täysimääräisesti hyödyntävien lomakkeiden luominen</span><span class="sxs-lookup"><span data-stu-id="8c225-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="8c225-130">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="8c225-130">Human Resources application in Teams</span></span>

<span data-ttu-id="8c225-131">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="8c225-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="8c225-132">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="8c225-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="8c225-133">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="8c225-133">For more information, see:</span></span>

- <span data-ttu-id="8c225-134">[Työntekijän loma- ja poissaolokokemus Microsoft Teamsissa](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020 Release Wave 1 -suunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="8c225-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="8c225-135">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="8c225-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="8c225-136">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="8c225-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="8c225-137">Human Resources -sovellus Teamsin esiversiotoiminnoissa</span><span class="sxs-lookup"><span data-stu-id="8c225-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="8c225-138">**Ilmoitukset**: Poissaolopyyntöjen lähettäjät ja hyväksyjät saavat ilmoitukset Teamsin Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="8c225-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="8c225-139">Hyväksyjät voivat hyväksyä tai hylätä poissaolopyyntöjä, ja lähettäjille ilmoitetaan, jos pyyntö hyväksyttiin tai hylättiin.</span><span class="sxs-lookup"><span data-stu-id="8c225-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="8c225-140">**Esimiehen poissaolokalenteri**: Esimiehet voivat nähdä suorien alaisten hyväksytyt ja odottavat poissaolot kalenterinäkymässä.</span><span class="sxs-lookup"><span data-stu-id="8c225-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="8c225-141">Tämän näkymän avulla on helppo hahmottaa, milloin ryhmä jäsenet ovat poissa töistä.</span><span class="sxs-lookup"><span data-stu-id="8c225-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="8c225-142">Dataverseen sisältyvät tarkistusluettelokohdat</span><span class="sxs-lookup"><span data-stu-id="8c225-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="8c225-143">Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="8c225-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="8c225-144">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="8c225-144">Known issues</span></span>

<span data-ttu-id="8c225-145">**Ominaisuuksien hallinta** -työtilassa voi olla ominaisuuksia, jotka on poistettu käytöstä esikatselun ominaisuutena, kun ne ovat yleisesti saatavilla.</span><span class="sxs-lookup"><span data-stu-id="8c225-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="8c225-146">Alla on luettelo yleisesti käytettävissä olevista ominaisuuksista, joiden tila on virheellinen.</span><span class="sxs-lookup"><span data-stu-id="8c225-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="8c225-147">Etujen hallinta</span><span class="sxs-lookup"><span data-stu-id="8c225-147">Benefits management</span></span>
- <span data-ttu-id="8c225-148">Palvelupyynnön hallinta</span><span class="sxs-lookup"><span data-stu-id="8c225-148">Case management</span></span>
- <span data-ttu-id="8c225-149">Tietokannan lokikirjaus (valvonta)</span><span class="sxs-lookup"><span data-stu-id="8c225-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="8c225-150">Loman jaksotus yhdelle yritykselle tai yhdelle suunnitelmalle</span><span class="sxs-lookup"><span data-stu-id="8c225-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="8c225-151">Lomien ja poissaolojen jaksotuksen keskeytys</span><span class="sxs-lookup"><span data-stu-id="8c225-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="8c225-152">Saldon oikaisun syykoodi ja kommentti</span><span class="sxs-lookup"><span data-stu-id="8c225-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="8c225-153">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="8c225-153">Buy and sell leave</span></span>
- <span data-ttu-id="8c225-154">Loma- ja poissaolokalenteri</span><span class="sxs-lookup"><span data-stu-id="8c225-154">Leave and absence calendar</span></span>
- <span data-ttu-id="8c225-155">Loman siirtokirjaussäännöt</span><span class="sxs-lookup"><span data-stu-id="8c225-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="8c225-156">Loman jaksotuksen tarkistus</span><span class="sxs-lookup"><span data-stu-id="8c225-156">Leave accrual auditing</span></span>
- <span data-ttu-id="8c225-157">Loman jaksotuksen poisto</span><span class="sxs-lookup"><span data-stu-id="8c225-157">Leave accrual deletion</span></span>
- <span data-ttu-id="8c225-158">Lomien jaksotusten pyöristys</span><span class="sxs-lookup"><span data-stu-id="8c225-158">Leave accrual rounding</span></span>
- <span data-ttu-id="8c225-159">Määritä useita lomatyyppejä yhdessä lomasuunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="8c225-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="8c225-160">Poissaolon päivityksen parannukset</span><span class="sxs-lookup"><span data-stu-id="8c225-160">Update time-off enhancements</span></span>
- <span data-ttu-id="8c225-161">Käytä työntekijän toimen laskennallista kokopäivätoimisuutta jaksotuksessa</span><span class="sxs-lookup"><span data-stu-id="8c225-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="8c225-162">Yritystenvälinen kompensaationäkymä</span><span class="sxs-lookup"><span data-stu-id="8c225-162">Cross company compensation view</span></span>
- <span data-ttu-id="8c225-163">Kehityskeskustelujen tulostaminen</span><span class="sxs-lookup"><span data-stu-id="8c225-163">Print performance reviews</span></span>
- <span data-ttu-id="8c225-164">Loman jaksotuksen juhlapäiväkorjaukset</span><span class="sxs-lookup"><span data-stu-id="8c225-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="8c225-165">Etuussuunnitelman työntekijäentiteetti</span><span class="sxs-lookup"><span data-stu-id="8c225-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="8c225-166">**EtuussuunnitelmaTyöntekijä**-entiteetissä on äskettäin havaittu kaksi ongelmaa.</span><span class="sxs-lookup"><span data-stu-id="8c225-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="8c225-167">Kun työntekijöiden rekisteröitymisiä tuodaan, **Kattavuuskoodi** ja **Suunnitelman tyypin koodi** määritetään virheellisesti.</span><span class="sxs-lookup"><span data-stu-id="8c225-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="8c225-168">Näiden ongelmien vuoksi työtekijöiden etuussuunnitelmat näkyvät virheellisesti **Työtekijän etuussuunnitelma**- ja **Avoin ilmoittautuminen** -lomakkeissa työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="8c225-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="8c225-169">Tämä ongelma voi vaikuttaa myös työntekijän mahdollisuuteen valita suunnitelma työntekijän itsepalvelussa.</span><span class="sxs-lookup"><span data-stu-id="8c225-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="8c225-170">Tällä hetkellä ongelmaa ei voi välttää.</span><span class="sxs-lookup"><span data-stu-id="8c225-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="8c225-171">Tätä ongelmaa käsitellään korkean prioriteetin korjauksena, ja korjaus otetaan käyttöön seuraavassa versiossa.</span><span class="sxs-lookup"><span data-stu-id="8c225-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c225-172">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="8c225-172">See also</span></span>

[<span data-ttu-id="8c225-173">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8c225-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8c225-174">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="8c225-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8c225-175">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="8c225-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8c225-176">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="8c225-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]