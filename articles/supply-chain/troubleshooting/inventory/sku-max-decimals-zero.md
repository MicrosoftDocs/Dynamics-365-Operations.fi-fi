---
title: Varastointiyksikön desimaalien enimmäismäärä on 0
description: Kun varastotapahtuma tai varastovaraus yritetään kirjata, virhesanoma "Varastointiyksikön desimaalien enimmäismäärä on 0" avautuu.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476267"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Varastointiyksikön desimaalien enimmäismäärä on 0


## <a name="symptoms"></a>Oireet

Kun yrität kirjata varastotapahtuman tai varastovarauksen, näkyviin tulee seuraava virhesanoma:

> Varastointiyksikön desimaalien enimmäismäärä on 0.

Tämä ongelma esiintyy, kun varastotapahtuman määräksi määritetään desimaaliarvo, joka on kentän tukemaa tarkkuustasoa pienempi. Varastotapahtuman määräksi on esimerkiksi määritetty *0,5*, mutta määränä tuetaan vain kokonaislukua. Tämän vuoksi arvon pitäisi olla *1* eikä *0,5*.

## <a name="resolution"></a>Ratkaisu

1. Seuraavan komentosarjan suorittaminen SQL Server -esiintymässä pyöristää varastotapahtumien määrät. Tämä komentosarja korjaa **inventTrans**-taulukon arvot.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Käytettävissä olevan varaston yhdenmukaisuustarkistuksen suorittaminen siten, että **korjaa virhe** -vaihtoehto on valittu. Näin tarkistetaan, että **inventSum**-taulukossa on oikeat arvot.

> [!IMPORTANT]
> On suositeltavaa, että komentosarjaa muokataan huolellisesti ympäristöön sopivaksi ja että se testataan testiympäristössä ja sen tuloksena saatava tiedot tarkistetaan, ennen kuin komentosarja suoritetaan tuotantoympäristössä.
