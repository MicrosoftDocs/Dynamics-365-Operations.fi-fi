--- 
title: "Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna"
description: "Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 101ebe4a2e177a5702a162297e1820598e56a6e5
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="ff547-103">Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna</span><span class="sxs-lookup"><span data-stu-id="ff547-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff547-104">Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="ff547-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="ff547-105">Rahdinkuljettajan polttoaineindeksi on määritettävä ennen tämän ohjauksen suorittamista.</span><span class="sxs-lookup"><span data-stu-id="ff547-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="ff547-106">Sen voi määrittää Määritä rahdinkuljettajan polttoaineindeksi -ohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="ff547-106">You can use the “Set up a carrier fuel index” guide to do this.</span></span> <span data-ttu-id="ff547-107">Logistiikkapäällikkö tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="ff547-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="ff547-108">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ff547-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="ff547-109">Lisämaksun päätietojen luominen</span><span class="sxs-lookup"><span data-stu-id="ff547-109">Create an accessorial master</span></span>
1. <span data-ttu-id="ff547-110">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="ff547-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="ff547-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ff547-111">Click New.</span></span>
3. <span data-ttu-id="ff547-112">Kirjoita arvo Lisämaksun päätiedot -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff547-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="ff547-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff547-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ff547-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ff547-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="ff547-115">Rahdinkuljettajan lisämaksun luominen</span><span class="sxs-lookup"><span data-stu-id="ff547-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="ff547-116">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Rahdinkuljettajan lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="ff547-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="ff547-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ff547-117">Click New.</span></span>
3. <span data-ttu-id="ff547-118">Kirjoita Rahdinkuljettajan lisämaksun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ff547-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="ff547-119">Avaa haku valitsemalla Lähetyksen rahdinkuljettaja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ff547-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ff547-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ff547-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff547-121">Tässä esimerkissä valitaan kuorma-autonkuljettaja.</span><span class="sxs-lookup"><span data-stu-id="ff547-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="ff547-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ff547-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ff547-123">Avaa haku valitsemalla Rahdinkuljettajan palvelu -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ff547-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ff547-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ff547-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ff547-125">Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ff547-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ff547-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ff547-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ff547-127">Tässä esimerkissä valitaan juuri luodut lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="ff547-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="ff547-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ff547-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="ff547-129">Lisämaksun määritysten luominen</span><span class="sxs-lookup"><span data-stu-id="ff547-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="ff547-130">Valitse Lisämaksun määritykset.</span><span class="sxs-lookup"><span data-stu-id="ff547-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="ff547-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ff547-131">Click New.</span></span>
3. <span data-ttu-id="ff547-132">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff547-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ff547-133">Ota käyttöön Ehdot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="ff547-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="ff547-134">Voit määrittää ehdoissa, että polttoaineen lisämaksua käytetään aina. Tässä esimerkissä voit myös valita, että sitä käytetään vain tietyllä alueella.</span><span class="sxs-lookup"><span data-stu-id="ff547-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="ff547-135">Kirjoita arvo Postinumero lähtö -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff547-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="ff547-136">Kirjoita arvo Postinumero kohde -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ff547-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="ff547-137">Ota käyttöön Laskenta-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="ff547-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="ff547-138">Laskenta-osassa voit määrittää, miten polttoaineen lisämaksu lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ff547-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="ff547-139">Laskenta riippuu laskelman perustaksi valitusta lisämaksun yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="ff547-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="ff547-140">Valitse Lisämaksun tyyppi -kentässä Polttoaineen lisämaksu.</span><span class="sxs-lookup"><span data-stu-id="ff547-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="ff547-141">Valitse Lisämaksun yksikkö -kentässä Kilometri.</span><span class="sxs-lookup"><span data-stu-id="ff547-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="ff547-142">Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ff547-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ff547-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ff547-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ff547-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ff547-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="ff547-145">Rahdinkuljettajan hinnoitteluprofiilin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ff547-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="ff547-146">Valitse Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="ff547-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="ff547-147">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ff547-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ff547-148">Ota Luokituksen profiilit -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ff547-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="ff547-149">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="ff547-149">Click Edit.</span></span>
5. <span data-ttu-id="ff547-150">Avaa haku valitsemalla Rahdinkuljettajan polttoaineindeksi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ff547-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ff547-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ff547-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ff547-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ff547-152">Click Save.</span></span>


