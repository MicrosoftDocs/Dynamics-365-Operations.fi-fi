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
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570307"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Myynnin päivityshistorian puhdistustyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia

## <a name="symptoms"></a>Oireet

**Myynnin päivityshistorian puhdistus** -erätyö epäonnistuu tai siinä on suorituskykyyn liittyviä ongelmia.  

## <a name="cause"></a>Syy

Näin voi tapahtua, kun järjestelmäsi sisältää useita myyntipäivityksiä, jotka voivat aiheuttaa suuria määriä myynnin päivitystietoja. Puhdistustyö yrittää siivota kaikki nämä tiedot yhdessä tapahtumassa. Tämän tuloksena työn suoritus voi kestää hyvin kauan tai epäonnistua.

## <a name="resolution"></a>Ratkaisu

Uusi versio **Myynnin päivityshistorian puhdistus** -erätyöstä on käytettävissä Supply Chain Management -versiolle 10.0.19 ja sitä uudemmille versioille. Tämä ominaisuus on oletusarvoisesti pois käytöstä. Tietoja siitä, miten toiminto toimii ja miten se otetaan käyttöön ominaisuuksien hallinnassa, on kohdassa [Myyntihistorian tietojen puhdistuksen ajoittaminen](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

