---
title: Tuontitöiden päivämäärän ja ajan synkronoiminen
description: Kun töitä tuodessa käytetään UTC-aikavyöhykkeitä aikavyöhykkeiden muunnot eivät aiheuta ongelmia.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748666"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Tuontitöiden päivämäärän ja ajan synkronoiminen

[!include [banner](../includes/banner.md)]

On tärkeää, että tuontityön aikavyöhykkeeksi määritetään koordinoitu yleisaika (UTC). Tuoduissa tiedoissa voi näkyä odottamattomia päivämääriä ja aikoja, jos käytössä on jokin muu asetus. Jos asetus ei ole oikea, tuontiprosessi muuntaa UTC-päivämäärän paikalliseen muotoon ja järjestelmäasetukset muuntavat sen sitten uudelleen.

Tämän kaksoismuunnon vuoksi päivämäärät muuttavat sovellusten välillä. Kaksoismuunto voi aiheuttaa esimerkiksi sen, että työntekijällä on eri alkamispäivä Dynamics 365 Human Resourcesissa ja Dynamics 365 Financessa paikallisten aikavyöhykkeiden erojen vuoksi. Tämä ongelma ratkaistaan määrittämällä tuontityöhön UTC-aika.

1. Valitse Dynamics 365 Finance and Operationsissa **Tiedonhallinta**.

2. Valitse ensin **Tuo projektit** ja sitten projekti.

3. Valitse **Lähteen päivämäärämuoto** kohdassa **CSV-Unicode**.

   [![Lähteen päivämäärämuodon muuttaminen UTC-muotoon](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Muuta **Aikavyöhyke**-asetukseksi **Koordinoitu yleisaika** ja muuta **Kieli**-asetukseksi **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]