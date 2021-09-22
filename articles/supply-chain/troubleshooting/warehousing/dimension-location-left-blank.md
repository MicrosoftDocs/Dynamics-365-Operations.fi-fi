---
title: Dimensiosijainti ei voi olla tyhjä, jos sarjanumero on määritetty
description: Jos saat tämän virhesanoman, kun vahvistat lähetyksen, kun olet luonut sarjanimikkeelle siirtotilauksen, oletusarvoisen vastaanottosijainnin kenttä on tyhjä.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6f58c72438d5d1d93e59e46525debd65d44d9a76
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476264"
---
# <a name="error-when-confirming-shipment-after-creating-a-transfer-order-for-a-serial-item"></a>Virhe vahvistettaessa lähetystä sarjanumeronimikkeen siirtotilauksen luonnin jälkeen

## <a name="symptoms"></a>Oireet

Jos sarjanimikkeelle luodaan siirtotilaus käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja kun lähetystä yritetään vahvistaa työn valmistumisen jälkeen, tämä virhesanoma avautuu:

> Dimensiosijainti ei voi olla tyhjä, jos dimension sarjanumero on määritetty.

## <a name="cause"></a>Syy

Tämä aiheutuu siitä, että lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä.

## <a name="resolution"></a>Ratkaisu

Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa. Varmista, että tämä sijainti on rekisterikilpiohjattu.
