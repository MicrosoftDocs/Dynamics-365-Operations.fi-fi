---
title: Kulujen hallinnan Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään Power BI -sisältöpaketin kulujen hallinnan sisältöä.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: aadf43d478eb4bf5af20df02dcc6399a7a2e71a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743504"
---
# <a name="expense-management-power-bi-content"></a>Kulujen hallinnan Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä aiheessa käsitellään Power BI -sisällön kulujen hallinnan sisältöä. 

## <a name="overview"></a>Yleiskuvaus
Versiosta 8.1 alkaen kulujen hallinnan kanssa on käytettävissä kaksi Power BI -sisältöpakettia. 
- Kuluraportteja lähettäville työntekijöille on suunniteltu henkilökohtainen koontinäyttö. 

  Tämä koontinäyttö on mukautettu antamaan käyttäjille tärkeitä tietoja lähettämättömistä ja lähetetyistä summista sekä historiatietoja ja muita tietoja kulutapahtumien historiasta. Henkilökohtaisessa koontinäytössä on yksi sivu, jossa on käyttäjän kannalta tärkeimmät tiedot.

- Ostoreskontran käyttäjille ja esimiehille on oma hallinnan koontinäyttö. Koontinäyttö on suunniteltu siten, että sen avulla voi seurata työntekijän kokonaiskuluja ja raportoida niistä. Siinä tärkeitä kulumittareita, kuten lähettämättömät kulut, kilometrimäärä ja kuluraporttien keskimääräinen summa. Se käyttää tapahtumatietoja, ja siinä on kaikkien yritysten kulujen hallinnan koostenäkymät. Siinä on myös työntekijäkohtainen erittely ja mahdollisuus lisätä taloushallinnon dimension tietoja. Järjestelmänvalvojan kuluanalytiikan sisältö: 
  - Yhteenvetosivu, jolla on tärkeitä mittareita kulujen summista sekä tietoja luonnosvaiheessa olevista, keskeneräisistä ja valmiista kuluraporteista. 
  - Työntekijätilastosivulla voi tarkastella työntekijäkohtaisia tietoja ajan, kustannuslajin ja tilastoryhmän perusteella. 
  - Työntekijän vertailusivulla voi vertailla useita työntekijöitä aikavälillä. 

Kaikkien summat näytetään yrityksen valuuttana. Kaikkien yritysten tiedot näytetään, mutta voit tarvittaessa lisätä yrityssuodattimen. 

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
Expense Admin Dashboard.pbix- ja Expense Personal Dashboard.pbix-tiedostot (Power BI -sisältö) sijaistee Microsoft Dynamics Lifecycle Servicesin (LCS) jaettujen resurssien kirjastosta. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).
Sisältö on käytettävissä kulujenhallinnan työtilassa upotetun Power BI -sisältönä. Kulun omistaja voi käyttää henkilökohtaisia kuluja itse, kun taas ostoreskontran käyttäjät ja esimiehet voivat käyttää kaikkien käyttäjien kulutietojen hallintasisältöä.

## <a name="refreshing-the-power-bi-content"></a>Power BI -sisällön päivittäminen
Kulujenhallinnan Power BI -sisältö edellyttää, että TrvBiExpenseMeasurement-mitta ja BudgetActivityMeasure päivitetään yksikkösäilöstä. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mittarit, jotka sisältyvät Power BI -sisältöön
Sisältö sisältää joukon raporttisivuja. Jokainen sivu koostuu joukosta mittareita, jotka ovat visualisoitu kaavioiden, ruutujen ja taulukoiden muodossa. Seuraavassa taulukossa on yhteenveto Power BI -sisällössä käytettävistä visualisoinneista.

**Henkilökohtainen kuluanalytiikka**

| Raporttisivu | Visualisointi                             |
|-------------|-------------------------------------------|
| Omat kulut | Kilometrikorvauksen määrä                         |
|             | Keskeneräiset kuluraportit                |
|             | Nro lähettämättömiä kuluja               |
|             | Maksettavat henkilökohtaiset kulut              |
|             | Lähettämätön määrä                        |
|             | Lähetetty määrä                          |
|             | Hyvistä odottava summa             |
|             | Kuluraportit sekä niiden summat ja tila   |
|             | Lähetetyt mutta hyväksymättömät kuluraportit  |
|             | Kulut kustannustyypin mukaan                     |
|             | Kulut kauppiaan mukaan                      |
|             | Kulut käsiteltyjen kulujen mukaan            |
|             | Kulut projektin mukaan                       |
|             | Tapahtuman kokonaissumman kehittyminen        |

**Järjestelmänvalvojan kuluanalytiikka**

| Raporttisivu         | Visualisointi                           |           
|---------------------|-----------------------------------------|
| Kuluyhteenveto    | Kulusummaluonnos                   |
|                     | Kululuonnosrivien määrä           |
|                     | Kululuonnosrivit                     |
|                     | Kuluraportin käytäntörikkeet        |
|                     | Avoin summa                      |
|                     | Lähetetyt mutta hyväksymättömät kulut       |
|                     | Hyväksytyt kulut                       |
|                     | Kulujen kokonaissumma                    |
|                     | Kuluraportin yhteenveto                |
|                     | Kulut kustannustyypin mukaan                   |
|                     | Kulut kauppiaan mukaan                    |
|                     | Kulut työntekijän mukaan                   |
|                     | Kulujen vs. projekti                     |
| Työntekijävertailu | Kulusummat                         |
|                     | Kulusummien kehittymien työntekijän mukaan   |
| Työntekijätilastot | Kuluraportit kustannustyypin mukaan            |
|                     | Henkilökohtaiset kulut                       |
|                     | Kuluraportit tilastoryhmän mukaan     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]