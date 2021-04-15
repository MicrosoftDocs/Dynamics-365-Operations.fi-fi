---
title: Etuuskelpoisuussääntöjen ja -käytäntöjen määrittäminen
description: Tässä artikkelissa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805943"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="2cc62-103">Etuuskelpoisuussääntöjen ja -käytäntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2cc62-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2cc62-104">Tässä aiheessa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin.</span><span class="sxs-lookup"><span data-stu-id="2cc62-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="2cc62-105">Etukelpoisuuden käytäntösääntötyypin luominen</span><span class="sxs-lookup"><span data-stu-id="2cc62-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="2cc62-106">Valitse **Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytäntösääntötyypit**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="2cc62-107">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-107">Select **New**.</span></span>
3. <span data-ttu-id="2cc62-108">Anna **Säännön nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2cc62-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="2cc62-109">Anna arvo **Kuvaus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="2cc62-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="2cc62-110">Avaa haku valitsemalla **Kyselyn nimi** -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="2cc62-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="2cc62-111">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2cc62-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="2cc62-112">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-112">Select **Save**.</span></span>
8. <span data-ttu-id="2cc62-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2cc62-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="2cc62-114">Etukelpoisuuden käytäntö</span><span class="sxs-lookup"><span data-stu-id="2cc62-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="2cc62-115">Valitse **Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="2cc62-116">Valitse aiemmin luotu etukäytäntö.</span><span class="sxs-lookup"><span data-stu-id="2cc62-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="2cc62-117">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2cc62-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="2cc62-118">Ota käyttöön **Käytäntöorganisaatiot**-osien laajennus.</span><span class="sxs-lookup"><span data-stu-id="2cc62-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="2cc62-119">Voit lisätä organisaatiot, jotka haluat lisätä käytäntöön, tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="2cc62-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="2cc62-120">Laajenna tai tiivistä **Käytäntösäännöt**-osa.</span><span class="sxs-lookup"><span data-stu-id="2cc62-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="2cc62-121">Valitse luettelosta aiemmin luotu käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="2cc62-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="2cc62-122">Valitse **Luo käytäntösääntö**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="2cc62-123">Syötä **Voimaantulopäivä**-kenttään päivämäärä, jolloin haluat ottaa käytännön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2cc62-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="2cc62-124">Kun voimaantulo- ja päättymispäivät määritetään, voit muuttaa käytäntösääntöjä jatkossa. Näin käytäntöön ei tarvitse palata silloin, kun haluat ottaa muutokset käyttöön.</span><span class="sxs-lookup"><span data-stu-id="2cc62-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="2cc62-125">Lisää tarvittaessa where-lauseke **Lisää ehto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2cc62-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="2cc62-126">Jos esimerkiksi haluat kohdistaa säännön vain myyntipäällikköihin, voit luoda seuraavan where-lauseen: kun toimen kuvaus on yhtä suuri kuin myyntipäällikkö.</span><span class="sxs-lookup"><span data-stu-id="2cc62-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="2cc62-127">Useita where-lauseita voi lisätä säännössä kerralla.</span><span class="sxs-lookup"><span data-stu-id="2cc62-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="2cc62-128">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-128">Select **OK**.</span></span>
11. <span data-ttu-id="2cc62-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="2cc62-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="2cc62-130">Säännön liittäminen etuun</span><span class="sxs-lookup"><span data-stu-id="2cc62-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="2cc62-131">Siirry kohtaan **Henkilöstöhallinto > Edut > Edut**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="2cc62-132">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="2cc62-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="2cc62-133">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2cc62-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="2cc62-134">Laajenna tai tiivistä **Oikeutussäännöt**-osa.</span><span class="sxs-lookup"><span data-stu-id="2cc62-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="2cc62-135">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-135">Select **Edit**.</span></span>
6. <span data-ttu-id="2cc62-136">Valitse **Oikeutus**-kentässä sääntö.</span><span class="sxs-lookup"><span data-stu-id="2cc62-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="2cc62-137">Valitse **Sääntötyyppi**-kentässä aiemmin luotu sääntö.</span><span class="sxs-lookup"><span data-stu-id="2cc62-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="2cc62-138">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="2cc62-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="2cc62-139">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="2cc62-139">Select **Save**.</span></span>
11. <span data-ttu-id="2cc62-140">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="2cc62-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]