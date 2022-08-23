---
title: Sähköisten sanomien määrittäminen
description: Tässä artikkelissa on tietoja sähköisten sanomien (EM) ominaisuuden määrittämisestä.
author: AdamTrukawka
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 12beb1adbfa4e2f235c8a7c69e786d342c4a4f68
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279299"
---
# <a name="set-up-electronic-messages"></a>Sähköisten sanomien määrittäminen

[!include [banner](../includes/banner.md)]

**Sähköiset sanomat** (EM) -ominaisuus auttaa sinua ylläpitämään erillisiä sähköisiä raportointiprosesseja eri asiakirjatyypeille. Joissakin monimutkaisissa skenaarioissa, jotka tukevat [maakohtaisia raportointiominaisuuksia](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality), EM-ominaisuuden määritys koostuu monien sanomien tilojen, sanomien nimikkeiden tilojen, toimintojen, lisäkenttien ja suoritettavien luokkien yhdistelmästä. Näissä skenaarioissa käytettävissä on tuotavia tietoyksikköpaketteja. Jos käytät näitä tietoyksikköpaketteja, tuo ne yritykseen tietojen hallintatyökalulla. Lisätietoja tietojen hallintatyökalun käytöstä on kohdassa [Tiedonhallinta](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Jos et tuo tietoyksikköpakettia, voit määrittää EM-ominaisuuden manuaalisesti. Siinä tapauksessa seuraavat elementit on määritettävä:

- [Numerosarjat](#sequences)
- [Sanoman nimiketyypit](#types)
- [Sanoman nimikkeiden tilat](#item)
- [Sanomien tilat](#statuses)
- [Lisäkentät](#additional)
- [Suoritettavan luokan asetukset](#executable)
- [Tietueiden täyttötoiminnot](#populate)
- [Tietueiden täyttäminen useista yrityksistä](#multiple-companies-populate)
- [Verkkosovellukset](#applications)
- [Verkkopalvelun asetukset](#settings)
- [Sanoman käsittelytoiminnot](#actions)
- [Sähköisen sanoman käsittely](#processing)

Seuraavissa osissa on lisätietoja jokaisesta edellä mainitusta elementistä.

## <a name="number-sequences"></a><a id="sequences"></a>Numerosarjat

Määritä sekä sanomien että sanoman nimikkeiden numerosarjat. Sen jälkeen sanomat ja sanomien nimikkeet numeroidaan automaattisesti numerosarjojen avulla. Määritettyjä numeroita käytetään järjestelmässä sanomien ja sanomien nimikkeiden yksilöivinä tunnisteina. Voit määrittää sähköisten sanomien numerosarjat kohdasta **Kirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**.

## <a name="message-item-types"></a><a id="types"></a>Sanoman nimiketyypit

Sanomien nimikkeiden tyypit ilmaisevat sähköisissä sanomissa käytettävät tietuetyypit. Voit määrittää sanomien nimikkeiden tyypit kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanoman nimiketyypit**.

## <a name="message-item-statuses"></a><a id="item"></a>Sanoman nimikkeiden tilat

Sanomien nimikkeiden tiloilla ilmaistaan sanomien nimikkeissä käytettävät tilat käsittelyssä, jota olet määrittämässä. Voit määrittää sanomien nimikkeiden tilat kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanoman nimikkeiden tilat**.

Sanoman nimikkeen tilan **Salli poistaminen** -parametri määrittää, voitko poistaa sanomien nimikkeitä, joilla on tämä tila **Sähköiset sanomat**- tai **Sähköisen sanoman nimikkeet** -sivulla.

## <a name="message-statuses"></a><a id="statuses"></a>Sanomien tilat

Määritä sanomien tilat, joiden on oltava käytettävissä sanomien käsittelyssä. Voit määrittää sanomien tilat kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanomien tilat**.

Seuraavassa taulukossa käsitellään **Sanomien tilat**-sivun kenttiä.

| Kentän nimi          | Kuvaus |
|---------------------|-------------|
| Sanoman tila      | Anna sanoman tilan yksilöivä nimi. Sanomien tilojen avulla kuvaillaan sähköisen sanoman tilaa koko ajan. Annettu nimi näkyy **Sähköiset sanomat** -sivulla ja sähköisiin sanomiin liittyvässä lokissa. |
| Kuvaus         | Anna sanoman tilan kuvaus. |
| Vastaustyyppi       | Valitse sanoman tilan vastaustyyppi. Joiden käsiteltävien toimintojen tuloksena voi olla useita vastaustyyppejä. Esimerkiksi **Verkkopalvelu**-tyypin toiminnon seurauksena voi olla **Suoritettu onnistuneesti**- tai **Tekninen virhe** -tyyppi sen mukaan, mikä on suorituksen tulos. Määritä tässä tapauksessa sanomien tilat molemmille vastaustyypeille. Lisätietoja toimintotyypeistä ja niihin liittyvistä vastaustyypeistä on tämän artikkelin myöhemmässä [Sanoman käsittelytoimintojen tyypit](#action-types) -osassa. |
| Sanoman nimikkeen tila | Joskus sähköisen sanoman tilan on vaikutettava liittyvien sanoman nimikkeiden tilaan. Valitse tässä kentässä sanoman nimikkeen tila, jonka haluat liittää sanoman tilaan. |
| Salli poistaminen        | Valitse tämä valintaruutu, jos käyttäjien tulisi saada poistaa sähköisiä sanomia, joilla on tämä tila **Sähköiset sanomat** -sivulla. |

## <a name="additional-fields"></a><a id="additional"></a>Lisäkentät

EM-ominaisuus sallii sinun kerätä tietueita Microsoft Dynamics 365 Financen tapahtumataulukoista sanomien nimikkeiksi. Voit tällä tavoin valmistella tietueet raportointia varten ja sitten raportoida ne. Tapahtumatauluissa ei kuitenkaan joskus ole riittävästi tietoja tietueiden täyttämiseen raportin edellyttämällä tavalla. Voit täyttää kaikki tietueen raportoitavat tiedot määrittämällä lisäkenttiä. Lisäkenttiä voidaan liittää sanomiin ja sanomien nimikkeisiin. Voit määrittää lisäkenttiä kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Lisäkentät**.

Seuraavassa taulukossa käsitellään **Lisäkentät**-sivun yleiset kenttiä.

| Kenttä       | kuvaus |
|-------------|-------------|
| Kentän nimi  | Anna prosessiin liittyvien sähköisten sanomien tai sanomien nimikkeiden lisäkentän nimi. Tämä nimi näkyy prosessia käytettäessä käyttöliittymässä. Nimeä voidaan käyttää myös prosessiin liittyvissä sähköisen raportoinnin (ER) kokoonpanoissa. |
| kuvaus | Anna lisäkentän kuvaus. |
| Käyttäjän muokkaus   | Valitse asetukseksi **Kyllä**, jos käyttäjien tulisi voida muuttaa lisäkentän arvoa käyttöliittymässä. |
| Inventoija     | Valitse asetukseksi **Kyllä**, jos lisäkentässä on oltava sähköisessä raportissa numerosarja. Lisäkentän arvo täytetään automaattisesti, kun **Sähköisen raportoinnin vienti** -tyyppinen toiminto suoritetaan. |
| Piilotettu      | Määritä tämän asetuksen arvoksi **Kyllä**, jos lisäkenttä tulisi piilottaa käyttöliittymän **Sähköiset sanomat**- tai **Sähköisen sanoman nimikkeet** -sivulta. |

Voit määrittää ennalta lisäkentälle mahdollisia arvoja **Arvot**-pikavälilehdestä. Tämän jälkeen nämä arvot ovat käyttäjien valittavissa. Näin niitä ei tarvitse täyttää manuaalisesti käsittelyn aikana. Kentät käsitellään seuraavassa taulukossa.

| Kenttä                | kuvaus |
|----------------------|-------------|
| Kentän arvo          | Anna kentän arvo, jota käytetään sanomassa tai sanoman nimikkeessä raportoinnin aikana. |
| Kuvaus          | Anna kentän arvon kuvaus. |
| Tilityyppi         | Tiettyjen kenttien arvojen käyttö voi rajoittua tiettyihin tilityyppeihin. Valitse yksi seuraavista arvoista: **Kaikki**, **Asiakas** tai **Toimittaja**. |
| Tilikoodi         | Jos valitse **Tilityyppi**-kentässä **Asiakas** tai **Toimittaja**, voit rajoittaa kentän arvon käytön vain tiettyyn ryhmään tai taulukkoon. |
| Tilin/ryhmän numero | Jos valitse **Tilityyppi**-kentässä **Asiakas** tai **Toimittaja** ja jos annat ryhmän tai taulun **Tilikoodi**-kentässä, voit antaa tietyn ryhmän tai edustajan. |
| Voimassa            | Määritä päivämäärä, jolloin arvon huomioonottaminen alkaa. |
| Vanhentuminen           | Määritä päivämäärä, jolloin arvon huomioonottaminen loppuu. |

Oletusarvoisesti **Tilin/ryhmän numero**-, **Tilikoodi**-, **Voimassa**- ja **Vanhentuminen**-kenttien määrittämät yhdistelmäehdot eivät vaikuta lisäkenttien arvojen valintaan. Näitä yhdistelmiä voi kuitenkin käyttää suoritettavassa luokassa toteuttamaan tietyn logiikan, joka laskee lisäkenttien arvot.

## <a name="executable-class-settings"></a><a id="executable"></a>Suoritettavan luokan asetukset

Suoritettava luokka on X++-menetelmä tai luokka, jota sähköinen sanomankäsittely voi kutsua suhteessa toimintoon, jos prosessi edellyttää arviointia.

Voit määrittää manuaalisesti suoritettavan luokan, jota on kutsuttava käsittelyn aikana, kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Suoritettavan luokan asetukset**. Avaa **Suoritettavan luokan asetukset** -sivu, luo rivi ja määritä seuraavat kentät.

| Kenttä                 | kuvaus |
|-----------------------|-------------|
| Suoritettava luokka      | Anna nimi, jota käytetään sen sanoman käsittelytoiminnon määrityksen aikana, johon liittyen tämä luokka kutsutaan. |
| kuvaus           | Anna suorittavan luokan kuvaus. |
| Suoritettavan luokan nimi | Valitse suoritettava X++-luokka. |
| Suoritustaso       | Tämä kenttä määritetään automaattisesti, koska arvo on määritetty valitulle suoritettavalle luokalle. Tämä kenttä rajoittaa tasoa, jolla liittyvä arviointi suoritetaan. |
| Luokan kuvaus     | Tämä kenttä määritetään automaattisesti, koska arvo on määritetty valitulle suoritettavalle luokalle. |
| Toimenpidetyyppi           | Tämä kenttä on käytettävissä, kun **\[EM\] Suoritettavan luokan toimintotyyppi** -ominaisuus otetaan käyttöön **Ominaisuuksien hallinta** -työtilassa. Käytä tätä kenttää määrittääksesi toimintotyypin suoritettavalle luokalle. Tämä kenttä sallii sinun hallita tarkemmin seuraavia toimintoja, jotka ovat käytettävissä sähköiselle sanomalle **Sähköiset sanomat** -sivulla. |

Joissakin suoritettavissa luokissa voi olla pakollisia parametreja, jotka on määritettävä, ennen kuin suoritettava luokka suoritetaan ensimmäisen kerran. Voit määrittää nämä parametrit valitsemalla toimintoruudusta **Parametrit**. Määritä kentät avautuvassa valintaikkunassa ja valitse sitten **OK**. On tärkeää, että valitset **OK**. Muussa tapauksessa parametreja ei tallenneta tietokantaan eikä suoritettavaa luokaa kutsuta oikein.

## <a name="populate-records-actions"></a><a id="populate"></a>Tietueiden täyttötoiminnot

Voit määrittää tietueiden täyttötoiminnoilla toimintoja, jotka lisäävät tietueita sanoman nimikkeiden taulukkoon, jotta ne voidaan sitten lisätä sähköiseen sanomaan. Jos sähköisen sanoman on esimerkiksi raportoitava asiakkaan laskut, sinun on määritettävä tietueiden täyttötoiminto, joka on linkitetty Asiakkaan laskupäiväkirja -taulukon **Tietolähde**-kenttään.

Voit määrittää tietueiden täyttötoiminnot kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Tietueiden täyttötoiminnot**. Luo jokaiselle sellaiselle toiminnolle uusi tietue, jonka on lisättävä tietueita taulukkoon, ja määritä seuraavat kentät.

| Kenttä       | Kuvaus |
|-------------|-------------|
| Nimi        | Anna nimi prosessin toiminnolle, joka täyttää tietueet. |
| Kuvaus | Anna tietueiden täyttötoiminnon kuvaus. |

Lisää **Tietolähteiden määritys** -pikavälilehdessä rivi jokaiselle prosessissa käytettävälle tietolähteelle ja määritä seuraavat kentät.

| Kenttä                  | kuvaus |
|------------------------|-------------|
| Nimi                   | Anna tietolähteen nimi. |
| Sanoman nimiketyyppi      | Valitse sen sanoman nimikkeiden tyyppi, jota käytetään, kun tietolähteelle luodaan tietueita. |
| Tilityyppi           | Valitse tietolähteestä saatuihin tietueisiin liitettävän tilin tyyppi. |
| Päätaulun nimi      | Valitse tietolähteenä käytettävä taulukko. |
| Asiakirjan numerokenttä  | Valitse kenttä, josta asiakirjan numero saadaan valitussa päätaulukossa. Tämän kentän arvoa käytetään sanoman nimikkeen **Asiakirjan numero** -kentän arvona. |
| Asiakirjan päivämääräkenttä    | Valitse kenttä, josta asiakirjan päivämäärä saadaan valitussa päätaulukossa. Tämän kentän arvoa käytetään sanoman nimikkeen **Sanoman nimikkeen päivämäärä** -kentän arvona. |
| Asiakirjan tilikenttä | Valitse kenttä, josta asiakirjan tili saadaan valitussa päätaulukossa. Tämän kentän arvoa käytetään sanoman nimikkeen **Tilinumero**-kentän arvona. |
| Yhtiö                | Tämä kenttä on käytettävissä, kun **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -ominaisuus otetaan käyttöön **Ominaisuuksien hallinta** -työtilasta. Käytä tätä ominaisuuttaa määrittääksesi yritysten välisiä tietolähteitä tietueiden täyttötoimintoja varten. Tietoja voi noutaa useista yrityksistä. |
| Käyttäjän kysely             | <p>Jos määrität kyselyn valitsemalla ruudukon yläpuolelta **Muokkaa kyselyä** ja määrität ehdot, joita on käytettävä valitussa päätaulukossa, josta tiedot täytetään, tämä valintaruutu valitaan automaattisesti. Muussa tapauksessa kaikki tietueet täytetään valitusta päätaulukon lähteestä.</p><p>Kun **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -ominaisuus on käytössä **Ominaisuuksien hallinta** -työtilassa ja tietueita täytyy kerätä useista yrityksistä, lisää jokaiselle raportointiin sisällytettävälle lisäyritykselle rivi. Valitse kullekin uudelle riville **Muokkaa kyselyä** ja määritä ehto, joka koskee vain rivin **Yritys**-kentässä määritettyä yritystä. Kun olet valmis, **Tietolähteiden määritys** -ruudukko sisältää rivit kaikille yrityksille, jotka on sisällytettävä raportointiin.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a>Tietueiden täyttäminen useista yrityksistä

Jos yrityksen täytyy raportoida usealta yritykseltä samassa -Financetietokannassa, määritä [tietueiden täyttötoiminnot](#populate) kaikille yrityksille, joiden tiedot on sisällytettävä raportointiin.

Ota tämä ominaisuus käyttöön Finance-ympäristössä tekemällä seuraavat vaiheet. 

1. Valitse **Työtilat** \> **Ominaisuuden hallinta**.
2. Etsi ja valitse **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -toiminto luettelosta.
3. Valitse **Ota käyttöön nyt**. 

Noudattamalla seuraavia ohjeita voit määrittää usean yrityksen [tietueiden täyttötoiminnot](#populate), joista tiedot on sisällytettävä raportointiin.

1. Valitse **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Tietueiden täyttötoiminnot**.

    Kun **Yritysten väliset kyselyt tietueiden täyttötoiminnoille** -toiminto on käytössä, **Tietueiden täyttötoiminnot** -sivun **Tietolähteiden asetukset** -ruudukko sisältää **Yritys**-kentän. Tässä kentässä näkyy nykyisen yrityksen tunnus aiemmin luotujen tietueiden osalta, jotka on luotu yleisen [tietueiden täyttötoimintojen](#populate) määrityksen yhteydessä.

2. Lisää **Tietolähteiden asetukset** -ruudukkoon rivi kutakin raportointiin sisällytettävää tytäryhtiötä varten ja määritä seuraavat kentät.

    | Kentän nimi             | Arvo |
    |------------------------|-------|
    | Nimi                   | Kirjoita tekstiarvo, joka auttaa ymmärtämään, mistä tämä tietue tulee. Kirjoita esimerkiksi **Tietolähteen nimi – tytäryhtiö 1**. |
    | Sanoman nimiketyyppi      | Valitse viestinimiketyyppi, jota EM-käsittely edellyttää. |
    | Tilityyppi           | Määritä tilityyppi, jota EM-käsittely edellyttää. Valitse **Kaikki**, jos EM-käsittelyllä ei ole tiettyä tilityyppiä. |
    | Päätaulun nimi      | Määritä sen päätaulun nimi, jota EM-käsittely edellyttää. |
    | Asiakirjan numerokenttä  | Määritä kenttä, joka sisältää EM-käsittelyn tietueiden asiakirjan numeron. |
    | Asiakirjan päivämääräkenttä    | Määritä kenttä, joka sisältää EM-käsittelyn tietueiden asiakirjan päivämäärän. |
    | Asiakirjan tilikenttä | Määritä kenttä, joka sisältää EM-käsittelyn tietueiden asiakirjan tilin. |
    | Yritys                | Valitse tytäryhtiön tunnus. |
    | Käyttäjän kysely             | Tämä valintaruutu valitaan automaattisesti, kun määrität ehtoja valitsemalla **Muokkaa kyselyä**. |

3. Valitse kullekin uudelle riville **Muokkaa kyselyä** ja määritä ehto, joka koskee rivin **Yritys**-kentässä määritettyä yritystä.

## <a name="web-applications"></a><a id="applications"></a>Verkkosovellukset

Käytä verkkosovellusten asetuksia määrittääksesi verkkosovelluksen tukemaan Open Authorization (OAuth) 2.0 -protokollaa. OAuth on avoin standardi, jonka avulla käyttäjät voivat muodostaa suojatun delegoidun käyttöoikeuden sovellukseen käyttäjätunnuksia jakamatta. Voit käyttää myös valtuutusprosessia hakemalla valtuutuskoodin ja käyttöoikeustunnuksen. Voit määrittää verkkosovellusten asetukset kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Verkkosovellukset**.

Seuraavassa taulukossa käsitellään **Verkkosovellukset**-sivun kenttiä.

| Kenttä                        | Kuvaus |
|------------------------------|-------------|
| Sovelluksen nimi             | Anna verkkosovelluksen nimi. |
| Kuvaus                  | Anna verkkosovelluksen kuvaus. |
| URL-perusosoite                     | Anna verkkosovelluksen perusverkko-osoite. |
| Varmennuksen URL-osoite       | Määritä polku, jolla valtuutuksen URL-osoite muodostetaan. |
| Tunnuksen URL-osoite               | Määritä polku, jolla tunnuksen URL-osoite muodostetaan. |
| Uudelleenohjauksen URL-osoite                 | Anna uudelleenohjauksen URL-osoite. |
| Asiakastunnus                    | Anna verkkosovelluksen asiakasohjelman tunnus. |
| Asiakkaan salausavain                | Anna verkkosovelluksen asiakasohjelman salauskoodi. |
| Palvelimen tunnus                 | Anna verkkosovelluksen palvelimen tunnus. |
| Varmennuksen muodon yhdistäminen | Valitse sähköisen raportin muoto, jolla muodostetaan valtuutuspyyntö. |
| Tuo tunnuksen mallin yhdistäminen   | Valitse sähköisen raportoinnin tuontimallin yhdistäminen, jolla käyttöoikeustunnus tallennetaan. |
| Myönnetty alue                | Sovelluksen käyttöpyynnöille myönnetty vaikutusalue. Kenttä päivitetään automaattisesti. |
| Käyttöoikeustietue päättyy  | Jäljellä oleva aika ennen käyttöoikeustunnuksen vanhentumista. Kenttä päivitetään automaattisesti. | 
| Hyväksy                       | Määritä verkkopyynnön **Hyväksy**-ominaisuus. Anna esimerkiksi **application/vnd.hmrc.1.0+json**. |
| Sisältötyyppi                 | Määritä sisältötyyppi. Anna esimerkiksi **application/json**. |

Myös seuraavat **Verkkosovellukset**-sivun toimintoruudun painikkeet tukevat valtuutusprosessia:

- **Hae varmennuskoodi** – verkkosovelluksen varmennuksen käynnistäminen. Tämä toiminto luo valtuutuspyynnön käyttämällä **Varmennuksen muodon yhdistäminen** -kentässä määritettyä ER-muotoa.
- **Hanki käyttöoikeustunnus** – käyttöoikeustunnuksen hakuprosessin käynnistäminen.
- **Päivitä käyttöoikeustunnus** – käyttöoikeustunnuksen päivittäminen. Tämä toiminto tuo vastaanotettua käyttöoikeustunnusta koskevat tiedot käyttämällä **Tuo tunnuksen mallin yhdistäminen** -kentässä määritettyä ER-muotoa.

Kun verkkosovelluksen käyttöoikeustunnus on tallennettu järjestelmän tietokantaan salattuna, sitä voidaan käyttää verkkopalvelupyyntöihin. Tietoturvan vuoksi käyttöoikeustunnuksen käyttöoikeus on rajoitettava vain niille käyttöoikeusrooleille, jotka voivat käsitellä kyseisiä pyyntöjä. Jos käyttöoikeusryhmään kuulumattomat yrittävät käsitellä pyyntöä, he saavat virheen, joka ilmoittaa, etteivät he saa käyttää valittua verkkosovellusta toisen sovelluksen kautta. Määritä käyttöoikeustunnuksen käyttöoikeuden omaavat käyttöoikeusroolit **Verkkosovellukset**-sivun **Käyttöoikeusroolit**-pikavälilehdessä. Jos verkkosovellukselle ei ole määritetty käyttöoikeusrooleja, vain järjestelmänvalvoja voi toimia käyttämällä verkkosovellusta.

**Toimintoloki**-pikavälilehti tallentaa käyttäjään liittyviä tietoja sekä päivämäärän ja ajan jokaiselle toiminnolle valitulla verkkosovelluksella.

Jotkin verkkopalvelut saattavat edellyttää, että pyyntöihin sisällytetään eri otsikot. Järjestelmänvalvoja voi määrittää lisäotsikoita ja niiden arvot **Täydennysotsikot**-pikavälilehdestä ja käyttää niitä sitten pyynnön luonnin aikana.

## <a name="web-service-settings"></a><a id="settings"></a>Verkkopalvelun asetukset

Käytä verkkopalveluasetuksia määrittääksesi tietojen suoran siirron verkkopalveluun. Voit määrittää verkkopalveluiden asetukset kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Verkkopalvelun asetukset**.

Seuraavassa taulukossa käsitellään **Verkkopalvelun asetukset** -sivun kenttiä.

| Kenttä                          | kuvaus |
|--------------------------------|-------------|
| Internet-palvelu                    | Anna verkkopalvelun nimi. |
| kuvaus                    | Anna verkkopalvelun kuvaus. |
| Internet-osoite               | <p>Anna verkkopalvelun verkko-osoite. Jos verkkopalvelulle on määritetty verkkosovellus ja verkkopalvelun verkko-osoitteen tulisi vastata valitulle verkkosovellukselle määritettyä verkko-osoitetta, valitse **Kopioi URL-perusosoite**. Verkkosovelluksen URL-perusosoite kopioidaan tähän kenttään.</p><p>**Varoitus:** Tässä määrittämäsi kolmansien osapuolten palvelut tai muut palvelut eivät vaadi varmennetta eivätkä ne välttämättä täytä Microsoftin tietosuojastandardeja. Sinun tulisi tutustua kunkin palvelun tietosuojadokumentaatioon ja tehdä yhteistyötä kunkin palveluntarjoajan kanssa saadaksesi lisätietoja palvelun tarjoamasta yhteensopivuustasosta. Sinun vastuullasi on varmistaa, että nämä palvelut ovat tietoturvaa ja yksityisyyttä koskevien standardien sekä lakisääteisten standardien mukaisia. Käytä palveluita omalla vastuullasi. Microsoft ei anna nimenomaisesti ilmaistuja takuita, sitoumuksia tai ehtoja. Suosittelemme vahvasti, että käytät vain palveluita, jotka tarjoavat suojattuja ja valtuutettuja yhteyksiä, kuten HTTPS.</p> |
| Varmenne                    | Valitse aiemmin määritetty Azure Key Vault -varmenne. |
| Internet-sovellus                | Valitse aiemmin määritetty verkkosovellus. |
| Pyynnön tyyppi – XML        | Valitse asetukseksi **Kyllä**, jos vastaustyyppi on XML. |
| Pyyntömenetelmä                 | Määritä pyyntömenetelmä. HTTP määrittää pyyntömenetelmäjoukon, joka ilmaisee tietylle resurssille suoritettavan toiminnon. Pyyntömenetelmä voi olla **GET**, **POST** tai jokin muu HTTP-menetelmä. |
| Pyynnön otsikot                | Määritä pyynnön otsikot. Pyynnön otsikko on HTTP-otsikko, jota voi käyttää HTTP-pyynnössä. Se ei liity viestin sisältöön. |
| Hyväksy                         | Määritä verkkopyynnön Hyväksy-ominaisuus. |
| Hyväksy koodaus                | Määritä koodauksen hyväksymisen arvo. Koodauksen hyväksymispyynnön HTTP-otsikko ilmaisee sisällön koodauksen asiakasohjelman ymmärtämällä tavalla. Tämä sisältökoodaus on yleensä pakkausalgoritmi. |
| Sisältötyyppi                   | Määritä sisältötyyppi. Sisältötyyppiyksikön HTTP-otsikko ilmaisee resurssin mediatyypin. |
| Onnistuneet vastauskoodit       | Määritä HTTP-tilakoodi, joka ilmaisee pyynnön onnistumisen. |
| Otsikoiden muodon yhdistämispyyntö | Valitse sähköisen raportin muoto, jolla muodostetaan verkkopyynnön otsikot. |

## <a name="message-processing-actions"></a><a id="actions"></a>Sanoman käsittelytoiminnot

Sanoman käsittelytoiminnoilla voi luoda toimintoja prosesseihin ja määrittää näiden toimintojen parametrit. Voit määrittää sanomien käsittelytoiminnot kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sanoman käsittelytoiminnot**.

Seuraavissa taulukoissa käsitellään **Sanoman käsittelytoiminnot** -sivun kenttiä.

### <a name="general-fasttab"></a>Yleinen-pikavälilehti

| Kenttä                                     | kuvaus |
|-------------------------------------------|-------------|
| Toimenpidetyyppi                               | Valitse toiminnon tyyppi. Lisätietoja käytettävissä olevista asetuksista on tämän artkkelin myöhemmässä osassa [Sanoman käsittelytoimintojen tyypit](#action-types). |
| Muodon määritys                            | Valitse toiminnolle kutsuttava ER-muoto. Kenttä on käytettävissä vain **Sähköisen raportoinnin vienti**-, **Sähköisen raportoinnin tuonti**- ja **Sähköisen raportoinnin vientiviesti** -tyyppien toiminnoille. |
| Muodon yhdistämisen URL-osoite               | Valitse toiminnolle kutsuttava ER-muoto. Tätä muotoa käytetään muodostamaan URL-osoitteen polku, joka lisätään valitulle verkkopalvelimelle määritettyyn perusverkko-osoitteeseen. Tämä kenttä on käytettävissä vain **Verkkopalvelu** -tyypin toiminnoilla. |
| Sanoman nimiketyyppi                         | Valitse toiminnon arvioitavien tietueiden tyyppi. Kenttä on käytettävissä **Sanoman nimikkeen suoritustaso**-, **Sähköisen raportoinnin vienti**-, **Sähköisen raportoinnin tuonti**- ja **Verkkopalvelu**-tyyppien sekä muiden tyyppien toiminnoille. Jos tämä kenttä jätetään tyhjäksi, kaikki sanoman käsittelyä varten määritetyt sanoman nimiketyypit arvioidaan. |
| Suoritettava luokka                          | Valitse olemassa oleva suoritettavan luokan asetus. Tämä kenttä on käytettävissä vain **Sanoman nimikkeen suoritustaso**- ja **Sanoman suoritustaso** -tyyppien toiminnoissa. |
| Tietueiden täyttötoiminto                   | Valitse olemassa oleva tietueiden täyttötoiminto. Tämä kenttä on käytettävissä vain **Täytä tietueet** -tyypin toiminnoilla. |
| Internet-palvelu                               | Valitse olemassa oleva verkkopalvelu. Tämä kenttä on käytettävissä vain **Verkkopalvelu** -tyypin toiminnoilla. |
| Lähetettävän tiedoston nimi                         | Kirjoita sen sähköisen sanoman liitteen nimi, joka tämän toiminnon on lähetettävä. Jos useilla liitteillä on sama alkuperäinen tiedostonimi, viimeisin tiedosto lähetetään. Jos liitettä ei löydy, jolla on määritetty alkuperäinen tiedostonimi, pyyntö lähetetään ilman sisältöä. Tämä kenttä on käytettävissä vain **Verkkopalvelu** -tyypin toiminnoilla. |
| Tiedostonimi                                 | Määritä toiminnon tuloksena olevan tiedoston nimi. Tämä tiedosto voi olla verkkopalvelimen tai muodostetun raportin vastaus. Tämä kenttä on vain **Verkkopalvelu**- ja **Sähköisen raportoinnin vientiviesti** -tyypin toimintojen käytettävissä. |
| Tiedostojen liittäminen lähdeasiakirjoihin          | Valitse tämä valintaruutu liittääksesi luodut tiedostot EM-nimikkeiden viitatun päätaulukon tietueisiin. Tämä kenttä on käytettävissä vain **Sähköisen raportoinnin vienti**- ja **Verkkopalvelu**-tyyppien toiminnoille. |
| Liitä tiedostoja tulostusarkistosta nimikkeisiin | Valitse tämä valintaruutu noutaaksesi erilliset XML-tiedostot tulosarkistotiedostosta ja liittääksesi ne vastaaviin sähköisten sanomien nimikkeisiin. Tämä kenttä on vain **Sähköisen raportoinnin vienti** -tyypin toimintojen käytettävissä. |
| Vientikohtainen sanomien nimikkeiden määrä        | Määritä rajoitus yhteen tiedostoon (sanomaan) sisällytettävien sanomien nimikkeiden määrälle. Tämä kenttä on vain **Sähköisen raportoinnin vienti** -tyypin toimintojen käytettävissä. |
| Käytä ER-lähdettä                             | Valitse tämä valintaruutu käyttääksesi ER-lähdeparametreja tuonnissa. Muussa tapauksessa käytetään sähköisen sanoman liitettä. Tämä kenttä on vain **Sähköisen raportoinnin tuonti** -tyypin toimintojen käytettävissä. |
| Näytä valintaikkuna                               | Valitse asetukseksi **Kyllä**, jos valintaikkuna on näytettävä käyttäjille ennen raportin luomista. Tämä kenttä on vain **Sähköisen raportoinnin vientiviesti** -tyypin toimintojen käytettävissä. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Sanoman käsittelytoimintotyypit

Seuraavat vaihtoehdot ovat käytettävissä **Toimintotyyppi**-kentässä:

- **Luo viesti** – Tämän toimintotyypin avulla käyttäjille voidaan antaa mahdollisuus luoda sanomia manuaalisesti **Sähköinen sanoma** -sivulla. Tämän tyypin toiminnolle ei voi määrittää alkuperäistä tilaa.
- **Täytä tietueet** – Tämä toimintotyypin täytyy olla valmiiksi määritettynä. Liitä se tietueiden täyttötoimintoon sisällyttääksesi toiminnon käsittelyyn. Tätä toimintotyyppiä oletetaan käytettävän joko sanoman käsittelyn ensimmäisenä toimintona (kuten yhtään sähköistä sanomaa ei luotu etukäteen) tai toimintona, joka lisää sanoman nimikkeitä aiemmin **Luo viesti** -tyypin toiminnolla luotuun sanomaan. Tämän vuoksi tämän tyypin toiminnoille voidaan määrittää vain sanoman nimikkeiden tulostila. Alkuperäinen tila voidaan määrittää vain sanomille.
- **Sanoman suoritustaso** – tämän toimintotyypin avulla voi määrittää suoritettavan luokan, joka on arvioitava sanomatasolla.
- **Sanoman nimikkeen suoritustaso** – tämän toimintotyypin avulla voi määrittää suoritettavan luokan, joka on arvioitava sanoman nimiketasolla.
- **Sähköisen raportoinnin vienti** – Käytä tätä toimintotyyppiä toiminnoille, joiden tulisi luoda raportti vietävän ER-määritykseen perusteella sanoman nimikkeen tasolla.
- **Sähköisen raportoinnin vientiviesti** – Käytä tätä toimintotyyppiä toiminnoille, joiden tulisi luoda raportti vietävän ER-määrityksen perusteella sanoman tasolla (jos sanomalla ei esimerkiksi ole yhtään sanoman nimikettä).
- **Sähköisen raportoinnin tuonti** – Käytä tätä toimintotyyppiä toiminnoille, joiden tulisi luoda raportti tuotavan ER-määrityksen perusteella.
- **Viestitason käyttäjän käsittely** – Tämän toimintotyypin toiminnoissa oletetaan, että käyttäjä tekee manuaalisia toimintoja sanomatasolla. Käyttäjä voi esimerkiksi päivittää sanomien tilan.
- **Käyttäjän käsittely** – Tämän toimintotyypin toiminnoissa oletetaan, että käyttäjä tekee manuaalisia toimintoja sanoman nimiketasolla. Käyttäjä voi esimerkiksi päivittää sanoman nimikkeiden tilan.
- **Verkkopalvelu** – Tämän toimintotyypin toiminnoilla muodostettu raportti lähetetään verkkopalveluun. Tätä toimintotyyppiä ei käytetä italialaisessa myynti- ja ostolaskujen tietoliikenteen raportoinnissa. **Sanoman käsittelytoiminnot** -sivu sisältää tälle toimintotyypille **Muut tiedot** -pikavälilehden, josta voit määrittää vahvistustekstin. Tämä vahvistusteksti näytetään käyttäjille ennen valitun verkkopalvelun pyyntöjen käsittelemistä.
- **Pyynnön vahvistus** – tällä toimintotyypillä pyydetään vahvistus palvelimesta.

### <a name="initial-statuses-fasttab"></a>Alkuperäiset tilat -pikavälilehti

> [!NOTE]
> **Alkuperäiset tilat** -pikavälilehti ei ole käytettävissä toiminnoissa, joiden alkuperäinen toimintotyyppi on **Luo viesti**.

| Kenttä               | Kuvaus |
|---------------------|-------------|
| Sanoman nimikkeen tila | Valitse se sanoma nimikkeen tila, jonka perusteella valittu sanoman käsittelytoiminto on arvioitava. |
| kuvaus         | Valitun sanoman nimikkeen tilan kuvaus. |

### <a name="result-statuses-fasttab"></a>Tulostilat-pikavälilehti

| Kenttä               | kuvaus |
|---------------------|-------------|
| Sanoman tila      | Valitse ne sanoman tilat, joiden perusteella valittu sanoman käsittelytoiminto on arvioitava. Tämä kenttä on käytettävissä vain sanomatasolla arvioitavissa sanoman käsittelytoiminnoissa. Se on esimerkiksi käytettävissä **Sähköisen raportoinnin vienti**- ja **Sähköisen raportoinnin tuonti** -tyyppien toiminnoissa muttei **Käyttäjän käsittely**- ja **Sanoman nimikkeen suoritustaso** -tyyppien toiminnoissa. |
| kuvaus         | Valitun sanoman tilan kuvaus. |
| Vastaustyyppi       | Valitun sanoman tilan vastaustyyppi. |
| Sanoman nimikkeen tila | Valitse tulostilat, joka on oltava käytettävissä, kun valittu sanoman käsittelytoiminto on arvioitu. Tämä kenttä on käytettävissä vain sanoman nimiketasolla arvioitavissa sanoman käsittelytoiminnoissa. Se on esimerkiksi käytettävissä **Käyttäjän käsittely**- ja **Sanoman nimikkeen suoritustaso** -tyyppien toiminnoissa. Sanomatasolla arvioitavissa sanoman käsittelytoiminnoissa tässä kentässä on se sanoman nimikkeen tila, joka määritettiin valitulle sanoman tilalle. |

Seuraavassa taulukossa on tulostilat, jotka on määritettävä erilaisille toiminto- ja vastaustyypeille.

| Sähköisen sanoman toiminnon tyyppi tai vastaustyyppi | Suoritettu onnistuneesti | Liiketoiminnan virhe | Tekninen virhe | Käyttäjän määrittämä | Peruuta  |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Luo viesti                               | X                     |                |                 |              |        |
| Sähköisen raportoinnin vienti                  | X                     |                |                 |              |        |
| Sähköisen raportoinnin tuonti                  |                       |                |                 |              |        |
| Internet-palvelu                                  | X                     |                | X               |              |        |
| Käyttäjän käsittely                              |                       |                |                 |              |        |
| Sanoman suoritustaso                      |                       |                |                 |              |        |
| Täytä tietueet                             |                       |                |                 |              |        |
| Sanoman nimikkeen suoritustaso                 |                       |                |                 |              |        |
| Pyynnön vahvistus                         | X                     | X              | X               |              |        |
| Sähköisen raportoinnin vientiviesti          | X                     |                |                 |              |        |
| Viestitason käyttäjän käsittely                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Sähköisen sanoman käsittely

Sähköinen sanoman käsittely on EM-ominaisuuden peruskäsite. Se koostaa sähköisen sanoman arvioitavat toiminnot. Toiminnot voidaan linkittää käyttämällä alkuperäistä tilaa ja tuloksen tilaa. **Käyttäjän käsittely** -tyypin toiminnot puolestaan voidaan aloittaa itsenäisesti. Voit määrittää sähköisten sanomien käsittelyn kohdasta **Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sähköisen sanoman käsittely**.

**Toiminto**-pikavälilehdessä käsittelyyn voi lisätä esimääritettyjä toimintoja. Voit määrittää, suoritetaanko toiminto itsenäisesti vai onko käsittelyn aloitettava se. Voit määrittää toiminnon, jonka vain käyttäjä voi aloittaa käsittelyssä, valitsemalla kyseisen toiminnon **Suorita erikseen** -kentässä **Kyllä**. Jos toiminto on käynnistettävä käsittelemällä sanomat tai sanoman nimikkeet, joiden tilana on toiminnon alkuperäiseksi tilaksi määritetty tila, valitse **Suorita erikseen** -kentässä **Ei**. **Käyttäjätoiminto**-tyypin toiminnot on aina suoritettava erikseen.

Joskus useita toimintoja on koottava sarjaksi, vaikka ensimmäinen toiminto on määritetty erikseen suoritettavaksi. Oletetaan esimerkiksi, että käyttäjän täytyy aloittaa raportin luonti. Raportti on kuitenkin lähetettävä heti luonnin jälkeen verkkopalveluun ja verkkopalvelun vastauksen on heijastuttava järjestelmään. Tällöin voit luoda erottamattoman järjestyksen toiminnoille, jotka on aina suoritettava yhdessä. Valitse **Toiminto**-pikavälilehdessä ruudukon yläpuolella **Erottamattomat järjestykset** ja luo järjestys. Valitse sitten kaikkien yhdessä suoritettaville toiminnoille järjestys **Erottamattoman järjestys** -kentästä. Tässä esimerkissä **Suorita erikseen** -kentäksi valitaan **Kyllä** järjestyksen ensimmäiselle toiminnolle ja **Ei** kaikille muille toiminnoille.

**Sähköisen raportoinnin vienti**- ja **Sähköisen raportoinnin vientiviesti** -tyyppien toiminnot suoritetaan ER-muodossa, jolla on syöttöparametreja. Jos sähköisen sanoman käsittely sisältää jommankumman tyyppisiä toimintoja, sinun täytyy määrittää syöttöparametrien arvot ennen raportin luontia. Näin järjestelmä voi luoda raportin käyttämällä erähallintaa. Voit valita ruudukon yläpuolelta **Parametrit** määrittääksesi valitun toimintotyypin (**Sähköisen raportoinnin vienti** tai **Sähköisen raportoinnin vientiviesti**) parametrit. Valitse **Käytä parametrejä** -valintaruutu toiminnolle, joka on suoritettava määritetyin parametrein erähallinnassa.

Käytä **Sanoman nimikkeen lisäkentät** -pikavälilehteä lisätäksesi sanoman nimikkeisiin liittyviä esimääritettyjä lisäkenttiä. Lisäkenttiä on lisättävä jokaiselle sanoman nimiketyypille, johon kentät liittyvät. Voit määrittää oletusarvon, joka annetaan lisäkentälle käsittelyn aikana.

Käytä **Sanoman lisäkentät** -pikavälilehteä lisätäksesi sanomiin liittyviä esimääritettyjä lisäkenttiä. Voit määrittää oletusarvon, joka annetaan lisäkentälle käsittelyn aikana.

Käytä **Käyttöoikeusroolit**-pikavälilehteä määrittääksesi käyttöoikeusrooleja, jotka on esimääritetty järjestelmässä tiettyä käsittelytapaa varten. Käyttäjät, joilla on tietty rooli, näkevät vain kyseiselle roolille määritetyn käsittelyn.

Käytä **Erä**-pikavälilehteä määrittääksesi käsittelyn erähallinnassa tehtäväksi. Suosittelemme määrittämään erähallinnan käsittelyllesi suoraan **Sähköiset sanomat**- tai **Sähköisen sanoman nimikkeet** -sivulta, kun valitset toimintoruudusta **Suorita käsittely** aloittaaksesi käsittelyn.
