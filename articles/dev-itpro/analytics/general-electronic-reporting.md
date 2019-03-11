---
title: Sähköinen raportointi (ER)
description: Tämä aihe esittelee sähköisen raportointityökalun. Artikkelissa on tietoja keskeisistä käsitteistä ja sähköisen raportoinnin tukemista skenaarioista. Lisäksi siinä on luettelo muodoista, jotka on suunniteltu osana tätä ratkaisua ja jotka julkaistaan sen osana.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e619b24fc790399452d6233b2d04987357d87186
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "310803"
---
# <a name="electronic-reporting-er"></a>Sähköinen raportointi (ER)

[!include [banner](../includes/banner.md)]

Tämä aihe esittelee sähköisen raportointityökalun. Artikkelissa on tietoja keskeisistä käsitteistä ja sähköisen raportoinnin tukemista skenaarioista. Lisäksi siinä on luettelo muodoista, jotka on suunniteltu osana tätä ratkaisua ja jotka julkaistaan sen osana.

ER on työkalu, jolla voit määrittää saapuvien ja lähtevien sähköisten asiakirjojen muodon eri maiden ja alueiden säädösten mukaisesti. Sähköinen raportointi mahdollistaa näiden muotojen hallinnan niiden elinkaaren aikana. Voit esimerkiksi ottaa käyttöön uusia säädöksiin perustuvia vaatimuksia ja luoda vaatimusten mukaisia liiketoiminnan asiakirjoja, jotka mahdollistavat sähköisen tiedonsiirron viranomaisten, pankkien ja muiden osapuolien välillä.

Sähköinen raportointimoduuli on suunnattu yrityskäyttäjille eikä kehittäjille. Koska määritykset koskevat muotoja koodin sijaan, sähköisten asiakirjojen muotojen käsittely- ja muokkausprosessi on nopeaa ja helppoa.

Sähköinen raportointi tukee tällä hetkellä TXT-, XML- ja Microsoft Word -tietoja sekä OPENXML-muotoisia laskentataulukkoja. Laajennettu liittymä tukee kuitenkin myös muita muotoja.

## <a name="capabilities"></a>Toiminnot
Sähköisessä raportointimoduulissa on seuraavat toiminnot:

- Se on yksi yhteinen, eri toimialueilla toimiva sähköisen raportoinnin työkalu, joka korvaa yli 20 erilaista Microsoft Dynamics 365 for Finance and Operationsin sähköisen raportoinnin moduulia.
- Se eristää raportin muodon tällä hetkellä käyttöönotetusta Finance and Operationsista. Toisin sanoen muotoa voi käyttää Finance and Operationsin eri versioissa.
- Se tukee alkuperäiseen muotoon perustuvan mukautetun muodon luontia. Sen toiminnoilla voi myös päivittää automaattisesti mukautetut muodot, kun alkuperäiseen muotoon on tehty muutoksia. Tämä onnistuu lokalisointi- ja mukautusvaatimusten avulla.
- Siitä tulee ensisijainen vakiotyökalu lokalisointivaatimusten tukemiseen sähköisessä raportoinnissa – sekä Microsoftille että sen kumppaneille.
- Se tukee mahdollisuutta jakaa muotoja kumppaneille ja asiakkaille Microsoft Dynamics Lifecycle Servicesissä (LCS).

## <a name="key-concepts"></a>Avainkäsitteet
### <a name="components"></a>Komponentit

Sähköinen raportointi tukee kahdenlaisia osia: **tietomalleja** ja **muotoa**.

#### <a name="data-model-components"></a>Tietomalliosat

Tietomallikomponentti on tietorakenne abstrakti kuvaus. Sen avulla tietty liiketoiminnan toimialue voidaan selittää riittävän yksityiskohtaisesti kyseisen toimialueen raportointitarpeiden mukaisesti. Tietomalliosassa on seuraavat osat:

- Tietomalli joukkona toimialuekohtaisia liiketoimintayksiköitä ja rakenteeltaan hierarkkisena määrityksenä kyseisten yksiköiden välisistä suhteista.
- Mallin yhdistämismääritykset, jotka linkittävät valitut Finance and Operations -tietolähteet yksittäisiin tietomallin elementteihin ja jotka määrittävät suorituksenaikaisen tiedonkulun ja säännöt liiketoiminnan tietojen täyttämiseen tietomalliosassa.

Tietomallin liiketoimintayksikkö ilmaistaan säilönä (tietue). Liiketoimintayksikön ominaisuudet esitetään tietokohteina (kentät). Kullakin tiedolla on yksilöllinen nimi, otsikko, kuvaus ja arvo. Kunkin tiedon arvo voidaan suunnitella tunnistettavaksi esimerkiksi merkkijonona, kokonaislukuna, reaalilukuna, päivämääränä, valintalistan tyyppinä tai totuusarvona. Se voi olla myös toinen tietue tai tietueluettelo.

Yksittäisessä tietomallikomponentissa voi olla useita toimialuekohtaisten liiketoimintayksiköiden hierarkioita. Siinä voi olla myös suorituksenaikaista rapottikohtaista tiedonkulku tukevia yhdistämismäärityksiä. Hierarkiat erotellaan sen yksittäisen tietueen perusteella, joka on valittu mallien yhdistämisen juureksi. Esimerkiksi maksutoimialueen alueen tietomalli voi tukea seuraavia yhdistämismäärityksiä:

- Yritys \> Toimittaja \> Ostoreskontratoimialueen maksutapahtumat
- Asiakas \> Yritys \> Myyntireskontran toimialueen maksutapahtumat

Huomaa, että liiketoimintayksiköt, kuten yritys ja maksutapahtumat, suunnitellaan kerran. Eri yhdistämismääritykset ja käytä niitä sitten uudelleen.

Lähteviä sähköisiä asiakirjoja tukevassa mallin yhdistämismäärityksessä on seuraavat ominaisuudet:

- Se voi käyttää Finance and Operationsin tietotyyppejä tietomallina. Se voi käyttää esimerkiksi taulukoita, tietoyksiköitä, menetelmiä tai valintaluetteloita.
- Se tukee käyttäjän syöttöparametreja, jotka voidaan määrittää tietomallin tietolähteiksi, kun osa tiedoista on määritettävä suorituksen aikana.
- Se tukee Finance and Operationsin tietojen muuntamista tarvittaviksi ryhmiksi. Voit myös suodattaa, lajittelu ja summata tietoja sekä loogisia laskettuja kenttiä, jotka on suunniteltu Microsoft Excelin kaavoja muistuttavilla kaavoilla seuraavassa kuvassa esitetyllä tavalla. Lisätietoja on ohjeaiheessa [Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md)).

[![Kaavan suunnittelutoiminto](./media/ER-overview-01.png)](./media/ER-overview-01.png)

Saapuvia sähköisiä asiakirjoja tukevassa mallin yhdistämismäärityksessä on seuraavat ominaisuudet:

- Se voi käyttää erilaisia päivitettäviä tietoelementtejä kohteina. Näitä tietoelementtejä ovat esimerkiksi taulut, tietoyksiköt ja näkymät. Tietoja voi päivittää saapuvien sähköisten asiakirjojen tiedoilla. Yhdessä mallin yhdistämismäärityksessä voidaan käyttää useita kohteita.
- Se tukee käyttäjän syöttöparametreja, jotka voidaan määrittää tietomallin tietolähteiksi, kun osa tiedoista on määritettävä suorituksen aikana.

Tietomallikomponentti on suunniteltu käytettäväksi kullakin liiketoiminnan toimialueella yhtenäisenä tietolähteenä raportoinnissa, joka eristää raportoinnin Finance and Operationsin tietolähteiden fyysisestä toteuttamisesta. Se kuvaa toimialuekohtaisia liiketoimintakonsepteja ja toimintoja muodossa, joka tehostaa raportointimuotojen alkusuunnittelua ja sen jälkeisestä ylläpitoa.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Lähtevien sähköisten asiakirjojen muotokomponentit

Muoto-osa on raporttitulostuksen malli, joka luodaan suorituksen aikana. Malli sisältää seuraavat elementit:

- Muoto, joka määrittää suorituksen aikana luodun lähtevän sähköisen asiakirjan rakenteen ja sisällön.
- Tietolähteet käyttäjän syöttöparametrijoukkona ja valittua tiedon yhdistämismääritystä käyttävänä toimialuekohtaisena tietomallina.
- Muodon yhdistämismääritys muodon tietolähteen sidosjoukkona. Siinä on sellaisia muodon yksittäisiä elementtejä, jotka määrittävät suorituksen aikana tiedonkulun ja tulostusmuodon luontisäännöt.
- Muotomäärityksen vahvistaminen joukkona määritettävissä olevia sääntöjä, jotka ohjaavat raportin luomista suorituksen aikana suoritettavan raportin yhteyden mukaisesti. Sääntö voi esimerkiksi pysäyttää toimittajan maksujen tulostuksen luonnin ja aiheuttaa poikkeuksen, kun tietyt valitun toimittajan määritteet, kuten pankkitilin numero, puuttuvat.

Muoto-osa tukee seuraavia toimintoja:

- Raporttitulostuksen luonti yksittäisinä, erimuotoisina tiedostoina: teksti, XML, Microsoft Word -asiakirja tai laskentataulukko.
- Useiden tiedostojen luonti erikseen sekä kyseisten tiedostojen kerääminen zip-tiedostoihin.

Muotokomponentin avulla tietyt raporttitulostuksessa käytettäviä tiedostoja voidaan liittää.

- OPENXML-laskentataulukkomuodossa tulostusmallina käytettävän laskentataulukon sisältävät Excel-laskentataulukot.
- Microsoft Word -asiakirjamuodossa tulostusmallina käytettävän asiakirjan sisältävät Microsoft Word -tiedostot.
- Muut tiedostot, jotka voidaan sisällyttää muodon tulostukseen etukäteen määritettyinä tiedostoina.

Seuraavassa kuvassa osoitetaan tiedonkulku näissä muodoissa.

[![Lähtevien muotokomponenttien tiedonkulku](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Voit suorittaa yksittäisen sähköisen raportoinnin muotomäärityksen ja luoda lähtevän sähköisen asiakirjan tunnistamalla muotomääritysten yhdistämismääritykset.

#### <a name="format-components-for-incoming-electronic-documents"></a>Saapuvien sähköisten asiakirjojen muotokomponentit
Muotokomponentti on saapuvan asiakirjan malli, joka tuodaan suorituksen aikana. Malli sisältää seuraavat elementit:

- Muoto, joka määrittää suorituksen aikana tuodun, tietoja sisältävän saapuvan sähköisen asiakirjan rakenteen ja sisällön. Saapuva asiakirja jäsennetään muotokomponentin avulla eri muodoissa, kuten teksti- ja XML-muodossa.
- Muodon yhdistämismääritys, joka sitoo yksittäiset muotoelementit toimialuekohtaisen tietomallin elementteihin. Tietomallin elementit määrittävät suorituksen aikana tiedonkulun ja saapuvan asiakirjan tietojen tuontisäännöt ja tallentavat tiedot sitten tietomalliin.
- Muotomäärityksen vahvistaminen joukkona määritettävissä olevia sääntöjä, jotka ohjaavat tietojen tuontia suorituksen aikana asiayhteyden mukaisesti. Sääntö voi esimerkiksi pysäyttää sellaisten tiliotteen tietojen tuonnin, jossa on toimittajan maksuja, ja aiheuttaa poikkeuksen, kun tietyt toimittajan määritteet, kuten toimittajan tunnuskoodi, puuttuvat.

Seuraavassa kuvassa osoitetaan tiedonkulku näissä muodoissa.

[![Saapuvien muotokomponenttien tiedonkulku](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Jos haluat tuoda saapuvan sähköisen asiakirjan tietoja suorittamalla sähköisen raportoinnin muotomääritykset, sinun on tunnistettava muotomäärityksen toivotut yhdistämismääritykset sekä mallin yhdistämismääritysten integrointikohta. Voit käyttää saman mallin yhdistämismäärityksiä ja kohteita yhdessä erityyppisten saapuvien asiakirjojen erilaisten muotojen kanssa.

#### <a name="component-versioning"></a>Komponenttien versionhallinta

Sähköisissä raportointiosissa tuetaan versionhallintaa. Sähköisen raportoinnin komponenteissa muutoksia hallitaan seuraavalla työnkululla:

1. Ensimmäisenä luotu versio merkitään **Luonnos**-versioksi. Tätä versiota voidaan muokata ja sillä voi suorittaa testiajoja.
2. **Luonnos**-versio voidaan muuntaa **Valmis**-versioksi. Tätä versiota voidaan käyttää paikallisissa raportointiprosesseissa.
3. **Valmis**-versio voidaan muuntaa **Jaettu**-versioksi. Tämä versio julkaistaan LCS:ssä ja sitä voidaan käyttää yleisissä raportoinnin prosesseissa.
4. **Jaettu**-versio voidaan muuntaa **Lopetettu**-versioksi. Tämä versio voidaan sitten poistaa.

Versioita, joiden tila on joko **Valmis** tai **Jaettu**, voidaan käyttää muissa tiedonsiirroissa. Seuraavat toimet voidaan suorittaa komponentissa, jolla on nämä tilat:

- Komponentit voidaan sarjoittaa XML-muodossa ja viedä XML-muotoisena tiedostona.
- Komponentti voidaan sarjoittaa uudelleen XML-tiedostosta ja tuoda Finance and Operationsiin ER-komponentin uutena versiona.

#### <a name="component-date-effectivity"></a>Komponentin päivämäärän voimassaolo

Sähköisen raportointikomponentin versioilla on voimassaolopäivämäärät. Voit määrittää sähköiselle raportointikomponentille **Voimaantulopäivä**-arvon määrittämään päivän, josta lähtien kyseinen komponentti on voimassa raportointiprosesseissa. Finance and Operationsin istunnon päivämäärää käytetään määrittämään, onko komponentti suoritettavissa. Jos tiettynä päivänä on voimassa useampia kuin yksi versio, viimeisintä versiota käytetään raportointiprosessissa.

#### <a name="component-access"></a>Komponenttien käyttöoikeudet

Sähköisten raportointiosien käyttöoikeus määräytyy maan/alueen ISO-koodiasetuksista. Jos tämä asetus on tyhjä muotomääritysten valitussa versiossa, muoto-osaa voidaan käyttää suorituksenaikainen missä tahansa yrityksessä. Jos asetuksessa on ISO-maa-/aluekoodeja, muoto-osia voidaan käyttää vain niissä yrityksissä, joiden ensisijainen osoite on määritetty joksikin muoto-osan ISO-maa-/aluekoodiksi.

Tietomuoto-osien eri versioilla voi olla erilaiset ISO-maa/aluekoodeja koskevat asetukset.

#### <a name="configuration"></a>Määritys

Sähköinen raportointimääritys on tietyn sähköisen raportointikomponentin paketoija. Kyse voi olla joko tietomallikomponentista tai muotokomponentista. Määritykset voivat sisältää sähköisen raportointikomponentin eri versioita. Kukin määritys merkitään tietyn määrityslähteen omistamaksi. Määrityskomponentin **Luonnos**-versiota voidaan muokata, jos kyseisten määritysten omistaja on valittu Finance and Operationsin ER-asetusten aktiiviseksi lähteeksi.

Kussakin mallimäärityksessä on tietomallikomponentti. Uusien muotomääritysten alkuperä voi olla tietty tietomallimääritys. Luotu määritysmuoto tulee näkyviin määrityspuuhun alkuperäisen tietomallimääritysten alikohteena.

Luodussa muotomäärityksessä on muotokomponentti. Alkuperäisten mallimääritysten tietomallikomponentti lisätään automaattisesti alimuodon muotokomponentin määritykseen oletustietolähteenä.

ER-määritykset jaetaan Finance and Operations -yrityksille.

#### <a name="provider"></a>Tarjoaja

Sähköinen raportointipalvelu on osapuolen tunniste, jota ilmaistaan sähköisten raportointimääritysten tekijä (omistaja). Voit hallita sähköisen raportoinnin avulla määrityspalvelujen luetteloa. Sähköisille asiakirjoille Finance and Operations -ratkaisun osana julkaistujen muotomääritysten omistajaksi merkitään **Microsoftin** määrityspalvelu.

Lisätietoja uuden sähköisen raportointipalvelun rekisteröimisestä on tehtäväoppaassa **ER Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi** (liiketoimintaprosessin **7.5.4.3 IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen (10677)** osa).

#### <a name="repository"></a>Säilö

Sähköiset raportointimääritykset tallennetaan sähköisen raportoinnin säilöön. Tällä hetkellä tuetaan neljää ER-säilöä: **Operatiiviset resurssit**, **LCS-projektit (LCS)**, **Tiedostojärjestelmä** ja **Sääntöjen konfigurointipalvelu (RCS)**.

**Operatiivisten resurssien** säilö antaa mahdollisuuden käyttää määritysluetteloa, jonka Microsoft sähköisen raportoinnin määrityspalveluna julkaisee Finance and Operations -ratkaisun osana. Nämä määritykset voidaan tuoda nykyiseen Finance and Operationsin esiintymään ja niitä voidaan käyttää sähköisessä raportoinnissa. Niitä voidaan käyttää myös muissa lisälokalisoinneissa ja -mukautuksissa.

**LCS-projektin** säilö tarjoaa mahdollisuuden käyttää tietyn LCS-projektin (LCS-projektiresurssikirjaston) määritysluetteloa, joka valittiin säilön rekisteröintivaiheessa. Sähköinen raportointi mahdollistaa jaettujen määritysten latauksen nykyisestä Finance and Operationsin esiintymästä tiettyyn **LCS-projektin** säilöön. Voit myös tuoda määrityksiä **LCS-projektin** säilöstä nykyiseen Finance and Operationsin esiintymään.

**Tiedostojärjestelmä**-säilössä on luettelo määrityksistä, jotka sijaitsevat xml-tiedostoina tietyssä sellaisen paikallisen laitteen tietojärjestelmän kansiossa, joka isännöi AOS-palvelua. Tarvittava kansio valitaan säilön rekisteröintivaiheessa. Voit tuoda määrityksiä **Tiedostojärjestelmä**-säilöstä nykyiseen Finance and Operationsin esiintymään. Huomaa, että tätä säilötyyppiä voi käyttää seuraavista Dynamics 365 for Finance and Operations -ympäristöistä:
- kehitystyötä varten käyttöönotetut pilvipalveluympäristöt (jotka sisältävät liitettyjen pakettien testimalleja)
- paikallisesti käyttöönotetut ympäristöt (paikallinen yritystietojen käyttöönotto (LBD))

Sivulla [Sähköisen raportoinnin (ER) konfiguraatioiden tuonti](./electronic-reporting-import-ger-configurations.md) on lisätietoja.

**LCS-esiintymän** säilössä on tietyn RCS-esiintymän määritysluettelo, joka valittiin säilön rekisteröintivaiheessa. Sähköisen raportoinnin ansiosta voit tuoda valmiita tai jaettuja määrityksiä valitusta RCS-esiintymästä nykyiseen Finance and Operations -esiintymään sähköistä raportointia varten.

Sivulla [Sähköisen raportoinnin (ER) konfiguraatioiden tuonti sääntöjen konfigurointipalvelusta (RCS)](./rcs-download-configurations.md) on lisätietoja.

Tarvittavat **LCS-projekti**-, **Tiedostojärjestelmä**- ja **Sääntöjen konfigurointipalvelu (RCS)** -säilöt voidaan rekisteröidä erikseen kullekin nykyisen Finance and Operations -esiintymän määrityspalvelulle. Kukin säilö voidaan osoittaa tiettyyn määrityspalveluun.

## <a name="supported-scenarios"></a>Tuetut skenaariot
### <a name="building-a-data-model"></a>Tietomallin rakentaminen

Sähköisessä raportoinnissa on mallin suunnittelutoiminto, jolla voit luoda tietyn liiketoiminnan toimialueen tietomallin. Kaikki tietomallikohtaiset liiketoimintayksiköt ja niiden väliset suhteet voidaan esittää tietomallissa hierarkkisena rakenteena. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallista (maksutoimialueen tietomalli).

[![Maksutoimialueen tietomalli](./media/ER-overview-04.png)](./media/ER-overview-04.png)

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin suunnittelutoimialuekohtainen tietomalli** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="translating-data-model-content"></a>Tietomallin sisällön kääntäminen

Tietomallin sisältö (otsikot ja kuvaukset) voidaan kääntää muille Finance and Operationsin tukemille kielille. Tietomallin sisältö voidaan haluta kääntää seuraavista syistä:

- Suunnitteluvaiheessa sitä varten, että sisältö olisi paremmin sellaisten vieraskielisten muodon suunnittelijoiden ymmärrettävissä, jotka käyttävät tietomallia muotokomponenttien tietojen yhdistämismäärityksiin.
- Suorituksenaikana sen vuoksi, että sisällön käyttö olisi kätevämpää, kun kehotteet ja suoritustenaikaisten parametrien ohje sekä määritetyt tarkistussanomat (virheet ja varoitukset) näytetään kirjautuneen käyttäjän ensisijaisella kielellä.

Seuraavassa kuvassa on esimerkki tietomallin sisällön kääntämisestä englannista japaniksi.

[![Tietomallin englanninkielinen sisältö](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Japaniksi käännetty tietomallin sisältö](./media/ER-overview-06.png)](./media/ER-overview-06.png)

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Lähtevien asiakirjojen tietomallin yhdistämismääritysten määrittäminen

Sähköiseen raportointiin sisältyy mallin yhdistämismääritysten suunnittelutoiminto, jolla käyttäjät voivat tehdä yhdistämismäärityksiä tiettyihin Finance and Operationsin tietolähteisiin suunniteltuihin malleihin. Tiedot tuodaan suorituksen aikana yhdistämismäärityksen mukaisesti valituista tietolähteistä tietomalliin. Tietomallia käytetään sitten lähteviä sähköisiä asiakirjoja luovien sähköisten raportointimuotojen abstraktina tietolähteenä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin yhdistämismäärityksestä (**SEPA-tilisiirto**-mallin maksutoimialueen tietomallin yhdistämismääritys).

[![Esimerkki tietomallin yhdistämismäärityksestä](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen ja tietolähteiden valinta**- ja **Sähköisen raportoinnin tietomallin yhdistämismääritysten tekeminen valittuihin tietolähteisiin** -tehtäväoppaat (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Saapuvien asiakirjojen tietomallin yhdistämismääritysten määrittäminen
Sähköiseen raportointiin sisältyy mallin yhdistämismääritysten suunnittelutoiminto, jolla käyttäjät voivat tehdä yhdistämismäärityksiä tiettyihin kohteisiin suunniteltuihin tietomalleihin. Tietomallien yhdistämismääritys voidaan esimerkiksi tehdä Finance and Operationsin päivitettäviin tietokomponentteihin (tauluihin, tietoyksiköihin ja näkymiin). Finance and Operationsin tiedot päivitetään yhdistämismääritysten perusteella suorituksen aikana tietomallin tiedoilla. Tietomalli täytetään sähköisen tietomallimuodon abstraktina tallennuksena saapuvasta sähköisestä asiakirjasta tuotavilla tiedoilla. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin yhdistämismäärityksestä. Tässä esimerkissä maksutoimialueen tietomallin **NETS-yhdistämismäärityksen tuonti** -mallin yhdistämismäärityksellä tuetaan norjalaisen NETS-pankkimuodon tiliotteiden tuontia.

[![NETS-tuontimallin yhdistämismäärityksen tuontiesimerkki](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Suunnitellun malliosan tallentaminen mallimäärityksinä

Sähköinen raportointi voi tallentaa suunnitellun tietomallin yhdessä liitettyjen tietojen yhdistämismääritysten kanssa nykyisen Finance and Operationsin esiintymän mallimäärityksinä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin määrityksestä (maksumallin määritykset).

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin tietomallin yhdistämismääritysten tekeminen valittuihin tietolähteisiin** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tietomallia perusteena käyttävän muodon muodostaminen

Sähköinen raportointi tukee muodon suunnittelutoimintoa, jolla voit muodostaa valitulle liiketoiminnan toimialueelle sähköisen asiakirjan muodon valitsemalla pohjaksi mallikomponentin. Sama sähköisen raportoinnin muodon suunnittelutoiminto mahdollistaa luodun muodon yhdistämismäärityksen tekemisen valitun toimialueen tietomallin yhdistämismäärityksen tietolähteenä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta (Yhdistyneen kuningaskunnan **BACS**-maksumuotoa tukeva muotomääritys).

[![Esimerkki tietomallia perusteena käyttävästä muodosta](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML-laskentataulukkomuodossa luotavien sähköisten asiakirjojen määritysten muodostaminen

Sähköisen raportointimuodon suunnittelutoiminnolla voidaan muodostaa OPENXML-laskentataulukon muotoinen sähköinen asiakirja. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta (muotomääritys, jolla luodaan valitun maksukirjauskansion tietoja sisältävä OPENXML-laskentataulukko).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin OPENXML-muotoisten raporttimääritysten luonti** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia). Käytä tehtäväoppaan mallin tuontivaiheessa mallina Excel-tiedostoa [Maksuraportin malli (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Word-asiakirjan muodossa luotavien sähköisten asiakirjojen määritysten muodostaminen
Sähköisen raportointimuodon suunnittelutoiminnolla voidaan muodostaa Word-asiakirjan muotoinen sähköinen asiakirja. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta. Huomaa, että tämä muoto käyttää uudelleen aiemmin luotuja sähköisen raportoinnin määrityksiä, jotka suunniteltiin alun perin suunniteltu luomaan raportti OPENXML-muodossa.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Tutustu skenaarion tietoihin toistamalla Sähköisen raportoinnin Micrsoft Word -muotoisten raporttimääritysten suunnittelu -tehtäväopas (liiketoimintaprosessin osa 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)). Käytä tehtäväoppaan mallin tuontivaiheessa seuraavia Word-tiedostoja sähköisen raportointimuodon malleina:

- [Maksuraportin malli (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Maksuraportin sidottu malli (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Saapuvien sähköisten asiakirjojen tietojen tuontimääritysten muodostaminen
Sähköisen raportointimuodon suunnittelutoiminnolla voi kuvata sähköisen asiakirjan, jolla tietoja aiotaan tuoda joko XML- tai tekstimuodossa. Saapuva tiedosto jäsennetään suunnitellulla muodolla. Sähköisen raportointimuodon yhdistämismäärityksen suunnittelutoiminnoilla voidaan määrittää, miten suunnitellun muodon elementit sidotaan tietomalliin. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodostaja muodon yhdistämismäärityksestä. Tässä esimerkissä tuodaan NETS-tiliotteita, joissa on tekstimuotoisia toimittajan maksutietoja.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Tutustu skenaarion tietoihin toistamalla Tarvittavien sähköisen raportoinnin määritysten luonti tietojen tuontiin ulkoisesta tiedostosta -tehtäväopas (liiketoimintaprosessin osa 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)). Toista opas käyttämällä seuraavia tiedostoja:

- [Sähköisen raportoinnin tietomallien määritys (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Sähköisen raportointimuodon määritys (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Malli saapuvasta XML-muotoisesta asiakirjasta (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Saapuvan asiakirjan tietojen hallinnan työkirjamalli (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Suunnitellun muoto-osan tallentaminen muotomäärityksenä

Suunniteltu muoto voidaan tallentaa sähköisessä raportoinnissa yhdessä määritettyjen tietojen yhdistämismääritysten kanssa nykyisen Finance and Operations -esiintymän muotomäärityksenä. Edeltävässä kuvassa on esimerkki tämän tyyppisestä muotomäärityksestä (**BACS (UK)** on **Maksumalli**-määrityksen alikohde). Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Finance and Operationsin määrittäminen käyttämään luotua muotoa sisäisesti

Finance and Operations voidaan määrittää aloittamaan luodun muodon käyttö sähköisten raporttien luomiseksi. Luodun muotomäärityksen viite on määritettävä tietyn toimialueen asetuksissa. Jos esimerkiksi halutaan aloittaa BACS-muotoisten sähköisten toimittajamaksujen sähköisen raportointimuodon määritysten käyttö, muotomääritykseen on viitattava maksutapakohtaisesti, kuten seuraavissa kuvissa:

[![BACS (UK) -muodon määritykset](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Viittaus BACS (UK) -muotoon maksutavassa](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon käyttö sähköisen asiakirjan luonti maksuja varten** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

## <a name="handling-er-components"></a>Sähköisten raportointien osien käsittely
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Sähköisten raportointiosan tarjoaminen ulkoiseen käyttöön (lokalisointi) julkaisemalla se LCS:ssä

Luodun osan (malli tai muoto) omistaja voi julkaista osan valmiin version LCS:ssä sähköisen raportoinnin avulla. Edellytetään nykyisen sähköisen raportoinnin määrityspalvelun **LCS-projektityypin** säilöä. Kun valmiin osaversion tila vaihdetaan tilasta **VALMIS** tilaksi **JAETTU**, tämä versio julkaistaan LCS:ssä. Kun osa on julkaistu LCS:ssä, kyseisen osan omistajasta tulee osan tuen palvelutarjoaja. Jos esimerkiksi tämä muoto-osa on suunniteltu luomaan lakisääteisiä sähköisiä asiakirjoja (esimerkiksi lokalisointiskenaarion mukaisesti), oletetaan, että muoto pidetään lakimuutosten mukaisena ja että palvelu julkaisee osasta uusia versioita aina, kun on uusia lakisääteisiä vaatimuksia tulee. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen lataaminen Lifecycle Servicesiin**-tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Sähköisen raportointiosan tuonti LCS:stä sisäistä käyttöä varten

Voit tuoda sähköisessä raportoinnissa sähköisiä raportointikomponentteja LCS:stä nykyiseen Finance and Operations -esiintymään. Tämä edellyttää **LCS-projektityypin** säilöä. Kun sähköinen raportointikomponentti on tuotu LCS:stä nykyiseen Finance and Operations -esiintymään, tämän esiintymän omistajasta tulee tuodun osan omistajan (laatijan) tarjoaman palvelun kuluttaja. Jos esimerkiksi tämä muotokomponentti on suunniteltu luomaan Finance and Operationsissa määritettyjä sähköisiä asiakirjoja tietyssä maa- tai aluekohtaisessa muodossa (lokalisointiskenaario), oletetaan, että palvelun kuluttaja pystyy hankkimaan kaikki tähän muotoon tehdyt päivitykset, jotta se pysyy lakisääteisten vaatimusten mukaisena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen tuonti Lifecycle Servicesistä** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Muodon rakentaminen toisen muodon pohjalta (mukauttaminen)

Voit luoda (johtaa) sähköisessä raportoinnissa uuden osan LCS:stä tuodun osan (perustan) nykyisestä versiosta. Käyttäjä voi esimerkiksi haluat johtaa uuden muodon toteuttaakseen jonkin tietyn sähköisen asiakirjan vaatimuksen (kuten lisäkentän tai laajan kuvauksen) mukautusskenaarion tukena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön sen perusversio** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Muodon päivittäminen valitsemalla perusmuodon uusi versio (pohjustus)

Voit ottaa sähköisessä raportoinnissa automaattisesti käyttöön viimeisimpään perusosaan versioon tehdyt muutokset nykyisessä johdetun osan luonnosversiossa. Tätä prosessia kutsutaan *pohjustamiseksi*. Esimerkiksi LCS:stä tuodun muodon uusimpaan versioon tehdyt lakisääteiset muutokset voidaan yhdistää automaattisesti tämän sähköisen asiakirjan muodon mukautettuun versioon. Muutoksia, joita ei voi yhdistetään automaattisesti, pidetään ristiriitoina. Nämä ristiriidat jätetään ratkaistavaksi manuaalisesti kyseisen osan suunnittelutyökaluun. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön kyseisen muodon perusversio** -tehtäväopas (osa **7.5.5.3 Muutetun IT-palvelu- ja -ratkaisuosan hankinta ja kehittäminen (10683)** -liiketoimintaprosessia).

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Finance and Operations -ratkaisussa toimitettavien sähköisten raportointimääritysten luettelo

| Toimialakohtaiset tietomallimääritykset: otsikko | Toimialue                | Tietomalliriippuvainen muotomääritykset: otsikko | Kuvaus                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Tarkistustiedostomalli                                 | Tilintarkistus       |                                                   |                                                                    |
|                                                  |                       | Tarkistustiedosto (NL)                                   | Alankomaisen tarkistustiedostomuoto                                  |
| BAS-malli                                        | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | Australian BAS-muoto                                           |
| Rakennustuotannon malli               | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | CIS-kuukausipalautus (UK)                           | Yhdistyneen kuningaskunnan CIS-kuukausipalautusmuoto                   |
| Maksukehotusmalli                          | Sähköinen laskutus  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-maksukehotus (DK)                     | Tanskan OIOUBL-maksukehotusmuoto                        |
| Sähköinen kirjanpitomalli (MX)          | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | Apukirjanpidon XML (MX)                         | Meksikon tilikohtainen tapahtumien apukirjanpidon raporttimuoto |
|                                                  |                       | Tilikartan XML (MX)                         | Meksikon tilikartan raporttimuoto                          |
|                                                  |                       | Kirjauskansioiden XML (MX)                                 | Meksikon kirjauskansiotapahtumien raporttimuoto                      |
|                                                  |                       | Pääkirjan XML (MX)                            | Meksikon pääkirjan raporttimuoto                             |
| ELSTER-malli                                     | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Saksan Elster-muoto                                          |
| EU-myyntiluettelon malli                              | Kaupparaportointi       |                                                   |                                                                    |
|                                                  |                       | EU-myyntiluettelo (DE)                                | Saksan TXT-muotoinen EU-myyntiluettelo                               |
|                                                  |                       | EU-myyntiluettelo (DK)                                | Tanskan TXT-muotoinen EU-myyntiluettelo                               |
|                                                  |                       | EU-myyntiluettelo (FR)                                | Ranskan XML-muotoinen EU-myyntiluettelo                                |
|                                                  |                       | EU-myyntiluettelo (NL)                                | Alankomaiden XML-muotoinen EU-myyntiluettelo                           |
|                                                  |                       | EU-myyntiluettelon TXT-muoto (UK)                            | Yhdistyneen kuningaskunnan TXT-muotoinen EU-myyntiluettelo                    |
|                                                  |                       | EU-myyntiluettelon XML-muoto (UK)                            | Yhdistyneen kuningaskunnan XML-muotoinen EU-myyntiluettelo                    |
|                                                  |                       | EU-myyntiluettelon sarakekohtainen raportti                   | EU-myyntiluettelon sarakekohtainen raportti                                    |
|                                                  |                       | EU-myyntiluettelon rivikohtainen raportti                      | EU-myyntiluettelon rivikohtainen raportti                                       |
| FEC-kirjanpitomalli (FR)                        | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | FEC-kirjanpidon tietojen XML-muoto (FR)                      | Ranskan FEC-kirjanpidon tietojen viennin XML-muoto                   |
| Saksan tarkistustiedosto                                | Tilintarkistus       |                                                   |                                                                    |
|                                                  |                       | Saksan tarkistustiedostotuloste                          | Saksan ja Itävallan tarkistustiedoston tuloste                          |
| Intrastat-malli                                  | Kaupparaportointi       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Saksan Intrastat-muoto                                       |
|                                                  |                       | Intrastat (DK)                                    | Tanskan Intrastat-muoto                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Ranskan Intrastat INTRACOM -muoto                               |
|                                                  |                       | Intrastat-SAISUNIC (FR)                           | Ranskan Intrastat SAISUNIC -muoto                               |
|                                                  |                       | Intrastat (NL)                                    | Alankomaiden Intrastat-muoto                               |
|                                                  |                       | Intrastat (UK)                                    | Yhdistyneen kuningaskunnan Intrastat-muoto                            |
|                                                  |                       | Intrastat-raportti                                  | Intrastatin Excel-muotoinen hallintaraportti                                     |
| Myyntilaskumalli                           | Sähköinen laskutus  |                                                   |                                                                    |
|                                                  |                       | OIOUBL, projektin hyvityslasku (DK)                   | OIOUBL, Tanskan projektin hyvityslaskumuoto                      |
|                                                  |                       | OIOUBL-projektilasku (DK)                       | Tanskan OIOUBL-projektilaskumuoto                          |
|                                                  |                       | OIOUBL, myynnin hyvityslasku (DK)                     | OIOUBL, Tanskan myynnin hyvityslaskumuoto                        |
|                                                  |                       | OIOUBL-myyntilasku (DK)                         | Tanskan OIOUBL-myyntilaskumuoto                            |
| OB-ilmoitusmalli                             | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | OB-ilmoitus (NL)                               | Alankomaiden OB-ilmoitusmuoto                          |
| Maksumalli                                    | Maksut              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Tanskan Betalingsservice-maksumuoto                        |
|                                                  |                       | Vekselin maksusuoritus (FR)                  | Ranskan vekselin maksusuorituksen muoto                      |
|                                                  |                       | BTL91 (NL)                                        | Alankomaiden toimittajan BTL91-maksumuoto                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB, Ranskan suoraveloituksen maksumuoto                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB, Ranskan kotimaan toimittajien maksumuoto                    |
|                                                  |                       | Nordea-toimittaja (DK)                                | Tanskan Nordea Corporate Netbankin toimittajan maksumuoto         |
|                                                  |                       | ANZ Direct Credit Service (AU)                    | Australian ANZ Direct Credit Service -muoto                 |
|                                                  |                       | CBA Direct Credit Service (AU)                    | Australian CBA Direct Credit Service -muoto                 |
|                                                  |                       | NAB Direct Credit Service (AU)                    | Australian NAB Direct Credit Service -muoto                 |
|                                                  |                       | STG Direct Credit Service (AU)                    | Australian STG Direct Credit Service -muoto                 |
|                                                  |                       | WBC Direct Entry System (AU)                      | Australian WBC Direct Entry System -muoto                   |
|                                                  |                       | DirectLink (NZ)                                   | Uuden-Seelannin DirectLink-muoto                              |
|                                                  |                       | JBA-maksutiedosto (JP)                             | Japanin JBA-maksumuoto                                       |
|                                                  |                       | ISO20022-tilisiirto                          | Eurooppalainen SEPA-tilisiirtomuoto                             |
|                                                  |                       | ISO20022-tilisiirto (FR)                     | Ranskan SEPA-tilisiirtomuoto                             |
|                                                  |                       | ISO20022-tilisiirto (DE)                     | Saksan SEPA-tilisiirtomuoto                            |
|                                                  |                       | ISO20022-tilisiirto (NL)                     | Alankomaiden SEPA-tilisiirtomuoto                    |
|                                                  |                       | ISO20022-suoraveloitus                             | Eurooppalainen SEPA-suoraveloitusmuoto                                |
|                                                  |                       | ISO20022-suoraveloitus (FR)                        | Ranskan SEPA-suoraveloitusmuoto                                |
|                                                  |                       | ISO20022-suoraveloitus (DE)                        | Saksan SEPA-suoraveloitusmuoto                               |
|                                                  |                       | ISO20022-suoraveloitus (NL)                        | Alankomaiden SEPA-suoraveloitusmuoto                       |
|                                                  |                       | BACS (UK)                                         | Yhdistyneen kuningaskunnan BACS-toimittajamaksumuoto                  |
| Käänteinen veloitus                                   | Veroilmoitus         |                                                   |                                                                    |
|                                                  |                       | Käänteisen veloituksen myyntiluettelo                         | Käänteisen kulun arvonlisäveroluettelon muoto                                   |
| Hollantilainen XBRL-integraatiomalli                     | XBRL-raportointi        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Alankomaiden Semansys XBRL -vientimuoto                    |
| GAF-malli (MY)                                   | Tilintarkistus       |                                                   |                                                                    |
|                                                  |                       | GAF-tiedosto (MY)                                     | Malesian GAF-muoto                                         |
| Ostoreskontran erääntymisraportti (CN)                         | Toimittajan tietojen analysointi |                                                   |                                                                    |
|                                                  |                       | Ostoreskontran erääntymisraportin muoto (CN)                   | Kiinan ostoreskontran erääntymisraportin muoto                               |
| Toimittajan laskun ilmoitusmalli                 | Toimittajan tietojen analysointi |                                                   |                                                                    |
|                                                  |                       | Toimittajan laskun ilmoitus (IS)                   | Islannin toimittajan laskun ilmoitusmuoto                      |
|                                                  |                       | Toimittajan laskun ilmoitusraportti (IS)            | Islannin toimittajan laskun ilmoitusraportti                      |

## <a name="additional-resources"></a>Lisäresurssit

[Lokalisointivaatimukset – Luo sähköisen raportoinnin määritykset](electronic-reporting-configuration.md)

[Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md)
