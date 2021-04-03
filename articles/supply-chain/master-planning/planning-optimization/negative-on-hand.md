---
title: Suunnittelu negatiivisilla käytettävissä olevalla määrillä
description: Tässä ohjeaiheessa kerrotaan, miten negatiivista käytettävissä olevaa määrää käsitellään suunnittelun optimoinnissa.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ba36d87a991a3b0088800313da2cac3a769f2894
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232299"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Suunnittelu negatiivisilla käytettävissä olevalla määrillä

[!include [banner](../../includes/banner.md)]

Jos järjestelmässä näkyy negatiivinen käytettävissä oleva koostettu määrä, suunnittelumoduuli käsittelee määrää arvona 0 (nolla), mikä helpottaa ylitarjonnan välttämistä. Tämä toiminto toimii seuraavasti:

1. Suunnittelun optimointitoiminto koostaa käytettävissä olevat määrät kattavuusdimensioiden alimmalla tasolla. (Jos esimerkiksi *sijainti* ei ole kattavuusdimensio, suunnittelun optimointi koostaa käytettävissä olevat määrät *varaston* tasolla.)
1. Jos kattavuusdimensioiden alimman tason koostettu kokonaismäärä on negatiivinen, järjestelmä olettaa, että käytettävissä oleva määrä on todella 0 (nolla).

> [!IMPORTANT]
> Suunnittelujärjestelmän tarkkuus on sama kuin syöttötietojen tarkkuus. Jos syöttötiedot ovat virheellisiä, negatiiviset käytettävissä olevat tietueet osoittavat, että varaston tietoja ei ole synkronoitu Microsoft Dynamics 365 Supply Chain Management -sovelluksessa todellisen tilanteen kanssa. Suunnittelun tulos on siis virheellinen. Jos haluat tarkan suunnittelun tuloksen, minimoi negatiivista käytettävissä olevaa määrää näyttävien tietueiden määrä.

## <a name="example-1"></a>Esimerkki 1

Varasto 13 on määritetty seuraavalla tavalla:

- **Kattavuuskoodi:** Min./Maks.
- **Minimi:** 15 kappaletta (kpl)
- **Maksimi:** 25 kpl

Kattavuusdimension alin taso on *varasto*. Seuraavat käytettävissä olevat määrät tallennetaan *sijainnin* tasolle:

- **Toimipaikka 1, varasto 13, sijainti 1:** 20 kpl
- **Toimipaikan 1 varasto 13, sijainti 2:** &minus;8 kpl

Tämän vuoksi varaston 13 käytettävissä oleva koostettu määrä on 12 kpl. (= 20 kpl &minus; 8 kpl).

Tässä tapauksessa suunnittelumoduuli käyttää käytettävissä olevan varaston koostetta, joka on 12 kpl. varastolle 13.

Tuloksena on 13 kappaleen suunniteltu tilaus. (= 25 kpl &minus; 12 kpl) ja täyttää varaston 13 käyttämällä 12 kappaletta. 25 kappaleeseen asti

## <a name="example-2"></a>Esimerkki 2

Varasto 13 on määritetty seuraavalla tavalla:

- **Kattavuuskoodi:** Min./Maks.
- **Minimi:** 15 kpl
- **Maksimi:** 25 kpl

Kattavuusdimension alin taso on *varasto*. Seuraavat käytettävissä olevat määrät tallennetaan *sijainnin* tasolle:

- **Toimipaikka 1, varasto 13, sijainti 1:** 4 kpl
- **Toimipaikan 1 varasto 13, sijainti 2:** &minus;8 kpl

Tämän vuoksi varaston 13 käytettävissä oleva koostettu määrä on &minus;4 kpl. (= 4 kpl &minus; 8 kpl). Se on toisin sanoen pienempi kuin 0 (nolla).

Tässä tapauksessa suunnittelumoduuli olettaa, että varaston 13 käytettävissä oleva määrä on 0 kpl. sen sijaan, että se olisi &minus;4 kpl.

Tuloksena on 25 kappaleen suunniteltu tilaus. (= 25 kpl &minus; 0 kpl) ja täyttää varaston 13 käyttämällä 0 kappaletta. 25 kappaleeseen asti

## <a name="related-resources"></a>Liittyvät resurssit

[Suunnittelun optimoinnin yleiskuvaus](planning-optimization-overview.md)

[Suunnittelun optimoinnin aloittaminen](get-started.md)

[Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)

[Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)

[Suunnittelutyön peruuttaminen](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]