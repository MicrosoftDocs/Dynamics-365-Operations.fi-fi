---
title: Numerosarjan esittely
description: "Microsoft Dynamics 365 for Operationsin numerosarjoja käytetään luettavien, yksilöllisten tunnisteiden luomiseen päätietojen tietueille ja tapahtumatietueille, jotka edellyttävät tunnisteita. Tunnisteen vaativaa päätiedon tietuetta tai tapahtumatietuetta kutsutaan nimellä <em>viite</em>."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a812c93a13fd36f44e659c9976099af62793098f
ms.lasthandoff: 03/31/2017


---

# <a name="number-sequence-overview"></a>Numerosarjan esittely

[!include[banner](../includes/banner.md)]


Microsoft Dynamics 365 for Operationsin numerosarjoja käytetään luettavien, yksilöllisten tunnisteiden luomiseen päätietojen tietueille ja tapahtumatietueille, jotka edellyttävät tunnisteita. Tunnisteen vaativaa päätiedon tietuetta tai tapahtumatietuetta kutsutaan nimellä <em>viite</em>.

Ennen kuin voit luoda Microsoft Dynamics 365 for Operationsin viitteelle uusia tietueita, määritä numerosarja ja liitä se viitteeseen. Suosittelemme, että määrität numerosarjat **Organisaation hallinto** -sivujen avulla. Jos moduulikohtaiset asetukset ovat pakollisia, voit käyttää moduulin parametrisivua määrittämään moduulin numerosarjan viitteitä. Voit määrittää esimerkiksi kohdissa **Myyntireskontra** ja **Ostoreskontra** numerosarjaryhmiä, joilla kohdistetaan tietyt numerosarjat tietyille asiakkaille tai toimittajille. Kun määrität numerosarjan, sinun on määritettävä alue, joka määrittää, mitkä organisaatio käyttää numerosarjaa. Vaikutusalue voi olla **Jaettu**, **Yritys**, **Oikeushenkilö** tai **Toimintayksikkö**. Vieläkin tarkempia numerosarjoja saadaan yhdistämällä vaikutusalueet **Oikeushenkilö** ja **Yritys** sekä **Kirjanpidon vuosikalenterin kausi**. Numerosarjan muodot koostuvat segmenteistä. Numerosarjat, joiden vaikutusalue on muu kuin **Jaettu **, voivat sisältää osia, jotka vastaavat vaikutusaluetta. Esimerkiksi numerosarja, jonka vaikutusalue on **Oikeushenkilö**, voi sisältää yrityssegmentin. Liittämällä vaikutusaluesegmentin numerosarjan muodossa voit tunnistaa tietyn tietueen vaikutusalueen katsomalla sen numero. Segmenttien, jotka vastaavat vaikutusalueita, numerosarjamuodot voivat sisältää **Vakio** ja **Aakkosnumeerinen**-segmentit. **Vakio** -segmentti sisältää numeroita, kirjaimia tai symboleja, jotka eivät muutu. **Aakkosnumeerinen**-segmentti sisältää joukon kirjaimia tai numeroita, jotka lisääntyvät aina, kun numeroa käytetään. Käyttää ristikkomerkkiä (\#) edustamaan kasvavia numeroita ja et-merkkiä (&) edustamaan kasvavia kirjaimia. Esimerkiksi muodon \#\#\#\#\#\_2017 avulla luodaan sarja 00001\_2017, 00002\_2017 jne.
Numerosarjaesimerkit
------------------------

Seuraavissa esimerkeissä näytetään, kuinka segmenttejä käytetään numerosarjamuotojen luomiseen. Erityisesti esimerkit osoittavat alueen segmenttien vaikutuksen.
### <a name="expense-report-numbers"></a>Kuluraportin numerot

Seuraavassa esimerkissä kuluraportin numerot määritetään yritykselle, jonka nimi on **CS**. **Alue: **Matkalaskut **Viite: **Kuluraportin numero **Vaikutusalue: **Oikeushenkilö **Oikeushenkilö: **CS
| Segmentit  | Segmenttityyppi | Arvo     |
|-----------|--------------|-----------|
| Segmentti 1 | Oikeushenkilö | CS        |
| Segmentti 2 | Vakio     | –KULU– |
| Segmentti 3 | Aakkosnumeerinen | \#\#\#\#  |

**Esimerkki numeromuotoilusta**: CS-KULU-0039 Määrität vastaavat numerosarjamuodot muille yrityksille. Jos vaihdat vain esimerkiksi **RW**-yrityksen yritys-segmentin arvon, muotoiltu numero on RW-KULU-0039. Voit myös vaihtaa koko numerosarjamuodon muihin yrityksiin. Nyt voit esimerkiksi ohittaa yrityksen vaikutusalueen segmentin ja luoda muotoillun numeron, kuten Exp-0001.

### <a name="sales-order-numbers"></a>Myyntitilausnumerot

Seuraavassa esimerkissä myyntitilausnumerot määritetään yritystunnukselle **CEU**. **Alue: **Myynti **Viite: **Myyntitilaus **Vaikutusalue: **Yritys **Yritys: **CEU
| Segmentit  | Segmenttityyppi | Arvo    |
|-----------|--------------|----------|
| Segmentti 1 | Vakio     | MT-      |
| Segmentti 2 | Aakkosnumeerinen | \#\#\#\# |

**Esimerkki numeromuotoilusta**: SO-0029 Vaikka vaikutusalueen segmenttiä ei ole sisällytetty muotoon, numerointi käynnistyy uudelleen kunkin yrityksen tunnuksen kohdalla. Jos käytät samaa muotoa kaikille yrityksen tunnuksille, samoja numeroita käytetään kussakin yrityksessä. Esimerkiksi myyntitilausta SO-0029 käytetään jokaisessa yrityksessä. Voit myös vaihtaa koko numerosarjamuodon muuhun yritystunnukseen.

### <a name="purchase-requisition-numbers"></a>Ostoehdotuksen numerot

Seuraavassa esimerkissä ostoehdotusnumerot ovat organisaation laajuisia. **Alue: **Osto **Viite: **Ostoehdotus **Vaikutusalue: **Jaettu
| Segmentit  | Segmenttityyppi | Arvo    |
|-----------|--------------|----------|
| Segmentti 1 | Vakio     | Tarv.      |
| Segmentti 2 | Aakkosnumeerinen | \#\#\#\# |

**Esimerkki numeromuotoilusta**: Ehd0052 Koska vaikutusalue on **Jaettu**, numerosarjan muotoilua käytetään koko organisaatiossa. Et voi määrittää erilaisia numerosarjamuotoja organisaation eri osille. Numerosarjojen suorituskykyyn liittyviä tietoja
-----------------------------------------------

Mieti seuraavia tietoja siitä, miten numerosarjat määritys voi vaikuttaa järjestelmän suorituskykyyn, ennen kuin määrität numerosarjoja.
### <a name="continuous-and-non-continuous-number-sequences"></a>Jatkuvat ja ei-jatkuvat numerosarjat

Numerosarjat voivat olla jatkuvia tai ei-jatkuvia. Jatkuva numerosarja ei ohita yhtäkään numeroa, mutta numeroita ei voi käyttää peräkkäin. Ei-jatkuvien numerosarjojen numerot käytetään sarjassa, mutta numerosarja voi ohittaa numeroita. Jos esimerkiksi käyttäjä peruuttaa tapahtuman, numero luodaan mutta sitä ei käytetä. Jatkuvassa numerosarjassa sitä numeroa kierrätetään myöhemmin. Numerosarjassa, joka ei ole jatkuva numerosarja, numeroa ei käytetä. Ulkoiset asiakirjat, kuten ostotilaukset, myyntitilaukset ja laskut, vaativat tavallisesti jatkuvat numerosarjat. Kuitenkin jatkuvat numerosarjat saattavat heikentää järjestelmän vasteaikaa, koska järjestelmän on pyydettävä numeroa tietokannasta aina, kun uusi asiakirja tai tietue luodaan. Jos käytössä ei ole jatkuvaa numerosarja, **Esijako** voidaan ottaa käyttöön **Numerosarja**-sivun **Suorituskyky**-pikavälilehdessä. Kun määrität ennalta kohdistettavan numeroiden määrän, järjestelmä valitsee numerot ja tallentaa ne muistiin. Uudet numerot pyydetään tietokannasta vasta sitten, kun esijaettu määrä on käytetty. Elleivät säännökset vaadi jatkuvien numerosarjojen käyttöä, suosittelemme, että käytät ei-jatkuvia numerosarjoja paremman suorituskyvyn vuoksi.

### <a name="automatic-cleanup-of-number-sequences"></a>Automaattinen numerosarjojen puhdistus

Järjestelmä ei voi kierrättää numeroita automaattisesti jatkuvia numerosarjoja varten sähkökatkoksen, sovellusvirheen tai muun odottamattoman vian takia. Voit suorittaa vapautusprosessi manuaalisesti tai automaattisesti palauttaaksesi menetetyt numerot. Mieti palvelimen käyttö puhdistusprosessin suunnittelussa. On suositeltavaa suorittaa vapautus erätyönä hiljaisena aikana.






