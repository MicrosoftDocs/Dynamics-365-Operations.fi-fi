---
title: Käytä ER-mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista
description: Tässä ohjeaiheessa kerrotaan JOIN-tietolähteiden käytöstä sähköisessä raportoinnissa (ER).
author: NickSelin
ms.date: 04/26/2021
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
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: be5646eaf395310c8b34586ef1274a41b5b97029
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944703"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a>Käytä sähköisen raportoinnin (ER) mallimäärityksissä JOIN-tietolähteitä saadaksesi tietoja useista sovellustaulukoista

[!include[banner](../includes/banner.md)]

Kun määrität sähköisen raportoinnin (ER) mallimäärityksiä tai muotoja, voit [lisätä](#review) tarvittavia **Liitä**-tyypin tietolähteitä. Suunnitteluvaiheessa **Liitä**-tietolähde määritetään useiden tietolähteiden sarjaksi, ja jokainen tietolähde palauttaa tietueluettelon. Ensimmäistä tietolähdettä lukuun ottamatta sinulle on määritettävä jokaiselle niistä tarvittavat ehdot nykyisen ja aiempien tietolähteiden tietueiden liittämiselle. Suorituksen aikana määritetty **Liitä**-tyypin tietolähde [palauttaa](#executeERformat) yksittäisen yhteenliitetyn luettelon tietueista, jotka sisältävät kenttiä sisäkkäisten tietolähteiden tietueista.

Tällä hetkellä tuetaan seuraavia liitostyyppejä:

- Ulkoliitos (vasen):
    - Liittää kaikki määritettyjä ehtoja vastaavat ensimmäisen (vasemmanpuoleisen) tietolähteen tietueet yhteen ja lisää sitten kaikki määritettyjä ehtoja vastaavat toisen (oikeanpuoleinen) tietolähteen tietueet.
- Sisäliitos (oikea):
    - Liittää yhteen vain määritettyjä ehtoja vastaavat ensimmäisen (vasemmanpuoleisen) tietolähteen tietueet yhteen ja vain määritettyjä ehtoja vastaavat toisen (oikean) tietolähteen tietueet yhteen.

Kun määritetyn **Liitä**-tietolähteen kaikki tietolähteet ovat tyyppiä **Taulukkotietueet** Liitos-tietolähde voidaan [suorittaa tietokantatasolla](#analyze) käyttäen yksittäistä SQL-lausetta. Tämä lauseke vähentää tietokantakyselyjen määrää ja parantaa siten mallin yhdistämismäärityksen suorituskykyä. Muussa tapauksessa **Liitä**-tietolähde suoritetaan muistissa.

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

Etukäteen on myös ladattava ja tallennettava seuraavat ER-mallimääritystiedostot:

| **Sisällön kuvaus**  | **Tiedostonimi**   |
|--------------------------|-----------------|
| Esimerkeissä tietolähteenä käytettävä **ER-tietomalli**-konfiguraatiotiedosto.| [Model to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/5/c/1/5c1d8a57-6ebd-425b-bc5d-c71dde92c6af/ModeltolearnJOINdatasources.version.1.xml) |
| Esimerkissä käytettävä **ER-mallimääritys**-konfiguraatiotiedosto, joka soveltaa ER-tietomallia esimerkkeihin. | [Mapping to learn JOIN data sources.version.1.1.xml](https://user-images.githubusercontent.com/19827601/115923048-86b10400-a432-11eb-9e57-c37a02effcb4.png)|
| Esimerkissä käytettävä **ER-muoto**-konfiguraatiotiedosto. Tässä tiedostossa kuvataan tiedot, joilla täytetään esimerkkien ER-muotokomponentti. | [Format to learn JOIN data sources.version.1.1.xml](https://download.microsoft.com/download/f/f/8/ff8f1b48-14d0-4c73-9145-bcdf8b5265bc/FormattolearnJOINdatasources.version.1.1.xml) |

### <a name="activate-a-configurations-provider"></a>Aktivoi konfiguraatiolähde

1. Käytä joko Finance- tai RCS-sovellusta verkkoselaimesi ensimmäisessä istunnossa.
2. Siirry kohtaan **Organisaation hallinto \> Työtilat \> Sähköinen raportointi**.
3. Varmita **Lokalisointimääritykset**-sivun osassa **Määritysten tarjoajat**, että määritysten tarjoaja esimerkkiyritykselle [Litware, Inc.](http://www.litware.com) on luettelossa ja merkitty **Aktiiviseksi**. Jos konfiguraation lähde ei ole näkyvissä, suorita menettelyn [Konfiguraation lähteen luominen ja sen merkitseminen aktiiviseksi](tasks/er-configuration-provider-mark-it-active-2016-11.md) vaiheet.

    ![Sähköisen raportoinnin työtila](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a>ER-mallikonfiguraatiotiedostojen tuonti

1. Valitse **Raportointikonfiguraatiot**.
2. Tuo ER-tietomallin konfiguraatiotiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Model to learn JOIN data sources.version.1.1.xml**.
    4. Valitse **OK**.
3. Tuo ER-mallin yhdistämismäärityksen määritystiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Mapping to learn JOIN data sources.version.1.1.xm**.
    4. Valitse **OK**.
4. Tuo ER-muotokonfiguraatiotiedosto.
    1. Valitse **Vaihto**.
    2. Valitse **Lataa XML-tiedostosta**.
    3. Valitse **Selaa** löytääksesi tiedoston **Format to learn JOIN data sources.version.1.1.xm**.
    4. Valitse **OK**.
5. Laajenna konfiguraatioiden puurakenteessa nimike **Mallinnus JOIN-tietolähteiden selvittämiseksi** sekä muut mallinimikkeet (jos käytettävissä).
6. Pane merkille puurakenteen ER-konfiguraatioiden luettelo sekä **Versiot**-pikavälilehden versiotiedot. Niitä käytetään malliraporttisi tietolähteenä.

    ![Sähköisen raportoinnin konfiguraatiosivu](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a>Suorituksen jäljitysasetusten käyttöönotto

1. Valitse **KONFIGURAATIOT**.
2. Valitse **Käyttäjän parametrit**.
3. Määritä suorituksen jäljitysparametrit alla esitetyn näyttökuvan mukaisesti.

    ![Sähköisen raportoinnin käyttäjän parametrien sivu](./media/GER-JoinDS-Parameters.PNG)

    Kun nämä parametrit ovat käytössä, suorituksen jäljitys luodaan jokaiselle tuodun ER-muototiedoston suoritukselle. Luodun suorituksen jäljityksen tietojen avulla voit analysoida ER-muodon ja ER-mallin yhdistämismäärityksen komponenttien suorituksen. Lisätietoja sähköisen raportoinnin suorituksen jäljitystoiminnosta saat sivulta [Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md).

### <a name="review-er-model-mapping-part-1"></a>ER-mallimäärityksen tarkistus (osa 1)

Tarkista ER-mallin yhdistämismäärityskomponentin asetukset. Komponentti on määritetty käyttämään ER-konfiguraatioiden mallien tietoja, konfiguraatioiden ja konfiguraatiolähteiden tietoja käyttämättä **Liitä**-tyypin tietolähteitä.

1. Valitse konfiguraatio **Määritys JOIN-tietolähteiden selvittämiseksi**.
2. Avaa määritysluettelo valitsemalla **Suunnittelutoiminto**.
3. Tarkista määritystiedot valitsemalla **Suunnittelutoiminto**.
4. Valitse **Näytä tiedot**.
5. Laajenna konfiguraatioiden puurakenteessa tietomallinimikkeet **Set1** ja **Set1.Details**:

    1. Sitova **Details: Record list = Versions** ilmaisee, että nimike **Set1.Details** on sidottu **Versiot**-tietolähteeseen, joka palauttaa **ERSolutionVersionTable**-taulukon tietueita. Kukin tämän taulukon tietue edustaa yksittäistä ER-konfiguraation versiota. Tämän taulukon sisältö esitetään **Versiot**-pikavälilehdessä **Konfiguraatiot**-sivulla.
    2. Sitova **ConfigurationVersion: String = @.PublicVersionNumber** tarkoittaa, että kunkin ER-konfiguraation version julkisen version arvo perustuu **PublicVersionNumber**-kentän arvoon taulukossa **ERSolutionVersionTable** ja että se sijoitetaan nimikkeeseen **ConfigurationVersion**.
    3. Sitova **ConfigurationTitle: String = @.'>Relations'.Solution.Name** ilmaisee, että ER-konfiguraation nimi perustuu **Nimi**-kenttään taulukossa **ERSolutionTable**, joka vuorostaan perustuu monta yhteen -suhteeseen (**'>Relations'**) taulukkojen **ERSolutionVersionTable** ja **ERSolutionTable** välillä. Kulloisenkin sovellusesiintymän ER-konfiguraatioiden nimet esitetään **Konfiguraatiot**-sivun konfiguraatioiden puurakenteessa.
    4. Sitova **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** tarkoittaa, että kulloisenkin konfiguraation omistava konfiguraatiolähde perustuu **Nimi**-kenttään taulukossa **ERVendorTable**, joka vuorostaan perustuu monta yhteen -suhteeseen taulukkojen **ERSolutionTable** ja **ERVendorTable** välillä. ER-konfiguraatiolähteiden nimet esitetään konfiguraatioiden puurakenteessa **Konfiguraatiot**-sivun jokaisessa konfiguraation sivuotsikossa. Koko luettelo ER-konfiguraatiolähteistä esitetään taulukkosivulla **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraation lähde**.

    ![ER-mallimäärityksen suunnittelun sivu, luettelo sidotun tietomallin nimikkeistä](./media/GER-JoinDS-Set1Review.PNG)

6. Laajenna tietomallinimike **Set1.Summary** konfiguraatioiden puurakenteessa:

    1. Sitova **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** ilmaisee, että nimike **Set1.Summary.VersionsNumber** on sidottu **GroupBy**-tyypin **VersionsSummary**-tietolähteen koostekenttään **VersionsNumber**, joka määritettiin palauttamaan **ERSolutionVersionTable**-taulukon tietuemäärä **Versiot**-tietolähteen kautta.

    ![Ryhmittelyparametrien muokkaussivu](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. Sulje sivu.

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> ER-mallimäärityksen tarkistus (osa 2)

Tarkista ER-mallin yhdistämismäärityskomponentin asetukset. Komponentti on määritetty käyttämään ER-konfiguraatioiden mallien tietoja, konfiguraatioiden ja konfiguraatiolähteiden tietoja käyttäen **Liitä**-tyypin tietolähdettä.

1. Laajenna konfiguraatioiden puurakenteessa tietomallinimikkeet **Set2** ja **Set2.Details**. Sitova **Details: Record list = Details** ilmaisee, että nimike **Set2.Details** on sidottu **Tiedot**-tietolähteeseen, joka on määritetty **Liitä**-tyypin tietolähteeksi.

    ![ER-mallimäärityksen suunnittelun sivu, jossa näkyy laajennettu Set2:Record-tietomallin nimikkeet](./media/GER-JoinDS-Set2Review.PNG)

    **Liitä**-tietolähde voidaan lisätä valitsemalla **Toiminnot\Liitä**-tietolähde:

    ![ER-mallimäärityksen suunnittelun sivu, Liitä tietolähteen tyyppi](./media/GER-JoinDS-AddJoinDS.PNG)

2. Valitse **Tiedot**-tietolähde.
3. Valitse **Muokkaa** **Tietolähteet**-ruudussa.
4. Valitse **Muokkaa liitä**.
5. Valitse **Näytä tiedot**.

    ![JOIN-tietolähteen parametrisivu](./media/GER-JoinDS-JoinDSEditor.PNG)

    Tätä sivua käytetään **Liitä**-tyypin pakollisen tietolähteen suunnittelemiseen. Suorituksen aikana tämä tietolähde luo yksittäisen yhteenliitetetyn tietueluettelon **Liitettyjen luettelo** -ruudukon tietolähteistä. Tietueiden liitos alkaa tietolähteestä **ConfigurationProviders**, joka on ruudukossa ensimmäisenä (**Tyyppi**-sarake on tyhjänä sen osalta). Muiden tietolähteiden tietueet liitetään sen jälkeen päätietolähteen tietueisiin kyseisen ruudukon mukaisessa järjestyksessä. Jokainen liitettävä tietolähde on määritettävä kohdetietolähteen alaiseksi tietolähteeksi (`1Versions`-tietolähde on tietolähteen `1Configurations` alainen; `1Configurations`-tietolähde on tietolähteen **ConfigurationProviders** alainen). Kunkin määritetyn tietolähteen on sisällettävä liitoksen ehdot. Tässä **Liitä**-tyypissä määritetään seuraavat liitokset:

    - Kuhunkin tietolähteen **ConfigurationProviders** (johon viitataan **ERVendorTable**-taulukossa) liitetään vain tietolähteen **1Configurations** (johon viitataan **ERSolutionTable**-taulukossa) tietueita, joilla on sama arvo kentissä **SolutionVendor** ja **RecId**. Tähän liitokseen käytetään **Sisäliitos**-tyyppiä sekä seuraavia ehtoja tietueiden täsmäämiseen:

    FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)

    - Kuhunkin tietolähteen **1Configurations** (johon viitataan **ERSolutionTable**-taulukossa) liitetään vain tietolähteen **1Versions** (johon viitataan **ERSolutionVersionTable**-taulukossa) tietueita, joilla on sama arvo kentissä **Solution** ja **RecId**. Tähän liitokseen käytetään **Sisäliitos**-tyyppiä sekä seuraavia ehtoja tietueiden täsmäämiseen:

    FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)

    - **Suorita**-asetuksen arvoksi määritetään **Kysely**, mikä tarkoittaa, että tämä liitoksen tietolähde suoritetaan suorituksen aikana tietokannan tasolla suoran SQL-kutsun muodossa.

    Voit määrittää sovellustaulukkoja edustavien tietolähteiden tietueiden liitosten yhteydessä liitosehtoja käyttäen kenttäpareja, jotka eivät kuvaa olemassa olevia näiden taulukkojen välisiä AOT-suhteita. Myös tällainen liitos voidaan määrittää suoritettavaksi tietokantatasolla.

6. Sulje sivu.
7. Valitse **Peruuta**.
8. Laajenna tietomallinimike **Set2.Summary** konfiguraatioiden puurakenteessa:

    - Sitova **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** ilmaisee, että nimike **Set2.Summary.VersionsNumber** on sidottu **GroupBy**-tyypin **DetailsSummary**-tietolähteen koostekenttään **VersionsNumber**, joka määritettiin palauttamaan **Liitä**-tyypin **Tiedot**-tietolähteen liitettyjen tietueiden määrä.
    - **Suorita**-sijaintiasetuksen arvoksi määritetään **Kysely**, mikä tarkoittaa, että tämä **GroupBy**-tietolähde suoritetaan suorituksen aikana tietokannan tasolla suoran SQL-kutsun muodossa. Tämä toiminnallisuus on mahdollista, koska perustietolähde **Tiedot**, jonka tyyppi on **Liitä**, on määritetty suoritettavaksi tietokannan tasolla.

    ![GROUPBY-tietolähteen parametrisivu](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. Sulje sivu.
10. Valitse **Peruuta**.

### <a name="execute-er-format"></a><a name="executeERformat"></a> Suorita ER-muoto

1. Access Finance tai RCS on verkkoselaimesi toinen istunto, jossa käytetään samoja tunnistetietoja ja yritystä kuin ensimmäisessä istunnossa.
2. Siirry kohtaan **Organisaation hallinto \> Sähköinen raportointi \> Konfiguraatiot**.
3. Laajenna konfiguraatio **Mallinnus JOIN-tietolähteiden selvittämiseksi** configuration.
4. Valitse konfiguraatio **Muotoilu JOIN-tietolähteiden selvittämiseksi**.
5. Valitse **Suunnittelu**.
6. Valitse **Näytä tiedot**.
7. Valitse **Määritys**.
8. Valitse **Laajenna/kutista**.

    Tämä muotoilu on suunnitelty täyttämään luotava tekstitiedosto uudella rivillä kutakin ER-konfiguraation versiota kohden (**Versio**-sekvenssiä). Kukin luotu rivi sisältää sen konfiguraatiolähteen nimen, joka omistaa kulloisenkin konfiguraation, konfiguraation nimen sekä konfiguraation version puolipistein eroteltuna. Luodun tiedoston viimeinen rivi sisältää havaittujen ER-konfiguraatioiden versioiden määrän (**Yhteenveto**-sekvenssi).

    ![ER-muodon suunnittelutoiminnon sivu, Muoto-välilehti](./media/GER-JoinDS-FormatReview.PNG)

    Tietolähteitä **Tiedot** ja **Yhteenveto** käytetään täyttämään konfiguraatioversion tiedot luodussa tiedostossa:

    - Tietomallin **Set1** tietoja käytetään, kun valitset **Ei** **Valitsija**-tietolähteen osalta käyttäjän valintaikkunasivulla ER-muodon suorittamisen aikana.
    - Tietomallin **Set2** tietoja käytetään, kun valitset **Kyllä** **Valitsija**-tietolähteen osalta käyttäjän valintaikkunasivulla ER-muodon suorittamisen aikana.

    ![ER-muodon suunnittelutoiminnon sivu, Määritys-välilehti](./media/GER-JoinDS-FormatMappingReview.PNG)

9. Valitse **Suorita**.
10. Valitse valintaikkunasivulla **Ei** kentässä **Käytä JOIN-tietolähdettä**.
11. Valitse **OK**.
12. Tarkista luotu tiedosto.

    ![Sähköisten raporttiparametrien muodostettu tiedosto, joka ei käytä JOIN-tietolähdettä](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a>ER-muodon suorituksen jäljityksen analysointi

1. Valitse Financen tai RCS:n ensimmäisessä istunnussa **Suunnittelutoiminto**.
2. Valitse **Suorituskyvyn jäljitys**.
3. Valitse **Suorituskyvyn jäljitys** -ruudukossa viimeisimmän sellaisen ER-muodon suorituksen jäljityksen ylin tietue, joka käytti nykyistä mallimäärityskomponenttia.
4. Valitse **OK**.

    Saat suoritustilastoista tietoa kaksinkertaisista sovellustaulukkojen kutsuista:

    - **ERSolutionTable**-taulukon kutsumäärä vastaa konfiguraatioversioiden tietuiden määrää **ERSolutionVersionTable**-taulukossa, ja tällaisten kutsujen määrän vähentämisellä voidaan parantaa suorituskykyä.
    - **ERVendorTable**-taulukon kutsumäärä on kaksinkertainen niihin konfiguraatioversioiden tietueiden määrään nähden, jotka havaittiin **ERSolutionVersionTable**-taulukossa, ja myös tällaisten kutsujen määrän vähentämisellä voidaan parantaa suorituskykyä.

    ![ER-mallin yhdistämismäärityksen suunnitteluohjelman sivun suoritustilastot](./media/GER-JoinDS-Set1Run2.PNG)

5. Sulje sivu.

### <a name="execute-er-format"></a>Suorita ER-muoto

1. Siirry siihen verkkoselaimesi välilehteen, joka sisältää toisen Finance- tai RCS-istunnon.
2. Valitse **Suorita**.
3. Valitse valintaikkunasivulla **Kyllä** kentässä **Käytä JOIN-tietolähdettä**.
4. Valitse **OK**.
5. Tarkista luotu tiedosto.

    ![Sähköisten raporttiparametrien muodostettu tiedosto, joka käyttää JOIN-tietolähdettä](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> ER-muodon suorituksen jäljityksen analysointi

1. Valitse Financen tai RCS:n ensimmäisessä istunnussa **Suunnittelutoiminto**.
2. Valitse **Suorituskyvyn jäljitys**.
3. Valitse **Suorituskyvyn jäljitys** -ruudukossa ylin tietue, joka edustaa viimeisimmän selalisen ER-muodon suorituksen jäljitystä, joka käytti nykyistä mallimäärityskomponenttia.
4. Valitse **OK**.

    Tilastotiedot kertovat seuraavista:

    - Sovellustietokantaa on kutsuttu kerran, jotta saadaan tietueita taulukoista **ERVendorTable**, **ERSolutionTable** ja **ERSolutionVersionTable** pakollisia kenttiä varten.

    ![ER-mallin yhdistämismäärityksen suunnitteluohjelman sivun suorituskyvyn tilastotiedot](./media/GER-JoinDS-Set2Run2.PNG)

    - Sovellustietokantaa on kutsuttu kerran konfiguraatioversioiden laskemiseksi käyttämällä liitoksia, jotka konfiguroitiin **Tiedot**-tietolähteessä.

    ![ER-mallin yhdistämismäärityksen suunnitteluohjelman sivu, jossa näkyvät sovellustietokannan kutsut](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a>Rajoitukset

Kuten tämän ohjeaiheen esimerkistä voi nähdä, **LIITOS**-tietolähde voidaan muodostaa useista tietolähteistä, jotka kuvaavat niitä tietueissa olevia tietoja, jotka on lopulta yhdistettävä. Voit määrittää nämä tietolähteet valmiin ER-[SUODATIN](er-functions-list-filter.md)-toiminnon avulla. Kun määrität tietolähteen niin, että sitä kutsutaan **LIITOS**-tietolähteen ulkopuolelle, voit käyttää yrityksen alueita tietojen valinnan ehdon osana. **LIITOS**-tietolähteen ensimmäinen toteutus ei tue tämäntyyppisiä tietolähteitä. Jos esimerkiksi soitat [SUODATIN](er-functions-list-filter.md)-perusteisen tietolähteen suoritusalueella olevaan suodattimeen perustuvaan tietolähteeseen, näyttöön tulee poikkeus, **LIITOS**-tietolähde, jos kutsuttu tietolähde sisältää yritysalueita osana tietojen valitsemisen ehtoa.

Microsoft Dynamics 365 Finance -version 10.0.12 (elokuu 2020) avulla voit käyttää yrityksen alueita, kun haluat määrittää tietojen valitsemisen ehdoksi [SUODATUKSEEN](er-functions-list-filter.md) perustuvissa tietolähteissä, joita kutsutaan **LIITOS**-tietolähteen suoritusalueella. Sovellus [kysely](../dev-ref/xpp-library-objects.md#query-object-model)-muodostimen rajoitusten vuoksi yritysalueita tuetaan vain **LIITOS**-tietolähteen ensimmäisellä tietolähteellä.

### <a name="example"></a>Esimerkki

Sinun on esimerkiksi tehtävä sovellustietokantaan yksi puhelu, jotta saat luettelon useiden yritysten ulkomaankauppatapahtumista sekä kyseisissä tapahtumissa viitattavan varastonimikkeen yksityiskohdista.

Tässä tapauksessa voit määrittää seuraavat artefaktit ER-mallikartoitukseen:

- **Intrastat**-juuritietolähde, joka edustaa **Intrastat**-taulua.
- **Nimikkeet**-juuritietolähde, joka edustaa **InventTable**-taulua.
- **Yritykset**-juuritietolähde, joka palauttaa yritysten luettelon (tässä esimerkissä **DEMF** ja **GBSI**), jossa tapahtumia on käytettävä. Yrityskoodi on käytettävissä **Companies.Code**-kentässä.
- **X1**-juuritietolähde, jolla on lauseke `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`. Tämä lauseke sisältää yritysalueiden määritelmän osana tietojen valitsemisen ehtoa `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.
- **X2**-tietolähde **X1**-tietolähteen sisäkkäisenä nimikkeenä. Se sisältää lausekkeen `FILTER (Items, Items.ItemId = X1.ItemId)`.

Lopuksi voit määrittää **LIITOS**-tietolähteen, jossa **X1** on ensimmäinen tietolähde, ja **X2** on toinen tietolähde. Voit määrittää **Kyselyn** **Suorita**-vaihtoehdoksi, jos haluat suorittaa tämän tietolähteen tietokantatasolla suorana SQL-kutsuna.

Kun konfiguroitu tietolähde suoritetaan, kun ER -suoritus [jäljitetään](trace-execution-er-troubleshoot-perf.md), seuraava ilmoitus näkyy ER-mallin kartoituksen suunnittelussa osana ER-suorituskykyjälkeä.

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> Virhe ilmenee, jos suoritat **LIITOS**-tietolähteen, joka on määritetty siten, että se sisältää tietojenvalintaehtoja, joiden tietolähteiden **LIITOS**-tietolähteitä on suoritettu.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)

[Sähköisen raportoinnin muodon suorittamisen seuraaminen suorituskykyyn liittyvien ongelmien ratkaisemiseksi](trace-execution-er-troubleshoot-perf.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
