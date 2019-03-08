---
title: Pääsuunnittelu – toimipaikan kattavuus, varasto ei pakollinen
description: Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9475a7fbe40d7feb60c23e0d7164222469dffa75
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "353928"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="ffa31-103">Pääsuunnittelu – toimipaikan kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="ffa31-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffa31-104">Tässä aiheessa kuvataan, miten suunnitellaan nimike, jolle on suunniteltu toimipaikan dimensio kattavuutta varten.</span><span class="sxs-lookup"><span data-stu-id="ffa31-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="ffa31-105">Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:</span><span class="sxs-lookup"><span data-stu-id="ffa31-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="ffa31-106">Sivuston dimensio on asetettu pakolliseksi ja se on kirjoitettava kysyntätapahtumassa.</span><span class="sxs-lookup"><span data-stu-id="ffa31-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="ffa31-107">Varastodimensiota ei ole määritetty pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="ffa31-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="ffa31-108">Varasto on ehkä tiedossa, mutta sitä ei käytetä pääsuunnittelun laskennassa.</span><span class="sxs-lookup"><span data-stu-id="ffa31-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="ffa31-109">Toimipaikan dimensio on määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="ffa31-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="ffa31-110">Varaston dimensiota ei ole määritetty kattavuuden suunnittelua varten.</span><span class="sxs-lookup"><span data-stu-id="ffa31-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="ffa31-111">Tämän vuoksi tarjonta ja kysyntä yhdistetään toimipaikkakohtaisesti ja ehkä myös muiden sellaisten dimensioiden mukaan, joille on tehty kattavuussuunnitelma.</span><span class="sxs-lookup"><span data-stu-id="ffa31-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="ffa31-112">Seuraava kuva osoittaa, miten pääsuunnittelu etenee.</span><span class="sxs-lookup"><span data-stu-id="ffa31-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="ffa31-113">Kuvassa viitataan seuraaviin parametreihin:</span><span class="sxs-lookup"><span data-stu-id="ffa31-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="ffa31-114">Nimikkeen kattavuus on määritetty nimikkeelle.</span><span class="sxs-lookup"><span data-stu-id="ffa31-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="ffa31-115">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="ffa31-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ffa31-116">Valitse nimike ja valitse sitten **Suunnitelma &gt; Nimikkeen kattavuus**.</span><span class="sxs-lookup"><span data-stu-id="ffa31-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="ffa31-117">Varastolle on määritetty täydennyssuhteet.</span><span class="sxs-lookup"><span data-stu-id="ffa31-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="ffa31-118">Valitse **Inventoinnin- ja varastonhallinta &gt; Asetukset &gt; Varastoerittely &gt; Varastot**</span><span class="sxs-lookup"><span data-stu-id="ffa31-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="ffa31-119">Valitse **Pääsuunnittelu**-välilehdessä **Päävarasto**-kenttäryhmä.</span><span class="sxs-lookup"><span data-stu-id="ffa31-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="ffa31-120">Oletustilauksen tyypiksi on määritetty Tuotanto, Ostotilaus tai Kanban.</span><span class="sxs-lookup"><span data-stu-id="ffa31-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="ffa31-121">Valitse **Tuotetietojen hallinta &gt; Tuotteet &gt; Vapautetut tuotteet**.</span><span class="sxs-lookup"><span data-stu-id="ffa31-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="ffa31-122">Valitse nimike ja valitse sitten **Suunnitelma &gt; Tilauksen oletusasetukset**.</span><span class="sxs-lookup"><span data-stu-id="ffa31-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="ffa31-123">Tarkista **Tilauksen oletusasetukset** -lomakkeesta **Oletusarvoinen tilaustyyppi** -kenttä.</span><span class="sxs-lookup"><span data-stu-id="ffa31-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Toimipaikan kattavuuden kysyntä, varasto ei pakollinen    ](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="ffa31-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ffa31-125">Additional resources</span></span>
--------

[<span data-ttu-id="ffa31-126">Pääsuunnittelu ja multisite-toiminnot</span><span class="sxs-lookup"><span data-stu-id="ffa31-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="ffa31-127">Pääsuunnittelu – sivuston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="ffa31-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ffa31-128">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="ffa31-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="ffa31-129">Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="ffa31-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="ffa31-130">Pääsuunnittelu – tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ffa31-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



