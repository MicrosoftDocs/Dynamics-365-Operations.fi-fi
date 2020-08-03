---
title: Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Supply Chain Managementsta.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597113"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe päivitetään, koska Dynamics 365 Supply Chain Managementissa on uusia poistettuja tai vanhentuneita toimintoja.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Managementin version 10.0.11 poistetut tai vanhentuneet ominaisuudet

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Supply Chain Managementin sisäisen pääsuunnittelumoduulin käyttö jakeluskenaarioissa

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Jotta suorituskyky paranisi ja SQL-tietokannan kuormitus pienenisi pääsuunnittelun aikana, sisäinen Supply Chain Managementin pääsuunnittelumoduuli korvataan suunnittelun optimoinnilla. Suunnittelun optimointi mahdollistaa nopeat suunnitteluajot, jotka voidaan suorittaa myös toimiston aukioloaikoina. Tämän ansiosta suunnittelijat voivat reagoida välittömästi kysynnän muutoksiin tai suunnitteluparametreihin. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen pääsuunnittelumoduulin. |
| **Tuotealueet, joihin vaikutetaan**         | Supply Chain Management – Pääsuunnittelu |
| **Käytön asetukset**              | Vain pilvipalvelussa. Suunnittelun optimointia ei tueta paikallisilla käyttöönotoilla. |
| **Tila**                         | Vanhentunut. Huhtikuussa 2021 jakelu skenaarioita ei enää tueta Dynamics 365 Supply Chain Managementin sisäisellä pääsuunnittelumoduulilla. Jakeluskenaarioiden osalta asiakkaiden on käytettävä suunnittelun optimointia pääsuunnittelun laskennoissa. Lisätietoja on kohdassa [Suunnittelun optimoinnin dokumentointi](https://go.microsoft.com/fwlink/?linkid=2105830). Asiakkaat, joilla on käytössä paikalliset Dynamics 365 Supply Chain Management -käyttöönotot, voivat edelleen käyttää toimitusketjun hallinnan pääsuunnittelumoduulia jakeluskenaarioissa huhtikuun 2021 jälkeen. Muita ominaisuuksien parannuksia ei kuitenkaan ole käytettävissä. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset

Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
