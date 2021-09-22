---
title: Automaattisen varauksen kehote näkyy saatavissa olevan varaston yhteydessä
description: Kun käytät nimikettä varastossa, jossa varastoprosessit eivät ole käytössä, näkyviin tulee automaattisen varauksen kehote. Määritä kaikki sijainnin yläpuolella olevat dimensiot.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a15502ce8c5bc61d37cedd746985176408a2f362
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476265"
---
# <a name="auto-reservation-prompt-for-batch-number-is-shown-even-with-available-inventory"></a>Eränumeron automaattisen varauksen kehote näkyy myös saatavissa olevan varaston yhteydessä

## <a name="symptoms"></a>Oireet

Kun käytät nimikettä, jolla on *erä-yllä*-varaushierarkia varastossa, joka ei ole ottanut fyysisen varastoinnin prosesseja käyttöön, ja automaattinen varaus on käytössä, eränumeron automaattinen varauskehote tulee näyttöön, vaikka keräilyyn olisi käytettävissä vain yksi erä.

Kun käytät samaa nimikettä varastossa, jossa fyysisen varastoinnin prosessit ovat käytössä, automaattista varauskehotetta ei näytetä.

## <a name="resolution"></a>Ratkaisu

Jos varaushierarkiaksi on määritetty *erä-yllä* tai *sarja-yllä*, viitattu dimensio (**Eränumero** tai **Sarjanumero**) on aina määritettävä kysyntätilauksissa. Fyysisen varastoinnin prosessit voivat ehkä täydentää tietoja, jos käytettävissä on yksi erä- tai sarjanumero. Koska varastolle ei kuitenkaan ole otettu käyttöön fyysisen varastoinnin prosesseja, käyttäjän on aina määritettävä kaikki **Sijainti**-kentän yläpuolella olevat dimensiot.
