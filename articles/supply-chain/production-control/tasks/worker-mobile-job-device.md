---
title: Määritä työssä mobiililaitetta käyttävä työntekijä
description: Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ada42a98a8a87e377f939d063b17f9904f6b3408
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978231"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="b542b-103">Määritä työssä mobiililaitetta käyttävä työntekijä</span><span class="sxs-lookup"><span data-stu-id="b542b-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b542b-104">Tässä ohjeaiheessa kerrotaan, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="b542b-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="b542b-105">Varmista, että työntekijälle on määritetty tietty rooli</span><span class="sxs-lookup"><span data-stu-id="b542b-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="b542b-106">Tässä esimerkissä tarkistetaan, että käyttäjälle "SHANNON" on määritetty koneoperaattorin rooli ennen työntekijätilin määrittämistä.</span><span class="sxs-lookup"><span data-stu-id="b542b-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="b542b-107">Valitse **Siirtymisruutu > Moduulit > Järjestelmänhallinta > Käyttäjät > Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="b542b-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="b542b-108">Etsi käyttäjä pikasuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="b542b-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="b542b-109">Syötä tässä esimerkissä arvoksi `shannon`.</span><span class="sxs-lookup"><span data-stu-id="b542b-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="b542b-110">Valitse näyttöön tulevassa käyttäjätilissä **Käyttäjätunnus**-sarakkeessa oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="b542b-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="b542b-111">Valitse **Käyttäjän roolit** -puussa **Roolit > Koneenkäyttäjä**.</span><span class="sxs-lookup"><span data-stu-id="b542b-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="b542b-112">Palaa kotisivulle sulkemalla **Käyttäjän tiedot**- ja **Käyttäjät**-sivut.</span><span class="sxs-lookup"><span data-stu-id="b542b-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="b542b-113">Määritä työntekijän tili</span><span class="sxs-lookup"><span data-stu-id="b542b-113">Configure worker account</span></span>
1. <span data-ttu-id="b542b-114">Siirry kohtaan **Siirtymisruutu > Moduulit > Henkilöstöhallinto > Työntekijät > Työntekijät**.</span><span class="sxs-lookup"><span data-stu-id="b542b-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="b542b-115">Etsi käyttäjä pikasuodattimesta.</span><span class="sxs-lookup"><span data-stu-id="b542b-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="b542b-116">Syötä tässä esimerkissä arvoksi `shannon`.</span><span class="sxs-lookup"><span data-stu-id="b542b-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="b542b-117">Valitse näyttöön tulevassa käyttäjätilissä **Nimi**-sarakkeessa oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="b542b-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="b542b-118">Valitse**Aikarekisteröinti**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="b542b-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="b542b-119">Valitse **Aktivoi rekisteröintipäätteissä**.</span><span class="sxs-lookup"><span data-stu-id="b542b-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="b542b-120">Valitse tai kirjoita arvot seuraaviin kenttiin:</span><span class="sxs-lookup"><span data-stu-id="b542b-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="b542b-121">**Laskentaryhmä**</span><span class="sxs-lookup"><span data-stu-id="b542b-121">**Calculation group**</span></span>  
    - <span data-ttu-id="b542b-122">**Oletuslaskentaryhmä**</span><span class="sxs-lookup"><span data-stu-id="b542b-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="b542b-123">**Hyväksyntäryhmä**</span><span class="sxs-lookup"><span data-stu-id="b542b-123">**Approval group**</span></span>  
    - <span data-ttu-id="b542b-124">**Vakioprofiili**</span><span class="sxs-lookup"><span data-stu-id="b542b-124">**Standard profile**</span></span>  
    - <span data-ttu-id="b542b-125">**Profiiliryhmä**</span><span class="sxs-lookup"><span data-stu-id="b542b-125">**Profile group**</span></span>  

7. <span data-ttu-id="b542b-126">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b542b-126">Select **OK**.</span></span>
8. <span data-ttu-id="b542b-127">Anna uuden aikarekisteröinnin työntekijän nimilapun numero valitsemalla **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b542b-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="b542b-128">Anna arvo **Nimilapun tunnus**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="b542b-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="b542b-129">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="b542b-129">Select **Save**.</span></span>
10. <span data-ttu-id="b542b-130">Sulje **Työntekijän tiedot**- ja **Työntekijät**-sivut.</span><span class="sxs-lookup"><span data-stu-id="b542b-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="b542b-131">Määritä työntekijä laiteryhmään</span><span class="sxs-lookup"><span data-stu-id="b542b-131">Assign worker to device group</span></span>
1. <span data-ttu-id="b542b-132">Valitse **Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten**.</span><span class="sxs-lookup"><span data-stu-id="b542b-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="b542b-133">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="b542b-133">Select **Add**.</span></span>
3. <span data-ttu-id="b542b-134">Valitse luettelosta haluamasi työntekijä.</span><span class="sxs-lookup"><span data-stu-id="b542b-134">In the list, select the desired worker.</span></span> <span data-ttu-id="b542b-135">Valitse tässä esimerkissä **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="b542b-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="b542b-136">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="b542b-136">Select **OK**.</span></span>
5. <span data-ttu-id="b542b-137">Valitse **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="b542b-137">Select **Edit**.</span></span>
6. <span data-ttu-id="b542b-138">Voit määrittää **Tuotantoyksikkö**-kentässä työntekijän oletussuodattimen.</span><span class="sxs-lookup"><span data-stu-id="b542b-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="b542b-139">Tämä varmistaa, että vain valittujen tuotantoyksiköiden tuotantotyöt näytetään, kun työntekijä kirjautuu laitteeseen.</span><span class="sxs-lookup"><span data-stu-id="b542b-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="b542b-140">Anna haluttu arvo.</span><span class="sxs-lookup"><span data-stu-id="b542b-140">Enter the desired value.</span></span>
7. <span data-ttu-id="b542b-141">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="b542b-141">Close the page.</span></span>

