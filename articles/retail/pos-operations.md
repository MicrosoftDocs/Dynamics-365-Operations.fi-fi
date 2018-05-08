---
title: POS-toiminnot verkossa ja paikallisesti
description: "Tässä ohjeaiheessa on tietoja Microsoft Dynamics 365 for Retail -sovelluksen myyntipisteen toiminnoista. Ohjeaihe määrittää, missä kohdassa sovellusta toiminnot voidaan käynnistää ja ovatko ne käytettävissä offline-tilassa."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 8a24f8adc4f7886a1f942d83f7a4eb12e7034fcd
ms.openlocfilehash: d8cf283321b81c377498cd449b098f8fac1fe01f
ms.contentlocale: fi-fi
ms.lasthandoff: 03/22/2018

---

# <a name="pos-operations-online-and-offline"></a>POS-toiminnot verkossa ja paikallisesti

[!include [banner](includes/banner.md)]

Useimmat käyttäjän myyntipisteessä tekemät toimenpiteet ovat toimintoja. Toiminnot määritetään ja niitä hallinnoidaan Microsoft Dynamics 365 for Retail -sovelluksen taustajärjestelmässä. Myyntipisteen painikeruudukon painikkeisiin voi lisätä useita toimintoja. Käyttäjät voivat tämän jälkeen valita painikkeita ja käynnistää toimintoja. Muut toiminnot ovat osa myyntipisteen pääsovellusta. Ne käynnistetään joko näytön painikkeiden avulla tai muiden työnkulkujen tai prosessien osana.

Seuraavassa taulukossa on tietoja Dynamics 365 for Retail -sovelluksen Retail Modern POS- tai Cloud POS -myyntipisteen toiminnoista. Taulukossa määritetään myös, missä kohdassa sovellusta toiminnot voidaan käynnistää ja ovatko ne käytettävissä, kun myyntipiste on offline-tilassa.

Jotkin toiminnot eivät ole tällä hetkellä käytettävissä Dynamics 365 for Retail -sovelluksen Retail Modern POS- tai Cloud POS -myyntipisteessä. Jotkin toiminnot ovat paikallisia toimintoja. Ne edellyttävät lisälaajennuksia ja -konfiguraation. Joitakin Microsoft Dynamics AX 2012:n toimintoja ei tueta tällä hetkellä.

Seuraavat sarakkeet määsittävät toimintojen käynnistyskohdan:

- **Painikeruudukko** – toiminto voidaan määrittää myyntipisteen näyttöasettelun osana toimivien painikeruudukoiden painikkeisiin.
- **Tapahtumanäyttö** – toiminto voidaan käynnistää myyntipisteen painikeruudukoista, jotka on määritetty myyntipisteen tapahtumanäytössä.
- **Aloitusnäyttö** – toiminto voidaan käynnistää myyntipisteen painikeruudukoista, jotka on määritetty myyntipisteen aloitusnäytössä.

Huomautus: Alla mainitut toiminnot koskevat Dynamics 365 for Retail -sovelluksen uusinta versiota. Osa toiminnosta on ehkä muuttunut tai niitä ei ollut aiemmissa versioissa.

| Tunnus | Työvaihe | kuvaus | Painikeruudukko | Tapahtumanäyttö | Aloitusnäyttö | Käytettävissä offline-tilassa | Paikallinen |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivoi laite | Aktivoi nykyinen laite sallimalla todennettujen käyttäjien määrittää yhteystiedot ja määrittää liitteen ja kassakoneen tunnus. | En | En | En | En | En |
| 134 | Lisää liitos | Lisää ennalta valittu liitos tapahtumaan. Valitse liitos **Painikkeen ominaisuudet** -sivulla. | Kyllä | Kyllä | En | Kyllä | En |
| 135 | Lisää liitos luettelosta | Lisää liitos tapahtumaan valitsemalla se luettelosta. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 643 | Lisää kuponkikoodi | Lisää kuponki syöttämällä sen koodi myyntipisteessä. | Kyllä | Kyllä | En | Kyllä | En |
| 117 | Lisää kanta-asiakaskortti | Käyttäjää pyydetään syöttämään kanta-asiakaskortin numero. Se lisätään nykyiseen tapahtumaan. | Kyllä | Kyllä | En | Kyllä | En |
| 136 | Lisää sarjanumero | Tämän toiminnon avulla käyttäjä voi määrittää valitun tuotteen sarjanumeron. | Kyllä | Kyllä | En | Kyllä | En |
| 1 214 | Lisää toimitusosoite | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 519 | Lisää lahjakorttiin | Lisää rahaa määritettyyn lahjakorttiin. | Kyllä | Kyllä | En | En | En |
| 6 000 | Salli tilikausirekisteröinnin ohitus | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 1 212 | Toimitus pankkiin | Kirjaa pankkiin määritetyn rahamäärän ja muita tietoja, kuten rahankuljetuslaukun numeron. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 923 | Pankin yhteissummien tarkistus | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 915 | Tyhjä toiminto | Tämä toiminto edustaa mukautettavaa painiketta, jonka ohjelmistokehittäjä voi määrittää ohjelmallisesti mitä tahansa liiketoiminnassa tarvittavaa erikoistoimintoa varten. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1 053 | Piilotettu suljettu vuoro | Määritä nykyinen vuoro piilotetuksi suljetuksi vuoroksi ja kirjaa käyttäjä ulos. Piilotetun suljetun vuoron lisätapahtumat on suljettu. Siinä voi kuitenkin suorittaa kassatoimintoja, kuten maksuvälineen poiston ja kassan laskemisen maksuvälineittäin. | Kyllä | Kyllä | Kyllä | En | En |
| 310 | Laske kokonaissumma | Kun alennuksen laskeminen viivästyy, tämä toiminto käynnistää nykyisen tapahtuman laskennan. | Kyllä | Kyllä | En | Kyllä | En |
| 642 | Toteutus - kaikki tuotteet | Määritä kaikkien rivien toimitustavaksi **Nouto liikkeestä**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 641 | Toteutus - valitut tuotteet | Määritä valittujen rivien toimitustavaksi **Nouto liikkeestä**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 1 215 | Vaihda salasana | Tämän toiminnon avulla myyntipisteen käyttäjä voi vaihtaa oman salasanansa. | Kyllä | Kyllä | Kyllä | En | En |
| 123 | Muuta mittayksikköä | Muuta valitun rivinimikkeen mittayksikkö. | Kyllä | Kyllä | En | Kyllä | En |
| 639 | Poista tapahtuman oletusmyyntiedustaja | Poista provisiomyyntiryhmä (myyjä) tapahtumasta. | Kyllä | Kyllä | En | Kyllä | En |
| 106 | Tyhjennä määrä | Palauta valitun rivin määräksi **1**. | Kyllä | Kyllä | En | Kyllä | En |
| 640 | Poista myyntiedustaja riviltä | Poista provisiomyyntiryhmä (myyjä) valitulta riviltä. | Kyllä | Kyllä | En | Kyllä | En |
| 121 | Tyhjennä myyjä | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 1 055 | Sulje vuoro | Sulje nykyinen vuoro, tulosta Z-raportti ja kirjaa käyttäjä ulos järjestelmästä. | Kyllä | Kyllä | Kyllä | En | En |
| 925 | Kopioi pankkisekki | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 620 | Luo asiakastilaus | Muunna myyntipisteen tapahtuma asiakastilaukseksi. | Kyllä | Kyllä | En | Kyllä\* | En |
| 621 | Luo tarjous | Muunna myyntipisteen tapahtuma myyntitarjoukseksi. | Kyllä | Kyllä | En | Kyllä\* | En |
| 636 | Vähittäismyyntitapahtuman luominen | Tämän toiminnon avulla käyttäjä voi luoda vakiomyyntitapahtuman, kun oletusmyyntipisteen toiminta on asiakastilausten luominen. | Kyllä | Kyllä | En | Kyllä | En |
| 600 | Asiakas | Lisää määritetty asiakas tapahtumaan. | En | En | En | Kyllä | En |
| 1 100 | Asiakastilin talletus | Suorita maksu asiakkaan tilille. | Kyllä | Kyllä | Kyllä | Kyllä | Kyllä |
| 612 | Asiakkaan lisääminen | Tämän toiminnon avulla käyttäjä voi luoda uuden asiakastietueen. | Kyllä | Kyllä | Kyllä | Kyllä† | En |
| 603 | Asiakkaan tyhjentäminen | Poista asiakas nykyisestä tapahtumasta. | Kyllä | Kyllä | En | Kyllä | En |
| 602 | Asiakashaku | Tämän toiminnon avulla käyttäjä voi hakea asiakastietueen siirtymällä asiakkaan hakusivulle myyntipisteessä. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 609 | Asiakastapahtumat | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 917 | Tietokantayhteyden tila | Tämän toiminnon avulla käyttäjä voi tarkastella nykyisen yhteyden asetuksia ja siirtyä online- ja offline-tilojen välillä. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1 200 | Tilitä aloitussumma | Määritä summa, joka on kassassa päivän tai vuoron alkaessa. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 132 | Talletuksen ohitus | Ohita asiakastilausten oletusarvoinen ennakkomaksu. | Kyllä | Kyllä | En | Kyllä\* | En |
| 913 | Suunnittelutilan poistaminen käytöstä | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 912 | Suunnittelutilan ottaminen käyttöön | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 1 217 | Pura myyntirakenteet | Pura myyntirakenne sen komponenttituotteiksi. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 624 | Palautussummien näyttäminen | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 513 | Näytä summa | Näytä tapahtuman saldo asiakkaan näytössä. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 623 | Muokkaa asiakasta | Muokkaa nykyisen asiakkaan tietoja. | Kyllä | Kyllä | En | En | En |
| 614 | Muokkaa asiakastilausta | Jatka valittua tilausta niin, että sitä voidaan muokata myyntipisteessä. | En | En | En | En | En |
| 615 | Muokkaa tarjousta | Jatka valittua tarjousta niin, että sitä voidaan muokata myyntipisteessä. | En | En | En | En | En |
| 518 | Kulutilit | Kirjaa kassasta satunnaisia kuluja varten poistettavat rahat. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 919 | Jatkettu kirjautuminen | Määritä tai poista sisäänkirjautumisoikeus lukemalla viivakoodi tai kortti. | Kyllä | Kyllä | Kyllä | En | En |
| 1201 | Liukuva merkintä | Tämän toiminnon avulla käyttäjä voi lisätä rahaa nykyiseen kassaan tai vuoroon. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1218 | Pakota oheislaitteen lukituksen poisto | Järjestelmä käyttää tätä toimintoa sisäisesti myyntipisteen oheislaitteiden lukituksen poistamiseen. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 520 | Lahjakortin saldo | Näytä lahjakortin saldo. | Kyllä | Kyllä | En | En | En |
| 708 | Poista laitteen aktivointi | Poista nykyisen laitteen aktivointi niin, että sitä ei voi käyttää myyntipisteen kassakoneena. | En | En | En | En | En |
| 517 | Tulotilit | Rahasumma, joka sijoitetaan kassaan muusta kuin myynnistä johtuvasta syystä. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 801 | Varastohaku | Haku käytettävissä tilauksessa ja luvattavissa olevat määrät (ATP) nykyisessä myymälässä ja muissa käytettävissä olevissa sijainneissa. | Kyllä | Kyllä | Kyllä | En | En |
| 122 | Laskun kommentti | Tämän toiminnon avulla käyttäjä voi syöttää nykyistä tapahtumaa koskevan kommentin. | Kyllä | Kyllä | En | Kyllä | En |
| 511 | Myönnä hyvityslasku | Luo hyvityslasku ja anna tosite palautuksen sijaan. | Kyllä | Kyllä | En | En | En |
| 512 | Myönnä lahjakortti | Luo uusi lahjakortti määritetylle summalle. | Kyllä | Kyllä | En | En | En |
| 625 | Myönnä kanta-asiakaskortti | Anna asiakkaalle kanta-asiakkuuskortti, jotta asiakas voi osallistua myymälän kanta-asiakasohjelmaan. | Kyllä | Kyllä | Kyllä | En | En |
| 300 | Rivialennuksen summa | Kirjoita alennussumma tapahtuman rivinimikkeelle. Tätä toimintoa käytetään nimikkeille joista voidaan antaa alennusta, ja vain määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | En | Kyllä | En |
| 301 | Rivialennusprosentti | Kirjoita alennusprosentti tapahtuman rivinimikkeelle. Tätä toimintoa käytetään nimikkeille joista voidaan antaa alennusta, ja vain määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | En | Kyllä | En |
| 703 | Lukitse kassakone | Lukitse nykyinen kassakone, jolloin sitä ei voi käyttää. Nykyistä käyttäjää ei kuitenkaan kirjata ulos. | En | En | En | Kyllä | En |
| 701 | Kirjaudu ulos | Kirjaa nykyinen käyttäjä ulos kassakoneelta. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 521 | Kanta-asiakaskorttien pistesaldo | Näytä määritetyn kanta-asiakaskortin pistesaldo. | Kyllä | Kyllä | En | En | En |
| 918 | Ylläpidä työvuoroja | Näytä aktiivisten, keskeytettyjen ja piilotettujen suljettujen vuorojen luettelo. | Kyllä | Kyllä | Kyllä | En | En |
| 914 | Pienennä myyntipisteen ikkuna | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 1 000 | Kassan avaus | Suorita Ei myynti -toiminto ja avaa valittuna oleva kassakone. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 928 | Tilauksen täyttäminen | Tämän toiminnon avulla käyttäjät voivat kerätä, pakata, lähettää tai peruuttaa tilauksia myymälänoutoa varten. | Kyllä | Kyllä | Kyllä | En | En |
| 129 | Ohita rivituotteen vero | Ohita valitun rivinimikkeen vero ja käytä toista määritettyä veroa. | Kyllä | Kyllä | En | Kyllä | En |
| 130 | Ohita rivituotteen vero luettelosta | Ohita valitun rivinimikkeen vero ja korvaa sen verolla, jonka käyttäjä valitsee luettelosta. | Kyllä | Kyllä | En | Kyllä | En |
| 127 | Ohita tapahtuman vero | Ohita tapahtuman vero ja käytä toista määritettyä veroa. | Kyllä | Kyllä | En | Kyllä | En |
| 128 | Ohita tapahtuman vero luettelosta | Ohita tapahtuman vero ja korvaa sen verolla, jonka käyttäjä valitsee luettelosta. | Kyllä | Kyllä | En | Kyllä | En |
| 131 | Pakkausluettelo | Luo valitun tilauksen pakkausluettelo. | En | En | En | En | En |
| 710 | Muodosta laiteaseman laitepari | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 201 | Maksa kortilla | Hyväksy maksuksi kortti, kuten luottokortti tai pankkikortti. | Kyllä | Kyllä | En | Kyllä | En |
| 200 | Maksa käteisellä | Hyväksy käteismaksu. | Kyllä | Kyllä | En | Kyllä | En |
| 206 | Tee pikakäteismaksu | Viiimeistele tapahtuma yhdellä painalluksella ja hyväksy erääntyvä summa käteisenä (tasaraha). | Kyllä | Kyllä | En | Kyllä | En |
| 204 | Maksa sekillä | Hyväksy sekki maksuksi. | Kyllä | Kyllä | En | Kyllä | En |
| 213 | Maksa hyvityslaskulla | Hyväksy myymälän luoma hyvityslasku (tosite). | Kyllä | Kyllä | En | En | En |
| 203 | Maksa valuutalla | Hyväksy eri valuuttoina suoritettavat maksut. | Kyllä | Kyllä | En | Kyllä | En |
| 202 | Maksa asiakastililtä | Veloita tapahtuma asiakkaan tililtä. Maksutapa ei ole sallittu asiakkaan tilaustalletuksissa. | Kyllä | Kyllä | En | En | En |
| 214 | Maksa lahjakortilla | Hyväksy myymälän luoma lahjakortti. | Kyllä | Kyllä | En | En | En |
| 207 | Maksa kanta-asiakaskortilla | Hyväksy kanta-asiakaskortti maksuksi ja lunasta hyväksyttyjen tuotteiden pisteet. | Kyllä | Kyllä | En | En | En |
| 634 | Maksuhistoria | Näytä asiakkaan maksuhistoria nykyiselle asiakastilaukselle. | Kyllä | Kyllä | En | En | En |
| 803 | Keräys ja vastaanotto | Avaa **Keräys ja vastaanotto** -sivu, jolla voit valita tilaukset myymälän keräystä ja vastaanottoa varten. | Kyllä | Kyllä | Kyllä | En | En |
| 632 | Nouda kaikki tuotteet | Määritä kaikkien rivien toteutustavaksi **Nouto myymälästä**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 631 | Nouda valitut tuotteet | Määritä valittujen rivien toteutustavaksi **Nouto myymälästä**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 400 | Ponnahdusvalikko | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 101 | Hinnantarkistus | Tämän toiminnon avulla käyttäjä voi etsiä määritetyn tuotteen hinnan. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 104 | Hinnan ohitus | Ohita tuotteen hinta, jos tuotteen hinnan ohitukset on sallittu. | Kyllä | Kyllä | En | Kyllä | En |
| 1 058 | Tulosta kuitti X | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 1 059 | Tulosta kuitti Z | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 927 | Tulosta nimike-etiketti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 926 | Tulosta hyllyetiketti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 1 056 | Tulosta X | Tulosta nykyinen vuoro ja muodosta siitä X-raportti. | Kyllä | Kyllä | Kyllä | En | En |
| 103 | Tuotteen kommentti | Lisää kommentti valittuun rivinimikkeeseen tapahtumassa. | Kyllä | Kyllä | En | Kyllä | En |
| 100 | Tuotemyynti | Lisää määritetty tuote tapahtumaan. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 108 | Tuotehaku | Tämän toiminnon avulla käyttäjä voi hakea tuotteen siirtymällä tuotteen hakusivulle myyntipisteessä. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 633 | Tarjouksen vanhentumispäivä | Tämän toiminnon avulla käyttäjä voi tarkastella myyntitarjouksen vanhentumispäivämäärää tai muokata sitä. | Kyllä | Kyllä | En | Kyllä\* | En |
| 627 | Laske uudelleen | Laske kaikki asiakastilauksen rivit ja verot uudelleen nykyisen konfiguraation perusteella. | Kyllä | Kyllä | En | Kyllä\* | En |
| 515 | Jatka tilausta | Tämän toiminnon avulla käyttäjä voi hakea ja jatkaa asiakastilauksia ja myyntitarjouksia. | Kyllä | Kyllä | Kyllä | En | En |
| 504 | Jatka tapahtumaa | Tämän toiminnon avulla käyttäjä voi jatkaa aiemmin keskeytetyn tapahtuman nykyisessä myymälässä. | Kyllä | Kyllä | En | Kyllä# | En |
| 305 | Lunasta kanta-asiakkuuspisteet | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 635 | Hyvitä toimitusmaksut | Tämän toiminnon avulla käyttäjä voi hyvittää peruutetun tilauksen toimitusmaksut. | En | En | En | En | En |
| 644 | Poista kuponkikoodi | Käyttäjää pyydetään poistamaan kupongit valitsemalla ne tapahtumaan tällä hetkellä liitetystä kuponkiluettelosta. | Kyllä | Kyllä | En | Kyllä | En |
| 1 057 | Tulosta Z uudelleen | Tulosta edellisen vuoron tai valitun vuoron Z-raportti. | Kyllä | Kyllä | Kyllä | En | En |
| 1 216 | Nollaa salasana | Tämän toiminnon avulla salasanan palautuksen käyttöoikeuden omaava käyttäjä voi palauttaa toisen työntekijän salasanan tilapäisen salasanan avulla. | Kyllä | Kyllä | Kyllä | En | En |
| 109 | Palauta tuote | Suorita yksittäisten tuotteiden palautus. Seuraava skannattu tuote näytetään palautettuna tuotteena, jolla on negatiivinen määrä ja hinta. | Kyllä | Kyllä | En | Kyllä | En |
| 114 | Palautustapahtuma | Jatka edellistä tapahtumaa sen vastaanottonumeron avulla ja palauta jotkin sen tuotteista. | Kyllä | Kyllä | Kyllä | Kyllä§ | En |
| 1 211 | Toimitus kassakaappiin | Suorita toimitus kassakaappiin, jossa rahat siirretään kassakoneesta kassakaappiin. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 516 | Myyntilasku | Tämän toiminnon avulla asiakas voi maksaa valitun myyntilaskun. | Kyllä | Kyllä | En | En | En |
| 502 | Myyjä | Tämän toiminnon avulla käyttäjä voi määrittää **myynnin vastaanottajan** arvon myyntipisteen asiakastilausten myyntitilauksissa. | Kyllä | Kyllä | En | Kyllä\* | En |
| 2 000 | Aikataulujen hallinta | Tämän toiminnon avulla käyttäjät voivat luoda, muokata ja tarkastella työntekijän aikatauluja. | Kyllä | Kyllä | Kyllä | En | En |
| 2 001 | Aikataulupyynnöt | Tämän toiminnon avulla käyttäjä voi pyytää vapaata töistä, vaihtaa vuoroja tai tarjota vuoroa muille työntekijöille. | Kyllä | Kyllä | Kyllä | En | En |
| 622 | Hae | Tämän toiminnon avulla käyttäjät voivat määrittää ennalta myyntipisteen painikkeita ja suorittaa hakuja nimikkeen, asiakkaan tai luokan mukaan. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1 213 | Hae toimitusosoitetta | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 709 | Valitse laiteasema | Tämän toiminnon avulla käyttäjä voi valita laiteaseman käytettävissä olevien laiteasemien luettelosta. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 637 | Määritä tapahtuman oletusmyyntiedustaja | Tämän toiminnon avulla käyttäjä voi valita jonkin provisiomyyntiryhmän (myyjät) myöhemmin lisättävien rivien oletusmyyjäksi. | Kyllä | Kyllä | En | Kyllä | En |
| 105 | Määritä määrä | Muuta tapahtuman rivinimikkeen määrää. | Kyllä | Kyllä | En | Kyllä | En |
| 638 | Aseta myyntiedustaja riville | Tämän toiminnon avulla käyttäjä voi valita jonkin provisiomyyntiryhmän (myyjät) parhaillaan valittuna olevalle riville. | Kyllä | Kyllä | En | Kyllä | En |
| 630 | Lähetä kaikki tuotteet | Määritä kaikkien rivinimikkeiden toteutustavaksi **Lähetys**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 629 | Lähetä valitut tuotteet | Määritä valittujen rivien toteutustavaksi **Lähetys**. | Kyllä | Kyllä | En | Kyllä\* | En |
| 115 | Näytä kirjauskansio | Näytä myymälän kirjauskansio. Voit tarkastella tapahtumia, tulostaa kuitteja ja lahjojen kuitteja uudelleen ja palauttaa niitä palautusta varten. | Kyllä | Kyllä | Kyllä | Kyllä\*\* | En |
| 802 | Varaston inventointi | Tämän toiminnon avulla käyttäjä voi luoda varastotilanteelle tai inventoinneille varastonlaskennan kirjauskansioita tai muokata niitä. | Kyllä | Kyllä | Kyllä | En | En |
| 401 | Alavalikko | Tämä toiminto siirtää käyttäjän toiseen linkitettyyn painikeruudukkoon. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1 054 | Keskeytä vuoro | Keskeytä nykyinen vuoro niin, että nykyiselle kassakoneelle voidaan aktivoida uusi vuoro tai jokin muu vuoro. | Kyllä | Kyllä | Kyllä | En | En |
| 503 | Keskeytä tapahtuma | Keskeytä nykyinen myyntitapahtuma niin, että sitä voidaan jatkaa myöhemmin myymälässä. | Kyllä | Kyllä | En | Kyllä# | En |
| 1004 | Tehtävän tallennustoiminto | Avaa tehtävien tallennustoiminto ja tallenna myyntipisteen menettelytapavaiheet. | En | En | En | Kyllä | En |
| 1 052 | Kassan laskeminen maksuvälineittäin | Tämän toiminnon avulla käyttäjä voi määrittää kassan rahasumman kullekin inventoidulle maksutavalle. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 1 210 | Maksuvälineen poisto | Tämän toiminnon avulla käyttäjä voi poistaa rahaa nykyisestä kassasta tai vuorosta. | Kyllä | Kyllä | Kyllä | Kyllä | En |
| 920 | Kello | Tämän toiminnon avulla käyttäjät voivat leimata itsensä sisään työvuoroihin ja tauoille ja niiltä ulos. | Kyllä | Kyllä | Kyllä | En | En |
| 302 | Kokonaisalennuksen summa | Syötä tapahtuman alennussumma. Tätä toimintoa käytetään vain nimikkeissä, joista voidaan antaa alennusta määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | En | Kyllä | En |
| 303 | Kokonaisalennusprosentti | Syötä tapahtuman alennusprosentti. Tätä toimintoa käytetään vain nimikkeissä, joista voidaan antaa alennusta määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | En | Kyllä | En |
| 501 | Tapahtuman kommentti | Lisää kommentti nykyiseen tapahtumaan. | Kyllä | Kyllä | En | Kyllä | En |
| 922 | Näytä tuotteen tiedot | Avaa valittuna olevan rivinimikkeen tuotetietojen sivu. | Kyllä | Kyllä | En | Kyllä | En |
| 1003 | Raporttien tarkasteleminen | Näytä nykyiselle käyttäjälle määritetyt raportit. | Kyllä | Kyllä | Kyllä | En | En |
| 921 | Näytä aikamerkinnät | Näytä kaikkien myymälän työntekijöiden aikamerkinnät. | Kyllä | Kyllä | Kyllä | En | En |
| 211 | Mitätöi maksu | Mitätöi tapahtuman valittuna oleva maksurivi. | Kyllä | Kyllä | En | Kyllä | En |
| 102 | Mitätöi tuote | Mitätöi tapahtuman valittuna oleva rivinimike. | Kyllä | Kyllä | En | Kyllä | En |
| 500 | Mitätöi tapahtuma | Mitätöi nykyinen tapahtuma. | Kyllä | Kyllä | En | Kyllä | En |
| 916 | Windows-työnkulun perusta | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | En |
| 924 | Pankkikorttien X-raportti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |

\* Toiminto on käytettävissä offline-tilassa vain, kun asiakastilausta tai myyntitilausta luodaan ja kun näiden tilausten offiline-tilassa tapahtuva luominen on määritetty myyntipisteen toimintoprofiilissa. Toimintoa ei voi suorittaa, kun tilaukset luodaan Real-time Service -palvelun avulla tai kun tilauksia jatketaan tai muokataan.

† Toiminnon voi suorittaa offline-tilassa vain, kun asiakkaiden offline-tilassa luominen on sallittu myyntipisteen toimintoprofiilissa.

‡ Kun myyntipiste on offline-tilassa, keskeytettyjä tapahtumia voidaan jatkaa vain nykyisen kassakoneen offline-tietokannasta. Käyttäjät eivät voi peruuttaa ja jatkaa tapahtumia missä tahansa kassakoneissa.

§ Kun myyntipiste on offline-tilassa, vain nykyisen offline-tietokannan tapahtumia voi jatkaa palautusta varten.

\*\* Kun myyntipiste on offline-tilassa, vain nykyisen offline-kanavatietokannan tapahtumat näytetään kirjauskansiossa.

