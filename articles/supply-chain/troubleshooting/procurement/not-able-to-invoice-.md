---
title: Asiakkaalle näkyvää myyntitilausta ei voi laskuttaa
description: Et voi enää laskuttaa alkuperäistä myyntitilausta ja alkuperäistä suoratoimitusostotilausta sen jälkeen, kun Kirjaa lasku automaattisesti -asetus on käytössä.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026469"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Asiakkaalle näkyvää myyntitilausta ei voi laskuttaa

Tietopankin numero: 4611793

## <a name="symptoms"></a>Oireet

Et voi enää laskuttaa alkuperäistä myyntitilausta ja alkuperäistä suoratoimitusostotilausta sen jälkeen, kun **Kirjaa lasku automaattisesti** -asetus on käytössä toimittajan **Konsernin sisäinen** -sivulla.

## <a name="resolution"></a>Ratkaisu

Konsernin sisäisen ja suoratoimitustilauslaskujen synkronointia ohjaavat ja pakottavat parametrit, jotka on kuvattu kohdassa [Konsernin sisäisen tilauksen kirjausparametrien määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Kun olet määrittänyt nämä parametrit, sinun on ensin laskutettava konsernin sisäinen myyntitilaus. Tämän jälkeen alkuperäiset myyntitilaukset ja ostotilaukset synkronoidaan.
