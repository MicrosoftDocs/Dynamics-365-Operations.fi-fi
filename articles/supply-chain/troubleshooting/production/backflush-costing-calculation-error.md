---
title: Jälkikustannuslaskennan laskentavirhe varaston sulkemisen aikana
description: Aiemmissa versioissa olet voinut saada jälkikustannuslaskennan virheen varaston sulkemisen yhteydessä. Tämä ongelma on korjattu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476213"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Jälkikustannuslaskennan laskentavirhe varaston sulkemisen aikana

## <a name="symptoms"></a>Oireet

Jos versiota 10.0.13 edeltävissä versioissa ei käytetä lean-tuotannon kustannuslaskentaan, seuraava virheellinen varoitussanoma annetaan varastoa suljettaessa:

> Olet sulkemassa varaston päivämäärällä %1. Jälkikustannuslaskentaa ei suoriteta päivämäärällä %1, jolla kohdistuskauden loppu on rekisteröity. Muista suorittaa jälkikustannuslaskentaa päivämäärällä %1, jolla kohdistuskausi päättyy. Varastojen arvostus, myytyjen tuotteiden kustannukset ja varianssit eivät ehkä ole oikein alareskontrassa tai kirjanpidossa, kunnes tämä on suoritettu.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma on korjattu versiosta 10.0.13 alkaen. Lisätietoja on artikkelissa [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
