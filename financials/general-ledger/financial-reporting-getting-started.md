---
title: Taloushallinnan raportointi
description: "Tässä ohjeaiheessa kerrotaan, miten voit löydät talousraportoinnin Microsoft Dynamics 365 for Operationsissa ja miten käytät taloudellisen raportoinnin ominaisuuksia. Se sisältää kuvauksen oletusraporteista, jotka toimitetaan."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>Taloushallinnan raportointi

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa kerrotaan, miten voit löydät talousraportoinnin Microsoft Dynamics 365 for Operationsissa ja miten käytät taloudellisen raportoinnin ominaisuuksia. Se sisältää kuvauksen oletusraporteista, jotka toimitetaan.

<a name="accessing-financial-reporting"></a>Taloushallinnon raportoinnin käyttäminen
-----------------------------

**Talousraportointi**-valikko sijaitsee seuraavissa paikoissa Microsoft Dynamics 365 for Operationsissa:

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
Talousraportointi sisältää 22 oletusraporttia. Kaikki raportit käyttävät Microsoft Dynamics 365 for Operationsin päätilin oletusluokkia. Voit käyttää näitä raportteja sellaisenaan tai omien talousraportointitarpeiden lähtökohtana. Perinteisten raporttien, kuten tuloslaskelma tai tase, lisäksi nämä oletusraportit sisältävät raportteja, jotka näyttävät millaisia raportteja voidaan luoda. Kukin raportti seuraavassa taulukossa linkittyy raporttia koskevaan Office Mix -esitykseen.

| Oletusraportti                                                                                         | kuvaus                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 kuukauden juokseva yhden sarakkeen tuloslaskelma – oletus](https://mix.office.com/watch/76kc7bm3wnt1) | Näyttää organisaation kannattavuuden 12 viime kuukauden aikana yhdessä sarakkeessa.                                                                                                                                                                                                                                      |
| [12 kuukauden trendin tuloslaskelma – oletus](https://mix.office.com/watch/12brmfge5p8r)                 | Näyttää organisaation kannattavuuden kunkin 12 viime kuukauden aikana. Näiden 12 kuukauden ei tarvitse olla yhtenä tilikautena.                                                                                                                                                                                             |
| [Todellinen vs. budjetti – oletus](https://mix.office.com/watch/fi439lkwr0no)                                | Näyttää alkuperäisen budjetin kaikkien tilien tarkat saldotiedot ja vertaa muutettua budjettia toteutuneeseen, jolla on varianssi.                                                                                                                                                                          |
| [Tarkistustiedot – oletus](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti sisältää saatavien ja maksettavien saldot raportointivaluutassa ja paikallisessa valuutassa sekä muita tapahtumatietoja, kuten käyttäjätunnus, tietoja viimeksi muokannut käyttäjä, viimeisin muokkauspäivä ja kirjauskansion tunnus. |
| [Saldoluettelo – oletus](https://mix.office.com/watch/1kezwu2a10fq4)                                   | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti sisältää alku- ja loppusaldot, saatavien ja maksettavien saldot kuluvalle kaudelle ja vuoden alusta sekä muita tapahtumatietoja, kuten tositteen.                                                                    |
| [Tase – oletus](https://mix.office.com/watch/zkgq0u7visw9)                                   | Näyttää organisaation vuoden rahoitusaseman.                                                                                                                                                                                                                                                             |
| [Tase ja tuloslaskelma rinnakkain – oletus](https://mix.office.com/watch/zkgq0u7visw9) | Näyttää organisaation vuoden rahoitusaseman ja kannattavuuden rinnakkain.                                                                                                                                                                                                                              |
| [Kassavirta – oletus](https://mix.office.com/watch/jd3go9pz6390)                                       | Antaa tietoja organisaation rahaliikenteestä.                                                                                                                                                                                                                                   |
| [Tarkka JE- ja TB-arviointi – oletus](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | Näyttää kaikkien tilien alkusaldon ja tehtävän tiedot.                                                                                                                                                                                                                                                      |
| [Yksityiskohtainen pääkirja – oletus](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | Näyttää kaikkien niiden tilien saldotiedot, joilla saatavien ja maksettavien saldot, ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.                                                                                                                                  |
| [Kulujen kolmen vuoden vuosineljänneksen trendi – oletus](https://mix.office.com/watch/gwm4zu7tmtj8)             | Antaa lisätietoja kuluneiden 12 vuosineljänneksen kuluista kolmen viime vuoden ajalta.                                                                                                                                                                                                                                   |
| [Taloudellisten otsikoinen JE- ja TB-arviointi – oletus](https://mix.office.com/watch/1sw9fmtwgjb1f)            | Näyttää yhteenvedon saldoista ja taloudellisten otsikoiden (varat, velka, omistajan oma pääoma, tuotto, kulu, voitto tai tappio) tehtävä.                                                                                                                                                                           |
| [Tuloslaskelma – oletus](https://mix.office.com/watch/sbuhgl5hzuhi)                                | Näyttää organisaation tuottavuusnäkymän kuluvalle kaudelle sekä vuoden alusta tähän asti.                                                                                                                                                                                                                                   |
| [Kirjanpidon tapahtumaluettelo – oletus](https://mix.office.com/watch/19h9v2rmh48vy)                        | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti näyttää saapuvien ja maksettavien saldot sekä muita tapahtumatietoja, kuten tapahtumapäivän, kirjauskansion numeron, tositteen, kirjaustyypin ja jäljitysnumeron.                                                                            |
| [Tunnusluvut – oletus](https://mix.office.com/watch/b08hfc5h92me)                                          | Näyttää organisaation vakavaraisuusasteen, kannattavuuden ja tehokkuusasteen.                                                                                                                                                                                                                           |
| [Juokseva 12 kuukauden kulut – oletus](https://mix.office.com/watch/iywod5qmqhz7)                       | Antaa lisätietoja kunkin kuluneen 12 kuukauden kuluista. Näiden 12 kuukauden ei tarvitse olla yhtenä tilikautena.                                                                                                                                                                                                       |
| [Juokseva vuosineljänneksen tuloslaskelma – oletus](https://mix.office.com/watch/1k4yl6a6oyxqc)               | Näyttää organisaation kannattavuuden neljännesvuosittain edelliseltä vuodelta ja vuoden alusta.                                                                                                                                                                                                                   |
| [Tase rinnakkain – oletus](https://mix.office.com/watch/zkgq0u7visw9)                      | Näyttää organisaation vuoden rahoitusaseman. Tämä raportti näyttää varat ja velat sekä osakkeenomistajien oman pääoman rinnakkain.                                                                                                                                                                                |
| [Pääkirjan yhteenveto – oletus](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | Näyttää kaikkien niiden tilien saldotiedot, joilla on alku- ja loppusaldot ja saatavien ja maksettavien saldot sekä niiden nettoeron.                                                                                                                                                                  |
| [Pääkirjan yhteenveto vuosittain – oletus](https://mix.office.com/watch/1ewwgbpv0iwrl)           | Näyttää kaikkien tilien niiden saldotiedot, joilla on alku- ja loppusaldot, ja saatavien ja maksettavien saldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.                                                                                                                           |
| [Viikoittainen myynti ja alennukset – oletus](https://mix.office.com/watch/112ng0hy5de0j)                     | Antaa lisätietoja kuukauden jokaisen viikon myynnistä ja alennuksista. Tämä raportti sisältää neljän viikon yhteisarvon.                                                                                                                                                                                                              |
| [Käytettävissä olevat budjettivarat -oletus](https://mix.office.com/watch/15hcpezcbx7tv)                         | Tarkastele tarkistetun budjetin, toteutuneiden menojen, budjettivarausten ja käytettävissä olevien budjettivarojen yksityiskohtaista vertailua.                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Talousraporttien avaaminen
Kun napsautat **Talousraportointi**-valikon, näkyviin tulee luettelo yrityksen oletusraportteja. Voit sitten avata raportin tai muokata sitä. Avaa jokin oletusraportti valitsemalla sen nimi. Kun raportti avataan ensimmäisen kerran, se luodaan automaattisesti edelliselle kuukaudelle. Jos esimerkiksi avaat raportin ensimmäisen kerran elokuussa 2016, raportti luodaan päivämäärälle 31.7.2016. Kun raportti on avattu, voit aloittaa siihen perehtymisen porautumalla tiettyyn tietoon ja muuttamalla raporttiasetuksia.

## <a name="creating-and-modifying-financial-reports"></a>Talousraporttien luominen ja muokkaaminen
Voit luoda raporttiluettelosta uuden raportin tai muokata aiemmin luotua raporttia. Jos sinulla on tarvittavat käyttöoikeudet, voit luoda uuden taloudellisen raportin valitsemalla **Uusi** toimintoruudussa. Raportin suunnitteluohjelma ladataan laitteeseen. Kun raportin suunnitteluohjelma käynnistyy, voit luoda sitten uuden raportin. Kun uusi raportti on tallennettu, se tukee näkyviin talousraporttiluetteloon. Luettelossa näkyvät vain raportit, jotka on luotu Microsoft Dynamics 365 for Operationsissa käytössä olevalle yritykselle. Lisätietoja talousraporttien luomisesta ja muokkaamisesta Dynamics 365 for Operationsissa saat lukemalla näitä [blogimerkintöjä](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) Dynamicsin talousraportoinnin blogista. **Huomautus:** Tietokoneelle, jolle ladataan raportin suunnitteluohjelman asiakasohjelma, on oltava asennettuna Microsoft .NET Frameworkin versio 4.6.2. Tämä Microsoft .NET Framework -versio voidaan ladata ja asentaa [täältä](https://www.microsoft.com/en-us/download/details.aspx?id=53345). Jos käytössäsi on Chrome, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät incognito-tilaa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa. Voit myös muokata talousraporttiluettelossa näkyvää raporttia. Raporttia ympäröivä alue on valittu, valitse toimintoruudussa **Muokkaa**. Raportin suunnitteluohjelma käynnistyy.

<a name="see-also"></a>Lisätietoja
--------

[Näytä raportit](view-financial-reports.md)

[Dynamicsin talousraportointi -blogi](http://blogs.msdn.com/b/dynamics_financial_reporting/)




