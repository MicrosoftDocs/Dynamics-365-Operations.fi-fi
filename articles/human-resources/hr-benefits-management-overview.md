---
title: Etujen hallinnan yleiskatsaus
description: Dynamics 365 Human Resourcesin etujen hallintaominaisuuden yleiskuvaus. Tarjoa työntekijöillesi laajennetut etuvaihtoehdot helppokäyttöisellä verkkokokemuksella.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: 91a4425b4f020f90843bb3b0b280b7ee28463670
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230151"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="46097-104">Etujen hallinnan yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="46097-104">Benefits management overview</span></span>

<span data-ttu-id="46097-105">Pysyäksesi kilpailukykyisenä sinun on tarjottava laaja etuvalikoima. Näin houkuttelet parhaita työntekijöitä ja saat heidät pidettyä.</span><span class="sxs-lookup"><span data-stu-id="46097-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="46097-106">Vakioetujen, kuten terveyshuollon ja hammashoidon lisäksi, sinun kannattaa ehkä tarjota myös laajennettuja palveluja, kuten adoptioapua, virkistysohjelmia ja vaatetuslisiä.</span><span class="sxs-lookup"><span data-stu-id="46097-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="46097-107">Microsoft Dynamics 365 Human Resourcesin etujen hallinta tarjoaa sinulle joustavan ratkaisun, joka tukee laajaa kirjoa etuvaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="46097-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="46097-108">Human Resources sisältää myös helppokäyttöisen työntekijäkokemuksen, joka esittelee valikoimasi.</span><span class="sxs-lookup"><span data-stu-id="46097-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="46097-109">Parannettujen etuussuunnitelmien avulla voit luoda ja hallita yksilöllisiä etuussuunnitelmia ja tukea monimutkaisia etujen hinnastoja ja sisäkkäisiä tasoja.</span><span class="sxs-lookup"><span data-stu-id="46097-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="46097-110">Voit helposti luoda etuusohjelmia ja -nippuja sekä automaattisen rekisteröinnin sääntöjä, jotka helpottavat työntekijöiden kokemusta.</span><span class="sxs-lookup"><span data-stu-id="46097-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="46097-111">Joustoluotto-ohjelmien avulla voit käyttää suhteellista laskentaa eläköitymisen ja muiden elämäntapahtumien tukemiseen.</span><span class="sxs-lookup"><span data-stu-id="46097-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="46097-112">Laajat kelpoisuussäännöt varmistavat, että annat oikeat edut oikeiden työntekijöiden käyttöön.</span><span class="sxs-lookup"><span data-stu-id="46097-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="46097-113">Verkkorekisteröinti etuja varten tarjoaa työntekijöillesi helpon kokemuksen.</span><span class="sxs-lookup"><span data-stu-id="46097-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="46097-114">Pätevän elämäntapahtuman käsittely tukee tulevia elämäntapahtumia.</span><span class="sxs-lookup"><span data-stu-id="46097-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="46097-115">Jos haluat käyttää demotietoja, sinun on otettava eristysympäristösi uudelleen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="46097-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="46097-116">Etujen hallinnan tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="46097-116">Benefits management known issues</span></span>

### <a name="flex-credit-programs"></a><span data-ttu-id="46097-117">Bonushyvitysohjelmat</span><span class="sxs-lookup"><span data-stu-id="46097-117">Flex credit programs</span></span>

<span data-ttu-id="46097-118">Joustoluotto-ohjelmalle määritetty kokonaisluottoarvo ei näy **Työntekijän etujen suunnitelmat** -lomakkeessa.</span><span class="sxs-lookup"><span data-stu-id="46097-118">The total credit value defined for a flex credit program doesn't display in the **Worker benefit plans** form.</span></span> <span data-ttu-id="46097-119">Jos määrität joustoluotto-ohjelman arvoksi **Ei mitään**, saat virheilmoituksen **Työntekijän etuussuunnitelma** -lomakkeesta, kun valitset ja vahvistat suunnitelmat.</span><span class="sxs-lookup"><span data-stu-id="46097-119">Also, if you set a flex credit program to have a proration rule of **None**, you get an error in the **Worker benefit plan** form when selecting and confirming plans.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="46097-120">Etujen hallinnan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="46097-120">Enable Benefits management</span></span>

<span data-ttu-id="46097-121">Tässä artikkeleissa esitellään, miten ominaisuudet otetaan käyttöön Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="46097-121">This article describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="46097-122">Siinä kerrotaan myös, mitkä Human Resourcesin olemassa olevat ominaisuudet etujen hallinta korvaa ja mitkä ominaisuudet poistetaan käytöstä, kun etujen hallinta otetaan käyttöön.</span><span class="sxs-lookup"><span data-stu-id="46097-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46097-123">Kun etujenhallinta on otettu käyttöön **Tuotanto**-ympäristössä, sitä ei voi poistaa käytöstä.</span><span class="sxs-lookup"><span data-stu-id="46097-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="46097-124">On suositeltavaa ottaa käyttöön ja testata etujenhallinta **Eristys**-ympäristössä, ennen kuin otat sen käyttöön **Tuotanto** -ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="46097-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="46097-125">Vanhojen etutoimintojen ja uusien etujen hallintatoimintojen välillä on huomattavia eroja, jotka edellyttävät lisäasetuksia ja jotka on testattava ennen niiden asettamista tuotantoon.</span><span class="sxs-lookup"><span data-stu-id="46097-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="46097-126">Hallitse ominaisuuksia</span><span class="sxs-lookup"><span data-stu-id="46097-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="46097-127">Työntekijätietojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-127">Configure employee information</span></span>

<span data-ttu-id="46097-128">Ennen kuin voit rekisteröidä työntekijöitä etuuksiin, sinun on annettava tarvittavat tiedot.</span><span class="sxs-lookup"><span data-stu-id="46097-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="46097-129">Työntekijä on rekisteröitävä **Kiinteässä kompensaatiosuunnitelmassa** aloituspäivämääränä, ja **Työntekijä**-lomakkeen **Työsuhteen tiedot** on valittava **Etuuden maksutiheydestä**.</span><span class="sxs-lookup"><span data-stu-id="46097-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="46097-130">Kun luot etuussuunnitelman, joka käyttää sukupuoleen tai ikään perustuvia kursseja, sinun on syötettävä työntekijän syntymäpäivämäärä ja sukupuoli, jotta voit laskea etuuskustannuksen.</span><span class="sxs-lookup"><span data-stu-id="46097-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="46097-131">Etujen hallinnan määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-131">Configure Benefits management</span></span>

<span data-ttu-id="46097-132">Ennen kuin voit luoda työn tekijöille etuussuunnitelmia, sinun on määritettävä suunnitelmille asetuksia.</span><span class="sxs-lookup"><span data-stu-id="46097-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="46097-133">Aseta etujenhallinnan parametrit</span><span class="sxs-lookup"><span data-stu-id="46097-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="46097-134">Oikeutussääntöjen ja -asetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="46097-135">Henkilökohtaisten yhteyshenkilöiden oikeutusasetusten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="46097-136">Kattavuusasetusten luominen</span><span class="sxs-lookup"><span data-stu-id="46097-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="46097-137">Maksutiheyksien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="46097-138">Elämäntapahtumatyyppien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="46097-139">Suunnitelmantyyppien luominen</span><span class="sxs-lookup"><span data-stu-id="46097-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="46097-140">Määritä syykoodit</span><span class="sxs-lookup"><span data-stu-id="46097-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="46097-141">Määritä tasokoodit</span><span class="sxs-lookup"><span data-stu-id="46097-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="46097-142">Hintojen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="46097-143">Vähennysten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="46097-144">Odotuspäivien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="46097-145">Odotuskausien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="46097-146">Pyöristyssääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="46097-147">Työsuhdeluokkien luominen</span><span class="sxs-lookup"><span data-stu-id="46097-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="46097-148">Määritä työsuhteen tyypit</span><span class="sxs-lookup"><span data-stu-id="46097-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="46097-149">Määritä työntekijän itsepalvelu</span><span class="sxs-lookup"><span data-stu-id="46097-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="46097-150">Etuussuunnitelmien luominen</span><span class="sxs-lookup"><span data-stu-id="46097-150">Create benefit plans</span></span>

<span data-ttu-id="46097-151">Näissä artikkeleissa esitellään, miten etuussuunnitelmia, niput ja joustoluotto-ohjelmat mukaan luettuna, luodaan.</span><span class="sxs-lookup"><span data-stu-id="46097-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="46097-152">Etusuunnitelmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="46097-153">Liukumahyvitysohjelmien määrittäminen</span><span class="sxs-lookup"><span data-stu-id="46097-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="46097-154">Etusuunnitelmien käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-154">Process benefit plans</span></span>

<span data-ttu-id="46097-155">Sinun on käsiteltävä joitakin muutoksia, jotta ne olisivat aktiivisia.</span><span class="sxs-lookup"><span data-stu-id="46097-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="46097-156">Rekisteröintikelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="46097-157">Elämäntapahtumien käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="46097-158">Elämäntapahtumien muutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="46097-159">Elämäntapahtumien kelpoisuuden käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="46097-160">Maksumuutosten käsittely</span><span class="sxs-lookup"><span data-stu-id="46097-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

