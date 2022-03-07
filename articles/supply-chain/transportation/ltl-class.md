---
title: Kuorma-autokuormaa pienemmät (LTL) luokat
description: Tässä aiheessa selitetään, mitkä ovat kuorma-autokuormaa pienemmät (LTL) luokat ja miten ne määritetään Microsoft Dynamics 365 Supply Chain Managementissa.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941807"
---
# <a name="less-than-truckload-ltl-classes"></a>Kuorma-autokuormaa pienemmät (LTL) luokat

[!include [banner](../includes/banner.md)]

Kuorma-autokuormaa pienempi luokka on rahdin lähetysluokka, jota käytetään toimitettavissa olevien nimikkeiden luokittamiseen. Yleensä jokaisella tuote- tai kauppatavaratyypillä on National Motor Freight Classification (NMFC) -koodi, joka vastaa LTL-lähetysten tiettyä rahtiluokan numeroa. LTL-rahtiluokat edustavat nimikeluokkia, kun taas NMFC-koodit liittyvät kunkin 18 rahtiluokan tiettyihin kauppatavaroihin.

Toiminnolla voi suorittaa seuraavia tehtäviä järjestelmää käyttämällä:

- Määritä yrityksessä käytettävät LTL-rahtiluokat.
- Määritä jokainen LTL-luokka NMFC-koodiin **NMFC-koodit**-sivulla. Lisätietoja on kohdassa [National Motor Freight Classification (NMFC) -koodit](nmfc-codes.md).
- Määritä NMFC-koodi (ja siten siihen liittyvä LTL-koodi) jokaiselle tuotteelle **Tuotteet**-sivulla.
- Arvioi tarkasti kaikkien niiden tuotteiden LTL-luokka, joihin on liitetty NMFC-koodi.
- Voit määrittää kunkin LTL-luokan pakkausvaatimukset tarkistamalla kansainväliset LTL-standardit. Näin varmistat, että tuotteesi suojataan ja toimitetaan varmasti.
- Hae tarkat lähetysarviot kunkin tuotteen LTL-rahtiluokan perusteella.

Tässä ohjeaiheessa käsitellään LTL-luokkien luontia Microsoft Dynamics 365 Supply Chain Managementissa.

## <a name="create-an-ltl-class"></a>Luo LTL-luokka

Luo LTL-luokka seuraavien ohjeiden avulla.

1. Noudata seuraavia ohjeita:

    - Valitse **Varastonhallinta \> Asetukset \> Varasto \> LTL-luokat**.
    - Valitse **Kuljetustenhallinta \> Asetukset \> Kuljetusstandardit \> LTL-luokat**.

2. Valitse toimintoruudussa **Uusi** ja luo LTL-luokka. Määritä sitten seuraavat kentät:

    - **LTL-luokka** – Kirjoita yrityksen sisäinen LTL-luokkatunnus kauppatavaran tyypille. Useimmat yritykset käyttävät kansainvälistä standardia. Tässä tapauksessa tämän kentän arvo vastaa **Luokka**-kentän arvoa. Jos yrityksesi käyttää kuitenkin omaa standardia, kirjoita sen mukainen koodi.
    - **Nimi** – Kirjoita kuvaava nimi, joka auttaa sinua ja muita käyttäjiä valitsemaan oikean LTL-luokan jokaiselle NMFC-koodille.
    - **Luokka** – Syötä kauppatavaratyypin kansainvälinen LTL-vakioluokan tunnus. Tähän kirjoitettavan koodin on vastattava virallista standardia.

## <a name="example-set-up-ltl-classes"></a>Esimerkki: LTL-luokkien määrittäminen

Seuraavassa esimerkissä kerrotaan, miten määritetään kaksi erilaista LTL-luokkaa, joita voit käyttää erityyppisten tuotteiden kanssa.

1. Valitse **Varastonhallinta \> Asetukset \> Varasto \> LTL-luokat**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **LTL-luokka:** *92.5*
    - **Nimi:** *Tietokoneet, näytöt, jäähdytyskoneet*
    - **Luokka:** *92.5*

1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä uudelle riville seuraavat arvot:

    - **LTL-luokka:** *125*
    - **Nimi:** *Pienet kodinkoneet*
    - **Luokka:** *125*

1. Valitse toimintoruudussa **Tallenna**.

## <a name="additional-resources"></a>Lisäresurssit

- [National Motor Freight Classification (NMFC) -koodit](nmfc-codes.md)
- [Rahtikirjan luominen](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
