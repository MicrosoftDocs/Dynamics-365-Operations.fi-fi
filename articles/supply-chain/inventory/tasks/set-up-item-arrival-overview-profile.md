---
title: Määritä nimikkeen saapumisen yhteenvedon profiili
description: Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b61d77072358083a35de28003176cb88e53453e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555106"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="57929-103">Määritä nimikkeen saapumisen yhteenvedon profiili</span><span class="sxs-lookup"><span data-stu-id="57929-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="57929-104">Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili.</span><span class="sxs-lookup"><span data-stu-id="57929-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="57929-105">Saapumisen yleiskuvaprofiili on sääntökokoelma, jota käytetään, kun käyttäjä Saapumisten yhteenveto -sivun.</span><span class="sxs-lookup"><span data-stu-id="57929-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="57929-106">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="57929-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="57929-107">Yleensä vastaanottoassistentti tekee tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="57929-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="57929-108">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Jakelu > Saapumisen yleiskuvaprofiilit.</span><span class="sxs-lookup"><span data-stu-id="57929-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="57929-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="57929-109">Click New.</span></span>
    * <span data-ttu-id="57929-110">Koska työskentelet lähes samassa varastossa, jossa täydet kuormat puretaan, sinun kannattaa luoda saapumisen yleiskuvaprofiili vastaanotettujen nimikkeiden rekisteröintiprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="57929-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="57929-111">Kirjoita Saapumisen yleiskuvaprofiilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="57929-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="57929-112">Valitse vaihtoehto Näytä rivit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="57929-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="57929-113">Määritä, mitä rivejä vastaanotoissa näytetään: Kaikki – Näytetään kaikki rivit tilasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="57929-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="57929-114">Käsittelyssä – Näyttää vastaanotot, joiden etenemisen tila on Valmis tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="57929-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="57929-115">Se tarkoittaa, että jokaiselle riville on saapumisen kirjauskansioon rekisteröity koko määrä tai osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="57929-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="57929-116">Ei valmis – Näyttää vastaanotot, joiden etenemisen tila on Ei mitään tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="57929-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="57929-117">Se tarkoittaa, että millekään riville ei ole saapumisen kirjauskansioon rekisteröity määrää tai rekisteröitynä on vain osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="57929-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="57929-118">Laajenna tai tiivistä Saapumisasetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="57929-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="57929-119">Kirjoita arvo Päivää eteenpäin -kenttään.</span><span class="sxs-lookup"><span data-stu-id="57929-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="57929-120">Tämä määrittää suodattimen, joka näyttää muutaman seuraavan päivän kuluessa vastaanotettavat vastaanottorivit (määrittämästäsi numerosta riippuen).</span><span class="sxs-lookup"><span data-stu-id="57929-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="57929-121">Kirjoita arvo Päivää taaksepäin -kenttään.</span><span class="sxs-lookup"><span data-stu-id="57929-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="57929-122">Tämä määrittää suodattimen, joka näyttää vastaanottorivit, joiden odotetaan saapuvan tiettyjen päivien kuluttua.</span><span class="sxs-lookup"><span data-stu-id="57929-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="57929-123">Kirjoita arvo Varastot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="57929-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="57929-124">Suodata vähintään yhden varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="57929-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="57929-125">Valitse arvo Toimitustapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="57929-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="57929-126">Tämä määrittää suodatuksen, jolla näytetään vain tätä toimitustapaa käyttävät vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="57929-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="57929-127">Valitse Nimi-kentässä WHS.</span><span class="sxs-lookup"><span data-stu-id="57929-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="57929-128">Valitse varasto 24 Varasto-kentästä.</span><span class="sxs-lookup"><span data-stu-id="57929-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="57929-129">Tämä on oletusvarasto, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="57929-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="57929-130">Valitse Sijainti-kentästä Lastauspaikan ovi.</span><span class="sxs-lookup"><span data-stu-id="57929-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="57929-131">Tämä on oletustoimipaikka, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="57929-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="57929-132">Laajenna tai tiivistä Saapumiskyselyn tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="57929-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="57929-133">Valitse toimipaikka 2 Rajoita toimipaikkaan -kenttään.</span><span class="sxs-lookup"><span data-stu-id="57929-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="57929-134">Tämä määrittää suodatuksen, jolla näytetään vain tämän toimipaikan vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="57929-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="57929-135">Määritä Ostotilaukset-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="57929-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="57929-136">Valitse vastaanottorivit ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="57929-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="57929-137">Määritä Siirtotilaukset-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="57929-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="57929-138">Valitse vastaanottorivit siirtotilauksista.</span><span class="sxs-lookup"><span data-stu-id="57929-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="57929-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="57929-139">Click Save.</span></span>
18. <span data-ttu-id="57929-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="57929-140">Close the page.</span></span>

