---
title: "Käytäntöpäällikön Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu käytäntöpäällikön Power BI -sisältöön. Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: fi-fi
ms.lasthandoff: 06/20/2017


---

# Käytäntöpäällikön Power BI -sisältö
<a id="practice-manager-power-bi-content" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä aiheessa kuvataan, mitä kuuluu **käytäntöpäällikön** Microsoft Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## Yleiskuvaus
<a id="overview" class="xliff"></a>

**Käytäntöpäällikön** Power BI -sisältö on luotu käytäntö- ja projektipäälliköille. Se sisältää organisaatiossa käsiteltäviin projekteihin liittyviä tärkeitä mittareita. Koontinäyttö sisältää projektien ja liittyvien asiakkaiden yleiskatsauksen. Raporttitason suodatinta voidaan käyttää tiettyjen yritysten raportoinnissa. Tämä Power BI -sisältö hakee tietoja projektikirjanpidon koostemitoista.

**Käytäntöpäällikön** Power BI -sisältö sisältää viisi raporttisivua. Yksi sivu sisältää yleiskatsauksen ja neljällä sivulla on tietoja projektikustannuksista, tuotoista, ansaitun arvon hallinnasta ja eri dimensioiden mukaan eritellyistä tuntimittareista.

Kaikki sisällön summat näytetään järjestelmän valuutassa. Järjestelmän valuutta määritetään **Järjestelmän parametrit** -sivulla.

## Power BI -sisällön käyttö
<a id="accessing-the-power-bi-content" class="xliff"></a>
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **käytäntöpäällikön** Power BI -sisällön raportit näkyvät **projektinhallinnan** työtilassa.

## Raportit, jotka sisältyvät Power BI -sisältöön
<a id="reports-that-are-included-in-the-power-bi-content" class="xliff"></a>

Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **käytäntöpäällikön** Power BI -sisällön kultakin raporttisivulta.

| Raporttisivu       | Mittarit |
|-------------------|---------|
| Projektien yleiskatsaus | <ul><li>Luodut projektit</li><li>Arvioidut projektit</li><li>Keskeneräiset projektit</li><li>Projektien määrä vaiheen mukaan</li><li>Projektien määrä kaupungin mukaan</li><li>Toteutunut tuotto asiakkaan mukaan</li><li>Budjetoitu käyttökate projektin mukaan</li><li>Ansaitun arvon hallinnan yleiskatsaus</li></ul> |
| Kustannus              | <ul><li>Toteutunut vs. budjetoitu kustannus kuukauden mukaan</li><li>Toteutunut vs. budjetoitu kustannus vuoden mukaan</li><li>Toteutunut vs. budjetoitu kustannus luokan mukaan</li><li>Toteutunut kustannus tapahtumatyypin mukaan</li></ul> |
| Myyntituotto           | <ul><li>Toteutunut tuotto kuukauden mukaan</li><li>Toteutunut tuotto postinumeron mukaan</li><li>Toteutunut vs. budjetoitu tuotto luokan mukaan</li><li>Toteutunut tuotto asiakkaan toimialan mukaan</li></ul> |
| Ansaitun arvon menetelmä               | Kustannusten ja aikataulutehokkuuden indeksi projektin mukaan |
| Tunnit             | <ul><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit vs. budjetoidut tunnit</li><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit projektin mukaan</li><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit resurssin mukaan</li><li>Toteutuneiden laskutettavien tuntien suhdeluku projektin mukaan</li><li>Toteutuneiden laskutettavien tuntien suhdeluku resurssin mukaan</li></ul> |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Pohjana olevien tietojen vientitoiminnon avulla voit viedä visualisoinnin kokoamat pohjana olevat tiedot.

## Power BI -sisällön laajentaminen
<a id="extending-the-power-bi-content" class="xliff"></a>
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä. Voit muokata nämä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista ne sitten analysoitavaksi Power BI.com -vuokraajassa. 

**Käytäntöpäällikön** Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

Muista ladata käyttämääsi Dynamics 365:n versiota vastaava **käytäntöpäällikön** sisältö.

## Tietomallin ja yksiköiden tiedot
<a id="understanding-the-data-model-and-entities" class="xliff"></a>

Seuraavia tietoja käytetään **käytäntöpäällikön** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md).

Seuraavissa osissa käsitellään kussakin yksikössä käytössä olevat koostetut mitat.

### Yksikkö: ProjectAccountingCube_ActualHourUtilization
<a id="entity-projectaccountingcubeactualhourutilization" class="xliff"></a>
**Tietolähde:** ProjEmplTrans

| Tärkeät koostemitat      | Kenttä                              | kuvaus | 
|--------------------------------|------------------------------------|-------------|
| Todellinen laskutus - käyttötunnit | Sum(ActualUtilizationBillableRate) | Toteutuneiden laskutettujen käyttötuntien kokonaismäärä. |
| Todellinen laskutus - rasitetunnit   | Sum(ActualBurdenBillableRate)      | Toteutuneen kuormituksen kokonaismäärä. |

### Yksikkö: ProjectAccountingCube_Actuals
<a id="entity-projectaccountingcubeactuals" class="xliff"></a>
**Tietolähde:** ProjTransPosting

| Tärkeät koostemitat | Kenttä              | kuvaus | 
|---------------------------|--------------------|-------------|
| Todellinen tuotto            | Sum(ActualRevenue) | Kaikkien tapahtumien kirjatun tuoton kokonaismäärä. |   
| Toteutunut kustannus               | Sum(ActualCost)    | Kaikkien tapahtumatyyppien kirjattujen kustannusten kokonaismäärä. |

### Yksikkö: ProjectAccountingCube_Customer
<a id="entity-projectaccountingcubecustomer" class="xliff"></a>
**Tietolähde:** CustTable

| Tärkeät koostemitat | Kenttä                                            | kuvaus | 
|---------------------------|--------------------------------------------------|-------------|
| Projektien lukumäärä        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Käytettävissä olevien projektien määrä. |


### Yksikkö: ProjectAccountingCube_Forecasts
<a id="entity-projectaccountingcubeforecasts" class="xliff"></a>
**Tietolähde:** ProjTransBudget

| Tärkeät koostemitat | Kenttä                  | kuvaus | 
|---------------------------|------------------------|-------------|
| Budjetoitu kustannus               | Sum(BudgetCost)        | Kaikkien tapahtumatyyppien ennustettujen kustannusten kokonaismäärä. |
| Budjetoitu tuotto            | Sum(BudgetRevenue)     | Ennustetun jaksotetun tai laskutetun tuoton kokonaismäärä.  |
| Budjetoitu käyttökate       | Sum(BudgetGrossMargin) | Ennustetun kokonaistuoton summan ja ennustettujen kokonaiskustannusten summan välinen ero. |

### Yksikkö: ProjectAccountingCube_ProjectPlanCostsView
<a id="entity-projectaccountingcubeprojectplancostsview" class="xliff"></a>
**Tietolähde:** Projekti

| Tärkeät koostemitat | Kenttä                    | kuvaus | 
|---------------------------|--------------------------|-------------|
| Suunniteltu kustannus              | Sum(SumOfTotalCostPrice) | Kaikkien projektitapahtumatyyppien ja suunniteltujen tehtävien kokonaiskustannushinta-arviot. |

### Yksikkö: ProjectAccountingCube_Projects
<a id="entity-projectaccountingcubeprojects" class="xliff"></a>
**Tietolähde:** Projekti

| Tärkeät koostemitat    | Kenttä | kuvaus | 
|------------------------------|-------|-------------|
| Kustannustehokkuuden indeksi       | ProjectAccountingCube_Projects [Ansaittu arvo] / ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] | Toteutuneilla kokonaiskustannuksilla jaetun ansaitun kokonaisarvon laskelma. |
| Aikataulutehokkuuden indeksi   | ProjectAccountingCube_Projects [Ansaittu arvo] / ProjectAccountingCube_Projects [Valmiiden tehtävien suunnitellut kokonaiskustannukset] | Suunnitelluilla kokonaiskustannuksilla jaetun ansaitun kokonaisarvon laskelma. |
| Työn valmiusprosentti | Työn valmiusprosentti = ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] / (ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] + ProjectAccountingCube_Projects [Projektin suunnitellut kokonaiskustannukset] - ProjectAccountingCube_Projects [Valmiiden tehtävien suunnitellut kokonaiskustannukset) | Työn valmistumisprosentti yhteensä, joka perustuu projektin valmistuneiden tehtävien toteutuneisiin kokonaiskustannuksiin ja suunniteltuihin kustannuksiin. |
| Toteutunut lasketettavien tuntien suhde  | ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat käyttötunnit yhteensä] / (ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat tunnit yhteensä] + ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat rasitetunnit yhteensä) | Toteutuneiden laskutettavien tuntien kokonaismäärä käyttötuntien ja rasitetuntien perusteella. |
| Ansaittu arvo                 | ProjectAccountingCube_Projects [Projektin suunnitellut kokonaiskustannukset] * ProjectAccountingCube_Projects [Työn valmiusprosentti] | Suunnitellut kokonaiskustannukset kerrottuna työn valmistumisprosentilla. |

### Yksikkö: ProjectAccountingCube_TotalEstimatedCosts
<a id="entity-projectaccountingcubetotalestimatedcosts" class="xliff"></a> 
**Tietolähde:** ProjTable

| Tärkeät koostemitat       | Kenttä               | kuvaus | 
|---------------------------------|---------------------|-------------|
| Valmiin tehtävän suunniteltu kustannus | Sum(TotalCostPrice) | Kaikkien projektitapahtumatyyppien ja valmiiden tehtävien kokonaiskustannushinta-arviot. |

