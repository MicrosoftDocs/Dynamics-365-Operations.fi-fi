---
title: Kuormituksen luonnin työtila
description: Tässä aiheessa käsitellään kuormituksen luonnin työtilan käyttämistä.
author: Henrikan
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 5b1ab86be84f3ade58ea354417bfcc2dc0bd87e9e2cb8debb36ea43f7b877f54
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714255"
---
# <a name="load-building-workbench"></a>Kuormituksen luonnin työtila

Kuormituksen luonnin työtilassa voidaan käyttää kuormituksen luontistrategioita kuormia luotaessa.

## <a name="create-a-load-building-strategy"></a>Kuormituksen luontistrategian luominen

Kuormitusten luontistrategioita käytetään kuormien automaattiseen luontiin. Tämä ominaisuus voi olla kätevä seuraavissa tilanteissa:

- Tietty tuotejoukko lähetetään säännöllisesti, kuormitusstrategiat auttavat säästämään aikaan, sillä samaa kuormaa ei tarvitse luoda joka kerta.
- Jos haluat tehostaa toimintaa välttämällä puoliksi täytettyjä kuormia, kuormitusstrategia voivat auttaa täyttämään kunkin kuorman mahdollisimman hyvin.

Kuormituksen luontistrategian `TMSLoadBuildingVolumeStrategy`-nimisessä luokassa on *Tilavuuteen perustuva kuormituksen luontistrategia* -niminen strategia. Sen avulla voit käyttää kuormamallissa määritettyjä suurimpia korkeus- ja painoarvoja tai korvata asetukset syöttämällä uudet arvot. Tämä strategia on ainoa heti käytettävissä oleva strategia. (Käytössä voi kuitenkin olla muutamia mukautettuja strategioita.)

Voit käyttää valmista *Tilavuuteen perustuva kuormituksen luontistrategia* -strategiaa valitsemalla se **Kuormituksen luonnin työtila** -sivun **Kuormituksen luontistrategia** -kentässä (**Kuljetustenhallinta &gt; Suunnittelu &gt; Kuormituksen luonnin työtila**).

Kuormituksen luontistrategia luodaan seuraavasti:

1. Valitse **Kuljetustenhallinta &gt; Määritys &gt; Kuormituksen luonti &gt; Kuormituksen luontistrategiat**.
1. Varmista, että käytössä on kaikkien luokkien uusimmat versiot valitsemalla toimintoruudussa **Luo luokkaluettelo**.
1. Valitse toimintoruudussa **Uusi**.
1. Anna strategialle yksilöivä nimi, valitse sille kuormituksen luontistrategia ja anna kuvaus.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Parametrit**.
1. Valitse **Kuormituksen luontistrategian parametrit** -sivun luettelossa **Tilavuuskapasiteetti** ja anna sitten **Arvo**-kenttään se prosenttiosuus kuorman kokonaistilavuuskapasiteetista, jota käytetään uudessa kuormituksen luontistrategiassa.
1. Valitse luettelossa **Painokapasiteetti** ja anna sitten **Arvo**-kenttään se prosenttiosuus kuorman kokonaispainokapasiteetista, jota käytetään uudessa kuormituksen luontistrategiassa.
1. Sulje **Kuormituksen luontistrategian parametrit** -sivu.
1. Sulje **Kuormituksen luontistrategiat** -sivu.

Kuormituksen luontistrategia voidaan nyt määrittää kuormituksen luontimalliin. Vaihtoehtoisesti voit käyttää sitä suoraan kuormasuunnittelun työtilassa.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Kuormituksen luontistrategian käyttäminen kuormituksen luonnin työtilassa

1. Valitse **Kuljetustenhallinta &gt; Suunnittelu &gt; Kuormituksen luonnin työtila**.
1. Noudata seuraavia ohjeita:

    - Valitse strategia **Kuormituksen luontistrategia** -kentässä.
    - Jos olet määrittänyt kuormituksen luontimallin ja määrittänyt siihen kuormituksen luontistrategian, valitse toimintoruudun **Mallien hallinta** -välilehdessä **Käytä mallia**. Valitse sitten avattavassa **Käytä kuormituksen luontimallia** -valintaikkunassa malli **Kuormituksen luontimallin nimi** -kentässä.

1. Valitse **Kuormitusmallien järjestys** -pikavälilehdessä vähintään yksi [kuormitusmalli](load-template.md). Työtila yrittää sovittaa kuormituksen tämän tyyppisiin kontteihin tässä määritetyssä järjestyksessä. Yleensä pienin kontti kannattaa sijoittaa ensimmäiseksi luetteloon, sillä näin varmistetaan, että pienin mahdollinen kontti valitaan ensimmäisenä.
1. Valitse toimintoruudussa **Ehdota kuormia**.
1. Tarkista ehdotetut kuormat ja ehdotetut kuormarivit.
1. Luo **Ehdotetut kuormarivit** -pikavälilehden lähdeasiakirjan riveihin perustuvat kuormat valitsemalla toimintoruudussa **Luo kuormat**.
1. Sulje **Kuormituksen luonnin työtila** -sivu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]