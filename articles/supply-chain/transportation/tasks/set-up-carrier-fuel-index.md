---
title: Rahdinkuljettajan polttoaineindeksin määrittäminen
description: Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e972f2ba8211c47b11a4b83dac9ff60f813b1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837577"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="28210-103">Rahdinkuljettajan polttoaineindeksin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="28210-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28210-104">Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.</span><span class="sxs-lookup"><span data-stu-id="28210-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="28210-105">Polttoaineindeksialue määrittää, millä alueella polttoaineindeksiä käytetään. Polttoaineindeksi määrittää polttoaineen hinnan tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="28210-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="28210-106">Jotta muutos huomioidaan polttoainehinnoissa ajan kuluessa, voit liittää useat polttoaineindeksit rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="28210-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="28210-107">Yleensä kuljetuskoordinaattori tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="28210-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="28210-108">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="28210-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="28210-109">Polttoaineindeksialueen luominen</span><span class="sxs-lookup"><span data-stu-id="28210-109">Create a fuel index region</span></span>
1. <span data-ttu-id="28210-110">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksialueet.</span><span class="sxs-lookup"><span data-stu-id="28210-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="28210-111">Ensin luodaan erilaisia toiminta-alueita ja lasketaan polttoaineen lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="28210-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="28210-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="28210-112">Click New.</span></span>
3. <span data-ttu-id="28210-113">Syötä Alue-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="28210-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="28210-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="28210-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="28210-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="28210-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="28210-116">Luo polttoaineindeksi</span><span class="sxs-lookup"><span data-stu-id="28210-116">Create a fuel index</span></span>
1. <span data-ttu-id="28210-117">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="28210-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="28210-118">Määritetyille alueille on syötettävä nykyiset polttoainemaksut.</span><span class="sxs-lookup"><span data-stu-id="28210-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="28210-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="28210-119">Click New.</span></span>
3. <span data-ttu-id="28210-120">Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="28210-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="28210-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="28210-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="28210-122">Syötä Litrahinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="28210-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="28210-123">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="28210-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="28210-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="28210-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="28210-125">Rahdinkuljettajan polttoaineindeksin luominen</span><span class="sxs-lookup"><span data-stu-id="28210-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="28210-126">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Rahdinkuljettajan polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="28210-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="28210-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="28210-127">Click New.</span></span>
3. <span data-ttu-id="28210-128">Kirjoita Rahdinkuljettajan polttoaineindeksi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="28210-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="28210-129">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="28210-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="28210-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="28210-130">Click New.</span></span>
6. <span data-ttu-id="28210-131">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="28210-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="28210-132">Syötä Litrahinta alkaen -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="28210-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="28210-133">Tässä esimerkissä Litrahinta alkaen -kenttään syötetään arvo 1,95.</span><span class="sxs-lookup"><span data-stu-id="28210-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="28210-134">Litrahinta enintään -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="28210-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="28210-135">Tässä esimerkissä Litrahinta enintään -kenttään syötetään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="28210-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="28210-136">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="28210-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="28210-137">Tässä esimerkissä prosentiksi syötetään 3.</span><span class="sxs-lookup"><span data-stu-id="28210-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="28210-138">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="28210-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="28210-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="28210-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="28210-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="28210-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="28210-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="28210-141">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]