---
title: Osittain lähetettyä kuormaa ei voi vapauttaa varastoon
description: Aiemmissa versioissa osittain lähetettyä kuormaa ei voinut vapauttaa uudelleen käytettäessä tiettyjä toimintoja keskeneräisiin varauksiin. Tämä on korjattu.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476245"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>Osittain lähetettyä kuormaa ei voi vapauttaa varastoon

## <a name="symptoms"></a>Oireet

Osittain lähetettyä kuormaa ei voi vapauttaa varastoon. Kun vapautus varastoon tehdään, Toiminto valmis -sanoma avautuu mutta mitään ei tapahdu eikä jäljellä olevalle määrälle luoda työtä. Tämä ongelma esiintyy käytettäessä kuljetuskuormatoimintoa ja varaus on keskeneräinen.

## <a name="resolution"></a>Ratkaisu

[KB 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) (Osittain lähetetyt kuormat voidaan uudelleenaallottaa ja -käsitellä) on korjattu [versiossa 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15).
