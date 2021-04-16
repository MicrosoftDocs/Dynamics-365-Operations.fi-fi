---
title: Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona. Varastodimensio ei ole pakollinen.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce4960ed6406587557ce12b72b30fa9a620d6b18
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833494"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="db3f4-104">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="db3f4-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db3f4-105">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolla on toimipaikka ja varasto kattavuusdimensiona.</span><span class="sxs-lookup"><span data-stu-id="db3f4-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="db3f4-106">Varastodimensio ei ole pakollinen.</span><span class="sxs-lookup"><span data-stu-id="db3f4-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="db3f4-107">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="db3f4-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="db3f4-108">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="db3f4-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="db3f4-109">Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="db3f4-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="db3f4-110">Toimipaikan ja varaston dimensiot on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="db3f4-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="db3f4-111">Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="db3f4-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="db3f4-112">Multisite-toiminnot eivät kuitenkaan vaikuta niihin.</span><span class="sxs-lookup"><span data-stu-id="db3f4-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="db3f4-113">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="db3f4-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="db3f4-114">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="db3f4-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="db3f4-115">Varaston asetukseksi on määritetty **Manuaalinen**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="db3f4-116">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="db3f4-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="db3f4-117">Tarkista **Pääsuunnittelu**-pikavälilehden **Manuaalinen**-kenttä.</span><span class="sxs-lookup"><span data-stu-id="db3f4-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="db3f4-118">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="db3f4-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="db3f4-119">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="db3f4-120">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="db3f4-121">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="db3f4-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="db3f4-122">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="db3f4-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="db3f4-123">Tarkista **Pääsuunnittelu**-pikavälilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="db3f4-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="db3f4-124">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="db3f4-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="db3f4-125">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="db3f4-126">Valitse ensin nimike ja sitten toimintoruudun **Suunnittelu**-välilehdessä **Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="db3f4-127">Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="db3f4-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Kysynnän toimipaikka ja varaston kattavuus, varasto pakollinen](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="db3f4-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="db3f4-129">Additional resources</span></span>
--------

[<span data-ttu-id="db3f4-130">Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="db3f4-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="db3f4-131">Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="db3f4-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="db3f4-132">Pääsuunnittelu toimipaikan kattavuudelle, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="db3f4-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="db3f4-133">Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="db3f4-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="db3f4-134">Tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="db3f4-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]