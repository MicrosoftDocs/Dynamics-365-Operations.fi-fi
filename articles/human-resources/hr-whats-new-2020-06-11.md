---
title: Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (11. kesäkuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin 11. kesäkuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711791"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="cde5e-103">Dynamics 365 Human Resourcesin uudet ja muuttuneet ominaisuudet (11. kesäkuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="cde5e-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="cde5e-104">Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="cde5e-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="cde5e-105">Muutokset koskevat koontiversion numeroa 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="cde5e-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="cde5e-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="cde5e-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="cde5e-107">Sujuvoitettu työntekijälomake aiheuttaa joskus alilomakkeen sulkemispainikkeiden (X) toiminnan päättymisen (442369)</span><span class="sxs-lookup"><span data-stu-id="cde5e-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="cde5e-108">Kun uusi **Työntekijä**-lomake otettiin käyttöön, sulkemispainike (**X**) ei aina toimi alilomakkeissa.</span><span class="sxs-lookup"><span data-stu-id="cde5e-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="cde5e-109">Tämä ongelma oli ajoittainen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-109">This problem was intermittent.</span></span> <span data-ttu-id="cde5e-110">Lomakkeen voisi sulkea sen jälkeen, kun olet poistunut ja palannut siihen takaisin.</span><span class="sxs-lookup"><span data-stu-id="cde5e-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="cde5e-111">Voisit esimerkiksi valita valikkovaihtoehdon vasemmalla, siirtyä sitten **Työntekijä**-lomakkeeseen ja sulkea sen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="cde5e-112">Tämän viikon julkaisu korjaa tämän ongelman.</span><span class="sxs-lookup"><span data-stu-id="cde5e-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="cde5e-113">Työntekijän henkilökohtaisen yhteyshenkilöentiteetti ei vie henkilökohtaisia yhteyshenkilöitä, joiden tyyppinä on ylätason suhde</span><span class="sxs-lookup"><span data-stu-id="cde5e-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="cde5e-114">Tässä versiossa **Työntekijän henkilökohtainen yhteyshenkilö** -entiteetti vie kaikki suhdetyypit.</span><span class="sxs-lookup"><span data-stu-id="cde5e-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="cde5e-115">HcmPositionWorkerAssignmentV2Entity-entiteetin pitäisi oletusarvoisesti olla Ceridian-palkanlaskennan integraatiopaketin osa (448506)</span><span class="sxs-lookup"><span data-stu-id="cde5e-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="cde5e-116">Tämän muutoksen myötä **HcmPositionWorkerAssignmentV2Entity** sisältyy Ceridian-palkanlaskennan integraatiopakettiin.</span><span class="sxs-lookup"><span data-stu-id="cde5e-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="cde5e-117">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="cde5e-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="cde5e-118">Tietokannan lokiinkirjaus</span><span class="sxs-lookup"><span data-stu-id="cde5e-118">Database logging</span></span>

<span data-ttu-id="cde5e-119">Tietokantakirjaustoiminnon avulla voit määrittää, mitä taulukoita ja kenttiä seurataan.</span><span class="sxs-lookup"><span data-stu-id="cde5e-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="cde5e-120">Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan.</span><span class="sxs-lookup"><span data-stu-id="cde5e-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="cde5e-121">Tietokantakirjauksen ominaisuuksien avulla nähdään nämä muutokset ajan kuluessa.</span><span class="sxs-lookup"><span data-stu-id="cde5e-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="cde5e-122">Lisätietoja on kohdassa [Tietokantakirjauksen määrittäminen ja hallinta](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="cde5e-123">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="cde5e-123">Human Resources application in Teams</span></span>

<span data-ttu-id="cde5e-124">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="cde5e-125">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="cde5e-126">Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="cde5e-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="cde5e-127">Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="cde5e-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="cde5e-128">Etujen hallintayksiköt julkaisevat.</span><span class="sxs-lookup"><span data-stu-id="cde5e-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="cde5e-129">DMF-yksikköjen avulla voi tuoda ja viedä tietoja, mikä helpottaa etuuksien hallinnan määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="cde5e-130">Tietojen siirtämiseen on käytettävissä etuuksien hallintamalli.</span><span class="sxs-lookup"><span data-stu-id="cde5e-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="cde5e-131">Malli vie tiedot ja tuo ne peräkkäin tietojen riippuvaisuuksia noudattaen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="cde5e-132">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="cde5e-132">Buy and sell leave</span></span> 

<span data-ttu-id="cde5e-133">Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi.</span><span class="sxs-lookup"><span data-stu-id="cde5e-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="cde5e-134">Tätä prosessia hallitaan usein manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="cde5e-134">This process is often managed manually.</span></span> <span data-ttu-id="cde5e-135">Tämä toiminto automatisoi henkilöstöosaston käytäntöjen ja pyyntöjen hallinnan.</span><span class="sxs-lookup"><span data-stu-id="cde5e-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="cde5e-136">Se sujuvoittaa lomien hallintaprosessia ja auttaa poistamaan virheitä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="cde5e-137">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="cde5e-137">For more information, see:</span></span>

- [<span data-ttu-id="cde5e-138">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="cde5e-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="cde5e-139">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="cde5e-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="cde5e-140">Yhden yrityksen tai yhden suunnitelman mukainen loman jaksotus</span><span class="sxs-lookup"><span data-stu-id="cde5e-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="cde5e-141">Asiakkaat voi käsitellä yhden yrityksen tai yhden suunnitelman loma- ja poissaolosuunnitelman jaksotukset.</span><span class="sxs-lookup"><span data-stu-id="cde5e-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="cde5e-142">Tämä selkeyttää jaksotusprosessia, kun asiakkailla on erilaisia lomavuosi- tai loman jaksotuskäytäntöjä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="cde5e-143">Lisätietoja on kohdassa [Loman jaksottaminen yrityksen tai lomasuunnitelman mukaan](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="cde5e-144">Liitteiden lisääminen poissaolopyyntöihin</span><span class="sxs-lookup"><span data-stu-id="cde5e-144">Add attachments to time off requests</span></span>

<span data-ttu-id="cde5e-145">Mahdollisuus lisätä liitteitä hyväksyttyihin lomapyyntöihin on tärkeää nykyisessä COVID-19-tilanteessa.</span><span class="sxs-lookup"><span data-stu-id="cde5e-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="cde5e-146">Työntekijät voivat nyt lisätä nämä liitteet.</span><span class="sxs-lookup"><span data-stu-id="cde5e-146">Employees can now add these attachments.</span></span> <span data-ttu-id="cde5e-147">He saavat lisää merkityksellisiä tietoja lomapyyntöihin tehtävistä päivityksistä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="cde5e-148">Lisätietoja on kohdassa [Liitteen lisääminen aiemmin luotuun pyyntöön](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="cde5e-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="cde5e-149">Syykoodin lisääminen jaksotuskeskeytyksiin</span><span class="sxs-lookup"><span data-stu-id="cde5e-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="cde5e-150">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="cde5e-151">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="cde5e-151">Carry forward rules</span></span> 

<span data-ttu-id="cde5e-152">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="cde5e-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="cde5e-153">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="cde5e-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="cde5e-154">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="cde5e-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="cde5e-155">Valittujen lomatyyppien jaksotuksen keskeyttäminen</span><span class="sxs-lookup"><span data-stu-id="cde5e-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="cde5e-156">Voit luoda säännön, joka keskeyttää työntekijöiden lomaa ja palkatonta lomaa varten annettujen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="cde5e-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="cde5e-157">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="cde5e-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="cde5e-158">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="cde5e-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="cde5e-159">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten</span><span class="sxs-lookup"><span data-stu-id="cde5e-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="cde5e-160">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="cde5e-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="cde5e-161">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="cde5e-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="cde5e-162">Ympäristön uudet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="cde5e-162">New platform capabilities</span></span> 

<span data-ttu-id="cde5e-163">Kentistä voi tehdä pakollisia mukautuksia käyttämällä.</span><span class="sxs-lookup"><span data-stu-id="cde5e-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="cde5e-164">Tämä toiminto edellyttää **tallennettujen näkymien** ottamista käyttöön.</span><span class="sxs-lookup"><span data-stu-id="cde5e-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="cde5e-165">Työntekijän itsepalvelun nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="cde5e-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="cde5e-166">Human Resourcesin parametreissa on uusi vaihtoehto, jolla voi päivittää Työntekijän itsepalvelu -työtilan nimen itsepalveluksi.</span><span class="sxs-lookup"><span data-stu-id="cde5e-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="cde5e-167">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="cde5e-167">See also</span></span>

[<span data-ttu-id="cde5e-168">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="cde5e-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="cde5e-169">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="cde5e-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="cde5e-170">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="cde5e-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="cde5e-171">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="cde5e-171">Manage features</span></span>](hr-admin-manage-features.md)