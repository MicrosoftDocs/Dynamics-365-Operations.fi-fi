---
title: Taloushallinnon raportoinnin yleiskatsaus
description: Tässä ohjeaiheessa kerrotaan, miten löydät talousraportoinnin Microsoft Dynamics 365 Financessa ja miten käytät taloudellisen raportoinnin ominaisuuksia.
author: aprilolson
ms.date: 07/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da997af4c4cab7b99dfa14f185de6a7c057d6831b7ee576787c17b550fa60194
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748207"
---
# <a name="get-started-with-financial-reporting"></a>Financial reportingin aloittaminen 

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, miten löydät talousraportoinnin ja miten käytät taloudellisen raportoinnin ominaisuuksia. Se sisältää myös kuvauksen oletusraporteista, jotka toimitetaan.

## <a name="accessing-financial-reporting"></a>Taloushallinnon raportoinnin käyttäminen

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
-   Tapahtuman kirjaaminen vähintään yhdelle tilille
-   Päätili näkyy **Taloushallinnon raportoinnin asetukset** -sivun **Valitut**-sarakkeessa (**Kirjanpito > Kirjanpidon asetukset > Taloushallinnon raportoinnin asetukset**)

## <a name="granting-security-access-to-financial-reporting"></a>Taloushallinnon raportoinnin käyttöoikeuksien myöntäminen
Käyttäjät, joille on määritetty soveltuvat oikeudet ja tehtävät käyttöoikeusroolin kautta, voivat käyttää taloushallinnon raportoinnin toimintoja. Seuraavissa osissa käsitellään nämä oikeudet ja tehtävät sekä niihin liitetyt roolit.

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

Kun käyttäjä on lisätty tai rooli on muuttunut, taloushallinnon raporttien pitäisi olla käyttäjän käytettävissä muutamassa minuutissa. 

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
| [Yksityiskohtainen pääkirja – oletus](trial-balance-financial-reports.md)| Näyttää kaikkien niiden tilien saldotiedot, joilla saatavien ja maksettavien saldot, ja näiden nettosaldot sekä tapahtumapäivämäärän, tositteen ja kirjauskansion kuvauksen.                                                                                                                                  |
| Kulujen kolmen vuoden vuosineljänneksen trendi – oletus             | Antaa lisätietoja kuluneiden 12 vuosineljänneksen kuluista kolmen viime vuoden ajalta.                                                                                                                                                                                                                                   |
| Taloudellisten otsikoinen JE- ja TB-arviointi – oletus            | Näyttää yhteenvedon saldoista ja taloudellisten otsikoiden (varat, velka, omistajan oma pääoma, tuotto, kulu, voitto tai tappio) tehtävä.                                                                                                                                                                           |
| [Tuloslaskelma – oletus](income-statement-financial-report.md)| Näyttää organisaation tuottavuusnäkymän kuluvalle kaudelle sekä vuoden alusta tähän asti.                                                                                                                                                                                                                                   |
| Kirjanpidon tapahtumaluettelo – oletus                        | Näyttää kaikkien tilien tarkat saldotiedot. Tämä raportti näyttää saapuvien ja maksettavien saldot sekä muita tapahtumatietoja, kuten tapahtumapäivän, kirjauskansion numeron, tositteen, kirjaustyypin ja jäljitysnumeron.                                                                            |
| Tunnusluvut – oletus                                          | Näyttää organisaation vakavaraisuusasteen, kannattavuuden ja tehokkuusasteen.                                                                                                                                                                                                                           |
| Juokseva 12 kuukauden kulut – oletus                       | Antaa lisätietoja kunkin kuluneen 12 kuukauden kuluista. Näiden 12 kuukauden ei tarvitse olla yhtenä tilikautena.                                                                                                                                                                                                       |
| Juokseva vuosineljänneksen tuloslaskelma – oletus               | Näyttää organisaation kannattavuuden neljännesvuosittain edelliseltä vuodelta ja vuoden alusta.                                                                                                                                                                                                                   |
| Tase rinnakkain – oletus                      | Näyttää organisaation vuoden rahoitusaseman. Tämä raportti näyttää varat ja velat sekä osakkeenomistajien oman pääoman rinnakkain.                                                                                                                                                                                |
| [Pääkirjan yhteenveto – oletus](trial-balance-financial-reports.md)| Näyttää kaikkien niiden tilien saldotiedot, joilla on alku- ja loppusaldot ja saatavien ja maksettavien saldot sekä niiden nettoeron.                                                                                                                                                                  |
| [Pääkirjan yhteenveto vuosittain – oletus](trial-balance-financial-reports.md)| Näyttää kaikkien tilien niiden saldotiedot, joilla on alku- ja loppusaldot, ja saatavien ja maksettavien saldot sekä niiden kuluvan vuoden ja edellisen vuoden nettoeron.                                                                                                                           |
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
* Jos käytössäsi on Chrome-selain, sinun on asennettava ClickOnce-laajennus ladataksesi raportin suunnittelun asiakasohjelman. Jos käytät Chromea incognito-tilassa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa. Lisätietoja Chrome ClickOnce -laajennuksesta on kohdassa [Pilvikäyttöönottojen järjestelmävaatimukset](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Jos käytät Microsoft Edgea Chrome-selaimen kanssa, sinun ei tarvitse asentaa ClickOnce-laajennusta Edge Chromiumiin. Voit kuitenkin ottaa käyttöön ClickOnce-asetuksen, jotta voit ladata raporttien suunnittelun asiakasohjelman. Jos käytät incognito-tilaa, varmista, että ClickOnce-laajennus on käytössä incognito-tilassa.
     1. Avaa uusi selain Microsoft Edgessä.
     2. Anna **edge://flags** ja paina **Enter**-näppäintä.
     3. Valitse **ClickOnce-tuki**-vaihtoehto tai käytä tätä suoraa linkkiä: **edge://flags/#edge-click-once**.
     4. Määritä avattavan valikon vaihtoehdon asetukseksi **Käytössä**.
     5. Valitse **Käynnistä selain uudelleen**.

Ongelma 2: Käyttäjälle ei ole määritetty Financial Reportingin käyttöön tarvittavia oikeuksia. 

* Voit tarkistaa, onko käyttäjällä oikeuksia valitsemalla **Kyllä** seuraavan virheen yhteydessä: Yhteyden muodostaminen Financial Reporting -palvelimeen ei onnistu. Valitse Kyllä, jos haluat jatkaa, ja määritä toinen palvelimen osoite. Valitse sitten **Testaa yhteys**. Jos oikeuksia ei ole, seuraava sanoma avautuu: Yhteyden muodostaminen epäonnistui. Käyttäjällä ei ole palvelinyhteyttä varten tarvittavia käyttöoikeuksia. Ota yhteyttä järjestelmänvalvojaan.
* Tarvittavien oikeuksien luettelo on kohdassa [Taloushallinnon raportoinnin käyttöoikeuksien myöntäminen](#granting-security-access-to-financial-reporting). Taloushallinnon raportoinnin suojaus perustuu näihin oikeuksiin. Käyttö ei ole mahdollista ellei näitä oikeuksia (tai muuta nämä oikeudet sisältävää käyttöoikeusroolia) ole määritetty. 
* **Yrityskäyttäjäpalvelu yritykseen** -integrointitehtävä (joka vastaa käyttäjäintegraatiota ja tiedetään sellaiseksi) suoritetaan 5 minuutin välein. Oikeusmuutosten voimaantulo Financial Reportingissa voi kestää 10 minuuttia. 
  Jos toinen käyttäjä voi avata Report Designerin, valitse ensin **Työkalut** ja sitten **Integroinnin tila**. Varmista, että integrointimääritys Yrityksen käyttäjäpalvelu yritykseen on suoritettu, koska sinulle on määritetty oikeus käyttää Financial Reportingia. 
* On mahdollista, että jokin muu virhe on estänyt **Dynamics-käyttäjästä Financial Reporting -käyttäjään integroinnin** valmistumisen. On myös mahdollista, että datamart-nollaus on käynnistetty muttei vielä päättynyt tai että tapahtui toinen järjestelmävirhe. Yritä suorittaa prosessi uudelleen myöhemmin. Jos ongelma jatkuu, ota yhteys järjestelmänvalvojaan.

Ongelma 3: **ClickOnce Report Designerin** kirjautumissivulta päästään etenemään mutta kirjautuminen Report Designeriin ei onnistu. 

* Paikallisessa tietokoneessa olevan ajan on järjestelmään kirjauduttaessa oltava viiden minuutin sisällä taloushallinnon raportointipalvelimen ajasta. Jos ero on yli viisi minuuttia, järjestelmä ei salli kirjautumista. 
* Jos tietokoneessa oleva aika poikkeaa taloushallinnon raportointipalvelimen ajasta, tietokoneen ajan automaattisesti määrittävä Windows-asetus kannattaa ottaa käyttöön. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Report Designerin ongelmien vianmääritys tapahtumien katseluohjelmassa

Tapahtumien katseluohjelmassa voi analysoida joitakin taloushallinnon raportoinnin käyttöön liittyviä ongelmia. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Mitä tapahtuu, kun taloushallinnon raportoinnissa on yhteysongelmia? 

Seuraavien vaiheiden ansiosta yhteydenotto Microsoftin tukeen tehostuu ja ongelman ratkaiseminen nopeutuu. 
 
Seuraavat ohjeet selittävät, miten tapahtuvien katseluohjelman sanomat otetaan käyttöön taloushallinnon raportoinnissa. Tapahtumien katseluohjelman luomat lokit auttavat teknikoita määrittämään yhteysongelman syyn nopeasti. Lähetä näiden lokien kopiot yhdessä palvelupyynnön kanssa, kun otat yhteyden tukeen.

> 1.    Kopioi RegisterETW.zip-tiedosto asiakasohjelman työasemaan (ensisijaisesti pöytäkoneeseen) ja pura [RegisterETW.zip](https://dev.azure.com/msdyneng/e6f12261-a46a-4af1-ac0c-e22bc2c5a478/_apis/git/repositories/ff923027-67f0-43fb-b63c-6d6b6423840f/Items?path=%2F.attachments%2FRegisterETW-c1a35291-6aa6-4462-a2bc-4ba117fd5f8e.zip&download=false&resolveLfs=true&%24format=octetStream&api-version=5.0-preview.1&sanitize=true&versionDescriptor.version=wikiMaster).

> 2.    Varmista, että Windowsin tapahtumien katseluohjelma on suljettu.

> 3.    Avaa järjestelmänvalvojan PowerShell-komentorivi ja siirry hakemistoon, jossa RegisterETW.ps1 sijaitsee.

> 4.    Suorita seuraava komento: .\RegisterETW.ps1
   
   Onnistunut PowerShell-tuloste vahvistetaan sanomalla **RegisterETW-komentosarja valmis**.
Avaa tapahtumien katseluohjelma uudelleen, jolloin seuraavat lokit ovat kohdassa **Microsoft > Dynamics**: * MR-Client * MR-DVT * MR-Integration * MR-Logger * MR-Reporting * MR_SchedulerTasks * MR-Sql * MR-TraceManager
   
> 5. Toisinna ongelma Report Designerissa.
   
> 6. Vie MR-Logger-tapahtumat tapahtumien katseluohjelmassa.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Taloushallinnon raportoinnin yhdistämisongelmien vianmääritys

Ongelma: vastaanotettiin virhe, jonka mukaan taloushallinnon raportointipalvelimeen ei voi muodostaa yhteyttä.

* Määritä, esiintyykö ongelma Chrome- ja Edge-selaimissa.
* Jos ongelma esiintyy vain yhdessä selaimessa, kyse voi olla ClickOnce-ongelmassa. 
* Kun yhteysvirhesanoma annetaan, testaa yhteyttä valitsemalla **Testi** ja katso, mikä sanoma avautuu. 
* Ongelman syy voi olla se, että toisella käyttäjällä ei ole taloushallinnon raportoinnin käyttöoikeutta. Jos käyttäjällä ei ole käyttöoikeutta, avautuva sanoma ilmoittaa, ettei heillä ole käyttöoikeutta.
* Jos ongelma esiintyy useissa selaimissa, varmista, että työaseman kellon määrityksenä on Automaattinen.
* Tee yhteistyötä käyttäjän kanssa, jolla on suojauksenvalvojan oikeudet Dynamics 365 Financessa ja järjestelmänvalvojan oikeudet verkkotoimialueella, työasemaan kirjautumisessa. Näin voidaan tarkistaa, voidaanko yhteys muodostaa. Jos yhteydenmuodostus onnistuu, ongelma voi liittyä verkko-oikeuksiin.
* Poista palomuuri tilapäisesti käytöstä työasemassa. Jos yhteys voidaan nyt muodostaa Report Designeriin, ongelma liittyy palomuuriin. Ratkaise ongelma yhteistyössä organisaation IT-osaston kanssa.

## <a name="additional-resources"></a>Lisäresurssit
- [Näytä raportit](view-financial-reports.md)
- [Talousraporttien raportointipuiden määritykset](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
