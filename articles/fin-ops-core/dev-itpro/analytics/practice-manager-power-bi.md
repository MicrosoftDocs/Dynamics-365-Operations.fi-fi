---
title: Käytäntöpäällikön Power BI -sisältö
description: Tässä artikkelissa kuvataan, mitä kuuluu käytäntöpäällikön Power BI -sisältöön.
author: sericks007
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.assetid: ''
ms.search.form: ProjManagementWorkspace
ms.openlocfilehash: 92c2881c89da0b23e3a66c0f8bbcafd91c38c6e3
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206501"
---
# <a name="practice-manager-power-bi-content"></a>Käytäntöpäällikön Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan, mitä kuuluu **käytäntöpäällikön** Microsoft Power BI -sisältöön. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytettävistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Käytäntöpäällikön** Power BI -sisältö on luotu käytäntö- ja projektipäälliköille. Se sisältää organisaatiossa käsiteltäviin projekteihin liittyviä tärkeitä mittareita. Koontinäyttö sisältää projektien ja liittyvien asiakkaiden yleiskatsauksen. Raporttitason suodatinta voidaan käyttää tiettyjen yritysten raportoinnissa. Tämä Power BI -sisältö hakee tietoja projektikirjanpidon koostemitoista.

**Käytäntöpäällikön** Power BI -sisältö sisältää viisi raporttisivua. Yksi sivu sisältää yleiskatsauksen ja neljällä sivulla on tietoja projektikustannuksista, tuotoista, ansaitun arvon hallinnasta ja eri dimensioiden mukaan eritellyistä tuntimittareista.

Kaikki sisällön summat näytetään järjestelmän valuutassa. Järjestelmän valuutta määritetään **Järjestelmän parametrit** -sivulla.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen

**Käytäntöpäällikön** Power BI -sisältö näkyy **Projektinhallinta**-työtilassa.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön

Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **käytäntöpäällikön** Power BI -sisällön kultakin raporttisivulta.

| Raporttisivu       | Mittarit |
|-------------------|---------|
| Projektien yleiskatsaus | <ul><li>Luodut projektit</li><li>Arvioidut projektit</li><li>Keskeneräiset projektit</li><li>Toteutunut tuotto asiakkaan mukaan</li><li>Budjetoitu käyttökate projektin mukaan</li><li>Ansaitun arvon hallinnan yleiskatsaus</li></ul> |
| Kustannus              | <ul><li>Toteutunut vs. budjetoitu kustannus kuukauden mukaan</li><li>Toteutunut vs. budjetoitu kustannus vuoden mukaan</li><li>Toteutunut vs. budjetoitu kustannus luokan mukaan</li><li>Toteutunut kustannus tapahtumatyypin mukaan</li></ul> |
| Myyntituotto           | <ul><li>Toteutunut tuotto kuukauden mukaan</li><li>Toteutunut tuotto postinumeron mukaan</li><li>Toteutunut vs. budjetoitu tuotto luokan mukaan</li><li>Toteutunut tuotto asiakkaan toimialan mukaan</li></ul> |
| Ansaitun arvon menetelmä               | Kustannusten ja aikataulutehokkuuden indeksi projektin mukaan |
| Tunnit             | <ul><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit vs. budjetoidut tunnit</li><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit projektin mukaan</li><li>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit resurssin mukaan</li><li>Toteutuneiden laskutettavien tuntien suhdeluku projektin mukaan</li><li>Toteutuneiden laskutettavien tuntien suhdeluku resurssin mukaan</li></ul> |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Pohjana olevien tietojen vientitoiminnon avulla voit viedä visualisoinnin kokoamat pohjana olevat tiedot.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

Seuraavia tietoja käytetään **käytäntöpäällikön** Power BI -sisällön raporttisivujen täyttämiseen. Nämä tiedot esitetään koottuina mittauksina, joka vaiheistetaan yksikkösäilössä. Yksikkösäilö on analytiikkaa varten optimoitu Microsoft SQL Server -tietokanta. Lisätietoja on kohdassa [Power BI:n ja yksikkösäilön integraatio](power-bi-integration-entity-store.md).

Seuraavissa osissa käsitellään kussakin yksikössä käytössä olevat koostetut mitat.

### <a name="entity-projectaccountingcube_actualhourutilization"></a>Yksikkö: ProjectAccountingCube\_ActualHourUtilization
**Tietolähde:** ProjEmplTrans

| Tärkeät koostemitat      | Kenttä                              | kuvaus |
|--------------------------------|------------------------------------|-------------|
| Todellinen laskutus - käyttötunnit | Sum(ActualUtilizationBillableRate) | Toteutuneiden laskutettujen käyttötuntien kokonaismäärä. |
| Todellinen laskutus - rasitetunnit   | Sum(ActualBurdenBillableRate)      | Toteutuneen kuormituksen kokonaismäärä. |

### <a name="entity-projectaccountingcube_actuals"></a>Yksikkö: ProjectAccountingCube\_Actuals
**Tietolähde:** ProjTransPosting

| Tärkeät koostemitat | Kenttä              | kuvaus |
|---------------------------|--------------------|-------------|
| Todellinen tuotto            | Sum(ActualRevenue) | Kaikkien tapahtumien kirjatun tuoton kokonaismäärä. |
| Toteutunut kustannus               | Sum(ActualCost)    | Kaikkien tapahtumatyyppien kirjattujen kustannusten kokonaismäärä. |

### <a name="entity-projectaccountingcube_customer"></a>Yksikkö: ProjectAccountingCube\_Customer
**Tietolähde:** CustTable

| Tärkeät koostemitat | Kenttä                                             | kuvaus |
|---------------------------|---------------------------------------------------|-------------|
| Projektien lukumäärä        | COUNTA(ProjectAccountingCube\_Projects\[PROJECTS\]) | Käytettävissä olevien projektien määrä. |

### <a name="entity-projectaccountingcube_forecasts"></a>Yksikkö: ProjectAccountingCube\_Forecasts
**Tietolähde:** ProjTransBudget

| Tärkeät koostemitat | Kenttä                  | kuvaus |
|---------------------------|------------------------|-------------|
| Budjetoitu kustannus               | Sum(BudgetCost)        | Kaikkien tapahtumatyyppien ennustettujen kustannusten kokonaismäärä. |
| Budjetoitu tuotto            | Sum(BudgetRevenue)     | Ennustetun jaksotetun tai laskutetun tuoton kokonaismäärä. |
| Budjetoitu käyttökate       | Sum(BudgetGrossMargin) | Ennustetun kokonaistuoton summan ja ennustettujen kokonaiskustannusten summan välinen ero. |

### <a name="entity-projectaccountingcube_projectplancostsview"></a>Yksikkö: ProjectAccountingCube\_ProjectPlanCostsView
**Tietolähde:** Projekti

| Tärkeät koostemitat | Kenttä                    | kuvaus |
|---------------------------|--------------------------|-------------|
| Suunniteltu kustannus              | Sum(SumOfTotalCostPrice) | Kaikkien projektitapahtumatyyppien ja suunniteltujen tehtävien kokonaiskustannushinta-arviot. |

### <a name="entity-projectaccountingcube_projects"></a>Yksikkö: ProjectAccountingCube\_Projects
**Tietolähde:** Projekti

| Tärkeät koostemitat    | Kenttä | kuvaus |
|------------------------------|-------|-------------|
| Kustannustehokkuuden indeksi       | ProjectAccountingCube\_Projects\[Ansaittu arvo\] ÷ ProjectAccountingCube\_Projects\[Valmiiden tehtävien toteutuneet kokonaiskustannukset\] | Toteutuneilla kokonaiskustannuksilla jaetun ansaitun kokonaisarvon laskelma. |
| Aikataulutehokkuuden indeksi   | ProjectAccountingCube\_Projects\[Ansaittu arvo\] ÷ ProjectAccountingCube\_Projects\[Valmiiden tehtävien suunnitellut kokonaiskustannukset\] | Suunnitelluilla kokonaiskustannuksilla jaetun ansaitun kokonaisarvon laskelma. |
| Työn valmiusprosentti | Työn valmiusprosentti = ProjectAccountingCube\_Projects\[Valmiiden tehtävien toteutuneet kokonaiskustannukset\] ÷ (ProjectAccountingCube\_Projects\[Valmiiden tehtävien toteutuneet kokonaiskustannukset\] + ProjectAccountingCube\_Projects\[Projektin suunnitellut kokonaiskustannukset\] – ProjectAccountingCube\_Projects\[Valmiiden tehtävien suunnitellut kokonaiskustannukset\]) | Työn valmistumisprosentti yhteensä, joka perustuu projektin valmistuneiden tehtävien toteutuneisiin kokonaiskustannuksiin ja suunniteltuihin kustannuksiin. |
| Toteutunut lasketettavien tuntien suhde  | ProjectAccountingCube\_Projects\[Projektin toteutuneet laskutettavat käyttötunnit yhteensä\] ÷ (ProjectAccountingCube\_Projects\[Projektin toteutuneet laskutettavat tunnit yhteensä\] + ProjectAccountingCube\_Projects\[Projektin toteutuneet laskutettavat rasitetunnit yhteensä\]) | Toteutuneiden laskutettavien tuntien kokonaismäärä käyttötuntien ja rasitetuntien perusteella. |
| Ansaittu arvo                 | ProjectAccountingCube\_Projects\[Projektin suunnitellut kokonaiskustannukset\] × ProjectAccountingCube\_Projects\[Työn valmiusprosentti\] | Suunnitellut kokonaiskustannukset kerrottuna työn valmistumisprosentilla. |

### <a name="entity-projectaccountingcube_totalestimatedcosts"></a>Yksikkö: ProjectAccountingCube\_TotalEstimatedCosts 
**Tietolähde:** ProjTable

| Tärkeät koostemitat       | Kenttä               | kuvaus |
|---------------------------------|---------------------|-------------|
| Valmiin tehtävän suunniteltu kustannus | Sum(TotalCostPrice) | Kaikkien projektitapahtumatyyppien ja valmiiden tehtävien kokonaiskustannushinta-arviot. |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
