---
title: Käynnissä olevat työt päättyvät, kun viimeisen työn osamäärä raportoidaan
description: Kun työkorttilaitetta käytetään raportoimaan osittainen määrä tuotantotilauksen viimeisessä työssä, kaikki aiemmat työt, joiden tilana on keskeneräinen, päättyvät.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476270"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>Edelliset käynnissä olevat työt päättyvät, kun viimeisen työn osamäärä raportoidaan

## <a name="symptoms"></a>Oireet

Kun työkorttilaitetta käytetään raportoimaan osittainen määrä tuotantotilauksen viimeisessä työssä, kaikki kyseisen tilauksen aiemmat työt, joiden tilana on keskeneräinen, päättyvät automaattisesti.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. **Ilmoita valmiiksi** -välilehden **Tuotantotilauksen oletusarvot** -sivulla on **Tee reitityksen loppumerkintä** -niminen vaihtoehto. Jos tämän aiheen asetuksena on *Kyllä*, reittikortin kirjauskansio kirjataan kun työntekijä käyttää työkorttilaitetta ja työkorttipäätettä viimeisimmän toiminnon ilmoittamiseen. Tämä kirjauskansio kirjaa kaikki toiminnot valmiiksi ja lopettaa kaikki tuotantotyöt. Kun **Tee reitityksen loppumerkintä** -asetuksena on *Kyllä*, järjestelmä ei ota huomioon työn tilaa, jonka työntekijä valitsi, kun tämä ilmoitti viimeisimmän toiminnon. Järjestelmä ei myöskään ota huomioon, ilmoittaako työntekijä täyden vai osittaisen määrän.
