---
title: Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa
description: Tässä artikkelissa selitetään, miten Viivästyneen veron laskeminen -toiminto otetaan käyttöön auttamaan verolaskelmien suorittamista, kun kirjauskansion rivejä on erittäin paljon.
author: EricWang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 02a038318d4c0fb44b6fcc4bb159ea87c2e9368a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887916"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a>Viivästyneen veron laskemisen ottaminen käyttöön kirjauskansioissa
[!include [banner](../includes/banner.md)]


Tässä artikkelissa selitetään, miten voit viivästyttää arvonlisäveron laskemista kirjauskansioissa. Tämä ominaisuus auttaa parantamaan verolaskelmien suorittamista, kun kirjauskansion rivejä on paljon.

Oletusarvoisesti kirjauskansion rivien arvonlisäverosummat lasketaan aina, kun veroihin liittyviä kenttiä päivitetään. Näitä kenttiä ovat arvonlisäveroryhmien ja nimikkeiden arvonlisäryhmien kentät. Kaikki kirjauskansiorivien päivitykset aiheuttavat verosummien uudelleenlaskennan kaikkien kirjauskansiorivien osalta. Vaikka tämä toimintatapa auttaa käyttäjiä näkemään reaaliaikaisesti laskettuja verosummia, se voi myös heikentää suorituskykyä, jos kirjauskansiorivejä on erittäin paljon.

Viivästynyt veron laskenta -toiminnon avulla voit lykätä verojen laskemista kirjauskansioista, minkä vuoksi se auttaa suorituskykyongelmien ratkaisemisessa. Kun tämä toiminto on käytössä, verosummia lasketaan vain, kun käyttäjä tekee valinnan **Arvonlisävero** tai tekee kirjauksen kirjauskansioon.

Voit viivästyttää arvonlisäverojen laskentaa kolmella tasolla:

- Oikeushenkilö
- Kirjauskansion nimi
- Kirjauskansion otsikko

Järjestelmä kohtelee kirjauskansion otsikon asetusta ensisijaisena. Oletusarvoisesti tämä asetus perustuu kirjauskansion nimeen. Oletusarvoisesti kirjauskansion nimen asetus perustuu **Kirjanpitoparametrit**-sivun asetukseen, kun kirjauskansion nimi luodaan. Seuraavissa osissa selitetään, miten viivästetty verojen laskeminen otetaan käyttöön yritysten, kirjauskansioiden nimien ja kirjauskansioiden otsikkojen osalta.

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a>Viivästyneen verojen laskemisen käyttöönotto yritystasolla

1. Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpitoparametrit**.
2. Aseta **Arvonlisävero**-välilehden **Yleinen**-pikavälilehden **Viivästynyt veron laskenta** -asetuken arvoksi **Kyllä**.

![Kirjanpitoparametrien kuva.](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a>Viivästyneen verojen laskemisen käyttöönotto kirjauskansion nimen tasolla

1. Siirry kohtaan **Kirjanpito \> Kirjauskansion asetukset \> Kirjauskansioiden nimet**.
2. Aseta **Viivästynyt veron laskenta** -asetuksen arvoksi **Kyllä** **Arvonlisävero**-osan **Yleiset**-pikavälilehdessä.

![Kirjauskansioiden nimien kuva.](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a>Viivästyneen verojen laskemisen käyttöönotto otsikkotasolla

1. Siirry kohtaan **Kirjanpito \> Kirjauskansioviennit \> Yleiset kirjauskansiot**.
2. Valitse **Uusi**.
3. Valitse kirjauskansion nimi.
4. Aseta **Asetukset**-välilehden **Viivästynyt veron laskenta** -asetuksen arvoksi **Kyllä**.

![Kirjauskansiosivun kuva.](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
