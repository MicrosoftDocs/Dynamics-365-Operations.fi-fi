---
title: Kulujen hallinnan Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään Power BI -sisältöpaketin kulujen hallinnan sisältöä.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a07d9ed7e4c57c2444d1c2a017109509c153aad4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/07/2019
ms.locfileid: "1503124"
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
