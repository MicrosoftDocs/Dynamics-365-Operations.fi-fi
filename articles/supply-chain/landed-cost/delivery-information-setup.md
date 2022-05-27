---
title: Toimitustietojen asetukset
description: Tässä aiheessa kuvataan, miten toimitustiedot määritetään Aiheutunut kustannus -moduulia varten.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a0b510e4f58ca1cfec940093d118618693c68d38
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694680"
---
# <a name="delivery-information-setup"></a>Toimitustietojen asetukset

[!include [banner](../../includes/banner.md)]

Tässä aiheessa kuvataan, miten toimitustiedot määritetään **Aiheutunut kustannus** -moduulia varten.

## <a name="shipping-ports"></a>Lähetyssatamat

Lähetyssatamat osoittavat, mistä ja minne tuotteita lähetetään. Jokaiselle merikuljetukselle määritetään lähtö- ja kohdesatamat kontille valitun matkan perusteella. Lähetyssatamia käytetään matkan etappien ja merikuljetuksen tehtävien muodostamiseen. Ne määritetään tavallisesti käyttämällä fyysisen lähetyssataman kaupungin ja maan tai alueen nimeä.

Voit työstää lähetyssatamia valitsemalla **Aiheutunut kustannus \> Toimitustietojen asetukset \> Lähetyssatamat**. Tältä sivulta voit tarkastella, lisätä ja poistaa lähetyssatamiesi tietueita. Seuraavassa taulukossa kuvataan kentät, jotka ovat käytettävissä kullekin tietueelle.

| Kenttä | kuvaus |
|---|---|
| Lähetyssatama | Syötä lähetyssatamalle yksilöllinen nimi/numero. |
| kuvaus | Syötä lähetyssataman kuvaus. |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a>Seurannan ohjauskeskus

Käytä seurannan ohjauskeskusta määrittääksesi merikuljetukseen liittyvät läpimenoajat, tilapäivitykset ja tiedonkulun, kun kontit etenevät epatista toiseen. Kun luot seurantatietueen, se liitetään merikuljetuksen matkan tiettyyn etappiin. Kun merikuljetus päivittää etapin, siihen liittyvä tietue päivitetään ja täytetään määritysten mukaisesti. Voit päivittää yksittäisten merikuljetusten seurantatiedot **Kaikki merikuljetukset** -sivulta.

Voit avata seurannan ohjauskeskuksen valitsemalla **Aiheutunut kustannut \> Toimitustietojen asetukset \> Seurannan ohjauskeskus**.

Seurannan ohjauskeskus näyttää yhden kolmesta sivunäkymästä, riippuen luetteloruudun **Luontityyppi**-kentässä valitusta arvosta: *Tyhjä*, *Läpimenoaika* tai *Tilapäivitys*. Jokainen luontityppi päivittää eri tietojoukon, joka liittyy merikuljetuksen etenemiseen lähtöpisteestä lopulliseen määränpäähän.

### <a name="common-rule-settings"></a>Yhteiset sääntöjen asetukset

Seuraavassa taulukossa näytetään kentät, jotka ovat käytettävissä kaikille kolmelle luontityypille seurannan ohjauskeskuksessa.

| Kenttä | kuvaus |
|---|---|
| Lähdetaulukko, Lähdekenttä | Nämä kentät osoittavat tietokannassa olevan lähdetaulukon ja -kentän. Sääntö lataa kentän arvon ja käyttää sitä sitten säännön muiden asetusten määrittämällä tavalla. |
| Kohdetaulukko, Kohdekenttä | Nämä kentät osoittavat tietokannassa olevan kohdetaulukon ja -kentän. Sääntö lataa kentän arvon ja sitten käyttää sitä (tai korvaa sen) säännön muiden asetusten määrittämällä tavalla. |
| Tehtävä | Tämä kenttä osoittaa tehtävätyypin, joka tulisi lisätä säännön määrittämälle kontille. |
| Vastaavuusehdot | Tämä kenttä määrittää, miten järjestelmä tunnistaa vastaavuuden säännöllä. Järjestelmä tarkistaa jokaisessa esiintymässä lähde- ja kohdetaulukoiden tiedot määrittääkseen, tulisiko kohdetaulussa kenttä päivittää ja milloin.<p>Tässä esimerkissä lähdetaulukko on *Merikuljetukset* ja kohdetaulukko *Ostotilaus* tai *Ostorivit*. *Merikuljetukset*-taulukon **Lähtösatama**-arvo on *Hongkong* ja *Ostotilaus*-taulukon **Lähtösatama**-arvo on *Shanghai*. Järjestelmä luo säännön, jonka lähtösatama on *Hongkong*. Tässä tapauksessa **Vastaavuusehdot**-kentän arvot toimivat näin:</p><ul><li>**Molemmat** – Kohdekenttää ei päivitetä, koska satamat eivät vastaa toisiaan.</li><li>**Lähde** – Kohdekenttä päivitetään, koska lähdetaulukon lähtösatama on *Hongkong*.</li><li>**Kohde** – Kohdekenttää ei päivitetä, koska kohdetaulukon lähtösatama on *Shanghai* (eikä *Hongkong*).</li></ul> |
| Kopioi toiminto | Käytettävissä olevat arvot ovat *Kopioi* ja *Oletus*. Valitse *Kopioi* kopioidaksesi lähdekentän arvon kohdekenttään. Valitse *Oletus* määrittääksesi kohdekentälle staattisen arvon. |
| Oletus | Kun **Kopioi toiminto** -kentän arvoksi on määritetty *Oletus*, **Oletus**-kenttä määrittää kohdekentän oletusarvon. Jos toiminto liittyy esimerkiksi sataman päivitykseen ja **Kopioi toiminto** -kentän arvoksi on määritetty *Oletus*, **Oletus**-kenttä määrittää sataman. |
| Etappi | Tämä kenttä osoittaa matkan etapin, jolle määritetty toiminto, esimerkiksi lastaus tai tulli, tapahtuu. |
| Palvelun tarjoaja | Jos matkan tämänhetkiselle tilapäivitykselle/etapille käytetään tiettyä palveluntarjoajaa, tämä kenttä osoittaa palveluntarjoajan. Palveluntarjoajat on määritetty toimittajatilissä. |

### <a name="lead-time-rules"></a>Läpimenoaikojen säännöt

Läpimenoaika on arvioitu aika, jonka merikuljetus tarvitsee matkan määritetyn etapin suorittamiseen merikuljetukselle. Matkan kunkin etapin läpimenoaikaa käytetään merikuljetuksen arvioidun toimituspäivän laskemiseen. Sen jälkeen tämä päivämäärä syötetään merikuljetuksen jokaisen ostorivin **Vahvistettu toimituspäivä** -kenttään.

Läpimenoaikojen sääntöjä käytetään päivämäärien päivitysten hallintaan. Tehtävät luodaan automaattisesti, kun merikuljetukselle käytetetään matkamallia.

Voit lisätä läpimenoaikojen säännön seurannan ohjauskeskukseen noudattamalla seuraavia ohjeita.

1. Noudata seuraavia ohjeita:

    - Valitse **Aiheutunut kustannus \> Monietappisen matkan määritys \> Etapit**. Valitse etappi, jolle haluat määrittää läpimenoajat, ja valitse sitten toimintoruudusta **Seurannan ohjauskeskus**. Seurannan ohjauskeskus lataa alustavasti valitun etapin tiedot.
    - Valitse **Aiheutunut kustannus \> Toimitustietojen asetukset \> Seurannan ohjauskeskus**. Sitten sinun on valittava etappi manuaalisesti tämän menettelyn vaiheessa 4.

1. Määritä luetteloruudussa **Luontityyppi**-kentän arvoksi *Läpimenoaika*.
1. Valitse toimintoruudussa **Uusi**.
1. Jos aloitit seurannan ohjauskeskuksesta vaiheessa 1, valitse **Etappi**-kentästä etappi, jolle haluat luoda läpimenoaikojen säännön. Jos aloitit **Etapit**-sivulta, **Etappi**-kenttä sisältää valmiiksi etapin, jonka valitsit ennen kuin avasit seurannan ohjauskeskuksen.

    Monet kentät määritetään automaattisesti **Etappi**-kentän perusteella seuraavalla tavalla:

    - **Lähdetaulukko:** *Konttitehtävät*
    - **Lähdekenttä:** *Alkamispäivä*
    - **Kohdetaulukko:** *Konttitehtävät*
    - **Kohdekenttä:** *Arvioitu päättymispäivä*

1. Valitse **Tehtävä**-kentästä tehtävä, jolle tämänhetkistä sääntöä tulisi käyttää.
1. Valitse **Läpimenoaika**-kentästä läpimenoaika (päivinä), jota tulisi käyttää, kun tämänhetkinen sääntö käynnistyy.

### <a name="status-update-rules"></a>Tilapäivitysten säännöt

Tietueet, joiden **Luontityyppi**-kentäksi on määritetty *Tilapäivitys*, päivittävät ostotilausrivien tilan tai merikuljetus-, kontti- tai pakkaustason tilan. Tilat voidaan määrittää erikseen. Käytä niitä kertoaksesi käyttäjälle tai osastolle merikuljetuksen edistymisestä (esimerkiksi vastaanotetuista asiakirjoista tai matkalla olevista tavaroista).

Kun **Luontityyppi**-kentän arvoksi on määritetty *Tilapäivitys*, seurannan ohjauskeskus sisältää **Rivit**-pikavälilehden, jossa voit määrittää kustannusalueen ja merikuljetuksen päivitetyn tilan. Oletetaan esimerkiksi, että sinulla on rivi, jossa **Kustannusalue**-kentän arvoksi on määritetty *Kontti* ja **Merikuljetuksen tila** -kentän arvoksi on määritetty *Tuotteet kuljetettavana*. Tällöin, kun tilaus suoritetaan määritetylle etapille, kontin **Merikuljetuksen tila** -kentän arvoksi päivitetään *Tuotteet kuljetettavana*.

Tilapäivitykset tarjoavat merikuljetuksen tilan kaikille merikuljetuksen riveille ja merikuljetukseen liittyville ostotilausriveille. Kun merikuljetus etenee matkallaan satamasta, meriteitse ja tullin läpi kohdevarastoon, merikuljetustietueen **Merikuljetuksen tila** -kenttä tarjoaa pikaisen katsauksen nimikkeiden senhetkisestä vaiheesta.

Voit lisätä tilapäivitysten säännön seurannan ohjauskeskukseen noudattamalla seuraavia ohjeita.

1. Noudata seuraavia ohjeita:

    - Valitse **Aiheutunut kustannus \> Monietappisen matkan määritys \> Etapit**. Valitse etappi, jolle haluat määrittää tilapäivityksen, ja valitse sitten toimintoruudusta **Seurannan ohjauskeskus**. Seurannan ohjauskeskus lataa alustavasti valitun etapin tiedot.
    - Valitse **Aiheutunut kustannus \> Toimitustietojen asetukset \> Seurannan ohjauskeskus**. Sitten sinun on valittava etappi manuaalisesti tämän menettelyn vaiheessa 4.

1. Määritä luetteloruudussa **Luontityyppi**-kentän arvoksi *Tilapäivitys*.
1. Valitse toimintoruudussa **Uusi**.
1. Jos aloitit seurannan ohjauskeskuksesta vaiheessa 1, valitse **Etappi**-kentästä etappi, jolle haluat luoda tilapäivitysten säännön. Jos aloitit **Etapit**-sivulta, **Etappi**-kenttä sisältää valmiiksi etapin, jonka valitsit ennen kuin avasit seurannan ohjauskeskuksen.

    Monet kentät määritetään automaattisesti **Etappi**-kentän perusteella seuraavalla tavalla:

    - **Lähdetaulukko:** *Konttitehtävät*
    - **Lähdekenttä:** *Todellinen päättymispäivä*
    - **Kohdetaulukko:** Tämä kenttä on tyhjä.
    - **Kohdekenttä:** Tämä kenttä on tyhjä.

1. Valitse **Tehtävä**-kentästä tehtävä, jolle sääntöäsi tulisi käyttää.
1. Syötä **Rivit**-pikavälilehteen jokaisen kustannusalueen tilapäivitykset.

### <a name="blank-type-rules"></a>Tyhjät säännöt

Voit käyttää tietueita, joiden **Luontityyppi**-arvo on *Tyhjä*, korvataksesi tai syöttääksesi kentän arvon toisen kentän tietojen perusteella. Aiheutunut kustannus -sivun kenttä korvaa Microsoft Dynamics 365 Supply Chain Managementin muilla alueilla olevat tiedot seurannan ohjauskeskuksessa määritettyjen sääntöjen perusteella.

1. Valitse **Aiheutunut kustannus \> Toimitustietojen asetukset \> Seurannan ohjauskeskus**.
1. Määritä luetteloruudussa **Luontityyppi**-kentän arvoksi *Tyhjä*.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä sääntösi edellyttämät lähde- ja kohdearvot, vastaavuusehdot, kopiointitoiminto ja muut asiaankuuluvat parametrit.

### <a name="required-tracking-control-setup"></a>Pakolliset seurannan ohjauksen asetukset

Jokaiselle matkamallille täytyy määrittää kaksi tietuetta seurannan ohjauskeskuksessa. Näiden molempien tietueiden **Luontityyppi**-arvo on *Tyhjä*, ja niitä käytetään kaikissa aiheutuneiden kustannusten toteutuksissa. Ne auttavat varmistamaan, että oston vahvistuspäivä ja kuljetettavien tavaroiden odotetut päivämäärät päivitetään merikuljetuksille ja niihin liittyville ostotilausriveille odotetulla tavalla.

Ensimmmäinen tietue tarvitaan ostosrivien päivittämiseen. Sillä on oltava seuraavat asetukset:

- **Lähdetaulukko:** *Konttitehtävät*
- **Lähdekenttä:** *Arvioitu päättymispäivä*
- **Kohdetaulukko:** *Ostorivit*
- **Lähdekenttä:** *Vahvistetus- tai toimituspäivä*

Toinen tietue tarvitaan kuljetettavien tavaroiden tapahtumien päivittämiseen. Sillä on oltava seuraavat asetukset:

- **Lähdetaulukko:** *Konttitehtävät*
- **Lähdekenttä:** *Arvioitu päättymispäivä*
- **Kohdetaulukko:** *Kuljetettavien tuotteiden tilaus*
- **Lähdekenttä:** *Odotettu päivämäärä*
