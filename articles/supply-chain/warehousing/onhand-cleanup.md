---
title: Varastonhallinnan käytettävissä olevien merkintöjen tyhjennystyö
description: Tässä aiheessa kuvataan käytettävissä olevien tapahtumien tyhjennystyö, joka auttaa parantamaan järjestelmän suorituskykyä tunnistamalla ja poistamalla aiheeseen liittyviä, mutta tarpeettomia tietueita.
author: perlynne
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: b2bdfb7fa0c9c4d9e1f630a41357dc405f0082bc
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103860"
---
# <a name="warehouse-management-on-hand-entries-cleanup-job"></a>Varastonhallinnan käytettävissä olevien merkintöjen tyhjennystyö

[!include [banner](../includes/banner.md)]

Käytettävissä olevan varaston laskennassa käytettävien kyselyiden suorituskyky vaikuttaa siihen, kuinka monta tietuetta taulukoissa on mukana. Yksi tapa parantaa suorituskykyä on vähentää niiden tietojen määrää, joita tietokannan on harkittava.

Tässä aiheessa kuvataan käytettävissä olevien tapahtumien tyhjennystyö, joka poistaa tarpeettomat tietueet InventSum- ja WHSInventReserve-tauluista. Näissä taulukoissa on tietoja nimikkeistä, jotka on otettu käyttöön varastonhallinnan käsittelyä varten. (Näitä nimikkeitä kutsutaan WHS-nimikkeiksi.) Näiden tietojen poistaminen voi merkittävästi parantaa käytettävissä olevien laskelmien suorituskykyä.

## <a name="what-the-cleanup-job-does"></a>Mitä puhdistustyö tekee

Käytettävissä olevien tapahtumien tyhjennystyö poistaa kaikki WHSInventReserve- ja InventSum-taulujen tietueet, joissa kentän arvot ovat *0* (nolla). Nämä tiedot voidaan poistaa, koska ne eivät vaikuta käytettävissä oleviin tietoihin. Työtehtävä poistaa vain ne tiedot, jotka ovat **Sijainti**-tason alapuolella.

Jos negatiivinen fyysinen varasto on sallittu, tyhjennystyö ei ehkä voi poistaa kaikkia asiaankuuluvia merkintöjä. Tämän rajoituksen syy on se, että työn on sallittava tietty tilanne, jossa rekisterikilvessä on useita sarjanumeroita ja jokin näistä sarjanumeroista on muuttunut negatiiviseksi. Esimerkiksi järjestelmä on nolla, joka on käytettävissä rekisterikilven tasolla, kun rekisterikilvessä on +1 kpl sarjanumero 1:tä ja –1 kpl sarjanumero 2:ta. Tässä erityisessä skenaariossa työ tekee leveää ensimmäistä poistoa, jossa se yrittää poistaa ensin alemmasta tasosta.

## <a name="schedule-and-configure-the-cleanup-job"></a>Tyhjennystyön ajoittaminen ja määrittäminen

Käytettävissä olevien tapahtumien tyhjennystyö on saatavilla kohdassa **Varastonhallinta \> Kausittaiset tehtävät \> Siivous \> Varastonhallinnan varastosaldon tapahtumat**. Käytä vakiotyöasetuksia, kun haluat hallita työn suorituksen laajuutta ja aikataulua. Lisäksi käytössä on seuraavat asetukset:

- **Poista, jos tätä ei ole päivitetty näin moneen päivään** – Anna vähimmäispäivien määrä, jonka työn tulisi odottaa, ennen kuin se poistaa käytettävissä olevan tapahtuman, joka on laskenut nollaan määrään. Tämän asetuksen avulla voit vähentää edelleen käytössä olevien merkintöjen poistoriskiä. Jos haluat, että tyhjennys tapahtuu mahdollisimman pian, kirjoita joko *0* (nolla) tai jätä kenttä tyhjäksi.
- **Enimmäissuoritusaika (tuntia)** – Määritä tyhjennystyön enimmäissuoritusaika tunteina. Jos työ ei valmistunut ennen tämän ajan umpeutumista, se tallentaa tähän mennessä suoritetun työn ja sulkee sen. Tämä ominaisuus on erityisen tärkeä toteutuksille, joilla on suuri varastokäyttö. Näissä tapauksissa voit ajoittaa työn suoritettavaksi silloin, kun järjestelmän kuormitus on mahdollisimman kevyt. Jos haluat, että erätyö jatkuu, kunnes se on suoritettu loppuun, kirjoita joko *0* (nolla) tai jätä kenttä tyhjäksi. Tämä asetus on käytettävissä vain, jos järjestelmään liittyvä toiminto on [otettu käyttöön järjestelmässäsi](#max-execution-time).

Vaikka voit suorittaa työn tavallisten aukioloaikojen aikana, on suositeltavaa suorittaa työ työajan ulkopuolella. Näin voit estää ristiriitoja, joita voi ilmetä, jos käyttäjä käyttää myös siivottua tietuetta.

Jos työ yrittää poistaa nimikkeen tietueen samalla, kun toinen käyttäjä käyttää tietuetta, tyhjennystyön tai käyttäjän kohdalla ilmenee lukkiutumisen virhe.

Kun työ suoritetaan, sen toteutuskoko on 100. Toisin sanoen, se yrittää sitoutua kerran jokaista 100:a poistoa kohti. Koska joitakin poistoja on määritetty, saattaa kuitenkin olla tilanteita, joissa samassa tapahtumassa voidaan poistaa yli 100 tietuetta. Tämän vuoksi lukitusestoja voi joskus ilmetä.

## <a name="possible-user-impact"></a>Mahdollinen käyttäjän vaikutus

Käyttäjät saattavat vaikuttaa, jos käytettävissä olevien tapahtumien tyhjennystyö poistaa kaikki tietyn tason tietueet (kuten rekisterikilven tason). Tässä tapauksessa toiminto, jonka mukaan varasto oli aiemmin käytettävissä rekisterikilvessä, ei ehkä toimi odotetulla tavalla, koska tarvittavat käytettävissä olevat tiedot eivät ole enää saatavilla. Näin voi tapahtua esimerkiksi seuraavissa tilanteissa:

- Kun käyttäjä poistaa **Varastoluettelo**-kohdassa ehdon **Määrä \<\> 0** valinnan tai valitsee ehdon **Suljetut tapahtumat** **Dimensionäyttö**-asetuksia.
- Kun käyttäjä määrittää menneiden kausien **Varastotilanne/varastodimensio** -raportissa **Alkupäivämäärä**-parametrin.

Puhdistustyö kuitenkin parantaa suorituskykyä, minkä pitäisi korvata nämä pienet toimintojen heikennykset.

## <a name="make-the-maximum-execution-time-setting-available"></a><a name="max-execution-time"></a>Parhaan suoritusajan määrittäminen käyttöön

**Enimmäissuoritusaika**-asetus on käytettävissä vain, kun *Varastonhallinnan käytettävissä olevan varaston merkintöjen siivoustyön enimmäissuoritusaika* -toiminto on käytössä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on poistettu oletusarvoisesti käytöstä. Järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Varastonhallinnan käytettävissä olevan varaston merkintöjen siivoustyön enimmäissuoritusaika* [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]