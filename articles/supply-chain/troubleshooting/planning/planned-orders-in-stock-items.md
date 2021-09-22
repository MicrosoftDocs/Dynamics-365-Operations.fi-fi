---
title: Suunnitellut tilaukset luodaan varastolle tuotantotilauksien kanssa
description: Suunnitellut tilaukset luodaan, vaikka nimikkeitä on varastossa ja niillä on jo tuotantotilaukset.
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: aa803bcd7d43aa36675596050ccbe06831f1724d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476277"
---
# <a name="planned-orders-are-generated-for-in-stock-with-production-orders"></a>Suunnitellut tilaukset luodaan varastolle tuotantotilauksien kanssa

## <a name="symptoms"></a>Oireet

Suunnitellut tilaukset luodaan, vaikka nimikkeitä on varastossa ja niillä on jo tuotantotilaukset.

## <a name="resolution"></a>Ratkaisu

Tämä ongelma on ehkä mahdollista korjata lisäämällä soveltuvien ryhmien **Positiiviset päivät** -arvoa **Kattavuusryhmä**-sivulla. Tämä muutos saa järjestelmän määrittää, voiko käytettävissä olevaa varastoa käyttää kysyntään. Silloin uutta suunniteltua tilausta ei luoda varastossa oleville nimikkeille.
