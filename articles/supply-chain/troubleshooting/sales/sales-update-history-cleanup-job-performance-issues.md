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
ms.openlocfilehash: 371a8c7178cd7c5091d6dd9a91d0ee03b943a269
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103185"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Myynnin päivityshistorian puhdistustyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia

## <a name="symptoms"></a>Oireet

**Myynnin päivityshistorian puhdistus** -erätyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia.  

## <a name="cause"></a>Syy

Näin voi tapahtua, kun järjestelmäsi sisältää useita myyntipäivityksiä, jotka voivat aiheuttaa suuria määriä myynnin päivitystietoja. Puhdistustyö yrittää siivota kaikki nämä tiedot yhdessä tapahtumassa. Tämän tuloksena työn suoritus voi kestää hyvin kauan tai epäonnistua.

## <a name="resolution"></a>Ratkaisu

Uusi versio **Myynnin päivityshistorian puhdistus** -erätyöstä on käytettävissä Supply Chain Management -versiolle 10.0.19 ja sitä uudemmille versioille. Tämä ominaisuus on oletusarvoisesti pois käytöstä. Tietoja siitä, miten toiminto toimii ja miten se otetaan käyttöön ominaisuuksien hallinnassa, on kohdassa [Myyntihistorian puhdistuksen suorituskyvyn parannukset](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

