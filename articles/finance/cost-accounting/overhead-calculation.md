---
title: Yleiskustannuslaskenta
description: Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 60bce611ae1f6ed5d63860793cd5d1da3c421a9e
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551801"
---
# <a name="overhead-calculation"></a>Yleiskustannuslaskenta

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan tyypillinen yleiskustannusten laskenta- ja kohdistusprosessi.

## <a name="term-definition"></a>Sanaston määritelmä

Yleiskustannukset ovat yrityksen toiminnasta syntyviä kustannuksia, joita ei voi suoraan liittää mihinkään tiettyyn liiketoiminnan tehtävään, tuotteeseen tai palveluun. Yleiskustannukset ovat tärkeä tuki voittoa tuottavien tehtävien luonnissa. Seuraavassa on joitakin esimerkkejä yleiskustannuksista:

-   Vuokra
-   Sähkö
-   Hallinnon palkat

## <a name="overhead-calculation-overview"></a>Yleiskustannuslaskennan yleiskuva
Yleiskustannusten laskenta suorittaa kustannuslaskennan käytännöt oikeassa järjestyksessä. Yleiskustannusten laskennan voi suorittaa useita kertoja samalle tilikaudelle, jos kustannuslaskennan käytännöt ovat muuttuneet tai erityisiä virheitä on havaittu. Kukin laskenta-ajo tallennetaan ja kullekin annetaan yksilöllinen versiotunnus, jonka avulla eri laskenta-ajoja voi verrata toisiinsa. Yleiskustannusten laskenta luo kustannustapahtumia, joille annetaan kirjauspäivä. Kirjauspäivä vastaa laskennassa käytettyä tilikauden päättymispäivämäärää. Yksilöivä versiotunnus sisältää seuraavat tiedot:

-   Versiotyyppi
-   Päivämäärä ja aika
-   Kustannuslaskennan kirjanpito
-   Tilikausi 
-   Tilikausi  

Yleiskustannusten laskenta ajetaan versiosta riippumattomana. Voit siis laskea budjetin version ennen todellista versiota. Yleiskustannusten laskenta koostuu neljästä vaiheesta, jotka esitellään seuraavassa kuvassa. Kussakin vaiheessa luodaan kirjauskansion otsikko, jolla on kirjauskansiovientejä. Tämä kirjauskansion otsikko säilyttää kunkin laskentavaiheen syöttötiedot. Käytännöt ja säännöt ajetaan kullekin kirjauskansion riville, ja tuloksena luodaan kustannustapahtumia. Tämän ansiosta kaikki laskutoimitukset ovat täysin jäljitettävissä. 

[![Yleiskustannuslaskenta.](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a>Laske ja kohdista sähkön yleiskustannukset
Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi. Tarkka johdon näkymä ei täten ole saatavilla kustannuslaskennassa. Jotta kustannuslaskenta tarjoaisi oikean johdon näkymän kaikista organisaation yksiköistä ja tasoista, kustannusten on virrattava organisaation yksiköiden läpi. Tämän virran on perustuttava joko tarkkaan tietoon kulutuksesta tai perusteltuun arvioon. Sähkökustannukset voi kirjata kirjanpitoon seuraavassa taulukossa kuvatulla tavalla.

<table>
<thead>
<tr>
<th>Kirjauspäivä</th>
<th colspan="2">Kustannuspaikka</th>
<th colspan="2">Päätili</th>
<th>Summa kirjanpitovaluuttana</th>
</tr>
</thead>
<tbody>
<tr>
<td>3.1.2017</td>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a>Vaihe 1: Käsittele kustannustoiminnan laskenta

Kun kustannustapahtumat tuodaan lähdetiedoista, niille asetetaan kustannuslaskennassa oletusarvoisesti **Luokittelematon** -kustannustoimintaluokka. Voit luokitella kustannustapahtumia uudelleen **kiinteäksi kustannukseksi** tai **muuttuvaksi kustannukseksi** kustannustoiminnan käytäntösäännöillä.

#### <a name="define-the-cost-behavior-rule"></a>Määritä kustannustoiminnan sääntö

Joissain tapauksissa osa kustannuksesta on kiinteä ja loppuosa perustuu kulutukseen. Sähkölaskut sopivat usein tähän määritelmään. Maksat ensin määrätyn, kiinteän maksun, jonka lisäksi maksat kulutuksesta kilowattitunteina (kWh). Jos kiinteä maksu on esimerkiksi 1 000,00, kustannustoiminnan sääntö määritetään seuraavasti:

-   Kiinteä määrä 1 000,00
    -   0 &lt;= 1 000,00 = Kiinteä
    -   1000,01 &lt; N = Muuttuva

##### <a name="journal"></a>Kirjauskansio

<table>
<thead>
<tr>
<th>Kirjauskansio</th>
<th>Kirjauskansion tyyppi</th>
<th colspan="3">Kirjanpidon vuosikalenterin kausi</th>
<th>Versio</th>
</tr>
</thead>
<tbody>
<tr>
<td>00001</td>
<td>Kustannustoiminnan laskentakirjauskansio</td>
<td>Tilivuosi</td>
<td>2017</td>
<td>Kausi 1</td>
<td>Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)

<table>
<thead>
<tr>
<th>Kirjauspäivä</th>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>3.1.2017</td>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Luokittelematon</td>
<td>10 000,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kustannusmerkinnät

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
<th>Kirjauspäivä</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Luokittelematon</td>
<td>10 000,00</td>
<td>3.1.2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Luokittelematon</td>
<td>-10 000,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>1 000,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>9,000.00</td>
<td>31.1.2017</td>
</tr>
</tbody>
</table>

Lisätietoja on kohdassa [Kustannustoimintakäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).
### <a name="step-2-process-the-cost-distribution-calculation"></a>Vaihe 2: Käsittele kustannusten jaon laskenta

Kustannusten jakoa käytetään kustannusten jakamiseen yhdestä kustannusobjektista toiseen (tai useampaan kustannusobjektiin) määrittämällä asiaankuuluvan kohdistusperusteen. Kustannusten jako ja kustannusten kohdistus eroavat toisistaan sillä, että kustannusten jako tapahtuu aina alkuperäisen kustannuksen ensisijaisen kustannuselementin tasolla.

#### <a name="define-the-cost-distribution-rule"></a>Määritä kustannusten jaon sääntö

Tietyt kustannukset, kuten sähkö, rekisteröidään kirjanpidossa kokonaissummaksi. Kustannuslaskenta ei tarjoa tästä tarpeeksi tarkkoja tietoja. Muuttuva kustannus tulisi jakaa yksittäisille kustannusobjekteille reiluin perustein. Loogisin kohdistusperuste on sähkönkulutus (kWh). Luodaan tilastollinen dimensionjäsen nimeltä Sähkö, johon kirjataan sähkönkulutus. Oletusarvon mukaan kaikki tilastolliset dimensiojäsenet ovat käytettävissä kohdistusperusteina.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>kWh</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>1 000</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>6,000</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>0</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa on esitetty tulos, kun sähkönkulutusta käytetään kohdistusperusteena muuttuville kuluille.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>1 000</td>
<td>(1 000 ÷ 7 000) × 9 000,00</td>
<td>1,285.71</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>6,000</td>
<td>(6 000 ÷ 7 000) × 9 000,00</td>
<td>7,714.29</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>0</td>
<td>(0 ÷ 7 000) × 9 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

Kiinteä kustannus tulisi jakaa tasaisesti yksittäisille kustannusobjekteille, jotka ovat kuluttaneet sähköä. Voit käyttää sähkön tilastollista dimensiojäsentä kaavan kohdistusperusteena tämän tavoitteen saavuttamiseksi: (sähkö &gt;0,00) Seuraavassa taulukossa on esitetty tulos siitä, kun sähkönkulutus on määritetty muuttuvien kustannusten kohdistusperusteeksi.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Resepti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>(1 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>(6 000 &gt; 0,00)</td>
<td>1</td>
<td>(1 ÷ 2) × 1 000,00</td>
<td>500,00</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>(0 &gt; 0,00)</td>
<td>0</td>
<td>(0 ÷ 2) × 1 000,00</td>
<td>0,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Kirjauskansio

<table>
<thead>
<tr>
<th>Kirjauskansio</th>
<th>Kirjauskansion tyyppi</th>
<th colspan="3">Kirjanpidon vuosikalenterin kausi</th>
<th>Versio</th>
</tr>
</thead>
<tbody>
<tr>
<td>00002</td>
<td>Kustannusten jaon laskentakirjauskansio</td>
<td>Tilivuosi</td>
<td>2017</td>
<td>Kausi 1</td>
<td>Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kirjauskansioviennit (Kustannusobjektin saldon kirjauskansioviennit)

<table>
<thead>
<tr>
<th>Kirjauspäivä</th>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>31.1.2017</td>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>1 000,00</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>9,000.00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kustannusmerkinnät

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
<th>Kirjauspäivä</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>-1 000,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>500,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>500,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC099</td>
<td>Oletuskustannuspaikka</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-9 000,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>1,285.71</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>7,714.29</td>
<td>31.1.2017</td>
</tr>
</tbody>
</table>

Lisätietoja on kohdassa [Jakelukäytännön luominen ja määrittäminen kustannusten hallinnan yksikköön](tasks/create-assign-cost-distribution-policy-cost-control-unit.md). 

### <a name="step-3-process-the-overhead-rate-calculation"></a>Vaihe 3: Käsittele yleiskustannustason laskenta

Yleiskustannustasolla veloitetaan yksi tai useampi määrätty kustannusobjekti. Veloitus perustuu ennalta määrättyyn kustannustasoon sekä määritetyn kohdistusperusteen suuruuteen. 

#### <a name="define-the-overhead-rate"></a>Määritä yleiskustannustaso.

Kustannusobjekti CC001 HR vaikuttaa joukkoon sisäisiä projekteja. Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon projektit.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Tunnit</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekti 1</td>
<td>3</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekti 2</td>
<td>1</td>
</tr>
</tbody>
</table>

Kustannusprojektien osuudelle on määritetty ennalta kustannushinta.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Yksiköt</th>
<th>Osuus</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Muuttuva kulu</td>
<td>1</td>
<td>10</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa on esitetty tulos, kun Henkilöstöhallinnon projekteja käytetään kohdistusperusteena.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kustannustaso</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>Proj 1</td>
<td>Projekti 1</td>
<td>3</td>
<td>10 001</td>
<td>(3 ÷ 1) × 10,00</td>
<td>30,00</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Projekti 2</td>
<td>1</td>
<td>10 001</td>
<td>(1 ÷ 1) × 10,00</td>
<td>10,00</td>
</tr>
</tbody>
</table>

##### <a name="journal"></a>Kirjauskansio

<table>
<thead>
<tr>
<th>Kirjauskansio</th>
<th>Kirjauskansion tyyppi</th>
<th colspan="3">Kirjanpidon vuosikalenterin kausi</th>
<th>Versio</th>
</tr>
</thead>
<tbody>
<tr>
<td>00003</td>
<td>Yleiskustannustason laskelman kirjauskansio</td>
<td>Tilivuosi</td>
<td>2017</td>
<td>Kausi 1</td>
<td>Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a>Kirjauskansioviennit (Yleiskustannustason laskennan kirjauskansioviennit)

<table>
<thead>
<tr>
<th>Kirjauspäivä</th>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
</tr>
</thead>
<tbody>
<tr>
<td>31.1.2017</td>
<td>Proj 1</td>
<td>Sisäinen proj 1</td>
<td>3,00</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>Proj 2</td>
<td>Sisäinen proj 2</td>
<td>1,00</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kustannusmerkinnät

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
<th>Kirjauspäivä</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC0001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-30,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Proj 1</td>
<td>Sisäinen proj 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>30,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-10,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Proj 2</td>
<td>Sisäinen proj 2</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>10.00</td>
<td>31.1.2017</td>
</tr>
</tbody>
</table>

Lisätietoja on kohdassa [Yleisen laskennan suorittaminen](cost-rollup.md#perform-overhead-calculation).

### <a name="step-4-process-the-cost-allocation-calculation"></a>Vaihe 4: Käsittele kustannusten kohdistuksen laskenta

Kohdistuksella kustannusobjektin saldo liitetään toisiin kustannusobjekteihin käyttämällä kohdistusperustetta. Finance tukee vastavuoroista kohdistusmenetelmää. Vastavuoroisessa kohdistusmenetelmässä tunnistetaan oheiskustannusobjektien käyttämät, keskinäiset palvelut täysin. Järjestelmä määrittää oikean kohdistusjärjestyksen automaattisesti. Kustannusobjektin saldo kohdistetaan yhdellä kohdistusperusteella. Kustannusobjektien dimensiot ja niiden vastaavat jäsenet ylittävät kohdistukset ovat tuettuja. Kustannusseurantayksikkö hallitsee kohdistusjärjestystä. 

[![Vastavuoroinen menetelmä.](./media/reciprocal-method.png)](./media/reciprocal-method.png)

#### <a name="define-the-cost-allocation"></a>Määritä kustannuksen kohdistus

Tämä on yksinkertainen esimerkki, jossa kerrotaan, miten voit jäljittää kustannuksen virran. Kustannusobjekti CC001 HR liittyy useaan kustannusobjektiin. Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Henkilöstöhallinnon palvelut.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>HR-palvelut</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>35</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>55</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10</td>
</tr>
</tbody>
</table>

Kustannusobjekti CC002 Taloushallinto liittyy useaan kustannusobjektiin. Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Taloushallinnon palvelut.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Taloushallinnon palvelut</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>65</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>35</td>
</tr>
</tbody>
</table>

Kustannusobjekti CC003 Kokoonpano liittyy useaan kustannusobjektiin. Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Kokoonpanopalvelut.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Kokoonpanopalvelut (tuntia)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>60</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>20</td>
</tr>
</tbody>
</table>

Kustannusobjekti CC004 Pakkaus liittyy useaan kustannusobjektiin. Kulutetun suuruuden mittaamiseen luodaan tilastollinen dimensiojäsen nimeltä Pakkauspalvelut.

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Pakkauspalvelut (tuntia)</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>80</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>15</td>
</tr>
</tbody>
</table>

> [!NOTE]
> Tilastomittaukset, kuten tämän tuotteen kuluttamat tuotantotunnit, voidaan johtaa lähdetiedoista. Lisätietoja on kohdassa [Tilastomittauksen lähdemalli](statistical-measure-provider-template.md#statistical-measure-provider-template). Seuraavassa taulukossa näytetään tulos, kun henkilöstöhallinnon palveluja käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
<th>Kustannustoiminta</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>35</td>
<td>(35 ÷ 100) × 500,00</td>
<td>175.00</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>55</td>
<td>(55 ÷ 100) × 500,00</td>
<td>275.00</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10</td>
<td>(10 ÷ 100) × 500,00</td>
<td>50,00</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>35</td>
<td>(35 ÷ 100) × 1 245,71</td>
<td>436.00</td>
<td>Muuttuva kulu</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>55</td>
<td>(55 ÷ 100) × 1 245,71</td>
<td>685.14</td>
<td>Muuttuva kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10</td>
<td>(10 ÷ 100) × 1 245,71</td>
<td>124.57</td>
<td>Muuttuva kulu</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa näytetään tulos, kun Taloushallinnon palveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
<th>Kustannustoiminta</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>65</td>
<td>(65 ÷ 100) × (500,00 + 175,00)</td>
<td>438.75</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>35</td>
<td>(35 ÷ 100) × (500,00 + 175,00)</td>
<td>236.25</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>65</td>
<td>(65 ÷ 100) × (7 714,29 + 436,00)</td>
<td>5,297.69</td>
<td>Muuttuva kulu</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>35</td>
<td>(35 ÷ 100) × (7 714,29 + 436,00)</td>
<td>2,852.60</td>
<td>Muuttuva kulu</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa näytetään tulos, kun Kokoonpanopalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
<th>Kustannustoiminta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>60</td>
<td>(60 ÷ 80) × (275,00 + 438,75)</td>
<td>535.31</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>20</td>
<td>(20 ÷ 80) × (275,00 + 438,75)</td>
<td>178.44</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>60</td>
<td>(60 ÷ 80) × (5 297,69 + 685,14)</td>
<td>4,487.12</td>
<td>Muuttuva kulu</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>20</td>
<td>(20 ÷ 80) × (5 297,69 + 685,14)</td>
<td>1,495.71</td>
<td>Muuttuva kulu</td>
</tr>
</tbody>
</table>

Seuraavassa taulukossa näytetään tulos, kun Pakkauspalveluita käytetään kohdistusperusteena kokonaiskustannukselle (kiinteät ja muuttuvat kustannukset).

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th>Suuruus</th>
<th>Kohdistuskerroin</th>
<th>Summa</th>
<th>Kustannustoiminta</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>80</td>
<td>(80 ÷ 95) × (50,00 + 236,25)</td>
<td>241.05</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>15</td>
<td>(15 ÷ 95) × (50,00 + 236,25)</td>
<td>45.20</td>
<td>Kiinteä kustannus</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>80</td>
<td>(80 ÷ 95) × (2 852,60 + 124,57)</td>
<td>2,507.09</td>
<td>Muuttuva kulu</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>15</td>
<td>(15 ÷ 95) × (2 852,60 + 124,57)</td>
<td>470.08</td>
<td>Muuttuva kulu</td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a>Kirjauskansioviennit (kustannusobjektin saldon kirjauskansioviennit)

<table>
<thead>
<tr>
<th>Kirjauskansio</th>
<th>Kirjauskansion tyyppi</th>
<th colspan="3">Kirjanpidon vuosikalenterin kausi</th>
<th>Versio</th>
</tr>
</thead>
<tbody>
<tr>
<td>00004</td>
<td>Kustannusten kohdistuskirjauskansio</td>
<td>Tilivuosi</td>
<td>2017</td>
<td>Kausi 1</td>
<td>Yleiskustannusten laskenta / 01-02-2017 23:51:00 / Kirjanpito /2017 / Kausi 1</td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a>Kirjauskansion rivit

<table>
<thead>
<tr>
<th>Kirjauspäivä</th>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
</tr>
</thead>
<tbody>
<tr>
<td>31.1.2017</td>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>500,00</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>1,245.71</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>675.00</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>8,150.29</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>713.75</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>5,982.83</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC003</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>286.25</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>CC003</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>2,977.17</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>776.36</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>6,994.21</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>Tuote 2</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>223.64</td>
</tr>
<tr>
<td>31.1.2017</td>
<td>Tuote 2</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>1,965.79</td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a>Kustannusmerkinnät

<table>
<thead>
<tr>
<th colspan="2">Kustannusobjekti</th>
<th colspan="2">Kustannustaso</th>
<th>Kustannustoiminta</th>
<th>Summa</th>
<th>Kirjauspäivä</th>
</tr>
</thead>
<tbody>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>-500,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>175.00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>275.00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>50,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC001</td>
<td>Henkilöstöhallinto</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-1 245,71</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>436.00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>685.14</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>124.57</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>-675,00</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>438.75</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>236.25</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC002</td>
<td>Myyntitiedot</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-8 150,29</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>5,297.69</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC004</td>
<td>Pakkaus</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>2,852.60</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>-713,75</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>535.31</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>178.44</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-5 982,83</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>4,487.12</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>1,495.71</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>-286,25</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>241.05</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Kiinteä kustannus</td>
<td>45.20</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>CC003</td>
<td>Kokoonpano</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>-2 977,17</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 1</td>
<td>Tuote 1</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>2,507.09</td>
<td>31.1.2017</td>
</tr>
<tr>
<td>Tuote 2</td>
<td>Tuote 2</td>
<td>10 001</td>
<td>Sähkö</td>
<td>Muuttuva kulu</td>
<td>470.08</td>
<td>31.1.2017</td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a>Johtopäätökset
Kirjanpidossa kirjataan tyhjään kustannuspaikkatunnukseen sähkökustannus arvolla 10 000,00. Tämän ansiosta kustannuslaskijat tietävät, että kustannus on kohdistettava. Kustannukset virtaavat kirjanpidossa organisaation yksiköiden ja tasojen läpi käytössä olevien käytäntöjen ja sääntöjen mukaisesti. Kukin kustannus on liitetty kustannusperusteeseen, joka sisältää parhaan arvion kustannusten kohdistuksesta.

Kustannustaso | Kustannusobjekti<br>CC099 | Kustannusobjekti<br>CC001 | Kustannusobjekti<br>CC002 | Kustannusobjekti<br>CC003 | Kustannusobjekti<br>CC004 | Kustannusobjekti<br>Proj 1 | Kustannusobjekti<br>Proj 2 | Kustannusobjekti<br>Tuote 1 | Kustannusobjekti<br>Tuote 2 | Yhteensä
---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:
10001 Sähkö | 0,00 | 0,00 | 0,00 | 0,00 |  | 30.00 | 10.00 | 7,770.57 | 2,189.43 | 10,000.00 |
Luokittelematon | 0,00 |  |  |  |  |  |  |  |  |  |
Kiinteä kustannus | 0,00 | 0,00 | 0,00 | 0,00 | 0,00 |  |  | 776.36 | 223.64 | 1,000.00 |
Muuttuva kulu | 000 | 0,00 | 0,00 | 0,00 | 0,00 | 30,00 | 10,00 | 6,994.21 | 1,965.79 | 9,000.00 |

> [!NOTE]
> Tässä ohjeaiheessa esitellään, miten ensisijainen kustannuselementti, 10001 Sähkö, virtaa kustannusobjektien läpi. Tästä syystä tämä yleiskustannus kohdistetaan organisaation alimmalle tasolle. Toisin sanoen alimman tason kustannusobjektit kantavat kustannuksen. Jos tarvitset visuaalisen näkymän kustannuksen virrasta kustannusobjektien välillä, voit käyttää kustannuksen koontikäytäntösääntöjä kustannusvirran visualisointiin. Lisätietoja on kohdassa [Kustannusten koontikäytäntö ja yleiskustannuslaskenta](cost-rollup.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
