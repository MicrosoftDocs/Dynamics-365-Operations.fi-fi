---
title: Varastoarvon raportit
description: Tässä artikkelissa käsitellään varaston arvon raporttien määrittämistä, luomista ja käyttämistä. Näissä raporteissa on tietoja varastotilanteen ja kirjanpitovaraston määristä ja summista.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f97b5bd228c6f769438d50bb27950b8d8fbda3e8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334922"
---
# <a name="inventory-value-reports"></a>Varastoarvon raportit

[!include [banner](../includes/banner.md)]

Varaston arvon raporteissa on tietoja varastotilanteen ja kirjanpitovaraston määristä ja summista. Raportteja voi tarkastella eri tavoin. Esimerkiksi kokonaissummat tai tapahtumat voidaan näyttää tai suodatus voidaan tehdä nimikkeiden tai aikavälin mukaan. Myytyjen tuotteiden kustannusten (MTKUST) arvoja tai keskeneräisen työn (KET) arvoja voidaan tarkastella. Myös muita asetuksia voidaan määrittää.

Varaston arvon raporttien avulla voidaan tehdä seuraavia tehtäviä:

- kirjanpidon ja varaston välinen täsmäyttäminen
- tietyn kauden käytettävissä olevaan varastoon ja arvoihin perehtyminen
- tiettyä tarkoitusta varten räätälöityjen raporttimääritysten luominen
- raporttimääritysten tallentaminen käytettäviksi useita kertoja
- alueiden lisääminen suodattamaan tietoja raporttia suoritettaessa.

## <a name="types-of-inventory-value-report"></a>Varaston arvon raporttityypit

Varaston arvon raporttityyppejä on kaksi: **Varaston arvo** (vakioraportti) ja **Varaston arvon raportin tallennustila**.

### <a name="standard-inventory-value-report"></a>Varaston arvon vakioraportti

**Varaston arvo** -vakioraportti on yksinkertainen raportti, jonka avulla voidaan valita sisällytettävät tiedot ja jossa tiedot sitten näytetään näytöllä. Tuloksia ei tallenneta. Siinä ei ole myöskään vuorovaikutteisia suodatus-, porautumis-, selaus- tai vientiominaisuuksia. Tämän vuoksi **Varaston arvon raportin tallennustila** -raporttia kannattaakin käyttää useimmissa tapauksissa.

### <a name="inventory-value-report-storage-report"></a>Varaston arvon raportin tallennustila -raportti

**Varaston arvon raportin tallennustila** -raportin tuloksena on joko vuorovaikutteinen sivu Microsoft Dynamics 365 Supply Chain Managementissa tai jossakin seuraavassa muodossa viety asiakirja.

Kun tarkastelet raporttia selaimessa, sarakkeita ja yhdistettyjä saldoja muutetaan dynaamisesti määrittämästäsi asettelusta riippuen. Voit esimerkiksi lajitella tulokset, suodattaa ne ja porautua tietoihin.

Raportin tulokset tallennetaan **Varastoarvon** tietoyksikköön. Näin voit suodattaa ja viedä tulokset muotoon, joka voi olla esimerkiksi pilkuilla eroteltu CSV tai Microsoft Excel -muoto.

**Varaston arvon raportin tallennustila** -raportti on kätevä, kun tuloste sisältää useita rivejä. Sinulla on esimerkiksi 50 000 nimikettä, ja 300 myymälää on luotu varastoina. Tässä tapauksessa, jos pyydät varaston loppusaldoja nimikkeen, toimipaikan ja varaston mukaan, tuotos sisältää useita rivejä.

> [!NOTE]
> **Varasto arvon raportin tallennustila** -raportti ei sisällä raporttiasettelussa määritettyjä välisummia. Se ei myöskään sisällä kirjanpidon saldoja, vaikka kyseiset saldot olisi määritetty raportin asettelussa. Täsmäytys kirjanpitoon on tehtävä käyttämällä pääkirjasaldoja. **Raportin arvo** -vakioraportti sisältää kuitenkin nämä välisummat ja saldot.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Varaston arvon raportin tallennusominaisuuden ottaminen käyttöön tai pois käytöstä

Jos haluat käyttää tätä ominaisuutta, se on otettava käyttöön järjestelmässä. Supply Chain Managementin versiosta 10.0.25 alkaen tämä ominaisuus on oletusarvoisesti käytössä. Supply Chain Managementin versiosta 10.0.29 alkaen tämä toiminto on pakollinen, eikä sitä voi poistaa käytöstä. Jos käytät vanhempaa versiota kuin 10.0.29, järjestelmänvalvojat voivat ottaa tämän toiminnon käyttöön tai pois käytöstä hakemalla *Varastoarvoraporttien säilö* -toimintoa [Toimintojen hallinta](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) -työtilassa.

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Varaston arvon raporttimääritysten määrittäminen

**Varaston arvon raportit** -sivulla määritetään sisältö, joka sisällytetään erityyppisiin varaston arvon raportteihin. Määritettävien raporttityyppien määrää ei ole rajoitettu. Raportin tyyppi valitaan aina, kun jompikumpi varaston arvon raporttityyppi määritetään.

1. Valitse **Kustannushintojen hallinta \> Varaston kirjanpitokäytäntöjen määrittäminen \> Varaston arvon raportit**.
1. Noudata seuraavia ohjeita:

    - Aiemmin luotua raporttia voi muokata valitsemalla sen luetteloruudussa ja valitsemalla sitten toimintoruudussa **Muokkaa**.
    - Uusi raportti luodaan valitsemalla toimintoruudussa **Uusi**.

1. Määritä uuden tai valitun raportin otsikossa seuraavat kentät:

    - **Tunnus** – Anna raportille lyhyt tunnus. Tämän arvon on oltava yksilöivä kaikkiin muihin varaston arvon raporttimäärityksiin nähden. Sitä ei voi muokata, kun uusi määritys on tallennettu.
    - **Nimi** – anna raportille kuvaava nimi.

1. Jos kyse on uusista raporttimäärityksistä, valitse toimintoruudussa **Tallenna**, jolloin loput kentät tulevat käyttöön.
1. Valitse **Yleiset**-pikavälilehdellä seuraavat lisäkentät:

    - **Päivämääräväli** – Valitse esimääritetty päivämääräväli. Tämä päivämääräväli voidaan ohittaa, kun raportti suoritetaan.
    - **Alue** – valitse *Kirjauspäivä* tai *Tapahtuman aika* sen päivämäärän ja ajan mukaan, joita käytetään noudettaessa tietueita raporttiin.
    - **Dimensioyhdistelmä** – Valitse suoritettavien tietojen dimensioyhdistelmä. (Dimensiot määritetään kirjanpidossa.) Tiedot voidaan suorittaa esimerkiksi *päätilille* tai *päätilille ja liiketoimintayksikölle*. Valitussa dimensioyhdistelmässä saa olla enintään kaksi dimensiota. Lisätietoja on kohdassa [Taloushallinnon dimensioyhdistelmät](../../finance/general-ledger/financial-dimension-sets.md).

1. Määritä **Sarakkeet**-pikavälilehdessä seuraavat kentät: Näiden kenttien avulla määritetään raporttiin sisältyvät sarakkeet ja kyseisten sarakkeiden tietotyypit.

    - **Varasto** – Varaston arvot näytetään, kun valitset asetukseksi *Kyllä*. Nämä arvot voidaan täsmäyttää sitten kirjanpitotilin saldojen kanssa.
    - **KET** – Varaston KET-arvot näytetään, kun valitset asetukseksi *Kyllä*. Nämä arvot voidaan täsmäyttää sitten KET-tilin saldojen kanssa kirjanpidossa. Kun asetukseksi valitaan *Kyllä*, raportti näyttää ne varastotilanteen määrät ja summat, joiden tila on KET. Tuotantotilaukset, joiden tila on KET, on valittu tai raportoitu valmiiksi, mutta niitä ei ole päätetty.
    - **Lykätty MTKUST** – Kun asetukseksi valitaan *Kyllä*, näytettävässä sarakkeessa näkyy lykätyn myytyjen tuotteiden kustannusten varastotilanteen määrät ja summat. Lykätty MTKUST näytetään käyttämällä varastotilanteen määriä ja summia, koska sillä tehdään pakkausluettelon määrien ja summien vastakirjaus.
    - **MTKUST** – Kun asetukseksi valitaan *Kyllä*, näytettävässä sarakkeessa näkyy myytyjen tuotteiden kustannusten kirjanpitovaraston määrät ja summat. MTKUST näytetään käyttämällä kirjanpitovaraston määriä ja summia, koska sillä tehdään laskun määrien ja summien vastakirjaus.
    - **Tulos** – kun asetukseksi valitaan *Kyllä*, näytettävässä sarakkeessa näkyy kirjanpitovaraston summa, joka kirjattiin varaston tulostileille.
    - **Tulosta kumulatiiviset tiliarvot vertailua varten** – Kun asetukseksi valitaan *Kyllä*, näytettävässä sarakkeessa näytetään kirjanpitotilin saldo. Tällä tavoin pääkirjaa ei tarvitsee. Tätä asetusta voi käyttää vain **Raportin arvo** -vakioraportissa; sitä ei siis käytetä **Varaston arvon raportin tallennustila** -raportissa. Kun asetukseksi on valittu *Kyllä*, seuraavien kenttien avulla on määritettävä kukin kirjanpitotili, joka halutaan luetteloon. Tämä perustuu käyttöönotettuihin **Taloushallinnon toimi** -vaihtoehtoihin.

        > [!NOTE]
        > Jos johonkin näistä kentistä valitaan *summatili*, sekä kunkin summatiliin sisällytetyn varastotilin summa että summatilin summa näytetään.

        - **Varastotili** – Määritä kirjanpitotili, jonka varastotiedot näytetään. (Sekä **Varasto**- että **Tulosta kumulatiiviset tiliarvot vertailua varten** -vaihtoehdon asetuksena on oltava *Kyllä*.)
        - **KET-tili** – Määritä kirjanpitotili, jonka KET-tiedot näytetään. (Sekä **KET**- että **Tulosta kumulatiiviset tiliarvot vertailua varten** -vaihtoehdon asetuksena on oltava *Kyllä*.)
        - **Lykätty MTKUST-tili** – Määritä kirjanpitotili, jonka lykätyt MTKUST-tiedot näytetään. (Sekä **Lykätty MTKUST**- että **Tulosta kumulatiiviset tiliarvot vertailua varten** -vaihtoehdon asetuksena on oltava *Kyllä*.)
        - **MTKUST-tili** – Määritä kirjanpitotili, jonka MTKUST-tiedot näytetään. (Sekä **MTKUST**- että **Tulosta kumulatiiviset tiliarvot vertailua varten** -vaihtoehdon asetuksena on oltava *Kyllä*.)

    - **Tee yhteenveto fyysisistä ja taloudellisista arvoista** – Kun asetukseksi valitaan *Kyllä*, varaston kokonaismäärän ja -summan näyttävä sarake näytetään. (Se on yhteenveto sekä varastotilanteen että kirjanpitovaraston arvoista.) Jos asetukseksi on valittu *Ei*, raportti näyttää sekä varastotilanteen että kirjanpitovaraston arvot.
    - **Sisällytä kirjanpitoon kirjaamattomat** – Kun asetukseksi valitaan *Kyllä*, näytettävä sarake näyttää tapahtumat, joita ei koskaan kirjattu kirjanpitoon. Seuraavien nimiketyyppien tapahtumia ei ole ehkä kirjattu kirjanpitoon:

        - Vastaanotetut mutta vielä laskuttamattomat nimikkeen, kun liittyvän nimimalliryhmän **Kirjaa varastotilanne** -vaihtoehdon valinta on poistettu.
        - Vastaanotetut mutta laskuttamattomat nimikkeen, kun **Kirjaa vastaanotto kirjanpitoon** -vaihtoehdon valinta on poistettu **Tuotteen vastaanotto** -pikavälilehdessä **Ostoreskontran parametrit** -sivun **Yleiset**-välilehdessä (**Ostoreskontra \> Asetukset \> Ostoreskontran parametrit**).

    - **Laske keskimääräinen yksikkökustannus** – Kun asetuksena on *Kyllä*, näytettävä sarake näyttää keskimääräisen yksikkökustannuksen. Keskimääräinen yksikkökustannus on kokonaismäärällä jaettu kokonaissumma.
    - **Kokonaismäärä ja -arvo** – Kun asetukseksi valitaan *Kyllä*, näytettävät sarakkeet näyttävät varastotilanteen (ja kirjanpitovaraston määrien) kokonaismäärän sekä varastotilanteen (ja kirjanpitovaraston summien) kokonaissumman. Voit määrittää tämän asetuksen arvoksi *Kyllä* vain, jos **Tee yhteenveto fyysisistä ja taloudellisista arvoista** -asetuksen arvoksi on määritetty *Ei*.
    - **Varastodimensiot** – Tässä ruudukossa valitaan kunkin raportissa näytettävän dimension **Näytä**-valintaruutu. Vain niiden dimensioiden arvot näkyvät raportissa, joissa **Kirjanpitovarasto**-asetus on otettu käyttöön. Muissa dimensioissa näkyy vain tyhjiä sarakkeita. Näytettäviksi valituissa dimensioissa voidaan lisäksi näyttää yhteissummat valitsemalla **Yhteensä**-valintaruutu.
    - **Resurssitunnus** – Kun **Näytä**-asetukseksi valitaan *Kyllä*, näytettävä sarake määrittää nimikkeen kullekin riville. Myös yhteissummat näytetään, kun **Yhteensä**-asetukseksi valitaan *Kyllä*. Kullakin rivillä olevan nimikkeen perusteella sarakkeessa näkyy jokin seuraavista tietotyypeistä:

        - **Materiaali** – sarakkeessa näkyy soveltuvan materiaalitietueen `ItemID`-kentän arvo.
        - **Työ** – sarakkeessa näkyy soveltuvan työtietueen `WorkCenterID`-kentän arvo.
        - **Välillinen kustannus** – sarakkeessa näkyy soveltuvan kustannustietueen `CodeID`-kentän arvo.

        Jos sekä **Resurssitunnus**- että **Resurssiryhmä**-kentän **Näytä**-asetukseksi on valittu *Ei*, näkyvissä on vain valittuihin varastodimensioihin perustuva varaston kokonaisarvo.

    - **Resurssiryhmä** – Kun **Näytä**-asetukseksi valitaan *Kyllä*, näytettävä sarake määrittää resurssiryhmän kullekin riville. Myös yhteissummat näytetään, kun **Yhteensä**-asetukseksi valitaan *Kyllä*. Kullakin rivillä olevan nimikkeen perusteella sarakkeessa näkyy jokin seuraavista tietotyypeistä:

        - **Materiaali** – sarakkeessa näkyy soveltuvan materiaalitietueen `ItemGroup`-kentän arvo.
        - **Työ** – sarakkeessa näkyy soveltuvan työtietueen `WorkcenterGroup`-kentän arvo.
        - **Välillinen kustannus** – sarakkeessa näkyy soveltuvan kustannustietueen `CostGroup`-kentän arvo. (`CostGroupType`-arvon on oltava *Epäsuora*.)

        Jos sekä **Resurssitunnus**- että **Resurssiryhmä**-kentän **Näytä**-asetukseksi on valittu *Ei*, näkyvissä on vain valittuihin varastodimensioihin perustuva varaston kokonaisarvo.

1. Määritä **Rivit**-pikavälilehdessä seuraavat kentät. Näiden kenttien avulla voidaan lisätä vastaavia keskeneräiseen työhön liittyviä aliosia raporttiin tai poistaa niitä.

    - **Materiaali** – Kun asetukseksi on valittu *Kyllä*, materiaalia koskevia tietoja näytetään. *Materiaali* on oletusresurssityyppi, koska luotettavan tuloksen luonti edellyttää, että materiaalit sisällytetään kaikkiin raporttimäärityksiin.
    - **Työ** – kun asetukseksi valitaan *Kyllä*, keskeneräisen työn työkustannukset näytetään.
    - **Välillinen kustannus** – kun asetukseksi valitaan *Kyllä*, keskeneräisen työn välilliset kustannukset näytetään.
    - **Suora ulkoistaminen** – Kun asetukseksi valitaan *Kyllä*, keskeneräisen työn suoran ulkoistamisen kustannukset näytetään. Tästä tiedostoa on hyötyä alihankinnassa.
    - **Erittelytaso** – Raportin näyttöasetuksen valinta:

        - *Tapahtumat* – Kaikki liittyvien tapahtumien näyttäminen raportissa. Huomaa, että suorituskykyongelmia voi esiintyä, jos tarkasteltavissa raporteissa on runsaasti tapahtumia. Niinpä tätä asetusta käytettäessä kannattaa käyttää **Varaston arvon raportin tallennustila** -raporttia.
        - *Yhteensä* – yhteistuloksen näyttäminen.

    - **Sisällytä alkusaldo** – Kun asetukseksi valitaan *Kyllä*, alkusaldo näytetään. Tämä asetus on käytettävissä vain, kun **Erittelytaso**-kentän asetuksena on *Tapahtumat*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Varaston arvon raportin tallennustila -raportin luominen

**Varaston arvon raportin tallennustila** -raportti luodaan ja tallennetaan seuraavasti:

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston arvoraportin tallennus**.
1. Valitse toimintoruudussa **Uusi**.
1. Määritä **Varaston arvo** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Nimi** – anna raportille yksilöivä nimi.
    - **Tunnus** – Valitse raportissa käytettävät [varaston arvon raporttimääritykset](#report-configuration). Määritykset määrittävät raporttiin sisällytettävät sarake- ja rivivaihtoehdot.
    - **Päivämääräväli** – Tämän osan kenttien avulla määritetään, mitkä tietueet sisällytetään raporttiin. Voit määrittää päivämäärävälin joko valitsemalla esimääritetyn alueen (suhteessa raportin luontipäivämäärään) **Päivämäärävälin koodi** -kentässä tai valitsemalla tietyt päivämäärät **Alkamispäivä**- ja **Päättymispäivä**-kentistä.

1. Määritä **Sisällytettävät tietueet** -pikavälilehdessä suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät tiedot. Valitse **Suodatin**, jolloin vakiokyselyeditori-ikkuna avautuu. Tässä ikkunassa määritetään valinta- ja lajitteluehdot sekä liitokset. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Supply Chain Managementissa. Kaikkia näitä suodattimia käytetään varastotapahtumissa muttei kirjanpidon saldossa. Tämä kannattaa muistaa suodattimia määritettäessä. Muussa tapauksessa varaston ja kirjanpidon välillä saattaa esiintyä ristiriitoja.
1. Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein raportti luodaan. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.

    > [!NOTE]
    > Tämä raportti suoritetaan aina osana erätyötä.

1. Ota asetukset käyttöön valitsemalla **OK** ja sulje valintaikkuna.

Kun erätyö on valmis, raportti näkyy **Varaston arvon raportin tallennus** -sivulla. Sivu on ehkä päivitettävä, ennen kuin päivitetty raportti tulee näkyviin.

> [!IMPORTANT]
> Valitussa varaston arvon raporttimäärityksessä voidaan saada virheellinen alkusaldo, jos sama päivämäärä valitaan sekä **Päivämäärästä**- että **Päivämäärään**-kentässä ja jos **Sisällytä alkusaldo** -asetuksena on *Kyllä*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Varaston arvon raportin tallennustila -raporttiin tutustuminen

Kun olet luonut raportin, voit tarkastella sitä ja tutustua sen tietoihin milloin tahansa seuraavien ohjeiden mukaisesti.

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston arvoraportin tallennus**.
1. Valitse raportti luettelosta. Tällä sivulla näytetään valitun raportin luontiin käytetyn [varaston arvon raporttimääritysten](#report-configuration) tiedot.
1. Näytä raportin sisältö valitsemalla toimintoruudussa **Näytä tiedot**.
1. Tutki raporttia noudattamalla seuraavia vaiheita:

    - Kuten useimmilla standardisivuilla Supply Chain Management -sovelluksessa voit valita melkein minkä tahansa sarakkeen otsikon lajitellaksesi tai suodattaaksesi ruudukon kyseisen sarakkeen arvojen perusteella.
    - **Suodatin**-kentän avulla voit suodattaa raportin minkä tahansa useiden käytettävissä olevan sarakkeen arvon mukaan.
    - Käytä näytä-valikkoa ( **Suodatin**-kentän yläpuolella) lajittelu- ja suodatusvaihtoehtojen suosikkiyhdistelmien tallentamiseen ja lataamiseen.

## <a name="export-an-inventory-value-report-storage-report"></a>Varaston arvon raportin tallennustila -raportin vieminen

Jokainen luotu raportti tallennetaan **Varastoarvo**-tietoentiteettiin. Voit käyttää Supply Chain Management -sovelluksen vakiotiedonhallintatoimintoja, jos haluat viedä tämän entiteetin tiedot mihin tahansa tuettuun tietomuotoon, kuten CSV- tai Excel-muotoon.

Seuraavassa esimerkissä näytetään, miten **Varaston arvon raportin tallennustila** -raportti viedään.

1. Valitse **Järjestelmänhallinta \> Työtilat \> Tietojen hallinta**.
1. Valitse **Vienti/Tuonti**-osassa **Vienti**-ruutu.
1. Näkyviin tulevalla **Vie**-sivulla voit määrittää vientityön. Syötä ensin työlle ryhmänimi.
1. Valitse **Valitut yksiköt** -osassa **Lisää yksikkö**.
1. Näyttöön tulevassa valintaikkunassa kuvaillaan seuraavat kentät:

    - **Yksikön nimi** – Valitse *Varastoarvo*.
    - **Kohteen tietomuoto** – Valitse muoto, johon tiedot viedään.

1. Valitse **Lisää**, jos haluat lisätä uuden rivin. Valitse sitten **Sulje**, jolloin valintaikkuna suljetaan.
1. Tavallisesti viedään yksi raportti kerralla. Jos haluat viedä yksittäisen raportin, määritä suodattimen avulla **Kysely**-valintaikkunaan juuri lisäämäsi rivi. Näin voit määrittää, mikä **Varastoarvo**-kohteen raportti sisältyy vientiin. Määritä seuraavat suodatusasetukset seuraavien vaiheiden mukaisesti viedäksesi yhden raportin:

    1. Valitse **Väli**-välilehdessä **Lisää**, jos haluat lisätä rivin.
    2. Aseta **Taulu**-kentän arvoksi *Varastoarvo*.
    3. Aseta **Johdettu taulu** -kentän arvoksi *Varastoarvo*.
    4. Määritä **Kenttä**-kenttä sille kentälle, jonka mukaan haluat suodattaa. Yleensä käytetään **Suorituksen nimi** -kenttää ja/tai **Suoritusaika**-kenttää.
    5. Määritä **Ehto**-kentästä arvo, jonka haluat etsiä valitusta kentästä. (Jos valitsit **Suorituksen nimi** -kentän edellisessä vaiheessa, tämä arvo on raportin nimi. Jos valitsit **Suoritusaika**-kentän, se on aika, jolloin raportti luotiin.)
    6. Lisää tarvittaessa rivejä **Väli**-välilehteen, kunnes olet yksilöinyt etsittävän raportin.

1. Valitse **OK** tallentaaksesi asetukset ja sulje valintaikkuna.
1. Tallenna vientiasetukset valitsemalla **Tallenna**.
1. Valitse **Vientiasetukset**-välilehdellä **Vie nyt** luodaksesi vientitiedoston.
1. Näkyviin tulevalla **Suorituksen yhteenveto** -sivulla näkyy vientityön tila ja vietyjen entiteettien luettelo. Valitse **Entiteetin käsittelyn tila** -osassa listasta **Varaston arvo** -yksikkö. Lataa tästä yksiköstä viedyt tiedot valitsemalla **Lataa tiedosto**.

Lisätietoja tietojen hallinnan käyttämisestä tietojen viemisessä on kohdassa [Tietojen tuonti- ja vientitöiden yleiskatsaus](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Varaston arvon vakioraportin luominen

**Varaston arvo** -vakioraporttia luodaan seuraavasti:

1. Valitse **Kustannushintojen hallinta \> Kyselyt ja raportit \> Varaston kirjanpidon tilaraportit \> Varaston arvo**.
1. Määritä **Varaston arvon raportti** -valintaikkunan **Parametrit**-pikavälilehdessä seuraavat kentät:

    - **Nimi** – anna raportille yksilöivä nimi.
    - **Tunnus** – Valitse raportissa käytettävät [varaston arvon raporttimääritykset](#report-configuration). Määritykset määrittävät raporttiin sisällytettävät sarake- ja rivivaihtoehdot.
    - **Päivämääräväli** – Tämän osan kenttien avulla määritetään, mitkä tietueet sisällytetään raporttiin. Voit määrittää päivämäärävälin joko valitsemalla esimääritetyn alueen (suhteessa raportin luontipäivämäärään) **Päivämäärävälin koodi** -kentässä tai valitsemalla tietyt päivämäärät **Alkamispäivä**- ja **Päättymispäivä**-kentistä.

1. Määritä **Sisällytettävät tietueet** -pikavälilehdessä suodattimet ja rajoitteet, joiden avulla määritetään raporttiin sisällytettävät tiedot. Valitse **Suodatin**, jolloin vakiokyselyeditori-ikkuna avautuu. Tässä ikkunassa määritetään valinta- ja lajitteluehdot sekä liitokset. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Supply Chain Managementissa.
1. Määritä **Suorita taustalla** -pikavälilehdessä, miten, milloin ja kuinka usein raportti luodaan. Kentät toimivat samalla tavalla kuin muissakin [taustatöissä](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Supply Chain Managementissa.
1. Ota asetukset käyttöön valitsemalla **OK** ja sulje valintaikkuna. Raportti avautuu.

## <a name="reading-inventory-value-reports"></a>Varaston arvon raporttien lukeminen

Tässä osassa on ohjeita raportin lukemiseen ja varaston arvon raportin hahmottamiseen.

Supply Chain Management tukee kahta varaston tilaa liittyvää tärkeää käsitettä:

- **Taloudellinen päivitys** – Tämä käsite ilmaisee, että varastotapahtumat on jo laskutettu. Tuotantotilausten osalta se ilmaisee tuotantotilauksen päättymisen.
- **Fyysinen päivitetty** – Tämä käsite ilmaisee, että vaikka varastotapahtumia ei ole vielä laskutettu, ne on vastaanotettu tai lähetetty. Tuotantotilausten osalta se ilmaisee, että materiaali on poimittu tai että tuotantotilaus on raportoitu valmiiksi.

Kun nämä kaksi käsitettä ovat hallussa, raporttitulosteen seuraavat sarakkeet on helppo ymmärtää:

- **Varasto: rahoitusmäärä** – taloudellisesti päivitetty määrä.
- **Varasto: rahoitussumma** – taloudellisesti päivitetyn varaston arvon summa.
- **Varasto: kirjattu fyysinen määrä** – fyysisesti päivitetty määrä.
- **Varasto: kirjattu fyysinen summa** – fyysisesti päivitetyn varaston arvon summa.
- **Varasto: kirjaamaton fyysinen määrä** – Määrä, jossa on kirjanpitoon kirjaamattomia varastotapahtumia. Esimerkki: Nimikemalliryhmässä **Kirjaa varastotilanne**- ja **Kirjaa varastokirjanpito** -asetusten valinta on poistettu, mutta kyseiseen ryhmään on linkitetty nimike. Ostotilaus luodaan, vastaanotetaan ja laskutetaan. Jos tässä vaiheessa tarkastellaan nimikkeen varaston arvon raporttia, huomataan, että ostotilauksen määrä ja arvo näkyvät **Varasto: kirjaamaton fyysinen määrä**- ja **Varasto: kirjaamaton fyysinen summa** -sarakkeissa.
- **Varasto: kirjaamaton fyysinen summa** – Raportit voidaan määrittää näyttämään kirjaamattomat summat. Tätä arvoa ei pidä kuitenkaan käyttää, jos käytössä on varaston täsmäytysraportti. Jos sitä käytetään, summaa ei kirjata kirjanpitoon.
- **Varasto: määrä** – tietueen kaikki määräsarakkeiden määrä yhteensä.
- **Varasto: summa** – Tietueen kaikki summasarakkeiden määrä yhteensä. Varaston täsmäytystä käytettäessä tätä saraketta ei pidä käyttää, jos raportissa on **Varasto: kirjaamaton fyysinen summa** -sarake. Siinä tapauksessa **Varasto: kirjaamaton fyysinen summa** -summa on jätettävä pois kokonaissummasta.
- **Keskimääräinen yksikkökustannus** – kokonaismäärällä jaettu kokonaissumma.

Yleensä varaston arvon raporttia käytetään varaston arvon ja määrän tarkastelemiseen. Joskus kaikki liittyvät varastodimensiot eivät kuitenkaan näy raportissa. Jos odotetut dimensiot eivät näy raportissa, tarkista seuraavat asetukset:

- Tarkista nimikkeen varasto- ja seurantadimensioryhmät. Vain niiden dimensioiden arvot voidaan näyttää raportissa, joissa **Kirjanpitovarasto**-asetus on otettu käyttöön.
- Valitse **Kustannushintojen hallinta \> Varaston kirjanpitokäytäntöjen määrittäminen \> Varaston arvon raportit**, valitse sitten raportin luontiin käytetyt raporttimääritykset ja varmista, että tarvittavat varastodimensiot on valittu **Näytä**-sarakkeessa.

Esimerkki: Nimikkeen nimiketunnus on *A0001*. Varastodimensioryhmässä varastokirjanpito on otettu käyttöön vain toimipaikassa. Varastotilanne on otettu käyttöön sekä toimipaikassa että varastossa. Seurantadimensioryhmässä eränumero otettu käyttöön varastotilanteessa mutta ei kirjanpitovarastossa. Tämän jälkeen käytetään raporttimääritystä, jossa valitaan niin toimipaikka, varasto kuin eränumerokin. Raporttia tarkasteltaessa näkyvissä on toimipaikan arvo. Varaston ja eränumeron sarakkeet ovat tyhjiä. Tämä esimerkki osoittaakin, että varaston arvot raportit näyttävät vain kirjanpitovarastossa käyttöönotetun varastodimension.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
