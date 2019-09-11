---
title: Työaikarekisteröinti – yleiskatsaus
description: Aikarekisteröinnin työntekijät voivat määrittää erityyppisiä ajan rekisteröintejä, joita ovat esimerkiksi saapuminen, poistuminen, epäsuorien toimintojen rekisteröinti sekä poissaolorekisteröinti. Tässä ohjeaiheessa kuvataan rekisteröintejä, niiden laskemista, hyväksyntää sekä työnkulkua, jolla voidaan lisätä rakenne ja automaattinen hyväksyntä työaikaraporttien hyväksyntäprosessiin.
author: ShylaThompson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmWorker, JmgCalcApprovePickDialog, JmgGroupApprove, JmgGroupCalc, JmgGroupSigningTable, JmgRegistration, JmgTimeCalcParmeters, WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 53351
ms.assetid: 885b0cdf-53d7-4cb4-92fe-da1b9e32b39f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e88d64340a7f4963956d1dce3c31f3542cc30f8
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865229"
---
# <a name="time-and-attendance-registration-overview"></a>Työaikarekisteröinti – yleiskatsaus

[!include [banner](../includes/banner.md)]

Aikarekisteröinnin työntekijät voivat määrittää erityyppisiä ajan rekisteröintejä, joita ovat esimerkiksi saapuminen, poistuminen, epäsuorien toimintojen rekisteröinti sekä poissaolorekisteröinti. Tässä ohjeaiheessa kuvataan rekisteröintejä, niiden laskemista, hyväksyntää sekä työnkulkua, jolla voidaan lisätä rakenne ja automaattinen hyväksyntä työaikaraporttien hyväksyntäprosessiin. 

<a name="registrations"></a>Rekisteröitymiset
-------------

Työajan seurantaa käyttävissä yrityksissä työntekijöiden täytyy rekisteröidä työssä käyttämänsä aika sekä läsnäoloaikansa. Joissain yrityksissä työntekijöiden on kirjattava vain saapumis- ja poistumisaika. Muissa yrityksissä työntekijöiden on ehkä rekisteröitävä myös ajankäyttö todellisiin tehtäviin ja taukoihin. Työajan seurannan käyttäjiä ovat yleensä:
-   työntekijät, joiden on rekisteröitävä työajan käyttö säännöllisesti, esimerkiksi päivittäin, viikoittain tai kahden viikon välein
-   esimiehet, päälliköt ja palkanlaskijat, jotka laskevat, hyväksyvät ja siirtävät työntekijän kirjaamat tiedot käsiteltäviksi edelleen.

| **Huomautus**                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jos Työajan seuranta suoritetaan samanaikaisesti Tuotannonohjauksen kanssa, kaikki tuotteita, projektitehtäviä, epäsuoria tehtäviä, poissaolokoodeja, ylityötä ja liukuvaa työaikaa koskevat rekisteröinnit kirjataan järjestelmään ja niitä käytetään palkanlaskennassa molemmissa moduuleissa. |

## <a name="time-registrations-workers"></a> Aikarekisteröinnin työntekijät
Jotta työntekijät voivat kirjata työaikansa, heidät on määritettävä aikarekisteröinnin työntekijöiksi työnantajayrityksessään.

Tämän jälkeen työntekijät voivat rekisteröidä tietyntyyppisiä tietoja.

-   Saapumismerkintä töihin tultaessa ja poistumismerkintä töistä lähdettäessä.
-   Ajan ja nimikkeiden kulutus tuotantotöissä.
-   Koneen käyttöön käytetty aika tuotannossa, jos kone on määritetty resurssiksi.

| **Huomautus**                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työntekijä voidaan määrittää automaattisesti tekemään aikarekisteröinnit tietyllä tuotantokoneella, jos työntekijä haluaa työskennellä koneenkäyttäjänä tuotantotyötä aloittaessaan. |

-   Projekteihin ja projektitehtäviin liittyvät aikarekisteröinnit.
-   Projektimaksujen ja nimikkeen kulutuksen kirjaaminen vastaaviin projektimaksujen kirjauskansioihin ja projektin nimikekirjauskansioihin.
-   Suunniteltu poissaolo.
-   Myöhästymisestä tai liian aikaisesta työpaikalta poistumisesta aiheutuva poissaolo.
-   Tauot, joko manuaalisesti kirjatut tai järjestelmän automaattisesti laskemat.
-   Epäsuorat toiminnot eli tuottamattomat tehtävät, joihin työntekijä voi osallistua työpäivän aikana. Näitä ovat esimerkiksi kokoukset tai työtilan siivoaminen.
-   Ylityö, jotka voidaan kirjata lisätunneiksi, liukuvaksi työajaksi tai ylityöksi.

## <a name="adding-clock-out-registrations"></a>Poistumismerkinnän lisääminen
Jos työntekijä unohtaa kirjata itsensä ulos työpäivän päätteeksi, puuttuva merkintä voidaan lisätä suorittamalla erätyö. Järjestelmä vertaa työhönsaapumisaikaa ja työstäpoistumisaikaa työntekijälle määritetyn profiilin mukaisesti ja lisää puuttuvan poistumismerkinnän automaattisesti profiilin poistumisaikaa vastaavasti. Saapumis- ja poistumismerkinnät ovat erittäin tärkeitä, jotta aikarekisteröinnit voidaan laskea ja hyväksyä ennen tietojen siirtämistä palkanlaskentaan.

## <a name="calculating-registrations"></a>Rekisteröintien laskeminen
Kun työajan seurannan piiriin kuuluva työntekijä määritetään laskentaryhmään, joka liittyy tavallisesti tiettyyn tiimiin, vuoroon tai työryhmään. Tiimin päällikkö tai esimies tavallisesti tarkistaa työntekijöiden tekemät merkinnät ja vastaa myös kunkin laskentaryhmän laskentojen suorittamisesta päivittäin. Laskentaprosessin aikana tiimin päällikkö tai esimies voi:
-   korjata virheellisiä merkintöjä. Hän voi esimerkiksi muuttaa kytkentäkoodeja ja muokata tuotantotöitä koskevaa palautetta.
-   lisätä puuttuvia merkintöjä. Hän voi esimerkiksi luoda poistumismerkintöjä ja poissaolotapahtumia.
-   poistaa virheellisiä merkintöjä.

Koska kirjatun ajan on vastattava työntekijän aikaprofiilia ennen kirjattujen tietojen laskentaa, sellaisten työntekijöiden työaikaprofiili täytyy ohittaa, joiden vakiotyöaikaprofiilissa on jokin poikkeus. Jos työntekijän profiilissa on määritetty päivävuoro ja työntekijä on suostunut tekemään yövuoroa ilman ylityökorvausta, tiimin päällikön tai esimiehen on ohitettava työntekijän oletusprofiili, jotta työaika voidaan laskea vakiotyötuntihinnalla eikä ylityönä. Laskenta näyttää myös virhesanoman, jos jokin poissaolomerkintä puuttuu. Se täytyy lisätä, ennen kuin laskenta voidaan suorittaa.

## <a name="approving-registrations"></a>Rekisteröintien hyväksyminen
Aikarekisteröinnin työntekijälle täytyy määrittää laskentaryhmän lisäksi myös hyväksyntäryhmä. Ryhmä on yleensä tiimi-, vuoro- tai työryhmäkohtainen. Sinun täytyy hyväksyä oikein lasketut – toisin sanoen virheettömät – aikarekisteröinnit, ennen kuin järjestelmä voi luoda palkkatietueet siirrettäviksi palkkajärjestelmään. Yleensä kirjatut tiedot hyväksyy palkanlaskennan järjestelmänvalvoja, joka voi ennen hyväksyntää tehdä seuraavat toimet:
-   ohittaa yksittäisten työntekijöiden palkkasopimukset
-   kirjata lisiä manuaalisesti
-   syöttää lisätietoja poissaolomerkinnöistä.

| **Huomautus**                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jos joillekin työntekijöille on laskettu ylityötä, ylityö voidaan kohdistaa tiettyihin töihin päivän aikana. Tällä on merkitystä, jos työkustannukset lasketaan työntekijöiden palkkojen perusteella. |

## <a name="approving-registrations-using-workflow"></a> Rekisteröintien hyväksyminen työnkulun avulla
Voit määrittää työnkulun hyväksyntäprosessin, joka hyväksyy automaattisesti työnkulkusääntöjen mukaiset rekisteröinnit ja jättää vain poikkeamat käsiteltäviksi manuaalisesti. Jos työnkulun hyväksyntä otetaan käyttöön, tiimin päällikkö tai esimies lähettää lasketut rekisteröinnit hyväksyttäviksi. Työnkulkuprosessi luo asianmukaiset hyväksynnät ja tehtävät ja määrittää ne sitten työnkulussa määritetyille oikeille käyttäjille ja rooleille. Työajan seurannalle on kaksi työnkulun hyväksyntää.

| Työnkulku                                  | Tarkoitus                                                                                                   | Rekisteröintityyppi                                                                                                                                                                                                                                     |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työajan seurantapäivien kokonaismäärä            | Työnkulun tarkistaa rekisteröinnit esimerkiksi päivittäisen odotetun työtuntimäärän perusteella. |                                                                                                                                                                                                                                                       |
| Työajan seurannan kirjauskansion rekisteröinti. | Työnkulku tarkistaa kunkin rekisteröintityypin rekisteröintipäivämäärän.                           | Työajan seuranta • Saapuminen • Poistuminen • Poissaolo • Tauko • Kytkentäkoodi • Projekti • Projektitehtävä • Epäsuora tehtävä Tuotantotyöt • Jono ennen • Asetukset • Prosessi • Limitys • Kuljetus • Jono jälkeen • Aloita apu • Lopeta apu |



## <a name="transferring-approved-registrations"></a>Hyväksyttyjen rekisteröintien siirtäminen
Rekisteröintien hyväksymisen jälkeen ne voidaan siirtää kausittaiseen palkanlaskentatyöhön. Siirretty rekisteröinti kirjataan tehtävään tai työhön, johon se liittyy, kuten tuotantotilaukseen tai projektiin. Rekisteröintien perusteella kullekin työntekijälle luodaan palkanlaskentatapahtumia.  

## <a name="reversing-transferred-registrations"></a>Siirrettyjen rekisteröintien palauttaminen
Tapahtumia voidaan peruuttaa eli palauttaa siihen asti, kunnes palkanlaskentakauden maksusiirto on suoritettu. Tällöin palkanlaskentatiedot on siirretty ulkoiseen tiedostoon. Palautettavat rekisteröinnit vedetään takaisin ja tuotantotilauksiin tai projekteihin kirjatut tapahtumat vastakirjataan ja neutralisoidaan.

| **Huomautus**                                                 |
|----------------------------------------------------------|
| Ulkoinen tiedosto voidaan tuoda palkkajärjestelmään. |

## <a name="registrations-in-electronic-timecards"></a>Sähköisten kellokorttien merkinnät
Työntekijöille, joiden työtehtävät eivät edellytä välitöntä palautetta esimerkiksi tuotantotöistä mutta jotka työskentelevät projektitehtävissä, sopii sähköinen kellokortti. Sähköisen kellokortin avulla rekisteröintejä voidaan tehdä joustavasti milloin tahansa ja toiminta-aikatauluun sopivimmalla tavalla – päivittäin, viikoittain tai kun työntekijä on palannut toimistolle poissaolon jälkeen. Jotta työntekijät voivat käyttää sähköistä kellokorttia, työntekijän tiedoissa on määritettävä Käytä kellokorttia -vaihtoehto. Sähköisen kellokortin avulla työntekijä voi rekisteröidä seuraavat tiedot:

-   Päivämäärä
-   Rekisteröintityyppi
-   Työviite, kuten projekti, epäsuora toiminto tai tuotantotilaus
-   Työn tunnus
-   käytetty aika.
-   Projektimaksut
-   Projektinimikkeet




