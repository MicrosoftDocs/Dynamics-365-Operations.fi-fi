---
title: Kaksoisraportointi
description: Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 406fbb53fc4cd17a7c257b5f5463227118c9051f44d81db000fbe87dca142efe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767053"
---
# <a name="dual-reporting"></a>Kaksoisraportointi

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää esimerkin sekä International Financial Reporting Standard (IFRS) -raportoinnin että resurssin vuokrauksen lakisääteisen raportoinnin vaatimusten täyttämisestä. Vaatimuksena on Microsoft Dynamics 365 Financen kirjanpitotasojen käyttökokemus. Sen avulla esimerkki on helpompi ymmärtää.

## <a name="example"></a>Esimerkki

Seuraavassa esimerkissä otetaan huomioon vuokraus Italian lakisääteisessä raportoinnissa käyttämällä sekä käteisvaroihin perustuvaa menetelmää että IFRS-raportointimenetelmiä. Yrityksen on muodostettava kolme kirjaa, joiden avulla sekä Italian lakisääteiset vaatimukset että IFRS 16 -vaatimukset otetaan huomioon. Yksi kirja vaaditaan IFRS 16:lle, toinen lakisääteisille vaatimuksille ja kolmas lakisääteisten kirjausten automaattista käänteistä kirjausta varten. Kirjat määritetään seuraavissa taulukoissa esitetyllä tavalla.

**IFRS 16 -kirja**

IFRS 16 -kirja määritetään niin, että se on yhdenmukainen IFRS 16 -kirjanpitostandardin kanssa. Kaikki tähän kirjaan kirjatut tapahtumat kirjataan mukautettuun tasoon.

| Nimi                                    | kuvaus    |
|-----------------------------------------|----------------|
| Kirjan tyyppi                               | IFRS 16        |
| Kirjan kuvaus                        | IFRS 16        |
| Kirjanpitotaso                           | Mukautettu kerros 1 |
| Vuokran tyyppi                              | Finance        |
| Kirjanpitokehys                    | IFRS 16        |
| Vuokra-/käyttöajan määrittäminen         | 0,00           |
| Nykyinen arvo / resurssin käyvän arvon määrittäminen | 0,00           |
| Lyhytaikainen kynnysarvo                    | 12             |
| Arvoltaan vähäinen kynnysarvo                     | 5,000.00       |
| Maksu toimittajalle                           | Nro             |

**Lakisääteinen kirja**

Lakisääteinen kirja on käteisvaroihin perustuva kirja, jonne yritys kirjaa vuokrauksen kulut käteisvarojen summana, joka maksetaan joka kuukausi vuokrana. Tämä kirja ei tuota käyttöoikeusomaisuuserää tai vuokrasopimusvelkaa.

| Nimi                                    | kuvaus |
|-----------------------------------------|-------------|
| Kirjan tyyppi                               | Lakisääteinen   |
| Kirjan kuvaus                        | Paikallinen GAAP  |
| Kirjanpitotaso                           | Valittu     |
| Vuokran tyyppi                              | Automaattinen   |
| Kirjanpitokehys                    | Maksuperuste  |
| Vuokra-/käyttöajan määrittäminen         | 0,00        |
| Nykyinen arvo / resurssin käyvän arvon määrittäminen | 0,00        |
| Lyhytaikainen kynnysarvo                    | 0           |
| Arvoltaan vähäinen kynnysarvo                     | 0           |
| Maksu toimittajalle                           | Nro          |

**Lakisääteinen palautuskirja**

Lakisääteinen palautuskirja määritetään samalla tavalla kuin lakisääteinen kirja.

| Nimi                                    | kuvaus                    |
|-----------------------------------------|--------------------------------|
| Kirjan tyyppi                               | Lakisääteinen – palautus           |
| Kirjan kuvaus                        | Kirjaa käänteiseen lakisääteiseen kirjaan |
| Kirjanpitotaso                           | Mukautettu kerros 1                 |
| Vuokran tyyppi                              | Automaattinen                      |
| Kirjanpitokehys                    | Maksuperuste                     |
| Vuokra-/käyttöajan määrittäminen         | 0,00                           |
| Nykyinen arvo / resurssin käyvän arvon määrittäminen | 0,00                           |
| Lyhytaikainen kynnysarvo                    | 0                              |
| Arvoltaan vähäinen kynnysarvo                     | 0                              |
| Maksu toimittajalle                           | Nro                             |

Tässä esimerkissä on luotu vuokraus, jolla on seuraavat asetukset **Yleistä**- ja **Maksuaikataulurivit**-välilehdissä.

**Yleinen-välilehti**

| Kenttä                      | Arvo            |
|----------------------------|------------------|
| Inkrementaalinen lainakorko | 5 %               |
| Aloituspäivämäärä          | 1.1.2020         |
| Vuokraryhmä                | Rakennukset        |
| Toimittaja                     | 1001             |
| Resurssin käypä arvo    | 245,000          |
| Käyttöomaisuuden käyttöikä          | 120              |
| Annuiteetin tyyppi               | Tavallinen annuiteetti |
| Yhdistämisväli       | Kuukausittain          |

**Maksusuunnitelmarivit-välilehti**

| Kenttä             | Arvo      |
|-------------------|------------|
| Aloituspäivä        | 1.1.2020   |
| Kausiväli   | Kuukautta     |
| Kaudet           | 24         |
| Päättymispäivämäärä          | 31.12.2020 |
| Maksun toistuvuus | Kuukausittain    |
| Maksun summa    | 1 000      |

Jotta tämä vuokraus voidaan ottaa huomioon kahdessa kehyksessä, käytetään sekä nykyistä että mukautettua kirjaustasoa. Seuraavassa taulukossa on esimerkki jokaisesta kirjauskansiomerkinnästä, joka vaaditaan vastaamaan tasapuolisesti kunkin raportointistandardin mukaisia taloustietoja. Kunkin vuokrauksen ensimmäisen kuukauden kirjauskansiomerkinnän yksityiskohtainen kuvaus annetaan jälkikäteen.

<table>
<thead>
<tr>
<th rowspan='3'>Tilinumero</th>
<th rowspan='3'>kuvaus</th>
<th colspan='3'>Lakisääteinen kirja (nykyinen taso)</th>
<th rowspan='3'>Nykyinen taso yhteensä</th>
<th>Palautuskirja (mukautettu taso)</th>
<th colspan='4'>IFRS 16 -kirja (mukautettu taso)</th>
<th rowspan='3'>Nykyinen taso + mukautettu taso yhteensä</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
<th>JE-130</th>
<th>JE-140</th>
<th>JE-150</th>
<th>JE-160</th>
<th>JE-170</th>
</tr>
<tr>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Vuokran kulu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
<td>-1 000,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>2</td>
<td>Pankkikulu</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>ALV-kulu</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Selvitystili</td>
<td>-1 000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
<td>1,000.00</td>
<td></td>
<td>-1 000,00</td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Ostoreskontra</td>
<td></td>
<td>-1 008,00</td>
<td>1,008.00</td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Käyttöoikeusomaisuuserä</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>22,794.00</td>
<td></td>
<td></td>
<td></td>
<td>22,793.90</td>
</tr>
<tr>
<td>7</td>
<td>Rahoitusleasingsopimuksen velvoite</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td>-22 794,00</td>
<td>1,000.00</td>
<td>-94,97</td>
<td></td>
<td>-21 888,87</td>
</tr>
<tr>
<td>8</td>
<td>Korkokustannus</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td>94.97</td>
<td></td>
<td>94.97</td>
</tr>
<tr>
<td>9</td>
<td>Maksu</td>
<td></td>
<td></td>
<td>-1 008,00</td>
<td>-1 008,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Poistokulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>949.75</td>
<td>949.75</td>
</tr>
<tr>
<td>11</td>
<td>Kertynyt poisto</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td>-949,75</td>
<td>-949,75</td>
</tr>
</tbody>
</table>

Kuten edellä olevasta taulukosta ilmenee, sekä lakisääteinen raportointi että IFRS-raportointi edellyttävät kolmen kirjan käyttämistä.

- Lakisääteinen kirja tallentaa vuokrat nykyisen tason käteisvaroihin perustuvan kirjanpidon sääntöjen mukaisesti.
- Lakisääteinen palautuskirja kumoaa lakisääteiset kirjauskansiomerkinnät.
- IFRS 16 -kirja luo IFRS 16:n pakolliset kirjauskansiomerkinnät.

Sinun on syötettävä vuokraus vain kerran. Tämän jälkeen voit avata **Kirjat**-sivun, ja näet kaikki vuokraukseen liittyvät kirjat.

> [!NOTE]
> Kun luot kirjoja, kaikkien kolmen on liityttävä samaan vuokraustietueeseen.

Ensimmäinen kirjauskansiomerkintä tallentaa vuokrauksen lakisääteiseen kirjaan. Voit luoda maksut eränä tai valitsemalla maksusuunnitelman lakisääteisestä kirjasta.

Tässä esimerkissä maksusuunnitelmasta luodaan seuraava kirjauskansiomerkintä lakisääteistä kirjaa varten.

### <a name="lease-payment--1312020--je-100"></a>Vuokra – 31.1.2020 – JE 100

| Tilityyppi | Tilinumero | Taso   | Tilin kuvaus | Veloitus    | Luotto   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 1              | Valittu | Vuokran kulu       | 1,000.00 |          |
| Ledger       | 4              | Valittu | Selvitystili    |          | 1,000.00 |

Ostoreskontran käsittelijä käyttää Dynamics 365:n vakiotoimintoa luodessaan resurssin vuokrauksen ulkopuoliselle vuokraukselle laskun maksamista varten. Sen sijaan, että debettiliksi valittaisiin **Vuokran kulu** ostoreskontran käsittelijä valitsee selvitystilin seuraavan merkinnän luomiseksi.

### <a name="ap-process--1312020--je-110"></a>Ostoreskontran prosessi – 31.1.2020 – JE 110

| Tilityyppi | Tilinumero | Taso   | Tilin kuvaus | Veloitus    | Luotto   |
|--------------|----------------|---------|---------------------|----------|----------|
| Ledger       | 4              | Valittu | Selvitystili    | 1,000.00 |          |
| Ledger       | 2              | Valittu | Pankkikulu            | 3.00     |          |
| Ledger       | 3              | Valittu | ALV-kulu         | 5.00     |          |
| Toimittaja       | 5              | Valittu | Ostoreskontra    |          | 1,008.00 |

Kun toimittajalle annetaan ilmoitus, seuraat säännöllistä maksuprosessia. Tämän prosessin aikana luodaan seuraava kirjauskansiomerkintä.

### <a name="cash-payment--1312020--je-120"></a>Käteismaksu – 31.1.2020 – JE 120

| Tilityyppi | Tilinumero | Taso   | Tilin kuvaus | Veloitus    | Luotto   |
|--------------|----------------|---------|---------------------|----------|----------|
| Toimittaja       | 5              | Valittu | Ostoreskontra    | 1,008.00 |          |
| Pankki         | 9              | Valittu | Maksu                |          | 1,008.00 |

Nyt tämä vuokraus on otettu kokonaan huomioon lakisääteisen raportoinnin vaatimusten mukaisesti, ja voit luoda pääkirjan nykyisen tason mukaan. Järjestelmä palauttaa pääkirjan, jossa ovat seuraavat luvut.

<table>
<thead>
<tr>
<th rowspan='3'>Tilinumero</th>
<th rowspan='3'>kuvaus</th>
<th colspan='3'>Lakisääteinen kirja (nykyinen taso)</th>
<th rowspan='3'>Nykyinen taso yhteensä</th>
</tr>
<tr>
<th>JE-100</th>
<th>JE-110</th>
<th>JE-120</th>
</tr>
<tr>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
<th>Debet (kredit)</th>
</tr>
</thead>
<tbody>
<tr>
<td>1</td>
<td>Vuokran kulu</td>
<td>1,000.00</td>
<td></td>
<td></td>
<td>1,000.00</td>
</tr>
<tr>
<td>2</td>
<td>Pankkikulu</td>
<td></td>
<td>3.00</td>
<td></td>
<td>3.00</td>
</tr>
<tr>
<td>3</td>
<td>ALV-kulu</td>
<td></td>
<td>5.00</td>
<td></td>
<td>5.00</td>
</tr>
<tr>
<td>4</td>
<td>Selvitystili</td>
<td>-1 000,00</td>
<td>1,000.00</td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>5</td>
<td>Ostoreskontra</td>
<td></td>
<td>-1 008,00</td>
<td>1,008.00</td>
<td>0,00</td>
</tr>
<tr>
<td>6</td>
<td>Käyttöoikeusomaisuuserä</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>7</td>
<td>Rahoitusleasingsopimuksen velvoite</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>8</td>
<td>Korkokustannus</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>9</td>
<td>Maksu</td>
<td></td>
<td></td>
<td>-1 008,00</td>
<td>-1 008,00</td>
</tr>
<tr>
<td>10</td>
<td>Poistokulu</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
<tr>
<td>11</td>
<td>Kertynyt poisto</td>
<td></td>
<td></td>
<td></td>
<td>0,00</td>
</tr>
</tbody>
</table>

Jos haluat käyttää IFRS 16 -lukuja ja suorittaa saman pääkirjan, lakisääteisen kirjapidon kirjauskansioviennit on palautettava ja IFRS 16 -kirjauskansioviennit kirjattava. Tässä esimerkissä on myös lakisääteinen palautuskirja siltä varalta, että haluat palauttaa lakisääteiset kirjauskansioviennit. Palautuskirjassa on samat asetukset kuin lakisääteisessä kirjassa, mutta vastakkainen kirjausprofiili. Esimerkiksi lakisääteinen kirja *veloitti* vuokrauksen kulutilin, mutta palautuskirja *hyvittää* tämän tilin. Nämä suhteet on helppo määrittää resurssin vuokrauksen kirjaustileillä **Resurssin vuokrauksen parametrit** -sivulla (**Resurssin vuokraus \> Asetukset \> Resurssin vuokrauksen parametrit**).

Kun lakisääteisessä kirjassa käytettyä prosessia käytetään palautuskirjassa, luodaan seuraava kirjauskansiovienti. Erona on se, että palautuskirja kirjaa vastakirjaukset lakisääteisestä kirjasta. Vastakirjaukset tehdään myös mukautetussa tasossa. Kun pääkirja suoritetaan nykyisellä tasolla, palautuskirjauskansiovientejä ei sisällytetä.

### <a name="lease-payment--1312020--je-130"></a>Vuokra – 31.1.2020 – JE 130

| Tilityyppi | Tilinumero | Taso  | Tilin kuvaus | Veloitus    | Luotto   |
|--------------|----------------|--------|---------------------|----------|----------|
| Ledger       | 4              | Mukautettu | Selvitystili    | 1,000.00 |          |
| Ledger       | 1              | Mukautettu | Vuokran kulu       |          | 1,000.00 |

Nyt lakisääteiset kirjauskansioviennit on eliminoitu, ja voit kirjata kaikki IFRS 16:n edellyttämät kirjauskansioviennit IFRS 16 -kirjaan. Nämä viennit sisältävät käyttöoikeusomaisuuserän ja velan alkuperäisen kirjauksen sekä koron ja poiston tietueen.

### <a name="initial-recognition--112020--je-140"></a>Alkuperäinen kirjaus – 1.1.2020 – JE 140

| Tilityyppi | Tilinumero | Taso  | Tilin kuvaus      | Veloitus     | Luotto    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| Ledger       | 6              | Mukautettu | Käyttöoikeusomaisuuserä                | 22,793.90 |           |
| Ledger       | 7              | Mukautettu | Rahoitusleasingsopimuksen velvoite |           | 22,793.90 |

Vuokra kirjataan kuten muut vuokrat. Selvitystiliä käytetään, jotta voidaan varmistaa käteisen hyvitys vain kerran.

### <a name="lease-payment--1312020--je-150"></a>Vuokra – 31.1.2020 – JE 150

| Tilityyppi | Tilinumero | Taso  | Tilin kuvaus      | Veloitus    | Luotto   |
|--------------|----------------|--------|--------------------------|----------|----------|
| Ledger       | 7              | Mukautettu | Rahoitusleasingsopimuksen velvoite | 1,000.00 |          |
| Ledger       | 4              | Mukautettu | Selvitystili         |          | 1,000.00 |

Korkokulun kirjauskansiovienti luodaan velan kuoletusaikataulusta.

### <a name="interest-expense--1312020--je-160"></a>Korkokustannus – 31.1.2020 – JE 160

| Tilityyppi | Tilinumero | Taso  | Tilin kuvaus      | Veloitus | Luotto |
|--------------|----------------|--------|--------------------------|-------|--------|
| Ledger       | 8              | Mukautettu | Korkokustannus         | 94.97 |        |
| Ledger       | 7              | Mukautettu | Rahoitusleasingsopimuksen velvoite |       | 94.97  |

Poistokulun kirjauskansiovienti luodaan resurssin poistoaikataulusta.

### <a name="depreciation-expense--1312020--je-170"></a>Poistokulu – 31.1.2020 – JE 170

| Tilityyppi | Tilinumero | Taso  | Tilin kuvaus      | Veloitus  | Luotto |
|--------------|----------------|--------|--------------------------|--------|--------|
| Ledger       | 10             | Mukautettu | Poistokulu     | 949.75 |        |
| Ledger       | 11             | Mukautettu | Kertynyt poisto |        | 949.75 |

Kun kaikki nämä kirjauskansioviennit on luotu ja kirjattu, näkyvissä ovat seuraavat mukautetun tason 1 arvot. Huomaa, että viimeinen sarake sisältää pankkikulun, ALV-kulun ja käteisvähennyksen edelliseltä tasolta, mutta ei lakisääteisen raportoinnin kirjauskansiovientejä. Näin saavutetaan todelliset kaksoisraportoinnin ominaisuudet. Tässä vaiheessa yritys on juuri suorittanut pääkirjan ja yhdistää nykyisen tason mukautettuun tasoon IFRS-pääkirjan luomista varten.

| Tilinumero | kuvaus              | Lakisääteinen kirja\-Nykyinen taso\-JE\-100\-Debet \(Kredit\) | Lakisääteinen kirja\-Nykyinen taso\-JE\-110\-Debet \(Kredit\) | Lakisääteinen kirja\-Nykyinen taso\-JE\-120\-Debet \(Kredit\) | Nykyinen taso \- Kokonaissummat | - | Palautuskirja\-Mukautettu taso\-JE\-130\-Debet \(Kredit\) | IFRS 16 -kirja\-Mukautettu taso\-JE\-140\-Debet \(Kredit\) | IFRS 16 -kirja\-Mukautettu taso\-JE\-150\-Debet \(Kredit\) | IFRS 16 -kirja\-Mukautettu taso\-JE\-160\-Debet \(Kredit\) | IFRS 16 -kirja\-Mukautettu taso\-JE\-170\-Debet \(Kredit\) | Mukautettu taso \+ Nykyinen taso \- Kokonaissummat |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| 1          | Vuokran kulu            | 1,000\.00                                         |                                                   |                                                   | 1,000\.00               |   | \-1 000                                         |                                                |                                                |                                                |                                                | 0\.00                                   |
| 2          | Pankkikulu                 |                                                   | 3\.00                                             |                                                   | 3\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 3\.00                                   |
| 3          | ALV-kulu              |                                                   | 5\.00                                             |                                                   | 5\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 5\.00                                   |
| 4          | Selvitystili         | \-1 000\.00                                       | 1,000\.00                                         |                                                   | 0\.00                   |   | 1 000                                           |                                                | \-1 000                                        |                                                |                                                | 0\.00                                   |
| 5          | Ostoreskontra         |                                                   | \-1 008\.00                                       | 1,008\.00                                         | 0\.00                   |   |                                                 |                                                |                                                |                                                |                                                | 0\.00                                   |
| 6          | Käyttöoikeusomaisuuserä                |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | 22,794                                         |                                                |                                                |                                                | 22,793\.90                              |
| 7          | Rahoitusleasingsopimuksen velvoite |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 | \-22 794                                       | 1 000                                          | \-94\.97                                       |                                                | \-21,888\.87                            |
| 8          | Korkokustannus         |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                | 94\.97                                         |                                                | 94\.97                                  |
| 9          | Maksu                     |                                                   |                                                   | \-1 008\.00                                       | \-1 008\.00             |   |                                                 |                                                |                                                |                                                |                                                | \-1 008\.00                             |
| 10         | Poistokulu     |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | 949\.75                                        | 949\.75                                 |
| 11         | Kertynyt poisto |                                                   |                                                   |                                                   | 0\.00                   |   |                                                 |                                                |                                                |                                                | \-949\.75                                      | \-949\.75                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
