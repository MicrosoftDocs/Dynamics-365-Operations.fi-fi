---
title: Työvoiman järjestäminen osastojen, töiden ja toimien avulla
description: Osastot, työt ja toimet ovat organisaatioelementtejä, joita ylläpidetään henkilöstöhallinnossa. Tässä artikkelissa kuvataan elementtien käsitteellisiä tietoja.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: e1dace0dc6477e259d1004440c4cda8060bf90e3
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130226"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="ebf27-104">Työvoiman järjestäminen osastojen, töiden ja toimien avulla</span><span class="sxs-lookup"><span data-stu-id="ebf27-104">Organize your workforce by using departments, jobs, and positions</span></span>

<span data-ttu-id="ebf27-105">Osastot, työt ja toimet ovat organisaatioelementtejä, joita ylläpidetään henkilöstöhallinnossa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="ebf27-106">Tässä artikkelissa kuvataan elementtien käsitteellisiä tietoja.</span><span class="sxs-lookup"><span data-stu-id="ebf27-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="ebf27-107">Seuraavassa esimerkissä on kuvattu tässä artikkelissa käytettäviä käsitteitä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="ebf27-108">**Osasto**</span><span class="sxs-lookup"><span data-stu-id="ebf27-108">**Department**</span></span>|<span data-ttu-id="ebf27-109">**Sijainti**</span><span class="sxs-lookup"><span data-stu-id="ebf27-109">**Position**</span></span>|<span data-ttu-id="ebf27-110">**Työ**</span><span class="sxs-lookup"><span data-stu-id="ebf27-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="ebf27-111">**Myynti**</span><span class="sxs-lookup"><span data-stu-id="ebf27-111">**Sales**</span></span>|<span data-ttu-id="ebf27-112">Myyntipäällikkö (Itä)</span><span class="sxs-lookup"><span data-stu-id="ebf27-112">Sales manager (East)</span></span>|<span data-ttu-id="ebf27-113">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-113">Sales manager</span></span>|
|<span data-ttu-id="ebf27-114">**myynti**</span><span class="sxs-lookup"><span data-stu-id="ebf27-114">**Sales**</span></span>|<span data-ttu-id="ebf27-115">Myyntipäällikkö (Länsi)</span><span class="sxs-lookup"><span data-stu-id="ebf27-115">Sales manager (West)</span></span>|<span data-ttu-id="ebf27-116">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-116">Sales manager</span></span>|
|<span data-ttu-id="ebf27-117">**myynti**</span><span class="sxs-lookup"><span data-stu-id="ebf27-117">**Sales**</span></span>|<span data-ttu-id="ebf27-118">Myyntipäällikkö (Keski)</span><span class="sxs-lookup"><span data-stu-id="ebf27-118">Sales manager (Central)</span></span>|<span data-ttu-id="ebf27-119">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-119">Sales manager</span></span>|
|<span data-ttu-id="ebf27-120">**Kirjanpito**</span><span class="sxs-lookup"><span data-stu-id="ebf27-120">**Accounting**</span></span>|<span data-ttu-id="ebf27-121">Taloushallintopäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-121">Accounting supervisor</span></span>|<span data-ttu-id="ebf27-122">Laskentapäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-122">Accounting manager</span></span>|
|<span data-ttu-id="ebf27-123">**Kirjanpito**</span><span class="sxs-lookup"><span data-stu-id="ebf27-123">**Accounting**</span></span>|<span data-ttu-id="ebf27-124">Kirjanpitäjä A</span><span class="sxs-lookup"><span data-stu-id="ebf27-124">Accounting-A</span></span>|<span data-ttu-id="ebf27-125">Kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="ebf27-125">Accountant</span></span>|
|<span data-ttu-id="ebf27-126">**Henkilöstöhallinto**</span><span class="sxs-lookup"><span data-stu-id="ebf27-126">**Human resources**</span></span>|<span data-ttu-id="ebf27-127">Henkilöstöpäällikkö (Itä)</span><span class="sxs-lookup"><span data-stu-id="ebf27-127">HR manager (East)</span></span>|<span data-ttu-id="ebf27-128">Henkilöstöpäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-128">HR manager</span></span>|
|<span data-ttu-id="ebf27-129">**Henkilöstöhallinto**</span><span class="sxs-lookup"><span data-stu-id="ebf27-129">**Human resources**</span></span>|<span data-ttu-id="ebf27-130">Henkilöstöpäällikkö (Länsi)</span><span class="sxs-lookup"><span data-stu-id="ebf27-130">HR manager (West)</span></span>|<span data-ttu-id="ebf27-131">Henkilöstöpäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-131">HR manager</span></span>|
|<span data-ttu-id="ebf27-132">**Henkilöstöhallinto**</span><span class="sxs-lookup"><span data-stu-id="ebf27-132">**Human resources**</span></span>|<span data-ttu-id="ebf27-133">Henkilöstöpäällikkö (Keski)</span><span class="sxs-lookup"><span data-stu-id="ebf27-133">HR manager (Central)</span></span>|<span data-ttu-id="ebf27-134">Henkilöstöpäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="ebf27-135">Osastot</span><span class="sxs-lookup"><span data-stu-id="ebf27-135">Departments</span></span>
------------

<span data-ttu-id="ebf27-136">Osasto on toimintayksikkö, joka edustaa organisaation luokkaa tai toiminta-aluetta ja vastaa tietystä organisaation osa-alueesta, kuten myynnistä tai kirjanpidosta.</span><span class="sxs-lookup"><span data-stu-id="ebf27-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="ebf27-137">Osastoa käytetään toiminta-alueiden raportoinnissa, ja sillä voi olla tulosvastuu.</span><span class="sxs-lookup"><span data-stu-id="ebf27-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="ebf27-138">Osasto voi myös sisältää kustannuspaikkojen ryhmän.</span><span class="sxs-lookup"><span data-stu-id="ebf27-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="ebf27-139">Organisaation osastoja ovat esimerkiksi myynti, kirjanpito ja henkilöstöhallinto.</span><span class="sxs-lookup"><span data-stu-id="ebf27-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="ebf27-140">Työt ja toimet</span><span class="sxs-lookup"><span data-stu-id="ebf27-140">Jobs and positions</span></span>
<span data-ttu-id="ebf27-141">Työ sisältää tehtäviä ja vastuita, joita työn suorittajalta edellytetään.</span><span class="sxs-lookup"><span data-stu-id="ebf27-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="ebf27-142">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="ebf27-143">Työssä tarvittavat vastuualueet, työtehtävät, taidot, koulutustiedot ja todistukset tarvitaan myös työhön liittyvissä toimissa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="ebf27-144">Työtehtävät</span><span class="sxs-lookup"><span data-stu-id="ebf27-144">Job tasks</span></span>

<span data-ttu-id="ebf27-145">Voit luoda työtehtäviä, jotka kuvaavat kyseisessä toimessa toimivan työntekijän perustehtäviä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="ebf27-146">Samaan työtehtävään voidaan lisätä useita töitä, ja töiden toimet perivät työtehtävät.</span><span class="sxs-lookup"><span data-stu-id="ebf27-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="ebf27-147">Seuraavassa taulukossa on esimerkkejä työtehtävistä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ebf27-148">Työ</span><span class="sxs-lookup"><span data-stu-id="ebf27-148">Job</span></span></th>
<th><span data-ttu-id="ebf27-149">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="ebf27-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebf27-150">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="ebf27-151"><span class="input">Suorituskykytarkistus</span> – Arvioi jokaisen myyjän suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="ebf27-152"><span class="input">Poissaolotarkistus</span> – Hyväksy tai hylkää kunkin myyjän poissaolopyynnöt tai -rekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="ebf27-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebf27-153">Kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="ebf27-153">Accountant</span></span></td>
<td><span data-ttu-id="ebf27-154"><span class="input">TAL-raportti</span> – Esitä viikoittaiset talousraportit talousjohtajalle.</span><span class="sxs-lookup"><span data-stu-id="ebf27-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="ebf27-155">Työtehtävät</span><span class="sxs-lookup"><span data-stu-id="ebf27-155">Job functions</span></span>

<span data-ttu-id="ebf27-156">Työtehtävät ovat</span><span class="sxs-lookup"><span data-stu-id="ebf27-156">Job functions are like job tasks.</span></span> <span data-ttu-id="ebf27-157">työhön määritettyjä tehtäviä tai vastuita.</span><span class="sxs-lookup"><span data-stu-id="ebf27-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="ebf27-158">Työtehtävät voidaan määrittää töille, ja niitä voidaan käyttää kompensaatiosuunnitelmien kelpoisuussääntöjen määrittämisessä ja käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="ebf27-159">Seuraavassa taulukossa on esimerkkejä työtehtävistä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="ebf27-160">Työ</span><span class="sxs-lookup"><span data-stu-id="ebf27-160">Job</span></span>           | <span data-ttu-id="ebf27-161">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="ebf27-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="ebf27-162">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="ebf27-162">Sales manager</span></span> | <span data-ttu-id="ebf27-163">Hnk.hallinto – Sinulle raportoivien henkilöiden hallinta.</span><span class="sxs-lookup"><span data-stu-id="ebf27-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="ebf27-164">Kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="ebf27-164">Accountant</span></span>    | <span data-ttu-id="ebf27-165">TAL-tarkastus – Ylläpidä tiettyjen tilien taloustietoja.</span><span class="sxs-lookup"><span data-stu-id="ebf27-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="ebf27-166">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="ebf27-166">Job types</span></span>

<span data-ttu-id="ebf27-167">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="ebf27-168">Työtyypit voidaan työtehtävien tapaan määrittää töille, ja niitä voidaan käyttää kompensaatiosuunnitelmien kelpoisuussääntöjen määrittämisessä ja käyttöönotossa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="ebf27-169">Seuraavassa luettelossa on esimerkkejä työtyypeistä:</span><span class="sxs-lookup"><span data-stu-id="ebf27-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="ebf27-170">Kokoaikainen</span><span class="sxs-lookup"><span data-stu-id="ebf27-170">Full-time</span></span>
-   <span data-ttu-id="ebf27-171">Osa-aikainen</span><span class="sxs-lookup"><span data-stu-id="ebf27-171">Part-time</span></span>
-   <span data-ttu-id="ebf27-172">Palkka</span><span class="sxs-lookup"><span data-stu-id="ebf27-172">Salary</span></span>
-   <span data-ttu-id="ebf27-173">Tuntipalkka</span><span class="sxs-lookup"><span data-stu-id="ebf27-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="ebf27-174">Vastuualueet</span><span class="sxs-lookup"><span data-stu-id="ebf27-174">Areas of responsibility</span></span>

<span data-ttu-id="ebf27-175">Vastuualueiden avulla voi osoittaa tietyssä toimessa toimivan työntekijän vastuulla olevat työroolit, prosessit ja tuotteet.</span><span class="sxs-lookup"><span data-stu-id="ebf27-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="ebf27-176">Esimerkiksi Kirjanpitäjä-toimessa vastuualue voi olla Tuotteen A talousraportointi.</span><span class="sxs-lookup"><span data-stu-id="ebf27-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="ebf27-177">Toimet</span><span class="sxs-lookup"><span data-stu-id="ebf27-177">Positions</span></span>
----------

<span data-ttu-id="ebf27-178">Toimet ovat organisaatiohierarkian alemman tason tärkeä osa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="ebf27-179">Toimi on työn yksittäinen esiintymä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="ebf27-180">Esimerkiksi toimi Myyntipäällikkö (Itä) on vain yksi Myyntipäällikkö-työhön liittyvistä toimista.</span><span class="sxs-lookup"><span data-stu-id="ebf27-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="ebf27-181">Toimet sijoittuvat osastoille, ja niitä määritetään työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="ebf27-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="ebf27-182">Toimen luominen ja ylläpito</span><span class="sxs-lookup"><span data-stu-id="ebf27-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="ebf27-183">Voit tarkastella toimiin liittyvää järjestelmän muutoshistoriaa helppokäyttöisellä luettelosivulla.</span><span class="sxs-lookup"><span data-stu-id="ebf27-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="ebf27-184">Voit luoda syykoodeja, joita käyttäjät voivat valita toimia luodessaan tai muokatessaan.</span><span class="sxs-lookup"><span data-stu-id="ebf27-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="ebf27-185">Voit luoda henkilöstön toimintotyyppejä ja määrittää henkilöstötoiminnoille numerojärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="ebf27-186">Voit määrittää työnkulun niin, että toimien lisäämiselle ja muuttamiselle tarvitaan hyväksyntä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="ebf27-187">Toimen kesto</span><span class="sxs-lookup"><span data-stu-id="ebf27-187">Position duration</span></span>

<span data-ttu-id="ebf27-188">Jokainen toimi on voimassa tietyn aikavälin.</span><span class="sxs-lookup"><span data-stu-id="ebf27-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="ebf27-189">Sitä kutsutaan kestoksi.</span><span class="sxs-lookup"><span data-stu-id="ebf27-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="ebf27-190">Esimerkiksi kesätöiden kesto voi olla 1.5.2015–31.8.2015.</span><span class="sxs-lookup"><span data-stu-id="ebf27-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="ebf27-191">Työntekijämääritykset</span><span class="sxs-lookup"><span data-stu-id="ebf27-191">Worker assignments</span></span>

<span data-ttu-id="ebf27-192">Kun määrität työntekijän johonkin toimeen, täytät kyseisen toimen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="ebf27-193">Voit määrittää työntekijöitä useisiin toimiin, mutta kuhunkin toimeen voi määrittää vain yhden työntekijän kerrallaan.</span><span class="sxs-lookup"><span data-stu-id="ebf27-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="ebf27-194">Raportointisuhteet</span><span class="sxs-lookup"><span data-stu-id="ebf27-194">Reporting relationships</span></span>

<span data-ttu-id="ebf27-195">Toimet ovat organisaatiohierarkian alemman tason tärkeitä osia.</span><span class="sxs-lookup"><span data-stu-id="ebf27-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="ebf27-196">Toimi-lomakkeessa voit määrittää toimen, jolle toinen toimi raportoi.</span><span class="sxs-lookup"><span data-stu-id="ebf27-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="ebf27-197">Kun määrität työntekijän toimeen, joka raportoi toiselle toimelle, luot näihin kahteen toimeen määritettyjen työntekijöiden välisen raportointisuhteen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="ebf27-198">Esimerkki: Toimi Kirjanpitäjä A raportoi toimelle Kirjanpidon esimies.</span><span class="sxs-lookup"><span data-stu-id="ebf27-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="ebf27-199">Kim Akers on nimitetty kirjanpidon esimieheksi ja Sanjay Patel kirjanpitäjäksi A.</span><span class="sxs-lookup"><span data-stu-id="ebf27-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="ebf27-200">Sanjay Patel raportoi siis Kim Akersille.</span><span class="sxs-lookup"><span data-stu-id="ebf27-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="ebf27-201">Jos organisaatio käyttää matriisihierarkiaan tai jotakin toista mukautettua hierarkiaa, voit määrittää toimien hierarkiatyypit ja lisätä sitten toimiin raportointisuhteet jokaiselle määrittämällesi hierarkiatyypille.</span><span class="sxs-lookup"><span data-stu-id="ebf27-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="ebf27-202">Esimerkki: Lori Penor on Adventure Worksin johtaja, joka nimitetään pääjohtajan toimeen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="ebf27-203">Lori johtaa pienoissovellusten puhdistamiseen käytettävän tuotteen kehitystyötä.</span><span class="sxs-lookup"><span data-stu-id="ebf27-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="ebf27-204">Lori tarvitsee kirjanpitäjän avuksi tuotekehityksen taloushallintoon.</span><span class="sxs-lookup"><span data-stu-id="ebf27-204">Lori requires an accountant to help her with the finances for developing the product.</span></span> <span data-ttu-id="ebf27-205">Hän on rekrytoinut Sanjay Patelin kirjanpitäjäksi.</span><span class="sxs-lookup"><span data-stu-id="ebf27-205">Therefore, she has recruited Sanjay Patel to be her accountant.</span></span> <span data-ttu-id="ebf27-206">Sanjay raportoi suoraan Kim Akersille, mutta hän työskentelee myös Lori Penorin kanssa pienoissovelluksen tuotekehityksen taloushallinnossa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="ebf27-207">Edellisessä esimerkissä määrittäisit Sanjay Patelin ja Lori Penorin välisen työsuhteen suorittamalla seuraavat tehtävät:</span><span class="sxs-lookup"><span data-stu-id="ebf27-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="ebf27-208">Luo Pienoissovellus-niminen mukautettu toimen hierarkiatyyppi, jotta voit luoda hierarkian, joka sisältää pienoissovelluksen tuotekehityksestä vastaavat toimet.</span><span class="sxs-lookup"><span data-stu-id="ebf27-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="ebf27-209">Määritä pääjohtajan toimi toimeksi, jolle kirjanpitäjä A:n toimi raportoi Pienoissovellus-hierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="ebf27-210">Toimihierarkian avulla voit tarkastella toimien raportointirakennetta.</span><span class="sxs-lookup"><span data-stu-id="ebf27-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="ebf27-211">Jos toimihierarkioita on useita, voit tarkastella kutakin hierarkiatyyppiä toimihierarkiassa.</span><span class="sxs-lookup"><span data-stu-id="ebf27-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="ebf27-212">Voit myös hakea toimia toimen tunnuksen tai siihen nimitetyn henkilön nimen perusteella.</span><span class="sxs-lookup"><span data-stu-id="ebf27-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="ebf27-213">Toimihierarkia on organisaatiohierarkia.</span><span class="sxs-lookup"><span data-stu-id="ebf27-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="ebf27-214">Voimassaolotietueet</span><span class="sxs-lookup"><span data-stu-id="ebf27-214">Date effective records</span></span>
<span data-ttu-id="ebf27-215">Joissakin tietueissa voit määrittää tietueeseen tehtävät tulevat muutokset.</span><span class="sxs-lookup"><span data-stu-id="ebf27-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="ebf27-216">Seuraavat tiedot ovat voimassaolotietueita.</span><span class="sxs-lookup"><span data-stu-id="ebf27-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ebf27-217">Tietueet</span><span class="sxs-lookup"><span data-stu-id="ebf27-217">Records</span></span></th>
<th><span data-ttu-id="ebf27-218">Voimassaolotiedot</span><span class="sxs-lookup"><span data-stu-id="ebf27-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ebf27-219">Työt</span><span class="sxs-lookup"><span data-stu-id="ebf27-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="ebf27-220">Jotkin yksityiskohtaiset työtiedot</span><span class="sxs-lookup"><span data-stu-id="ebf27-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="ebf27-221">Työn luokittelutiedot</span><span class="sxs-lookup"><span data-stu-id="ebf27-221">Job classification information</span></span></li>
<li><span data-ttu-id="ebf27-222">Kompensaatiotiedot</span><span class="sxs-lookup"><span data-stu-id="ebf27-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ebf27-223">Toimet</span><span class="sxs-lookup"><span data-stu-id="ebf27-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="ebf27-224">Jotkin yksityiskohtaiset toimitiedot</span><span class="sxs-lookup"><span data-stu-id="ebf27-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="ebf27-225">Työntekijämääritykset</span><span class="sxs-lookup"><span data-stu-id="ebf27-225">Worker assignments</span></span></li>
<li><span data-ttu-id="ebf27-226">Toimen kestot</span><span class="sxs-lookup"><span data-stu-id="ebf27-226">Position durations</span></span></li>
<li><span data-ttu-id="ebf27-227">Positiohierarkiat</span><span class="sxs-lookup"><span data-stu-id="ebf27-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ebf27-228">Voit muokata edellä olevassa taulukossa mainittuja toimen tai työn tietoja ja määrittää päivämäärän, jona toimen tai työn muutokset tulevat voimaan.</span><span class="sxs-lookup"><span data-stu-id="ebf27-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="ebf27-229">Esimerkki: Toimi voidaan määrittää vain yhdelle työntekijälle, mutta Sanjay Patel, joka on nimitetty kirjanpitäjä A:n toimeen, on lähdössä yrityksestä kahden viikon kuluttua.</span><span class="sxs-lookup"><span data-stu-id="ebf27-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="ebf27-230">Joe Healy tulee hänen tilalleen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-230">Joe Healy will replace Sanjay Patel when he leaves.</span></span> <span data-ttu-id="ebf27-231">Vaikka Sanjay on edelleen toimessaan, voit määrittää Joe Healyn samaan toimeen siten, että määritys tulee voimaan vasta Sanjayn viimeisen työpäivän jälkeen.</span><span class="sxs-lookup"><span data-stu-id="ebf27-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>





