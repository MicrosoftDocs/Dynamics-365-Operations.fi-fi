---
title: Pääsuunnittelu ja ostokauppasopimukset
description: Tässä ohjeaiheessa kuvataan, miten suunnittelun optimointi voi löytää suunnitellun tilauksen toimittajan ja/tai läpimenoajan, joka perustuu parhaaseen hintaan tai toimitusaikaan, joka löytyy ostosopimuksista.
author: ChristianRytt
manager: tfehr
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b302c5ace34a11a53a98c733b59633a11a463bfa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426851"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Pääsuunnittelu ja ostokauppasopimukset

[!include [banner](../../includes/banner.md)]

Tässä ohjeaiheessa kuvataan, miten suunnittelun optimointi voi löytää suunnitellun tilauksen toimittajan ja/tai läpimenoajan, joka perustuu parhaaseen hintaan tai toimitusaikaan, joka löytyy ostosopimuksista, jotka on määritetty tietylle tuotteelle.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Ostosopimusten ottaminen käyttöön suunnittelun optimointitoimintoa varten

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [Toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) työtilaa tarkistaakseen toiminnon tilan sekä laittaa sen päälle, jos sitä vaaditaan. Tässä tapauksessa toiminto näkyy seuraavalla tavalla:

- **Moduuli:** *Pääsuunnittelu*
- **Ominaisuuden nimi:** *Ostosopimukset suunnittelun optimointitoimintoa varten*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Valmistele järjestelmä arvioimaan ostosopimukset pääsuunnittelun aikana

Noudattamalla näitä ohjeita voit määrittää järjestelmän käyttämään suunnittelun optimointia, joka arvioi ostosopimukset.

1. Valitse **Pääsuunnittelu \> Määritys \> Pääsuunnittelun parametrit**. Määritä **Suunnitellut tilaukset** -välilehden **Toimittaja**-osassa seuraavat arvot:

    - **Etsi kauppasopimus** – Määritä tämän vaihto ehdon arvoksi **Kyllä**, jos haluat sisällyttää ostosopimukset pääsuunnitteluun.
    - **Hakuehto** – Valitse kerroin, jonka haluat priorisoida kullekin ostosopimukselle: **Vähimmäisläpimenoaika** tai **Alhaisin yksikköhinta**.

1. Siirry kohtaan **Hankkiminen ja hankinta \> Asetukset \> Hinnat ja alennukset \> Aktivoi hinta/alennus** ja varmista, että **Toimittaja**-asetukseksi on määritetty **Kyllä**.
1. Siirry kohtaan **Tuotetietojen hallinta \> Asetus \> Dimensio ja muuttujaryhmät \> Varastodimensioryhmät** ja valitse varastodimensioryhmä, joka koskee tuotteita, joiden pääsuunnittelun on tarkoitus arvioida ostosopimukset. Varmista, että kullakin tämän ryhmän merkityksellisellä varastodimensiolla on valintamerkki **Ostohinnat**-sarakkeessa. Toista tämä vaihe kaikkien muiden asianmukaisten varastodimensioryhmien osalta.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Valmistele vapautettu tuote ostosopimusten arviointia varten pääsuunnittelun aikana

Kun järjestelmä on valmisteltu edellisessä osassa kuvatulla tavalla, varmista seuraavien vaiheiden avulla, että kaikki tämän ominaisuuden kanssa käytettävät tuotteet on määritetty oikein.

1. Valitse **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet** ja avaa kohdetuote.
1. Varmista, että **Osto**-pikavälilehdessä ei ole määritetty toimittajaa **Toimittaja**-kentässä.
1. Napsauta toimintoruudussa **Suunnitelma**-välilehden **Kattavuusryhmä**-kohdassa **Nimikkeen kattavuus**. Näkyviin tulee **Nimikkeen kattavuus** -sivu valitulle tuotteelle. Varmista seuraavat asetukset:

    - **Yleinen**-välilehdessä voit määrittää toimittajan ohituksia. Jos haluat, että suunnittelun optimoinnin avulla voit valita toimittajan ostosopimusten avulla, estä toimittajan ohitukset poistamalla **Käytä tiettyä asetusta** -valintaruutu.
    - **Läpimenoaika**-välilehdessä voit määrittää toimitusajan ohituksia. Jos haluat, että suunnittelun optimointi käyttää ostosopimuksia läpimenoaikojen valitsemiseen, sinun on estettävä läpimenoaikojen ohitukset. Poista niiden toimitusajan tyyppien valintaruudut, jotka haluat valita käyttämällä ostosopimuksia (**Osto**, **Tuotanto** ja/tai **Siirto**).

1. Palaa valitun tuotteen tietosivuun sulkemalla **Nimikkeen kattavuus** -sivu.
1. Avaa **Tarjontaennuste**-sivu valitsemalla toimintoruudun **Suunnitelma**-välilehden **Ennuste**-ryhmästä **Tarjontaennuste**. Varmista, ettei tässä kuvassa olevalla rivillä ole arvoa **Toimittajatili**-sarakkeessa.
1. Palaa valitun tuotteen tietosivuun sulkemalla **Tarjontaennuste**-sivu.
1. Valitse sitten toimintoruudussa **Osto**-välilehden **Kauppasopimukset**-ryhmässä **Näytä kauppasopimukset**. Varmista, että kaikki asianmukaiset ostosopimukset on luetteloitu. Varmista myös, että **Ohita läpi menoaika** -asetuksen arvoksi on määritetty **Ei** kullekin sopimukselle, jossa haluat suunnittelun optimoinnin käyttävän kyseiselle sopimukselle määritettyä läpimenoaikaa.
1. Napsauta toimintoruudussa **Suunnitelma**-välilehden **Tilauksen asetukset** -kohdassa **Oletusarvoiset tilauksen asetukset**. Näkyviin tulee **Oletusarvoiset tilauksen asetukset** -sivu valitulle tuotteelle. Tarkastele **Ostotilaus**-pikavälilehden **Oston läpimenoaika** -kentän arvoa. Jos nimikkeen kattavuuden läpimenoajan ohitus ei ole määritetty, suunnittelun optimointi käyttää tätä arvoa, kun se valitsee kauppasopimukset, joissa **Ohita läpimenoaika** -asetuksen arvoksi on määritetty **Kyllä**. Tämän vuoksi tätä arvoa tulee muuttaa tarpeen mukaan.
1. Toista tämä toimenpide jokaiselle oleelliselle tuotteelle.

> [!NOTE]
> Ostosopimusrivin valuutan on vastattava valitun toimittajan valuuttaa. Pääsuunnittelu sisällyttää tietoja vain sellaisista ostosopimusriveistä, joiden valuutta vastaa toimittajan valuuttaa.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Esimerkkejä siitä, miten suunnittelun optimointi löytää toimittaja- ja läpimenoajat

Seuraavassa taulukossa on esimerkkejä siitä, miten vapautetun tuotteen eri asetukset ja niihin liittyvät ostokauppasopimukset vaikuttavat tuloksena olevaan suunniteltuun ostotilaukseen liittyviin arvoihin. Kahden oikeanpuoleisimman sarakkeen **Lihavoidut** arvot ovat suunnittelun optimoinnin valitsemat arvot. Muiden sarakkeiden ***lihavointi- ja kursivointi*** -arvot ovat asetuksia, jotka tuottavat kullekin riville tulokseksi saatavat arvot.

| Vapautettu tuote: Toimittaja | Tilauksen oletusasetuset: Läpimenoaika | Nimikekattavuus: Ohita toimittaja | Nimikekattavuus: Ohita läpimenoaika | Kauppasopimus: Toimittaja | Kauppasopimus: Läpimenoaika | Kauppasopimus: Ohita läpimenoaika | Tuloksena oleva toimittaja | Tuloksena oleva läpimenoaika |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001*** | ***1*** | Nro | Nro | US003 | 3 | Nro | **US001** | **1** |
| US001 | 1 | ***Kyllä: US002*** | ***Kyllä: 2*** | US003 | 3 | Nro | **US002** | **2** |
| *(Tyhjä)* | 1 | Nro | Nro | ***US003*** | ***3*** | Nro | **US003** | **3** |
| *(Tyhjä)* | ***1*** | Nro | Nro | ***US003*** | 3 | Kyllä | **US003** | **1** |
| *(Tyhjä)* | ***1*** | ***Kyllä: US002*** | Nro | US003 | 3 | Nro | **US002** | **1** |
| *(Tyhjä)* | ***1*** | ***Kyllä: US002*** | Nro | US003 | 3 | Nro | **US002** | **1** |
| *(Tyhjä)* | 1 | Nro | Kyllä: 2 | ***US003*** | ***3*** | Nro | **US003** | **3** |
| *(Tyhjä)* | 1 | Nro | ***Kyllä: 2*** | ***US003*** | 3 | Kyllä | **US003** | **2** |

## <a name="additional-resources"></a>Lisäresurssit

[Ostosopimukset](../../procurement/purchase-agreements.md)
