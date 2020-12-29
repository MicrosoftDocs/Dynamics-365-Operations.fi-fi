---
title: Manuaalisten oikaisujen tekeminen perusennusteeseen
description: Tässä ohjeaiheessa kerrotaan, miten voit tehdä manuaalisia oikaisuja perusennusteeseen ja tarkastella ennusteen tietoja.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dc5d1812fa926216a75b6fc4e3cf820ccc3ef6d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427311"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Manuaalisten oikaisujen tekeminen perusennusteeseen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten voit tehdä manuaalisia oikaisuja perusennusteeseen ja tarkastella ennusteen tietoja. 

Ennen kuin teet manuaalisia oikaisuja, on tärkeää, että ymmärrät muutamia eri sivujen konsepteja.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Ruudukko Oikaistu kysynnän ennuste -sivulla
**Oikaistu kysynnän ennuste** -sivu sisältää ruudukon, jossa on seuraava rakenne:

-   Ensimmäisessä sarakkeessa näytetään nimike, nimikkeen kohdistustunnukset, yritykset ja niin edelleen, joille ennuste on luotu. Sivun alaotsikko antaa kuvauksen nykyisistä ennustedimensioista, jotka näkyvät ruudukossa. Jos esimerkiksi sivun alaotsikko on **Yritys/Toimipaikka/Nimikkeen kohdistustunnus**, ja yksi ruudukon riviotsikoista on **USMF / 1 / D\_Alloc**, kyseinen rivi näyttää ennusteen USMF-yrityksen toimipaikalle 1, ja **D\_Alloc** nimikkeen kohdistustunnuksen.
-   Seuraavissa sarakkeissa näytetään ennustejaksot, joille ennuste on luotu. Kussakin sarakkeen otsikossa on sarakkeen näyttämä ennustejakson ensimmäinen päivä.
-   Solujen arvot edustavat yhden nimikkeen, nimikkeen kohdistustunnuksen jne. ennustetta tälle nimenomaiselle ennustejaksolle.

## <a name="forecast-aggregation-and-de-aggregation"></a>Ennusteen koostaminen ja koosteen purkaminen
Sivun alaotsikko näyttää ennusteen koostamisen tason. 

Jos esimerkiksi sivun alaotsikko on **Yritys/Toimipaikka/Kohdistustunnus/Nimikkeen numero/Väri/Koko/Konfiguraatio/Tyyli**, ennusteen koostetta ei ole ja ennuste näytetään nimikkeen ja sen dimensioiden tasolla. Voit muuttaa koostetta **Muuta ennustedimensioita** -sivulla, jonka voit avata sovellusvalikosta. 

Muokkaa ennustetta napsauttamalla mitä tahansa käytettävissä olevaa solua ja kirjoita oikaistu ennusteen arvo. Muokattu solu muuttuu heti lihavoiduksi osoittamaan, että sen näyttämä ennuste ei ole kysynnän ennusteen palvelun luoma ennuste, vaan sitä on muokattu manuaalisesti. 

Jos muutat koosteen niin, että sivu näyttää enemmän koostettuja tietoja, voit näet **Kysynnän ennusteen rivit** -sivulla yksittäiset ennusteen rivit, joista koostettu ennuste on muodostunut. 

Olet esimerkiksi luonut ennusteen nimiketasolla mutta tiedät, että tämän nimikkeen kysyntä tulee kasvamaan kaikissa toimipaikoissa kampanjasta tai vastaavasta tapahtumasta johtuen. Tässä tapauksessa voit määrittää koosteen arvoksi **Yritys/Nimikkeen kohdistustunnus/Nimike** **Muuta ennustedimensioita** -sivulla. Voit oikaista nimikkeen yleisen ennusteen kaikissa toimipaikoissa **Oikaistu kysynnän ennuste** -ruudukossa. Näet muutoksesi vaikutuksen kaikissa toimipaikoissa, kun avaat **Kysynnän ennusteen rivit** -sivun. Tällä sivulla näet yhden rivin nimikkeelle kussakin toimipisteessä, oikaistun ennusteen määrän sekä alkuperäisen ennusteen määrän. 

Kun ennustetun määrän oikaisu tehdään koostetasolla, järjestelmä käyttää painotettua kohdistusta jakaakseen muutoksen riveille, joista kooste muodostuu. 

Voit myös tehdä manuaalisia oikaisuja **Kysynnän ennusteen rivit** -sivulla muokkaamalla joko **Kokonaismäärä**-arvoa tai **Määrä**-soluja koosteen purkuruudukossa.

## <a name="viewing-details-of-the-forecast"></a>Ennusteen tietojen tarkasteleminen
Voit avata **Kysynnän ennusteen tiedot** -sivun nähdäksesi ennustetta koskevia lisätietoja. 

**Kysynnän ennusteen tiedot** -sivulla näet seuraavat tiedot graafisessa ja taulukkomuodossa.

-   Historiallinen kysyntä, johon ennusteet perustuvat.
-   Nykyinen ennuste, jota pääsuunnittelu käyttää.
-   Uudet kysynnän ennusteen arvot ja niiden manuaalisten oikaisujen määrät.
-   Ennustettujen arvojen luottamusväli.
-   Ennustemalli, jota käytettiin ennusteen luontiin. Jos tarkastelet koostetietoja, näet luettelon kaikista menetelmistä, joita on käytetty kaikissa aikasarjojen koosteissa.
-   Sisäisen mallin tarkkuus (MAPE). Lisätietoa ennusteen tarkkuudesta on kohdassa [Ennusteen tarkkuuden valvonta](monitor-forecast-accuracy.md).

**Huomautuksia:**

-   Jos otat **Ennustemallin valinnan käyttöön kysynnän ennusteen tiedoissa** ominaisuuksien hallinnasta, voit valita ennustemallit, jotka sisällytetään historialliseen ennusteeseen **Kysynnän ennusteen tiedot** -sivulla.
-   Sivun **Ennuste** -kohdassa näkyvä luottamusväli kuvaa luottamusvälin ylärajan ja luottamusvälin alarajan erotusta. Jos haluat nähdä ylärajan ja alarajan arvot, pidä kohdistinta **Historiallinen kysyntä ja ennuste graafisesti** -osiossa olevan kaavion yläpuolella.
-   Jos käytät kysynnän ennustamisen Microsoft Azuren automaattianalyysiä, voit määrittää luotettavuustasoprosentin, joka luodulla ennusteella tulee olla. Luottamusväli koostuu arvoalueesta, joka toimii hyvinä ennusteina kysynnän ennusteelle. 95 prosentin luotettavuustasoprosentti osoittaa, että on 5 %:n riski, että kysynnän ennuste on luottamusvälin ulkopuolella.

Voit myös tehdä manuaalisia oikaisuja ennusteeseen **Kysynnän ennusteen tiedot** -sivulla muokkaamalla **Ennuste**-rivin arvoja **Ennuste**-osiossa.

<a name="additional-resources"></a>Lisäresurssit
--------

[Ennusteen tarkkuuden seuranta](monitor-forecast-accuracy.md)

[Tilastollisen perusennusteen luominen](generate-statistical-baseline-forecast.md)



