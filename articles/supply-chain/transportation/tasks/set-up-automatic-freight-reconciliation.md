---
title: Rahdin automaattisen täsmäytyksen määrittäminen
description: Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään.
author: ShylaThompson
manager: AnnBe
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7772ad779495b36941a3dc86cc456d80a964467
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562020"
---
# <a name="set-up-automatic-freight-reconciliation"></a><span data-ttu-id="f2b40-103">Rahdin automaattisen täsmäytyksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="f2b40-103">Set up automatic freight reconciliation</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2b40-104">Tässä menettelyssä kuvataan, miten automaattisen rahdintäsmäytyksen tiedot määritetään.</span><span class="sxs-lookup"><span data-stu-id="f2b40-104">This procedure shows how to set up data for automatic freight reconciliation.</span></span> <span data-ttu-id="f2b40-105">Yleensä tämän prosessin tekee varastopäällikkö.</span><span class="sxs-lookup"><span data-stu-id="f2b40-105">This is typically done by a warehouse manager.</span></span> <span data-ttu-id="f2b40-106">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="f2b40-106">You can use this procedure in demo data company USMF.</span></span>


## <a name="set-up-the-freight-bill-type"></a><span data-ttu-id="f2b40-107">Määritä rahtilaskun tyyppi</span><span class="sxs-lookup"><span data-stu-id="f2b40-107">Set up the freight bill type</span></span>
1. <span data-ttu-id="f2b40-108">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-108">Go to Transportation management > Setup > Freight reconciliation > Freight bill type.</span></span>
    * <span data-ttu-id="f2b40-109">Rahtilaskun tyyppi määrittää, miten rahtilaskut ja kuljettajan laskut täsmäytetään.</span><span class="sxs-lookup"><span data-stu-id="f2b40-109">The freight bill type defines how freight bills and carrier invoices  should be matched.</span></span>  
2. <span data-ttu-id="f2b40-110">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-110">Click New.</span></span>
3. <span data-ttu-id="f2b40-111">Kirjoita arvo Rahtilaskun tyyppi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2b40-111">In the Freight bill type field, type a value.</span></span>
4. <span data-ttu-id="f2b40-112">Kirjoita Laskennan kokoonpano -kenttään Microsoft.Dynamics.Ax.Tms.dll.</span><span class="sxs-lookup"><span data-stu-id="f2b40-112">In the Engine assembly field, type 'Microsoft.Dynamics.Ax.Tms.dll'.</span></span>
    * <span data-ttu-id="f2b40-113">Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin koodikirjasto.</span><span class="sxs-lookup"><span data-stu-id="f2b40-113">This is the standard Transportation management matching engine code library.</span></span>  
5. <span data-ttu-id="f2b40-114">Kirjoita Moduulin luokka -kenttään Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer.</span><span class="sxs-lookup"><span data-stu-id="f2b40-114">In the Engine class field, type 'Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer'.</span></span>
    * <span data-ttu-id="f2b40-115">Tämä on standardi Kuljetuksenhallinnan kohdistusmoduulin luokka.</span><span class="sxs-lookup"><span data-stu-id="f2b40-115">This is the standard Transportation management matching engine class.</span></span>  
6. <span data-ttu-id="f2b40-116">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-116">Click New.</span></span>
7. <span data-ttu-id="f2b40-117">Valitse kuvaus-kenttään arvo, jonka tulee täsmätä sekä rahti- että kuljettajan laskulla.</span><span class="sxs-lookup"><span data-stu-id="f2b40-117">In the Description field, choose the value that should match on the freight bill and the carrier invoice.</span></span>  
8. <span data-ttu-id="f2b40-118">Valitse Täsmäytys vaaditaan -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="f2b40-118">In the Match required field, select 'Yes'.</span></span>
    * <span data-ttu-id="f2b40-119">Jos määrität tämän kentän arvoksi Kyllä, se tarkoittaa, että Kuvaus-kenttään valitun arvon on vastattava sekä rahtikirjaa että kuljettajan laskua.</span><span class="sxs-lookup"><span data-stu-id="f2b40-119">If you set this field to Yes this means that the value selected in the Description field needs to match on both the freight bill and the carrier invoice.</span></span> <span data-ttu-id="f2b40-120">Jos asetat arvoksi Ei, toinen näistä kentistä voi olla tyhjä.</span><span class="sxs-lookup"><span data-stu-id="f2b40-120">If you set it to No, the field can be blank on one of these.</span></span>  
9. <span data-ttu-id="f2b40-121">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f2b40-121">Click Save.</span></span>

## <a name="set-up-the-freight-bill-type-assignment"></a><span data-ttu-id="f2b40-122">Aseta rahtilaskun määritys</span><span class="sxs-lookup"><span data-stu-id="f2b40-122">Set up the freight bill type assignment</span></span>
1. <span data-ttu-id="f2b40-123">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2b40-123">Close the page.</span></span>
2. <span data-ttu-id="f2b40-124">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Rahtilaskun tyyppimääritykset.</span><span class="sxs-lookup"><span data-stu-id="f2b40-124">Go to Transportation management > Setup > Freight reconciliation > Freight bill type assignments.</span></span>
    * <span data-ttu-id="f2b40-125">Rahtilaskun tyyppimääritystä käytetään tietyn kuljettajan rahtilaskutyypin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="f2b40-125">The freight bill type assignment is used to specify which freight bill type is used for a particular carrier.</span></span>   
3. <span data-ttu-id="f2b40-126">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-126">Click New.</span></span>
4. <span data-ttu-id="f2b40-127">Syötä tai valitse arvo Menetelmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f2b40-127">In the Mode field, enter or select a value.</span></span>
5. <span data-ttu-id="f2b40-128">Syötä tai valitse arvo Lähetyksen rahdinkuljettaja -kentässä.</span><span class="sxs-lookup"><span data-stu-id="f2b40-128">In the Shipping carrier field, enter or select a value.</span></span>
6. <span data-ttu-id="f2b40-129">Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-129">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
7. <span data-ttu-id="f2b40-130">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2b40-130">Close the page.</span></span>

## <a name="set-up-the-audit-master"></a><span data-ttu-id="f2b40-131">Aseta päätarkastus</span><span class="sxs-lookup"><span data-stu-id="f2b40-131">Set up the audit master</span></span>
1. <span data-ttu-id="f2b40-132">Siirry kohtaan Kuljetustenhallinta > Asetukset > Rahdin täsmäytys > Päätarkistus.</span><span class="sxs-lookup"><span data-stu-id="f2b40-132">Go to Transportation management > Setup > Freight reconciliation > Audit master.</span></span>
    * <span data-ttu-id="f2b40-133">Päätarkistuksessa määritetään automaattisen rahtitäsmäytyksen toleranssitaso.</span><span class="sxs-lookup"><span data-stu-id="f2b40-133">The audit master defines the tolerance limits for automatic freight reconciliation.</span></span> <span data-ttu-id="f2b40-134">Se määrittää kuinka paljon rahtilasku ja kuljettajan laskun rahasummat voivat poiketa toisistaan, että täsmäytys on edelleen sallittua.</span><span class="sxs-lookup"><span data-stu-id="f2b40-134">It specifies by how much the monetary amounts on the freight bill and the carrier invoice can differ and still allow reconciliation to occur.</span></span> <span data-ttu-id="f2b40-135">Se määrittää myös, miten ristiriidat käsitellään.</span><span class="sxs-lookup"><span data-stu-id="f2b40-135">It also defines how to handle discrepancies.</span></span>  
2. <span data-ttu-id="f2b40-136">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-136">Click New.</span></span>
3. <span data-ttu-id="f2b40-137">Kirjoita arvo Tarkistuksen päätunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f2b40-137">In the Audit master ID field, type a value.</span></span>
4. <span data-ttu-id="f2b40-138">Valitse Lähetyksen rahdinkuljettaja -kenttään saman lähetyksen rahdinkuljettaja, jonka valitsit aikaisemmin.</span><span class="sxs-lookup"><span data-stu-id="f2b40-138">In the Shipping carrier  field, select the same shipping carrier as you did earlier.</span></span>
5. <span data-ttu-id="f2b40-139">Valitse Rahtilaskun tyyppi -kentässä aiemmin luomasi rahtilaskun tyyppi.</span><span class="sxs-lookup"><span data-stu-id="f2b40-139">In the Freight bill type field, select the freight bill type that you created earlier.</span></span>
6. <span data-ttu-id="f2b40-140">Laajenna Toleranssi-osa.</span><span class="sxs-lookup"><span data-stu-id="f2b40-140">Expand the Tolerance section.</span></span>
7. <span data-ttu-id="f2b40-141">Syötä Vähimmäistoleranssitaso-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f2b40-141">In the Minimum tolerance level field, enter a number.</span></span>
8. <span data-ttu-id="f2b40-142">Syötä Enimmäistoleranssitaso-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="f2b40-142">In the Maximum tolerance level field, enter a number.</span></span>
9. <span data-ttu-id="f2b40-143">Laajenna Tulos-osa.</span><span class="sxs-lookup"><span data-stu-id="f2b40-143">Expand the Result section.</span></span>
10. <span data-ttu-id="f2b40-144">Anna tai valitse Liikamaksun syykoodi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f2b40-144">In the Overpayment reason code field, enter or select a value.</span></span>
    * <span data-ttu-id="f2b40-145">Jos rahtilaskun ja kuljettajan laskun rahasummat eroavat toisistaan, liika- ja alimaksujen syykoodit määrittävät tilit, joille ero tulisi kirjata, kunhan ero on toleranssitasojen puitteissa.</span><span class="sxs-lookup"><span data-stu-id="f2b40-145">If the monetary amounts differ on the freight bill and the carrier invoice, the overpayment and underpayment reason codes specify the accounts that the difference should be registered on, as long as the difference is within the tolerance levels.</span></span>  
11. <span data-ttu-id="f2b40-146">Anna tai valitse Alimaksun syykoodi -kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="f2b40-146">In the Underpayment reason code field, enter or select a value.</span></span>
12. <span data-ttu-id="f2b40-147">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="f2b40-147">Close the page.</span></span>

