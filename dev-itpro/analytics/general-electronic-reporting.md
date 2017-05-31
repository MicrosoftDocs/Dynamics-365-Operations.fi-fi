---
title: "Sähköisen raportoinnin yleiskatsaus"
description: "Artikkeli esittelee sähköisen raportointityökalun. Artikkelissa on tietoja keskeisistä käsitteistä ja sähköisen raportoinnin tukemista skenaarioista. Lisäksi siinä on luettelo muodoista, jotka on suunniteltu osana tätä ratkaisua ja jotka julkaistaan sen osana."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: caa9f4c73f4c6b5b7637b5b012bd9ed3b7dd6392
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-overview"></a>Sähköisen raportoinnin yleiskatsaus

[!include[banner](../includes/banner.md)]


Artikkeli esittelee sähköisen raportointityökalun. Artikkelissa on tietoja keskeisistä käsitteistä ja sähköisen raportoinnin tukemista skenaarioista. Lisäksi siinä on luettelo muodoista, jotka on suunniteltu osana tätä ratkaisua ja jotka julkaistaan sen osana.

Sähköinen raportointi on työkalu, jolla voit määrittää sähköisten asiakirjojen muodon eri maiden ja alueiden säädösten mukaisesti. Sähköinen raportointi mahdollistaa näiden muotojen hallinnan niiden elinkaaren aikana. Voit esimerkiksi ottaa käyttöön uusia säädöksiin perustuvia vaatimuksia ja luoda vaatimusten mukaisia liiketoiminnan asiakirjoja, jotka mahdollistavat sähköisen tiedonsiirron viranomaisten, pankkien ja muiden osapuolien välillä. Sähköinen raportointimoduuli on suunnattu yrityskäyttäjille eikä kehittäjille. Koska määritykset koskevat muotoja eikä koodia, sähköisten asiakirjojen muotojen käsittely- ja säätöprosessi on nopeaa ja helppoa. Sähköinen raportointi tukee tällä hetkellä TXT-, XML- ja OPENXML-muotoisia laskentataulukkoja. Laajennettu liittymä tukee kuitenkin myös muita muotoja.

## <a name="capabilities"></a>Toiminnot
Sähköisessä raportointimoduulissa on seuraavat toiminnot:

-   Se on yksi yhteinen, eri toimialueilla toimiva sähköisen raportoinnin työkalu, joka korvaa yli 20 erilaista Microsoft Dynamics 365 for Operationsin sähköisen raportoinnin moduulia.
-   Se eristää raportin muodon tällä hetkellä käyttöönotetusta Dynamics 365 for Operationsista. (Toisin sanoen muotoa voi käyttää Microsoft Dynamics 365 for Operationsin eri versioissa.)
-   Se tukee alkuperäiseen muotoon perustuvan mukautetun muodon luontia. Sen toiminnoilla voi päivittää automaattisesti mukautetut muodot, kun alkuperäiseen muotoon on tehty muutoksia. Tämä onnistuu uusien lokalisointi- ja mukautusvaatimusten avulla.
-   Siitä tulee ensisijainen vakiotyökalu lokalisointivaatimusten tukemiseen sähköisessä raportoinnissa – sekä Microsoftille että sen kumppaneille.
-   Se tukee mahdollisuutta jakaa muotoja kumppaneille ja asiakkaille Microsoft Dynamics Lifecycle Services (LCS) -palveluissa.

## <a name="concepts"></a>Käsitteet
### <a name="components"></a>Komponentit

Sähköinen raportointi tukee kahdenlaisia osia: **tietomalleja**ja **muotoa**.

#### <a name="data-model-components"></a>Tietomalliosat

Tietomalliosa on yrityksen tietyn toimialueen tietorakenteen abstrakti kuvaus, joka on riittävän yksityiskohtainen tämän toimialueen raportointivaatimuksiin. Tietomalliosassa on seuraavat osat:

-   Tietomalli joukkona toimialuekohtaisia liiketoimintayksiköitä ja rakenteeltaan hierarkkinen määritys kyseisten yksiköiden välisistä suhteista.
-   Mallin yhdistämismääritykset, jotka linkittävät valitut Microsoft Dynamics 365 for Operations -tietolähteet yksittäisiin tietomallin elementteihin ja jotka määrittävät suorituksenaikaisen tiedonkulun ja säännöt liiketoiminnan tietojen täyttämiseen tietomalliosassa.

Tietomallin liiketoimintayksikkö ilmaistaan säilönä (tietue). Liiketoimintayksikön ominaisuudet esitetään tietokohteina (kentät). Kullakin tiedolla on yksilöllinen nimi, otsikko, kuvaus ja arvo. Kunkin tiedon arvo voidaan suunnitella tunnistettavaksi esimerkiksi merkkijonona, kokonaislukuja, reaalilukuna, päivämääränä, valintalistan tyyppinä tai totuusarvona. Se voi olla myös toinen tietue tai tietueluettelo. Yksittäinen tietomalli voi sisältää useita toimialuekohtaisten liiketoimintayksiköiden hierarkioita sekä mallien yhdistämismäärityksiä, jotka tukevat tiettyä suorituksenaikaista raporttikohtaista tiedonkulkua. Hierarkiat erotellaan sen yksittäisen tietueen perusteella, joka on valittu mallien yhdistämisen juureksi. Esimerkiksi maksutoimialueen alueen tietomalli voi tukea seuraavia yhdistämismäärityksiä:

-   Yritys -&gt; Toimittaja -&gt; AP-toimialueen maksutapahtumat
-   Asiakas -&gt; Yritys -&gt; AR-toimialueen maksutapahtumat

Huomaa, että liiketoimintayksiköt (kuten yritys ja tapahtumat) suunnitellaan kerran. Eri yhdistämismääritykset ja käytä niitä sitten uudelleen. Mallin yhdistämismäärityksessä on seuraavat toiminnot:

-   Se voi käyttää Dynamics 365 for Operationsin tietotyyppejä tietomallina. Se voi käyttää esimerkiksi taulukoita, tietoyksiköitä, menetelmiä tai valintaluetteloita.
-   Se tukee käyttäjän syöttöparametreja, jotka voidaan määrittää tietomallin tietolähteiksi, kun osa tiedoista on määritettävä suorituksen aikana.
-   Se tukee Dynamics 365 for Operationsin tietojen muuntamista pakollisiksi ryhmiksi, suodatusta, lajittelua ja summatietoja sekä sellaisten loogisten laskentakenttien liittämistä, jotka on suunniteltu Microsoft Excelin kaltaisilla kaavoilla. (Lisätietoja on artikkelissa [Sähköisen raportoinnin kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md).)

[![Excelin kaltainen lomake-editori](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Tietomalliosa on suunniteltu käytettäväksi kullakin liiketoiminnan toimialueella yhtenäisenä tietolähteenä raportoinnissa, joka eristää raportoinnin Microsoft Dynamics 365 for Operationsin tietolähteiden fyysisestä toteuttamisesta sekä kuvaa toimialuekohtaisia liiketoimintakonsepteja ja toimintoja muodossa, joka tehostaa raportointimuotojen alkusuunnittelua ja sen jälkeisestä ylläpitoa.

#### <a name="format-components"></a>Muoto-osat

Muoto-osa on raporttitulostuksen malli, joka luodaan suorituksen aikana. Malli sisältää seuraavat elementit:

-   Muoto, joka määrittää suorituksen aikana luodun sähköisen raportoinnin asiakirjan rakenteen ja sisällön.
-   Tietolähteet käyttäjän syöttöparametrijoukkona ja valittua tiedon yhdistämismääritystä käyttävänä toimialuekohtaisena tietomallina.
-   Muodon yhdistämismääritys muodon tietolähteen sidosjoukkona, jolla on sellaisia muodon yksittäisiä elementtejä, jotka määrittävät suorituksen aikana tiedonkulun ja tulostusmuodon luontisäännöt.
-   Muodon vahvistus määritettävänä sääntöjoukko, jolla hallitaan suorituksenaikaista raportin luontia suorituskontekstin mukaan. (Sääntö voi esimerkiksi pysäyttää toimittajan maksujen tulostuksen luonnin ja aiheuttaa poikkeuksen, kun tietyt valitun toimittajan määritteet, kuten pankkitilin numero puuttuvat.)

Muoto-osa tukee seuraavia toimintoja:

-   Raporttitulostuksen luonti yksittäisinä, erimuotoisina tiedostoina: teksti, XML tai laskentataulukko.
-   Useiden tietojen luonti erikseen sekä kyseisten tiedostojen kerääminen zip-tiedostoihin.

Muoto-osa mahdollistaa tiettyjen raporttitulostuksessa käytettävien tiedostojen liittämisen.

-   OPENXML-laskentataulukkomuodossa tulostusmallina käytettävän laskentataulukon sisältävät Excel-laskentataulukot.
-   Muut tiedostot, jotka voidaan sisällyttää muodon tulostukseen etukäteen määritettyinä tiedostoina.

#### <a name="component-versioning"></a>Komponenttien versionhallinta

Sähköisissä raportointiosissa tuetaan versionhallintaa. Sähköisissä raportointiosissa muutoksia hallitaan seuraavalla työnkululla:

-   Ensimmäisenä luotu versio merkitään **LUONNOS**-versioksi. Tätä versiota voidaan muokata ja sillä voi suorittaa testiajoja.
-   **LUONNOS**-versio voidaan muuntaa **VALMIS**-versioksi. Tätä versiota voidaan käyttää paikallisissa raportointiprosesseissa.
-   **VALMIS**-versio voidaan muuntaa **JAETTU**-versioksi. Tämä versio julkaistaan LCS:ssä ja sitä voidaan käyttää yleisissä raportoinnin prosesseissa.
-   **JAETTU**-versio voidaan muuntaa **LOPETETTU**-versioksi. Tämä versio voidaan sitten poistaa.

Versioita, joiden tila on joko **VALMIS** tai **JAETTU**, voidaan käyttää muissa tiedonsiirroissa. Jos osalla on jompikumpi näistä tiloista, siinä voidaan suorittaa seuraavat toimet:

-   Ne voidaan sarjoittaa XML-muodossa ja viedä Dynamics 365 for Operationsista XML-muotoisena tiedostona.
-   Ne voivat sarjoittaa uudelleen XML-tiedostosta ja tuoda Dynamics 365 for Operationsiin sähköisen raportointiosan uutena versiona.

#### <a name="component-date-effectivity"></a>Komponentin päivämäärän voimassaolo

Sähköisen raportointiosan versioilla on voimassaolopäivämäärät. Sähköiselle raportointiosalle voidaan määrittää**Voimaantulopäivä**määrittämään päivä, josta lähtien tämä osa on voimassa raportointiprosesseissa. Dynamics 365 for Operationsin istunnon päivämäärää käytetään määrittämään, onko komponentti suoritettavissa. Jos tiettynä päivänä on voimassa useampia kuin yksi versio, viimeisintä versiota käytetään raportointiprosessissa.

#### <a name="component-access"></a>Komponenttien käyttöoikeudet

Sähköisten raportointiosien käyttöoikeus määräytyy maan/alueen ISO-koodiasetuksista. Jos tämä asetus on tyhjä muotomääritysten valitussa versiossa, muoto-osaa voidaan käyttää suorituksenaikainen missä tahansa Dynamics 365 for Operations -yrityksessä. Jos asetuksessa on ISO-maa-/aluekoodeja, muoto-osia voidaan käyttää vain niissä Dynamics 365 for Operations -yrityksissä, joiden ensisijainen osoite on määritetty joksikin muoto-osan ISO-maa-/aluekoodiksi. Tietomuoto-osien eri versioilla voi olla erilaiset ISO-maa/aluekoodeja koskevat asetukset.

#### <a name="configuration"></a>Määritys

Sähköiset raportointimääritykset ovat tietyn sähköisen raportointiosan paketointi, joka voi olla joko **Tietomalli**tai **Muoto**. Määritykset voivat sisältää eri versioita tietystä sähköisen raportointiosasta. Jokainen konfiguraatio merkitään tietyn konfiguraation tekijän omistamaksi. Määritysten osan **LUONNOS**-versiota voidaan muokata, jos kyseisten määritysten omistaja on valittu Dynamics 365 for Operationsin sähköisten raportointiasetusten aktiiviseksi lähteeksi. Kussakin mallimäärityksessä on **Tietomalli**-osa. Uusien muotomääritysten alkuperä (josta määritykset johdetaan) voi olla tietty tietomallin määritys. Luotu määritysmuoto tulee määrityspuuhun alkuperäisten tietomallin määritysten alikohde. Luodussa muotomäärityksessä on **Muoto**-osa. Alkuperäisten mallimääritysten **Tietomalli**-osa lisätään automaattisesti alimuodon määritykseen **Muoto**-osaan oletustietolähteenä. Sähköiset raportointimääritykset jaetaan Dynamics 365 for Operations -yrityksille.

#### <a name="provider"></a>Tarjoaja

Sähköinen raportointipalvelu on osapuolen tunniste, jota ilmaistaan sähköisten raportointimääritysten tekijä (omistaja). Voit hallita sähköisen raportoinnin avulla määrityspalvelujen luetteloa. Sähköisille asiakirjoille Dynamics 365 for Operations -ratkaisun osana julkaistujen muotomääritysten omistajaksi merkitään **Microsoftin** määrityspalvelu.

#### <a name="repository"></a>Säilö

Sähköiset raportointimääritykset tallennetaan sähköisen raportoinnin säilöön. Tällä hetkellä tuetaan seuraavia sähköisen raportointisäilöjen tyyppejä: **Operations-resurssi**ja **LCS-projekti**. **Operations-resurssien** säilö tarjoaa mahdollisuuden käyttää määritysluetteloa, jonka Microsoft julkaisee Dynamics 365 for Operations -ratkaisun osana sähköisenä raportointipalveluna. Nämä määritykset voidaan tuoda nykyiseen Dynamics 365 for Operationsin esiintymään ja niitä voidaan käyttää sähköisessä raportoinnissa. Niitä voidaan käyttää myös muissa lisälokalisoinneissa ja -mukautuksissa. **LCS-projektin**säilö tarjoaa mahdollisuuden käyttää tietyn LCS-projektin (LCS-projektiresurssikirjaston) määritysluetteloa, joka valittiin säilön rekisteröintivaiheessa. Sähköinen raportointi mahdollistaa jaettujen määritysten latausta nykyisestä Dynamics 365 for Operationsin esiintymästä tiettyyn **LCS-projektin**säilöön. Voit myös tuoda määrityksiä tietystä **LCS-projektin** säilöstä nykyiseen Dynamics 365 for Operationsin esiintymään. Vaaditut **LCS-projektin**säilöt voidaan rekisteröidä erikseen kullekin nykyisen Dynamics 365 for Operationsin esiintymän määrityspalvelulle. Kukin säilö voidaan osoittaa tiettyyn määrityspalveluun.

## <a name="supported-scenarios"></a>Tuetut skenaariot
### <a name="building-a-data-model"></a>Tietomallin rakentaminen

Sähköisessä raportoinnissa on mallin suunnittelutoiminto, jolla voit luoda tietyn liiketoiminnan toimialueen tietomallin. Kaikki tietomallikohtaiset liiketoimintayksiköt ja niiden väliset suhteet voidaan esittää tietomallissa hierarkkisena rakenteena. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallista (maksutoimialueen tietomalli). [![Esimerkki tietomallista](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin suunnittelutoimialuekohtainen tietomalli** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="translating-data-model-content"></a>Tietomallin sisällön kääntäminen

Tietomallin sisältö (otsikot ja kuvaukset) voidaan kääntää muille Dynamics 365 for Operationsin tukemille kielille. Tietomallin sisältö voidaan haluta kääntää seuraavista syistä:

-   Suunnitteluvaiheessa, jotta sisältö olisi paremmin sellaisten vieraskielisten muodon suunnittelijoiden ymmärrettävissä, jotka käyttävät tietomallia muoto-osien tietojen yhdistämismäärityksiin.
-   Suorituksenaikana, jotta sisällön käyttö olisi kätevämpää, kun kehotteet ja suoritustenaikaisten parametrien ohje sekä määritetyt tarkistussanomat (virheet ja varoitukset) näytetään Dynamics 365 for Operationsiin kirjautuneen käyttäjän ensisijaisella kielellä.

Seuraavassa kuvassa on esimerkki tietomallin sisällön kääntämisestä englannista japaniksi. [![Tietomallin sisältö englanniksi](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Tietomallin sisältö on käännettynä japaniksi](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Tietomallien yhdistämisen konfigurointi

Sähköiseen raportointiin sisältyy mallin yhdistämismääritysten suunnittelutoiminto, jolla käyttäjät voivat tehdä yhdistämismäärityksiä malleihin, jotka he ovat suunnitelleet tiettyihin Dynamics 365 for Operationsin tietolähteisiin. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin yhdistämismäärityksestä (**SEPA-tilisiirto**-mallin maksutoimialueen tietomallin yhdistämismääritys). [![Esimerkki tietomallin määrityksestä](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen ja tietolähteiden valinta**- ja **Sähköisen raportoinnin tietomallin yhdistämismääritysten tekeminen valittuihin tietolähteisiin** -tehtäväoppaat (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Suunnitellun malliosan tallentaminen mallimäärityksinä

Sähköinen raportointi voi tallentaa suunnitellun tietomallin yhdessä liitettyjen tietojen yhdistämismääritysten kanssa nykyisen Dynamics 365 for Operationsin esiintymän mallimäärityksinä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin määrityksestä (maksumallin määritykset). [![Esimerkki tietomallin määrityksestä](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Tutustu skenaarion tietoihin toistamalla **Sähköisen raportointi – yhdistä tietomalli valittuihin tietolähteisiin** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tietomallia perusteena käyttävän muodon muodostaminen

Sähköinen raportointi tukee muodon suunnittelutoimintoa, jolla voit muodostaa valitulle liiketoiminnan toimialueelle tietyn sähköisen asiakirjan muodon valitsemalla malliosan pohjaksi. Sama sähköisen raportoinnin muodon suunnittelutoiminto mahdollistaa luodun muodon yhdistämismäärityksen tekemisen valitun toimialueen tietomallin yhdistämismäärityksen tietolähteenä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta (Yhdistyneen kuningaskunnan **BACS**-maksumuotoa tukeva muotomääritys). [![Esimerkki muodosta, jonka pohjana on tietomalli](./media/pic-format-1024x690.png)](./media/pic-format.png) Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin suunnittelun toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML-laskentataulukkomuodossa luotavien sähköisten asiakirjojen määritysten muodostaminen

Sähköisen raportoinnin muotoilun suunnittelutoiminnolla voidaan muodostaa tietty OPENXML-laskentataulukkomuotoinen sähköinen asiakirja. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta (muotomääritys, jolla luodaan valitun maksukirjauskansion tietoja sisältävä OPENXML-laskentataulukko):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin OPENXML-muotoisten raporttimääritysten luonti** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia). Käytä jäljempänä mainittavaa Excel-tiedostoa sähköisen raportointimuodon suunnittelussa, jotta voit suorittaa loppuun tämän tehtäväoppaan muotomallin tuontimallin: [Maksuraportin malli (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Suunnitellun muoto-osan tallentaminen muotomäärityksenä

Suunniteltu muoto voidaan tallentaa sähköisessä raportoinnissa yhdessä määritettyjen tietojen yhdistämismääritysten kanssa nykyisen Dynamics 365 for Operations -esiintymän muotomäärityksenä. Edeltävässä kuvassa on esimerkki tämän tyyppisestä muotomäärityksestä (**BACS (UK)** on **Maksumalli**-määrityksen alikohde). Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Dynamics 365 for Operationsin määrittäminen käyttämään luotua muotoa sisäisesti

Dynamics 365 for Operations voidaan määrittää aloittamaan luodun muodon käyttö sähköisten raporttien luomiseksi. Luodun muotomäärityksen viite on määritettävä tietyn toimialueen asetuksissa. Jos esimerkiksi halutaan aloittaa BACS-muotoisten sähköisten toimittajamaksujen sähköisen raportointimuodon määritysten käyttö, muotomääritykseen on viitattava maksutapakohtaisesti, kuten seuraavissa kuvissa: 

[![BACS (UK) -muodon määritykset](media/ger-bacs-uk-format-configuration.png) 

[![Viittaus BACS (UK) -muotoon maksutavassa](media/ger-bacs-uk-format-method.png) 

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon käyttö sähköisen asiakirjan luonti maksuja varten** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

## <a name="handling-er-components"></a>Sähköisten raportointien osien käsittely
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Sähköisten raportointiosan tarjoaminen ulkoiseen käyttöön (lokalisointi) julkaisemalla se LCS:ssä

Luodun osan (malli tai muoto) omistaja voi julkaista osan valmiin version LCS:ssä sähköisen raportoinnin avulla. Edellytetään nykyisen sähköisen raportoinnin määrityspalvelun **LCS-projektityypin**säilöä. Kun valmiin osaversion tila vaihdetaan tilasta **VALMIS** tilaksi **JAETTU**, tämä versio julkaistaan LCS:ssä. Kun osa on julkaistu LCS:ssä, kyseisen osan omistajasta tulee osan tuen palvelutarjoaja. Jos esimerkiksi tämä muoto-osa on suunniteltu luomaan lakisääteisiä sähköisiä asiakirjoja (esimerkiksi lokalisointiskenaarion mukaisesti), oletetaan, että muoto pidetään lakimuutosten mukaisena ja että palvelu julkaisee osasta uusia versioita aina, kun on uusia lakisääteisiä vaatimuksia tulee. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen lataaminen Lifecycle Servicesiin**-tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Sähköisen raportointiosan tuonti LCS:stä sisäistä käyttöä varten

Voit tuoda sähköisessä raportoinnissa sähköisiä raportointiosia LCS:stä nykyiseen Dynamics 365 for Operations -esiintymään. Tämä edellyttää **LCS-projektityypin**säilöä. Kun sähköinen raportointiosa on tuotu LCS:stä nykyiseen Dynamics 365 for Operations -esiintymään, tämän Dynamics 365 for Operations -esiintymän omistajasta tulee tuodun osan omistajan (laatijan) tarjoaman palvelun kuluttaja. Jos esimerkiksi tämä muoto-osa on suunniteltu luomaan Dynamics 365 for Operationsissa määritettyjä sähköisiä asiakirjoja tietyssä maa-/aluekohtaisessa muodossa (lokalisointiskenaario), oletetaan, että palvelun kuluttaja pystyy hankkimaan kaikki tähän muotoon tehdyt päivitykset, jotta se pysyy lakisääteisten vaatimusten mukaisena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen tuonti Lifecycle Servicesistä** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Muodon rakentaminen toisen muodon pohjalta (mukauttaminen)

Voit luoda (johtaa) sähköisessä raportoinnissa uuden osan LCS:stä tuodun osan (perustan) nykyisestä versiosta. Käyttäjä voi esimerkiksi haluat johtaa uuden muodon toteuttaakseen jonkin tietyn sähköisen asiakirjan vaatimuksen (kuten lisäkentän tai laajan kuvauksen) mukautusskenaarion tukena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön sen perusversio** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Muodon päivittäminen valitsemalla perusmuodon uusi versio (pohjustus)

Voit ottaa sähköisessä raportoinnissa automaattisesti käyttöön viimeisimpään perusosaan versioon tehdyt muutokset nykyisessä johdetun osan luonnosversiossa. Tätä prosessia kutsutaan *pohjustamiseksi*. Esimerkiksi LCS:stä tuodun muodon uusimpaan versioon tehdyt lakisääteiset muutokset voidaan yhdistää automaattisesti tämän sähköisen asiakirjan muodon mukautettuun versioon. Muutoksia, joita ei voi yhdistetään automaattisesti, pidetään ristiriitoina. Nämä ristiriidat jätetään ratkaistavaksi manuaalisesti kyseisen osan suunnittelutyökaluun. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön sen perusversio** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Dynamics 365 for Operations -ratkaisuun toimitettavien sähköisten raportointimääritysten luettelo
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



<a name="see-also"></a>Lisätietoja
--------

[Lokalisointivaatimukset – Luo sähköisen raportoinnin määritykset](electronic-reporting-configuration.md)

[Sähköisen raportoinnin konfiguraatioiden elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md)




