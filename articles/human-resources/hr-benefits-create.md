---
title: Luo uusi etu
description: Tässä tehtävässä näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 7ca390e296b28d1d22fc7bab85bac83fbffcead8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805967"
---
# <a name="create-a-new-benefit"></a><span data-ttu-id="fa091-103">Luo uusi etu</span><span class="sxs-lookup"><span data-stu-id="fa091-103">Create a new benefit</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fa091-104">Tässä tehtävässä näytetään, miten uuden etuuden luomisessa käytettävät etuuselementit luodaan.</span><span class="sxs-lookup"><span data-stu-id="fa091-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="fa091-105">Tämän tehtävän luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="fa091-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="fa091-106">Tämä tehtävä on tarkoitettu etuuspäällikölle.</span><span class="sxs-lookup"><span data-stu-id="fa091-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="fa091-107">Edun elementtien luominen</span><span class="sxs-lookup"><span data-stu-id="fa091-107">Create benefit elements</span></span>
1. <span data-ttu-id="fa091-108">Valitse Henkilöstöhallinto > Edut > Asetukset > Edun elementit.</span><span class="sxs-lookup"><span data-stu-id="fa091-108">Go to Human resources > Benefits > Setup > Benefit elements.</span></span>
2. <span data-ttu-id="fa091-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa091-109">Click New.</span></span>
3. <span data-ttu-id="fa091-110">Syötä Tyyppi-kenttään luotavan edun tyypin nimi.</span><span class="sxs-lookup"><span data-stu-id="fa091-110">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="fa091-111">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa091-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fa091-112">Valitse Samanaikainen rekisteröinti -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fa091-112">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="fa091-113">Voit rajoittaa työntekijöiden mahdollisuutta rekisteröityä useisiin terveydenhoitosuunnitelmiin valitsemalla Yksi rekisteröinti tyyppiä kohti.</span><span class="sxs-lookup"><span data-stu-id="fa091-113">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="fa091-114">Valitse Palkanlaskentaluokka-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fa091-114">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="fa091-115">Valitse Suunnitelmat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="fa091-115">Click the Plans tab.</span></span>
8. <span data-ttu-id="fa091-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa091-116">Click New.</span></span>
9. <span data-ttu-id="fa091-117">Kirjoita arvo Suunnitelma-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa091-117">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="fa091-118">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa091-118">In the Description field, type a value.</span></span>
11. <span data-ttu-id="fa091-119">Anna tai valitse Tyyppi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa091-119">In the Type field, enter or select a value.</span></span>
12. <span data-ttu-id="fa091-120">Valitse Palkanlaskennan vaikutus -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fa091-120">In the Payroll impact field, select an option.</span></span>
13. <span data-ttu-id="fa091-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="fa091-121">Click Save.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="fa091-122">Edun luominen</span><span class="sxs-lookup"><span data-stu-id="fa091-122">Create a benefit</span></span>
1. <span data-ttu-id="fa091-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="fa091-123">Close the page.</span></span>
2. <span data-ttu-id="fa091-124">Siirry kohtaan Henkilöstöhallinto > Edut > Edut.</span><span class="sxs-lookup"><span data-stu-id="fa091-124">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="fa091-125">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="fa091-125">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="fa091-126">Anna tai valitse Suunnitelma-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="fa091-126">In the Plan field, enter or select a value.</span></span>
5. <span data-ttu-id="fa091-127">Syötä tai valitse arvo kentässä Vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="fa091-127">In the Option field, enter or select a value.</span></span>
6. <span data-ttu-id="fa091-128">Syötä päivämäärä ja kellonaika Voimaantulo-kenttään.</span><span class="sxs-lookup"><span data-stu-id="fa091-128">In the Effective field, enter a date and time.</span></span>
7. <span data-ttu-id="fa091-129">Valitse Uusi etu.</span><span class="sxs-lookup"><span data-stu-id="fa091-129">Click Create benefit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]