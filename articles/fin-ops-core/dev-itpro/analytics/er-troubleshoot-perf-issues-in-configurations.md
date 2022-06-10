---
title: ER-konfiguraatioiden suorituskykyongelmien vianmääritys
description: Tässä ohjeaiheessa on tietoja sähköisen raportoinnin konfiguraatioiden suorituskykyyn liittyvistä ongelmista ja korjaamisesta.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERFormatMappingRunJobTable, ERParameters, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: maximbel
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e727e06c73ff445bf4219ac5a9eee7bec25740d9
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811677"
---
# <a name="troubleshooting-performance-issues-in-er-configurations"></a>ER-konfiguraatioiden suorituskykyongelmien vianmääritys

Tässä ohjeaiheessa on tietoja [sähköisen raportoinnin](general-electronic-reporting.md) (ER) [konfiguraatioiden](general-electronic-reporting.md#Configuration) suorituskykyyn liittyvistä ongelmista ja niiden ratkaisemisesta.

Suorituskyvyn tutkimus käsittää yleensä useita vaiheita.

1. [Kerää](#collecting-data) tiedot.
2. Analysoi kerätyt tiedot.
3. Analyysin tulosten perusteella voit [tehdä muutoksia](#making-changes) ER-konfiguraatioiden avulla tai päättää kerätä lisää tietoja.

## <a name="troubleshooting"></a>Vianmääritys

### <a name="analyze-execution-time"></a>Suoritusajan analysoiminen

Suoritusaika voi riippua odottamattomista seikoista, kuten muista samassa ympäristössä suoritetuista tehtävistä ja välimuistista, joka käyttää tietoja ensimmäisen kutsumisen yhteydessä. Siksi sinun on toistettava suoritus ja mittaus useita kertoja.

Joskus suorituskykyongelmat eivät johdu raportoinnissa käytettävästä ER-muodon konfiguraatiosta. Sen sijaan ne johtuvat X++-koodista, jota käytetään tämän ER-muodon konfiguraation avaamiseen.

1. Voit tarkastella raportin suoritusaikaa joko [toimintokeskuksessa](#infolog-time) tai [tapahtumalokissa](#event-log-time).
2. Vertaa raportin suoritusaikaa skenaarion kokonaissuoritukseen.
3. Jos raportin suoritusaika on paljon pienempi kuin kokonaissuorituksen aika, ota huomioon raportin käsittelemien tietojen määrä:

    - Jos raportissa on pieni määrä tietoja, ongelma saattaa liittyä konfiguraation latausaikaan.
    - Jos raportti käsittelee paljon tietoja, ongelma saattaa liittyä X++-koodin esikäsittelyyn. Analysoi tämä tapaus [jäljitysjäsentimen](#analyze-trace-parser-trace) avulla.

    Lisätietoja on seuraavissa osissa.

4. Suorita useita testejä, joihin liittyy erilaisia tietomääriä. Näin voit määrittää, miten suoritusaika määräytyy datamäärän mukaan.

### <a name="analyze-trace-parser-traces"></a><a name="analyze-trace-parser-trace"></a>Analysoi jäljityksen jäsentimen jäljitykset

Valmistele pieni esimerkki tai kerää useita jäljityksiä raportin luonnin satunnaisten osien aikana.

Tee sitten [jäljityksen jäsentimessä](#trace-parser) normaali alhaalta ylöspäin -analyysi ja vastaa seuraaviin kysymyksiin:

- Mitkä ovat ajan kulutuksen kannalta käytetyimmät metodit?
- Kuinka suuren osan kokonaisajasta nämä metodit käyttävät?

Vastaa samoihin kysymyksiin kyselyiden osalta.

Jos näet, että menetelmien etuliitteenä on "ER", siirry seuraavaan osaan.

Jos näet, että metodit tai kyselyt ovat peräisin sovelluspaketista, kannattaa käyttää yleisiä optimointeja (esimerkiksi indeksien luontia).

Analysoi kutsujen määrä. Jos määrä on odotettua suurempi, harkitse konfiguraation vastaavien solmujen välimuistiin tallentamista.

### <a name="analyze-database-calls"></a><a name="analyze-database-calls"></a>Tietokantakutsujen analysoiminen

Valmistele esimerkki, jossa on hieman tietoja, jotta voit kerätä [ER-jäljityksen](#electronic-reporting-traces).

Avaa sitten jäljitys ER-mallin määritysten suunnitteluohjelmassa ja katso sivun alaosaa. Vastaa seuraaviin kysymyksiin:

- Onko kyselyiden kaksoiskappaleita? Jos on, harkitse jotakin seuraavista korjauksista:

    - [Käytä välimuistiintallentamista](#use-caching), jos yhdessä päätietueessa on useita kutsuja.
    - [Käytä välimuistiin tallennettua ja parametrien perusteella laskettua kenttää](#cached-parameterized), jos samaan tietueeseen kohdistuu kutsuja eri tietueissa.
    - [Käytä **JOIN**-tietolähdettä](#use-join-datasource), jos sinun on luettava eri tietokannasta merkittävä määrä eri tietueita.

- Vastaako kyselyiden ja noudettujen tietueiden määrä yleistä tietomäärää? Jos asiakirjassa on esimerkiksi 10 riviä, osoittavatko tilastotiedot, että raportti sisältää 10 riviä tai 1 000 riviä? Jos sinulla on noudettuna suuri tietueiden määrä, ota huomioon jokin seuraavista korjauksista:

    - [Käytä **FILTER**-toimintoa **WHERE**-toiminnon asemesta](#filter), kun käsittelet tietoja Microsoft SQL Serverin puolella.
    - Välimuistiin tallentaminen estää samojen tietojen hakemisen.
    - [Koostavia tietofunktioita käyttämällä](#collected-data) voidaan välttää samojen tietojen hakeminen yhteenvetoa varten.

### <a name="analyze-perfview-traces"></a>PerfView-jäljityksen analysoiminen

[PerfView](#perfview) on työkalu kokeneille kehittäjille. Lisätietoja seuraavista vaiheista on ohjeaiheessa [Seinäkellon ajan tutkimuksen perustiedot](https://channel9.msdn.com/Series/PerfView-Tutorial/Tutorial-12-Wall-Clock-Time-Investigation-Basics).

1. Kerää jäljitys säieajan avulla.
2. Sisällytä vain pinot, jotka käyttävät **runUnattended**-määritystä, kun haluat suodattaa vain konfiguraation suorittamisen sisältävät säikeet. (Lisää **runUnattended** **IncPats**-syöttöruutuun.)
3. Kerää kaikki, suorittimen, verkon ja estojen ajat.
4. Lataa [PerfViewin ER-esimääritykset](https://download.microsoft.com/download/2/d/0/2d037b0f-ffd1-4d65-b64f-fcdf51f2c81f/ER_PerfViewPresets.xml).
5. Valitse **ER** \> **Muu esimääritys**.
6. Tarkastele nimiä:

    - Todennäköisesti näet alustan koodin, joka kuluttaa eniten aikaa.
    - Voit kaksoisnapauttaa (tai kaksoisnapsauttaa) ja käydä läpi **kutsuttavia kohteita**.

        Jos käytössä on luokkia, joissa on etuliite "ERExpression" ja jos ne ovat kaavoihin liittyviä toimintoja, voit päätellä toiminnon nimen luokan nimen perusteella ja voit tarkastella määritteitä ER-säilössä.

### <a name="fixes"></a>Korjaukset

- Jos kyselyt kuluttavat suurimman osan suorittimen ajasta, yritä vähentää kyselyiden määrää:

    - [Tarkista ER-jäljitys](#analyze-database-calls) kaksoiskappalekyselyiden varalta.
    - Katso, montako tietuetta haetaan, ja arvioi, paljonko tietoja pitäisi teoreettisesti hakea.

- Jos näet, että käytettävät toiminnot kuluttavat suurimman osan suorittimen ajasta, etsi konfiguraation paikka, joka kuluttaa eniten resursseja.
- Jos näet, että tietojen keruutoiminnot kuluttavat suurimman osan suoritinajasta, kannattaa mallin määrityspuolella korvata ne *SQL:n GROUP BY -määrityksellä*.

### <a name="collecting-data"></a><a name="collecting-data"></a>Tietojenkeruu

Ympäristösi mukaan saatavilla olevia tietoja voidaan kerätä useilla eri tavoilla:

- Hae kokonaissuoritusaika:

    - Toimintokeskuksesta
    - Tapahtumalokista

- Profiloi suoritus:

    - ER-työkalujen avulla
    - Jäljityksen jäsennyksen avulla
    - PerfViewin avulla

#### <a name="collecting-data-in-a-production-environment"></a>Tietojen kerääminen tuotantoympäristössä

Joskus ongelmat voidaan toistaa vain tuotantoympäristössä. Tietoja voidaan kerätä seuraavilla tavoilla:

- [Jäljityksen jäsentimen](../perf-test/trace-trace-tutorial.md) jäljityksien avulla
- Käyttämällä [ER-suorituksen](trace-execution-er-troubleshoot-perf.md) jäljitystä
- Käyttämällä kokonaissuorituksen aikaa

#### <a name="collecting-data-in-a-development-environment"></a>Tietojen kerääminen kehitysympäristössä

Tuotantoympäristössä käytettävissä olevien mainittujen työkalujen lisäksi kehitysympäristössä voi käyttää useita työkaluja:

- Tapahtumaloki (Microsoft-Dynamics-ElectronicReporting). Tämä loki voi antaa sinulle kokonaissuorituksen ajan.
- Yleiset .NET-työkalut, esimerkiksi PerfView.

Kehitysympäristön avulla voit myös joustavammin kokeilla. Voit esimerkiksi poistaa raporttien osia käytöstä, kun haluat nähdä, miten suoritusaika vaikuttaa.

### <a name="tools"></a><a name="tools"></a>Työkalut

#### <a name="execution-time-in-the-action-center"></a><a name="infolog-time"></a>Suoritusaika toimintokeskuksessa

ER voi näyttää konfiguraation suoritusajan toimintokeskuksessa. Tämä vaihtoehto toimii vain tietylle käyttäjälle ja tietylle yritykselle, ja vain vuorovaikutteisissa istunnoissa. Voit ottaa tämän ominaisuuden käyttöön noudattamalla seuraavia ohjeita.

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Käyttäjän parametrit** -valintaikkunassa **Näytä tiedoston luontiaika** -valinnaksi **Kyllä**.

#### <a name="execution-time-in-the-event-log"></a><a name="event-log-time"></a>Suoritusaika tapahtumalokissa

1. Avaa Windowsin tapahtumien katseluohjelma.
2. Avaa **Sovellukset ja palvelut** -kohdassa **Microsoft-Dynamics-ElectronicReporting/Operational**.
3. Etsi **FormatMapingRun**-tapahtumia, joissa **EventID=2**, koska nämä tapahtumat sisältävät kulunutta aikaa koskevat tiedot.

#### <a name="trace-parser-traces"></a><a name="trace-parser"></a>Jäljityksen jäsentimen jäljitykset 

Koska ER on toteutettu X++-koodilla, voit käyttää yleisiä X++-työkaluja suorituskyvyn analysoimiseen. Lisätietoja on kohdassa [Jäljityksen ottaminen jäljityksen jäsennyksen avulla](../perf-test/trace-trace-tutorial.md).

Tähän lähestymistapaan liittyy muutamia rajoituksia. Koska osa ER:stä on toteutettu C#-koodilla, kaikki tiedot eivät ole käytettävissä. Voit kuitenkin tarkastella tietojen käyttötietoja. Lisäksi pitkät raporttien ajot voivat ylittää jäljityksen tallennusrajoitukset.

#### <a name="er-traces"></a><a name="electronic-reporting-traces"></a>ER-jäljitys

ER voi kerätä omat jäljityksensä, ja sillä on visuaalisia ja analyysityökaluja kyseisiä jäljityksiä varten. Lisätietoja: [Sähköisen raportoinnin muotojen suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).

#### <a name="perfview"></a><a name="perfview"></a>PerfView

Koska sekä X++ että ER on toteutettu .NET-alustalla, voit käyttää yleisiä .NET-työkaluja. Voit käyttää esimerkiksi maksutonta [PerfView](https://github.com/Microsoft/perfview)-työkalua.

Voit myös kerätä tietoja komentoriviltä. Esimerkiksi seuraava Windows PowerShell -komentosarja kerää suoritusajan, kunnes kaikki kaavan suoritukset pysäytetään koneessa.

```powershell
c:\programs\PerfView collect "e:\traces\$(date -format "ddMMyyyy_hhmm").etl" `
    -CircularMB:20000 -ThreadTime `
    -NoNGenRundown `
    -StopOnEtwEvent:Microsoft-Dynamics-ElectronicReporting/FormatMappingRun/Stop
```

Tähän lähestymistapaan liittyy muutamia rajoituksia. Sinulla on oltava järjestelmänvalvojan käyttöoikeus koneeseen. Lisäksi sinun on oltava kokenut kehittäjä, koska oppimiseen kuluu pitkä aika.

### <a name="making-changes"></a><a name="making-changes"></a>Muutosten tekeminen

#### <a name="use-caching"></a><a name="use-caching"></a>Käytä välimuistiin tallentamista

Vaikka välimuistiin tallentaminen vähentää tietojen hakemiseen tarvittavaa aikaa, se kuluttaa muistia. Käytä välimuistiin tallentamista, kun haettavat tiedot eivät ole hyvin suuria. Lisätietoja ja esimerkki siitä, miten välimuistiin tallentamista käytetään, on kohdassa [Mallin määrityksen parantaminen suoritusjäljityksen tietojen perusteella](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace).

#### <a name="reduce-volume-of-data-fetched"></a><a name="reduce-fetched-data"></a>Haettujen tietojen määrän pienentäminen

Voit pienentää välimuistin muistin kulutusta rajoittamalla suorituksen aikana haettavan sovellustaulun tietueiden kenttien määrää. Tässä tapauksessa voit noutaa vain ne sovellustaulun kenttäarvot, joita tarvitset ER-mallimäärityksessä. Muita taulun kenttiä ei noudeta. Siksi välimuistiin haetuissa tietueissa tarvittava muistin määrä pienenee. Lisätietoja: [ER-ratkaisujen suorituskyvyn parantaminen vähentämällä ajon aikana haettujen taulukenttien määrää](er-reduce-fetched-fields-number.md).

#### <a name="use-a-cached-parameterized-calculated-field"></a><a name="cached-parameterized"></a>Käytä välimuistiin tallennettua parametrisoitua laskettua kenttää

Joskus arvot on etsittävä toistuvasti. Esimerkkejä tällaisista ovat tilien nimet ja tilinumerot. Voit säästää aikaa luomalla lasketun kentän, jonka parametrit ovat ylimmällä tasolla, ja lisätä sitten kentän välimuistiin.

Tätä menetelmää kannattaa käyttää vain, jos välimuistiin tallennettujen tietojen koko on pieni. Lisätietoja on kohdassa [ER-ratkaisujen suorituskyvyn parantamiseen lisäämällä parametrisoituja laskettujen kenttien tietolähteitä](er-calculated-field-ds-performance.md).

#### <a name="use-a-join-data-source"></a><a name="use-join-datasource"></a>Käytä JOIN-tietolähdettä

**JOIN**-tietolähde mahdollistaa usean yhdistetyn tietueen hakemisen yhdellä kyselyllä. Kutakin liitettyä tietuetta ei tarvitse hakea erillisellä kyselyllä. Jos sinulla on esimerkiksi 1 000 riviä ja haet kunkin rivin nimiketiedot suhteen mukaan, kyselyjä on 1 001 (= 1 000 + 1). Jos käytät **JOIN**-tietolähdettä, samat tiedot voi hakea vain yhden kyselyn avulla. Lisätietoja: [Käytä sähköisen raportoinnin (ER) mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista](er-join-data-sources.md).

#### <a name="use-the-filter-function-instead-of-the-where-function"></a><a name="filter"></a>Käytä FILTER-toimintoa WHERE-toiminnon asemesta

**[FILTER](er-functions-list-filter.md)**-toiminto suorittaa ehdot SQL Serverissä, kun taas **WHERE**-toiminto noutaa kaikki tiedot luettelosta yksi tietue kerrallaan ja soveltaa ehtoa kuhunkin tietueeseen. Haluat esimerkiksi valita yhden tietueen 1 000 tietueesta. Jos käytät **WHERE**-toimintoa, kaikki 1 000 tietuetta haetaan. Jos kuitenkin käytät **FILTER**-toimintoa, noudetaan täsmälleen yksi tietue. **FILTER** voi käyttää myös tietokantapuolen indeksejä.

#### <a name="using-collected-data-functions-or-an-accumulated-data-data-source"></a><a name="collected-data"></a>Kerättyjen tietotoimintojen tai kumulatiivisen datatietolähteen käyttäminen

Jos konfiguraatiossa on *GROUP BY* -komponentti, joka sisältää aiemmin haettujen tietojen yhteenvedon raportissa, komponentti noutaa kaikki tiedot uudelleen. Käyttämällä kerättyjä datafunktioita ER:n avulla voit koota tietoja ensimmäisen noutamisen yhteydessä. Lisä tietoja on kohdassa [ER – Määritä muoto suorittamaan laskenta ja summaus](tasks/er-format-counting-summing-2.md).

#### <a name="rewrite-parts-of-the-configuration-in-x"></a>Korvaa osia konfiguraatiosta X++-koodissa

ER tukee taulujen ja luokkien sekä laajennusten kutsumenetelmiä. Harkitse mallimäärityksen osien uudelleen kirjoittamista X++-koodissa suorituskyvyn parantamiseksi.

ER voi kuluttaa seuraavien lähteiden tietoja:

- Luokat (**objekti**- ja **luokka**-tietolähteet)
- Taulut (**taulu**- ja **taulutietue**-tietolähteet)

[ER-sovellusliittymän (API)](er-apis-app73.md#how-to-access-internal-x-objects-by-using-erobjectsfactory) avulla voi myös lähettää esilasketut tiedot kutsuvasta koodista. Sovellusohjelma sisältää useita esimerkkejä tästä lähestymistavasta.
