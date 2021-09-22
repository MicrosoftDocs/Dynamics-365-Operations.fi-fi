---
title: Määrä ei ole kelvollinen poimintatyölle, jossa on useita rekisterikilpiä
description: Kun poimintatyössä on useita rekisterikilpiä yhdessä sijainnissa, määrä ei ole kelvollinen kpl-yksikköä varten. Tarkista, että seuraavat kentät ovat oikein.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476187"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Määrä ei kelpaa, kun keräystyötä on useaan rekisterikilpeen liittyen yhdessä sijainnissa

## <a name="symptoms"></a>Oireet

Kun poimintatyössä on useita rekisterikilpiä yhdessä sijainnissa, määrä ei ole kelvollinen *kpl*-yksikköä varten ja saat seuraavan virhesanoman:

> Määrä ei kelpaa yksikköä 1 % varten.

## <a name="resolution"></a>Ratkaisu

Varmista, että vapautetun tuotteen tai tuotevariantin **Yksikön sarjaryhmän tunnus**- ja **Yksikkömuunnokset**-kentät on määritetty oikein.

Huomaa, että virhesanomaa on parannettu versiossa 10.0.15 siten, että odotettu määrä näytetään (katso [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Uusi virhesanoma on:

> Määrä ei kelpaa. Odotettiin %1 %2.
