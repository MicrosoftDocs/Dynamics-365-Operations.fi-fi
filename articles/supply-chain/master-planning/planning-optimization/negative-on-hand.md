---
title: Suunnittelu negatiivisilla käytettävissä olevalla määrillä
description: Tässä ohjeaiheessa kerrotaan, miten negatiivista käytettävissä olevaa määrää käsitellään suunnittelun optimoinnissa.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 4eb8f6aee50d74127ecc816af691a96bb1d8966b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469139"
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

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Suunnittelu, kun varaus negatiivista käytettävissä olevan varaston varausta vastaan on olemassa

Jos varastoa oikaistaan fyysisten varausten ollessa olemassa, voi aiheuttaa tilanteen, jossa tilaus varataan fyysisesti negatiivista varastoa vastaan. Koska on olemassa fyysinen varaus, suunnittelun optimointi olettaa, että käytettävissä oleva varasto tukee sitä, vaikka käyttövaraston vastaanottoa ei olisi vielä rekisteröity järjestelmään. Näin ollen oletetaan, että täydennystä ei tarvita eikä luoda suunniteltua tilausta tilauksen määrän täydentämiseen.

Seuraava esimerkki havainnollistaa tätä skenaariota.

### <a name="example"></a>Esimerkki

Järjestelmä konfiguroi sen seuraavasti:

- Tuote *FG* on olemassa, ja sitä on *10* kappaletta. käytettävissä olevassa varastossa.
- Tuotekonfiguraatio mahdollistaa fyysisen negatiivisen varaston.
- Myyntitilaus on olemassa *10* kpl:n määrän osalta. tuotteesta *FG*.
- Myyntitilauksen määrä varataan fyysisesti olemassa olevalle käytettävissä olevalle varastolle.

Tämän jälkeen oikaiset tuotteen *FG* määrän niin, että käytettävissä oleva varasto on 0 (nolla). Koska käytettävissä olevan tuotteen varasto on nolla, myyntitilauksen määrä varataan nyt negatiivista varastoa vastaan. Jos suoritat pääsuunnittelun nyt, myyntitilauksen toimitusta varten ei luoda suunniteltua tilausta, koska suunnittelun optimointi olettaa, että tarvittava käytettävissä oleva varasto on olemassa fyysisen varauksen toimitusta varten.

## <a name="related-resources"></a>Liittyvät resurssit

- [Suunnittelun optimoinnin yleiskatsaus](planning-optimization-overview.md)
- [Suunnittelun optimoinnin aloittaminen](get-started.md)
- [Suunnittelun optimoinnin sopivuusanalyysi](planning-optimization-fit-analysis.md)
- [Suunnitelman historia- ja suunnittelulokien tarkasteleminen](plan-history-logs.md)
- [Suunnittelutyön peruuttaminen](cancel-planning-job.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
