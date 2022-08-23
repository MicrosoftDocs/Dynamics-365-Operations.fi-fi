---
title: Sähköisen raportoinnin osat
description: Tässä artikkelissa käsitellään sähköisen raportoinnin osia.
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285028"
---
# <a name="electronic-reporting-components"></a>Sähköisen raportoinnin osat

[!include [banner](../includes/banner.md)]

Sähköinen raportointi tukee seuraavia osatyyppejä:

- Tietomalli
- Mallin määritys
- Muoto
- Metatiedot

## <a name="data-model-component"></a>Tietomallin komponentti

Tietomallikomponentti on tietorakenne abstrakti kuvaus. Se kuvailee tietyn yrityksen toimialueen riittävän yksityiskohtaisesti, että se tyydyttää kyseisen toimialueen raportointitarpeet. Tietomalliosassa on seuraavat osat:

- **Tietomalli** – joukko toimialuekohtaisia liiketoimintayksiköitä ja rakenteeltaan hierarkkisia kyseisten yksiköiden välisten suhteiden määrityksiä.
- **Mallin yhdistämismääritykset** – valitut sovelluksen tietolähteet linkitetään yksittäisiin tietomallin elementteihin määrittämään suorituksenaikainen tiedonkulku ja säännöt liiketoimintatietojen täyttämiseen tietomalliosassa.

Tietomallin liiketoimintayksikkö ilmaistaan säilönä tai tietueena. Liiketoimintayksikön ominaisuudet ilmaistaan tietokohteina tai kenttinä. Kullakin tiedolla on yksilöllinen nimi, otsikko, kuvaus ja arvo. Kunkin tietoyksikön arvo voidaan suunnitella tunnistettavaksi merkkijonona, kokonaislukuna, reaalilukuna, päivämääränä, valintalistan tyyppinä tai totuusarvona. Tietoyksikkö voi olla myös toinen tietue tai tietueluettelo.

Yksittäisessä tietomallikomponentissa voi olla useita toimialuekohtaisten liiketoimintayksiköiden hierarkioita. Siinä voi olla myös suorituksenaikaista raporttikohtaista tiedonkulkua tukevia yhdistämismäärityksiä. Hierarkiat erotellaan sen yksittäisen tietueen perusteella, joka on valittu mallien yhdistämisen juureksi. Esimerkiksi maksutoimialueen alueen tietomalli voi tukea seuraavia yhdistämismäärityksiä:


- Yritys \> Toimittaja \> Ostoreskontratoimialueen maksutapahtumat
- Asiakas \> Yritys \> Myyntireskontran toimialueen maksutapahtumat

Liiketoimintayksiköt, kuten yritys ja maksutapahtumat, suunnitellaan vain kerran. Eri yhdistämismääritykset voivat käyttää niitä tarpeen mukaan uudelleen.

## <a name="model-mapping-component"></a>Mallimääritysosa

Mallin yhdistämismääritys linkittää sovelluksen tietolähteet yksittäisiin tietomallin elementteihin määrittämään suorituksenaikainen tiedonkulku ja säännöt liiketoimintatietojen täyttämiseen tietomalliosassa.

Lähteviä sähköisiä asiakirjoja tukevassa mallin yhdistämismäärityksessä on seuraavat ominaisuudet:

- Se voi käyttää eri tietotyyppejä tietomallina. Näitä tietotyyppejä ovat esimerkiksi taulut, tietoyksiköt, menetelmät ja valintaluettelot.
- Se tukee käyttäjän syöttöparametreja, jotka voidaan määrittää tietomallin tietolähteiksi, kun osa tiedoista on määritettävä suorituksen aikana.
- Se tukee tietojen muuntamista tarvittaviksi ryhmiksi. Voit myös suodattaa, lajitella ja summata tietoja sekä loogisia laskettuja kenttiä, jotka on suunniteltu Microsoft Excelin kaavoja muistuttavilla kaavoilla. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kaavojen suunnittelutoiminto](general-electronic-reporting-formula-designer.md).

Saapuvia sähköisiä asiakirjoja tukevassa mallin yhdistämismäärityksessä on seuraavat ominaisuudet:

- Se voi käyttää erilaisia päivitettäviä tietoelementtejä kohteina. Näitä tietoelementtejä ovat esimerkiksi taulut, tietoyksiköt ja näkymät. Tiedot voidaan päivittää saapuvien sähköisten asiakirjojen tiedoilla. Yhdessä mallin yhdistämismäärityksessä voidaan käyttää useita kohteita.
- Se tukee käyttäjän syöttöparametreja, jotka voidaan määrittää tietomallin tietolähteiksi, kun osa tiedoista on määritettävä suorituksen aikana.

Tietomalliosa on suunniteltu käytettäväksi kullakin yrityksen toimialueella raportoinnin yhtenäisenä tietolähteenä. Yhtenäinen tietolähde eristää raportoinnin tietolähteiden fyysisestä toteutuksesta. Osa ilmaisee toimialuekohtaisia liiketoimintakonsepteja ja toimintoja muodossa, joka tehostaa raportointimuotojen alkusuunnittelua ja sen jälkeisestä ylläpitoa.

## <a name="format-component"></a>Muotokomponentti

### <a name="format-components-for-outgoing-electronic-documents"></a>Lähtevien sähköisten asiakirjojen muotokomponentit

Muoto-osa on raporttitulostuksen malli, joka luodaan suorituksen aikana. Malli sisältää seuraavat elementit:

- Muoto, joka määrittää suorituksen aikana luodun lähtevän sähköisen asiakirjan rakenteen ja sisällön.
- Tietolähteet käyttäjän syöttöparametrijoukkona ja valittua tiedon yhdistämismääritystä käyttävänä toimialuekohtaisena tietomallina.
- Muodon yhdistämismääritys muodon tietolähteen sidosjoukkona. Siinä on sellaisia muodon yksittäisiä elementtejä, jotka määrittävät suorituksen aikana tiedonkulun ja tulostusmuodon luontisäännöt.
- Muotomäärityksen vahvistaminen joukkona määritettävissä olevia sääntöjä, jotka ohjaavat raportin luomista suorituksen aikana suoritettavan raportin yhteyden mukaisesti. Sääntö voi esimerkiksi pysäyttää toimittajan maksujen tulostuksen luonnin ja aiheuttaa poikkeuksen, kun tietyt valitun toimittajan määritteet, kuten pankkitilin numero, puuttuvat.

Muoto-osa tukee seuraavia toimintoja:

- Raporttitulostuksen luonti yksittäisinä, erimuotoisina tiedostoina,kuten tekstinä, XML-tiedostona, Microsoft Word -asiakirjana tai laskentataulukkona
- Useiden tiedostojen luonti erikseen sekä kyseisten tiedostojen kerääminen zip-tiedostoihin

Muotokomponentin avulla tietyt raporttitulostuksessa käytettäviä tiedostoja voidaan liittää.

- OPENXML-laskentataulukkomuodossa tulostusmallina käytettävän laskentataulukon sisältävät Excel-laskentataulukot.
- Microsoft Word-asiakirjamuodossa tulostusmallina käytettävän asiakirjan sisältävät Word-tiedostot
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


## <a name="component-versioning"></a>Komponenttien versionhallinta

Sähköisissä raportointiosissa tuetaan versionhallintaa. Sähköisen raportoinnin komponenteissa muutoksia hallitaan seuraavalla työnkululla:

1. Ensimmäisenä luotu versio merkittiin **Luonnos**-versioksi. Tätä versiota voidaan muokata ja sillä voi suorittaa testiajoja.
2. **Luonnos**-versio voidaan muuntaa **Valmis**-versioksi. Tätä versiota voidaan käyttää paikallisissa raportointiprosesseissa.
3. **Valmis**-versio voidaan muuntaa **Jaettu**-versioksi. Tämä versio julkaistaan Microsoft Dynamics Lifecycle Servicesissä (LCS:ssä), ja sitä voidaan käyttää yleisissä raportointiprosesseissa.
4. **Jaettu**-versio voidaan muuntaa **Lopetettu**-versioksi. Tämä versio voidaan poistaa.

Versioita, joiden tila on joko **Valmis** tai **Jaettu**, voidaan käyttää muissa tiedonsiirroissa. Seuraavat toimet voidaan suorittaa komponentissa, jolla on nämä tilat:

- Komponentit voidaan sarjoittaa XML-muodossa ja viedä XML-muotoisena tiedostona.
- Komponentti voidaan sarjoittaa uudelleen XML-tiedostosta ja tuoda sovellukseen ER-komponentin uutena versiona.

Lisätietoja on kohdassa [Uuden tietomallimäärityksen tuominen](er-quick-start1-new-solution.md#ImportDataModel) ja [Johdetun muodon valmiin version vieminen](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Luonnosversiot suorituksen aikana

ER-kehyksen henkilökohtaisissa käyttäjäparametreissasi voit ottaa käyttöön vaihtoehdon, jonka avulla voit määrittää, käytetäänkö ER-konfiguraation luonnosversiota suorituksen aikana. Lisätietoja **Suorita luonnos** -vaihtoehdon käyttöönotosta ER-konfiguraatioissa on kohdassa [Merkitse mukautettu muoto suoritettavaksi](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER-käyttäjän parametrit ovat yritys- ja käyttäjäkohtaisia.

### <a name="draft-format-versions-at-runtime"></a>Luonnosmuotoversiot suorituksen aikana

Kun suoritat ER-ratkaisun, sen muotokomponenttien luonnosversiot ohitetaan oletusarvoisesti. Sen sijaan käytössä on vain asianmukainen versio, jonka tila on muu kuin **Luonnos**. Joskus voit pakottaa ER:n käyttämään ER-muotomäärityksen luonnosversiota suorituksen aikana. Kun olet esimerkiksi olet ottanut käyttöön tarvittavat muutokset luonnosversioon, voit tehdä testisuorituksen tämän luonnosversion avulla. Näin voit vahvistaa muutosten oikeellisuuden. Jos haluat aloittaa luonnosmuotoversion käytön, sinun on [määritettävä](er-quick-start2-customize-report.md#MarkFormatRunnable) ER-konfiguraation **Suorita luonnos** -asetuksen arvoksi **Kyllä**.

### <a name="draft-model-mapping-versions-at-runtime"></a>Malliluonnoksen yhdistämisen versiot suorituksen aikana

Kun suoritat ER-ratkaisun, sen mallin yhdistämismäärityskomponenttien luonnosversioita käytetään aina. Joskus voit pakottaa ER:n ohittamaan ER-malli yhdistämismäärityksen luonnosversion suorituksen aikana. **Versiossa 10.0.29 ja sitä myöhemmässä versiossa** voit ottaa käyttöön **Ota aina huomioon ER-mallin yhdistämismääritysten Suorita luonnos -vaihtoehto** -ominaisuuden, jolla ohjataan suorituksen aikana käytettävää mallin yhdistämisen versiota. Kun tämä ominaisuus on käytössä, tapahtuu seuraavaa:

- Kun **Suorita luonnos** -asetuksena on **Ei** mallin yhdistämismääritykselle, konfiguroinnin suurinta ei-luonnosversiota käytetään suorituksen aikana. Poikkeus annetaan, jos konfiguraatio ei ole käytettävissä nykyisessä Finance-esiintymässä.
- Kun **Suorita luonnos** -asetuksena on **Kyllä** mallin yhdistämismääritykselle, konfiguroinnin luonnosversiota käytetään suorituksen aikana.

## <a name="component-date-effectivity"></a>Komponentin päivämäärän voimassaolo

Sähköisen raportoinnin muotokomponentin versioilla on voimassaolopäivämäärät. Voit määrittää sähköisen raportoinnin muotokomponentille voimaantulopäivämäärän määrittämään päivän, jonka jälkeen kyseinen osa on voimassa raportointiprosesseissa. Sovellusistunnon päivämäärää käytetään määrittämään, voiko osan suorittaa. Jos tiettynä päivänä on voimassa useampia kuin yksi versio, viimeisintä versiota käytetään raportointiprosessissa.

## <a name="component-access"></a>Komponenttien käyttöoikeudet

Sähköisen raportoinnin ja mallimäärityksen osien käyttöoikeus suorituksen aikana määräytyy maan tai alueen ISO (International Organization for Standardization) -koodiasetuksista. Jos tämä asetus on tyhjä muodon tai mallin yhdistämismääritysten valitussa versiossa, muodon tai mallin yhdistämisosaa voidaan käyttää suorituksenaikainen missä tahansa yrityksessä. Jos asetuksessa on ISO-maa- tai -aluekoodeja, muodon tai mallin määrityksen osia voidaan käyttää vain niissä yrityksissä, joiden ensisijainen osoite on määritetty joksikin muoto-osan ISO-maa- tai -aluekoodiksi.

Muodon tai mallin määritysosien eri versioilla voi olla erilaiset ISO-maa/aluekoodeja koskevat asetukset.

Lisätietoja on kohdassa [Maakontekstista riippuvaisten sähköisen raportoinnin mallimääritysten määrittäminen](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

