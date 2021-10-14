---
title: Huoltotilausten luominen automaattisesti
description: Voit luoda huoltotilauksia yhtä huoltosopimusta tai useita huoltosopimuksia varten.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fc63a720dd06c85be17ca61de1fe7c25f1cf3f7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571542"
---
# <a name="create-service-orders-automatically"></a>Huoltotilausten luominen automaattisesti    

[!include [banner](../includes/banner.md)]


Voit luoda huoltotilauksia yhtä huoltosopimusta tai useita huoltosopimuksia varten. Kun huoltotilaukset on luotu, voit tarkastella niitä **Huoltotilaukset**-lomakkeessa.

Huoltotilauksia luodaan vain huoltosopimuksen voimassaolokaudelle. Jos **Luo huoltotilauksia** -lomakkeessa määritetty jakso on ennen huoltosopimuksen alkupäivämäärää tai loppupäivämäärän jälkeen, huoltotilauksia luodaan vain jaksolle, joka kuuluu huoltosopimukseen.

Kun huoltotilauksia luodaan manuaalisesti tai automaattisesti huoltosopimusriviltä, huoltotilauksen on sijoituttava alkamis- ja päättymispäivän väliselle kaudelle, ellei rivillä määritetä päättymispäivää.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Huoltotilausten automaattinen luonti huoltosopimukseen

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**.

2.  Valitse huoltosopimus.

3.  Valitse **Toimita**-välilehti ja valitse sitten **Suunnitellut huoltotilaukset**.

4.  Määritä huoltojakso antamalla päivämäärät **Aloituspäivämäärä**- ja **Lopetuspäivämäärä**-kenttiin.

5.  Valitse **Näytä infoloki** -valintaruutu, niin näyttöön tulee luotujen huoltotilausten luettelo.

6.  Valitse tapahtumatyypit **Sisällytä tapahtumatyypit** -kenttäryhmässä. Tapahtumatyypit vastaavat huoltosopimuksessa luotuja rivejä, ja kukin valittu tapahtumatyyppi luo useita huoltotilauksia sen mukaan, mikä huoltoväli huoltosopimuksen rivillä on määritetty.

7.  Valitse **Jatkuva**-valintaruutu, jos haluat luoda huoltotilauksia, jotka puuttuvat huoltotilausten jatkuvasta sarjasta.

8.  Napsauta **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Huoltotilausten automaattinen luonti useisiin huoltosopimuksiin

1.  Valitse **Huoltohallinta** \> **Kausittainen** \> **Huoltotilaukset** \> **Luo huoltotilauksia**

2.  Napsauta **Valitse**, niin voit lisätä tai poistaa ehdot, joiden avulla luot huoltotilauksia.

3.  Valitse **OK**.

## <a name="see-also"></a>Lisätietoja

[Huoltotilaukset](service-orders.md)

[Huoltotilausten automaattinen luonti](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]