---
title: Organisaatiohierarkian suunnitteleminen
description: Ennen kuin määrität organisaation ja organisaatiohierarkiat, varmista, että suunnittelet miten liiketoimintasi mallinnetaan.
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c779b5948370444b0b474568bb63b347c4a0831
ms.sourcegitcommit: 79621e667cd7f48ba3bdbf2731f6f33d8e9f57f6
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/10/2021
ms.locfileid: "5154406"
---
# <a name="plan-your-organizational-hierarchy"></a>Organisaatiohierarkian suunnitteleminen

[!include [banner](../includes/banner.md)]

Ennen kuin määrität organisaation ja organisaatiohierarkiat, varmista, että suunnittelet liiketoimintasi mallinnuksen. Organisaatiomallilla on huomattava vaikutus toteutukseen ja liiketoimintaprosesseihin.

Organisaatiohierarkiat edustavat liiketoiminnan muodostavien organisaatioiden välisiä suhteita. Tämän vuoksi tärkein harkittava asia organisaatioita mallinnettaessa on liiketoiminnan rakenne. Suosittelemme, että määrittelet organisaatiorakenteet toiminnallisten alueiden, kuten taloushallinto ja kirjanpito, henkilöstöhallinto, operatiiviset toiminnot, ostotoiminnot, sekä myynti ja markkinointi, johtajilta ja päälliköiltä saamasi palautteen perusteella.

Kun suunnittelet hierarkiat, on myös tärkeää ottaa huomioon suhde organisaatiohierarkian että taloushallinnon dimensioiden välillä. Voit määrittää useita organisaation hierarkioita edustamaan yrityksesi eri näkymiä. Taloushallinnon dimensioiden avulla voit luoda raportteja näistä näkymistä. Kumppanisi käyttäminen luomaan hierarkiat, jotka kohdistuvat sekä organisaation että lakisääteisen raportoinnin tarpeisiin.

> [!NOTE]
> Voit käyttää taloushallinnon dimensioita edustamaan yrityksiä ilman, että luot yrityksiä. Taloushallinnon dimensioita ei ole kuitenkaan suunniteltu vastaamaan yritysten toiminnallisiin tai liiketaloudellisiin tarpeisiin. Yksiköiden välisen kirjanpidon toiminnallisuus on suunniteltu käsittelemään vain jokaisen tapahtuman luomat kirjanpitomerkinnät.

> [!IMPORTANT]
> Älä määritä pelkästään tämän artikkelin avulla, miten organisaatioita mallinnetaan. Tämä dokumentaatio on ohje. Voit pyytää lisäohjeita yhteistyökumppaniltasi. Kumppanisi on hankkinut kokemusta eri toimialoilla ja erilaisten asiakkaiden kanssa.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Valitse, mallinnetaanko sisäiset organisaatiot yrityksinä vai toimintayksiköinä

Sinulla on oltava vähintään yksi yritys yrityksellesi. Yritys voi solmia lainmukaisia sopimuksia ja jolta edellytetään suorituskykyä kuvaavien raporttien laatimista.

Yrityksiä voidaan käyttää tapahtumasidonnaiseen liiketoimintaan tai konsolidointia varten. Tämä tarkoittaa, että Finance and Operationsissa oleva yksikkö ei välttämättä vastaa todellista yksikköä yrityksessäsi. Esimerkiksi tapahtumiin osallistuva yritys voi omistaa tytäryhtiöitä. Tässä skenaariossa tapahtumat vaativat yrityksen ja tytäryhtiöiden saldojen ja tulosten konsolidointiin vaaditaan virtuaaliyritys.

Liiketoimintasi sisäiset organisaatiot, kuten aluekohtaiset toimistot, voidaan kuvata lisäyrityksinä tai pääyrityksen toimintayksiköinä. Toimintayksikön ei tarvitse olla oikeudellisesti määritetty organisaatio. Toimintayksiköitä käytetään hallitsemaan liiketoiminnan taloudellisia resursseja ja operatiivisia prosesseja. Esimerkiksi osastot ja kustannuspaikat ovat toimintayksiköitä.

Eräät toiminnot toimivat eri tavalla riippuen siitä, onko organisaatio yritys vai toimintayksikkö. Harkitse kuvattua toiminnallisuutta tarkkaan päätöksiä tehdessäsi.

### <a name="master-data"></a>Päätiedot

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Eräät päätiedot, kuten asiakkaat, maksuehdot, veroviranomaiset ja toimipaikkakohtainen varastojärjestys, tulee määrittää jokaiselle yritykselle. Eräät perustiedot, kuten käyttäjät, tuotteet ja useimmat henkilöstöhallinnon tiedot, jaetaan kaikkien yritysten välillä.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Päätiedot jaetaan toimintayksikköjen kesken.

### <a name="module-parameters"></a>Moduulin parametrit

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Moduulien, kuten myyntireskontran, ostoreskontran ja maksuliikenteen hallinnan parametrit on määritettävä oikeushenkilöä kohden. Yritysten moduulien asetukset ovat erillisiä, joten kukin tytäryhtiön voi noudattaa paikallisia lakisääteisiä vaatimuksia ja yrityskäytäntöjä. Esimerkiksi ammattilaispalveluja tarjoavalla yrityksellä ja tuotantoyrityksellä saattaa olla erilaiset moduuliparametrit, vaikka ne raportoivat samalle emoyhtiölle.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Moduulin parametrit jaetaan toimintayksiköiden kesken.

### <a name="data-security"></a>Tietoturva

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Suurin osa tiedoista suojataan automaattisesti yrityksen tunnuksen avulla. Yrityksen tunnus on yksilöivä tunnus yritykseen liitettäville tiedoille. Yritys voidaan liittää vain yhteen oikeushenkilöön, ja oikeushenkilö voi liittyä vain yhteen yritykseen. Käyttäjillä on pääsy vain niiden yritysten tietoihin, joihin heillä on käyttöoikeus. Sinun ei tarvitse mukauttaa tietojen suojaamiseksi yrityksen tunnuksella.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Tiedot voidaan suojata toimintayksikkökohtaisesti luomalla mukautettuja tietoturvakäytäntöjä. Tietoturvakäytännöillä rajoitetaan tietojen käyttöä. Oletetaan esimerkiksi, että käyttäjä voi luoda ostotilauksia vain tietyssä liiketoimintayksikössä. Tietoturvakäytäntöjen avulla voidaan estää käyttäjiä käyttämästä ostotilauksen tietoja muista toimintayksiköistä. Tapahtumien määrä ja suojauskäytäntöjen lukumäärä voivat vaikuttaa suorituskykyyn. Suojauskäytännöt suunnitellessasi pidä mielessä suorituskykyä.

### <a name="ledgers"></a>Kirjanpidot

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Jokaisella yrityksellä on oltava kirjanpito, joka tarjoaa tilikartan, kirjanpitovaluutan, raportointivaluutan ja kirjanpidon vuosikalenterin. Taseen voi luoda ainoastaan yritykselle. Useampi kuin yksi yritys voi käyttää päätilejä, dimensioita, tilirakenteita, tilikarttoja ja tilisääntöjä.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Toimintayksiköllä ei voi olla omia kirjanpitotietoja. Jos sisäiset organisaatiosi eivät edellytä yksilöivää kirjanpitoa,voit mallintaa ne liiketoiminnan yksiköiksi. Kirjanpitotiedot määritetään hierarkian ylätason yritykselle. Tuloilmoitukset voidaan luoda yrityksen toimintayksiköille tai ylemmän tason yritykselle.

### <a name="fiscal-calendars"></a>Kirjanpidon kalenterit

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Jokaisella yrityksellä on oma kirjanpidon vuosikalenteri. Jos sisäisten organisaatioidesi on käytettävä eri tilikautta ja eri tilikalentereita, on organisaatiot mallinnettava yrityksinä.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Toimintayksiköiden on jaettava kirjanpidon vuosikalenteri. Jos sisäiset organisaatiosi voivat käyttää samaa tilikautta ja tilikalentereita, voit mallintaa organisaatiot liiketoiminnan yksiköiksi.

### <a name="consolidation"></a>Konsolidointi

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Sinun on konsolidoitava aluekohtaisten toimipaikkojen taloudelliset tulokset yksityiskohtaiseen konsolidoituun yritykseen, jotta voit valmistella raportit.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Konsolidointi ei tarvita, koska tiedot on jo jaettu eri yksiköiden kesken.

### <a name="centralized-payments"></a>Keskitetyt maksut

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Keskitetyt maksut on määritettävä niin, että laskut kaikille alatason yrityksille voidaan maksaa yhden ylemmän tason yrityksen kautta.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Keskitetyt maksut eivät ole pakollisia, koska kaikki laskut kirjataan yhdelle yritykselle.

### <a name="intercompany-transactions"></a>Konsernin sisäiset tapahtumat

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Konsernin sisäiset myyntitilaukset, ostotilaukset, maksut tai vastaanotot voidaan kohdistaa toisiinsa. Sinun ei tarvitse käyttää kirjauskansion tositteita. Voit tarkastella konsernin sisäisiä tapahtumia osakirjanpitotasolla (myyntireskontra, ostoreskontra). Seuraavissa esimerkeissä havainnollistetaan, kuinka konsernin sisäiset tapahtumat käsitellään.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Esimerkki 1: Pääkonttori toimittaa palveluja alueellisille toimistoille, ja pääkonttorin on veloitettava alueellisia toimistoja näistä palveluista.

Jos mallinnat aluekohtaiset toimistot yrityksinä, sinulla on seuraavat vaihtoehdot:

- Pääkonttori luo kirjauskansioviennin veloittaakseen aluekohtaisia toimistoja kulun takia. Tapahtumat eivät voi erääntyä.
- Pääkonttori lähettää palvelujen ostotilauksen alueelliselle toimistolle. Myyntitilaus luodaan automaattisesti yritykselle konsernin aluetoimistolle konsernin sisäisten alikirjanpidon tapahtumien kanssa.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Esimerkki 2: Pääkonttori hankkii alueelliselle toimistolle toimitettavan palvelun ja maksaa siitä.

Jos mallinnat aluekohtaiset toimistot yrityksinä, sinulla on seuraavat vaihtoehdot:

- Lasku ja maksu ovat pääkonttorin säännösten vaatimusten mukaisia. Pääkonttorit voivat luoda kirjauskansioviennin veloittaakseen aluekohtaisia toimistoja kulun takia. Tapahtumat eivät voi erääntyä.
- Lasku ja maksu ovat pääkonttorin säännösten vaatimusten mukaisia. Pääkonttorit voivat luoda konsernin sisäisen osakirjanpitotapahtuman.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Toimintayksiköiden välisiä konsernin sisäisiä tapahtumia tuetaan vain kirjaustositteiden kautta. Toimintayksikkö ei voi laatia tai vastaanottaa ostotilausta, myyntitilausta tai laskua toiselta saman yrityksen toimintayksiköltä. Et voi tarkastella konsernin sisäisiä tapahtumia osakirjanpitotasolla (myyntireskontra, ostoreskontra). Seuraavissa esimerkeissä havainnollistetaan, kuinka konsernin sisäiset tapahtumat käsitellään.

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Esimerkki 1: Pääkonttori toimittaa palveluja alueellisille toimistoille, ja pääkonttorin on veloitettava alueellisia toimistoja näistä palveluista.

Jos mallinnat aluekohtaisen toimiston liiketoiminnan yksikkönä, pääkonttori syöttää veloitettavan kulun ja koodit aluekohtaiselle toimipaikalle.

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Esimerkki 2: Pääkonttori hankkii alueelliselle toimistolle toimitettavan palvelun ja maksaa siitä.

Jos mallinnat aluekohtaisen toimiston liiketoiminnan yksikkönä, lasku ja maksu seuraavat pääkonttorin säännösten vaatimuksia. Lasku voidaan koodata paikalliseen toimipaikkaan. Käytä tuloilmoituksessa täsmäyttävää taloushallinnon dimensiota kustannusten raportoimiseksi alueelliselle toimistolle.

### <a name="local-tax-requirements"></a>Paikalliset verovaatimukset

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Yritykseen sovelletaan sen rekisteröintimaan/-alueen veroviranomaisten verolakeja. Esimerkiksi Tanskassa rekisteröityyn yritykseen sovelletaan Tanskan verolakeja ja sääntöjä. Oikeushenkilö voi kuulua vain yhteen maahan/alueeseen. Maa tai alue, jonka olet valinnut yrityksen ensisijaiseksi osoitteeksi määrää yrityksen käytettävissä olevia maa- tai aluekohtaisia ominaisuuksia. Jos yrityksen ensisijainen osoite on esimerkiksi Tanskassa, Tanskan verolakeihin ja sääntöihin liittyvät ominaisuudet ovat käytettävissä. Tämän vuoksi, jos organisaatiosi ovat eri maissa tai eri alueilla ja vaativat erilaiset veroasetukset, sinun on määritettävä organisaatiot erillisiksi yrityksiksi.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Toimintayksiköt käyttävät pääyrityksen maakontekstia. Samassa yrityksessä olevilla toimintayksiköillä ei voi olla erilaisia maa-/aluekohtaisia vaatimuksia. Jos yritykset ovat samassa maassa/alueella ja käyttävät samoja veroasetuksia, voit määrittää ne liiketoiminnan yksiköiksi.

### <a name="statutory-reporting-for-a-countryregion"></a>Lakisääteinen maa- tai aluekohtainen raportointi

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Tuettujen maiden tai alueiden kohdalla voidaan luoda useimmat lakisääteiset raportit. Lisätietoja kullekin maalle/alueella saatavilla olevista raporteista on [Microsoft Dynamics Localization Portalissa](https://docs.microsoft.com/dynamics/s-e/). (CustomerSource-kirjautuminen on pakollista.)

> [!NOTE]
> Kirjanpidon kirjanpitotason avulla voit tehdä oikaisevat kirjaukset emoyhtiölle, joka käyttää eri kirjanpidon vakiota kuin tytäryhtiö. Esimerkiksi yrityksessä, joka käyttää yleisesti Isossa-Britanniassa (UK GAAP) hyväksyttyjä kirjanpitokäytäntöjä, voit tehdä oikaisevat kirjaukset kirjanpitotasolla. Nämä tapahtumat voidaan konsolidoida emoyhtiöksi, joka käyttää Yhdysvalloissa yleisesti hyväksyttyjä kirjanpitoperiaatteita (GAAP). Oikaisumerkinnät eivät vaikuta UK GAAP -raportointiin.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Lakisääteiset raportit on luotava käyttämällä toista sovellusta. Sinun on varmistettava, että Finance and Operations -sovelluksissa kerätään tiedot jokaisen toimintayksikön vaatimusten tukemiseksi, kun ne poikkeavat pääkonttorin vaatimuksista.

### <a name="currency"></a>Valuutta

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Jos organisaatioidesi on käytettävä erilaisia toimintavaluuttoja, on organisaatiot mallinnettava yrityksinä. Toimintavaluutat määritetään yrityskohtaisesti. Voit syöttää tapahtumia eri valuuttoina.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Jos yritykset käyttävät samaa toimintavaluuttaa, voit mallintaa organisaatiot liiketoiminnan yksiköiksi. Toimintayksiköiden on jaettava perusvaluutta. Voit syöttää tapahtumia ja luoda raportteja eri valuuttoina.

### <a name="year-end-closing"></a>Tilinpäätös

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Jos lainsäädännön ja kirjanpitokäytäntöjen eroavat niiden maiden/alueiden välillä missä yritykset ovat, voidaan tarvita erilaisia tilinpäätöstoimenpiteitä. Tämä tarkoittaa, että sinun on mallinnettava organisaatiot yrityksinä. Jokaisella yrityksellä on omat vuoden päätökseen liittyvät menettelyt.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Jos lainsäädännön ja kirjanpitokäytäntöjen ovat samat niiden maiden/alueiden välillä missä yritykset ovat, voidaan käyttää yhtenäisiä tilinpäätöstoimenpiteitä. Tämä tarkoittaa, että voit mallintaa organisaatiot toimintayksiköinä. Kaikkien toimintayksiköiden on käytettävä samaa tilinpäätösmenettelyä.

### <a name="number-sequences"></a>Numerosarjat

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Eräiden viittausten numerosarjat voidaan määrittää yrityskohtaisesti. Eräät numerosarjat voidaan jakaa.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Eräiden viittausten numerosarjat voidaan määrittää toimintayksikkökohtaisesti. Eräät numerosarjat voidaan jakaa.

### <a name="products"></a>Tuotteet

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Tuotteiden määritelmät jaetaan, ja ne on vapautettava yksittäisille yrityksille ennen kuin ne voidaan sisällyttää tapahtumiin. Jokaisella yrityksellä on oma joukko vapautettuja tuotteita, jotka voidaan sisällyttää tapahtuma-asiakirjoihin. Jos sisäisten organisaatioidesi on käytettävä erilaisia tuotteita, on organisaatiot mallinnettava yrityksinä.

> [!NOTE]
> Vaikka tuotteiden määritykset jaetaan, voit määrittää jokaisessa varastotoimipaikassa nimikkeelle eri myynnit, ostot ja varastointiparametrit jokaisessa yrityksessä, jossa tuote julkaistaan.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Kaikilla toimintayksiköillä on sama tuotejoukko. Jos sisäiset organisaatiosi voivat jakaa samoja tuotteita, voit mallintaa organisaatiot liiketoiminnan yksiköiksi.

### <a name="inquiry-and-reporting"></a>Kysely ja raportointi

#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Jos organisaatio perustuu yrityksenä

Sinun on muutettava yrityksiä manuaalisesti tapahtumien kirjoittamiseksi ja suoritettava kyselyt useissa yrityksissä. Tietoturvarajoitusten vuoksi konsolidoitu kysely ja raportointi voi kuluttaa paljon resursseja ja kestää pitkään.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Jos organisaatio perustuu liiketoiminnan yksikköihin

Sinun ei tarvitse muuttaa yrityksiä käyttämään tietoja useista toimintayksiköistä. Konsolidoitu kysely ja raportointi ja aluekohtainen kysely on helppoa ja nopeaa.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Parhaat käytännöt organisaatioiden ja hierarkioiden mallintamiseen

Ota huomioon seuraavat suositeltavat menetelmät organisaatiohierarkian käyttöönoton yhteydessä:

- Luo osasto yrityksen ja liiketoimintayksikön välisen liitoksen mallintamiseksi. Sitten voit koota tietoja osastosta yritykseen lakisääteistä raportointia varten ja osastosta liiketoimintayksikköön sisäistä raportointia varten. Osastot voivat olla voittokeskuksia. Jos käytät osastoja, sinun ei tarvitse käyttää yrityksiä ja liiketoimintayksiköiden tilirakennedimensioita tilirakenteessa. Voit käyttää vain osastoja dimensiona. On kuitenkin käytettävä kustannuspaikkoja ja osastoja tilirakenteen dimensioina tilirakenteessa, jos kustannuspaikkoja käytetään vain kustannusten kokoamiseen ja osastoja käytetään tuottokirjausta varten.
- Mallinna useita hierarkioita toimintayksiköille, jos tuloksen raportoinnin vaatimukset ovat monimutkaisia.
- Yksittäisessä yrityksessä ei mallinneta useita hierarkioita samaan hierarkiatarkoitukseen.
- Älä luo hierarkiaa joka tarkoitukseen. Voit yleensä käyttää yhtä hierarkiaa moneen tarkoitukseen. Esimerkiksi yksi toimintayksiköiden hierarkia voidaan määrittää kaikkiin käytäntöön liittyviin tarkoituksiin.
- Luo tasapainotetut hierarkiat. Hierarkiassa kaikki solmut, jotka ovat yhtä kaukana juurisolmusta, määritellään tasona. Tasapainotetussa hierarkiassa vain yhdentyyppinen liiketoiminnan yksikkö voi esiintyä kussakin tasossa, ja etäisyys juurisolmusta tasoihin on yhdenmukainen. Jos on keskitasoja osaston ja yrityksen tai liiketoimintayksikön välillä, paikkamerkin organisaatiot voivat olla pakollisia tasapainotetun hierarkian luomiseksi.
- Älä mallinna toimintayksiköiden erillistä hierarkiaa, jos yritysten rakenne on myös toimintarakenteesi. Yhdistelmähierarkia, johon kuuluu yrityksiä ja toimintayksiköitä voi olla hyödyllinen molemmille.
- Ennen kuin mallinnat tärkeimpiä uudelleenjärjestelyn tilanteita, käytä hierarkian voimassaolopäivämääriä vaikutusanalyysiin ja oikeellisuustarkistukseen.
- Käytä luonnostilaa hierarkian muuttamiseen ennen, kuin julkaiset uuden version tuotantoympäristössä.
- Rajoita niiden käyttäjien määrää, joilla on oikeudet lisätä organisaatioita hierarkiaan tai poistaa niitä tuotantoympäristössä. Pienempi numero laskee kalliiden virheiden mahdollisuutta ja tarvetta korjata virheitä.
