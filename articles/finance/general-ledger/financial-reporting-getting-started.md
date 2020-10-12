---
title: Taloushallinnon raportoinnin yleiskatsaus
description: Tässä ohjeaiheessa kerrotaan, miten löydät talousraportoinnin Microsoft Dynamics 365 Financessa ja miten käytät taloudellisen raportoinnin ominaisuuksia.
author: aprilolson
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7cc238c573a319073b451063782762c19a80017
ms.sourcegitcommit: 28a771d81322e72d88db63a20ff360de084a6087
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/22/2020
ms.locfileid: "3835107"
---
# <a name="get-started-with-financial-reporting"></a>Financial reportingin aloittaminen 

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten löydät talousraportoinnin ja miten käytät taloudellisen raportoinnin ominaisuuksia. Se sisältää myös kuvauksen oletusraporteista, jotka toimitetaan.

<a name="accessing-financial-reporting"></a>Taloushallinnon raportoinnin käyttäminen
-----------------------------

**Talousraportointi**-valikko sijaitsee seuraavissa sijainneissa:

-   **Kirjanpito** &gt; **Kyselyt ja raportit**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Perusbudjetointi**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Budjettisuunnittelu**
-   **Budjetointi** &gt; **Kyselyt ja raportit** &gt; **Budjetin hallinta**
-   Konsolidoinnit

Yrityksen talousraporttien luontia ja muodostamista varten kyseiselle yrityksen on määritettävä seuraavat tiedot:

-   Kirjanpidon vuosikalenteri
-   Ledger
-   Tilikartta
-   Valuutta

## <a name="granting-security-access-to-financial-reporting"></a>Financial Reporting -käyttöoikeuksien myöntäminen
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
| Ylläpidä raportoinnin suojausta | Ylläpidä raportoinnin suojausta ja suorita hallinnollisia tehtäviä. | FinancialReportsSecuritySystemMaintain |
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

Kun käyttäjä on lisätty tai rooli on muuttunut, raporttien pitäisi olla käyttäjän käytettävissä muutamassa minuutissa. 

> [!NOTE]
> Järjestelmänvalvojan rooli lisätään kaikkiin rooleihin taloudellisessa raportoinnissa.

## <a name="report-deletions-and-expirations"></a>Raportin poistot ja päättymiset
Raportteja luovat käyttäjät voivat poistaa omia raporttejaan. Käyttäjät, joilla on **Ylläpidä taloudellisen raportoinnin turvallisuutta** -velvollisuus, voivat poistaa muiden raportteja. 

Versiossa 10.0.8 on otettu käyttöön vanhentumispäivien käsite. Uusi pakollinen ominaisuus otetaan käyttöön ominaisuuksien hallinnan työtilan **Kaikki**-sivulla. **Taloudellisten raporttien säilytyskäytännöt** -toiminto sisältää seuraavat muutokset:
* Äskettäin luotuihin raportteihin merkitään automaattisesti vanhenemispäivä, joka on 90 päivää siitä, kun ne on luotu.
* Kaikki olemassa olevat raportit, jotka on luotu ennen kuin ominaisuus asennettiin, saavat 90 päivän vanhentumisajan. Päivämäärä voi näkyä tyhjänä lyhyen ajan, kunnes taloushallinnon raportointipalvelu on käynnissä, raportti luodaan ja palvelu suorittaa päivityksen aiemmin luotuihin raportteihin, joiden vanhentumispäivämäärä on tyhjä. 
* Käyttäjät, joilla on **Ylläpidä taloudellisen raportoinnin turvallisuutta** -velvollisuus, voivat käyttää tätä toimintoa. Kuka tahansa, jolla on **Ylläpidä kirjanpitoraporttia** -velvollisuus, jolle on myönnetty **Ylläpidä talousraportin vanhenemisoikeuksia**, voi myös muuttaa vanhentumisaikaa. Tällä hetkellä käytettävissä on kaksi säilytysvaihtoehtoa: 
  * Vanhentuminen 90 päivää.
  * Asetus, joka määrittää, että raportti ei vanhene.
  
Kun vanhenemisaika, kuten 90 päivää, on valittuna, sitä käytetään 90 päivän aikana tästä päivästä lähtien. Tämä on eri toiminta kuin 90 päivää alkuperäisen luontipäivämäärän määrityksestä, kun raportti luotiin. 
  
Lisäasetukset otetaan huomioon tulevissa toiminnoissa. Oletusarvo on 90 päivää, ja käyttäjät, joilla on tarvittavat käyttöoikeudet, voivat ohittaa **Talousraportit**-luettelosivun oletusarvon.    

## <a name="default-reports"></a>Oletusraportit
Talousraportointi sisältää 22 oletusraporttia. Jokaisessa raportissa käytetään oletuspäätililuokkia. Voit käyttää näitä raportteja sellaisenaan tai omien talousraportointitarpeiden lähtökohtana. Perinteisten raporttien, kuten tuloslaskelma tai tase, lisäksi nämä oletusraportit sisältävät raportteja, jotka näyttävät millaisia raportteja voidaan luoda. 

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
Kun valitset **Talousraportointi**-valikon, näkyviin tulee luettelo yrityksen oletusraportteja. Voit sitten avata raportin tai muokata sitä. Avaa jokin oletusraportti valitsemalla sen nimi. Kun raportti avataan ensimmäisen kerran, se luodaan automaattisesti edelliselle kuukaudelle. Jos esimerkiksi avaat raportin ensimmäisen kerran elokuussa 2019, raportti luotiin päivämäärälle 31.7.2019. Kun raportti on avattu, voit aloittaa siihen perehtymisen porautumalla tiettyyn tietoon ja muuttamalla raporttiasetuksia.

## <a name="creating-and-modifying-financial-reports"></a>Talousraporttien luominen ja muokkaaminen
Voit luoda raporttiluettelosta uuden raportin tai muokata aiemmin luotua raporttia. Jos sinulla on tarvittavat käyttöoikeudet, voit luoda uuden taloudellisen raportin valitsemalla **Uusi** toimintoruudussa. Raportin suunnitteluohjelma ladataan laitteeseen. Kun raportin suunnitteluohjelma käynnistyy, voit luoda sitten uuden raportin. Kun uusi raportti on tallennettu, se tukee näkyviin talousraporttiluetteloon. Luettelossa näkyvät vain raportit, jotka on luotu Dynamics 365 Financessa käytössä olevalle yritykselle. 

## <a name="reporting-tree-definitions"></a>Raportointipuiden määritykset 
Yksi komponentti, jota käytetään talousraporttien muodostamiseen, on raportointipuun määritys. Raportointipuun määritys auttaa määrittämään organisaation rakenteen ja hierarkian. Se on dimensiot ylittävä hierarkkinen rakenne, joka perustuu taloushallinnon tietojen dimensioiden suhteisiin. Sen avulla saadaan tietoja raportointiyksikkötasolla ja kaikkien puun yksiköiden yhteenvetotasolla.

Luotavien raportointipuiden määrälle ei ole asetettu ylärajaa. Eri puiden avulla organisaation tietoja voi tarkastella eri tavoin. Kukin raportointipuu voi sisältää minkä tahansa osastojen ja yhteenvetoyksiköiden yhdistelmän, mutta raporttimääritys voi linkittää vain yhteen raportointipuuhun kerrallaan. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Report Designerin avaamisongelmien vianmääritys
Tietyt yleiset ongelmat voivat aiheuttaa hankaluuksia, kun Report Designer avataan. Seuraavaksi käsitellään näitä ongelmia ja niiden ratkaisuja.

Ongelma 1: Report Designer ei käynnisty, kun valitaan **Uusi** tai **Muokkaa**.

* Valitse Internet Explorerissa ensin **Asetukset** ja sitten **Internet-asetukset**. Valitse **Suojaus**-välilehdessä ensin Luotettavat sivuston ja sitten **Sivustot**. Anna **Lisää tämä sivusto vyöhykkeeseen** -kohdassa \*\.dynamics.com ja valitse sitten **Lisää**. 
* Valitse Internet Explorerissa ensin **Asetukset** ja sitten **Internet-asetukset**. Valitse ensin **Suojaus**-välilehti ja sitten Luotettavat sivustot. Vaihda Vyöhykkeen suojaustaso -kohdan asetukseksi **Melko pieni**.
* Poista ponnahdusikkunoiden esto käytöstä selaimessa.
* Työasemien on asennettava Microsoft .NET -kehys 4.6.2 tai uudempi versio. Tämä Microsoft .NET Framework -versio voidaan ladata ja asentaa [Microsoft Download Centeristä](https://www.microsoft.com/download/details.aspx?id=53345).
* Jos käytössä on Chrome-selain, Report Designer -asiakasohjelman lataamista varten on asennettava ClickOnce-laajennus. Jos käytät incognito-tilaa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa. Jos kirjautuminen ei onnistu Chrome-selaimella kokeile ongelmassa 1 kuvattuja Internet Explorerin tai Edgen asennusvaiheita. 

Ongelma 2: Käyttäjälle ei ole määritetty Financial Reportingin käyttöön tarvittavia oikeuksia. 

* Voit tarkistaa, onko käyttäjällä oikeuksia valitsemalla **Kyllä** seuraavan virheen yhteydessä: Yhteyden muodostaminen Financial Reporting -palvelimeen ei onnistu. Valitse Kyllä, jos haluat jatkaa, ja määritä toinen palvelimen osoite. Valitse sitten **Testaa yhteys**. Jos oikeuksia ei ole, seuraava sanoma avautuu: Yhteyden muodostaminen epäonnistui. Käyttäjällä ei ole palvelinyhteyttä varten tarvittavia käyttöoikeuksia. Ota yhteyttä järjestelmänvalvojaan.
* Tarvittavien oikeuksien luettelo on kohdassa [Financial Reporting -käyttöoikeuksien myöntäminen](#granting-security-access-to-financial-reporting). Financial Reportingin suojaus perustuu näihin oikeuksiin. Käyttö ei ole mahdollista ellei näitä oikeuksia (tai muuta nämä oikeudet sisältävää käyttöoikeusroolia) ole määritetty. 
* **Yrityskäyttäjäpalvelu yritykseen** -integrointitehtävä (joka vastaa käyttäjäintegraatiota ja tiedetään sellaiseksi) suoritetaan 5 minuutin välein. Oikeusmuutosten voimaantulo Financial Reportingissa voi kestää 10 minuuttia. 
  Jos toinen käyttäjä voi avata Report Designerin, valitse ensin **Työkalut** ja sitten **Integroinnin tila**. Varmista, että integrointimääritys Yrityksen käyttäjäpalvelu yritykseen on suoritettu, koska sinulle on määritetty oikeus käyttää Financial Reportingia. 
* On mahdollista, että jokin muu virhe on estänyt **Dynamics-käyttäjästä Financial Reporting -käyttäjään integroinnin** valmistumisen. On myös mahdollista, että datamart-nollaus on käynnistetty muttei vielä päättynyt tai että tapahtui toinen järjestelmävirhe. Yritä suorittaa prosessi uudelleen myöhemmin. Jos ongelma jatkuu, ota yhteys järjestelmänvalvojaan.

Ongelma 3: ClickOnce Report Designerin kirjautumissivulta päästään etenemään mutta kirjautuminen Report Designeriin ei onnistu. 

* Paikallisessa tietokoneessa olevan ajan kirjautumistietoja annettaessa on oltava viiden minuutin sisällä Financial Reporting -palvelimen ajasta. Jos ero on yli viisi minuuttia, järjestelmä ei salli kirjautumista. 
* Tässä tapauksessa kannattaa ottaa käyttöön Windows-asetus, joka määrittää tietokoneen ajan automattisesti. 

## <a name="additional-resources"></a>Lisäresurssit
- [Näytä raportit](view-financial-reports.md)
- [Talousraporttien raportointipuiden määritykset](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)
