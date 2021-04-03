---
title: Luo Affordable Care Act -raportit etujen hallinnassa
description: Tässä aiheessa kuvataan, kuinka etujen hallinnan avulla voit seurata tietoja, jotka on raportoitu Affordable Care Act (ACA) työnantajan toimeksiannosta lomakkeella 1095-B ja lomakkeessa 1095-C.
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 24df18f428e4ca14859bc34048a6bda5e03d1b2f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464371"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="e3882-103">ACA-raporttien luominen etujen hallinnassa</span><span class="sxs-lookup"><span data-stu-id="e3882-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e3882-104">Etujen hallinnan avulla voit seurata tietoja, jotka on raportoitu Affordable Care Act (ACA) työnantajan toimeksiannosta lomakkeella 1095-B ja lomakkeessa 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e3882-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="e3882-105">Kuten ACA-raportointitoiminto vanhassa **Edut**-työtilassa, tämä toiminto koskee vain Yhdysvalloissa olevia yrityksiä.</span><span class="sxs-lookup"><span data-stu-id="e3882-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="e3882-106">Jotta voit käyttää näitä toimintoja, sinun on ensin otettava käyttöön **Lisäetujen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="e3882-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="e3882-107">Lisätietoja, kuten tärkeät etujen hallintaa koskevat tiedot ovat kohdassa [Etujen hallinnan ottaminen käyttöön ja poistaminen käytöstä](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="e3882-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3882-108">Voit käyttää ACA-raportointia vain joko **Etujen hallinta** -työtilasta tai vanhasta **Edut**-työtilasta, mutta et molemmista.</span><span class="sxs-lookup"><span data-stu-id="e3882-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="e3882-109">Esimerkiksi jos siirryt etujenhallintaan, ACA-raportointi on käytettävissä vain **Etujen hallinta** -työtilassa, ei vanhassa **Edut**-työtilasta.</span><span class="sxs-lookup"><span data-stu-id="e3882-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="e3882-110">Jos siirryt etujenhallintaan rekisteröitymisvuoden keskellä, sinun on määritettävä työntekijöiden tiedot oikein koko vuoden ajaksi Etujen hallinnassa.</span><span class="sxs-lookup"><span data-stu-id="e3882-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="e3882-111">Näin varmistat, että saat koko vuoden tarkat raportointitiedot.</span><span class="sxs-lookup"><span data-stu-id="e3882-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="e3882-112">Aloittaminen</span><span class="sxs-lookup"><span data-stu-id="e3882-112">Getting started</span></span>

<span data-ttu-id="e3882-113">Voit seurata 1095-lomakkeiden tietoja luomalla ensin yhden tai useita Affordable Care -kattavuusryhmiä.</span><span class="sxs-lookup"><span data-stu-id="e3882-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="e3882-114">Ryhmät ilmaisevat seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="e3882-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="e3882-115">Työntekijälle tehty kattavuustarjous.</span><span class="sxs-lookup"><span data-stu-id="e3882-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="e3882-116">Työntekijän osuus pienimmän kustannuksen kuukausittaisen lisän kustannuksista, jos kustannukset ovat liittovaltion köyhyysrajan yläpuolella.</span><span class="sxs-lookup"><span data-stu-id="e3882-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="e3882-117">Työnantajan käyttämä Safe Harbor (jos sovellettavissa)</span><span class="sxs-lookup"><span data-stu-id="e3882-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="e3882-118">Affordable Care -kattavuusryhmien avulla voit hallita näitä tietoja useille työntekijätietueille, joissa on samat ehdot.</span><span class="sxs-lookup"><span data-stu-id="e3882-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="e3882-119">Voit helposti liittää ryhmiä yhteen tai useampiin työntekijöihin.</span><span class="sxs-lookup"><span data-stu-id="e3882-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="e3882-120">Affordable Care -kattavuusryhmän luominen tai muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="e3882-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="e3882-121">Valitse **Etujen hallinta** -työtilasta **Affordable Care -kattavuusryhmä**.</span><span class="sxs-lookup"><span data-stu-id="e3882-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Affordable Care -kattavuusryhmän valinta](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="e3882-123">Valitse **Uusi**, jos haluat luoda uuden Affordable Care -kattavuusryhmän tai muuta aiemmin luotua ryhmää valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e3882-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Valitse Uusi tai Muokkaa](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="e3882-125">Määritä seuraavat kentät.</span><span class="sxs-lookup"><span data-stu-id="e3882-125">Set the following fields.</span></span>

    | <span data-ttu-id="e3882-126">Kenttä</span><span class="sxs-lookup"><span data-stu-id="e3882-126">Field</span></span> | <span data-ttu-id="e3882-127">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e3882-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e3882-128">Nimi</span><span class="sxs-lookup"><span data-stu-id="e3882-128">Name</span></span> | <span data-ttu-id="e3882-129">Anna ryhmälle nimi.</span><span class="sxs-lookup"><span data-stu-id="e3882-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="e3882-130">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e3882-130">Description</span></span> | <span data-ttu-id="e3882-131">Anna ryhmän kuvaus.</span><span class="sxs-lookup"><span data-stu-id="e3882-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="e3882-132">Kattavuustarjous</span><span class="sxs-lookup"><span data-stu-id="e3882-132">Offer of coverage</span></span> | <span data-ttu-id="e3882-133">Työntekijöille, heidän aviopuolisolleen tai kumppanilleen ja heidän huollettavilleen tarjottava kattavuus.</span><span class="sxs-lookup"><span data-stu-id="e3882-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="e3882-134">Työntekijän osa kustannuksista</span><span class="sxs-lookup"><span data-stu-id="e3882-134">Employee share of cost</span></span> | <span data-ttu-id="e3882-135">Summa työntekijä, josta työntekijä vastaa.</span><span class="sxs-lookup"><span data-stu-id="e3882-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="e3882-136">Sovellettava kohta 4980H safe harbor</span><span class="sxs-lookup"><span data-stu-id="e3882-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="e3882-137">Turvakoodi 4980H Safe Harbor- tai siirtohelpotuskoodi.</span><span class="sxs-lookup"><span data-stu-id="e3882-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="e3882-138">Suunnitelman aloituskuukausi</span><span class="sxs-lookup"><span data-stu-id="e3882-138">Plan start month</span></span> | <span data-ttu-id="e3882-139">Valitse kalenterikuukausi, jolloin etusuunnitelman vuosi alkaa.</span><span class="sxs-lookup"><span data-stu-id="e3882-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="e3882-140">Ryhmän ensimmäinen voimassaolopvm</span><span class="sxs-lookup"><span data-stu-id="e3882-140">Group valid from</span></span> | <span data-ttu-id="e3882-141">Tietueen ensimmäinen voimassaolopäivä.</span><span class="sxs-lookup"><span data-stu-id="e3882-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="e3882-142">Ryhmän viimeinen voimassaolopvm</span><span class="sxs-lookup"><span data-stu-id="e3882-142">Group valid through</span></span> | <span data-ttu-id="e3882-143">Tietueen viimeinen voimassaolopäivä.</span><span class="sxs-lookup"><span data-stu-id="e3882-143">The last date when this record is valid.</span></span> <span data-ttu-id="e3882-144">Jos erääntymispäivää ei ole, valitse **Ei koskaan**.</span><span class="sxs-lookup"><span data-stu-id="e3882-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Kattavuusryhmän luominen](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="e3882-146">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e3882-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="e3882-147">Usean työntekijän liittäminen Affordable Care -kattavuusryhmään</span><span class="sxs-lookup"><span data-stu-id="e3882-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="e3882-148">Valitse **Etujen hallinta** -työtilasta **Affordable Care -kattavuusryhmä**.</span><span class="sxs-lookup"><span data-stu-id="e3882-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="e3882-149">Valitse ryhmä, johon työntekijät määritetään.</span><span class="sxs-lookup"><span data-stu-id="e3882-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="e3882-150">Valitse **Joukkomääritys**.</span><span class="sxs-lookup"><span data-stu-id="e3882-150">Select **Mass assignment**.</span></span>

    ![Valitse Joukkomääritys](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="e3882-152">Valitse työntekijät luettelosta ja valitse sitten **Määritä**.</span><span class="sxs-lookup"><span data-stu-id="e3882-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Määritetään työntekijät ryhmään](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="e3882-154">Kattavuusvaihtoehtojen useiden versioiden ylläpitäminen</span><span class="sxs-lookup"><span data-stu-id="e3882-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="e3882-155">Voit ylläpitää useita versioita mistä tahansa kattavuusryhmästä.</span><span class="sxs-lookup"><span data-stu-id="e3882-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="e3882-156">Kun organisaatiossasi jokin muuttuu tai tarjotut edut muuttuvat, voit pitää ryhmän tiedot ajan tasalla ilman, että sinun ei tarvitse luoda uutta ryhmää ja määrittää siihen työntekijöitä uudelleen.</span><span class="sxs-lookup"><span data-stu-id="e3882-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="e3882-157">Kun olet luonut Affordable Care -kattavuusryhmät, voit määrittää niihin työntekijöitä joukkotoimintona.</span><span class="sxs-lookup"><span data-stu-id="e3882-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="e3882-158">Voit myös liittää työntekijät ryhmiin yksitellen ja määrittää, seurataanko ja raportoidaanko ACA-tietoja.</span><span class="sxs-lookup"><span data-stu-id="e3882-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="e3882-159">Jos työntekijän ACA-tietoja ei tarvitse seurata ja raportoida, voit määrittää **Raportin kattavuus** -asetuksen arvoksi **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e3882-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="e3882-160">Esimerkiksi osa-aikatyöntekijöille ei aina tarvitse olla ACA-raportointia.</span><span class="sxs-lookup"><span data-stu-id="e3882-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="e3882-161">Työntekijän oletusarvojen korvaaminen</span><span class="sxs-lookup"><span data-stu-id="e3882-161">Override default values for an employee</span></span>

<span data-ttu-id="e3882-162">Jos työntekijä on liitetty Affordable Care -kattavuusryhmään, voit muuttaa seuraavia asetuksia kuukausien osalta, jotka edellyttävät eri arvoja:</span><span class="sxs-lookup"><span data-stu-id="e3882-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="e3882-163">Kattavuustarjous</span><span class="sxs-lookup"><span data-stu-id="e3882-163">Offer of coverage</span></span>
- <span data-ttu-id="e3882-164">Työntekijän osa kustannuksista</span><span class="sxs-lookup"><span data-stu-id="e3882-164">Employee share of cost</span></span>
- <span data-ttu-id="e3882-165">Sovellettava kohta 4980H safe harbor</span><span class="sxs-lookup"><span data-stu-id="e3882-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="e3882-166">Vuoden 2020 ACA-raporteissa on raportoitava sekä työpaikan että kotiosoitteen postinumerot lomakkeessa 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e3882-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="e3882-167">Arvot täytetään automaattisesti nykyisten aktiivisten sijaintien perusteella.</span><span class="sxs-lookup"><span data-stu-id="e3882-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="e3882-168">Jos jompikumpi sijainti oli eri vuoden minkä tahansa osan aikana, arvo on ohitettava.</span><span class="sxs-lookup"><span data-stu-id="e3882-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="e3882-169">1095-C-raportin **Postinumero**-kenttä (rivi 17) täytetään vain, jos **Kattavuustarjous**-koodi sisältää **1L**–**1Q** seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="e3882-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="e3882-170">**1L, 1M tai 1N:** Ensisijaisen asuinpaikan postinumero</span><span class="sxs-lookup"><span data-stu-id="e3882-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="e3882-171">**1O, 1P, 1Q:** Ensisijainen työn postinumero</span><span class="sxs-lookup"><span data-stu-id="e3882-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="e3882-172">Jos haluat määrittää poikkeuksia Affordable Care -kattavuusryhmän arvoille, noudata seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="e3882-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="e3882-173">Valitse **henkilöstöhallinnan** työtilassa **linkit** ja valitse sitten **työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="e3882-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="e3882-174">Valitse luettelosta työntekijä.</span><span class="sxs-lookup"><span data-stu-id="e3882-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="e3882-175">Valitse **Työsuhde**-välilehden **Lisätiedot**-osasta **Affordable Care -kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="e3882-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Yhden työntekijän asetusten muuttaminen](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="e3882-177">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e3882-177">Select **Edit**.</span></span>
5. <span data-ttu-id="e3882-178">Valitse jokaiselle muutosta edellyttävälle kuukaudelle **Ohita oletus** -valintaruutu ja muuta sitten muita arvoja tarpeen mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3882-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Oletusarvojen ohitus](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="e3882-180">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e3882-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="e3882-181">Terveydenhuollon kattavuuden raportointi</span><span class="sxs-lookup"><span data-stu-id="e3882-181">Report health care coverage</span></span>

<span data-ttu-id="e3882-182">Sinun on seurattava kaikkia työnantajan kustantamia, itsevakuutettuja terveydenhuollon kattavuuksia kokoaikaisille ja osa-aikaisille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="e3882-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="e3882-183">Sisällytä kukin työntekijä ja heidän huollettavansa 1095-C-raporttiin niiden kuukausien osalta, jolloin työntekijät on katettu.</span><span class="sxs-lookup"><span data-stu-id="e3882-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="e3882-184">Seuraavia ohjeita noudattamalla voit määrittää, onko etusuunnitelma raportoitava.</span><span class="sxs-lookup"><span data-stu-id="e3882-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="e3882-185">Valitse **Etujen hallinta** -työtilassa **Etuussuunnitelmat**.</span><span class="sxs-lookup"><span data-stu-id="e3882-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="e3882-186">Valitse raportoitava etusuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="e3882-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="e3882-187">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e3882-187">Select **Edit**.</span></span>
4. <span data-ttu-id="e3882-188">Määritä **Raportoidaan Affordable Care Act -lain mukaan** -arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e3882-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Terveydenhuollon kattavuuden raportointi](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="e3882-190">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e3882-190">Select **Save**.</span></span>

<span data-ttu-id="e3882-191">Jos työntekijä valitsee huollettavalleen terveyskattavuuden, huollettavan kattavuuskauden määrittää päivämäärä, jolloin huollettava on rekisteröity tai poistettu.</span><span class="sxs-lookup"><span data-stu-id="e3882-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="e3882-192">Huollettavien kattavuuspäivämäärät lasketaan automaattisesti sen kauden perusteella, jolloin huollettava oli oikeutettu ja aktiivinen suunnitelmassa rekisteröintivuoden aikana.</span><span class="sxs-lookup"><span data-stu-id="e3882-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="e3882-193">Luo 1095-B- ja 1095-C-lomakkeita</span><span class="sxs-lookup"><span data-stu-id="e3882-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="e3882-194">Voit luoda ACA:n 1095-B- ja 1095-C-lomakkeita ja jakaa ne työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="e3882-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="e3882-195">Voit myös luoda sähköisesti lomakkeen 1095-C ja vastaavat 1094-C-siirtotiedostot lähetettäväksi Internal Revenue Service (IRS) -palveluun.</span><span class="sxs-lookup"><span data-stu-id="e3882-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="e3882-196">Valitse **Etujen hallinta** -työtilassa **ACA 1095-B -lomake** tai **ACA 1095-C -lomake**.</span><span class="sxs-lookup"><span data-stu-id="e3882-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="e3882-197">Muuta parametreja tarpeen mukaan ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3882-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3882-198">Jos tulostat 1095-C-lomakkeet yli 500 työntekijälle, PDF-tiedostoja on useita.</span><span class="sxs-lookup"><span data-stu-id="e3882-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="e3882-199">**Tiedostonhallinnan parametrit** -sivun **Tiedoston enimmäiskoko megatavuina** -kentän arvo on suositeltavaa suurentaa arvoksi **150**.</span><span class="sxs-lookup"><span data-stu-id="e3882-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="e3882-200">(Voit avata sivun nopeasti siirtymispalkin hakukentän avulla.)</span><span class="sxs-lookup"><span data-stu-id="e3882-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Tiedoston enimmäiskoon muuttaminen](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="e3882-202">Voit tarkistaa raporttien tilan ja tarkastella niitä avaamalla **Sähköisen raportoinnin työt** -sivun siirtymispalkin hakukentän avulla.</span><span class="sxs-lookup"><span data-stu-id="e3882-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Sähköisen raportoinnin työt -sivun hakeminen](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="e3882-204">Valitse näytettävä raportti ja valitse sitten **Näytä tiedostot**.</span><span class="sxs-lookup"><span data-stu-id="e3882-204">Select the report to view, and then select **Show files**.</span></span>

    ![Näytetään tiedostot](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="e3882-206">Valitse **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="e3882-206">Select **Open**.</span></span>

    ![Tiedoston avaaminen](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="e3882-208">Avaa zip-tiedosto ja valitse raportti selaimen ikkunan alaosassa näkyvästä ilmoitusrivistä.</span><span class="sxs-lookup"><span data-stu-id="e3882-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="e3882-209">Voit tarkastella tai tulostaa PDF-tiedoston.</span><span class="sxs-lookup"><span data-stu-id="e3882-209">You can view or print the PDF file.</span></span>

    ![Esimerkki 1095-C-lomakkeesta](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="e3882-211">ACA-kattavuustietojen tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e3882-211">View ACA coverage information</span></span>

<span data-ttu-id="e3882-212">**Työntekijöiden Affordable Care -kattavuus** -sivulla näkyvät seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="e3882-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="e3882-213">Kuhunkin kattavuusryhmään liitetyt työntekijät</span><span class="sxs-lookup"><span data-stu-id="e3882-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="e3882-214">Työntekijät, joiden ei tarvitse sisältyä raporttiin</span><span class="sxs-lookup"><span data-stu-id="e3882-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="e3882-215">Määrittämättömät työntekijät</span><span class="sxs-lookup"><span data-stu-id="e3882-215">Unassigned employees</span></span>

<span data-ttu-id="e3882-216">Näitä tietoja voi tarkastella seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="e3882-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="e3882-217">Valitse **Etujen hallinta** -työtilasta **Työntekijöiden Affordable Care -kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="e3882-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="e3882-218">Valitse **Ryhmän nimi**-kentässä ryhmä.</span><span class="sxs-lookup"><span data-stu-id="e3882-218">In the **Group name** field, select a group.</span></span>

    ![ACA-kattavuuden tarkasteleminen](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="e3882-220">Jos jokin Affordable Care -kattavuusryhmän oletusarvoista on korvattu, muutetun arvon vieressä näkyy tähtimerkki.</span><span class="sxs-lookup"><span data-stu-id="e3882-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="e3882-221">Jos jokaisen 12 kuukauden arvo on sama eikä sitä ole korvattu, arvo näkyy **Kaikki 12 kuukautta** -sarakkeessa.</span><span class="sxs-lookup"><span data-stu-id="e3882-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="e3882-222">Voit tarkastella työntekijöitä, jotka on merkitty ACA-raportoinnin ulkopuolle ja jotka eivät vaadi lomaketta 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e3882-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="e3882-223">Valitse **Suodatusperuste**-kentässä **Ei ACA-raportoitava**.</span><span class="sxs-lookup"><span data-stu-id="e3882-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="e3882-224">Voit tarkastella työntekijöitä, joita ei ole liitetty ryhmään tai jotka on liitetty vanhentuneeseen ryhmään.</span><span class="sxs-lookup"><span data-stu-id="e3882-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="e3882-225">Valitse **Suodatusperuste**-kentässä mukaan **Ei määritetty tai vanhentunut ryhmä**.</span><span class="sxs-lookup"><span data-stu-id="e3882-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="e3882-226">Vie Exceliin</span><span class="sxs-lookup"><span data-stu-id="e3882-226">Export to Excel</span></span>

<span data-ttu-id="e3882-227">Voit viedä minkä tahansa luettelon Microsoft Exceliin seuraavien ohjeiden mukaan.</span><span class="sxs-lookup"><span data-stu-id="e3882-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="e3882-228">Valitse **Avaa Microsoft Officessa** -painike.</span><span class="sxs-lookup"><span data-stu-id="e3882-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="e3882-229">Valitse **HCM Human Resources – väliaikainen taulu sisäiseen käyttööön**.</span><span class="sxs-lookup"><span data-stu-id="e3882-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="e3882-230">Valitse **Lataa**.</span><span class="sxs-lookup"><span data-stu-id="e3882-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="e3882-231">ACA-raportoitavien huollettavien tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e3882-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="e3882-232">Jos sinun on raportoitava kattavuuteen kuuluvat henkilöt itsevakuutettujen kattavuuden vuoksi, voit tarkastella huollettavia, jotka on katettu **ACA-raportoitaviksi** merkityissä etusuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="e3882-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="e3882-233">Valitse toimintoruudussa **Näytä huollettavien kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="e3882-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Huollettavien kattavuuden tarkasteleminen](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="e3882-235">Näkyviin tulee työntekijän huollettavien kattavuustiedot.</span><span class="sxs-lookup"><span data-stu-id="e3882-235">Coverage information for the employee's dependents is shown.</span></span>

![Huollettavan kattavuus](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="e3882-237">Sivulla näkyvät vain ne edut, jotka on merkitty **ACA-raportoitaviksi**.</span><span class="sxs-lookup"><span data-stu-id="e3882-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]