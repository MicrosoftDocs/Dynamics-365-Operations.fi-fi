---
title: Kanta-asiakaskortit ja palkkiopisteet
description: Tässä ohjeaiheessa käsitellään asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tietojen integrointia kaksoiskirjoituksella.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: d20dca3e8f15d04b85bcdf102dda8794c68dc2d54acb65dbd0088da1e6c6cdc5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765095"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kanta-asiakaskortit ja palkkiopisteet

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Yritykset luokittelevat asiakkaat ja tarjoavat kehittyneitä palveluita asiakkaan ostosten ja kulutustottumusten perusteella. Esimeriksi Dynamics 365 Commerce sisältää infrastruktuurin ja toiminnot, jotka helpottavat ja käsittelevät asiakkaan kanta-asiakaskortteja, palkkiopisteitä, kanta-asiakashinnoittelun ja palkkiopohjaisia ostoskokemuksia. Kun asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tiedot synkronoidaan Dataverseen, Customer Engagement -sovellukset voivat käyttää näitä tietoja. Esimerkiksi Dynamics 365 Customer Servicen käyttäjät voivat käyttää tietoja tarjotakseen samoja kehittyneitä palveluita tukipalvelun kautta.

## <a name="templates"></a>Mallit

Finance and Operations -sovellukset | Asiakkaiden aktivointisovellukset     | kuvaus
|-----------------------------|-----------------------------------|-------------|
[Kanta-asiakaskortti](mapping-reference.md#149) | msdyn_loyaltycards | Tämä malli synkronoi tietoja asiakkaan kanta-asiakaskorteista. |
[Kanta-asiakastasot](mapping-reference.md#226) | msdyn_loyaltylevels | Tämä malli synkronoi tietoja asiakkaan palkkiopisteistä. |
[Kanta-asiakkaan palkkiopisteet](mapping-reference.md#150) | msdyn_loyaltyrewardpoints | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
