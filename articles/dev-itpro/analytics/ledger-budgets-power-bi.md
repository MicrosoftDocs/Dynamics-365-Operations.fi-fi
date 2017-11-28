---
title: "Todellinen vs. budjetti – Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään Todellinen vs. budjetti – Power BI -sisältöä Siinä selitetään, miten sisältöön sisältyvät raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä."
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f09af96fb1c76d8737d2c535f1a46565a18deca0
ms.contentlocale: fi-fi
ms.lasthandoff: 11/03/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>Todellinen vs. budjetti – Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa käsitellään **Todellinen vs. budjetti** – Microsoft Power BI -sisältöä Siinä kuvataan, miten avaat Power BI -raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä. 

# <a name="overview"></a>Yleiskuvaus

**Todellinen vs. budjetti** – Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa todellisen ja budjetoidun suorituksen vertailun seurannasta. **Todellinen vs. budjetti** – Power BI -sisältö tuo näkyvyyttä budjetin variansseihin. Voit analysoida kuluvan vuoden budjettia tililuokan, budjettikoodin, päätilin, päätilin kuvauksen tai tilikauden mukaan. Saat tällä tavoin paremman käsityksen varianssien syystä. 

# <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttö
Jos käytössä on Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys, **Todellinen vs. budjetti** – Power BI -sisällön raportit näkyvät **Kirjanpitobudjetit ja ennusteet**- ja **Talousjohtaja**-työtilassa.

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **Todellinen vs. budjetti** – Power BI -sisällön kultakin raporttisivulta.

| Raportti                      | Mittarit |
|-----------------------------|---------|
| Kulut – todellinen vs. budjetti | <ul><li>Kuluvan vuoden kokonaiskulut</li><li>Kuluvan vuoden budjetoidut kokonaiskulut</li></ul> |
| Tuotto – todellinen vs. budjetti  | <ul><li>Kuluvan vuoden kokonaistuotto</li><li>Kuluvan vuoden budjetoitu kokonaistuotto</li><ul> |
| Kulu                     | <ul><li>Kuluvan vuoden kokonaiskulut</li><li>Budjettiin perustuva kulutavoite </li><ul> |
| Myyntituotto                     | <ul><li>Kuluvan vuoden kokonaistuotto</li><li>Budjettiin perustuva tuottotavoite </li><ul> |
| Nettotuotto                  | <ul><li>Kuluvan vuoden nettotulot</li><li>Budjettiin perustuva nettotulotavoite </li><ul> |

## <a name="extending-the-power-bi-content"></a>Power BI -sisällön laajentaminen
Jos käytät Microsoft Dynamics Lifecycle Servicesin (LCS) sisältöpaketteja, voit tehdä erinomaisia analyyseja henkilöille, jotka eivät käytä Microsoft Dynamics 365:tä. Voit muokata näitä sisältöpaketit sisältämään muita raportteja ja visuaalisia tietoja ja julkaista sitten sisältöpaketit analysoitavaksi Power BI.com -vuokraajassa. 

**Todellinen vs. budjetti** – Power BI -sisältö sijaitsee LCS:n Jaettu omaisuus -kirjastossa. Lisätietoja sisällön lataamisesta ja sen käyttöönottamisesta organisaatiossa on ohjeaiheessa [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md). Katso Power BI -sisällön käyttöönotosta kertova esittely Office Mixin kohdassa [Microsoftin ja kumppaneiden Power BI -sisältö Dynamics Lifecycle Services -sovelluksessa](https://mix.office.com/watch/9puyb1b2xs1w).

# <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

| Kokonaisuus                    | Sisältö |
|---------------------------|----------|
| Kirjanpitotehtävät | Kirjanpidon tapahtumasummat |
| Budjettitehtävät         | Budjettirekisterin tapahtumasummat |
| Päätilit             | Päätilit, joiden mukaan raportit suodatetaan |
| Kirjanpidon kalenterit          | Kirjanpidon kalenterit, joiden mukaan raportit suodatetaan |
| Kirjanpidot                   | Kirjanpidot, joilla raporit suodatetaan nykyiseen kirjanpitoon |
| Budjettikoodit              | Budjettikoodit, joiden mukaan raportit suodatetaan |
| Yritykset            | Yritykset, joilla raporit suodatetaan nykyiseen yritykseen |

