---
title: Todellinen vs. budjetti – Power BI -sisältö
description: Tässä artikkelissa käsitellään todellisen ja budjetin Power BI -sisältöä Siinä käsitellään raporttien käyttöä ja tietomallia koskevia tietoja.
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ff57d052b66103ad716ad8d55afb4fcb095d2c02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847279"
---
# <a name="actual-vs-budget-power-bi-content"></a>Todellinen vs. budjetti – Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään **todellisen ja budjetin** Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="overview"></a>Yleiskuvaus

**Todellinen vs. budjetti** – Power BI -sisältö luotiin henkilöille, jotka vastaavat organisaatiossa todellisen ja budjetoidun suorituksen vertailun seurannasta. **Todellinen vs. budjetti** – Power BI -sisältö tuo näkyvyyttä budjetin variansseihin. Voit analysoida kuluvan vuoden budjettia tililuokan, budjettikoodin, päätilin, päätilin kuvauksen tai tilikauden mukaan. Saat tällä tavoin paremman käsityksen varianssien syystä.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen
**Todellinen vs. budjetti** – Power BI -sisällön raportit näkyvät **Kirjanpitobudjetit ja ennusteet**- ja **Talousjohtaja**-työtiloissa.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Raportit, jotka sisältyvät Power BI -sisältöön
Seuraavassa taulukossa on tietoja mittareista, jotka löytyvät **Todellinen vs. budjetti** – Power BI -sisällön kultakin raporttisivulta.

| Raportti                      | Mittarit                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Kulut – todellinen vs. budjetti | <ul><li>Kuluvan vuoden kokonaiskulut</li><li>Kuluvan vuoden budjetoidut kokonaiskulut</li></ul>  |
| Tuotto – todellinen vs. budjetti  | <ul><li>Kuluvan vuoden kokonaistuotto</li><li>Kuluvan vuoden budjetoitu kokonaistuotto</li><ul>     |
| Kulu                     | <ul><li>Kuluvan vuoden kokonaiskulut</li><li>Budjettiin perustuva kulutavoite</li><ul> |
| Myyntituotto                     | <ul><li>Kuluvan vuoden kokonaistuotto</li><li>Budjettiin perustuva tuottotavoite</li><ul>   |
| Nettotuotto                  | <ul><li>Kuluvan vuoden nettotulot</li><li>Budjettiin perustuva nettotulotavoite</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot

| Kokonaisuus                    | Sisältö                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Kirjanpitotehtävät | Kirjanpidon tapahtumasummat                                       |
| Budjettitehtävät         | Budjettirekisterin tapahtumasummat                                      |
| Päätilit             | Päätilit, joiden mukaan raportit suodatetaan                                               |
| Kirjanpidon kalenterit          | Kirjanpidon kalenterit, joiden mukaan raportit suodatetaan                                            |
| Kirjanpidot                   | Kirjanpidot, joilla raporit suodatetaan nykyiseen kirjanpitoon              |
| Budjettikoodit              | Budjettikoodit, joiden mukaan raportit suodatetaan                                                |
| Yritykset            | Yritykset, joilla raporit suodatetaan nykyiseen yritykseen |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]