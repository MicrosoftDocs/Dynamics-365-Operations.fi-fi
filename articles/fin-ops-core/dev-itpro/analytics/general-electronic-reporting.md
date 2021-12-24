---
title: Sähköisen raportoinnin (ER) yleiskatsaus
description: Tässä aiheessa on sähköisen raportointityökalun yleiskatsaus. Siinä käsitellään keskeisiä käsitteitä, tuettuja skenaarioita ja muotoja, jotka osa ratkaisua.
author: NickSelin
ms.date: 11/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b772acd4a8d0849803cefa8fc14ae3dd6e18831
ms.sourcegitcommit: ac23a0a1f0cc16409aab629fba97dac281cdfafb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/29/2021
ms.locfileid: "7867277"
---
# <a name="electronic-reporting-er-overview"></a>Sähköisen raportoinnin (ER) yleiskatsaus

[!include [banner](../includes/banner.md)]

Tämä aihe esittelee sähköisen raportointityökalun. Artikkelissa on tietoja keskeisistä käsitteistä ja sähköisen raportoinnin tukemista skenaarioista. Lisäksi siinä on luettelo muodoista, jotka on suunniteltu osana tätä ratkaisua ja jotka julkaistaan sen osana.

ER on konfiguroitavissa oleva työkalu, jonka avulla voit luoda ja ylläpitää säännöstenmukaista sähköistä raportointia ja maksuja. Se perustuu seuraaviin kolmeen käsitteeseen:

- Konfigurointi koodauksen asemesta:

    - Konfiguroinnin voi tehdä yrityskäyttäjä, eikä se edellytä kehittäjää.
    - Tietomalli on määritetty liiketoiminnassa.
    - Visuaalisia editoreja käytetään kaikkien ER-konfiguraation komponenttien luomiseen.
    - Tietojen muuntamisessa käytettävä kieli muistuttaa Microsoft Excel -kohteessa käytettävää kieltä.

- Yksi konfiguraatio useita Dynamics 365 Finance -julkaisuja varten:

    - Hallitse yhtä liiketoimintaehtona määritettyä toimialuekohtaista tietomallia.
    - Sen julkaisutiedot vapautumiseen sidonnaisten tietomallien määrityksissä.
    - Ylläpidä tietomalliin perustuvia nykyisen version useiden julkaisujen yhtä muotoa.

- Helppo tai automaattinen päivitys:

    - Sähköisen raportoinnin konfiguraatioiden versiointia tuetaan.
    - Microsoft Dynamics Lifecycle Services (LCS) -käyttöomaisuuskirjastoa voidaan käyttää ER-konfiguraatioiden tietovarastona versionvaihtoa varten.
    - Alkuperäiseen ER-konfiguraatioon perustuvat paikalliset versiot voidaan ottaa käyttöön aliversioina.
    - ER-konfiguraatiopuu on työkalu, jonka avulla voidaan hallita versioiden riippuvuuksia.
    - Sijaintierot eli delta-konfiguraatiot tallennetaan, jotta alkuperäisen ER-konfiguraation voi päivittää automaattisesti uuteen versioon.
    - Lokalisointiversioiden automaattisen päivityksen yhteydessä löydetyt ristiriidat on helppo ratkaista manuaalisesti.

ER:n avulla voit määrittää sähköisten muotojen rakenteita ja sitten kuvailla, kuinka rakenteet tulee täyttää datan ja algoritmien avulla. Voit käyttää reseptin kieltä, joka muistuttaa tietojen muuntamisen Excel-kieltä. Jotta tietokannan alustaminen olisi määrityksestä hallittavampaa, uudelleenkäyttökelpoista ja muodon muutoksista riippumatta, käyttöön tulee välitietomallimalli. Tämän ansiosta käyttöönottotiedot voidaan piilottaa muotomäärityksestä, ja sitä voidaan käyttää uudelleen useissa muotomäärityksissä.

ER:n avulla voit määrittää sekä saapuvien että lähtevien sähköisten asiakirjojen muodot eri maiden ja alueiden lakisääteisten vaatimusten mukaisesti. Sähköinen raportointi mahdollistaa näiden muotojen hallinnan niiden elinkaaren aikana. Voit esimerkiksi ottaa käyttöön uusia säädöksiin perustuvia vaatimuksia ja luoda vaatimusten mukaisia liiketoiminnan asiakirjoja, jotka mahdollistavat sähköisen tiedonsiirron viranomaisten, pankkien ja muiden osapuolien välillä.

Sähköinen raportointimoduuli on suunnattu yrityskäyttäjille eikä kehittäjille. Koska määritykset koskevat muotoja koodin sijaan, sähköisten asiakirjojen muotojen käsittely- ja muokkausprosessi on nopeaa ja helppoa.

Sähköinen raportointi tukee tällä hetkellä TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel sekä OPENXML-muotoisia laskentataulukkoja.

## <a name="capabilities"></a>Toiminnot

Sähköisessä raportointimoduulissa on seuraavat toiminnot:

- Se on yksi yhteinen, eri toimialueilla toimiva sähköisen raportoinnin työkalu, joka korvaa yli 20 erilaista Finance and Operationsin sähköisen raportoinnin moduulia.
- Se eristää raportin muodon nykyisestä käyttöönotosta. Toisin sanoen muotoa voi käyttää eri versioissa.
- Se tukee alkuperäiseen muotoon perustuvan mukautetun muodon luontia. Sen toiminnoilla voi myös päivittää automaattisesti mukautetut muodot, kun alkuperäiseen muotoon on tehty muutoksia. Tämä onnistuu lokalisointi- ja mukautusvaatimusten avulla.
- Siitä tulee ensisijainen vakiotyökalu lokalisointivaatimusten tukemiseen sähköisessä raportoinnissa – sekä Microsoftille että sen kumppaneille.
- Se tukee mahdollisuutta jakaa muotoja kumppaneille ja asiakkaille Microsoft Dynamics Lifecycle Servicesissä (LCS).

## <a name="key-concepts"></a>Avainkäsitteet

### <a name="main-data-flow"></a>Päätietovirta

[![ER:n päätietovirta.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponentit

ER tukee seuraavia osatyyppejä:

- Tietomalli
- Mallin määritys
- Muoto
- Metatiedot

Lisätietoja on kohdassa [Sähköisen raportoinnin osat](er-overview-components.md).


#### <a name="component-versioning"></a>Komponenttien versionhallinta

Sähköisissä raportointiosissa tuetaan versionhallintaa. Sähköisen raportoinnin komponenteissa muutoksia hallitaan seuraavalla työnkululla:

1. Ensimmäisenä luotu versio merkitään **Luonnos**-versioksi. Tätä versiota voidaan muokata ja sillä voi suorittaa testiajoja.
2. **Luonnos**-versio voidaan muuntaa **Valmis**-versioksi. Tätä versiota voidaan käyttää paikallisissa raportointiprosesseissa.
3. **Valmis**-versio voidaan muuntaa **Jaettu**-versioksi. Tämä versio julkaistaan LCS:ssä ja sitä voidaan käyttää yleisissä raportoinnin prosesseissa.
4. **Jaettu**-versio voidaan muuntaa **Lopetettu**-versioksi. Tämä versio voidaan sitten poistaa.

Versioita, joiden tila on joko **Valmis** tai **Jaettu**, voidaan käyttää muissa tiedonsiirroissa. Seuraavat toimet voidaan suorittaa komponentissa, jolla on nämä tilat:

- Komponentit voidaan sarjoittaa XML-muodossa ja viedä XML-muotoisena tiedostona.
- Komponentti voidaan sarjoittaa uudelleen XML-tiedostosta ja tuoda sovellukseen ER-komponentin uutena versiona.

#### <a name="component-date-effectivity"></a>Komponentin päivämäärän voimassaolo

Sähköisen raportointikomponentin versioilla on voimassaolopäivämäärät. Voit määrittää sähköiselle raportointikomponentille **Voimaantulopäivä**-arvon määrittämään päivän, josta lähtien kyseinen komponentti on voimassa raportointiprosesseissa. Sovellusistunnon päivämäärää käytetään määrittämään, voiko osan suorittaa. Jos tiettynä päivänä on voimassa useampia kuin yksi versio, viimeisintä versiota käytetään raportointiprosessissa.

#### <a name="component-access"></a>Komponenttien käyttöoikeudet

Sähköisten raportointiosien käyttöoikeus määräytyy maan/alueen ISO-koodiasetuksista. Jos tämä asetus on tyhjä muotomääritysten valitussa versiossa, muoto-osaa voidaan käyttää suorituksenaikainen missä tahansa yrityksessä. Jos asetuksessa on ISO-maa-/aluekoodeja, muoto-osia voidaan käyttää vain niissä yrityksissä, joiden ensisijainen osoite on määritetty joksikin muoto-osan ISO-maa-/aluekoodiksi.

Tietomuoto-osien eri versioilla voi olla erilaiset ISO-maa/aluekoodeja koskevat asetukset.

#### <a name="configuration"></a><a name="Configuration"></a>Määritys

Sähköinen raportointimääritys on tietyn sähköisen raportointikomponentin paketoija. Kyse voi olla joko tietomallikomponentista tai muotokomponentista. Määritykset voivat sisältää sähköisen raportointikomponentin eri versioita. Kukin määritys merkitään tietyn määrityslähteen omistamaksi. Määritysten osan **Luonnos**-versiota voidaan muokata, jos kyseisten määritysten omistaja on valittu sovelluksen sähköisten raportointiasetusten aktiiviseksi lähteeksi.

Kussakin mallimäärityksessä on tietomallikomponentti. Uusien muotomääritysten alkuperä voi olla tietty tietomallimääritys. Luotu määritysmuoto tulee näkyviin määrityspuuhun alkuperäisen tietomallimääritysten alikohteena.

Luodussa muotomäärityksessä on muotokomponentti. Alkuperäisten mallimääritysten tietomallikomponentti lisätään automaattisesti alimuodon muotokomponentin määritykseen oletustietolähteenä.

Sähköiset raportointimääritykset jaetaan sovelluksen yrityksille.

#### <a name="provider"></a><a name="Provider"></a>Palvelu

Sähköinen raportointipalvelu on osapuolen tunniste, jota ilmaistaan sähköisten raportointimääritysten tekijä (omistaja). Voit hallita sähköisen raportoinnin avulla määrityspalvelujen luetteloa. Sähköisille asiakirjoille Finance and Operations -ratkaisun osana julkaistujen muotomääritysten omistajaksi merkitään **Microsoft**-määrityspalvelu.

Lisätietoja uuden sähköisen raportointipalvelun rekisteröimisestä on tehtäväoppaassa **ER Konfiguraation lähteen luominen ja merkitseminen aktiiviseksi** (liiketoimintaprosessin **7.5.4.3 IT-palvelujen ja -ratkaisujen komponenttien hankkiminen ja kehittäminen (10677)** osa).

#### <a name="repository"></a><a name="Repository"></a>Säilö

Sähköiset raportointimääritykset tallennetaan sähköisen raportoinnin säilöön. Tällä hetkellä tuetaan seuraavia ER-säilötyyppejä: 

- Jaettu LCS-kirjasto
- LCS-projekti
- Tiedostojärjestelmä
- RCS
- Operations-resurssit
- Yleinen tietovarasto

**Jaettu LCS-kirjasto** -säilön kautta voi käyttää Lifecycle Servicesin (LCS) jaetun omaisuuskirjaston määritysluetteloa. Tämä ER-rekisterityyppi voidaan rekisteröidä vain Microsoft-palvelulle. Voit tuoda jaetusta LCS-kirjastosta ER-määritysten uusimmat versiot nykyiseen esiintymään.

**LCS-projektin** säilö tarjoaa mahdollisuuden käyttää tietyn LCS-projektin (LCS-projektiresurssikirjaston) määritysluetteloa, joka valittiin, kun säilö rekisteröintiin. Sähköinen raportointi mahdollistaa jaettujen määritysten latauksen nykyisestä esiintymästä tiettyyn **LCS-projektin** säilöön. Voit myös tuoda määrityksiä **LCS-projektin** säilöstä nykyiseen Finance and Operations -sovellukseen.

**Tiedostojärjestelmä**-säilössä on luettelo määrityksistä, jotka sijaitsevat xml-tiedostoina tietyssä sellaisen paikallisen laitteen tietojärjestelmän kansiossa, joka isännöi AOS-palvelua. Tarvittava kansio valitaan säilön rekisteröintivaiheessa. Voit tuoda määrityksiä **Tiedostojärjestelmä**-säilöstä nykyiseen esiintymään. 

Huomaa, että tätä säilötyyppiä voi käyttää seuraavista ympäristöistä:

- kehitystyötä varten käyttöönotetut pilvipalveluympäristöt (jotka sisältävät liitettyjen pakettien testimalleja)
- paikallisesti käyttöön otetut ympäristöt

Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti](./electronic-reporting-import-ger-configurations.md)

**RCS**-säilössä on tietyn esiintymän [Määrityspalvelu (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) -määritysluettelo, joka valittiin säilön rekisteröintivaiheessa. Sähköisen raportoinnin ansiosta voit tuoda valmiita tai jaettuja määrityksiä valitusta RCS-esiintymästä nykyiseen esiintymään, joten voit käyttää niitä sähköisessä raportoinnissa.

Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti RCS:stä](./rcs-download-configurations.md).

**Yleinen tietovarasto** -arkiston avulla voit käyttää [konfigurointipalvelun](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) yleisessä tietovarastossa olevien kokoonpanojen luetteloa. Tämä ER-rekisterityyppi voidaan rekisteröidä vain Microsoft-palvelulle. Voit tuoda yleisestä tietovarastosta ER-määritysten uusimmat versiot nykyiseen esiintymään.

Lisätietoja on kohdassa [Sähköisen raportoinnin konfiguraatioiden tuonti konfiguraatiopalvelun yleisestä säilöstä](./er-download-configurations-global-repo.md).

**Operatiivisten resurssien** säilö antaa mahdollisuuden käyttää määritysluetteloa, jonka Microsoft sähköisen raportoinnin määrityspalveluna julkaisee aluksi sovellusratkaisun osana. Nämä määritykset voidaan tuoda nykyiseen esiintymään sähköistä raportointia tai näytetehtäväoppaisen toistamista varten. Niitä voidaan käyttää myös muissa lisälokalisoinneissa ja -mukautuksissa. Huomaa, että Microsoftin toimittamien sähköisten raportointimääritysten uusimmat versiot on tuotava LCS:n jaetun ominaisuuskirjastosta käyttämällä vastaavaa ER-säilöä.

Tarvittavat **LCS-projekti**-, **Tiedostojärjestelmä**- ja **Sääntöjen konfigurointipalvelu (RCS)** -säilöt voidaan rekisteröidä erikseen kullekin nykyisen esiintymän määrityspalvelulle. Kukin säilö voidaan osoittaa tiettyyn määrityspalveluun.

## <a name="supported-scenarios"></a>Tuetut skenaariot

### <a name="building-a-data-model"></a>Tietomallin rakentaminen

Sähköisessä raportoinnissa on mallin suunnittelutoiminto, jolla voit luoda tietyn liiketoiminnan toimialueen tietomallin. Kaikki tietomallikohtaiset liiketoimintayksiköt ja niiden väliset suhteet voidaan esittää tietomallissa hierarkkisena rakenteena. 

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin suunnittelutoimialuekohtainen tietomalli** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="translating-data-model-content"></a>Tietomallin sisällön kääntäminen

Tietomallin sisältö (otsikot ja kuvaukset) voidaan kääntää muille sovelluksen tukemille kielille. Tietomallin sisältö voidaan haluta kääntää seuraavista syistä:

- Suunnitteluvaiheessa sitä varten, että sisältö olisi paremmin sellaisten vieraskielisten muodon suunnittelijoiden ymmärrettävissä, jotka käyttävät tietomallia muotokomponenttien tietojen yhdistämismäärityksiin.
- Suorituksenaikana sen vuoksi, että sisällön käyttö olisi kätevämpää, kun kehotteet ja suoritustenaikaisten parametrien ohje sekä määritetyt tarkistussanomat (virheet ja varoitukset) näytetään kirjautuneen käyttäjän ensisijaisella kielellä.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Lähtevien asiakirjojen tietomallin yhdistämismääritysten määrittäminen

Sähköiseen raportointiin sisältyy mallin yhdistämismääritysten suunnittelutoiminto, jolla käyttäjät voivat tehdä yhdistämismäärityksiä malleihin, jotka he ovat suunnitelleet tiettyihin sovelluksen tietolähteisiin. Tiedot tuodaan suorituksen aikana yhdistämismäärityksen mukaisesti valituista tietolähteistä tietomalliin. Tietomallia käytetään sitten lähteviä sähköisiä asiakirjoja luovien sähköisten raportointimuotojen abstraktina tietolähteenä. 

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin mallin yhdistämismäärityksen määrittäminen ja tietolähteiden valinta**- ja **Sähköisen raportoinnin tietomallin yhdistämismääritysten tekeminen valittuihin tietolähteisiin** -tehtäväoppaat (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Saapuvien asiakirjojen tietomallin yhdistämismääritysten määrittäminen

Sähköiseen raportointiin sisältyy mallin yhdistämismääritysten suunnittelutoiminto, jolla käyttäjät voivat tehdä yhdistämismäärityksiä tiettyihin kohteisiin suunniteltuihin tietomalleihin. Tietomallien yhdistämismääritys voidaan esimerkiksi tehdä päivitettäviin tietokomponentteihin (tauluihin, tietoyksiköihin ja näkymiin). Tiedot päivitetään yhdistämismääritysten perusteella suorituksen aikana tietomallin tiedoilla. Tietomalli täytetään sähköisen tietomallimuodon abstraktina tallennuksena saapuvasta sähköisestä asiakirjasta tuotavilla tiedoilla. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Suunnitellun malliosan tallentaminen mallimäärityksinä

Sähköinen raportointi voi tallentaa suunnitellun tietomallin yhdessä liitettyjen tietojen yhdistämismääritysten kanssa nykyisen esiintymän mallimäärityksinä. Seuraavassa kuvassa on esimerkki tämän tyyppisestä tietomallin määrityksestä (maksumallin määritykset).

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin tietomallin yhdistämismääritysten tekeminen valittuihin tietolähteisiin** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Tietomallia perusteena käyttävän muodon muodostaminen

Sähköinen raportointi tukee muodon suunnittelutoimintoa, jolla voit muodostaa valitulle liiketoiminnan toimialueelle sähköisen asiakirjan muodon valitsemalla pohjaksi mallikomponentin. Sama sähköisen raportoinnin muodon suunnittelutoiminto mahdollistaa luodun muodon yhdistämismäärityksen tekemisen valitun toimialueen tietomallin yhdistämismäärityksen tietolähteenä. 

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>OPENXML-laskentataulukkomuodossa luotavien sähköisten asiakirjojen määritysten muodostaminen

Sähköisen raportointimuodon suunnittelutoiminnolla voidaan muodostaa OPENXML-laskentataulukon muotoinen sähköinen asiakirja. 

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin OPENXML-muotoisten raporttimääritysten luonti** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia). Käytä tehtäväoppaan mallin tuontivaiheessa mallina Excel-tiedostoa [Maksuraportin malli (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Word-asiakirjan muodossa luotavien sähköisten asiakirjojen määritysten muodostaminen

Sähköisen raportointimuodon suunnittelutoiminnolla voidaan muodostaa Word-asiakirjan muotoinen sähköinen asiakirja. Seuraavassa kuvassa on esimerkki tämän tyyppisestä muodosta. Huomaa, että tämä muoto käyttää uudelleen aiemmin luotuja sähköisen raportoinnin määrityksiä, jotka suunniteltiin alun perin suunniteltu luomaan raportti OPENXML-muodossa.

Tutustu skenaarion tietoihin toistamalla Sähköisen raportoinnin Micrsoft Word -muotoisten raporttimääritysten suunnittelu -tehtäväopas (liiketoimintaprosessin osa 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)). Käytä tehtäväoppaan mallin tuontivaiheessa seuraavia Word-tiedostoja sähköisen raportointimuodon malleina:

- [Maksuraportin malli (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Maksuraportin sidottu malli (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Saapuvien sähköisten asiakirjojen tietojen tuontimääritysten muodostaminen

Sähköisen raportointimuodon suunnittelutoiminnolla voi kuvata sähköisen asiakirjan, jolla tietoja aiotaan tuoda joko XML- tai tekstimuodossa. Saapuva tiedosto jäsennetään suunnitellulla muodolla. Sähköisen raportointimuodon yhdistämismäärityksen suunnittelutoiminnoilla voidaan määrittää, miten suunnitellun muodon elementit sidotaan tietomalliin. 

Tutustu skenaarion tietoihin toistamalla Tarvittavien sähköisen raportoinnin määritysten luonti tietojen tuontiin ulkoisesta tiedostosta -tehtäväopas (liiketoimintaprosessin osa 7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)). Toista opas käyttämällä seuraavia tiedostoja:

- [Sähköisen raportoinnin tietomallien määritys (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [Sähköisen raportointimuodon määritys (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Malli saapuvasta XML-muotoisesta asiakirjasta (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Saapuvan asiakirjan tietojen hallinnan työkirjamalli (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Suunnitellun muoto-osan tallentaminen muotomäärityksenä

Suunniteltu muoto voidaan tallentaa sähköisessä raportoinnissa yhdessä määritettyjen tietojen yhdistämismääritysten kanssa nykyisen esiintymän muotomäärityksenä. Edeltävässä kuvassa on esimerkki tämän tyyppisestä muotomäärityksestä (**BACS (UK)** on **Maksumalli**-määrityksen alikohde). Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin toimialuekohtainen muoto** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Financen määrittäminen käyttämään luotua muotoa sisäisesti

Sovellus voidaan määrittää aloittamaan luodun muodon käyttö sähköisten raporttien luomiseksi. Luodun muotomäärityksen viite on määritettävä tietyn toimialueen asetuksissa. Jos esimerkiksi halutaan aloittaa BACS-muotoisten sähköisten toimittajamaksujen sähköisen raportointimuodon määritysten käyttö, muotomääritykseen on viitattava maksutapakohtaisesti.

Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon käyttö sähköisen asiakirjan luonti maksuja varten** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

## <a name="handling-er-components"></a>Sähköisten raportointien osien käsittely

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Sähköisten raportointiosan tarjoaminen ulkoiseen käyttöön (lokalisointi) julkaisemalla se LCS:ssä

Luodun osan (malli tai muoto) omistaja voi julkaista osan valmiin version LCS:ssä sähköisen raportoinnin avulla. Edellytetään nykyisen sähköisen raportoinnin määrityspalvelun **LCS-projektityypin** säilöä. Kun valmiin osaversion tila vaihdetaan tilasta **VALMIS** tilaksi **JAETTU**, tämä versio julkaistaan LCS:ssä. Kun osa on julkaistu LCS:ssä, kyseisen osan omistajasta tulee osan tuen palvelutarjoaja. Jos esimerkiksi tämä muoto-osa on suunniteltu luomaan lakisääteisiä sähköisiä asiakirjoja (esimerkiksi lokalisointiskenaarion mukaisesti), oletetaan, että muoto pidetään lakimuutosten mukaisena ja että palvelu julkaisee osasta uusia versioita aina, kun on uusia lakisääteisiä vaatimuksia tulee. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen lataaminen Lifecycle Servicesiin**-tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Sähköisen raportointiosan tuonti LCS:stä sisäistä käyttöä varten

Voit tuoda sähköisessä raportoinnissa sähköisiä raportointiosia LCS:stä nykyiseen esiintymään. Tämä edellyttää **LCS-projektityypin** säilöä. Kun sähköinen raportointikomponentti on tuotu LCS:stä nykyiseen esiintymään, tämän esiintymän omistajasta tulee tuodun osan omistajan (laatijan) tarjoaman palvelun kuluttaja. Jos esimerkiksi tämä muoto-osa on suunniteltu luomaan sovelluksessa määritettyjä sähköisiä asiakirjoja tietyssä maa-/aluekohtaisessa muodossa (lokalisointiskenaario), oletetaan, että palvelun kuluttaja pystyy hankkimaan kaikki tähän muotoon tehdyt päivitykset, jotta se pysyy lakisääteisten vaatimusten mukaisena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin määrityksen tuonti Lifecycle Servicesistä** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Muodon rakentaminen toisen muodon pohjalta (mukauttaminen)

Voit luoda (johtaa) sähköisessä raportoinnissa uuden osan LCS:stä tuodun osan (perustan) nykyisestä versiosta. Käyttäjä voi esimerkiksi haluat johtaa uuden muodon toteuttaakseen jonkin tietyn sähköisen asiakirjan vaatimuksen (kuten lisäkentän tai laajan kuvauksen) mukautusskenaarion tukena. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön sen perusversio** -tehtäväopas (osa **7.5.4.3 IT-palvelu- ja -ratkaisuosien hankinta ja kehittäminen (10677)** -liiketoimintaprosessia).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Muodon päivittäminen valitsemalla perusmuodon uusi versio (pohjustus)

Voit ottaa sähköisessä raportoinnissa automaattisesti käyttöön viimeisimpään perusosaan versioon tehdyt muutokset nykyisessä johdetun osan luonnosversiossa. Tätä prosessia kutsutaan *pohjustamiseksi*. Esimerkiksi LCS:stä tuodun muodon uusimpaan versioon tehdyt lakisääteiset muutokset voidaan yhdistää automaattisesti tämän sähköisen asiakirjan muodon mukautettuun versioon. Muutoksia, joita ei voi yhdistetään automaattisesti, pidetään ristiriitoina. Nämä ristiriidat jätetään ratkaistavaksi manuaalisesti kyseisen osan suunnittelutyökaluun. Tutustu skenaarion tietoihin toistamalla **Sähköisen raportoinnin muodon päivitys ottamalla käyttöön kyseisen muodon perusversio** -tehtäväopas (osa **7.5.5.3 Muutetun IT-palvelu- ja -ratkaisuosan hankinta ja kehittäminen (10683)** -liiketoimintaprosessia).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Luettelo Financessa julkaistuista ER-määrityksistä

Financen ER-määritysten luetteloa päivitetään jatkuvasti. Tällä hetkellä tuettujen ER-määritysten luetteloa voi tarkastella avaamalla [yleisen tietovaraston](er-download-configurations-global-repo.md). **Käytöstä poistamisen tiedot** -pikavälilehdessä voi tarkastella tietoja määrityksistä, jotka on poistettu käytöstä tai joita ei enää ylläpidetä. 

![Yleisen tietovaraston sisällön suodattaminen Konfiguraatiosäilö-sivulla.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Lisäresurssit

- [Sähköisen raportoinnin (ER) määritysten luominen](electronic-reporting-configuration.md)
- [Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
