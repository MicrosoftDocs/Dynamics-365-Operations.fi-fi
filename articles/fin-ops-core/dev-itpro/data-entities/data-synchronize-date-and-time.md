---
title: Tuontitöiden päivämäärän ja ajan synkronoiminen
description: Kun töitä tuodessa käytetään UTC-aikavyöhykkeitä aikavyöhykkeiden muunnot eivät aiheuta ongelmia.
author: peakerbl
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8faa7b73349c48d3a02b685546b47c4969c6027
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109429"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>Tuontitöiden päivämäärän ja ajan synkronoiminen

[!include [banner](../includes/banner.md)]

On tärkeää, että tuontityön aikavyöhykkeeksi määritetään koordinoitu yleisaika (UTC). Tuoduissa tiedoissa voi näkyä odottamattomia päivämääriä ja aikoja, jos käytössä on jokin muu asetus. Jos asetus ei ole oikea, tuontiprosessi muuntaa UTC-päivämäärän paikalliseen muotoon ja järjestelmäasetukset muuntavat sen sitten uudelleen.

Tämän kaksoismuunnon vuoksi päivämäärät muuttavat sovellusten välillä. Kaksoismuunto voi aiheuttaa esimerkiksi sen, että työntekijällä on eri alkamispäivä Dynamics 365 Human Resourcesissa ja Dynamics 365 Financessa paikallisten aikavyöhykkeiden erojen vuoksi. Tämä ongelma ratkaistaan määrittämällä tuontityöhön UTC-aika.

1. Valitse Dynamics 365:n talous- ja toimintosovelluksissa **Tietojen hallinta**.

2. Valitse ensin **Tuo projektit** ja sitten projekti.

3. Valitse **Lähteen päivämäärämuoto** kohdassa **CSV-Unicode**.

   [![Lähteen päivämäärämuodon muuttaminen UTC-muotoon.](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. Muuta **Aikavyöhyke**-asetukseksi **Koordinoitu yleisaika** ja muuta **Kieli**-asetukseksi **En-US**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

