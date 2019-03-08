---
title: Mittayksikön hallinta
description: Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3e208b7f1faab77f2b97ff7b440a228656684fca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "358919"
---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="29fb4-103">Mittayksikön hallinta</span><span class="sxs-lookup"><span data-stu-id="29fb4-103">Manage unit of measure</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29fb4-104">Tässä menettelyssä kerrotaan, miten mittayksikkö määritetään, miten yksikkö ja sen kuvaukset käännetään ja miten liittyvien yksiköiden muunnossäännöt määritetään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="29fb4-105">Voit käydä tämän menettelyn läpi esittelytietojen avulla tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="29fb4-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="29fb4-106">Siirry Vapautetun tuotteen ylläpito -kohtaan.</span><span class="sxs-lookup"><span data-stu-id="29fb4-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="29fb4-107">Valitse Yksiköt.</span><span class="sxs-lookup"><span data-stu-id="29fb4-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="29fb4-108">Mittayksikön luominen</span><span class="sxs-lookup"><span data-stu-id="29fb4-108">Create a unit of measure</span></span>
1. <span data-ttu-id="29fb4-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="29fb4-109">Click New.</span></span>
2. <span data-ttu-id="29fb4-110">Kirjoita arvo Yksikkö-kenttään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="29fb4-111">Syötä mittayksikköön viitatessa käytettävä tunnus tai symboli.</span><span class="sxs-lookup"><span data-stu-id="29fb4-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="29fb4-112">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="29fb4-113">Syötä mittayksikölle kuvaava nimi järjestelmän kielellä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="29fb4-114">Valitse Yksikköluokka-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="29fb4-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="29fb4-115">Yksikköluokka määrittää, mihin loogiseen ryhmittelyyn, kuten alue, paino tai määrä, mittayksikkö kuuluu.</span><span class="sxs-lookup"><span data-stu-id="29fb4-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="29fb4-116">Syötä Desimaalitarkkuus-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="29fb4-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="29fb4-117">Määritä, miten paljon mittayksikön desimaaleja pyöristetään laskelman valmistuessa.</span><span class="sxs-lookup"><span data-stu-id="29fb4-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="29fb4-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="29fb4-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="29fb4-119">Yksikkökäännösten määrittäminen</span><span class="sxs-lookup"><span data-stu-id="29fb4-119">Define unit translations</span></span>
1. <span data-ttu-id="29fb4-120">Valitse Yksikön tekstit.</span><span class="sxs-lookup"><span data-stu-id="29fb4-120">Click Unit texts.</span></span>
2. <span data-ttu-id="29fb4-121">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="29fb4-121">Click New.</span></span>
    * <span data-ttu-id="29fb4-122">Käytä yksikön tekstiä, kun luot mittayksikköä kuvaavan tunnuksen tai symbolin käännöksen. Tätä käytetään asiakas- tai toimittajakohtaisten kielten ulkoisissa asiakirjoissa.</span><span class="sxs-lookup"><span data-stu-id="29fb4-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="29fb4-123">Syötä tai valitse arvo Kieli-kentässä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="29fb4-124">Kirjoita arvo Teksti-kenttään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="29fb4-125">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="29fb4-125">Click Save.</span></span>
6. <span data-ttu-id="29fb4-126">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="29fb4-126">Close the page.</span></span>
7. <span data-ttu-id="29fb4-127">Valitse Käännetyt yksiköiden kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="29fb4-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="29fb4-128">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="29fb4-128">Click New.</span></span>
    * <span data-ttu-id="29fb4-129">Määritä mittayksikön kielikohtaiset kuvaukset.</span><span class="sxs-lookup"><span data-stu-id="29fb4-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="29fb4-130">Syötä tai valitse arvo Kieli-kentässä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="29fb4-131">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="29fb4-132">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="29fb4-132">Click Save.</span></span>
12. <span data-ttu-id="29fb4-133">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="29fb4-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="29fb4-134">Yksikön muunnössääntöjen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="29fb4-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="29fb4-135">Valitse Yksikön muunnokset.</span><span class="sxs-lookup"><span data-stu-id="29fb4-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="29fb4-136">Määritä mittayksikön muuntamisen säännöt valitussa yksikköluokassa.</span><span class="sxs-lookup"><span data-stu-id="29fb4-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="29fb4-137">Avaa valintaikkuna valitsemalla Uusi.</span><span class="sxs-lookup"><span data-stu-id="29fb4-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="29fb4-138">Syötä Kerroin-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="29fb4-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="29fb4-139">Muuntokerroin Yksiköstä- ja Yksikköön-kohdan välillä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="29fb4-140">Esimerkiksi senttimetrien muuntokerroin metreiksi on 100, koska metri sisältää 100 senttimetriä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="29fb4-141">Syötä tai valitse Yksikköön-kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="29fb4-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="29fb4-142">Valitse vaihtoehto Pyöristys-kentässä.</span><span class="sxs-lookup"><span data-stu-id="29fb4-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="29fb4-143">Määritä, miten muunnettu arvo pyöristetään.</span><span class="sxs-lookup"><span data-stu-id="29fb4-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="29fb4-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="29fb4-144">Click OK.</span></span>
7. <span data-ttu-id="29fb4-145">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="29fb4-145">Close the page.</span></span>

