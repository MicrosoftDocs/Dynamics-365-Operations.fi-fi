---
title: Myyntipisteen toiminnot (POS) verkossa ja paikallisesti
description: Tässä ohjeaiheessa on tietoja Dynamics 365 Commercen myyntipisteen toiminnoista. Ohjeaihe määrittää, missä kohdassa sovellusta toiminnot voidaan käynnistää ja ovatko ne käytettävissä offline-tilassa.
author: jblucher
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-09-27
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5e139b7b12b8f2e549fb9c2c8e39125e190c7396
ms.sourcegitcommit: 4d52c67f52ad0add63cd905df61367b344389069
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/16/2022
ms.locfileid: "8311976"
---
# <a name="online-and-offline-point-of-sale-pos-operations"></a>Myyntipisteen toiminnot (POS) verkossa ja paikallisesti

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Useimmat käyttäjien myyntipisteessä tekemät toimenpiteet ovat toimintoja. Toiminnot määritetään ja niitä hallinnoidaan Dynamics 365 Commercen taustajärjestelmässä. Myyntipisteen painikeruudukon painikkeisiin voi lisätä useita toimintoja. Käyttäjät voivat tämän jälkeen valita painikkeita ja käynnistää toimintoja. Muut toiminnot ovat osa myyntipisteen pääsovellusta. Ne käynnistetään joko näytön painikkeiden avulla tai muiden työnkulkujen tai prosessien osana.

Seuraavassa taulukossa on tietoja Modern POS- ja Cloud POS -toiminnoista. Taulukossa määritetään myös, missä kohdassa sovellusta toiminnot voidaan käynnistää ja ovatko ne käytettävissä, kun myyntipiste on offline-tilassa.

Jotkin toiminnot eivät ole tällä hetkellä käytettävissä Modern POS:ssa tai Cloud POS:ssa. Jotkin toiminnot ovat paikallisia toimintoja. Ne edellyttävät lisälaajennuksia ja -konfiguraation. Joitakin Microsoft Dynamics AX 2012:n toimintoja ei tueta tällä hetkellä.

Seuraavat sarakkeet määsittävät toimintojen käynnistyskohdan:

- **Painikeruudukko** – toiminto voidaan määrittää myyntipisteen näyttöasettelun osana toimivien painikeruudukoiden painikkeisiin.
- **Tapahtumanäyttö** – toiminto voidaan käynnistää myyntipisteen painikeruudukoista, jotka on määritetty myyntipisteen tapahtumanäytössä.
- **Aloitusnäyttö** – toiminto voidaan käynnistää myyntipisteen painikeruudukoista, jotka on määritetty myyntipisteen aloitusnäytössä.

> [!NOTE]
> Alla mainitut toiminnot koskevat Commercen uusinta versiota. Osa toiminnosta on ehkä muuttunut tai niitä ei ollut aiemmissa versioissa.


| Tunnus | Työvaihe | kuvaus | Painikeruudukko | Tapahtumanäyttö | Aloitusnäyttö | Käytettävissä offline-tilassa | Paikallinen |
|----|-----------|-------------|-------------|--------------------|----------------|-------------------|-----------------|
| 707 | Aktivoi laite | Aktivoi nykyinen laite sallimalla todennettujen käyttäjien määrittää yhteystiedot ja määrittää liitteen ja kassakoneen tunnus. | Ei | Ei | Ei | Ei | Ei |
| 134 | Lisää liitos | Lisää ennalta valittu liitos tapahtumaan. Valitse liitos **Painikkeen ominaisuudet** -sivulla. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 135 | Lisää liitos luettelosta | Lisää liitos tapahtumaan valitsemalla se luettelosta. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 137 | Lisää liitos asiakkaaseen | Lisää liitos asiakkaaseen **Asiakastiedot**-sivulla. | Ei | Ei | Ei | Kyllä | Ei |
| 138 | Poista asiakkaan liitos | Poista liitos **Asiakastiedot**-sivulla. | Ei | Ei | Ei | Kyllä | Ei |
| 643 | Lisää kuponkikoodi | Lisää kuponki syöttämällä sen koodi myyntipisteessä. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 141 | Lisää otsikon kulut | Lisää muut kulut tilauksen otsikkoon. | Kyllä | Kyllä | Ei | Ei| Ei |
| 141 | Lisää rivin kulut | Lisää muut kulut valitulle myyntiriville. | Kyllä | Kyllä | Ei | Ei| Ei |
| 117 | Lisää kanta-asiakaskortti | Käyttäjää pyydetään syöttämään kanta-asiakaskortin numero. Se lisätään nykyiseen tapahtumaan. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 136 | Lisää sarjanumero | Tämän toiminnon avulla käyttäjä voi määrittää valitun tuotteen sarjanumeron. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 1 214 | Lisää toimitusosoite | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 519 | Lisää lahjakorttiin | Lisää rahaa määritettyyn lahjakorttiin. | Kyllä | Kyllä | Ei | Ei | Ei |
| 6 000 | Salli tilikausirekisteröinnin ohitus | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 1 212 | Toimitus pankkiin | Kirjaa pankkiin määritetyn rahamäärän ja muita tietoja, kuten rahankuljetuslaukun numeron. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 923 | Pankin yhteissummien tarkistus | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 915 | Tyhjä toiminto | Tämä toiminto edustaa mukautettavaa painiketta, jonka ohjelmistokehittäjä voi määrittää ohjelmallisesti mitä tahansa liiketoiminnassa tarvittavaa erikoistoimintoa varten. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1 053 | Piilotettu suljettu vuoro | Määritä nykyinen vuoro piilotetuksi suljetuksi vuoroksi ja kirjaa käyttäjä ulos. Piilotetun suljetun vuoron lisätapahtumat on suljettu. Siinä voi kuitenkin suorittaa kassatoimintoja, kuten maksuvälineen poiston ja kassan laskemisen maksuvälineittäin. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 310 | Laske kokonaissumma | Kun alennuksen laskeminen viivästyy, tämä toiminto käynnistää nykyisen tapahtuman laskennan. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 642 | Toteutus - kaikki tuotteet | Määritä kaikkien rivien toimitustavaksi **Nouto liikkeestä**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 641 | Toteutus - valitut tuotteet | Määritä valittujen rivien toimitustavaksi **Nouto liikkeestä**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 647 | Muuta toimitustapaa | Muuta esimääritettyjen lähetyksen myyntirivien toimitustapaa. | Kyllä | Kyllä | Ei | Ei| Ei |
| 1215 | Vaihda salasana | Tämän toiminnon avulla myyntipisteen käyttäjä voi vaihtaa oman salasanansa. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 123 | Muuta mittayksikköä | Muuta valitun rivinimikkeen mittayksikkö. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 639 | Poista tapahtuman oletusmyyntiedustaja | Poista provisiomyyntiryhmä (myyjä) tapahtumasta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 106 | Tyhjennä määrä | Palauta valitun rivin määräksi **1**. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 640 | Poista myyntiedustaja riviltä | Poista provisiomyyntiryhmä (myyjä) valitulta riviltä. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 121 | Tyhjennä myyjä | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 1 055 | Sulje vuoro | Sulje nykyinen vuoro, tulosta Z-raportti ja kirjaa käyttäjä ulos järjestelmästä. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 139 | Päätä tapahtuma | Pyytää käyttäjää valitsemaan maksutavan | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 925 | Kopioi pankkisekki | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 620 | Luo asiakastilaus | Muunna myyntipisteen tapahtuma asiakastilaukseksi. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 621 | Luo tarjous | Muunna myyntipisteen tapahtuma myyntitarjoukseksi. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 636 | Vähittäismyyntitapahtuman luominen | Luo vakiomyyntitapahtuma, kun oletusmyyntipisteen toiminta on asiakastilausten luominen. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 600 | Asiakas | Lisää määritetty asiakas tapahtumaan. | Ei | Ei | Ei | Kyllä | Ei |
| 1 100 | Asiakastilin talletus | Suorita maksu asiakkaan tilille. | Kyllä | Kyllä | Kyllä | Kyllä | Kyllä |
| 612 | Asiakkaan lisääminen | Uuden asiakastietueen luominen. | Kyllä | Kyllä | Kyllä | Kyllä† | Ei |
| 603 | Asiakkaan tyhjentäminen | Poista asiakas nykyisestä tapahtumasta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 602 | Asiakashaku | Hae asiakastietuetta siirtymällä asiakkaan hakusivulle myyntipisteessä. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 609 | Asiakastapahtumat | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 917 | Tietokantayhteyden tila | Tarkastele nykyisen yhteyden asetuksia ja siirtyä online- ja offline-tilojen välillä. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1 200 | Tilitä aloitussumma | Määritä summa, joka on kassassa päivän tai vuoron alkaessa. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 132 | Talletuksen ohitus | Ohita asiakastilausten oletusarvoinen ennakkomaksu. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 913 | Suunnittelutilan poistaminen käytöstä | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 912 | Suunnittelutilan ottaminen käyttöön | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 1 217 | Pura myyntirakenteet | Pura myyntirakenne sen komponenttituotteiksi. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 624 | Palautussummien näyttäminen | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 513 | Näytä summa | Näytä tapahtuman saldo asiakkaan näytössä. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 623 | Muokkaa asiakasta | Muokkaa nykyisen asiakkaan tietoja. | Kyllä | Kyllä | Ei | Ei | Ei |
| 614 | Muokkaa asiakastilausta | Jatka valittua tilausta niin, että sitä voidaan muokata myyntipisteessä. | Ei | Ei | Ei | Ei | Ei |
| 615 | Muokkaa tarjousta | Jatka valittua tarjousta niin, että sitä voidaan muokata myyntipisteessä. | Ei | Ei | Ei | Ei | Ei |
| 518 | Kulutilit | Kirjaa kassasta satunnaisia kuluja varten poistettavat rahat. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 919 | Jatkettu kirjautuminen | Määritä tai poista sisäänkirjautumisoikeus lukemalla viivakoodi tai kortti. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1201 | Liukuva merkintä | Lisää rahaa nykyiseen kassaan tai vuoroon. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1218 | Pakota oheislaitteen lukituksen poisto | Järjestelmä käyttää tätä toimintoa sisäisesti myyntipisteen oheislaitteiden lukituksen poistamiseen. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 520 | Lahjakortin saldo | Näytä lahjakortin saldo. | Kyllä | Kyllä | Ei | Ei | Ei |
| 708 | Poista laitteen aktivointi | Poista nykyisen laitteen aktivointi niin, että sitä ei voi käyttää myyntipisteen kassakoneena. | Ei | Ei | Ei | Ei | Ei |
| 804 | Saapuva toiminto | Käytä saapuvan myymälän varastonhallinnan toimintoja. | Kyllä | Ei | Kyllä | Ei| Ei |
| 517 | Tulotilit | Rahasumma, joka sijoitetaan kassaan muusta kuin myynnistä johtuvasta syystä. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 801 | Varastohaku | Haku käytettävissä tilauksessa ja luvattavissa olevat määrät (ATP) nykyisessä myymälässä ja muissa käytettävissä olevissa sijainneissa. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 806 | Varaston oikaisu | Oikaise myymälävarastossa olevaa tai olematonta varastoa käyttämällä oikaisu- tai siirtokirjauskansiota. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 807 | Varaston siirtotapahtuma | Siirrä nimikkeitä yhdestä varastosijainnista toiseen myymälävaraston sisällä. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 122 | Laskun kommentti | Lisää nykyistä tapahtumaa koskeva kommentti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 511 | Myönnä hyvityslasku | Luo hyvityslasku ja anna tosite palautuksen sijaan. | Kyllä | Kyllä | Ei | Ei | Ei |
| 512 | Myönnä lahjakortti | Luo uusi lahjakortti määritetylle summalle. | Kyllä | Kyllä | Ei | Ei | Ei |
| 625 | Myönnä kanta-asiakaskortti | Anna asiakkaalle kanta-asiakkuuskortti, jotta asiakas voi osallistua myymälän kanta-asiakasohjelmaan. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 300 | Rivialennuksen summa | Kirjoita alennussumma tapahtuman rivinimikkeelle. Tätä toimintoa käytetään nimikkeille joista voidaan antaa alennusta, ja vain määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 301 | Rivialennusprosentti | Kirjoita alennusprosentti tapahtuman rivinimikkeelle. Tätä toimintoa käytetään nimikkeille joista voidaan antaa alennusta, ja vain määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 703 | Lukitse kassakone | Lukitse nykyinen kassakone, jolloin sitä ei voi käyttää. Nykyistä käyttäjää ei kuitenkaan kirjata ulos. | Ei | Ei | Ei | Kyllä | Ei |
| 701 | Kirjaudu ulos | Kirjaa nykyinen käyttäjä ulos kassakoneelta. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 521 | Kanta-asiakaskorttien pistesaldo | Näytä määritetyn kanta-asiakaskortin pistesaldo. | Kyllä | Kyllä | Ei | Ei | Ei |
| 142 | Kulujen hallinta | Tarkastele ja hallitse tapahtumaa koskevia muuttuvia kuluja. | Kyllä | Kyllä | Ei | Ei| Ei |
| 918 | Ylläpidä työvuoroja | Näytä aktiivisten, keskeytettyjen ja piilotettujen suljettujen vuorojen luettelo. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 914 | Pienennä myyntipisteen ikkuna | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 1 000 | Kassan avaus | Suorita Ei myynti -toiminto ja avaa valittuna oleva kassakone. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 928 | Tilauksen täyttäminen | Tämän toiminnon avulla käyttäjät voivat kerätä, pakata, lähettää tai peruuttaa tilauksia myymälänoutoa varten. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 805 | Lähtevä toiminto | Käytä lähtevien siirtotilausten siirtojen lähetysten hallinnan toimintoja. | Kyllä | Ei | Kyllä | Ei| Ei |
| 129 | Ohita rivituotteen vero | Ohita valitun rivinimikkeen vero ja käytä toista määritettyä veroa. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 130 | Ohita rivituotteen vero luettelosta | Ohita valitun rivinimikkeen vero ja korvaa sen verolla, jonka käyttäjä valitsee luettelosta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 127 | Ohita tapahtuman vero | Ohita tapahtuman vero ja käytä toista määritettyä veroa. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 128 | Ohita tapahtuman vero luettelosta | Ohita tapahtuman vero ja korvaa sen verolla, jonka käyttäjä valitsee luettelosta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 131 | Pakkausluettelo | Luo valitun tilauksen pakkausluettelo. | Ei | Ei | Ei | Ei | Ei |
| 710 | Muodosta laiteaseman laitepari | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 201 | Maksa kortilla | Hyväksy maksuksi kortti, kuten luottokortti tai pankkikortti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 200 | Maksa käteisellä | Hyväksy käteismaksu. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 206 | Tee pikakäteismaksu | Viiimeistele tapahtuma yhdellä painalluksella ja hyväksy erääntyvä summa käteisenä (tasaraha). | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 204 | Maksa sekillä | Hyväksy sekki maksuksi. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 213 | Maksa hyvityslaskulla | Hyväksy myymälän luoma hyvityslasku (tosite). | Kyllä | Kyllä | Ei | Ei | Ei |
| 203 | Maksa valuutalla | Hyväksy eri valuuttoina suoritettavat maksut. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 202 | Maksa asiakastililtä | Veloita tapahtuma asiakkaan tililtä. Maksutapa ei ole sallittu asiakkaan tilaustalletuksissa. | Kyllä | Kyllä | Ei | Ei | Ei |
| 214 | Maksa lahjakortilla | Hyväksy myymälän luoma lahjakortti. | Kyllä | Kyllä | Ei | Ei | Ei |
| 207 | Maksa kanta-asiakaskortilla | Hyväksy kanta-asiakaskortti maksuksi ja lunasta hyväksyttyjen tuotteiden pisteet. | Kyllä | Kyllä | Ei | Ei | Ei |
| 634 | Maksuhistoria | Näytä asiakkaan maksuhistoria nykyiselle asiakastilaukselle. | Kyllä | Kyllä | Ei | Ei | Ei |
| 803 | Keräys ja vastaanotto | Avaa **Keräys ja vastaanotto** -sivu, jolla voit valita tilaukset myymälän keräystä ja vastaanottoa varten. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 632 | Nouda kaikki tuotteet | Määritä kaikkien rivien toteutustavaksi **Nouto myymälästä**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 631 | Nouda valitut tuotteet | Määritä valittujen rivien toteutustavaksi **Nouto myymälästä**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 400 | Ponnahdusvalikko | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 101 | Hinnantarkistus | Tämän toiminnon avulla käyttäjä voi etsiä määritetyn tuotteen hinnan. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 104 | Hinnan ohitus | Ohita tuotteen hinta, jos tuotteen hinnan ohitukset on sallittu. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 1 058 | Tulosta kuitti X | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 1 059 | Tulosta kuitti Z | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 927 | Tulosta nimike-etiketti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 926 | Tulosta hyllyetiketti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 1 056 | Tulosta X | Tulosta nykyinen vuoro ja muodosta siitä X-raportti. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 103 | Tuotteen kommentti | Lisää kommentti valittuun rivinimikkeeseen tapahtumassa. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 100 | Tuotemyynti | Lisää määritetty tuote tapahtumaan. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 108 | Tuotehaku | Hae tuotetta siirtymällä tuotteen hakusivulle myyntipisteessä. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 633 | Tarjouksen vanhentumispäivä | Tarkastele myyntitarjouksen vanhentumispäivämäärää tai muokkaa sitä. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 627 | Laske uudelleen | Laske kaikki asiakastilauksen rivit ja verot uudelleen nykyisen konfiguraation perusteella. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 143 | Laske veloitukset uudelleen | Laske uudelleen tilausta koskevat automaattiset kulut. | Kyllä | Kyllä | Ei | Ei| Ei |
| 515 | Jatka tilausta | Hae ja jatka asiakastilauksia ja myyntitarjouksia. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 504 | Jatka tapahtumaa | Jatka aiemmin keskeytettyä tapahtumaa nykyisessä myymälässä. | Kyllä | Kyllä | Ei | Kyllä# | Ei |
| 305 | Lunasta kanta-asiakkuuspisteet | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 635 | Hyvitä toimitusmaksut | Peruuta tilauksen lähetyskulujen hyvitys. | Ei | Ei | Ei | Ei | Ei |
| 644 | Poista kuponkikoodi | Käyttäjää pyydetään poistamaan kupongit valitsemalla ne tapahtumaan tällä hetkellä liitetystä kuponkiluettelosta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 1 057 | Tulosta Z uudelleen | Tulosta edellisen vuoron tai valitun vuoron Z-raportti. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 1 216 | Nollaa salasana | Tämän toiminnon avulla salasanan palautuksen käyttöoikeuden omaava käyttäjä voi palauttaa toisen työntekijän salasanan tilapäisen salasanan avulla. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 1219 | URL-osoitteen avaaminen myyntipisteessä | Avaa myyntipisteen järjestelmänvalvojan konfiguroitu URL-osoite. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 109 | Palauta tuote | Suorita yksittäisten tuotteiden palautus. Seuraava skannattu tuote näytetään palautettuna tuotteena, jolla on negatiivinen määrä ja hinta. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 114 | Palautustapahtuma | Jatka edellistä tapahtumaa sen vastaanottonumeron avulla ja palauta jotkin sen tuotteista. | Kyllä | Kyllä | Kyllä | Kyllä§ | Ei |
| 1 211 | Toimitus kassakaappiin | Suorita toimitus kassakaappiin, jossa rahat siirretään kassakoneesta kassakaappiin. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 516 | Myyntilasku | Tämän toiminnon avulla asiakas voi maksaa valitun myyntilaskun. | Kyllä | Kyllä | Ei | Ei | Ei |
| 502 | Myyjä | Määritä **myynnin vastaanottajan** arvo myyntipisteen asiakastilausten myyntitilauksissa. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 2000 | Aikataulujen hallinta | Tätä toimintoa ei tueta vielä. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 2001 | Aikataulupyynnöt | Tätä toimintoa ei tueta vielä. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 622 | Etsi tilauksia | Tämän toiminnon avulla käyttäjät voivat määrittää ennalta myyntipisteen painikkeita ja suorittaa hakuja nimikkeen, asiakkaan tai luokan mukaan. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1 213 | Hae toimitusosoitetta | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 709 | Valitse hardware station | Valitse laiteasema käytettävissä olevien laiteasemien luettelosta. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 637 | Määritä tapahtuman oletusmyyntiedustaja | Valitse jokin provisiomyyntiryhmä (myyjät) myöhemmin lisättävien rivien oletusmyyjäksi. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 105 | Määritä määrä | Muuta tapahtuman rivinimikkeen määrää. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 638 | Aseta myyntiedustaja riville | Valitse jokin provisiomyyntiryhmä (myyjät) parhaillaan valittuna olevalle riville. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 630 | Lähetä kaikki tuotteet | Määritä kaikkien rivinimikkeiden toteutustavaksi **Lähetys**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 629 | Lähetä valitut tuotteet | Määritä valittujen rivien toteutustavaksi **Lähetys**. | Kyllä | Kyllä | Ei | Kyllä\* | Ei |
| 115 | Näytä kirjauskansio | Näytä myymälän kirjauskansio. Voit tarkastella tapahtumia, tulostaa kuitteja ja lahjojen kuitteja uudelleen ja palauttaa niitä palautusta varten. | Kyllä | Kyllä | Kyllä | Kyllä\*\* | Ei |
| 802 | Varaston inventointi | Luo varastotilanteelle tai inventoinneille varastonlaskennan kirjauskansioita tai muokkaa niitä. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 401 | Alavalikko | Tämä toiminto siirtää käyttäjän toiseen linkitettyyn painikeruudukkoon. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1 054 | Keskeytä vuoro | Keskeytä nykyinen vuoro niin, että nykyiselle kassakoneelle voidaan aktivoida uusi vuoro tai jokin muu vuoro. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 503 | Keskeytä tapahtuma | Keskeytä nykyinen myyntitapahtuma niin, että sitä voidaan jatkaa myöhemmin myymälässä. | Kyllä | Kyllä | Ei | Kyllä# | Ei |
| 1004 | Tehtävän tallennustoiminto | Avaa tehtävien tallennustoiminto ja tallenna myyntipisteen menettelytapavaiheet. | Ei | Ei | Ei | Kyllä | Ei |
| 1 052 | Kassan laskeminen maksuvälineittäin | Määritä kassan rahasumma kullekin inventoidulle maksutavalle. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 1 210 | Maksuvälineen poisto | Poista rahaa nykyisestä kassasta tai työvuorosta. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 920 | Kellonaika | Leimaa sisään työvuoroihin ja tauoille ja niiltä ulos. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 302 | Kokonaisalennuksen summa | Syötä tapahtuman alennussumma. Tätä toimintoa käytetään vain nimikkeissä, joista voidaan antaa alennusta määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 303 | Kokonaisalennusprosentti | Syötä tapahtuman alennusprosentti. Tätä toimintoa käytetään vain nimikkeissä, joista voidaan antaa alennusta määritettyjen alennusrajojen mukaisesti. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 501 | Tapahtuman kommentti | Lisää kommentti nykyiseen tapahtumaan. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 922 | Näytä tuotteen tiedot | Avaa valittuna olevan rivinimikkeen tuotetietojen sivu. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 1003 | Raporttien tarkasteleminen | Näytä nykyiselle käyttäjälle määritetyt raportit. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 921 | Näytä aikamerkinnät | Näytä kaikkien myymälän työntekijöiden aikamerkinnät. | Kyllä | Kyllä | Kyllä | Ei | Ei |
| 211 | Mitätöi maksu | Mitätöi tapahtuman valittuna oleva maksurivi. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 102 | Mitätöi tuote | Mitätöi tapahtuman valittuna oleva rivinimike. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 500 | Mitätöi tapahtuma | Mitätöi nykyinen tapahtuma. | Kyllä | Kyllä | Ei | Kyllä | Ei |
| 916 | Windows-työnkulun perusta | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei |
| 924 | Pankkikorttien X-raportti | Tätä toimintoa ei tueta. | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Ei käytettävissä | Kyllä |
| 311 | Poista järjestelmäalennukset tapahtumasta | Poista kaikki järjestelmän käyttämät alennukset, mukaan lukien kuponkialennukset, tapahtumasta. Tämä ei poista manuaalisia alennuksia. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |
| 312 | Käytä järjestelmäalennuksia uudelleen | Käytä tapahtuman järjestelmäalennuksia uudelleen, jos ne on poistettu **Poista järjestelmäalennukset tapahtumasta** -toiminnolla. | Kyllä | Kyllä | Kyllä | Kyllä | Ei |

\* Toiminto on käytettävissä offline-tilassa vain, kun asiakastilausta tai myyntitilausta luodaan ja kun näiden tilausten offiline-tilassa tapahtuva luominen on määritetty myyntipisteen toimintoprofiilissa. Toimintoa ei voi suorittaa, kun tilaukset luodaan Real-time Service -palvelun avulla tai kun tilauksia jatketaan tai muokataan.

† Toiminnon voi suorittaa offline-tilassa vain, kun asiakkaiden offline-tilassa luominen on sallittu myyntipisteen toimintoprofiilissa.

‡ Kun myyntipiste on offline-tilassa, keskeytettyjä tapahtumia voidaan jatkaa vain nykyisen kassakoneen offline-tietokannasta. Käyttäjät eivät voi peruuttaa ja jatkaa tapahtumia missä tahansa kassakoneissa.

§ Kun myyntipiste on offline-tilassa, vain nykyisen offline-tietokannan tapahtumia voi jatkaa palautusta varten.

\*\* Kun myyntipiste on offline-tilassa, vain nykyisen offline-kanavatietokannan tapahtumat näytetään kirjauskansiossa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
