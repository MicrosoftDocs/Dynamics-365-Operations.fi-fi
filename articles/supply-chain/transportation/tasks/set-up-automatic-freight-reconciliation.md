---
title: Rahdin automaattisen täsmäytyksen määrittäminen
description: Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f11edc15821faad84485d5b81e4a9ded0b7e974
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426859"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="21404-103">Rahdin automaattisen täsmäytyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="21404-103">Set up automatic freight reconciliation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21404-104">Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="21404-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="21404-105">Yleensä tämän prosessin tekee varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="21404-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="21404-106">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="21404-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="21404-107">Määritä rahtilaskun tyyppi</span><span class="sxs-lookup"><span data-stu-id="21404-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="21404-108">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="21404-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="21404-109">Rahtilaskun tyyppi määrittää, miten rahtilaskut ja kuljettajan laskut täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="21404-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="21404-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21404-110">Click New.</span></span>
3. <span data-ttu-id="21404-111">Kirjoita arvo Rahtilaskun tyyppi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="21404-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="21404-112">Kirjoita Laskennan kokoonpano -kenttään Microsoft.Dynamics.Ax.Tms.dll.</span><span class="sxs-lookup"><span data-stu-id="21404-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="21404-113">Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin koodikirjasto.</span><span class="sxs-lookup"><span data-stu-id="21404-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="21404-114">Kirjoita Moduulin luokka -kenttään Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="21404-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="21404-115">Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin luokka.</span><span class="sxs-lookup"><span data-stu-id="21404-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="21404-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21404-116">Click New.</span></span>
7. <span data-ttu-id="21404-117">Valitse kuvaus-kenttään arvo, jonka tulee täsmätä sekä rahti- että kuljettajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="21404-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="21404-118">Valitse Täsmäytys vaaditaan -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="21404-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="21404-119">Jos määrität tämän kentän arvoksi Kyllä, se tarkoittaa, että Kuvaus-kenttään valitun arvon on vastattava sekä rahtikirjaa että kuljettajan laskua.</span><span class="sxs-lookup"><span data-stu-id="21404-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="21404-120">Jos asetat arvoksi Ei, toinen näistä kentistä voi olla tyhjä.</span><span class="sxs-lookup"><span data-stu-id="21404-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="21404-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="21404-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="21404-122">Aseta rahtilaskun määritys</span><span class="sxs-lookup"><span data-stu-id="21404-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="21404-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21404-123">Close the page.</span></span>
2. <span data-ttu-id="21404-124">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppimääritykset.</span><span class="sxs-lookup"><span data-stu-id="21404-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="21404-125">Rahtilaskun tyyppimääritystä käytetään tietyn kuljettajan rahtilaskutyypin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="21404-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="21404-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21404-126">Click New.</span></span>
4. <span data-ttu-id="21404-127">Syötä tai valitse arvo Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="21404-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="21404-128">Syötä tai valitse arvo Lähetyksen rahdinkuljettaja -kentässä.</span><span class="sxs-lookup"><span data-stu-id="21404-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="21404-129">Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="21404-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="21404-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21404-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="21404-131">Aseta päätarkastus</span><span class="sxs-lookup"><span data-stu-id="21404-131">Set up the audit master</span></span>
1. <span data-ttu-id="21404-132">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Päätarkistus.</span><span class="sxs-lookup"><span data-stu-id="21404-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="21404-133">Päätarkistuksessa määritetään automaattisen rahtitäsmäytyksen toleranssitaso.</span><span class="sxs-lookup"><span data-stu-id="21404-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="21404-134">Se määrittää kuinka paljon rahtilasku ja kuljettajan laskun rahasummat voivat poiketa toisistaan, että täsmäytys on edelleen sallittua.</span><span class="sxs-lookup"><span data-stu-id="21404-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="21404-135">Se määrittää myös, miten ristiriidat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="21404-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="21404-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="21404-136">Click New.</span></span>
3. <span data-ttu-id="21404-137">Kirjoita arvo Tarkistuksen päätunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="21404-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="21404-138">Valitse Lähetyksen rahdinkuljettaja -kenttään saman lähetyksen rahdinkuljettaja, jonka valitsit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="21404-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="21404-139">Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="21404-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="21404-140">Laajenna Toleranssi-osa.</span><span class="sxs-lookup"><span data-stu-id="21404-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="21404-141">Syötä Vähimmäistoleranssitaso-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="21404-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="21404-142">Syötä Enimmäistoleranssitaso-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="21404-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="21404-143">Laajenna Tulos-osa.</span><span class="sxs-lookup"><span data-stu-id="21404-143">Expand the Result section.</span></span>
10. <span data-ttu-id="21404-144">Anna tai valitse Liikamaksun syykoodi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="21404-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="21404-145">Jos rahtilaskun ja kuljettajan laskun rahasummat eroavat toisistaan, liika- ja alimaksujen syykoodit määrittävät tilit, joille ero tulisi kirjata, kunhan ero on toleranssitasojen puitteissa.</span><span class="sxs-lookup"><span data-stu-id="21404-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="21404-146">Anna tai valitse Alimaksun syykoodi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="21404-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="21404-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="21404-147">Close the page.</span></span>

