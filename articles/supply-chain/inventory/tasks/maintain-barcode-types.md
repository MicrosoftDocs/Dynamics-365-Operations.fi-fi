---
title: Viivakoodityyppien ylläpito
description: Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana.
author: perlynne
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4102f8036c0aede7c8a2adcaa9b8799a71ac7ada
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441286"
---
# <a name="maintain-bar-code-types"></a>Viivakoodityyppien ylläpito

[!include [banner](../../includes/banner.md)]

Tässä menettelyssä käsitellään, miten määritetään uusi viivakoodimääritys, jota voidaan sitten käyttää keräilyluetteloraportin osana. Voit käydä tämän menettelyn läpi emotietojen yrityksen USMF avulla tai käyttää omia tietojasi. Jos käytössä on USMF, voit käyttää esimerkiksi esillä olevia arvoja. Yleensä varastopäällikkö tekee nämä tehtävät.

1. Valitse **Viivakoodit**.
1. Valitse **Uusi**.
1. Kirjoita **Viivakoodiasetukset**-kenttään arvo.
1. Kirjoita **Kuvaus**-kenttään arvo.
1. Valitse **Viivakoodityyppi**-kentässä vaihtoehto.
    * Jos käytössä on USMF, valitse Koodi 39.
1. Määritä **Muodon tunnus** -kentässä viivakoodin muodon yksilöivä tunnus. Viivakoodin muotoja käytetään viivakoodien luomiseen ja tunnistamaan myyntipistejärjestelmään luettavat viivakoodit nopeasti. Lisätietoja: [Viivakoodin muotojen määritys](../../../commerce/set-up-bar-code-masks.md).
1. Lisää **Koko**-kenttään numero.
1. Anna **Enimmäispituus**-kentässä numero.
1. Valitse **Tallenna**.
1. Sulje sivu.
1. Valitse **Varasto ja varastonhallinnan parametrit**.
1. Anna tai valitse **Viivakoodiasetukset**-kentässä arvo.
    * Valitse aiemmin luodut viivakoodiasetukset. Ota kuitenkin huomioon, että viivakoodimuodon on vastattava prosessissa käytetyn tietuetyypin yksilöllistä tunnistetta. Esimerkiksi keräilyreittien viivakoodimuodon on vastattava keräilyreittiviitteen muotoa, joka on yleensä numerosarja.  
1. Valitse **Tallenna**.
1. Sulje sivu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
