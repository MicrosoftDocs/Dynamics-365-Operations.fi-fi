---
title: "Määritä nimikkeen saapumisen yhteenvedon profiili"
description: "Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4b4b89f39008218721ef092ee01a93522d1461b1
ms.contentlocale: fi-fi
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="20cac-103">Määritä nimikkeen saapumisen yhteenvedon profiili</span><span class="sxs-lookup"><span data-stu-id="20cac-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20cac-104">Tässä tehtävässä määritetään saapumisen yleiskuvaprofiili.</span><span class="sxs-lookup"><span data-stu-id="20cac-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="20cac-105">Saapumisen yleiskuvaprofiili on sääntökokoelma, jota käytetään, kun käyttäjä Saapumisten yhteenveto -sivun.</span><span class="sxs-lookup"><span data-stu-id="20cac-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="20cac-106">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="20cac-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="20cac-107">Yleensä vastaanottoassistentti tekee tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="20cac-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="20cac-108">Valitse Inventoinnin- ja varastonhallinta > Asetukset > Jakelu > Saapumisen yleiskuvaprofiilit.</span><span class="sxs-lookup"><span data-stu-id="20cac-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="20cac-109">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="20cac-109">Click New.</span></span>
    * <span data-ttu-id="20cac-110">Koska työskentelet lähes samassa varastossa, jossa täydet kuormat puretaan, sinun kannattaa luoda saapumisen yleiskuvaprofiili vastaanotettujen nimikkeiden rekisteröintiprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="20cac-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="20cac-111">Kirjoita Saapumisen yleiskuvaprofiilin nimi -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="20cac-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="20cac-112">Valitse vaihtoehto Näytä rivit -kentässä.</span><span class="sxs-lookup"><span data-stu-id="20cac-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="20cac-113">Määritä, mitä rivejä vastaanotoissa näytetään: Kaikki – Näytetään kaikki rivit tilasta riippumatta.</span><span class="sxs-lookup"><span data-stu-id="20cac-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="20cac-114">Käsittelyssä – Näyttää vastaanotot, joiden etenemisen tila on Valmis tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="20cac-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="20cac-115">Se tarkoittaa, että jokaiselle riville on saapumisen kirjauskansioon rekisteröity koko määrä tai osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="20cac-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="20cac-116">Ei valmis – Näyttää vastaanotot, joiden etenemisen tila on Ei mitään tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="20cac-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="20cac-117">Se tarkoittaa, että millekään riville ei ole saapumisen kirjauskansioon rekisteröity määrää tai rekisteröitynä on vain osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="20cac-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="20cac-118">Laajenna tai tiivistä Saapumisasetukset-osa.</span><span class="sxs-lookup"><span data-stu-id="20cac-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="20cac-119">Kirjoita arvo Päivää eteenpäin -kenttään.</span><span class="sxs-lookup"><span data-stu-id="20cac-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="20cac-120">Tämä määrittää suodattimen, joka näyttää muutaman seuraavan päivän kuluessa vastaanotettavat vastaanottorivit (määrittämästäsi numerosta riippuen).</span><span class="sxs-lookup"><span data-stu-id="20cac-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="20cac-121">Kirjoita arvo Päivää taaksepäin -kenttään.</span><span class="sxs-lookup"><span data-stu-id="20cac-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="20cac-122">Tämä määrittää suodattimen, joka näyttää vastaanottorivit, joiden odotetaan saapuvan tiettyjen päivien kuluttua.</span><span class="sxs-lookup"><span data-stu-id="20cac-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="20cac-123">Kirjoita arvo Varastot-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20cac-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="20cac-124">Suodata vähintään yhden varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="20cac-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="20cac-125">Valitse arvo Toimitustapa-kenttään.</span><span class="sxs-lookup"><span data-stu-id="20cac-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="20cac-126">Tämä määrittää suodatuksen, jolla näytetään vain tätä toimitustapaa käyttävät vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="20cac-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="20cac-127">Valitse Nimi-kentässä WHS.</span><span class="sxs-lookup"><span data-stu-id="20cac-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="20cac-128">Valitse varasto 24 Varasto-kentästä.</span><span class="sxs-lookup"><span data-stu-id="20cac-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="20cac-129">Tämä on oletusvarasto, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="20cac-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="20cac-130">Valitse Sijainti-kentästä Lastauspaikan ovi.</span><span class="sxs-lookup"><span data-stu-id="20cac-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="20cac-131">Tämä on oletustoimipaikka, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="20cac-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="20cac-132">Laajenna tai tiivistä Saapumiskyselyn tiedot -osa.</span><span class="sxs-lookup"><span data-stu-id="20cac-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="20cac-133">Valitse toimipaikka 2 Rajoita toimipaikkaan -kenttään.</span><span class="sxs-lookup"><span data-stu-id="20cac-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="20cac-134">Tämä määrittää suodatuksen, jolla näytetään vain tämän toimipaikan vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="20cac-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="20cac-135">Määritä Ostotilaukset-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="20cac-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="20cac-136">Valitse vastaanottorivit ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="20cac-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="20cac-137">Määritä Siirtotilaukset-kentän arvoksi Kyllä.</span><span class="sxs-lookup"><span data-stu-id="20cac-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="20cac-138">Valitse vastaanottorivit siirtotilauksista.</span><span class="sxs-lookup"><span data-stu-id="20cac-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="20cac-139">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="20cac-139">Click Save.</span></span>
18. <span data-ttu-id="20cac-140">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="20cac-140">Close the page.</span></span>

