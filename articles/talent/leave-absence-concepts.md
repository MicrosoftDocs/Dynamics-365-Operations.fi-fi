---
title: Loman ja poissaolon käsitteet
description: Tässä ohjeaiheessa käsitellään loman ja poissaolon käsitteitä sekä poissaolosaldojen määrittämistä.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/19/2019
ms.locfileid: "857289"
---
# <a name="leave-and-absence-concepts"></a><span data-ttu-id="ab81d-103">Loman ja poissaolon käsitteet</span><span class="sxs-lookup"><span data-stu-id="ab81d-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ab81d-104">Tässä ohjeaiheessa käsitellyt käsitteet ja termit auttavat määrittämään, miten työntekijälle myönnetään palkkioksi vapaa-aikaa ja miten työntekijän aikasaldot lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ab81d-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="ab81d-105">Lisätietoja lomien ja poissaolojen hallinnasta on kohdassa [Lomien ja poissaolojen hallinta](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="ab81d-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="ab81d-106">Lomasuunnitelman tiedot</span><span class="sxs-lookup"><span data-stu-id="ab81d-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="ab81d-107">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-107">Start date</span></span>

<span data-ttu-id="ab81d-108">Aloituspäivämäärä on päivämäärä, jolloin kertymän käsittely alkaa.</span><span class="sxs-lookup"><span data-stu-id="ab81d-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="ab81d-109">Aloituspäivämäärä on myös vuosipäivä, jonka mukaan siirtokirjaussummat lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ab81d-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="ab81d-110">Jaksotukset</span><span class="sxs-lookup"><span data-stu-id="ab81d-110">Accruals</span></span>

<span data-ttu-id="ab81d-111">Kertymät määrittävät, milloin ja miten usein työntekijälle myönnetään palkkiona vapaa-aikaa.</span><span class="sxs-lookup"><span data-stu-id="ab81d-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="ab81d-112">Kertymisten myöntämisajankohtaa ja suhteellista jakoa koskevat käytännöt määritetään **Jaksotukset**-osassa, kun loma- ja poissaolosuunnitelma määritetään.</span><span class="sxs-lookup"><span data-stu-id="ab81d-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="ab81d-113">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-113">Accrual frequency</span></span>

<span data-ttu-id="ab81d-114">Kertymäväli määrittää, kuinka usein loma kerätään tai myönnetään palkkioksi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="ab81d-115">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-115">The following options are available:</span></span>

- <span data-ttu-id="ab81d-116">Päivittäin</span><span class="sxs-lookup"><span data-stu-id="ab81d-116">Daily</span></span>
- <span data-ttu-id="ab81d-117">Viikoittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-117">Weekly</span></span>
- <span data-ttu-id="ab81d-118">Kaksi kertaa viikossa</span><span class="sxs-lookup"><span data-stu-id="ab81d-118">Biweekly</span></span>
- <span data-ttu-id="ab81d-119">Kaksi kertaa kuussa</span><span class="sxs-lookup"><span data-stu-id="ab81d-119">Semimonthly</span></span>
- <span data-ttu-id="ab81d-120">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-120">Monthly</span></span>
- <span data-ttu-id="ab81d-121">Neljännesvuosittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-121">Quarterly</span></span>
- <span data-ttu-id="ab81d-122">Puolivuosittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-122">Semiannually</span></span>
- <span data-ttu-id="ab81d-123">Vuosittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-123">Annually</span></span>
- <span data-ttu-id="ab81d-124">Ei mitään</span><span class="sxs-lookup"><span data-stu-id="ab81d-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="ab81d-125">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-125">Accrual period basis</span></span>

<span data-ttu-id="ab81d-126">Kertymäkauden perusta määrittää päivämäärän, jonka avulla kertymäkaudet lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ab81d-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="ab81d-127">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-127">The following options are available:</span></span>

- <span data-ttu-id="ab81d-128">**Suunnitelman aloituspäivämäärä**</span><span class="sxs-lookup"><span data-stu-id="ab81d-128">**Plan start date**</span></span>
- <span data-ttu-id="ab81d-129">**Työntekijäkohtainen päivämäärä** – Kun tämä asetus on valittu, arvo määrittää alkuperäisen päivämääräarvon, jonka avulla kertymäkaudet lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ab81d-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="ab81d-130">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-130">The following options are available:</span></span>

    - <span data-ttu-id="ab81d-131">Mukautettu</span><span class="sxs-lookup"><span data-stu-id="ab81d-131">Custom</span></span>
    - <span data-ttu-id="ab81d-132">Vuosipäivän päivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-132">Anniversary date</span></span>
    - <span data-ttu-id="ab81d-133">Alkuperäinen työsuhteen alkamispäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-133">Original hire date</span></span>
    - <span data-ttu-id="ab81d-134">Ikälisäpäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-134">Seniority date</span></span>
    - <span data-ttu-id="ab81d-135">Työntekijän muutettu aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="ab81d-136">Työntekijän aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="ab81d-137">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-137">Accrual award date</span></span>

<span data-ttu-id="ab81d-138">Palkkion kertymäpäivämäärä määrittää, milloin työntekijälle myönnetään palkkiona vapaa-aikaa.</span><span class="sxs-lookup"><span data-stu-id="ab81d-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="ab81d-139">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-139">The following options are available:</span></span>

- <span data-ttu-id="ab81d-140">**Jaksotuskauden loppupäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden viimeisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="ab81d-141">Oikean määrän kertyminen edellyttää, että kertymisprosessi sisältää koko kauden.</span><span class="sxs-lookup"><span data-stu-id="ab81d-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="ab81d-142">Esimerkki: Kertymäkausi on 1.1.–31.1.2018.</span><span class="sxs-lookup"><span data-stu-id="ab81d-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="ab81d-143">Jos tammikuu halutaan tässä tapauksessa sisällyttää, kertymä on suoritettava 1.2.2018.</span><span class="sxs-lookup"><span data-stu-id="ab81d-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="ab81d-144">**Jaksotuskauden aloituspäivämäärä** – työntekijälle myönnetään palkkiona vapaa-aikaa palkkiokauden ensimmäisenä päivänä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="ab81d-145">Kertymäkäytäntö rekisteröinnin yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ab81d-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="ab81d-146">Rekisteröitymiseen liittyvä kertymäkäytäntö määrittää, miten kertymä lasketaan, kun työntekijä rekisteröidään kertymäkauden aikana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="ab81d-147">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-147">The following options are available:</span></span>

- <span data-ttu-id="ab81d-148">**Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella.</span><span class="sxs-lookup"><span data-stu-id="ab81d-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="ab81d-149">Kyseistä eroa käytetään, kun kertymiä käsitellään.</span><span class="sxs-lookup"><span data-stu-id="ab81d-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="ab81d-150">**Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="ab81d-151">**Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.</span><span class="sxs-lookup"><span data-stu-id="ab81d-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="ab81d-152">Kertymäkäytäntö rekisteröitymisen poiston yhteydessä</span><span class="sxs-lookup"><span data-stu-id="ab81d-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="ab81d-153">Kertymäkäytännön rekisteröinnin poisto määrittää, miten kertymä lasketaan, kun työntekijän rekisteröinti poistetaan kertymäkauden aikana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="ab81d-154">Käytettävissä ovat seuraavat asetukset:</span><span class="sxs-lookup"><span data-stu-id="ab81d-154">The following options are available:</span></span>

- <span data-ttu-id="ab81d-155">**Suhteellisesti jaettu** – Päivien välinen ero määritetään rekisteröitymis- ja aloituspäivämäärän välisen eron perusteella.</span><span class="sxs-lookup"><span data-stu-id="ab81d-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="ab81d-156">Kyseistä eroa käytetään, kun kertymiä käsitellään.</span><span class="sxs-lookup"><span data-stu-id="ab81d-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="ab81d-157">**Täysi kertymä** – tasoon perustuva täysi kertymä myönnetään palkkiona ensimmäisen kertymäkäsittelyn aikana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="ab81d-158">**Ei kertymää** – jaksotusta ei myönnetä palkkiona ennen seuraavaa kertymäkautta.</span><span class="sxs-lookup"><span data-stu-id="ab81d-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="ab81d-159">Kertymäaikataulu</span><span class="sxs-lookup"><span data-stu-id="ab81d-159">Accrual schedule</span></span>

<span data-ttu-id="ab81d-160">Kertymäaikataulu määrittää, miten työntekijälle kertyy vapaa-aikaa, sekä työntekijälle kertyvät määrät, joille tehdään siirtokirjaus.</span><span class="sxs-lookup"><span data-stu-id="ab81d-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="ab81d-161">Luotujen tasojen avulla vapaa-aikaa voidaan myöntää palkkiona eri perustein.</span><span class="sxs-lookup"><span data-stu-id="ab81d-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="ab81d-162">Työkuukaudet</span><span class="sxs-lookup"><span data-stu-id="ab81d-162">Months of service</span></span>

<span data-ttu-id="ab81d-163">**Työkuukaudet**-arvo määrittää, kuinka monta kuukautta työntekijän on vähintään oltava töissä, jotta heille voi syntyä kertymiä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="ab81d-164">Jos työntekijöille ei määritetä vähimmäisarvoa, arvoksi määritetään **0**.</span><span class="sxs-lookup"><span data-stu-id="ab81d-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="ab81d-165">Työtunnit</span><span class="sxs-lookup"><span data-stu-id="ab81d-165">Hours worked</span></span>

<span data-ttu-id="ab81d-166">**Työtunnit**-arvo määrittää, kuinka monta tuntia työntekijän on tehtävä töitä kertymäkaudella, jotta hänelle voi syntyä kertymiä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="ab81d-167">Jos työntekijöille ei määritetä vähimmäisarvoa, arvoksi määritetään **0**.</span><span class="sxs-lookup"><span data-stu-id="ab81d-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="ab81d-168">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-168">Accrual amount</span></span>

<span data-ttu-id="ab81d-169">Kertymäsumma on se tuntien tai päivien määrä, joka työntekijöille kertyy kunkin kauden aikana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="ab81d-170">Kausi perustuu kertymäväliin.</span><span class="sxs-lookup"><span data-stu-id="ab81d-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="ab81d-171">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-171">Minimum balance</span></span>

<span data-ttu-id="ab81d-172">Vähimmäissaldolla voi olla negatiivinen arvo, jos työntekijät pyytämä loma-aika ylittää heidän käytössään olevan loma-ajan.</span><span class="sxs-lookup"><span data-stu-id="ab81d-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="ab81d-173">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-173">Maximum carry-forward</span></span>

<span data-ttu-id="ab81d-174">Kertymäprosessi oikaisee enimmäissiirtokirjauksen saldon ylittävät lomasaldot aloituspäivämäärän vuosipäivänä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="ab81d-175">Myönnetty summa</span><span class="sxs-lookup"><span data-stu-id="ab81d-175">Grant amount</span></span>

<span data-ttu-id="ab81d-176">Myönnetty summa on työntekijöille aluksi myönnetty tuntien tai päivien määrä, kun rekisteröityvät lomasuunnitelmaan ensimmäisen kerran.</span><span class="sxs-lookup"><span data-stu-id="ab81d-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="ab81d-177">Summaa ei jaksoteta kullekin kertymäkaudelle.</span><span class="sxs-lookup"><span data-stu-id="ab81d-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="ab81d-178">Rekisteröitymiset ja saldot</span><span class="sxs-lookup"><span data-stu-id="ab81d-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="ab81d-179">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-179">Enrollment date</span></span>

<span data-ttu-id="ab81d-180">Rekisteröintipäivä määrittää, milloin työntekijä voi aloittaa vapaa-ajan keräämisen.</span><span class="sxs-lookup"><span data-stu-id="ab81d-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="ab81d-181">Jos työntekijä esimerkiksi on rekisteröitynyt lomasuunnitelmaan 15.6.2018, hän voi aloittaa vapaa-ajan keräämisen vasta 15.6.2018.</span><span class="sxs-lookup"><span data-stu-id="ab81d-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="ab81d-182">Nykyinen saldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-182">Current balance</span></span>

<span data-ttu-id="ab81d-183">Nykyisen saldo on se loman määrä, joka on vapaa-aikapyyntöjen käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="ab81d-184">Tämä määrä sisältää kertymät, hyväksytyt pyynnöt ja oikaisut kuluvaan päivämäärään mennessä.</span><span class="sxs-lookup"><span data-stu-id="ab81d-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="ab81d-185">Nykyiseen saldoon liittyviä esimerkkejä</span><span class="sxs-lookup"><span data-stu-id="ab81d-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="ab81d-186">Vuosisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-186">Annual plan</span></span>

<span data-ttu-id="ab81d-187">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-187">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-188">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-188">Plan start date</span></span> | <span data-ttu-id="ab81d-189">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-189">Enrollment date</span></span> | <span data-ttu-id="ab81d-190">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-190">Accrual frequency</span></span> | <span data-ttu-id="ab81d-191">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-191">Accrual period basis</span></span> | <span data-ttu-id="ab81d-192">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-193">1/1/2018</span></span>        | <span data-ttu-id="ab81d-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-194">1/1/2018</span></span>        | <span data-ttu-id="ab81d-195">Vuosittainen</span><span class="sxs-lookup"><span data-stu-id="ab81d-195">Annual</span></span>            | <span data-ttu-id="ab81d-196">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-196">Plan start date</span></span>      | <span data-ttu-id="ab81d-197">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-197">End of accrual period</span></span> |

<span data-ttu-id="ab81d-198">Kertymät käsitellään 1. tammikuuta 2019 (1.1.2019), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-199">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-199">**Results**</span></span>

| <span data-ttu-id="ab81d-200">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-200">Accrual amount</span></span> | <span data-ttu-id="ab81d-201">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-201">Minimum balance</span></span> | <span data-ttu-id="ab81d-202">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-202">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-203">Pyydetty määrä</span><span class="sxs-lookup"><span data-stu-id="ab81d-203">Request amount</span></span> | <span data-ttu-id="ab81d-204">Nykyinen saldo (1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab81d-205">200</span><span class="sxs-lookup"><span data-stu-id="ab81d-205">200</span></span>            | <span data-ttu-id="ab81d-206">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-206">0</span></span>               | <span data-ttu-id="ab81d-207">120</span><span class="sxs-lookup"><span data-stu-id="ab81d-207">120</span></span>                   | <span data-ttu-id="ab81d-208">40</span><span class="sxs-lookup"><span data-stu-id="ab81d-208">40</span></span>             | <span data-ttu-id="ab81d-209">160</span><span class="sxs-lookup"><span data-stu-id="ab81d-209">160</span></span>                              |

<span data-ttu-id="ab81d-210">Nykyinen saldo (160) = kertynyt määrä (200) – pyydetty määrä (40)</span><span class="sxs-lookup"><span data-stu-id="ab81d-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="ab81d-211">Kaksi kertaa kuussa -suunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-211">Semimonthly plan</span></span>

<span data-ttu-id="ab81d-212">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-212">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-213">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-213">Plan start date</span></span> | <span data-ttu-id="ab81d-214">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-214">Enrollment date</span></span> | <span data-ttu-id="ab81d-215">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-215">Accrual frequency</span></span> | <span data-ttu-id="ab81d-216">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-216">Accrual period basis</span></span> | <span data-ttu-id="ab81d-217">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-218">1/1/2018</span></span>        | <span data-ttu-id="ab81d-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-219">2/1/2018</span></span>        | <span data-ttu-id="ab81d-220">Kaksi kertaa kuussa</span><span class="sxs-lookup"><span data-stu-id="ab81d-220">Semimonthly</span></span>       | <span data-ttu-id="ab81d-221">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-221">Plan start date</span></span>      | <span data-ttu-id="ab81d-222">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-222">End of accrual period</span></span> |

<span data-ttu-id="ab81d-223">Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-224">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-224">**Results**</span></span>

| <span data-ttu-id="ab81d-225">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-225">Accrual amount</span></span> | <span data-ttu-id="ab81d-226">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-226">Minimum balance</span></span> | <span data-ttu-id="ab81d-227">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-227">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-228">Pyydetty määrä</span><span class="sxs-lookup"><span data-stu-id="ab81d-228">Request amount</span></span> | <span data-ttu-id="ab81d-229">Nykyinen saldo (1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab81d-230">5</span><span class="sxs-lookup"><span data-stu-id="ab81d-230">5</span></span>              | <span data-ttu-id="ab81d-231">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-231">0</span></span>               | <span data-ttu-id="ab81d-232">120</span><span class="sxs-lookup"><span data-stu-id="ab81d-232">120</span></span>                   | <span data-ttu-id="ab81d-233">8</span><span class="sxs-lookup"><span data-stu-id="ab81d-233">8</span></span>              | <span data-ttu-id="ab81d-234">22</span><span class="sxs-lookup"><span data-stu-id="ab81d-234">22</span></span>                               |

<span data-ttu-id="ab81d-235">Nykyinen saldo (22) = kertynyt määrä (5 × 6) – pyydetty määrä (8)</span><span class="sxs-lookup"><span data-stu-id="ab81d-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="ab81d-236">Kuukausisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-236">Monthly plan</span></span>

<span data-ttu-id="ab81d-237">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-237">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-238">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-238">Plan start date</span></span> | <span data-ttu-id="ab81d-239">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-239">Enrollment date</span></span> | <span data-ttu-id="ab81d-240">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-240">Accrual frequency</span></span> | <span data-ttu-id="ab81d-241">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-241">Accrual period basis</span></span> | <span data-ttu-id="ab81d-242">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-243">1/1/2018</span></span>        | <span data-ttu-id="ab81d-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-244">2/1/2018</span></span>        | <span data-ttu-id="ab81d-245">Kaksi kertaa kuussa</span><span class="sxs-lookup"><span data-stu-id="ab81d-245">Semimonthly</span></span>       | <span data-ttu-id="ab81d-246">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-246">Plan start date</span></span>      | <span data-ttu-id="ab81d-247">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-247">End of accrual period</span></span> |

<span data-ttu-id="ab81d-248">Kertymät käsitellään 1. toukokuuta 2018 (1.5.2018), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-249">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-249">**Results**</span></span>

| <span data-ttu-id="ab81d-250">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-250">Accrual amount</span></span> | <span data-ttu-id="ab81d-251">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-251">Minimum balance</span></span> | <span data-ttu-id="ab81d-252">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-252">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-253">Pyydetty määrä</span><span class="sxs-lookup"><span data-stu-id="ab81d-253">Request amount</span></span> | <span data-ttu-id="ab81d-254">Nykyinen saldo (1.1.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="ab81d-255">5</span><span class="sxs-lookup"><span data-stu-id="ab81d-255">5</span></span>              | <span data-ttu-id="ab81d-256">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-256">0</span></span>               | <span data-ttu-id="ab81d-257">120</span><span class="sxs-lookup"><span data-stu-id="ab81d-257">120</span></span>                   | <span data-ttu-id="ab81d-258">8</span><span class="sxs-lookup"><span data-stu-id="ab81d-258">8</span></span>              | <span data-ttu-id="ab81d-259">7</span><span class="sxs-lookup"><span data-stu-id="ab81d-259">7</span></span>                                |

<span data-ttu-id="ab81d-260">Nykyinen saldo (7) = kertynyt määrä (5 × 3) – pyydetty määrä (8)</span><span class="sxs-lookup"><span data-stu-id="ab81d-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="ab81d-261">Ennustettu saldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-261">Forecasted balance</span></span>

<span data-ttu-id="ab81d-262">*Ennustettu saldo* on se loman määrä, joka on käytettävissä tulevana ajankohtana.</span><span class="sxs-lookup"><span data-stu-id="ab81d-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="ab81d-263">Kertymät ja siirtokirjausten oikaisut ennustetaan kyseiseen päivämäärään saakka.</span><span class="sxs-lookup"><span data-stu-id="ab81d-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="ab81d-264">Seuraavaa kaavaa käytetään:</span><span class="sxs-lookup"><span data-stu-id="ab81d-264">The following formula is used:</span></span>

<span data-ttu-id="ab81d-265">Maanantain ennustettu saldo = nykyinen saldo – pyynnöt + kertymät – siirtokirjausoikaisu</span><span class="sxs-lookup"><span data-stu-id="ab81d-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="ab81d-266">Esimerkkejä ennustetusta saldosta</span><span class="sxs-lookup"><span data-stu-id="ab81d-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="ab81d-267">Vuosisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-267">Annual plan</span></span>

<span data-ttu-id="ab81d-268">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-268">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-269">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-269">Plan start date</span></span> | <span data-ttu-id="ab81d-270">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-270">Enrollment date</span></span> | <span data-ttu-id="ab81d-271">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-271">Accrual frequency</span></span> | <span data-ttu-id="ab81d-272">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-272">Accrual period basis</span></span> | <span data-ttu-id="ab81d-273">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-274">1/1/2018</span></span>        | <span data-ttu-id="ab81d-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-275">1/1/2018</span></span>        | <span data-ttu-id="ab81d-276">Vuosittainen</span><span class="sxs-lookup"><span data-stu-id="ab81d-276">Annual</span></span>            | <span data-ttu-id="ab81d-277">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-277">Plan start date</span></span>      | <span data-ttu-id="ab81d-278">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-278">End of accrual period</span></span> |

<span data-ttu-id="ab81d-279">Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-280">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-280">**Results**</span></span>

| <span data-ttu-id="ab81d-281">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-281">Accrual amount</span></span> | <span data-ttu-id="ab81d-282">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-282">Minimum balance</span></span> | <span data-ttu-id="ab81d-283">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-283">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-284">Nykyinen saldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-284">Current balance</span></span> | <span data-ttu-id="ab81d-285">Ennustettu saldo (15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab81d-286">20</span><span class="sxs-lookup"><span data-stu-id="ab81d-286">20</span></span>             | <span data-ttu-id="ab81d-287">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-287">0</span></span>               | <span data-ttu-id="ab81d-288">20</span><span class="sxs-lookup"><span data-stu-id="ab81d-288">20</span></span>                    | <span data-ttu-id="ab81d-289">40</span><span class="sxs-lookup"><span data-stu-id="ab81d-289">40</span></span>              | <span data-ttu-id="ab81d-290">40</span><span class="sxs-lookup"><span data-stu-id="ab81d-290">40</span></span>                                   |

<span data-ttu-id="ab81d-291">Ennustettu saldo (40) = kertynyt määrä (20) + nykyinen saldo (40) – siirtokirjausoikaisu (20)</span><span class="sxs-lookup"><span data-stu-id="ab81d-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="ab81d-292">Kaksi kertaa kuussa -suunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-292">Semimonthly plan</span></span>

<span data-ttu-id="ab81d-293">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-293">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-294">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-294">Plan start date</span></span> | <span data-ttu-id="ab81d-295">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-295">Enrollment date</span></span> | <span data-ttu-id="ab81d-296">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-296">Accrual frequency</span></span> | <span data-ttu-id="ab81d-297">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-297">Accrual period basis</span></span> | <span data-ttu-id="ab81d-298">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-299">1/1/2018</span></span>        | <span data-ttu-id="ab81d-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-300">2/1/2018</span></span>        | <span data-ttu-id="ab81d-301">Kaksi kertaa kuussa</span><span class="sxs-lookup"><span data-stu-id="ab81d-301">Semimonthly</span></span>       | <span data-ttu-id="ab81d-302">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-302">Plan start date</span></span>      | <span data-ttu-id="ab81d-303">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-303">End of accrual period</span></span> |

<span data-ttu-id="ab81d-304">Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-305">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-305">**Results**</span></span>

| <span data-ttu-id="ab81d-306">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-306">Accrual amount</span></span> | <span data-ttu-id="ab81d-307">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-307">Minimum balance</span></span> | <span data-ttu-id="ab81d-308">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-308">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-309">Nykyinen saldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-309">Current balance</span></span> | <span data-ttu-id="ab81d-310">Ennustettu saldo (15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab81d-311">5</span><span class="sxs-lookup"><span data-stu-id="ab81d-311">5</span></span>              | <span data-ttu-id="ab81d-312">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-312">0</span></span>               | <span data-ttu-id="ab81d-313">20</span><span class="sxs-lookup"><span data-stu-id="ab81d-313">20</span></span>                    | <span data-ttu-id="ab81d-314">40</span><span class="sxs-lookup"><span data-stu-id="ab81d-314">40</span></span>              | <span data-ttu-id="ab81d-315">35</span><span class="sxs-lookup"><span data-stu-id="ab81d-315">35</span></span>                                   |

<span data-ttu-id="ab81d-316">Ennustettu saldo (35) = kertynyt määrä (5 × 3) + nykyinen saldo (40) – siirtokirjausoikaisu (20)</span><span class="sxs-lookup"><span data-stu-id="ab81d-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="ab81d-317">Kuukausisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-317">Monthly plan</span></span>

<span data-ttu-id="ab81d-318">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-318">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-319">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-319">Plan start date</span></span> | <span data-ttu-id="ab81d-320">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-320">Enrollment date</span></span> | <span data-ttu-id="ab81d-321">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-321">Accrual frequency</span></span> | <span data-ttu-id="ab81d-322">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-322">Accrual period basis</span></span> | <span data-ttu-id="ab81d-323">Palkkion jaksotuspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="ab81d-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-324">1/1/2018</span></span>        | <span data-ttu-id="ab81d-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-325">2/1/2018</span></span>        | <span data-ttu-id="ab81d-326">Kaksi kertaa kuussa</span><span class="sxs-lookup"><span data-stu-id="ab81d-326">Semimonthly</span></span>       | <span data-ttu-id="ab81d-327">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-327">Plan start date</span></span>      | <span data-ttu-id="ab81d-328">Kertymäkauden loppupäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-328">End of accrual period</span></span> |

<span data-ttu-id="ab81d-329">Kertymät käsitellään 15. helmikuuta 2019 (15.2.2019), joten siihen sisältyy koko kausi.</span><span class="sxs-lookup"><span data-stu-id="ab81d-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="ab81d-330">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-330">**Results**</span></span>

| <span data-ttu-id="ab81d-331">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-331">Accrual amount</span></span> | <span data-ttu-id="ab81d-332">Vähimmäissaldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-332">Minimum balance</span></span> | <span data-ttu-id="ab81d-333">Enimmäissiirtokirjaus</span><span class="sxs-lookup"><span data-stu-id="ab81d-333">Maximum carry-forward</span></span> | <span data-ttu-id="ab81d-334">Nykyinen saldo</span><span class="sxs-lookup"><span data-stu-id="ab81d-334">Current balance</span></span> | <span data-ttu-id="ab81d-335">Ennustettu saldo (15.2.2019)</span><span class="sxs-lookup"><span data-stu-id="ab81d-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="ab81d-336">10</span><span class="sxs-lookup"><span data-stu-id="ab81d-336">10</span></span>             | <span data-ttu-id="ab81d-337">0</span><span class="sxs-lookup"><span data-stu-id="ab81d-337">0</span></span>               | <span data-ttu-id="ab81d-338">20</span><span class="sxs-lookup"><span data-stu-id="ab81d-338">20</span></span>                    | <span data-ttu-id="ab81d-339">40</span><span class="sxs-lookup"><span data-stu-id="ab81d-339">40</span></span>              | <span data-ttu-id="ab81d-340">30</span><span class="sxs-lookup"><span data-stu-id="ab81d-340">30</span></span>                                   |

<span data-ttu-id="ab81d-341">Ennustettu saldo (30) = kertynyt määrä (10 × 1) + nykyinen saldo (40) – siirtokirjausoikaisu (20)</span><span class="sxs-lookup"><span data-stu-id="ab81d-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="ab81d-342">Esimerkkejä jaetusta saldosta</span><span class="sxs-lookup"><span data-stu-id="ab81d-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="ab81d-343">Jaettu kuukausisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-343">Prorated monthly plan</span></span>

<span data-ttu-id="ab81d-344">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-344">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-345">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-345">Plan start date</span></span> | <span data-ttu-id="ab81d-346">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-346">Accrual frequency</span></span> | <span data-ttu-id="ab81d-347">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab81d-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-348">1/1/2018</span></span>        | <span data-ttu-id="ab81d-349">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-349">Monthly</span></span>           | <span data-ttu-id="ab81d-350">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-350">Plan start date</span></span>      |

<span data-ttu-id="ab81d-351">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-351">**Results**</span></span>

| <span data-ttu-id="ab81d-352">Työntekijä </span><span class="sxs-lookup"><span data-stu-id="ab81d-352">Employee</span></span>            | <span data-ttu-id="ab81d-353">Työkuukaudet</span><span class="sxs-lookup"><span data-stu-id="ab81d-353">Months of service</span></span> | <span data-ttu-id="ab81d-354">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-354">Enrollment date</span></span> | <span data-ttu-id="ab81d-355">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-355">Start date</span></span> | <span data-ttu-id="ab81d-356">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-356">Accrual amount</span></span> | <span data-ttu-id="ab81d-357">Kertymän käsittely</span><span class="sxs-lookup"><span data-stu-id="ab81d-357">Process accrual</span></span> | <span data-ttu-id="ab81d-358">Tase</span><span class="sxs-lookup"><span data-stu-id="ab81d-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab81d-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab81d-359">Jeannette Nicholson</span></span> | <span data-ttu-id="ab81d-360">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-360">0.00</span></span>              | <span data-ttu-id="ab81d-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-361">6/1/2018</span></span>        | <span data-ttu-id="ab81d-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-362">6/1/2018</span></span>   | <span data-ttu-id="ab81d-363">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-363">1.00</span></span>           | <span data-ttu-id="ab81d-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-364">9/1/2018</span></span>        | <span data-ttu-id="ab81d-365">3,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-365">3.00</span></span>    |
| <span data-ttu-id="ab81d-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab81d-366">Jay Norman</span></span>          | <span data-ttu-id="ab81d-367">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-367">0.00</span></span>              | <span data-ttu-id="ab81d-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-368">6/15/2018</span></span>       | <span data-ttu-id="ab81d-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-369">6/15/2018</span></span>  | <span data-ttu-id="ab81d-370">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-370">1.00</span></span>           | <span data-ttu-id="ab81d-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-371">9/1/2018</span></span>        | <span data-ttu-id="ab81d-372">2,53</span><span class="sxs-lookup"><span data-stu-id="ab81d-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="ab81d-373">Täyden kertymän kuukausisuunnitelma</span><span class="sxs-lookup"><span data-stu-id="ab81d-373">Full accrual monthly plan</span></span>

<span data-ttu-id="ab81d-374">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-374">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-375">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-375">Plan start date</span></span> | <span data-ttu-id="ab81d-376">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-376">Accrual frequency</span></span> | <span data-ttu-id="ab81d-377">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab81d-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-378">1/1/2018</span></span>        | <span data-ttu-id="ab81d-379">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-379">Monthly</span></span>           | <span data-ttu-id="ab81d-380">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-380">Plan start date</span></span>      |

<span data-ttu-id="ab81d-381">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-381">**Results**</span></span>

| <span data-ttu-id="ab81d-382">Työntekijä </span><span class="sxs-lookup"><span data-stu-id="ab81d-382">Employee</span></span>            | <span data-ttu-id="ab81d-383">Työkuukaudet</span><span class="sxs-lookup"><span data-stu-id="ab81d-383">Months of service</span></span> | <span data-ttu-id="ab81d-384">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-384">Enrollment date</span></span> | <span data-ttu-id="ab81d-385">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-385">Start date</span></span> | <span data-ttu-id="ab81d-386">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-386">Accrual amount</span></span> | <span data-ttu-id="ab81d-387">Kertymän käsittely</span><span class="sxs-lookup"><span data-stu-id="ab81d-387">Process accrual</span></span> | <span data-ttu-id="ab81d-388">Tase</span><span class="sxs-lookup"><span data-stu-id="ab81d-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab81d-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab81d-389">Jeannette Nicholson</span></span> | <span data-ttu-id="ab81d-390">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-390">0.00</span></span>              | <span data-ttu-id="ab81d-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-391">6/1/2018</span></span>        | <span data-ttu-id="ab81d-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-392">6/1/2018</span></span>   | <span data-ttu-id="ab81d-393">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-393">1.00</span></span>           | <span data-ttu-id="ab81d-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-394">9/1/2018</span></span>        | <span data-ttu-id="ab81d-395">3,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-395">3.00</span></span>    |
| <span data-ttu-id="ab81d-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab81d-396">Jay Norman</span></span>          | <span data-ttu-id="ab81d-397">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-397">0.00</span></span>              | <span data-ttu-id="ab81d-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-398">6/15/2018</span></span>       | <span data-ttu-id="ab81d-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-399">6/15/2018</span></span>  | <span data-ttu-id="ab81d-400">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-400">1.00</span></span>           | <span data-ttu-id="ab81d-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-401">9/1/2018</span></span>        | <span data-ttu-id="ab81d-402">3,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="ab81d-403">Ei kertymää kuukausisuunnitelmassa</span><span class="sxs-lookup"><span data-stu-id="ab81d-403">No accrual monthly plan</span></span>

<span data-ttu-id="ab81d-404">**Suunnitelman asetukset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-404">**Plan setup**</span></span>

| <span data-ttu-id="ab81d-405">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-405">Plan start date</span></span> | <span data-ttu-id="ab81d-406">Kertymäväli</span><span class="sxs-lookup"><span data-stu-id="ab81d-406">Accrual frequency</span></span> | <span data-ttu-id="ab81d-407">Kertymäkauden perusta</span><span class="sxs-lookup"><span data-stu-id="ab81d-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="ab81d-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-408">1/1/2018</span></span>        | <span data-ttu-id="ab81d-409">Kuukausittain</span><span class="sxs-lookup"><span data-stu-id="ab81d-409">Monthly</span></span>           | <span data-ttu-id="ab81d-410">Suunnitelman aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-410">Plan start date</span></span>      |

<span data-ttu-id="ab81d-411">**Tulokset**</span><span class="sxs-lookup"><span data-stu-id="ab81d-411">**Results**</span></span>

| <span data-ttu-id="ab81d-412">Työntekijä </span><span class="sxs-lookup"><span data-stu-id="ab81d-412">Employee</span></span>            | <span data-ttu-id="ab81d-413">Työkuukaudet</span><span class="sxs-lookup"><span data-stu-id="ab81d-413">Months of service</span></span> | <span data-ttu-id="ab81d-414">Rekisteröintipäivä</span><span class="sxs-lookup"><span data-stu-id="ab81d-414">Enrollment date</span></span> | <span data-ttu-id="ab81d-415">Aloituspäivämäärä</span><span class="sxs-lookup"><span data-stu-id="ab81d-415">Start date</span></span> | <span data-ttu-id="ab81d-416">Jaksotussumma</span><span class="sxs-lookup"><span data-stu-id="ab81d-416">Accrual amount</span></span> | <span data-ttu-id="ab81d-417">Kertymän käsittely</span><span class="sxs-lookup"><span data-stu-id="ab81d-417">Process accrual</span></span> | <span data-ttu-id="ab81d-418">Tase</span><span class="sxs-lookup"><span data-stu-id="ab81d-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="ab81d-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="ab81d-419">Jeannette Nicholson</span></span> | <span data-ttu-id="ab81d-420">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-420">0.00</span></span>              | <span data-ttu-id="ab81d-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-421">6/1/2018</span></span>        | <span data-ttu-id="ab81d-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-422">6/1/2018</span></span>   | <span data-ttu-id="ab81d-423">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-423">1.00</span></span>           | <span data-ttu-id="ab81d-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-424">9/1/2018</span></span>        | <span data-ttu-id="ab81d-425">3,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-425">3.00</span></span>    |
| <span data-ttu-id="ab81d-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="ab81d-426">Jay Norman</span></span>          | <span data-ttu-id="ab81d-427">0,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-427">0.00</span></span>              | <span data-ttu-id="ab81d-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-428">6/15/2018</span></span>       | <span data-ttu-id="ab81d-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-429">6/15/2018</span></span>  | <span data-ttu-id="ab81d-430">1,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-430">1.00</span></span>           | <span data-ttu-id="ab81d-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="ab81d-431">9/1/2018</span></span>        | <span data-ttu-id="ab81d-432">2,00</span><span class="sxs-lookup"><span data-stu-id="ab81d-432">2.00</span></span>    |
