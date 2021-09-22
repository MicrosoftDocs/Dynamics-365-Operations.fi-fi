---
title: Varastonhallinnan prosesseja on käytössä
description: Kun varaat tai vapautat töitä, saatat saada sanoman, jonka mukaan varastonhallinnan prosesseja on käytössä. Voit korjata ongelman jollakin seuraavista tavoista.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476180"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Työtä ei voi varata tai vapauttaa, koska prosesseja käytetään parhaillaan

## <a name="symptoms"></a>Oireet

Kun käytetään erillistä valmistusta, ilmenee seuraava virhe:

> Varastonhallinnan prosesseja on käytössä. Jos työrivejä ei ole vielä rekisteröity, voit peruuttaa luodun työn sekä mahdolliset kuorma- tai toimitusrivit ja jatkaa sitten keräily- tai lähetysprosessin kanssa.

## <a name="cause"></a>Syy

Tämä ongelma esiintyy, jos rivin työtä yritetään varata tai vapauttaa, kun varastotapahtuman tila on *Keräilty*, mikä ilmaisee, että materiaali on keräilty.

## <a name="resolution"></a>Ratkaisu

Ongelma korjataan jollakin seuraavista tavoista:

- Muuta tuotantotilauksen tilaksi jälleen *Ennakkolaskettu* tai *Vapautettu*.
- Avaa kyseisen tuotantotilauksen tietosivu. Kumoa kaikkien kerättyjen tapahtumien keräys valitsemalla toimintoruudun **Varasto**-välilehden **Pysäytä**-ryhmässä **Pysäytä ja kumoa keräys**. Käsittele sitten tuotantotilaus valitsemalla **Poista pysäytys**.

*Kumoa keräys*- ja *Pysäytä*-toimintojen selitys:
  
- **Kumoa keräys** – Tämä toiminto kumoaa niiden tuoterakennerivien ja kaavarivien varastotapahtumien tilan, joissa tilana on *Kerätty*, *Tilauksessa* ja niiden väliin jäävät tilat. Kun raaka-aineiden keräilytyö on valmis, rivien tilaksi määritetään *Kerätty*. Tämä tila estää tuotantotilauksen palauttamisen *Luotu*-tilaan. Tässä tapauksessa tapahtuman voi palauttaa *Kumoa keräys* -toiminnolla *Kerätty*-tilasta ja palauttaa tuotantotilauksen *Luotu*-tilaan.
- **Pysäytä** – Tämä toiminto määrittää **Pysäytetty**-merkinnän tuotantotilaukseen, jolloin tilauksen tilaa ei voi päivittää. **Pysäytetty**-merkintä näkyy tuotantotilauksen tietosivun **Varasto**-pikavälilehdessä.

> [!NOTE]
>
> - Painikkeet ovat näkyvät vain silloin, kun tuotantotilaus luodaan nimikkeille, joissa varastoprosessit on otettu käyttöön.
> - **Pysäytä**-ryhmä näkyy vain tuotantotilauksen tietosivun toimintoruudun **Varasto**-välilehdessä. Se ei näy **Tuotantotilaukset**-luettelosivun **Varasto**-pikavälilehdessä.
