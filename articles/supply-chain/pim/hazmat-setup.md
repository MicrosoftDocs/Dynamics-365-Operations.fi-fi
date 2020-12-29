---
title: Vaarallisten aineiden määrittäminen
description: Tässä ohjeaiheessa käsitellään sellaisten tietojen määrittämistä, joita tarvitaan nimikkeiden luokitteluun vaarallisiksi aineiksi. Kun luot myyntitilauksen, joka sisältää vaaralliseksi aineeksi luokitellun nimikkeen, järjestelmä luo kyseiselle myyntitilaukselle vaarallisen aineen ohjeet toimituksen yhteydessä.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b049559b64045e80a40afd99bac30a9cfe1d0580
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4427258"
---
# <a name="set-up-hazardous-materials"></a>Vaarallisten aineiden määrittäminen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Vaaralliset aineet -toiminnon käyttäminen edellyttää, että ensimmäiseksi määritetään tiedot, joilla nimikkeet luokitellaan vaarallisiksi aineiksi. Kun sitten luot myyntitilauksen, joka sisältää vaaralliseksi aineeksi luokitellun nimikkeen, järjestelmä luo kyseiselle myyntitilaukselle vaarallisen aineen ohjeet toimituksen yhteydessä.

## <a name="turn-on-the-hazardous-materials-feature-for-your-system"></a>Vaaralliset aineet -ominaisuuden ottaminen käyttöön järjestelmässä

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Tuotetietojen hallinta*
- **Toiminnon nimi:** *Vaarallisten aineiden tuotetiedot ja lähetysohjeet*

## <a name="hazardous-material-regulations"></a>Vaarallisia aineita koskevat määräykset

Vaarallisiin aineisiin liittyvien prosessien käyttöä varten on luotava ensin määräys. Määräykset määrittävät, miten tulostettu lähetysteksti luodaan nimikkeelle. Lisäksi ne määrittävät liitetyt toimitustavat.

Yleisiä määräyksiä:

- **ADR** – Vaarallisten tavaroiden kansainväliseen maantiekuljetukseen liittyviä säädöksiä
- **CFR 49** – Yhdysvaltojen vaarallisten tavaroiden kuljetusta koskevia säädöksiä
- **IMDG** – Merenkulun kansainvälinen vaarallisten tavaroiden koodeksi (IMDG)
- **IATA** – Kansainvälisin ilmakuljetusliiton (IATA) vaarallisten tavaroiden säädökset

Näiden määräysten avulla määritetään, mitkä tiedot näytetään, kun nimikkeen lähetysteksti tulostetaan. Voit määrittä kaikki noudatettavat määräykset.

> [!IMPORTANT]
> Vaarallisiin aineisiin liittyvien tietokoodien määritystoiminto ei tarkoita, että yritys noudattaa määräyksiä. Se on vain työkalu, jonka avulla voit muodostaa omia yritysprosesseja.

Yleensä määräys on saatavana kuljetustapaa varten, kuten vesi-, maantie- ja ilmakuljetuksia varten. Tämän vuoksi kukin määräys voidaan liittää toimitustapaan. Toimitustapaa käytetään, kun tietyt asiakirjat tulostetaan varastonhallinnassa. Kukin lähetys linkitetään varastonhallinnassa lähetyksen rahdinkuljettajaan ja rahdinkuljetuspalveluun, jotka määritetään **Kuljetus**-moduulissa. Toimitustapa liitetään lähetyksen rahdinkuljettajaan ja rahdinkuljetuspalveluun. Kun raportti suoritetaan, toimitustavan avulla etsitään vapautettuun nimikkeeseen liitetty tulostettava lähetysteksti.

Nämä määritystiedot eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteiset vaarallisten aineiden tiedot.

Voit määrittää kullekin määräykselle materiaaliluettelon ja käyttää sitä vapautettuihin nimikkeisiin liitettävänä malliluettelona. Voit määrittää kullekin määräykselle myös tulostusasetukset. Voit määrittää tulostusasetusten avulla, miten nimikkeen lähetysteksti luodaan. Tulostusasetusten avulla muodostetaan vapautetun nimikkeen tulostettavan lähetysteksti.

Voit määrittää vaarallisten aineiden määräykset valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden määräys**. Voit luoda **Vaarallisten aineiden määräys** -sivulla niin monta määräystä kuin haluat ja määrittää niistä jokaisen seuraavissa alaosissa käsiteltyjen kenttien avulla.

### <a name="hazardous-material-regulation-header"></a>Vaarallisia aineita koskevan määräyksen otsikko

Kullakin määräyksellä on koodi ja kuvaus. Seuraavassa taulukossa käsitellään otsikossa valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Sääntelykoodi | Anna koodi, jolla vaarallisten aineiden määräystietue tunnistetaan. |
| kuvaus | Anna vaarallisten aineiden määräyksen kuvaus. |

### <a name="print-setup-fasttab"></a>Tulostusasetukset-pikavälilehti

Kullakin määräyksellä voi olla haluttu määrä tulostusasetuksia. Tulostusasetukset määritetään **Tulostusasetukset**-pikavälilehdessä. Seuraavassa taulukossa käsitellään kussakin tulostusasetuksessa valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Järjestys | Määritä järjestys, jossa kenttiin viitataan lähetystekstissä. |
| Tulosta kenttä | Valitse lähetystekstiin sisällytettävä kenttä. Kaikki vaarallisten aineiden kentät eivät ole tulostettavissa. Vain yleiset kentät, joilla määritetään eri määräysten lähetysteksti, ovat käytettävissä. Määritä ensimmäinen tulostettava kenttä kenttäerottimena, jonka **Järjestys**-arvo on *0* (nolla), jolloin sitä voi käyttää erottamaan muita kenttiä. Kenttäerottimeen tarvitaan vain yksi viittaus.<p>Käytettävissä ovat seuraavat arvot:</p><ul></li><li>**Kenttäerotin**– Tätä tulostuskenttää käytetään tekstin kenttäerottimena. Järjestyksessä tarvitaan vain yksi kenttäerotin. Yleensä tämän tulostuskentän **Järjestys**-arvoksi on määritettävä *0* (nolla). Järjestelmä etsii kenttäerottimen ja käyttää ensimmäistä, jonka se löytää luettelossa. Merkkijonossa käytettävä tekstiarvo saadaan **Tulostus jälkeen** -kentästä.</li><li>**Tunnus** – tämä tulostuskenttä lisää [tunnistuskoodin ja/tai kuvauksen](#identification) tulostustekstiin.</li><li>**Luokka** – tämä tulostuskenttä lisää [luokkakoodin ja/tai kuvauksen](#classes) tulostustekstiin.</li><li>**Jako** – tämä tulostuskenttä lisää [jakokoodin ja/tai kuvauksen](#divisions) tulostustekstiin.</li><li>**Pakkausryhmä** – tämä tulostuskenttä lisää [pakkausryhmäkoodin ja/tai kuvauksen](#packing-group) tulostustekstiin.</li><li>**Tunnelikoodi ja/tai kuvaus** – tämä tulostuskenttä lisää [tunnelikoodin ja/tai kuvauksen](#tunnel) tulostustekstiin.</li><li>**Varsinainen lähetyksen nimi** – tämä tulostuskenttä lisää [varsinaisen lähetyksen nimen](hazmat-items.md#hazmat-description) tulostustekstiin.</li><li>**Tekninen nimi** – tämä tulostuskenttä lisää [teknisen nimen ja/tai kuvauksen](#technical-name) tulostustekstiin.</li><li>**Kuljetusluokka** – tämä tulostuskenttä lisää [kuljetusluokkakoodin ja/tai kuvauksen](#transport-category) tulostustekstiin.</li><li>**Lastaus** – tämä tulostuskenttä lisää [lastauskoodin ja/tai kuvauksen](#stowage) tulostustekstiin.</li><li>**Kiinteä teksti** – tämä tulostuskenttä lisää tekstin, joka on määritetty tälle riville **Kiinteä teksti**-kentässä.</li><li>**Selitekoodi ja/tai kuvaus** – tämä tulostuskenttä lisää [selitekoodin ja/tai kuvauksen](#label) tulostustekstiin.</li><li>**Lentorahtipakkaus** – tämä tulostuskenttä lisää [lentorahtipakkauksen ohjeiden koodin ja/tai kuvauksen](#packing-instruction) tulostustekstiin.</li><li>**Rajoitettu määrä** – tämä kenttä tarkistaa, onko nimike merkitty [rajoitetun määrän nimikkeeksi](hazmat-items.md#material-management) ja jos on, lisää tämän rivin **Kiinteä teksti**-kentässä määritetyn tekstin.</li><li>**Pakkauksen kuvaus** – tämä tulostuskenttä lisää [pakkauksen kuvauksen](#packing-description) tulostustekstiin.</li></ul> |
| Tulosta ennen | Anna teksti, joka on tulostettava ennen **Tulostuskenttä**-asetuksessa määritettyä sisältöä. |
| Tulosta jälkeen | Anna teksti, joka on tulostettava **Tulostuskenttä**-asetuksessa määritetyn sisällön jälkeen. |
| Tulosta edellisen kanssa | Valitsemalla tämän valintaruudun voit estää kenttäerottimen tulostamisen edellisen kentän ja tämän kentän väliin. Valitse tämä valintaruutu joko valinnaisten tulostuskenttien tai toiseen tulostuskenttään sisältyvien kenttien yhteydessä. |
| Kiinteä teksti | Jos **Tulostuskenttä**-kentän asetuksena on **Kiinteä teksti** tai **Rajoitettu määrä**, anna tulostettava teksti. |
| Sisällytä tulostukseen | Valitse, mitkä valitun tulostuskentän arvot tulostetaan tälle riville. Voit tulostaa koodin, kuvauksen tai sekä koodin että kuvauksen. |

### <a name="mode-of-delivery-fasttab"></a>Toimitustapa-pikavälilehti

Määräys on jaettu taulukko, joka ei se ole yrityskohtainen. Toimitustavat ovat kuitenkin yrityskohtaisia. Niinpä toimitustapaa määritettäessä on valittava määräyksen, yrityksen ja toimitustavan välinen suhde.

Seuraavassa taulukossa käsitellään **Toimitustapa**-pikavälilehdessä valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Yhtiö | Valitse tähän määräykseen liitettävä yritys. |
| Toimitustapa | Valitse valitun yrityksen perusteella määräykseen liitettävä toimitustapa. |

### <a name="country-fasttab"></a>Maa-pikavälilehti

Viitteeksi voidaan määrittää maat tai alueet, joita määräys koskee. Kun lähetysraportteja suoritetaan, vain toimitustapaa käytetään määräyksen määrittämiseen. Kun tarkastelet varastolähetystä, toimitustapaan ei ole suoraa linkkiä. Lähetys voidaan liittää lähetyksen rahdinkuljettajaan ja rahdinkuljetuspalveluun. Kun rahdinkuljetuspalvelu määritetään, se on liitettävä toimitustapaan. Tätä suhdetta käytetään lähetysraporteissa, kuten rahtikirjassa, nimikkeen tulostettavan lähetystekstin löytämiseen.

Seuraavassa taulukossa käsitellään **Maa**-pikavälilehdessä valittavana oleva kenttä.

| Kenttä | kuvaus |
|---|---|
| Maa/alue | Valitse määräykseen liitettävä maa tai alue. |

## <a name="material-codes"></a><a name="hazmat-codes"></a>Materiaalikoodit

Materiaalikoodit muodostavat asetukset, jotka liittyvät tiettyyn vaaralliseen osaan, joka voi sisältyä vapautettuun tuotteeseen. Kukin materiaalikoodi kuuluu tiettyyn vaarallisten aineiden määräykseen, ja sen määrityksen on oltava kyseisen määräyksen mukainen. Kun materiaalikoodi otetaan käyttöön vapautetussa tuotteessa käyttämällä **Materiaalikoodi**-kentässä, kaikkia materiaalikoodin vaarallisten aineiden asetuksia käytetään automaattisesti kyseisessä tuotteessa. Tämän vuoksi vapautettujen tuotteiden määritysprosessi nopeutuu eikä siinä esiinny yhtä paljon virheitä.

Vaarallisten aineiden määritelmiä hallitaan seuraavasti:

1. Valitse **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden määräys**.
2. Valitse määräys, jolle vaarallisten aineiden määräys määritetään.
3. Valitse toimintoruudun **Asetukset**-välilehdessä **Vaaralliset aineet**.
4. Anna **Materiaalikoodi**-kentässä vaarallisen aineen määritelmän materiaalikoodi. Tämä arvo valitaan, kun materiaalikoodia käytetään vapautetussa tuotteessa.

    **Määräyksen koodi** -kenttä on vain luku -muotoinen ja siinä näkyy, vaiheessa 2 valittu määräys.

5. Tämän sivun jäljellä olevien kenttien avulla voi luoda ja määrittää kunkin vaarallisen aineen, joka koskee valittua määräystä. Käytettävissä olevat kentät ovat niiden vaarallisten aineiden kenttien alijoukko, jotka ovat käytettävissä yksittäisissä vapautetuissa tuotteissa. Lisätietoja on kohdassa [Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet](hazmat-items.md).

## <a name="hazardous-material-classification-groups"></a><a name="classification-groups"></a>Vaarallisten aineiden luokitteluryhmät

Kukin vaarallisten aineiden luokitteluryhmä määrittää kenttäarvojen ryhmän, jotka muodostavat mallin. Voit käyttää tätä mallia myöhemmin, kun määrität vapautetun nimikkeen vaarallisten aineiden tiedot.

Kun vaarallisten aineiden luokitteluryhmän koodi määritetään vapautetulle nimikkeelle, kyseiseen luokitteluryhmään liitetyt tiedot kopioidaan nimikkeen soveltuviin kenttiin. Niinpä voit yksinkertaistaa määritysprosesseja muodostamalla usein yhdessä käytettyjen liittyvien kenttäarvojen joukon.

Nämä määritystiedot eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteiset vaarallisten aineiden tiedot.

Voit määrittää vaarallisten aineiden luokitteluryhmät valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden luokitteluryhmä**. Voit luoda **Vaarallisten aineiden luokitteluryhmä** -sivulla niin monta ryhmää kuin haluat ja määrittää niistä jokaisen seuraavassa taulukossa käsiteltyjen kenttien avulla.

| Kenttä | kuvaus |
|---|---|
| Ryhmäkoodi | Anna ryhmän yksilöivä koodi. |
| kuvaus | Anna ryhmän kuvaus. |
| Luokkakoodi | Liitä vaarallisten aineiden [luokkakoodi](#classes) ryhmään. |
| Jakokoodi | Liitä vaarallisten aineiden [jakokoodi](#divisions) ryhmään. |
| Pakkausryhmän koodi | Liitä [pakkausryhmäkoodi](#packing-group) ryhmään. |
| Kuljetusluokan koodi | Liitä [kuljetusluokkakoodi](#transport-category) ryhmään. |
| Kerroin | Anna vaarallisten aineiden kerroin, jota käytetään vaarallisten aineiden valittuun luokkaan ja jakoon sovellettavan määräyksen mukaan. Tätä kerrointa käytetään sen kaavan osana, joka laskee kuormaan tai lähetykseen sisältyvien *vaarallisten aineiden kokonaispistemäärän*. Lisätietoja vaarallisten aineiden pisteistä ja kertoimesta on kohdassa [Materiaalien hallinta -pikavälilehti](hazmat-items.md#material-management). |

## <a name="hazardous-material-classes"></a><a name="classes"></a>Vaarallisten aineiden luokat

Vaarallisten aineiden luokka yhdistetään tyypillisesti luokkaluetteloon, joka annetaan noudatettavassa määräyksessä. Yhdysvaltalaisessa säädöksessä CFR 49 luokassa 3 luokitellaan tulenarat ja syttyvät nesteet. Voit määrittää luokat, jotka liittyvät luokiteltaviin materiaaleihin.

Kukin luokka liitetään materiaalimääritykseen määräykseen liittyvässä materiaaliluettelossa. Luokka määritetään tarpeen mukaan kullekin vapautetulle nimikkeelle kuvailemaan tuotteen vaarallisia ominaisuuksia.

Nämä määritystiedot eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteiset vaarallisten aineiden tiedot.

Vaarallisten aineiden luokkia käytetään yhdessä jakojen, ryhmien ja yhteensopivuusryhmien kanssa seuraavasti:

- Kun vapautetulle nimikkeelle määritetään vaarallisten aineiden luokka, myös [vaarallisten aineiden jako](#divisions) on määritettävä.
- Voit käyttää vaarallisten aineiden luokkia yhdessä [vaarallisten aineiden luokitteluryhmien](#classification-groups) kanssa, joilla voi sitten muodostaa nimikkeen määrittämiseen tarvittavan koodimallin.
- Voit käyttää [vaarallisten aineiden yhteensopivuusryhmiä](#compatibility-groups) määrittämään, mitkä vaarallisten aineiden luokat ja jaot voidaan lähettää yhdessä.

Voit määrittää vaarallisten aineiden luokat valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden luokka**. Voit luoda **Vaarallisten aineiden luokka** -sivulla niin monta luokkaa kuin haluat ja määrittää niistä jokaisen seuraavassa taulukossa käsiteltyjen kenttien avulla.

| Kenttä | kuvaus |
|---|---|
| Luokkakoodi | Anna luokan yksilöivä koodi. Tämä koodi määritetään nimikkeelle. Sitä käytetään sitten valintaluetteloissa, kun vaarallisten aineiden luokka määritetään vapautetulle nimikkeelle. |
| kuvaus | Anna luokan kuvaus. |

## <a name="hazardous-material-divisions"></a><a name="divisions"></a>Vaarallisten aineiden jaot

Vaarallisten aineiden jako on vaarallisten aineiden luokan alijoukko. Jokaiselle vaarallisia aineita sisältävälle tuotteelle on määritettävä sekä jako että luokka.

Jos luokassa ei ole jakoja, luo jako, jonka koodi on *0*. Esimerkiksi IATA-määräyksessä luokan 7 radioaktiivisissa materiaaleissa ei ole alajakoja. Luo siinä tapauksessa *0*-jako, jonka voi liittää vapautettuun tuotteeseen luokkaa määritettäessä.

Nämä määritystiedot eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteiset vaarallisten aineiden tiedot.

Vaarallisten aineiden jakoja käytetään yhdessä luokkien, ryhmien ja yhteensopivuusryhmien kanssa seuraavasti:

- Kun vapautetulle nimikkeelle määritetään vaarallisten aineiden jako, myös [vaarallisten aineiden luokka](#classes) on määritettävä.
- Voit käyttää vaarallisten aineiden jakoja yhdessä [vaarallisten aineiden luokitteluryhmien](#classification-groups) kanssa, joilla voi sitten muodostaa nimikkeen määrittämiseen tarvittavan koodimallin.
- Voit käyttää [vaarallisten aineiden yhteensopivuusryhmiä](#compatibility-groups) määrittämään, mitkä vaarallisten aineiden luokat ja jaot voidaan lähettää yhdessä.

Voit määrittää vaarallisten aineiden jaot valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden jako**. Voit luoda **Vaarallisten aineiden jako** -sivulla niin monta jakoa kuin haluat ja määrittää niistä jokaisen seuraavassa taulukossa käsiteltyjen kenttien avulla.

| Kenttä | kuvaus |
|---|---|
| Jaosto | Anna koodi, jota käytetään jaon viitenumerona. |
| kuvaus | Anna jaon kuvaus. |
| Luokka | Etsi ja määritä luokka, johon jako kuuluu. |

## <a name="hazardous-material-compatibility-groups"></a><a name="compatibility-groups"></a>Vaarallisten aineiden yhteensopivuusryhmät

Vaarallisten aineiden yhteensopivuusryhmät määrittävät, mitkä vaarallisten aineiden luokat ja jaot voidaan lähettää yhdessä. Kun käyttäjät luovat varaston kuormia tai lähetyksiä, he voivat suorittaa yhteensopivuustarkistuksen, joka antaa varoituksen, jos kuorma tai lähetys sisältää nimikkeitä, jotka eivät kuulu samaan yhteensopivuusryhmään.

Nämä määritystiedot eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteiset vaarallisten aineiden tiedot.

Voit määrittää vaarallisten aineiden yhteensopivuusryhmät valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden yhteensopivuusryhmä**. Voit luoda **Vaarallisten aineiden yhteensopivuusryhmä** -sivulla niin monta yhteensopivuusryhmää kuin haluat ja määrittää niistä jokaisen seuraavissa alaosissa käsiteltyjen kenttien avulla.

### <a name="hazardous-material-compatibility-group-header"></a>Vaarallisten aineiden yhteensopivuusryhmän ylätunniste

Kullakin yhteensopivuusryhmällä on koodi ja kuvaus. Seuraavassa taulukossa käsitellään otsikossa valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Yhteensopivuusryhmä | Anna yhteensopivuusryhmän yksilöivä koodi |
| kuvaus | Anna yhteensopivuusryhmän kuvaus. |

### <a name="compatibility-group-details"></a>Yhteensopivuusryhmän tiedot

Kukin yhteensopivuusryhmät määrittää luettelon vaarallisten aineiden luokista ja jaoista, jotka voidaan lähettää yhdessä.

| Kenttä | kuvaus |
|---|---|
| Luokka | Valitse vaarallisten aineiden luokka, joka on yhteensopiva muiden ryhmän luokkien kanssa. |
| Jaosto | Valitse vaarallisten aineiden jako, joka kuuluu valittuun luokkaan. |

## <a name="hazardous-material-specification-values"></a>Vaarallisten aineiden määritysten arvot

Microsoft Dynamics 365 Supply Chain Management sisältää useita vaarallisten aineiden määritystyyppejä. Kullekin tyypille on määritettävä keskitetty arvojoukko kunkin soveltuvan kentän osalta. Käyttäjät voivat sitten valita jonkin näistä arvoista, kun he määrittävät vaarallisten aineiden määritelmiä tai vapautettuja tuotteita. Supply Chain Management sisältää sivukokoelman, jossa voi muodostaa arvoja. Kukin sivu on varattu yhdelle määritystyypille. Seuraavissa alaosissa on kuvaus kustakin käytettävissä olevasta määrityksestä ja tietoja tavasta, jolla voidaan muodostaa siinä käytettävissä olevia arvoja.

Yksi esimerkki vaarallisten aineiden määrityksestä on _lastauskoodi_, joka määrittää, miten tiettyä materiaalia säilytetään kuljetuksen aikana. Voit määrittää tämän osan tietojen avulla keskitetyn lastauskoodikokoelman. Tämä kokoelma näytetään sitten käyttäjille avattavana luettelona, kun he määrittävät vapautetun tuotteen lastauskoodin.

Nämä vaarallisten aineiden määrityskoodit eivät ole yrityskohtaisia. Tämän vuoksi kaikki yritykset voivat jakaa yhteisen arvojoukon.

[Materiaalikoodien](#hazmat-codes) avulla kullekin määritykselle voi määrittää yhteisen tietyssä määräyksessä käytettävän asetuskokoelman. Voit sitten käyttää tarpeen mukaan sopivaa koodia kussakin vapautetussa tuotteessa. Lisätietoja vaarallisten aineiden koodin käyttämisestä tietyssä vapautetussa tuotteessa ja kyseisen tuotteen yksittäisten asetusten määrittämisestä jonkin tässä kuvatun määrityksen osalta on kohdassa [Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet](hazmat-items.md).

### <a name="hazardous-material-emergency-response"></a>Vaarallisten materiaalien hätätilannevastaus

*Vaarallisten aineiden hätätilannevastaus* -määritys ilmaisee, mitä on tehtävä, jos jokin menee vikaan kuljetettaessa tiettyä vaarallista ainetta sisältävää tuotetta.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden hätätilannevastaus**. Voit luoda **Vaarallisten aineiden hätätilannevastaus** -sivulla haluamasi määrän arvoja ja määrittää kullekin luokittelukoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-identification"></a><a name="identification"></a>Vaarallisen materiaalin tunnistus

*Vaarallisten aineiden tunnistus* -määritys määrittää vaarallisen aineen luokan tai luonteen. Tämä arvo on tyypillisesti koodi, joka perustuu Yhdistyneiden kansakuntien (YK) standardiin. Kullakin luokalla on koodi ja kuvaus, ja se voi määrittää rajoituksia kuljetustavoille. Esimerkiksi tulenarka nimike tai materiaali määritetään luomalla vaarallisten aineiden luokka, joka käyttää koodia *TA* ja kuvausta *Tulenarka*. Voit myös määrittää, että luokkaa ei saa kuljettaa ilmateitse.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen tunnistus**. Voit luoda **Vaarallisen aineen tunnistus** -sivulla niin monta arvoa kuin haluat ja määrittää niistä jokaisen seuraavassa taulukossa käsiteltyjen kenttien avulla.

| Kenttä | kuvaus |
|---|---|
| Tunnus | Anna koodi, jota käytetään vaarallisen aineen luokan määrittävänä viitenumerona. |
| kuvaus | Anna luokan kuvaus. |
| Ilmakuljetusten rajoitus | Tämän valintaruutu ilmaisee, että tätä vaarallisen aineen luokkaa ei saa kuljettaa lentorahtina. |
| Merikuljetusten rajoitus | Tämän valintaruutu ilmaisee, että tätä vaarallisen aineen luokkaa ei saa kuljettaa laivarahtina. |

### <a name="hazardous-material-label"></a><a name="label"></a>Vaarallisen materiaalin etiketti

*Vaarallisen aineen etiketti* -määritys määrittää vaarallisten tavaroiden etiketin, jota on käytettävä soveltuvissa vapautetuissa tuotteissa. Etiketeissä puolestaan kuvataan, miten tuotetta on käsiteltävä. Tuote voi esimerkiksi sisältää myrkyllistä kaasua. Siinä tapauksessa määritetään myrkyllisen kaasun etikettiä vastaava etikettikoodi. Voit myös muodostaa liiketoimintaprosessin siten, että se hakee tämän arvon tuotteita lähetettäessä.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen etiketti**. Voit luoda **Vaarallisen aineen etiketti** -sivulla haluamasi määrän etikettejä ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-packing-descriptions"></a><a name="packing-description"></a>Vaarallisten materiaalien pakkauskuvaukset

*Vaarallisten aineiden pakkauskuvaukset* -määritys ilmaisee, miten vaarallinen nimike on pakattava. Se on esimerkiksi ehkä pakattava tietyn tyyppiseen terästynnyriin tai muun tyyppiseen erikoispakkaukseen.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden pakkauskuvaukset**. Voit luoda **Vaarallisten aineiden pakkauskuvaukset** -sivulla haluamasi määrän pakkauskuvauksia ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-packing-group"></a><a name="packing-group"></a>Vaarallisen materiaalin pakkausryhmä

*Vaarallisen aineen pakkausryhmä* -määritys määrittää vaarallisen nimikkeen pakkausryhmän. Pakkausryhmän avulla voi määrittää koodin ja kuvauksen ilmaisemaan, miten vaarallisten aineiden nimikkeet on pakattava kuljetuksen tai lähetyksen aikana. Pakkausryhmä määritetään nimikkeelle **Nimikkeen vaaralliset aineet** -sivulla.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen pakkausryhmä**. Voit luoda **Vaarallisen aineen pakkausryhmä** -sivulla haluamasi määrän pakkausryhmiä ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-packing-instruction"></a><a name="packing-instruction"></a>Vaarallisen materiaalin pakkausohje

*Vaarallisen aineen pakkausohje* -määritys määrittää pakkausohjeet, joita on noudatettava, kun tietty vaarallinen nimike valmistellaan lentorahtia varten.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen pakkausohje**. Voit luoda **Vaarallisen aineen pakkausohje** -sivulla haluamasi määrän pakkausohjetunnuksia ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-stowage"></a><a name="stowage"></a>Vaarallisen materiaalin ahtaus

*Vaarallisen aineen lastaus* -määritys ilmaisee, miten tuote on lastattava laivaan, kun se kuljetaan laivarahtina.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen lastaus**. Voit luoda **Vaarallisen aineen lastaus** -sivulla haluamasi määrän lastaustunnuksia ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.

### <a name="hazardous-material-transport-category"></a><a name="transport-category"></a>Vaarallisten materiaalien kuljetusluokka

*Vaarallisten aineiden kuljetusluokka* -määritystä käytetään tyypillisesti ryhmittelemään samankaltaisia vaarallisia tuotteita raporteissa. Kuljetusluokkia käytetään esimerkiksi **Lähetyksen yhteenveto** -raportissa, joka voidaan tulostaa varaston lähetystietueesta.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden kuljetusluokka**. Voit luoda **Vaarallisten aineiden kuljetusluokka** -sivulla haluamasi määrän kuljetusluokkia ja määrittää kullekin näyttönimen ja lyhyen kuvauksen.

### <a name="hazardous-material-technical-name"></a><a name="technical-name"></a>Vaarallisen materiaalin tekninen nimi

*Vaarallisen aineen tekninen nimi* -määrityksellä voi antaa yleisesti käytetyn tai yrityksen sisäisen nimen, joka kuvaa kutakin materiaalia.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisen aineen tekninen nimi**. Voit luoda **Vaarallisen aineen tekninen nimi** -sivulla haluamasi määrän teknisiä nimiä ja määrittää kullekin näyttönimen ja lyhyen kuvauksen.

### <a name="hazardous-material-tunnel"></a><a name="tunnel"></a>Vaarallisten materiaalien tunneli

*Vaarallisten aineiden tunneli* -määritys rajoittaa tunnelityyppejä, joiden kautta vaarallisia aineita voidaan kuljettaa, määrittämällä käytettävät tunnelityypit. Tunneliluokat luodaan vaarallisten aineiden kuljetuksen sovellettavien määräysten mukaan. Tätä määritystä käytetään yleensä vain maantiekuljetuksissa.

Voit määrittää tämän määrityksen valitsemalla **Tuotetietojen hallinta \> Asetukset \> Vaarallisten aineiden lähetysohjeet \> Vaarallisten aineiden tunneli**. Voit luoda **Vaarallisten aineiden tunneli** -sivulla haluamasi määrän tunnelitunnuksia ja määrittää kullekin tunnistuskoodin ja lyhyen kuvauksen.
