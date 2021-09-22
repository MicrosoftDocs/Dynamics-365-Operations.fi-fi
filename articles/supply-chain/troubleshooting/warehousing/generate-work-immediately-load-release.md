---
title: Keräilytyön luominen heti, kun kuorma vapautetaan
description: Jos työ on luotava heti, kun kuorma vapautetaan, aaltomalli on määritettävä vastaavasti. Tämä sivu esittelee vaiheet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476246"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Keräilytyötä ei luoda heti, kun lähtevä kuorma vapautetaan

## <a name="symptoms"></a>Oireet

Lähtevä kuorma luodaan käyttämällä myynti- tai siirtotilausta ja vapauttamalla kuorma varastoon. Keräilytyötä ei kuitenkaan ole vielä luotu.

## <a name="resolution"></a>Ratkaisu

Jos työ on luotava heti, kun kuorma vapautetaan, aaltomalli on määritettävä vastaavasti. Määritä aaltomallin seuraavissa asetuksissa *Kyllä*:

- Automatisoi aallon luonti
- Käsittele aalto, kun se vapautetaan varastoon
- Automatisoi aallon vapautus
