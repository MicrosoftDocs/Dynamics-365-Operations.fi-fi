---
title: Taloushallinnan raportointi
description: "Tässä ohjeaiheessa kerrotaan, miten pääset käyttämään taloushallinnon raportointia Microsoft Dynamics 365 for Finance and Operationsissa ja miten taloushallinnon raportointiominaisuuksia käytetään. Se sisältää kuvauksen oletusraporteista, jotka toimitetaan."
author: aprilolson
manager: AnnBe
ms.date: 09/26/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a128f326cb89ab00e69be40801553c0ac551446e
ms.openlocfilehash: c6d504a7b0640f45de4aa9f8fb60d2b1d37818bb
ms.contentlocale: fi-fi
ms.lasthandoff: 09/27/2018

---

# <a name="financial-reporting"></a>Taloushallinnan raportointi

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten pääset käyttämään taloushallinnon raportointia Microsoft Dynamics 365 for Finance and Operationsissa ja miten taloushallinnon raportointiominaisuuksia käytetään. Se sisältää kuvauksen oletusraporteista, jotka toimitetaan.

<a name="accessing-financial-reporting"></a>Taloushallinnon raportoinnin käyttäminen
-----------------------------

**Talousraportointi**-valikko sijaitsee seuraavissa paikoissa Finance and Operationsissa:

-   **Kirjanpito** &gt; **Kyselyt ja raportit**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Perusbudjetointi**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Budjettisuunnittelu**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Budjetin hallinta**
-   Konsolidoinnit

Yrityksen talousraporttien luontia ja muodostamista varten kyseiselle yrityksen on määritettävä seuraavat tiedot:

-   Kirjanpidon vuosikalenteri
-   Kirjanpito
-   Tilikartta
-   Valuutta

Käyttäjät, joille on määritetty soveltuvat oikeudet ja tehtävät käyttöoikeusroolin kautta, voivat käyttää talousraportointitoimintoja. Seuraavissa osissa käsitellään nämä oikeudet ja tehtävät sekä niihin liitetyt roolit.

### <a name="duties"></a>Velvollisuudet

| Tehtävän selite                            | Kuvaus                                                             | AOT-nimi                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Ylläpidä raportoinnin suojausta | Ylläpidä raportoinnin suojausta ja suorita hallinnollisia tehtäviä. | FinancialReportsSecurityMaintain |
| Ylläpidä raportteja            | Suunnittele ja ylläpidä raportteja.                                  | FinancialReportsMaintain         |
| Luo raportit            | Luo ja päivitä raportit.                                 | FinancialReportsGenerate         |
| Arvioi taloudellista suorituskykyä          | Arvioi ja analysoi taloudellista suorituskykyä.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Oikeudet

| Oikeuksien otsikko                       | Kuvaus                                                             | AOT-nimi                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Ylläpidä raportoinnin suojausta | Ylläpidä raportoinnin suojausta ja suorita hallinnollisia tehtäviä. | FinancialReportsSecurityMaintain |
| Ylläpidä raportteja            | Suunnittele ja ylläpidä raportteja.                                  | FinancialReportsMaintainReports  |
| Luo raportit            | Luo ja päivitä raportit.                                 | FinancialReportsGenerateReports  |
| Näytä raportit                | Näytä raportit.                                                 | FinancialReportsView             |

### <a name="roles"></a>Roolit

| Oikeuksien otsikko                       | Tulli                                  | Roolit                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Ylläpidä raportoinnin suojausta | Ylläpidä raportoinnin suojausta | Tietoturvapäällikkö                                                          |
| Ylläpidä raportteja            | Ylläpidä raportteja            | Talouspäällikkö, taloushallintopäällikkö, controlleri, budjettipäällikkö |
| Luo raportit            | Luo raportit            | Toimitusjohtaja, Talousjohtaja, Kirjanpitäjä                                                            |
| Näytä raportit                | Arvioi taloudellista suorituskykyä          | Ei määritetty                                                                   |

Kun käyttäjä on lisätty tai rooli on muuttunut, raporttien pitäisi olla käyttäjän käytettävissä muutamassa minuutissa. **Huomautus:** järjestelmänvalvojan rooli lisätään kaikkiin rooleihin taloudellisessa raportoinnissa.

## <a name="default-reports"></a>Oletusraportit
Talousraportointi sisältää 22 oletusraporttia. Kaikki raportit käyttävät Finance and Operationsin päätilin oletusluokkia. Voit käyttää näitä raportteja sellaisenaan tai omien talousraportointitarpeiden lähtökohtana. Perinteisten raporttien, kuten tuloslaskelma tai tase, lisäksi nämä oletusraportit sisältävät raportteja, jotka näyttävät millaisia raportteja voidaan luoda. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Oletusraportti                                                                                         | Kuvaus                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 kuukauden juokseva yhden sarakkeen tuloslaskelma – oletus | Näyttää organisaation kannattavuuden 12 viime kuukauden aikana yhdessä sarakkeessa.                                                                                                                                                                                                                                      |
| 12 kuukauden trendin tuloslaskelma – oletus                 | Näyttää organisaation kannattavuuden kunkin 12 viime kuukauden aikana. Näiden 12 kuukauden ei tarvitse olla yhtenä tilikautena.                                                                                                                                                                                             |
| Todellinen vs. budjetti – oletus                                | Näyttää alkuperäisen budjetin kaikkien tilien tarkat saldotiedot ja vertaa muutettua budjettia toteutuneeseen, jolla on varianssi.                                                                                                                                                                          |
| Tarkistustiedot – oletus                                  | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti sisältää saatavien ja maksettavien saldot raportointivaluutassa ja paikallisessa valuutassa sekä muita tapahtumatietoja, kuten käyttäjätunnus, tietoja viimeksi muokannut käyttäjä, viimeisin muokkauspäivä ja kirjauskansion tunnus. |
| Saldoluettelo – oletus                                   | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti sisältää alku- ja loppusaldot, saatavien ja maksettavien saldot kuluvalle kaudelle ja vuoden alusta sekä muita tapahtumatietoja, kuten tositteen.                                                                    |
| Tase – oletus                                   | Näyttää organisaation vuoden rahoitusaseman.                                                                                                                                                                                                                                                             |
| Tase ja tuloslaskelma rinnakkain – oletus | Näyttää organisaation vuoden rahoitusaseman ja kannattavuuden rinnakkain.                                                                                                                                                                                                                              |
| Kassavirta – oletus                                       | Antaa tietoja organisaation rahaliikenteestä.                                                                                                                                                                                                                                   |
| Tarkka JE- ja TB-arviointi – oletus                      | Näyttää kaikkien tilien alkusaldon ja tehtävän tiedot.                                                                                                                                                                                                                                                      |
| Yksityiskohtainen pääkirja – oletus                         | Näyttää kaikkien niiden tilien saldotiedot, joilla saatavien ja maksettavien saldot, ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.                                                                                                                                  |
| Kulujen kolmen vuoden vuosineljänneksen trendi – oletus             | Antaa lisätietoja kuluneiden 12 vuosineljänneksen kuluista kolmen viime vuoden ajalta.                                                                                                                                                                                                                                   |
| Taloudellisten otsikoinen JE- ja TB-arviointi – oletus            | Näyttää yhteenvedon saldoista ja taloudellisten otsikoiden (varat, velka, omistajan oma pääoma, tuotto, kulu, voitto tai tappio) tehtävä.                                                                                                                                                                           |
| Tuloslaskelma – oletus                                | Näyttää organisaation tuottavuusnäkymän kuluvalle kaudelle sekä vuoden alusta tähän asti.                                                                                                                                                                                                                                   |
| Kirjanpidon tapahtumaluettelo – oletus                        | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti näyttää saapuvien ja maksettavien saldot sekä muita tapahtumatietoja, kuten tapahtumapäivän, kirjauskansion numeron, tositteen, kirjaustyypin ja jäljitysnumeron.                                                                            |
| Tunnusluvut – oletus                                          | Näyttää organisaation vakavaraisuusasteen, kannattavuuden ja tehokkuusasteen.                                                                                                                                                                                                                           |
| Juokseva 12 kuukauden kulut – oletus                       | Antaa lisätietoja kunkin kuluneen 12 kuukauden kuluista. Näiden 12 kuukauden ei tarvitse olla yhtenä tilikautena.                                                                                                                                                                                                       |
| Juokseva vuosineljänneksen tuloslaskelma – oletus               | Näyttää organisaation kannattavuuden neljännesvuosittain edelliseltä vuodelta ja vuoden alusta.                                                                                                                                                                                                                   |
| Tase rinnakkain – oletus                      | Näyttää organisaation vuoden rahoitusaseman. Tämä raportti näyttää varat ja velat sekä osakkeenomistajien oman pääoman rinnakkain.                                                                                                                                                                                |
| Pääkirjan yhteenveto – oletus                          | Näyttää kaikkien niiden tilien saldotiedot, joilla on alku- ja loppusaldot ja saatavien ja maksettavien saldot sekä niiden nettoeron.                                                                                                                                                                  |
| Pääkirjan yhteenveto vuosittain – oletus           | Näyttää kaikkien tilien niiden saldotiedot, joilla on alku- ja loppusaldot, ja saatavien ja maksettavien saldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.                                                                                                                           |
| Viikoittainen myynti ja alennukset – oletus                     | Antaa lisätietoja kuukauden jokaisen viikon myynnistä ja alennuksista. Tämä raportti sisältää neljän viikon yhteisarvon.                                                                                                                                                                                                              |
| Käytettävissä olevat budjettivarat -oletus                         | Tarkastele tarkistetun budjetin, toteutuneiden menojen, budjettivarausten ja käytettävissä olevien budjettivarojen yksityiskohtaista vertailua.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Talousraporttien avaaminen
Kun napsautat **Talousraportointi**-valikon, näkyviin tulee luettelo yrityksen oletusraportteja. Voit sitten avata raportin tai muokata sitä. Avaa jokin oletusraportti valitsemalla sen nimi. Kun raportti avataan ensimmäisen kerran, se luodaan automaattisesti edelliselle kuukaudelle. Jos esimerkiksi avaat raportin ensimmäisen kerran elokuussa 2016, raportti luodaan päivämäärälle 31.7.2016. Kun raportti on avattu, voit aloittaa siihen perehtymisen porautumalla tiettyyn tietoon ja muuttamalla raporttiasetuksia.

## <a name="creating-and-modifying-financial-reports"></a>Talousraporttien luominen ja muokkaaminen
Voit luoda raporttiluettelosta uuden raportin tai muokata aiemmin luotua raporttia. Jos sinulla on tarvittavat käyttöoikeudet, voit luoda uuden taloudellisen raportin valitsemalla **Uusi** toimintoruudussa. Raportin suunnitteluohjelma ladataan laitteeseen. Kun raportin suunnitteluohjelma käynnistyy, voit luoda sitten uuden raportin. Kun uusi raportti on tallennettu, se tukee näkyviin talousraporttiluetteloon. Luettelossa näkyvät vain raportit, jotka on luotu Finance and Operationsissa käytössä olevalle yritykselle. 

> [!NOTE] 
> Tietokoneelle, jolle ladataan raportin suunnitteluohjelman asiakasohjelma, on oltava asennettuna Microsoft .NET Frameworkin versio 4.6.2. Tämä Microsoft .NET Framework -versio voidaan ladata ja asentaa [Microsoftin latauskeskuksesta](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät incognito-tilaa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa. Voit myös muokata talousraporttiluettelossa näkyvää raporttia. Raporttia ympäröivä alue on valittu, valitse toimintoruudussa **Muokkaa**. Raportin suunnitteluohjelma käynnistyy.

## <a name="additional-resources"></a>Lisäresurssit
- [Raporttien näyttäminen](view-financial-reports.md)




