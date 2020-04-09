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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2df4695b796b4e96e01fe5dac538b344cb76b910
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146718"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="1bb13-103">Ota käyttöön työajanseurantaan perustuva palkanlaskentaprosessi</span><span class="sxs-lookup"><span data-stu-id="1bb13-103">Enable the payroll process for time and attendance</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1bb13-104">Tässä menettelyssä kerrotaan, miten palkanlaskentaprosessi otetaan käyttöön työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="1bb13-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="1bb13-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="1bb13-106">Maksulajin ja liittyvän maksumäärän luominen</span><span class="sxs-lookup"><span data-stu-id="1bb13-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="1bb13-107">Työajan seuranta > Asetukset > Palkanlaskenta > Maksutyypit</span><span class="sxs-lookup"><span data-stu-id="1bb13-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="1bb13-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1bb13-108">Click New.</span></span>
3. <span data-ttu-id="1bb13-109">Kirjoita Maksulaji-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1bb13-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="1bb13-110">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bb13-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1bb13-111">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1bb13-111">Click Save.</span></span>
6. <span data-ttu-id="1bb13-112">Valitse Taksat.</span><span class="sxs-lookup"><span data-stu-id="1bb13-112">Click Rates.</span></span>
    * <span data-ttu-id="1bb13-113">Maksulajien taksat määritetään erillisille ajanjaksoille. Työntekijöille voidaan erillisiä yksilöllisiä taksoja. Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa. Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="1bb13-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="1bb13-114">Taksoja ei aina tarvitse luoda maksulajeihin työajan seurannassa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="1bb13-115">Tiedot voivat jo olla palkkajärjestelmässä, jonka avulla palkat luodaan.</span><span class="sxs-lookup"><span data-stu-id="1bb13-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="1bb13-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1bb13-116">Click New.</span></span>
8. <span data-ttu-id="1bb13-117">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1bb13-118">Syötä Taksa-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="1bb13-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="1bb13-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1bb13-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="1bb13-120">Maksusopimuksen luominen</span><span class="sxs-lookup"><span data-stu-id="1bb13-120">Create a pay agreement</span></span>
1. <span data-ttu-id="1bb13-121">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bb13-121">Close the page.</span></span>
2. <span data-ttu-id="1bb13-122">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bb13-122">Close the page.</span></span>
3. <span data-ttu-id="1bb13-123">Siirry Maksusopimukset-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="1bb13-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="1bb13-124">Työajan seuranta > Asetukset > Maksusopimukset</span><span class="sxs-lookup"><span data-stu-id="1bb13-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="1bb13-125">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1bb13-125">Click New.</span></span>
5. <span data-ttu-id="1bb13-126">Kirjoita Maksusopimus-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="1bb13-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="1bb13-127">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bb13-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="1bb13-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1bb13-128">Click Save.</span></span>
8. <span data-ttu-id="1bb13-129">Valitse Sopimusrivit.</span><span class="sxs-lookup"><span data-stu-id="1bb13-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="1bb13-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1bb13-130">Click New.</span></span>
10. <span data-ttu-id="1bb13-131">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="1bb13-132">Syötä tai valitse arvo Profiilityyppi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bb13-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="1bb13-133">Syötä tai valitse arvo Maksulaji-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bb13-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="1bb13-134">Työajan seurannan työntekijän maksusopimuksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1bb13-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="1bb13-135">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bb13-135">Close the page.</span></span>
2. <span data-ttu-id="1bb13-136">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="1bb13-136">Close the page.</span></span>
3. <span data-ttu-id="1bb13-137">Siirry Aikarekisteröinnin työntekijät -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="1bb13-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="1bb13-138">Työajan seuranta > Asetukset > Aikarekisteröinnin työntekijät</span><span class="sxs-lookup"><span data-stu-id="1bb13-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="1bb13-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="1bb13-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="1bb13-140">Valitse Työsuhde-välilehti.</span><span class="sxs-lookup"><span data-stu-id="1bb13-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="1bb13-141">Laajenna Aikarekisteröinti-osa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="1bb13-142">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="1bb13-142">Click Edit.</span></span>
8. <span data-ttu-id="1bb13-143">Syötä tai valitse arvo Maksusopimus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="1bb13-143">In the Pay agreement field, enter or select a value.</span></span>

