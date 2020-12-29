---
title: Rahdinkuljettajan polttoaineindeksin määrittäminen
description: Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ade30b63454dfd997aa47a62cde21b066140fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/29/2020
ms.locfileid: "4427539"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="66aff-103">Rahdinkuljettajan polttoaineindeksin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="66aff-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="66aff-104">Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.</span><span class="sxs-lookup"><span data-stu-id="66aff-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="66aff-105">Polttoaineindeksialue määrittää, millä alueella polttoaineindeksiä käytetään. Polttoaineindeksi määrittää polttoaineen hinnan tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="66aff-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="66aff-106">Jotta muutos huomioidaan polttoainehinnoissa ajan kuluessa, voit liittää useat polttoaineindeksit rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="66aff-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="66aff-107">Yleensä kuljetuskoordinaattori tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="66aff-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="66aff-108">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="66aff-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="66aff-109">Polttoaineindeksialueen luominen</span><span class="sxs-lookup"><span data-stu-id="66aff-109">Create a fuel index region</span></span>
1. <span data-ttu-id="66aff-110">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksialueet.</span><span class="sxs-lookup"><span data-stu-id="66aff-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="66aff-111">Ensin luodaan erilaisia toiminta-alueita ja lasketaan polttoaineen lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="66aff-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="66aff-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="66aff-112">Click New.</span></span>
3. <span data-ttu-id="66aff-113">Syötä Alue-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="66aff-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="66aff-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="66aff-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="66aff-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="66aff-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="66aff-116">Luo polttoaineindeksi</span><span class="sxs-lookup"><span data-stu-id="66aff-116">Create a fuel index</span></span>
1. <span data-ttu-id="66aff-117">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="66aff-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="66aff-118">Määritetyille alueille on syötettävä nykyiset polttoainemaksut.</span><span class="sxs-lookup"><span data-stu-id="66aff-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="66aff-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="66aff-119">Click New.</span></span>
3. <span data-ttu-id="66aff-120">Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="66aff-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="66aff-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="66aff-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="66aff-122">Syötä Litrahinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66aff-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="66aff-123">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="66aff-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="66aff-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="66aff-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="66aff-125">Rahdinkuljettajan polttoaineindeksin luominen</span><span class="sxs-lookup"><span data-stu-id="66aff-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="66aff-126">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Rahdinkuljettajan polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="66aff-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="66aff-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="66aff-127">Click New.</span></span>
3. <span data-ttu-id="66aff-128">Kirjoita Rahdinkuljettajan polttoaineindeksi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="66aff-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="66aff-129">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="66aff-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="66aff-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="66aff-130">Click New.</span></span>
6. <span data-ttu-id="66aff-131">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="66aff-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="66aff-132">Syötä Litrahinta alkaen -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66aff-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="66aff-133">Tässä esimerkissä Litrahinta alkaen -kenttään syötetään arvo 1,95.</span><span class="sxs-lookup"><span data-stu-id="66aff-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="66aff-134">Litrahinta enintään -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66aff-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="66aff-135">Tässä esimerkissä Litrahinta enintään -kenttään syötetään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="66aff-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="66aff-136">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="66aff-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="66aff-137">Tässä esimerkissä prosentiksi syötetään 3.</span><span class="sxs-lookup"><span data-stu-id="66aff-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="66aff-138">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="66aff-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="66aff-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="66aff-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="66aff-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="66aff-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="66aff-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="66aff-141">Click Save.</span></span>

