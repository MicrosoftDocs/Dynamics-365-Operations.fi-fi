---
title: Numerosarjojen yleiskatsaus
description: Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille.
author: MargoC
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c036a6bf315ddb4df93c43bb3aa2b9370c7fba36
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190071"
---
# <a name="number-sequences-overview"></a>Numerosarjojen yleiskatsaus

[!include [banner](../includes/banner.md)]

Numerosarjoilla luodaan luettavia, yksilöllisiä tunnisteita niitä edellyttäville päätietojen tietueille ja tapahtumatietueille. Tunnisteen vaativaa päätiedon tietuetta tai tapahtumatietuetta kutsutaan nimellä *viite*.

Ennen kuin voit luoda viitteelle uusia tietueita, määritä numerosarja ja kohdista se viitteeseen. Suosittelemme, että määrität numerosarjat **Organisaation hallinto** -sivujen avulla. Jos moduulikohtaiset asetukset ovat pakollisia, voit käyttää moduulin parametrisivua määrittämään moduulin numerosarjan viitteitä. Voit määrittää esimerkiksi kohdissa **Myyntireskontra** ja **Ostoreskontra** numerosarjaryhmiä, joilla kohdistetaan tietyt numerosarjat tietyille asiakkaille tai toimittajille.

Kun määrität numerosarjan, sinun on määritettävä alue, joka määrittää, mitkä organisaatio käyttää numerosarjaa. Vaikutusalue voi olla **Jaettu**, **Yritys**, **Oikeushenkilö** tai **Toimintayksikkö**. Vieläkin tarkempia numerosarjoja saadaan yhdistämällä vaikutusalueet **Oikeushenkilö** ja **Yritys** sekä **Kirjanpidon vuosikalenterin kausi**.

Numerosarjan muodot koostuvat segmenteistä. Numerosarjat, joiden vaikutusalue on muu kuin **Jaettu**, voivat sisältää osia, jotka vastaavat vaikutusaluetta. Esimerkiksi numerosarja, jonka vaikutusalue on **Oikeushenkilö**, voi sisältää yrityssegmentin. Liittämällä vaikutusaluesegmentin numerosarjan muodossa voit tunnistaa tietyn tietueen vaikutusalueen katsomalla sen numero.

Segmenttien, jotka vastaavat vaikutusalueita, numerosarjamuodot voivat sisältää **Vakio** ja **Aakkosnumeerinen**-segmentit. **Vakio** -segmentti sisältää numeroita, kirjaimia tai symboleja, jotka eivät muutu. **Aakkosnumeerinen**-segmentti sisältää joukon kirjaimia tai numeroita, jotka lisääntyvät aina, kun numeroa käytetään. Käyttää ristikkomerkkiä (\#) edustamaan kasvavia numeroita ja et-merkkiä (&) edustamaan kasvavia kirjaimia. Esimerkiksi muodon \#\#\#\#\#\_2017 avulla luodaan sarja 00001\_2017, 00002\_2017 jne.

## <a name="number-sequence-examples"></a>Numerosarjaesimerkit

Seuraavissa esimerkeissä näytetään, kuinka segmenttejä käytetään numerosarjamuotojen luomiseen. Erityisesti esimerkit osoittavat alueen segmenttien vaikutuksen.

### <a name="expense-report-numbers"></a>Kuluraportin numerot

Seuraavassa esimerkissä kuluraportin numerot määritetään yritykselle, jonka nimi on **CS**.

- **Alue:** Matkalaskut
- **Viite:** Kuluraportin numero
- **Vaikutusalue:** Yritys
- **Yritys:** CS

| Segmentit  | Segmenttityyppi | Arvo     |
|-----------|--------------|-----------|
| Segmentti 1 | Oikeushenkilö | CS        |
| Segmentti 2 | Vakio     | –KULU– |
| Segmentti 3 | Aakkosnumeerinen | \#\#\#\#  |

**Esimerkki muotoillusta numerosta**: CS-KULU-0039

Voit myös määrittää vastaavan numerosarjamuodon muihin yrityksiin. Jos vaihdat vain esimerkiksi **RW**-yrityksen yritys-segmentin arvon, muotoiltu numero on RW-KULU-0039. Voit myös vaihtaa koko numerosarjamuodon muihin yrityksiin. Nyt voit esimerkiksi ohittaa yrityksen vaikutusalueen segmentin ja luoda muotoillun numeron, kuten Exp-0001.

### <a name="sales-order-numbers"></a>Myyntitilausnumerot

Seuraavassa esimerkissä myyntitilausnumerot määritetään yritystunnukselle **CEU**.

- **Alue:** Myynti
- **Viite:** Myyntitilaus
- **Vaikutusalue:** yritys
- **Yritys:** CEU

| Segmentit  | Segmenttityyppi | Arvo    |
|-----------|--------------|----------|
| Segmentti 1 | Vakio     | MT-      |
| Segmentti 2 | Aakkosnumeerinen | \#\#\#\# |

**Esimerkki muotoillusta numerosta**: MT-0029

Vaikka vaikutusalueen segmenttiä ei ole sisällytetty muotoon, numerointi käynnistyy uudelleen jokaisen yrityksen tunnuksen kohdalla. Jos käytät samaa muotoa kaikille yrityksen tunnuksille, samoja numeroita käytetään kussakin yrityksessä. Esimerkiksi myyntitilausta SO-0029 käytetään jokaisessa yrityksessä. Voit myös vaihtaa koko numerosarjamuodon muuhun yritystunnukseen.

### <a name="purchase-requisition-numbers"></a>Ostoehdotuksen numerot

Seuraavassa esimerkissä ostoehdotusnumerot ovat organisaation laajuisia.

- **Alue:** osto
- **Viite:** ostoehdotus
- **Vaikutusalue:** Jaettu

| Segmentit  | Segmenttityyppi | Arvo    |
|-----------|--------------|----------|
| Segmentti 1 | Vakio     | Tarv.      |
| Segmentti 2 | Aakkosnumeerinen | \#\#\#\# |

**Esimerkki muotoillusta numerosta**: Rek0052

Vaikutusalue on **Jaettu**, joten numerosarjan muotoa käytetään koko organisaatiossa. Et voi määrittää erilaisia numerosarjamuotoja organisaation eri osille.

## <a name="performance-considerations-for-number-sequences"></a>Numerosarjojen suorituskykyyn liittyviä tietoja

Mieti seuraavia tietoja siitä, miten numerosarjat määritys voi vaikuttaa järjestelmän suorituskykyyn, ennen kuin määrität numerosarjoja.

### <a name="continuous-and-non-continuous-number-sequences"></a>Jatkuvat ja ei-jatkuvat numerosarjat

Numerosarjat voivat olla jatkuvia tai ei-jatkuvia. Jatkuva numerosarja ei ohita yhtäkään numeroa, mutta numeroita ei voi käyttää peräkkäin. Ei-jatkuvien numerosarjojen numerot käytetään sarjassa, mutta numerosarja voi ohittaa numeroita. Jos esimerkiksi käyttäjä peruuttaa tapahtuman, numero luodaan mutta sitä ei käytetä. Jatkuvassa numerosarjassa sitä numeroa kierrätetään myöhemmin. Numerosarjassa, joka ei ole jatkuva numerosarja, numeroa ei käytetä.

Ulkoiset asiakirjat, kuten ostotilaukset, myyntitilaukset ja laskut, vaativat tavallisesti jatkuvat numerosarjat. Kuitenkin jatkuvat numerosarjat saattavat heikentää järjestelmän vasteaikaa, koska järjestelmän on pyydettävä numeroa tietokannasta aina, kun uusi asiakirja tai tietue luodaan.

Jos käytössä ei ole jatkuvaa numerosarja, **Esijako** voidaan ottaa käyttöön **Numerosarja**-sivun **Suorituskyky**-pikavälilehdessä. Kun määrität ennalta kohdistettavan numeroiden määrän, järjestelmä valitsee numerot ja tallentaa ne muistiin. Uudet numerot pyydetään tietokannasta vasta sitten, kun esijaettu määrä on käytetty.

Elleivät säännökset vaadi jatkuvien numerosarjojen käyttöä, suosittelemme, että käytät ei-jatkuvia numerosarjoja paremman suorituskyvyn vuoksi.

### <a name="automatic-cleanup-of-number-sequences"></a>Automaattinen numerosarjojen puhdistus

Järjestelmä ei voi kierrättää numeroita automaattisesti jatkuvia numerosarjoja varten sähkökatkoksen, sovellusvirheen tai muun odottamattoman vian takia. Voit suorittaa vapautusprosessi manuaalisesti tai automaattisesti palauttaaksesi menetetyt numerot.

Mieti palvelimen käyttö puhdistusprosessin suunnittelussa. On suositeltavaa suorittaa vapautus erätyönä hiljaisena aikana.
