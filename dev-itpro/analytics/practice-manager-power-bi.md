---
title: "Käytäntöpäällikön Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mitä kuuluu käytäntöpäällikön Power BI -sisältöön. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Käytäntöpäällikön Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, mitä kuuluu **käytäntöpäällikön** Microsoft Power BI -sisältöön. Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

## <a name="overview"></a>Yleiskuvaus

**Käytäntöpäällikön** Power BI -sisältö on luotu käytäntö- ja projektipäälliköille. Se sisältää organisaatiossa käsiteltäviin projekteihin liittyviä tärkeitä mittareita. Koontinäyttö sisältää projektien ja liittyvien asiakkaiden yleiskatsauksen. Raporttitason suodatinta voidaan käyttää tiettyjen yritysten raportoinnissa. Tämä Power BI sisältö hakee tiedot Microsoft Dynamics 365 for Operations -ohjelman projektikirjanpidon koostetuista mitoista.

**Käytäntöpäällikön** Power BI -sisältö sisältää viisi raporttisivua. Yksi sivu sisältää yleiskatsauksen ja neljä sivua projektikustannukset, tuotot, ansaitun arvon hallinnan ja tunnin mittausarvot, jotka on jaettu eri dimensioille.

Kaikki sisällön summat näytetään järjestelmän valuutassa. Järjestelmän valuutta määritetään **Järjestelmän parametrit** -sivulla.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö

**Käytäntöpäällikön** Power BI -sisältö löytyy Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Dynamics 365 for Operationsin tietoihin, on artikkelissa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).

Katso Power BI -sisällön käyttöönotosta kertova esittely [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -palveluissa](https://mix.office.com/watch/9puyb1b2xs1w) -kohdan Office mixistä.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön

Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **käytäntöpäällikön** Power BI -sisällön kultakin raporttisivulta.

| Raporttisivu                                          | Mittarit               |
|------------------------------------------------------|-----------------------------------------------|
| Koontinäyttö  | Luodut projektit<br>Arvioidut projektit<br>Keskeneräiset projektit<br>Projektien määrä vaiheen mukaan<br>Projektien määrä kaupungin mukaan<br>Toteutunut tuotto asiakkaan mukaan<br>Budjetoitu käyttökate projektin mukaan<br>Ansaitun arvon hallinnan yleiskatsaus |
| Kustannus                                                 | Toteutunut vs. budjettikustannus kuukauden mukaan<br>Toteutunut vs. budjettikustannus vuoden mukaan<br>Toteutunut vs. budjettikustannus luokan mukaan<br>Toteutunut kustannus tapahtumatyypin mukaan       |
| Myyntituotto                                              | Toteutunut tuotto kuukauden mukaan<br>Toteutunut tuotto postinumeron mukaan<br>Toteutunut vs. budjetoitu tuotto luokan mukaan<br>Toteutunut tuotto asiakkaan toimialan mukaan        |
| Ansaitun arvon menetelmä                                                  | Kustannusten ja aikataulutehokkuuden indeksi projektin mukaan                 |
| Tunnit                                                | Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit vs. budjetoidut tunnit<br>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit projektin mukaan<br>Toteutuneet laskutettavat käyttötunnit vs. toteutuneet laskutettavat rasitetunnit resurssin mukaan<br>Toteutuneiden laskutettavien tuntien suhdeluku projektin mukaan<br>Toteutuneiden laskutettavien tuntien suhdeluku resurssin mukaan |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Pohjana olevien tietojen vientitoiminnon avulla voit viedä visualisoinnin kokoamat pohjana olevat tiedot.

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

Dynamics 365 for Operations -tietoja käytetään **käytäntöpäällikön** Power BI -sisällön raporttisivujen täyttämisessä. Nämä tiedot esitetään koottuina mittauksina, jotka vaiheistetaan yksikkösäilössä, joka on analytiikkaa varten optimoitu Microsoft SQL -tietokanta. Lisätietoja on ohjeaiheessa [yleiskatsaus Power BI:n integraatiosta yksikkökaupan kanssa](power-bi-integration-entity-store.md).

Seuraavissa osissa esitellään kussakin yksikössä käytössä olevat koostetut mitat.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Yksikkö: ProjectAccountingCube_ActualHourUtilization
**Tietolähde**: ProjEmplTrans

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Toteutuneiden laskutettujen käyttötuntien kokonaismäärä |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Toteutuneen kuormituksen kokonaismäärä             |

### <a name="entity-projectaccountingcubeactuals"></a>Yksikkö: ProjectAccountingCube_Actuals
**Tietolähde**: ProjTransPosting

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Kaikkien tapahtumien kirjatun tuoton kokonaismäärä |   
| ActualCost   |                             Sum(ActualCost)           |    Kaikkien tapahtumatyyppien kirjattujen kustannusten kokonaismäärä    |

### <a name="entity-projectaccountingcubecustomer"></a>Yksikkö: ProjectAccountingCube_Customer
**Tietolähde**: CustTable

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Projektien lukumäärä        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Käytettävissä olevien projektien määrä    |


### <a name="entity-projectaccountingcubeforecasts"></a>Yksikkö: ProjectAccountingCube_Forecasts
**Tietolähde**: ProjTransBudget

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Kaikkien tapahtumatyyppien ennustettujen kustannusten kokonaismäärä     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Ennustetun jaksotetun/laskutetun tuoton kokonaismäärä         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Ennustetun kokonaistuoton summan ja ennustettujen kokonaiskustannusten summan välinen ero

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Yksikkö: ProjectAccountingCube_ProjectPlanCostsView
**Tietolähdee**: Project

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Kaikkien projektitapahtumatyyppien ja suunniteltujen tehtävien kokonaiskustannushinta arvioissa |

### <a name="entity-projectaccountingcubeprojects"></a>Yksikkö: ProjectAccountingCube_Projects
**Tietolähde**: Project

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Kustannustehokkuuden indeksi  |ProjectAccountingCube_Projects [Ansaittu arvo] / ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] |     Ansaittu kokonaisarvo jaettuna toteutuneilla kokonaiskustannuksilla - laskelma|
|  Aikataulutehokkuuden indeksi |ProjectAccountingCube_Projects [Ansaittu arvo] / ProjectAccountingCube_Projects [Valmiiden tehtävien suunnitellut kokonaiskustannukset]|Ansaittu kokonaisarvo jaettuna suunnitelluilla kokonaiskustannuksilla - laskelma |
|Työn valmiusprosentti |Työn valmiusprosentti = ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] / (ProjectAccountingCube_Projects [Valmiiden tehtävien toteutuneet kokonaiskustannukset] + ProjectAccountingCube_Projects [Projektin suunnitellut kokonaiskustannukset] - ProjectAccountingCube_Projects [Valmiiden tehtävien suunnitellut kokonaiskustannukset)|Työn valmistumisprosentti yhteensä, joka perustuu projektin valmistuneen tehtävän toteutuneisiin kokonaiskustannuksiin ja suunniteltuihin kustannuksiin|
|Projektin toteutuneiden laskutettavien tuntien suhdeluku|ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat käyttötunnit yhteensä] / (ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat tunnit yhteensä] + ProjectAccountingCube_Projects [Projektin toteutuneet laskutettavat rasitetunnit yhteensä)|Toteutuneet laskutettavat tunnit yhteensä käytön ja rasitteen perusteella|
|Ansaittu arvo|ProjectAccountingCube_Projects [Projektin suunnitellut kokonaiskustannukset] * ProjectAccountingCube_Projects [Työn valmiusprosentti]|Suunnitellut kokonaiskustannukset kerrottuna työn valmistumisprosentilla|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Yksikkö: ProjectAccountingCube_TotalEstimatedCosts 
**Tietolähde**: ProjTable

| Tärkeät koostemitat                | Kenttä                                | kuvaus                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Kaikkien projektitapahtumatyyppien ja valmiiden tehtävien kokonaiskustannushinta arvioissa|

## <a name="additional-resources"></a>Lisäresurssit

Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

- [Tietoyksiköt](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Työtilojen Power BI -integroinnin konfiguroiminen](configure-power-bi-integration.md)

