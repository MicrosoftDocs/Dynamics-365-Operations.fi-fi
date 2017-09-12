--- 
title: "Ylläpidä tuotemallin reititystä"
description: "Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="5a0c2-103">Ylläpidä tuotemallin reititystä</span><span class="sxs-lookup"><span data-stu-id="5a0c2-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a0c2-104">Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="5a0c2-105">Tämä menetelmä käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -mallia prosessin selittämiseen.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="5a0c2-106">Lisää reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="5a0c2-106">Add a route operation</span></span>
1. <span data-ttu-id="5a0c2-107">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="5a0c2-108">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="5a0c2-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a0c2-110">Valitse tähän harjoitukseen Korkealaatuinen kaiutinmalli.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="5a0c2-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5a0c2-112">Laajenna Reitityksen työvaihe -osa.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="5a0c2-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-113">Click Add.</span></span>
7. <span data-ttu-id="5a0c2-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5a0c2-115">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="5a0c2-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="5a0c2-117">Anna reitityksen työvaiheen tiedot</span><span class="sxs-lookup"><span data-stu-id="5a0c2-117">Enter route operation details</span></span>
1. <span data-ttu-id="5a0c2-118">Valitse Reitityksen työvaiheen tiedot.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-118">Click Route operation details.</span></span>
2. <span data-ttu-id="5a0c2-119">Anna tai valitse Toiminto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="5a0c2-120">Lisää Työvaiheen</span><span class="sxs-lookup"><span data-stu-id="5a0c2-120">In the Oper.</span></span> <span data-ttu-id="5a0c2-121">Nro</span><span class="sxs-lookup"><span data-stu-id="5a0c2-121">No.</span></span> <span data-ttu-id="5a0c2-122">numero.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-122">field, enter a number.</span></span>
    * <span data-ttu-id="5a0c2-123">Työvaihenumerot määrittävät reittijärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="5a0c2-124">Jokainen reitityksen työvaiheen ominaisuus voi saada staattisen arvon tai se voidaan yhdistää määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="5a0c2-125">Määritteeseen yhdistettäessä arvo määritetään osana määritystä.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="5a0c2-126">Anna tai valitse arvo Reititysryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="5a0c2-127">Reititysryhmä määrittää kustannuslaskennan, kulutuksen ja asetusten tärkeimmät toiminnot.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="5a0c2-128">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="5a0c2-129">Valitse Ajat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-129">Click the Times tab.</span></span>
7. <span data-ttu-id="5a0c2-130">Syötä Prosessimäärä-kenttään</span><span class="sxs-lookup"><span data-stu-id="5a0c2-130">In the Process qty.</span></span> <span data-ttu-id="5a0c2-131">numero.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-131">field, enter a number.</span></span>
    * <span data-ttu-id="5a0c2-132">Määritä, kuinka monta käsitellään yhdessä työvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="5a0c2-133">Lisää Tunnit/aika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="5a0c2-134">Lisää aikasuhde.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="5a0c2-135">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-135">Select the Set check box.</span></span>
10. <span data-ttu-id="5a0c2-136">Lisää Ajoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="5a0c2-137">Määritä määritetyn määrän käsittelyaika.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="5a0c2-138">Valitse Resurssivaatimukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="5a0c2-139">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-139">Click Add.</span></span>
13. <span data-ttu-id="5a0c2-140">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="5a0c2-141">Valitse Vaatimustyyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="5a0c2-142">Päätä, haluatko määrittää tietyt resurssit vai ominaisuudet, jotka niillä on oltava.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="5a0c2-143">Anna tai valitse Tarve-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="5a0c2-144">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="5a0c2-144">Click OK.</span></span>


