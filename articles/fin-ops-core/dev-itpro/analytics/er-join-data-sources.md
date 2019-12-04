---
title: Käytä ER-mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista
description: Tässä ohjeaiheessa kerrotaan JOIN-tietolähteiden käytöstä sähköisessä raportoinnissa (ER).
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667951"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Käytä sähköisen raportoinnin (ER) mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista

[!include[banner](../includes/banner.md)]

Kun määrität sähköisen raportoinnin (ER) mallimäärityksiä tai muotoja, voit [lisätä](#review) tarvittavia **Liitä**-tyypin tietolähteitä. Suunnitteluvaiheessa **Liitä**-tietolähde määritetään useiden tietolähteiden sarjaksi, ja jokainen tietolähde palauttaa tietueluettelon. Ensimmäistä tietolähdettä lukuun ottamatta sinulle on määritettävä jokaiselle niistä tarvittavat ehdot nykyisen ja aiempien tietolähteiden tietueiden liittämiselle. Suorituksen aikana määritetty **Liitä**-tyypin tietolähde [palauttaa](#executeERformat) yksittäisen yhteenliitetyn luettelon tietueista, jotka sisältävät kenttiä sisäkkäisten tietolähteiden tietueista.

Tällä hetkellä tuetaan seuraavia liitostyyppejä:

- Ulkoliitos (vasen):
    - Liittää kaikki määritettyjä ehtoja vastaavat ensimmäisen (vasemmanpuoleisen) tietolähteen tietueet yhteen ja lisää sitten kaikki määritettyjä ehtoja vastaavat toisen (oikeanpuoleinen) tietolähteen tietueet.
- Sisäliitos (oikea):
    - Liittää yhteen vain määritettyjä ehtoja vastaavat ensimmäisen (vasemmanpuoleisen) tietolähteen tietueet yhteen ja vain määritettyjä ehtoja vastaavat toisen (oikean) tietolähteen tietueet yhteen.

Kun määritetyn **Liitä**-tietolähteen kaikki tietolähteet ovat tyyppiä **Taulukkotietueet** Liitos-tietolähde voidaan [suorittaa tietokantatasolla](#analyze) käyttäen yksittäistä SQL-lausetta. Tämä vähentää tietokantakyselyjen määrää ja parantaa siten mallimäärityksen suorituskykyä. Muussa tapauksessa **Liitä**-tietolähde suoritetaan muistissa.

> [!NOTE]
> **VALUEIN**-toiminnon käyttämistä ER-lausekkeissa, joissa määritetään ehtoja tietueiden liittämiselle toisiinsa Liitä-tyypin tietolähteissä, ei vielä tueta. Kohdassa [Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md) esitetään lisätietoja tästä toiminnosta.

Saat lisätietoja tästä toiminnosta suorittamalla tämän ohjeaiheen seuraavan esimerkin.

## <a name="example-use-join-data-sources-in-er-model-mappings"></a>Esimerkki: JOIN-tietolähteiden käyttö ER-mallimäärityksissä

Seuraavissa vaiheissa selitetään, miten järjestelmänvalvoja tai sähköisen raportoinnin kehittävä voi määrittää sähköisen raportoinnin (ER) mallimäärityksen saadakseen tietoja samanaikaisesti useista sovellustaulukoista käyttämällä **Liitos**-tyypin tietolähteitä parantaakseen tietojen käytön suorituskykyä. Nämä vaiheet voidaan suorittaa mitä tahansa Dynamics 365 Finance -yrityksestä tai Regulatory Configuration Serviceä (RCS) varten.

### <a name="prerequisites"></a>Edellytykset

Tämän aiheen esimerkkien suorittaminen edellyttää käyttöoikeuksia johonkin seuraavista riippuen siitä, mitä palvelua vaiheiden suorittamiseen käytetään:

**Finance-käyttöoikeudet seuraaville rooleille:**

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

**RCS-käyttöoikeudet seuraaville rooleille:**

- Sähköisen raportoinnin kehittäjä
- Sähköisen raportoinnin toiminnallinen konsultti
- Järjestelmänvalvoja

Sinun on myös ensin suoritettava menettelyn [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.

Lisäksi sinun on ladattava etukäteen [Microsoft Download Centeristä](https://go.microsoft.com/fwlink/?linkid=000000) ja tallennettava paikallisesti seuraavat ER-konfiguraatiotiedostomallit:

| **Sisällön kuvaus**  | **Tiedostonimi**   |
|--------------------------|-----------------|
| Esimerkeissä tietolähteenä käytettävä **ER-tietomalli**-konfiguraatiotiedosto.| [Model to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Esimerkissä käytettävä **ER-mallimääritys**-konfiguraatiotiedosto, joka soveltaa ER-tietomallia esimerkkeihin. | [Mapping to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Esimerkissä käytettävä **ER-muoto**-konfiguraatiotiedosto. Tässä tiedostossa kuvataan tiedot, joilla täytetään esimerkkien ER-muotokomponentti. | [Format to learn JOIN data sources.version.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a>Aktivoi konfiguraatiolähde

1. Käytä joko Finance- tai RCS-sovellusta verkkoselaimesi ensimmäisessä istunnossa.
2. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.
3. Tarkista **Lokalisointikonfiguroinnit**-sivun **Konfiguraation lähteet** -osassa, että näyteyrityksen Litware, Inc. (http://www.litware.com) konfiguraation lähde on luettelossa ja että sen tila on **Aktiivinen**. Jos konfiguraation lähde ei ole näkyvissä, suorita menettelyn [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.

    ![Sähköisen raportoinnin työtila](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>ER-mallikonfiguraatiotiedostojen tuonti

1. Valitse **Raportointikonfiguraatiot**.
2. Tuo ER-tietomallin konfiguraatiotiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Model to learn JOIN data sources.version.1.1.xml**.
    4. Valitse **OK**.
3. Tuo ER-mallimäärityksen konfiguraatiotiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Mapping to learn JOIN data sources.version.1.1.xm**.
    4. Valitse **OK**.
4.  Tuo ER-muotokonfiguraatiotiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Format to learn JOIN data sources.version.1.1.xm**.
    4. Valitse **OK**.
5.  Laajenna konfiguraatioiden puurakenteessa nimike **Mallinnus JOIN-tietolähteiden selvittämiseksi** sekä muut mallinimikkeet (jos käytettävissä).
6.  Pane merkille puurakenteen ER-konfiguraatioiden luettelo sekä **Versiot**-pikavälilehden versiotiedot. Niitä käytetään malliraporttisi tietolähteenä.

    ![Sähköisen raportoinnin konfiguraatiosivu](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Suorituksen jäljitysasetusten käyttöönotto
1.  Valitse **KONFIGURAATIOT**.
2.  Valitse **Käyttäjän parametrit**.
3.  Määritä suorituksen jäljitysparametrit alla esitetyn näyttökuvan mukaisesti.

    ![Sähköisen raportoinnin käyttäjän parametrien sivu](./media/GER-JoinDS-Parameters.PNG)

    Kun nämä parametrit ovat käytössä, suorituksen jäljitys luodaan jokaiselle tuodun ER-muototiedoston suoritukselle. Luodun suorituksen jäljityksen tietojen avulla voit analysoida ER-muodon ja ER-mallimäärityksen komponenttien suorituksen. Lisätietoja sähköisen raportoinnin suorituksen jäljitystoiminnosta saat sivulta [Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER-mallimäärityksen tarkistus (osa 1)

Tarkista ER-mallimäärityskomponentin asetukset. Komponentti on määritetty käyttämään ER-konfiguraatioiden mallien tietoja, konfiguraatioiden ja konfiguraatiolähteiden tietoja käyttämättä **Liitä**-tyypin tietolähteitä.

1.  Valitse konfiguraatio **Määritys JOIN-tietolähteiden selvittämiseksi**.
2.  Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.
3.  Tarkista määritystiedot valitsemalla **Suunnittelutoiminto**. 
4.  Valitse **Näytä tiedot**.
5.  Laajenna konfiguraatioiden puurakenteessa tietomallinimikkeet **Set1** ja **Set1.Details**:

    1. Sitova **Details: Record list = Versions** ilmaisee, että nimike **Set1.Details** on sidottu **Versiot**-tietolähteeseen, joka palauttaa **ERSolutionVersionTable**-taulukon tietueita. Kukin tämän taulukon tietue edustaa yksittäistä ER-konfiguraation versiota. Tämän taulukon sisältö esitetään **Versiot**-pikavälilehdessä **Konfiguraatiot**-sivulla.
    2. Sitova **ConfigurationVersion: String = @.PublicVersionNumber** tarkoittaa, että kunkin ER-konfiguraation version julkisen version arvo perustuu **PublicVersionNumber**-kentän arvoon taulukossa **ERSolutionVersionTable** ja että se sijoitetaan nimikkeeseen **ConfigurationVersion**.
    3. Sitova **ConfigurationTitle: String = @.'>Relations'.Solution.Name** ilmaisee, että ER-konfiguraation nimi perustuu **Nimi**-kenttään taulukossa **ERSolutionTable**, joka vuorostaan perustuu monta yhteen -suhteeseen (**'>Relations'**) taulukkojen **ERSolutionVersionTable** ja **ERSolutionTable** välillä. Kulloisenkin sovellusesiintymän ER-konfiguraatioiden nimet esitetään **Konfiguraatiot**-sivun konfiguraatioiden puurakenteessa.
    4. Sitova **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** tarkoittaa, että kulloisenkin konfiguraation omistava konfiguraatiolähde perustuu **Nimi**-kenttään taulukossa **ERVendorTable**, joka vuorostaan perustuu monta yhteen -suhteeseen taulukkojen **ERSolutionTable** ja **ERVendorTable** välillä. ER-konfiguraatiolähteiden nimet esitetään konfiguraatioiden puurakenteessa **Konfiguraatiot**-sivun jokaisessa konfiguraation sivuotsikossa. Koko luettelo ER-konfiguraatiolähteistä esitetään taulukkosivulla **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraation lähde**.

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-Set1Review.PNG)

6.  Laajenna tietomallinimike **Set1.Summary** konfiguraatioiden puurakenteessa:

    1. Sitova **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** ilmaisee, että nimike **Set1.Summary.VersionsNumber** on sidottu **GroupBy**-tyypin **VersionsSummary**-tietolähteen koostekenttään **VersionsNumber**, joka määritettiin palauttamaan **ERSolutionVersionTable**-taulukon tietuemäärä **Versiot**-tietolähteen kautta.

    ![GROUPBY-tietolähteen parametrisivu](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  Sulje sivu.

### <a name="review"></a> ER-mallimäärityksen tarkistus (osa 2)

Tarkista ER-mallimäärityskomponentin asetukset. Komponentti on määritetty käyttämään ER-konfiguraatioiden mallien tietoja, konfiguraatioiden ja konfiguraatiolähteiden tietoja käyttäen **Liitä**-tyypin tietolähdettä.

1.  Laajenna konfiguraatioiden puurakenteessa tietomallinimikkeet **Set2** ja **Set2.Details**. Ota huomioon, että sitova **Details: Record list = Details** ilmaisee, että nimike **Set2.Details** on sidottu **Tiedot**-tietolähteeseen, joka on määritetty **Liitä**-tyypin tietolähteeksi.

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-Set2Review.PNG)

    **Liitä**-tietolähde voidaan lisätä valitsemalla **Toiminnot\Liitä**-tietolähde:

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-AddJoinDS.PNG)

2.  Valitse **Tiedot**-tietolähde.
3.  Valitse **Muokkaa** **Tietolähteet**-ruudussa.
4.  Valitse **Muokkaa liitä**.
5.  Valitse **Näytä tiedot**.

    ![JOIN-tietolähteen parametrisivu](./media/GER-JoinDS-JoinDSEditor.PNG)

    Tätä sivua käytetään **Liitä**-tyypin pakollisen tietolähteen suunnittelemiseen. Suorituksen aikana tämä tietolähde luo yksittäisen yhteenliitetetyn tietueluettelon **Liitettyjen luettelo** -ruudukon tietolähteistä. Tietueiden liitos alkaa tietolähteestä **ConfigurationProviders**, joka on ruudukossa ensimmäisenä (**Tyyppi**-sarake on tyhjänä sen osalta). Muiden tietolähteiden tietueet liitetään sen jälkeen päätietolähteen tietueisiin kyseisen ruudukon mukaisessa järjestyksessä. Jokainen liitettävä tietolähde on määritettävä kohdetietolähteen alaiseksi tietolähteeksi (**1Versions**-tietolähde on tietolähteen **1Configurations** alainen; **1Configurations**-tietolähde on tietolähteen **ConfigurationProviders** alainen). Kunkin määritetyn tietolähteen on sisällettävä liitoksen ehdot. Tässä **Liitä**-tyypissä määritetään seuraavat liitokset:

    - Kuhunkin tietolähteen **ConfigurationProviders** (johon viitataan **ERVendorTable**-taulukossa) liitetään vain tietolähteen **1Configurations** (johon viitataan **ERSolutionTable**-taulukossa) tietueita, joilla on sama arvo kentissä **SolutionVendor** ja **RecId**. Tähän liitokseen käytetään **Sisäliitos**-tyyppiä sekä seuraavia ehtoja tietueiden täsmäämiseen: 

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Kuhunkin tietolähteen **1Configurations** (johon viitataan **ERSolutionTable**-taulukossa) liitetään vain tietolähteen **1Versions** (johon viitataan **ERSolutionVersionTable**-taulukossa) tietueita, joilla on sama arvo kentissä **Solution** ja **RecId**. Tähän liitokseen käytetään **Sisäliitos**-tyyppiä sekä seuraavia ehtoja tietueiden täsmäämiseen:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - **Suorita**-asetuksen arvoksi määritetään **Kysely**, mikä tarkoittaa, että tämä liitoksen tietolähde suoritetaan suorituksen aikana tietokannan tasolla suoran SQL-kutsun muodossa.

    Huomaa, että voit sovellustaulukkoja edustavien tietolähteiden tietueiden liitosten yhteydessä määrittää liitosehtoja käyttäen kenttäpareja, jotka eivät kuvaa olemassa olevia näiden taulukkojen välisiä AOT-suhteita. Myös tällainen liitos voidaan määrittää suoritettavaksi tietokantatasolla.

6.  Sulje sivu.
7.  Valitse **Peruuta**.
8.  Laajenna tietomallinimike **Set2.Summary** konfiguraatioiden puurakenteessa:

    - Sitova **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** ilmaisee, että nimike **Set2.Summary.VersionsNumber** on sidottu **GroupBy**-tyypin **DetailsSummary**-tietolähteen koostekenttään **VersionsNumber**, joka määritettiin palauttamaan **Liitä**-tyypin **Tiedot**-tietolähteen liitettyjen tietueiden määrä.
    - Huomaa, että **Suorita**-sijaintiasetuksen arvoksi määritetään **Kysely**, mikä tarkoittaa, että tämä **GroupBy**-tietolähde suoritetaan suorituksen aikana tietokannan tasolla suoran SQL-kutsun muodossa. Tämä on mahdollista, koska perustietolähde **Liitä**-tyypin perustietolähde **Tiedot** on määritetty suoritettavaksi tietokannan tasolla.

    ![GROUPBY-tietolähteen parametrisivu](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  Sulje sivu.
10. Valitse **Peruuta**.

### <a name="executeERformat"></a> Suorita ER-muoto

1.  Access Finance tai RCS on verkkoselaimesi toinen istunto, jossa käytetään samoja tunnistetietoja ja yritystä kuin ensimmäisessä istunnossa.
2.  Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
3.  Laajenna konfiguraatio **Mallinnus JOIN-tietolähteiden selvittämiseksi** configuration.
4.  Valitse konfiguraatio **Muotoilu JOIN-tietolähteiden selvittämiseksi**.
5.  Valitse **Suunnittelu**.
6.  Valitse **Näytä tiedot**.
7.  Valitse **Määritys**.
8.  Valitse **Laajenna/kutista**.

    Huomaa, että tämä muotoilu on suunnitelty täyttämään luotava tekstitiedosto uudella rivillä kutakin ER-konfiguraation versiota kohden (**Versio**-sekvenssiä). Kukin luotu rivi sisältää sen konfiguraatiolähteen nimen, joka omistaa kulloisenkin konfiguraation, konfiguraation nimen sekä konfiguraation version puolipistein eroteltuna. Luodun tiedoston viimeinen rivi sisältää havaittujen ER-konfiguraatioiden versioiden määrän (**Yhteenveto**-sekvenssi).

    ![ER-muodon suunnittelutoiminnon sivu](./media/GER-JoinDS-FormatReview.PNG)

    Tietolähteitä **Tiedot** ja **Yhteenveto** käytetään täyttämään konfiguraatioversion tiedot luodussa tiedostossa:

    - Tietomallin **Set1** tietoja käytetään, kun valitset **Ei** **Valitsija**-tietolähteen osalta käyttäjän valintaikkunasivulla ER-muodon suorittamisen aikana.
    - Tietomallin **Set2** tietoja käytetään, kun valitset **Kyllä** **Valitsija**-tietolähteen osalta käyttäjän valintaikkunasivulla ER-muodon suorittamisen aikana.

    ![ER-muodon suunnittelutoiminnon sivu](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  Valitse **Suorita**.
10. Valitse valintaikkunasivulla **Ei** kentässä **Käytä JOIN-tietolähdettä**.
11. Valitse **OK**.
12. Tarkista luotu tiedosto.

    ![ER käyttäjän valintaikkunasivu](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>ER-muodon suorituksen jäljityksen analysointi

1.  Valitse Financen tai RCS:n ensimmäisessä istunnussa **Suunnittelutoiminto**.
2.  Valitse **Suorituskyvyn jäljitys**.
3.  Valitse **Suorituskyvyn jäljitys** -ruudukossa viimeisimmän sellaisen ER-muodon suorituksen jäljityksen ylin tietue, joka käytti nykyistä mallimäärityskomponenttia.
4.  Valitse **OK**.

    Huomaa, että saat suoritustilastoista tietoa kaksinkertaisista sovellustaulukkojen kutsuista:

    - **ERSolutionTable**-taulukon kutsumäärä vastaa konfiguraatioversioiden tietuiden määrää **ERSolutionVersionTable**-taulukossa, ja tällaisten kutsujen määrän vähentämisellä voidaan parantaa suorituskykyä.
    - **ERVendorTable**-taulukon kutsumäärä on kaksinkertainen niihin konfiguraatioversioiden tietueiden määrään nähden, jotka havaittiin **ERSolutionVersionTable**-taulukossa, ja myös tällaisten kutsujen määrän vähentämisellä voidaan parantaa suorituskykyä.

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-Set1Run2.PNG)

5.  Sulje sivu.

### <a name="execute-er-format"></a>Suorita ER-muoto

1.  Siirry siihen verkkoselaimesi välilehteen, joka sisältää toisen Finance- tai RCS-istunnon.
2.  Valitse **Suorita**.
3.  Valitse valintaikkunasivulla **Kyllä** kentässä **Käytä JOIN-tietolähdettä**.
4.  Valitse **OK**.
5.  Tarkista luotu tiedosto.

    ![ER käyttäjän valintaikkunasivu](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> ER-muodon suorituksen jäljityksen analysointi

1.  Valitse Financen tai RCS:n ensimmäisessä istunnussa **Suunnittelutoiminto**.
2.  Valitse **Suorituskyvyn jäljitys**.
3.  Valitse **Suorituskyvyn jäljitys** -ruudukossa ylin tietue, joka edustaa viimeisimmän selalisen ER-muodon suorituksen jäljitystä, joka käytti nykyistä mallimäärityskomponenttia.
4.  Valitse **OK**.

    Huomaa, että suoritustilastoista ilmenee seuraavaa:

    - Sovellustietokantaa on kutsuttu kerran, jotta saadaan tietueita taulukoista **ERVendorTable**, **ERSolutionTable** ja **ERSolutionVersionTable** pakollisia kenttiä varten.

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-Set2Run2.PNG)

    - Sovellustietokantaa on kutsuttu kerran konfiguraatioversioiden laskemiseksi käyttämällä liitoksia, jotka konfiguroitiin **Tiedot**-tietolähteessä.

    ![ER-mallimäärityksen suunnittelun sivu](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)
