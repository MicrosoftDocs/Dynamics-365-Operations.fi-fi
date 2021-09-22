---
title: Klusteriprofiilia ei löydy
description: Kun käytät saapuvia varastotoimintoja, voi ilmetä virhe, jonka mukaan klusteriprofiilia ei löydy. Varmista, että klusteriprofiilit on määritetty oikein.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476272"
---
# <a name="cluster-profile-cant-be-found"></a>Klusteriprofiilia ei löydy

## <a name="symptoms"></a>Oireet

Kun käytät saapuvia varastotoimintoja, voit saada seuraavan virhesanoman:

> "Laatutilaus %1 on luotu. Klusteriprofiilia ei löydy. Tarkista määrityksesi."

Tämä virhesanoma liittyy vastaanottoprosessiin, jossa laadunhallinta on otettu käyttöön. Ympäristön määritysten mukaan virhesanoman luovan tapahtuman lisätiedot voivat auttaa korjaamaan ongelman.

## <a name="resolution"></a>Ratkaisu

Tarkista ensimmäiseksi klusterikeräilyn määritys ja varmista, että klusteriprofiilit on määritetty oikein. Et voi käyttää mobiililaitteen klusterikeräilyn valikkokohdetta, ellei klusteriprofiileja ole määritetty. Ympäristön mukaan on ehkä tarkistettava myös liittyvät määritykset.
