---
title: Määritä työssä mobiililaitetta käyttävä työntekijä
description: Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.
author: ShylaThompson
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8573909476009d5f37a3c0d02ac57b0d518dc267
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148742"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="716d2-103">Määritä työssä mobiililaitetta käyttävä työntekijä</span><span class="sxs-lookup"><span data-stu-id="716d2-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="716d2-104">Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="716d2-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="716d2-105">Varmista, että työntekijälle on määritetty tietty rooli</span><span class="sxs-lookup"><span data-stu-id="716d2-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="716d2-106">Tässä esimerkissä tarkistetaan, että käyttäjälle "SHANNON" on määritetty koneoperaattorin rooli ennen työntekijätilin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="716d2-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="716d2-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="716d2-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="716d2-108">Etsi käyttäjä pikasuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="716d2-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="716d2-109">Syötä tässä esimerkissä arvoksi `shannon`.</span><span class="sxs-lookup"><span data-stu-id="716d2-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="716d2-110">Valitse näyttöön tulevassa käyttäjätilissä **Käyttäjätunnus**-sarakkeessa oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="716d2-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="716d2-111">Valitse **Käyttäjän roolit** -puussa **Roolit > Koneenkäyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="716d2-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="716d2-112">Palaa kotisivulle sulkemalla **Käyttäjän tiedot**- ja **Käyttäjät**-sivut.</span><span class="sxs-lookup"><span data-stu-id="716d2-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="716d2-113">Määritä työntekijän tili</span><span class="sxs-lookup"><span data-stu-id="716d2-113">Configure worker account</span></span>
1. <span data-ttu-id="716d2-114">Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työntekijät > Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="716d2-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="716d2-115">Etsi käyttäjä pikasuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="716d2-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="716d2-116">Syötä tässä esimerkissä arvoksi `shannon`.</span><span class="sxs-lookup"><span data-stu-id="716d2-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="716d2-117">Valitse näyttöön tulevassa käyttäjätilissä **Nimi**-sarakkeessa oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="716d2-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="716d2-118">Valitse**Aikarekisteröinti**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="716d2-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="716d2-119">Valitse **Aktivoi rekisteröintipäätteissä**.</span><span class="sxs-lookup"><span data-stu-id="716d2-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="716d2-120">Valitse tai kirjoita arvot seuraaviin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="716d2-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="716d2-121">**Laskentaryhmä**</span><span class="sxs-lookup"><span data-stu-id="716d2-121">**Calculation group**</span></span>  
    - <span data-ttu-id="716d2-122">**Oletuslaskentaryhmä**</span><span class="sxs-lookup"><span data-stu-id="716d2-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="716d2-123">**Hyväksyntäryhmä**</span><span class="sxs-lookup"><span data-stu-id="716d2-123">**Approval group**</span></span>  
    - <span data-ttu-id="716d2-124">**Vakioprofiili**</span><span class="sxs-lookup"><span data-stu-id="716d2-124">**Standard profile**</span></span>  
    - <span data-ttu-id="716d2-125">**Profiiliryhmä**</span><span class="sxs-lookup"><span data-stu-id="716d2-125">**Profile group**</span></span>  

7. <span data-ttu-id="716d2-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="716d2-126">Select **OK**.</span></span>
8. <span data-ttu-id="716d2-127">Anna uuden aikarekisteröinnin työntekijän nimilapun numero valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="716d2-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="716d2-128">Anna arvo **Nimilapun tunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="716d2-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="716d2-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="716d2-129">Select **Save**.</span></span>
10. <span data-ttu-id="716d2-130">Sulje **Työntekijän tiedot**- ja **Työntekijät**-sivut.</span><span class="sxs-lookup"><span data-stu-id="716d2-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="716d2-131">Määritä työntekijä laiteryhmään</span><span class="sxs-lookup"><span data-stu-id="716d2-131">Assign worker to device group</span></span>
1. <span data-ttu-id="716d2-132">Valitse **Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten**.</span><span class="sxs-lookup"><span data-stu-id="716d2-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="716d2-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="716d2-133">Select **Add**.</span></span>
3. <span data-ttu-id="716d2-134">Valitse luettelosta haluamasi työntekijä.</span><span class="sxs-lookup"><span data-stu-id="716d2-134">In the list, select the desired worker.</span></span> <span data-ttu-id="716d2-135">Valitse tässä esimerkissä **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="716d2-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="716d2-136">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="716d2-136">Select **OK**.</span></span>
5. <span data-ttu-id="716d2-137">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="716d2-137">Select **Edit**.</span></span>
6. <span data-ttu-id="716d2-138">Voit määrittää **Tuotantoyksikkö**-kentässä työntekijän oletussuodattimen.</span><span class="sxs-lookup"><span data-stu-id="716d2-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="716d2-139">Tämä varmistaa, että vain valittujen tuotantoyksiköiden tuotantotyöt näytetään, kun työntekijä kirjautuu laitteeseen.</span><span class="sxs-lookup"><span data-stu-id="716d2-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="716d2-140">Anna haluttu arvo.</span><span class="sxs-lookup"><span data-stu-id="716d2-140">Enter the desired value.</span></span>
7. <span data-ttu-id="716d2-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="716d2-141">Close the page.</span></span>

