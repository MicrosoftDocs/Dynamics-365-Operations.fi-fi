---
title: Suunniteltu ostotilaus luodaan, kun osto on negatiivisten päivien sisällä
description: Jos kattavuuskoodi on Minimi/maksimi, suunnittelun optimointi luo suunnitellun ostotilauksen, kun osto on negatiivisten päivien sisällä.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026479"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a>Suunniteltu ostotilaus luodaan, kun osto on negatiivisten päivien sisällä

Tietopankin numero: 4614298

## <a name="symptoms"></a>Oireet

Jos kattavuuskoodi on *Minimi/maksimi*, suunnittelun optimointi luo suunnitellun ostotilauksen, kun osto on negatiivisten päivien sisällä.

## <a name="resolution"></a>Ratkaisu

Suunnittelun optimointi ei tue negatiivisia päiviä. Se varmistaa kuitenkin aina, ettei suunniteltuja tilauksia ajoiteta läpimenoajan sisällä suhteessa nykyiseen päivämäärään. Esimerkiksi oston läpimenoaika on 10 päivää, ja ostotilauksen odotetaan saapuvan kahdeksan päivää tästä päivästä. Tässä tapauksessa ostotilausta käytetään kysynnän toimituksena, joka on viisi päivää tästä päivästä alkaen.

Siksi on suositeltavaa säätää läpimenoaikoja siten, että ne kattavat kaikki skenaariot (tai lähes kaikki).
