---
title: Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi
description: Tässä aiheessa kerrotaan, miten asynkronisia asiakkaita muunnetaan synkronisiksi asiakkaiksi Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691441"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi

[!include [banner](includes/banner.md)]

Tässä aiheessa kerrotaan, miten asynkronisia asiakkaita muunnetaan synkronisiksi asiakkaiksi Microsoft Dynamics 365 Commercessa.

Asynkroniset asiakkaita muunnetaan synkronisiksi asiakkaiksi seuraavien vaiheiden avulla.

1. Suorita Commerce headquartersissa **P-työ** lähettääksesi asynkronisia asiakkaita Commerce headquartersiin.
1. Suorita **Synkronoi asiakkaat ja yrityskumppanit asynkronisesta tilasta** -työ asiakastilien tunnusten luontia varten. (Tämä työ on ollut aiemmin nimeltään **Asiakkaiden ja liikekumppanien synkronoiminen asynkronisesta tilasta**.)
1. Synkronoi uudet asiakastilitunnukset kanaviin suorittamalla **1010**-työ.

Jos tilaus viittaa asynkroniseen asiakkaaseen tai osoitteeseen, jota ei ole vielä synkronoitu Commerce Headquarters -synkronointiin, asiakas tai osoite **synkronoituu tilausten** erätyön osana. Jos käteis- ja siirtotapahtuma viittaa asynkroniseen asiakkaaseen tai osoitteeseen, asiakas tai osoite synkronoidaan ennen päivän lopun (EOD) kirjausta.

## <a name="additional-resources"></a>Lisäresurssit

[Myymälöiden asiakashallinta](customer-mgmt-stores.md)

[Asynkroninen asiakkaan luontitila](async-customer-mode.md)

[Asiakkaan määritteet](dev-itpro/customer-attributes.md)

[Offline-tietojen poissulkeminen](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
