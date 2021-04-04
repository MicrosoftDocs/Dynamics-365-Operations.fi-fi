---
title: Kanta-asiakaskortit ja palkkiopisteet
description: Tässä ohjeaiheessa käsitellään asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tietojen integrointia kaksoiskirjoituksella.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568025"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Kanta-asiakaskortit ja palkkiopisteet

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Yritykset luokittelevat asiakkaat ja tarjoavat kehittyneitä palveluita asiakkaan ostosten ja kulutustottumusten perusteella. Esimeriksi Dynamics 365 Commerce sisältää infrastruktuurin ja toiminnot, jotka helpottavat ja käsittelevät asiakkaan kanta-asiakaskortteja, palkkiopisteitä, kanta-asiakashinnoittelun ja palkkiopohjaisia ostoskokemuksia. Kun asiakkaan kanta-asiakaskorttien ja palkkiopisteiden tiedot synkronoidaan Dataverseen, Customer Engagement -sovellukset voivat käyttää näitä tietoja. Esimerkiksi Dynamics 365 Customer Servicen käyttäjät voivat käyttää tietoja tarjotakseen samoja kehittyneitä palveluita tukipalvelun kautta.

## <a name="templates"></a>Mallipohjat

| Finance and Operations -sovellukset | Dynamics 365:n mallipohjaiset sovellukset | kuvaus |
|-----------------------------|-----------------------------------|-------------|
| Kanta-asiakaskortti                | msdyn\_loyaltycards               | Tämä malli synkronoi tietoja asiakkaan kanta-asiakaskorteista. |
| Kanta-asiakkaan palkkiopisteet       | msdyn\_loyaltyrewardpoints        | Tämä malli synkronoi tietoja asiakkaan palkkiopisteistä. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]