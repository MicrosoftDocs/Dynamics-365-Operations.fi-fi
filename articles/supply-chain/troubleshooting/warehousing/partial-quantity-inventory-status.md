---
title: Tee varaston tilan muutos osittaisen määrän työtä varten
description: Tällä sivulla selitetään, miten luodaan valikkokohde, joka sisältää asianmukaiset asetukset siihen, että työntekijät voivat tehdä varaston tilamuutoksen erän osittaiselle määrälle.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476178"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Ota käyttöön varaston tilan muutos osittaisen määrän työtä varten

## <a name="symptoms"></a>Oireet

Sinun on tehtävä erän osittaisen määrän varaston tilan muutos.

## <a name="resolution"></a>Ratkaisu

Varastonhallinnan mobiilisovellukseen voidaan luoda valikkovaihtoehto, jolla työntekijät voivat tehdä tämän muutoksen. Luo (tai muokkaa) **Mobiililaitteen valikkovaihtoehdot** -sivulla valikkovaihtoehto, jossa on seuraavat asetukset:

- **Tila:** *Työ*
- **Käytä aiemmin luotua työtä:** *Ei*
- **Työn luontiprosessi:** *Siirto*
- **Näytä varaston tila:** *Kyllä*

Sivulla voi määrittää tarvittaessa myös muita kenttiä.
