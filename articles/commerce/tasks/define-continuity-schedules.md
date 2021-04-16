---
title: Määritä jatkuvuuden aikataulut
description: Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset).
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8414377ddec0e001f003f842866725eb58bd75a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791604"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="10b38-103">Määritä jatkuvuuden aikataulut</span><span class="sxs-lookup"><span data-stu-id="10b38-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10b38-104">Tässä ohjeaiheessa neuvotaan jatkuvuusohjelman määrittäminen (toiselta nimeltään toistuvat tilaukset).</span><span class="sxs-lookup"><span data-stu-id="10b38-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="10b38-105">Aiheessa käytetään esittelytietojen USRT-yritystä.</span><span class="sxs-lookup"><span data-stu-id="10b38-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="10b38-106">Luo jatkuvuusohjelma</span><span class="sxs-lookup"><span data-stu-id="10b38-106">Create continuity program</span></span>
1. <span data-ttu-id="10b38-107">Siirry kohtaan Retail ja Commerce > Jatkuvuus > Jatkuvuusohjelmat.</span><span class="sxs-lookup"><span data-stu-id="10b38-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="10b38-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="10b38-108">Click New.</span></span>
3. <span data-ttu-id="10b38-109">Kirjoita Aikataulun tunnus -kenttään jatkuvuusaikataulun tunnus.</span><span class="sxs-lookup"><span data-stu-id="10b38-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="10b38-110">Valitse Tilauksen aloitus -kentässä Valitse 'Ensimmäinen tapahtuma'.</span><span class="sxs-lookup"><span data-stu-id="10b38-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="10b38-111">Jos asiakas tekee uuden jatkuvuusohjelman tilauksen, tuotteen toimitukselle on kaksi vaihtoehtoa: 1.</span><span class="sxs-lookup"><span data-stu-id="10b38-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="10b38-112">Ensimmäinen tapahtuma: jatkuvuusohjelman ensimmäinen tuote toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="10b38-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="10b38-113">2.</span><span class="sxs-lookup"><span data-stu-id="10b38-113">2.</span></span> <span data-ttu-id="10b38-114">Nykyinen tapahtuma: nykyinen tuote toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="10b38-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="10b38-115">Esimerkki:</span><span class="sxs-lookup"><span data-stu-id="10b38-115">For example.</span></span> <span data-ttu-id="10b38-116">kolme kuukautta ohjelmaa tilanneet asiakkaat saavat ohjelman kolmannen tuotteen.</span><span class="sxs-lookup"><span data-stu-id="10b38-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="10b38-117">Valitse Kyllä, jos haluat kehotteen tilauksen alkamispäivämäärästä.</span><span class="sxs-lookup"><span data-stu-id="10b38-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="10b38-118">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="10b38-118">Click Add line.</span></span>
7. <span data-ttu-id="10b38-119">Anna Nimiketunnus-kenttään ensimmäisen tuotteen tunnus (0013).</span><span class="sxs-lookup"><span data-stu-id="10b38-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="10b38-120">Kirjoita "CP".</span><span class="sxs-lookup"><span data-stu-id="10b38-120">Type 'CP'.</span></span>
9. <span data-ttu-id="10b38-121">Anna päivämäärä, jona ensimmäinen tuote on tilattavissa.</span><span class="sxs-lookup"><span data-stu-id="10b38-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="10b38-122">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="10b38-122">Click Add line.</span></span>
11. <span data-ttu-id="10b38-123">Kirjoita Nimiketunnus-kenttään 0014.</span><span class="sxs-lookup"><span data-stu-id="10b38-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="10b38-124">Poista Päivämäärävälin koodi -kentän arvon niin, että kenttä on tyhjä.</span><span class="sxs-lookup"><span data-stu-id="10b38-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="10b38-125">Poista päivämääräväli tätä toimintaohjetta varten.</span><span class="sxs-lookup"><span data-stu-id="10b38-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="10b38-126">Päivämäärä määritetään kasvavana ensimmäisen nimikkeen aloituspäivämäärästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="10b38-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="10b38-127">Tähän kenttään syötetään väli, jona tuotteet toimitetaan.</span><span class="sxs-lookup"><span data-stu-id="10b38-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="10b38-128">Anna arvoksi 30.</span><span class="sxs-lookup"><span data-stu-id="10b38-128">Type '30'.</span></span>
    * <span data-ttu-id="10b38-129">Kuukausittaisen ohjelman aikaväliksi täytetään 30 päivää.</span><span class="sxs-lookup"><span data-stu-id="10b38-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="10b38-130">Valitse Lisää rivi.</span><span class="sxs-lookup"><span data-stu-id="10b38-130">Click Add line.</span></span>
15. <span data-ttu-id="10b38-131">Kirjoita Nimiketunnus-kenttään 0015.</span><span class="sxs-lookup"><span data-stu-id="10b38-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="10b38-132">Kirjoita "End".</span><span class="sxs-lookup"><span data-stu-id="10b38-132">Type 'End'.</span></span>
17. <span data-ttu-id="10b38-133">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="10b38-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="10b38-134">Liitä jatkuvuusnimikkeeseen</span><span class="sxs-lookup"><span data-stu-id="10b38-134">Assign to continuity item</span></span>
1. <span data-ttu-id="10b38-135">Mene Tuotetietojen hallinta > Tuotteet > Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="10b38-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="10b38-136">Valitse nimike 0016.</span><span class="sxs-lookup"><span data-stu-id="10b38-136">Select item '0016'.</span></span>
    * <span data-ttu-id="10b38-137">Tässä menettelyssä valitaan nimiketunnus 0016.</span><span class="sxs-lookup"><span data-stu-id="10b38-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="10b38-138">Tavallisesti luotaisiin vapautettu tuote, johon käytetään jatkuvuuden liiketoimintalogiikkaa silloin, kun se lisätään myyntitilaukseen puhelinkeskuksesta.</span><span class="sxs-lookup"><span data-stu-id="10b38-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="10b38-139">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="10b38-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="10b38-140">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="10b38-140">Click Edit.</span></span>
5. <span data-ttu-id="10b38-141">Laajenna tai tiivistä Myydä-osa .</span><span class="sxs-lookup"><span data-stu-id="10b38-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="10b38-142">Syötä tähän kenttään jatkuvuusohjelma, jota nimike vastaa.</span><span class="sxs-lookup"><span data-stu-id="10b38-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="10b38-143">Kirjoita aiemmin luotu aikataulun tunnus.</span><span class="sxs-lookup"><span data-stu-id="10b38-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="10b38-144">Kun tämä nimike myydään puhelinkeskuksessa, valitun jatkuvuusohjelman liiketoimintalogiikkaa sovelletaan nimikkeeseen.</span><span class="sxs-lookup"><span data-stu-id="10b38-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="10b38-145">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="10b38-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]