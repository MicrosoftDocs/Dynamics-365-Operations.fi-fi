---
title: Pääsuunnittelu ja multisite-toiminnot
description: Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10981e0fe201566c83fd28c792000865bc533cd3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "317427"
---
# <a name="master-planning-and-multisite-functionality"></a><span data-ttu-id="a26f4-103">Pääsuunnittelu ja multisite-toiminnot</span><span class="sxs-lookup"><span data-stu-id="a26f4-103">Master planning and multisite functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a26f4-104">Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="a26f4-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="a26f4-105">Toimipaikkadimensio on pakollinen ja myös varastodimension voi määrittää pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="a26f4-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="a26f4-106">Kun dimensio on pakollinen, kaikkiin varastotapahtumiin on syötettävä dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="a26f4-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="a26f4-107">Sen vuoksi alkuperäisen kysynnän toimipaikka ja varasto ovat tunnettuja pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="a26f4-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="a26f4-108">Toimipaikkadimensio on myös yhdenmukainen, jolloin toimipaikan arvo ei muutu alemman tason kysynnän hajotuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="a26f4-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="a26f4-109">Kun varastoa ei määritetä pakolliseksi, se ei välttämättä ole tunnettu alkuperäisessä kysynnässä.</span><span class="sxs-lookup"><span data-stu-id="a26f4-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="a26f4-110">Suunnitteluohjelman on määritettävä käytettävä varasto nimikkeelle ja yksittäisille varastoille määritettyjen asetusten sekä tilausrivin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="a26f4-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="a26f4-111">Seuraavat aiheet kuvaavat suunnitteluohjelman toimintaa määritettäessä erilaisia asetuksia käytettävän varaston määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="a26f4-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="a26f4-112">Pääsuunnittelu – sivuston ja varaston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="a26f4-112">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="a26f4-113">Pääsuunnittelu – sivuston kattavuus, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="a26f4-113">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="a26f4-114">Pääsuunnittelu – toimipaikan ja varaston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="a26f4-114">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a26f4-115">Pääsuunnittelu – sivuston kattavuus, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="a26f4-115">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="a26f4-116">Pääsuunnittelu – tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a26f4-116">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



