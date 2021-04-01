---
title: Manuaalinen poisto
description: Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7187290b51a0fd526bd0f4cbad9b479cd46ec31
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256760"
---
# <a name="manual-depreciation"></a>Manuaalinen poisto

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää manuaalisen poistomenetelmän yleiskatsauksen.

Kun määrität käyttöomaisuuden poistoprofiilin ja valitset **Poistoprofiilit**-sivun **Menetelmä**-kentässä **Manuaalinen**, poistoprofiiliin määritetty käyttöomaisuuden poisto määräytyy sen prosentin mukaan, joka annetaan kalenterivuoden kullekin aikavälille. Aikavälit, joille määrität prosenttiosuuden, kirjataan **Poistoprofiilit**-sivun **Yleinen**-pikavälilehden **Kausifrekvenssi**-kentässä valitun arvon mukaisesti. Valittavana on seuraavat arvot:

-   Vuosittain
-   Kuukausittain
-   Neljännesvuosittain
-   Puolivuosittain
-   Päivittäin

Valitse kausifrekvenssin valinnan jälkeen **Manuaalinen aikataulu** ja määritä kunkin kirjausvälin prosenttiosuudet. Manuaaliset aikataulut ja kirjausvälit määrittävät yhdessä poistosumman, kuten artikkelissa myöhemmin käsiteltävissä esimerkeissä. Manuaalinen poisto lasketaan aina prosenttina hankintahinnasta. Manuaalisissa poistoissa poistoväleille annettavien prosenttien summan ei tarvitse olla 100 prosenttia. Manuaalinen poisti on joustava poistomenetelmä, jota käytetään usein määritettäessä **Kirjat**-sivulla lisäpoistoprofiili, esimerkiksi muu kuin kausittainen poisto jotain erityistarkoitusta (esimerkiksi verotusta) varten.

## <a name="examples"></a>Esimerkkejä
Hankintahinta: 11 000,00 Odotettavissa oleva jäännösarvo: 1 000,00 Seuraavassa taulukossa on aikavälit ja prosentit, jotka määritetään **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivulla.

| Aikavälin numero | Prosentti |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

Seuraavassa taulukossa esitetään, miten kunkin aikavälin poisto lasketaan.

|  Aikavälin numero | Vuotuisen poistomäärän laskeminen | Nettokirjanpitoarvo aikavälin lopussa |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11 000 – 1 000) × 10 % = 1 000                | 10 000 (11 000 – 1 000)                   |
| 2                | (11 000 – 1 000) × 50 % = 5 000                | 5 000 (10 000 – 5 000)                    |
| 3                | (11 000 – 1 000) × 8 % = 800                   | 4 200 (5 000 – 800)                       |

Jos valitset **Kausifrekvenssi**-kentässä **Kuukausittain**, määrität 12 manuaalisen aikataulun aikaväliä. Seuraavassa taulukossa esitellään kahden ensimmäisen aikavälin poistosummat.

| Väli | Poiston määrä            |
|----------|--------------------------------|
| Tammikuu  | (11 000 – 1 000) × 10 % = 1 000 |
| Helmikuu | (11 000 – 1 000) × 50 % = 5 000 |

Jos valitset *<strong><em>Kausifrekvenssi</em>*-kentässä</strong> <strong>Puolivuosittain</strong>, määrität kaksi manuaalisen aikataulun aikaväliä. Seuraavassa taulukossa esitellään näiden kahden aikavälin poistosummat.

| Väli    | Poiston määrä            |
|-------------|--------------------------------|
| 30. kesäkuuta     | (11 000 – 1 000) × 10 % = 1 000 |
| 31. joulukuuta | (11 000 – 1 000) × 50 % = 5 000 |

Aikavälien prosenttien yhteissumman ei tarvitse olla 100. Näyttöön avautuu kuitenkin sanoma, jos **Käyttöomaisuuserän poistoprofiilisuunnitelma** -sivun **Kumulatiivinen prosentti** -kentän arvo ei ole **100**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]