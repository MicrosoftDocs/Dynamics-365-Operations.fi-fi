---
title: Pääsuunnittelu ajoittaa enemmän kuin käytettävissä olevan kapasiteetin
description: Pääsuunnittelu ei näytä noudattavan kapasiteettirajoituksia ja sen aikataulutus ylittää käytettävissä olevan kapasiteetin
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476242"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Pääsuunnittelu ajoittaa enemmän kuin käytettävissä olevan kapasiteetin

## <a name="symptoms"></a>Oireet

Pääsuunnittelu ei näytä noudattavan kapasiteettirajoituksia ja sen aikataulutus ylittää käytettävissä olevan kapasiteetin

Jos käytettävässä toiminnon aikatauluttamisessa on rajallinen kapasiteetti ja reititys määrittää yhdistelmätarpeet sekä resurssiryhmälle että yksittäisille resursseille, on olemassa pieni ylivarauksen mahdollisuus, joka johtuu algoritmin tavasta tarkistaa kapasiteettiristiriidat. Tämä ylivaraus voi esiintyä, kun pääsuunnittelun suorittamiseen käytetään lisätyöasemia. Se tapahtuu todennäköisimmin siinä tapauksessa, että useilla töillä on suhteellisen lyhyt suoritusaika.

## <a name="resolution"></a>Ratkaisu

Jos on ylivarauksia ei saa missään tapauksessa esiintyä toimintojen ajoittamisessa, voit tehdä pääsuunnittelun ajoituksesta yksisäikeisen ottamalla **Tarkka rajallinen kapasiteetti toimintojen ajoituksessa** -asetuksen käyttöön **Pääsuunnittelun parametrit** -sivulla. Tämä asetus ei ole oletusarvoisesti käytettävissä. Se on lisättävä manuaalisesti sivulle mukautustoimintojen avulla. Tätä asetusta käytettäessä ajoitus hidastuu, koska rinnakkainen käsittely ei ole käytössä.
