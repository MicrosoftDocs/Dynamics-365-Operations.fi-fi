---
title: Kuorman paino voi sisältää vain positiivisia numeroita
description: Kun käsittelet töitä sijaintien väillä, voi ilmetä kuorman painoa koskeva virhe, ja päivityksesi voi peruuntua. Korjaa ongelma seuraavien ohjeiden mukaisesti.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476216"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Kuormituksen painovirhe ja päivitys peruutettu käsiteltäessä työtä eri sijaintien välillä

## <a name="symptoms"></a>Oireet

Jos työ on avoin, kun työ käsitellään pakkaussijainneista valmistelusijainteihin tai valmistelusijainneista laiturisijainteihin, seuraava virhesanoma saattaa avautua:

> Kenttä 'Kuorman paino'(=-%1) voi sisältää vain positiivisia arvoja. Päivitys on keskeytetty.

## <a name="resolution"></a>Ratkaisu

Voit korjata ongelman valitsemalla **Järjestelmänhallinta \> Kausittaiset tehtävät \> Tietokanta \> Yhdenmukaisuustarkistus** ja suorittamalla **Varaston kuorman painon yhdenmukaisuustarkistus** -prosessin.
