---
title: "Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen"
description: "Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e753edacb0e2e019d701745308e7d9190ef09fe8
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="1e8ce-104">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1e8ce-105">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="1e8ce-106">Varastodimensio ei ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="1e8ce-107">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="1e8ce-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="1e8ce-108">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="1e8ce-109">Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="1e8ce-110">Toimipaikan ja varaston dimensiot on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="1e8ce-111">Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="1e8ce-112">Multisite-toiminnot eivät kuitenkaan vaikuta niihin.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="1e8ce-113">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="1e8ce-114">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="1e8ce-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="1e8ce-115">Varaston asetukseksi on määritetty **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="1e8ce-116">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="1e8ce-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="1e8ce-117">Tarkista **Pääsuunnittelu**-pikavälilehden **Manuaalinen**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="1e8ce-118">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="1e8ce-119">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1e8ce-120">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-120">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="1e8ce-121">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="1e8ce-122">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="1e8ce-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="1e8ce-123">Tarkista **Pääsuunnittelu**-pikavälilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="1e8ce-124">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="1e8ce-125">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1e8ce-126">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-126">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="1e8ce-127">Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="1e8ce-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Kysynnän toimipaikka ja varaston kattavuus, varasto pakollinen](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="1e8ce-129">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1e8ce-129">See also</span></span>
--------

[<span data-ttu-id="1e8ce-130">Pääsuunnittelu ja multisite-toiminnot</span><span class="sxs-lookup"><span data-stu-id="1e8ce-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="1e8ce-131">Pääsuunnittelu – sivuston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-131">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1e8ce-132">Pääsuunnittelu – sivuston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-132">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1e8ce-133">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1e8ce-134">Pääsuunnittelu – tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1e8ce-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




