---
title: Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34a1a2cec9f86932fe2de9f3886059621903b262
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578169"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="2cb04-104">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="2cb04-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cb04-105">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona.</span><span class="sxs-lookup"><span data-stu-id="2cb04-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="2cb04-106">Varastodimensio ei ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="2cb04-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="2cb04-107">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="2cb04-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="2cb04-108">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="2cb04-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="2cb04-109">Tätä asetusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="2cb04-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="2cb04-110">Varastodimensiota ei ole määritetty pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="2cb04-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="2cb04-111">Varasto on ehkä tiedossa, mutta sitä ei käytetä pääsuunnittelun laskennassa.</span><span class="sxs-lookup"><span data-stu-id="2cb04-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="2cb04-112">Toimipaikan ja varaston dimensiot on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="2cb04-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="2cb04-113">Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="2cb04-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="2cb04-114">Multisite-toiminnot eivät kuitenkaan vaikuta niihin.</span><span class="sxs-lookup"><span data-stu-id="2cb04-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="2cb04-115">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="2cb04-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="2cb04-116">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="2cb04-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="2cb04-117">Varaston asetukseksi on määritetty Manuaalinen.</span><span class="sxs-lookup"><span data-stu-id="2cb04-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="2cb04-118">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="2cb04-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="2cb04-119">Tarkista **Pääsuunnittelu**-pikavälilehden **Manuaalinen**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="2cb04-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="2cb04-120">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="2cb04-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="2cb04-121">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="2cb04-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2cb04-122">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="2cb04-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="2cb04-123">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="2cb04-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="2cb04-124">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="2cb04-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="2cb04-125">Tarkista **Pääsuunnittelu**-pikavälilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="2cb04-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="2cb04-126">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="2cb04-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="2cb04-127">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="2cb04-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="2cb04-128">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="2cb04-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="2cb04-129">Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="2cb04-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Toimipaikan ja varaston kysyntä, ei varastoa](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="2cb04-131">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="2cb04-131">Additional resources</span></span>
--------

[<span data-ttu-id="2cb04-132">Pääsuunnittelu ja multisite-toiminnot</span><span class="sxs-lookup"><span data-stu-id="2cb04-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="2cb04-133">Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="2cb04-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2cb04-134">Pääsuunnittelu – sivuston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="2cb04-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="2cb04-135">Pääsuunnittelu – sivuston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="2cb04-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="2cb04-136">Pääsuunnittelu – tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="2cb04-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



