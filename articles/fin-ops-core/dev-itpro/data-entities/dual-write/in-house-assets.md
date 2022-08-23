---
title: Sisäiset resurssit huoltoa varten
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Field Service voi auttaa sekä asiakasresurssien että sisäisten resurssien huollossa.
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: b3e741c85fcad2abc18879280ef7332ae091c984
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289247"
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
