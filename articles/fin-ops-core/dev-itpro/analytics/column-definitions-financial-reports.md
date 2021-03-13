---
title: Talousraporttien sarakemääritykset
description: Tässä artikkelissa on tietoja sarakemäärityksistä. Sarakkeen määritys on raporttiosa, joka määrittää talousraportin kunkin sarakkeen sisällön.
author: ShylaThompson
manager: AnnBe
ms.date: 10/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 106601
ms.assetid: 66e72a48-edab-4e9d-815f-596a1623c258
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 820604fac96f5c86be3f7206ca88b3eb1fc6c32a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093106"
---
# <a name="column-definitions-in-financial-reports"></a>Talousraporttien sarakemääritykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja sarakemäärityksistä. Sarakkeen määritys on raporttiosa tai rakenneosa, joka määrittää talousraportin kunkin sarakkeen sisällön. Kuten rivimäärityksiäkin, sarakkeiden perusmäärityksiä voi käyttää useilla raporteilla.

## <a name="create-and-modify-a-column-definition"></a>Sarakkeen määrityksen luominen ja muokkaaminen

Sarakkeen määritys voi sisältää 2–255 saraketta.

### <a name="create-a-column-definition"></a>Sarakkeen määrityksen luominen

1. Valitse Report Designer -ohjelman siirtymisruudussa **Sarakkeiden määritykset**.
2. Valitse **Tiedosto**-valikossa **Uusi** ja valitse sitten **Sarakkeen määritys**.
3. Lisää sarakkeen määrityksen sisältö.

### <a name="open-a-column-definition"></a>Sarakkeen määrityksen avaaminen

1. Valitse Report Designer -ohjelman siirtymisruudussa **Sarakkeiden määritykset**.
2. Avaa sarakkeen määritys kaksoisnapsauttamalla sitä.

### <a name="add-a-column-to-a-column-definition"></a>Sarakkeen lisääminen sarakemääritykseen

1. Valitse Report Designerissa **Sarakkeiden määritykset** ja avaa muokattava sarakkeen määritys.
2. Valitse sarake, johon uusi sarake lisätään.
3. Valitse **Muokkaa**-valikossa **Lisää sarake**. Uusi sarake näkyy valitsemasi sarakkeen vasemmalla puolella.

### <a name="delete-a-column-from-a-column-definition"></a>Sarakkeen poistaminen sarakemäärityksestä

1. Valitse raporttien suunnitteluohjelmassa **Sarakemääritykset** ja avaa sen jälkeen muokattava sarakemääritys.
2. Valitse poistettava sarake.
3. Valitse **Muokkaa**-valikosta **Poista sarake**.

## <a name="contents-of-a-column-definition"></a>Sarakemäärityksen sisältö
Sarakkeen määritys sisältää seuraavat tiedot:

- Kuvausten sarake rivin määrityksessä
- Summasarakkeet, joissa on taloushallinnon tiedot, tai laskutoimitukset, jotka perustuvat sarakkeen määrityksen muihin tietoihin
- Sarakkeiden muotoilu
- Määritesarakkeet

Nämä tiedot näkyvät seuraavilla sarakkeen määrityksen alueilla:

- Sarakkeen määrityksen otsikon alue sisältää otsikon tekstin ja raportin muotoilun. Otsikko voi koskea yhtä tai useaa tietosaraketta, tai se voi koskea sarakkeita ehdollisesti. Sarakemääritys voi sisältää niin monta sarakeotsikkoriviä kuin on tarpeen.

    > [!NOTE]
    > Sarakeotsikot koskevat raportin tietojen jokaista saraketta. Raporttiotsikot koskevat koko raporttia. Voit määrittää raportin otsikot raportin määrityksen **Ylä- ja alatunnisteet** -välilehdessä.

- Sarakkeiden tietorivit sijaitsevat sarakkeen määrityksen otsikoiden rivien alla. Sarakkeiden tietorivit määrittävät raportin tiedot. Seuraavassa taulukossa luetellaan sarakkeiden tietorivit.

    | Sarakkeen tietorivin nimi                                                | Kuvaus                                                                                            |
    |-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
    | Sarakelaji                                                           | (Pakollinen) Määritä sarakkeen tietojen tyyppi.                                                     |
    | Kirjakoodi/määriteluokka                                          | Määritä **FD**- ja **ATTR**-tyypin sarakkeiden taloushallinnon tiedot.                       |
    | Tilikausi, Katetut jaksot                                    | Määritä **FD**-tyypin sarakkeiden taloushallinnon tiedot.                                     |
    | Resepti                                                               | Määritä **CALC**-tyypin sarakkeiden laskentakaava.                                        |
    | Sarakkeen leveys, Lisävälilyönnit ennen saraketta, Muotoilun ohitus, Tulostuksen hallinta | Määritä erikoismuotoiluasetukset.                                                                        |
    | Sarakkeen rajoitukset                                                   | Rajoita tietoja.                                                                                         |
    | Raportoinnin yksikkö                                                        | Rajoita saraketta niin, että sarakkeessa näkyvät vain tietyn raportoinnin yksikön tiedot.                      |
    | Valuutan näyttö, Valuuttasuodatin                                      | Muotoile valuuttaa.                                                                                       |
    | Dimensiosuodatin                                                      | Määritä tietojen rajoituksessa käytettävä suodatin tietyille taloushallinnon tietojen raportoinnin yksiköille.                           |
    | Määritesuodatin                                                      | Määritä taloushallinnon tietojen rajoituksessa käytettävä suodatin.                                                       |
    | Alkamispäivämäärä, Päättymispäivämäärä                                                   | Rajoita taloushallinnon tiedot tietyille päivämäärille.                                                         |
    | Perustelu                                                         | Tasaa rivin määrityksessä määritetty kuvausteksti vasemmalle tai oikealle tai keskitä se. |

## <a name="column-restrictions-in-a-column-definition"></a>Sarakkeen rajoitukset sarakkeen määrityksessä
Voit käyttää sarakkeen rajoituksia määrittäessäsi, miten sarakkeen määritys käyttää tietoja tai laskee ne. Voit myös rajata raportin sarakkeen koskemaan tiettyä yksikköä tai tiettyjä päivämääriä.

> [!NOTE]
> **Sarakerajoitus**-koodi korvaa minkä tahansa rivimäärityksen kanssa ristiriidassa olevan asetuksen.

### <a name="column-restrictions-cell"></a>Sarakkeen rajoitukset -solu

**Sarakkeen rajoitukset** -solu voi sisältää koodeja, jotka rajoittavat tai piilottavat tietoja, kuten rivin muotoilua tai sarakkeen tietoja ja summia.

#### <a name="add-a-column-restriction-in-a-column-definition"></a>Sarakkeen rajoituksen lisääminen sarakkeen määritykseen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta rajoitettavan sarakkeen **Sarakkeen rajoitukset** -solua.
3. Valitse **Sarakkeen rajoitukset** -valintaikkunan luettelosta yksi koodi tai useita koodeja ja valitse sitten **OK**.

### <a name="column-restriction-codes"></a>Sarakerajoituskoodit

Seuraavassa taulukossa esitellään sarakkeen rajoituksen koodit.

| Sarakkeen rajoituksen koodi | Kuvaus |
|-------------------------|-------------|
| SU                      | Piilottaa sarakkeen alaviivan, jos alaviivan komento (**---**) tai kaksoisalaviivan komento (**===**) on syötetty rivin määritykseen. Tämän voi tehdä, jos et halua alaviivaa prosenttilaskennan luomien summien kohdalle. |
| ST                      | Piilottaa kokonaissummat niin, että vain tiedot näytetään sarakkeessa (esimerkiksi tilastosarakkeessa). |
| SD                      | Piilota tiedot niin, että sarakkeessa näytetään vain **TOT**- ja **CAL**-rivi (rivin määrityksestä). |
| PR                      | Rajoita **FD**-sarakkeen summat debet-summiin. |
| CR                      | Rajoita **FD**-sarakkeen summat kredit-summiin. |
| ADJ                     | Rajoita sarakkeen summat kauden oikaisusummiin, jos summia ovat käytettävissä. |
| XAD                     | Rajoita sarakkeen summat niin, että kauden oikaisusummat suljetaan pois. |
| SS                      | Rajoita sarakkeen summat niin, että vain kirjatut tapahtumat sisällytetään, jos tapahtumia on käytettävissä. |
| UPT                     | Rajoita sarakkeen summat niin, että vain kirjaamattomat tapahtumat sisällytetään, jos tapahtumia on käytettävissä.<p><strong>Huomautus:</strong> Kaikki tietopalvelut eivät tue kirjaamattomia tapahtumia. </p> |

### <a name="restrict-a-column-to-a-reporting-unit"></a>Sarakkeen rajoittaminen raportoinnin yksikköön

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta rajoitettavan sarakkeen **Raportoinnin yksikkö** -solua.
3. Valitse **Raportoinnin yksikön valinta** -valintaikkunan **Raportointipuu**-luettelosta puu.
4. Laajenna tai tiivistä yksikköluettelo, valitse raportoinnin yksikkö ja valitse sitten **OK**.

## <a name="format-column-headers"></a>Sarakeotsikoiden muotoileminen
Voit lisätä, muokata ja poistaa raportissa sarakkeiden yläosassa näkyviä otsikoita. Voit määrittää myös ehdollisen koonnin sarakeotsikoita sarakkeiden määritysten **Jakso**-kentän ja raporttien määritysten **Perusjakso**-kentän perusteella. Perusjaksotoiminto säästää aikaa vaiheittaisten ennusteraporttien luomisen yhteydessä.

### <a name="create-and-manage-column-headers"></a>Sarakeotsikoiden luominen ja hallinta

Voit lisätä, muokata ja poistaa raportissa sarakkeiden yläosassa näkyviä otsikoita **Sarakeotsikko**-valintaikkunassa. Seuraavassa taulukossa esitellään **Sarakeotsikot**-valintaikkunan kentät.

| Kenttä                 | Kuvaus |
|-----------------------|-------------|
| Sarakeotsikon teksti    | Tämä teksti näkyy sarakeotsikossa. Voit kirjoittaa tekstin suoraan kenttään tai valita sarakeotsikon aina raportin luomisen yhteydessä päivittävän vaihtoehdon valitsemalla **Lisää automaattinen teksti**. Voit lisätä useita automaattisen tekstin koodeja valitsemalla uudelleen **Lisää automaattinen teksti** ja valitsemalla sitten toisen koodin luettelosta. |
| Muotoiluasetukset        | Käytä sarakeotsikossa muotoilua, kuten ruuutua tai alleviivausta. |
| Levitä mistä, Levitä mihin | Määritä sarake tai sarakkeet, joita otsikon teksti koskee. |
| Perustelu         | Määritä, miten sarakeotsikko kohdistetaan sarakkeeseen tai **Levitä mistä**- ja **Levitä mihin** -kentässä määritettyyn sarakeväliin. |

### <a name="create-a-column-header"></a>Sarakeotsikon luominen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta otsikkosolua.
3. Syötä **Sarakeotsikko**-valintaikkunassa sarakeotsikon teksti. Vaihtoehtoisesti voit valita **Lisää automaattinen teksti** -kohdan, jossa voit valita vaihtoehdon.
4. Valitse **Muotoiluasetukset**-kentässä otsikon muoto.
5. Syötä **Levitä mistä** -kenttään sen sarakkeen kirjain, josta sarakeotsikko alkaa. Syötä **Levitä mihin** -kenttään sen sarakkeen kirjain, johon sarakeotsikko loppuu.
6. Määritä **Tasaus**-kohdassa, tasataanko otsikon teksti vasemmalle vai oikealle vai keskitetäänkö se.
7. Napsauta **OK**.

### <a name="add-a-column-header-row"></a>Sarakeotsikon rivin lisääminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Valitse otsikkorivin solu.
3. Valitse **Muokkaa**-valikossa **Lisää rivi**. Uusi rivi lisätään vaiheessa 2 valitsemasi rivin yläpuolelle.

> [!NOTE]
> Jos raportissa on vähintään neljä tai ylätunnistetta, tunnisteet ovat päällekkäisiä, kun raportti viedään Excel-työkirjaan. Voit tarkastella kaikkia raportin otsikoita lisäämällä raportin määritykseen ylämarginaalin.

### <a name="delete-a-column-header-row"></a>Sarakeotsikon rivin poistaminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Valitse otsikon rivillä poistettava solu.
3. Valitse **Muokkaa**-valikossa **Poista rivi**.

### <a name="create-an-automatically-generated-header"></a>Automaattisesti luodun otsikon luominen

Raportin suunnittelija voi luoda sarakeotsikoita automaattisesti automaattisen tekstin koodien perusteella. Automaattisen tekstin koodit ovat muuttujia, jotka päivitetään aina raportin luomisen yhteydessä. Mikä tahansa sarakeotsikko voi sisältää näitä koodeja. Ne määrittävät raportin muuttuvia tietoja, kuten päivämääriä ja jaksojen numeroita. Tämän vuoksi useissa raportin määrityksissä, ajanjaksoissa ja raportointipuissa voidaan käyttää yhtä sarakkeen määritystä. Koska automaattisen tekstin koodeissa käytetään sarakkeen määrityksen tietorivien kalenterin tietoja, niitä tuetaan vain **CALC**- ja **FD**-sarakkeissa. Tapa, jolla automaattisen tekstin koodi näkyy sarakeotsikon solussa, vaikuttaa siihen, miten tiedot näkyvät raportissa. Automaattisen tekstin koodeissa käytetään isoja ja pieniä kirjaimia **Sarakeotsikko**-valintaikkunassa. Tämän vuoksi teksti näkyy näin myös raportissa. Esimerkiksi vakiokalenterivuoden **\@CalMonthLong** muuntaa kuukauden **7** muotoon **Heinäkuu**. Jos raportin tekstin pitää olla isoilla kirjaimilla (esimerkiksi **HEINÄKUU**), kirjoita myös koodi isoin kirjaimin **Sarakeotsikon teksti** -ruutuun. Kirjoita esimerkiksi **\@CALMONTHLONG**. Tekstissä voi käyttää sekä isoja ja pieniä kirjaimia. Voit syöttää otsikon tekstin esimerkiksi tällaisena: **Period \@FiscalPeriod-\@FiscalYear from \@StartDate to \@EndDate**. Luotu raportin otsikko muistuttaa seuraavaa tekstiä: **Jakso 1–02 01/01/02–01/31/02**.

> [!NOTE]
> Joidenkin tekstien muoto, kuten pitkä päivämäärä, riippuu palvelimen alueellisista asetuksista. Voit muuttaa näitä asetuksia valitsemalla **Käynnistä**-painikkeen, **Ohjauspaneeli**-kohdan ja valitsemalla sitten **Alue ja kieli** -kohdan. Seuraavassa taulukossa luetellaan sarakeotsikoiden käytettävissä olevat automaattisen tekstin asetukset.


| Automaattinen teksti -asetus ja koodi                | Kuvaus |
|-----------------------------------------|-------------|
| Kuukauden nimi (@CalMonthLong)              | Tulosta kuluvan kuukauden nimi sarakeotsikkoon. Jos haluat pyöristää raportin summat tuhansiksi, miljooniksi tai miljardeiksi tai määrittää raportin sarakkeiden leveyden pienemmäksi kuin 9 merkkiä, kuukauden nimi lyhennetään nimen kolmeksi ensimmäiseksi merkiksi. |
| Kuukauden nimen lyhenne (@CalMonthShort) | Tulosta valitun tilikauden kuukauden nimen lyhenne. |
| Jakson numero (@FiscalPeriod)           | Tulosta tilikauden numeerinen muoto, joka sarakkeelle on määritetty. Jos sarake levitetään useille jaksoille, tulostetaan välin viimeinen jakso. |
| Jakson kuvaus (@FiscalPeriodName)  | Tulosta taloushallinnon tiedoissa määritetty tilikauden kuvaus. |
| Tilikausi (@FiscalYear)               | Tulosta sarakkeen tilikausi numeerisessa muodossa. |
| Kalenterivuosi (@CalYear)                | Tulosta sarakkeen kalenterivuosi numeerisessa muodossa. |
| Alkamispäivämäärä (@StartDate)                 | Tulosta sarakkeen alkamispäivämäärä. |
| Päättymispäivämäärä (@EndDate)                     | Tulosta sarakkeen päättymispäivämäärä. |
| Yksikön nimi puusta (@UnitName)         | Jos sarake rajoitetaan tietylle raportointipuun yksikölle, tulosta sarakeotsikon yksikön nimi. |
| Yksikön kuvaus (@UnitDesc)            | Jos sarake rajoitetaan tietylle raportointipuun yksikölle, tulosta sarakeotsikon yksikön kuvaus. |
| Kirjakoodi (@BookCode)                   | Tulosta sarakkeelle määritetty kirjakoodi. |
| Tyhjä rivi (@Blank)                     | Lisää sarakeotsikkoon tyhjä rivi. |

### <a name="create-a-conditional-spanning-header"></a>Ehdollisen koonnin otsikon luominen

Ehdollisen koonnin otsikot voivat olla useiden tietyn jakson tietoihin perustuvien sarakkeiden käytössä. Jos käsittelyssä on esimerkiksi tilikauden budjettiraportti, ja haluat näyttää edellisten kuukausien toteutuneet budjetit tulevien kuukausien ennustettujen budjettien kanssa, voit päivittää raportin otsikon automaattisesti ehdollisen koonnin otsikon avulla. Ota huomioon seuraavat tilanteet, kun luot ehdollisen jatkuvan otsikon:

- Mikä tahansa pysäytysehto (**Levitä mihin** -kenttä), joka täsmää ennen aloitusehtoa (**Levitä mistä** -kenttä) ohitetaan. Esimerkiksi sarakkeen B levitysehto on BASE+1 - BASE. BASE on sarakkeessa C ja BASE+1 sarakkeessa D. Tässä tapauksessa sarakkeen C pysäytysehto ohitetaan ja otsikon tulostus alkaa sarakkeesta D.
- Jos määritetyt sarakeotsikot ovat päällekkäisiä, ne ovat päällekkäisiä myös raporttiin tulostettuna. Raportti luodaan, mutta seuraava varoitus tulee näkyviin **Raportin jonon tila** -kentässä: "Sarakeotsikot, jotka käyttävät pohjaa leikkaavat muiden sarakkeiden otsikoiden kanssa ja tämä saattaa aiheuttaa päällekkäistä tekstiä." Esimerkiksi sarakkeen B otsikkomääritys on B to BASE+1, ja sarakkeen D otsikkomääritys on is BASE+1 to F. Tässä tapauksessa otsikot tulostetaan toistensa päälle, jolloin niitä ei voi lukea. Kun BASE-määritystä käytetään **Levitä mistä / Levitä mihin** -määrityksessä, muista aina tarkistaa luotava raportti päällekkäisten otsikoiden varalta.
- Jos levitysehdon BASE-määritys määritetään Ei tulostusta (**NP**) -sarakkeessa, se ohitetaan sarakkeen määrityksessä tehdyistä valinnoista huolimatta. Tämä skenaario on sama kuin sarakeotsikon määrityksen luomatta jättäminen.
- Ehdollisten tulostussarakkeiden (**P&lt;B**, **P&gt;=B**) ehdollisen koonnin otsikot toimivat kuten mikä tahansa sarakeotsikon määritys. Jos esimerkiksi ehto on epätosi, mikä tahansa levitysehtoa vastaava peräkkäinen sarake käynnistää otsikon tulostuksen.

#### <a name="create-a-conditional-spanning-header"></a>Ehdollisen koonnin otsikon luominen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta otsikkosolua.
3. Syötä **Sarakeotsikko**-valintaikkunassa sarakeotsikon teksti. Vaihtoehtoisesti voit valita **Lisää automaattinen teksti** -kohdan, jossa voit valita vaihtoehdon.
4. Valitse **Muotoiluasetukset**-kentässä otsikon muotoilutyyli.
5. Määritä perusjaksoon liittyvä kausi, joka määritetään raportin luomisen yhteydessä. Syötä **Levitä mistä**- ja **Levitä mihin** -kenttään jonkin seuraavista arvoista: **BASE**, **BASE-X** tai **BASE+X**, jossa X on perusjakson jaksojen määrä. Jos syötät esimerkiksi **Levitä mistä** -kenttään **BASE**-arvon, ehdollisen koonnin sarakeotsikon teksti alkaa sarakeotsikosta, jossa raportin määrityksen **perusjakson** arvo on sama kuin **jakson** arvo. Se päättyy **Levitä mihin** -kenttään määritettyyn sarakkeeseen. Jos siis levitys tapahtuu välillä BASE - M ja raportin määrityksen **perusjakson** arvo on **4**, otsikko alkaa sarakkeesta, jossa jakson arvoksi on määritetty **4**. Se päättyy sarakkeeseen M. Otsikot päättyvät ja alkavat vain tulostussarakkeissa.
6. Määritä **Tasaus**-kohdassa, tasataanko otsikon teksti vasemmalle vai oikealle vai keskitetäänkö se.
7. Valitse **OK**.

#### <a name="example-of-a-conditional-spanning-header"></a>Ehdollisen koonnin otsikon esimerkki

Käyttäjä on luomassa dynaamista kuuden kuukauden ennusteen raporttia. Käyttäjä haluaa tulostaa toteutuneita tietoja sisältäviin sarakkeisiin sanan Toteutunut ja budjettiennusteita sisältäviin sarakkeisiin sanan Budjetti. Raportti suoritetaan joka kuukausi, joten kuukausi kuukaudelta toteutuneita sarakkeita on yksi enemmän ja budjettisarakkeita yksi vähemmän. Vaikka käyttäjä voi muokata sarakkeen määritystä otsikoiden oikaisua varten manuaalisesti aina, kun raportti luodaan, hän päättää luoda ehdollisen koonnin otsikot ja säästää aikaa ja työtä. Näin otsikot luodaan automaattisesti oikeisiin sarakkeisiin aina, kun raportti suoritetaan. Käyttäjä avaa Report Designerin, valitsee siirtymisruudussa **Sarakkeen määritys** -kohdan ja avaa raportin sarakkeen määrityksen. Sitten käyttäjä syöttää seuraavat tiedot: Raportin määrityksen perusjakso on 4.

|      Muoto         |  A   | D             | K             | D             | E             | F             | G             | H             | I             | J             | K             | L             | M             |
|---------------------|------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|
| Otsikko 1            |      | Todellinen        | Budjetti        |               |               |               |               |               |               |               |               |               |               |
| Otsikko 2            |      | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong | @CalMonthLong |
| Otsikko 3            |      |               |               |               |               |               |               |               |               |               |               |               |               |
| Saraketyyppi         | KUV | TD            | TD            | TD            | TD            | TD            | TD            | TD            | TD            | TD            | TD            | FD            | FD            |
| Kirjakoodi/määrite |      | TOTEUTUNUT        | BUDJETTI2012    | TOTEUTUNUT        | BUDJETTI2012    | TOTEUTUNUT        | BUDJETTI2012    | TOTEUTUNUT        | BUDJETTI2012    | TOTEUTUNUT        | BUDJETTI2012    | TOTEUTUNUT        | BUDJETTI2012    |
| Tilikausi         |      | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          | BASE          |
| Kausi              |      | 1             | 1             | 2             | 2             | 3             | 3             | 4             | 4             | 5             | 5             | 6             | 6             |
| Katetut kaudet     |      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      | KAUSITTAINEN      |
| Sarakkeen leveys        | 30   | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            | 10            |
| Tulostusohjaus       |      | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        | P&lt;=B       | P&gt;B        |

Tämän jälkeen käyttäjä kaksoisnapsauttaa sarakeotsikon solua sarakkeessa B ja avaa **Sarakeotsikko**-valintaikkunan, johon hän syöttää seuraavat tiedot.

| Kenttä              | Arvo                 |
|--------------------|-----------------------|
| Sarakeotsikon teksti | Todellinen                |
| Lisää automaattinen teksti    | Valintaa ei ole tehty. |
| Muotoiluasetukset     | Ruutu                   |
| Perustelu      | Valintaa ei ole tehty. |
| Levitä mistä        | D                     |
| Levitä mihin          | BASE                  |

Tietojen syöttämisen jälkeen käyttäjä napsauttaa **OK-painiketta**. Tämän jälkeen hän kaksoisnapsauttaa sarakeotsikon solua sarakkeessa C ja avaa **Sarakeotsikko**-valintaikkunan, johon hän syöttää seuraavat tiedot.

| Kenttä              | Arvo                 |
|--------------------|-----------------------|
| Sarakeotsikon teksti | Budjetti                |
| Lisää automaattinen teksti    | Valintaa ei ole tehty. |
| Muotoiluasetukset     | Ruutu                   |
| Perustelu      | Valintaa ei ole tehty. |
| Levitä mistä        | BASE+1                |
| Levitä mihin          | M                     |

Tämän jälkeen toteutuneita tietoja sisältäviin sarakkeisiin tulostetaan sana Toteutunut ja budjettiennusteita sisältäviin sarakkeisiin sana Budjetti aina, kun raportti luodaan. Tämän lisäksi sarakkeiden määrä oikaistaan joka kuukausi.

## <a name="apply-column-justification"></a>Sarakkeen tasauksen käyttäminen
**Tasaus**-solun avulla raportin kuvaussarakkeessa käytetään tasausmuotoilua. Tämä vaihtoehto vaikuttaa vain sarakkeen kuvauksiin, ei toteutuneisiin arvoihin.

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta **Tasaus**-solua.
3. Valitse jokin seuraavista luettelon arvoista:

    - **Ei mitään** – tasausta ei käytetä.
    - **Vasen** – sarakkeen kuvaukset tasataan vasemmalle.
    - **Keskitys** – sarakkeen kuvaukset keskitetään.
    - **Oikea** – sarakkeen kuvaukset tasataan oikealle.

## <a name="add-special-formatting-options"></a>Erityismuotoiluvalintojen lisääminen
Sarakkeen määrityksen muotoilusarakkeen tietorivien valituissa sarakkeissa käytetään erityismuotoilua. Vaikka jotkin **Tulostuksen hallinta**- ja **Sarakkeiden rajoitukset** -vaihtoehdoista ovat **FD**-sarakekohtaisia, suurin osa vaihtoehdoista koskee kaikkia saraketyyppejä. Sarakkeen määrityksessä määritetty muotoilu korvaa raportin määrityksessä määritetyn muotoilun. Rivin määrityksessä määritetty muotoilu korvaa kuitenkin sarakkeen määrityksessä määritetyn muotoilun. Seuraavilla riveillä käytetään muotoilurivejä:

- Sarakkeen leveys
- Lisävälilyönnit ennen saraketta
- Muotoilun/valuutan korvaus
- Tulostuksen hallinta

### <a name="changing-the-column-width"></a>Sarakkeen leveyden muuttaminen

**Sarakkeen leveys** -solu määrittää tämän sarakkeen merkkien määrän tulostetussa raportissa. Sarakkeen leveys on tärkeä sarakkeissa, jotka sisältävät summia (sarakkeet, joiden tyyppi on **CALC**, **WKS** tai **FD**), kuvauksissa (sarakkeet, joiden tyyppi on **DESC**) tai täytöissä (sarakkeet, joiden tyyppi on **FILL**). Oletusarvoisesti on valittuna **Sovita**-vaihtoehto. Tällöin kunkin sarakkeen leveys määritetään automaattisesti sarakkeen sisällön mukaan.

#### <a name="specify-the-width-of-a-column-on-a-report"></a>Raportin sarakkeen leveyden määrittäminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Syötä **Sarakkeen leveys** -soluun sarakkeen leveyden välilyöntien määrä. Sarakkeen leveyden enimmäismäärä on 255 merkkiä (tämä luku sisältää sentit, pilkut ja sulut) Vaihtoehtoisesti voit ottaa käyttöön raportin suunnittelijan ja valita sarakkeen leveyden solun sisällön perusteella kaksoisnapsauttamalla **Sarakkeen leveys** -solua ja valitsemalla sitten **Sovita**.

### <a name="add-space-between-columns"></a>Välilyönnin lisääminen sarakkeiden väliin

**Lisävälilyönnit ennen saraketta** -solu määrittää sarakkeiden välisen erottimen leveyden sarakkeen määrityksessä. **Lisävälilyönnit ennen saraketta** -asetus vaikuttaa sarakkeen tietoriveihin, mutta ei sarakeotsikoiden riveihin. Tämän vaihtoehdon avulla voit erotella sarakeryhmät tai lisätä muutaman välilyönnin ennen kuvausta, jolloin kuvaussarake sisennetään raportin vasemmalle tasatuista otsikoista. Kunkin sarakkeen välissä olevien välilyöntien oletusmäärä on kaksi. Voit muuttaa tätä asetusta raportin määrityksen **Asetukset**-välilehdessä.

#### <a name="specify-the-space-between-columns"></a>Sarakkeiden välisten välien määrittäminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Syötä **Lisävälilyönnit ennen saraketta** -soluun sarakkeiden väliin lisättävien välilyöntien määrä.

### <a name="specify-a-format-currency-override"></a>Valuutan muotoilun ohituksen määrittäminen

**Muotoilun/valuutan ohitus** -solussa määritetään sarakkeen desimaalin, valuutan ja prosenttimäärien muotoilu. Tämä muotoilu korvaa sarakkeen ja raportin määrityksessä tai järjestelmän oletusarvoissa määritetyn muotoilun.

#### <a name="assign-a-format-currency-override-to-a-report-column"></a>Valuutan muotoilun korvaamisen määrittäminen raportin sarakkeelle

1. Avaa raporttien suunnitteluohjelmassa sarakemääritys, jota haluat muokata.
2. Kaksoisnapsauta **Muotoilun/valuutan korvaus** -solua summasarakkeessa.
3. Valitse **Muotoilun ohitus** -valintaikkunassa muotoiluasetukset.

### <a name="add-a-print-control-code"></a>Tulostuksen hallintakoodin lisääminen

**Tulostuksen hallinta** -solu voi sisältää koodeja, joiden mukaan sarakkeen näyttö- tai tulostusominaisuuksia muokataan. Tulostuksen hallintakoodeja on kaksi eri tyyppiä: tavalliset tulostuksen hallintakoodit ja ehdolliset hallintakoodit.

#### <a name="regular-print-control-codes"></a>Tavalliset tulostuksen hallintakoodit

| Tulostuksen hallintakoodi | Käännös                                     | Kuvaus |
|--------------------|-------------------------------------------------|-------------|
| NP                 | Piilotettu                                     | Tämän sarakkeen summat suljetaan pois tulostettavasta raportista ja laskutoimituksista. Voit ottaa piilotetun sarakkeen mukaan laskutoimitukseen viittaamalla sarakkeeseen suoraan laskentakaavassa. Piilotettu sarake C voidaan esimerkiksi sisällyttää seuraavaan laskutoimitukseen: **B+C+D**. Piilotettua saraketta C ei kuitenkaan oteta mukaan esimerkiksi seuraavaan laskutoimitukseen: **B:D**. |
| XCR                | Merkin muuttaminen, jos rivin tavallinen saldo on kredit | Luo budjetti tai vertaileva raportti, jossa mikä tahansa kielteinen varianssi (kuten tuoton vaje tai kulujen ylitys) on aina negatiivinen. Ota tämä koodi käyttöön **CALC**-sarakkeessa ja vaihda sarakesumman etumerkki, jos annetun rivin tavallinen saldo on kredit (kuten rivin määrityksen **Tavallinen saldo** -sarakkeen **C**-arvo määrittää).<p><strong>Huomautus:</strong> Varmista, että <strong>TOT</strong>- ja </strong>CAL</strong>-riveille, joissa usein on kredit-saldo, syötetään rivin määrityksen <strong>Tavallinen saldo</strong> -sarakkeeseen <strong>C</strong>.</p> |
| X0                 | Sarakkeen piilottaminen, jos ne ovat nollia tai tyhjiä          | Sulje **FD**-sarake pois raportista, jos sarakkeen kaikki solut ovat tyhjiä tai sisältävät vain nollia. |
| SR                 | Estä pyöristys                               | Estä tämän sarakkeen summien pyöristys. |
| XR                 | Piilota koonti                                 | Piilota koonti. Jos raportissa käytetään raportointipuuta, tämän sarakkeen summia ei koota vastaaviksi ylätason solmuiksi. |
| RP                 | Sarakkeen toistaminen jokaisella sivulla                      | Toista määritetty sarake raportin jokaisella sivulla. Voit käyttää esimerkiksi tulostuksen **RP**-hallintakoodia, kun haluat sisällyttää rivien koodeja noutavan **ROW**-tyyppiä olevan sarakkeen jokaiselle sivulla. |
| WT                 |  Rivitä teksti                                      |  Jos sarakkeen teksti on liian pitkä, eikä sitä voida sovittaa sarakkeen tilaan, se voidaan rivittää. Tällöin teksti mahtuu sarakkeeseen. |

#### <a name="conditional-print-control-codes"></a>Ehdolliset tulostuksen hallintakoodit

| Ehdolliset tulostuksen hallintakoodi | kuvaus                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------|
| (ei mitään)                         | Poista ehdollisen tulostuksen valinta.                                                  |
| P&lt;B                         | Näyttää tietyn sarakkeen vain, jos jakso on pienempi kuin perusjakso.             |
| P&gt;B                         | Näyttää tietyn sarakkeen vain, jos jakso on suurempi kuin perusjakso.             |
| P=B                            | Näyttää tietyn sarakkeen vain, jos jakso on yhtä suuri kuin perusjakso.              |
| P&lt;=B                        | Näyttää tietyn sarakkeen vain, jos jakso on pienempi tai yhtä suuri kuin perusjakso. |
| P&gt;=B                        | Näyttää tietyn sarakkeen vain, jos jakso on suurempi tai yhtä suuri kuin perusjakso. |

#### <a name="add-print-control-codes-to-a-report-column"></a>Tulostuksen hallintakoodin lisääminen raporttisarakkeeseen

1. Avaa raporttien suunnitteluohjelmassa sarakemääritys, jota haluat muokata.
2. Kaksoisnapsauta **Tulostusohjaus**-solua.
3. Valitse **Tulostuksen hallinta** -valintaikkunassa koodi **Valitse tulostuksen hallinnan asetukset** -luettelosta. Voit valita useita koodeja pitämällä Ctrl-näppäintä alhaalla koodien valinnan aikana.
4. Valitse vaihtoehto **Ehdollisen tulostuksen asetukset** -kentässä. Oletusasetus on **(ei mitään)**. Voit valita vain yhden ehdollisen tulostuskoodin kerrallaan.
5. Valitse **OK**.

> [!TIP]
> Voit myös syöttää tulostuskoodeja suoraan **Tulostuksen hallinta** -soluun. Erota tulostuksen useat hallintakoodit pilkuilla.

## <a name="column-types"></a>Sarakelajit
Raportin kunkin sarakkeen tietojen lajin määrittää sarakkeen määrityksen **Sarakelaji**-rivin arvo. Kussakin sarakemäärityksessä on oltava vähintään yksi kuvaussarake (**KUV**) ja yksi summasarake (**TD**, **LTAUL** tai **LASK**).

> [!NOTE]
> Saraketyyppikoodit eivät sovellu kaikkiin kirjanpitojärjestelmiin. Jos valitset lajin, joka ei kelpaa organisaation kirjanpitojärjestelmässä, sarake näkyy raportissa tyhjänä.

### <a name="specify-a-column-type"></a>Sarakelajin määrittäminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta oikeassa sarakkeessa **Sarakelaji**-rivin solua.
3. Valitse luettelosta sarakelaji. Eri sarakelajit esitellään seuraavassa taulukossa.

    <table>
    <thead>
    <tr>
    <th>Sarakelajin koodi</th>
    <th>Kuvaus</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>TD</td>
    <td>Näytä taloustiedot, kun käytät rivimääritelmän <strong>Linkki taloushallinnon dimensioihin</strong> -saraketta. Kun valitset <strong>TD</strong>-saraketyypin, seuraaville riveille määritetään automaattisesti oletusasetukset: <ul>
    <li><strong>Kirjauskoodi/määriteryhmä</strong> TOTEUTUNUT</li>
    <li><strong>Kirjauskoodi/määriteryhmä</strong> TOTEUTUNUT</li>
    <li><strong>Tilikausi:</strong> BASE</li>
    <li><strong>Kausi:</strong> BASE</li>
    <li><strong>Katetut kaudet</strong> Kausittainen</li>
    <li><strong>Sarakkeen leveys:</strong> 14</li>
    </ul>
Näitä oletusasetuksia voi muuttaa.</td>
    </tr>
    <tr>
    <td>CALC</td>
    <td>Näytä <strong>Kaava</strong>-solussa määritetyn yksinkertaisen tai monimutkaisen laskutoimituksen tulokset. Lisätietoja on kohdassa <a href="advanced-formatting-options-financial-reporting.md">Muotoilun lisäasetukset taloushallinnon raportoinnissa</a>.</td>
    </tr>
    <tr>
    <td>KUVAUS</td>
    <td>Näytä rivin kuvaus rivin määrityksestä. Vaikka kuvaussarake on usein raportin ensimmäinen sarake, se voi olla missä tahansa kohdassa.</td>
    </tr>
    <tr>
    <td>ROW</td>
    <td>Näytä taloushallinnon rivien yksittäisten rivien koodit rivin määrityksen <strong>Rivin koodi</strong> -sarakkeesta. Lisätietoja on kohdassa <a href="row-definitions-financial-reporting.md">Rivien määritykset taloushallinnon raportoinnissa</a>.</td>
    </tr>
    <tr>
    <td>ACCT (tilikoodit)</td>
    <td>Näytä jokaisella rivillä käytettävät taloushallinnon tietojen segmentti- tai dimensioarvot. Tili- ja tapahtumatietojen raporteissa tulostetaan täydellinen tilinumero, (esimerkiksi <strong>110140-070-0101</strong>). Jos liittyvän rivimäärityksen <strong>Linkki taloushallinnon dimensioihin</strong> -sarakkeessa on määritetty alueita, hakasulkeissa olevaa aluetta käsitellään samoin kuin yksittäistä arvoa (esimerkiksi <strong>[110140:110700]-070-[0101:0200]</strong>). Talousraporteissa ja korkean tason raporteissa, jotka voivat olla yhdistelmiä useista tileistä, tulostetaan taloushallinnon tietojen linkki rivimäärityksestä (esimerkiksi <strong>1100:1200</strong>).</td>
    </tr>
    <tr>
    <td>FILL</td>
    <td>Täytä soluun merkki, joka on heittomerkkien sisällä. Jos et syötä merkkiä, sarake on tyhjä. Esimerkiksi sarakkeen, jolla on ellipsi (...), voi täyttää syöttämällä <strong>FILL</strong> <strong>'.'</strong>.</td>
    </tr>
    <tr>
    <td>PAGE</td>
    <td>Lisää raporttiin pystysuora sivunvaihto. <strong>SIVU</strong>-sarakkeen oikealla puolella olevat sarakkeet tulevat eri sivulle.</td>
    </tr>
    <tr>
    <td>ATTR</td>
    <td>Jos kirjanpitojärjestelmä tukee määritteitä, näytä sarakkeessa tilin tai tapahtuman määrite. Määrite, jota käytetään yhdessä täydellisessä tilissä, poimii taloushallinnon tiedoista tilin tai tapahtuman taustatietoja. Tilitason määritteet näyttävät tietoja tilistä, ja tapahtumatason määritteet näyttävät tietoja tapahtuman kirjaushetkeltä. Kun valitset saraketyypiksi <strong>MÄÄR</strong>, määritä sarakemäärityksen <strong>Kirjauskoodi/määriteryhmä</strong>-tietorivillä.</td>
    </tr>
    </tbody>
    </table>

### <a name="financial-dimensions-column"></a>Taloushallinnon dimensioiden sarake

Seuraavia **sarakkeen määrityksen** rivien määrityksiä käytetään sarakkeissa, joiden sarakelaji on **FD** (summat taloushallinnon dimensioista).

#### <a name="book-codeattribute-category-cell"></a>Kirjakoodi/määriteluokka-solu

**Kirjakoodi/määriteluokka**-solu määrittää **FD**-sarakkeen tietojen kirjakoodin Sarakkeen määritys voi sisältää useita toteutuneiden tietojen, budjetin ja tilastojen sarakkeita. Sarakkeen määrityksessä voidaan näyttää myös erilaisia jaksoja, kuten kuluva tai vuoden alusta, sekä erilaisia summia. Kirjakoodien luettelo vaikuttaa toteutuneiden, budjetin ja tilastojen (muu kuin taloushallinto) asetuksiin, jotka on määritetty taloushallinnon tiedoissa.

#### <a name="fiscal-year-cell"></a>Tilikausi-solu

**Tilikausi**-solu määrittää tilikauden, jonka sarake sisältää. Vuosi voi olla suhteessa perusvuoteen, joka on määritetty raportin luomisen yhteydessä. Valittavissa ovat seuraavat vaihtoehdot.

| Vaihtoehto  | Kuvaus                                                                                                                  |
|---------|------------------------------------------------------------------------------------------------------------------------------|
| PERUS    | Käytä raportin ajassa määritettyä perusvuotta.                                                                          |
| BASE+\# | Käytä vuotta, joka on \# vuotta perusvuoden jälkeen. Voit käyttää esimerkiksi kolmatta vuotta perusvuoden jälkeen syöttämällä **BASE+3**. |
| BASE-\# | Käytä vuotta, joka on \# vuotta ennen perusvuotta. Voit käyttää esimerkiksi edellistä vuotta syöttämällä **BASE-1**.                 |
| \#      | Syötä toteutunut tilikausi.                                                                                                |

#### <a name="period-cell"></a>Jakso-solu

**Jakso**-solu määrittää tilikaudet, jonka sarake sisältää. Jakso voi olla suhteessa perusjaksoon, joka määritetään raportin luomisen yhteydessä. Valittavissa ovat seuraavat vaihtoehdot.

| Vaihtoehto          | kuvaus |
|-----------------|-------------|
| PERUS            | Käytä perusjaksoa. |
| BASE+\#         | Käytä jaksoa, joka on \# jaksoa perusjakson jälkeen. Voit käyttää esimerkiksi kolmatta jaksoa perusjakson jälkeen syöttämällä **BASE+3**. |
| BASE-\#         | Käytä jaksoa, joka on \# jaksoa ennen perusjaksoa. Voit käyttää esimerkiksi edellistä jaksoa syöttämällä **BASE-1**. |
| BASE-\#:BASE    | Useiden jaksojen käyttäminen on mahdollista niin, että aloitat useiden jaksojen käyttämisen ennen perusjaksoa ja jatkat perusjaksoon asti. Jos haluat käyttää esimerkiksi kolmea edellistä jaksoa ja perusjaksoa, syötä **BASE-3:BASE**. |
| BASE:BASE+\#    | Useiden jaksojen käyttäminen on mahdollista niin, että aloitat perusjaksosta ja jatkat käyttämistä useita jaksoja perusjakson jälkeen. Voit käyttää esimerkiksi perusjaksoa ja seuraavaa kahta jaksoa syöttämällä **BASE:BASE+2**. |
| BASE-\#:BASE+\# | Useiden jaksojen käyttäminen on mahdollista niin, että aloitat useita jaksoja ennen perusjaksoa alkavilla jaksoilla ja jatkat useita jaksoja perusjakson jälkeen jatkuviin jaksoihin. Jos haluat käyttää esimerkiksi kolmea edellistä jaksoa, perusjaksoa ja seuraavia kahta jaksoa, syötä **BASE-3:BASE+2**. |
| 1:BASE          | Useiden jaksojen käyttäminen on mahdollista niin, että aloitat ensimmäisestä jaksosta perusjaksoon asti. |
| \#              | Käytä aina tiettyä jaksonumeroa. Tämän toiminnon käyttämistä ei suositella, koska se vähentää sarakkeen määrityksen joustavuutta. |
| \#                                      : \#           | Käytä aina tiettyä jaksoväliä. Tämän toiminnon käyttämistä ei suositella, koska se vähentää sarakkeen määrityksen joustavuutta. |

Voit siirtyä tilikauden ulkopuolelle minkä tahansa jakson määrityksissä. Voit myös yhdistää jaksoväleissä eri vuosia. Esimerkiksi voit määrittää kausia, jotka on **BASE-5** (esittämään viimeisintä kuutta ajanjaksoa) ja ajaa raportin, jossa on peruskautena 2. Tällöin raportissa näkyy tietoja määritetyn tilikauden kahdesta ensimmäisestä kaudesta ja edellisen tilikauden viimeisestä neljästä kaudesta.

### <a name="specify-the-periods-for-an-fd-column"></a>TD-sarakkeen kausien määrittäminen

1. Avaa raporttien suunnitteluohjelmassa sarakemääritys, jota haluat muokata.
2. Kaksoisnapsauta **FD**-sarakkeessa **Jakso**-rivin solua. Valitse sitten vaihtoehto luettelosta.
3. Tee kaava valmiiksi siirtymisruudun yläpuolella olevalla kaavarivillä tai **Jakso**-solussa. Korvaa kaikki numeromerkit (\#) sopivalla arvolla.

#### <a name="periods-covered-cell"></a>Katetut jaksot -solu

**Katetut jaksot** -solu määrittää summan, joka näytetään sarakkeessa. Tämä summa on suhteessa sarakkeen **Tilikausi**- ja **Jakso**-soluun. Valittavissa ovat seuraavat vaihtoehdot.

| Vaihtoehto      | Kuvaus                                                                 |
|-------------|-----------------------------------------------------------------------------|
| PERIODIC    | Näytä nykyisen jakson tai jaksovälin tehtävän summa. |
| PERIODIC/BB | Näytä nykyisen jakson tai jaksovälin alkusaldo.   |
| YTD         | Näytä tehtävän summa vuoden alusta.                               |
| YTD/BB      | Näytä vuoden alkusaldo.                                 |

### <a name="specify-the-periods-that-are-covered-for-an-fd-column"></a>FD-sarakkeen katettujen jaksojen määrittäminen

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta **FD**-sarakkeessa **Katetut jaksot** -rivin solua. Valitse sitten vaihtoehto luettelosta.

### <a name="attribute-filter-in-a-column-definition"></a>Sarakkeen määrityksen määritesuodatin

Määritteet ovat taloushallinnon tietojen arvoja, jotka määrittävät tilin tai tapahtuman tarkemmin. Tilimääritteitä ovat **Käyttöomaisuus**, **Velka**, **Tuotto** ja **Kulu**. Tapahtumamääritteitä ovat **Tapahtuman kuvaus** ja **Tapahtuman käyttöpäivämäärä**. Määritetuki voi vaihdella eri Microsoft Dynamics ERP -järjestelmien kesken. **Määritesuodatin**-solu rajoittaa **FD**-sarakkeiden tiedot määritettyihin määriteluokkien arvoihin tai alueisiin. Vaikka tätä toimintoa voi käyttää yhdessä **ATTR**-sarakkeen kanssa, **ATTR**-sarake ei ole pakollinen. **FD**-sarake sisältää tilien tai tapahtumien rajoituksen, jonka raportti saa määritesuodattimesta.

> [!NOTE]
> Jos haluat tarkistaa, mitä määritteitä ERP-järjestelmäsi tukee, tutustu järjestelmäsi integrointioppaaseen.

#### <a name="apply-an-attribute-filter-for-an-fd-column-on-a-report"></a>Määritesuodattimen käyttäminen raportin FD-sarakkeessa

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta **TD**-sarakkeen **Määritesuodatin**-solua.
3. Kaksoisnapsauta **Määritesuodatin**-valintaikkunan **Määrite**-sarakkeen solua ja valitse sitten haluamasi suodatintyyppi.
4. Voit rajoittaa tuloksia lisää syöttämällä **Mistä**- ja **Mihin**-sarakkeiden alue. **Mistä**-solussa on oltava arvo.
5. Napsauta **OK**.

#### <a name="example-of-an-attribute-filter"></a>Määritesuodattimen esimerkki

Seuraavassa esimerkissä esitetään osa sarakkeen kuvausta, joka sisältää tilimääritteen **Kirjakoodi/määriteluokka**-rivillä. Tämän sarakkeen määritesuodatin määrittää arvovälin, joka sisällytetään raporttiin.

|      Suodatus                  | A    | D                   |
|------------------------------|------|---------------------|
| Saraketyyppi                  | KUV | TD                  |
| Kirjauskoodi/määriteryhmä |      | TOTEUTUNUT              |
| Tilikausi                  |      | BASE                |
| Kausi                       |      | 1:BASE              |
| Katetut kaudet              |      | KAUSITTAINEN            |
| ...                          |      |                     |
| Sarakkeen leveys                 | 30   |                     |
| ...                          |      |                     |
| Määritesuodatin             |      | Viite=\[01:10\] |

### <a name="dimension-filter-in-a-column-definition"></a>Sarakkeen määrityksen dimensiosuodatin

Dimensiosuodatinta käytetään rajoitettaessa **FD**-sarake tietyille dimensioarvoille. Suodatin voi sisältää yksittäisen dimension, dimensioiden alueen tai dimensioryhmän. Suodatin voi sisältää myös dimensioarvojoukkoja. Koska dimensioarvot voivat vaihdella, kohteeseen ..\\financial-dimensions\\dimension perustuvan järjestelmän ei tarvitse olla tietyn pituinen. Suodatin otetaan käyttöön siitä huolimatta, sisältääkö raportti raportointipuun. Yleismerkkejä (\* tai?) voi käyttää missä tahansa kohdassa. Lisää useita tilejä määritettäessä pilkku tilien väliin, kuten seuraavassa esimerkissä: +Tili=\[1200\], +Tili=\[1100\], Osasto=\[01?\] Voit vastaanottaa tietyn tilin kaikki osastot sulkemalla osaston dimension pois dimensiosuodattimesta. Esimerkiksi molemmat seuraavista dimensiosuodattimista käsitellään samalla tavalla:

- +tili=\[1100\],osasto
- +tili=\[1100\]

Voit käyttää myös mitä tahansa aakkosnumeerisen merkin yhdistelmää tarkassa vastineessa. Esimerkiksi **Sijainti = \[10\*\]** sisältää kaikki sijainnin dimensioarvot, jotka alkavat arvolla 10.

#### <a name="apply-a-dimension-filter-for-a-column-on-a-report"></a>Dimensiosuodattimen käyttäminen raportin sarakkeessa

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta **FD**-sarakkeen **Dimensiosuodatin**-solua.
3. Syötä **Dimensiot**-valintaikkunaan käytettävät suodattimet.
4. Napsauta **OK**.

### <a name="format-a-multiple-currency-report-in-a-column-definition"></a>Usean valuutan raportin muotoileminen sarakkeen määrityksessä

Usean valuutan raportti voi näyttää summat kirjanpidon kirjanpitovaluutassa, kirjanpidon raportointivaluutassa, alkuperäisen tapahtuman valuutassa tai muunnetussa raportointivaluutassa. Yrityksen kirjanpitovaluutta määritetään kirjanpidon asetuksissa. Älä sekoita tätä asetusta käyttöjärjestelmän järjestelmän alueellisiin asetuksiin, joissa määritetään raporteissa käytettävät oletusvaluutan symbolit. Seuraavat valuuttaan liittyvät solut ovat käytettävissä sarakkeen määrityksessä.

- **Valuutan näyttö** – määrittää, minkä tyypin valuutassa (kirjanpito, raportointi, tapahtuma tai muunnettu raportointi) tapahtumat näytetään. Raportointivaluuttaan muuntamistoimintoa kutsutaan joskus valuutan muuntamiseksi. Valuutan muunnon avulla kirjanpidon summat voidaan raportoida muussa kuin yrityksen perusvaluutassa tai raportointivaluutassa, jossa tapahtuma annettiin.
- **Valuuttasuodatin** – Määritä valuuttasuodatin. Vain valitussa valuutassa syötetyt tapahtumat näytetään raportissa.

> 
Seuraavien vaiheiden avulla voit määrittää yrityksen kirjanpitovaluutan.

1. Valitse raporttien suunnitteluohjelman **Yritys**-valikosta **Yritykset**.
2. Valitse **Yritykset**-valintaikkunassa yritys. Valitse sitten **Näytä**.
3. Voit tarkastella valitulle yritykselle määritettyä valuuttaa **Alueelliset asetukset** -kohdan **Näytä yritys** -valintaikkunassa.

#### <a name="specify-the-currency-on-a-multiple-currency-report"></a>Valuutan määrittäminen usean valuutan raportissa

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Kaksoisnapsauta soveltuvan **FD**-sarakkeen **Valuutan näyttö** -solua ja valitse valuutan tietojen näyttöasetukseksi **Kirjanpitovaluutta**, **Kirjanpidon raportointi**, tapahtumavaluutta tai valitse muunto toiseksi raportointivaluutaksi.
3. Kaksoisnapsauta soveltuvan **FD**-sarakkeen **Valuutan suodatin** -solua ja valitse luettelosta soveltuva valuuttakoodi. Vain tässä valuutassa syötetyt tapahtumat näytetään raportissa.


### <a name="example-for-currency-display-and-currency-filter-cells"></a>Valuutan näytön ja valuuttasuodattimen solujen esimerkkejä

Käyttäjä on tehnyt sarakkeen määrityksessä seuraavat valuuttavalinnat:

- **Valuuttasuodatin:** Jeni
- **Valuutan näyttö:** kirjanpitovaluutta kirjanpidosta (USA:n dollarit)

Valitusta valuuttasuodattimesta johtuen raportissa näkyvät vain tapahtumat, jotka on syötetty Japanin jeneinä (JPY). Valitusta valuutan näyttöasetuksesta johtuen tapahtumat näkyvät raportissa kirjanpitovaluutassa eli Yhdysvaltojen dollareina (USD).

#### <a name="currency-filter-and-currency-display-combinations"></a>Valuuttasuodattimen ja valuutan näytön yhdistelmät

Seuraavassa taulukossa näytetään tulokset, joita saadaan **Valuutan näyttö**- ja **Valuuttasuodatin**-solun erilaisilla yhdistelmillä tehtyjen valintojen kanssa. Perusvaluutta on Yhdysvaltojen dollari (USD).


| Valuutan näyttö -solu                        | Valuuttasuodatin-solu | Raportin tulos |
|----------------------------------------------|----------------------|---------------|
| Tapahtumavaluutta                 | **JENI**              | **6 000 Y** – Tuloksessa näytetään vain jeneinä syötetyt tapahtumat. |
| Kirjanpitovaluutta kirjanpidosta | **JENI**              |**60 $** – Tuloksessa näytetään vain jeneinä syötetyt tapahtumat, jotka näytetään Yhdysvaltojen dollareina.<p><strong>Huomautus:</strong> Muuntokurssina käytetään noin 100 jeniä yhtä Yhdysvaltojen dollaria kohti.</p> |
| Kirjanpitovaluutta kirjanpidosta | Tyhjä                | **2 310 $** – Tuloksessa näytetään kaikki tiedot kirjanpidossa määritetyssä kirjanpitovaluutassa.<p><strong>Huomautus:</strong> Tämä summa on kaikkien tapahtumien summa kirjanpitovaluutassa.</p> |
| Tapahtumavaluutta                 | Tyhjä                | **2 250 $** – Tuloksessa näytetään kaikki summat valuutassa, jossa tapahtuma suoritettiin. Tämä tarkoittaa sitä, että kokonaissummassa eri valuuttojen summat lasketaan yhteen. |

### <a name="calculation-column-in-a-column-definition"></a>Laskenta-sarake sarakkeen määrityksessä

Sarakkeen tyyppi **CALC** sarakemäärityksessä tukee monimutkaisia laskelmia **Kaava**-solussa ja siinä voi olla operaattorit **+**, **-**, **\**_, ja _*/** sekä lausekkeet **IF/THEN/ELSE**. Laskenta-sarake, voi myös viitata toiseen sarakkeeseen, myös seuraaviin sarakkeisiin. Laskelmasarake voi myös sisältää tilikauden ja jakson, jotka tukevat sarakkeen otsikoita. Laskentakaavan pituus voi olla enintään 1 024 merkkiä. Käytä erityistä muotoilun ohitusta, jos haluat esittää laskutoimituksen tuloksen prosenttilukuna.

> [!NOTE]
> Kaavojen laskemisen tulokset eivät sisällä arvoja tulostumattomista sarakealueista. Esimerkiksi **A:D** tulostaa **0** (nolla) -arvon, kun taas piilotettujen arvojen **A+B+C** tulostaa arvon.

#### <a name="operators-in-calculation-columns"></a>Laskentasarakkeiden operaattorit

Voit lisätä, vähentää, kertoa ja jakaa sarakkeita syöttämällä sarakkeiden kirjaimet laskentajärjestyksessä ja syöttämällä kirjainten väliin sopivan operaattorin. Seuraavassa taulukossa esitellään laskentasarakkeessa käytettävät operaattorit.

| Operaattori | Esimerkkilaskutoimitus | kuvaus |
|----------|---------------------|-------------|
| +        | A+C                 | Laske sarakkeen A ja sarakkeen C summa yhteen. |
| :        | A:C A:C-D           | Lisää peräkkäiset sarakkeet toisiinsa. Esimerkiksi kaava **A:C** laskee sarakkeiden A–C summat yhteen, kun taas kaava **A:C-D** laskee sarakkeiden A–C summat yhteen ja vähentää sitten sarakkeen D summan. |
| -        | A-C                 | Vähentää sarakkeen A arvosta sarakkeen C arvon.<p><strong>Huomautus:</strong> Voit myös käyttää miinusmerkkiä (-) sarakkeen etumerkin vaihtamiseen. Esimerkiksi <strong>-A+B</strong> lisää sarakkeen A käänteisen summan sarakkeen B summaan.</p> |
| \*       | A\*C                | Kerro sarakkeen A summa sarakkeen C summalla. |
| /        | A/C                 | Jaa sarakkeen A summa sarakkeen C summalla. |

#### <a name="use-a-calculation-formula-in-a-column-definition"></a>Laskentakaavan käyttäminen sarakkeen määrityksessä

1. Avaa Report Designer -ohjelmassa muokattava sarakkeen määritys.
2. Syötä kaava soveltuvaan **CALC**-sarakkeen **Kaava**-soluun.

#### <a name="complex-calculations"></a>Monimutkaiset laskutoimitukset

Monimutkainen laskutoimitus voi sisältää minkä tahansa solun viitteiden, operaattorien, arvojen ja sisäkkäisten sulkeiden tasojen yhdistelmän. Voit esimerkiksi laskea sarakkeiden A ja B keskiarvon käyttämällä laskentakaavaa **((A+B)/2)**.

#### <a name="specify-report-cells-in-a-column-calculation"></a>Raportin solujen määrittäminen sarakelaskelmassa

Voit viitata raportin tiettyyn soluun syöttämällä sarakkeen kirjaimen ja rivin koodi. Esimerkiksi **B.100** viittaa rivin koodiin 100 sarakkeessa B. Voit jakaa koko sarakkeen raportin samassa sarakkeessa olevan tietyn solun summalla. Esimerkiksi **B/B.100**-laskutoimitus tarkoittaa, että sarakkeen B summa tulee jakaa sarakkeen B rivin koodin 100 mukaisella summalla. Jos laskutoimitus viittaa toisesta sarakkeesta riippuvaan sarakkeeseen, riippuvainen sarake ratkaistaan ensin. Jos sarakkeeseen viitataan sarakkeessa, joka viittaa ensimmäiseen sarakkeeseen, tuloksena saadaan kehäviittausvirhe.

> [!NOTE]
> Tämä laskelma saattaa olla virheellinen, jos muokkaat raportin laskentaprioriteettia. Voit määrittää laskennan prioriteetin raportin määrityksen **Asetukset**-välilehdessä.

#### <a name="multiply-or-divide-a-column-by-a-base-row"></a>Sarakkeen kertominen tai jakaminen perusrivillä

Voit luoda sarakkeen, joka näyttää kaikki määritetyn sarakkeen arvot perusnumeron prosenttilukuna. Voit siis näyttää rivien väliset suhteet, kuten myyntirivin tai kokonaiskulujen rivin prosenttiosuuden. Voit kertoa tai jakaa kunkin rivin tietyllä perusrivin sarakkeella, kun syötät laskutoimituksessa käytettävän sarakkeen ja sitten **\*BASEROW**- tai **/BASEROW**-arvon. Syötä esimerkiksi **C\*BASEROW** tai **C/BASEROW**.

> [!NOTE]
> Kun käytät perusrivilaskentaa sarakemäärityksessä, varmista, että kaikilla tämän sarakemäärityksen kanssa käytettävillä rivimäärityksillä on ainakin yksi perusrivi laskentaa varten.

#### <a name="divide-the-amount-in-a-column-by-the-number-of-periods"></a>Sarakkeen summan jakaminen jaksojen määrällä

Voit jakaa sarakkeen summan määritetyllä jaksojen määrällä. Esimerkiksi **B/Jaksot**-kaava jakaa sarakkeen B arvon sarakkeen B jaksojen määrällä. Jos laskutoimitukseen otetaan mukaan useita sarakkeita, määritä jaksojen määrä, jota käytetään laskutoimituksessa. Esimerkiksi **(B+C)/Jaksot**-kaava laskee sarakkeen B ha C summat yhteen ja jakaa tuloksen jakson arvolla.

## <a name="additional-resources"></a>Lisäresurssit

[Talousraporttien suunnittelutoiminnon rivimääritykset](row-definitions-financial-reporting.md)

[Muotoilun lisäasetukset taloushallinnon raporteissa](advanced-formatting-options-financial-reporting.md)
