---
title: Yksi tosite useille asiakkaan tai toimittajan tietueille
description: Tämä aihe sisältää yhteenvedon siitä, mitä tapahtuu, kun kirjaat yhden tositteen useille asiakkaan tai toimittajan tietueille. Tämä toiminto poistetaan Microsoft Dynamics 365 for Finance and Operationsin tulevista versioista, minkä vuoksi emme suosittele tämän kirjausmenetelmän käyttöä kirjanpidon vaikutuksen vuoksi tilityskäsittelyyn.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acd0ca65685bc32f4601ad1e38d072f5ab79858d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512381"
---
# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Yksi tosite useille asiakkaan tai toimittajan tietueille

[!include [banner](../includes/banner.md)]

Tämä aihe sisältää yhteenvedon siitä, mitä tapahtuu, kun kirjaat yhden tositteen useille asiakkaan tai toimittajan tietueille. Tämä toiminto poistetaan Microsoft Dynamics 365 for Finance and Operationsin tulevista versioista, minkä vuoksi emme suosittele tämän kirjausmenetelmän käyttöä kirjanpidon vaikutuksen vuoksi tilityskäsittelyyn. 

Tavallisimpia esimerekkejä yhden tositteen käytöstä useita asiakkaita tai toimittajia varten ovat asiakkaiden välisten saldojen siirto ja balansin nettoutus asiakkaiden ja toimittajien välillä samassa organisaatiossa. 

Sama tosite useille asiakkaille tai toimittajille voidaan kirjata jommallakummalla seuraavista tavoista:

-   Käyttämällä kirjauskansiota, jossa on **Vain yksi tositenumero** -kohta valittuna niin, että jokainen kirjauskansioon lisätty rivi sisältyy samaan tositteeseen.
-   Käyttämällä monirivitosittetta, joissa ei ole kirjanpidon vastatiliä, useille asiakkaille tai toimittajille.
-   Tositteen määrittäminen tilille ja vastatilille, joka on toimittaja/toimittaja, asiakas/asiakas, toimittaja/asiakas tai asiakas/toimittaja.

Tässä aiheessa kerrotaan, miten tilitystä käsitellään kirjattaessa yksi tosite jossa on useita asiakkaan tai toimittajan tietueita. Tämä aihe sisältää myös ratkaisuehdotuksia, joiden avulla voit selvittää, kuinka vältetään usean asiakkaan tai toimittajan yhteisen tositteen käyttöä. Erityisesti on esimerkkejä, jotka kuvataan kahta yleistä tilitysskenaariota, joihin usean asiakkaan tai toimittajan yhteisen tositteen käyttö vaikuttaa:

-   Käteisalennuksen laskeminen
-   Uudelleenarvostuksen laskeminen

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Miten tilitys vaikuttaa yhden tositteen käyttöön
Kun kirjaat tositteen, jossa on useita asiakas- tai toimittajatietueita, kun yksi kirjanpidon tosite luodaan, joka sisältää useita ostoreskontran tai myyntireskontran saldoja. Tilitysprosessin aikana alkuperäisiä kirjanpidon kirjauksia käytetään käteisalennuksen, toteutumattomien voittojen ja tappioiden, toteutuneiden voittojen ja tappioidensekä alkuperäisen tiedoston yhteenvetotilin kirjanpitomerkintöjen luomista varten. Esimerkiksi jos käteisalennus tehdään tilitettäessä toimittajamaksua laskulle, käteisalennuksen kirjanpidon täytyy kirjata ostoreskontran kirjanpitotilille alkuperäisestä laskusta. Jos alkuperäinen lasku kirjattiin tositteeseen, joka sisältää useita toimittajatietueita, tehdään alkuperäisen kirjanpidon yhteenveto. Koska tässä tapauksessa ei voida siirtyä jokaisen toimittajatapahtuman yksityiskohtaiseen kirjanpidon kirjaukseen yhdessä tositteessa, ei voida määrittää, kuinka käyttäjä tarkoitetti käteisalennuksen laskettavaksi.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Usean toimittajan yhteinen tosite ja vaikutus käteisalennuksen kirjanpitoon

Seuraavassa esimerkissä useita toimittajalaskuja kirjataan kirjanpidossa yhdelle tositteelle **Kirjauskansio**-sivulla. Nämä laskut jakautuvat useille tilin dimensioille.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Tosite** | **Tilityyppi** | **Tili**  | **Kuvaus** | **Veloitus** | **Hyvitys** |
| GNJL001     | Toimittaja           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Toimittaja           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Toimittaja           | 1001         | INV3            |           | 300,00     |
| GNJL001     | Kirjanpito           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Kirjanpito           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Kirjanpito           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Kirjanpito           | 606300-004-- | INV3            | 300,00    |            |

Kirjauksen jälkeen luodaan yksi tosite.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Tosite** | **Tili**  | **Kirjaustyyppi** | **Summa tapahtuman valuuttana** |
| GNJL001     | 606300-001-- | Kirjanpidon kirjauskansio   | 50,00                              |
| GNJL001     | 606300-002-- | Kirjanpidon kirjauskansio   | 50,00                              |
| GNJL001     | 606300-003-- | Kirjanpidon kirjauskansio   | 200,00                             |
| GNJL001     | 606300-004-- | Kirjanpidon kirjauskansio   | 300,00                             |
| GNJL001     | 200110-001-  | Toimittajan saldo   | -100,00                            |
| GNJL001     | 200110-001-  | Toimittajan saldo   | -200,00                            |
| GNJL001     | 200110-001-  | Toimittajan saldo   | -300,00                            |

Huomaa, että tosite sisältää toimittajasaldon kirjaustapaa varten kolme merkintää yhteen tositteeseen. Esimerkissä ei ole keinoa määrittää, että 50,00 debet tilillä 606300 001 ja 50,00 debet tilillä 606300 002 on tarkoitettu vastakirjaukseksi tilin 200110 001 toimittajasaldon kirjaukselle. Tämä johtuu siitä, että käyttäjä on kirjoittanut useita toimittajatietueita samaan tositteeseen.

Tämän esimerkin avulla voimme analysoida vaikutusta, joka yhden tositteen käytöllä on alempaan tilityksen laskentaan. Oletetaan, että maksat 200,00 laskusta 197,00 ottaen 3,00:n käteisalennuksen. Huomaa, että käteisalennuksen tiliarvo kohdistetaan kaikkiin dimensioihin laskutositteen kulutileistä. Tämä johtuu siitä, että yhtä tositetta käytettiin edellä olevan laskun kirjaamiseen ilman merkintää, miten käyttäjä tarkoitti kulujakaumat vastaamaan toimittajan saldoa yhdessä tositteessa.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Tosite** | **Tili**  | **Kirjaustyyppi**     | **Veloitus** | **Hyvitys** |
| APPAYM001   | 200110-001-  | Toimittajan saldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pankki                 |           | 197.00     |
| 14000056    | 520200-001-- | Toimittajan käteisalennus |           | 0.25       |
| 14000056    | 520200-002-- | Toimittajan käteisalennus |           | 0.25       |
| 14000056    | 520200-003-- | Toimittajan käteisalennus |           | 1,00       |
| 14000056    | 520200-004-- | Toimittajan käteisalennus |           | 1.50       |
| 14000056    | 200110-001-  | Toimittajan saldo       | 3,00      |            |

Jos käyttäjä on tyytymätön käteisalennuksen jakamiseen kulujakaumiin alkuperäisestä laskusta, pitää käyttää useita tositteita laskujen kirjaamiseen yhden tositteen asemesta. Seuraavassa on esimerkki useiden tositteiden kirjaamiseen kirjanpitoon yhden tositteen sijaan, alussa olevan esimerkin mukaisesti.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili**  | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| GNJL001     | Toimittaja           | 1001         | INV1            |           | 100,00     | Kirjanpito          | &lt;tyhjä&gt;      |
| GNJL001     | Kirjanpito           | 606300-001-- | INV1            |   50,00   |            | Kirjanpito          | &lt;tyhjä&gt;      |
| GNJL001     | Kirjanpito           | 606300-002-- | INV1            |   50,00   |            | Kirjanpito          | &lt;tyhjä&gt;      |
| GNJL002     | Toimittaja           | 1001         | INV2            |           | 200,00     | Kirjanpito          | 606300-003--       |
| GNJL003     | Toimittaja           | 1001         | INV3            |           | 300,00     | Kirjanpito          | 606300-004--       |

Kun INV2 on maksettu, tehdään seuraava merkintä. Huomaa, että käteisalennuksen taloushallinnon dimensiot noudattavat liittyvien kulujen taloushallinnon dimensioita.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Tosite** | **Tili**  | **Kirjaustyyppi**     | **Veloitus** | **Hyvitys** |
| APPAYM001   | 200110-001-  | Toimittajan saldo       | 197.00    |            |
| APPAYM001   | 110110-001-  | Pankki                 |           | 197.00     |
| 14000056    | 520200-003-- | Toimittajan käteisalennus |           | 3,00       |
| 14000056    | 200110-001-  | Toimittajan saldo       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Usean toimittajan yhteinen tosite ja vaikutus toteutuneeseen voiton/tappion kirjanpitoon

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Tilityyppi** | **Tili**  |
| GNJL001     | Toimittaja           | 1001        | INV1            |           | 100,00     | Kirjanpito           | 606300-001-- |
| GNJL001     | Toimittaja           | 1001        | INV2            |           | 200,00     | Kirjanpito           | 606300-002-- |

Seuraavassa esimerkissä useita toimittajalaskuja kirjataan kirjanpidossa yhdelle tositteelle **Kirjauskansio**-sivulla. Nämä laskut jakautuvat useille tilin dimensioille. Kirjauksen jälkeen luodaan yksi tosite.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Tosite** | **Tili**  | **Kirjaustyyppi** | **Summa tapahtumavaluuttana (EUR)** | **Summa kirjanpitovaluuttana (USD)** |
| GNJL001     | 606300-001-- | Kirjanpidon kirjauskansio   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Kirjanpidon kirjauskansio   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Toimittajan saldo   | -100,00                                  | -114,00                                 |
| GNJL001     | 200110-001-  | Toimittajan saldo   | -200,00                                  | -228,00                                 |

Huomaa, että tosite sisältää toimittajasaldon kirjaustapaa varten kaksi merkintää yhteen tositteeseen. Ei ole mahdollista määrittää, että 606300-001 tilin debet on tarkoitus vastakirjata 100,00 toimittajasaldotapahtumaksi tiliin 200110- 001. Tämä johtuu siitä, että käyttäjä on kirjoittanut useita toimittajatietueita samaan tositteeseen. 

Tämän esimerkin avulla voimme analysoida vaikutusta, joka yhden tositteen käytöllä on alempaan tilityksen laskentaan. Oletetaan, että kirjanpitovaluutta on USD ja edelliset tapahtumat on kirjattu tapahtumavaluuttana EUR. Oletetaan, että maksat 200,00 EUR laskun kokonaan, mutta ilmenee toteutunut tappio oman laskun kirjaamisen ja maksun välisen vaihtokurssin eron vuoksi. Huomaa, että toteutuneen tappion tiliarvo kohdistetaan kaikkiin dimensioihin laskutositteen kulutileistä. Tässä tapauksessa sekä dimension 001 ja 002 on kohdistettu, vaikka käyttäjästä voi vaikuttaa, että ainoastaan 002 kuuluu kulutiliin maksettavalta laskulta. Tämä johtuu siitä, että yhtä tositetta käytettiin edellä olevan laskun kirjaamiseen ilman merkintätapaa, miten käyttäjä tarkoitti kulujakaumat vastaamaan toimittajan saldoa yhdessä tositteessa.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Tosite** | **Tili** | **Kirjaustyyppi**   | **Summa tapahtumavaluuttana (EUR)** | **Summa kirjanpitovaluuttana (USD)** |
| APPAYM001   | 200110-001- | Toimittajan saldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pankki               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-001- | Vaihtokurssitappio | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Vaihtokurssitappio | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Toimittajan saldo     |                                          | -2,00                                   |

Jos käyttäjä on tyytymätön vaihtokurssin tappion jakamiseen kulujakaumiin alkuperäisestä laskusta, pitää käyttää useita tositteita laskujen kirjaamiseen yhden tositteen asemesta. Seuraavassa on esimerkki useiden tositteiden kirjaamiseen kirjanpitoon yhden tositteen sijaan, alussa olevan esimerkin mukaisesti.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| GNJL002     | Toimittaja           | 1001        | INV1            |           | 100,00     | Kirjanpito          | 606300-001--       |
| GNJL003     | Toimittaja           | 1001        | INV2            |           | 200,00     | Kirjanpito          | 606300-002--       |

Kun INV2 on maksettu, tehdään seuraava merkintä. Huomaa, että vaihtokurssitappion taloushallinnon dimensiot noudattavat liittyvien kulujen taloushallinnon dimensioita.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Tosite** | **Tili** | **Kirjaustyyppi**   | **Summa tapahtumavaluuttana (EUR)** | **Summa kirjanpitovaluuttana (USD)** |
| APPAYM001   | 200110-001- | Toimittajan saldo     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Pankki               | -200,00                                  | -230,00                                 |
| 14000056    | 801300-002- | Vaihtokurssitappio | 0,00                                     | 2,00                                    |
| 14000056    | 200110-001- | Toimittajan saldo     |                                          | -2,00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Yksi tosite saldon siirroille ja nettoutusskenaarioille
Kaksi yleisesti käytettyjä skenaarioita, jotka käyttävät yhtä tositetta, joka sisältää useita asiakas- tai toimittajasaldosiirtoja yhdeltä asiakkaalta/toimittajalta toiselle asiakkaalle/toimittajalle, ja saman organisaation asiakkaan ja toimittajan nettouttaminen. Seuraavissa kahdessa esimerkissä kuvataan suositeltua tapaa syöttämällä nämä skenaariot Finance and Operations -järjestelmään vaihtoehtona niiden kirjoittamiselle yhteen tositteeseen. 

*Saldon siirto* on yksi tosite jossa on useita asiakkaita, joka kirjoitetaan saldon siirtoa varten asiakkaalta asiakkaalle (sama toimittajille). Tämä skenaario voi ilmetä, kun vastuu laskun maksamisesta siirtyy toiselle osapuolelle, kuten tytäryhtiön siirtämä vastuu emoyhtiölle. 

Tässä esimerkissä oletetaan myynti, jossa asiakas on oikeutettu käteisalennukseen, jos maksu tehdään 10 päivän kuluessa. Tässä esimerkissä asiakas käyttää vakuutusyhtiötä, joka vastaa laskun maksamisesta. Vakuutusyhtiö on määritetty toiseksi asiakkaaksi järjestelmässä. Alkuperäisen asiakkaan saldo siirretään vakuutusyhtiölle, joka maksaa laskun, ottamalla 2 % käteisalennuksen alennuskauden aikana. 

Esimerkin vuoksi oletetaan, että seuraava myynti on tehty asiakkaan ACMEsta. Seuraavat kirjanpitokirjaukset edustavat myyntiä.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Kirjanpitotili** | **Kirjaustyyppi** | **Veloitus** | **Hyvitys** |
| 401100-002-023-    | Myyntituotto          |           | 100        |
| 130100-002-        | Asiakkaan saldo | 100       |            |

Seuraavaksi käyttäjä siirtää ACME:sta maksamattoman saldon vakuutusyhtiölle yhdessä myyntireskontran maksukirjauskansion tositteessa. Finance and Operations -järjestelmässä vakuutusyhtiö määritetään Vakuutus-asiakkaaksi.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| ARPAYM001   | Asiakas         | ACME        | Tapahtumien siirto        |           | 100,00     | Asiakas        | Vakuutus          |

Huomaa, että edellinne tapahtuma sisältyy yhteen tositteeseen. Tämä tosite sisältää kaksi asiakastietueita. Seuraava tosite luodaan, kun edellä oleva kirjanpidon tapahtuma kirjataan.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Tosite** | **Tili** | **Kirjaustyyppi** | **Summa tapahtuman valuuttana** |
| ARPAYM001   | 130100-002- | Asiakkaan saldo | 100,00                             |
| ARPAYM001   | 130100-002- | Asiakkaan saldo | -100,00                            |

Seuraavaksi oletetaan, että saat vakuutus-asiakkaalta maksun 98,00 ja päätät tilittää maksun laskulla, joka on luotu saldosiirrolla. Tämä aiheuttaa seuraavan tositteen kirjaamisen. Odotuksena voi olla, että tilitys käyttää kirjanpitodimensioita alkuperäisestä laskusta, mutta se ei ole mahdollista, koska vakuutus-asiakkaalle ei ole laskuasiakirjaa. Huomaa, että oletusarvoisesti käteisalennuksen jakeludimensio on peräisin siirrosta luodusta asiakassiirrosta, ei alkuperäisen laskun tuottotilistä. Oletusarvoisesti tämä on tulosta yhden tositteen käyttämisestä saldojen siirtoon.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Tosite** | **Tili** | **Kirjaustyyppi** | **Veloitus** | **Hyvitys** |
| ARPAYM002   | 110110-002- | Pankki             | 98.00     |            |
| ARPAYM002   | 130100-002- | Asiakkaan saldo |           | 98.00      |

Käteisalennukseen liittyvässä tositteessa taloushallinnon dimension oletusarvo tulee siirrosta luodusta asiakastapahtumasta, koska siirrolla on useampia kuin yksi asiakas.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Tosite** | **Tili** | **Kirjaustyyppi**       | **Veloitus** | **Hyvitys** |
| ARP-00001   | 403300-002- | Asiakkaan käteisalennus | 2,00      |            |
| ARP-00001   | 130100-002- | Asiakkaan saldo       |           | 2,00       |

Jos käyttäjä on tyytymätön käteisalennuksen taloushallinnon dimension oletusarvoon, yhden tositteen sijaan pitää saldon siirron kirjaamiseen käyttää useita tositteita. Tämä skenaario tulee suorittaa luomalla hyvityslasku asiakkaalle, JOLTA saldo on siirretty, ja veloituslasku tai lasku asiakkaalle, JOLLE saldo siirretään. Seuraavassa esimerkissä esitetään miten useat tositteet voidaan kirjoittaa myyntireskontran maksukirjauskansioon saldon siirtämiseksi sen sijaan, että käytetään yhtä tositetta tämän esimerkin mukaisesti.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| ARPAYM001   | Asiakas         | ACME        |                 |           | 100,00     | Kirjanpito          | 401100-002-023-    |
| ARPAYM002   | Asiakas         | Vakuutus   |                 | 100,00    |            | Kirjanpito          | 401100-002-023-    |

Tämä tarkoittaa sitä, että kun vakuutus-asiakas maksaa tositteella ARPAYM02 98,00, tositteen ARPAYM002 kirjanpidon tiliviennin oikeita taloushallinnon dimensioita käytetään.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Tosite** | **Tili** | **Kirjaustyyppi** | **Veloitus** | **Hyvitys** |
| ARPAYM003   | 110110-002- | Pankki             | 98.00     |            |
| ARPAYM003   | 130100-002  | Asiakkaan saldo |           | 98.00      |

Käteisalennukseen liittyvän tositteen taloushallinnon dimensioita käytetään vastakirjauksen tuottotililtä, joka näkyy ARPAYM002-tilin tositteessa.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Tosite** | **Tili**     | **Kirjaustyyppi**       | **Veloitus** | **Hyvitys** |
| ARP-00001   | 403300-002-023- | Asiakkaan käteisalennus | 2,00      |            |
| ARP-00001   | 130100-002-     | Asiakkaan saldo       |           | 2,00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Yksi tosite ja nettoutus useille asiakkaille ja toimittajielle
Nettoutus voi olla hyödyllinen, kun organisaatio ostaa tai myy samalle yritykselle. Sen sijaan, että toimittajan laskuja maksetaan ja odotetaan myyntilaskujen maksua, toimittajan laskut ja myyntilaskut nettoutetaan. Nettoutustapahtuma täsmäytetään avoimia saldoja vastaan. 

Oletetaan esimerkiksi, että toimittaja 1001 ja asiakas US-008 ovat sama yksikkö, joten organisaatiosi haluaa nettouttaa osto- ja myyntisaldot ennen maksua / jäljellä olevan saldon vastaanottoa. Oletetaan, että asiakastietue on velkaa 75,00 EUR ja toimittajatietue on velkaa 100,00 EUR, mikä tarkoittaa sitä, että haluat nettouttaa saldot ja maksaa toimittajalle vain 25,00 EUR. Lisäksi oletetaan että kirjanpitovaluutta on USD. Tässä tapauksessa nettoutustapahtuma kirjataan yhtenä tositteena tilin ostoreskontran maksukirjauskansioon.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| APPAYM001   | Toimittaja           | 1001        | Nettoutus         |  75,00    |            | Asiakas        | US-008             |

Ei-toivottujen ongelmien välttämiseksi tämän tapahtuman tulevissa kirjauksissa yhden tositteen käytön sijaan pitää merkitä useita tositteita kirjauskansioon nettoutustapahtuman tallentamiseksi. Huomaa, että asiakkaan ja toimittajan saldot vastakirjataan yhdelle selvitystilille, jotta vältetään yhden tositteen käyttö, joka sisältää useita asiakkaan ja toimittajan saldoja.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Tosite** | **Tilityyppi** | **Tili** | **Kuvaus** | **Veloitus** | **Hyvitys** | **Vastatilin tyyppi** | **Vastatili** |
| 001         | Asiakas         | US-008      |                 |           |  75,00     | Kirjanpito          | 999999---          |
| 002         | Toimittaja           | 1001        |                 |  75,00    |            | Kirjanpito          | 999999---          |





