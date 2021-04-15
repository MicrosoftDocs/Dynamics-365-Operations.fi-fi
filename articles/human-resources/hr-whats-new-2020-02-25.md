---
title: Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Human Resourcesin 25. helmikuuta 2020 julkaistuja uusia tai muuttuneita ominaisuuksia.
author: andreabichsel
ms.date: 02/25/2020
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
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc79c464f74961fd431f1d42583e4dcd67c30fb9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790401"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a><span data-ttu-id="6d65c-103">Dynamics 365 Human Resourcesin uudet tai muuttuneet ominaisuudet (25. helmikuuta 2020)</span><span class="sxs-lookup"><span data-stu-id="6d65c-103">What's new or changed in Dynamics 365 Human Resources (February 25, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6d65c-104">Tässä artikkelissa käsitellään Dynamics 365 Human Resourcesin uusia tai muuttuneita toimintoja.</span><span class="sxs-lookup"><span data-stu-id="6d65c-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6d65c-105">Muutokset koskevat koontiversion numeroa 8.1.2927.</span><span class="sxs-lookup"><span data-stu-id="6d65c-105">Changes apply to build number 8.1.2927.</span></span> <span data-ttu-id="6d65c-106">Joissakin otsikoissa suluissa olevat luvut viittaavat tukinumeroihin LCS-palveluissa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a><span data-ttu-id="6d65c-107">Palvelupyyntöjen hallinnan siirtymisen ja tietojen hallinnan kehyksen (DMF) yksikön (414754) käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="6d65c-107">Enable Case Management navigation and data management framework (DMF) entity (414754)</span></span>

<span data-ttu-id="6d65c-108">Tämä esikatselutoiminto ottaa käyttöön lisänavigoinnin palvelupyyntöjen hallinnan palvelupyyntöjä varten.</span><span class="sxs-lookup"><span data-stu-id="6d65c-108">This preview feature enables additional navigation to case management cases.</span></span> <span data-ttu-id="6d65c-109">Voit ottaa tämän esikatselutoiminnon käyttöön **Toimintojen hallinta** -työtilassa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-109">You can enable this preview feature in the **Feature Management** workspace.</span></span> <span data-ttu-id="6d65c-110">Nämä valikkovaihtoehdot näkyvät **Yhteensopivuus**-työtilassa  Dynamics 365 Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-110">These menu items appear in the **Compliance** workspace of Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6d65c-111">Tämän muutoksen avulla Human Resources voi tehdä seuraavaa:</span><span class="sxs-lookup"><span data-stu-id="6d65c-111">With this change, Human Resources can access:</span></span>

- <span data-ttu-id="6d65c-112">Kaikki tapaukset</span><span class="sxs-lookup"><span data-stu-id="6d65c-112">All cases</span></span>
- <span data-ttu-id="6d65c-113">Omat tapaukset</span><span class="sxs-lookup"><span data-stu-id="6d65c-113">My cases</span></span>
- <span data-ttu-id="6d65c-114">Omat avoimet tapaukset</span><span class="sxs-lookup"><span data-stu-id="6d65c-114">My open cases</span></span>
- <span data-ttu-id="6d65c-115">Erääntyneet tapaukset</span><span class="sxs-lookup"><span data-stu-id="6d65c-115">My overdue cases</span></span>
- <span data-ttu-id="6d65c-116">Työnkulun avulla minulle määritetyt tapaukset</span><span class="sxs-lookup"><span data-stu-id="6d65c-116">Cases assigned to me through workflow</span></span>

<span data-ttu-id="6d65c-117">Näiden uusien palvelupyyntönäkymien avulla käytettävissä on myös **Palvelupyynnön tiedot** -DMF-yksikkö.</span><span class="sxs-lookup"><span data-stu-id="6d65c-117">Along with these new views into cases, the **Case detail** DMF entity is also available.</span></span>

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a><span data-ttu-id="6d65c-118">Suhteen määritysten käyttöönotto yleisessä osoitekirjassa (414762)</span><span class="sxs-lookup"><span data-stu-id="6d65c-118">Enable Relationship definitions in global address bBook (414762)</span></span>

<span data-ttu-id="6d65c-119">Yhteydet ovat nyt käytössä yleisessä osoitekirjassa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-119">Relationships are now enabled in the global address book.</span></span> <span data-ttu-id="6d65c-120">Ennen tämän viikon julkaisua **Suhde**-tietoruutu näytti kaikki järjestelmän määrittämät suhteet.</span><span class="sxs-lookup"><span data-stu-id="6d65c-120">Prior to this week's release, the **Relationship** fact box displayed any system-defined relationships.</span></span> <span data-ttu-id="6d65c-121">Nyt voit määrittää nämä suhteet yleisen osoitekirjan sivulla.</span><span class="sxs-lookup"><span data-stu-id="6d65c-121">Now you can define those relationships within the global address book page.</span></span>

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a><span data-ttu-id="6d65c-122">Toimi voidaan poistaa, kun toimella on aktiivisia kompensaatiotietueita (414568)</span><span class="sxs-lookup"><span data-stu-id="6d65c-122">A position can be removed when active compensation records exist for the position (414568)</span></span>

<span data-ttu-id="6d65c-123">Tämän muutoksen myötä näkyviin tulee varoitus, jos yrität poistaa toimen ja työntekijällä on aktiivinen kompensaatiotietue samaa toimea varten.</span><span class="sxs-lookup"><span data-stu-id="6d65c-123">With this change, a warning appears when you attempt to delete a position and a worker has an active compensation record for that same position.</span></span> <span data-ttu-id="6d65c-124">Jos näin käy, työntekijän kiinteä kompensaatiotietue on päivitettävä ennen toimen poistamista.</span><span class="sxs-lookup"><span data-stu-id="6d65c-124">When this happens, you must update the employee fixed compensation record before removing the position.</span></span>

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a><span data-ttu-id="6d65c-125">Suorituskyvyn tarkistuksen työnkulku lisää joskus kuittaukset henkilöiltä, jotka eivät ole prosessin osa (414171)</span><span class="sxs-lookup"><span data-stu-id="6d65c-125">Performance review workflow occasionally adds sign-offs from people who are not part of the process (414171)</span></span>

<span data-ttu-id="6d65c-126">Tämä muutos korjaa ongelman, jossa kirjausten lisäosallistujat lisätään suorituskyvyn arvioon.</span><span class="sxs-lookup"><span data-stu-id="6d65c-126">This change corrects an issue where additional sign-off participants are added to the performance review.</span></span>

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a><span data-ttu-id="6d65c-127">Työntekijän toimen tehtävää ei luoda Dataversessä, kun valinta tehdään Uusi työntekijä -valintaikkunassa (413479)</span><span class="sxs-lookup"><span data-stu-id="6d65c-127">Worker position assignment not created in Dataverse when selected on the New Worker dialog (413479)</span></span>

<span data-ttu-id="6d65c-128">Tämä muutos korjaa ongelman, kun uusi työntekijä palkataan ja tämä liitetään toimeen **Uusi työntekijä** -valintaikkunassa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-128">This change corrects an issue when hiring a new worker and assigning the new hire to a position through the **New worker** dialog.</span></span> <span data-ttu-id="6d65c-129">Nyt toimen tehtävä näkyy Dataverse -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-129">Now the position assignment is reflected in Dataverse.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6d65c-130">Tulossa pian</span><span class="sxs-lookup"><span data-stu-id="6d65c-130">Coming soon</span></span>

### <a name="updated-dataverse-solution"></a><span data-ttu-id="6d65c-131">Päivitetty Dataverse -ratkaisu</span><span class="sxs-lookup"><span data-stu-id="6d65c-131">Updated Dataverse solution</span></span>

<span data-ttu-id="6d65c-132">Uusi Dataverse -ratkaisu tulee pian saataville seuraavin muutoksin:</span><span class="sxs-lookup"><span data-stu-id="6d65c-132">A new Dataverse solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="6d65c-133">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="6d65c-133">Description</span></span> | <span data-ttu-id="6d65c-134">Muutos</span><span class="sxs-lookup"><span data-stu-id="6d65c-134">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="6d65c-135">**Työn/toimen** yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="6d65c-135">**Job/Position** entity changes</span></span> | <span data-ttu-id="6d65c-136">**Kompensaatioalue** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-136">**Compensation region** added</span></span></br><span data-ttu-id="6d65c-137">**Taloushallinnon dimensiot** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-137">**Financial dimensions** added</span></span> |
| <span data-ttu-id="6d65c-138">**Työntekijä**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="6d65c-138">**Worker** entity changes</span></span> | <span data-ttu-id="6d65c-139">**Nimien järjestys** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-139">**Name sequence** added</span></span></br><span data-ttu-id="6d65c-140">**Työskentelee kotoa** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-140">**Works from home** added</span></span></br><span data-ttu-id="6d65c-141">**Kieliä** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-141">**Language** added</span></span></br><span data-ttu-id="6d65c-142">**Ikälisäpäivä** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-142">**Seniority date** added</span></span></br><span data-ttu-id="6d65c-143">**Vuosipäivän päivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-143">**Anniversary date** added</span></span></br><span data-ttu-id="6d65c-144">**Alkuperäinen työsuhteen alkamispäivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-144">**Original hire date** added</span></span> |
| <span data-ttu-id="6d65c-145">**Työsuhde**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="6d65c-145">**Employment** entity changes</span></span> | <span data-ttu-id="6d65c-146">**Taloushallinnon dimensiot** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-146">**Financial dimensions** added</span></span></br><span data-ttu-id="6d65c-147">**Irtisanomisen syy** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-147">**Termination reason** added</span></span></br><span data-ttu-id="6d65c-148">**Päättymispäivämäärä** nimettiin uudelleen **Siirtymäpäivästä**</span><span class="sxs-lookup"><span data-stu-id="6d65c-148">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="6d65c-149">**Koeajan päivämäärä** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-149">**Probation date** added</span></span> |
| <span data-ttu-id="6d65c-150">**Työntekijän osoite**-yksikön muutokset</span><span class="sxs-lookup"><span data-stu-id="6d65c-150">**Worker address** entity changes</span></span> | <span data-ttu-id="6d65c-151">**Katuosoite** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-151">**Street address** added</span></span></br><span data-ttu-id="6d65c-152">**Osoiterivi 1**, **Osoiterivi 2** ja **Osoiterivi 3**, jotka on merkitty poistettaviksi</span><span class="sxs-lookup"><span data-stu-id="6d65c-152">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="6d65c-153">Uudet muuttuvat kompensaatioasetusten entiteetit</span><span class="sxs-lookup"><span data-stu-id="6d65c-153">New variable compensation setup entities</span></span> | <span data-ttu-id="6d65c-154">**Muuttuvan kompensaatiosuunnitelman tyyppi**</span><span class="sxs-lookup"><span data-stu-id="6d65c-154">**Compensation variable plan type**</span></span></br><span data-ttu-id="6d65c-155">**Muuttuva kompensaatiosuunnitelma**</span><span class="sxs-lookup"><span data-stu-id="6d65c-155">**Compensation variable plan**</span></span></br><span data-ttu-id="6d65c-156">**Hyvityssäännöt**</span><span class="sxs-lookup"><span data-stu-id="6d65c-156">**Vesting rules**</span></span></br><span data-ttu-id="6d65c-157">**Muuttuvan kompensaatiosuunnitelman taso**</span><span class="sxs-lookup"><span data-stu-id="6d65c-157">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="6d65c-158">Uusi **Työntekijäkalenterin työ**-yksikkö</span><span class="sxs-lookup"><span data-stu-id="6d65c-158">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="6d65c-159">**Työkalenteriyksikkö** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-159">**Work calendar entity** added</span></span> |
| <span data-ttu-id="6d65c-160">Uusi **Palkanlaskennan toimen tiedot** -yksikkö</span><span class="sxs-lookup"><span data-stu-id="6d65c-160">New **Payroll position detail** entity</span></span> | <span data-ttu-id="6d65c-161">**Palkanlaskennan toimen tiedot** lisätty</span><span class="sxs-lookup"><span data-stu-id="6d65c-161">**Payroll position detail** added</span></span> |
| <span data-ttu-id="6d65c-162">Uusi **Otsikko**-yksikkö</span><span class="sxs-lookup"><span data-stu-id="6d65c-162">New **Title** entity</span></span> | <span data-ttu-id="6d65c-163">**Otsikko** lisätty.</span><span class="sxs-lookup"><span data-stu-id="6d65c-163">**Title** added.</span></span> <span data-ttu-id="6d65c-164">Uusi **Otsikko**-yksikkö sisältyy synkronointiprosessiin Human Resources- ja Dataverse -sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="6d65c-164">The new **Title** entity will be included in the sync process between Human Resources and Dataverse.</span></span> <span data-ttu-id="6d65c-165">Siihen ei aluksi viitata **Työn sijainti**- tai **Työ**-yksiköissä.</span><span class="sxs-lookup"><span data-stu-id="6d65c-165">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

<span data-ttu-id="6d65c-166">Seuraavien viikkojen aikana nämä yksikön muutokset ovat käytettävissä kaikissa ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="6d65c-166">Over the next few weeks, these entity changes will be available in all environments.</span></span> <span data-ttu-id="6d65c-167">Voit asentaa Human Resources -sovelluksen uusimman Dataverse -ratkaisun manuaalisesti seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="6d65c-167">To manually install the latest Dataverse solution for Human Resources:</span></span>

1.  <span data-ttu-id="6d65c-168">Siirry [Power Platform-hallintakeskukseen](https://admin.powerplatform.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="6d65c-168">Go to the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com).</span></span>

2.  <span data-ttu-id="6d65c-169">Valitse **Ympäristö**.</span><span class="sxs-lookup"><span data-stu-id="6d65c-169">Select **Environments**.</span></span>

3.  <span data-ttu-id="6d65c-170">Etsi ympäristö, jonka haluat päivittää.</span><span class="sxs-lookup"><span data-stu-id="6d65c-170">Find the environment you want to upgrade.</span></span> <span data-ttu-id="6d65c-171">Tämän on vastattava Human Resources -sovelluksen **ympäristön nimeä** **Common Data Service -tiedot** -osan **Tietoja**-lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="6d65c-171">This should correspond to **Environment name** in the **Common Data Service information** section in the **About** form in Human Resources.</span></span>

4.  <span data-ttu-id="6d65c-172">Valitse ympäristö, jos haluat tarkastella ympäristön tietoja.</span><span class="sxs-lookup"><span data-stu-id="6d65c-172">Select the environment to view the environment details.</span></span>

5.  <span data-ttu-id="6d65c-173">Valitse **Hallitse ratkaisuja** -painike yläosan toimintopalkista.</span><span class="sxs-lookup"><span data-stu-id="6d65c-173">In the action bar at the top, select **Manage Solutions**.</span></span> <span data-ttu-id="6d65c-174">Näyttöön avautuu uusi selainikkuna. Siirry **Dynamics 365 -hallintakeskukseen** ympäristössäsi.</span><span class="sxs-lookup"><span data-stu-id="6d65c-174">A new browser window will open and navigate to **Dynamics 365 Administration Center** in the context of your environment.</span></span>

6.  <span data-ttu-id="6d65c-175">Valitse **Ratkaisu**-luettelossa **Dynamics 365 Human Resources -ankkuri**.</span><span class="sxs-lookup"><span data-stu-id="6d65c-175">In the **Solution** list, select **Dynamics 365 Human Resources Anchor**.</span></span>

7.  <span data-ttu-id="6d65c-176">Ota uusin ratkaisu käyttöön valitsemalla **Päivitä versio**.</span><span class="sxs-lookup"><span data-stu-id="6d65c-176">Select **Upgrade** to apply the latest solution.</span></span>

## <a name="in-preview"></a><span data-ttu-id="6d65c-177">Esiversiossa</span><span class="sxs-lookup"><span data-stu-id="6d65c-177">In preview</span></span>

<span data-ttu-id="6d65c-178">Seuraavat esikatseluominaisuudet ovat olleet käytettävissä 3. helmikuuta 2020 alkaen:</span><span class="sxs-lookup"><span data-stu-id="6d65c-178">The following preview features became available on February 3, 2020:</span></span>

- <span data-ttu-id="6d65c-179">Lisätietoja **Lomien ja poissaolojen esikatseluominaisuuksista** on kohdassa [Lomien ja poissaolojen esikatseluominaisuudet](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span><span class="sxs-lookup"><span data-stu-id="6d65c-179">**Leave and absence preview features** - For more information, see [Leave and absence preview features](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).</span></span>

- <span data-ttu-id="6d65c-180">**Etujen hallinnan esikatselu** – Lisätietoja, kuten tunnettuja ongelmia, on kohdassa [Etujen hallinnan yleiskuvaus](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6d65c-180">**Benefits management preview feature** - For more information, including known issues, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6d65c-181">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="6d65c-181">See also</span></span>

[<span data-ttu-id="6d65c-182">Human Resourcesin uudet ja muuttuneet ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="6d65c-182">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="6d65c-183">Yhteenveto Dynamics 365 Human Resourcesin vuoden 2019 julkaisuaallosta 2</span><span class="sxs-lookup"><span data-stu-id="6d65c-183">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="6d65c-184">Päivitysprosessi</span><span class="sxs-lookup"><span data-stu-id="6d65c-184">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="6d65c-185">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="6d65c-185">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]