---
title: Määritä työssä mobiililaitetta käyttävä työntekijä
description: Tässä menettelyssä näytetään, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "327386"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="0a830-103">Määritä työssä mobiililaitetta käyttävä työntekijä</span><span class="sxs-lookup"><span data-stu-id="0a830-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a830-104">Tässä menettelyssä näytetään, miten työntekijän käyttäjätilille määritetään oikeat roolit, ja annetaan sitten työntekijälle mahdollisuus tehdä työnohjauksen rekisteröintejä.</span><span class="sxs-lookup"><span data-stu-id="0a830-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="0a830-105">Määritä rooleja käyttäjätilille</span><span class="sxs-lookup"><span data-stu-id="0a830-105">Assign roles to user account</span></span>
1. <span data-ttu-id="0a830-106">Valitse Järjestelmänhallinta > Käyttäjät > Käyttäjät.</span><span class="sxs-lookup"><span data-stu-id="0a830-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="0a830-107">Suodata pikasuodatuksella työntekijä, jonka käyttäjätili on liitetty koneenkäyttäjän rooliin.</span><span class="sxs-lookup"><span data-stu-id="0a830-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="0a830-108">Mallitiedoissa nimenä on Shannon.</span><span class="sxs-lookup"><span data-stu-id="0a830-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="0a830-109">Valitse käyttäjätilitietue.</span><span class="sxs-lookup"><span data-stu-id="0a830-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="0a830-110">Avaa käyttäjätilin tiedot napsauttamalla luettelossa valitulla rivillä Nimi-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0a830-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="0a830-111">Valitse puussa Roolit\Koneenkäyttäjä.</span><span class="sxs-lookup"><span data-stu-id="0a830-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="0a830-112">Sulje käyttäjätietojen tietosivu.</span><span class="sxs-lookup"><span data-stu-id="0a830-112">Close the user account details page.</span></span>
7. <span data-ttu-id="0a830-113">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0a830-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="0a830-114">Määritä työntekijän tili.</span><span class="sxs-lookup"><span data-stu-id="0a830-114">Configure worker account.</span></span>
1. <span data-ttu-id="0a830-115">Valitse Henkilöstöhallinto > Työntekijät > Työntekijät.</span><span class="sxs-lookup"><span data-stu-id="0a830-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="0a830-116">Suodata pikasuodatuksella työntekijä, jonka käyttäjätili on liitetty koneenkäyttäjän rooliin.</span><span class="sxs-lookup"><span data-stu-id="0a830-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="0a830-117">Mallitiedoissa nimenä on Shannon.</span><span class="sxs-lookup"><span data-stu-id="0a830-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="0a830-118">Valitse käyttäjätilitietue.</span><span class="sxs-lookup"><span data-stu-id="0a830-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="0a830-119">Avaa käyttäjätilin tiedot napsauttamalla luettelossa valitulla rivillä Nimi-linkkiä.</span><span class="sxs-lookup"><span data-stu-id="0a830-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="0a830-120">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="0a830-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="0a830-121">Laajenna Aikarekisteröinti-pikavälilehti ja valitse Aktivoi rekisteröintipäätteissä.</span><span class="sxs-lookup"><span data-stu-id="0a830-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="0a830-122">Valitse Aktivoi rekisteröintipäätteissä.</span><span class="sxs-lookup"><span data-stu-id="0a830-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="0a830-123">Anna tai valitse Laskentaryhmä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="0a830-124">Anna tai valitse Oletuslaskentaryhmä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="0a830-125">Anna tai valitse Hyväksyntäryhmä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="0a830-126">Anna tai valitse Vakioprofiili-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="0a830-127">Anna tai valitse Profiiliryhmä-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="0a830-128">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0a830-128">Click OK.</span></span>
14. <span data-ttu-id="0a830-129">Anna uuden aikarekisteröinnin työntekijän nimilapun numero valitsemalla Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0a830-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="0a830-130">Kirjoita Nimilapun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0a830-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="0a830-131">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="0a830-131">Click Save.</span></span>
17. <span data-ttu-id="0a830-132">Käytä SaveRecord-pikavalintaa.</span><span class="sxs-lookup"><span data-stu-id="0a830-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="0a830-133">Sulje työntekijän tietosivu.</span><span class="sxs-lookup"><span data-stu-id="0a830-133">Close the worker details page.</span></span>
19. <span data-ttu-id="0a830-134">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0a830-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="0a830-135">Määritä työntekijä laiteryhmään.</span><span class="sxs-lookup"><span data-stu-id="0a830-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="0a830-136">Valitse Tuotannonhallinta > Asetukset > Tuotannonohjaus > Konfiguroi työkortti laitteita varten.</span><span class="sxs-lookup"><span data-stu-id="0a830-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="0a830-137">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="0a830-137">Click Add.</span></span>
3. <span data-ttu-id="0a830-138">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="0a830-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="0a830-139">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="0a830-139">Click OK.</span></span>
5. <span data-ttu-id="0a830-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="0a830-140">Click Edit.</span></span>
6. <span data-ttu-id="0a830-141">Voit määrittää Tuotantoyksikkö-kentässä työntekijän oletussuodattimen.</span><span class="sxs-lookup"><span data-stu-id="0a830-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="0a830-142">Tämä varmistaa, että vain valittujen tuotantoyksiköiden tuotantotyöt näytetään, kun työntekijä kirjautuu laitteeseen.</span><span class="sxs-lookup"><span data-stu-id="0a830-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="0a830-143">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="0a830-143">Close the page.</span></span>

