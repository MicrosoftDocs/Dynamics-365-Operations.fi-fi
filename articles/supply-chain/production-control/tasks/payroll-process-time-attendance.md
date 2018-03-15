---
title: "Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi"
description: "Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: dadf0e87eac8522f61bb094c146e37f46a21fc09
ms.openlocfilehash: 16d8fc2120dfb7b356b238957019a29d05963f9a
ms.contentlocale: fi-fi
ms.lasthandoff: 02/06/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="90f16-103">Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi</span><span class="sxs-lookup"><span data-stu-id="90f16-103">Enable the payroll process for time and attendance</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90f16-104">Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="90f16-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="90f16-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="90f16-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="90f16-106">Maksulajin ja liittyvän maksumäärän luominen</span><span class="sxs-lookup"><span data-stu-id="90f16-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="90f16-107">Työajan seuranta > Asetukset > Palkanlaskenta > Maksutyypit</span><span class="sxs-lookup"><span data-stu-id="90f16-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="90f16-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="90f16-108">Click New.</span></span>
3. <span data-ttu-id="90f16-109">Kirjoita Maksulaji-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="90f16-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="90f16-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="90f16-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="90f16-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="90f16-111">Click Save.</span></span>
6. <span data-ttu-id="90f16-112">Valitse Taksat.</span><span class="sxs-lookup"><span data-stu-id="90f16-112">Click Rates.</span></span>
    * <span data-ttu-id="90f16-113">Maksulajien taksat määritetään erillisille ajanjaksoille. Työntekijöille voidaan erillisiä yksilöllisiä taksoja. Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa. Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="90f16-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="90f16-114">Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="90f16-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="90f16-115">Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="90f16-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="90f16-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="90f16-116">Click New.</span></span>
8. <span data-ttu-id="90f16-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="90f16-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="90f16-118">Syötä Taksa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="90f16-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="90f16-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="90f16-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="90f16-120">Maksusopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="90f16-120">Create a pay agreement</span></span>
1. <span data-ttu-id="90f16-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="90f16-121">Close the page.</span></span>
2. <span data-ttu-id="90f16-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="90f16-122">Close the page.</span></span>
3. <span data-ttu-id="90f16-123">Siirry Maksusopimukset-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="90f16-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="90f16-124">Työajan seuranta > Asetukset > Maksusopimukset</span><span class="sxs-lookup"><span data-stu-id="90f16-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="90f16-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="90f16-125">Click New.</span></span>
5. <span data-ttu-id="90f16-126">Kirjoita Maksusopimus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="90f16-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="90f16-127">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="90f16-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="90f16-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="90f16-128">Click Save.</span></span>
8. <span data-ttu-id="90f16-129">Valitse Sopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="90f16-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="90f16-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="90f16-130">Click New.</span></span>
10. <span data-ttu-id="90f16-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="90f16-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="90f16-132">Syötä tai valitse arvo Profiilityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="90f16-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="90f16-133">Syötä tai valitse arvo Maksulaji-kenttään.</span><span class="sxs-lookup"><span data-stu-id="90f16-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="90f16-134">Työajan seurannan työntekijän maksusopimuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="90f16-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="90f16-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="90f16-135">Close the page.</span></span>
2. <span data-ttu-id="90f16-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="90f16-136">Close the page.</span></span>
3. <span data-ttu-id="90f16-137">Siirry Aikarekisteröinnin työntekijät -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="90f16-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="90f16-138">Työajan seuranta > Asetukset > Aikarekisteröinnin työntekijät</span><span class="sxs-lookup"><span data-stu-id="90f16-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="90f16-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="90f16-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="90f16-140">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="90f16-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="90f16-141">Laajenna Aikarekisteröinti-osa.</span><span class="sxs-lookup"><span data-stu-id="90f16-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="90f16-142">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="90f16-142">Click Edit.</span></span>
8. <span data-ttu-id="90f16-143">Syötä tai valitse arvo Maksusopimus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="90f16-143">In the Pay agreement field, enter or select a value.</span></span>

