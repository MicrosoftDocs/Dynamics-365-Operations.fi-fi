---
title: Kirjanpidon ulkomaanvaluutan uudelleenarvostus
description: 'Tämä aihe sisältää yhteenvedon kirjanpidon ulkomaan valuutan uudelleenarvostusprosessista seuraavasti: asetukset, prosessin suorittaminen, prosessin laskeminen ja uudelleenarvostustapahtumien palauttaminen tarvittaessa.'
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49f724eb31904c7fd745864c9d71f401a4d539e29b5ff01814334adf6f0ebc37
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771653"
---
# <a name="foreign-currency-revaluation-for-general-ledger"></a>Kirjanpidon ulkomaanvaluutan uudelleenarvostus

[!include [banner](../includes/banner.md)]

Tämä aihe sisältää yhteenvedon kirjanpidon ulkomaan valuutan uudelleenarvostusprosessista seuraavasti: asetukset, prosessin suorittaminen, prosessin laskeminen ja uudelleenarvostustapahtumien palauttaminen tarvittaessa. 

Kirjanpidon käytännöt edellyttävät kauden lopussa tehtävää kirjanpitotilien valuuttamääräisten saldojen uudelleenarvostusta käyttäen eri vaihtokurssityyppejä (nykyinen, historiallinen, keskiarvo jne.). Esimerkiksi yksi kirjanpitomenetelmä edellyttää saamisten ja velkojen uudelleenarvostusta nykyisellä vaihtokurssilla, käyttöomaisuuden uudelleenarvostusta historiallisen vaihtokurssin mukaan sekä tulostilien uudelleenarvostusta kuukauden keskiarvon mukaan. Kirjanpidon ulkomaanvaluutan uudelleenarvostusta voidaan käyttää taseen ja tasetilien uudelleenarvostukseen. 

> [!NOTE]
> Ulkomaanvaluutan uudelleenarvostuksen voi ajaa sekä osto- että myyntireskontrassa. Jos käytät kyseisiä moduuleja, avoimet tapahtumat pitää uudelleenarvostaa käyttäen moduulien ulkomaanvaluutan uudelleenarvostusta. Ostoreskontran ja myyntireskontran ulkomaanvaluutan uudelleenarvostus luo kirjanpitoon kirjauksen, joka kuvaa toteutumatonta voittoa tai tappiota, joilla varmistetaan, että alareskontrat ja kirjanpito voidaan täsmäyttää. Koska ostoreskontran ja myyntireskontran ulkomaanvaluutan uudelleenarvostus luo kirjauksia kirjanpitoon, myyntireskontran ja ostoreskontran päätilit on jätettävä kirjanpidon ulkomaanvaluutan uudelleenarvostuksen ulkopuolelle. 

Uudelleenarvostusprosessia suoritettaessa kunkin päätilin ulkomaan valuuttana kirjattu saldo uudelleenarvostetaan. Uudelleenarvostusprosessin aikana luodut toteutumaton voitto- tai tappiotransaktiot ovat järjestelmän luomia. Kaksi tapahtumaa voidaan luoda, yksi kirjanpitovaluuttaa ja toinen raportointikurssin valuuttaa varten tarvittaessa. Jokainen kirjanpitomerkintä kirjaa toteutumattoman voiton tai tappion ja päätilin uudelleenarvostetaan.

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

**Kurssin päivämäärän** avulla voit määrittää päivämäärän, joka on vaihtokurssin oletusarvo. Voit esimerkiksi uudelleenarvostaa saldot 1.1.-31.1. välisenä aikana ja käyttää 1. helmikuuta määritettyä vaihtokurssia. 

Valitse mitä päätilejä käytetään: kaikki, tasetili, tulostili. Vain uudelleenarvostettaviksi merkityt päätilit (Päätilit-sivulla) uudelleenarvostetaan. Jos haluat edelleen rajata päätilialuetta, määritä päätilialue tai yksittäiset päätilit **Sisällytettävät tietueet** -välilehdessä. 

Uudelleenarvostusprosessi voidaan suorittaa vähintään yhdelle oikeushenkilölle. Haussa näkyvät vain ne oikeushenkilöt, joihin sinulla on käyttöoikeus. Valitse oikeushenkilöt, joille haluat suorittaa uudelleenarvostusprosessin. 

Uudelleenarvostus voidaan tehdä yhden tai useiden valuuttojen suhteen. Hakuun sisällytetään kaikki valuutat, jotka on kirjattu päivämäärävälillä ja jotka koskevat päätiliä (tase- tai tulostili) ja uudelleenarvostettaviksi valittuja oikeushenkilöitä. Luetteloon sisältyy kirjanpitovaluutta, mutta mitään ei uudelleenarvosteta, jos kirjanpitovaluutta on valittuna. 

Määritä **Esikatsele ennen kirjausta** arvoksi **Kyllä**, jos haluat tarkastella kirjanpidon uudelleenarvostuksen tulosta. Kirjanpidon esikatselu eroaa ostoreskontran ja myyntireskontran ulkomaanvaluutan uudelleenarvostuksen simuloinnista. Ostoreskontran ja myyntireskontran simulointi on raportti, mutta kirjanpidon esikatselu voidaan kirjata suorittamatta uudelleenarvostusprosessia uudelleen. Esikatselun tulokset voidaan viedä Microsoft Exceliin säilyttämään historiatiedot määrien laskemisesta. Et voi käyttää eräkäsittelyä, jos haluat esikatsella uudelleenarvostuksen tuloksia. Esikatselussa käyttäjä voi kirjata kaikkien oikeushenkilöiden tulokset **Kirjaa** -painikkeella. Jos yhden oikeushenkilön tuloksissa on ongelma, käyttäjällä voi kirjata oikeushenkilöiden osajoukon **Valitse kirjattavat yritykset** -painikkeella. 

Kun ulkomaanvaluutan uudelleenarvostusprosessi on valmis, luodaan tietue jolla jäljitetään jokaisen ajon historia.  Kullekin juridiselle henkilölle ja kirjanpitotasolle luodaan erillinen tietue.

## <a name="calculate-unrealized-gainloss"></a>Laske toteutumaton voitto/tappio
Toteutumaton voitto/tappio-tapahtumat luodaan erillään kirjanpidon uudelleenarvostuksesta ja ostoreskontran ja myyntireskontran uudelleenarvostusprosessista. Ostoreskontran ja myyntireskontran edellinen uudelleenarviointi palautetaan kokonaan (olettaen, että tapahtumaa ei ole vielä selvitetty) ja luodaan uusi tapahtuma toteutumattomalle voitolle/tappiolle uuden vaihtokurssin mukaan. Tämä johtuu siitä, että ostoreskontran ja myyntireskontran jokainen yksittäinen tapahtuma uudelleenarvioidaan. Kirjanpidon edellistä uudelleenarviointia ei palauteta. Sen sijaan luodaan tapahtuma päätilin saldon (mukaan lukien kaikki edeltävät uudelleenarvostusmäärät) ja vaihtokurssin perusteella lasketun uuden arvon väliselle erotukselle kurssin päivämääränä. 

**Esimerkki** Päätilille 110110 on olemassa seuraavat saldot.

| Päivämäärä   | Kirjanpitotili| Tapahtuman summa | Kirjanpitosumma |
|------------|--------------------|------------------------|-----------------------|
| 20. tammikuuta | 110110 (käteinen)      | 500 EUR (debet)        | 1000 USD (debet)      |

Päätili uudelleenarvostetaan 31.1.  Toteutumaton voitto/tappio lasketaan seuraavasti.

| Nykyinen saldo tapahtuman valuuttana | Nykyinen saldo kirjanpitovaluuttana | Vaihtokurssi uudelleenarvostuksessa | Uusi summa kirjanpitovaluuttana | Toteutumaton voitto/tappio    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 USD (500 x 1,666667)        | 166,67 tappio (833,33-1000) |

Seuraava kirjanpitomerkintä luodaan.

| Päivämäärä   | Kirjanpitotili       | Veloitus | Luotto |
|------------|--------------------------|-----------|------------|
| 31. tammikuuta | 110110 (käteinen)            |           | 166.67     |
| 31. tammikuuta | 801400 (toteutumaton tappio) | 166.67    |            |

Uusi tapahtumia ei kirjata helmikuulle.  Päätili uudelleenarvostetaan 28.2.

| Nykyinen saldo tapahtuman valuuttana | Nykyinen saldo kirjanpitovaluuttana | Vaihtokurssi uudelleenarvostuksessa | Uusi summa kirjanpitovaluuttana | Toteutumaton voitto/tappio    |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| 500 EUR                                     | 833,33 USD (1000-166.67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416,67 voitto (1250-833,33) |

Seuraava kirjanpitomerkintä luodaan.

| Päivämäärä    | Kirjanpitotili       | Veloitus | Luotto |
|-------------|--------------------------|-----------|------------|
| Helmikuun 28. | 110110 (käteinen)            | 416.67    |            |
| Helmikuun 28. | 801600 (toteutumaton voitto) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Ulkomaanvaluutan uudelleenarvostuksen palautus
Jos uudelleenarvostustapahtuma pitää palauttaa, valitse **Palautustapahtuma** -painike **Ulkomaanvaluutan uudelleenarvostus**-sivulla. Uusi ulkomaanvaluutan uudelleenarvostus -historiatietue luodaan ylläpitämään historian kirjausketjua ulkomaanvaluutan uudelleenarvioinnin ajankohdasta tai palautuksesta. 

Ulkomaanvaluutan uudelleenarvostuksen tuloksia ei tarvitse palauttaa päivämääräjärjestyksessä, mutta tarvittaessa sinun täytyy peruuttaa myös uudempi uudelleenarvostus, jotta voidaan varmistaa että kunkin uudelleenarvostetun päätilin saldot täsmäävät. Peruutukset voidaan tehdä muussa kuin päivämääräjärjestyksessä, koska ei voida määrittää, mitkä päätilit on uudelleenarvostettu ja kuinka usein tämä on tapahtunut. Organisaatio saattaa esimerkiksi määrittää käteisennakoiden päätilien uudelleenarvostuksen tapahtuvaksi neljännesvuosittain mutta kaikkien muiden päätilien uudelleenarvostuksen kerran kuukaudessa.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
