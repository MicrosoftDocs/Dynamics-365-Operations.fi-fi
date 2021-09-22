---
title: Nimikkeen RM:ää ei voi varata, kun tuotantotilaus vapautetaan
description: 'Tuotantotilausta vapautettaessa voi ilmetä virhe: "Nimikkeen RM:ää ei voitu varata täysin." Varmista, että koko määrä on käytettävissä, tai varaa nimikkeet manuaalisesti.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476255"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Nimikkeen RM:ää ei voi varata kokonaan, kun tuotantotilaus vapautetaan

## <a name="symptoms"></a>Oireet

Jos kaikki tuoterakennerivinimikkeet eivät ole käytettävissä, kun tuotantotilaus vapautetaan varastoon , ja **Vapauta varastoon** -käytännöksi on määritetty *Edellytä täyttä varaamista*, seuraava virhesanoma avautuu:

> Nimikettä RM ei voitu varata täysin. Varmista, että koko määrä on käytettävissä, tai varaa nimikkeet manuaalisesti, mikäli tuoterakennerivin Varaus-kentän arvoksi on määritetty Manuaalinen tai Aloitettu. Tilausta ei voitu vapauttaa varastoon, koska kaikkia materiaaleja ei voitu varata.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus, ja se toimii odotetulla tavalla. Korjaa tämä ongelma noudattamalla virhesanoman "Varmista, että koko määrä on käytettävissä, tai varaa nimikkeet manuaalisesti, mikäli tuoterakennerivin Varaus-kentän arvoksi on määritetty Manuaalinen tai Aloitettu." ohjeita.
