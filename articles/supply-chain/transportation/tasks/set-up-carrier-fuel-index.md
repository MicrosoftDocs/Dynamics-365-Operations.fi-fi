--- 
title: "Rahdinkuljettajan polttoaineindeksin määrittäminen"
description: "Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3a6a02c2eca3cecc8b7519a5951a958aa5bc637b
ms.contentlocale: fi-fi
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="5d26e-103">Rahdinkuljettajan polttoaineindeksin määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5d26e-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d26e-104">Tässä ohjauksessa kerrotaan, miten polttoaineindeksialue, polttoaineindeksi ja rahdinkuljettajan polttoaineindeksi luodaan.</span><span class="sxs-lookup"><span data-stu-id="5d26e-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="5d26e-105">Polttoaineindeksialue määrittää, millä alueella polttoaineindeksiä käytetään. Polttoaineindeksi määrittää polttoaineen hinnan tiettynä aikana.</span><span class="sxs-lookup"><span data-stu-id="5d26e-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="5d26e-106">Jotta muutos huomioidaan polttoainehinnoissa ajan kuluessa, voit liittää useat polttoaineindeksit rahdinkuljettajaan.</span><span class="sxs-lookup"><span data-stu-id="5d26e-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="5d26e-107">Yleensä kuljetuskoordinaattori tekee nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="5d26e-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="5d26e-108">Voit käyttää tätä menettelyä USMF-demoyrityksen tiedoilla tai omilla tiedoillasi.</span><span class="sxs-lookup"><span data-stu-id="5d26e-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="5d26e-109">Polttoaineindeksialueen luominen</span><span class="sxs-lookup"><span data-stu-id="5d26e-109">Create a fuel index region</span></span>
1. <span data-ttu-id="5d26e-110">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksialueet.</span><span class="sxs-lookup"><span data-stu-id="5d26e-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="5d26e-111">Ensin luodaan erilaisia toiminta-alueita ja lasketaan polttoaineen lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="5d26e-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="5d26e-112">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5d26e-112">Click New.</span></span>
3. <span data-ttu-id="5d26e-113">Syötä Alue-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5d26e-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="5d26e-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5d26e-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5d26e-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d26e-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="5d26e-116">Luo polttoaineindeksi</span><span class="sxs-lookup"><span data-stu-id="5d26e-116">Create a fuel index</span></span>
1. <span data-ttu-id="5d26e-117">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="5d26e-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="5d26e-118">Määritetyille alueille on syötettävä nykyiset polttoainemaksut.</span><span class="sxs-lookup"><span data-stu-id="5d26e-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="5d26e-119">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5d26e-119">Click New.</span></span>
3. <span data-ttu-id="5d26e-120">Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5d26e-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5d26e-121">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5d26e-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5d26e-122">Syötä Litrahinta-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5d26e-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="5d26e-123">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="5d26e-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="5d26e-124">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d26e-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="5d26e-125">Rahdinkuljettajan polttoaineindeksin luominen</span><span class="sxs-lookup"><span data-stu-id="5d26e-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="5d26e-126">Valitse Kuljetustenhallinta > Asetukset > Polttoaineindeksit > Rahdinkuljettajan polttoaineindeksit.</span><span class="sxs-lookup"><span data-stu-id="5d26e-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="5d26e-127">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5d26e-127">Click New.</span></span>
3. <span data-ttu-id="5d26e-128">Kirjoita Rahdinkuljettajan polttoaineindeksi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="5d26e-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="5d26e-129">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5d26e-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5d26e-130">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="5d26e-130">Click New.</span></span>
6. <span data-ttu-id="5d26e-131">Syötä Voimaantulon aloituspäivä ja -aika -kenttään päivämäärä ja aika.</span><span class="sxs-lookup"><span data-stu-id="5d26e-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="5d26e-132">Syötä Litrahinta alkaen -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5d26e-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="5d26e-133">Tässä esimerkissä Litrahinta alkaen -kenttään syötetään arvo 1,95.</span><span class="sxs-lookup"><span data-stu-id="5d26e-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="5d26e-134">Litrahinta enintään -kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5d26e-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="5d26e-135">Tässä esimerkissä Litrahinta enintään -kenttään syötetään arvo 2.</span><span class="sxs-lookup"><span data-stu-id="5d26e-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="5d26e-136">Syötä Prosentti-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5d26e-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="5d26e-137">Tässä esimerkissä prosentiksi syötetään 3.</span><span class="sxs-lookup"><span data-stu-id="5d26e-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="5d26e-138">Avaa haku valitsemalla Valuutta-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="5d26e-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5d26e-139">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5d26e-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5d26e-140">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5d26e-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5d26e-141">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5d26e-141">Click Save.</span></span>


