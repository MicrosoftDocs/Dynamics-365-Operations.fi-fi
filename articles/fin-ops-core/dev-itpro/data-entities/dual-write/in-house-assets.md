---
title: Sisäiset resurssit huoltoa varten
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Field Service voi auttaa sekä asiakasresurssien että sisäisten resurssien huollossa.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: c946af11737a77c4dadd824893e6cc1e4c77b587
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858619"
---
# <a name="in-house-assets-for-servicing"></a>Sisäiset resurssit huoltoa varten

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service on suunniteltu asiakasresurssien huoltoa varten. Dynamics 365 Supply Chain Managementin resurssien hallinta on suunniteltu sisäisten resurssien ylläpitoa varten. Näiden kahden sovelluksen integroinnin avulla voi käyttää Field Service -sovellusta sekä asiakasresurssien että sisäisten resurssien kanssa. Voit myös luokitella resurssit toiminnallisen sijainnin tai hierarkian perusteella sekä seurata huoltoa tarkasti.

Lisätietoja on kohdassa [Dynamics 365 Field Servicen ja Supply Chain Managementin integroiminen](/dynamics365/field-service/supply-chain-field-service-integration).

## <a name="templates"></a>Mallit

Sisäiset resurssit sisältävät perustaulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
[Resurssien hallinnan resurssien elinkaarimallit](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[Resurssien hallinnan resurssien elinkaaritilat](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[Resurssien hallinnan resurssityypit](mapping-reference.md#124) | msdyn_customerassetcategories | |
[Resurssien hallinnan resurssit](mapping-reference.md#125) | msdyn_customerassets | |
[Resurssien hallinnan toiminnallisen sijainnin elinkaarimallit](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[Resurssien hallinnan toiminnallisen sijainnin elinkaaritilat](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[Resurssien hallinnan toiminnallisen sijainnin tyypit](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[Resurssien hallinnan toiminnalliset sijainnit](mapping-reference.md#136) | msdyn_functionallocations | |
[Resurssien hallinnan valmistajat](mapping-reference.md#153) | msdyn_manufacturers | |
[Resurssien hallinnan mallit](mapping-reference.md#154) | msdyn_models | |
[Resurssien hallinnan takuu](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
