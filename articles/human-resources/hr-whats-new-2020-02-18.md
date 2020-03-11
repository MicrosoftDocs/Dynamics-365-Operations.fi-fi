---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (18. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 96e66c86e98cc1cfee82221da06f9c57a17d170b
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/20/2020
ms.locfileid: "3077458"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="04cf6-103">Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (18. helmikuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="04cf6-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="04cf6-104">Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="04cf6-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="04cf6-105">Muutokset koskevat koontiversion numeroa 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="04cf6-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="04cf6-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="04cf6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="04cf6-107">Ympäristön update 32 -päivitys</span><span class="sxs-lookup"><span data-stu-id="04cf6-107">Platform update 32</span></span> 

<span data-ttu-id="04cf6-108">Platform Update 32 on nyt saatavana.</span><span class="sxs-lookup"><span data-stu-id="04cf6-108">Platform update 32 is now available.</span></span> <span data-ttu-id="04cf6-109">Lisätietoja on kohdassa [Finance and Operations -sovellusten Platform update 32:n uudet ja muuttuneet ominaisuudet (helmikuu 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="04cf6-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="04cf6-110">Hakuarvot muistetaan, kun muutat näkymäasetuksia tehostetussa työntekijälomakkeessa (383833)</span><span class="sxs-lookup"><span data-stu-id="04cf6-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="04cf6-111">Uusi **työntekijälomake** muistaa nyt hakuarvot, kun muutat näkymän asetuksia ja otat muutokset käyttöön.</span><span class="sxs-lookup"><span data-stu-id="04cf6-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="04cf6-112">Kompensaation hallinnan yhteenvetoruudut esikatselutoiminnon uudelleenohjauksesta väärään muotoon (401861)</span><span class="sxs-lookup"><span data-stu-id="04cf6-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="04cf6-113">Pysyvät ja muuttuvat kompensaation hallinnan ruudut näyttävät nyt oikeat tiedot uudessa **työntekijälomakkeessa**.</span><span class="sxs-lookup"><span data-stu-id="04cf6-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="04cf6-114">Koskee vain tehostettua työntekijälomakkeen esikatselutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="04cf6-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="04cf6-115">Voit ottaa tämän esikatselutoiminnon käyttöön **ominaisuuksien hallinnassa**.</span><span class="sxs-lookup"><span data-stu-id="04cf6-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="04cf6-116">Lisätietoja on ohjeaiheessa [Toimintojen hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="04cf6-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="04cf6-117">Joidenkin lomapyyntötietueiden tyhjä Tila-kenttä Common Data Servicessä (414915)</span><span class="sxs-lookup"><span data-stu-id="04cf6-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="04cf6-118">Tämä muutos korjaa ongelman Common Data Servicessä, kun lomapyynnön **Tila**-kentän arvoksi on määritetty **Tarkistus**.</span><span class="sxs-lookup"><span data-stu-id="04cf6-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="04cf6-119">Common Data Service ilmaisee nyt tilan.</span><span class="sxs-lookup"><span data-stu-id="04cf6-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="04cf6-120">Osaamisalueaukkoanalyysi on mahdollinen vain määritetylle työlle (411390)</span><span class="sxs-lookup"><span data-stu-id="04cf6-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="04cf6-121">Voit tehdä osaamisalueaukkoanalyysin mille tahansa Human Resources -sovelluksen määritetylle työlle.</span><span class="sxs-lookup"><span data-stu-id="04cf6-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="04cf6-122">Järjestelmän valuuttaa ei synkronoida Common Data Servicestä Human Resources -sovellukseen uusissa ympäristöissä (418011)</span><span class="sxs-lookup"><span data-stu-id="04cf6-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="04cf6-123">Common Data Servicen järjestelmän valuutan voi nyt synkronoida Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="04cf6-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="04cf6-124">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="04cf6-124">In preview</span></span>

- [<span data-ttu-id="04cf6-125">Lomien ja poissaolojen esikatseluominaisuudet</span><span class="sxs-lookup"><span data-stu-id="04cf6-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="04cf6-126">Etujen hallinnan esikatseluominaisuudet</span><span class="sxs-lookup"><span data-stu-id="04cf6-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="04cf6-127">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="04cf6-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="04cf6-128">Päivitetty Common Data Service -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="04cf6-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="04cf6-129">Uusi Common Data Service -ratkaisu tulee pian saataville seuraavin muutoksin:</span><span class="sxs-lookup"><span data-stu-id="04cf6-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="04cf6-130">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="04cf6-130">Description</span></span> | <span data-ttu-id="04cf6-131">Muutos</span><span class="sxs-lookup"><span data-stu-id="04cf6-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="04cf6-132">**Työn/toimen** yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="04cf6-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="04cf6-133">**Kompensaatioalue** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-133">**Compensation region** added</span></span></br><span data-ttu-id="04cf6-134">**Taloushallinnon dimensiot** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="04cf6-135">**Työntekijä**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="04cf6-135">**Worker** entity changes</span></span> | <span data-ttu-id="04cf6-136">**Nimien järjestys** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-136">**Name sequence** added</span></span></br><span data-ttu-id="04cf6-137">**Työskentelee kotoa** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-137">**Works from home** added</span></span></br><span data-ttu-id="04cf6-138">**Kieliä** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-138">**Language** added</span></span></br><span data-ttu-id="04cf6-139">**Ikälisäpäivä** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-139">**Seniority date** added</span></span></br><span data-ttu-id="04cf6-140">**Vuosipäivän päivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-140">**Anniversary date** added</span></span></br><span data-ttu-id="04cf6-141">**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-141">**Original hire date** added</span></span> |
| <span data-ttu-id="04cf6-142">**Työsuhde**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="04cf6-142">**Employment** entity changes</span></span> | <span data-ttu-id="04cf6-143">**Taloushallinnon dimensiot** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-143">**Financial dimensions** added</span></span></br><span data-ttu-id="04cf6-144">**Irtisanomisen syy** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-144">**Termination reason** added</span></span></br><span data-ttu-id="04cf6-145">**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</span><span class="sxs-lookup"><span data-stu-id="04cf6-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="04cf6-146">**Koeajan päivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-146">**Probation date** added</span></span> |
| <span data-ttu-id="04cf6-147">**Työntekijän osoite**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="04cf6-147">**Worker address** entity changes</span></span> | <span data-ttu-id="04cf6-148">**Katuosoite** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-148">**Street address** added</span></span></br><span data-ttu-id="04cf6-149">**Osoiterivi 1**, **Osoiterivi 2**ja **Osoiterivi 3**, jotka on merkitty poistettaviksi</span><span class="sxs-lookup"><span data-stu-id="04cf6-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="04cf6-150">Uudet muuttuvat kompensaatioasetusten entiteetit</span><span class="sxs-lookup"><span data-stu-id="04cf6-150">New variable compensation setup entities</span></span> | <span data-ttu-id="04cf6-151">**Muuttuvan kompensaatiosuunnitelman tyyppi**</span><span class="sxs-lookup"><span data-stu-id="04cf6-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="04cf6-152">**Muuttuva kompensaatiosuunnitelma**</span><span class="sxs-lookup"><span data-stu-id="04cf6-152">**Compensation variable plan**</span></span></br><span data-ttu-id="04cf6-153">**Hyvityssäännöt**</span><span class="sxs-lookup"><span data-stu-id="04cf6-153">**Vesting rules**</span></span></br><span data-ttu-id="04cf6-154">**Muuttuvan kompensaatiosuunnitelman taso**</span><span class="sxs-lookup"><span data-stu-id="04cf6-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="04cf6-155">Uusi **Työntekijäkalenterin työ**-yksikkö</span><span class="sxs-lookup"><span data-stu-id="04cf6-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="04cf6-156">**Työkalenteriyksikkö** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="04cf6-157">Uusi **Palkanlaskennan toimen tiedot** -yksikkö</span><span class="sxs-lookup"><span data-stu-id="04cf6-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="04cf6-158">**Palkanlaskennan toimen tiedot** lisätty</span><span class="sxs-lookup"><span data-stu-id="04cf6-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="04cf6-159">Uusi **Otsikko**-yksikkö</span><span class="sxs-lookup"><span data-stu-id="04cf6-159">New **Title** entity</span></span> | <span data-ttu-id="04cf6-160">**Otsikko** lisätty.</span><span class="sxs-lookup"><span data-stu-id="04cf6-160">**Title** added.</span></span> <span data-ttu-id="04cf6-161">Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Common Data Service -sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="04cf6-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="04cf6-162">Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä.</span><span class="sxs-lookup"><span data-stu-id="04cf6-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="04cf6-163">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="04cf6-163">See also</span></span>

[<span data-ttu-id="04cf6-164">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="04cf6-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="04cf6-165">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="04cf6-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="04cf6-166">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="04cf6-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="04cf6-167">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="04cf6-167">Manage features</span></span>](hr-admin-manage-features.md)