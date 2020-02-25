---
title: Kattavuusasetusten luominen
description: ''
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
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008828"
---
# <a name="create-coverage-options"></a><span data-ttu-id="5e404-102">Kattavuusasetusten luominen</span><span class="sxs-lookup"><span data-stu-id="5e404-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5e404-103">Microsoft Dynamics 365 Human Resourcesin kattavuusasetukset ovat osallistujan valitsemia kattavuustasoja etuussuunnitelmassa tai -ohjelmassa, kuten Vain työntekijä terveydenhoitosuunnitelman osalta tai 2 x palkka henkivakuutussuunnitelman osalta.</span><span class="sxs-lookup"><span data-stu-id="5e404-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="5e404-104">Kun etujen kattavuusasetukset on määritetty, niitä voidaan käyttää uudelleen, ja voit kohdistaa astuksen yhdelle tai useammalle suunnitelmalle.</span><span class="sxs-lookup"><span data-stu-id="5e404-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="5e404-105">Kun kattavuus setukset on määritetty, liitä kattavuusasetukset etuussuunnitelmatyyppiin.</span><span class="sxs-lookup"><span data-stu-id="5e404-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="5e404-106">Tämän jälkeen suunnitelmatyyppi yhdistetään etuussuunnitelmaan tai -ohjelmaan.</span><span class="sxs-lookup"><span data-stu-id="5e404-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="5e404-107">Suunnitelmatyyppiin yhdistetyt kattavuusasetukset ovat käytettävissä kaikissa suunnitelmissa, jotka luodaan kyseisellä suunnitelmatyypillä.</span><span class="sxs-lookup"><span data-stu-id="5e404-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="5e404-108">Valitse **Etujen hallinta** -työtilassa **Asetukset**-kohdasta **Kattavuusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="5e404-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="5e404-109">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="5e404-109">Select **New**.</span></span>

3. <span data-ttu-id="5e404-110">Määritä seuraavien kenttien arvot.</span><span class="sxs-lookup"><span data-stu-id="5e404-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e404-111">Kenttä</span><span class="sxs-lookup"><span data-stu-id="5e404-111">Field</span></span> | <span data-ttu-id="5e404-112">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5e404-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e404-113">**Kattavuusasetus**</span><span class="sxs-lookup"><span data-stu-id="5e404-113">**Coverage option**</span></span> | <span data-ttu-id="5e404-114">Yksilöllinen kattavuusasetuksen nimi.</span><span class="sxs-lookup"><span data-stu-id="5e404-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="5e404-115">**Kuvaus**</span><span class="sxs-lookup"><span data-stu-id="5e404-115">**Description**</span></span> | <span data-ttu-id="5e404-116">Kattavuusasetuksen kuvaus.</span><span class="sxs-lookup"><span data-stu-id="5e404-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="5e404-117">**Kattavuuskoodi**</span><span class="sxs-lookup"><span data-stu-id="5e404-117">**Coverage code**</span></span> | <span data-ttu-id="5e404-118">Kattavuuskoodit määrittävät kullekin kelvolliselle katetulle henkilötyypille enimmäis- ja vähimmäismäärät.</span><span class="sxs-lookup"><span data-stu-id="5e404-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="5e404-119">Kattavuuskoodi ilmaisee, kenet katetaan tai suunnitelmatyypille sallitun kattavuusmäärän.</span><span class="sxs-lookup"><span data-stu-id="5e404-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="5e404-120">Voit ilmaista kattavuusmäärän dollarisummana tai prosenttiosuutenta.</span><span class="sxs-lookup"><span data-stu-id="5e404-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="5e404-121">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="5e404-121">For example:</span></span></br></br><span data-ttu-id="5e404-122">- **Työnt+1** – Täyttääkseen kelpoisuusvaatimuksen työntekijällä on oltava valittuna yksi huollettava (tämän määrän ylittävät huollettavat eivät enää kuulu suunnitelman piitiin).</span><span class="sxs-lookup"><span data-stu-id="5e404-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="5e404-123">- **Työnt+perhe** – Täyttääkseen kelpoisuusvaatimukset työntekijällä on oltava valittuna vähintään kaksi huollettavaa.</span><span class="sxs-lookup"><span data-stu-id="5e404-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="5e404-124">**Enimmäismäärä**</span><span class="sxs-lookup"><span data-stu-id="5e404-124">**Maximum number**</span></span> | <span data-ttu-id="5e404-125">Huollettavien enimmäismäärä.</span><span class="sxs-lookup"><span data-stu-id="5e404-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="5e404-126">**Tila**</span><span class="sxs-lookup"><span data-stu-id="5e404-126">**Status**</span></span> | <span data-ttu-id="5e404-127">Kattavuusasetuksen tila.</span><span class="sxs-lookup"><span data-stu-id="5e404-127">The status of the coverage option.</span></span> <span data-ttu-id="5e404-128">Jos kattavuusasetuksen tilaksi asetetaan Passiivinen, kyseistä kattavuusasetusta ei voida valita suunnitelmatyypeissä.</span><span class="sxs-lookup"><span data-stu-id="5e404-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="5e404-129">**Prosenttia**</span><span class="sxs-lookup"><span data-stu-id="5e404-129">**Percent**</span></span> | <span data-ttu-id="5e404-130">Prosenttiosuus.</span><span class="sxs-lookup"><span data-stu-id="5e404-130">The percent amount.</span></span> <span data-ttu-id="5e404-131">Tämä kenttä on aktiivinen vain, jos kattavuuskoodikentässä on valittu % x palkka.</span><span class="sxs-lookup"><span data-stu-id="5e404-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="5e404-132">**Jakaja**</span><span class="sxs-lookup"><span data-stu-id="5e404-132">**Divisor**</span></span> | <span data-ttu-id="5e404-133">Laskennassa käytettävä jalkaja, kun valitaan kattavuuskoodi % x palkka.</span><span class="sxs-lookup"><span data-stu-id="5e404-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="5e404-134">**Vähimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="5e404-134">**Percent minimum**</span></span> | <span data-ttu-id="5e404-135">Vähimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="5e404-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="5e404-136">**Enimmäisprosenttiosuus**</span><span class="sxs-lookup"><span data-stu-id="5e404-136">**Percent maximum**</span></span> | <span data-ttu-id="5e404-137">Enimmäisprosenttiosuus, kun valitset Prosenttiosuus-kattavuuskoodin.</span><span class="sxs-lookup"><span data-stu-id="5e404-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="5e404-138">Liitä kohtaan **Henkilökohtaisen yhteyshenkilön kelpoisuusvaihtoehdot** asianmukainen henkilökohtaisen yhteyshenkilön kelpoisuusasetus kullekin kattavuusasetukselle.</span><span class="sxs-lookup"><span data-stu-id="5e404-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="5e404-139">Määritä **Itsepalvelu**-kohdassa seuraavien kenttien arvot:</span><span class="sxs-lookup"><span data-stu-id="5e404-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="5e404-140">Kenttä</span><span class="sxs-lookup"><span data-stu-id="5e404-140">Field</span></span> | <span data-ttu-id="5e404-141">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="5e404-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e404-142">**Salli työntekijän korvaussumma**</span><span class="sxs-lookup"><span data-stu-id="5e404-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="5e404-143">Määrittää, saavatko työntekijät muokata etujen itsepalvelun maksumäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="5e404-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5e404-144">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen maksumäärän perusteella, jonka työntekijä syöttää etujen itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="5e404-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="5e404-145">**Salli työntekijän kattavuussumma**</span><span class="sxs-lookup"><span data-stu-id="5e404-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="5e404-146">Määrittää, saavatko työntekijät muokata etujen itsepalvelun kattavuusmäärää, kun he valitsevat etuja.</span><span class="sxs-lookup"><span data-stu-id="5e404-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="5e404-147">Jos valitset tämän valintaruudun, järjestelmä laskee etuussuunnitelman parametrit sen kattavuusmäärän perusteella, jonka työntekijä syöttää työntekijän itsepalveluun.</span><span class="sxs-lookup"><span data-stu-id="5e404-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="5e404-148">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="5e404-148">Select **Save**.</span></span> 
