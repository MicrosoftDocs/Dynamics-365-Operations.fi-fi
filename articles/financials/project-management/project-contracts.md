---
title: Projektisopimukset
description: "Tässä artikkelissa käsitellään erityyppisille projekteille ja rahoituslähteille luotavia projektisopimuksia, sopimusten hallintaa ja projektin asiakkaiden laskuttamista Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Artikkelissa on myös esimerkkejä."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 0d7d3b64b0d6a662246074b12e3a3fe105dfae47
ms.contentlocale: fi-fi
ms.lasthandoff: 09/14/2017

---

# <a name="project-contracts"></a><span data-ttu-id="15154-103">Projektisopimukset</span><span class="sxs-lookup"><span data-stu-id="15154-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="15154-104">Tässä artikkelissa käsitellään erityyppisille projekteille ja rahoituslähteille luotavia projektisopimuksia, sopimusten hallintaa ja projektin asiakkaiden laskuttamista Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa. Artikkelissa on myös esimerkkejä.</span><span class="sxs-lookup"><span data-stu-id="15154-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="15154-105">Projektisopimukselle luotavan projektin tyyppi määrittää, miten projektin asiakkaita laskutetaan.</span><span class="sxs-lookup"><span data-stu-id="15154-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="15154-106">Vaikka voit muuttaa projektisopimusta ja siihen liittyvää projektia, et voi vaihtaa projektityyppiä.</span><span class="sxs-lookup"><span data-stu-id="15154-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="15154-107">Projektisopimuksen avulla voit laskuttaa yhden projektin tai useita projekteja samanaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="15154-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="15154-108">Projektisopimus auttaa lisäksi varmistamaan, että projektirakenteen kaikissa aliprojekteissa käytetään yhdenmukaista laskutusmenettelyä.</span><span class="sxs-lookup"><span data-stu-id="15154-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="15154-109">Jokainen laskutettava projekti on liitettävä johonkin projektisopimukseen.</span><span class="sxs-lookup"><span data-stu-id="15154-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="15154-110">Projektisopimuksen asetukset koskevat kaikkia projektisopimukseen liittyviä projekteja ja aliprojekteja.</span><span class="sxs-lookup"><span data-stu-id="15154-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="15154-111">Projektisopimus voi määrittää vähintään yhden rahoituslähteen.</span><span class="sxs-lookup"><span data-stu-id="15154-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="15154-112">Niinpä voitkin jakaa laskutuksen usean rahoittajan kesken, määrittää rahoitusrajat niin, että rahoituslähteiltä laskutetaan enintään määritetty summa, ja määrittää rahoitussäännöt menojen laskuttamista varten.</span><span class="sxs-lookup"><span data-stu-id="15154-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="15154-113">Projektisopimusten rahoitus</span><span class="sxs-lookup"><span data-stu-id="15154-113">Funding for project contracts</span></span>
<span data-ttu-id="15154-114">Joissakin projektisopimuksissa määritetään, että useat osapuolet jakavat projektikustannusten rahoitusvastuun.</span><span class="sxs-lookup"><span data-stu-id="15154-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="15154-115">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="15154-115">Here are some examples:</span></span>

-   <span data-ttu-id="15154-116">Suuri asiakas, jolla on useita divisioonia, pyytää rahoituksen jakamista divisioonan mukaan.</span><span class="sxs-lookup"><span data-stu-id="15154-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="15154-117">Yritys jakaa suuren projektin kustannukset ulkoisen organisaation kanssa.</span><span class="sxs-lookup"><span data-stu-id="15154-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="15154-118">Kaksi kuntaa rahoittaa yhdessä tieprojektia.</span><span class="sxs-lookup"><span data-stu-id="15154-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="15154-119">Siltaprojekti rahoitetaan julkishallinnolla ja yksityiseltä yritykseltä saatavalla rahoituksella.</span><span class="sxs-lookup"><span data-stu-id="15154-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="15154-120">Voit jakaa Finance and Operationsissa yhden tapahtuman tai koko projektin laskutuksen useiden asiakkaiden, avustusten tai organisaatioiden kesken.</span><span class="sxs-lookup"><span data-stu-id="15154-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="15154-121">Monen rahoittajan projekteissa kaikkia projektin lisärahoitukseen osallistuvia kutsutaan rahoituslähteiksi.</span><span class="sxs-lookup"><span data-stu-id="15154-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="15154-122">Kun asiakas, organisaatio tai avustus on määritetty rahoituslähteeksi, se määrittää vähintään yhteen rahoitussääntöön.</span><span class="sxs-lookup"><span data-stu-id="15154-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="15154-123">Säännöt sisältävät kriteerit, jotka määrittävät, miten kulut kohdistetaan projektin useita rahoituslähteitä.</span><span class="sxs-lookup"><span data-stu-id="15154-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="15154-124">Koska varastoituja nimikkeitä, kuten ostoehdotusten ja ostotilausten nimikkeitä, ei voi jakaa, kustannussummaa ei voi jakaa useiden rahoituslähteiden kesken jakeluajankohtana.</span><span class="sxs-lookup"><span data-stu-id="15154-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="15154-125">Rahoituslähteen arvo onkin 0 (nolla), kunnes varasto-otto on kirjattu.</span><span class="sxs-lookup"><span data-stu-id="15154-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="15154-126">Kun varasto-otto on kirjattu, kustannussumma jaetaan projektin tilin jakosääntöjen mukaan.</span><span class="sxs-lookup"><span data-stu-id="15154-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="15154-127">Voit helpottaa laskutuksen jakamista useiden rahoituslähteiden kesken seuraavien ohjeiden avulla:</span><span class="sxs-lookup"><span data-stu-id="15154-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="15154-128">Määritä kaikki projektille kirjatut tapahtumat käyttämään samaa myyntivaluuttaa kuin projektisopimus.</span><span class="sxs-lookup"><span data-stu-id="15154-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="15154-129">Määritä rahoitusrajat, jotta rahoituslähdettä laskutetaan vain projektin osalta vain määritetty summa.</span><span class="sxs-lookup"><span data-stu-id="15154-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="15154-130">Määritä jokaiselle työntekijälle, luokalle, luokkaryhmälle ja tapahtumatyypille (tai kaikille tapahtumatyypeille) rahoitussäännöt ja rahoitusrajat.</span><span class="sxs-lookup"><span data-stu-id="15154-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="15154-131">Valitse valinnainen alkamis- ja päättymispäivä määrittämään jakso, jolloin kukin rahoitussääntö on voimassa.</span><span class="sxs-lookup"><span data-stu-id="15154-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="15154-132">Määritä prosenttiosuus, josta kukin rahoituslähde vastaa.</span><span class="sxs-lookup"><span data-stu-id="15154-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="15154-133">Määrittää, mikä rahoituslähde vastaa rahoituksen kohdistuslaskelmien aiheuttamista pyöristyseroista.</span><span class="sxs-lookup"><span data-stu-id="15154-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="15154-134">Määritä säännöt määrittämään, miten projektikustannukset laskutetaan ulkoisille asiakkaille ja veloitetaan sisäisille organisaatioille.</span><span class="sxs-lookup"><span data-stu-id="15154-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="15154-135">Kirjaa tapahtumat pidossa olevalle rahoitustilille, kunnes lisärahoitusta saadaan tai kunnes päätät vastata kustannuksista sisäisesti.</span><span class="sxs-lookup"><span data-stu-id="15154-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="15154-136">Tapahtumaan liitettävä veroryhmä määritetään etsimällä veroryhmän määritys projektista.</span><span class="sxs-lookup"><span data-stu-id="15154-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="15154-137">Jos veroryhmän määritys ei ole tehty projektitasolla, sitä etsitään projektisopimuksesta.</span><span class="sxs-lookup"><span data-stu-id="15154-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="15154-138">Esimerkki: Useita rahoituslähteitä (yksinkertainen)</span><span class="sxs-lookup"><span data-stu-id="15154-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="15154-139">Seuraavassa taulussa on skenaarioita rahoituksen kohdistuksen hallinnasta, kun rahoituslähteitä on useita.</span><span class="sxs-lookup"><span data-stu-id="15154-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="15154-140">Nämä skenaariot perustuvat seuraaviin oletuksiin:</span><span class="sxs-lookup"><span data-stu-id="15154-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="15154-141">Prioriteettiasetukset huomioidaan varojen kohdistuksessa ennen rahoitussääntöehtojen käyttöä.</span><span class="sxs-lookup"><span data-stu-id="15154-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="15154-142">Rahoitussäännön kelpoisuusaikaa aika ei ole määritetty päivämääräalueella.</span><span class="sxs-lookup"><span data-stu-id="15154-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15154-143"><strong>Skenaario</strong></span><span class="sxs-lookup"><span data-stu-id="15154-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="15154-144"><strong>Rahoituslähde </strong></span><span class="sxs-lookup"><span data-stu-id="15154-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="15154-145"><strong>Kohdistusprosentti </strong></span><span class="sxs-lookup"><span data-stu-id="15154-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="15154-146"><strong>Kohdistusprioriteetti </strong></span><span class="sxs-lookup"><span data-stu-id="15154-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15154-147">Haluat kohdistaa kustannukset yhteen rahoituslähteeseen, kunnes sen varat on käytetty, sitten toiseen rahoituslähteeseen, kunnes sen varat on käytetty, ja lopuksi jäljellä olevat kustannukset kolmanteen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="15154-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-148">Rahoituslähde 1</span><span class="sxs-lookup"><span data-stu-id="15154-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="15154-149">Rahoituslähde 2</span><span class="sxs-lookup"><span data-stu-id="15154-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="15154-150">Rahoituslähde 3</span><span class="sxs-lookup"><span data-stu-id="15154-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-151">100 %</span><span class="sxs-lookup"><span data-stu-id="15154-151">100%</span></span></li>
<li><span data-ttu-id="15154-152">100 %</span><span class="sxs-lookup"><span data-stu-id="15154-152">100%</span></span></li>
<li><span data-ttu-id="15154-153">100 %</span><span class="sxs-lookup"><span data-stu-id="15154-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-154">1</span><span class="sxs-lookup"><span data-stu-id="15154-154">1</span></span></li>
<li><span data-ttu-id="15154-155">2</span><span class="sxs-lookup"><span data-stu-id="15154-155">2</span></span></li>
<li><span data-ttu-id="15154-156">3</span><span class="sxs-lookup"><span data-stu-id="15154-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15154-157">Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="15154-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="15154-158">Kun jommankumman rahoituslähteet varat on käytetty, haluat maksaa jäljellä olevat kustannukset kolmannesta rahoituslähteestä.</span><span class="sxs-lookup"><span data-stu-id="15154-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-159">Rahoituslähde 1</span><span class="sxs-lookup"><span data-stu-id="15154-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="15154-160">Rahoituslähde 2</span><span class="sxs-lookup"><span data-stu-id="15154-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="15154-161">Rahoituslähde 3</span><span class="sxs-lookup"><span data-stu-id="15154-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-162">75 %</span><span class="sxs-lookup"><span data-stu-id="15154-162">75%</span></span></li>
<li><span data-ttu-id="15154-163">25 %</span><span class="sxs-lookup"><span data-stu-id="15154-163">25%</span></span></li>
<li><span data-ttu-id="15154-164">100 %</span><span class="sxs-lookup"><span data-stu-id="15154-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-165">1</span><span class="sxs-lookup"><span data-stu-id="15154-165">1</span></span></li>
<li><span data-ttu-id="15154-166">1</span><span class="sxs-lookup"><span data-stu-id="15154-166">1</span></span></li>
<li><span data-ttu-id="15154-167">2</span><span class="sxs-lookup"><span data-stu-id="15154-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15154-168">Haluat kohdistaa 75 prosenttia kustannuksista yhteen rahoituslähteeseen ja 25 prosenttia toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="15154-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="15154-169">Kun jommankumman rahoituslähteet varat on käytetty, haluat jakaa jäljellä olevat kustannukset kolmannen ja neljännen rahoituslähteen kesken.</span><span class="sxs-lookup"><span data-stu-id="15154-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-170">Rahoituslähde 1</span><span class="sxs-lookup"><span data-stu-id="15154-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="15154-171">Rahoituslähde 2</span><span class="sxs-lookup"><span data-stu-id="15154-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="15154-172">Rahoituslähde 3</span><span class="sxs-lookup"><span data-stu-id="15154-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="15154-173">Rahoituslähde 4</span><span class="sxs-lookup"><span data-stu-id="15154-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-174">75 %</span><span class="sxs-lookup"><span data-stu-id="15154-174">75%</span></span></li>
<li><span data-ttu-id="15154-175">25 %</span><span class="sxs-lookup"><span data-stu-id="15154-175">25%</span></span></li>
<li><span data-ttu-id="15154-176">50 %</span><span class="sxs-lookup"><span data-stu-id="15154-176">50%</span></span></li>
<li><span data-ttu-id="15154-177">50 %</span><span class="sxs-lookup"><span data-stu-id="15154-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-178">1</span><span class="sxs-lookup"><span data-stu-id="15154-178">1</span></span></li>
<li><span data-ttu-id="15154-179">1</span><span class="sxs-lookup"><span data-stu-id="15154-179">1</span></span></li>
<li><span data-ttu-id="15154-180">2</span><span class="sxs-lookup"><span data-stu-id="15154-180">2</span></span></li>
<li><span data-ttu-id="15154-181">2</span><span class="sxs-lookup"><span data-stu-id="15154-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15154-182">Haluat kohdistaa ensimmäiset 25 prosenttia kustannuksista yhteen rahoituslähteeseen ja loput toiseen rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="15154-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-183">Rahoituslähde 1</span><span class="sxs-lookup"><span data-stu-id="15154-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="15154-184">Rahoituslähde 2</span><span class="sxs-lookup"><span data-stu-id="15154-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-185">25 %</span><span class="sxs-lookup"><span data-stu-id="15154-185">25%</span></span></li>
<li><span data-ttu-id="15154-186">100 %</span><span class="sxs-lookup"><span data-stu-id="15154-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15154-187">1</span><span class="sxs-lookup"><span data-stu-id="15154-187">1</span></span></li>
<li><span data-ttu-id="15154-188">2</span><span class="sxs-lookup"><span data-stu-id="15154-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="15154-189">Esimerkki: Useita rahoituslähteitä (monitahoinen)</span><span class="sxs-lookup"><span data-stu-id="15154-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="15154-190">Sinulla on kolme rahoituslähdettä, joita haluat käyttää seuraavassa järjestyksessä:</span><span class="sxs-lookup"><span data-stu-id="15154-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="15154-191">Käytä rahoituslähdettä 2 ja 3 yhtä paljon, kunnes rahoituslähde 2 on kulutettu.</span><span class="sxs-lookup"><span data-stu-id="15154-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="15154-192">Jatka rahoituslähteen 3 käyttöä, kunnes se on kulutettu.</span><span class="sxs-lookup"><span data-stu-id="15154-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="15154-193">Käytä rahoituslähdettä 1 sen jälkeen, kun rahoituslähde 3 on kulutettu.</span><span class="sxs-lookup"><span data-stu-id="15154-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="15154-194">Voit saavuttaa tämän tavoitteen toimimalla seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="15154-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="15154-195">Määritä rahoituslähteille 2 ja 3 kummallekin rahoitusrajasumma.</span><span class="sxs-lookup"><span data-stu-id="15154-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="15154-196">Luo seuraavat rahoitussäännöt:</span><span class="sxs-lookup"><span data-stu-id="15154-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="15154-197">Sääntö 1 (prioriteetti 1): kohdistaa 50 prosenttia tapahtumista rahoituslähteeseen 2 ja 50 prosenttia rahoituslähteeseen 3.</span><span class="sxs-lookup"><span data-stu-id="15154-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="15154-198">Sääntö 2 (prioriteetti 2): kohdista 100 prosenttia tapahtumista rahoituslähteeseen 3.</span><span class="sxs-lookup"><span data-stu-id="15154-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="15154-199">Sääntö 3 (prioriteetti 3): kohdista 100 prosenttia tapahtumista rahoituslähteeseen 1.</span><span class="sxs-lookup"><span data-stu-id="15154-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="15154-200">Nämä asetukset toimivat, koska tapahtumia verrataan sääntöihin ja rajoihin, joiden perustella määritetään, käytetäänkö niitä mitään tapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="15154-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="15154-201">Jos mitään tiettyä sääntöä tai rajaa ei käytetä tapahtumassa, käytetään kaikkien tapahtumien sääntöä.</span><span class="sxs-lookup"><span data-stu-id="15154-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="15154-202">Kaikkien tapahtumien sääntö vastaa kaikkia tapahtumia.</span><span class="sxs-lookup"><span data-stu-id="15154-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="15154-203">Jos tapahtumaa vastaava sääntö löytyy, kyseisessä säännössä kohdistettua prosenttia käytetään ensin. Tätä ennen kuitenkin tarkistetaan, koskeeko jokin määritetty raja löydettyä vastinetta.</span><span class="sxs-lookup"><span data-stu-id="15154-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="15154-204">Jos soveltuva raja löytyy ja rahoituslähteen varat on kulutettu, rahoitusrajaan liitetty rahoitussääntö hylätään ja ohjelma tarkistaa seuraavan käytettävän säännön.</span><span class="sxs-lookup"><span data-stu-id="15154-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="15154-205">Joissakin tapauksissa vain osa tapahtumasta voidaan kohdistaa säännön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="15154-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="15154-206">Syynä voi olla esimerkiksi se, että raja saavutetaan tapahtumaa kohdistettaessa.</span><span class="sxs-lookup"><span data-stu-id="15154-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="15154-207">Siinä tapauksessa säännön mukaan kohdistetaan vain tietty summa, kuten 50 prosenttia kuhunkin rahoituslähteeseen.</span><span class="sxs-lookup"><span data-stu-id="15154-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="15154-208">Näin menetellään säännössä 1, joka käsiteltiin aiemmin tässä osassa.</span><span class="sxs-lookup"><span data-stu-id="15154-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="15154-209">Loput kohdistetaan järjestyksessä seuraavan säännön mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="15154-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="15154-210">Seuraavassa taulussa tätä skenaariota käsitellään tarkemmin.</span><span class="sxs-lookup"><span data-stu-id="15154-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="15154-211"><strong>Kohdistus </strong></span><span class="sxs-lookup"><span data-stu-id="15154-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="15154-212"><strong>Erittely</strong></span><span class="sxs-lookup"><span data-stu-id="15154-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15154-213">Rahoitussäännöt</span><span class="sxs-lookup"><span data-stu-id="15154-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-214">Sääntö 1 (prioriteetti 1): Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15154-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="15154-215">Rahoituslähteen 2 kohdistus 50 % ja rahoituslähteen 3 50 %.</span><span class="sxs-lookup"><span data-stu-id="15154-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="15154-216">Sääntö 2 (prioriteetti 2): Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15154-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="15154-217">Rahoituslähteen 3 kohdistus 100 %.</span><span class="sxs-lookup"><span data-stu-id="15154-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="15154-218">Sääntö 3 (prioriteetti 2): Kaikki tapahtumat.</span><span class="sxs-lookup"><span data-stu-id="15154-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="15154-219">Rahoituslähteen 1 kohdistus 100 %.</span><span class="sxs-lookup"><span data-stu-id="15154-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15154-220">Rahoitusrajat</span><span class="sxs-lookup"><span data-stu-id="15154-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-221">Rahoituslähteen 1 raja = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="15154-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="15154-222">Rahoituslähteen 2 raja = 500,00</span><span class="sxs-lookup"><span data-stu-id="15154-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="15154-223">Rahoituslähteen 3 raja = 750,00</span><span class="sxs-lookup"><span data-stu-id="15154-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15154-224">Tapahtuma 1</span><span class="sxs-lookup"><span data-stu-id="15154-224">Transaction 1</span></span></td>
<td><span data-ttu-id="15154-225"><strong>Tapahtuman summa:</strong> 100,00<strong> Rahoitus:</strong> Tapahtuma maksetaan vain säännön 1 mukaisesti, koska tapahtuma on maksettu kokonaan, kun sääntöä 1 on käytetty.</span><span class="sxs-lookup"><span data-stu-id="15154-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="15154-226">Tapahtuma rahoitetaan tason rahoituslähteen 2 ja 3 kesken.</span><span class="sxs-lookup"><span data-stu-id="15154-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="15154-227">Rahoituslähde 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="15154-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="15154-228">Rahoituslähde 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="15154-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="15154-229">Tapahtuma 2</span><span class="sxs-lookup"><span data-stu-id="15154-229">Transaction 2</span></span></td>
<td><span data-ttu-id="15154-230"><strong>Tapahtuman summa:</strong> 5 000.00<strong>Rahoitus:</strong> Tapahtuma maksetaan kolmen säännön mukaisesti.<strong>Sääntö 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="15154-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="15154-231">Rahoituslähde 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="15154-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="15154-232">Rahoituslähde 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="15154-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="15154-233">
<strong>Sääntö 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="15154-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="15154-234">Rahoituslähde 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="15154-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="15154-235">
<strong>Sääntö 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="15154-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="15154-236">Rahoituslähde 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="15154-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="15154-237">Rahoitus yhteensä, joka jaetaan kullekin rahoituslähteelle</span><span class="sxs-lookup"><span data-stu-id="15154-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="15154-238">Rahoituslähde 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="15154-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="15154-239">Rahoituslähde 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="15154-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="15154-240">Rahoituslähde 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="15154-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="15154-241">Laskutussäännöt</span><span class="sxs-lookup"><span data-stu-id="15154-241">Billing rules</span></span>
<span data-ttu-id="15154-242">Kun neuvottelet projektisopimuksen asiakkaan kanssa, voit määrittää, miten ja milloin voit laskuttaa asiakkaalta projektin työn.</span><span class="sxs-lookup"><span data-stu-id="15154-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="15154-243">Voit määrittää projektisopimukseen ja projektin määrittämisen jälkeen projektin laskutussäännöt.</span><span class="sxs-lookup"><span data-stu-id="15154-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="15154-244">Tarjoussäännöt on määritetty projektisopimukseen perustuvissa projektiehdoissa.</span><span class="sxs-lookup"><span data-stu-id="15154-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="15154-245">Luotavat laskutussäännöt määräytyvät projektisopimuksen ehtojen ja projektityypin, kuten Aika ja materiaali tai Kiinteä hinta, mukaan.</span><span class="sxs-lookup"><span data-stu-id="15154-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="15154-246">Voit luoda yhteen projektisopimukseen useita laskutussääntöjä.</span><span class="sxs-lookup"><span data-stu-id="15154-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="15154-247">Voit määrittää laskutussäännön useita projekteja varten, jotka liittyvät samaan projektisopimukseen ja joilla on samanlaiset laskutusehdot.</span><span class="sxs-lookup"><span data-stu-id="15154-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="15154-248">Voit määrittää seuraavat laskutussääntöjen tyypit:</span><span class="sxs-lookup"><span data-stu-id="15154-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="15154-249">**Toimitusyksikkö** – Laskuta asiakasta, kun toimitusyksikkö on valmis.</span><span class="sxs-lookup"><span data-stu-id="15154-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="15154-250">Määrität sopimuksen toimitusyksiköt.</span><span class="sxs-lookup"><span data-stu-id="15154-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="15154-251">**Edistyminen** – Laskuta asiakasta, kun projektista on valmiina tietty prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="15154-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="15154-252">Voit määrittää laskutuksen säännön automaattisesti laskemaan prosenttiosuus työn valmistumisesta, tai voit manuaalisesti laskea prosenttiosuuden työn valmistumisesta ja asiakkaalta laskutettavan summan.</span><span class="sxs-lookup"><span data-stu-id="15154-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="15154-253">**Välitavoite** – laskuta asiakasta projektin välitavoitteen koko summa, kun välitavoite saavutetaan.</span><span class="sxs-lookup"><span data-stu-id="15154-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="15154-254">**Maksu** – laskuta asiakasta palveluistasi sekä veloita häneltä hallinnointipalkkio, joka on tavallisesti prosenttiosuus palveluiden kustannuksesta.</span><span class="sxs-lookup"><span data-stu-id="15154-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="15154-255">**Aika ja materiaali** – laskuta asiakasta projektissa käytetyistä materiaaleista ja ajasta.</span><span class="sxs-lookup"><span data-stu-id="15154-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="15154-256">Voit määrittää kaikentyyppisten laskutussääntöjen kohdalla myyntilaskuista vähennettävän pidätysprosentin, kunnes projekti saavuttaa sovitun vaiheen.</span><span class="sxs-lookup"><span data-stu-id="15154-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="15154-257">Maksun pidätysprosentti määritetään projektisopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="15154-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="15154-258">Summa lasketaan ja vähennetään myyntilaskun rivien kokonaissummasta.</span><span class="sxs-lookup"><span data-stu-id="15154-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="15154-259">Voit määrittää **Aika ja materiaali**- ja **Edistyminen** -laskutussäännöille laskutettavia luokkia.</span><span class="sxs-lookup"><span data-stu-id="15154-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="15154-260">Laskutettavat luokat osoittavat tapahtumat, jotka pitää sisällyttää myyntilaskuihin.</span><span class="sxs-lookup"><span data-stu-id="15154-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="15154-261">Kun olet valmis laskuttamaan asiakasta, projektin laskutettava summa lasketaan laskutuksen säännöillä ja projektin laskuehdotus luodaan.</span><span class="sxs-lookup"><span data-stu-id="15154-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="15154-262">Seuraavissa osassa on esimerkkejä laskutussääntöjen määrittämisestä projektille ja niiden hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="15154-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="15154-263">Esimerkki: Luo toimitettujen yksiköiden määrään perustuva laskutussääntö</span><span class="sxs-lookup"><span data-stu-id="15154-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="15154-264">Organisaatio solmii sopimuksen yhteensä viiden koulutusistunnon toimittamisesta asiakkaan työntekijöille. Kunkin koulutusistunnon hinta on 10 000.</span><span class="sxs-lookup"><span data-stu-id="15154-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="15154-265">Laskutat asiakasta jokaisen koulutusistunnon jälkeen.</span><span class="sxs-lookup"><span data-stu-id="15154-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="15154-266">Käytät sopimuksen laskutussääntöjen määrittämiseen seuraavia arvoja:</span><span class="sxs-lookup"><span data-stu-id="15154-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="15154-267">Toimitusyksikkö on yksi koulutustilaisuus.</span><span class="sxs-lookup"><span data-stu-id="15154-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="15154-268">Yksikköhinta on 10 000 koulutustilaisuutta kohti.</span><span class="sxs-lookup"><span data-stu-id="15154-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="15154-269">Yksiköiden kokonaismäärä on viisi koulutustapahtumaa.</span><span class="sxs-lookup"><span data-stu-id="15154-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="15154-270">Kun yksi koulutusistunto on suoritettu, voit luoda laskun ensimmäisen yksikön toimituksesta summalle 10 000 ja lähettää laskun asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="15154-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="15154-271">Esimerkki: Luo projektin valmistumisasteeseen perustuva laskutussääntö (lasketaan manuaalisesti)</span><span class="sxs-lookup"><span data-stu-id="15154-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="15154-272">Organisaatiosi, joka on erikoistunut ohjelmistokonsultointiin, sitoutuu kehittämään asiakkaalle osan tuotteesta, jota asiakas kehittää.</span><span class="sxs-lookup"><span data-stu-id="15154-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="15154-273">Organisaatiosi sitoutuu toimittamaan tuotteelle ohjelmistokoodia kuuden kuukauden ajan.</span><span class="sxs-lookup"><span data-stu-id="15154-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="15154-274">Asiakas suostuu maksamaan organisaatiollesi työstä yhteensä 100 000.</span><span class="sxs-lookup"><span data-stu-id="15154-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="15154-275">Luot laskutussäännön, jolla asiakasta laskutetaan projektissa suoritetun prosenttimääräisen työn perusteella. Prosenttiosuus on määritetty sopimuksessa.</span><span class="sxs-lookup"><span data-stu-id="15154-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="15154-276">Ensimmäisen kuukauden lopussa tapaat asiakkaan ja määrität valmiin työn osuuden.</span><span class="sxs-lookup"><span data-stu-id="15154-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="15154-277">Kun olette tarkastaneet projektin yhdessä asiakkaan kanssa, päätätte, että projekti on 15-prosenttisesti valmis.</span><span class="sxs-lookup"><span data-stu-id="15154-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="15154-278">Luot laskun summalle 15 000 (15 prosenttia summasta 100 000) ja lähetät sen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="15154-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="15154-279">Esimerkki: Luo projektin valmistumisasteeseen perustuva laskutussääntö (lasketaan automaattisesti)</span><span class="sxs-lookup"><span data-stu-id="15154-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="15154-280">Organisaatiosi on ohjelmistokehitysyritys, joka sopii kehittävänsä asiakkaalle palkanlaskennan kirjanpitopaketin hintaan 30 000.</span><span class="sxs-lookup"><span data-stu-id="15154-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="15154-281">Asiakas sitoutuu maksamaan organisaatiollesi työn valmistumisprosentin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="15154-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="15154-282">Arvioit, että projektikustannukset ovat 20 000.</span><span class="sxs-lookup"><span data-stu-id="15154-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="15154-283">Projektisopimus määrittää työluokat laskutusprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="15154-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="15154-284">Määrität laskutussäännöt, jotka laskevat automaattisesti laskujen summat kunkin luokan töiden valmistumisprosentin mukaan.</span><span class="sxs-lookup"><span data-stu-id="15154-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="15154-285">Asetat budjetin jokaiselle luokalle:</span><span class="sxs-lookup"><span data-stu-id="15154-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="15154-286">**Kehitys** – kustannus 15 000 ja tuotto 20 000</span><span class="sxs-lookup"><span data-stu-id="15154-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="15154-287">**Asennus** – kustannus 5 000 ja tuotto 10 000</span><span class="sxs-lookup"><span data-stu-id="15154-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="15154-288">Kun myyntilasku luodaan ensimmäisen kerran, laskutussumma lasketaan automaattisesti perusteella seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="15154-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="15154-289">Työntekijä lähettää projektiin aikaraportin kuukauden kuluttua.</span><span class="sxs-lookup"><span data-stu-id="15154-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="15154-290">Työntekijän tuntikustannukset ovat 5 000 kehitykselle ja 1 000 asennukselle.</span><span class="sxs-lookup"><span data-stu-id="15154-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="15154-291">Kehitystyöstä on suoritettu 33 prosenttia (toteutunut kustannus 5 000 / budjetoitu kustannus 15 000) ja asennustyöstä on suoritettu 20 prosenttia (toteutunut kustannus 1 000 / budjetoitu kustannus 5 000).</span><span class="sxs-lookup"><span data-stu-id="15154-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="15154-292">Laskun summa 8 667 lasketaan automaattisesti (33 prosenttia 20 000:sta + 20 prosenttia 10 000:sta).</span><span class="sxs-lookup"><span data-stu-id="15154-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="15154-293">Luot laskun summalle 8 667 ja lähetät sen asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="15154-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="15154-294">Esimerkki: Luo laskutussääntö sovittujen välitavoitteiden perusteella</span><span class="sxs-lookup"><span data-stu-id="15154-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="15154-295">Organisaatio on johdon konsultointiyritys, joka on sopinut suorittavansa markkinointitutkimuksen kuluttajatuotteelle, jota asiakas suunnittelee myyvänsä.</span><span class="sxs-lookup"><span data-stu-id="15154-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="15154-296">Asiakas sitoutuu käyttämään palveluitasi kolmen kuukauden ajan maaliskuusta alkaen ja sitoutuu maksamaan organisaatiollesi 50 000.</span><span class="sxs-lookup"><span data-stu-id="15154-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="15154-297">Projektissa on kolme välitavoitetta:</span><span class="sxs-lookup"><span data-stu-id="15154-297">The project has three milestones:</span></span>

-   <span data-ttu-id="15154-298">Välitavoite 1: Kerää kuluttajatiedot – 31. maaliskuuta</span><span class="sxs-lookup"><span data-stu-id="15154-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="15154-299">Välitavoite 2: Analysoi kuluttajatiedot – 30. huhtikuuta</span><span class="sxs-lookup"><span data-stu-id="15154-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="15154-300">Välitavoite 3: esitä ehdotus tuotteen kannattavuudesta – 31. toukokuuta</span><span class="sxs-lookup"><span data-stu-id="15154-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="15154-301">Asiakas sopii maksavansa organisaatiolle 10 000 ensimmäisestä välitavoitteesta, 20 000 toisesta välitavoitteesta ja 20 000 kolmannesta välitavoitteesta.</span><span class="sxs-lookup"><span data-stu-id="15154-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="15154-302">Projektisopimusta määritettäessä sovit laskuttavasi asiakasta valmistuneen välitavoitteen perusteella.</span><span class="sxs-lookup"><span data-stu-id="15154-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="15154-303">Laskutussääntöasetukset sisältävät seuraavat vaiheet:</span><span class="sxs-lookup"><span data-stu-id="15154-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="15154-304">Määritä projektin välitavoitteet.</span><span class="sxs-lookup"><span data-stu-id="15154-304">Define the project milestones.</span></span>
-   <span data-ttu-id="15154-305">Määritä summa, joka asiakkaalta laskutetaan, kun kukin välitavoite valmistuu.</span><span class="sxs-lookup"><span data-stu-id="15154-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="15154-306">Kun ensimmäinen välitavoite valmistuu 31. maaliskuuta, merkitset välitavoitteen valmiiksi ja luot sitten laskun summalle 10 000. Lasku lähetetään asiakkaalle.</span><span class="sxs-lookup"><span data-stu-id="15154-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="15154-307">Et voi luoda laskua välitavoitteelle, ennen kuin välitavoite on merkitty valmiiksi.</span><span class="sxs-lookup"><span data-stu-id="15154-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="15154-308">Esimerkki: Luo palveluihin ja hallintokuluun perustuva laskutussääntö</span><span class="sxs-lookup"><span data-stu-id="15154-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="15154-309">Organisaatio on johdon konsultointiyritys, joka on sopinut suorittavansa markkinointitutkimuksen arvioidakseen asiakkaan, vähittäismyyntiyrityksen, kehittämän tuotteen kannattavuuden.</span><span class="sxs-lookup"><span data-stu-id="15154-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="15154-310">Sopimuksen ehdoissa määritetään, että käytettävissä on yrityksen kolmen parhaan johdon konsultin palvelut ja että käytössä on veloitus käytetyn ajan ja materiaalin perusteella.</span><span class="sxs-lookup"><span data-stu-id="15154-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="15154-311">Asiakas sopii maksuksi 100/tunti ja 10 prosentin hallintakulun projektiin käytettyjen konsultointituntien osalta.</span><span class="sxs-lookup"><span data-stu-id="15154-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="15154-312">Luo projektisopimusta määritettäessä laskutussääntö, joka lisää 10 prosentin hallintokulun projektissa käytettyihin konsultointitunteihin.</span><span class="sxs-lookup"><span data-stu-id="15154-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="15154-313">Kun luot laskun asiakkaalle, asiakkaalta laskutetaan 10 prosentin hallintokulu ja konsultointituntien hinta.</span><span class="sxs-lookup"><span data-stu-id="15154-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="15154-314">Jos esimerkiksi kolme konsulttia työskenteli projektissa yhteensä 200 tuntia, lasku luodaan summalle 22 000 seuraavan laskelman perusteella:</span><span class="sxs-lookup"><span data-stu-id="15154-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="15154-315">200 tuntia 100 tunnissa = 20,000</span><span class="sxs-lookup"><span data-stu-id="15154-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="15154-316">10 prosentin hallintamaksu = 2 000</span><span class="sxs-lookup"><span data-stu-id="15154-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="15154-317">Laskun kokonaissumma = 22.000</span><span class="sxs-lookup"><span data-stu-id="15154-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="15154-318">Jos maksut ovat verotettavia asiakkaalle ja arvonlisäveroryhmä valitaan projektisopimukseen, arvonlisäveroryhmä syötetään automaattisesti laskutuksen säännön maksuille.</span><span class="sxs-lookup"><span data-stu-id="15154-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="15154-319">Esimerkki: Luo laskutussääntö ajan ja materiaalien arvolle</span><span class="sxs-lookup"><span data-stu-id="15154-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="15154-320">Organisaatiosi on ohjelmointialan konsulttiyritys, joka sopii toimittavansa viisi teknistä konsulttia työskentelemään asiakkaan ohjelmistokehitysprojektissa seuraavan kuuden kuukauden ajan.</span><span class="sxs-lookup"><span data-stu-id="15154-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="15154-321">Asiakas sopii maksavansa 150/konsultointitunnista ja toimistotarvikekulut.</span><span class="sxs-lookup"><span data-stu-id="15154-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="15154-322">Organisaatiosi lähettää laskun asiakkaalle jokaisen kuukauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="15154-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="15154-323">Projektisopimusta määritettäessä sovit laskuttavasi asiakasta joka kuukausi projektiin käytetyn ajan ja materiaalin perusteella.</span><span class="sxs-lookup"><span data-stu-id="15154-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="15154-324">Luot laskutussäännön, joka sisältää seuraavat tiedot:</span><span class="sxs-lookup"><span data-stu-id="15154-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="15154-325">Sopimuskausi on kuusi kuukautta.</span><span class="sxs-lookup"><span data-stu-id="15154-325">The contract period is six months.</span></span>
-   <span data-ttu-id="15154-326">Konsultointiaika lasketaan hinnalla 150/tunti.</span><span class="sxs-lookup"><span data-stu-id="15154-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="15154-327">Toimistotarvikkeet laskutetaan kustannuksen perusteella, eikä projektin kokonaiskustannus voi olla suurempi kuin 10 000.</span><span class="sxs-lookup"><span data-stu-id="15154-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="15154-328">Luot myyntilaskun projektin aikana kunkin kalenterikuukauden lopussa.</span><span class="sxs-lookup"><span data-stu-id="15154-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="15154-329">Konsultit kirjaavat projektiin ensimmäisen kuukauden aikana yhteensä 800 tuntia.</span><span class="sxs-lookup"><span data-stu-id="15154-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="15154-330">Projektin veloitettujen toimistotarvikkeiden kustannus on 2 000.</span><span class="sxs-lookup"><span data-stu-id="15154-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="15154-331">Niinpä kuukauden lopussa luodaan arvo, jonka arvo on 122 000 (800 tuntia x 150/tunti + 2 000 toimistotarvikkeisiin).</span><span class="sxs-lookup"><span data-stu-id="15154-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




