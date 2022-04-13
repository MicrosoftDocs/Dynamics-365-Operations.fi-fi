---
title: Tietueiden ryhmittely ja laskelmien kokoaminen GROUPBY-tietolähteiden avulla
description: Tässä ohjeaiheessa kerrotaan GROUPBY-tietolähteiden käytöstä sähköisessä raportoinnissa (ER).
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b79dfe62122a031ae9ed7f51ea7ff578cd47358
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462294"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Tietueiden ryhmittely ja laskelmien kokoaminen GROUPBY-tietolähteiden avulla

[!include[banner](../includes/banner.md)]

Kun määrität [sähköisen raportoinnin (ER)](general-electronic-reporting.md) mallimäärityksiä tai muotoja, voit [lisätä](#AddMmDataSource2) tarvittavia **GroupBy**-tyypin tietolähteitä.

Suunnittelun aikana **GroupBy**-tietolähde on konfiguroitu tunnistamaan seuraavat elementit:

- [Perustietolähde](#BaseDataSource), joka sisältää suoritusaikana ryhmiteltävät tietueet
- Perustietolähteen [ryhmittelykentät](#GroupingFields), joita käytetään tietueiden ryhmittelyssä ajon aikana
- [Koostefunktiot](#AggregateFunctions), jotka määrittävät kullekin löydetylle ryhmälle suoritettavat koostelaskelmat ajon aikana

Suorituksen aikana konfiguroitu **GroupBy**-tietolähde ryhmittelee tietueet, joiden ryhmittelykentissä on samat arvot, ja palauttaa sitten tietueluettelon. Kukin tietue edustaa yhtä ryhmää. Tietolähde näyttää kunkin ryhmän kenttäarvot, joiden mukaan alkuperäiset tietueet on ryhmitelty, laskettujen koostefunktioiden arvot ja ryhmään kuuluvan perustietolähteen tietueiden luettelon.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Koostefunktiot

Ajon aikana jokainen koostelaskelma tehdään kullekin tietueryhmälle. Tämä laskenta tehdään käyttämällä yksittäisen kentän tai lausekkeen arvoa tietueissa tietolähteessä, joka on valittu ryhmittelyyn muokattavassa **GroupBy**-tyypin tietolähteessä. Tällä hetkellä tuetaan seuraavia koostefunktioita:

- **AVG** – Tämä toiminto palauttaa ryhmän arvojen keskiarvon. Sitä voidaan käyttää vain numerokenttien kanssa.
- **COUNT** – Tämä toiminto palauttaa ryhmässä olevien kohteiden määrän.
- **Min** – Tämä toiminto palauttaa ryhmän arvojen minimiarvon.
- **Max** – Tämä toiminto palauttaa ryhmän arvojen maksimiarvon.
- **SUM** – Tämä toiminto palauttaa ryhmän kaikkien arvojen summan. Sitä voidaan käyttää vain numerokenttien kanssa.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Suorituksen sijainti

Kun muokkaat **GroupBy**-tietolähdettä ja määrität perustietolähteen, joka sisältää ryhmiteltävät tietueet, järjestelmä tunnistaa tehokkaimman [sijainnin](#ExecutionLocation) **GroupBy**-tietolähteen suorittamiseksi. Jos perustietolähde on [kyselykelpoinen](er-functions-list-filter.md#usage-notes) (eli jos se voidaan suorittaa tietokantatasolla), sovellustietokanta määritetään myös muokattavan **GroupBy**-tietolähteen suoritussijainniksi. Muutoin sovelluspalvelimen muisti määritetään suoritussijainniksi.

Voit muuttaa automaattisesti havaittua suoritussijaintia manuaalisesti valitsemalla sijainnin, joka on sovellettavissa konfiguroituun tietolähteeseen. Jos valittu suorituspaikka ei ole käytettävissä, [oikeellisuustarkistusvirhe](er-components-inspections.md#i5) heitetään suunnitteluaikana.

> [!TIP]
> On suositeltavaa ryhmitellä tietolähteet tietokannan sijainnin avulla, jos tietueita on paljon.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Muistin kulutus

Jos **GroupBy**-tietolähde suoritetaan oletusarvoisesti muistissa, sovelluspalvelimen muistiin tallennetaan perustietolähteen tietueet, jotka kuuluvat kuhunkin löydettyyn ryhmään yksittäisen ryhmän tietueina. Muistin kulutusta voi vähentää estämällä **GroupBy**-tietolähteiden tallennusvaraston, jos ne on määritetty laskemaan vain koostetoimintoja eikä ryhmän tietueita käytetä ajon aikana. Jos haluat vähentää muistinkulutusta tällä tavalla, ota käyttöön **Vähennä sähköisen raportoinnin muistin käyttöä, kun tietueiden ryhmittelyä käytetään vain koostetietojen laskentaan** -toiminto **ominaisuudenhallinnan** työtilassa.

## <a name="alternatives"></a><a name="Alternatives"></a>Vaihtoehdot

Samanlaiset koostamiset voidaan laskea [erityyppisten](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) tietolähteiden tai ER:n sisäänrakennettujen toimintojen avulla.

Lisätietoja tästä ominaisuudesta saa suorittamalla seuraavan esimerkin.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Esimerkki: GROUPBY-tietolähteen käyttäminen koostelaskelmiin ja tietueiden ryhmittelyyn

Tämä esimerkki osoittaa, miten järjestelmänvalvojan tai sähköisen raportoinnin toiminnallisen konsultin roolin omaava käyttäjä voi määrittää **GROUPBY**-tietolähdettä käyttävän ER-muotomäärityksen sekä miten tällä tavoin lasketaan koostefunktioita ja ryhmitellään tietueita. Tämän mallimäärityksen avulla tulostetaan valvontaraportti, kun Intrastat-ilmoitus luodaan. Tämän raportin avulla voit tarkistaa raportoidut Intrastat-tapahtumat.

Tässä esimerkissä ohjeaiheessa käsitellyt toimenpiteet voidaan suorittaa **DEMF**-yrityksessä Microsoft Dynamics 365 Financessa. 

### <a name="prepare-sample-data"></a>Näytetietojen valmisteleminen

Varmista, että raportoinnin Intrastat-tapahtumat on määritetty **Intrastat**-sivulla. Erilaisia kuljetuskoodeja varten on oltava tapahtumia, koska tapahtumat ryhmitellään tämän esimerkin **Kuljetus**-kentän mukaan.

![Intrastat-tapahtumien valmisteleminen Intrastat-sivulla.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Määritä ER-kehys

Seuraa vaiheita kohdassa [Määritä ER-kehys](er-quick-start2-customize-report.md#ConfigureFramework) luodaksesi ER-parametrien vähimmäisjoukon. Nämä asetukset on suoritettava, ennen kuin ER-kehystä käytetään ER-muotomäärityksen suunnitteluun.

### <a name="import-the-standard-er-format-configuration"></a>Tuo ER-muodon vakiokonfiguraatio

Seuraa vaiheita kohdassa [Tuo ER-muodon vakiokonfiguraatio](er-quick-start2-customize-report.md#ImportERSolution1) lisätäksesi ER-vakiokonfiguraatiot nykyiseen Dynamics 365 Finance -ilmentymääsi. Tuo säilöstä versio 1 **Intrastat-mallin** konfiguraatiosta.

### <a name="create-a-custom-data-model-configuration"></a>Mukautetun tietomallimäärityksen luominen

Lisää manuaalisesti uusi ER-tietomallin **Intrastat-malli (Littware)** -konfiguraatio, joka on johdettu tuodusta **Intrastat-mallin** konfiguraatiosta kohdan [Lisää mukautettu tietomallikonfiguraatio](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) vaiheiden avulla.

### <a name="configure-a-custom-data-model-component"></a>Mukautetun tietomallikomponentin määritys

Noudattamalla näitä ohjeita voit tehdä tarvittavat muutokset johdettuun **Intrastat-malli (Litware)** -tietomalliin, jotta sitä voidaan käyttää näyttämään kuljetuskoodit, joissa on tarvittavat tiedot.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Konfiguraatiot**-sivun konfiguraatiopuussa **Intrastat-malli (Litware)**.
3. Valitse **Suunnittelu**.
4. Valitse **Tietomallin suunnittelu** -sivun mallipuusta **Intrastat**.
5. Valitse **Uusi**, jos haluat lisätä valittuun **Intrastat**-solmuun uuden upotetun solmun. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Kirjoita **Nimi**-kenttään **Kuljetus**.
    2. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

6. Valitse **Uusi**, jos haluat lisätä juuri lisättyyn **Kuljetus**-solmuun uuden upotetun solmun. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Kirjoita **Nimi**-kenttään **Koodi**.
    2. Valitse **Nimiketyyppi**-kentässä **Merkkijono**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

7. Valitse **Uusi**, jos haluat lisätä **Kuljetus**-solmuun toisen upotetun solmun. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Kirjoita **Nimi**-kenttään **TotalInvoicedAmount**.
    2. Valitse **Nimiketyyppi**-kentässä **Reaaliluku**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

8. Valitse **Uusi**, jos haluat lisätä **Kuljetus**-solmuun toisen upotetun solmun. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Anna **Nimi**-kentässä **NumberOfTransactions**.
    2. Valitse **Nimiketyyppi**-kentässä **Kokonaisluku**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

9. Valitse **Uusi**, jos haluat lisätä **Kuljetus**-solmuun toisen upotetun solmun. Tee seuraavat toimet avattavassa valintaikkunassa tietomallisolmun lisäämistä varten:

    1. Kirjoita **Nimi**-kenttään **Tapahtuma**.
    2. Valitse **Nimiketyyppi**-kentässä **Tietueluettelo**.
    3. Valitse **Lisää** lisätäksesi uuden solmun.

10. Valitse juuri lisätyn **Tapahtuma**-solmun **Solmu**-pikavälilehdessä **Muuta nimikkeen viitettä**.
11. Valitse **Muuta nimikkeen viitettä**-valintaikkunan tietomallipuusta **CommodityRecord**. Valitse sitten **OK**.

![Konfiguroitu tietomalli ER-tietomallin suunnittelussa.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Mukautetun tietomallin rakenteen täydentäminen

Suorita **Intrastat-malli (Litware)** -tietomallin suunnittelu [Tietomallin rakenteen täydentäminen](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) -ohjeen vaiheiden avulla.

### <a name="create-a-new-model-mapping-configuration"></a>Uuden mallin yhdistämismäärityksen luominen

Lisää manuaalisesti uusi ER-mallimäärityksen **Intrastat-näytemääritys** -konfiguraatio johdetulle **Intrastat-malli (Litware)** -konfiguraatiolle [Uuden mallin yhdistämismäärityksen luominen](er-quick-start1-new-solution.md#CreateModelMapping) -ohjeen vaiheiden avulla.

### <a name="add-a-new-model-mapping-component"></a>Uuden mallin yhdistämismäärityksen komponentin lisääminen

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Laajenna **Konfiguraatiot**-sivun määrityspuun vasemmassa ruudussa **Intrastat-malli** -konfiguraatio.
3. Valitse **Intrastat-esimerkkiyhdistämismääritys** -määritys.
4. Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.
5. Poista aiemmin luotu määrityskomponentti valitsemalla **Poista**.
6. Lisää uusi yhdistämismäärityksen komponentti valitsemalla **Uusi**.
7. Valitse **Määritelmä** -kentässä **Intrastat**.
8. Kirjoita **Nimi**-kenttään **Intrastat-määritys**.
9. Määritä uusi yhdistämismääritys valitsemalla **Suunnittelutoiminto**.

### <a name="design-the-added-model-mapping-component"></a>Lisätyn mallimäärityskomponentin suunnitteleminen

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Tietolähteen lisääminen sovellustaulun käyttämiseen

Konfiguroi tietolähde, jotta voit käyttää Intrastat-tapahtumien tietoja sisältäviä sovellustauluja.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Dynamics 365 for Operations\\Taulukkotiedot**.
2. Lisää uusi **Intrastat**-taulun käyttöön käytettävä tietolähde valitsemalla **Tietolähteet**-ruudusta **Lisää juuri**. Jokainen **Intrastat**-taulun tietue edustaa yhtä Intrastat-tapahtumaa.
3. Syötä **Tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **Tapahtuma**.
4. Anna **Taulu**-kenttään **Intrastat**.
5. Lisää uusi tietolähde valitsemalla **OK**.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Tietolähteen lisääminen Intrastat-tapahtumien ryhmittelemiseen

Määritä **GroupBy**-tietolähde Intrastat-tapahtumien ryhmittelemiseen ja koostefunktioiden laskemiseen.

1. Valitse **Mallin määrityksen suunnittelu** -sivun **Tietolähdetyypit**-ruudusta **Funktiot\\Group by**.
2. Lisää uusi Intrastat-tapahtumien ryhmittelyyn ja koostefunktioiden laskemiseen käytettävä tietolähde valitsemalla **Tietolähteet**-ruudusta **Lisää juuri**.
3. Syötä **Tietolähteen ominaisuudet** -valintaikkunan **Nimi**-kenttään **TransportRecord**.
4. Valitse **Muokkaa ryhmää** määrittääksesi ryhmittelyehdot.
5. Valitse **Muokkaamisen Group By -parametrit** -sivun oikeanpuoleisen ruudun tietolähdeluettelosta **Tapahtuma**-tietolähde ja laajenna se.
6. Valitse **Lisää kenttä kohteeseen \> Mitä ryhmään** osoittamaan, että **Tapahtuma**-tietolähde on valittu <a name="BaseDataSource">perustietolähteeksi</a> määritetylle **GroupBy**-tietolähteelle. **Tapahtuma**-tietolähteen tietueet ryhmitellään ja tämän tietolähteen kenttäarvoja käytetään koostefunktioiden laskennassa.
7. Valitse **Tapahtuma\Kuljetus** -kenttä ja sitten **Lisää kenttä kohteeseen \> Ryhmitelty kenttä** osoittamaan, että perustietolähteen **Kuljetus**-kenttä on valittu <a name="GroupingFields">ryhmittelyehdoksi</a> määritetylle **GroupBy**-tietolähteelle. Toisin sanoen **Tapahtuma**-tietolähteen tietueet ryhmitellään **Kuljetus**-kentän arvon perusteella. Jokainen konfiguroitu **GroupBy**-tietolähteen tietue vastaa yhtä kuljetuskoodia, jotka on löydetty perustietolähteen tietueista.
8. Valitse **Tapahtuma\AmountMST**-kenttä ja noudata seuraavia ohjeita:

    1. Valitse **Lisää kenttä kohteeseen\>Koostekentät** sen merkiksi , että tälle kentälle lasketaan <a name="AggregateFunctions">koostefunktio</a>.
    2. Valitse **Koosteet**-ruudun siinä tietueessa, joka on lisätty valitulle **Tapahtuma\AmountMST** -kentälle **Menetelmä** -kentässä **Sum**-funktio.
    3. Kirjoita valinnaiseen **Nimi**-kenttään **TotalInvoicedAmount**.

    Nämä asetukset määrittävät, että jokaiselle kuljetusryhmälle lasketaan **Tapahtuma\AmountMST**-kentän kokonaissumma.

9. Valitse **Tapahtuma\RecId**-kenttä ja noudata seuraavia ohjeita:

    1. Valitse **Lisää kenttä kohteeseen \> Koostekentät** sen merkiksi , että tälle kentälle lasketaan koostefunktio.
    2. Valitse **Koosteet**-ruudun siinä tietueessa, joka on lisätty valitulle **Tapahtuma\RecId** -kentälle **Menetelmä** -kentässä **Count**-funktio.
    3. Kirjoita valinnaiseen **Nimi**-kenttään **NumberOfTransactions**.

    Nämä asetukset määrittävät, että jokaiselle kuljetusryhmälle lasketaan ryhmän tapahtumien määrä.

10. Valitse **Tallenna**.
11. Tarkista muokattavan tietolähteen <a name="ExecutionLocation">suoritus</a>parametrit. Huomaa, että **Automaattinen tunnistus** on valittu automaattisesti **Suorituspaikka**-kentässä, ja **Suoritus kohteessa** -kentässä on arvo **SQL**. Nämä asetukset määrittävät, että valittu **Tapahtuma**-perustietolähde on parhaillaan kyselykelpoinen ja voit suorittaa muokattavan **GroupBy**-tietolähteen tietokantatasolla.
12. Tarkista käytettävissä olevien arvojen luettelo avaamalla **Suoritussijainti**-kentän haku. Huomaa, että voit valita **Query** tai **InMemory**, jotta tämä **GroupBy**-tietolähde voidaan suorittaa vastaavasti tietokantatasolla tai sovelluspalvelimen muistissa.
13. Valitse **Tallenna** ja sulje sitten **Muokkaa Group By -parametreja** -sivu.
14. Viimeistele **GroupBy**-tietolähteen asetukset valitsemalla **OK**.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>GroupBy-tietolähteen sitominen tietomallikenttiin

Sido määritetty tietolähde tietomallin kenttiin, jotta voit määrittää, miten tietomalli täytetään sovellustiedoilla suorituksen aikana.

1. Laajenna **Mallin määrityksen suunnittelu** -sivun **Tietomalli**-ruudussa **Kuljetus**-solmu.
2. Laajenna **Tietolähteet**-ruudussa **TransportRecord**-tietolähde.
3. Lisää sidonta, joka paljastaa löydetyt kuljetusryhmät:

    1. Valitse **Tietomalli**-ruudussa **Kuljetus**-kohde.
    2. Valitse **Tietolähteet**-ruudussa **TransportRecord**-tietolähde.
    3. Valitse **Sido**.

4. Lisää sidonta, joka paljastaa kunkin löydetyn kuljetusryhmän kuljetuskoodin:

    1. Valitse **Transport.Code** -tietomallikohde.
    2. Valitse ryhmitelty **TransportRecord.grouped.TransportMode** -kenttä.
    3. Valitse **Sido**.

5. Lisää sitova toiminto, joka paljastaa jokaisen löydetyn kuljetusryhmän lasketut koostefunktiot:

    1. Valitse **Transport.NumberOfTransactions** -tietomallikohde.
    2. Valitse **TransportRecord.aggregated.NumberOfTransactions** -koostekenttä.
    3. Valitse **Sido**.
    4. Valitse **Transport.TotalInvoicedAmount** -tietomallikohde.
    5. Valitse **TransportRecord.aggregated.TotalInvoicedAmount** -koostekenttä.
    6. Valitse **Sido**.

6. Lisää sidonta, joka paljastaa kuhunkin löydettyyn kuljetusryhmään kuuluvat tapahtumatietueet:

    1. Valitse **Transport.Transaction** -tietomallikohde.
    2. Valitse **TransportRecord.lines**-kenttä.
    3. Valitse **Sido**.

    Voit edelleen konfiguroida **Transport.Transaction**-tietomallinimikkeen ja **TransportRecord.lines**-tietolähdekentän upotettujen kohteiden sidonnat, jotta voit suorituksen aikana paljastaa kuhunkin löydettyyn kuljetusryhmään kuuluvien Intrastat-tapahtumien tiedot.

![Konfiguroitu mallin määritys ER-tietomallin määrityksen suunnittelussa.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Lisätyn mallimäärityskomponentin vianmääritys

Määritetyn mallin yhdistämismärityksen testaaminen [ER-tietolähteen virheenkorjauksen](er-debug-data-sources.md) avulla.

1. Valitse **Mallin määrityksen suunnittelu** -sivulla **Aloita virheenkorjaus**.
2. Valitse **Tietolähteiden virheenkorjaus** -sivun vasemmanpuoleisessa ruudussa **TransportRecord**-tietolähde ja valitse sitten **Lue kaikki tiedot**.
3. Laajenna **TransportRecord**-tietolähde ja toimi seuraavasti:

    1. Valitse **TransportRecord.grouped.TransportMode** -tietolähde.
    2. Valitse **Hae arvo**.
    3. Valitse **TransportRecord.grouped.NumberOfTransactions** -tietolähde.
    4. Valitse **Hae arvo**.
    5. Valitse **TransportRecord.grouped.TotalInvoicedAmount** -tietolähde.
    6. Valitse **Hae arvo**.

4. Valitse oikeanpuoleisesta ruudusta **Laajenna kaikki**.

**TransportRecord**-tietolähde paljastaa kaksi tietuetta ja esittää kaksi kuljetuskoodia. Jokaisen kuljetuskoodin osalta lasketaan tapahtumien määrä ja laskutettu kokonaissumma.

> [!NOTE]
> "Laiskan lukemisen" menetelmää käytetään, kun **GroupBy**-tietolähdettä kutsutaan tietokantakutsujen optimoimiseksi. Siksi osa **GroupBy**-tietolähteen kenttäarvoista lasketaan ER-tietolähteen virheenkorjauksessa vain, jos ne on sidottu tietomallikenttiin.

![Tietolähteen virheenkorjauksen tulokset Tietolähteiden virheenkorjaus -sivulla.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Usein kysytyt kysymykset

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Onko mitään tapaa laskea kokonaisloppusummat, kun ryhmän loppusummat lasketaan?

Kyllä. Jos haluat laskea kokonaisloppusummat, määritä toinen **GroupBy**-tietolähde, jossa aiemmin konfiguroimaasi **GroupBy**-tietolähdettä käytetään perustietolähteenä. Seuraavassa kuvassa esitetään **GroupBy**-tyypin **Summat**-tietolähde, jota käytetään **SUM**-funktion laskennassa. Tämä perustuu **GroupBy**-tyypin **TransportRecord**-tietolähteen **SUM**-funktion koostamiseen.

![Summat-tietolähde ER-mallin määrityssuunnittelijassa.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Seuraavassa kuvassa näkyvät **Summat**-tietolähteen virheenkorjauksen tulokset.

![Summat-tietolähteen virheenkorjauksen tulokset Tietolähteiden virheenkorjaus -sivulla.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)
- [Suoritettavan ER-muodon tietolähteiden vianmääritys tiedonkulun ja muunnoksen analysointia varten](er-debug-data-sources.md)
- [DATA COLLECTION -tietolähteiden käyttäminen sähköisissä raportointimuodoissa](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
