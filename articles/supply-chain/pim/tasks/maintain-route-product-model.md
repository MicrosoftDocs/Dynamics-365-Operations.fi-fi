---
title: Ylläpidä tuotemallin reititystä
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13bbdc706280317c5a1ab7fb21c9585f1c7d48ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247787"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="35ab1-103">Ylläpidä tuotemallin reititystä</span><span class="sxs-lookup"><span data-stu-id="35ab1-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35ab1-104">Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="35ab1-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="35ab1-105">Tämä menetelmä käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -mallia prosessin selittämiseen.</span><span class="sxs-lookup"><span data-stu-id="35ab1-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="35ab1-106">Lisää reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="35ab1-106">Add a route operation</span></span>
1. <span data-ttu-id="35ab1-107">Valitse Tuotevarianttimallin määritys.</span><span class="sxs-lookup"><span data-stu-id="35ab1-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="35ab1-108">Valitse Tuotekonfiguraation mallit.</span><span class="sxs-lookup"><span data-stu-id="35ab1-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="35ab1-109">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="35ab1-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="35ab1-110">Valitse tähän harjoitukseen Korkealaatuinen kaiutinmalli.</span><span class="sxs-lookup"><span data-stu-id="35ab1-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="35ab1-111">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="35ab1-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="35ab1-112">Laajenna Reitityksen työvaihe -osa.</span><span class="sxs-lookup"><span data-stu-id="35ab1-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="35ab1-113">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="35ab1-113">Click Add.</span></span>
7. <span data-ttu-id="35ab1-114">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35ab1-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="35ab1-115">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="35ab1-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="35ab1-116">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="35ab1-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="35ab1-117">Anna reitityksen työvaiheen tiedot</span><span class="sxs-lookup"><span data-stu-id="35ab1-117">Enter route operation details</span></span>
1. <span data-ttu-id="35ab1-118">Valitse Reitityksen työvaiheen tiedot.</span><span class="sxs-lookup"><span data-stu-id="35ab1-118">Click Route operation details.</span></span>
2. <span data-ttu-id="35ab1-119">Anna tai valitse Toiminto-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="35ab1-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="35ab1-120">Lisää Työvaiheen</span><span class="sxs-lookup"><span data-stu-id="35ab1-120">In the Oper.</span></span> <span data-ttu-id="35ab1-121">Nro</span><span class="sxs-lookup"><span data-stu-id="35ab1-121">No.</span></span> <span data-ttu-id="35ab1-122">numero.</span><span class="sxs-lookup"><span data-stu-id="35ab1-122">field, enter a number.</span></span>
    * <span data-ttu-id="35ab1-123">Työvaihenumerot määrittävät reittijärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="35ab1-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="35ab1-124">Jokainen reitityksen työvaiheen ominaisuus voi saada staattisen arvon tai se voidaan yhdistää määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="35ab1-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="35ab1-125">Määritteeseen yhdistettäessä arvo määritetään osana määritystä.</span><span class="sxs-lookup"><span data-stu-id="35ab1-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="35ab1-126">Anna tai valitse arvo Reititysryhmä-kentässä.</span><span class="sxs-lookup"><span data-stu-id="35ab1-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="35ab1-127">Reititysryhmä määrittää kustannuslaskennan, kulutuksen ja asetusten tärkeimmät toiminnot.</span><span class="sxs-lookup"><span data-stu-id="35ab1-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="35ab1-128">Valitse Asetukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="35ab1-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="35ab1-129">Valitse Ajat-välilehti.</span><span class="sxs-lookup"><span data-stu-id="35ab1-129">Click the Times tab.</span></span>
7. <span data-ttu-id="35ab1-130">Syötä Prosessimäärä-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35ab1-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="35ab1-131">Määritä, kuinka monta käsitellään yhdessä työvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="35ab1-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="35ab1-132">Lisää Tunnit/aika-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="35ab1-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="35ab1-133">Lisää aikasuhde.</span><span class="sxs-lookup"><span data-stu-id="35ab1-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="35ab1-134">Valitse Määritä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="35ab1-134">Select the Set check box.</span></span>
10. <span data-ttu-id="35ab1-135">Lisää Ajoaika-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="35ab1-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="35ab1-136">Määritä määritetyn määrän käsittelyaika.</span><span class="sxs-lookup"><span data-stu-id="35ab1-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="35ab1-137">Valitse Resurssivaatimukset-välilehti.</span><span class="sxs-lookup"><span data-stu-id="35ab1-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="35ab1-138">ValitseLisää.</span><span class="sxs-lookup"><span data-stu-id="35ab1-138">Click Add.</span></span>
13. <span data-ttu-id="35ab1-139">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="35ab1-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="35ab1-140">Valitse Vaatimustyyppi-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="35ab1-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="35ab1-141">Päätä, haluatko määrittää tietyt resurssit vai ominaisuudet, jotka niillä on oltava.</span><span class="sxs-lookup"><span data-stu-id="35ab1-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="35ab1-142">Anna tai valitse Tarve-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="35ab1-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="35ab1-143">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="35ab1-143">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]