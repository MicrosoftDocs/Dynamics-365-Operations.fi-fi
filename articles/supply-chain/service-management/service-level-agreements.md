---
title: Palvelutasosopimukset – yleiskatsaus
description: Palvelutasosopimuksessa asiakas hyväksyy huoltoyrityksen ongelman vastaanottamiseen ja ongelman ratkaisuun perustuvan vähimmäisvasteajan.
author: ShylaThompson
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55d65de5c041bd100bf8267bdbe3c5c5eb061a61
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835915"
---
# <a name="service-level-agreements-overview"></a>Palvelutasosopimukset – yleiskatsaus       

[!include [banner](../includes/banner.md)]


Palvelutasosopimus on huoltoyhtiön ja huoltoasiakkaan välinen sopimus. Palvelutasosopimuksessa asiakas hyväksyy huoltoyrityksen ongelman vastaanottamiseen ja ongelman ratkaisuun perustuvan vähimmäisvasteajan.

Palvelutasosopimus määrittää asiakkaille tarjottavan vakiopalveluntason. Sopimus myös ilmaisee huoltoyritykselle selkeästi huoltotyön valmistumisajankohdan.

Palvelusopimuksia voidaan tehdä haluttu määrä, jotta huoltoasiakkaille voidaan tarjota eri tasoisia palveluita.

## <a name="create-a-service-level-agreement"></a>Palvelutasosopimuksen luominen

1.  Valitse **Huoltohallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Palvelutasosopimukset**.

2.  Kirjoita palvelutasosopimuksen nimi **Palvelutasosopimus**-kenttään.

3.  Kirjoita aika, jonka haluat sallia huoltopyynnöille, jotka liittyvät palvelutasosopimukseen. Valitse sitten kalenteri, jos haluat palvelutasosopimuksen perustuvan tiettyyn kalenteriin.

## <a name="apply-a-service-level-agreement"></a>Palvelutasosopimuksen kohdistaminen

Palvelutasosopimus kohdistetaan suoraan huoltosopimukseen.

Manuaalisesti luotavat ja huoltosopimukseen palvelutasosopimuksen avulla liitettävät huoltotilaukset arvioidaan kyseisen palvelutasosopimuksen avulla.

Automaattisesti luotavia huoltotilauksia ei liitetä palvelutasosopimukseen.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Palvelutasosopimuksen kohdistaminen huoltosopimukseen

1.  Valitse **Palvelunhallinta** \> **Yleinen** \> **Palvelusopimukset** \> **Palvelusopimukset**. Valitse huoltosopimus, jota haluat käyttää palvelutasosopimuksessa, ja valitse sitten **Muokkaa** **toimintoruudussa**.

2.  Valitse **Palvelutasosopimus**-kentässä palvelutasosopimus, joka liitetään.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Palvelutasosopimuksen kohdistaminen huoltosopimusryhmään

1.  Valitse **Palvelunhallinta** \> **Asetukset** \> **Huoltosopimukset** \> **Huoltosopimusryhmät**.

2.  Valitse **Palvelutasosopimus**-kentässä palvelutasosopimus, joka liitetään.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Huoltotilaukseen kuluvan ajan seuraaminen palvelutasosopimuksen mukaan

Luodessasi uuden huoltotilauksen huoltosopimukseen, johon palvelutasosopimus on liitetty, huollon toimituksen aikaväli alkaa ja järjestelmä alkaa seurata toimitusaikaa. Lisäksi voit määrittää seuraavat asetukset:

  - Voit käynnistää ja pysäyttää huoltotilauksen ajanoton, kun haluat rekisteröidä huoltotilauksiin kuluneen kokonaisajan.

  - Voit seurata yhteensopivuutta palvelutasosopimuksessa määritetyllä aikavälillä.

  - Voit määrittää syykoodit, jotka on määritettävä, jos palvelutasosopimuksen aikaväli ylitetään.

## <a name="see-also"></a>Lisätietoja

[Palvelutasosopimusten yhteensopivuuden tarkasteleminen](view-compliance-with-service-level-agreements.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]