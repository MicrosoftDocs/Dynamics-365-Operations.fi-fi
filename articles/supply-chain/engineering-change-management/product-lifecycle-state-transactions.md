---
title: Tuotteen elinkaaren tilat ja tapahtumat
description: Tässä aiheessa käsitellään niiden tapahtumien hallintaa, jotka ovat sallittuja kussakin elinkaaren tilassa suunnittelutuotteen elinkaaren eri vaiheissa.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEcoResProductLifecycleStateChange
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 9c6ba9831b84e1220ee158d8186675107b490124
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5266172"
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]