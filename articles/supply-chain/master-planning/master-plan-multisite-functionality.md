---
title: Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus
description: Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: d0b715e0c17263519a9bb1b3780170812271d93d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813750"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="c2ad8-103">Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c2ad8-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2ad8-104">Pääsuunnittelussa otetaan huomioon toimipaikan ja varaston dimensioiden asetukset.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="c2ad8-105">Toimipaikkadimensio on pakollinen ja myös varastodimension voi määrittää pakolliseksi.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="c2ad8-106">Kun dimensio on pakollinen, kaikkiin varastotapahtumiin on syötettävä dimension arvo.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="c2ad8-107">Sen vuoksi alkuperäisen kysynnän toimipaikka ja varasto ovat tunnettuja pääsuunnittelun aikana.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="c2ad8-108">Toimipaikkadimensio on myös yhdenmukainen, jolloin toimipaikan arvo ei muutu alemman tason kysynnän hajotuksen aikana.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="c2ad8-109">Kun varastoa ei määritetä pakolliseksi, se ei välttämättä ole tunnettu alkuperäisessä kysynnässä.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="c2ad8-110">Suunnitteluohjelman on määritettävä käytettävä varasto nimikkeelle ja yksittäisille varastoille määritettyjen asetusten sekä tilausrivin tietojen perusteella.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="c2ad8-111">Seuraavat aiheet kuvaavat suunnitteluohjelman toimintaa määritettäessä erilaisia asetuksia käytettävän varaston määrityksessä.</span><span class="sxs-lookup"><span data-stu-id="c2ad8-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="c2ad8-112">Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="c2ad8-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c2ad8-113">Pääsuunnittelu toimipaikan kattavuudelle, varasto pakollinen</span><span class="sxs-lookup"><span data-stu-id="c2ad8-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="c2ad8-114">Toimipaikan ja varaston kattavuuden pääsuunnittelu, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="c2ad8-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c2ad8-115">Pääsuunnittelu toimipaikan kattavuudelle, varasto ei pakollinen</span><span class="sxs-lookup"><span data-stu-id="c2ad8-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="c2ad8-116">Tuoterakenneversion määrittäminen</span><span class="sxs-lookup"><span data-stu-id="c2ad8-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



