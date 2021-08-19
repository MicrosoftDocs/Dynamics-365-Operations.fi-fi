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
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778503"
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
