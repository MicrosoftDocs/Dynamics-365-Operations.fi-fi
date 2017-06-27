---
title: Dimensioon perustuva tuotekonfigurointi
description: "Dimensioihin perustuva tuotekonfiguraatio edustaa yksinkertaista ratkaisua useiden varianttien luomiselle yhdestä päätuotteesta ja sen tuoterakenteesta."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d13fc55342030d96d38f264f6bff9586832b4ab5
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="dimension-based-product-configuration"></a>Dimensioon perustuva tuotekonfigurointi

[!include[banner](../includes/banner.md)]


Dimensioihin perustuva tuotekonfiguraatio edustaa yksinkertaista ratkaisua useiden varianttien luomiselle yhdestä päätuotteesta ja sen tuoterakenteesta.

Dimensioihin perustuva tuotekonfiguraatio on yksi kolmesta sisäänrakennetusta tuotekonfiguraatiomenetelmistä. Kaksi muuta menetelmää ovat ennalta määritettyjä variantteja ja poissulkeva konfiguraatio. Kaikki kolme menetelmää käyttävät päätuotetta lähtökohtana ja sallivat käyttäjän luoda useita tuotevariantteja yhdelle päätuotteelle.

## <a name="key-concepts"></a>Avainkäsitteet
Dimensioihin perustuva tuotekonfiguraatio perustuu seuraaviin avainkäsitteisiin:

-   Päätuotteet
-   Tuotedimension konfigurointi
-   Konfiguraatioryhmät
-   Tuoterakenne (BOM)
-   Konfiguraatioreitti
-   Konfiguraatiosäännöt

### <a name="product-masters"></a>Päätuotteet

Kaikkien tuotemallien konfigurointiprosessien aloituspiste on päätuote. Dimensioihin preustuvaan tuotekonfiguraation tarvitaan päätuote tässä tietyssä määritysmenetelmässä ja tuote dimensioryhmä, johon sisältyy konfiguraatio tuotedimensio.

### <a name="configuration-product-dimension"></a>Tuotedimension konfigurointi

Konfiguraatio tuotedimensiota käytetään päätuotteen tuotevarianttien tunnistamiseksi dimensioihin perustuvan konfiguraatiomenetelmän avulla. Käyttäjä lisää Konfiguraation dimensioarvon ja sen tulisi auttaa tunnistamaan erilliset tuotevariantit.

### <a name="configuration-groups"></a>Konfiguraatioryhmät

Konfiguraatioryhmät määritetään keskusrekisterissä ja niitä voidaan käyttää kaikkiin dimensioihin perustuviin tuotekonfiguraatiomalleihin. konfiguraatioryhmät liitetään yksittäisiin tuoterakenneriveihin ja ne sisältävät useita rivejä, jotka ovat toisensa poissulkevia. Tällöin yksittäiselle tuotevariantille voidaan valita vain yksi ryhmän rivi.

### <a name="bill-of-materials-bom"></a>Tuoterakenne (BOM)

Tuoterakenne edustaa dimensioihin perustuvan tuotekonfiguraation rakenneosia. Sen on sisällytettävä kaikki eri tuotteet, jotka ovat käytettävissä missä vain tuotevariantissa. Tuoterakenteen kukin rivi voi viitata tuoterakenneryhmään. Jos rivi ei viittaa konfiguraatioryhmään, se sisällytetään kaikkiin tuotemallin muuttujiin.

### <a name="configuration-route"></a>Konfiguraatioreitti

Konfiguraatioreititys määrittää konfiguraatioryhmien järjestyksen, niin kuin ne näkyvät käyttäjälle tuotteen konfigurointiprosessin aikana.

### <a name="configuration-rules"></a>Konfiguraatiosäännöt

Konfiguraatiosäännöt edustavat mekanismia, jolla varmistetaan että tuote joka sisältyy yhteen tuoterakenteen konfiguraatioryhmään, tukee joko muun tuotteen sisällytystä tai pois jättämistä eri konfigurointiryhmästä samassa tuoterakenteessa.

## <a name="product-modeling-process"></a>Tuotemallinnusprosessi
Luonnollinen järjestys tuotemallin dimensioihin perustuvan tuotteen rakentamiseen alkaa asianmukaisien konfiguraatioryhmien määrittämisestä. On tärkeää varmistaa, että kaikki tuotteet joita käytetään tuotemallissa, on julkaistu sille yritykselle, jota varten tuotemalli on rakennettu. Näiden rakenneosien ollessa paikallaan, käyttäjä voi luoda tuoterakenteen ja määrittää konfiguraatioryhmät kaikille olennaisille tuoterakenneriveille. Kun tuoterakenne on valmis, konfiguraatioreititys voidaan määrittää järjestämällä konfiguraatioryhmät asianmukaiseen järjestykseen. \[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimensioihin perustuva tuotemallinnusprosessi](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimensioihin perustuva tuotemallinnusprosessi\[/caption\] Jos tiettyjä tuotteita löytyy erilaisista konfiguraatiokäyttäjäryhmistä, joita joko täytyy tai ei saa käyttää yhdessä, voit luoda konfiguraatiosäännöt, jotka vahvistavat näitä tuotemallin suhteita. Sen jälkeen kun tuoterakenne on sidottu yhteen dimensioihin perustuvan päätuotteen kanssa tuoterakenneversion kautta ja kummatkin on sekä hyväksytty että aktivoitu, voit luoda tuotemallin konfiguraatioita ja syöttää kullekin knfiguraatiolle nimen. Konfiguraatiot voidaan määrittää ennen kuin mitään tapahtumia on luotu, tai se voidaan tehdä kun jotain konfiguraatiota tarvitaan.

### <a name="suggested-use"></a>Käyttöehdotukset

Dimensioihin perustuvaa määritysmenetelmää kannattaa käyttää tuotteisiin, joilla on rajallinen vaihtelevaisuus ja yhdistelmä standardin tuotedimension mitoista, väristä, tyylistä ja konfiguraatio on sopimaton tunnistamaan tietyn tuotevariantin. Esimerkki voisi olla polkupyörän rungon korkeus, pyörän koko, jarrutyypit ja eri vaihteet.




