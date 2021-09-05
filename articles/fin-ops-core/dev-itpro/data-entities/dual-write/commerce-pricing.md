---
title: Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c3f1527e5f37bebba57661ca86b1a3aae7e62da0
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416752"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.

Dynamics 365 Commerce -hinnoittelumoduuli tukee useimpia kuluttajakaupan (B2C) hinnoitteluskenaarioita, kuten myymälätason hinnoittelua, kumppanuus- ja lojaalisuushinnoittelua, yhdistelmäalennuksia, määräalennuksia ja kynnysalennuksia. Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä.

Kun käytät [kaksoiskirjoittamista ](./dual-write-overview.md), hinnoittelutarpeisiisi on kolme vaihtoehtoa. Voit käyttää kiinteähintaista hinnoittelua, joka tulee Dynamics 365 Salesin hinnastosta, hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa, tai hinnoittelumoduulia Dynamics 365 Commercessa. Näiden vaihtoehtojen joukossa on Commercen hinnoittelumoduuli, joka soveltuu parhaiten asiakaskaupan skenaarioihin.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Käytä Commercen hinnoittelumoduulia Salesissa

> [!NOTE]
> Tällä hetkellä Commercen hinnoittelumoduulia voidaan käyttää vain tarjousten luomiseen Salesissa. Myyntitilausten integrointi Commercen hinnoittelumoduuliin ei ole vielä käytettävissä.

Kun käyttäjät aloittavat tarjouksen Salesissa, kaksoiskirjoituskehys kopioi tarjouksen tiedot Commerceen. Aiemmin luotuihin tarjousriveihin tai uusiin tarjousriveihin Salesissa tehdyt muutokset kopioidaan Commerceen. Kun käyttäjät haluavat käyttää Commercen hinnoittelumoduulia tarjouksen hinnoittelussa, he voivat valita **Hintatarjouksen** päivittääkseen tarjouksen hinnat Commercen hinnoittelumoduulin perusteella. Tämän jälkeen hinnat päivitetään automaattisesti sekä Salesissa että Commercessa.

## <a name="prerequisites"></a>Edellytykset

- Ennen kuin voit käyttää Commercen hinnoittelu moduulia Salesissa, sinun on suoritettava vaiheet kohdassa [Mahdollisesta asiakkaasta käteiseen kaksoiskirjoituksella](./dual-write-prospect-to-cash.md).
- Sinun on poistettava kauppasopimuksen arviointi käytöstä manuaaliselle syötölle seuraamalla näitä vaiheita:

    1. Siirry Commerce-ympäristössäsi kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
    1. Tyhjennä **Hinnat** välilehden **Kauppasopimuksen arviointi** -pikavälilehdellä **Manuaalinen syöttö** -valintaruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Prospektista käteiseksi -kaksoiskirjoitus](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]