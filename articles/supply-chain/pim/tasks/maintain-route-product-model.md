---
title: Ylläpidä tuotemallin reititystä
description: Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921262"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="e7510-103">Ylläpidä tuotemallin reititystä</span><span class="sxs-lookup"><span data-stu-id="e7510-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7510-104">Tämän menettelyn suorittaminen edellyttää, että tuotemääritysmalli on luotu aiemmin.</span><span class="sxs-lookup"><span data-stu-id="e7510-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="e7510-105">Tämä menetelmä käyttää USMF-demoyrityksen Korkealaatuinen kaiutin -mallia prosessin selittämiseen.</span><span class="sxs-lookup"><span data-stu-id="e7510-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="e7510-106">Lisää reitityksen työvaihe</span><span class="sxs-lookup"><span data-stu-id="e7510-106">Add a route operation</span></span>

1. <span data-ttu-id="e7510-107">Valitse **Tuotetietojen hallinta \> Tuotteet \> Tuotekonfiguraation mallit**.</span><span class="sxs-lookup"><span data-stu-id="e7510-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="e7510-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="e7510-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7510-109">Valitse tähän harjoitukseen Korkealaatuinen kaiutinmalli.</span><span class="sxs-lookup"><span data-stu-id="e7510-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="e7510-110">Valitse luettelossa valitulla rivillä oleva linkki.</span><span class="sxs-lookup"><span data-stu-id="e7510-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="e7510-111">Laajenna **Reitityksen työvaihe** -osa.</span><span class="sxs-lookup"><span data-stu-id="e7510-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="e7510-112">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e7510-112">Select **Add**.</span></span>
1. <span data-ttu-id="e7510-113">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="e7510-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="e7510-114">Kirjoita **Kuvaus**-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="e7510-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="e7510-115">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e7510-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="e7510-116">Anna reitityksen työvaiheen tiedot</span><span class="sxs-lookup"><span data-stu-id="e7510-116">Enter route operation details</span></span>

1. <span data-ttu-id="e7510-117">Valitse **Reitityksen työvaiheen tiedot**.</span><span class="sxs-lookup"><span data-stu-id="e7510-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="e7510-118">Anna tai valitse **Toiminto**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e7510-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="e7510-119">Valitse **Työvaiheen nro**</span><span class="sxs-lookup"><span data-stu-id="e7510-119">In the **Oper. No.**</span></span> <span data-ttu-id="e7510-120">numero.</span><span class="sxs-lookup"><span data-stu-id="e7510-120">field, enter a number.</span></span>
    * <span data-ttu-id="e7510-121">Työvaihenumerot määrittävät reittijärjestyksen.</span><span class="sxs-lookup"><span data-stu-id="e7510-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="e7510-122">Jokainen reitityksen työvaiheen ominaisuus voi saada staattisen arvon tai se voidaan yhdistää määritteeseen.</span><span class="sxs-lookup"><span data-stu-id="e7510-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="e7510-123">Määritteeseen yhdistettäessä arvo määritetään osana määritystä.</span><span class="sxs-lookup"><span data-stu-id="e7510-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="e7510-124">Anna tai valitse arvo **Reititysryhmä**-kentässä.</span><span class="sxs-lookup"><span data-stu-id="e7510-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="e7510-125">Reititysryhmä määrittää kustannuslaskennan, kulutuksen ja asetusten tärkeimmät toiminnot.</span><span class="sxs-lookup"><span data-stu-id="e7510-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="e7510-126">Valitse **Määritys**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e7510-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="e7510-127">Valitse **Ajat**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e7510-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="e7510-128">Syötä **Prosessimäärä**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e7510-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="e7510-129">Määritä, kuinka monta käsitellään yhdessä työvaiheessa.</span><span class="sxs-lookup"><span data-stu-id="e7510-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="e7510-130">Lisää **Tunnit/aika**-kenttään luku.</span><span class="sxs-lookup"><span data-stu-id="e7510-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="e7510-131">Lisää aikasuhde.</span><span class="sxs-lookup"><span data-stu-id="e7510-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="e7510-132">Valitse **Määritä**-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="e7510-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="e7510-133">Lisää **Ajoaika**-kenttään numero.</span><span class="sxs-lookup"><span data-stu-id="e7510-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="e7510-134">Määritä määritetyn määrän käsittelyaika.</span><span class="sxs-lookup"><span data-stu-id="e7510-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="e7510-135">Valitse **Resurssivaatimukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e7510-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="e7510-136">Valitse **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e7510-136">Select **Add**.</span></span>
1. <span data-ttu-id="e7510-137">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="e7510-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="e7510-138">Valitse **Vaatimustyyppi**-kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="e7510-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="e7510-139">Päätä, haluatko määrittää tietyt resurssit vai ominaisuudet, jotka niillä on oltava.</span><span class="sxs-lookup"><span data-stu-id="e7510-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="e7510-140">Anna tai valitse **Tarve**-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="e7510-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="e7510-141">Valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7510-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]