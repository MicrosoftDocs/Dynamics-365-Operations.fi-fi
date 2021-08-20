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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756748"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Asiakkaalle näkyvää myyntitilausta ei voi laskuttaa

Tietopankin numero: 4611793

## <a name="symptoms"></a>Oireet

Et voi enää laskuttaa alkuperäistä myyntitilausta ja alkuperäistä suoratoimitusostotilausta sen jälkeen, kun **Kirjaa lasku automaattisesti** -asetus on käytössä toimittajan **Konsernin sisäinen** -sivulla.

## <a name="resolution"></a>Ratkaisu

Konsernin sisäisen ja suoratoimitustilauslaskujen synkronointia ohjaavat ja pakottavat parametrit, jotka on kuvattu kohdassa [Konsernin sisäisen tilauksen kirjausparametrien määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Kun olet määrittänyt nämä parametrit, sinun on ensin laskutettava konsernin sisäinen myyntitilaus. Tämän jälkeen alkuperäiset myyntitilaukset ja ostotilaukset synkronoidaan.
