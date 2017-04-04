---
title: Kirjanpidon ulkomaanvaluutan uudelleenarvostus
description: "Tässä aiheessa on yleiskatsaus seuraavista kirjanpidon ulkomaanvaluutan uudelleenarvostuksen prosessin - asennuksen prosessi, prosessi ja miten uudelleenarvostus, tapahtumat täytyy palauttaa laskutoimituksen suorittaminen tarvittaessa."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Kirjanpidon ulkomaanvaluutan uudelleenarvostus

Tässä aiheessa on yleiskatsaus seuraavista kirjanpidon ulkomaanvaluutan uudelleenarvostuksen prosessin - asennuksen prosessi, prosessi ja miten uudelleenarvostus, tapahtumat täytyy palauttaa laskutoimituksen suorittaminen tarvittaessa. 

Kirjanpidon käytännöt edellyttävät kauden lopussa tehtävää kirjanpitotilien valuuttamääräisten saldojen uudelleenarvostusta käyttäen eri vaihtokurssityyppejä (nykyinen, historiallinen, keskiarvo jne.). Esimerkiksi yksi kirjanpitomenetelmä edellyttää saamisten ja velkojen uudelleenarvostusta nykyisellä vaihtokurssilla, käyttöomaisuuden uudelleenarvostusta historiallisen vaihtokurssin mukaan sekä tulostilien uudelleenarvostusta kuukauden keskiarvon mukaan. Kirjanpidon ulkomaanvaluutan uudelleenarvostusta voidaan käyttää taseen ja tasetilien uudelleenarvostukseen. 

> [!NOTE]
> Ulkomaanvaluutan uudelleenarvostus on myös käytettävissä (AR) myyntireskontran ja ostoreskontran (AP). Jos käytät näitä moduuleja, avoimet tapahtumat arvostetaan avulla näiden moduulien ulkomaanvaluutan uudelleenarvostuksen. Ostoreskontran ja myyntireskontran ulkomaanvaluutan uudelleenarvostus luo kirjanpitoon kirjauksen, joka kuvaa toteutumatonta voittoa tai tappiota, joilla varmistetaan, että alareskontrat ja kirjanpito voidaan täsmäyttää. Koska ostoreskontran ja myyntireskontran ulkomaanvaluutan uudelleenarvostus luo kirjauksia kirjanpitoon, myyntireskontran ja ostoreskontran päätilit on jätettävä kirjanpidon ulkomaanvaluutan uudelleenarvostuksen ulkopuolelle. 

Uudelleenarvostusprosessia suoritettaessa kunkin päätilin ulkomaan valuuttana kirjattu saldo uudelleenarvostetaan. Uudelleenarvostusprosessin aikana luodut toteutumaton voitto- tai tappiotransaktiot ovat järjestelmän luomia. Kaksi tapahtumaa voi voidaan luoda yksi kirjanpitovaluutta ja toinen raportointi valuutan tarvittaessa; Kirjaa kirjanpidon tekstien Realisoitumaton voitto tai tappio ja muutoksista päätili.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen suorittamisen valmisteleminen
Seuraavat asetukset on määritettävä ennen uudelleenarvostusprosessin suorittamista.

-   **Päätili**-sivulla:
-   Jos päätili pitää uudelleenarvostaa kirjanpidossa, valitse **Ulkomaanvaluutan uudelleenarvostus**. Jos päätiliä ei uudelleenarvosteta (esimerkiksi jos ostoreskontra ja myyntireskontra uudelleenarvostetaan osakirjanpidossa), poista tämän valintaruudun valinta.
-   Jos päätili on valittuna uudelleenarvostettavaksi, kirjoita **vaihtokurssin tyyppi**. Tätä vaihtokurssia käytetään päätilin uudelleenarvostamisessa. Erillistä **Talousraportoinnin vaihtokurssin tyyppi** -kenttää voidaan käyttää taloushallinnon raporteissa. Kahta kenttää ei ole synkronoitu, joten uudelleenarvostuksessa ja taloushallinnon raporteissa voidaan käyttää eri vaihtokurssityyppejä.

-   **Kirjanpito**-sivulla:
-   Määritä **vaihtokurssin tyyppi**. Jos päätilin vaihtokurssin tyyppiä ei ole määritetty, tätä vaihtokurssia käytetään ulkomaanvaluutan uudelleenarvostuksen yhteydessä.
-   Määritä valuutan uudelleenarvostuksen toteutuneen voiton, toteutuneen tappion, toteutumattoman voiton ja toteutumattoman tappion tilit. Toteutuneen voiton ja toteutuneen tappion tilejä käytetään selvitettäessä osto- ja myyntireskontran tapahtumia ja toteutumattoman voiton ja toteutumattoman tappion tilejä uudelleenarvioitaessa avoimia tapahtumia ja kirjanpidon päätilejä.

-   **Valuutan uudelleenarvostustilit**-sivulla:
-   Valitse toinen valuutan uudelleenarvostustili jokaiselle valuutalle ja yritykselle. Jos tilejä ei ole määritetty, käytetään **Kirjanpito**-sivun tilejä.

## <a name="process-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen käsittely
Kun asetukset on tehty, päätilien saldot uudelleenarvostetaan **Ulkomaanvaluutan uudelleenarvostus** -sivun avulla. Voit suorittaa prosessin reaaliaikaisena tai ajoittaa sen erän avulla. 

**Ulkomaanvaluutan uudelleenarvostus**-sivulla näkyvät kunkin uudelleenarvostusprosessi historiatiedot, mukaan lukien ajankohta jolloin prosessi on suoritettu, mitä kriteereitä määritettiin, linkki uudelleenarvostustositteeseen ja merkintä edellisen uudelleenarvostuksen peruuttamisesta. Voit suorittaa uudelleenarvostusprosessin valitsemalla **Ulkomaanvaluutan uudelleenarvostus** -painikkeen. 

**Aloituspäivämäärä** ja **päättymispäivämäärä**- arvot määrittävät päivämäärävälin, jolla valuuttasaldo lasketaan uudelleenarvostusta varten. Kun tulostilit uudelleenarvostetaan, kaikkien päivämääräalueella suoritettavien tapahtumien summa uudelleenarvostetaan. Kun tasetili uudelleenarvostetaan, aloituspäivämäärää ei oteta huomioon. Sen sijaan uudelleenarvostettava saldo määräytyy tilivuoden alusta päättymispäivämäärään. 

**Kurssin päivämäärä** avulla voit määrittää päivämäärän, jonka vaihtokurssi oletus. Esimerkiksi voit uudelleenarvostaa saldojen välisen päivämäärä alue, tammikuun 1 tammikuu 31, mutta käytetään vaihtokurssia, joka on määritelty 1 päivänä helmikuuta. 

Valitse mitä päätilejä käytetään: kaikki, tasetili, tulostili. Vain päätilit uudelleenarvostuksen (-tilin pääsivu) merkitään niiden uudelleenarvostuksen. Jos haluat rajoittaa edelleen alueen päätilit, käytä tietueiden **sisältämään** -välilehti ja Määritä päätilit tai yksittäisiä päätilit. 

Uudelleenarvostusprosessi voi suorittaa yhden tai useamman oikeussubjektien. Hakua näyttää vain juridiset henkilöt, joihin sinulla on käyttöoikeus. Valitse oikeushenkilöt, joille haluat suorittaa uudelleenarvostuksen prosessi. 

Uudelleenarvostus voidaan tehdä yhden tai useiden valuuttojen suhteen. Haku sisältää kaikki valuutat, jotka on kirjattu päivämäärävälillä päätilin (taseen tai tuloslaskelman), jos haluat uudelleenarvostaa valitut oikeushenkilöt lajin kannalta. Kirjanpitovaluutan valuuttakoodi sisältyy luetteloon, mutta mitään uudelleenarvostetaan, jos on valittu kirjanpitovaluutta. 

Määritä **esikatselu ennen kirjausta**, **Kyllä**, jos haluat tarkastella pääkirjanpidon uudelleenarvostuksen tulos. Esikatselu yleensä kirjanpidon eroaa-AR- ja AP-ulkomaanvaluutan uudelleenarvostuksen simulointi. Myyntireskontran ja Ostoreskontran simulointi on raportti, mutta kirjanpito on esikatselu, joka voidaan kirjata tarvitsematta suorittaa uudelleenarvostuksen prosessin uudelleen. Esikatselun tulokset voidaan viedä Microsoft Exceliin säilyttämään historiatiedot, kuinka määrät on laskettu. Et voi käyttää eräkäsittelyä, jos haluat esikatsella uudelleenarvostuksen tuloksia. Esikatselussa käyttäjä voi kirjata kaikkien oikeushenkilöiden tulokset **Kirjaa** -painikkeella. Jos yhden oikeushenkilön tuloksissa on ongelma, käyttäjällä voi kirjata oikeushenkilöiden osajoukon **Valitse kirjattavat yritykset** -painikkeella. 

Ulkomaanvaluutan uudelleenarvostus-prosessi on valmis, kun tietue luodaan jäljittää jokaisen sarjan.  Erillinen tietue luodaan kullekin oikeushenkilölle ja kirjanpitotaso.

## <a name="calculate-unrealized-gainloss"></a>Laske toteutumaton voitto/tappio
Toteutumaton voitto/tappio-tapahtumat luodaan erillään kirjanpidon uudelleenarvostuksesta ja ostoreskontran ja myyntireskontran uudelleenarvostusprosessista. Ostoreskontran ja myyntireskontran edellinen uudelleenarviointi palautetaan kokonaan (olettaen, että tapahtumaa ei ole vielä selvitetty) ja luodaan uusi tapahtuma toteutumattomalle voitolle/tappiolle uuden vaihtokurssin mukaan. Tämä johtuu siitä, että ostoreskontran ja myyntireskontran jokainen yksittäinen tapahtuma uudelleenarvioidaan. Kirjanpidossa Edellinen uudelleenarvostus ei ole palautettu. Sen sijaan delta välisen tasapainon päätili, mukaan lukien perusteella vaihtokurssin nopeus päivämäärä uuden arvon ja edellisen summien uudelleenarvostus luodaan tapahtuma. 

**Esimerkki** on olemassa seuraavat saldot päätilin 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Päivämäärä**   | **Kirjanpitotili** | **Tapahtuman summa** | **Kirjanpitosumma** |
| 20. tammikuuta | 110110 (käteinen)      | 500 EUR (debet)        | 1000 USD (debet)      |

Päätilin arvostetaan tammikuun 31.  Toteutumaton voitto/tappio lasketaan seuraavasti.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Nykyinen saldo tapahtuman valuuttana** | **Nykyinen saldo kirjanpitovaluuttana** | **Vaihtokurssi uudelleenarvostuksessa** | **Uusi summa kirjanpitovaluuttana** | **Toteutumaton voitto/tappio**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 tappio (833,33-1000) |

Seuraava kirjanpitomerkintä luodaan.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Päivämäärä**   | **Kirjanpitotili**       | **Veloitus** | **Hyvitys** |
| 31. tammikuuta | 110110 (käteinen)            |           | 166.67     |
| 31. tammikuuta | 801400 (toteutumaton tappio) | 166.67    |            |

Uusi eikä tapahtumia kirjata kuukauden helmikuuta.  Päätilin arvostetaan-helmikuun 28.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Nykyinen saldo tapahtuman valuuttana** | **Nykyinen saldo kirjanpitovaluuttana** | **Vaihtokurssi uudelleenarvostuksessa** | **Uusi summa kirjanpitovaluuttana** | **Toteutumaton voitto/tappio**    |
| 500 EUR                                     | 833,33 USD (1000-166.67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 voitto (1250-833,33) |

Seuraava kirjanpitomerkintä luodaan.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Päivämäärä**    | **Kirjanpitotili**       | **Veloitus** | **Hyvitys** |
| Helmikuun 28. | 110110 (käteinen)            | 416.67    |            |
| Helmikuun 28. | 801600 (toteutumaton voitto) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen palautus
Jos uudelleenarvostustapahtuma pitää palauttaa, valitse **Palautustapahtuma** -painike**Ulkomaanvaluutan uudelleenarvostus**-sivulla. Uusi ulkomaanvaluutan uudelleenarvostus -historiatietue luodaan ylläpitämään historian kirjausketjua ulkomaanvaluutan uudelleenarvioinnin ajankohdasta tai palautuksesta. 

Voit peruuttaa tulokset uudelleenarvostuksen päivämäärä ei toimi, mutta sinun täytyy peruuttaa myös entistä paremmin ajan tasalla varmistaakseen että oikeat saldot jokaisen uudelleenarvostettujen päätilin uudelleenarvostus. Peruutukset voi ilmetä ajan tasalla järjestyksessä, koska ei voi määrittää, mitkä päätilit arvostetaan ja kun ne arvostetaan taajuus on. Esimerkiksi organisaation pakko arvostaa uudelleen niiden cash päätilit neljännesvuosittain, mutta kaikki muut päätilit kuukausittain.


