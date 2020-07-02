---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2020)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 37f21fffe209e17a6fe89c2661e49fc0dc8b9655
ms.sourcegitcommit: 88f38d584c5befb96e4d1daab4b28af5519ef125
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/11/2020
ms.locfileid: "3443461"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="b5cb4-103">Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (28. toukokuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="b5cb4-104">Tässä ohjeaiheessa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="b5cb4-105">Muutokset koskevat koontiversion numeroa 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="b5cb4-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="b5cb4-107">LeaveRequest-yksikkö ei toimi, kun otat käyttöön useita tyyppejä per lomasuunnitelma (447498)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="b5cb4-108">Tämän muutoksen avulla **LeaveEnrollmentV2Entity** on nyt käytettävissä korjaamaan virheen, joka ilmenee, kun otat käyttöön useita lomatyyppejä.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="b5cb4-109">Erän varausvirheen vähennystoiminto (esikatselu) (446619)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="b5cb4-110">Kun otat tämän toiminnon käyttöön, voit odottaa eräkehystaulujen eston vähentämistä, kun valitset tehtäviä ja viimeistelytöitä.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="b5cb4-111">UpdateConflict työntekijän tallennuksen aikana estää tietueen muokkaamisen henkilöillä (427915)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="b5cb4-112">Tämä muutos korjaa virheen, kun uusi työntekijä lisätään, osoitetiedot päivitetään ja kieliasetus muutetaan.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="b5cb4-113">Tässä ainutlaatuisessa skenaariossa tietuetta ilmaisevaa virhettä ei voitu päivittää.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="b5cb4-114">Liitettä ei voi lisätä hyväksyttyyn lomapyyntöön uudelleen lähettämistä varten (425407)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="b5cb4-115">Tämä muutos sallii nyt liitteiden lisäämisen hyväksyttyihin lomapyyntöihin.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="b5cb4-116">Käyttäjä voi lisätä työntekijälle kompensaation toisessa yrityslomakkeessa (409529)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="b5cb4-117">Tämä muutos poistaa käytöstä kompensaatioasetukset, jotka estävät väärän yrityksen kompensaatiotietojen tahattoman syötön.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="b5cb4-118">Virhe siirrettäessä työntekijää ja työntekijän toimen määrityspäivämäärä on ennen toimen kestoa (429402)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="b5cb4-119">Virhesanomat, kun työntekijä siirretään tässä skenaariossa, on päivitetty kuvaamaan paremmin ongelman korjaamiseen tarvittavia muutoksia.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="b5cb4-120">Liiteominaisuudet työntekijöiden itsepalvelussa hyödyttävät ilmoittautumista</span><span class="sxs-lookup"><span data-stu-id="b5cb4-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="b5cb4-121">Voit nyt lisätä liitteitä etuuksien rekisteröintiprosessin aikana jokaiselle suunnitelmalle, johon työntekijä on ilmoittautumassa.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="b5cb4-122">Tämän jälkeen voit tarkastella liitteitä **Työntekijän kirjatut edut** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b5cb4-123">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="b5cb4-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="b5cb4-124">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="b5cb4-124">Human Resources application in Teams</span></span>

<span data-ttu-id="b5cb4-125">Työntekijät voivat tarkastella ja pyytää lomaa työstä Microsoft Teamsissä.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="b5cb4-126">Ne voivat olla vuorovaikutuksessa botin kanssa luodakseen lomapyyntöjä.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="b5cb4-127">Lisätietoja on kohdassa [Human Resources -sovellus Teamsissa](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="b5cb4-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="b5cb4-128">Loman keskeytys</span><span class="sxs-lookup"><span data-stu-id="b5cb4-128">Leave suspension</span></span>

<span data-ttu-id="b5cb4-129">Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="b5cb4-130">Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="b5cb4-131">Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="b5cb4-132">Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb4-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="b5cb4-133">Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="b5cb4-134">Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b5cb4-135">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="b5cb4-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="b5cb4-136">Tietokannan kirjaaminen (kesäkuussa esikatselussa)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="b5cb4-137">Tietokannan kirjaamistoiminnon avulla voit määrittää, mitä taulua ja kenttiä seurataan.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="b5cb4-138">Sen avulla voit myös määrittää tapahtumat, jotka käynnistävät muutosten seurannan.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="b5cb4-139">Kyselytoiminnot ovat käytettävissä, jotta nämä muutokset tulevat näkyviin ajan mittaan.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="b5cb4-140">Loman vaihtaminen rahaksi ja lomapalkan vaihtaminen vapaaksi (esikatselussa 1. kesäkuuta)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="b5cb4-141">Jotkut organisaatiot tarjoavat edun, jonka avulla työntekijät voivat vaihtaa lomaa rahaksi tai rahaa vapaaksi.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="b5cb4-142">Tätä prosessia hallitaan usein manuaalisesti.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-142">This process is often managed manually.</span></span> <span data-ttu-id="b5cb4-143">Tämän toiminnon avulla voit hallita HR-osaston käytäntöjä ja pyyntöjä entistä automatisoidummin. Se auttaa poistamaan virheitä ja virtaviivaistamaan lomanhallintaprosessia.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="b5cb4-144">Lisätietoja:</span><span class="sxs-lookup"><span data-stu-id="b5cb4-144">For more information, see:</span></span>

- [<span data-ttu-id="b5cb4-145">Käytäntöjen hallinta loman vaihtamisessa rahaksi ja lomapalkan vaihtamisessa vapaaksi</span><span class="sxs-lookup"><span data-stu-id="b5cb4-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="b5cb4-146">Vaihda lomaa rahaksi tai lomapalkka vapaaksi</span><span class="sxs-lookup"><span data-stu-id="b5cb4-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="b5cb4-147">Tietojen hallintakehys (DMF) -yksiköt etuuksien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="b5cb4-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="b5cb4-148">Etujen hallintayksiköt julkaisevat.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="b5cb4-149">DMF-yksiköt sallivat tietojen tuomisen ja viemisen, jotta etuuksien hallinta voidaan määrittää helposti.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="b5cb4-150">Tietojen siirtämiseen on käytettävissä myös etujen hallintamalli.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="b5cb4-151">Malli vie tiedot ja tuo ne peräkkäisessä järjestyksessä tietoriippuvuuksien noudattamista varten.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="b5cb4-152">Lisää syykoodi jaksotuskeskeytyksiin (Kesäkuun 1.)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="b5cb4-153">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="b5cb4-154">Siirtokirjauksen suorituksen säännöt (Kesäkuun 1.)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="b5cb4-155">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="b5cb4-156">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="b5cb4-157">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="b5cb4-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="b5cb4-158">Valitun lomatyypin kertymän keskeyttäminen (Kesäkuun 1.)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="b5cb4-159">Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="b5cb4-160">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="b5cb4-161">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="b5cb4-162">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (Kesäkuun 1.)</span><span class="sxs-lookup"><span data-stu-id="b5cb4-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="b5cb4-163">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="b5cb4-163">A DMF entity is now available for accrual suspensions.</span></span>