---
title: Dimensioon perustuva tuotekonfigurointi
description: Dimensioihin perustuva tuotekonfiguraatio edustaa yksinkertaista ratkaisua useiden varianttien luomiselle yhdestä päätuotteesta ja sen tuoterakenteesta.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb2690ec5296f65430268a211108551348a4a060
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555951"
---
# <a name="dimension-based-product-configuration"></a><span data-ttu-id="ebef5-103">Dimensioon perustuva tuotekonfigurointi</span><span class="sxs-lookup"><span data-stu-id="ebef5-103">Dimension-based product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebef5-104">Dimensioihin perustuva tuotekonfiguraatio edustaa yksinkertaista ratkaisua useiden varianttien luomiselle yhdestä päätuotteesta ja sen tuoterakenteesta.</span><span class="sxs-lookup"><span data-stu-id="ebef5-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="ebef5-105">Dimensioihin perustuva tuotekonfiguraatio on yksi kolmesta sisäänrakennetusta tuotekonfiguraatiomenetelmistä.</span><span class="sxs-lookup"><span data-stu-id="ebef5-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="ebef5-106">Kaksi muuta menetelmää ovat ennalta määritettyjä variantteja ja poissulkeva konfiguraatio.</span><span class="sxs-lookup"><span data-stu-id="ebef5-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="ebef5-107">Kaikki kolme menetelmää käyttävät päätuotetta lähtökohtana ja sallivat käyttäjän luoda useita tuotevariantteja yhdelle päätuotteelle.</span><span class="sxs-lookup"><span data-stu-id="ebef5-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="ebef5-108">Avainkäsitteet</span><span class="sxs-lookup"><span data-stu-id="ebef5-108">Key concepts</span></span>
<span data-ttu-id="ebef5-109">Dimensioihin perustuva tuotekonfiguraatio perustuu seuraaviin avainkäsitteisiin:</span><span class="sxs-lookup"><span data-stu-id="ebef5-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="ebef5-110">Päätuotteet</span><span class="sxs-lookup"><span data-stu-id="ebef5-110">Product masters</span></span>
-   <span data-ttu-id="ebef5-111">Tuotedimension konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ebef5-111">Configuration product dimension</span></span>
-   <span data-ttu-id="ebef5-112">Konfiguraatioryhmät</span><span class="sxs-lookup"><span data-stu-id="ebef5-112">Configuration groups</span></span>
-   <span data-ttu-id="ebef5-113">Tuoterakenne (BOM)</span><span class="sxs-lookup"><span data-stu-id="ebef5-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="ebef5-114">Konfiguraatioreitti</span><span class="sxs-lookup"><span data-stu-id="ebef5-114">Configuration route</span></span>
-   <span data-ttu-id="ebef5-115">Konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="ebef5-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="ebef5-116">Päätuotteet</span><span class="sxs-lookup"><span data-stu-id="ebef5-116">Product masters</span></span>

<span data-ttu-id="ebef5-117">Kaikkien tuotemallien konfigurointiprosessien aloituspiste on päätuote.</span><span class="sxs-lookup"><span data-stu-id="ebef5-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="ebef5-118">Dimensioihin preustuvaan tuotekonfiguraation tarvitaan päätuote tässä tietyssä määritysmenetelmässä ja tuote dimensioryhmä, johon sisältyy konfiguraatio tuotedimensio.</span><span class="sxs-lookup"><span data-stu-id="ebef5-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="ebef5-119">Tuotedimension konfigurointi</span><span class="sxs-lookup"><span data-stu-id="ebef5-119">Configuration product dimension</span></span>

<span data-ttu-id="ebef5-120">Konfiguraatio tuotedimensiota käytetään päätuotteen tuotevarianttien tunnistamiseksi dimensioihin perustuvan konfiguraatiomenetelmän avulla.</span><span class="sxs-lookup"><span data-stu-id="ebef5-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="ebef5-121">Käyttäjä lisää Konfiguraation dimensioarvon ja sen tulisi auttaa tunnistamaan erilliset tuotevariantit.</span><span class="sxs-lookup"><span data-stu-id="ebef5-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="ebef5-122">Konfiguraatioryhmät</span><span class="sxs-lookup"><span data-stu-id="ebef5-122">Configuration groups</span></span>

<span data-ttu-id="ebef5-123">Konfiguraatioryhmät määritetään keskusrekisterissä ja niitä voidaan käyttää kaikkiin dimensioihin perustuviin tuotekonfiguraatiomalleihin.</span><span class="sxs-lookup"><span data-stu-id="ebef5-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="ebef5-124">konfiguraatioryhmät liitetään yksittäisiin tuoterakenneriveihin ja ne sisältävät useita rivejä, jotka ovat toisensa poissulkevia.</span><span class="sxs-lookup"><span data-stu-id="ebef5-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="ebef5-125">Tällöin yksittäiselle tuotevariantille voidaan valita vain yksi ryhmän rivi.</span><span class="sxs-lookup"><span data-stu-id="ebef5-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="ebef5-126">Tuoterakenne (BOM)</span><span class="sxs-lookup"><span data-stu-id="ebef5-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="ebef5-127">Tuoterakenne edustaa dimensioihin perustuvan tuotekonfiguraation rakenneosia.</span><span class="sxs-lookup"><span data-stu-id="ebef5-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="ebef5-128">Sen on sisällytettävä kaikki eri tuotteet, jotka ovat käytettävissä missä vain tuotevariantissa.</span><span class="sxs-lookup"><span data-stu-id="ebef5-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="ebef5-129">Tuoterakenteen kukin rivi voi viitata tuoterakenneryhmään.</span><span class="sxs-lookup"><span data-stu-id="ebef5-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="ebef5-130">Jos rivi ei viittaa konfiguraatioryhmään, se sisällytetään kaikkiin tuotemallin muuttujiin.</span><span class="sxs-lookup"><span data-stu-id="ebef5-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="ebef5-131">Konfiguraatioreitti</span><span class="sxs-lookup"><span data-stu-id="ebef5-131">Configuration route</span></span>

<span data-ttu-id="ebef5-132">Konfiguraatioreititys määrittää konfiguraatioryhmien järjestyksen, niin kuin ne näkyvät käyttäjälle tuotteen konfigurointiprosessin aikana.</span><span class="sxs-lookup"><span data-stu-id="ebef5-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="ebef5-133">Konfiguraatiosäännöt</span><span class="sxs-lookup"><span data-stu-id="ebef5-133">Configuration rules</span></span>

<span data-ttu-id="ebef5-134">Konfiguraatiosäännöt edustavat mekanismia, jolla varmistetaan että tuote joka sisältyy yhteen tuoterakenteen konfiguraatioryhmään, tukee joko muun tuotteen sisällytystä tai pois jättämistä eri konfigurointiryhmästä samassa tuoterakenteessa.</span><span class="sxs-lookup"><span data-stu-id="ebef5-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="ebef5-135">Tuotemallinnusprosessi</span><span class="sxs-lookup"><span data-stu-id="ebef5-135">Product modeling process</span></span>
<span data-ttu-id="ebef5-136">Luonnollinen järjestys tuotemallin dimensioihin perustuvan tuotteen rakentamiseen alkaa asianmukaisien konfiguraatioryhmien määrittämisestä.</span><span class="sxs-lookup"><span data-stu-id="ebef5-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="ebef5-137">On tärkeää varmistaa, että kaikki tuotteet joita käytetään tuotemallissa, on julkaistu sille yritykselle, jota varten tuotemalli on rakennettu.</span><span class="sxs-lookup"><span data-stu-id="ebef5-137">It is important to ensure that all products which will be used in the BOM have been released to the company that the product model is built for.</span></span> <span data-ttu-id="ebef5-138">Näiden rakenneosien ollessa paikallaan, käyttäjä voi luoda tuoterakenteen ja määrittää konfiguraatioryhmät kaikille olennaisille tuoterakenneriveille.</span><span class="sxs-lookup"><span data-stu-id="ebef5-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="ebef5-139">Kun tuoterakenne on valmis, konfiguraatioreititys voidaan määrittää järjestämällä konfiguraatioryhmät asianmukaiseen järjestykseen.</span><span class="sxs-lookup"><span data-stu-id="ebef5-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="ebef5-140">[![Dimensioihin perustuva tuotemallinnusprosessi](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span><span class="sxs-lookup"><span data-stu-id="ebef5-140">[![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="ebef5-141">Sen jälkeen kun tuoterakenne on sidottu yhteen dimensioihin perustuvan päätuotteen kanssa tuoterakenneversion kautta ja kummatkin on sekä hyväksytty että aktivoitu, voit luoda tuotemallin konfiguraatioita ja syöttää kullekin knfiguraatiolle nimen.</span><span class="sxs-lookup"><span data-stu-id="ebef5-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="ebef5-142">Konfiguraatiot voidaan määrittää ennen kuin mitään tapahtumia on luotu, tai se voidaan tehdä kun jotain konfiguraatiota tarvitaan.</span><span class="sxs-lookup"><span data-stu-id="ebef5-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="ebef5-143">Käyttöehdotukset</span><span class="sxs-lookup"><span data-stu-id="ebef5-143">Suggested use</span></span>

<span data-ttu-id="ebef5-144">Dimensioihin perustuvaa määritysmenetelmää kannattaa käyttää tuotteisiin, joilla on rajallinen vaihtelevaisuus ja yhdistelmä standardin tuotedimension mitoista, väristä, tyylistä ja konfiguraatio on sopimaton tunnistamaan tietyn tuotevariantin.</span><span class="sxs-lookup"><span data-stu-id="ebef5-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="ebef5-145">Esimerkki voisi olla polkupyörän rungon korkeus, pyörän koko, jarrutyypit ja eri vaihteet.</span><span class="sxs-lookup"><span data-stu-id="ebef5-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>

### <a name="next-step"></a><span data-ttu-id="ebef5-146">Seuraava vaihe</span><span class="sxs-lookup"><span data-stu-id="ebef5-146">Next step</span></span> 

<span data-ttu-id="ebef5-147">Seuraavat kahdeksan tehtäväopasta ovat siinä järjestyksessä, missä ne on tehtävä.</span><span class="sxs-lookup"><span data-stu-id="ebef5-147">The following eight task guides are listed in the order in which you should complete them.</span></span> 

1.  [<span data-ttu-id="ebef5-148">Dimensioihin perustuvan päätuotteen luominen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-148">Create a dimension-based product master (Task guide)</span></span>](tasks/create-dimension-based-product-master.md)
2.  [<span data-ttu-id="ebef5-149">Dimensioihin perustuvan päätuotteen vapauttaminen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-149">Release a dimension-based product master (Task guide)</span></span>](tasks/release-dimension-based-product-master.md)
3.  [<span data-ttu-id="ebef5-150">Julkaistun päätuotteen perusmääritysten päättäminen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-150">Complete basic setup of a released product master (Task guide)</span></span>](tasks/complete-basic-setup-released-product-master.md)
4.  [<span data-ttu-id="ebef5-151">Konfiguraatioryhmien määrittäminen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-151">Define configuration groups (Task guide)</span></span>](tasks/define-configuration-groups.md)
5.  [<span data-ttu-id="ebef5-152">Tuoterakenteen luominen dimensioihin perustuvalle päätuotteelle (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-152">Create a bill of materials for a dimension-based product master (Task guide)</span></span>](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [<span data-ttu-id="ebef5-153">Konfiguraatioreittien määrittäminen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-153">Define configuration routes (Task guide)</span></span>](tasks/define-configuration-route.md)
7.  [<span data-ttu-id="ebef5-154">Konfiguraatiosääntöjen luominen (tehtäväopas)</span><span class="sxs-lookup"><span data-stu-id="ebef5-154">Create configuration rules (Task guide)</span></span>](tasks/create-configuration-rules.md)
8.  [<span data-ttu-id="ebef5-155">Dimensioihin perustuvien konfiguraatioiden luominen (tehtäväopas)t</span><span class="sxs-lookup"><span data-stu-id="ebef5-155">Create dimension-based configurations (Task guide)</span></span>](tasks/create-dimension-based-configurations.md)

