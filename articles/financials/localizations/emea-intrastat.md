---
title: Intrastat
description: "Tämä artikkeli sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa. Artikkeli sisältää raportointiprosessin yleiskatsauksen ja kertoo pakolliset asetukset ja edellytykset."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2ee60f3d1155b89d342b94832fbdbe898a5063c6
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---

# <a name="intrastat"></a>Intrastat

[!include [banner](../includes/banner.md)]

Tämä artikkeli sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa. Artikkeli sisältää raportointiprosessin yleiskatsauksen ja kertoo pakolliset asetukset ja edellytykset.

Intrastat on järjestelmä, jolla kerätään tietoja ja muodostetaan tilastoja Euroopan unionin (EU) jäsenvaltioiden ja alueiden välisestä kaupasta. Intrastat-raportointi on pakollista aina, kun tuote ylittää EU-maan tai -alueen rajan. Monissa maissa ja monilla alueilla Intrastat-raportointi koskee myös palveluja. Intrastat-raporteissa voidaan kerätä pakollisia ja valinnaisia elementtejä. Seuraavat elementit ovat pakollisia: tietojen ilmoittamisesta vastuussa olevan osapuolen arvonlisäveronumero (ALV-numero), viitekausi, suunta (saapuva vai lähtevä), 8-numeroinen tavarankoodi, kumppanin jäsenvaltio (lähettäjäjäsenvaltio saapuvissa ja määräjäsenvaltio lähetyksissä), tavaroiden arvo, tavaroiden määrä (nettopaino ja lisäyksikkö) ja tapahtuman luonne. Maat ja alueet voivat myös kerätä erilaisten ehtojen mukaisesti valinnaisia elementtejä. Valinnaisia elementtejä ovat esimerkiksi alkuperämaa tai -alue, toimitusehdot, kuljetustapa, yksityiskohtaisempi tavaran koodi kuin CN8, alkuperäalue lähetyksissä ja määräalue saapuvissa, tilastomenettely, tilastoarvo, tavaroiden kuvaus sekä kuormauksen tai kuorman purkamisen satama tai lentoasema.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat-raportointiprosessin yhteenveto
Seuraavissa osissa kuvataan Intrastat-raportoinnissa käytettävää yleistä tiedonkulkua.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Anna toisen EU-maan tai -alueen rajan ylittävä tapahtuma

Myyntilasku, vapaatekstilasku, ostolasku, projektilaskun, asiakkaan pakkausluettelo, toimittajan tuotteen vastaanotto tai siirtotilaus siirretään Intrastat-kirjauskansioon vain, jos määrämaan tai -alueen tyyppi (lähtevissä) tai lähettäjätyyppi (saapuvissa) on **EU**. Tämän toiminto laajennettiin Microsoft Dynamics 365 for Operationsiin (1611), ja sen avulla voit määrittää rahtiosoitteita EU:n sisäisille tapahtumille. Jos rahtiosoite on eri kuin toimittajan osoite (tai asiakkaan osoite palautustilauksen osalta), Intrastat-raportointi toimii näillä tiedoilla. Kun luot myyntitilauksen, vapaatekstilaskun, ostotilauksen, toimittajan laskun, projektilaskun tai siirtotilauksen, joissakin ulkomaankauppaan liittyvissä kentissä on oletusarvot asiakirjan otsikossa tai rivillä. Tapahtuman oletuskoodi otetaan vastaavasta kentästä **Ulkomaankaupan parametrit**-sivulla. Tavaran oletuskoodi, alkuperämaa tai -alue sekä alkuperäosavaltio tai -provinssi otetaan nimikkeestä. Voit muuttaa oletusarvoja ja lisätä muut ulkomaankauppaan liittyvät tiedot: tilastomenettelyn, kuljetustavan ja sataman.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Voit luoda tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla.

Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta luodaan kuukausittain. Voit siirtää tapahtumat vapaatekstilaskusta, myyntilaskusta, asiakkaan pakkausluettelosta, toimittajan laskusta, toimittajan pakkausluettelosta, projektilaskusta tai siirtotilauksesta **Ulkomaankaupan parametrit** -sivulla määritettyjen ehtojen mukaisesti. Voit antaa tapahtumat myös manuaalisesti. Voit päivittää manuaalisesti siirretyt tapahtumat Intrastat-kirjauskansiossa, jos päivitys on tarpeellinen. Voit tiivistää Intrastat-kirjauskansion tapahtumat **Intrastatin tiivistys** -sivulla määritettyjen erityisehtojen mukaisesti. Joissakin maissa ja joillakin alueilla voi käyttää pienen tapahtuman rajaa. Voit sitten raportoida kyseisen rajan alle jäävät tapahtumat erityisellä tavaran koodilla. Voit päivittää tavaran koodin vastaavilla Intrastat-kirjauskansion riveillä **Ulkomaankaupan parametrit** -sivun **Vähimmäisraja**-asetuksen mukaisesti. Voit myös tiivistää kyseiset tapahtumat **Intrastatin tiivistys** -asetuksen mukaisesti. Voit tarkistaa Intrastat-kirjauskansion tapahtumien valmiusasteen **Ulkomaankaupan parametrit** -sivun **Tarkista asetukset** -asetuksen perusteella. Vastaavien kenttien tietojen valmiusaste voidaan tarkistaa: maa tai alue, osavaltio tai provinssi, paino, tavaran koodi, tapahtumakoodi, lisäyksikkö, satama, alkuperä, toimitusehdot, kuljetustapa ja ALV-tunnus. Tapahtumat, jotka eivät ole valmiita, saavat merkinnän ei kelpaa.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Voit raportoida tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla.

Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta raportoidaan kuukausittain. Voit tulostaa Intrastat-raportin **Ulkomaankaupan parametrit** -sivun **Raporttimuodon yhdistäminen** -asetusten mukaisesti. Voit myös luoda sähköisen tiedoston **Ulkomaankaupan parametrit** -sivun **Tiedostomuodon yhdistäminen** -asetusten mukaisesti. Lisätietoja Intrastat-raportoinnista, kuten edellytyksistä, on Intrastat-raportoinnin tehtävätallenteissa:

-   EU Intrastat -ilmoituksen luominen
-   Siirrä tapahtumat Intrastatiin
-   Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulussa luetellaan Intrastat-raportoinnin edellytykset.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Osoitemääritys</td>
<td>Määritä maiden ja alueiden ISO (International Organization for Standardization) -koodit.</td>
</tr>
<tr class="even">
<td>Oikeushenkilö</td>
<td>Määritä tuonnin ja viennin ALV-tunnukset, sivuliikkeen alanumeron tuonti ja vienti sekä yritykselle määritetty Intrastat-koodi.</td>
</tr>
<tr class="odd">
<td>Tuoteluokkahierarkia (myyntihierarkia, hankintahierarkia)</td>
<td>Määritä luokkasolmujen Intrastat-kauppatavarakoodit <strong>Luokkahierarkia</strong>-sivun <strong>Kauppatavarakoodit</strong>-välilehdessä. Kun määrität kauppatavarakoodin pääluokkasolmulle, koodia käytetään kaikissa aliluokkasolmuissa. Valittuja kauppatavarakoodeja voi käyttää <strong>Valittu</strong>-näkymässä, kun valitset kauppatavarakoodin vapautetun tuotteen tiedoissa sekä myynti-, osto- ja siirtotilausriveillä.</td>
</tr>
<tr class="even">
<td>Vapautetun tuotteen tiedot</td>
<td>Määritä seuraavat vapautettujen tuotteiden ulkomaankaupan tiedot:
<ul>
<li><strong>Kauppatavarakoodi</strong> – valitse joko määritetyistä tuoteluokista haettu valittujen kauppatavaroiden luettelo tai täydellinen Intrastat-kauppatavarakoodien luettelo.</li>
<li><strong>Tilastollinen maksuprosentti</strong></li>
<li><strong>Alkuperämaa tai -alue</strong> – valitse oletusmaa tai -alue, josta tavarat kokonaisuudessaan hankittiin tai jossa ne valmistettiin.</li>
<li><strong>Alkuperäosavaltio tai -provinssi tai määräosavaltio tai -provinssi</strong> – saapuvien oletusarvoinen määräosavaltio tai -provinssi ja lähtevien alkuperäosavaltio tai -provinssi.</li>
<li><strong>Nettopaino kilogrammoina</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Asiakkaat</td>
<td>Määritä asiakkaan EU-maassa tai -alueella oleva toimitusosoite.</td>
</tr>
<tr class="even">
<td>Toimittajat</td>
<td>Määritä toimittajan EU-maassa tai -alueella oleva toimitusosoite.</td>
</tr>
<tr class="odd">
<td>Muut kulut</td>
<td>Määritä laskusummaan, tilastosumman tai molempiin sisällytettävä muiden kulujen koodi. Määritä <strong>Kulukoodit</strong>-sivun <strong>Ulkomaankauppa</strong>-välilehdessä <strong>Intrastat-laskun arvo</strong> sisällyttämään kulujen summa laskun arvoon. Määritä myös <strong>Tilastollinen Intrastat-arvo</strong> sisällyttämään kulujen summa tilastoarvoon.</td>
</tr>
<tr class="even">
<td>Sähköinen raportointi</td>
<td>Määritä sähköisen raportoinnin määritykset viemään Intrastat-tiedot sähköisenä tiedostona viranomaisten pyytämässä muodossa ja luomaan esikatselu käyttäjälle soveltuvassa luettavassa muodossa (kuten Microsoft Excelissä).</td>
</tr>
<tr class="even">
<td>Varastointi</td>
<td>Liitä toimittajatilit varastokoodeihin verovapausnumeron täyttämiseksi siirtotilausta siirrettäessä.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Määritys
Seuraavissa osissa käsitellään pakollisia Intrastat-raportoinnin asetuksia.

### <a name="set-up-all-required-intrastat-related-lists"></a>Kaikkien Intrastatiin liittyvien luetteloiden määrittäminen

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Luettelo</th>
<th>Lisätiedot</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kauppatavarakoodit</td>
<td>Määritä tyypin <strong>Kauppatavarakoodi</strong> luokkahierarkia ja anna kaikki kauppatavarakoodit yhdistetyn nimikkeistöluettelon mukaisesti. Määritä jokaiselle kauppatavaralle seuraavat tiedot:
<ul>
<li>Kauppatavaran nimi ja kauppatavarakoodi</li>
<li>Kutsumanimi ja/tai käännetty nimi</li>
<li><strong>Ulkomaankauppa</strong>-välilehden raportoinnin (lisä)yksiköiden asetukset. Voit valita lisäyksikön yksikköluettelosta. Voit myös määrittää, raportoidaanko kauppatavaroiden paino valitun lisäyksikön lisäksi.</li>
</ul></td>
</tr>
<tr class="even">
<td>Tapahtumakoodit</td>
<td>Määritä tapahtuman luonne maan tai alueen vaatimusten mukaisesti. Kullekin määritetylle tapahtumakoodille on määritettävä säännöt laskusummien sekä siirtotilausten ja myynti- ja ostotilausten tilastosummien laskemiseen.
<ul>
<li>Siirtotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:
<ul>
<li><strong>Tyhjä</strong> – määrä on 0 (nolla).</li>
<li><strong>Rahoituksellinen kustannus</strong> – summa on yhtä suuri kuin rahoituksellinen kustannus.</li>
<li><strong>Kokonaiskustannukset</strong> – summa on yhtä suuri kuin tapahtuman kokonaiskustannukset.</li>
<li><strong>Manuaalinen</strong> – summa on yhtä suuri kuin siirtotilausrivillä manuaalisesti määritetty summa.</li>
</ul></li>
<li>Myynti- ja ostotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:
<ul>
<li><strong>Tyhjä</strong> – määrä on 0 (nolla).</li>
<li><strong>Laskun summa</strong> – summa on yhtä suuri kuin kauppatavaran laskutettu summa.</li>
<li><strong>Veron peruste</strong> – summa on yhtä suuri kuin summa, joka laskutetaan ennen alennusten käyttöä.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Välitystavat</td>
<td>Määritä kuljetustapa maan tai alueen vaatimusten mukaisesti. Voit kullekin toimitustavalla oletuskuljetustavan <strong>Ulkomaankauppa</strong>-välilehdessä.</td>
</tr>
<tr class="even">
<td>Satamat</td>
<td>Määritä kuormauksen tai kuorman purkamisen satama tai lentoasema, jos kyseiset tiedot kerään maassa tai alueella.</td>
</tr>
<tr class="odd">
<td>Tilastomenettelyt</td>
<td>Määritä tilastomenettely, jos nämä tiedot kerätään maassa tai alueella.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Intrastat-tapahtumien tiivistämissääntöjen määrittäminen

Voit valita **Intrastatin tiivistys** -sivulla tiivistyksessä käytettävät kentät. Kaikki tapahtumat, joilla Intrastat-kirjauskansiossa valittujen kenttien kaltainen arvoyhdistelmä, tiivistetään yhdeksi tapahtumaksi, kun suoritat tiivistystoiminnon Intrastat-kirjauskansiossa.

### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

Määritä seuraavan taulun parametrit **Ulkomaankaupan parametrit** -sivulla.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Välilehti</th>
<th>Parametrit</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Yleinen</td>
<td><ul>
<li><strong>Yleinen</strong> – määritä seuraavat tiedot:
<ul>
<li>Myyntitilausten, ostotilausten, hyvityslaskujen ja siirtotilausten tapahtumakoodien oletusarvot. Hyvityslaskulle määritettyä tapahtumakoodia käytetään myös fyysisten tavaroiden palautuskoodina, ja sitä käytetään poikkeavin fyysisten palautusten ja oikaisuhyvityslaskujen vertailussa.</li>
<li>Intrastat-raporttien valmistelusta vastaava työntekijä.</li>
</ul></li>
<li><strong>Vähimmäisraja</strong> – määritä raja-arvon alittavien tapahtumien päivitysasetukset:
<ul>
<li>Raja-arvo ja paino</li>
<li>Raja-arvon alittavissa tapahtumissa käytettävä kauppatavarakoodi</li>
</ul></li>
<li><strong>Siirrä</strong> – Määritä ehdot, joilla tapahtumat siirretään Intrastat-kirjauskansioon. Voit määrittää, että tapahtumat siirretään vasta, kun nimikkeissä toteutuu yksi seuraavista ehdoista tai kaikki ehdot toteutuvat:
<ul>
<li>Nimikkeet eivät ole palvelunimikkeitä.</li>
<li>Nimillä on kauppatavarakoodi.</li>
<li>Nimikkeillä on paino.</li>
<li>Nimikkeillä on lisäyksiköitä.</li>
</ul></li>
<li><strong>Tarkista asetukset</strong> – Määritä Intrastat-tietojen valmiusasteen tarkistussäännöt. Voit valita, mitkä tiedot tarkistetaan.</li>
<li><strong>Pyöristyssäännöt</strong> – määritä seuraavat Intrastat-raportoinnin pyöristyssummien ja painojen asetukset:
<ul>
<li>Pyöristyssääntö (tarkkuus)</li>
<li>Pyöristystavoista: ylöspäin, alaspäin tai normaali</li>
<li>Summien ja painojen desimaalien määrä</li>
<li>Ohjeet alle 1 kilogramman (kg) painojen pyöristämiseen: ylöspäin 1 kg:hen, normaali tai ei pyöristystä</li>
</ul></li>
<li><strong>Sähköinen raportointi</strong> – määritä viittaukset sähköisen raportoinnin määrityksiin, jotta voit luoda sähköisen tiedoston ja raportin.</li>
<li><strong>Kauppatavarakoodihierarkia</strong> – määritä Intrastat-kauppatavarakoodia CN8 ilmaiseva <strong>Kauppatavarakoodi</strong>-tyypin luokkahierarkia.</li>
</ul></td>
</tr>
<tr class="even">
<td>Edustajan yhteystiedot</td>
<td>Määritä edustajan nimi, osoite, verovapausnumero, puhelinnumero ja faksinumero.</td>
</tr>
<tr class="odd">
<td>Maan tai alueen ominaisuudet</td>
<td>Määritä nykyinen yritys maaksi tai alueeksi <strong>Kotimaa</strong>. Määritä nykyisen yrityksen kanssa EU-kauppaa tekevien EU-maiden tai -alueiden maaksi tai alueeksi <strong>EU</strong>. Kunkin maan tai alueen kohdalla ilmoitetaan myös maa- ta aluekoodi ulkomaankauppaa varten.</td>
</tr>
<tr class="even">
<td>Numerojärjestys</td>
<td>Määritä Intrastat-kirjauskansion numerosarja.</td>
</tr>
</tbody>
</table>






