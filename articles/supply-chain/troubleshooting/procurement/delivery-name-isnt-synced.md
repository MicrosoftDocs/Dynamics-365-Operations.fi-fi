---
title: Toimituksen nimeä ei synkronoida ostotilauksen toimitusosoitteen muuttamisen jälkeen
description: Kun muutat ostotilauksen otsikon toimitusosoitetta, toimituksen nimeä ei synkronoida
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 588d1ef6250d249aa4fc9da4f5125e9a34c0255f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476196"
---
# <a name="the-delivery-name-isnt-synced-after-changing-a-purchase-order-delivery-address"></a>Toimituksen nimeä ei synkronoida ostotilauksen toimitusosoitteen muuttamisen jälkeen

## <a name="symptoms"></a>Oireet

Ostotilauksen otsikossa oleva osoite päivitetään osoitteeksi, joka ei ole toimitusosoite. Vaikka osoite päivitetään ostotilauksessa, toimituksen nimeä ei päivitetä päivitetyn osoitteen perusteella.

## <a name="resolution"></a>Ratkaisu

Tämä on suunniteltu ominaisuus. Valittu osoite on luokiteltava toimitusosoitteeksi. Muussa tapauksessa toimituksen nimeä ei päivitetä valitun osoitteen perusteella.
