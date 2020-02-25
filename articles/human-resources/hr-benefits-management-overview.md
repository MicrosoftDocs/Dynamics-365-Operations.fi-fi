---
title: Etujen hallinnan yleiskuvaus
description: Dynamics 365 Human Resourcesin etujen hallinnan esikatseluominaisuuden yleiskuvaus. Tarjoa työntekijöillesi laajennetut etuvaihtoehdot helppokäyttöisellä verkkokokemuksella.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029460"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="86c70-104">Etujen hallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="86c70-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="86c70-105">Pysyäksesi kilpailukykyisenä sinun on tarjottava laaja etuvalikoima. Näin houkuttelet parhaita työntekijöitä ja saat heidät pidettyä.</span><span class="sxs-lookup"><span data-stu-id="86c70-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="86c70-106">Vakioetujen, kuten terveyshuollon ja hammashoidon lisäksi, sinun kannattaa ehkä tarjota myös laajennettuja palveluja, kuten adoptioapua, virkistysohjelmia ja vaatetuslisiä.</span><span class="sxs-lookup"><span data-stu-id="86c70-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="86c70-107">Microsoft Dynamics 365 Human Resourcesin etujen hallinnan esikatseluominaisuus tarjoaa sinulle joustavan ratkaisun, joka tukee laajaa kirjoa etuvaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="86c70-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="86c70-108">Human Resources sisältää myös helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi.</span><span class="sxs-lookup"><span data-stu-id="86c70-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="86c70-109">Parannettujen etuussuunnitelmien avulla voit luoda ja hallita yksilöllisiä etuussuunnitelmia ja tukea monimutkaisia etujen hinnastoja ja sisäkkäisiä tasoja.</span><span class="sxs-lookup"><span data-stu-id="86c70-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="86c70-110">Voit helposti luoda etuusohjelmia ja -nippuja sekä automaattisen rekisteröinnin sääntöjä, jotka helpottavat työntekijöiden kokemusta.</span><span class="sxs-lookup"><span data-stu-id="86c70-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="86c70-111">Joustoluotto-ohjelmien avulla voit käyttää suhteellista laskentaa eläköitymisen ja muiden elämäntapahtumien tukemiseen.</span><span class="sxs-lookup"><span data-stu-id="86c70-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="86c70-112">Laajat kelpoisuussäännöt varmistavat, että annat oikeat edut oikeiden työntekijöiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="86c70-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="86c70-113">Verkkorekisteröinti etuja varten tarjoaa työntekijöillesi helpon kokemuksen.</span><span class="sxs-lookup"><span data-stu-id="86c70-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="86c70-114">Kelpoisten elämäntapahtumien käsittely integroituu työntekijöiden itsepalveluun ja tukee myös tulevia elämäntapahtumia.</span><span class="sxs-lookup"><span data-stu-id="86c70-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="86c70-115">Jos haluat käyttää demotietoja, sinun on otettava eristysympäristösi uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="86c70-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="86c70-116">Voit antaa suoraa palautetta tai ilmoittaa ongelmista osoitteeseen D365BenefitsPreview@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="86c70-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="86c70-117">Etujen hallinnan tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="86c70-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="86c70-118">Kelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-118">Eligibility processing</span></span>

<span data-ttu-id="86c70-119">Käsiteltäessä kelpoisuutta sellaisten etujen osalta, joissa käytetään arvoja 1–5 kertaa palkka, prosenttiosuutta pakasta ja kiinteä kattavuusmäärä, sinun on määritettävä **Edun tiedot** ja **Työntekijän aloituspäivä** **Työsuhdehistoria**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="86c70-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="86c70-120">Sinun on myös sisällytettävä arvot **Työtunnit**, **Maksuväli** ja **Vuosittaisten etujen palkkasumma**.</span><span class="sxs-lookup"><span data-stu-id="86c70-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="86c70-121">Jos työntekijällä on kiinteä kompensaatio, määritä **Työtunnit** ja **Maksuväli**.</span><span class="sxs-lookup"><span data-stu-id="86c70-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="86c70-122">Vuosittainen palkkamäärä lasketaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="86c70-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="86c70-123">Jos työntekijä on palkallinen, arvoa **Työtunnit** ei tarvita.</span><span class="sxs-lookup"><span data-stu-id="86c70-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="86c70-124">Suosittelemme uusia työntekijöitä luotaessa ensin kiinteän kompensaation syöttämistä.</span><span class="sxs-lookup"><span data-stu-id="86c70-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="86c70-125">Voit päivittää etutietojen tietuetta kohdassa **Työntekijä > Työntekijän historia > Työsuhteen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="86c70-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="86c70-126">Muuta päivämääräksi työntekijän aloituspäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="86c70-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="86c70-127">Työntekijän itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="86c70-127">Employee self-service</span></span>

<span data-ttu-id="86c70-128">Työntekijän summaa ei lasketa, kun henkivakuutuksen kattavuutta päivitetään.</span><span class="sxs-lookup"><span data-stu-id="86c70-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="86c70-129">Jos työntekijälle esimerkiksi tarjotaan henkivakuutussuunnitelmaa, hän voi valita enintään 50 000 dollarin kattavuuden hintaan 0,36 dollaria per 1 000 dollaria kattavuutta.</span><span class="sxs-lookup"><span data-stu-id="86c70-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="86c70-130">Kun työntekijä päivittää kattavuusmäärän, työntekijän siihen liittyvät kulut pysyvät nollana.</span><span class="sxs-lookup"><span data-stu-id="86c70-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="86c70-131">Jos kyseessä on etuussuunnitelma, jossa kyseisen suunnitelmatyypin voi valita vain kerran, käyttäjä saa virheilmoituksen, jos hän yrittää luopua suunnitelmasta sellaisen valittuaan.</span><span class="sxs-lookup"><span data-stu-id="86c70-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="86c70-132">Esimerkki: Käyttäjä valitsee terveydenhuoltosuunnitelman ja lisää sen ostoskoriin.</span><span class="sxs-lookup"><span data-stu-id="86c70-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="86c70-133">Sen jälkeen hän valitsee **Luovu** saadakseen toisen terveydenhuoltosuunnitelman.</span><span class="sxs-lookup"><span data-stu-id="86c70-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="86c70-134">Käyttäjä saa virheilmoituksen.</span><span class="sxs-lookup"><span data-stu-id="86c70-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="86c70-135">Etujen hallinnan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="86c70-135">Enable Benefits management</span></span>

<span data-ttu-id="86c70-136">Etujen hallinta on esikatseluominaisuus, ja se on käytettävissä vain **Sandbox**-ympäristöissä.</span><span class="sxs-lookup"><span data-stu-id="86c70-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="86c70-137">Näissä artikkeleissa esitellään, miten esikatseluominaisuudet otetaan käyttöön Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="86c70-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="86c70-138">Niissä kerrotaan myös, mitkä Human Resourcesin olemassa olevat ominaisuudet etujen hallinta korvaa ja mitkä ominaisuudet poistetaan käytöstä, kun etujen hallinta otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="86c70-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="86c70-139">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="86c70-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="86c70-140">Esikatseluominaisuus: Etujen hallinta</span><span class="sxs-lookup"><span data-stu-id="86c70-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="86c70-141">Etujen hallinnan määritys</span><span class="sxs-lookup"><span data-stu-id="86c70-141">Configure Benefits management</span></span>

<span data-ttu-id="86c70-142">Ennen kuin voit luoda työn tekijöille etuussuunnitelmia, sinun on määritettävä suunnitelmille asetuksia.</span><span class="sxs-lookup"><span data-stu-id="86c70-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="86c70-143">Aseta etujenhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="86c70-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="86c70-144">Oikeutussääntöjen ja -asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="86c70-145">Henkilökohtaisen yhteyshenkilön kelpoisuusasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="86c70-146">Kattavuusasetusten luominen</span><span class="sxs-lookup"><span data-stu-id="86c70-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="86c70-147">Määritä maksun toistuvuus</span><span class="sxs-lookup"><span data-stu-id="86c70-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="86c70-148">Elämäntapahtumatyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="86c70-149">Suunnitelmatyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="86c70-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="86c70-150">Määritä syykoodit</span><span class="sxs-lookup"><span data-stu-id="86c70-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="86c70-151">Tasokoodien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="86c70-152">Hintojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="86c70-153">Vähennysten määritys</span><span class="sxs-lookup"><span data-stu-id="86c70-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="86c70-154">Odotuspäivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="86c70-155">Odotuskausien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="86c70-156">Pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="86c70-157">Luo työsuhdeluokat</span><span class="sxs-lookup"><span data-stu-id="86c70-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="86c70-158">Määritä työsuhteen tyypit</span><span class="sxs-lookup"><span data-stu-id="86c70-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="86c70-159">Määritä työntekijän itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="86c70-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="86c70-160">Etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="86c70-160">Create benefit plans</span></span>

<span data-ttu-id="86c70-161">Näissä artikkeleissa esitellään, miten etuussuunnitelmia, niput ja joustoluotto-ohjelmat mukaan luettuna, luodaan.</span><span class="sxs-lookup"><span data-stu-id="86c70-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="86c70-162">Etuussuunnitelmien määritys</span><span class="sxs-lookup"><span data-stu-id="86c70-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="86c70-163">Työntekijöiden etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="86c70-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="86c70-164">Joustoluotto-ohjelmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="86c70-165">Tulevien elämäntapahtumien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="86c70-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="86c70-166">Etuussuunnitelmien käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-166">Process benefit plans</span></span>

<span data-ttu-id="86c70-167">Sinun on käsiteltävä joitakin muutoksia, jotta ne olisivat aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="86c70-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="86c70-168">Rekisteröintikelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="86c70-169">Elämäntapahtumien käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="86c70-170">Elämäntapahtumien muutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="86c70-171">Elämäntapahtumien kelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="86c70-172">Maksumuutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="86c70-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

