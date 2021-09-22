---
title: Tälle sijainnille on määritettävä rekisterikilpi
description: Jos saat tämän virhesanoman, kun olet luonut siirtotilauksen WMS-yhteensopivalle varastolle, siirtovaraston oletusarvoisen vastaanottosijainnin kenttä on tyhjä.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2e562ad2b41dd149f215adc83bd2d54e55dccc05
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476195"
---
# <a name="license-plate-specification-error-when-confirming-shipment-for-a-transfer-order"></a>Rekisterikilven määritysvirhe siirtotilauksen lähetystä vahvistettaessa

## <a name="symptoms"></a>Oireet

Jos siirtotilaus luodaan käyttämällä varastoa, jossa on otettu käyttöön edistyksellinen varastonhallinta, ja lähetystä yritetään vahvistaa työn valmistumisen jälkeen, ilmenee seuraava virhesanoma:

> Tälle sijainnille on määritettävä rekisterikilpi.

## <a name="cause"></a>Syy

Tämä aiheutuu siitä, että lähtövaraston kuljetusvaraston **Oletusvastaanottosijainti** -kenttä on tyhjä.

## <a name="resolution"></a>Ratkaisu

Korjaa ongelma määrittämällä oletusvastaanottosijainti kuljetusvarastossa. Varmista, että tämä sijainti on rekisterikilpiohjattu.
