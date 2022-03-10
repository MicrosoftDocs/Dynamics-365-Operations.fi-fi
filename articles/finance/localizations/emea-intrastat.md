---
title: Intrastat – yleiskatsaus
description: Tämä aihe sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa.
author: EvgenyPopovMBS
ms.date: 01/13/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 97c2b4068f3b8d38281e637ec80f04b19d19be61
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2022
ms.locfileid: "7986034"
---
# <a name="intrastat-overview"></a>Intrastat – yleiskatsaus

[!include [banner](../includes/banner.md)]

Tämä aihe sisältää tietoja Intrastat-raportoinnista, jota käytetään Euroopan unionin (EU) jäsenvaltioiden ja alueiden välillä käytävän tavaroiden (ja joissakin tapauksessa myös palveluiden) kaupan raportoinnissa. Tämä artikkeli sisältää myös raportointiprosessin yleiskatsauksen ja kertoo pakolliset asetukset ja edellytykset.

Intrastat on järjestelmä, jolla kerätään tietoja ja muodostetaan tilastoja Euroopan unionin (EU) jäsenvaltioiden ja alueiden välisestä kaupasta. Intrastat-raportointi on pakollista aina, kun tuote ylittää EU-maan tai -alueen rajan. Monissa maissa ja monilla alueilla Intrastat-raportointi koskee myös palveluja. Intrastat-raporteissa voidaan kerätä pakollisia ja valinnaisia elementtejä. Seuraavat elementit ovat pakollisia: tietojen ilmoittamisesta vastuussa olevan osapuolen arvonlisäveronumero (ALV-numero), viitekausi, suunta (saapuva vai lähtevä), 8-numeroinen tavarankoodi, kumppanin jäsenvaltio (lähettäjäjäsenvaltio saapuvissa ja määräjäsenvaltio lähetyksissä), tavaroiden arvo, tavaroiden määrä (nettopaino ja lisäyksikkö) ja tapahtuman luonne. Maat ja alueet voivat myös kerätä erilaisten ehtojen mukaisesti valinnaisia elementtejä. Valinnaisia elementtejä ovat esimerkiksi alkuperämaa tai -alue, toimitusehdot, kuljetustapa, yksityiskohtaisempi tavaran koodi kuin CN8, alkuperäalue lähetyksissä ja määräalue saapuvissa, tilastomenettely, tilastoarvo, tavaroiden kuvaus sekä kuormauksen tai kuorman purkamisen satama tai lentoasema.

## <a name="overview-of-the-intrastat-reporting-process"></a>Intrastat-raportointiprosessin yhteenveto
Seuraavissa osissa kuvataan Intrastat-raportoinnissa käytettävää yleistä tiedonkulkua.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Anna toisen EU-maan tai -alueen rajan ylittävä tapahtuma

Myyntilasku, vapaatekstilasku, ostolasku, projektilaskun, asiakkaan pakkausluettelo, toimittajan tuotteen vastaanotto tai siirtotilaus siirretään Intrastat-kirjauskansioon vain, jos määrämaan tai -alueen tyyppi (lähtevissä) tai lähettäjätyyppi (saapuvissa) on **EU**. Tämän toiminto laajennettiin Microsoft Dynamics 365 for Operationsiin (1611), ja sen avulla voit määrittää rahtiosoitteita EU:n sisäisille tapahtumille. Jos rahtiosoite on eri kuin toimittajan osoite (tai asiakkaan osoite palautustilauksen osalta), Intrastat-raportointi toimii näillä tiedoilla. Kun luot myyntitilauksen, vapaatekstilaskun, ostotilauksen, toimittajan laskun, projektilaskun tai siirtotilauksen, joissakin ulkomaankauppaan liittyvissä kentissä on oletusarvot asiakirjan otsikossa tai rivillä. Tapahtuman oletuskoodi otetaan vastaavasta kentästä **Ulkomaankaupan parametrit**-sivulla. Tavaran oletuskoodi, alkuperämaa tai -alue sekä alkuperäosavaltio tai -provinssi otetaan nimikkeestä. Voit muuttaa oletusarvoja ja lisätä muut ulkomaankauppaan liittyvät tiedot: tilastomenettelyn, kuljetustavan ja sataman.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Voit luoda tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla

Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta luodaan kuukausittain. Voit siirtää tapahtumat vapaatekstilaskusta, myyntilaskusta, asiakkaan pakkausluettelosta, toimittajan laskusta, toimittajan pakkausluettelosta, projektilaskusta tai siirtotilauksesta **Ulkomaankaupan parametrit** -sivulla määritettyjen ehtojen mukaisesti. Voit antaa tapahtumat myös manuaalisesti. Voit päivittää manuaalisesti siirretyt tapahtumat Intrastat-kirjauskansiossa, jos päivitys on tarpeellinen. Voit tiivistää Intrastat-kirjauskansion tapahtumat **Intrastatin tiivistys** -sivulla määritettyjen erityisehtojen mukaisesti. Joissakin maissa ja joillakin alueilla voi käyttää pienen tapahtuman rajaa. Voit sitten raportoida kyseisen rajan alle jäävät tapahtumat erityisellä tavaran koodilla. Voit päivittää tavaran koodin vastaavilla Intrastat-kirjauskansion riveillä **Ulkomaankaupan parametrit** -sivun **Vähimmäisraja**-asetuksen mukaisesti. Voit myös tiivistää kyseiset tapahtumat **Intrastatin tiivistys** -asetuksen mukaisesti. Voit tarkistaa Intrastat-kirjauskansion tapahtumien valmiusasteen **Ulkomaankaupan parametrit** -sivun **Tarkista asetukset** -asetuksen perusteella. Vastaavien kenttien tietojen valmiusaste voidaan tarkistaa: maa tai alue, osavaltio tai provinssi, paino, tavaran koodi, tapahtumakoodi, lisäyksikkö, satama, alkuperä, toimitusehdot, kuljetustapa ja ALV-tunnus. Tapahtumat, jotka eivät ole valmiita, saavat merkinnän ei kelpaa.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Voit raportoida tietoja EU-maiden -ja alueiden välisestä kaupasta Intrastat-kirjauskansion avulla

Tilastoja varten tiedot EU-maiden ja -alueiden välisestä kaupasta raportoidaan kuukausittain. Voit tulostaa Intrastat-raportin **Ulkomaankaupan parametrit** -sivun **Raporttimuodon yhdistäminen** -asetusten mukaisesti. Voit myös luoda sähköisen tiedoston **Ulkomaankaupan parametrit** -sivun **Tiedostomuodon yhdistäminen** -asetusten mukaisesti. Lisätietoja Intrastat-raportoinnista, kuten edellytyksistä, on Intrastat-raportoinnin tehtävätallenteissa:

  - EU Intrastat -ilmoituksen luominen
  - Siirrä tapahtumat Intrastatiin
  - Rahtiosoitteen määrittäminen yhteisönsisäiselle tapahtumalle.

## <a name="prerequisites"></a>Edellytykset
Seuraavassa taulussa luetellaan Intrastat-raportoinnin edellytykset.

|  Edellytys  |  Kuvaus  |
|-------------------------|-------------------------|
| Osoitemääritys | Määritä maiden ja alueiden ISO (International Organization for Standardization) -koodit. |
| Oikeushenkilö | Määritä tuonnin ja viennin ALV-tunnukset, sivuliikkeen alanumeron tuonti ja vienti sekä yritykselle määritetty Intrastat-koodi. |
| Tuoteluokkahierarkia (myyntihierarkia, hankintahierarkia) | Määritä luokkasolmujen Intrastat-kauppatavarakoodit **Luokkahierarkia**-sivun **Kauppatavarakoodit**-välilehdessä. Kun määrität kauppatavarakoodin pääluokkasolmulle, koodia käytetään kaikissa aliluokkasolmuissa. Valittuja kauppatavarakoodeja voi käyttää **Valittu**-näkymässä, kun valitset kauppatavarakoodin tuotteen tiedoissa sekä myynti-, osto- ja siirtotilausriveillä. |
| Vapautetun tuotteen tiedot | Määritä seuraavat vapautettujen tuotteiden ulkomaankaupan tiedot:<ul><li>**Kauppatavarakoodi** – valitse joko määritetyistä tuoteluokista haettu valittujen kauppatavaroiden luettelo tai täydellinen Intrastat-kauppatavarakoodien luettelo.</li><li>**Tilastollinen maksuprosentti**</li><li>**Alkuperämaa tai -alue** – valitse oletusmaa tai -alue, josta tavarat kokonaisuudessaan hankittiin tai jossa ne valmistettiin.</li><li>**Alkuperäosavaltio tai -provinssi tai määräosavaltio tai -provinssi** – saapuvien oletusarvoinen määräosavaltio tai -provinssi ja lähtevien alkuperäosavaltio tai -provinssi.</li><li>**Nettopaino kilogrammoina**</li><li>**Sulje pois** ‑ Ota tämä parametri käyttöön, kun haluat, ettei tämän tuotteen tapahtumia siirretä Intrastatiin</li></ul> |
| Asiakkaat | Määritä asiakkaan EU-maassa tai -alueella oleva toimitusosoite. |
| Toimittajat | Määritä toimittajan EU-maassa tai -alueella oleva toimitusosoite. |
| Muut kulut | Määritä laskusummaan, tilastosumman tai molempiin sisällytettävä muiden kulujen koodi. Määritä **Kulukoodit**-sivun **Ulkomaankauppa**-välilehdessä **Intrastat-laskun arvo** sisällyttämään kulujen summa laskun arvoon. Määritä myös **Tilastollinen Intrastat-arvo** sisällyttämään kulujen summa tilastoarvoon.</br>Lisätietoja on [tapahtumakoodien ja muiden kulujen](#transaction-codes-and-miscellaneous-charges) arvostelusss. |
| Sähköinen raportointi | Määritä sähköisen raportoinnin määritykset viemään Intrastat-tiedot sähköisenä tiedostona viranomaisten pyytämässä muodossa ja luomaan esikatselu käyttäjälle soveltuvassa luettavassa muodossa (kuten Microsoft Excelissä). |
| Varastointi | Liitä toimittajatilit varastokoodeihin verovapausnumeron täyttämiseksi siirtotilausta siirrettäessä.</br>Lisätietoja on [siirtotilauksen](#transfer-order) esimerkissä.|

## <a name="setup"></a>Asetukset
Seuraavissa osissa käsitellään pakollisia Intrastat-raportoinnin asetuksia.

### <a name="set-up-all-required-intrastat-related-lists"></a>Kaikkien Intrastatiin liittyvien luetteloiden määrittäminen

|   Luettelo   |   Lisätiedot   |
|-------------------------|-------------------------|
| Kauppatavarakoodit | Määritä tyypin **Kauppatavarakoodi** luokkahierarkia ja anna kaikki kauppatavarakoodit yhdistetyn nimikkeistöluettelon mukaisesti. Määritä jokaiselle kauppatavaralle seuraavat tiedot:<ul><li>Kauppatavaran nimi ja kauppatavarakoodi</li><li>Kutsumanimi ja/tai käännetty nimi</li><li>**Ulkomaankauppa**-välilehden raportoinnin (lisä)yksiköiden asetukset. Voit valita lisäyksikön yksikköluettelosta. Voit myös määrittää, raportoidaanko kauppatavaroiden paino valitun lisäyksikön lisäksi.</li></ul>Lisätietoja on [Lisäyksiköiden](#additional-units) esimerkissä.|
| Tapahtumakoodit | Määritä tapahtuman luonne maan tai alueen vaatimusten mukaisesti. Kullekin määritetylle tapahtumakoodille on määritettävä säännöt laskusummien sekä siirtotilausten ja myynti- ja ostotilausten tilastosummien laskemiseen.<ul><li>Siirtotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:<ul><li>**Tyhjä** – määrä on 0 (nolla).</li><li>**Rahoituksellinen kustannus** – summa on yhtä suuri kuin rahoituksellinen kustannus.</li><li>**Kokonaiskustannukset** – summa on yhtä suuri kuin tapahtuman kokonaiskustannukset.</li><li>**Manuaalinen** – summa on yhtä suuri kuin siirtotilausrivillä manuaalisesti määritetty summa.</li></ul></li><li>Myynti- ja ostotilauksille määritetään jokin seuraavista laskusummien ja tilastosummien laskusäännöistä:<ul><li>**Tyhjä** – määrä on 0 (nolla).</li><li>**Laskun summa** – summa on yhtä suuri kuin kauppatavaran laskutettu summa.</li><li>**Veron peruste** – summa on yhtä suuri kuin summa, joka laskutetaan ennen alennusten käyttöä.</li></ul></ul>Lisätietoja on [tapahtumakoodien ja muiden kulujen](#transaction-codes-and-miscellaneous-charges) arvostelusss. |
| Välitystavat | Määritä kuljetustapa maans tai alueen; vaatimusten mukaisesti. Voit kullekin toimitustavalla oletuskuljetustavan **Ulkomaankauppa**-välilehdessä. |
| Satamat | Määritä kuormauksen tai kuorman purkamisen satama tai lentoasema, jos kyseiset tiedot kerään maassa tai alueella. |
| Tilastomenettelyt | Määritä tilastomenettely, jos nämä tiedot kerätään maassa tai alueella. |



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
<li>Myyntitilausten, ostotilausten, hyvityslaskujen ja siirtotilausten tapahtumakoodien oletusarvot. Hyvityslaskulle määritettyä tapahtumakoodia käytetään myös fyysisten tavaroiden palautuskoodina, ja sitä käytetään poikkeavin fyysisten palautusten ja oikaisuhyvityslaskujen vertailussa. Fyysisten tavaroiden palautukset raportoidaan Intrastat-siirrossa eri suuntaan. Saapumisen palautus ilmoitetaan lähetykseksi ja lähetyksen palautus ilmoitetaan saapumiseksi.</li>
<li>Intrastat-raporttien valmistelusta vastaava työntekijä.</li>
</ul></li>
<li><strong>Vähimmäisraja</strong> – määritä raja-arvon alittavien tapahtumien päivitysasetukset:
<ul>
<li>Raja-arvo ja paino</li>
<li>Raja-arvon alittavissa tapahtumissa käytettävä kauppatavarakoodi</li>
</ul></li>
<li><strong>Siirrä</strong> – Määritä ehdot, joilla tapahtumat siirretään Intrastat-kirjauskansioon. Voit määrittää, että tapahtumat siirretään vasta, kun nimikkeissä toteutuu yksi seuraavista ehdoista tai kaikki ehdot toteutuvat:
<ul>
<li>Nimikkeet eivät&#39; ole palvelunimikkeitä.</li>
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
  <li> <strong>Vaihtokurssin tyyppi</strong> – Voit myös määrittää vaihtokurssin, jota käytetään Intrastat-myynnin ja -oston raportointiin ulkomaalaisina valuuttoina. Tätä käytetään, jos kurssi ei ole sama kuin se, jota käytetään, kun tapahtuma kirjataan.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Edustajan yhteystiedot</td>
<td>Määritä edustajan&#39; nimi, osoite, ALV-tunnus, puhelinnumero ja faksinumero.</td>
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

## <a name="example"></a>Esimerkki

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a>Tapahtumakoodit ja muut kulut

Tässä ohjeaiheessa käsitellään skenaariota, jossa Saksassa sijaitsevan yrityksen täytyy ostaa tuotteita Italiassa olevalta yritykseltä. Jotta tämä osto voidaan tehdä, saksalaisen yrityksen on määritettävä uudet tapahtumakoodit ja määritettävä laskusumman ja tilastollisen summan laskentasäännöt kyseisiä tapahtumakoodeja varten. Lisäksi yrityksen on määritettävä muut kulut ja niiden prosentit, kun yritys luo laskun. Näitä arvoja käytetään tilastollisen arvon laskelmassa.

Tässä skenaariossa käytetään **DEMF**-yritystä.

#### <a name="preliminary-setup"></a>Alustavat asetukset

1. Valitse **Organisaation hallinta** > **Organisaatio** > **Yritykset** ja valitse **DEMF**.
2. Varmista **Osoitteet**-pikavälilehdellä, että **Maa/alue**-kentän arvoksi on määritetty **DEU(Saksa)**.
3. Valitse **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**.
4. Valitse ruudukossa **DE-001**.
5. Valitse **Osoite**-pikavälilehdessä **Muokkaa**.
6. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **ITA**.
7. Sulje valintaikkuna valitsemalla **OK**.

#### <a name="set-up-transaction-codes"></a>Määritä tapahtumakoodit

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
2. Valitse ruudukossa **11**. Valitse sitten toimintoruudussa **Poista**.
3. Valitse toimintoruudussa **Uusi**.
4. Kirjoita **Tapahtumakoodi**-pikavälilehden **Tapahtuma** **-koodi**-kenttään **11**.
5. Syötä **Nimi**-kenttään **Suora osto tai myynti**.
6. Valitse **Myynti ja ostot** -osan **Laskun summa** -kentästä **Laskun summa**.
7. Valitse **Tilastosumma**-kentästä **Laskun summa**.
8. Valitse toimintoruudussa **Tallenna**.

#### <a name="set-up-miscellaneous-charges"></a>Muiden kulujen määrittäminen

1. Valitse **Myyntireskontra** > **Kulujen määritys** > **Kulujen koodi**.
2. Valitse ruudukossa **Rahti**.
3. Valitse toimintoruudussa **Muokkaa**.
4. Määritä **Ulkomaankauppa**-pikavälilehdessä **Intrastat-laskun arvoksi** ja **Intrastatin tilastollisen arvon** arvoksi **Kyllä**.

#### <a name="set-up-foreign-trade-parameters"></a>Määritä ulkomaankaupan parametrit

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
2. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtuma****koodi**-kentässä **11**.
3. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kenttään on määritetty **Intrastat**.

#### <a name="create-a-purchase-order"></a>Luo ostotilaus

1. Valitse **Ostoreskontra** > **Ostotilaukset** > **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo ostotilaus** -valintaikkunan **Toimittajatili**-kentässä **DE-001**.
4. Valitse **OK**.
5. Tarkista **Otsikko**-välilehden **Ulkomaan****kauppa**-pikavälilehdessä, että **Tapahtumakoodi**-kentän määrityksenä on **11**.
6. Valitse **Rivit**-välilehden **Ostotilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **D0003**. Anna sitten **Määrä**-kenttään **10**.
7. Varmista **Rivin tiedot**-pikavälilehden **Ulkomaankauppa**-välilehden **Ulkomaankauppa**-osiossa, että **Tapahtumakoodi**-kenttä on asetettu automaattisesti.
8. Valitse **Kulut**-osan **Myyntitiedot**-valikon **Ostotilausrivit**-pikavälilehdestä **Ylläpidä kuluja**.
9. Valitse **Kulujen koodi** -kentässä **RAHTI**.
10. Kirjoita **Kulujen arvo** -kenttään **30**.
11. Valitse toimintoruudussa **Tallenna**. Sulje sitten sivu.
12. Valitse toimintoruudun **Ostot**-välilehden **Toiminnot**-ryhmässä **Vahvista**.
13. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
14. Valitse toimintoruudussa **Oletusarvo kohteesta**. Valitse **Rivien oletusmäärä** -kentässä **Tilattu määrä**. Valitse sitten **OK**.
15. Anna **Toimittajan laskun otsikko** -pikavälilehden **Laskun tunnus** -osan **Numero**-kentässä **00100**.
16. Valitse **Laskujen päivämäärät** -osan **Laskun päivämäärä** -kentässä **24.11.2021** (24. marraskuuta 2021).
17. Kirjaa lasku valitsemalla toimintoruudussa **Kirjaa**.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Toimittajan laskun siirtäminen Intrastat-kirjauskansioon

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Toimittajan lasku**-asetukseksi **Kyllä**.
4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio.

   ![Rivi, joka esittää Intrastat-sivun ostotilauksen sekalaisten kulujen kanssa](media/intrastat_overview_1.png)

5. Tarkista ostotilauksen **Yleiset**-välilehti. Huomaa, että **Laskun arvo** -kentässä näkyvät **Laskun summa**- ja **Laskukulujen summa** -kenttien summa. **Tilastollinen arvo** -kentässä näkyy **tilastollisen summan** ja **tilastollisten kulujen summa** -kenttien summa.

   ![Ostotilauksen tiedot sekalaisten kulujen kera Intrastat-sivun Yleiset-välilehdellä](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Siirtotilaus

Tässä esimerkissä Saksan yrityksen on kuljetettava kaksi tavarayksikköä Saksan varastosta Italian varastoon. Myös tälle tuotteelle on määritettävä 20 prosentin hintaa koskevat kulut **Tilastollinen arvo** -kentässä kirjanpitoa varten. Tässä esimerkissä käytetään **DEMF**-yritystä.

#### <a name="preliminary-setup"></a>Alustavat asetukset

1. Valitse **Organisaation hallinta** > **Organisaatio** > **Yritykset** ja valitse **DEMF**.
2. Varmista **Osoitteet**-pikavälilehdellä, että **Maa/alue**-kentän arvoksi on määritetty **DEU(Saksa)**.
3. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
4. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kenttään on määritetty **Intrastat**.
5. Valitse **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**.
6. Valitse ruudukossa **DE-001**.
7. Valitse **Osoite**-pikavälilehdessä **Muokkaa**.
8. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **ITA**.
9. Sulje valintaikkuna valitsemalla **OK**.

#### <a name="set-up-transaction-codes"></a>Määritä tapahtumakoodit

1. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Tapahtumakoodit**.
2. Valitse ruudukossa **11**. Valitse sitten toimintoruudussa **Poista**.
3. Valitse toimintoruudussa **Uusi**.
4. Kirjoita **Tapahtumakoodi**-pikavälilehden **Tapahtuma** **-koodi**-kenttään **11**.
5. Syötä **Nimi**-kenttään **Suora osto tai myynti**.
6. Valitse **Siirtotilaus**-osan **Laskun summa** -kentästä **Kokonaiskustannus**.
7. Valitse **Tilastosumma**-kentästä **Kokonaiskulu**.
8. Valitse toimintoruudussa **Tallenna**.
9. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
10. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Siirtotilaus**-kentästä **11**.

#### <a name="set-up-charges-for-an-item"></a>Nimikkeen kulujen määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse ruudukossa **D0001**.
3. Syötä **Ulkomaankauppa**-pikavälilehdessä **Intrastat**-osan **Kuluprosentti**-kenttään **20**.

#### <a name="change-the-site-address"></a>Toimipaikan osoitteen muuttaminen

1. Valitse **Varastonhallinta** > **Asetukset** > **Varasto** > **Toimipaikat**.
2. Valitse ruudukossa **1**.
3. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
4. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **DEU**.
5. Valitse **OK**.
6. Valitse ruudukossa **2**.
7. Valitse **Osoitteet**-pikavälilehdessä **Muokkaa**.
8. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **ITA**.
9. Valitse **OK**.
10. Siirry kohtaan **Varastonhallinta** > **Asetukset** > **Varasto** > **Varastot**.
11. Valitse ruudukossa **21**.
12. Valitse **Yleiset**-pikavälilehden **Viite**-osan **Toimittajatili**-kentässä **DE-001**.

#### <a name="create-a-transfer-order"></a>Siirtotilauksen luonti

1. Valitse **Varastonhallinta** > **Saapuvat tilaukset** > **Siirtotilaus**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Rivit**-välilehden **Siirtotilauksen otsikko** -pikavälilehden **Yhteenveto**-osan **Varastosta**-kentästä **11**. Valitse **Varastoon**-kentässä **21**.
4. Valitse **Rivit**-välilehden **Siirtotilausrivit**-pikavälilehdestä **Lisää**.
5. Valitse **Nimikkeen numero** -kentässä **D0001**. Anna sitten **Siirtomäärä**-kenttään **2**.
6. Varmista **Rivin tiedot**-pikavälilehden **Ulkomaankauppa**-välilehden **Ulkomaankauppa**-osiossa, että **Tapahtumakoodi**-kenttä on asetettu automaattisesti.
7. Valitse toimintoruudun **Lähetä**-välilehden **Toiminnot** -ryhmässä **Lähetä siirtotilaus**.
8. Valitse **Lähetys**-valintaikkunan **Yhteenveto**-välilehden **Päivitä**-kentästä **Kaikki**.
9. Lähteä tilaus valitsemalla **OK**.
10. Valitse toimintoruudun **Vastaanota**-välilehden **Toiminnot**-ryhmässä **Vastaanota**.
11. Valitse **Vastaanota**-valintaikkunan **Yhteenveto**-välilehden **Päivitä**-kentästä **Kaikki**.
12. Lähteä tilaus valitsemalla **OK**.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Siirrä siirtomääräys Intrastat-päiväkirjaan

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunassa **Siirtotilaus**-asetuksen arvoksi **Kyllä** ja kaikkien muiden asetusten arvoksi **Ei**.
4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio.

   ![Intrastat-sivulla olevan siirtotilauksen ilmaiseva rivi](media/intrastat_overview_3.png)

5.  Tarkista siirtotilauksen **Yleiset**-välilehti.

    Huomaa, että **Laskun arvo**- ja **Tilastoarvo**-osioiden kentät määritetään automaattisesti. **Laskun summa**- ja **Tilastosumma**-kentät perustuvat **Tapahtumakoodit**-sivun asetuksiin. **Kuluprosentti**-kentän arvo **20** on **Vapautettu tuote** -sivulla määritetty arvo. **Tilastollisten kulujen summa** -kentän arvo on kulujen määrällinen lauseke (koska 107,24 on 20 prosenttia 536,18:sta). **Tilastollinen arvo** -kentän arvo on **tilastollinen summa**- ja **tilastollisten kulujen summa** -kenttien arvojen summa.

  ![Siirtotilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Lisäyksiköt

Tässä esimerkissä Saksan yrityksen on ostettava 10 yksikköä Italian yritykseltä. Tullikoodien lisäksi kyseisille tavaroille on määritettävä lisäyksiköt. Esimerkissä kerrotaan, miten luodaan uusia mittayksiköitä, määritetään Intrastat-kauppatavarakoodille lisäyksiköitä, kirjataan lisäyksiköitä muodostavat tapahtumat ja tarkistetaan Intrastat-kirjauskansio, jossa lisäyksiköiden kenttä on määritetty.

#### <a name="preliminary-setup"></a>Alustavat asetukset

1. Valitse **Organisaation hallinta** > **Organisaatio** > **Yritykset** ja valitse **DEMF**.
2. Varmista **Osoitteet**-pikavälilehdellä, että **Maa/alue**-kentän arvoksi on määritetty **DEU(Saksa)**.
3. Valitse **Vero** > **Määritys** > **Ulkomaankauppa** > **Ulkomaankaupan parametrit**.
4. Valitse **Intrastat**-välilehden **Yleiset**-pikavälilehden **Tapahtuma****koodi**-kentässä **11**.
5. Varmista, että **Kauppatavarakoodihierarkia**-pikavälilehden **Luokkahierarkia**-kenttään on määritetty **Intrastat**.
6. Valitse **Ostoreskontra** > **Toimittajat** > **Kaikki toimittajat**.
7. Valitse ruudukossa **DE-001**.
8. Valitse **Osoite**-pikavälilehdessä **Muokkaa**.
9. Valitse **Muokkaa osoitetta** -valintaikkunan **Maa tai alue** -kentässä **ITA**.
10. Sulje valintaikkuna valitsemalla **OK**.

#### <a name="create-a-unit-of-measure"></a>Mittayksikön luominen

1. Valitse **Organisaation hallinta** > **Määritys** > **Yksiköt** > **Yksiköt**.
2. Valitse toimintoruudussa **Uusi**.
3. Syötä määrän mittayksikön nimi **Yksikkö**-kenttään. Syötä tässä esimerkissä arvoksi **GRM**.
4. Valitse **Yleinen**-pikavälilehden **Luokitus**-osan **Yksikköluokka**-kentästä ominaisuus, jota yksikkö mittaa. Valitse tässä esimerkissä **Massa**.
5. Valitse **Yksikköjärjestelmä**-kentästä mittajärjestelmä, johon yksikkö kuuluu. Valitse tässä esimerkissä **Metriset yksiköt**.

#### <a name="set-up-unit-conversions"></a>Määritä yksikön muunnokset

1. Valitse **Organisaation hallinta** > **Määritys** > **Yksiköt** > **Yksikön muunnokset**.
2. Valitse **Luokkien väliset muunnokset**-välilehdessä **Uusi**.
3. Valitse **Yksikkömuunnos** -valintaikkunan **Tuote**-kentässä **F00007**.
4. Valitse **Yksiköstä**-kentässä **kpl**.
5. Valitse **Yksikköön**-kentässä **GRM**.
6. Tarkista, että muuntokurssi on **1 = 1**.
7. Valitse **OK**.
8. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
9. Valitse ruudukossa **F00007**.
10. Anna **Varastonhallinta**-pikavälilehden **Varasto**-osan **Yksikkö**-kentässä **GRM**.
11. Valitse toimintoruudussa **Tallenna**.

#### <a name="set-up-product-information"></a>Tuotetietojen määrittäminen

1. Valitse **Tuotetietojen hallinta** > **Tuotteet** > **Vapautetut tuotteet**.
2. Valitse ruudukossa **F00007**.
3. Valitse **Ulkomaankauppa**-pikavälilehden **Intrastat**-osan **Kauppatavara**-kentässä **920 20 34**.
4. Valitse toimintoruudussa **Tallenna**.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Lisäyksikön liittäminen Intrastate-kauppatavarakoodiin

1. Valitse **Tuotetietojen hallinta** > **Määritys** > **Luokat ja määritteet** > **Luokkahierarkiat**.
2. Valitse luettelosta **Intrastat**.
3. Valitse ruudukossa **Kaiutin**.
4. Valitse **Ulkomaankauppa**-pikavälilehden **Lisäyksiköt** -kentässä **GRM**.
5. Valitse toimintoruudussa **Tallenna**.

   Lisätietoja on kohdassa [Mittayksiköiden hallinta](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Luo ostotilaus

1. Valitse **Ostoreskontra** > **Ostotilaukset** > **Kaikki ostotilaukset**.
2. Valitse toimintoruudussa **Uusi**.
3. Valitse **Luo ostotilaus** -valintaikkunan **Toimittajatili**-kentässä **DE-001**.
4. Valitse **OK**.
5. Tarkista **Otsikko**-välilehden **Ulkomaankauppa**-pikavälilehdessä, että **Tapahtumakoodi**-kentän määrityksenä on **11**.
6. Valitse **Rivit**-välilehden **Ostotilauksen rivit** -pikavälilehden **Nimikkeen numero** -kentässä **F00007**. Anna sitten **Määrä**-kenttään **10**.
7. Varmista **Rivin tiedot**-pikavälilehden **Ulkomaankauppa**-välilehden **Ulkomaankauppa**-osiossa, että **Tapahtumakoodi**- ja **Kauppatavara**-kentät on asetettu automaattisesti.
8. Valitse toimintoruudun **Ostot**-välilehden **Toiminnot**-ryhmässä **Vahvista**.
9. Valitse Toimintoruudun **Laskutus**-välilehden **Luo**-ryhmässä **Lasku**.
10. Valitse toimintoruudussa **Oletusarvo kohteesta**. Valitse **Rivien oletusmäärä** -kentässä **Tilattu määrä**. Valitse sitten **OK**.
11. Anna **Toimittajan laskun otsikko** -pikavälilehden **Laskun tunnus** -osan **Numero**-kentässä **VE-0010**.
12. Valitse **Laskujen päivämäärät** -osan **Laskun päivämäärä** -kentässä **5.10.2021** (5. lokakuuta 2021).
13. Kirjaa lasku valitsemalla toimintoruudussa **Kirjaa**.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Toimittajan laskun siirtäminen Intrastat-kirjauskansioon

1. Valitse **Vero** > **Ilmoitukset** > **Ulkomaankauppa** > **Intrastat**.
2. Valitse toimintoruudussa **Siirto**.
3. Määritä **Intrastat (Siirto)** -valintaikkunan **Toimittajan lasku**-asetukseksi **Kyllä**.
4. Siirrä tapahtumat valitsemalla **OK** ja tarkista Intrastat-kirjauskansio.

   ![Intrastat-sivulla olevan ostotilauksen ilmaiseva rivi](media/intrastat_overview_5.png)

5. Tarkista ostotilauksen **Yleiset**-välilehti. Huomaa, että **Yksikkö**-osan **lisäyksiköiden määrä**- ja **Lisäyksikkö**-kentät määritetään automaattisesti.

   ![Ostotilauksen tiedot Intrastat-sivun Yleiset-välilehdessä](media/intrastat_overview_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
