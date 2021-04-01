---
title: Työajan seurannan poissaolojen rekisteröinti
description: Tässä ohjeaiheessa kerrotaan, miten poissaolojen rekisteröintejä käsitellään työajan seurannassa.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 961b87fb066018f9f6ecc3dcc3cc88e64574bb64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246546"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="2abae-103">Työajan seurannan poissaolojen rekisteröinti</span><span class="sxs-lookup"><span data-stu-id="2abae-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2abae-104">Tässä ohjeaiheessa esitellään poissaoloihin liittyvät käsitteet ja kerrotaan, miten poissaoloja käsitellään työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="2abae-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="2abae-105">Normaaleihin työtunteihin perustuva poissaolo</span><span class="sxs-lookup"><span data-stu-id="2abae-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="2abae-106">Kun työntekijät eivät työskentele normaalien työtuntien aikana, heille kirjataan poissaolo.</span><span class="sxs-lookup"><span data-stu-id="2abae-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="2abae-107">Normaalit työtunnit määritetään työntekijän normaalin työajan profiilissa.</span><span class="sxs-lookup"><span data-stu-id="2abae-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="2abae-108">Tässä esimerkissä työntekijä työskentelee sellaisen päiväprofiilin mukaan, jossa sisäänleimaus tehdään kello 7.00 ja ulosleimaus kello 15.00.</span><span class="sxs-lookup"><span data-stu-id="2abae-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="2abae-109">Jos työntekijä leimaa itsensä sisään kello 9.00, hänelle kirjataan kyseiseltä päivältä poissaolo ajalta 7.00–9.00.</span><span class="sxs-lookup"><span data-stu-id="2abae-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="2abae-110">Tässä tapauksessa työntekijöitä pyydetään antamaan poissaolon syy.</span><span class="sxs-lookup"><span data-stu-id="2abae-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="2abae-111">He voivat määrittää syyn valitsemalla poissaolokoodin.</span><span class="sxs-lookup"><span data-stu-id="2abae-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="2abae-112">Poissaolokoodit</span><span class="sxs-lookup"><span data-stu-id="2abae-112">Absence codes</span></span>

<span data-ttu-id="2abae-113">Poissaolokoodit määrittävät erilaiset poissaolon tyypit.</span><span class="sxs-lookup"><span data-stu-id="2abae-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="2abae-114">Yritys määrittää poissaolokoodit.</span><span class="sxs-lookup"><span data-stu-id="2abae-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="2abae-115">Poissaolokoodeihin voi kohdistaa erilaisia sääntöjä.</span><span class="sxs-lookup"><span data-stu-id="2abae-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="2abae-116">Poissaolokoodi voidaan määrittää esimerkiksi maksun palkan pienentämistä tai myöntämistä varten.</span><span class="sxs-lookup"><span data-stu-id="2abae-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="2abae-117">Tässä esimerkissä yritys määrittää **Myöhässä**-poissaolokoodin, jota työntekijät käyttävät saapuessaan töihin myöhässä ilman hyvää syytä.</span><span class="sxs-lookup"><span data-stu-id="2abae-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="2abae-118">Yritys määrittää myös **Sisäinen kurssi** -poissaolokoodin, jota työntekijät käyttävät osallistuessaan sisäisille kursseille.</span><span class="sxs-lookup"><span data-stu-id="2abae-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="2abae-119">Nämä poissaolokoodit voidaan määrittää niin, että **Myöhässä**-koodi pienentää työntekijän palkkaa, mutta **Sisäinen kurssi** -koodi ei.</span><span class="sxs-lookup"><span data-stu-id="2abae-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="2abae-120">Voit määrittää automaattisia poissaolokoodeja.</span><span class="sxs-lookup"><span data-stu-id="2abae-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="2abae-121">Näitä poissaolokoodeja voi käyttää työntekijän työajan laskemisessa, kun poissaoloa ei ole rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="2abae-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="2abae-122">Työntekijän aikaprofiili määrittää, käytetäänkö normaalin työajan tai liukuma-ajan poissaolokoodia.</span><span class="sxs-lookup"><span data-stu-id="2abae-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="2abae-123">Normaalin työajan ja liukuma-ajan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2abae-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="2abae-124">Määritä normaalin työajan ja liukuma-ajan parametrit käyttämällä **Automaattinen poissaolon lisäys**- ja **Automaattinen liukuvan työajan lisäys** -vaihtoehtoa **Työajan seurannan parametrit** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2abae-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="2abae-125">Poissaoloryhmät</span><span class="sxs-lookup"><span data-stu-id="2abae-125">Absence groups</span></span>

<span data-ttu-id="2abae-126">Poissaolokoodit ryhmitellään poissaoloryhmiksi.</span><span class="sxs-lookup"><span data-stu-id="2abae-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="2abae-127">Poissaoloryhmien avulla ryhmitellään poissaolokoodit, joilla on yhteisiä ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="2abae-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="2abae-128">Esimerkkejä ovat poissaolokoodit, joiden syy on luvallinen poissaolo tai esimerkiksi lääkärikäynti, valamiespalvelu tai sairas lapsi.</span><span class="sxs-lookup"><span data-stu-id="2abae-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="2abae-129">Suunniteltu poissaolo</span><span class="sxs-lookup"><span data-stu-id="2abae-129">Planned absence</span></span>

<span data-ttu-id="2abae-130">Jos tiedetään, että työntekijä on poissa tietyn ajan, kuten esimerkiksi tulevan loman ajan, voidaan käyttää suunniteltua poissaoloa.</span><span class="sxs-lookup"><span data-stu-id="2abae-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="2abae-131">Suunniteltu poissaolo määritetään poissaolokoodien avulla niin, että koodit ottavat huomioon suunnitellun poissaolon.</span><span class="sxs-lookup"><span data-stu-id="2abae-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="2abae-132">Kun määrität suunnitellun poissaolon, sinulta ei pyydetä poissaolokoodia poissaolojakson aikana aikarekisteröintien laskemisen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="2abae-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="2abae-133">Suunniteltu poissaolo voidaan määrittää yksittäiselle työntekijälle. Työntekijöiden suunnitellun poissaolon joukkopäivitystä varten voidaan myös määrittää erätyö.</span><span class="sxs-lookup"><span data-stu-id="2abae-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="2abae-134">Suunnitellun poissaolon määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2abae-134">Set up planned absence</span></span>

1. <span data-ttu-id="2abae-135">Valitse **Henkilöstöhallinto** &gt; **Työntekijät** &gt; **Työntekijät** ja valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="2abae-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="2abae-136">Valitse **Aika** &gt; **Aikamääritykset** &gt; **Ajan poissaolomerkintä** ja määritä suunniteltu poissaolo.</span><span class="sxs-lookup"><span data-stu-id="2abae-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="2abae-137">Keskeytetty suunniteltu poissaolo</span><span class="sxs-lookup"><span data-stu-id="2abae-137">Interrupted planned absence</span></span>

<span data-ttu-id="2abae-138">Jos käytät **Keskeytys**-vaihtoehtoa suunnitellun poissaolon määrityksen yhteydessä, suunniteltu poissaolo keskeytetään, jos työntekijä kirjautuu sisään suunnitellun poissaolojakson aikana.</span><span class="sxs-lookup"><span data-stu-id="2abae-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="2abae-139">Suunniteltu poissaolo merkitään **keskeytetyksi**. Poissaolo ei vaikuta tuleviin laskelmiin.</span><span class="sxs-lookup"><span data-stu-id="2abae-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="2abae-140">Suunnitellun poissaolon määrittäminen keskeytystä varten</span><span class="sxs-lookup"><span data-stu-id="2abae-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="2abae-141">Avaa **Ajan poissaolomerkintä** -sivu suunnitellun poissaolon määrittämisen yhteydessä kerrotulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="2abae-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="2abae-142">Valitse **Keskeytä**.</span><span class="sxs-lookup"><span data-stu-id="2abae-142">Select **Interrupt**.</span></span>

<span data-ttu-id="2abae-143">**Keskeytä**-vaihtoehtoa käytetään, kun aika rekisteröidään työnohjauksen päätteessä tai laitteessa.</span><span class="sxs-lookup"><span data-stu-id="2abae-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="2abae-144">Vaihtoehtoa ei käytetä, jos rekisteröinnit syötetään laskenta- ja hyväksyntäsivuilla tai **Sähköinen kellokortti** -sivulla.</span><span class="sxs-lookup"><span data-stu-id="2abae-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="2abae-145">Esimerkkejä poissaolon käyttämisestä liukumaprofiilissa</span><span class="sxs-lookup"><span data-stu-id="2abae-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="2abae-146">Seuraavat kolme esimerkkiä näyttävät, miten poissaolo lasketaan profiilille, jolle on määritetty liukuvat jaksot.</span><span class="sxs-lookup"><span data-stu-id="2abae-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="2abae-147">Esimerkeissä käytetään seuraavaa profiilia.</span><span class="sxs-lookup"><span data-stu-id="2abae-147">The examples use the following profile.</span></span>

| <span data-ttu-id="2abae-148">Saapuminen</span><span class="sxs-lookup"><span data-stu-id="2abae-148">Clock-in</span></span> | <span data-ttu-id="2abae-149">Vakioaika</span><span class="sxs-lookup"><span data-stu-id="2abae-149">Standard time</span></span>    | <span data-ttu-id="2abae-150">Tauko</span><span class="sxs-lookup"><span data-stu-id="2abae-150">Break</span></span>             | <span data-ttu-id="2abae-151">Vakioaika</span><span class="sxs-lookup"><span data-stu-id="2abae-151">Standard time</span></span> | <span data-ttu-id="2abae-152">Vaje-</span><span class="sxs-lookup"><span data-stu-id="2abae-152">Flex-</span></span>        | <span data-ttu-id="2abae-153">Poistuminen</span><span class="sxs-lookup"><span data-stu-id="2abae-153">Clock-out</span></span> | <span data-ttu-id="2abae-154">Ylijäämä</span><span class="sxs-lookup"><span data-stu-id="2abae-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="2abae-155">8.00</span><span class="sxs-lookup"><span data-stu-id="2abae-155">8 AM</span></span>     | <span data-ttu-id="2abae-156">9.00–11.30</span><span class="sxs-lookup"><span data-stu-id="2abae-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="2abae-157">11.30–12.00</span><span class="sxs-lookup"><span data-stu-id="2abae-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="2abae-158">12.00–15.00</span><span class="sxs-lookup"><span data-stu-id="2abae-158">12 PM to 3 PM</span></span> | <span data-ttu-id="2abae-159">15.00–16.00</span><span class="sxs-lookup"><span data-stu-id="2abae-159">3 PM to 4 PM</span></span> | <span data-ttu-id="2abae-160">16.00</span><span class="sxs-lookup"><span data-stu-id="2abae-160">4 PM</span></span>      | <span data-ttu-id="2abae-161">16.00–18.00</span><span class="sxs-lookup"><span data-stu-id="2abae-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="2abae-162">Esimerkki 1: Kirjautuminen ulos liukuman vähennysjakson aikana</span><span class="sxs-lookup"><span data-stu-id="2abae-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="2abae-163">Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 15.30.</span><span class="sxs-lookup"><span data-stu-id="2abae-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="2abae-164">Koska työntekijä leimaa itsensä ulos liukuman vähennysjakson aikana, poissaoloa ei kirjata, vaan työntekijän liukumasaldosta vähennetään puoli tuntia.</span><span class="sxs-lookup"><span data-stu-id="2abae-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="2abae-165">Esimerkki 2: Kirjautuminen ulos normaalin työjakson aikana</span><span class="sxs-lookup"><span data-stu-id="2abae-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="2abae-166">Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 14.30.</span><span class="sxs-lookup"><span data-stu-id="2abae-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="2abae-167">Koska työntekijä leimaa itsensä ulos normaalin työjakson aikana, poissaoloksi lasketaan kello 14.30–16.00 välinen aika. Rekisteröity poissaolojakso on 1,5 tuntia.</span><span class="sxs-lookup"><span data-stu-id="2abae-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="2abae-168">Jakson poissaolokoodi on annettava.</span><span class="sxs-lookup"><span data-stu-id="2abae-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="2abae-169">Esimerkki 3: Kirjautuminen ulos liukuman lisäysjakson aikana</span><span class="sxs-lookup"><span data-stu-id="2abae-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="2abae-170">Työntekijä leimaa itsensä sisään kello 8.00 ja ulos kello 16.30.</span><span class="sxs-lookup"><span data-stu-id="2abae-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="2abae-171">Koska työntekijä leimaa itsensä ulos liukuman lisäysjakson aikana, poissaoloa ei kirjata, vaan työntekijän liukumasaldoon lisätään puoli tuntia.</span><span class="sxs-lookup"><span data-stu-id="2abae-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="2abae-172">Poissaolo laskennassa ja hyväksyntäprosessi</span><span class="sxs-lookup"><span data-stu-id="2abae-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="2abae-173">Työntekijän aikarekisteröinnit on laskettava ja hyväksyttävä, ennen kuin ne voidaan siirtää palkanlaskentajärjestelmän maksukohteiksi.</span><span class="sxs-lookup"><span data-stu-id="2abae-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="2abae-174">Hyväksyjä voi muuttaa työntekijän aikarekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="2abae-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="2abae-175">Hyväksyjä voi muuttaa jopa mitä tahansa työntekijän rekisteröimää poissaoloa.</span><span class="sxs-lookup"><span data-stu-id="2abae-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="2abae-176">Jos hyväksyjä syöttää poissaolokoodin sisältävän ajanjakson manuaalisesti, työajan seurannan parametrien oletuspoissaolokoodi ei korvaa kyseisen jakson poissaolokoodia.</span><span class="sxs-lookup"><span data-stu-id="2abae-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="2abae-177">Tässä esimerkissä työntekijä leimaa itsensä sisään kello 10.00 ja valitsee myöhästymisen osoittavan poissaolokoodin.</span><span class="sxs-lookup"><span data-stu-id="2abae-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="2abae-178">Myöhemmin työntekijä ilmoittaa esimiehelle, että hänellä oli aika lääkärille kello 8.00–10.00.</span><span class="sxs-lookup"><span data-stu-id="2abae-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="2abae-179">Lääkärissäkäynti ei aiheuta vähennystä työntekijän palkasta.</span><span class="sxs-lookup"><span data-stu-id="2abae-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="2abae-180">Tämän vuoksi esimies voi tässä tapauksessa korjata kello 8.00 ja 10.00 väliset kaksi tuntia manuaalisesti syöttämällä poissaolokoodin, joka osoittaa näiden kahden tunnin poissaolon syyksi sairauden.</span><span class="sxs-lookup"><span data-stu-id="2abae-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="2abae-181">Poissaolon laskeminen ja hyväksyminen</span><span class="sxs-lookup"><span data-stu-id="2abae-181">Calculate and approve absence</span></span>

- <span data-ttu-id="2abae-182">Valitse **Työajan seuranta** &gt; **Tarkista ja hyväksy** &gt; **Hyväksy tai laske**.</span><span class="sxs-lookup"><span data-stu-id="2abae-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]