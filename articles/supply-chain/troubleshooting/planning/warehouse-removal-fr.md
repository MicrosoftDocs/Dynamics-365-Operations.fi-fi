---
title: Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä
description: Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 96af593d2e8a738258fe614f0f252620cb48c5f19eeb4425c9659ee6f9cd8c0c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741210"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä

Tietopankin numero: 4614408

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun **Varasto**-dimensiota ei ole määritetty **Ennustedimensiot**-välilehdellä **Kysynnän ennusteen parametri** -sivulla. **Varasto**-sarake näkyy kuitenkin **Kysynnän ennuste** -sivulla (**Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteyksikkö \> Kysynnän ennusteen rivit**).

## <a name="resolution"></a>Ratkaisu

**Ennustedimensiot**-välilehden asetukset **Kysynnän ennusteen parametri** -sivulla ei vaikuta **Kysynnän ennuste** -sivuun. Ne ohjaavat perusennustetta, joka luodaan ja näkyy oikaistussa kysyntäennusteessa. Ne eivät kuitenkaan ohjaa dimensioita, joita "todellinen" kysyntäennuste edellyttää. Valtuuttamalla **Oikaistu kysynnän ennuste** -sivulla näkyvät tietueet voit muuntaa ne ennustemallin "todellisiksi" ennustetapahtumiksi. Tätä mallia voidaan sitten käyttää pääsuunnittelussa.

**Kysynnän ennuste** -sivulla kysynnän ennusteen riveillä näkyvät "todellisen" ennusteen dimensiot ovat osa varastodimensioita. (Käyttäytyminen muistuttaa myyntitilausrivien toimintatapaa.) Jos järjestelmää ei ole määritetty käyttämään **varastoa** pakollisena varastodimensiona, voit piilottaa sarakkeen mukauttamalla sivun.
