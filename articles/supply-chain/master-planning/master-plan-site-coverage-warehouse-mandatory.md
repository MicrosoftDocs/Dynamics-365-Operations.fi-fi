---
title: Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona. Varasto ei ole pakollinen dimensio.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eaac165865b04a7c4ad2f08ca758b07fd41eaaa0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833542"
---
# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="b39f3-104">Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="b39f3-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b39f3-105">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikka kattavuuden dimensiona.</span><span class="sxs-lookup"><span data-stu-id="b39f3-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="b39f3-106">Varasto ei ole pakollinen dimensio.</span><span class="sxs-lookup"><span data-stu-id="b39f3-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="b39f3-107">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="b39f3-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b39f3-108">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="b39f3-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="b39f3-109">Tätä asetusta ei voi muokata.</span><span class="sxs-lookup"><span data-stu-id="b39f3-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="b39f3-110">Varaston dimensio on asetettu pakolliseksi ja se on määritettävä kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="b39f3-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b39f3-111">Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="b39f3-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="b39f3-112">Myös muita dimensioita voidaan määrittää kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="b39f3-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="b39f3-113">Multisite-toiminnot eivät kuitenkaan vaikuta niihin.</span><span class="sxs-lookup"><span data-stu-id="b39f3-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="b39f3-114">Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="b39f3-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="b39f3-115">Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="b39f3-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="b39f3-116">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="b39f3-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b39f3-117">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="b39f3-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b39f3-118">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="b39f3-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="b39f3-119">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="b39f3-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b39f3-120">Valitse nimike ja valitse sitten **Suunnitelma &gt; Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="b39f3-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="b39f3-121">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="b39f3-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b39f3-122">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="b39f3-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b39f3-123">Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="b39f3-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b39f3-124">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="b39f3-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="b39f3-125">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="b39f3-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b39f3-126">Valitse nimike ja valitse sitten **Suunnitelma &gt; Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="b39f3-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="b39f3-127">Tarkista **Tilauksen oletusasetukset** -lomakkeessa **Oletusarvoinen tilaustyyppi**.</span><span class="sxs-lookup"><span data-stu-id="b39f3-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Toimipaikan kattavuuden kysyntä, varasto pakollinen](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b39f3-129">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b39f3-129">Additional resources</span></span>
--------

[<span data-ttu-id="b39f3-130">Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="b39f3-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b39f3-131">Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="b39f3-131">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b39f3-132">Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="b39f3-132">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b39f3-133">Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="b39f3-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b39f3-134">Tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="b39f3-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]