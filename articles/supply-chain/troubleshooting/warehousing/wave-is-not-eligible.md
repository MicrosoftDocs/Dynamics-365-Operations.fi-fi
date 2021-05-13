---
title: Aalto ei ole puhdistuskelpoinen.
description: Aalto ei ole puhdistuskelpoinen.
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3e5142cf40a6c0d308e8e952bbe17e85b498826d
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924324"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Aalto ei ole puhdistuskelpoinen.

Virhekoodi: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Oireet

Järjestelmä näyttää seuraavan virhesanoman:

> Aaltoa %1 ei voi tyhjentää.

Aallon tietoja ei voi puhdistaa.  

## <a name="cause"></a>Syy

Aaltoa käsitellään parhaillaan, kuten jokin seuraavista ehdoista on osoittanut:

- **Aallon tila** -kentän arvona on *Suoritetaan*.
- Kun valitset **Erätyö** **Aalto**-ryhmässä toimintoruudun **Aalto**-välilehdellä, **Tila**-kentän arvoksi ei määritetä *Päättynyt*, *Virhe* tai *Peruutettu*. Siksi erätyö on tällä hetkellä käynnissä.

## <a name="resolution"></a>Ratkaisu

Valitse toimintoruudun **Aalto**-välilehden **Aalto**-ryhmässä **Erätyö** ja seuraa jotakin seuraavista vaiheista:

- Jos **Tila**-kentän arvona on *Suoritetaan*: Valitse toimintoruudussa **Erätyö**-välilehdellä **Erätyö**-ryhmässä **Näytä tehtävät**. Voit valvoa edistymistä päivittämällä **Etätehtävät**-sivun.
- Jos **Tila**-kentän arvona ei ole *Suoritetaan*: Valitse toimintoruudussa **Erätyö**-välilehdellä **Toiminnot**-ryhmässä **Muuta tila**. Valitse **Valitse uusi tila** -kentässä *Odottaa*. Valitse sitten **OK**.
