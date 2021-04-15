---
title: Omaisuuden leasingin aloittaminen
description: Tässä ohjeaiheessa käsitellään ominaisuuden leasingominaisuutta sekä opastetaan omaisuuden vuokrasopimuksen luomisessa ja kyseisten sopimusten tietojen näyttämisessä.
author: moaamer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6d5b51e89ec0e64182671872573ec0140939a836
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814125"
---
# <a name="asset-leasing-get-started"></a>Omaisuuden leasingin aloittaminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään ominaisuuden leasingominaisuutta sekä opastetaan omaisuuden vuokrasopimuksen luomisessa ja kyseisten sopimusten tietojen näyttämisessä. Ohjeaiheessa myös määritellään käyttöliittymässä ja ohjeissa käytetyt termit. Omaisuuden leasing on lisäominaisuus, jolla hallitaan, seurataan ja automatisoidaan vuokratun omaisuuden rahoitustapahtumia Microsoft Dynamics 365 Financessa. Omaisuuden leasing noudattaa kansainvälisiä kirjanpitostandardeja (IFRS 16) ja US GAAP -standardeja (ASC 842). Omaisuuden leasing tallentaa ja käsittelee tärkeimmät vuokrasopimuksia koskevat tiedot ja auttaa luomaan kirjauskansiovientejä koko leasingsopimuksen elinkaaren ajan alkukirjaamisesta, ja kuukausittaisista kirjauskansiovienneistä arvonalennukseen ja leasingsopimuksen päättymiseen. Omaisuuden leasing integroituu saumattomasti Dynamics 365 Financen komponentteihin, mukaan lukien käyttöomaisuuseriin, ostoreskontraan ja kirjanpitoon.

Lisätietoja tilinpäätösstandardeista on IFRS 16- ja US GAAP ASC 842 -standardien ohjeissa.

## <a name="asset-leasing-elements"></a>Käyttöomaisuuden leasing-elementit
Seuraavassa kaaviossa on vuokrasopimusten liiketoimintaprosessin tärkeimmät elementit.

[![Käyttöomaisuuden leasing-elementit](./media/overview-01.png)](./media/overview-01.png)

Vuokratun omaisuuden pääkomponentit:

- **Vuokrasopimus** – Vuokralle antaja omistaa omaisuuden ja sopii vuokralle ottajan kanssa omaisuuden vuokraamisesta tietyksi ajaksi säännöllistä vuokraa vastaan. Vuokralle antajan ja vuokralle ottajan välisen oikeudellisen sopimuksen lisäksi vuokrasopimus sisältää hallintaa koskevat päätökset, kuten todennäköisyyden uusimisoption käyttämisestä ja omistuksen siirtämisestä.

- **Vuokran laskenta ja luokittelu kirjanpitostandardin mukaisesti** – Vuokran laskenta ja luokittelu määrittävät kirjanpitostandardin, jota käytetään alkuperäisessä ja myöhemmässä arvostamisessa, sekä luokittelutestin, joka määrittää vuokrasopimustyypin. Vuokrasopimus voi olla rahoitusleasingsopimus, käyttöleasingsopimus, lyhytaikainen vuokrasopimus tai arvoltaan vähäinen vuokrasopimus. Järjestelmä laskee myös tulevien vähimmäisvuokrien nykynettoarvon arvostusta ja luokittelua varten.

- **Vuokratapahtumat** – Omaisuuden leasing tukee leasingsopimusten käyttöoikeusomaisuuserän alkukirjaamista taseessa sekä myöhempää arvostusta joko taseen leasingsopimuksissa tai taseen ulkopuolisissa leasingsopimuksissa. Alkuperäinen kirjaamistapahtuma arvostaa tulevien vähimmäisvuokrien nykynettoarvon. Näiden tietojen avulla määritetään alkuperäinen käyttöoikeusomaisuuserä ja vuokrasopimusvelka, jotka vaikuttavat organisaation taseeseen. Myöhemmät kuukausittaisten vuokratapahtumien arvostus sisältää vuokrasopimusvelan koron kertymisen, mikä nostaa vuokrasopimusvelkaa. Se myös arvostaa vuokrasopimusvelkaa vähentävien vuokrien kertymisen, joka tullaan maksamaan vuokralle antajalle. Arvostus sisältää lisäksi käyttöoikeusomaisuuserän kuoletuksen.

  Taseen ulkopuolisissa vuokrasopimuksissa järjestelmä laskee vuokrakulun suoraan sen mukaan, kumpi on pienempi: omaisuuden taloudellinen kokonaisvaikutusaika tai vuokra-aika. Vuokran oikaisut arvostavat sopimuksen muokkaukset, kuten vuokrasopimuksen laajentamisen tai pidentämisen, sekä arvonalennustapahtuman, joka käyttää käyttöoikeusomaisuuseriä ei-takaisinsaatavina kustannuksina.

  Koska omaisuuden leasing integroituu kirjanpitoon voidaan varmistaa, kaikki kirjattavat vuokratapahtumat päivittävät tilikartan. Omaisuuden leasing integroituu ostoreskontraan, jolloin vuokralle antajan laskuja voidaan seurata ostoreskontrassa ja tulevat maksut voidaan ottaa sieltä. Integroituminen käyttöomaisuuserien kanssa antaa mahdollisuuden seurata vuokrasopimuksia käyttöomaisuuserien rekisterissä ja kirjata käyttöoikeusomaisuuserien tapahtumat, kuten omaisuuden alkuperäisen kirjaamisen, poiston ja arvonalennuksen, käyttöomaisuuseristä.   

## <a name="asset-leasing-components"></a>Omaisuuden leasingin komponentit 
Omaisuuden leasing tekee vuokrasopimuksen tietojen, maksusuunnitelmien, alkamis- ja päättymispäivien sekä maksun toistuvuuden yhdistämismääritykset. Se myös automatisoi nykynettoarvon, kuukausittaisten vuokrien, koron ja vuokrasopimuksen kuoletuksen laskutoimitukset. Järjestelmä suorittaa vuokrasopimuksen luokittelutestit määrityksen mukaan. Järjestelmä myös luo ja kirjaa vastaavat vuokratapahtumat, jotka perustuvat noudatettavan kirjanpitostandardin määrittämään järjestelmään.

Seuraavassa kaaviossa on vuokrasopimuskirja, vuokrasopimus, laskettu maksusuunnitelma, vuokrasopimusten ja vuokrasopimuskirjojen luokittelutestit sekä vastaavat kirjanpitotapahtumat.

[![Leasing, vuokrasopimuskirja ja maksusuunnitelma](./media/overview-02.png)](./media/overview-02.png)

- **Vuokrasopimuskirja** – Vuokrasopimuskirja sisältää kaikki vuokrasopimuksen tiedot, kuten vuorka-ajan, käyvän arvon ja vuokrat. Se sisältää myös käytettävän kirjanpitostandarding, vuokrasopimustyypin ja raja-arvot, jotka otetaan huomioon vuokrasopimuksen luokittelutestissä. Vuokrasopimuskirja sisältää myös vuokratapahtumat, jotka kirjataan kirjanpitoon. 
  
- **Vuokrasopimus** – Vuokrasopimus sisältää omaisuuden leasingtiedot, joihin omaisuuden leasing perustuu, leasingtietojen lähteenä on vuokrasopimus ja hallintapäätös, jotka molemmat tehdöön Dynamics 365 Financen ulkopuolella. Omaisuuden käypä arvo on hinta, joka omaisuudesta transaktiossa maksettaisiin arvostuspäivänä. Tämä arvo voi määräytyä omaisuuden tyypin, markkinatilanteen ja muiden ehtojen perusteella, jotka voidaan ottaa arvioinnissa huomioon. Omaisuuden käypä arvo otetaan huomioon luokittelutestiyhtälössä.

- **Omaisuuden käyttöikä** – Tämä ilmaisee omaisuuden käyttöiän jäljellä olevat kaudet vuokrasopimuksen alkamispäivästä alkaen. Omaisuuden käyttöikä otetaan huomioon luokittelutestiyhtälössä. Se ei ole sama kuin käyttöomaisuuserissä määritetty käyttöikä.

- **Inkrementaalinen lainakorko** – Tätä korkoprosenttia käytetään nykyisen nettoarvon laskemiseen. Järjestelmä käyttää vuokrien nykyisen nettoarvon laskemiseen laskennallista korkoa, jos se on määritetty vuokrasopimuksen tiedoissa. Jos laskennallista korkoa ei ole määritetty, järjestelmä käyttää inkrementaalista lainakorkoa.

- **Annuiteettityyppi** – Tämä tarkoittaa sitä, että vuokra erääntyy joko maksukauden alussa tai sen lopussa. Se voi olla ennakkomaksu tai erääntyvä annuiteetti (vuokrakauden alussa) tai tavallinen annuiteetti (vuokrakauden lopussa).

  Ensimmäinen kuukauden kausinumeroksi katsotaan ennakomaksussa nolla; ensimmäinen kuukausi katsotaan olevan kausi 1 jälkimaksuissa.

- **Yhdistämisväli** – Tämä ilmaisee, kuinka moneksi jaksoksi korko yhdistetään vuosittain. Se voidaan tehdä kuukausittain (12 jaksoa vuodessa), neljännesvuosittain (4 jaksoa vuodessa), puolivuosittain (2 jaksoa vuodessa) tai vuosittain (1 jakso vuodessa). Jaksojen määrä otetaan huomioon nykyistä nettoarvoa laskettaessa.

- **Alkamispäivä** – Tämä on päivämäärä, jolloin vuokralle antaja antaa omaisuuden vuokralle ottajan käyttöön. Kaikki vuokrasopimuksen laskelmat ja tapahtumat perustuvat alkamispäivään. Alkamispäivän on syytä olla jakson alussa (kuukauden ensimmäinen päivä), sillä niin voidaan varmistaa, että myöhemmin tehtävät laskelmat ovat tarkkoja. Sopimuksen varsinaisen allekirjoituspäivämäärän voi antaa **Sopimuksen allekirjoituksen päivämäärä** -kenttään.

- **Vuokra-aika** - Tämä ilmaisee vuokrajakson pituuden kuukausina.

> [!NOTE] 
> Vuokra-ajan määritelmä perustuu kausien tai aikavälien määrään maksusuunnitelman riveillä. Aikavälien määritetty määrä muunnetaan kuukausiksi.

- **Maksusuunnitelman rivi** – Riville tallennetaan kausikohtaiset vuokrat. Siinä määritetään myös, käytetäänkö uusimiskautta ja sisällytetäänkö se käyttöoikeusomaisuuserän ja vuokrasopimusvelan alkuperäiseen arvostukseen. Voit määrittää erääntyvien vuokrien alkamispäivän ja kausivälit, jotka ilmaisevat vuokrasopimuksen pituuden päivinä, kuukausina tai vuosina.

- **Maksun toistuvuus** – Tämä ilmaisee, onko maksu kuukausittainen, neljännesvuosittainen, puolivuosittainen vai vuosittainen. Päättymispäivä lasketaan automaattisesti alkamispäivän ja annettujen kausien määrän määrän perusteella.

- **Maksusuunnitelma** – tämä ilmaisee lasketun nykynettoarvon, joka perustuu vuokrien kattamaan aikaan, maksujen summaan, yhdistämisjaksoihin ja annuiteettityyppiin.

- **Kaudet** – Nämä vuokrasopimuskaudet vastaavat sisäistä yhdistämistä ja annuiteettityyppiä. Yhdistämisväli määrittää, miten kaudet jaetaan. Voit määrittää seuraavat yhdistämisvälit:

  - Kuukausittain, 12 kautta vuodessa
  - Neljännesvuosittain, 4 kautta vuodessa
  - Puolivuosittain, 2 kautta vuodessa
  - Vuosittain, 1 kausi vuodessa

Ensimmäisen kauden alussa on kausi nolla, jos annuiteetin tyyppi on erääntyvä annuiteetti. Muussa tapauksessa ensimmäisen kausisi on yksi, annuiteetin tyyppi on jälkimaksu.

- **Kuukaudet** – Tämä ilmaisee, kuinka monta kalenterikuukautta vuokrasopimuksen aikana on. Maksusumma on maksun toistuvuudessa määritetty maksettava summa. Valmiiksi laskettu nettoarvo on nykyiseen nettoarvoon perustuva kausikohtainen vuokra, yhdistämisvälit ja inkrementaalinen lainakorko.

> [!NOTE] 
> Nykyinen nettoarvo lasketaan diskontatun kassavirtayhtälön perusteella.

- **Kirjat** – Tämä on esimääritetty asetus, joka liitetään kuhunkin vuokrasopimukseen. Kirja määritettää käytettävän kirjanpitostandardin, vuokrasopimustyyppit ja raja-arvon, jota käytetään luokittelutestien perusteena. Luokittelutestien avulla vuokrasopimustyyppi voidaan määrittää automaattisesti.

- **Kirjanpitojärjestelmä** – Tämä näyttää valitun, tuetun kirjanpitostandardin, joka on joko IFRS 16 tai ASC 842. Kirjanpitostandardi määritetään vuokrasopimukseen liitetyssä kirjassa. Kirjanpitostandardi määrittää kirjausprofiilissa määritettävät kirjanpitotilit.

- **Vuokrasopimustyypit** – Tämä ilmaisee kumpaa vuokrasopimustyyppiä käytetetään: rajoitusleasingsopimusta vai käyttöleasingsopimusta. Rahoitusleasingsopimuksessa vuokrattuun omaisuuteen liittyvät riskit ja palkkiot siirretään vuokralle ottajalle. Käyttöleasingsopimuksessa vuokrattuun omaisuuteen liittyvät riskit ja palkkiot jäävät vuokralle antajalle. Kolmas vaihtoehto on vuokrasopimustyypin automaattinen tunnistaminen joko rahoitus- tai käyttöleasingsopimuksessa kirjassa määritettyjen raja-arvojen perusteella. Tämä automaattinen tunnistus suoritetaan vuokrasopimuksen uudelleenluokittelutestin aikana.

- **Raja-arvot** – Tämän avulla vuokrasopimuksen luokittelutesteissä voidaan selvittää, onko omaisuus luokiteltu joksikin seuraavista:

  - **Vuokra-aika** – Tätä käyttöiän prosenttiosuutta käytetään luokittelutestissä. Järjestelmä luokittelee vuokrasopimuksen rahoitusleasingsopimukseksi, jos vuokrasopimustyyppi on määritetty automaattiseksi ja jos omaisuuden käyttöikää koskeva vuokra-aika on suurempi tai yhtä suuri kuin tässä määritetty prosenttisosuus.

  - **Nykyinen nettoarvo** – Tätä omaisuuden käyvän arvon prosenttiosuutta käytetään luokittelutestissä. Järjestelmä luokittelee vuokrasopimuksen rahoitusleasingsopimukseksi, jos tulevien vuokrien nykyinen nettoarvo omaisuuden käyvän arvon osalta on suurempi tai yhtä suuri kuin tässä määritetty prosenttisosuus.

  - **Lyhytaikainen vuokrasopimus** – jos vuokra-aika on pienempi tai yhtä suurin kuin määritetty arvo, vuokrasopimus luokitellaan lyhytaikaisesti vuokrasopimukseksi.

  - **Arvoltaan vähäinen** – jos omaisuuden käypä arvo on pienempi tai yhtä suurin kuin määritetty arvo, vuokrasopimus luokitellaan arvoltaan vähäiseksi vuokrasopimukseksi.

  - **Vuokrasopimuksen luokittelu ja tapahtumat** – Vuokrasopimuken luokittelu on automaattinen prosessi, jolla luokitellaan vuokrasopimuksia käyttämällä kirjoissa määritettyjä raja-arvoja muiden luokittelutestin ehtojen lisäksi. Tällä tavoin tunnistetaan, onko vuokrasopimus rahoitusleasingsopimus, käyttöleasingsopimus, lyhytaikainen vuokrasopimus tai arvoltaan vähäinen vuokrasopimus. Tämän avulla määritetään myös, onko toteutumaton vuokraprosessi käytössä.

Luokittelutestejä ovat esimerkiksi omistajuuden siirto, ostovaihtoehto, vuokra-aika, nykyinen nettoarvo ja ainutlaatuinen omaisuus. Seuraava kaavio selventää vuokrasopimuksen luokittelutestejä.

[![Vuokrasopimuksen luokittelutestit](./media/overview-03.png)](./media/overview-03.png)

Kukin vuokrasopimustyyppi käsittelee kirjanpitoa eri tavoin eri vuokratapahtumien osalta. Tapahtumat sisältävät alkuperäisen kirjaamisen, korkokulut, erääntyvät vuokrat ja vuokrapoistot, ja ne perustuvat käytössä olevaan kirjanpitostandardiin (IFRS 16 tai ASC 842). Kirjanpitotilit määritetään vuokrasopimuksen kirjausprofiilissa kummallekin tapahtumatyypille ja kirjanpitojärjestelmälle.

## <a name="asset-leasing-transactions"></a>Omaisuuden leasingtapahtumat

#### <a name="initial-recognition"></a>Alkuperäinen tunnustaminen 
Vuokratun omaisuuden alkuperäisessä kirjaamisessa käytetään laskettua nykyistä nettoarvoa, jotta se voidaan ilmoittaa taseessa. Tämän kirjanpitomerkintä luodaan automaattisesti. Tämä tapahtuma vähennetään käyttöoikeusomaisuuserätililä ja lisätään käyttöleasingsopimuksen velkatilille seuraavasti. Jos käyttöoimaisuus on liitetty vuokrasopimukseen, alkuperäinen kirjausvienti ilmaistaan käyttöomaisuuden hankintana. Tässä skenaariossa käyttöomaisuuden kirjausprofiili on määritettävä kirjaamaan käyttöoikeusomaisuustilille. 

> [!NOTE]
> Vain US GAAP ASC 842 tukee käyttöleasingsopimuksia.

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Käyttöleasingsopimus US GAAP -järjestelmässä            |     Käyttöoikeusomaisuuserä        |     Käyttöleasingsopimusvelka     |
|     Rahoitusleasingsopimus IFRS- ja US GAAP -järjestelmissä      |     Käyttöoikeusomaisuuserä        |     Rahoituksen vuokrasopimusvelka       |

#### <a name="lease-liability-amortization-interest-expense"></a>Vuokrasopimusvelan kuoletus (korkokulut) 
Korko huomioidaan vuokrasopimuksessa laskemalla korko vuokrasopimuksen alkusaldolle, kauden vuokra, lainakorko ja yhdistämisvälien kaudet vuodessa. Korkosumma kasvattaa käyttöleasingsopimuksen velkatiliä, sillä se lisätään siihen, mikä näkyy myös organisaation taseessa. Tapahtuma sisältä myös debet-merkinnän korkokulutilille, mikä näkyy rajoitusleasingsopimusten tuloslaskelmassa, ja vuokrasopimuksen kulutille käyttöleasingsopimuksissa.

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Käyttöleasingsopimusvelan vienti US GAAP ASC 842 -järjestelmässä    |     Vuokran kulu         |     Käyttöleasingsopimusvelka         |
|     Rahoitusleasingsopimusvelan vienti IFRS- ja US GAAP -järjestelmissä      |     Korkokustannus          |     Rahoituksen vuokrasopimusvelka           |

#### <a name="accrued-lease-payment"></a>Jaksotetut vuokrat
Jaksotettu vuokra kirjataan vuokrasopimuksen tulevana maksuna, joka on määrä käsitellä maksutapahtumana pankki- tai käteistililtä. Erääntyvä vuokra pienentää vuokravelkaa vähentämällä vuokraveltatiliä toimittajan alareskontrassa, jos vuokralle antaja on määritetty toimittajana, tai kirjaamalla kredit-puolen velkavekselien kirjanpitotilille, jolloin maksu suoritetaan joko toimittajalta tai velkavekseleistä.

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Käyttöleasingsopimus US GAAP -järjestelmässä              |  Käyttöleasingsopimusvelka    |   Toimittajan velka (alareskontra) / velkavekselit  |
|     Rahoitusleasingsopimus IFRS- ja US GAAP -järjestelmissä        |  Rahoituksen vuokrasopimusvelka      |   Toimittajan velka (alareskontra) / velkavekselit  |

#### <a name="asset-depreciation"></a>Omaisuuden poisto
Käyttöoikeusomaisuuserä poistetaan sen mukaan, kumpi on pienempi: omaisuuden käyttöikä tai vuokra-aika. US GAAP -käyttöleasingsopimuksen (ASC 842) poiston laskentamenetelmä perustuu suoran vuokrakulun ja korkosumman eroon. Rahoitusleasingsopimuksen poisto lasketaan käyttämällä suoraa vakiomenetelmää. Vuokrapoisto vaikuttaa debet-puolen korkokulujen tuloslaskelmaan. Rahoitusleasingsopimusten kumulatiivisen käyttöoikeusomaisuuserätilin lisääminen credit-puolelle vaikuttaa taseeseen. Jos vuokrasopimus on linkitetty käyttöomaisuuserään, poistotapahtumat suoritetaan vain käyttöomaisuusmoduulista. 

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Käyttöleasingsopimus US GAAP -järjestelmässä              |  Vuokran kulu                |   Käyttöoikeusomaisuuserän kumulatiivinen poisto     |
|     Rahoitusleasingsopimus IFRS- ja US GAAP -järjestelmissä        |   Käyttöoikeusomaisuuserän kulun poisto   |   Käyttöoikeusomaisuuserän kumulatiivinen poisto    |

#### <a name="short-term-lease"></a>Lyhytaikainen vuokra
Lyhytaikainen vuokrasopimus kirjataan kuluksi, joka vaikuttaa organisaation tuloslaskelmaan. Luotu erääntyvä vuokra vähennetään vuokrakulutililtä ja lisätään velkavekseli- tai toimittajan alareskontratilin kredit-puolelle.

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Lyhytaikaisen vuokrasopimuksen vienti IFRS- ja US GAAP -järjestelmissä     |  Vuokran kulu                |   Toimittajan velka (alareskontra) / velkavekselit  |

#### <a name="low-value-lease"></a>Arvoltaan vähäinen vuokrasopimus
Arvoltaan vuokrasopimus kirjataan kuluksi, joka vaikuttaa organisaation tuloslaskelmaan. Luotu erääntyvä vuokra vähennetään vuokrakulutililtä ja lisätään velkavekselin tai toimittajan alareskontran kredit-puolelle.

|     Laji                                          |     Veloitus                     |     Luotto                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Arvoltaan vähäisen vuokrasopimuksen vienti IFRS- ja US GAAP -järjestelmissä      |  Vuokran kulu                |   Toimittajan velka (alareskontra) / velkavekselit  |


#### <a name="index-revaluation"></a>Indeksin uudelleenarviointi
Tämä on muuttuvien vuokrien omaisuuden leasingtili indeksikoron mukaan arvostettuna. Indeksikoron vaihtelujen aiheuttamat muutokset vuokrissa katsotaan IFRS 16 -järjestelmässä vuokran oikaisuksi. Vuokravelka ja käyttöoikeusomaisuuserä oikaistaan tilille uusia maksuja varten. 

|     Laji                                          |     Veloitus                             |     Luotto                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Indeksin uudelleenarvostusvienti IFRS-järjestelmässä nousun yhteydessä  |  Käyttöoikeusomaisuuserä       |   Käyttöleasingsopimusvelka |
|   Indeksin uudelleenarvostusvienti IFRS-järjestelmässä laskun yhteydessä  |  Käyttöleasingsopimusvelka  |   Käyttöoikeusomaisuuserä      |

Jos maksu muuttuu indeksikoron muutoksen vuoksi, vain muuttuvat maksut muuttuvat ellei kassavirrassa ole muita muutoksia, kuten korkoprosentteihin liittyvä vuokra-aikojen muutos US GAAP ASC 842 -järjestelmässä.

#### <a name="lease-adjustment"></a>Vuokran muutos
Omaisuuden leasingissä vuokrasopimuksia voidaan oikaista, jos vuokra-aikaa muokataan, vuokrasopimusta pidennetään ja on jotain muita syitä, joiden vuoksi vuokrasopimus on oikaistava. Vuokrasopimuksen oikaisut kirjataan suurentamaan tai pienentämään käyttöoikeusomaisuuserää ja vuokravelkaa. Oikaisuprosessi käyttää siirrettyjä velan kuoletuksen ja omaisuuden saldon loppusaldoja oikaisupäivänä. Jos vuokrasopimus on linkitetty käyttöomaisuuteen, käyttöoikeusomaisuuserän oikaisu kirjataan käyttämällä käyttöomaisuudessa määritettyä tunnusta. 

|     Laji                                          |     Veloitus                             |     Luotto                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Vuokran oikaisuvienti IFRS- ja US GAAP -järjestelmissä nousun yhteydessä     |  Käyttöoikeusomaisuuserä       |   Käyttöleasingsopimusvelka |
|   Vuokran oikaisuvienti IFRS- ja US GAAP -järjestelmissä laskun yhteydessä     |  Käyttöleasingsopimusvelka  |   Käyttöoikeusomaisuuserä      |


#### <a name="lease-impairment"></a>Vuokrasopimuksen arvonalennus
Tämä ilmaisee käyttöoikeusomaisuuserän merkitsee saldon pienentämisen siirtämistä. Arvonalennus summan, tapahtumapäivän ja jäljellä olevien kausien määrittäminen. Jäljelle jäävä käyttöoikeusomaisuuserä kuoletetaan tasapoistoina. Vuokrasopimuksen arvonalentumislogiikka ottaa huomioon omaisuuden poistosuunnitelmassa olevan omaisuuden siirtoarvon.  

|     Laji                                          |     Veloitus                             |     Luotto                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Arvonalennus IFRS- ja US GAAP -järjestelmässä           |  Arvonalennuksen kulu                   |    Käyttöoikeusomaisuuserä     |

>[!NOTE]
> Jos vuokrasopimus on linkitetty kättöomaisuuteen, vuokrasopimuksen arvonalennus on kirjattava käyttöomaisuuseristä, sillä omaisuuden poisto suoritetaan käyttöomaisuusmoduulista.

**Kaksoisvaluutta** Vuokratapahtumat voidaan kirjata jonain muuna valuuttana kuin kirjanpito- ja raportointivaluuttana. Valuutan vaihtokurssi määritetään kirjanpidossa alkamispäivänä. Valuuttakursseja voidaan vaihtaa määrittämällä **Kiinteä kurssi** -kentän asetukseksi **Kyllä** vuokrasopimusta luotaessa. Kun vuokratapahtumat viedään, alkuperäinen kirjaaminen ja myöhemmät poistotapahtumat käyttävät alkamispäivän vaihtokurssia. Myöhemmät maksu- ja korkotpaahtumat käyttävät nykyistä aktiivista vaihtokurssia. 

## <a name="create-an-asset-lease"></a>Omaisuuden vuokrasopimuksen luominen
Luo uusi vuokrasopimus seuraavien ohjeiden mukaan. 

1. **Omaisuuuden leasing** -ominaisuuden käyttö edellyttää, että se otetaan käyttöön **Ominaisuuden hallinta** -työtilassa. Valitse **Ominaisuuden hallinta** -työtilassa **Kaikki**, jolloin kaikki ominaisuudet mainitaan sivulla. Valitse ensin **Omaisuuden leasing** ja sitten **Ota käyttöön nyt**.
2. Valitse **Omaisuuden leasing > Yleinen > Vuokrasopimuksen yhteenveto**. Anna pakollisten kenttien tiedot **Yleiset**-pikavälilehdessä. 
   - **Vuokran tiedot**
   - **Resurssin käyttöikä (kuukautta)**
   - **Vuokraryhmä**
   - **Inkrementaalinen lainakorko (%)**
   - **Yhdistämisväli**
   - **Annuiteetin tyyppi**
   - **Valuutta**
   - **Aloituspäivämäärä**

3. Siirry **Maksusuunnitelman rivit** -pikavälilehti, lisää maksurivi ja valitse sitten **Luo aikataulut**.

4. Valitse **Kirjat**. 

5. Siirry **Yleiset**-pikavälilehteen. **Ensimmäinen käyttöoikeusomaisuuserä** ja **vuokravelka** lasketaan. 

6. Siirry **Vuokrasopimuksen luokittelutesti** -pikavälilehti ja tarkista **Vuokrasopimustyyppi**-kentän arvo. 

   **Vuokrasopimuksen tyyppi** -luokitellaan automaattisesti **Kirjat**-sivulla määritettyjen ehtojen perusteella.

7.  Valitse **Maksusuunnitelma** **Toiminto**-osassa.  

   **Maksusuunnitelma**-sivulla on vuokrasopimuksen tunnuksen mukainen luettelo tulevista maksusuunnitelmista. Valitsemalla **Vahvista aikataulu** voit kirjata **Alkuperäinen kirjaus** -tapahtumat. 

[![Alkuperäinen kirjaus -toiminto](./media/overview-13.png)](./media/overview-13.png)

8. Luo alkuperäisen kirjauksen kirjauskansio valitsemalla **Alkuperäinen kirjaus**. 

9. Kirjaa alkuperäinen kirjaustapahtuma valitsemallat **Omaisuuden leasingkirjauskansiot**. 

   Voit avata maksusuunnitelmasta sivun, jossa luettelo käyttöoikeusomaisuuserän tapahtumista. 
 
   **Vuokravelan kuoletussuunnitelma** sisältää kullekin kaudelle lasketun korkosumman.
   
10. Luo kirjauskansio ja valitse **Omaisuuden leasingkirjauskansiot**. **Vuokravelan kuoletussuunnitelma** sisältää myös korkotapahtumat.

   Valitun vuokrasopimustunnuksen poistotapahtumat näkyvät **Omaisuuden poistosuunnitelma** -sivulla. 

   [![Käyttöoikeusomaisuuserän tapahtumat -sivu](./media/overview-20.png)](./media/overview-20.png)

   Alkuperäinen kirjaus, kumuloituntu poisto ja omaisuuden saldo näkyvät **Käyttöoikeusomaisuuserän tapahtumat** -sivulla. 

   Alkuperäinen kirjaus, vuokran korko, vuokra ja vuokravelan saldo näkyvät **Vuokravelan tapahtumat** -sivulla. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
