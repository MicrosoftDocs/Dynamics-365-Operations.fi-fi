---
title: Määritä nimikkeen saapumisen yhteenvedon profiili
description: Tässä aiheessa keskitytään saapumisen yleiskuvaprofiilin määrittämiseen.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55512c75445a5f3b9c1521376a20d48dd60e22c6
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145522"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="34e5a-103">Määritä nimikkeen saapumisen yhteenvedon profiili</span><span class="sxs-lookup"><span data-stu-id="34e5a-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="34e5a-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="34e5a-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="34e5a-105">Tässä aiheessa keskitytään saapumisen yleiskuvaprofiilin määrittämiseen.</span><span class="sxs-lookup"><span data-stu-id="34e5a-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="34e5a-106">Saapumisen yleiskuvaprofiili on sääntökokoelma, jota käytetään, kun käyttäjä Saapumisten yhteenveto -sivun.</span><span class="sxs-lookup"><span data-stu-id="34e5a-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="34e5a-107">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="34e5a-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="34e5a-108">Yleensä vastaanottoassistentti tekee tämän menettelyn.</span><span class="sxs-lookup"><span data-stu-id="34e5a-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="34e5a-109">Valitse siirtymisruudussa **Moduulit > Inventoinnin- ja varastonhallinta > Asetukset > Jakelu > Saapumisen yleiskuvaprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="34e5a-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-110">Select **New**.</span></span> <span data-ttu-id="34e5a-111">Koska työskentelet lähes samassa varastossa, jossa täydet kuormat puretaan, sinun kannattaa luoda saapumisen yleiskuvaprofiili vastaanotettujen nimikkeiden rekisteröintiprosessia varten.</span><span class="sxs-lookup"><span data-stu-id="34e5a-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="34e5a-112">Kirjoita **Saapumisen yleiskuvaprofiilin nimi** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="34e5a-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="34e5a-113">Valitse vaihtoehto **Näytä rivit** -kentässä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="34e5a-114">Määritä vastaanotoissa näytettävät rivit:</span><span class="sxs-lookup"><span data-stu-id="34e5a-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="34e5a-115">**Kaikki** – Näyttää kaikki rivit tilasta huolimatta.</span><span class="sxs-lookup"><span data-stu-id="34e5a-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="34e5a-116">**Käsittelyssä** – Näyttää vastaanotot, joiden etenemisen tila on Valmis tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="34e5a-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="34e5a-117">Se tarkoittaa, että jokaiselle riville on saapumisen kirjauskansioon rekisteröity koko määrä tai osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="34e5a-118">**Ei valmis** – Näyttää vastaanotot, joiden etenemisen tila on Ei mitään tai Osittain.</span><span class="sxs-lookup"><span data-stu-id="34e5a-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="34e5a-119">Se tarkoittaa, että millekään riville ei ole saapumisen kirjauskansioon rekisteröity määrää tai rekisteröitynä on vain osittainen määrä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="34e5a-120">Laajenna tai tiivistä **Saapumisasetukset**-osa.</span><span class="sxs-lookup"><span data-stu-id="34e5a-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="34e5a-121">Kirjoita arvo **Päivää eteenpäin** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="34e5a-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="34e5a-122">Tämä määrittää suodattimen, joka näyttää muutaman seuraavan päivän kuluessa vastaanotettavat vastaanottorivit (määrittämästäsi numerosta riippuen).</span><span class="sxs-lookup"><span data-stu-id="34e5a-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="34e5a-123">Kirjoita arvo **Päivää taaksepäin** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="34e5a-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="34e5a-124">Tämä määrittää suodattimen, joka näyttää vastaanottorivit, joiden odotetaan saapuvan tiettyjen päivien kuluttua.</span><span class="sxs-lookup"><span data-stu-id="34e5a-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="34e5a-125">Kirjoita arvo **Varastot**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="34e5a-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="34e5a-126">Suodata vähintään yhden varaston perusteella.</span><span class="sxs-lookup"><span data-stu-id="34e5a-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="34e5a-127">Valitse arvo **Toimitustapa**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="34e5a-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="34e5a-128">Tämä määrittää suodatuksen, jolla näytetään vain tätä toimitustapaa käyttävät vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="34e5a-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="34e5a-129">Valitse **Nimi**-kentässä WHS.</span><span class="sxs-lookup"><span data-stu-id="34e5a-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="34e5a-130">Valitse varasto 24 **Varasto**-kentästä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="34e5a-131">Tämä on oletusvarasto, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="34e5a-132">Valitse **Sijainti**-kentästä **Lastauspaikan ovi**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="34e5a-133">Tämä on oletustoimipaikka, jota käytetään tätä profiilia käyttävillä rekisteröidyillä vastaanottoriveillä.</span><span class="sxs-lookup"><span data-stu-id="34e5a-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="34e5a-134">Laajenna tai tiivistä **Saapumiskyselyn tiedot** -osa.</span><span class="sxs-lookup"><span data-stu-id="34e5a-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="34e5a-135">Valitse toimipaikka 2 **Rajoita toimipaikkaan** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="34e5a-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="34e5a-136">Tämä määrittää suodatuksen, jolla näytetään vain tämän toimipaikan vastaanottorivit.</span><span class="sxs-lookup"><span data-stu-id="34e5a-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="34e5a-137">Määritä **Ostotilaukset**-kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="34e5a-138">Valitse vastaanottorivit ostotilauksista.</span><span class="sxs-lookup"><span data-stu-id="34e5a-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="34e5a-139">Määritä **Siirtotilaukset**-kentän arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="34e5a-140">Valitse vastaanottorivit siirtotilauksista.</span><span class="sxs-lookup"><span data-stu-id="34e5a-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="34e5a-141">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="34e5a-141">Select **Save**.</span></span>
18. <span data-ttu-id="34e5a-142">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="34e5a-142">Close the page.</span></span>

