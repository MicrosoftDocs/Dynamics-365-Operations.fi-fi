---
title: Myynnin päivityshistorian puhdistustyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia
description: Myyntihistorian puhdistuksen erätyö voi epäonnistua tai kestää hyvin kauan, jos myyntipäivityksen tietoja on paljon.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920071"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Myynnin päivityshistorian puhdistustyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia

## <a name="symptoms"></a>Oireet

**Myynnin päivityshistorian puhdistus** -erätyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia.  

## <a name="cause"></a>Syy

Näin voi tapahtua, kun järjestelmäsi sisältää useita myyntipäivityksiä, jotka voivat aiheuttaa suuria määriä myynnin päivitystietoja. Puhdistustyö yrittää siivota kaikki nämä tiedot yhdessä tapahtumassa. Tämän tuloksena työn suoritus voi kestää hyvin kauan tai epäonnistua.

## <a name="resolution"></a>Ratkaisu

Uusi versio **Myynnin päivityshistorian puhdistus** -erätyöstä on käytettävissä Supply Chain Management -versiolle 10.0.19 ja sitä uudemmille versioille. Tämä ominaisuus ei ole oletusarvoisesti käytössä. Tietoja siitä, miten toiminto toimii ja miten se otetaan käyttöön ominaisuuksien hallinnassa, on kohdassa [Myyntihistorian puhdistuksen suorituskyvyn parannukset](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

