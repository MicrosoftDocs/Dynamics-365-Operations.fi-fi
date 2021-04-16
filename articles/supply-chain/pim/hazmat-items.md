---
title: Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet
description: Tässä ohjeaiheessa käsitellään vapautettujen tuotteiden vaarallisten aineiden ominaisuuksien määrittämistä, vaarallisten nimikkeiden varastointirajoitusten asettamista ja vaarallisten aineiden sisällyttämistä myyntitilaukseen, lähetykseen tai kuormaan.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b0fb2f77b4e95c90e3eb8a4c74929deead34de5c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829399"
---
# <a name="hazardous-materials-in-products-orders-shipments-and-loads"></a>Tuotteiden, tilausten, lähetysten ja kuormien vaaralliset aineet

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään vapautettujen tuotteiden vaarallisten aineiden ominaisuuksien määrittämistä, vaarallisten nimikkeiden varastointirajoitusten asettamista ja vaarallisten aineiden sisällyttämistä myyntitilaukseen, lähetykseen tai kuormaan.

## <a name="set-hazardous-material-specifications-for-products"></a>Tuotteiden vaarallisten aineiden määritysten määrittäminen

Sen jälkeen kun vaarallisten aineiden määräys ja liittyvät viitekoodit on määritetty kohdassa [Vaarallisten aineiden määrittäminen](hazmat-setup.md) kuvatulla tavalla, nämä tiedot voidaan liittää vapautettuihin nimikkeisiin. Lähetysasiakirjojen lähetysteksti haetaan vapautettujen nimikkeiden vaarallisten aineiden tiedoista.

Vapautetun nimikkeen vaaralliseen aineeseen liittämisen osana on määritettävä määräyksen koodi ja materiaali. Nimikkeeseen voidaan liittää kuljetustavan mukaan erilaisia määräyksen koodeja. Lisäksi jokaiseen nimikkeeseen voidaan liittää useita määräyksiä ja materiaalikoodeja.

Vapautettu tuote määritetään vaaralliseksi aineeksi seuraavasti:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tai luomalla tuote.
1. Määritä **Varastonhallinta**-pikavälilehden **Vaaralliset aineet** -asetukseksi **Kyllä**. Tämä asetus määrittää nimikkeen vaaralliseksi tavaraksi, ja sitä käytetään lähetysohjeita tulostettaessa.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Yhteensopivuus**-ryhmässä **Nimikkeen vaarallinen aine**.
1. Täytä valitun nimikkeen **Nimikkeen vaaralliset aineet** -sivu käyttämällä seuraavissa alaosissa kuvattuja kenttiä.

### <a name="item-hazardous-materials-header"></a>Nimikkeen vaarallisten aineiden otsikko

Seuraavassa taulukossa käsitellään kenttiä, jotka sijaitsevat **Nimikkeen vaaralliset aineet** -sivun yläosassa.

| Kenttä | kuvaus |
|---|---|
| Nimiketunnus | Käsiteltävänä oleva vapautettu tuote. |
| Sääntelykoodi | Valitse tuotetta koskeva vaarallisten aineiden määräys. Määräys määrittää, miten tulostettava lähetysteksti luodaan nimikkeelle ja mikä on liitetty toimitustapa. Kun koodi on määritetty, sitä ei voi muokata tällä sivulla. Uuden määräyksen koodin voi kuitenkin määrittää valitsemalla **Uusi**. |
| Materiaalin koodi | (Valinnainen) Valitse tuotetta koskeva vaarallisen aineen koodi. Materiaalikoodi on malli, joka sisältää monen tällä sivulla olevan kentän oletusarvot. Kun valitset koodin, kaikki sen vaarallisten aineiden määritykset kopioidaan valittuna olevaan tuotteeseen. Järjestelmä pyytää kuitenkin ensin vahvistamaan, että nimikkeen materiaalitiedot täytetään materiaalikoodista. |
| Ryhmäkoodi | (Valinnainen) Valitse tuotetta koskeva vaarallisen aineen luokitteluryhmä. Samoin kuin **Materiaalikoodi**-kentän kohdalla koodin valinnan myötä kaikki sen vaarallisten aineiden määritykset kopioidaan valittuna olevaan tuotteeseen. Järjestelmä pyytää kuitenkin ensin vahvistamaan, että nimikkeen luokitteluryhmän tiedot täytetään ryhmäkoodista. |

### <a name="descriptions-fasttab"></a><a name="hazmat-description"></a>Kuvaukset-pikavälilehti

Seuraavassa taulukossa käsitellään **Kuvaukset**-pikavälilehdessä valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Oikea lähetysnimi | Anna käytettävässä määräyksessä määritetty materiaalin vakiokuvaus. Voit kääntää arvon **Nimikkeen lähetystekstin käännös** -pikavälilehdessä seuraavassa ohjeessa kuvatulla tavalla. |
| Tekninen nimi | Valitse materiaalin yleinen nimi. Tämä nimi voi olla esimerkiksi nimi, jota yritys käyttää materiaalista sisäisesti. |
| N.O.S. | Tämän valintaruudun valinta osoittaa, että **Oikea lähetysnimi** ei ole nimikkeen N.O.S. (muutoin määritetty) -lähetysnimi. N.O.S. lähetysnimiä käytetään sellaisten samankaltaisten kemikaali- ja materiaaliryhmien kohdalla, joilla on tietty käyttötarkoitus mutta joita ei ehkä muutoin mainita tietyn määräyksen vaarallisten aineiden taulukossa. |

### <a name="item-ship-text-translation-fasttab"></a>Nimikkeen lähetystekstin käännös -pikavälilehti

**Nimikkeen lähetystekstin käännös** -pikavälilehdessä on ruudukko, joka sisältää **Kuvaukset**-pikavälilehdessä määritetyn ensisijaisen kielen **Oikea lähetysnimi** -arvojen käännökset. Näitä käännöksiä käytetään yhden tai usean lisäkielen lähetystekstin tulostamiseen.

Seuraavassa taulukossa käsitellään **Nimikkeen lähetystekstin käännös** -pikavälilehdessä valittavina olevat kentät.


| Kenttä | kuvaus |
|---|---|
| Kieli | Rivillä käytettävä kielikoodi. Esimerkiksi **pt-br** tarkoittaa Brasilian portugalia. |
| Lähetyksen tulostusteksti | Rivillä käytettävälle kielelle käännetty **Oikea lähetysnimi**. |

Voit lisätä käännöksen tai muokata sitä avaamalla **Tekstiin käännökset** -sivun valitsemalla **Käännökset** ruudukon yläpuolella. Toimi sitten jonkin seuraavien vaiheiden mukaisesti:

- Voit lisätä uuden käännöksen valitsemalla toimintoruudussa **Lisää**. Valitse ensin lisättävä kieli ja anna sitten käännetty teksti **Käännetty teksti** -kenttään.
- Voit muokata nykyistä käännöstä valitsemalla kohdekielen **Kieli**-kentässä ja muokkaamalla käännettyä tekstiä tarpeen mukaan **Käännetty teksti** -kentässä.

### <a name="material-management-fasttab"></a><a name="material-management"></a>Materiaalien hallinta -pikavälilehti

Seuraavassa taulukossa käsitellään **Materiaalien hallinta** -pikavälilehdessä valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Luokka | Valitse vaarallisen materiaaliin luokka, johon tuote noudatettavan määräyksen määritysten mukaan kuuluu. Jokaiselle vaarallisia aineita sisältävälle tuotteelle on määritettävä sekä jako että luokka. |
| kuvaus | **Luokka**-kentässä valitulle luokalle määritetty kuvaus. Kenttää ei voi muokata. |
| Jaosto | Valitse vaarallisen aineen jako, johon tuote noudatettavan määräyksen määritysten mukaan kuuluu. Jako on luokan alajoukko. Jokaiselle vaarallisia aineita sisältävälle tuotteelle on määritettävä sekä jako että luokka. |
| Tunnus | Valitse vaarallisen aineen tunnuskoodi. Tämä koodi perustuu tyypillisesti Yhdistyneiden kansakuntien (YK) standardiin. |
| Pakkausryhmä | Valitse nykyistä nimikettä koskeva pakkausryhmä. |
| kuvaus | **Pakkausryhmä**-kentässä valitulle ryhmälle määritetty kuvaus. Kenttää ei voi muokata. |
| Pakkauksen kuvaukset | Valitse käytettävä pakkaus kuvauskoodi. Tämä koodi viittaa kuvaukseen, jossa ilmaistaan, miten tuote on pakattava. |
| Vaarallisten aineiden etiketit | Valitse koodi, joka viittaa tuotteessa käytettävään vaarallisten aineiden etikettiin. |
| Rajoitettu määrä | Kun asetukseksi määritetään **Kyllä**, kun tuotteen kokonaispaino sisällytetään jokaiseen kuormaan ja jokaiselle kuormariville. |
| Määrä | Annan tuotteeseen sisältyvä vaarallisen aineen määrä määritettynä yksikkönä. Tämän arvon avulla lasketaan tuotteen sisältävien kuormien ja lähetysten vaarallisten aineiden kokonaispistemäärä. |
| Kerroin | Anna kerroin, jota käytetään laskettaessa kunkin tuotteen sisältävän kuormarivin vaarallisten aineiden pistemäärää. Käytettävä määräys määrittää tämän arvon tuotteessa olevan vaarallisen aineen tyypin mukaan. |
| Yksikkö | Valitse mittayksikkö, jota käytetään tuotteen vaarallisen aineen määrän ilmaisemiseen. Arvo on määritetty **Määrä**-kentässä. Tämän arvon avulla lasketaan tuotteen sisältävien kuormien ja lähetysten vaarallisten aineiden kokonaispistemäärä. |

#### <a name="how-the-hazardous-material-score-is-calculated"></a>Vaarallisen aineen pistemäärän laskeminen

Monia tuotteen **Materiaalien hallinta** -pikavälilehdessä määritettyjä arvoja käytetään laskemaan kunkin kyseisen tuotteen sisältävän kuormarivin *vaarallisen aineen pistemäärä*. Pistemäärä lasketaan seuraavalla kaavalla:

Vaarallisen aineen pistemäärä = *&lt;LineQty&gt;* × *&lt;HazmatQty&gt;* × *&lt;UnitConversion&gt;* × *&lt;Multiplier&gt;*

Kaavan selitys:

- *&lt;LineQty&gt;* on kuormariville määritetyn tuotteen määrä.
- *&lt;HazmatQty&gt;* on tuotteelle **Materiaalien hallinta** -pikavälilehden **Määrä**-kentässä määritetty vaarallisen aineen määrä.
- *&lt;UnitConversion&gt;* on muuntokerroin, jota käytetään muunnettaessa kuormarivin määrässä käytettyä yksikköä ja **Materiaalien hallinta** -pikavälilehden **Yksikkö**-kentässä määritettyä yksikköä.
- *&lt;Multiplier&gt;* on tuotteelle **Materiaalien hallinta** -pikavälilehden **Kerroin**-kentässä määritetty kerroin.

Pistemäärä ilmoitetaan jokaiselle kuormariville, joka sisältää tuotteen, joille nämä arvot on määritetty. Lisätietoja on jäljempänä tässä ohjeaiheessa kohdissa [Vaarallisia aineita sisältävät lähetykset](#hazmat-shipments) ja [Vaarallisia aineita sisältävät kuormat](#hazmat-loads).

#### <a name="how-the-hazardous-material-weight-is-calculated"></a>Vaarallisen aineen painon laskeminen

Sellaisten kuormien ja kuormarivien tuotteiden osalta, joiden **Materiaalien hallinta** -pikavälilehden **Rajoitettu määrä** -asetuksena on **Kyllä**, näytetään vaarallisen aineen kokonaispaino. Tätä käsitellään jäljempänä tämän ohjeaiheessa kohdissa [Vaarallisia aineita sisältävät lähetykset](#hazmat-shipments) ja [Vaarallisia aineita sisältävät kuormat](#hazmat-loads). Vaarallisen aineen paino lasketaan seuraavalla kaavalla:

Vaarallisen aineen paino = *&lt;LineQty&gt;* × *&lt;ProductWeight&gt;* × *&lt;UnitConversion&gt;*

Kaavan selitys:

- *&lt;LineQty&gt;* on kuormariville määritetyn tuotteen määrä.
- *&lt;ProductWeight&gt;* on tuotteelle määritetty nettopaino tuotteelle määritettynä varastoyksikkönä.
- *&lt;UnitConversion&gt;* on muuntokerron, jota käytetään kuormarivin määrän yksikön ja *&lt;ProductWeight&gt;*-kohdassa käytetyn varastoyksikön muuntamiseen.

### <a name="transport-information-fasttab"></a>Kuljetustiedot-pikavälilehti

Seuraavassa taulukossa käsitellään **Kuljetustiedot**-pikavälilehdessä valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Kuljetusluokka | Valitse liittyvä kuljetusluokka. |
| Tunnelin koodi | Valitse nimikkeelle liittyvä tunnelirajoituskoodi. |
| Vaarallisen materiaalin ahtaus | Valitse viitekoodi, jota käytetään laivarahdin ahtaukseen, kun nimike lähetetään laivarahtina. |
| Lentokoneen tyyppi | Valitse lentokonerajoitus, jotka käytetään lähetettäessä materiaalina lentorahtina. |
| Pakkaus – vain rahtilentokoneet | Valitse **Lentokoneen tyyppi** -kentässä valitun arvon perusteella pakkauksen ohjekoodi, jota käytetään, kun tuote voidaan lähettää vain rahtilentokoneella. |
| Pakkaus – matkustaja- ja rahtilentokoneet | Valitse **Lentokoneen tyyppi** -kentässä valitun arvon perusteella pakkauksen ohjekoodi, jota käytetään, kun tuote voidaan lähettää joko rahti- tai matkustajalentokoneella. |
| IATA-tähti | Kun asetukseksi valitaan **Kyllä**, tässä pikavälilehdessä annetut lentokuljetusmääritykset liittyvät IATA:n (International Air Transport Association) vaarallisten aineiden standardiin. Tämä kenttä on tarkoitettu vain tiedoksi. |
| Hätätilannevastaus | Valitse koodi, joka viittaa materiaalin hätätilannetta koskeviin käsittelyohjeisiin. |

### <a name="environmental-information-fasttab"></a>Ympäristötiedot-pikavälilehti

Seuraavassa taulukossa käsitellään **Ympäristötiedot**-pikavälilehdessä valittavina olevat kentät.

| Kenttä | kuvaus |
|---|---|
| Ympäristölle vaarallinen | Jos asetuksena on **Kyllä**, se ilmaisee, että tuote on ympäristölle vaarallinen. Käytä tätä kenttää omaa raportointia varten. |
| Merisaaste | Jos asetuksena on **Kyllä**, se ilmaisee, että tuote on merta saastuttava aine. Käytä tätä kenttää omaa raportointia varten. |

## <a name="set-stock-limits-for-hazardous-products"></a><a name="stock-limits"></a>Vaarallisten tuotteiden varastointirajojen määrittäminen

Tietyn tuotteen samassa paikassa varastoitavaa kokonaismäärää on ehkä turvallisuussyistä rajoitettava. Vapautetun tuotteen varastointirajojen määrittäminen:

1. Mene **Tuotetietojen hallinta \> Tuotteet \> Vapautetut tuotteet**.
1. Avaa tuotteen **Vapautetun tuotteen tiedot** -sivu valitsemalla tuote.
1. Valitse toimintoruudun **Varastonhallinta**-välilehden **Yhteensopivuus**-ryhmässä **Raportointitiedot**.
1. Määritä valitulle tuotteelle soveltuvat arvot **Vaarallisen aineen varaston raja**- ja **Vaarallisen aineen varoitusraja** -kentissä.

**Vaarallisen aineen varastoraja** -raportin avulla voi seurata vaarallisten aineiden varastotasoja varastoissa ja varmistaa, että tässä kohdassa määritettyjä turvarajoja noudatetaan. Lisätietoja on kohdassa [Vaarallisen aineen varastorajan raportti](hazmat-reports.md#stock-limit-report).

## <a name="sales-order-transactions-that-include-hazardous-materials"></a>Vaarallisia aineita sisältävät myyntitilaustapahtumat

Vaaralliseksi aineeksi luokitellun tuotteen sisällyttäminen myyntitilaukseen edellyttää, että se liitetään myyntitilauksessa soveltuvaan lähetyksen rahdinkuljettajaan. Avaa myyntitilaus ja määritä sitten **Lähetyksen rahdinkuljettaja**- ja **Rahdinkuljetuspalvelu**-kentät tarpeen mukaan **Toimitus**-pikavälilehdessä.

Rahdinkuljettaja liitetään myös toimitustapaan. Tämän vuoksi onkin varmistettava, että tiedot ovat vaarallisten aineiden määräyksen mukaisia. Vaarallisten aineiden määräyksessä määritetyn toimitustavan on siis vastattava myyntitilauksen ylätunnisteen määrityksiä. Tällä tavoin määräys, lähetyksen rahdinkuljettaja ja rahdinkuljetuspalvelu liitetään myyntitilauksessa käytettyihin lähetysriveihin.

Kun myyntitilaus on viimeistelty ja valmis lähetettäväksi, se voidaan vapauttaa varastoon ilmaisemaan siirtoa myynti- ja varastotoimintojen välillä.

## <a name="shipments-that-include-hazardous-materials"></a><a name="hazmat-shipments"></a>Vaarallisia aineita sisältävät lähetykset

### <a name="view-hazardous-material-scores-for-each-shipment-line"></a>Kunkin lähetysrivin vaarallisen aineen pistemäärien näyttäminen

Lähetyksen **Lähetyksen tiedot** -sivulla on vaarallisen aineen kokonaispaino ja -pistemäärä, jotka on laskettu kullekin kyseiseen lähetykseen sisältyvällä kuormariville. Pistemääriä ja painoja voi tarkastella seuraavasti:

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Avaa lähetyksen **Lähetyksen tiedot** -sivu valitsemalla lähetys.
1. Tarkasta rivit **Kuormarivit**-pikavälilehdessä. Jokaisella rivillä on näkyvissä vaarallisen aineen laskelmat seuraavissa kentissä:

    - **Vaarallisen aineen pisteet** – Tässä kentässä näkyy kuormarivin vaarallisen aineen pistemäärä. Arvo lasketaan käytetylle määräykselle ja vapautetun tuotteen määrityksissä määritettyjen sääntöjen ja arvojen mukaisesti. Laskelma käyttää kuormarivin määrää ja kerrointa vapautetun tuotteen [materiaalin hallintamäärityksissä](#material-management).
    - **Rajoitetun määrän nettopaino** – Jos tuote on merkitty rajoitetun määrän tuotteeksi, koska ne sisältävät vaarallisia aineita, tässä kentässä näkyy kuormariviin sisältyvän vaarallisen sisällön kokonaisnettopaino. Laskelma perustuu tuotteisiin, jotka on merkitty vapautetun tuotteen määrityksissä vaarallisiksi aineiksi. Jos nimike on merkitty rajoitetun määrän nimikkeeksi, laskelma käyttää kunkin kuormarivin määrää ja vapautetun tuotteen [materiaalin hallinnan määrityksissä](#material-management) olevaa painoa.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-shipment"></a>Lähetykseen sisältyvien vaarallisten aineiden yhteensopivuuden tarkistaminen

Järjestelmä voi arvioida, voidaanko kaikki lähetykseen sisältyvät vaaralliset aineet lähettää yhdessä. Järjestelmä arvioi yhteensopivuuden tarkistamalla kullekin lähetykseen sisältyvälle tuotteelle määritetyn yhteensopivuusryhmän. Lisätietoja on kohdassa [Vaarallisten aineiden yhteensopivuusryhmät](hazmat-setup.md#compatibility-groups).

Yhteensopivuus tarkistetaan seuraavasti:

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki lähetykset**.
1. Avaa lähetyksen **Lähetyksen tiedot** -sivu valitsemalla lähetys.
1. Valitse toimintoruudun **Lähetykset**-välilehden **Toiminnot**-ryhmässä **Yhteensopivuustarkistus**.

Saat ilmoituksen tarkistuksen tuloksista.

## <a name="loads-that-include-hazardous-materials"></a><a name="hazmat-loads"></a>Vaarallisia aineita sisältävät kuormat

### <a name="view-hazardous-material-scores-for-each-load-line"></a>Kunkin kuormarivin vaarallisen aineen pistemäärien näyttäminen

Kuorman **Kuorman tiedot** -sivulla on vaarallisen aineen kokonaispaino ja -pistemäärä, jotka on laskettu kyseille kuormalle ja jokaiselle kuormariville. Pistemääriä ja painoja voi tarkastella seuraavasti:

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki kuormat**.
1. Avaa kuorman **Kuorman tiedot** -sivu valitsemalla kuorma. (Voit kuorman tiedot myös valitsemalla linkin liittyvässä lähetyksessä.)
1. Voit tarkastella **Kuorma**-pikavälilehdessä koko kuorman vaarallisten aineiden kokonaispistemäärää ja -painoa seuraavien kenttien avulla:

    - **Vaarallisen aineen pisteet** – Tässä kentässä näkyy kuorman vaarallisen aineen pistemäärä. Arvo lasketaan käytetylle määräykselle ja vapautetun tuotteen määrityksissä määritettyjen sääntöjen ja arvojen mukaisesti. Laskelma käyttää kuormaan sisältyvää määrää ja kerrointa vapautetun tuotteen [materiaalin hallintamäärityksissä](#material-management).
    - **Rajoitetun määrän nettopaino** – Jos tuotteet on merkitty rajoitetun määrän tuotteeksi, koska ne sisältävät vaarallisia aineita, tässä kentässä näkyy kuormaan sisältyvän vaarallisen sisällön kokonaisnettopaino. Laskelma perustuu tuotteisiin, jotka on merkitty vapautetun tuotteen määrityksissä vaarallisiksi aineiksi. Jos nimike on merkitty rajoitetun määrän nimikkeeksi, laskelma käyttää kunkin kuorman määrää ja vapautetun tuotteen [materiaalin hallinnan määrityksissä](#material-management) olevaa painoa.

1. Voit tarkastella yksittäisten rivien pistemäärä ja painoa valitsemalla **Kuormarivit**-pikavälilehden. Kullakin rivillä olevat arvot muistuttavat koko kuorman arvoja, joita käsiteltiin edellisessä vaiheessa.

### <a name="check-for-compatibility-among-hazardous-materials-that-are-included-in-a-load"></a>Kuormaan sisältyvien vaarallisten aineiden yhteensopivuuden tarkistaminen

Järjestelmä voi arvioida, voidaanko kaikki kuormaan sisältyvät vaaralliset aineet lähettää yhdessä. Järjestelmä arvioi yhteensopivuuden tarkistamalla kullekin kuormaan sisältyvälle tuotteelle määritetyn yhteensopivuusryhmän. Lisätietoja on kohdassa [Vaarallisten aineiden yhteensopivuusryhmät](hazmat-setup.md#compatibility-groups).

Yhteensopivuus tarkistetaan seuraavasti:

1. Valitse **Varastonhallinta \> Lähetykset \> Kaikki kuormat**.
1. Avaa kuorman **Kuorman tiedot** -sivu valitsemalla lähetys. (Voit kuorman tiedot myös valitsemalla linkin liittyvässä lähetyksessä.)
1. Valitse toimintoruudun **Kuormat**-välilehden **Toiminnot**-ryhmässä **Yhteensopivuustarkistus**.

Saat ilmoituksen tarkistuksen tuloksista.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]