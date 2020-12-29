---
title: Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna
description: Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4427448"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="ae700-103">Liitä polttoaineindeksi rahdinkuljettajaan lisämaksuna</span><span class="sxs-lookup"><span data-stu-id="ae700-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ae700-104">Tässä ohjauksessa kerrotaan, miten polttoaineen lisämaksun määritys, rahdinkuljettajan lisämaksu, lisämaksun päätiedot luodaan ja liitetään rahdinkuljettajan polttoaineindeksiin rahdinkuljettajan kanssa.</span><span class="sxs-lookup"><span data-stu-id="ae700-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="ae700-105">Rahdinkuljettajan polttoaineindeksi on määritettävä ennen tämän ohjauksen suorittamista.</span><span class="sxs-lookup"><span data-stu-id="ae700-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="ae700-106">Sen voi määrittää Määritä rahdinkuljettajan polttoaineindeksi -ohjauksessa.</span><span class="sxs-lookup"><span data-stu-id="ae700-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="ae700-107">Logistiikkapäällikkö tekee yleensä nämä tehtävät.</span><span class="sxs-lookup"><span data-stu-id="ae700-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="ae700-108">Tämän menettelyn luomisessa käytetty esittelytietojen yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="ae700-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="ae700-109">Lisämaksun päätietojen luominen</span><span class="sxs-lookup"><span data-stu-id="ae700-109">Create an accessorial master</span></span>
1. <span data-ttu-id="ae700-110">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="ae700-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="ae700-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae700-111">Click New.</span></span>
3. <span data-ttu-id="ae700-112">Kirjoita arvo Lisämaksun päätiedot -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae700-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="ae700-113">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae700-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ae700-114">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ae700-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="ae700-115">Rahdinkuljettajan lisämaksun luominen</span><span class="sxs-lookup"><span data-stu-id="ae700-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="ae700-116">Valitse Kuljetustenhallinta > Asetukset > Luokitus > Rahdinkuljettajan lisämaksut.</span><span class="sxs-lookup"><span data-stu-id="ae700-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="ae700-117">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae700-117">Click New.</span></span>
3. <span data-ttu-id="ae700-118">Kirjoita Rahdinkuljettajan lisämaksun tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="ae700-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="ae700-119">Avaa haku valitsemalla Lähetyksen rahdinkuljettaja -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae700-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ae700-120">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ae700-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ae700-121">Tässä esimerkissä valitaan kuorma-autonkuljettaja.</span><span class="sxs-lookup"><span data-stu-id="ae700-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="ae700-122">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ae700-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ae700-123">Avaa haku valitsemalla Rahdinkuljettajan palvelu -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae700-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ae700-124">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ae700-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ae700-125">Avaa haku valitsemalla Lisämaksun päätiedot -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae700-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ae700-126">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ae700-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ae700-127">Tässä esimerkissä valitaan juuri luodut lisämaksun päätiedot.</span><span class="sxs-lookup"><span data-stu-id="ae700-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="ae700-128">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ae700-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="ae700-129">Lisämaksun määritysten luominen</span><span class="sxs-lookup"><span data-stu-id="ae700-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="ae700-130">Valitse Lisämaksun määritykset.</span><span class="sxs-lookup"><span data-stu-id="ae700-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="ae700-131">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="ae700-131">Click New.</span></span>
3. <span data-ttu-id="ae700-132">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae700-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ae700-133">Ota käyttöön Ehdot-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="ae700-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="ae700-134">Voit määrittää ehdoissa, että polttoaineen lisämaksua käytetään aina. Tässä esimerkissä voit myös valita, että sitä käytetään vain tietyllä alueella.</span><span class="sxs-lookup"><span data-stu-id="ae700-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="ae700-135">Kirjoita arvo Postinumero lähtö -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae700-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="ae700-136">Kirjoita arvo Postinumero kohde -kenttään.</span><span class="sxs-lookup"><span data-stu-id="ae700-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="ae700-137">Ota käyttöön Laskenta-osan laajennus.</span><span class="sxs-lookup"><span data-stu-id="ae700-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="ae700-138">Laskenta-osassa voit määrittää, miten polttoaineen lisämaksu lasketaan.</span><span class="sxs-lookup"><span data-stu-id="ae700-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="ae700-139">Laskenta riippuu laskelman perustaksi valitusta lisämaksun yksiköstä.</span><span class="sxs-lookup"><span data-stu-id="ae700-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="ae700-140">Valitse Lisämaksun tyyppi -kentässä Polttoaineen lisämaksu.</span><span class="sxs-lookup"><span data-stu-id="ae700-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="ae700-141">Valitse Lisämaksun yksikkö -kentässä Kilometri.</span><span class="sxs-lookup"><span data-stu-id="ae700-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="ae700-142">Avaa haku valitsemalla Alue-kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae700-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ae700-143">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ae700-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ae700-144">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ae700-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="ae700-145">Rahdinkuljettajan hinnoitteluprofiilin päivittäminen</span><span class="sxs-lookup"><span data-stu-id="ae700-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="ae700-146">Valitse Kuljetustenhallinta > Asetukset > Rahdinkuljettajat > Lähetyksen rahdinkuljettajat.</span><span class="sxs-lookup"><span data-stu-id="ae700-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="ae700-147">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="ae700-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ae700-148">Ota Luokituksen profiilit -osan laajennus käyttöön.</span><span class="sxs-lookup"><span data-stu-id="ae700-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="ae700-149">Valitse Muokkaa.</span><span class="sxs-lookup"><span data-stu-id="ae700-149">Click Edit.</span></span>
5. <span data-ttu-id="ae700-150">Avaa haku valitsemalla Rahdinkuljettajan polttoaineindeksi -kentässä avattavan valikon painike.</span><span class="sxs-lookup"><span data-stu-id="ae700-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ae700-151">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="ae700-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ae700-152">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="ae700-152">Click Save.</span></span>

