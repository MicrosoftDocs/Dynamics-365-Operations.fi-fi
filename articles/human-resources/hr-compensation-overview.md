---
title: Kompensaatiosuunnitelmat
description: Kompensaatio- ja etuuspäälliköt voiva käyttää kompensaation hallintaa organisaation työntekijöiden kiinteiden ja muuttuvien kompensaatiosuunnitelmien ylläpitämisessä ja käsittelemisessä.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: d537f17dad7e511400c48c6e624f7644048d1c6d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465723"
---
# <a name="compensation-plans"></a><span data-ttu-id="1fbb2-103">Kompensaatiosuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="1fbb2-103">Compensation plans</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fbb2-104">Kompensaatio- ja etuuspäälliköt voiva käyttää kompensaation hallintaa organisaation työntekijöiden kiinteiden ja muuttuvien kompensaatiosuunnitelmien ylläpitämisessä ja käsittelemisessä.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="1fbb2-105">Johdanto</span><span class="sxs-lookup"><span data-stu-id="1fbb2-105">Introduction</span></span>

<span data-ttu-id="1fbb2-106">Kompensaationhallinnan avulla ohjataan peruspalkan ja palkkioiden maksamista.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="1fbb2-107">Työntekijän kiinteän peruspalkan ja bonusten korotuksia hallitaan kiinteän kompensaatiosuunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="1fbb2-108">Bonusmaksujen, suorituskykypalkkioiden, optioiden, lahjoitusten sekä muiden kannusteiden maksamista hallitaan muuttuvan kompensaation suunnitelmien avulla.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="1fbb2-109">Työntekijä voidaan liittää yhteen tai useaan suunnitelmaan, ja työntekijällä voidaan käyttää kumpaakin suunnitelmatyyppiä.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="1fbb2-110">Työntekijän on täytettävä seuraavat vaatimukset, ennen kuin hänet voi rekisteröidä kompensaatiosuunnitelmaan:</span><span class="sxs-lookup"><span data-stu-id="1fbb2-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="1fbb2-111">Työntekijällä on oltava aktiivinen toimen määritys.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="1fbb2-112">Työntekijä on täytettävä kompensaatiosuunnitelman kelpoisuussääntöjen ehdot.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="1fbb2-113">Kompensaation määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1fbb2-113">Compensation setup</span></span>
<span data-ttu-id="1fbb2-114">Seuraavassa taulukossa on luettelo kompensaatioprosessin komponenteista, jotka voivat olla olennaisia yrityksen kompensaatiosuunnitelmien määrittämisessä.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1fbb2-115">Komponentti</span><span class="sxs-lookup"><span data-stu-id="1fbb2-115">Component</span></span></th>
<th><span data-ttu-id="1fbb2-116">Lisätietoja…</span><span class="sxs-lookup"><span data-stu-id="1fbb2-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fbb2-117">Kiinteän kompensaation toiminnot</span><span class="sxs-lookup"><span data-stu-id="1fbb2-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="1fbb2-118">Kiinteän kompensaation toiminnot, joilla on kaksi tarkoitusta:</span><span class="sxs-lookup"><span data-stu-id="1fbb2-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="1fbb2-119">Toiminnoilla voidaan määrittää minkälaiset tiedot on kirjattava, kun työntekijän kompensaatio muuttuu.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="1fbb2-120">Voit esimerkiksi edellyttää, että muutoksen syy, kuten ylennys tai alennus, kirjataan.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="1fbb2-121">Toiminnot voivat varmistaa, että laskentaa käytetään, kun kiinteitä kompensaatiosuunnitelmia käsitellään.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="1fbb2-122">Esimerkiksi Oma pääoma -tyypin toiminnot vertaavat työntekijöiden palkkaa työntekijän&#39;tason vähimmäisviitepisteeseen, mikä varmistaa, että työntekijälle maksetaan ainakin minimipalkka.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-123">Tasot</span><span class="sxs-lookup"><span data-stu-id="1fbb2-123">Levels</span></span></td>
<td><span data-ttu-id="1fbb2-124">Tasot on liitetty töihin ja mahdollisiin työviittaukseen liittyviin toimiin.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="1fbb2-125">Voit luoda yksittäisiä tasoja kolmelle kompensaatiosuunnitelmatyypille: palkkaluokka, kompensaatioluokka ja vaihe.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-126">Palkka-alueen käyttöastematriisi</span><span class="sxs-lookup"><span data-stu-id="1fbb2-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="1fbb2-127">Palkka-alueen käyttöastematriisi auttaa siirtämään työntekijät työtä vastaavaan tarkistuspisteeseen.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="1fbb2-128">Voit myös ohjata palkka-alueen käyttöasteen avulla yrityksen palkkiopääomia huomioimatta yksittäisen työntekijän&#39;suoritustasoa tai yrityksen yleistä suoritustasoa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="1fbb2-129">Esimerkiksi työntekijöille, joille maksetaan palkka-alueella pienempää palkkaa, annetaan suuremmat prosenttikorotukset kuin palkka-alueella suurempaa palkkaa saaville työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="1fbb2-130">Tällä tavoin voit järjestelmällisesti siirtää pääoman eroja.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="1fbb2-131">Palkka-alueen käyttöaste lasketaan seuraavasti: (kiinteä palkkio – alueen vähimmäisarvominimi) ÷ (alueen enimmäisarvo – alueen vähimmäisarvo).</span><span class="sxs-lookup"><span data-stu-id="1fbb2-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-132">Viitepisteiden määritykset</span><span class="sxs-lookup"><span data-stu-id="1fbb2-132">Reference point setups</span></span></td>
<td><span data-ttu-id="1fbb2-133">Viitepisteiden määritykset sisältävät matriisin palkka-alueita kuvaavien viitepisteiden joukon.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="1fbb2-134">Kukin palkka-alue voidaan liittää palkkioon.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="1fbb2-135">Palkkaluokka suunnitelmissa käytetään viitepisteinä usein vähimmäisarvo, keskiarvoa ja enimmäisarvoa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-136">Kompensaatiomatriisi</span><span class="sxs-lookup"><span data-stu-id="1fbb2-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="1fbb2-137">Kompensaatiomatriisin on joukko viitepisteitä ja tasoja, joiden avulla luodaan kompensaatiorakenne.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-138">Kompensaatiorakenne</span><span class="sxs-lookup"><span data-stu-id="1fbb2-138">Compensation structure</span></span></td>
<td><span data-ttu-id="1fbb2-139">Kompensaatiorakenne on kompensaatiomatriisi, jossa palkkiot on liitetty kunkin tason viitepisteisiin.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-140">Oikeutussäännöt</span><span class="sxs-lookup"><span data-stu-id="1fbb2-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="1fbb2-141">Oikeutussääntöjen avulla tunnistetaan tiettyjen töiden, työtehtävien, työtyyppien, osastojen, ammattijärjestöjen tai kompensaatioalueiden työntekijät, joita tietyt kompensaatiosuunnitelmat koskevat.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="1fbb2-142">Oikeutussäännöt on luotava sekä muuttuville että kiinteille kompensaatiosuunnitelmille, jotta työntekijä voidaan rekisteröidä suunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="1fbb2-143">Kun kompensaatiosuunnitelman oikeutussäännöt on määritetty, voit määrittää tasot, joita sovelletaan suunnitelman kattamiin töihin.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-144">Maksutiheydet</span><span class="sxs-lookup"><span data-stu-id="1fbb2-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="1fbb2-145">Maksutiheyksien avulla määritetään aikajakso, jolle kompensaation on määritetty.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="1fbb2-146">Esimerkiksi maksutiheys auttaa sinua ymmärtämään, jos kompensaatiosumma määritetään vuotuisena palkkana vs. tuntihintana.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="1fbb2-147">Maksutiheyksiä myös käytetään määrittämään muuntokertoimet, joiden avulla muunnetaan kompensaatiosummia kuukausittaisista, viikoittaisista, kahden viikon jaksoista ja tuntikohtaisista maksuista vuosittaiseen maksutiheyteen.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-148">Kompensaatioalueet</span><span class="sxs-lookup"><span data-stu-id="1fbb2-148">Compensation regions</span></span></td>
<td><span data-ttu-id="1fbb2-149">Kompensaatioalueiden avulla määritetään työntekijän kompensaatio työpaikan sijainnin perusteella.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-150">Tarkistuspiste</span><span class="sxs-lookup"><span data-stu-id="1fbb2-150">Control point</span></span></td>
<td><span data-ttu-id="1fbb2-151">Tarkistuspiste määrittää, mikä on ihanteellisen palkkio kompensaatiotason kaikille työntekijöille.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="1fbb2-152">Palkkaluokkasuunnitelmien rakenteissa tarkistuspisteet ovat yleensä palkka-alueen keskikohdassa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="1fbb2-153">Kompensaatioluokkarakenteissa tarkistuspisteitä käytetään harvoin.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-153">Band structures rarely use control points.</span></span> <span data-ttu-id="1fbb2-154">Voit määrittää kiinteän kompensaatiosuunnitelman tarkistuspisteen Kiinteät kompensaatiosuunnitelmat -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-155">Työtehtävät</span><span class="sxs-lookup"><span data-stu-id="1fbb2-155">Job functions</span></span></td>
<td><span data-ttu-id="1fbb2-156">Työtehtävien avulla luokitellaan ja suodatetaan tiettyjen töiden kompensaatiosuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-157">Työtyypit</span><span class="sxs-lookup"><span data-stu-id="1fbb2-157">Job types</span></span></td>
<td><span data-ttu-id="1fbb2-158">Työtyyppien avulla luokitellaan ja suodatetaan tiettyjen töiden kompensaatiosuunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-159">Muuttuvan kompensaation tyypit</span><span class="sxs-lookup"><span data-stu-id="1fbb2-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="1fbb2-160">Muuttuvat kompensaatiotyypit, kuten osakepalkkiot ja käteispalkkiot, määritetään muuttuvissa kompensaatiosuunnitelmissa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-161">Kompensaatioruudukot</span><span class="sxs-lookup"><span data-stu-id="1fbb2-161">Compensation grids</span></span></td>
<td><span data-ttu-id="1fbb2-162">Kompensaatioruudukot sisältävät kompensaation rakenteen.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="1fbb2-163">Kompensaatioruudukoita voidaan käyttää yhdelle tai useammalle kompensaatiosuunnitelmalle.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1fbb2-164">Suorituskykysuunnitelmat</span><span class="sxs-lookup"><span data-stu-id="1fbb2-164">Performance plans</span></span></td>
<td><span data-ttu-id="1fbb2-165">Suorituskykysuunnitelmien avulla voidaan liittää suorituskyky kohdistusmatriisiin käytettäväksi suoritusperusteisessa palkkastrategiassa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fbb2-166">Suorituskykyluokitukset</span><span class="sxs-lookup"><span data-stu-id="1fbb2-166">Performance ratings</span></span></td>
<td><span data-ttu-id="1fbb2-167">Suorituskykyluokituksia käytetään suorituskykysuunnitelmissa määrittämään tulospalkkion tai suorituskykypalkkion summa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="1fbb2-168">Prosessitapahtumat</span><span class="sxs-lookup"><span data-stu-id="1fbb2-168">Process events</span></span>
<span data-ttu-id="1fbb2-169">Prosessitapahtuma laskee tietyn kauden kompensaatiotiedot kaikille työntekijöille, jotka on rekisteröity vähintään yhteen kiinteään tai muuttuvaan kompensaatiosuunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="1fbb2-170">Voit suorittaa prosessitapahtuman toistuvasti laskettujen kompensaatiotulosten testaamiseksi tai päivittämiseksi.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="1fbb2-171">Kompensaatiotapahtumat</span><span class="sxs-lookup"><span data-stu-id="1fbb2-171">Compensation events</span></span>
-------------------

<span data-ttu-id="1fbb2-172">Aina kun prosessitapahtuma suoritetaan, kompensaatiotapahtuma luodaan.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="1fbb2-173">Kompensaatiotapahtumat sisältävät kunkin työntekijän kyseiseen prosessitapahtumaan sisältyvän kompensaatioprosessin tulokset.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="1fbb2-174">Kun laskelmat ovat oikein, voit ladata kompensaatiotapahtuman päivittääksesi kompensaatiotietueet työntekijöille, joihin prosessitapahtuma vaikuttaa.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="1fbb2-175">Suositukset</span><span class="sxs-lookup"><span data-stu-id="1fbb2-175">Recommendations</span></span>
<span data-ttu-id="1fbb2-176">Voit suositella prosessitapahtuman suorittamisen jälkeen muutoksia työntekijän palkankorotus- tai palkkiosummaan prosessitapahtuman laskemien ohjeiden perusteella.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="1fbb2-177">Työntekijäsuositusten tekeminen edellyttää, että suositukset on otettu käyttöön, kun kompensaatiosuunnitelmat tai prosessitapahtuma määritettiin.</span><span class="sxs-lookup"><span data-stu-id="1fbb2-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]