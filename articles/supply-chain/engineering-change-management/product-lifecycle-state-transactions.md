---
title: Tuotteen elinkaaren tilat ja tapahtumat
description: Tässä aiheessa käsitellään niiden tapahtumien hallintaa, jotka ovat sallittuja kussakin elinkaaren tilassa suunnittelutuotteen elinkaaren eri vaiheissa.
author: t-benebo
ms.date: 02/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1e9b8a9f25edfa654a57e0ab4071cd93c8033d85
ms.sourcegitcommit: d375ef4138e898621416754c40770d8ccca4d271
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2022
ms.locfileid: "8322741"
---
# <a name="product-lifecycle-states-and-transactions"></a>Tuotteen elinkaaren tilat ja tapahtumat

[!include [banner](../includes/banner.md)]

Suunnittelutuotteen elinkaaren eri vaiheissa on tärkeää, että kussakin elinkaaren tilassa sallittuja tapahtumia voidaan hallita. Esimerkiksi tuotteita, jotka eivät ole vielä täysin kehittyneessä tilassa, ei saa lisätä myyntitilaukseen. Jos tuotteen elinkaari on vastaavasti päättymässä, kyseisen tuotteen saapumista halutaan ehkä hallita.

Suunnittelutuotteen elinkaaren tilan muutokset liittyvät tuotteen suunnitteluversioihin. Niinpä myös tuotteen elinkaarentila voidaan liittää sen suunnitteluversioihin. Kun tuotteen elinkaaren tila on liitetty suunnitteluversioon, voit hallita elinkaaren tilan avulla suunnitteluversiossa sallittavia tapahtumia.

## <a name="create-and-manage-product-lifecycle-states"></a>Tuotteen elinkaaren tilojen luonti ja hallinta

Voit käyttää tuotteen elinkaaren tiloja valitsemalla **Suunnittelun muutostenhallinta \> Määritys \> Tuotteen elinkaaren tila**. Tee sitten jokin seuraavista:

- Luo uusi elinkaaren tila valitsemalla toimintoruudussa **Uusi** ja määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Muokkaa aiemmin luotua elinkaaren tilaa valitsemalla se luetteloruudussa ja sitten valitsemalla toimintoruudussa **Muokkaa**. Määritä sitten kentät seuraavissa alaosissa kuvatulla tavalla.
- Poista aiemmin luotu elinkaaren tila valitsemalla se luetteloruudussa ja valitsemalla sitten toimintoruudussa **Poista**.

> [!NOTE]
> Suunnittelutuotteet käyttävät samoja tuotteen elinkaaren tiloja kuin (muut kuin suunnittelut) vakiotuotteet. Voit avata myös tässä aiheessa käsitellyn **Tuotteen elinkaaren tila** -sivun valitsemalla **Tuotetietojen hallinta \> Määritys \> Tuotteen elinkaaren tila**. Lisätietoja sekä suunnittelutuotteiden että vakiotuotteiden tuotteen elinkaaren tiloista on kohdassa [Tuotteen elinkaaren tilan yleiskatsaus](../pim/product-lifecycle.md).

### <a name="header"></a>Otsikko

Määritä seuraavat kentät tuotteen elinkaaren tilan otsikossa.

| Kenttä | kuvaus |
|---|---|
| Alue | Anna tuotteen elinkaaren tilalle nimi. |
| kuvaus | Anna tuotteen elinkaaren tilan kuvaus. |

### <a name="general-fasttab"></a>Yleinen-pikavälilehti

Määritä seuraavat kentät **Yleiset**-pikavälilehdessä.

| Kenttä | kuvaus |
|---|---|
| Oletus yritykseen vapautettaessa | Määritä vakiotuotteissa asetukseksi *Kyllä*, jos tätä elinkaaren tilaa on käytettävä oletusarvoisesti kaikissa tuotteissa, kun ne vapautetaan ensimmäisen kerran. Määritä asetukseksi *Ei*, jos tätä elinkaaren tilaa käytetään myöhemmin manuaalisesti.<p>Tämä asetus ei koske suunnittelutuotteita. Suunnitteluyrityksessä luodun suunnittelutuotteen version elinkaaren tila määritetään suunnittelun muutosluokassa: Kun tuote vapautetaan operatiiviseen yritykseen, tuotteen elinkaaren tila kopioidaan. Kun suunnittelutuote vapautetaan operatiiviseen yritykseen, siinä on siis sama elinkaaren tila kuin se oli suunnitteluyrityksessä. Elinkaaren tila voidaan korvata operatiivisessa yrityksessä.</p> |
| On käytettävissä suunnitteluun | Määritä asetukseksi *Kyllä*, jos tässä elinkaaren tilassa olevat tuotteet sisällytetään laskelmiin pääsuunnittelu- ja tuoterakennetasoilla. Määritä asetukseksi *Ei*, jos elinkaaren tässä tilassa olevat tuotteet jätetään pois laskelmista. |

### <a name="enabled-business-processes-fasttab"></a>Käyttöönotetut liiketoimintaprosessit -pikavälilehti

**Käyttöönotetut liiketoimintaprosessit** -välilehden avulla voi hallita, mitä käytettävissä olevia liiketoimintaprosesseja voidaan käyttää tuotteissa, joilla on nykyinen elinkaaren tila. Tässä pikavälilehdessä olevat prosessit löytyvät automaattisesti seuraavasti:

- Kun uusi elinkaaren tila tallennetaan ensimmäisen kerran, sivu lataa kyseisellä hetkellä käytettävissä olevat liiketoimintaprosessit.
- Jos järjestelmään lisätään uusia liiketoimintaprosesseja, nykyisen elinkaaren tilan **Käyttöönotetut liiketoimintaprosessit** -pikavälilehden luettelo voidaan päivittää valitsemalla toimintoruudussa **Tarkista päivitysten saatavuus**.

Seuraavat kentät ovat käytettävissä kussakin **Käyttöönotetut liiketoimintaprosessit** -pikavälilehdessä olevassa prosessissa.

| Kenttä | kuvaus |
|---|---|
| Prosessoi | Tämä vain luku -muotoinen kenttä näyttää aiemmin luodun liiketoimintaprosessin nimen. |
| Prosessialue | Tämä vain luku -muotoinen kenttä näyttää aiemmin luodun prosessin alueen. |
| Käytäntö | Valitsemalla jonkin seuraavista arvoista voit määrittää, onko nykyinen prosessi sallittu tuotteissa, joilla on tämä elinkaaren tila, ja miten se sallitaan:<ul><li>**Käytössä** – liiketoimintaprosessi sallitaan.</li><li>**Estetty** – Prosessia ei sallita. Jos käyttäjä yrittää käyttää prosessia tuotteessa, jolla on tämä elinkaaren tila, järjestelmä estää yrityksen ja näyttää virheen. Voit esimerkiksi estää elinkaaren lopussa olevan tuotteen ostamisen.</li><li>**Käytössä mutta varoitus** – Vaikka prosessi sallitaan, siitä varoitetaan. Tuotantotilaukseen voidaan esimerkiksi asettaa prototyyppituote, jonka tuotekehitysosasto on luonut. Muiden osastojen on kuitenkin tiedettävä, että tuotetta ei ole tarkoitus vielä valmistaa.</li></ul> |

Jos muita elinkaaren tilasääntöjä lisätään mukautuksina, voit tarkastella kyseisiä sääntöjä käyttöliittymässä valitsemalla yläruudussa **Päivitä prosessit**. **Päivitä prosessit** -painike on vain järjestelmänvalvojien käytettävissä.

## <a name="lifecycle-states-for-released-products-and-product-variants"></a>Vapautettujen tuotteiden ja varianttien elinkaaren tilat

Jos tuotteella on variantteja (päätuotteita ja variantteja), päätuotteella on elinkaaren tila ja kullakin variantilla voi olla myös eri elinkaaren tila.

Jos joko variantti tai tuote on estetty tietyissä prosesseissa, myös prosessin käyttö estetään. Järjestelmä tarkistaa, onko prosessi estetty, seuraavasti:

- Suunnitteluohjatut tuotteet:
  - Jos nykyinen suunnitteluversio on estetty, estä prosessi.
  - Jos nykyinen variantti on estetty, estä prosessi.
  - Jos vapautettu tuote on estetty, estä prosessi.
- Vakiotuotteita varten:
  - Jos nykyinen variantti on estetty, estä prosessi.
  - Jos vapautettu tuote on estetty, estä prosessi.

Oletetaan esimerkiksi, että haluat myydä vain yhden variantin (punainen) tietystä tuotteesta (t-paita) ja estät kaikkien muiden varianttien myynnin tällä hetkellä. Voit toteuttaa tämän seuraavilla asetuksilla:

- Määritä tuotteelle elinkaaren tila, joka sallii prosessin. Voit esimerkiksi määrittää t-paita-tuotteelle elinkaaren tilaksi *Myytävä*, jolloin *Myyntitilaus*-liiketoimintaprosessi on mahdollinen.
- Määritä myytävälle variantille elinkaaren tila, joka sallii prosessin. Voit esimerkiksi määrittää myös punaiselle variantille elinkaaren tilaksi *Myytävä*.
- Kaikille muille varianteille määritetään toinen elinkaaren tila, jossa prosessi on estetty. Määritä esimerkiksi valkoiselle variantille (ja kaikille muille varianteille) elinkaaren tilaksi *Ei myytävä*, joka estää *Myyntitilaus*-liiketoimintaprosessin.

## <a name="default-product-lifecycle-states"></a>Tuotteen elinkaaren tilojen nollaaminen

Suunnitteluversion elinkaaren tila määrittyy sen suunnitteluluokan mukaan. Tila nollataan, kun luot uuden suunnitteluversion, myös uuden tuotteen ensimmäisen version kohdalla.

Kun luot uuden tuotteen tai suunnittelutuotteen voit määrittää oletusarvoisen elinkaaren tilan myös määrittämällä sen tuotteelle määritetyn vapautuskäytännön vapautetun tuotteen mallissa.

Tällöin tuotteella voi olla eri elinkaaren tila kuin versiolla, kun luot uuden suunnittelutuotteen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
