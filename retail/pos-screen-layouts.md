---
title: "Näytön asettelun määrittäminen POS"
description: "Tässä aiheessa on tietoja toimintojen - vähittäiskaupan myynti (POS) kokemuksia kohdan Microsoft Dynamics-365 näytön asettelua."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application user
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 90573
ms.assetid: a6868f93-02ed-4928-9f6a-3b7383e7e399
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d49c5c9773047940e524c71e59a674ebe8460ad7
ms.lasthandoff: 03/31/2017


---

# <a name="configure-screen-layouts-for-pos"></a>Näytön asettelun määrittäminen POS

Tässä aiheessa on tietoja toimintojen - vähittäiskaupan myynti (POS) kokemuksia kohdan Microsoft Dynamics-365 näytön asettelua.

Microsoft Dynamics-365 työvaiheiden - vähittäiskaupan myynti (POS)-käyttöliittymän kohdan voidaan määrittää visuaaliset profiilit ja näytön asettelut, kaupat, kassakoneet ja/tai käyttäjien määritetty yhdistelmä.

## <a name="visual-profile"></a>Visuaalinen profiili
Visuaaliset profiilit määritetään rekisterit ja visuaalisia elementtejä, joilla on erityinen rekisteri ja jaettu käyttäjille määritetään. Rekisterin tiedot kirjautuva käyttäjä on teemaa, värit ja kuvat. **Profiilin numero** -profiili on visuaalisen profiilin yksilöivä tunnus. **Kuvaus** -kuvauksen avulla voit määrittää kuvaava nimi, joka auttaa tunnistamaan oikean profiilin tilanteen. **Teema** -käyttäjät voivat valita Vaalea tai Tumma teemoja sovelluksen välillä. Nämä asetukset vaikuttavat koko sovellus fontin ja taustan värit. **Korostus väri** -lisävärejä käytetään koko Myyntipiste erottaa tai korostaa tiettyjä visuaalisia elementtejä, kuten laatat, painikkeita tai hyperlinkkejä. Nämä elementit ovat yleensä käyttökelpoisempaa. **Otsikon väri** -otsikon väri antaa käyttäjän määrittää sivun otsikon vähittäismyyjän yrityskohtaiset tarpeiden väri. Tämä ominaisuus on käytettävissä vain Dynamics 365-version toimintoja 1611. **Kirjautuminen taustoja** -käyttäjät voivat määrittää kirjautumisen näytön taustakuvana. Taustakuvat tiedostokoko on pidettävä mahdollisimman pieni, tallentaminen ja lastaus suuria tiedostoja on vaikutusta sovelluksen toimintaa ja suorituskykyä. **Sovelluksen tausta** -Myyntipisteen voit myös käyttää kuvan koko sovelluksen sijaan yhtenäinen teema väriä taustan. Kirjautuminen taustoja ja se on suositeltavaa pitää tiedostokoko mahdollisimman mahdollisimman vähän.

## <a name="screen-layouts"></a>Näytön asettelut
Näytön asettelun kokoonpano määrittää toimintoja, sisällön ja UI komponentit POS-Tervetuloa-näyttö ja näytön tapahtuman sijainti. ** Tervetuloa **-Tervetuloa-näyttö on yleensä sivu, jonka käyttäjät näkevät, kun he ensin kirjautua POS. Tervetuloa-näyttö voi koostua tavaramerkin kuva painikeruudukot, jotka tarjoavat pääsyn Myyntipisteen toimintoja. Toiminnot, jotka eivät liity nykyiseen tapahtumaan sijoitetaan yleensä tähän. **Tapahtuman näytön** -Transaction-näyttö on POS-sovelluksen päänäytössä myynti ja tilausten käsittelyyn. Tapahtuma-ikkunassa voidaan määrittää näytön asettelun suunnittelutoiminto. **Oletusarvon mukaiset aloituspäivän näytön** -jotkin vähittäismyyjät mieluummin, että kassa siirtyä suoraan näytön tapahtuman jälkeen kirjautuminen. Käynnistä näyttö oletusasetuksen mukaan käyttäjien määrittäminen kunkin näyttöasettelun.

### <a name="assignment"></a>Liitos

Näytön asettelu voidaan määrittää myymälän, rekisterin tai käyttäjän tasolla. Käyttäjän tehtävä ohittaa rekisterin ja tallentaa tehtävän ja varauksen Rekisteri korvaa säilön määritys. Yksinkertainen tilanteessa, jossa kaikki käyttäjät käyttää samaa asettelua rekisteri tai rooli näytön asettelu voidaan määrittää vain myymälässä. Tapauksissa, jossa tiettyihin rekistereihin tai käyttäjät vaativat erityisiä rakenteita ne voidaan määritellä asianmukaisesti.

### <a name="layout-sizes"></a>Asettelukoot

Tämä ominaisuus koskee vain version toiminnot 1611 Dynamics 365. Koska useissa tapauksissa voidaan käyttää näytön asettelun kautta useita Näyttökoot ja tarkkuudet, käyttäjät voivat määrittää niiden ulkoasu ja sisältö kunkin. POS-sovellus valitsee automaattisesti asettelun lähin koko laitteen käynnistyksen yhteydessä. Näytön asettelu voi sisältää myös täysi- ja compact laitteiden kokoonpanoja. Tämä kokoonpano avulla käyttäjä voi määrittää yhden näyttöasettelun, joka toimii eri kokoja ja lomakkeen tekijät säilössä. **Täydellinen Moderni POS -** -koko rakenteita käytetään yleensä parhaiten suurempia näkyy kuten PC-näytöissä tai tabletit. Käyttäjät voivat valita mitä Käyttöliittymän osat ovat, määrittää niiden koon ja asettelun ja määrittää niiden yksityiskohtaisia ominaisuuksia. Koko asettelut tukevat sekä vaaka- ja kokoonpanoja. **Moderni POS - Compact** -Compact asettelut parhaiten käytetään yleensä puhelimet tai pieni tabletit. Compact laitteiden rajoittuvat suunnittelun mahdollisuuksia. Käyttäjät voivat määrittää kentät vastaanotto- ja summat-ruudut ja sarakkeet.

### <a name="screen-layout-designer"></a>Näytön asettelun suunnittelutoiminto

Jokaisen asettelun kokoisen näytön asettelu on määritettävä käyttäen näytön asettelun suunnittelutoiminto. Suunnittelija avulla käyttäjät voivat määrittää ja määrittää tapahtuman näytön käyttöliittymäelementit. Näytön asettelun suunnittelutoiminto käyttää ClickOnce ladata, asentaa ja käynnistää sovelluksen käyttäjällä on oikeus käyttää sitä aina uusinta versiota. Tarkista selaimen ClickOnce käyttövaatimukset – joissakin selaimissa, Chrome, kuten vaatia laajennuksia. **Numeronäppäimistön** -numeronäppäimistön on tärkein syöttötapa-tapahtuman POS-näytön. Se voidaan määrittää näyttämään kokonaan näytössä pad, joka sopii erinomaisesti kosketusnäyttö, tai vain syötekentän, jota voidaan käyttää fyysistä näppäimistöä. Pad asetukset ovat käytettävissä vain täydellinen asettelu. Dynamics-365-version toimintoja 1611 compact asettelut on aina täydellinen numeronäppäimistön käytettävissä tapahtuman näytöstä. **Summat-paneelin** - paneelin summat voidaan määrittää joko yhden tai kahden sarakkeen näytettävät kentät kuten rivin määrä, alennussumma, kulut, välisumma ja ALV. Dynamics 365 version toiminnot 1611 compact asettelut tukevat vain yhtä summat-sarakkeen. **Kuitti** -** ** vastaanotto-paneeli sisältää myyntirivit, maksurivit ja tuotteiden ja palvelujen myyntipisteessä käsitellään toimitustiedot. Käyttäjät voivat määrittää sarakkeiden leveydet ja sijainti. Voit myös määrittää version toiminnot 1611 Dynamics 365 compact asetteluja, joka tulee näkyviin päärata-rivin lisätiedot. **Asiakkaan kortti** - asiakastiedot kortti näyttää tällä hetkellä tapahtumaan liittyvän asiakkaan mainoksissa. Voit piilottaa tai näyttää muita tietoja voidaan määrittää asiakaskortille. **Ohjausobjektin välilehdestä** - välilehti-ohjausobjektia voidaan sijoittaa näyttöasettelun ja muut ohjausobjektit, esimerkiksi numeronäppäimistön asiakkaan kortti tai painikeruudukot voi sijoittaa sisään välilehti. Välilehti-ohjausobjektin on säilö, joka auttaa käyttäjiä mahtuu enemmän sisältöä näytön. Välilehti-ohjain on käytettävissä vain koko asetteluissa. ** Kuva **-logon tai muu tavaramerkin kuva näyttää tapahtuman näytössä voidaan käyttää kuvakehys. Kuva-ohjausobjekti on käytettävissä vain koko asetteluissa. **Suositellut tuotteet** - Jos määritetty ohjausobjekti näyttää Tuote-ehdotukset perustuvat machine learning suositellut tuotteet ympäristön. Suositellut tuotteet-ohjausobjekti on käytettävissä vain koko version toiminnot 1611 Dynamics 365 asettelut. ** Mukautetun ohjausobjektin **-mukautettu ohjausobjekti toimii paikkamerkin sisällä näyttöasettelun avulla käyttäjät voivat varata tilaa mukautettua sisältöä varten. Mukautettu ohjausobjekti on käytettävissä vain koko asetteluissa.

<a name="see-also"></a>Lisätietoja
--------

[Install the Retail POS Layout designer](install-pos-layout-designer.md)


