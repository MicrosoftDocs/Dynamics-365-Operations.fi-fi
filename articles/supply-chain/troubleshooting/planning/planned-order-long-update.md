---
title: Suunniteltujen tilausten päivittäminen kestää kauan
description: Suunnittelun tilauksen tarpeen määrää ja/tai toimituspäivää päivitettäessä päivityksen tallentaminen kestää tilauskohtaisesti tyypillisesti vähintään 30 sekuntia.
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476241"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Suunniteltujen tilausten päivittäminen kestää kauan

## <a name="symptoms"></a>Oireet

Suunnittelun tilauksen tarpeen määrää ja/tai toimituspäivää päivitettäessä päivityksen tallentaminen kestää tilauskohtaisesti tyypillisesti vähintään 30 sekuntia.

## <a name="resolution"></a>Ratkaisu

Tämä on tunnettu sisäisen pääsuunnittelumoduulin ongelma. Se johtuu taustalla olevasta tuoterakenteen automaattisesta hajotuksesta muokkausten aikana. Tämä ongelma korjataan suunnittelun optimoinnissa, jossa suunnittelija voi päivittää ja hyväksyä tilauksia ja sitten halutessaan käynnistää suunnitteluajon, joka päivittää taustatuoterakenteen suunnittelutilaukset.

Sisäisen pääsuunnittelumoduulin suorituskykyä voi parantaa seuraavasti:

1. Siirry kohtaan **Pääsuunnittelu \> Määritykset \> Suunnitelmat \> Pääsuunnitelmat**.
1. Valitse suunnitelma.
1. Laajenna **Aikarajat päivissä** -pikavälilehti.
1. Määritä **Hajotus**-asetukseksi *Kyllä* ja määritä tämän asetuksen alla olevaan kenttään 0 (nolla).

> [!NOTE]
> Tämä rajoittaa kyseisessä pääsuunnitelmassa suoritetut hajotukset yhteen päivään.
