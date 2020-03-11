---
title: Määritä jatkuvuuden aikataulut
description: Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset).
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a438656730863f345080bc99fef24cfff724f528
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022382"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="44b65-103">Määritä jatkuvuuden aikataulut</span><span class="sxs-lookup"><span data-stu-id="44b65-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="44b65-104">Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset).</span><span class="sxs-lookup"><span data-stu-id="44b65-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="44b65-105">Aiheessa käytetään esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="44b65-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="44b65-106">Luo jatkuvuusohjelma</span><span class="sxs-lookup"><span data-stu-id="44b65-106">Create continuity program</span></span>
1. <span data-ttu-id="44b65-107">Siirry kohtaan Retail ja Commerce > Jatkuvuus > Jatkuvuusohjelmat.</span><span class="sxs-lookup"><span data-stu-id="44b65-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="44b65-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="44b65-108">Click New.</span></span>
3. <span data-ttu-id="44b65-109">Kirjoita Aikataulun tunnus -kenttään jatkuvuusaikataulun tunnus.</span><span class="sxs-lookup"><span data-stu-id="44b65-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="44b65-110">Valitse Tilauksen aloitus -kentässä Valitse 'Ensimmäinen tapahtuma'.</span><span class="sxs-lookup"><span data-stu-id="44b65-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="44b65-111">Jos asiakas tekee uuden jatkuvuusohjelman tilauksen, tuotteen toimitukselle on kaksi vaihtoehtoa: 1.</span><span class="sxs-lookup"><span data-stu-id="44b65-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="44b65-112">Ensimmäinen tapahtuma: jatkuvuusohjelman ensimmäinen tuote toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="44b65-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="44b65-113">2.</span><span class="sxs-lookup"><span data-stu-id="44b65-113">2.</span></span> <span data-ttu-id="44b65-114">Nykyinen tapahtuma: nykyinen tuote toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="44b65-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="44b65-115">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="44b65-115">For example.</span></span> <span data-ttu-id="44b65-116">kolme kuukautta ohjelmaa tilanneet asiakkaat saavat ohjelman kolmannen tuotteen.</span><span class="sxs-lookup"><span data-stu-id="44b65-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="44b65-117">Valitse Kyllä, jos haluat kehotteen tilauksen alkamispäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="44b65-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="44b65-118">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="44b65-118">Click Add line.</span></span>
7. <span data-ttu-id="44b65-119">Anna Nimiketunnus-kenttään ensimmäisen tuotteen tunnus (0013).</span><span class="sxs-lookup"><span data-stu-id="44b65-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="44b65-120">Kirjoita "CP".</span><span class="sxs-lookup"><span data-stu-id="44b65-120">Type 'CP'.</span></span>
9. <span data-ttu-id="44b65-121">Anna päivämäärä, jona ensimmäinen tuote on tilattavissa.</span><span class="sxs-lookup"><span data-stu-id="44b65-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="44b65-122">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="44b65-122">Click Add line.</span></span>
11. <span data-ttu-id="44b65-123">Kirjoita Nimiketunnus-kenttään 0014.</span><span class="sxs-lookup"><span data-stu-id="44b65-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="44b65-124">Poista Päivämäärävälin koodi -kentän arvon niin, että kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="44b65-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="44b65-125">Poista päivämääräväli tätä toimintaohjetta varten.</span><span class="sxs-lookup"><span data-stu-id="44b65-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="44b65-126">Päivämäärä määritetään kasvavana ensimmäisen nimikkeen aloituspäivämäärästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="44b65-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="44b65-127">Tähän kenttään syötetään väli, jona tuotteet toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="44b65-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="44b65-128">Anna arvoksi 30.</span><span class="sxs-lookup"><span data-stu-id="44b65-128">Type '30'.</span></span>
    * <span data-ttu-id="44b65-129">Kuukausittaisen ohjelman aikaväliksi täytetään 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="44b65-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="44b65-130">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="44b65-130">Click Add line.</span></span>
15. <span data-ttu-id="44b65-131">Kirjoita Nimiketunnus-kenttään 0015.</span><span class="sxs-lookup"><span data-stu-id="44b65-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="44b65-132">Kirjoita "End".</span><span class="sxs-lookup"><span data-stu-id="44b65-132">Type 'End'.</span></span>
17. <span data-ttu-id="44b65-133">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="44b65-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="44b65-134">Liitä jatkuvuusnimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="44b65-134">Assign to continuity item</span></span>
1. <span data-ttu-id="44b65-135">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="44b65-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="44b65-136">Valitse nimike 0016.</span><span class="sxs-lookup"><span data-stu-id="44b65-136">Select item '0016'.</span></span>
    * <span data-ttu-id="44b65-137">Tässä menettelyssä valitaan nimiketunnus 0016.</span><span class="sxs-lookup"><span data-stu-id="44b65-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="44b65-138">Tavallisesti luotaisiin vapautettu tuote, johon käytetään jatkuvuuden liiketoimintalogiikkaa silloin, kun se lisätään myyntitilaukseen puhelinkeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="44b65-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="44b65-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="44b65-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="44b65-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="44b65-140">Click Edit.</span></span>
5. <span data-ttu-id="44b65-141">Laajenna tai tiivistä Myydä-osa .</span><span class="sxs-lookup"><span data-stu-id="44b65-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="44b65-142">Syötä tähän kenttään jatkuvuusohjelma, jota nimike vastaa.</span><span class="sxs-lookup"><span data-stu-id="44b65-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="44b65-143">Kirjoita aiemmin luotu aikataulun tunnus.</span><span class="sxs-lookup"><span data-stu-id="44b65-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="44b65-144">Kun tämä nimike myydään puhelinkeskuksessa, valitun jatkuvuusohjelman liiketoimintalogiikkaa sovelletaan nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="44b65-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="44b65-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="44b65-145">Click Save.</span></span>
