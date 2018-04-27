--- 
title: "Määritä edun oikeutussäännöt ja -käytännöt"
description: "Tässä tallenteessa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="7fda9-103">Määritä edun oikeutussäännöt ja -käytännöt</span><span class="sxs-lookup"><span data-stu-id="7fda9-103">Define benefit eligibility rules and policies</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fda9-104">Tässä tallenteessa kerrotaan, miten edun oikeutussäännöt ja -käytännöt luodaan. Tämän jälkeen näytetään, miten säännöt liitetään etuihin.</span><span class="sxs-lookup"><span data-stu-id="7fda9-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="7fda9-105">Tämän tallenteen luomisessa käytetty demotietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="7fda9-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="7fda9-106">Etukelpoisuuden käytäntösääntötyypin luominen</span><span class="sxs-lookup"><span data-stu-id="7fda9-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="7fda9-107">Valitse Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytäntösääntötyypit.</span><span class="sxs-lookup"><span data-stu-id="7fda9-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="7fda9-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="7fda9-108">Click New.</span></span>
3. <span data-ttu-id="7fda9-109">Kirjoita arvo Säännön nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7fda9-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="7fda9-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="7fda9-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7fda9-111">Avaa haku valitsemalla Kyselyn nimi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7fda9-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7fda9-112">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7fda9-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7fda9-113">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7fda9-113">Click Save.</span></span>
8. <span data-ttu-id="7fda9-114">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fda9-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="7fda9-115">Etukelpoisuuden käytäntö</span><span class="sxs-lookup"><span data-stu-id="7fda9-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="7fda9-116">Valitse Henkilöstöhallinto > Edut > Oikeutus > Etukelpoisuuden käytännöt.</span><span class="sxs-lookup"><span data-stu-id="7fda9-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="7fda9-117">Valitse aiemmin luotu etukäytäntö.</span><span class="sxs-lookup"><span data-stu-id="7fda9-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="7fda9-118">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7fda9-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7fda9-119">Ota käyttöön Käytäntöorganisaatiot-osien laajennus.</span><span class="sxs-lookup"><span data-stu-id="7fda9-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="7fda9-120">Tässä voit lisätä organisaatiot, jotka haluat lisätä käytäntöön, tai poistaa niitä.</span><span class="sxs-lookup"><span data-stu-id="7fda9-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="7fda9-121">Laajenna tai tiivistä Käytäntösäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="7fda9-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="7fda9-122">Valitse luettelosta aiemmin luotu käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="7fda9-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="7fda9-123">Valitse Luo käytäntösääntö.</span><span class="sxs-lookup"><span data-stu-id="7fda9-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="7fda9-124">Syötä Voimaantulopäivä-kenttään päivämäärä, jolloin haluat ottaa käytännön käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7fda9-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="7fda9-125">Kun voimaantulo- ja päättymispäivät määritetään, voit muuttaa käytäntösääntöjä jatkossa. Näin käytäntöön ei tarvitse palata silloin, kun haluat ottaa muutokset käyttöön.</span><span class="sxs-lookup"><span data-stu-id="7fda9-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="7fda9-126">Jos esimerkiksi haluat kohdistaa säännön vain myyntipäällikköihin, voit luoda seuraavan Where-lauseen: kun toimen kuvaus on yhtä suuri kuin myyntipäällikkö.</span><span class="sxs-lookup"><span data-stu-id="7fda9-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="7fda9-127">Where-lauseita voi yhdistää säännössä And- ja Or-operaattorin avulla.</span><span class="sxs-lookup"><span data-stu-id="7fda9-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="7fda9-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="7fda9-128">Click OK.</span></span>
11. <span data-ttu-id="7fda9-129">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fda9-129">Close the page.</span></span>
12. <span data-ttu-id="7fda9-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="7fda9-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="7fda9-131">Säännön liittäminen etuun</span><span class="sxs-lookup"><span data-stu-id="7fda9-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="7fda9-132">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="7fda9-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="7fda9-133">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="7fda9-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7fda9-134">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7fda9-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7fda9-135">Laajenna tai tiivistä Oikeutussäännöt-osa.</span><span class="sxs-lookup"><span data-stu-id="7fda9-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="7fda9-136">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="7fda9-136">Click Edit.</span></span>
6. <span data-ttu-id="7fda9-137">Valitse Oikeutus-kentässä luettelosta Sääntöön perustuva -kohta.</span><span class="sxs-lookup"><span data-stu-id="7fda9-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="7fda9-138">Avaa haku valitsemalla Sääntötyyppi-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="7fda9-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="7fda9-139">Etsi ja valitse luettelosta aiemmin luotu sääntö.</span><span class="sxs-lookup"><span data-stu-id="7fda9-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="7fda9-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="7fda9-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7fda9-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="7fda9-141">Click Save.</span></span>
11. <span data-ttu-id="7fda9-142">Sulje lomake.</span><span class="sxs-lookup"><span data-stu-id="7fda9-142">Close the form.</span></span>


