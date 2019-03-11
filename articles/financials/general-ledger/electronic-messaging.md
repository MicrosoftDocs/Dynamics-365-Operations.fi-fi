---
title: Sähköiset sanomat
description: Tässä aiheessa on Microsoft Dynamics 365 for Finance and Operationsin sähköisten sanomien yleiskatsaus ja määritystiedot.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "357930"
---
# <a name="electronic-messaging"></a>Sähköiset sanomat

[!include [banner](../includes/banner.md)]

Tässä aiheessa on Microsoft Dynamics 365 for Finance and Operationsin sähköisten sanomien yleiskatsaus ja määritystiedot.

Useiden eri maiden ja eri alueiden hallitukset ja viranomaiset eri puolilla maailmaa ovat äskettäin ottaneet käyttöön raportointivaatimuksia, jotka kyseisissä maissa ja kyseisillä alueilla rekisteröityneitä yrityksiä. Vaatimusten tarkoituksena on mahdollistaa tietojen saaminen kyseisistä yrityksistä sähköisessä muodossa suoraan niistä järjestelmistä, joissa tiedot kirjattiin, tallennettiin ja käsiteltiin.

Finance and Operationsin sähköiset sanomatoiminnot tukevat erilaisia sähköisiä prosesseja Finance and Operationsin sekä sellaisten julkishallinnon ja viranomaisten järjestelmien välillä, jotka mahdollistavat virallisten tietojen raportoinnin, lähettämisen ja vastaanottamisen.

Sähköisen viestinnän toiminnot on integroitu **sähköisen raportoinnin** (ER) moduulin kanssa. Näin ollen onkin mahdollista määrittää ER-muotoja sähköisiä sanomia varten. Lisätietoja on kohdassa [Sähköinen raportointi (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Sähköiset sanomat perustuvat seuraaviin yksiköihin:

- **Sähköinen sanoma** – Raportti tai ilmoitus, joka on raportoitava ja/tai lähetettävä sisäisesti. Sellainen on esimerkiksi verotoimistoon lähetettävä raportti.
- **Sähköisen sanoman nimikkeet** – tietueet, joiden on sisällyttävä raportoitavaan sanomaan.
- **Sähköisen sanoman käsittely** – Toimintoketju, jonka toiminnot voivat olla linkitettyjä tai linkittämättömiä. Sen avulla kerätään tarvittavat tiedot, luodaan raportit, tallennetaan tiedot Microsoft Azure Blob -säilöön, lähetetään raportit järjestelmän ulkopuolelle, saadaan vastaukset järjestelmän ulkopuolelta ja päivitetään tietokanta vastaanotettujen tietojen perusteella.

Seuraavassa kuvassa on tiedonkulku sähköisissä sanomissa.

![Sähköisten sanomien tiedonkulku](media/electronic-messaging-data-flow.png)

Sähköinen sanomatoiminto tukee seuraavia skenaarioita:

- Sellaisten sanomien luonti ja raporttien muodostaminen manuaalisesti, jotka perustuvat liitettyihin eri tyyppisiin ER-vientimuotoihin: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekstitiedosto ja Microsoft Word.
- Sellaisten sanomien luonti ja käsittely automaattisesti, jotka perustuvat viranomaiselta liitetyn ER-tuontimuodon avulla pyydettyihin ja saatuihin tietoihin.
- Tietojen kerääminen ja käsittely tietolähteestä (Finance and Operations -taulukosta) sanoman nimikkeinä.
- Lisätietojen tallentaminen ja eri arvojen arviointi kutsumalla erityisesti määritettyjä suorittavia luokkia suhteessa sanomiin tai sanoman nimikkeisiin.
- Sanoman nimikkeissä kerättyjen tietojen koostaminen, kyseisten tietojen jakaminen sanoman mukaan ja liitetyissä ER-vientimuodoissa olevien raporttien luominen.
- Luotujen raporttien lähettäminen verkkopalveluun käyttämällä Azure Key Vaultiin tallennettuja suojaustietoja.
- Vastaukseen saaminen verkkopalvelusta, vastauksen tulkinta ja Finance and Operationsin tietojen päivittäminen tarvittaessa.
- Kaikkien luotujen raporttien tallentaminen ja tarkastelu.
- Kaikkien niiden lokitietojen tallentaminen ja tarkasteleminen, jotka liittyvät sanoman tai sanoman nimikkeen yhteydessä suoritettuihin toimintoihin.
- Käsittelyn hallinta sanoman ja sanoman nimikkeen erilaisten tilojen avulla.

## <a name="set-up-electronic-messaging"></a>Sähköisen viestinnän määrittäminen

Sähköiset sanomat auttavat ylläpitämään erillisiä sähköisiä raportointiprosesseja eri asiakirjatyypeille. Joissakin monimutkaisissa skenaarioissa sähköisten sanomien määritys koostuu monien sanomatilojen, sanoman nimiketilojen, toimintojen, lisäkenttien ja suoritettavien luokkien yhdistelmästä. Näissä skenaarioissa käytettävissä on tuotavia tietoyksikköpaketteja. Jos käytät näitä tietoyksikköpaketteja, ne on tuotava yritykseen tietojen hallintatyökalulla. Lisätietoja tietojen hallintatyökalun käytöstä on kohdassa [Tiedonhallinta](../../dev-itpro/data-entities/data-entities-data-packages.md).

Jos et tuo tietoyksikköpakettia, voit määrittää sähköiset sanomatoiminnot manuaalisesti. Siinä tapauksessa seuraavat elementit on määritettävä: 

- [Numerosarjat](#number-sequences)
- [Sanoman nimikkeen tyypit ja tilat](#message-item-types-and-statuses)
- [Sanomien tilat](#message-statuses)
- [Lisäkentät](#additional-fields)
- [Suoritettavan luokan asetukset](#executable-class-settings)
- [Tietueiden täyttötoiminnot](#populate-records-actions)
- [Verkkopalvelun asetukset](#web-service-settings)
- [Sanoman käsittelytoiminnot](#message-processing-actions)
- [Sähköisen sanoman käsittely](#electronic-message-processing)

Seuraavissa osissa on lisätietoja jokaisesta edellä mainitusta elementistä.

### <a name="number-sequences"></a>Numerosarjat

Määritä sekä sanomien että sanoman nimikkeiden numerosarjat. Numerosarjoilla sanomat ja sanoman nimikkeet voidaan numeroida automaattisesti, ja määritetyt numerot ovat sanomien ja sanoman nimikkeiden yksilöiviä tunnisteita järjestelmässä. Voit määrittää sähköisen viestinnän numerosarjat **Kirjanpitoparametrit**-sivulla (**Pääkirjanpito** \> **Kirjanpidon asetukset** \> **Kirjanpitoparametrit**).

### <a name="message-item-types-and-statuses"></a>Sanoman nimikkeen tyypit ja tilat

Sanoman nimiketyypit ilmaisevat sähköisissä sanomissa käytettävät tietuetyypit. Voit määrittää sanoman nimiketyypit **Sanoman nimiketyypit** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Sanoman nimiketyypit**).

Sanoman nimikkeen tiloilla ilmaistaan sanoman nimikkeissä käytettävät tilat käsittelyssä, jota olet määrittämässä. Voit määrittää sanoman nimikkeiden tilat **Sanoman nimikkeiden tilat** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Sanoman nimikkeiden tilat**).

### <a name="message-statuses"></a>Sanomien tilat

Määritä sanomien tilat, joiden on oltava käytettävissä sanomien käsittelyssä. Voit määrittää sanomien tilat **Sanomien tilat** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Sanomien tilat**).

### <a name="additional-fields"></a>Lisäkentät

Voit käyttää sähköisissä sanomatoiminnoissa tapahtumataulukon tietueita. Voit tällä tavoin valmistella tietueet raportointia varten ja sitten raportoida ne. Joskus tapahtumataulukon tiedot eivät ole raporttivaatimusten mukaan riittävät tietueen raportointiin. Voit täyttää kaikki tietueen raportoivat tiedot määrittämällä lisäkenttiä. Lisäkentät voidaan liittää sekä sanomiin että sanoman nimikkeisiin. Voit määrittää lisäkentät **Lisäkentät**-sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Lisäkentät**).

Seuraavassa taulukossa käsitellään **Lisäkentät**-sivun kenttiä.

| Kenttä                | kuvaus |
|----------------------|-------------|
| Kentän nimi           | Anna prosessiin liittyvien sanoman nimikkeiden lisämääritteen nimi. Tämä nimi näkyy prosessia käytettäessä käyttöliittymässä. Sitä voidaan käyttää myös prosessiin liittyvissä ER-määrityksissä. |
| kuvaus          | Anna prosessiin liittyvien sanoman nimikkeiden lisämääritteen kuvaus. |
| Kentän arvo          | Anna kentän arvo, jota käytetään sanoman nimikkeeseen liittyen raportoinnin aikana. |
| Kentän kuvaus    | Anna sen kentän arvon kuvaus, jota käytetään sanoman nimikkeeseen liittyen raportoinnin aikana. |
| Tilityyppi         | Tietty lisäkenttien arvojen käyttö voi rajoittua tiettyihin tilityyppeihin. Valitse yksi seuraavista arvoista: **Kaikki**, **Asiakas** tai **Toimittaja**. |
| Tilikoodi         | Jos valitse **Tilityyppi**-kentässä **Asiakas** tai **Toimittaja**, voit rajoittaa kentän arvojen käytön vain tiettyyn ryhmään tai taulukkoon. |
| Tilin/ryhmän numero | Jos valitse **Tilityyppi**-kentässä **Asiakas** tai **Toimittaja** ja jos annat ryhmän tai taulun **Tilikoodi**-kentässä, voit antaa tietyn ryhmän tai edustajan. |
| Voimassa            | Määritä päivämäärä, jolloin arvon huomioonottaminen alkaa. |
| Vanhentuminen           | Määritä päivämäärä, jolloin arvon huomioonottaminen loppuu. |

### <a name="executable-class-settings"></a>Suoritettavan luokan asetukset

Suoritettava luokka on X++-menetelmä tai luokka, jota sähköinen sanomankäsittely voi kutsua suhteessa toimintoon, jos prosessi edellyttää arviointia.

Voit määrittää suoritettavan luokan manuaalisesti **Suoritettavan luokan asetukset** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Suoritettavan luokan asetukset**). Luo rivi ja määritä seuraavat kentät.

| Kenttä                 | kuvaus |
|-----------------------|-------------|
| Suoritettava luokka      | Anna nimi, jota käytetään sen sanoman käsittelytoiminnon määrityksen aikana, johon liittyen tämä luokka kutsutaan. |
| kuvaus           | Anna suorittavan luokan kuvaus. |
| Suoritettavan luokan nimi | Valitse suoritettava X++-luokka. |
| Suoritustaso       | Tämä kenttä määritetään automaattisesti, koska valitun suoritettavan luokan arvo on esimääritettävä. Tämä kenttä rajoittaa tasoa, jolla liittyvä arviointi suoritetaan. |
| Luokan kuvaus     | Tämä kenttä määritetään automaattisesti, koska valitun suoritettavan luokan arvo on esimääritettävä. |

### <a name="populate-records-actions"></a>Tietueiden täyttötoiminnot

Voit määrittää tietueen täyttötoiminnoilla toimintoja, joilla lisätään tietueita sanoman nimiketaulukkoon, jotta ne voidaan sitten lisätä sähköiseen sanomaan. Jos sähköisen sanoman on esimerkiksi raportoitava asiakkaan laskut, sinun on määritettävä **tietueiden täyttötoiminto**, joka on linkitetty **Asiakkaan laskupäiväkirja** -taulukkoon (**Tietolähde**-kentässä). Voit määrittää tietueen täyttötoiminnot **Tietueiden täyttötoiminto** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Tietueiden täyttötoiminnot**). Luo jokaiselle sellaiselle toiminnolle uusi tietue, jonka on lisättävä tietueita taulukkoon, ja määritä seuraavat kentät.

| Kenttä       | kuvaus                                                               |
|-------------|---------------------------------------------------------------------------|
| Nimi        | Anna nimi prosessin toiminnolle, joka täyttää tietueet.       |
| kuvaus | Anna kuvaus prosessin toiminnolle, joka täyttää tietueet. |

Lisää **Tietolähteiden määritys** -pikavälilehdessä rivi jokaiselle prosessissa käytettävälle tietolähteelle ja määritä seuraavat kentät.

| Kenttä                  | kuvaus |
|------------------------|-------------|
| Nimi                   | Anna tietolähteen nimi. |
| Sanoman nimiketyyppi      | Valitse sen sanoman nimiketyyppi, jota on käytettävä luotaessa tietolähteen tietueita. |
| Tilityyppi           | Valitse sen tilin tyyppi, joka on liitettävä tietolähteen tietueisiin. |
| Päätaulun nimi      | Valitse Finance and Operationsin taulukko, jonka on oltava tietolähde. |
| Asiakirjan numerokenttä  | Valitse kenttä, jonka asiakirjanumero on otettava valitusta taulusta. |
| Asiakirjan päivämääräkenttä    | Valitse kenttä, jonka asiakirjan päivämäärä on otettava valitusta taulusta. |
| Asiakirjan tilikenttä | Valitse kenttä, jonka asiakirjan tili on otettava valitusta taulusta. |
| Käyttäjän kysely             | Jos tämä valintaruutu on valittu, voit määrittää kyselyn valitsemalla **Muokkaa kyselyä** edellä olevassa ruudukossa. Muussa tapauksessa kaikki tietueet täytetään tietolähteestä. |

### <a name="web-service-settings"></a>Verkkopalvelun asetukset

Voit määrittää verkkopalvelun asetuksissa tietojen suoran siirron verkkopalveluun. Voit määrittää verkkopalvelun asetukset **Verkkopalvelun asetukset** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Verkkopalvelun asetukset**).

Seuraavassa taulukossa käsitellään **Verkkopalvelun asetukset** -sivun kenttiä.

| Kenttä                   | kuvaus |
|-------------------------|-------------|
| Internet-palvelu             | Anna verkkopalvelun nimi. |
| kuvaus             | Anna verkkopalvelun kuvaus. |
| Internet-osoite        | Anna verkkopalvelun verkko-osoite. |
| Todistus             | Valitse aiemmin määritetty Key Vault -varmenne. |
| Pyynnön tyyppi – XML | Valitse asetukseksi **Kyllä**, jos vastaustyyppi on XML. |
| Pyyntömenetelmä          | Määritä pyyntömenetelmä. HTTP määrittää pyyntömenetelmäjoukon, joka ilmaisee tietylle resurssille suoritettavan toiminnon. Menetelmä voi olla **GET**, **POST** tai jokin muu HTTP-menetelmä. |
| Pyynnön otsikot         | Määritä pyynnön otsikot. Pyynnön otsikko on HTTP-otsikko, jota voidaan käyttää HTTP-pyynnössä mutta joka ei liity sanoman sisältöön. |
| Hyväksy koodaus         | Määritä koodauksen hyväksyminen. Koodauksen hyväksymispyynnön HTTP-otsikko ilmaisee sisällön koodauksen asiakasohjelman ymmärtämällä tavalla. Tämä sisältökoodaus on yleensä pakkausalgoritmi. |
| Sisältötyyppi            | Määritä sisältötyyppi. Sisältötyyppiobjektin otsikko ilmaisee resurssin mediatyypin. |

### <a name="message-processing-actions"></a>Sanoman käsittelytoiminnot

Sanoman käsittelytoiminnoilla voi luoda toimintoja prosesseihin ja määrittää näiden toimintojen parametrit. Voit määrittää sanoman käsittelytoiminnot **Sanoman käsittelytoiminnot** -sivulla (**Vero** \> **Määritys** \> **Sähköiset sanomat** \> **Sanoman käsittelytoiminnot**).

Seuraavissa taulukoissa käsitellään **Sanoman käsittelytoiminnot** -sivun kenttiä.

#### <a name="general-fasttab"></a>Yleinen-pikavälilehti

| Kenttä                   | kuvaus |
|-------------------------|-------------|
| Toimenpidetyyppi             | Valitse toiminnon tyyppi. Lisätietoja käytettävissä olevista asetuksista on kohdassa [Sanoman käsittelytoimintojen tyypit](#message-processing-action-types). |
| Muodon määritys          | Valitse toiminnolle kutsuttava ER-muoto. Kenttä on käytettävissä vain **Sähköisen raportoinnin vienti**-, **Sähköisen raportoinnin tuonti**- ja **Sähköisen raportoinnin vientiviesti** -tyyppien toiminnoille. |
| Sanoman nimiketyyppi       | Valitse toiminnon arvioitavien tietueiden tyyppi. Kenttä on käytettävissä **Sanomanimikkeen suoritustaso**-, **Sähköisen raportoinnin vienti**- ja **Sähköisen raportoinnin tuonti** -tyyppien sekä joiden muiden tyyppien toiminnoille. Jos tämä kenttä jätetään tyhjäksi, kaikki sanoman käsittelyä varten määritetyt sanoman nimiketyypit arvioidaan. |
| Suoritettava luokka        | Valitse aiemmin luodut suoritettavan luokan asetukset. Tämä kenttä on käytettävissä vain **Sanoman nimikkeen suoritustaso**- ja **Sanoman suoritustaso** -tyyppien toiminnoissa. |
| Tietueiden täyttötoiminto | Valitse aiemmin määritetty tietueiden täyttötoiminto. Tämä kenttä on käytettävissä vain **Täytä tietueet** -tyypin toiminnoilla. |

##### <a name="message-processing-action-types"></a>Sanoman käsittelytoimintotyypit

Seuraavat vaihtoehdot ovat käytettävissä **Toimintotyyppi**-kentässä:

- **Täytä tietueet** – **Täytä tietueet** -toiminto on pitänyt määrittää aiemmin. Kun liität sen **Täytä tietueet** -tyypin toimintoon, se voidaan sisällyttää käsittelyyn. Oletuksena on, että tätä toimintotyyppiä käytetään sanoman käsittelyn ensimmäisenä toimintona. Tämän vuoksi tämän tyypin toiminnolla voidaan määrittää vain tulostila. Alkuperäistä tilaa ei voi määrittää.
- **Luo viesti** – Tämän tyypin avulla käyttäjille voidaan antaa mahdollisuus luoda sanomia manuaalisesti **Sähköinen sanoma** -sivulla. Tämän tyypin toiminnolle ei voi määrittää alkuperäistä tilaa.
- **Sanoman suoritustaso** – tämän tyypin avulla voi määrittää suoritettavan luokan, joka on arvioitava sanomatasolla.
- **Sanoman nimikkeen suoritustaso** – tämän tyypin avulla voi määrittää suoritettavan luokan, joka on arvioitava sanoman nimiketasolla.
- **Sähköisen raportoinnin vienti** – tämän tyypin toiminnoilla voi luoda raportin, joka perustuu vietävään ER-määritykseen sanoman nimiketasolla.
- **Sähköisen raportoinnin vientiviesti** – tämän tyypin toiminnoilla voi luoda raportin, joka perustuu vietävään ER-määritykseen sanomatasolla (jos sanomalla ei esimerkiksi ole yhtään sanoman nimikettä).
- **Sähköisen raportoinnin tuonti** – tämän tyypin toiminnoilla voi luoda raportin, joka perustuu tuovaan ER-määritykseen.
- **Viestitason käyttäjän käsittely** – Tämän tyypin toiminnoissa oletetaan, että käyttäjä tekee manuaalisia toimintoja. Käyttäjä voi esimerkiksi päivittää sanomien tilan.
- **Käyttäjän käsittely** – Tämän tyypin toiminnoissa oletetaan, että käyttäjä tekee manuaalisen toiminnon. Käyttäjä voi esimerkiksi päivittää sanoman nimikkeiden tilan.
- **Verkkopalvelu** – Tämän tyypin toiminnoilla muodostettu raportti lähetetään verkkopalveluun. Tätä toimintotyyppiä ei käytetä italialaisessa myynti- ja ostolaskujen tietoliikenteen raportoinnissa.
- **Pyynnön vahvistus** – tällä tyypillä pyydetään vahvistus palvelimesta.

#### <a name="initial-statuses-fasttab"></a>Alkuperäiset tilat -pikavälilehti

> [!NOTE]
> **Alkuperäiset tilat** -pikavälilehti ei käytettävissä toiminnoissa, joiden alkuperäinen tyyppi on **Täytä tietueet** tai **Luo viesti**.

| Kenttä               | kuvaus                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Sanoman nimikkeen tila | Valitse se sanoma nimikkeen tila, jonka perusteella valittu sanoman käsittelytoiminto on arvioitava. |
| kuvaus         | Valitun sanoman nimikkeen tilan kuvaus.                                                  |

#### <a name="result-statuses-fasttab"></a>Tulostilat-pikavälilehti

| Kenttä               | kuvaus |
|---------------------|-------------|
| Sanoman tila      | Valitse ne sanoman tilat, joiden perusteella valittu sanoman käsittelytoiminto on arvioitava. Tämä kenttä on käytettävissä vain sanomatasolla arvioitavissa sanoman käsittelytoiminnoissa. Se on esimerkiksi käytettävissä **Sähköisen raportoinnin vienti**- ja **Sähköisen raportoinnin tuonti** -tyyppien toiminnoissa. Se ei ole käytettävissä **Käyttäjän käsittely**- ja **Sanoman nimikkeen suoritustaso** -tyyppien toiminnoissa. |
| kuvaus         | Valitun sanoman tilan kuvaus. |
| Vastaustyyppi       | Valitun sanoman tilan vastaustyyppi. |
| Sanoman nimikkeen tila | Valitse tulostilat, joka on oltava käytettävissä, kun valittu sanoman käsittelytoiminto on arvioitu. Tämä kenttä on käytettävissä vain sanoman nimiketasolla arvioitavissa sanoman käsittelytoiminnoissa. Se on esimerkiksi käytettävissä **Käyttäjän käsittely**- ja **Sanoman nimikkeen suoritustaso** -tyyppien toiminnoissa. Sanomatasolla arvioitavissa sanoman käsittelytoiminnoissa tässä kentässä on se sanoman nimikkeen tila, joka määritettiin valitulle sanoman tilalle. |

### <a name="electronic-message-processing"></a>Sähköisen sanoman käsittely

Sähköinen sanoman käsittely on sähköisten sanomatoimintojen peruskäsite. Se koostaa sähköisen sanoman arvioitavat toiminnot. Toiminnot voidaan linkittää alkuperäinen tilan ja tulostilan kautta. **Käyttäjän käsittely** -tyypin toiminnot puolestaan voidaan aloittaa itsenäisesti. Voit valita **Sähköisen sanoman käsittely** -sivulla (**Vero** \> **Asetukset** \> **Sähköiset sanomat** \> **Sähköisen sanoman käsittely**) myös tuettavia käsittelyn lisäkenttiä.

**Toiminto**-pikavälilehdessä käsittelyyn voi lisätä esimääritettyjä toimintoja. Voit määrittää, suoritetaanko toiminto itsenäisesti vai onko käsittelyn aloitettava se. (Käyttäjän toiminnot on suoritettava itsenäisesti.)

**Sanoman nimikkeen lisäkentät** -pikavälilehdessä voi lisätä sanoman nimikkeisiin liittyviä esimääritettyjä lisäkenttiä. Lisäkenttiä on lisättävä jokaiselle sanoman nimiketyypille, johon kentät liittyvät.

**Sanoman lisäkentät** -pikavälilehdessä voi lisätä sanomaan liittyviä esimääritettyjä lisäkenttiä.

**Käyttöoikeusroolit**-pikavälilehdessä voi määrittää tiettyihin käsittelyihin järjestelmässä esimääritettyjä käyttöoikeusrooleja. Käyttäjät, joilla on tietty rooli, näkevät vain kyseiselle roolille määritetyn käsittelyn.

**Erä**-pikavälilehdessä voi määrittää käsittelyn erähallinnassa tehtäväksi.

## <a name="work-with-electronic-messages-functionality"></a>Sähköisten sanomatoimintojen käyttäminen

Jos työskentelet sanomatasolla, kannattaa käyttää **Sähköiset sanomat** -sivua (**Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanomat**). Jos työskentelet tietojen keräyksen (sanoman nimikkeen) tasolla, kannattaa käyttää **Sähköiset sanoman nimikkeet** -sivua (**Vero** \> **Kyselyt ja raportit** \> **Sähköiset sanomat** \> **Sähköiset sanoman nimikkeet**).

### <a name="electronic-messages"></a>Sähköiset sanomat

**Sähköiset sanomat** -sivulla on näkyvissä roolisi perusteella käytettävissä oleva käsittely. Käyttöoikeusroolit liitetään käsittelyyn kyseisen käsittelyn määrityksissä. Sivulla näytetään kunkin käytettävissä olevan käsittelyn sähköiset sanomat ja niihin liittyvät tiedot.

**Sanomat**-pikavälilehdessä näkyvät valitun käsittelyn sanomat. Valitun sanoman tilan ja esimääritetyn käsittelyn perusteella voit suorittaa joitakin toimintoja valitsemalla ruudukon yläpuolella olevia painikkeita:

- **Uusi** – tämä painike on liitetty **Luo viesti** -tyypin toimintoihin.
- **Poista** – tämä painike on käytettävissä, jos valitun sanoman nykyiseksi tilaksi on valittu **Salli poistaminen** -valintaruutu.
- **Luo raportti** – tämä painike on liitetty **Sähköisen raportoinnin vientiviesti** -tyypin toimintoihin.
- **Lähetä raportti** – tämä painike on liitetty **Verkkopalvelu**-tyypin toimintoihin.
- **Päivitä tila** – tämä painike on liitetty **Viestitason käyttäjän käsittely** -tyypin toimintoihin.
- **Sanoman nimikkeet** – avaa **Sähköisen sanoman nimikkeet** -sivun.

**Toimintoloki**-pikavälilehdessä on tietoja kaikista valitulle sanomalle suoritetuista toiminnoista.

**Sanoman lisäkentät** -pikavälilehdessä on kaikki lisäkentät, jotka on määritetty sanomille käsittelyn määrityksissä. Myös kyseisten lisäkenttien arvot näkyvät tässä välilehdessä.

**Sanoman nimikkeet** -pikavälilehdessä on kaikki valittuun sanomaan liittyvät sanoman nimikkeet.

Voit tarkastella kaikkia valitun viestin liitteitä. Nämä liitteet ovat jo luotuja ja vastaanotettuja raportteja. Valitse sanoma, jonka liitteitä haluat tarkastella. Valitse sitten **Liite**-painike toimintoruudussa.

![Liitepainike](media/attachment-icon.png)

**Liitteet**-sivulla on kaikki sanomaan liittyvät liitteet. Voit tarkastella tiedostoa valitsemalla sen vasemmalla olevasta luettelosta ja valitsemalla sitten **Avaa** toimintoruudussa.

![Avaa-painike](media/open-button.png)

Voit tarkastella tiettyyn sanomassa aiemmin suoritettuun toimintoon liittyviä liitteitä valitsemalla ensin sanoman **Sähköiset sanomat** -sivulla ja sitten toiminnon **Toimintoloki**-pikavälilehdessä. Valitse sitten **Liite**-painike toimintoruudussa.

Voit lisäksi suorittaa koko käsittelyn tai vain tietyn toiminnon valitsemalla **Suorita käsittely** toimintoruudussa.

### <a name="electronic-message-items"></a>Sähköisen sanoman nimikkeet

**Sähköisen sanoman nimikkeet** -sivulla on kaikki sanoman nimikkeet ja loki kullekin sanoman nimikkeelle suoritetuista toiminnoista. Siinä näkyy sanoman nimikkeille määritetyt lisäkentät sekä kyseisten kenttien arvot.

Seuraavassa taulukossa käsitellään **Sanoman nimikkeet** -välilehden kenttiä.

<table>
<thead>
<tr>
<th>Kenttä</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Käsittely</td>
<td>Sen käsittelyn nimi, jolla sanoman nimike luotiin.</td>
</tr>
<tr>
<td>Sanoman nimike</td>
<td>Sanoman nimikkeen tunnus. Tämä tunnus määritetään automaattisesti sen <strong>sanoman nimikkeen </strong> numerojärjestyksen perusteella, joka määritettiin <strong>Kirjanpitoparametrit</strong>-sivulla.</td>
</tr>
<tr>
<td>Sanoman nimikkeen päivämäärä</td>
<td>Päivämäärä, jolloin sanoman nimike luotiin.</td>
</tr>
<tr>
<td>Sanoman nimiketyyppi</td>
<td>Sanoman nimiketyyppi. Samaa käsittelyä varten voidaan määrittää useita sanomien nimiketyyppejä. (Niitä ovat esimerkiksi <strong>Saapuvat laskut</strong> ja <strong>Lähtevät laskut</strong>). Tämä kenttä voidaan täyttää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Sanoman nimikkeen tila</td>
<td>Sanoman nimikkeen varsinainen tila. Käytettävissä olevat tilat vaihtelevat sanoman nimiketyypin mukaan. Seuraavassa on muutamia esimerkkejä:
<ul>
<li><strong>Täytetty</strong> – tietue lisättiin Sanoman nimikkeet -taulukkoon.</li>
<li><strong>Arvioitu</strong> – sanoman nimikkeelle laskettiin lisämääritteitä.</li>
<li><strong>Raportoitu</strong> – sanoman nimikkeen lisääminen raporttiin onnistui.</li>
<li><strong>Poissuljettu</strong> – tätä tila voi olla kätevä, jos tietyt sanoman nimikkeet on suljettava pois raportista ennen vientiä.</li>
</ul>
</td>
</tr>
<tr>
<td>Lähetyspäivämäärä</td>
<td>Sanoman nimikkeen lähetyspäivämäärä, jos käsittely lähettää luodun raportin automaattisesti järjestelmän ulkopuolelle.</td>
</tr>
<tr>
<td>Asiakirjan numero</td>
<td>Tämä kenttä täytetään automaattisesti tietueiden täyttötoiminnon määritysten perusteella. Tämä kenttä voidaan täyttää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Tilinumero</td>
<td>Asiakkaan tai toimittajan tilinumero (tai muu kentän arvo sen kentän perusteella, joka määritettiin <strong>Täytä tietueet</strong> -toiminnossa). Tämä kenttä voidaan täyttää automaattisesti vain, kun lasku on lisätty Sanoman nimikkeet -taulukkoon.</td>
</tr>
<tr>
<td>Viesti</td>
<td>Sanoman numero. Tämä numero automaattisesti sen <strong>sanoman </strong> numerojärjestyksen perusteella, joka määritettiin <strong>Kirjanpitoparametrit</strong>-sivulla.</td>
</tr>
<tr>
<td>Sanoman tila</td>
<td>Sähköisen sanoman varsinainen tila.</td>
</tr>
<tr>
<td>Seuraava toiminto</td>
<td>Seuraava toiminto, joka voidaan käynnistää sanoman nimikkeen nykyiselle tilalle.</td>
</tr>
</tbody>
</table>

**Lisäkentät**-välilehdessä on valitun sanoman nimikkeen lisäkentät ja niiden arvot.

#### <a name="run-processing"></a>Suorita käsittely

Suorita sanoman nimikkeiden käsittely valitsemalla toimintaruudussa **Suorita käsittely**. Voit suorittaa tietyn toiminnon valitsemalla **Suorita käsittely** -valintaikkunan **Valitse toiminto** -asetukseksi **Kyllä** ja valitsemalla sitten toiminnon. Voit suorittaa koko käsittelyn jättämällä **Suorita toiminto** -asetukseksi **Ei**.

#### <a name="generate-report"></a>Luo raportti

Luo raportti valitsemalla toimintoruudussa **Luo raportti**. Tämä painike on liitetty **Sähköisen raportoinnin vienti** -tyypin toimintoihin.

#### <a name="update-status"></a>Päivitä tila

Päivät sanoman nimikkeiden tila valitsemalla toimintoruudussa **Päivitä tila**. Valitse päivitettävät sanoman nimikkeet **Päivitä tila** -valintaikkunan **Sisällytettävät tietueet** -pikavälilehdessä. Varmista, että määrität valintaehdot oikein, koska sanoman nimikkeiden tilat päivitetään näiden ehtojen, valitun toiminnon alkuperäisen tilan ja määritetyn **Uusi tila** -arvon mukaisesti. Kun tilan päivitys on valmis, juuri päivitettyjä nimikkeitä on vaikea selvittää. Tämän vuoksi tilapäivitysten peruuttaminen on hankalaa.

#### <a name="electronic-messages"></a>Sähköiset sanomat

Voit tarkastella valittuun sanoman nimikkeeseen liittyvä sähköistä sanomaa valitsemalla toimintoruudussa **Sähköinen sanoma**.

Voit tarkastella myös kaikkia sanoman nimikkeen tiedostoja. Valitse sanoman **Sanoma**-kenttä tai valitse toimintoruudussa **Sähköinen sanoma**. Valitse **Sähköinen sanoma** -sivulla tarkasteltavan sanoman raportti ja valitse sitten toimintoruudussa **Liite**-painike.

![Liitepainike](media/attachment-icon.png)

**Liitteet**-sivulla on kaikki sanomaan liittyvät liitteet. Voit tarkastella tiedostoa valitsemalla sen vasemmalla olevasta luettelosta ja valitsemalla sitten **Avaa** toimintoruudussa.

![Avaa-painike](media/open-button.png)

#### <a name="original-document"></a>Alkuperäinen tiedosto

Avaa valitun sanoman nimikkeen alkuperäinen tiedosto valitsemalla toimintoruudussa **Alkuperäinen tiedosto**.

## <a name="example"></a>Esimerkki

Kun olet luonut ER-muodon, yhdistänyt sen tietolähteisiin ja viimeistellyt sen, voit suorittaa sen **Sähköinen raportointi** -työtilassa. Voit tallentaa luotavan raportin paikallisesti.

Seuraavien raportointiprosessin ominaisuuksia hallintaa varten on määritettävä sähköinen sanomakäsittely:

- Raportin luonutta henkilöä koskevien tietojen kirjaaminen.
- Raportin luontiajankohdan kirjaaminen.
- Edellisinä kausina luotujen raporttien tallentaminen.

Tämä osan esimerkki näyttää, miten sähköiset sanomatoiminnot voidaan määrittää muodostamaan raportointiprosessi.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Excel-raportin luovan yksinkertaisen ER-vientimuodon kutsuvan käsittelyn määrittäminen ja suorittaminen

Tässä osassa on esimerkki tavasta, jolla sähköiset sanomat voidaan määrittää luomaan Exceliin vievään ER-muotoon perustuva raportti. Tässä esimerkissä Exceliin vievä ER-muoto on oltava luotuna, tietolähteisiin yhdistettynä ja viimeisteltynä. Numerosarja on oltava määritetty sähköisille sanomille.

Kun muodostat käsittelyn, määritettävät käsittelyn toiminnot ja tilat kannattaa määrittää ensin. Seuraava kuva osoittaa, miltä käsittely näyttää tässä esimerkissä.

![Käsittelymalli](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Sanomien tilojen luominen

1. Valitse **Vero \> Asetukset \> Sähköiset sanomat \> Sanomien tilat**.
2. Luo seuraavat sanomien tilat:

    - Uusi
    - Valmisteltu
    - Luotu

    ![Sanomien tilat](media/message-statuses.png)

3. Valitse **Uusi**-tilan rivillä **Salli poistaminen** -valintaruutu, jolloin käyttäjät voivat päästää sanomia, joissa on tämä tila.

#### <a name="create-additional-fields"></a>Lisäkenttien luominen

1. Valitse **Vero \> Asetukset \> Sähköiset sanomat \> Lisäkentät**.
2. Lisää lisäkenttä ja sen arvot. Esimerkki:

    ![Lisäkentät](media/additional-fields.png)

3. Käyttäjät voivat muokata kenttään, jos määrität **Käyttäjän muokkaus** -asetukseksi **Kyllä**.

#### <a name="create-message-processing-actions"></a>Sanoman käsittelytoimintojen luominen

Tässä esimerkissä luodaan seuraavat toiminnot:

- **Luo viesti**
- **Päivitä tilaksi Valmisteltu**
- **Luo raportti**
- **Päivitä alkuperäiseen tilaan** (valinnainen)

1. Valitse **Vero \> Asetukset \> Sähköiset sanomat \> Sanoman käsittelytoiminnot**.
2. Luo toiminto, jonka nimi on **Luo viesti**. Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Luo viesti**.
3. Luo toiminto, jonka nimi on **Päivitä tilaksi Valmisteltu**, ja määritä seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Viestitason käyttäjän käsittely**.
    - Valitse **Alkuperäiset tilat** -pikavälilehden **Sanoman tila** -kentässä **Uusi**.
    - Valitse **Tulostilat**-pikavälilehden **Sanoman tila** -kentässä **Valmisteltu**. Anna **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

4. Luo toiminto, jonka nimi on **Luo raportti**, ja määritä seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Sähköisen raportoinnin vienti**. Valitse **Muodon määritys** -kentässä ER-vientimuoto. Vaihtoehdot ovat **Excel**, **XML**, **JSON**, **Teksti** ja **Muu**.
    - Valitse **Alkuperäiset tilat** -pikavälilehden **Sanoman tila** -kentässä **Valmisteltu**.
    - Valitse **Tulostilat**-pikavälilehden **Sanoman tila** -kentässä **Luotu**. Anna **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

    ![Luo raporttitoiminto](media/generate-report-action.png)

5. Valinnainen: käyttäjät voivat luoda raportin useita kertoja, kun luot **Päivitä alkuperäiseen tilaan** -toiminnon ja määrität seuraavat kentät:

    - Valitse **Yleinen**-pikavälilehden **Toimintotyyppi**-kentässä **Viestitason käyttäjän käsittely**.
    - Valitse **Alkuperäiset tilat**-pikavälilehden **Sanoman tila** -kentässä **Luotu**.
    - Valitse **Tulostilat**-pikavälilehden **Sanoman tila** -kentässä **Valmisteltu** tai (ja) **Uusi**. Anna **Vastaustyyppi**-kentässä **Suoritettu onnistuneesti**.

#### <a name="electronic-message-processing"></a>Sähköisen sanoman käsittely

Tässä esimerkissä kaikki toiminnot on määritettävä erikseen suoritettaviksi. Oletuksena on, että käyttäjän on käynnistettävä jokainen toiminto.

1. Valitse **Vero \> Asetukset \> Sähköiset sanomat \> Sähköisen sanoman käsittely**.
2. Lisää käsittelyn tietue sekä kaikki aiemmin määritetyt toiminnot ja lisäkenttä.
3. Valinnainen: määritä **Käyttöoikeusroolit**-pikavälilehdessä käsittelyn käyttöoikeusroolit rajoittamaan tietyn raportoinnin käyttöä.
4. Valitse **Vero \> Kyselyt ja raportit \> Sähköiset sanomat \> Sähköiset sanomat**.
5. Luo sanoma valitsemalla **Uusi**. Voit lisätä tässä vaiheessa päivämäärät ja kuvauksen. Voit myös päivittää lisäkentän arvon tarvittaessa.

    ![Luo sähköinen sanoma](media/create-electronic-message.png)

**Toimintoloki**-pikavälilehden ruudukko täytetään automaattisesti kaikkien sanomassa suoritettujen toimintojen lokilla.

Voit nyt joko poistaa tai päivittää sanoman tilan. Päivitä sanoman tila valitsemalla **Päivitä tila** ja sitten **Uusi tila** -kentässä **Valmisteltu**. Valitse sitten **OK**.

![Päivitä sanoman tila](media/update-status.png)

Sanoman tilaksi päivitetään **Valmisteltu**, ja voit nyt luoda raportin valitsemalla **Luo raportti**. Raportti luodaan sekä sanoman tila ja toimintoloki päivitetään. Voit tarkastella luotu raporttia valitsemalla toimintoruudussa **Liite**.
