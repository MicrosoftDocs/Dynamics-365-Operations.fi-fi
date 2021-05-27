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
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026476"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a>Varaston kysynnän ennustedimensiota ei voi poistaa ennusteriveistä

Tietopankin numero: 4614408

## <a name="symptoms"></a>Oireet

Tämä ongelma ilmenee, kun **Varasto**-dimensiota ei ole määritetty **Ennustedimensiot**-välilehdellä **Kysynnän ennusteen parametri** -sivulla. **Varasto**-sarake näkyy kuitenkin **Kysynnän ennuste** -sivulla (**Pääsuunnittelu \> Ennuste \> Manuaalinen ennusteyksikkö \> Kysynnän ennusteen rivit**).

## <a name="resolution"></a>Ratkaisu

**Ennustedimensiot**-välilehden asetukset **Kysynnän ennusteen parametri** -sivulla ei vaikuta **Kysynnän ennuste** -sivuun. Ne ohjaavat perusennustetta, joka luodaan ja näkyy oikaistussa kysyntäennusteessa. Ne eivät kuitenkaan ohjaa dimensioita, joita "todellinen" kysyntäennuste edellyttää. Valtuuttamalla **Oikaistu kysynnän ennuste** -sivulla näkyvät tietueet voit muuntaa ne ennustemallin "todellisiksi" ennustetapahtumiksi. Tätä mallia voidaan sitten käyttää pääsuunnittelussa.

**Kysynnän ennuste** -sivulla kysynnän ennusteen riveillä näkyvät "todellisen" ennusteen dimensiot ovat osa varastodimensioita. (Käyttäytyminen muistuttaa myyntitilausrivien toimintatapaa.) Jos järjestelmää ei ole määritetty käyttämään **varastoa** pakollisena varastodimensiona, voit piilottaa sarakkeen mukauttamalla sivun.
