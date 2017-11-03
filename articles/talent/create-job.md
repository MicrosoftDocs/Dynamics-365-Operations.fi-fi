---
title: "Työn komponenttien määrittäminen"
description: "Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 962b3084c5340813d1697cab680621350510d4b9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="6ba93-103">Työn komponenttien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="6ba93-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="6ba93-104">Tässä aiheessa kuvataan käsitteellisiä elementtejä, joita työssä voi olla ja annetaan esimerkkejä siitä, miten voit käyttää näitä elementtejä organisaatiossasi.</span><span class="sxs-lookup"><span data-stu-id="6ba93-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="6ba93-105">Ennen kuin voit luoda uusia töitä, sinun pitää määrittää joitakin viitetietoja.</span><span class="sxs-lookup"><span data-stu-id="6ba93-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="6ba93-106">Voit luoda työn, jolla on vain nimi.</span><span class="sxs-lookup"><span data-stu-id="6ba93-106">You can create a job that has only a name.</span></span> <span data-ttu-id="6ba93-107">Kuitenkin antamalla lisätiedot, kuten tehtävänimike, annat oletusarvot toimille, jotka on määritetty työhön.</span><span class="sxs-lookup"><span data-stu-id="6ba93-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="6ba93-108">Lisäksi joitakin antamiasi tietoja voidaan käyttää suodattamaan kompensaatiosuunnitelmia tiettyihin töihin.</span><span class="sxs-lookup"><span data-stu-id="6ba93-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="6ba93-109">Jos haluat määrittää oikeutuksen, jota voit käyttää suodattamaan kompensaatiosuunnitelmia tiettyyn työhön, sinun on määritettävä työtehtävät ja työtyypit ennen töiden määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="6ba93-110">Kun nämä oletusarvot on käytettävissä, säästät aikaa, kun lisäät toimia työhön.</span><span class="sxs-lookup"><span data-stu-id="6ba93-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="6ba93-111">Jotkin työtä koskevat tiedot, kuten ammattinimike, tyyppi ja toiminto, ovat päivämääräsidonnaisia.</span><span class="sxs-lookup"><span data-stu-id="6ba93-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="6ba93-112">Jos luot työn tänään, mutta lisäät näitä tietoja vasta myöhemmin, ja sitten katsot työtä luontipäivämäärän suhteen, nämä tiedot eivät näy.</span><span class="sxs-lookup"><span data-stu-id="6ba93-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="6ba93-113">Siksi kannattaa luoda joitakin näitä viitetietoja ennen kuin niitä vaaditaan.</span><span class="sxs-lookup"><span data-stu-id="6ba93-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="6ba93-114">Tällä tavalla voit lisätä tiedot uusiin töihin niitä luotaessa.</span><span class="sxs-lookup"><span data-stu-id="6ba93-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="6ba93-115">Ammattinimikkeet</span><span class="sxs-lookup"><span data-stu-id="6ba93-115">Job titles</span></span>
<span data-ttu-id="6ba93-116">Ennen kuin voit luoda töitä, on määritettävä kyseisten töiden otsikot.</span><span class="sxs-lookup"><span data-stu-id="6ba93-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="6ba93-117">Toimet perivät ammattinimikkeet töiltä, joihin toimet liittyvät.</span><span class="sxs-lookup"><span data-stu-id="6ba93-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="6ba93-118">Ylläpidä ammattinimikkeitä käyttäen **Tittelit**-sivua, jonka voit avata käyttämällä hakutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="6ba93-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="6ba93-119">Anna **Tittelit **-sivulla tittelit, joita aiot käyttää töihisi.</span><span class="sxs-lookup"><span data-stu-id="6ba93-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="6ba93-120">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="6ba93-120">Job types</span></span>
<span data-ttu-id="6ba93-121">Työtyyppien avulla voi luokitella samankaltaisia töitä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="6ba93-122">Työtyypit eivät ole pakollisia.</span><span class="sxs-lookup"><span data-stu-id="6ba93-122">Job types aren't required.</span></span> <span data-ttu-id="6ba93-123">Kuitenkin jos aiot käyttää työtyyppejä, kun määrität oikeutussäännöt kompensaationhallintaan, sinun tulee määrittää työtyypit ennen töiden määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="6ba93-124">Työtyypit ovat: kokopäiväinen ja osa-aikainen sekä kuukausipalkka tai tuntipalkka.</span><span class="sxs-lookup"><span data-stu-id="6ba93-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6ba93-125">Voit ylläpitää työtyyppejä **Työtyypit**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6ba93-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="6ba93-126">Anna **Työtyypit**-sivulla työtyypin nimi ja lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6ba93-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="6ba93-127">Valitse **Vapautustila**-kentässä jokin seuraavista asetuksista ja ilmaistaksesi Fair Labor Standards Act (FLSA) -vapautustilan tämän työtyypin töille:</span><span class="sxs-lookup"><span data-stu-id="6ba93-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="6ba93-128">**Vapautus** – Työt on vapautettu ylitöistä FLSA-säädösten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6ba93-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="6ba93-129">**Ei vapautusta** – Töitä ei ole vapautettu ylitöistä FLSA-säädösten mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="6ba93-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="6ba93-130">**Ei koske** – FLSA-kattavuus ei ole käytössä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="6ba93-131">Työtehtävät</span><span class="sxs-lookup"><span data-stu-id="6ba93-131">Job functions</span></span>
<span data-ttu-id="6ba93-132">Työtehtävät kuvaavat toiminnalliset luokat korkealla tasolla ja yhdistävät korkean tason velvollisuudet.</span><span class="sxs-lookup"><span data-stu-id="6ba93-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="6ba93-133">Työtehtävät eivät ole pakollisia.</span><span class="sxs-lookup"><span data-stu-id="6ba93-133">Job functions aren't required.</span></span> <span data-ttu-id="6ba93-134">Voit käyttää työtehtäviä yhdessä työtyyppien kanssa suodattaaksesi kompensaatiosuunnitelmia tiettyihin töihin.</span><span class="sxs-lookup"><span data-stu-id="6ba93-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="6ba93-135">Voit liittää työtehtävät ja työtyypit kompensaatiosuunnitelmiin määrittämällä oikeutussäännöt **Oikeutussäännöt**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6ba93-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="6ba93-136">Sitten voit liittää kompensaatiosuunnitelmaan tasojoukon, jota käytetään tietyssä oikeutussäännön kautta määritetyssä työtyypin ja -tehtävän yhdistelmässä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="6ba93-137">(Nämä ominaisuudet koskevat sekä kiinteitä kompensaatiosuunnitelmia että muuttuvia kompensaatiosuunnitelmia). Jos kuitenkin aiot käyttää työtehtäviä, kun määrität oikeutussäännöt kompensaationhallinnalle, sinun tulee määrittää työtehtävät ennen kuin määrität työt.</span><span class="sxs-lookup"><span data-stu-id="6ba93-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="6ba93-138">Seuraavassa taulukossa on joitakin esimerkkejä työtehtävistä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="6ba93-139">Työ</span><span class="sxs-lookup"><span data-stu-id="6ba93-139">Job</span></span>           | <span data-ttu-id="6ba93-140">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="6ba93-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="6ba93-141">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="6ba93-141">Sales manager</span></span> | <span data-ttu-id="6ba93-142">Keskijohdon päällikkö</span><span class="sxs-lookup"><span data-stu-id="6ba93-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="6ba93-143">Kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="6ba93-143">Accountant</span></span>    | <span data-ttu-id="6ba93-144">Ammattilaiset</span><span class="sxs-lookup"><span data-stu-id="6ba93-144">Professionals</span></span>        |

<span data-ttu-id="6ba93-145">Voit ylläpitää työtehtäviä **Työtehtävät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6ba93-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="6ba93-146">Anna **Työtehtävät**-sivulla työtehtävän tunnistekoodi ja lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6ba93-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="6ba93-147">Työtehtävät</span><span class="sxs-lookup"><span data-stu-id="6ba93-147">Job tasks</span></span>
<span data-ttu-id="6ba93-148">Työtehtävät kuvaavat kyseisessä toimessa toimivan työntekijän perustehtäviä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="6ba93-149">Sama työtehtävä voidaan lisätä useisiin töihin, ja sellaisten töiden toimiin, jotka käyttävät näitä työtehtäviä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="6ba93-150">Seuraavassa taulukossa on joitakin esimerkkejä työtehtävistä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ba93-151">Työ</span><span class="sxs-lookup"><span data-stu-id="6ba93-151">Job</span></span></th>
<th><span data-ttu-id="6ba93-152">Työtehtävä</span><span class="sxs-lookup"><span data-stu-id="6ba93-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ba93-153">Myyntipäällikkö</span><span class="sxs-lookup"><span data-stu-id="6ba93-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="6ba93-154"><strong>Suorituskykytarkistus</strong> – Arvioi jokaisen myyjän suorituskykyä.</span><span class="sxs-lookup"><span data-stu-id="6ba93-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="6ba93-155"><strong>Poissaolotarkistus</strong> – Hyväksy tai hylkää kunkin myyjän poissaolopyynnöt tai -rekisteröinnit.</span><span class="sxs-lookup"><span data-stu-id="6ba93-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ba93-156">Kirjanpitäjä</span><span class="sxs-lookup"><span data-stu-id="6ba93-156">Accountant</span></span></td>
<td><span data-ttu-id="6ba93-157"><strong>TAL-raportti</strong> – Esitä viikoittaiset talousraportit talousjohtajalle.</span><span class="sxs-lookup"><span data-stu-id="6ba93-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6ba93-158">Voit ylläpitää työtehtäviä **Työtehtävät**-sivulla.</span><span class="sxs-lookup"><span data-stu-id="6ba93-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="6ba93-159">Anna **Työtehtävät**-sivulla työtehtävän nimi ja lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6ba93-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="6ba93-160">Voit myös lisätä lisätietoja **Huomautus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6ba93-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="6ba93-161">Muistiinpanoja voi päivittää tietylle työlle muuttamatta tähän kirjoitettuja muistiinpanoja.</span><span class="sxs-lookup"><span data-stu-id="6ba93-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="6ba93-162">Vastuualueet</span><span class="sxs-lookup"><span data-stu-id="6ba93-162">Areas of responsibility</span></span>
<span data-ttu-id="6ba93-163">Vastuualueiden avulla voi osoittaa tietyssä toimessa toimivan työntekijän vastuulla olevat työroolit, prosessit ja tuotteet.</span><span class="sxs-lookup"><span data-stu-id="6ba93-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="6ba93-164">Esimerkiksi Kirjanpitäjä-toimessa vastuualue voi olla Tuotteen A talousraportointi.</span><span class="sxs-lookup"><span data-stu-id="6ba93-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="6ba93-165">Ylläpidä vastuualueita **Vastuualueet**-sivulla, jonka voit etsiä käyttämällä hakutoimintoa.</span><span class="sxs-lookup"><span data-stu-id="6ba93-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="6ba93-166">Anna **Vastuualueet**-sivulla vastuun nimi ja lyhyt kuvaus.</span><span class="sxs-lookup"><span data-stu-id="6ba93-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="6ba93-167">Voit myös lisätä lisätietoja **Huomautus**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="6ba93-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="6ba93-168">Muistiinpanoja voi päivittää tietylle työlle muuttamatta tähän kirjoitettuja muistiinpanoja.</span><span class="sxs-lookup"><span data-stu-id="6ba93-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>




