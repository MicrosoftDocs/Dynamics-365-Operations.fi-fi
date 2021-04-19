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
ms.openlocfilehash: 040f9d26a137ebce1edc6adf28ff226b3a81e1ae
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748590"
---
# <a name="in-house-assets-for-servicing"></a>Sisäiset resurssit huoltoa varten

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service on suunniteltu asiakasresurssien huoltoa varten. Dynamics 365 Supply Chain Managementin resurssien hallinta on suunniteltu sisäisten resurssien ylläpitoa varten. Näiden kahden sovelluksen integroinnin avulla voi käyttää Field Service -sovellusta sekä asiakasresurssien että sisäisten resurssien kanssa. Voit myös luokitella resurssit toiminnallisen sijainnin tai hierarkian perusteella sekä seurata huoltoa tarkasti.

Lisätietoja on kohdassa [Dynamics 365 Field Servicen ja Supply Chain Managementin integroiminen](https://docs.microsoft.com/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Mallit

Sisäiset resurssit sisältävät perustaulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Finance and Operations -sovellukset | Dynamics 365:n mallipohjaiset sovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
| Resurssien hallinnan resurssien elinkaarimallit | msdyn\_assetlifecyclemodels | |
| Resurssien hallinnan resurssien elinkaaritilat | msdyn\_assetlifecyclestates | |
| Resurssien hallinnan resurssit | msdyn\_customerassets | |
| Resurssien hallinnan resurssityypit | msdyn\_customerassetcategories | |
| Resurssien hallinnan toiminnallisen sijainnin elinkaarimallit | msdyn\_functionallocationlifecyclemodels | |
| Resurssien hallinnan toiminnallisen sijainnin elinkaaritilat | msdyn\_functionallocationlifecyclestates | |
| Resurssien hallinnan toiminnalliset sijainnit | msdyn\_functionallocations | |
| Resurssien hallinnan toiminnallisen sijainnin tyypit | msdyn\_functionallocationtypes | |
| Resurssien hallinnan valmistajat | msdyn\_manufacturers | |
| Resurssien hallinnan mallit | msdyn\_models | |
| Resurssien hallinnan takuu | msdyn\_warranties | |

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