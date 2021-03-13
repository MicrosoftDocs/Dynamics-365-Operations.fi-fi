---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (1. toukokuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 1. toukokuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
manager: tfehr
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7e41762e4283d5a4b0c9dd8359c5fb2bdabfc26
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127870"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a><span data-ttu-id="35766-103">Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (1. toukokuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="35766-103">What's new or changed in Dynamics 365 Human Resources (May 1, 2020)</span></span>

<span data-ttu-id="35766-104">Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="35766-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="35766-105">Muutokset koskevat koontiversion numeroa 8.1.3196.</span><span class="sxs-lookup"><span data-stu-id="35766-105">Changes apply to build number 8.1.3196.</span></span> <span data-ttu-id="35766-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="35766-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a><span data-ttu-id="35766-107">Uusia suorituskyvyn hallintayksiköitä käytettävissä Data Management Frameworkissa (DMF)</span><span class="sxs-lookup"><span data-stu-id="35766-107">New Performance Management entities available in Data Management Framework (DMF)</span></span>

<span data-ttu-id="35766-108">Seuraavat yksiköt ovat nyt käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="35766-108">The following entities are now available.</span></span> <span data-ttu-id="35766-109">Jos nämä yksiköt eivät näy yksikköluettelossa, käytä **Päivitä yksiköt** -asetusta kohdassa **Framework-parametrit > Yksikköasetukset > Päivitä yksikköluettelo**.</span><span class="sxs-lookup"><span data-stu-id="35766-109">If you don't see these entities listed in the entities list, use the **Refresh entities** option in **Framework Parameters > Entity settings > Refresh entity list**.</span></span>

- <span data-ttu-id="35766-110">**Keskustelun kompetenssi**</span><span class="sxs-lookup"><span data-stu-id="35766-110">**Discussion Competency**</span></span>
- <span data-ttu-id="35766-111">**Keskustelun tavoitteet**</span><span class="sxs-lookup"><span data-stu-id="35766-111">**Discussion Goals**</span></span>
- <span data-ttu-id="35766-112">**Keskustelun mittaus**</span><span class="sxs-lookup"><span data-stu-id="35766-112">**Discussion Measurement**</span></span>
- <span data-ttu-id="35766-113">**Keskustelun aihe**</span><span class="sxs-lookup"><span data-stu-id="35766-113">**Discussion Topic**</span></span>
- <span data-ttu-id="35766-114">**Suoritustason kirjauskansio**</span><span class="sxs-lookup"><span data-stu-id="35766-114">**Performance Journal**</span></span>
- <span data-ttu-id="35766-115">**Mittaus**</span><span class="sxs-lookup"><span data-stu-id="35766-115">**Measurement**</span></span>
- <span data-ttu-id="35766-116">**Tavoitten mittaus**</span><span class="sxs-lookup"><span data-stu-id="35766-116">**Goal Measurement**</span></span>

<span data-ttu-id="35766-117">Lisäksi **Keskustelu**-kohteeseen lisättiin **Kokonaispistemäärä** ja **Keskimääräiset pisteet**.</span><span class="sxs-lookup"><span data-stu-id="35766-117">In addition, **Total score** and **Average score** were added to the **Discussion** entity.</span></span>

## <a name="increase-length-of-leave-request-comments-275641"></a><span data-ttu-id="35766-118">Kasvata lomapyynnön kommenttien pituutta (275641)</span><span class="sxs-lookup"><span data-stu-id="35766-118">Increase length of leave request comments (275641)</span></span>

<span data-ttu-id="35766-119">Lomapyyntöjä koskevat kommentit sallivat nyt yli 100 merkkiä.</span><span class="sxs-lookup"><span data-stu-id="35766-119">Comments on leave requests now allow more than 100 characters.</span></span>

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a><span data-ttu-id="35766-120">Lopulliset kommentit eivät näy, kun esimies tai työntekijä on kirjautuneena eri yritykseen (431688)</span><span class="sxs-lookup"><span data-stu-id="35766-120">Final comments on reviews don't appear when the manager or employee is signed into a different company (431688)</span></span>

<span data-ttu-id="35766-121">Kaikki kommentit näkyvät nyt, kun tarkastelet arvioita.</span><span class="sxs-lookup"><span data-stu-id="35766-121">All comments will now appear when viewing reviews.</span></span>

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a><span data-ttu-id="35766-122">Uusi työntekijälomake ei tue käyttäjän määrittämiä linkkejä (390374)</span><span class="sxs-lookup"><span data-stu-id="35766-122">User-defined links aren't supported on new Worker form (390374)</span></span>

<span data-ttu-id="35766-123">Käyttäjän määrittämät linkit ovat nyt käytössä tehokkaassa **työntekijä**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="35766-123">User-defined links are now enabled on the streamlined **Worker** form.</span></span>

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a><span data-ttu-id="35766-124">HcmRatingLevelEntity aiheuttaa OData-ohjelmointirajapinnan kaatumisen (439476)</span><span class="sxs-lookup"><span data-stu-id="35766-124">HcmRatingLevelEntity causes OData API crash (439476)</span></span>

<span data-ttu-id="35766-125">Tämä muutos korjaa ohjelmointirajapinnan kaatumisen.</span><span class="sxs-lookup"><span data-stu-id="35766-125">This change corrects the API crash.</span></span> <span data-ttu-id="35766-126">Samanlainen nimi aiheutti tämän virheen.</span><span class="sxs-lookup"><span data-stu-id="35766-126">A duplicate name cased this error.</span></span>

## <a name="in-preview"></a><span data-ttu-id="35766-127">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="35766-127">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="35766-128">Loman keskeytys</span><span class="sxs-lookup"><span data-stu-id="35766-128">Leave suspension</span></span>

<span data-ttu-id="35766-129">Voit keskeyttää työntekijän loman ja poissaolon henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="35766-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="35766-130">Loman keskeyttäminen pysäyttää valittujen lomatyyppien lomajaksotukset.</span><span class="sxs-lookup"><span data-stu-id="35766-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="35766-131">Jos keskeytys tapahtuu jaksotuksen käsittelyn jälkeen, loman keskeyttäminen luo suhteutetun oikaisun työntekijän lomasaldoon.</span><span class="sxs-lookup"><span data-stu-id="35766-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="35766-132">Lisätietoja on kohdassa [Loman keskeytys](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="35766-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="35766-133">Päivitä käyttäjäkokemus osoittamaan, että jaksotus on keskeytetty (429550)</span><span class="sxs-lookup"><span data-stu-id="35766-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="35766-134">Käyttökokemus ilmaisee nyt, että jaksotus on keskeytetty suunnitelmaa varten.</span><span class="sxs-lookup"><span data-stu-id="35766-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="35766-135">Valitun lomatyypin kertymän keskeyttäminen (272447)</span><span class="sxs-lookup"><span data-stu-id="35766-135">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="35766-136">Tässä julkaisussa HR voi luoda säännön, joka keskeyttää työntekijöiden loma- ja palkatonta lomaa varten syötettyjen lomapyyntöjen maksamisen.</span><span class="sxs-lookup"><span data-stu-id="35766-136">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="35766-137">Palkaton vapaa voi olla tyyppi, mutta sen ei tarvitse olla.</span><span class="sxs-lookup"><span data-stu-id="35766-137">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="35766-138">Voit keskeyttää minkä tahansa toiseen lomatyyppiin perustuvan loman.</span><span class="sxs-lookup"><span data-stu-id="35766-138">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="35766-139">DMF-yksikkö käytettävissä suoriteperusteisia keskeytyksiä varten (429549)</span><span class="sxs-lookup"><span data-stu-id="35766-139">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="35766-140">DMF-yksikkö on nyt käytettävissä suoriteperusteisia keskeytyksiä varten.</span><span class="sxs-lookup"><span data-stu-id="35766-140">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="35766-141">Lisää syykoodi jaksotuskeskeytyksiin (429547)</span><span class="sxs-lookup"><span data-stu-id="35766-141">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="35766-142">Syykoodit on lisätty kertymän keskeyttämiseen.</span><span class="sxs-lookup"><span data-stu-id="35766-142">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="35766-143">Aloita siirryttäessä henkilöstöhallinnon parametreista loma- ja poissaoloparametreihin</span><span class="sxs-lookup"><span data-stu-id="35766-143">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="35766-144">Tämä julkaisu alkaa yhdistää henkilöstöhallinnon parametreja loma- ja poissaoloparametreihin.</span><span class="sxs-lookup"><span data-stu-id="35766-144">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="35766-145">Siirtokirjauksen suorituksen säännöt</span><span class="sxs-lookup"><span data-stu-id="35766-145">Carry forward rules</span></span>

<span data-ttu-id="35766-146">Voit määrittää siirrettäville saldoille siirtosäännön, johon on siirto-oikaisut siirretään.</span><span class="sxs-lookup"><span data-stu-id="35766-146">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="35766-147">Jos työntekijä esimerkiksi siirtää vapaata kymmenen päivää eteenpäin, voit valita eri lomatyypin näiksi 10 päiväksi.</span><span class="sxs-lookup"><span data-stu-id="35766-147">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="35766-148">Lisätietoja on kohdassa [Loma- ja poissaolotyyppien määrittäminen](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="35766-148">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="35766-149">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="35766-149">Known issues</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="35766-150">SharePoint-esikatselu ei toimi joissakin ympäristöissä</span><span class="sxs-lookup"><span data-stu-id="35766-150">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="35766-151">Jos SharePoint-ohjelmassa tallennettujen asiakirjojen esikatselu ei toimi, kokeile seuraavia toimia:</span><span class="sxs-lookup"><span data-stu-id="35766-151">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="35766-152">Tarkista, että järjestelmänvalvojakäyttäjätilillä on käyttäjätietueeseen liittyvä sähköpostiviesti.</span><span class="sxs-lookup"><span data-stu-id="35766-152">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="35766-153">Voit tarkastella näitä tietoja **Käyttäjä**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="35766-153">You can view this information in the **User** page.</span></span> <span data-ttu-id="35766-154">Jos sähköpostia ei ole määritetty, sähköposti ja palveluntarjoaja on lisättävä OData Excel-lisäosaasi.</span><span class="sxs-lookup"><span data-stu-id="35766-154">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="35766-155">Oletusarvon mukaan sähköpostiosoitetta ei ole Excelin suunnittelussa.</span><span class="sxs-lookup"><span data-stu-id="35766-155">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="35766-156">Sinun on muokattava Excelin rakennetta, lisättävä kaikki kentät, otettava käyttöön ja päivitettävä.</span><span class="sxs-lookup"><span data-stu-id="35766-156">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="35766-157">Kun olet tehnyt nämä vaiheet, voit päivittää järjestelmänvalvojatilin.</span><span class="sxs-lookup"><span data-stu-id="35766-157">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="35766-158">Kun järjestelmänvalvojatiliin on liitetty sähköpostitili, kirjaudu henkilöstöresursseihin järjestelmänvalvojan tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="35766-158">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="35766-159">Avaa tiedoston esikatselu SharePoint-sovelluksen avulla.</span><span class="sxs-lookup"><span data-stu-id="35766-159">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="35766-160">Kirjaudu sisään toisella käyttäjätilillä, jolla on liitteiden käyttöoikeus, ja varmista, että esikatselu toimii odotetulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="35766-160">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="35766-161">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="35766-161">See also</span></span>

[<span data-ttu-id="35766-162">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="35766-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="35766-163">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="35766-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="35766-164">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="35766-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="35766-165">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="35766-165">Manage features</span></span>](hr-admin-manage-features.md)