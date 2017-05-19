---
title: "Määritä RFM-analyysi"
description: "Tässä ohjeaiheessa kerrotaan, kuinka asiakkaidesi Recency, Frequency, and Monetary (RFM) -analyysi määritetään."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b6f49413d6226a37e16a30a8f68095211faa6d3d
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-rfm-analysis"></a>Määritä RFM-analyysi

[!include[banner](includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, kuinka asiakkaidesi Recency, Frequency, and Monetary (RFM) -analyysi määritetään.

Recency, Frequency, and Monetary (RFM)-analyysi on työkalu, jonka avulla organisaatio voi arvioida asiakasostojen muodostamat tiedot. Kun olet määrittänyt RFM-analyysin, asiakkaille määritetään laskettu RFM-pistemäärä heidän tehdessään ostoksia. RFM-pisteytys voi olla kolmenumeroinen luokitus tai yhteenlaskettu numero, riippuen siitä, kuinka organisaatio on määrittänyt RFM-analyysin. Jos organisaatiosi käyttää tulokselle kolminumeroista luokitusta, ensimmäinen numero on asiakkaan oston äskettäisyysluokitus (miten äskettäin asiakas teki ostoksen organisaatioltasi). Toinen numero kuvaa, kuinka toistuvasti asiakas suorittaa ostoja organisaatioltasi. Kolmas numero on asiakkaan kuluttaman rahasumman luokitus (paljonko rahaa asiakas käyttää suorittaessaan ostoja organisaatiostasi). Organisaatiosi on esimerkiksi asettanut luokitukset asteikolle 1-5, jossa 5 on korkein luokitus. Tässä tapauksessa asiakkaan luokitus 535 kertoo seuraavaa tietoa asiakkaasta:

-   **Äskettäisyysluokitus 5** – Asiakas on tehnyt ostoksen äskettäin.
-   **Toistuvuusluokitus 3** – Asiakas ostaa organisaatiosi tuotteita normaalilla aikavälillä.
-   **Rahasummaluokitus 5** – Kun asiakas suorittaa oston, hän käyttää huomattavan summan rahaa.

Jos organisaatiosi käyttää tuloksena yhteenlaskettua lukua, yksittäiset luokitusluvut lasketaan yhteen. Saman esimerkin asiakkaalla on luokitus 13 (5 + 3 + 5).




