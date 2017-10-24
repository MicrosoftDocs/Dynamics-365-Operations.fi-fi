--- 
title: "Luo tuotenumero esimääritetyille tuotevarianteille"
description: "Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="24356-103">Luo tuotenumero esimääritetyille tuotevarianteille</span><span class="sxs-lookup"><span data-stu-id="24356-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="24356-104">Tässä oppaassa kuvataan, miten tuotenumeroiden nimikkeistö määritetään esimääritetyille tuotevarianteille ja miten se voidaan liittää asianmukaiseen tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="24356-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="24356-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="24356-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="24356-106">Uuden tuotenumeroiden nimikkeistö on määritetty värin ja koon tuotedimensioryhmään.</span><span class="sxs-lookup"><span data-stu-id="24356-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="24356-107">Tuotesuunnittelija tekee yleensä tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="24356-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="24356-108">Tuotenumeroiden nimikkeistön luominen</span><span class="sxs-lookup"><span data-stu-id="24356-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="24356-109">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="24356-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="24356-110">Valitse Tuotenimikkeistö.</span><span class="sxs-lookup"><span data-stu-id="24356-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="24356-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="24356-111">Click New.</span></span>
4. <span data-ttu-id="24356-112">Kirjoita nimikenttään nimikkeistön nimi, jolla kohteena olevan tuotedimensioryhmän tunnistaa, esimerkiksi ColorSize.</span><span class="sxs-lookup"><span data-stu-id="24356-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="24356-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24356-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="24356-114">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="24356-114">Click Add.</span></span>
7. <span data-ttu-id="24356-115">Valitse Päätuotteen numero.</span><span class="sxs-lookup"><span data-stu-id="24356-115">Click Product master number.</span></span>
8. <span data-ttu-id="24356-116">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="24356-116">Click Add.</span></span>
9. <span data-ttu-id="24356-117">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="24356-117">Click Text constant.</span></span>
10. <span data-ttu-id="24356-118">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24356-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="24356-119">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="24356-119">Click Add.</span></span>
12. <span data-ttu-id="24356-120">Valitse Väri.</span><span class="sxs-lookup"><span data-stu-id="24356-120">Click Color.</span></span>
13. <span data-ttu-id="24356-121">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="24356-121">Click Add.</span></span>
14. <span data-ttu-id="24356-122">Valitse Tekstivakio.</span><span class="sxs-lookup"><span data-stu-id="24356-122">Click Text constant.</span></span>
15. <span data-ttu-id="24356-123">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="24356-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="24356-124">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="24356-124">Click Add.</span></span>
17. <span data-ttu-id="24356-125">Valitse Koko.</span><span class="sxs-lookup"><span data-stu-id="24356-125">Click Size.</span></span>
18. <span data-ttu-id="24356-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24356-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="24356-127">Nimikkeistön määrittäminen päätuotteelle</span><span class="sxs-lookup"><span data-stu-id="24356-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="24356-128">Valitse Tuotedimensioryhmät.</span><span class="sxs-lookup"><span data-stu-id="24356-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="24356-129">Valitse SizeCol-tuotedimensioryhmä.</span><span class="sxs-lookup"><span data-stu-id="24356-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="24356-130">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="24356-130">Click Edit.</span></span>
4. <span data-ttu-id="24356-131">Valitse Käytä nimikkeistöä -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="24356-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="24356-132">Syötä tai valitse arvo Tuotevariantin numeron nimikkeistö -kentässä.</span><span class="sxs-lookup"><span data-stu-id="24356-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="24356-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="24356-133">Close the page.</span></span>


