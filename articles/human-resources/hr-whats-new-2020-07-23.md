---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. heinäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 23. heinäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055386"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="f7036-103">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (23. heinäkuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="f7036-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f7036-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f7036-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f7036-105">Muutokset koskevat koontiversion numeroa 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="f7036-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="f7036-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="f7036-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="f7036-107">Talousdimensioiden poistaminen sijainnista ei toimi odotetulla tavalla (445476)</span><span class="sxs-lookup"><span data-stu-id="f7036-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="f7036-108">Dimensioiden poistaminen sijainnista poistaa nyt samat sijainnit myös Dataverse -sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="f7036-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="f7036-109">Sijainnit, jotka eivät ole hierarkiassa, näyttävät passiiviset sijainnit (397257)</span><span class="sxs-lookup"><span data-stu-id="f7036-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="f7036-110">Sijainnit, jotka ovat passiivisia (joiden kesto on päättynyt), eivät enää näy sijaintien hierarkiassa **Sijainnit eivät ole hierarkiassa** -merkinnän kanssa.</span><span class="sxs-lookup"><span data-stu-id="f7036-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="f7036-111">Vahvistus, joka tapahtuu LeaveEnrollmentEntity- ja HcmWorkerEntity-entiteettien välillä Data Management Frameworkin (DMF) tuonnissa aiheuttaa tietojen latauksen hidastumista (442324)</span><span class="sxs-lookup"><span data-stu-id="f7036-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="f7036-112">Tämän version muutokset lisäävät **LeaveEnrollmentEntity**-entiteetin suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="f7036-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="f7036-113">Organisaation hallinnan mukauttaminen ei onnistu (447490)</span><span class="sxs-lookup"><span data-stu-id="f7036-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="f7036-114">Tämän muutoksen avulla voit nyt mukauttaa linkkejä **Organisaation hallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="f7036-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="f7036-115">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="f7036-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="f7036-116">Pakolliset kentät</span><span class="sxs-lookup"><span data-stu-id="f7036-116">Mandatory fields</span></span> 

<span data-ttu-id="f7036-117">Nyt voit tehdä kentistä pakollisia käyttämällä henkilöstöhallinnon mukauttamisominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="f7036-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="f7036-118">Tämä toiminto edellyttää **tallennettuja näkymiä**.</span><span class="sxs-lookup"><span data-stu-id="f7036-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="f7036-119">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="f7036-119">Human Resources application in Teams</span></span>

<span data-ttu-id="f7036-120">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="f7036-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="f7036-121">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="f7036-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="f7036-122">Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](./hr-admin-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="f7036-122">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="f7036-123">Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="f7036-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="f7036-124">Etujen hallintayksiköt julkaisevat.</span><span class="sxs-lookup"><span data-stu-id="f7036-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="f7036-125">DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="f7036-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="f7036-126">Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli.</span><span class="sxs-lookup"><span data-stu-id="f7036-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="f7036-127">Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.</span><span class="sxs-lookup"><span data-stu-id="f7036-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="f7036-128">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="f7036-128">Buy and sell leave</span></span> 

<span data-ttu-id="f7036-129">Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi.</span><span class="sxs-lookup"><span data-stu-id="f7036-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="f7036-130">Tätä prosessia hallitaan usein manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="f7036-130">This process is often managed manually.</span></span> <span data-ttu-id="f7036-131">Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan.</span><span class="sxs-lookup"><span data-stu-id="f7036-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="f7036-132">Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä.</span><span class="sxs-lookup"><span data-stu-id="f7036-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="f7036-133">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="f7036-133">For more information, see:</span></span>

- [<span data-ttu-id="f7036-134">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="f7036-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="f7036-135">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="f7036-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="f7036-136">Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus</span><span class="sxs-lookup"><span data-stu-id="f7036-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="f7036-137">Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="f7036-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="f7036-138">Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="f7036-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="f7036-139">Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="f7036-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="f7036-140">Liitteiden lisääminen poissaolopyyntöihin</span><span class="sxs-lookup"><span data-stu-id="f7036-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="f7036-141">Mahdollisuus lisätä liitteitä hyväksyttyihin lomapyyntöihin on tärkeää nykyisessä COVID-19-tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="f7036-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="f7036-142">Työntekijät voivat nyt lisätä nämä liitteet.</span><span class="sxs-lookup"><span data-stu-id="f7036-142">Employees can now add these attachments.</span></span> <span data-ttu-id="f7036-143">He saavat lisää merkityksellisiä tietoja lomapyyntöihin tehtävistä päivityksistä.</span><span class="sxs-lookup"><span data-stu-id="f7036-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="f7036-144">Lisätietoja on kohdassa [Liitteen lisääminen aiemmin luotuun pyyntöön](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="f7036-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="f7036-145">Syykoodin lisääminen jaksotuskeskeytyksiin</span><span class="sxs-lookup"><span data-stu-id="f7036-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="f7036-146">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="f7036-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="f7036-147">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="f7036-147">Carry forward rules</span></span> 

<span data-ttu-id="f7036-148">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="f7036-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="f7036-149">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="f7036-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="f7036-150">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="f7036-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="f7036-151">Valittujen lomatyyppien jaksotuksen keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="f7036-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="f7036-152">Voit luoda säännön, joka keskeyttää työntekijöiden lomaa ja palkatonta lomaa varten annettujen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="f7036-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="f7036-153">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="f7036-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="f7036-154">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="f7036-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="f7036-155">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten</span><span class="sxs-lookup"><span data-stu-id="f7036-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="f7036-156">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="f7036-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f7036-157">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="f7036-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="f7036-158">Dataverseen sisältyvät tarkistusluettelokohdat</span><span class="sxs-lookup"><span data-stu-id="f7036-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="f7036-159">Käyttöönotto-, käytöstäpoisto-, siirto- ja liiketoimintaprosessien tarkistusluettelokohdat ovat pian saatavilla Dataversessä.</span><span class="sxs-lookup"><span data-stu-id="f7036-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="f7036-160">Alustan muutokset</span><span class="sxs-lookup"><span data-stu-id="f7036-160">Platform changes</span></span>

<span data-ttu-id="f7036-161">Platform Update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="f7036-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="f7036-162">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="f7036-162">See also</span></span>

[<span data-ttu-id="f7036-163">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="f7036-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f7036-164">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="f7036-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="f7036-165">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="f7036-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="f7036-166">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="f7036-166">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]