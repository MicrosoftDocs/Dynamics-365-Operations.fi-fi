---
title: Talousraporttien raportointipuiden määritykset
description: Tässä artikkelissa käsitellään raportointipuiden määrityksiä. Raportointipuun määritys on raporttiosa, joka määrittää organisaation rakenteen.
author: jinniew
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: cf5062cfc7ce47a2356c72462da805e8d0d6a756
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727787"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Talousraporttien raportointipuiden määritykset

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja raporttipuun määrityksistä. Raportointipuun määritys on raporttiosa tai rakenneosa, joka auttaa määrittämään organisaation rakenteen ja organisaation.

Talousraportointi tukee joustavaa raportointia, joten muutoksia on helppo tehdä liiketoiminnan rakenteen muuttuessa. Raportit muodostetaan erilaisista osista eli rakenneosista. Yksi näistä rakenneosista on raportointipuun määritys. Raportointipuun määritys auttaa määrittämään organisaation rakenteen ja hierarkian. Se on dimensiot ylittävä hierarkkinen rakenne, joka perustuu taloushallinnon tietojen dimensioiden suhteisiin. Sen avulla saadaan tietoja raportointiyksikkötasolla ja kaikkien puun yksiköiden yhteenvetotasolla. Raportointipuiden määritykset voidaan yhdistää sarakkeiden ja raporttien määrityksiin. Näin luodaan rakenneosaryhmä, jota voidaan käyttää useissa yrityksissä. Raportointiyksikköä käytetään organisaatiokaavion jokaisessa ruudussa. Raporttiyksikkö voi olla yksittäinen osasto taloushallinnon tiedoista tai se voi olla korkeamman tason yhteenvetoyksikkö, joka yhdistää tietoja muista raporttiyksiköistä. Raportointipuun sisältävään raportin määritykseen luodaan yksi raportti kutakin raportointiyksikköä ja yhteenvetotasoa kohti. Näissä raporteissa käytetään raportin määrityksessä määritettyjä rivien ja sarakkeiden määrityksiä, jos raportin määrityksessä ei määritetä käyttämään rivin määrityksen raportointipuuta. Rivien ja sarakkeiden määritykset ovat talousraporttien suunnittelun ja toimintojen tärkeitä komponentteja. Raportointipuut parantavat komponenttien tehokkuutta ja tukevat joustavaa raportointia liiketoiminnan rakenteen muuttuessa. Talousraporteissa, jotka eivät perustu raportointipuuhun, käytetään vain joitakin talousraportoinnin ominaisuuksia. Samoissa rivien ja sarakkeiden määrityksissä voi käyttää useita raportointipuiden määrityksiä. Näin organisaation tietoja voidaan katsella eri tavoin.

## <a name="reporting-tree-best-practices"></a>Raportointipuun parhaat käytännöt
Ennen kuin luot raportointipuun, ota huomioon seuraavat parhaat käytännöt:

- Määritä ensin yrityksen tarvitsemat raportoinnin dimensiot.
- Ota huomioon tapa, jolla rakenne on määritetty, ja tee yritykselle organisaatiokaavio. Organisaatiokaavio auttaa visualisoimaan, miten raporttiyksiköt ryhmitellään yhteen tai useaan raporttipuuhun.
- Aloita alimmalta mahdolliselta erittelytasolta, kuten taloushallinnon tiedoissa määritetyistä osastoista ja projekteista. Lisää erittelytasolle tarvittava määrä ruutuja korkeamman tason divisioonien tai alueiden näyttämistä varten. Kukin ruutu edustaa mahdollista raportointiyksikköä luomassasi raportointipuussa.
- Mieti, mikä on paras tapa muodostaa puut. Voit luoda raportointipuun automaattisella muodostusprosessilla. Voit myös luoda raportointipuun manuaalisesti. On tärkeää, että tunnet molemmat menetelmät ennen puiden suunnittelua.
- Raportointiyksiköt voidaan lisätä raportointipuuhun taloushallinnon tietojen järjestelmässä määritettyjen raportointiyksiköiden avulla.

## <a name="create-multiple-reporting-trees"></a> Useiden raportointipuiden luominen
Luotavien raportointipuiden määrälle ei ole asetettu ylärajaa. Eri puiden avulla organisaation tietoja voi tarkastella eri tavoin. Kukin raporttipuu voi sisältää minkä tahansa osastojen ja yhteenvetoyksiköiden yhdistelmän. Raportin määritys voi sisältää linkin vain yhteen raportointipuuhun kerralla. Voit luoda erilaisia raportointipuita järjestämällä raportointiyksiköiden rakenteen uudelleen. Voit sitten käyttää samaa rivi- ja sarakemääritystä molemmissa raportointipuissa. Voit luoda tällä tavalla nopeasti erilaisia talousraporttiasetteluja. Jos luot useita raportointipuita, voit tulostaa joka kuukausi sarjan yrityksen toimintoja eri tavoin analysoivia ja esitteleviä raportteja. Lisätietoja on tämän artikkelin lopussa olevissa raportointiyksiköiden rakenne-esimerkeissä.

## <a name="create-a-reporting-tree-definition"></a> Raportointipuun määrityksen luominen
Raportointipuun määritys sisältää sarakkeet, joita käsitellään seuraavassa taulukossa.

| Raportointipuu-sarake | Kuvaus |
|-----------------------|-------------|
| Yritys                | Raportointiyksikön yrityksen nimi. Arvo **\@ANY**, joka määritetään tavallisesti vain yhteenvetotasolle, mahdollistaa raporttipuun käyttämisen kaikille yrityksille. Kaikille alielementeille on määritetty yritys. |
| Yksikön nimi             | Koodi, joka määrittää tämän raportointiyksikön graafisessa raportointipuussa. Varmista, että muodostettava yksilöllinen koodausjärjestelmä on yhdenmukainen ja että käyttäjien on helppo ymmärtää sitä. |
| Yksikön kuvaus      | Raportointiyksikön otsikko näkyy raportin ylä- tai alatunnisteessa, jos raportin määrityksen **Ylä- ja alatunnisteet** -välilehteen syötetään **UnitDesc**-koodi. Otsikko näkyy raportin rivin kuvauksessa, jos syötät rivin määrityksen **Kuvaus**-soluun **UnitDesc**. |
| Dimensiot            | Raportointiyksikkö, joka esittää tiedot suoraan taloushallinnon tiedoista. Se määrittää tilin ja liittyvien segmenttien loogisen asettelun ja pituudet. Kullakin raportointiyksikön rivillä on oltava dimensio tässä sarakkeessa. Voit sijoittaa dimension myös yhteenvetotietojen yksikköriville (esimerkiksi kuluille, jotka liittyvät suoraan kyseiseen yksikköön). Jos annat dimension yhteenvetotietojen yksikköriville, pääyksiköissä käytettäviä tilejä ei saa käyttää aliyksiköissä. Muussa tapauksessa summista voi tulla päällekkäisiä. |
| Rivien määritykset       | Raportointiyksikön rivimäärityksen nimi. Samaa rivimääritystä käytetään kullekin raporttipuun yksikölle. Kun luot raportin, tätä rivimääritystä käytetään kullekin raporttiyksikölle. Rivimääritys voi sisältää useita taloushallinnon dimensioiden linkkejä. Jos rivimääritys on määritetty raporttipuussa, valitse **Käytä rivimääritystä raporttipuusta** -valintaruutu raporttimäärityksen **Raportti**-välilehdessä. |
| Taloushallinnon dimensioiden linkki| Raportointiyksikössä käytettävä taloushallinnon dimensioiden linkki. Taloushallinnon dimensioilla määritetään rivimääritykselle linkitettävät taloushallinnon dimensiot. |
| Sivuvaihtoehdot          | Tämä sarake määrittää, estetäänkö raportointiyksikön tiedot, kun raporttia tarkastellaan tai se tulostetaan. |
| Koonti-%              | Pääyksikköön kohdistettavan raportointiyksikön prosenttiosuus. Tähän sarakkeeseen syötettävä prosenttiluku koskee rivin määrityksen jokaista riviä, ennen kuin rivin arvo lisätään pääraporttiin. Jos esimerkiksi aliyksikkö on jaettava tasan kahden osaston kesken, kunkin rivin summat kerrotaan 50 prosentilla, ennen kuin arvo lisätään osaston raporttiin. Yhdellä raportointiyksiköllä ei voi olla kahta pääyksikköä. Raportointiyksikön summat voidaan kohdistaa kahteen pääyksikköön luomalla toinen raportointiyksikkö, jolla on sama dimensio loppujen 50 prosentin kokoamiseen. Anna prosenttiluvut ilman desimaalipilkkua. Esimerkiksi **25** tarkoittaa 25 prosentin kohdistusta pääyksikköön. Jos desimaalipilkkua käytetään (**,25**), pääyksikölle kohdistetaan 0,25 prosenttia. Jos haluat käyttää prosenttilukua, joka on alle yksi, käytä raportin määrityksen **Salli koonti &lt; 1 %** -asetusta. Tämä vaihtoehto on **Raportin asetukset** -valintaikkunan **Lisäasetukset**-välilehdessä. Voit käyttää tätä valintaikkunaa raportin määrityksen **Asetukset**-välilehden **Muu**-painikkeella. |
| Yksikön suojaus         | Rajoitukset, joiden mukaan käyttäjät ja ryhmät voivat käyttää raportointiyksikön tietoja. |
| Lisäteksti       | Raporttiin sisällytettävä teksti. |

Voit luoda raportointipuun määrityksen seuraavien vaiheiden avulla.

1. Avaa Report Designer.
2. Valitse **Tiedosto** &gt; **Uusi** &gt; **Raportointipuun määritys**.
3. Valitse **Muokkaa** &gt; **Lisää raportointiyksiköitä dimensioista**.
4. Valitse **Lisää raportointiyksiköitä dimensioista** -valintaikkunassa jokaisen raportointipuuhun sisällytettävän dimension valintaruutu. **Lisää raportointiyksiköitä dimensioista** -valintaruutu sisältää seuraavat osat.

    | Osa                          | Kuvaus |
    |----------------------------------|-------------|
    | Raportointidimension segmentointi | Voit muokata segmenttien määrää ja pituutta **Jaa segmentit** ja **Yhdistä segmentit** -painikkeilla.<blockquote>[!NOTE] Voit yhdistää vain jakamiasi segmenttejä. Voit yhdistää useita dimensioita dimensioarvojen yleismerkkien avulla.</blockquote> |
    | Sisällytä / merkin sijainti       | Tässä osassa on luettelo taloushallinnon tiedoissa määritetyt dimensiot ja näyttää kunkin dimension pisimmän määritetyn arvon merkkien määrän. Valitse raportointipuuhierarkian dimensioon sisällytettävän dimension valintaruutu. |
    | Segmenttihierarkia ja -alueet     | Tämä osa näyttää dimensiohierarkian. Voit siirtää luettelon dimensioita, jos haluat muuttaa raportointijärjestystä. Voit määrittää kunkin dimension arvoalue **Dimensiosta**- ja **Dimensioon**-kentissä. Jos et määritä aluetta, kaikki dimension arvot lisätään raportointipuuhun.<blockquote>[!NOTE] Jos käytät useampaa kuin yhtä dimensiota, hauissa palautetaan vain ne dimensioyhdistelmät, joihin on kirjattu.</blockquote> |

    Jos haluat nähdä kuvan, jossa on esimerkki **Lisää raportointiyksiköt dimensioista** -valintaikkunasta, katso tässä artikkelissa jäljempänä olevaa osaa Esimerkki lisää raportointiyksiköt dimensioista -valintaruudusta.

5. Voit luoda lisäsegmenttejä (esimerkiksi jakaa yhden segmentin kahdeksi lyhyemmäksi segmentiksi) valitsemalla oikean kohdan **Merkin sijainti** -kentässä ja valitsemalla sitten **Jaa segmentit**.
6. Voit yhdistää kaksi segmenttiä yhdeksi segmentiksi valitsemalla jommankumman segmenttiruudun ja valitsemalla sitten **Yhdistä segmentit**.
7. Hierarkia määrittää, miten dimensiot raportoivat toisilleen. Se määrittää myös kunkin dimension alueen. Voit muuttaa dimensioiden hierarkiaa **Segmenttihierarkia ja -alueet** -alueella valitsemalla ensin siirrettävän dimension ja sitten **Siirrä ylös** tai **Siirrä alas**.
8. Voit lisätä uuden raportointipuun määrittämällä dimensioarvojen alueen **Segmenttihierarkia ja -alueet** -alueella seuraavien vaiheiden avulla:

    1. Anna alueen ensimmäinen arvo kyseisen dimension **Dimensiosta**-kentässä.
    2. Anna alueen viimeinen arvo **Dimensioon**-kentässä.

9. Toista vaiheet 7–8 **Segmenttihierarkia ja -alueet** -alueen jokaisessa dimensiossa.
10. Kun raportointiyksiköiden tuontitapa uuteen raportointipuuhun on määritetty, valitse **OK**.
11. Tallenna raportointipuu valitsemalla **Tiedosto** &gt; **Tallenna**. Syötä raportointipuulle yksilöivä nimi ja kuvaus ja valitse sitten **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Aiemmin luodun raportointipuun määrityksen avaaminen

1. Valitse Report Designerin siirtymisruudussa **Raportointipuiden määritykset**.
2. Avaa raportointipuuluettelo kaksoisnapsauttamalla sen nimeä.
3. Voit tarkastella raportointipuuhun liittyviä rakenneosia napsauttamalla raportointipuun määritystä hiiren kakkospainikkeella ja valitsemalla **Liitokset**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Raportointipuun tietojen koonti

Raportointipuuta käytettäessä aliraportointiyksiköiden summat kerätään pääraportointiyksikön tasolla. Tämä kooste tunnetaan tietojen kokoamisena. Raportointipuun pääyksiköiden summien koonnissa käytetään seuraavia sääntöjä.

- Raportointipuun aliyksiköissä on oltava dimensioita, ellei kyseessä ole yksitasoinen puu. Pääyksiköt eivät yleensä sisällä raportointipuun dimensioita.

    > [!NOTE]
    > Jos määrität sekä ali- että pääyksiköiden dimensiot, raporttiin voi syntyä päällekkäisiä tietoja.

- Raportointiyksiköt, jotka sisältävät raportointipuun dimensioita, vastaavat dimensioita, joita käytetään rivien ja sarakkeiden määrityksissä. Dimensioyhdistelmä määrittää kyseiseen yksikköön palautettavat summat. Esimerkiksi tässä artikkelissa on myöhemmin esimerkki 2, jonka rivit 6 ja 7 palauttavat vain osastot 00 ja 01.
- Pääraportointiyksiköiden summat, jotka eivät sisällä raportointipuun dimensioita, määritetään aliyksikön raportista. Niille kootaan määritetyn pääyksikön summat. Jos esimerkiksi pääyksiköllä (katso Contoso USA tietojen koontiesimerkissä 2) on kaksi aliyksikköä (022 ja 023) eikä se sisällä dimensioita, raportti luodaan jokaiselle ali- ja pääyksikölle. Päätason kokonaissumma on kahden alatason summan yhteismäärä.

### <a name="manage-reporting-units"></a>Raportointiyksiköiden hallinta

Jokainen raportointipuun määritys näytetään yksilöllisinä näkyminä. Graafinen näkymä näyttää pää- ja alihierarkian sekä laskentataulukkonäkymä, joka sisältää kunkin raportointiyksikön määritetyt tiedot. Graafinen näkymä ja laskentataulukkonäkymä liittyvät toisiinsa. Kun valitset raportointiyksikön yhdessä näkymässä, se valitaan myös toisessa näkymässä. Voit muodostaa taloushallinnon tietojen dimensiosuhteisiin perustuvia dimensiot ylittäviä hierarkioita. Voit käyttää raportointipuun määrityksen luomisessa samoja rivien määrityksiä useita kertoja riippumatta siitä, luotko osaston tuloslaskelmaa vai konsolidoitua yhteenvetotuloslaskelmaa. Rivin määrityksessä määritettävät dimensiot voidaan yhdistää raportointipuun määrityksen dimensioihin. Tuloksena on useita organisaation suorituskykyä esittäviä näkymiä.

### <a name="reporting-unit-structure"></a> Raportointiyksikön rakenne

Talousraportoinnissa käytetään seuraavia raportointiyksikkötyyppejä:

- Tietoyksikkö, joka esittää tiedot suoraan taloushallinnon tiedoista.
- Yhteenvetotietojen yksikkö sisältää alemman tason yksiköiden yhteenvetotiedot.

Päätason raportointiyksikkö on yhteenvetotietojen yksikkö, joka yhdistää erittelytietojen yksikön yhteenvetotiedot. Yhteenvetoyksikkö voi olla sekä erittely-yksikkö että yhteenvetoyksikkö. Tämän vuoksi yhteenvetoyksikkö voi hakea tiedot alatason yksiköstä tai taloushallinnon tiedoista. Pääyksikkö voi olla ylätason yksikön aliyksikkö. Aliraportointiyksikkö voi olla erittelytietojen yksikkö, joka noutaa tiedot suoraan taloushallinnon tiedoista. Aliraportointiyksikkö voi olla myös keskitason yhteenvetoyksikkö. Se voi siis toisin sanoen olla alatason yksikön pääyksikkö ja samalla myös ylätason yhteenvetoyksikön aliyksikkö. Yleisin raportointiyksiköiden skenaario on se, että **Dimensiot**-sarakkeen pääyksiköissä on tyhjiä soluja ja että aliyksiköillä on linkkejä määritettyihin tai yleismerkkejä sisältäviin dimensioyhdistelmiin.

### <a name="organize-reporting-units"></a> Raportointiyksiköiden järjestäminen

Voit järjestää raportointipuun määrityksen organisaatiorakenteen uudelleen siirtämällä graafisen näkymän raportointiyksiköitä. Voit myös ylentää raportointiyksiköitä raportointipuun ylemmälle tasolle tai alentaa ne alemmalle tasolle.

1. Avaa Report Designer -ohjelmassa muokattava raportointipuun määritys.
2. Valitse raportointiyksikkö raportointipuun määrityksen graafisessa näkymässä.
3. Vedä yksikkö uuteen kohtaan. Voit vaihtoehtoisesti napsauttaa yksikköä hiiren kakkospainikkeella ja valita **Ylennä raportointiyksikkö** tai **Alenna raportointiyksikkö**.
4. Tallenna muutokset valitsemalla **Tiedosto** &gt; **Tallenna**.

### <a name="add-text-about-a-reporting-unit"></a> Raportointiyksikköä koskevan tekstin lisääminen

Lisätekstin syöttö on enintään 255 merkkiä pitkä staattinen tekstimerkkijono, joka lisää raportointipuun määritykseen tietoja. Lisäteksti voi olla esimerkiksi lyhyt yrityskuvaus. Jokaiselle raportointipuun määrityksen raportointiyksikölle voi luoda enintään kymmenen lisätekstisyöttöä. Lisäteksti näkyy sen raportointipuun raportissa, johon teksti määritettiin. Voit lisätä lisätekstisyötöt rivin määrityksen **Kuvaus**-sarakkeesta ja raportin määrityksen **Ylä- ja alatunnisteet** -välilehdestä.

1. Avaa Report Designer -ohjelmassa muokattava raportointipuun määritys.
2. Kaksoisnapsauta raportointiyksikön rivin **Lisäteksti**-solua.
3. Kirjoita teksti **Lisäteksti**-valintaikkunan ensimmäiselle tyhjälle riville. Ensimmäinen tekstiä sisältävä rivi on nimeltään UnitText1 siitä huolimatta, mikä sen sijainti on **Lisäteksti**-valintaikkunassa.
4. Voit lisätä raportointiyksikköön tekstisyöttöjä kirjoittamalla tekstin tyhjälle riville.
5. Napsauta **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Lisätekstin poistaminen raportointiyksiköstä

1. Avaa raporttien suunnitteluohjelmassa raporttipuu, jota haluat muokata.
2. Kaksoisnapsauta raporttiyksikkörivin **Lisäteksti**-solua.
3. Valitse **Lisäteksti**-valintaikkunassa poistettava merkintä ja valitse sitten **Tyhjennä**. Voit napsauttaa merkintää kakkospainikkeella ja valita **Leikkaa**.
4. Napsauta **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Raportointiyksikön käyttöoikeuden rajoittaminen

Voit estää tiettyjen käyttäjien ja ryhmien käyttämästä raportointiyksikkö. Voit myös määrittää rajoituksia niin, että niitä käytetään raportointiyksikön aliraportointiyksikössä.

1. Avaa Report Designer -ohjelmassa muokattava raportointipuun määritys.
2. Kaksoisnapsauta **Yksikkösuojaus**-solua sen raporttiyksikön rivillä, jonka käyttöä haluat rajoittaa.
3. Valitse **Yksikön suojaus** -valintaikkunassa **Käyttäjät ja ryhmät**.
4. Valitse ne käyttäjät ja ryhmät, jotka tarvitsevat raportointiyksikön käyttöoikeuden, ja valitse sitten **OK**.
5. Voit rajoittaa aliraportointiyksiköiden käyttöoikeuksia valitsemalla **Lisää suojaus aliraportointiyksiköihin** -valintaruutu.
6. Napsauta **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Raportointiyksikön käyttöoikeuden poistaminen

1. Avaa Report Designer -ohjelmassa muokattava raportointipuun määritys.
2. Kaksoisnapsauta sen raportointiyksikön rivin **Yksikön suojaus** -solua, jonka käyttöoikeuden haluat poistaa.
3. Valitse **Yksikön suojaus** -valintaikkunassa nimi ja valitse sitten **Poista**.
4. Valitse **OK**.

## <a name="examples"></a>Esimerkkejä
### <a name="reporting-unit-structure--example-1"></a>Raportointiyksikön rakenne – esimerkki 1

Tämä on seuraavan raportointiyksikön raportointiyksiköiden rakenne:

- Contoso Japanin raportointiyksikkö on Contoso Japan Sales- ja Contoso Japan Consulting -aliyksiköiden pääyksikkö.
- Contoso Japan Sales -divisioonayksikkö on sekä Contoso Japan -yksikön aliyksikkö että Home Sales- ja Auto Sales -yksiköiden pääyksikkö.
- Alimman tason tietojen raportointiyksiköt (Home Sales, Auto Sales, Client Services ja Operations) edustavat taloushallinnon tietojen osastoja. Nämä raportointiyksiköt näkyvät kaavion varjostetulla alueella.
- Korkeamman tason yhteenvetotietojen yksiköt sisältävät erittelytietojen yksiköiden yhteenvetotietoja.

[![Contoso-yhteenvetoraportin rakenne – esimerkki 1.](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Raportointiyksikön rakenne – esimerkki 2

Seuraavan kaavion raportointiyksikössä on yritystoimintojen perusteella jaettu organisaatiorakenne.

[![Contoso-yhteenvetoraportin rakenne – esimerkki 2.](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Esimerkki Raportointiyksiköiden lisääminen dimensioista -valintaikkunasta

Seuraavassa kuvassa on esimerkki **Lisää raportointiyksiköitä dimensioista** -valintaikkunasta. Tässä esimerkissä tulokset palauttavat liiketoimintayksiköiden, kustannuspaikkojen ja osastojen yhdistelmän.

[![Lisää raporttiyksiköitä.](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Tuloksena on raportointipuu, joka lajitellaan ensin liiketoimintoyksikön, sitten kustannuspaikan ja lopuksi osaston mukaan. Viidennen raportointiyksikön dimensio on **Liiketoimintayksikkö = \[001\], Kustannuspaikka = \[\], Osasto = \[022\]** ja se tunnistaa liiketoimintayksikölle 001 ja osastolle 022 kuuluvien tilien raportointiyksikön.

[![Kuva raportointipuusta.](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Esimerkkejä tietojen koonnista

Seuraavassa esimerkissä on koottujen tietojen raportointipuun määrityksessä käytettäviä mahdollisia tietoja.

#### <a name="example-1"></a>Esimerkki 1

[![Usean yrityksen koonti.](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Esimerkki 2

[![Yritysten välisten osastojen koonti.](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Lisäresurssit

[Taloushallinnon raportointi](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
