---
title: Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa
description: Tässä aiheessa kuvataan, kuinka Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594915"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce -hinnoittelumoduulin käyttäminen Dynamics 365 Salesin kanssa

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, kuinka Dynamics 365 Commerce -hinnoittelumoduulia käytetään myyntitarjousten luomiseen Dynamics 365 Salesissa.

Dynamics 365 Commerce -hinnoittelumoduuli tukee useimpia kuluttajakaupan (B2C) hinnoitteluskenaarioita, kuten myymälätason hinnoittelua, kumppanuus- ja lojaalisuushinnoittelua, yhdistelmäalennuksia, määräalennuksia ja kynnysalennuksia. Hinnoittelumoduuli määrittää tietyn tarjouksen tai tilauksen parhaan hinnan käyttämällä monimutkaisia sääntöjä.

Kun käytät [kaksoiskirjoittamista ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), hinnoittelutarpeisiisi on kolme vaihtoehtoa. Voit käyttää kiinteähintaista hinnoittelua, joka tulee Dynamics 365 Salesin hinnastosta, hinnoittelumoduulia Dynamics 365 Supply Chain Managementissa, tai hinnoittelumoduulia Dynamics 365 Commercessa. Näiden vaihtoehtojen joukossa on Commercen hinnoittelumoduuli, joka soveltuu parhaiten asiakaskaupan skenaarioihin.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Käytä Commercen hinnoittelumoduulia Salesissa

> [!NOTE]
> Tällä hetkellä Commercen hinnoittelumoduulia voidaan käyttää vain tarjousten luomiseen Salesissa. Myyntitilausten integrointi Commercen hinnoittelumoduuliin ei ole vielä käytettävissä.

Kun käyttäjät aloittavat tarjouksen Salesissa, kaksoiskirjoituskehys kopioi tarjouksen tiedot Commerceen. Aiemmin luotuihin tarjousriveihin tai uusiin tarjousriveihin Salesissa tehdyt muutokset kopioidaan Commerceen. Kun käyttäjät haluavat käyttää Commercen hinnoittelumoduulia tarjouksen hinnoittelussa, he voivat valita **Hintatarjouksen** päivittääkseen tarjouksen hinnat Commercen hinnoittelumoduulin perusteella. Tämän jälkeen hinnat päivitetään automaattisesti sekä Salesissa että Commercessa.

## <a name="prerequisites"></a>Edellytykset

- Ennen kuin voit käyttää Commercen hinnoittelu moduulia Salesissa, sinun on suoritettava vaiheet kohdassa [Mahdollisesta asiakkaasta käteiseen kaksoiskirjoituksella](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- Sinun on poistettava kauppasopimuksen arviointi käytöstä manuaaliselle syötölle seuraamalla näitä vaiheita:

    1. Siirry Commerce-ympäristössäsi kohtaan **Myyntireskontra \> Asetukset \> Myyntireskontran parametrit**.
    1. Tyhjennä **Hinnat** välilehden **Kauppasopimuksen arviointi** -pikavälilehdellä **Manuaalinen syöttö** -valintaruutu.

## <a name="additional-resources"></a>Lisäresurssit

[Prospektista käteiseksi -kaksoiskirjoitus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)