---
title: Virheellinen rekisterikilpi tai sijaintivirhe mobiilisovelluksessa
description: Kun luet rekisterikilven tunnuksen tai sijainnin, saattaa ilmetä virhe, jonka mukaan se on virheellinen. Varmista, että mikään muu ei ole varannut rekisterikilven tunnusta.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f9f10dbade0d13b8fc4b0fc92981d84e6e28e83e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476279"
---
# <a name="invalid-license-plate-or-location-error-when-scanning-in-the-mobile-app"></a>Virheellinen rekisterikilpi tai sijainti -virhe luettaessa mobiilisovelluksessa

## <a name="symptoms"></a>Oireet

Kun luet rekisterikilven tunnuksen tai sijainnin, saattaa ilmetä seuraava virhesanoma:

> Rekisterikilpi tai sijainti ei kelpaa.

## <a name="resolution"></a>Ratkaisu

Varmista, että mikään muu ei ole varannut rekisterikilven tunnusta. Tämä ongelma esiintyi aiemmin, kun käyttäjän varastonhallinnan mobiilisovelluksessa skannaama arvo oli sekä kelvollinen sijainti että kelvollinen rekisterikilven tunnus. Tämä ongelma kuitenkin korjattiin versiossa 10.0.11.
