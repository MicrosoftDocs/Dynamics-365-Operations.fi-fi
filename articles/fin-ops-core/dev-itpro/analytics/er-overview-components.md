---
title: Sähköisen raportoinnin osat
description: Tässä aiheessa käsitellään sähköisen raportoinnin osia.
author: nselin
ms.date: 09/28/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de8bccf5a8a9bb81be51658010ad4c2ef67aabb2
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562246"
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

[![Saapuvien muotokomponenttien tiedonkulku.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Jos haluat tuoda saapuvan sähköisen asiakirjan tietoja suorittamalla sähköisen raportoinnin muotomääritykset, sinun on tunnistettava muotomäärityksen toivotut yhdistämismääritykset ja mallin yhdistämismääritysten integrointikohta. Voit käyttää saman mallin yhdistämismäärityksiä ja kohteita yhdessä erityyppisten saapuvien asiakirjojen erilaisten muotojen kanssa.

## <a name="component-versioning"></a>Komponenttien versionhallinta

Sähköisissä raportointiosissa tuetaan versionhallintaa. Sähköisen raportoinnin komponenteissa muutoksia hallitaan seuraavalla työnkululla:

1. Ensimmäisenä luotu versio merkitään **Luonnos**-versioksi. Tätä versiota voidaan muokata ja sillä voi suorittaa testiajoja.
2. **Luonnos**-versio voidaan muuntaa **Valmis**-versioksi. Tätä versiota voidaan käyttää paikallisissa raportointiprosesseissa.
3. **Valmis**-versio voidaan muuntaa **Jaettu**-versioksi. Tämä versio julkaistaan Microsoft Dynamics Lifecycle Servicesissä (LCS:ssä), ja sitä voidaan käyttää yleisissä raportointiprosesseissa.
4. **Jaettu**-versio voidaan muuntaa **Lopetettu**-versioksi. Tämä versio voidaan poistaa.

Versioita, joiden tila on joko **Valmis** tai **Jaettu**, voidaan käyttää muissa tiedonsiirroissa. Seuraavat toimet voidaan suorittaa komponentissa, jolla on nämä tilat:

- Komponentit voidaan sarjoittaa XML-muodossa ja viedä XML-muotoisena tiedostona.
- Komponentti voidaan sarjoittaa uudelleen XML-tiedostosta ja tuoda sovellukseen ER-komponentin uutena versiona.

## <a name="component-date-effectivity"></a>Komponentin päivämäärän voimassaolo

Sähköisen raportointikomponentin versioilla on voimassaolopäivämäärät. Voit määrittää sähköiselle raportointikomponentille voimaantulopäivämäärän määrittämään päivän, jonka jälkeen kyseinen osa on voimassa raportointiprosesseissa. Sovellusistunnon päivämäärää käytetään määrittämään, voiko osan suorittaa. Jos tiettynä päivänä on voimassa useampia kuin yksi versio, viimeisintä versiota käytetään raportointiprosessissa.

## <a name="component-access"></a>Komponenttien käyttöoikeudet

Sähköisten raportointiosien käyttöoikeus määräytyy maan tai alueen ISO (International Organization for Standardization) -koodiasetuksista. Jos tämä asetus on tyhjä muotomääritysten valitussa versiossa, muoto-osaa voidaan käyttää suorituksenaikainen missä tahansa yrityksessä. Jos asetuksessa on ISO-maa- tai -aluekoodeja, muoto-osia voidaan käyttää vain niissä yrityksissä, joiden ensisijainen osoite on määritetty joksikin muoto-osan ISO-maa- tai -aluekoodiksi.

Tietomuoto-osien eri versioilla voi olla erilaiset ISO-maa/aluekoodeja koskevat asetukset.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

