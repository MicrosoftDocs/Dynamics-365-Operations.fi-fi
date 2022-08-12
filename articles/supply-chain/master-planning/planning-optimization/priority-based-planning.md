---
title: Prioriteettipohjainen suunnittelu
description: Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin prioriteettipohjaista suunnitteluominaisuutta.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8f46a4d4e087a99c00ab7b4eabc74f60043cbf21
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186480"
---
# <a name="priority-based-planning"></a>Prioriteettipohjainen suunnittelu

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa käsitellään Microsoft Dynamics 365 Supply Chain Managementin prioriteettipohjaista suunnitteluominaisuutta. Tämä ominaisuus lisää kysyntäperustaisen suunnittelun tuen, mikä on yksi [kysyntäperustaisen tarvelaskennan (DDMRP)](ddmrp-overview.md) vaihe. Prioriteettipohjaisessa suunnittelussa suunnittelun optimointi voi luoda suunnittelun prioriteetteihin eikä tarvepäiviin perustuvia suunniteltuja tilauksia.

Prioriteettipohjaisessa suunnittelussa voidaan priorisoida täydennystilaukset, mikä varmistaa, että kiireinen tarve priorisoidaan vähemmän tärkeän tarpeen kustannuksella. Niinpä esimerkiksi negatiivisen varaston täydennystilaus priorisoidaan tavalliseen täydennyksen täyttötilaukseen nähden. Järjestelmä vo jakaa suuret tilaukset automaattisesti pienemmiksi tilauksiksi, joissa tilausrivit ryhmitellään prioriteetin mukaan. Sen jälkeen kaikki korkean prioriteetin tilaukset voidaan käsitellä ensin.

Seuraavasta videosta ominaisuudesta saa nopean yleiskäsityksen: [Suunnittelun optimoinnin tuki Dynamics 365 Supply Chain Managementin prioriteettipohjaisessa suunnittelussa](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Prioriteettipohjaisen suunnittelun ottaminen käyttöön järjestelmässä

Ennen kuin käytät tätä toimintoa, sen on oltava päällä järjestelmässäsi. Järjestelmänvalvojat voivat käyttää [toimintojen hallinnan](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) asetuksia ja tarkistaa toiminnon tilan sekä laittaa sen päälle tarvittaessa. **Ominaisuuksien hallinta** -työtilassa ominaisuus on luetteloitu seuraavalla tavalla:

- **Moduuli:** *Pääsuunnittelu*
- **Ominaisuuden nimi:** *Suunnittelun optimoinnin prioriteettipohjaisen tarvelaskennan tuki*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Missä ja miten suunnittelun prioriteetti määritetään

*Suunnittelun prioriteetin* tiedot kysynnästä ja tarjonnasta ovat keskeisessä asemassa prioriteettipohjaisessa suunnittelussa. Suunnittelun prioriteetti määrittää kysyntä- tai tarjontarivin tärkeyden. Suunnittelun optimointi käyttää sitä, kun **Kattavuuskoodi**-kentän asetuksena on *Prioriteetti*.

Suunnittelun prioriteetti on yleensä jokin luku (0–100), jossa 0 ilmaisee tärkeydeltään suurinta. Arvo näkyy ja määritetään **Suunnittelun prioriteetti** -kentässä. Tämä kenttä on seuraavilla sivuilla: **Kysynnän ennusteen rivit**, **Myyntitilauksen tiedot**, **Ostotilauksen tiedot**, **Siirtotilauksen tiedot** ja **Suunnitellun tilauksen tiedot**.

Kun soveltuvan nimikkeen tai kattavuusryhmän **Kattavuuskoodi**-kentän asetuksena on *Prioriteetti*, suunnittelun optimointi tasapainottaa tarjonnan ja kysynnän tarveperustaisen menetelmän avulla, kun se laskee suunnittelun prioriteetin sekä ottaa kunkin vapautetun tuotteen osalta huomioon arvot, jotka on määritetty **Nimikkeen kattavuus** -sivun **Minimi**-, **Uusintatilauspiste**- ja **Maksimi**-kenttiin.

> [!NOTE]
> *Prioriteetti*-arvon on **Kattavuuskoodi**-kentässä vain silloin, kun suunnittelun optimointi on otettu käyttöön.

Liittyvillä *suunnittelun prioriteettimalleilla* hallitaan suunnittelun prioriteettia ja jaetaan suunnitellut tilauksen prioriteettialueen mukaisesti. Lisäksi niiden avulla voidaan määrittää suunnittelun prioriteetin oletusarvot kullekin tarjonta- tai kysyntätyypillä sekä määrittää prioriteetin laskentatapa.

## <a name="types-of-priority-calculation-methods"></a>Prioriteetin laskentamenetelmätyypit

Kullakin suunnittelun prioriteettimallilla on **Prioriteetin laskentamenetelmä** -asetus. Sillä määritetään, miten pääsuunnittelu käyttää prioriteettia suunniteluissa tilauksissa. Käytettävissä on seuraavat arvot: *Prosenttia varaston enimmäismäärästä* ja *Prioriteettivälit*. *Prioriteettivälit* on *Prosenttia varaston enimmäismäärästä* -laskentamenetelmän edistynyt versio.

### <a name="percent-of-maximum-inventory-quantity"></a>Prosenttia varaston enimmäismäärästä

*Prosenttia varaston enimmäismäärästä* -laskentamenetelmässä tarjonnan prioriteettilaskelma etsii nykyisen *saatavilla oleva kokonaisvarasto* (nettovirran) nimikkeelle määritetyn **Varaston enimmäismäärä** -arvon prosenttiosuutena. Nimikkeelle ja toimittajalle luodaan sitten yksi suunniteltu tilaus (ellei maksimitilausmäärä pakota jakamaan tilauksen). Tilauksen suunnittelun prioriteetti lasketaan prosenttiosuutena maksimista.

Seuraavaa kaavaa käytetään:

*Prosenttia maksimista* = (*Nettovirran positio* × 100) ÷ *Varaston enimmäismäärän arvo nimikkeen kattavuudesta*

Tässä kaavassa *Nettovirran positio* lasketaan seuraavasti:

*Nettovirran positio* = *Käytettävissä oleva* + *Tilauksessa* – *Hyväksytty kysyntä*

- *Tilauksessa* on odotettu tarjonta.
- *Hyväksytty kysyntä* ilmaisee nettotarpeet, joiden tarvepäivä on suunnittelun aikarajan sisällä.

Pääsuunnitteluajon aikana luodaan uusia suunniteltuja tilauksia, kun nettovirran positio on pienempi kuin nimikkeen uusintatilauspisteen määrä. Suunnitellun tilauksen määrä on nimiketasolla määritettävän **Varaston enimmäismäärä** -arvon ja nettovirran position välinen ero. Suunnittelun tilauksen prioriteetti lasketaan **Varaston enimmäismäärä** -arvon *nettovirran position* prosenttiosuutena.

> [!NOTE]
> Laskettu prioriteetti ei voi olla negatiivinen edes silloin, kun kysyntä ylittää kokonaistarjonnan. Jos kysyntä ylittää kokonaistarjonnan, lasketuksi prioriteetiksi määritetään 0 (nolla).

### <a name="priority-ranges"></a>Prioriteettivälit

*Prioriteettivälit*-laskentamenetelmä on *Prosenttia varaston enimmäismäärästä* -laskentamenetelmä edistynyt versio, ja se määritetään suunnittelun prioriteettimallin tasolla. Useita uusia suunniteltuja toimitustilauksia voidaan luoda täyttämään nimikekohtainen kysyntä. Suunnittelun toimituksen prioriteetit noudattavat **Suunnittelun prioriteettimallit** -sivun **Suunnittelun prioriteettivälit** -ruudukossa määritettyjä arvoja.

Seuraavat lisäsäännöt otetaan käyttöön, kun **Prioriteetin laskentamenetelmä** -kentän asetuksena on *Prioriteettivälit*:

- Jos suunnitellun prioriteettimallin **Ota kysynnän prioriteetti huomioon** -vaihtoehdon asetuksena on *Kyllä*, kullekin kysyntäriville määritettävä prioriteetti rajoittaa prioriteettiväliä. Minkään suunnittelun toimitustilauksen prioriteetti ei voi olla pienempi kuin kysynnän prioriteetti. Alueen ylintä arvoa pidetään raja-arvona, johon kysynnän prioriteettiarvoa verrataan. Jos kysynnän prioriteetti on täsmälleen kahden alueen yläraja-arvon keskellä, se alue valitaan, jolla on korkein prioriteetti (eli pienin prioriteettiarvo).
- Jos suunnitellun prioriteettimallin **Suunnitellun tilauksen luonti** -kentän asetuksena on *Yksittäinen toimitus, jolla on ensisijainen prioriteetti*, vain yksi toimitus luodaan täyttämään maksimimäärään saakka. Prioriteetti määritetään ensimmäisen toimituksen käynnistävän alueen prioriteetin mukaan.
- Jos käytettävissä olevaa varastoa, toimitusta ja kysyntää ei ole, käytetään sitä **Suunnittelun prioriteettivälit** -ruudukon riviä, jossa **Määrästä**-kentän asetuksena on *Nolla*.
- Jos on kysyntää mutta ei käytettävissä olevaa varastoa tai odotettua toimitusta, käytetään sitä **Suunnittelun prioriteettivälit** -ruudukon riviä, jossa **Määrästä**-kentän asetuksena on *Nolla tai vähemmän*.
- Kun sitä aluetta, jonka osa kysyntä on, arvioidaan, **Ota kysynnän prioriteetti huomioon** -vaihtoehdon asetuksella on merkitystä.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Perinteisten aikajanalaskelmien ja prioriteettipohjaisen suunnittelun erot

Prioriteettipohjainen suunnittelu eroaa perinteisistä aikajanalaskelmista seuraavasti:

- Kaikkia tavallisia ennakkosuunnittelujen käsittelyjä käytetään edelleen. Näitä ennakkokäsittelyjä ovat muun muassa hyväksyttyjen suunniteltujen tilausten tarvekohdistus myynnin kysyntään, hankintaehdotuksen yhdistämiseen ja varauslogiikkaan. Vain se kysyntä käsitellään, joissa ei ole käytetty näitä ennakkokäsittelyjä.
- Tarvekohdistuksen aikana kaikki tarjonta otetaan huomioon määritetystä prioriteetista huolimatta. Tämä tarjonta sisältää käytettävissä olevan varaston, vapautetun toimituksen ja hyväksyttyjen suunniteltujen tilausten osan, jota ei ole tarvekohdistettu.
- Negatiivisten päivien kysyntää ei voi tarvekohdistaa tarjontaan koko kattavuusajanjaksona.
- Kun tarjonta tarvekohdistetaan kysyntään, korkeimman prioriteetin (eli jonka prioriteetin arvo on pienin) tarjonta käytetään ensimmäisenä. Käytettävissä olevan tarjonnan prioriteetin arvon katsotaan olevan 0 (nolla). Niinpä sitä käytetään ensimmäisenä lähteenä.
- Uudet suunnitellut toimitusrivit luodaan tavallisten sääntöjen mukaan esimerkiksi tilauksen pienimmälle ja suurimmalle koolle ja määrän kerrannaisille.

## <a name="planning-priority-models"></a>Suunnittelun prioriteettimallit

*Suunnittelun prioriteettimallit* määritetään kattavuusryhmillä, ja niillä hallitaan suunniteltujen tilausten suunnittelun prioriteettia. Niiden määrittämällä logiikalla päätellään, miten suunnittelun prioriteettiarvo lasketaan kuullekin suunnitellulle tilaukselle ja miten prioriteetti määritetään suunnitelluille tilauksille sekä toimitus- ja kysyntäriveille.

Suunnittelun prioriteettimalleja voi käyttää valitsemalla **Pääsuunnittelu \> Aseteukset \> Suunnittelun prioriteettimallit**. Kuten aiemmin mainittiin, kunkin mallin tärkein prioriteettiasetus on **Prioriteetin laskentamenetelmä** -arvo Tämä asetus määrittää, mitä laskentamenetelmää käytetään, kun pääsuunnittelu määrittää prioriteettiarvon suunniteltuihin tilauksiin.

> [!NOTE]
> Suunnittelun prioriteettimallit koskevat koko organisaatiota ja kaikkia sen yrityksiä.

### <a name="coverage-group"></a>Kattavuusryhmä

Prioriteettipohjaisessa suunnittelussa käytettäväksi tarkoitetun uuden kattavuusryhmän kuvaus on kohdassa [Nimikkeen kattavuussääntöjen määrittäminen](../tasks/define-coverage-rules-items.md). Kun kattavuusryhmä on luotu, seuraavat lisäkentät määritetään:

- **Kattavuuskoodi** – *Prioriteetti* valitaan, jos kattavuusryhmä käyttää prioriteettipohjaista suunnittelua.
- **Suunnittelun prioriteettimalli** – minkä tahansa koko organisaatiota koskevaan suunnittelun prioriteettimallin valinta.

### <a name="item-coverage"></a>Nimikkeen kattavuus

Nimikkeen kattavuusasetusten määrittämistä käsitellään kohdassa [Kattavuusasetukset](../coverage-settings.md). Kattavuusryhmälle valittu **Kattavuuskoodi**-arvo kopioidaan oletusarvoisesti nimikkeen kattavuusasetuksiin. Oletusarvo voidaan kuitenkin tarvittaessa ohittaa. Joissakin tapauksissa nimikkeen kattavuustietueen **Kattavuuskoodi**-kentän asetuksena on *Suunnittelu* mutta liittyvälle kattavuusryhmälle ei ole määritetty mitään suunnittelun prioriteettimallia. Näissä tapauksissa käytetään oletusarvoisesti mitä tahansa mallia, joiden **Prioriteetin laskentamenetelmä** -kentän asetuksena on *Prosenttia varaston enimmäismäärästä* ja **Suunnitellun tilauksen luonti** -kentän asetuksena on *Yksittäinen toimitus, jolla on ensisijainen prioriteetti*.

Kun **Kattavuuskoodi**-kentän asetukseksi määritetään *Prioriteetti*, **Uudelleentilauspiste**-kenttä tulee käytettäväksi nimikkeen kattavuusasetuksissa. Anna tässä kentässä uudelleentilauspoisteen määrä, jota järjestelmän on käytettävä, kun se päättelee, milloin tehdään suunnitellut tilaukset, joiden **Kattavuuskoodi**-arvo on *Prioriteetti*.

Uudelleentilauspisteen määrä lasketaan usein läpimenoajan aikaisena kysyntänä, johon on lisätty vähimmäisarvo (varmuusvarasto). Sen arvon on oltava **Minimi**- ja **Maksimi**-arvojen välissä.

Kentät voidaan määrittää esimerkiksi seuraavasti:

- **Minimi:** *10*
- **Uudelleentilauspiste:** *45*
- **Maksimi:** *60*

Tässä esimerkissä uudelleentilauspisteen määrä perustuu seitsemän päivän läpimenoaikaan ja päivittäinen keskiarvo on 5. Niinpä läpimenoajan aikainen kysyntä on 35. Minimiarvo 10 (varmuusvarasto) lisätään sitten, ja tällä tavoin saavutetaan uudelleentilauspiste 45. Kun tätä määritystä käytetään, toimitusta ehdotetaan, kun ennustettu käytettävissä oleva taso on alle 45. Tilauksen prioriteetti perustuu suunniteltuun prioriteettiasetukseen.

### <a name="manage-planning-priority-models"></a>Suunnittelun prioriteettimallien hallinta

Suunnittelun prioriteettimalleja käytetään seuraavasti:

1. Valitse **Pääsuunnittelu \> Määritys \> Suunnittelun prioriteettimallit**.
1. Valitse luetteloruudussa joko aiemmin luotu malli tai luo uusi malli valitsemalla toimintoruudussa **Uusi**.
1. Määritä tietueen ylätunnisteessa seuraavat kentät:

    - **Nimi** – Anna mallin nimi. Nimen on oltava yksilöivä organisaation kaikissa yksiköissä.
    - **Kuvaus** – anna mallin kuvaus.
    - **Prioriteetin laskentamenetelmä** – Valitse jokin seuraavista arvoista:

        - *Prioriteettialueet* – Jos valitset tämän arvon, **Suunnittelu prioriteettivälit** -ruudukko tulee käytettäväksi. Tässä ruudukossa on luotava useita prioriteettivälejä suunnittelun prioriteettiarvon määrittämistä varten.
        - *Prosenttia varaston enimmäismäärästä* – laske suunnittelun prioriteettiarvo prosenttiosuutena varaston enimmäismäärän ennustetun varastotason perusteella.

    - **Suunnitellun tilauksen luonti** – tämä kenttä on käytettävissä, kun **Prioriteetin laskentamenetelmä** -kentän asetuksena on *Prioriteettivälit*. Valitse jokin seuraavista:

        - *Yksittäinen toimitus, jolla on ensisijainen prioriteetti* – Älä jaa suunniteltuja tilauksia prioriteettivälin perusteella. Suunnitellun tilauksen suunnittelun prioriteetti perustuu tärkeimpään prioriteettiväliin (eli suunnittelun prioriteetin alhaisimpaan arvoon).
        - *Jaa prioriteettialueiden mukaan* – Jaa kysyntä useisiin suunniteltuihin tilauksiin suunnittelun prioriteettialueiden perusteella. Yksittäisten suunniteltujen tilausten suunnittelun prioriteetti määritetään liittyvän suunnittelun prioriteettialueen suunnittelun prioriteetin perusteella.

    - **Ota huomioon kysynnän prioriteetti** – Rajoita toimitusta varten luodun uuden suunnitellun tilauksen prioriteettia määrittämällä asetuksen arvoksi *Kyllä*. (Prioriteetti ei ole alhaisempi kuin liittyvän kysynnän prioriteetti.) Jos asetukseksi määritetään *Ei*, kysyntätilauksen prioriteettia ei oteta huomioon, kun toimitustilauksen prioriteetti lasketaan.

1. Jos **Prioriteetin laskentamenetelmä** -kentän asetukseksi määritetään *Prioriteettivälit*, prioriteettialueen rivejä voi lisätä tai poistaa tarpeen mukaan **Suunnittelun prioriteettialueet** -pikavälilehden **Lisää**- tai **Poista**-painikkeilla. Jos rivejä on useita ja uusi rivi lisätään, suunnittelun prioriteetiksi määritetään automaattisesti valitun ja sen yläpuolella olevan rivin keskiarvo. Määritä kullekin riville seuraavat kentät:

    - **Suunnittelun prioriteetti** – Anna arvona luku 0,00–100,00. Tämä arvo ilmaisee rivillä käytettävän suunnittelun prioriteetin. Alhaisin arvo ilmaisee korkeimman prioriteetin. Oletusarvo määritetään, mutta sitä voi muuttaa tarpeen mukaan. Samaa **Suunnittelu prioriteetti** -arvo ei vo käyttää samassa suunnittelun prioriteettimallissa kuin yhdellä suunnittelun prioriteettialueella.
    - **Kuvaus** – anna suunnittelun prioriteettialueen kuvaus (kuten *Uudelleentilauspiste maksimiin*).
    - **Määrästä** – Tämä on suunnittelun prioriteettialueen alaraja. Tämä vain luku -muotoinen arvo perustuu edellisen suunnittelun prioriteettialueen **Määrälle**- ja **Prosenttia määrästä** -arvoihin.
    - **Määrälle** – Valitse nimikkeen kattavuudesta kenttä, jolla alueen yläraja määritetään. Seuraavia arvoja tuetaan, ja ne vaikuttava seuraavan alueen **Määrästä**-arvoon:

        - *Nolla* – Tämä arvo ilmaiseen alueen negatiivisesta nolla (*Nolla tai vähemmän*–*Nolla*). Riveillä, joilla tämä arvo valitaan, **Määrälle prosentteina** -kenttä on vain luku -muotoinen ja sen asetuksena on aina *100* prosenttia.
        - *Varaston vähimmäismäärä* – Tämä arvo ilmaisee nimikkeen **Minimi**-arvon **Nimikkeen kattavuus** -sivulla. Riveillä, joilla tämä arvo on valittu, **Määrälle prosentteina** -kenttää voi muokata ja sitä käytetään seuraavan alueen **Määrästä**-arvona (esimerkiksi *80 % varaston vähimmäismäärästä*).
        - *Uudelleentilauspiste* – Tämä arvo ilmaisee nimikkeen **Uudelleentilauspiste**-arvon **Nimikkeen kattavuus** -sivulla. Riveillä, joilla tämä arvo on valittu, **Määrälle prosentteina** -kenttää voi muokata ja sitä käytetään seuraavan alueen **Määrästä**-arvona (esimerkiksi *80 % uudelleentilauspisteestä*).
        - *Varaston enimmäismäärä* – Tämä arvo ilmaisee nimikkeen **Maksimi**-arvon **Nimikkeen kattavuus** -sivulla. Riveillä, joilla tämä arvo on valittu, **Määrälle prosentteina** -kenttää voi muokata ja sitä käytetään seuraavan alueen **Määrästä**-arvona (esimerkiksi *80 % varaston vähimmäismäärästä*).
        - *Rajaton* – Tämä arvo ilmaisee alueen rajattoman ylärajan (*Rajaton tai vähemmän*–*Rajaton*). Riveillä, joilla tämä arvo valitaan, **Määrälle prosentteina** -kenttä on vain luku -muotoinen ja sen asetuksena on aina *100* prosenttia.

    - **Määrälle prosentteina** – Anna prosenttiarvo, jolla lasketaan suunnittelun prioriteettialueen yläraja **Määrälle**-kentässä valitun arvon perusteella. Jos **Määrälle**-kentän asetuksena on esimerkiksi *Varaston vähimmäismäärä* ja **Määrälle prosentteina** -kentän asetus on *50*, yläraja on 50 prosenttia liittyvän nimikkeen kattavuuden varaston vähimmäismäärästä.

1. Määritä **Suunnittelun prioriteetin oletusarvot** -pikavälilehdessä ne kentät, joita tarvitaan kunkin tarjonta- tai kysyntärivityypin (myyntitilaus, ostotilaus, siirtotilaus tai kysynnän ennuste) suunnittelun oletusprioriteettien määrittämiseen. Annettavien arvojen on oltava positiivisia.

## <a name="view-and-maintain-planning-priority"></a>Suunnittelun prioriteetin näyttäminen ja ylläpitäminen

Suunnittelun prioriteetti näytetään ja määritetään **Suunnittelun prioriteetti** -kentässä. Tämä kenttä on seuraavassa luettelossa olevien taulukoiden sivuilla. Prioriteetiksi määritetään jokin luku väliltä 0 (nolla) ja 100 nollan (0) ilmaistessa tärkeyden.

| Sivu | Kentän Sijainti | Arvon lähde |
|---|---|---|
| Kysynnän ennusteen rivit | <p>**Nimike**-välilehti</p><p>(Valitse ensin rivi yläosassa ja valitse sitten **Nimike**-välilehti.)</p> | Oletusarvo tai manuaalisesti määritetty arvo |
| Myyntitilauksen tiedot | <p>**Toimitus**-välilehti **Rivin erittely** -pikavälilehdessä</p><p>(Valitse rivi **Myyntitilausrivit**-pikavälilehdessä ja valitse sitten **Rivin erittely**-pikavälilehdessä **Toimitus**-välilehti.)</p> | Oletusarvo, konsernin sisäinen arvo tai manuaalisesti määritetty arvo |
| Ostotilauksen tiedot | <p>**Toimitus**-välilehti **Rivin erittely** -pikavälilehdessä</p><p>(Valitse rivi **Ostotilausrivit**-pikavälilehdessä ja valitse sitten **Rivin erittely**-pikavälilehdessä **Toimitus**-välilehti.)</p> | Suunniteltuja tilauksia vahvistettaessa määritetty arvo, konsernin sisäinen arvo tai manuaalisesti määritetty arvo |
| Siirtotilauksen tiedot | <p>**Toimitus**-välilehti **Rivin erittely** -pikavälilehdessä</p><p>(Valitse rivi **Siirtotilausrivit**-pikavälilehdessä ja valitse sitten **Rivin erittely**-pikavälilehdessä **Toimitus**-välilehti.)</p> | Suunniteltuja tilauksia vahvistettaessa määritetty arvo tai manuaalisesti määritetty arvo |
| Suunnitellun tilauksen tiedot | **Yleiset**-pikavälilehti | Pääsuunnittelun aikana laskettu arvo tai manuaalisesti määritetty arvo |

### <a name="intercompany-trade"></a>Konsernin sisäinen kauppa

Konsernin sisäisten tarjonta- ja kysyntärivien **Suunnittelun prioriteetti** -arvo jaetaan linkitettyjen entiteettien kanssa. Kummallakin puolella tehty muokkaus näkyy linkitetyllä tilausrivillä.

Seuraavassa on muutamia esimerkkejä:

- Käyttäjä muuttaa konsernin sisäisen myyntitilausrivin suunnittelun prioriteetin arvon 20 arvoksi 30. Tämä muutos näkyy linkitetyllä konsernin sisäisellä ostotilausrivillä.
- Käyttäjä muuttaa konsernin sisäisen ostotilausrivin suunnittelun prioriteetin arvon 40 arvoksi 50. Tämä muutos näkyy linkitetyllä konsernin sisäisellä myyntitilausrivillä.
