---
title: Kattavuusasetusten luominen
description: Microsoft Dynamics 365 Human Resources -ohjelman kattavuustasot osallistujan valitsemiselle etuussuunnitelmassa tai -ohjelmassa.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8690dbe00c2316ccf745f5222c3cbaa9c3379f85
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418374"
---
# <a name="create-coverage-options"></a><span data-ttu-id="41ad0-103">Kattavuusasetusten luominen</span><span class="sxs-lookup"><span data-stu-id="41ad0-103">Create coverage options</span></span>

<span data-ttu-id="41ad0-104">Microsoft Dynamics 365 Human Resources -ohjelman kattavuustasot osallistujan valitsemiselle etuussuunnitelmassa tai -ohjelmassa.</span><span class="sxs-lookup"><span data-stu-id="41ad0-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="41ad0-105">Kattavuusvaihtoehdot voivat olla esimerkiksi **Vain työntekijä** lääketieteellisessä suunnitelmassa tai **2 x palkka** henkivakuutussuunnitelmaa varten.</span><span class="sxs-lookup"><span data-stu-id="41ad0-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="41ad0-106">Voit käyttää kattavuusasetuksia uudelleen hyödyksi, kun ne on määritetty.</span><span class="sxs-lookup"><span data-stu-id="41ad0-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="41ad0-107">Voit liittää vaihtoehdon yhteen tai useaan suunnitelmaan.</span><span class="sxs-lookup"><span data-stu-id="41ad0-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="41ad0-108">Kun kattavuusasetukset on määritetty, liitä kattavuusasetukset etuussuunnitelmatyyppiin.</span><span class="sxs-lookup"><span data-stu-id="41ad0-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="41ad0-109">Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="41ad0-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="41ad0-110">Suunnitelmatyyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa suunnitelmissa, jotka luodaan kyseisellä suunnitelmatyypillä.</span><span class="sxs-lookup"><span data-stu-id="41ad0-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="41ad0-111">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Kattavuusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="41ad0-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="41ad0-112">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="41ad0-112">Select **New**.</span></span>

3. <span data-ttu-id="41ad0-113">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="41ad0-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="41ad0-114">Kenttä</span><span class="sxs-lookup"><span data-stu-id="41ad0-114">Field</span></span> | <span data-ttu-id="41ad0-115">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="41ad0-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41ad0-116">**Kattavuusasetus**</span><span class="sxs-lookup"><span data-stu-id="41ad0-116">**Coverage option**</span></span> | <span data-ttu-id="41ad0-117">Yksilöllinen kattavuusasetuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="41ad0-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="41ad0-118">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="41ad0-118">**Description**</span></span> | <span data-ttu-id="41ad0-119">Kattavuusasetuksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="41ad0-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="41ad0-120">**Kattavuuskoodi**</span><span class="sxs-lookup"><span data-stu-id="41ad0-120">**Coverage code**</span></span> | <span data-ttu-id="41ad0-121">Kattavuuskoodit määrittävät kullekin kelvolliselle katetulle henkilötyypille enimmäis- ja vähimmäismäärät.</span><span class="sxs-lookup"><span data-stu-id="41ad0-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="41ad0-122">Kattavuuskoodi ilmaisee, kenet katetaan tai suunnitelmatyypille sallitun kattavuusmäärän.</span><span class="sxs-lookup"><span data-stu-id="41ad0-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="41ad0-123">Voit ilmaista kattavuusmäärän dollarisummana tai prosenttiosuutenta.</span><span class="sxs-lookup"><span data-stu-id="41ad0-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="41ad0-124">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="41ad0-124">For example:</span></span></br></br><span data-ttu-id="41ad0-125">- **Työnt+1** – Täyttääkseen kelpoisuusvaatimuksen työntekijällä on oltava valittuna yksi huollettava (tämän määrän ylittävät huollettavat eivät enää kuulu suunnitelman piitiin).</span><span class="sxs-lookup"><span data-stu-id="41ad0-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="41ad0-126">- **Työnt+perhe** – Täyttääkseen kelpoisuusvaatimukset työntekijällä on oltava valittuna vähintään kaksi huollettavaa.</span><span class="sxs-lookup"><span data-stu-id="41ad0-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="41ad0-127">**Enimmäismäärä**</span><span class="sxs-lookup"><span data-stu-id="41ad0-127">**Maximum number**</span></span> | <span data-ttu-id="41ad0-128">Huollettavien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="41ad0-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="41ad0-129">**Tila**</span><span class="sxs-lookup"><span data-stu-id="41ad0-129">**Status**</span></span> | <span data-ttu-id="41ad0-130">Kattavuusasetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="41ad0-130">The status of the coverage option.</span></span> <span data-ttu-id="41ad0-131">Jos kattavuusasetuksen tilaksi asetetaan Passiivinen, kyseistä kattavuusasetusta ei voida valita suunnitelmatyypeissä.</span><span class="sxs-lookup"><span data-stu-id="41ad0-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="41ad0-132">**Prosenttia**</span><span class="sxs-lookup"><span data-stu-id="41ad0-132">**Percent**</span></span> | <span data-ttu-id="41ad0-133">Prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="41ad0-133">The percent amount.</span></span> <span data-ttu-id="41ad0-134">Tämä kenttä on aktiivinen vain, jos kattavuuskoodikentässä on valittu % x palkka.</span><span class="sxs-lookup"><span data-stu-id="41ad0-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="41ad0-135">**Jakaja**</span><span class="sxs-lookup"><span data-stu-id="41ad0-135">**Divisor**</span></span> | <span data-ttu-id="41ad0-136">Laskennassa käytettävä jalkaja, kun valitaan kattavuuskoodi % x palkka.</span><span class="sxs-lookup"><span data-stu-id="41ad0-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="41ad0-137">**Vähimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="41ad0-137">**Percent minimum**</span></span> | <span data-ttu-id="41ad0-138">Vähimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="41ad0-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="41ad0-139">**Enimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="41ad0-139">**Percent maximum**</span></span> | <span data-ttu-id="41ad0-140">Enimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="41ad0-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="41ad0-141">Liitä kohtaan **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** asianmukainen henkilökohtaisen yhteyshenkilön kelpoisuusasetus kullekin kattavuusasetukselle.</span><span class="sxs-lookup"><span data-stu-id="41ad0-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="41ad0-142">Määritä **Itsepalvelu**-kohdassa seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="41ad0-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="41ad0-143">Kenttä</span><span class="sxs-lookup"><span data-stu-id="41ad0-143">Field</span></span> | <span data-ttu-id="41ad0-144">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="41ad0-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="41ad0-145">**Salli työntekijän korvaussumma**</span><span class="sxs-lookup"><span data-stu-id="41ad0-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="41ad0-146">Määrittää, saavatko työntekijät muokata etujen itsepalvelun maksumäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="41ad0-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="41ad0-147">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen maksumäärän perusteella, jonka työntekijä syöttää etujen itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="41ad0-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="41ad0-148">**Salli työntekijän kattavuussumma**</span><span class="sxs-lookup"><span data-stu-id="41ad0-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="41ad0-149">Määrittää, saavatko työntekijät muokata etujen itsepalvelun kattavuusmäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="41ad0-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="41ad0-150">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen kattavuusmäärän perusteella, jonka työntekijä syöttää työntekijän itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="41ad0-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="41ad0-151">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="41ad0-151">Select **Save**.</span></span> 
