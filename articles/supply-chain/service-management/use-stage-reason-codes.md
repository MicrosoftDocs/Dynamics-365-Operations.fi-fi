---
title: Käytä jaksosyykoodeja
description: Käytä syykoodia osoittamaan, miksi huoltotasosopimus on peruutettu tai miksi huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja on ylitetty.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74594871e9eeed86ae2914d1e5a08c0af28ab643
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427227"
---
# <a name="use-stage-reason-codes"></a>Käytä jaksosyykoodeja 

[!include [banner](../includes/banner.md)]


Käytä syykoodia osoittamaan, miksi huoltotasosopimus on peruutettu tai miksi huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja on ylitetty.

Voit myös määrittää syykoodin pakolliseksi, kun huoltotasospimus peruutetaan tai kun huoltotasosopimuksessa asetettu huoltosopimuksen aikaraja ylitetään.

Jos olet määrittänyt syykoodin pakolliseksi, syykoodi on annettava seuraavissa tilanteissa:

  - kun huoltotilaus siirretään tasolle, jossa huoltotilauksen huoltotasosopimuksen ajan tallennus lopetetaan

  - kun huoltotilaus hyväksytään

  - kun ajan tallennus lopetetaan manuaalisesti.

## <a name="set-up-reason-codes"></a>Määritä syykoodit

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltotilaukset** \> **Vaiheen syykoodit**.

2.  Luo uusi syykoodi **Vaiheen syykoodit** -lomakkeella napsauttamalla **Uusi**.

3.  Anna **Vaiheen syykoodi** -kentässä yksilöivä vaiheen syykoodi.

4.  Anna **Kuvaus**-kentässä vaiheen syykoodin kuvaus.

5.  Tallenna muutokset sulkemalla lomake.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Syykoodien vaatiminen, kun huoltotasosopimus peruutetaan

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.

2.  Napsauta **Huollon hallinnan parametrit** -lomakkeessa **Yleiset**-linkkiä ja valitse sitten **Syykoodi peruutettaessa** -valintaruutu.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Syykoodien vaatiminen, kun huoltotasosopimuksen asettama huoltosopimuksen aikaraja ylitetään

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltohallinnan parametrit**.

2.  Napsauta **Huollon hallinnan parametrit** -lomakkeessa **Yleiset**-linkkiä ja valitse sitten **Syykoodi ajan ylittyessä** -valintaruutu.

## <a name="see-also"></a>Lisätietoja

[Huoltotilauksen ajanseurannan aloittaminen ja pysäyttäminen](start-and-stop-time-recording-on-a-service-order.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]