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
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641457"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Myynnin päivityshistorian puhdistustyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia

## <a name="symptoms"></a>Oireet

**Myynnin päivityshistorian puhdistus** -erätyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia.  

## <a name="cause"></a>Syy

Näin voi tapahtua, kun järjestelmäsi sisältää useita myyntipäivityksiä, jotka voivat aiheuttaa suuria määriä myynnin päivitystietoja. Puhdistustyö yrittää siivota kaikki nämä tiedot yhdessä tapahtumassa. Tämän tuloksena työn suoritus voi kestää hyvin kauan tai epäonnistua.

## <a name="resolution"></a>Ratkaisu

Uusi versio **Myynnin päivityshistorian puhdistus** -erätyöstä on käytettävissä Supply Chain Management -versiolle 10.0.19 ja sitä uudemmille versioille. Tämä ominaisuus ei ole oletusarvoisesti käytössä. Tietoja siitä, miten toiminto toimii ja miten se otetaan käyttöön ominaisuuksien hallinnassa, on kohdassa [Myyntihistorian puhdistuksen suorituskyvyn parannukset](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

