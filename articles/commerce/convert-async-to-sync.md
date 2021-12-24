---
title: Asynkronisten asiakkaiden muuntaminen synkronisiksi asiakkaiksi
description: Tässä aiheessa kerrotaan, miten asynkronisia asiakkaita muunnetaan synkronisiksi asiakkaiksi Microsoft Dynamics 365 Commercessa.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: d8a386299f2c67c870fe0b8f779c9155405c1f1a
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913794"
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
