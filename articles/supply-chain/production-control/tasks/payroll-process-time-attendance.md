---
title: Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi
description: Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "311102"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="55888-103">Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi</span><span class="sxs-lookup"><span data-stu-id="55888-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55888-104">Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="55888-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="55888-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="55888-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="55888-106">Maksulajin ja liittyvän maksumäärän luominen</span><span class="sxs-lookup"><span data-stu-id="55888-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="55888-107">Työajan seuranta > Asetukset > Palkanlaskenta > Maksutyypit</span><span class="sxs-lookup"><span data-stu-id="55888-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="55888-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55888-108">Click New.</span></span>
3. <span data-ttu-id="55888-109">Kirjoita Maksulaji-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="55888-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="55888-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55888-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="55888-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="55888-111">Click Save.</span></span>
6. <span data-ttu-id="55888-112">Valitse Taksat.</span><span class="sxs-lookup"><span data-stu-id="55888-112">Click Rates.</span></span>
    * <span data-ttu-id="55888-113">Maksulajien taksat määritetään erillisille ajanjaksoille. Työntekijöille voidaan erillisiä yksilöllisiä taksoja. Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa. Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="55888-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="55888-114">Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="55888-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="55888-115">Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="55888-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="55888-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55888-116">Click New.</span></span>
8. <span data-ttu-id="55888-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="55888-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="55888-118">Syötä Taksa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="55888-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="55888-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="55888-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="55888-120">Maksusopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="55888-120">Create a pay agreement</span></span>
1. <span data-ttu-id="55888-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="55888-121">Close the page.</span></span>
2. <span data-ttu-id="55888-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="55888-122">Close the page.</span></span>
3. <span data-ttu-id="55888-123">Siirry Maksusopimukset-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="55888-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="55888-124">Työajan seuranta > Asetukset > Maksusopimukset</span><span class="sxs-lookup"><span data-stu-id="55888-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="55888-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55888-125">Click New.</span></span>
5. <span data-ttu-id="55888-126">Kirjoita Maksusopimus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="55888-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="55888-127">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55888-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="55888-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="55888-128">Click Save.</span></span>
8. <span data-ttu-id="55888-129">Valitse Sopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="55888-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="55888-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="55888-130">Click New.</span></span>
10. <span data-ttu-id="55888-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="55888-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="55888-132">Syötä tai valitse arvo Profiilityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55888-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="55888-133">Syötä tai valitse arvo Maksulaji-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55888-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="55888-134">Työajan seurannan työntekijän maksusopimuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="55888-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="55888-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="55888-135">Close the page.</span></span>
2. <span data-ttu-id="55888-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="55888-136">Close the page.</span></span>
3. <span data-ttu-id="55888-137">Siirry Aikarekisteröinnin työntekijät -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="55888-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="55888-138">Työajan seuranta > Asetukset > Aikarekisteröinnin työntekijät</span><span class="sxs-lookup"><span data-stu-id="55888-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="55888-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="55888-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="55888-140">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="55888-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="55888-141">Laajenna Aikarekisteröinti-osa.</span><span class="sxs-lookup"><span data-stu-id="55888-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="55888-142">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="55888-142">Click Edit.</span></span>
8. <span data-ttu-id="55888-143">Syötä tai valitse arvo Maksusopimus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="55888-143">In the Pay agreement field, enter or select a value.</span></span>

