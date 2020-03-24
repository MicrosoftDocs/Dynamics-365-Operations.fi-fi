---
title: Kattavuusasetusten luominen
description: Microsoft Dynamics 365 Human Resourcesin kattavuusasetukset ovat osallistujan valitsemia kattavuustasoja etuussuunnitelmassa tai -ohjelmassa, kuten Vain työntekijä terveydenhoitosuunnitelman osalta tai 2 x palkka henkivakuutussuunnitelman osalta.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0af2b6ae0853b4c7f64c4d4f04299c87089d622b
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092703"
---
# <a name="create-coverage-options"></a><span data-ttu-id="30915-103">Kattavuusasetusten luominen</span><span class="sxs-lookup"><span data-stu-id="30915-103">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="30915-104">Microsoft Dynamics 365 Human Resourcesin kattavuusasetukset ovat osallistujan valitsemia kattavuustasoja etuussuunnitelmassa tai -ohjelmassa, kuten Vain työntekijä terveydenhoitosuunnitelman osalta tai 2 x palkka henkivakuutussuunnitelman osalta.</span><span class="sxs-lookup"><span data-stu-id="30915-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="30915-105">Kun etujen kattavuusasetukset on määritetty, niitä voidaan käyttää uudelleen, ja voit kohdistaa astuksen yhdelle tai useammalle suunnitelmalle.</span><span class="sxs-lookup"><span data-stu-id="30915-105">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="30915-106">Kun kattavuus setukset on määritetty, liitä kattavuusasetukset etuussuunnitelmatyyppiin.</span><span class="sxs-lookup"><span data-stu-id="30915-106">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="30915-107">Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="30915-107">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="30915-108">Suunnitelmatyyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa suunnitelmissa, jotka luodaan kyseisellä suunnitelmatyypillä.</span><span class="sxs-lookup"><span data-stu-id="30915-108">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="30915-109">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Kattavuusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="30915-109">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="30915-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="30915-110">Select **New**.</span></span>

3. <span data-ttu-id="30915-111">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="30915-111">Specify values for the following fields:</span></span>

   | <span data-ttu-id="30915-112">Kenttä</span><span class="sxs-lookup"><span data-stu-id="30915-112">Field</span></span> | <span data-ttu-id="30915-113">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="30915-113">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="30915-114">**Kattavuusasetus**</span><span class="sxs-lookup"><span data-stu-id="30915-114">**Coverage option**</span></span> | <span data-ttu-id="30915-115">Yksilöllinen kattavuusasetuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="30915-115">A unique coverage option name.</span></span> |
   | <span data-ttu-id="30915-116">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="30915-116">**Description**</span></span> | <span data-ttu-id="30915-117">Kattavuusasetuksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="30915-117">A description of the coverage option.</span></span> |
   | <span data-ttu-id="30915-118">**Kattavuuskoodi**</span><span class="sxs-lookup"><span data-stu-id="30915-118">**Coverage code**</span></span> | <span data-ttu-id="30915-119">Kattavuuskoodit määrittävät kullekin kelvolliselle katetulle henkilötyypille enimmäis- ja vähimmäismäärät.</span><span class="sxs-lookup"><span data-stu-id="30915-119">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="30915-120">Kattavuuskoodi ilmaisee, kenet katetaan tai suunnitelmatyypille sallitun kattavuusmäärän.</span><span class="sxs-lookup"><span data-stu-id="30915-120">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="30915-121">Voit ilmaista kattavuusmäärän dollarisummana tai prosenttiosuutenta.</span><span class="sxs-lookup"><span data-stu-id="30915-121">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="30915-122">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="30915-122">For example:</span></span></br></br><span data-ttu-id="30915-123">- **Työnt+1** – Täyttääkseen kelpoisuusvaatimuksen työntekijällä on oltava valittuna yksi huollettava (tämän määrän ylittävät huollettavat eivät enää kuulu suunnitelman piitiin).</span><span class="sxs-lookup"><span data-stu-id="30915-123">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="30915-124">- **Työnt+perhe** – Täyttääkseen kelpoisuusvaatimukset työntekijällä on oltava valittuna vähintään kaksi huollettavaa.</span><span class="sxs-lookup"><span data-stu-id="30915-124">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="30915-125">**Enimmäismäärä**</span><span class="sxs-lookup"><span data-stu-id="30915-125">**Maximum number**</span></span> | <span data-ttu-id="30915-126">Huollettavien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="30915-126">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="30915-127">**Tila**</span><span class="sxs-lookup"><span data-stu-id="30915-127">**Status**</span></span> | <span data-ttu-id="30915-128">Kattavuusasetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="30915-128">The status of the coverage option.</span></span> <span data-ttu-id="30915-129">Jos kattavuusasetuksen tilaksi asetetaan Passiivinen, kyseistä kattavuusasetusta ei voida valita suunnitelmatyypeissä.</span><span class="sxs-lookup"><span data-stu-id="30915-129">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="30915-130">**Prosenttia**</span><span class="sxs-lookup"><span data-stu-id="30915-130">**Percent**</span></span> | <span data-ttu-id="30915-131">Prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="30915-131">The percent amount.</span></span> <span data-ttu-id="30915-132">Tämä kenttä on aktiivinen vain, jos kattavuuskoodikentässä on valittu % x palkka.</span><span class="sxs-lookup"><span data-stu-id="30915-132">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="30915-133">**Jakaja**</span><span class="sxs-lookup"><span data-stu-id="30915-133">**Divisor**</span></span> | <span data-ttu-id="30915-134">Laskennassa käytettävä jalkaja, kun valitaan kattavuuskoodi % x palkka.</span><span class="sxs-lookup"><span data-stu-id="30915-134">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="30915-135">**Vähimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="30915-135">**Percent minimum**</span></span> | <span data-ttu-id="30915-136">Vähimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="30915-136">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="30915-137">**Enimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="30915-137">**Percent maximum**</span></span> | <span data-ttu-id="30915-138">Enimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="30915-138">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="30915-139">Liitä kohtaan **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** asianmukainen henkilökohtaisen yhteyshenkilön kelpoisuusasetus kullekin kattavuusasetukselle.</span><span class="sxs-lookup"><span data-stu-id="30915-139">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="30915-140">Määritä **Itsepalvelu**-kohdassa seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="30915-140">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="30915-141">Kenttä</span><span class="sxs-lookup"><span data-stu-id="30915-141">Field</span></span> | <span data-ttu-id="30915-142">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="30915-142">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="30915-143">**Salli työntekijän korvaussumma**</span><span class="sxs-lookup"><span data-stu-id="30915-143">**Allow employee contribution amount**</span></span> | <span data-ttu-id="30915-144">Määrittää, saavatko työntekijät muokata etujen itsepalvelun maksumäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="30915-144">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="30915-145">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen maksumäärän perusteella, jonka työntekijä syöttää etujen itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="30915-145">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="30915-146">**Salli työntekijän kattavuussumma**</span><span class="sxs-lookup"><span data-stu-id="30915-146">**Allow employee coverage amount**</span></span> | <span data-ttu-id="30915-147">Määrittää, saavatko työntekijät muokata etujen itsepalvelun kattavuusmäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="30915-147">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="30915-148">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen kattavuusmäärän perusteella, jonka työntekijä syöttää työntekijän itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="30915-148">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="30915-149">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="30915-149">Select **Save**.</span></span> 
