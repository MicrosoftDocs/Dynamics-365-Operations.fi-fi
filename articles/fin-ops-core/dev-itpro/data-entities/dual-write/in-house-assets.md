---
title: Sisäiset resurssit huoltoa varten
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Field Service voi auttaa sekä asiakasresurssien että sisäisten resurssien huollossa.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941411"
---
# <a name="in-house-assets-for-servicing"></a><span data-ttu-id="e57bd-103">Sisäiset resurssit huoltoa varten</span><span class="sxs-lookup"><span data-stu-id="e57bd-103">In-house assets for servicing</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="e57bd-104">Microsoft Dynamics 365 Field Service on suunniteltu asiakasresurssien huoltoa varten.</span><span class="sxs-lookup"><span data-stu-id="e57bd-104">Microsoft Dynamics 365 Field Service is designed to service customer assets.</span></span> <span data-ttu-id="e57bd-105">Dynamics 365 Supply Chain Managementin resurssien hallinta on suunniteltu sisäisten resurssien ylläpitoa varten.</span><span class="sxs-lookup"><span data-stu-id="e57bd-105">Asset management for Dynamics 365 Supply Chain Management is designed to maintain in-house assets.</span></span> <span data-ttu-id="e57bd-106">Näiden kahden sovelluksen integroinnin avulla voi käyttää Field Service -sovellusta sekä asiakasresurssien että sisäisten resurssien kanssa.</span><span class="sxs-lookup"><span data-stu-id="e57bd-106">Integration of these two apps lets you use Field Service to service both customer assets and in-house assets.</span></span> <span data-ttu-id="e57bd-107">Voit myös luokitella resurssit toiminnallisen sijainnin tai hierarkian perusteella sekä seurata huoltoa tarkasti.</span><span class="sxs-lookup"><span data-stu-id="e57bd-107">You can also classify the assets, based on functional location or hierarchy, and track the servicing at a detailed level.</span></span>

<span data-ttu-id="e57bd-108">Lisätietoja on kohdassa [Dynamics 365 Field Servicen ja Supply Chain Managementin integroiminen](/dynamics365/field-service/supply-chain-field-service-integration).</span><span class="sxs-lookup"><span data-stu-id="e57bd-108">For more information, see [Integrate Dynamics 365 Field Service and Supply Chain Management](/dynamics365/field-service/supply-chain-field-service-integration).</span></span>

## <a name="templates"></a><span data-ttu-id="e57bd-109">Mallit</span><span class="sxs-lookup"><span data-stu-id="e57bd-109">Templates</span></span>

<span data-ttu-id="e57bd-110">Sisäiset resurssit sisältävät perustaulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="e57bd-110">In-house-assets include a collection of core table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="e57bd-111">Finance and Operations -sovellukset</span><span class="sxs-lookup"><span data-stu-id="e57bd-111">Finance and Operations apps</span></span> | <span data-ttu-id="e57bd-112">Dynamics 365:n mallipohjaiset sovellukset</span><span class="sxs-lookup"><span data-stu-id="e57bd-112">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="e57bd-113">kuvaus</span><span class="sxs-lookup"><span data-stu-id="e57bd-113">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="e57bd-114">Resurssien hallinnan resurssien elinkaarimallit</span><span class="sxs-lookup"><span data-stu-id="e57bd-114">Asset management asset lifecycle models</span></span> | <span data-ttu-id="e57bd-115">msdyn\_assetlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="e57bd-115">msdyn\_assetlifecyclemodels</span></span> | |
| <span data-ttu-id="e57bd-116">Resurssien hallinnan resurssien elinkaaritilat</span><span class="sxs-lookup"><span data-stu-id="e57bd-116">Asset management asset lifecycle states</span></span> | <span data-ttu-id="e57bd-117">msdyn\_assetlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="e57bd-117">msdyn\_assetlifecyclestates</span></span> | |
| <span data-ttu-id="e57bd-118">Resurssien hallinnan resurssit</span><span class="sxs-lookup"><span data-stu-id="e57bd-118">Asset management assets</span></span> | <span data-ttu-id="e57bd-119">msdyn\_customerassets</span><span class="sxs-lookup"><span data-stu-id="e57bd-119">msdyn\_customerassets</span></span> | |
| <span data-ttu-id="e57bd-120">Resurssien hallinnan resurssityypit</span><span class="sxs-lookup"><span data-stu-id="e57bd-120">Asset management asset types</span></span> | <span data-ttu-id="e57bd-121">msdyn\_customerassetcategories</span><span class="sxs-lookup"><span data-stu-id="e57bd-121">msdyn\_customerassetcategories</span></span> | |
| <span data-ttu-id="e57bd-122">Resurssien hallinnan toiminnallisen sijainnin elinkaarimallit</span><span class="sxs-lookup"><span data-stu-id="e57bd-122">Asset management functional location lifecycle models</span></span> | <span data-ttu-id="e57bd-123">msdyn\_functionallocationlifecyclemodels</span><span class="sxs-lookup"><span data-stu-id="e57bd-123">msdyn\_functionallocationlifecyclemodels</span></span> | |
| <span data-ttu-id="e57bd-124">Resurssien hallinnan toiminnallisen sijainnin elinkaaritilat</span><span class="sxs-lookup"><span data-stu-id="e57bd-124">Asset management functional location lifecycle states</span></span> | <span data-ttu-id="e57bd-125">msdyn\_functionallocationlifecyclestates</span><span class="sxs-lookup"><span data-stu-id="e57bd-125">msdyn\_functionallocationlifecyclestates</span></span> | |
| <span data-ttu-id="e57bd-126">Resurssien hallinnan toiminnalliset sijainnit</span><span class="sxs-lookup"><span data-stu-id="e57bd-126">Asset management functional locations</span></span> | <span data-ttu-id="e57bd-127">msdyn\_functionallocations</span><span class="sxs-lookup"><span data-stu-id="e57bd-127">msdyn\_functionallocations</span></span> | |
| <span data-ttu-id="e57bd-128">Resurssien hallinnan toiminnallisen sijainnin tyypit</span><span class="sxs-lookup"><span data-stu-id="e57bd-128">Asset management functional location types</span></span> | <span data-ttu-id="e57bd-129">msdyn\_functionallocationtypes</span><span class="sxs-lookup"><span data-stu-id="e57bd-129">msdyn\_functionallocationtypes</span></span> | |
| <span data-ttu-id="e57bd-130">Resurssien hallinnan valmistajat</span><span class="sxs-lookup"><span data-stu-id="e57bd-130">Asset management manufacturers</span></span> | <span data-ttu-id="e57bd-131">msdyn\_manufacturers</span><span class="sxs-lookup"><span data-stu-id="e57bd-131">msdyn\_manufacturers</span></span> | |
| <span data-ttu-id="e57bd-132">Resurssien hallinnan mallit</span><span class="sxs-lookup"><span data-stu-id="e57bd-132">Asset management models</span></span> | <span data-ttu-id="e57bd-133">msdyn\_models</span><span class="sxs-lookup"><span data-stu-id="e57bd-133">msdyn\_models</span></span> | |
| <span data-ttu-id="e57bd-134">Resurssien hallinnan takuu</span><span class="sxs-lookup"><span data-stu-id="e57bd-134">Asset management warranty</span></span> | <span data-ttu-id="e57bd-135">msdyn\_warranties</span><span class="sxs-lookup"><span data-stu-id="e57bd-135">msdyn\_warranties</span></span> | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]