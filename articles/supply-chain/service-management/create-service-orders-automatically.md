---
title: Huoltotilausten luominen automaattisesti
description: Voit luoda huoltotilauksia yhtä huoltosopimusta tai useita huoltosopimuksia varten.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 914df1626b02110264b895e82dc9301f3aa0afce
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985115"
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

  


