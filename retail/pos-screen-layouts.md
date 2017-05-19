---
title: "Määritä näytön asettelu myyntipisteessä"
description: "Tässä aiheessa on tietoja Microsoft Dynamics 365 for Operations - Retail -sovelluksen myyntipisteiden käyttöliittymistä."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: efded720c40feb8a4541b52b40b88c377e32594e
ms.contentlocale: fi-fi
ms.lasthandoff: 04/26/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Määritä näytön asettelu myyntipisteessä

[!include[banner](includes/banner.md)]


Tässä aiheessa on tietoja Microsoft Dynamics 365 for Operations - Retail -sovelluksen myyntipisteiden käyttöliittymistä.

Microsoft Dynamics 365 for Operations - Retail -sovelluksen myyntipisteiden käyttöliittymät voidaan määrittää käyttäen visuaalisten profiilien ja näyttöasettelujen yhdistelmää, jotka on määritetty myymälöille, kassakoneille ja/tai käyttäjille.

## <a name="visual-profile"></a>Visuaalinen profiili
Visuaaliset profiilit määritetään kassakoneille ja niitä käytetään määrittämään visuaalisia elementtejä, jotka ovat kassakonekohtaisia ja kaikille työntekijöille jaettuja. Kaikki käyttäjät, jotka kirjautuvat kassakoneeseen, näkevät samat teemat, värit ja kuvat. 

**Profiilinumero** - profiilinumero on visuaalisen profiilin yksilöivä tunnus. 

**Kuvaus** - kuvauksen avulla voit määrittää kuvaavan nimen, joka auttaa tunnistamaan oikean profiilin tilanteen mukaan.

**Teema** - käyttäjät voivat valita vaalean tai tumman sovellusteeman. Nämä asetukset vaikuttavat koko sovelluksen fontteihin ja taustan väreihin.

**Korostuksen väri** - korostuksen värejä käytetään koko myyntipisteessä erottamaan tai korostamaan tiettyjä visuaalisia elementtejä, kuten ruutuja, painikkeita tai hyperlinkkejä. Nämä elementit ovat yleensä toimintoja.

**Otsikon väri** - otsikon väri antaa käyttäjän määrittää sivun otsikon värin vähittäismyyjän brändäyksen mukaisesti. Tämä ominaisuus on käytössä vain Dynamics 365 for Operations -versiossa 1611.

**Kirjautumisen tausta** - käyttäjät voivat määrittää kirjautumisnäytön taustakuvan. Taustakuvan tiedostokoko on pidettävä mahdollisimman pienenä, koska suurien tiedostojen tallentaminen ja lataaminen vaikuttavat sovelluksen toimintaan ja suorituskykyyn.

**Sovelluksen tausta** -Myyntipiste voi myös käyttää kuvaa taustana koko sovelluksessa yhtenäisen teemavärin sijaan. Samoin kuin kirjautumisnäytön taustassa, tiedostokoko olisi pidettävä mahdollisimman pienenä.

## <a name="screen-layouts"></a>Näytön asettelut
Näytön asettelun kokoonpano määrittää käyttöliittymän ohjausobjektien toiminnot, sisällön ja sijoittelut myyntipisteen Tervetuloa-näytössä ja tapahtumanäytössä. 

**Tervetuloa-näyttö** - Tervetuloa-näyttö on yleensä sivu, jonka käyttäjät näkevät, kun he ensin kirjautuvat myyntipisteeseen. Tervetuloa-näyttö voi koostua tavaramerkin kuvasta painikeruudukoista, jotka tarjoavat pääsyn myyntipisteen toimintoihin. Toiminnot, jotka eivät liity nykyiseen tapahtumaan sijoitetaan yleensä tähän. 

**Tapahtumanäyttö** - Tapahtumanäyttö on POS-sovelluksen päänäyttö myyntitapahtumien ja tilausten käsittelyyn. Tapahtumanäyttö voidaan määrittää näytön asettelun suunnittelutoiminnon avulla. 

**Oletusaloitusnäyttö** - jotkin vähittäismyyjät haluavat, että kassa siirtyy suoraan tapahtumanäyttöön kirjautumisen jälkeen. Oletusaloitusnäytön asetuksen avulla tämä voidaan määrittää kullekin näyttöasettelulle.

### <a name="assignment"></a>Liitos

Näytön asettelut voidaan määrittää myymälän, kassakoneen tai käyttäjän tasolla. Käyttäjän määritys korvaa kassakoneen ja myymälän määrityksen, ja kassakoneen määritys korvaa myymälän määrityksen. Yksinkertaisessa tilanteessa, jossa kaikki käyttäjät käyttävät samaa asettelua riippumatta kassakoneesta tai roolista, näytön asettelu voidaan määrittää vain myymälässä. Tapauksissa, jossa tietyt kassakoneet tai käyttäjät vaativat erityisiä asetteluita, ne voidaan määritellä asianmukaisesti.

### <a name="layout-sizes"></a>Asettelukoot

Tämä ominaisuus on käytössä vain Dynamics 365 for Operations -versiossa 1611. Koska useissa tapauksissa näytön asetteluita voidaan käyttää useissa näyttökoissa ja tarkkuuksissa, käyttäjät voivat määrittää kullekin näyttötyypille oman asettelun ja sisällön. POS-sovellus valitsee automaattisesti asettelun lähimmän koon laitteen käynnistyksen yhteydessä. Näytön asettelu voi sisältää myös täysikokoisten ja pienikokoisten laitteiden kokoonpanoja. Tämän kokoonpanon avulla käyttäjä voidaan määrittää yhteen näyttöasetteluun, joka toimii myymälän erikokoissa ja erityyppisissä laitteissa. 

**Modern POS - täydellinen** - täydelliset asettelut ovat yleensä parhaimmillaan suurissa näytöissä kuten PC-näytöissä tai tableteissa. Käyttäjät voivat valita mitä käyttöliittymän osia näytetään, määrittää niiden koon ja sijoittelun ja määrittää niiden yksityiskohtaisia ominaisuuksia. Täydelliset asettelut tukevat sekä vaaka- että pystykokoonpanoja. 

**Modern POS - kompakti** - kompaktit asettelut sopivat parhaiten puhelimiin tai pieniin tabletteihin. Kompaktien laitteiden suunnittelumahdollisuudet ovat rajalliset. Käyttäjät voivat määrittää kuitti- ja summaruutujen sarakkeet ja kentät.

### <a name="screen-layout-designer"></a>Näytön asettelun suunnittelutoiminto

Jokainen näyttöasettelun asettelun koko pitää määrittää näyttöasettelun suunnittelutoiminnossa. Suunnittelijan avulla käyttäjät voivat määrittää tapahtumanäytön käyttöliittymäelementit. Näytön asettelun suunnittelutoiminto käyttää ClickOnce-toimintoa lataamaan, asentamaan ja käynnistämään sovelluksen uusimman version aina, kun se avataan. Tarkista selaimen ClickOnce-käyttövaatimukset – joissakin selaimissa, kuten Chromessa, tarvitaan laajennuksia. 

**Numeronäppäimistö** - numeronäppäimistö on tärkein syöttötapa myyntipisteen tapahtumanäytössä. Se voidaan määrittää näyttämään näppäimistön kokonaan, mikä sopii erinomaisesti kosketusnäyttölaitteille, tai vain syötekentän, jota voidaan käyttää fyysisen näppäimistön kanssa. Numeronäppäimistön asetukset ovat käytettävissä vain täydellisessä asettelussa. Dynamics 365 for Operations -versiossa 1611 kompakteissa asetteluissa on täydellinen numeronäppäimistö aina näkyvillä tapahtumanäytössä.

**Summapaneeli** - summapaneeliin voidaan määrittää joko yksi tai kaksi saraketta näyttämään kentät kuten rivin määrä, alennussumma, kulut, välisumma ja ALV. Dynamics 365 for Operations -versiossa 1611 kompaktit asettelut tukevat vain yhtä summasaraketta. 

**Kuitti** - Kuittipaneeli sisältää myyntirivit, maksurivit ja toimitustiedot myyntipisteessä käsitellyille tuotteille ja palveluille. Käyttäjät voivat määrittää sarakkeet, leveydet ja sijainnit. Dynamics 365 for Operations -version 1611 kompakteissa näytöissä voit määrittää myös lisätiedot, jotka näkyvät päärivin alapuolella. 

**Asiakaskortti** - asiakaskortti näyttää tällä hetkellä tapahtumaan liittyvän asiakkaan tietoja. Asiakaskortti voidaan määrittää näyttämään tai piilottamaan lisätiedot. 

**Välilehtiohjausobjekti** - Välilehtiohjausobjekti voidaan sijoittaa näyttöasetteluun, ja muut ohjausobjektit, kuten numeronäppäimistö, asiakaskortti ja painikeruudukko voidaan sijoittaa välilehden sisään. Välilehtiohjausobjekti on säilö, joka auttaa käyttäjiä mahduttamaan enemmän sisältöä näyttöön. Välilehtiohjausobjekti on käytettävissä vain täydellisissä asetteluissa. 

**Kuva** - Kuva-ohjausobjektia voidaan käyttää näyttämään myymälän logo tai muu brändikuva tapahtumanäytössä. Kuva-ohjausobjekti on käytettävissä vain täydellisissä asetteluissa. 

**Suositellut tuotteet** - Jos tämä on määritetty ympäristöön, Suositellut tuotteet -ohjausobjekti näyttää tuote-ehdotuksia koneoppimiseen perustuen. Suositellut tuotteet-ohjausobjekti on käytettävissä vain Dynamics 365 for Operations -version 1611 täydellisissä asetteluissa. **Mukautettu ohjausobjekti **- Mukautettu ohjausobjekti toimii näytössä paikkamerkkinä varaamassa tilaa mukautetulle sisällölle. Mukautettu ohjausobjekti on käytettävissä vain täydellisissä asetteluissa.

<a name="see-also"></a>Lisätietoja
--------

[Retail POS-asettelun suunnittelutoiminto asentaminen](install-pos-layout-designer.md)




