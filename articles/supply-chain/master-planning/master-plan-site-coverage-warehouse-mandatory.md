---
title: "Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen"
description: "Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona. Varasto ei ole pakollinen dimensio."
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
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 14df626025a22237afe30cc5b08d42b475fc3a4f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="1f57d-104">Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="1f57d-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1f57d-105">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona.</span><span class="sxs-lookup"><span data-stu-id="1f57d-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="1f57d-106">Varasto ei ole pakollinen dimensio.</span><span class="sxs-lookup"><span data-stu-id="1f57d-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="1f57d-107">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="1f57d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="1f57d-108">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1f57d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="1f57d-109">Tätä asetusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="1f57d-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="1f57d-110">Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="1f57d-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="1f57d-111">Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="1f57d-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="1f57d-112">Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="1f57d-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="1f57d-113">Multisite-toiminnot eivät kuitenkaan vaikuta niihin.</span><span class="sxs-lookup"><span data-stu-id="1f57d-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="1f57d-114">Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="1f57d-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="1f57d-115">Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="1f57d-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="1f57d-116">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="1f57d-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="1f57d-117">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="1f57d-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="1f57d-118">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="1f57d-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="1f57d-119">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="1f57d-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1f57d-120">Valitse nimike ja valitse sitten **Suunnitelma &gt; Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="1f57d-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="1f57d-121">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="1f57d-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="1f57d-122">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="1f57d-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="1f57d-123">Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="1f57d-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="1f57d-124">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="1f57d-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="1f57d-125">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="1f57d-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="1f57d-126">Valitse nimike ja valitse sitten **Suunnitelma &gt; Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="1f57d-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="1f57d-127">Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="1f57d-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Toimipaikan kattavuuden kysyntä, varasto pakollinen](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="1f57d-129">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="1f57d-129">See also</span></span>
--------

[<span data-ttu-id="1f57d-130">Pääsuunnittelu ja multisite-toiminnot</span><span class="sxs-lookup"><span data-stu-id="1f57d-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="1f57d-131">Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="1f57d-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1f57d-132">Pääsuunnittelu – toimipaikan kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="1f57d-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="1f57d-133">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="1f57d-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="1f57d-134">Pääsuunnittelu – tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="1f57d-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




