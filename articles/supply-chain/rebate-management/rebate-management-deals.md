---
title: Ostohyvitysten hallintasopimukset
description: Tässä ohjeaiheessa kerrotaan, miten luodaan ostohyvitysten hallintasopimukset. Sopimuksia käytetään eri menetelmien ja perusteiden hallintaan maksujen ja rojaltien laskemiseksi. Niihin sisältyy sisällyttämistä ja poissulkemista koskevia sääntöjä.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 76cdbf21cfbc0db7b363d0fbf60a1ecd0046efc1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689660"
---
# <a name="rebate-management-deals"></a>Ostohyvitysten hallintasopimukset

[!include [banner](../includes/banner.md)]

Ostohyvitysten hallintasopimuksia käytetään eri menetelmien ja perusteiden hallintaan maksujen ja rojaltien laskemiseksi. Niihin sisältyy sisällyttämistä ja poissulkemista koskevia sääntöjä. Ostohyvitysten hallintasopimuksia on kolmenlaisia: asiakashyvitykset, asiakasrojaltit ja toimittajahyvitykset. Kaikki kolme tyyppiä käyttävät samanlaisia asetuksia. Tässä aiheessa kuvataan erot siellä, missä niitä on.

## <a name="create-a-deal"></a>Sopimuksen luominen

1. Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Kaikki ostohyvityksen hallintasopimukset**. **Kaikki ostohyvityksen hallintasopimukset** -luettelosivulla voit luoda ja työstää kaikentyyppisiä sopimuksia.

    Tee vaihtoehtoisesti jokin seuraavista vaiheista. Kussakin tapauksessa näkyviin tulevalla luettelosivulla on kaikki samat asetukset kuin **Kaikki ostohyvityksen hallintasopimukset** -luettelosivulla, mutta se on suodatettu näyttämään vain yhden tyyppiset tarjoukset.

    - Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Asiakkaan ostohyvityssopimukset** luovat vain asiakkaan ostohyvityssopimuksia.
    - Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Asiakkaan rojaltisopimukset** luovat vain asiakkaan rojaltisopimuksia.
    - Siirry kohtaan **Ostohyvityksen hallinta \> Ostohyvityksen hallintasopimukset \> Toimittajan ostohyvityssopimukset** luovat vain toimittajan ostohyvityssopimuksia.

1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Luo uusi sopimus** -valintaikkunassa seuraavat kentät:

    - **Ostohyvityksen hallintasopimus** – Jos olet [määrittänyt numerosarjan](rebate-management-parameters.md) ostohyvitystarjouksia varten, tämän kentän arvoksi määritetään automaattisesti yksilöllinen järjestelmän luoma tunnus. Syötä muussa tapauksessa yksilöivä tunnus.
    - **Kuvaus** – anna sopimuksen kuvaus.
    - **Moduuli** – Valitse kumppanin tyyppi, jota sopimus koskee (*Asiakas* tai *Toimittaja*). Riippuen sivusta, jolta aloitit, tämä kenttä voidaan määrittää automaattisesti valitun sopimustyypin perusteella. Tässä tapauksessa kenttä on vain luku -tilassa.
    - **Tyyppi** – Valitse sopimuksen tyyppi (*Ostohyvitys* tai *Rojalti*). Riippuen sivusta, jolta aloitit, tämä kenttä voidaan määrittää automaattisesti valitun sopimustyypin perusteella. Tässä tapauksessa kenttä on vain luku -tilassa.
    - **Täsmäytä mennessä** – Valitse, miten sopimus lasketaan ja täsmäytetään:

        - *Sopimus* – Yksi hyvitys olisi käsiteltävä kaikkien sopimuksen hyvitysten ja vähennysten osalta.
        - *Rivi* – Hyvitykset tulee käsitellä kullekin sopimuksen riville.

    - **Kirjausprofiili** – Valitse [kirjausprofiili](rebate-management-posting.md), jota käytetään tapahtumissa, joissa sopimusta sovelletaan. Tämä kenttä on käytettävissä vain, jos **Täsmäytä mennessä** -kentän arvoksi on valittu *Sopimus*. Jos sen arvoksi on määritetty *Rivi*, määritä profiili myöhemmin jokaiselle sopimukseen lisättävälle riville.
    - **Takuun kirjausprofiili** – Valitse [kirjausprofiili](rebate-management-posting.md), jota käytetään takuutapahtumissa. Takuutapahtumiin tarvitaan kirjausprofiileja vain, jos takuu koskee rojaltia. Muussa tapauksessa, vaikka kirjausprofiili ei ole pakollinen, jos kirjausprofiilia ei määritetä, virhe näytetään, kun takuut kirjataan. Tämä kenttä on käytettävissä vain, jos **Tyyppi** -kentän arvoksi on valittu *Rojalti*. 
    - **Hyvityksen tulos** – Valitse, miten hyvitys tai rojalti maksetaan:

        - *Talous* – Luo vapaatekstihyvityslasku tai ostoreskontran veloituslasku, jotta rahat voidaan maksaa tai vastaanottaa myöhemmin. Huomaa, että varauksia **voidaan** käyttää hyvityksissä, jos tämä vaihtoehto on valittuna. Tämä vaihtoehto on ainoa asetus, jos **Tyyppi** -kentän arvoksi on valittu *Rojalti*.
        - *Nimike* – Luo nimikkeiden myyntitilaus sopimuksen asetusten mukaan. Tässä myyntitilauksen hintaan määritetään 0 (nolla) kullekin nimikkeelle. Huomaa, että varauksia **ei voida** käyttää hyvityksissä, jos tämä vaihtoehto on valittuna.

    - **Ostohyvityksen valuutta** – Valitse valuutta, jota käytetään, kun ostohyvitys, vähennys tai rojalti maksetaan.
    - **Asiakirjan huomautukset** – Syötä tarvittaessa sopimusta käsittelevät huomautukset.
    - **Kumulatiivinen takuu** – Voit määrittää tämän asetuksen arvoksi *Kyllä* vain, jos **Tyyppi**-kentän arvoksi on määritetty *Rojalti*. Tämä vaihtoehto vaikuttaa taattujen vähennysmaksujen laskentaan. Tässä on esimerkki:

        - Kaupan tae on myydä arvo, joka johtaa 10 000 dollarin maksuun vuosineljännestä kohti.
        - Tavaroita myyvä organisaatio myy arvon, joka aiheuttaa 12 000 dollarin vähennysmaksun 1. neljänneksessä. Tuloksena on maksettava 12 000 dollarin rojalti, josta on vähennetty takuu 10 000 dollaria.
        - Jos **kumulatiivisen takauksen** vaihtoehdoksi on määritetty *Kyllä*, 1. vuosineljänneksellä maksettujen 2 000 dollarin rojaltien lisämäärä koskee 2. vuosineljännestä. Siksi asiakkaalle taataan 8 000 dollaria (10 000 dollaria vähennettynä 2 000 dollarin lisämaksulla).
        - 2. vuosineljänneksellä rekisteröidään myynti, joka käynnistää 5 000 dollarin rojaltin.
        - Järjestelmä yksilöi 3 000 dollarin maksun (8 000 dollaria vähennettynä maksettujen 5 000 dollarin rojaltien määrällä).
        - Jos **Kumulatiivinen takuu** -asetuksena on *Ei*, koko 10 000 dollaria taataan kussakin neljännesvuodessa. Tämä takaus vastaa ehdotettua 5 000 dollarin maksua 2. vuosineljänneksellä (10 000 dollaria vähennettynä maksettujen 5 000 dollarin rojaltien määrällä).

1. Valitse **OK** luodaksesi sopimuksen ja sulje valintaikkuna.

Tämä toimintosarja luo uuden sopimuksen otsikkotason. Seuraavaksi lisäät rivit sopimukseen.

## <a name="add-lines-to-a-deal"></a>Rivien lisääminen sopimukseen

Kun olet luonut sopimuksen edellisessä osassa kuvatulla tavalla, voit avata sen luettelosivulta. Tämän jälkeen voit lisätä rivejä, jotka yksilöivät sopimuksen asiakkaat tai toimittajat, nimikkeet, aikataulut, perusteen ja laskentamenetelmät. Sopimuksella voi olla yksi tai useita rivejä. Jos sopimuksessa on useita rivejä, ne ovat yleensä samantyyppisiä tai niihin liittyy samoja parametreja. Ennen kuin lisäät rivejä sopimukseen, sopimus ei tee mitään.

1. Avaa asianmukainen ostohyvityssopimusten luettelosivu edellisessä osassa kuvatulla tavalla.
1. Etsi ja avaa sopimus, jonka kanssa haluat työskennellä.
1. Lisää sopimuksen rivi ruudukkoon valitsemalla **Ostohyvityksen hallinta** -pikavälilehdessä jokin seuraavista painikkeista:

    - **Lisää rivi** – Lisää uusi tyhjä sopimusrivi.
    - **Kopioi rivi** – Jos olemassa oleva sopimusrivi muistuttaa lisättävää sopimusriviä, voit kopioida siitä kopion valitsemalla tämän painikkeen. Uusi sopimusrivi sisältää kaikki siihen liittyvien ostohyvityksen hallintatietojen asetukset. Voit sitten muokata asetuksia. Päivität esimerkiksi yleensä nimikesuhteen ja ostohyvitysprosentin.

1. Määritä seuraavat kentät uudella sopimusrivillä:

    - **Ostohyvityksen hallintanumero** – Jos olet [määrittänyt numerosarjan](rebate-management-parameters.md) ostohyvitysten hallintanumeroita varten, tämän kentän arvoksi määritetään automaattisesti yksilöllinen järjestelmän luoma tunnus. Syötä muussa tapauksessa yksilöivä tunnus.
    - **Tyyppi** – sopimuksen tyyppi, jota rivi koskee (*Ostohyvitys* tai *Rojalti*). Arvo kopioidaan otsikosta, eikä sitä voi muuttaa.
    - **Kuvaus** – anna sopimusrivin kuvaus.
    - **Yritys** – Valitse yritys (oikeushenkilö), jota sopimusrivi koskee. Käsittelyn aikana käyttäjät voivat käsitellä vain parhaillaan käytössä olevalle yritykselle määritettyjä sopimusrivejä. **Asiakkaan ostohyvityssopimukset** -luettelosivu sisältää usean yrityksen näkymän, joka perustuu käyttäjän suojaustasoon. Voit kuitenkin muokata ja käsitellä ostohyvitystä vain yrityksessä, jota parhaillaan käytät.
    - **Tilikoodi** – Valitse niiden asiakkaiden tai toimittajien käyttöalue, joita sopimusrivi koskee:

        - *Taulu* – sopimusrivi koskee tiettyä asiakasta tai toimittajaa.
        - *Ryhmä* – sopimusrivi koskee asiakas- tai toimittajaryhmää. Lisätietoja ryhmien määrityksestä on kohdassa [Ostohyvitysten hallintaryhmät](rebate-management-groups.md).
        - *Kaikki* – sopimusrivi koskee kaikkia asiakkaita tai toimittajia.

    - **Tilin suhde** – Jos olet valinnut *Taulu* tai **Tilikoodi**-kentässä, valitse asiakas tai toimittaja, jota sopimus koskee. Jos valitsit *Ryhmä*-vaihtoehdon, valitse asiakas- tai toimittajaryhmä. Jos valitsit *Kaikki*, tämä kenttä ei ole käytettävissä.
    - **Nimikekoodi** – Valitse niiden nimikkeiden käyttöalue, joita sopimusrivi koskee:

        - *Taulu* – sopimusrivi koskee tiettyä nimikettä.
        - *Ryhmä* – sopimusrivi koskee nimikeryhmää. Lisätietoja ryhmien määrityksestä on kohdassa [Ostohyvitysten hallintaryhmät](rebate-management-groups.md).
        - *Kaikki* – sopimusrivi koskee kaikkia nimikkeitä.

    - **Nimikkeen suhde** – Jos olet valinnut *Taulu* tai **Nimikekoodi**-kentässä, valitse nimike, jota sopimusrivi koskee. Jos valitsit *Ryhmä*-vaihtoehdon, valitse nimikeryhmä. Jos valitsit *Kaikki*, tämä kenttä ei ole käytettävissä.
    - **Yksikkötyyppi** – Valitse yksikkötyyppi, jota käytetään sopimusrivillä (*Varastoyksikkö* tai *todellisen painon yksikkö*). Huomaa, että tämä kenttä voi olla tyhjä vanhempia tietueita varten. Tässä tapauksessa käytetään *varastoyksikön* arvoa.
    - **(Varastonhallinnan parametrit)** – Määritä sopimusrivin jäljellä olevien kenttien varastonhallinnan parametreille arvot, joita käytetään sopimukseen sisältyvien nimikkeiden määrittämiseen (kuten nimikkeen koko, väri, tyyli, toimipaikka ja varasto). Voit lisätä dimensioita tai poistaa niitä valitsemalla toimintoruudusta **Näytä dimensiot**.

1. Valitse toimintoruudussa **Tallenna**.
1. Jos haluat rajoittaa edelleen sopimusrivin nimikkeiden joukkoa, valitse rivi ja valitse sitten **Ostohyvityksen hallinta** -pikavälilehdestä **Suodata** avataksesi **Kysely**-vakiovalintaikkunan.
1. Määritä jokaiselle lisättävälle sopimusriville **Ostohyvityksen hallinnan tiedot** -pikavälilehden laskentatiedot ja muut tiedot seuraavassa osassa kuvatulla tavalla.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Ostohyvitysten hallinnan tietojen lisääminen sopimusriviin

Jokaiselle sopimuksen riville on määritettävä tiedot **Ostohyvityksen hallinnan tiedot** -pikavälilehdessä. Valitse ensin sopimusrivi **Ostohyvityksen hallinta** -pikavälilehdestä. Määritä sitten arvot kyseiselle sopimusriville käyttäen **Ostohyvitysten hallinnan tiedot** -pikavälilehden eri välilehtiä. Seuraavissa aliosissa kuvataan, kuinka kutakin välilehteä käytetään.

### <a name="settings-on-the-general-tab"></a>Yleiset-välilehden asetukset

**Ostohyvitysten hallinnan tiedot** -pikavälilehden **Yleiset**-välilehdessä voit määrittää laskentatavan ja -perusteen valitulle sopimuksen riville. Nämä asetukset ohjaavat sitä, tarvitaanko vähimmäisostoa, sopimusriviin liittyviä kirjausprofiileja ja laskelman tietoja. Seuraavassa taulukossa näkyvät valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Laskentatapa | Valitse menetelmä, jota käytetään, kun valittu sopimusrivi yhdistetään muihin sopimusriveihin (*Vaiheittainen*, *Kumulatiivinen*, *Juokseva* tai *Yhteensä*). Tämän kentän arvo voi vaikuttaa merkittävästi ostohyvityslaskelmien tulokseen. Kunkin menetelmän täydellinen kuvaus sekä esimerkkejä, jotka osoittavat, miten se vaikuttaa ostohyvityksen laskentaan, on jäljempänä tässä ohjeaiheessa kohdassa [Sopimusrivien laskentamenetelmät](#calc-methods). |
| Peruste | Valitse, käytetäänkö ostohyvitystä määrän perusteella (eli ostettujen tai myytyjen yksiköiden kokonaismäärän) vai arvon (eli ostettujen tai myytyjen tuotteiden kokonaishinnan) perusteella. |
| Tapahtumatyyppi | <p>Valitse prosessin piste, jossa laskenta suoritetaan:</p><ul><li>*Tilaus* – Käytä laskelman pohjana tilattua määrää tai arvoa.</li><li>*Toimitettu* – Käytä laskelman pohjana toimitettua määrää tai arvoa.</li><li>*Lasku* – Käytä laskelman pohjana laskutettua määrää tai arvoa.</li></ul> |
| Yksikkö | Jos valitsit **Peruste**-kentästä *Määrä*, valitse yksikkö, jossa määrä on määritettävä. |
| Pienin summa | Määritä kausikohtainen vähimmäissumma, joka on maksettava. Voit määrittää negatiivisen arvon, jos haluat sallia negatiiviset ostohyvityssummat, jos hyvityslaskut ylittävät kauden myynnin. |
| Ostohyvityksen vähentämisperiaate | Valitse sopimusriviä koskeva [ostohyvityksen vähentämisperiaate](rebate-reduction-principle.md). |
| Muuttujan numero | Jos sopimusrivi koskee nimikettä, jolla on variantteja, valitse variantti, jota sopimusrivi koskee. |
| Toimittajan ostohyvityksen peruste | <p>Tämä kenttä näkyy vain toimittajien ostohyvitysten yhteydessä (koskee sopimuksia, joissa **Moduuli**-kentän arvo on *Toimittaja*). Valitse toimittajan hyvityksen peruste:</p><ul><li>*Ostotilaus* – Ostohyvitys, jonka toimittaja saa, perustuu ostotilauksen määrään tai arvoon.</li><li>*Myyntitilaus* – Toimittaja saa ostohyvityksen vasta, kun tavarat on myyty. Ostohyvitys perustuu myyntitilauksen määrään tai arvoon.</li></ul> |
| Hintaperuste | <p>Tämä kenttä näkyy vain toimittajien ostohyvitysten yhteydessä (sopimukset, joissa **Moduuli**-kentän arvo on *Toimittaja*). Jos valitsit **Toimittajan ostohyvityksen peruste** -kentästä *Myyntitilaus*, valitse sovellettava hintaperuste:</p><ul><li><p>*FIFO* – Kausittainen **Laske FIFO-ostohinta** -tehtävä on suoritettava, jotta ostohyvitys voidaan laskea. (Jos haluat suorittaa tehtävän, siirry kohteeseen **Ostohyvitysten hallinta \> Kausittaiset tehtävät \> Laske FIFO-ostohinta**.) FIFO-säännön avulla lasketaan myydyn varaston arvo. Tämän jälkeen käytetään tätä arvoa toimittajien ostohyvitysten laskemiseen. Tässä on esimerkki:</p><ul><li>**Myyty varasto:** 1 000 yksikköä, kukin 3,00 dollaria = 3 000 dollaria</li><li>**Nykyinen ostohinta, joka perustuu FIFO:on:** 2,00 dollaria</li><li>**Käyttölaskelma:** *Myydyt yksiköt* × *Nykyinen ostohinta* = 1 000 × 2,00 $= 2 000 $</li></ul></li><li><p>*Viimeisin ostohinta* – Toimittajan ostohyvitysten laskennassa käytetään viimeisen ostotapahtuman arvoa. Tässä on esimerkki:</p><ul><li>**Myyty varasto:** 1 000 yksikköä, kukin 3,00 dollaria = 3 000 dollaria</li><li>**Edellinen ostohinta:** 2,00 $</li><li>**Käyttölaskelma:** *Myydyt yksiköt* × *Edellinen ostohinta* = 1 000 × 2,00 $= 2 000 $</li></ul></li><li><p>*Keskimääräinen ostohinta* – Toimittajan ostohyvitykset lasketaan viime *X* kuukauden painotetulla keskiarvolla. Jos valitset tämän vaihtoehdon, kuukausien määrä on kirjoitettava **Kuukausien määrä** -kenttään (joka on käytettävissä vain, kun **Hintaperuste**-kentän arvoksi on määritetty *Keskimääräinen ostohinta*). Tässä on esimerkki:</p><ul><li>**Myyty varasto:** 1 000 yksikköä, kukin 3,00 dollaria = 3 000 dollaria</li><li>**Keskimääräinen ostohinta:** 2,00 $</li><li>**Käyttölaskelma:** *Myydyt yksiköt* × *Keskimääräinen ostohinta* = 1 000 × 2,00 $= 2 000 $</li></ul></li><li><p>*Myyntihinta* – Myyntihintaa käytetään toimittajan ostohyvitysten laskemiseen. Tässä on esimerkki:</p><ul><li>**Myyty varasto:** 1 000 yksikköä, kukin 3,00 dollaria = 3 000 dollaria</li><li>**Keskimääräinen ostohinta:** 2,00 $</li><li>**Käyttölaskelma:** *Myydyt yksiköt* × *myyntihinta* = 1 000 × 3,00 $= 3 000 $</li></ul></li></ul> |
| Kuukausien määrä | Tämä kenttä näkyy vain toimittajien ostohyvitysten yhteydessä (sopimukset, joissa **Moduuli**-kentän arvo on *Toimittaja*). Jos valitsit *Keskimääräinen ostohinta* **Hintaperuste**-kentässä, kirjoita käytettävä kuukausien määrä. |
| Kirjausprofiili | Valitse [kirjausprofiili](rebate-management-posting.md), joka koskee sopimusriviä. Tätä profiilia käytetään vain, kun sopimuksen otsikon **Täsmäytä mennessä** -kentässä on arvo *Rivi*. Jos **Täsmäytä mennessä** -kentän arvoksi määritetään *Sopimus*, sopimuksen otsikkoon määritettyä kirjausprofiilia käytetään aina. Jos kirjausprofiilia ei ole määritetty sopimusrivillä, sopimuksen otsikkoon määritettyä kirjausprofiilia käytetään. |
| Takuun kirjausprofiili | Tämä kenttä toimii kuten **Kirjausprofiili**-kenttä, mutta sitä käytetään vain rojalteille. |
| Maksutyyppi | Sopimukselle valitun kirjausprofiilin maksutyyppi. |
| Arvonlisävero, sisältyy | Valitse, sisältääkö tapahtuma veron. Veron sisältyminen on oleellista vain, kun **Peruste**-kentän arvoksi on määritetty *Arvo*. Laskun summaa käytetään veron sisältävänä summana. Jos ostohyvitys lasketaan prosenttiosuuden perusteella, järjestelmä kertoo ostohyvitysprosentin veron sisältävällä summalla. Huomaa, että laskelmassa käytetään sopimusrivin arvonlisäveroarvoa. |
| Sisällytä hyvityslaskut | <p>Valitse tämän vaihtoehden arvoksi *Kyllä*, jos haluat, että hyvityslaskut sisällytetään ostohyvityksen laskentaan.</p><p>Jos määrität tämän asetuksen arvoksi **Kyllä**, vaikutus vaihtelee *Tapahtumatyyppi*-kentän arvon mukaan:</p><ul><li>Jos **Tapahtumatyyppi**-kentän arvoksi on määritetty *Lasku*, laskutoimitus ottaa huomioon hyvityslaskut. Tämä konfiguraatio on tavallinen konfiguraatio.</li><li>Jos **Tapahtumatyyppi**-kentän arvoksi määritetään *Tilaus*, laskenta otta huomioon sekä myyntitilaukset, joissa on negatiivisia arvoja että avoimet palautetut tilaukset.</li></ul> |
| Alennettu summa | Valitse tähän vaihtoehtoon *Kyllä*, jos haluat käyttää laskelman pohjana nimikkeen tai nimikkeiden alennettua summaa, jos annetaan sopimusrivialennuksia. |
| Vain maksetut laskut | Valitse tähän vaihtoehtoon *Kyllä*, jos laskennassa tulisi ottaa huomioon vain kokonaan maksetut laskut. (Ostohyvitystä ei siis lasketa osittain maksetuille laskuille.) Tämä vaihtoehto on käytettävissä vain, kun **Tapahtumatyyppi**-kentän arvoksi on määritetty *Lasku*. |
| Sisällytä vapaatekstilaskut | Valitse tämän vaihtoehden arvoksi *Kyllä*, jos haluat, että vapaatekstilaskut sisällytetään laskentaan. Vapaatekstilaskuja voi sisällyttää vain sopimusriveihin, joissa **Nimikekoodi**-kentän arvoksi on määritetty *Kaikki*. |
| Sisällytä tilitysalennus | Määritä tähän vaihtoehtoon *Kyllä*, jos haluat vähentää ostohyvitystä ensimmäisellä tilitysalennuksella. Oletetaan, että organisaatio ottaa ensimmäisen tilitysalennuksen. Valitse tähän vaihtoehtoon *Ei*, jos haluat ottaa tilitysalennuksen käyttöön myöhemmin. |
| Tiedoston huomautukset | Kirjoita huomautukset, joita käytetään ostohyvitystapahtuman kirjauskansion rivien tapahtumatekstinä. |

### <a name="settings-on-the-dates-tab"></a>Päivämäärät-välilehden asetukset

**Ostohyvityksen hallinnan tiedot** -pikavälilehden **Päivämäärät**-välilehden asetukset määrittävät **Yleiset**-välilehdessä määritettyjen laskentojen tiheyden ja ajoituksen. Ne määrittävät, miten laskelmat suoritetaan käsittelyn aikana.

Tässä välilehdessä voit määrittää päivämääräalueen, joille valittu sopimusrivi on voimassa, sekä laskentatiheyden. Voit myös määrittää, kirjataanko takuu ja milloin.

Voit lisätä päivämäärärivejä ruudukkoon tai poistaa niitä ruudukosta työkalurivin painikkeilla. Jos olemassa on useita päivämäärärivejä, voimassaolon päivämäärävälit eivät saa olla päällekkäisiä. Muutoin saat virhesanoman, kun yrität tallentaa sopimuksen.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin päivämäärärivin osalta.

| Kenttä | kuvaus |
|---|---|
| Päivämäärästä | Kirjoita ensimmäinen päivämäärä, jolloin päivämäärärivi on voimassa. Jos sopimuksen otsikkoon määritetään päivämäärästä- ja päivämäärään-arvot, niitä käytetään jokaisen uuden päivämäärärivin oletusarvoina. |
| Päivämäärään | Kirjoita viimeinen päivämäärä, jolloin päivämäärärivi on voimassa. Jos sopimuksen otsikkoon määritetään päivämäärästä- ja päivämäärään-arvot, niitä käytetään jokaisen uuden päivämäärärivin oletusarvoina. |
| Per | Määritä, kuinka usein sopimusrivi lasketaan. Kirjoita tähän kokonaisluku ja valitse yksikkö **Kumuloi välein** -kentästä. Jos esimerkiksi haluat laskea joka toinen viikko, määritä **Per**-kentän arvoksi *2* ja **Kumuloi välein** -kentän arvoksi *Viikot*. |
| Kumuloi välein | Valitse yksikkö, jota käytetään **Per**-asetuksessa. Valitse *Elinkaari*, jos haluat laskea sopimusrivin koko elinkaaren. Valitse *Mukautettu kausi* valitaksesi kirjanpidossa määritetyn kauden. Tässä tapauksessa **Kauden tyyppi** -kenttä on myös määritettävä. |
| Kauden tyyppi | Tämä kenttä on käytettävissä vain, jos **Kumuloi välein** -kentän arvoksi on valittu *Mukautettu kausi*. Valittavissa olevat arvot tulevat kirjanpidossa määritetyistä kausityypeistä. |
| Viikon ensimmäinen päivä | Määritä, miten viikot määritetään kaudelle. Tämä kenttä on käytettävissä vain, jos **Kumuloi välein** -kentän arvoksi on valittu *Viikot*. |
| Vaadi per | Määritä, miten usein sopimusrivin ostohyvityssummat voidaan vaatia. Kirjoita tähän kokonaisluku ja valitse yksikkö **Vaadi välein** -kentästä. |
| Vaadi välein | Valitse yksikkö, jota käytetään **Vaadi per**-asetuksessa. Valitse *Elinkaari*, jos haluat sallia vaatimukset vain kerran sopimusrivin koko elinkaaren ajalla Valitse *Mukautettu kausi* valitaksesi kirjanpidossa määritetyn kauden. Tässä tapauksessa **Vaatimuskauden tyyppi** -kenttä on myös määritettävä. |
| Vaatimuskauden tyyppi | Tämä kenttä on käytettävissä vain, jos **Vaadi välein** -kentän arvoksi on valittu *Mukautettu kausi*. Valittavissa olevat arvot tulevat kirjanpidossa määritetyistä kausityypeistä. |
| Kirjausprosessi | Valitse tämä valintaruutu, jos vaatimusrivi tulee käsitellä kirjaushetkellä. Tämä vaihtoehto on käytettävissä vain sopimusriveillä, joissa **Yleiset**-välilehden **Tapahtumatyyppi**-kentän arvoksi on määritetty *Toimitettu* tai *Lasku*. Varausten osalta varaus kirjataan, kun toimitusilmoitus tai -lasku luodaan. |
| Takuu per | Tämä kenttä koskee vain rojaltisopimuksia. Määritä, miten usein rojaltin takuu on laskettava **Kumuloi välein** -asetuksen määrittämänä ajanjaksona. Kirjoita tähän kokonaisluku ja valitse maksuaika **Takuu maksettu** -kentästä. |
| Takuu maksettu | <p>Tämä kenttä koskee vain rojaltisopimuksia. Se määrittää yhdessä **Takuu per** -kentän kanssa takuun laskennan tiheyden. Valitse jokin seuraavista:</p><ul><li><p>*Kauden alku* – Takuu maksetaan päivämäärärivillä määritetyn sopimuskauden alussa. Täysi takuu käsitellään ensin. Vain takuusumman ylittävien rojaltien arvo kirjataan rojaltina. Tässä on esimerkki:</p><ul><li>**Vähimmäistakuu:** 10 000 $ kahden kuukauden aikana.</li><li>**Kuukausi 1:** 10 000 $ kirjattiin takuuna ja kirjattiin 0 $ rojalteina.</li><li>**Kuukausi 2:** 2 000 $ kirjattiin rojalteihin ja kirjattiin 0 $ takuita.</li><li>**Käyttölaskelma:** *Jäljellä oleva takuu* – *Kirjatut rojaltit* = 0 $ – 2 000 $ = -2 000 $.</li></ul><p>Koska rojaltin maksu on 2 000 $ vaaditaan, kirjauskansio luodaan summalle 2 000 $.</p><p>**Huomautus:** Takuu on laskettava ja kirjattava yhdessä ensimmäisen kauden vähennysten varauksen kanssa.</p></li><li><p>*Kauden loppu* – Takuuta ei makseta ennen vähennyssopimuksen loppua, joka on määritetty päivämäärärivillä. Tässä on esimerkki:</p><ul><li>**Vähimmäistakuu:** 10 000 $ kahden kuukauden aikana.</li><li>**Kuukausi 1:** 5 000 $ kirjattiin rojaltina, ja kirjauskansio luotiin.</li><li>**Kuukausi 2:** 7 000 $ kirjattiin rojaltina, ja kirjauskansio luotiin.</li><li>**Käyttölaskelma:** Koska royalit ylittävät takuusumman, 0 $ kirjataan takuuseen.</li></ul><p>**Huomautus:** Takuu on laskettava ja kirjattava vain yhdessä viimeisen kauden vähennysten ja ostohyvitysten kanssa.</p></li></ul> |
| Takuun vähimmäisarvo | Tämä kenttä koskee vain rojaltisopimuksia. Kirjoita rojaltin takuun vähimmäissumma sen valuutan mukaisesti, joka on määritetty sopimuksen otsikossa. |

### <a name="settings-on-the-lines-tab"></a>Rivit-välilehden asetukset

**Ostohyvitysten hallinnan tiedot** -pikavälilehden **Rivit**-välilehdessä voit määrittää laskentarivit valitulle sopimuksen riville. Jokaisella laskentarivillä on määritetty määrän tai arvon raja sekä liittyvä kompensaatiosumma tai -nimikkeet. **Yleiset**-välilehden **Peruste**-kentässä määritetään, perustuvatko kukin laskentarivi määrään vai arvoon.

Voit lisätä laskentarivejä ruudukkoon tai poistaa niitä ruudukosta työkalurivin painikkeilla. Laskentarivejä voi olla miten monta tahansa. Jos laskentarivejä on useita, niiden määrä- ja arvovälit eivät saa mennä päällekkäin.

Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kunkin laskentarivin osalta.

| Kenttä | kuvaus |
|---|---|
| Määrästä/arvosta | Kirjoita pienin määrä tai arvo, jota laskentarivi koskee. |
| Määrään/arvoon | Kirjoita suurin määrä tai arvo, jota laskentarivi koskee. |
| Ostohyvitysten hallintamenetelmä | <p>Tämä kenttä on käytettävissä vain sopimuksissa, joissa otsikon **Ostohyvityksen tulos** -kentän arvoksi on määritetty *Rahoitus*. Valitse ostohyvityksen laskemiseen käytettävä menetelmä:</p><ul><li>*Kiinteä* – Rivillä käytetään kiinteää hintasummaa.</li><li>*Prosentti* – Käytetään myyntisumman prosenttiosuutta.</li><li>*Hinta* – Käytetään kiinteää tilauskohtaista hintaa.</li></ul><p>**Tärkeää:** On suositeltavaa käyttää samaa menetelmää jokaiselle **Rivit**-välilehden laskentariville. Luo uusi sopimusrivi, jos uutta menetelmää tarvitaan. Muista, että **Ostohyvityksen hallinta** -pikavälilehden **Kopioi rivi** -painikkeella voit luoda uuden sopimusrivin aiemmin luodusta sopimusrivistä.</p><p>**Huomautus:** Jos **Ostohyvityksen tulos** -kentän arvoksi määritetään *Nimike*, tämän kentän arvoksi on aina määritetty *Kiinteä*. Lisätietoja nimikkeiden määrityksestä on tätä taulukkoa seuraavassa tekstissä. |
| Ostohyvitysten hallinnan summa | Tämä kenttä on käytettävissä vain sopimuksissa, joissa otsikon **Ostohyvityksen tulos** -arvoksi on määritetty *Rahoitus*. Kirjoita summa, jota käytetään ostohyvityksen laskemiseen. Summa perustuu **Ostohyvityksen hallintamenetelmä** -kentässä valittuun menetelmään. |

Kuten edellisessä taulukossa mainitaan, sopimuksille, joissa otsikon **Ostohyvityksen tulos** -kentän arvoksi on määritetty *Nimike*, on määritettävä nimikkeet, joita käytetään **Rivit**-välilehden jokaiselle laskentariville. Voit määrittää nimikkeet noudattamalla seuraavia vaiheita.

1. Luo **Rivit**-välilehdessä pakollinen laskentarivi, jos sitä ei ole, ja valitse se.
1. Jos tarjousta ei ole tallennettu laskentarivin luomisen jälkeen, valitse **Tallenna** toimintoruudussa.
1. Valitse **Rivit**-välilehdessä **Nimikkeet**.
1. Lisää nimikkeitä ruudukkoon tai poista nimikkeitä tarpeen mukaan **Nimikkeet**-sivun toimintoruudukon painikkeiden avulla. Määritä kullekin riville seuraavat kentät:

    - **Nimiketunnus** – Valitse annettu nimike.
    - **(Muut dimensiot)** – Jos tarvitset useampia dimensioita (esimerkiksi nimikkeen konfiguraatio, koko, väri, tyyli, toimipaikka tai varasto) nimikkeen määrittämiseen, määritä ne. Voit lisätä käytettäviä dimensioita tai poistaa niitä valitsemalla toimintoruudusta **Näytä dimensiot**.
    - **Määrä** – Syötä määrä, jota käytetään valitun laskentarivin raja-arvon jälkeen.
    - **Yksikkö** – Valitse yksikkö, jossa **Määrä**-arvo on määritetty.
    - **Kerrannainen** – Tämä kenttä toimii yhdessä **Määrä**-kentän kanssa. Voit esimerkiksi määrittää nimikerivillä **Määrä**-kentän arvoksi *2* ja **Kerrannainen**-kentän arvoksi *100*. Jos myyntitilauksen kokonaismäärä on 150, nimikkeistä on kaksi maksutonta (kaksi per 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Varastodimensiot-välilehden asetukset

**Ostohyvityksen hallinnan tiedot** -pikavälilehden **Varastodimensiot**-välilehdessä näkyvät kaikki valitulle sopimusriville määritetyn tuotteen käytettävissä olevat dimensioarvot. Se sisältää dimensiot, jotka eivät näy **Ostohyvityksen hallinta** -pikavälilehdessä. Voit muokata arvoja vain valittuun tuotteeseen käytettäville dimensioille.

**Ostohyvityksen hallinta** -pikavälilehden ruudukkoon voi lisätä dimensioita valitsemalla toimintoruudusta **Näytä dimensiot**.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Sopimusrivien laskentamenetelmät

Aina, kun määrität yhden sopimusrivin tiedot edellisessä osassa kuvatulla tavalla, sinun on valittava riville laskentatapa. Tässä osassa kuvataan kutakin laskentatapaa ja esitetään esimerkkejä, jotka osoittavat, miten kunkin menetelmän tilausten ja sopimusrivien kokonaishyvitys lasketaan. Näissä esimerkeissä tilaukset ja sopimusrivit ovat identtiset. Vain laskentamenetelmät ovat erilaiset.

### <a name="stepped-calculation-method"></a>Vaiheittainen laskentatapa

Vaiheittainen laskentamenetelmä laskee vaiheittaisesti, missä kukin sopimusrivi vaikuttaa ostohyvitykseen asteittain, kunnes myyntimäärä tai -arvo saavutetaan. Vaiheet voivat perustua myytyjen tuotteiden määrään tai arvoon. Tämä määräytyy **Ostohyvityksen hallinnan tiedot** -pikavälilehden **Yleiset**-välilehden **Peruste**-kentän asetuksen mukaan.

Esimerkiksi sopimusrivi on määritetty niin, että **Laskentamenetelmä**-kentän arvoksi määritetään *Vaiheittainen* ja **Peruste**-kentän arvoksi on määritetty *Arvo*. Siihen sisältyvät laskentarivit, joista saadaan seuraavat ostohyvitykset:

- **Rivi A:** 10 prosenttia 1 000 $ asti
- **Rivi B:** 25 prosenttia 2 500 $ asti

Jos ostetun tai myydyn tavaran arvo on 2 000 $, ostohyvityksen tulos 350 $ lasketaan seuraavasti:

- **Ostohyvitys (A):** *Raja (A)* × *Prosentti (A)* = 1 000 $ × 10 prosenttia = 100 $
- **Ostohyvitys (B):** (*Myyty arvo* – *Raja (A)*) × *Prosentti (B)* = (2 000 $ – 1 000 $) × 25 prosenttia = 250 $
- **Kokonaishyvitys:** *Ostohyvitys (A)* + *Ostohyvitys (B)* = 100 $ + 250 $= 350 $

Jos **Peruste**-kentän arvoksi määritetään *Määrä* (ei *Arvo*), vaiheittainen laskentamenetelmä toimii samalla tavalla. Ensimmäistä vaihetta käytetään määritettynä määränä, kunnes toinen vaihe on saavutettu. Toista vaihetta käytetään sitten kaikkiin määriin ensimmäisen vaiheen jälkeen, kunnes kolmas vaihe on saavutettu. Tämän jälkeen prosessi jatkuu kaikkien seuraavien vaiheiden läpi.

### <a name="cumulative-calculation-method"></a>Kumulatiivinen laskentamenetelmä

Kumulatiivisessa laskentamenetelmässä käytetään vain yhtä laskentariviä ostohyvityksen laskemiseen. Jos sopimusrivillä on käytettävissä useita laskentarivejä, saavutettua suurimman arvon tai suurimman määrän laskentariviä käytetään koko määränä tai arvona. Muiden laskentamenetelmien tapaan kumulatiivinen menetelmä määrittää ostohyvitysten laskennassa käytetyn myyntimäärän tai myyntiarvon **Ostohyvityksen hallinnan tiedot** -välilehden **Yleiset**-välilehden **Peruste**-kentän asetuksen avulla.

Esimerkiksi sopimusrivi on määritetty niin, että **Laskentamenetelmä**-kentän arvoksi määritetään *Kumulatiivinen* ja **Peruste**-kentän arvoksi on määritetty *Arvo*. Siihen sisältyvät laskentarivit, joista saadaan seuraavat ostohyvitykset:

- **Rivi A:** 10 prosenttia 1 000 $ asti
- **Rivi B:** 25 prosenttia 2 500 $ asti

Jos ostetun tai myydyn tavaran arvo on 2 000 $, laskenta käyttää vain riviä B. Oostohyvityksen tulos 500 $ lasketaan seuraavasti:

- **Kokonaishyvitys:** *Myyty arvo* × *Hyvitys (B)* = 2 000 $ × 25 prosenttia = 500 $

### <a name="rolling-calculation-method"></a>Juokseva laskentatapa

Juokseva laskentamenetelmä laskee kaikki mahdolliset sopimuksen laskentarivit. Jos laskentarivejä on useita ja niistä on saavutettu useita, käytetään kaikkia saavutettuja laskentarivejä, mutta kutakin prosenttiosuutta koskevat ylemmät raja-arvot. Muiden laskentamenetelmien tapaan juokseva menetelmä määrittää ostohyvitysten laskennassa käytetyn myyntimäärän tai myyntiarvon **Ostohyvityksen hallinnan tiedot** -välilehden **Yleiset**-välilehden **Peruste**-kentän asetuksen avulla.

Esimerkiksi sopimusrivi on määritetty niin, että **Laskentamenetelmä**-kentän arvoksi määritetään *Juokseva* ja **Peruste**-kentän arvoksi on määritetty *Arvo*. Siihen sisältyvät laskentarivit, joista saadaan seuraavat ostohyvitykset:

- **Rivi A:** 10 prosenttia 1 000 $ asti
- **Rivi B:** 25 prosenttia 2 500 $ asti

Jos ostetun tai myydyn tavaran arvo on 2 000 $, ostohyvityksen tulos 600 $ lasketaan seuraavasti:

- **Ostohyvitys (A):** *Raja (A)* × *Prosentti (A)* = 1 000 $ × 10 prosenttia = 100 $
- **Ostohyvitys (B):** *Myyty arvo* × *Prosentti (B)* = 2 000 $ × 25 prosenttia = 500 $
- **Kokonaishyvitys:** *Ostohyvitys (A)* + *Ostohyvitys (B)* = 100 $ + 500 $= 600 $

### <a name="total-calculation-method"></a>Yhteensä-laskentatapa

Yhteensä-laskentamenetelmässä käytetään kaikkia laskentarivejä ostohyvityksen laskemiseen. Se käyttää kokonaismäärää jokaisen saavutetun laskentarivin ostohyvityksen laskemiseen, ja jokainen laskentarivi soveltaa prosenttiosuuttaan koko summaan. Muiden laskentamenetelmien tapaan Yhteensä-menetelmä määrittää ostohyvitysten laskennassa käytetyn myyntimäärän tai myyntiarvon **Ostohyvityksen hallinnan tiedot** -välilehden **Yleiset**-välilehden **Peruste**-kentän asetuksen avulla.

Esimerkiksi sopimusrivi on määritetty niin, että **Laskentamenetelmä**-kentän arvoksi määritetään *Yhteensä* ja **Peruste**-kentän arvoksi on määritetty *Arvo*. Siihen sisältyvät laskentarivit, joista saadaan seuraavat ostohyvitykset:

- **Rivi A:** 10 prosenttia 1 000 $ asti
- **Rivi B:** 25 prosenttia 2 500 $ asti

Jos ostetun tai myydyn tavaran arvo on 2 000 $, ostohyvityksen tulos 700 $ lasketaan seuraavasti:

- **Ostohyvitys (A):** *Myyty arvo* × *Prosentti (A)* = 2 000 $ × 10 prosenttia = 200 $
- **Ostohyvitys (B):** *Myyty arvo* × *Prosentti (B)* = 2 000 $ × 25 prosenttia = 500 $
- **Kokonaishyvitys:** *Ostohyvitys (A)* + *Ostohyvitys (B)* = 200 $ + 500 $= 700 $
