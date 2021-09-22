---
title: Osamäärän kuormitusta ei voi vapauttaa erä-yllä-hierarkiassa
description: Kun käytetään nimikettä, jossa on erä-yllä-hierarkia, kuormariveillä on määritettävä sijainnin yläpuolella olevia dimensioita, jotta varasto kohdennetaan.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eb7e71cc271903cb689c33777b72862246f2dd42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476203"
---
# <a name="cant-release-a-load-for-partial-quantity-with-batch-above-reservation-hierarchy"></a>Osamäärän kuormitusta ei voi vapauttaa erä-yllä-varaushierarkiassa

## <a name="symptoms"></a>Oireet

Jos käytät nimikettä, jossa käytetään *erä-yllä*-varaushierarkiaa osittaisen määrän **Kuormasuunnittelun työtila** -sivun **Vapauta varastoon** -komento ei toimi, jos yrität vapauttaa kuorman. Seuraava virhesanoma avautuu:

> Jotta kuormituksen rivit voidaan määrittää aaltoon, niiden on määritettävä dimensiot sijainnin yläpuolelle. Voit määrittää nämä dimensiot varaamalla kuormituksen rivin ja luomalla sen uudelleen.

Jos käytät kuitenkin nimikettä, jossa käytetään *erä-alla*-varaushierarkiaa, voit vapauttaa kuorman osittaisen määrän **Kuormasuunnittelun työtila** -sivulta.

## <a name="cause"></a>Syy

Jos dimensio on **Sijainti**-dimension yläpuolella varaushierarkiassa, se on määritettävä ennen vapautusta varastoon. Varasto voidaan kohdistaa onnistuneesti vain, jos sijainnin yläpuolella olevissa dimensioissa ei ole aukkoja.

## <a name="resolution"></a>Ratkaisu

Varmista, että kaikki **Sijainnin** yläpuolella olevat dimensiot on kohdistettu varaamalla kuormarivin ja luomalla sen uudelleen.
