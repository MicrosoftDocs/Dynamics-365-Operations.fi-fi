---
title: Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet
description: Tässä ohjeaiheessa käsitellään ominaisuuksia, jotka on poistettu tai joiden poistoa suunnitellaan Dynamics 365 Supply Chain Managementsta.
author: kamaybac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 785f9055c44110d88b9494b5066647511840b646
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909644"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Poistetut tai vanhentuneet Dynamics 365 Supply Chain Management -ominaisuudet

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe päivitetään, koska Dynamics 365 Supply Chain Managementissa on uusia poistettuja tai vanhentuneita toimintoja.

- *Poistettu* ominaisuus ei ole enää käytettävissä tuotteessa.
- *Vanhentunutta* ominaisuutta ei enää kehitetä aktiivisesti ja se voidaan poistaa tulevassa päivityksessä.

Tämän luettelon avulla voit ottaa huomioon nämä poistuneet ja vanhentuneet ominaisuudet omassa suunnittelussasi.

> [!NOTE]
> Seuraavissa raporteissa on tarkempia tietoja Finance and Operations -sovellusten objekteista: [Teknisten tietojen raportit](/dynamics/s-e/). Voit verrata raporttien eri versioita saadaksesi lisätietoja objekteista, jotka on muutettu tai poistettu kussakin Finance and Operations -sovelluksissa.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Managementin version 10.0.18 poistetut tai vanhentuneet ominaisuudet

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations – varastointi (varastosovellus)

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Alkaen huhtikuusta 2021 *Dynamics 365 for Finance and Operations – varastointi* (varastosovellus) on vanhentunut, eikä sitä tueta huhtikuun 2022 jälkeen. Sen korvaa nyt *varastonhallinnan mobiilisovellus*, joka on julkaistu Supply Chain Managementin version 10.0.17 mukana. Uusi sovellus on täydellinen korvaava tuote, mutta käyttää samaa pohjana olevaa kehystä, mikä helpottaa siirtymistä sen käyttöön. Tarvittaessa näitä kahta sovellusta voidaan käyttää vierekkäin, jotta käyttäjät voivat asteittain opetella käyttämään uutta sovellusta.<br><br>Lisätietoja uudesta varastonhallinnan mobiilisovelluksesta on kohdissa [Varastonhallinnan mobiilisovellus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ja [Varastonhallinnan mobiilisovelluksen asentaminen ja yhdistäminen](../warehousing/install-configure-warehouse-management-app.md). |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, korvataan uudella varastonhallinnan mobiilisovelluksella. |
| **Tuotealueet, joihin vaikutetaan**         | Supply Chain Management – varastosovellus |
| **Käytön asetukset**              | Pilsi ja paikallinen käyttöönotto |
| **Tila**                         | Vanhentunut. Varastosovellus saa tukea virheiden ja tieoturvan korjauksiin, mutta sille ei enää ole käytettävissä toimintojen parannuksia. Huhtikuun 2022 jälkeen vanhaa varastosovellusta ei enää tueta ja asiakkaita pyydetään siirtymään uuteen varastonhallinnan mobiilisovellukseen. Vanha varastosovellus poistetaan sitten Microsoft Storesta ja Google Play -kaupasta.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Managementin version 10.0.15 poistetut tai vanhentuneet ominaisuudet

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11:n Dynamics 365 -tuki on vanhentunut

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Joulukuusta 2020 alkaen kaikkien Dynamics 365 -tuotteiden Microsoft Internet Explorer 11 -tuki vanhenee eikä Internet Explorer 11:tä tueta elokuun 2021 jälkeen.<br><br>Tämä vaikuttaa sellaisiin Dynamics 365 -tuotteita käyttäviin asiakkaisiin, jotka on suunniteltu käytettäviksi Internet Explorer 11 -liittymässä. Elokuun 2021 jälkeen Internet Explorer 11:tä ei tueta kyseisissä Dynamics 365 -tuotteissa. |
| **Onko toinen ominaisuus korvannut?**   | Asiakkaiden kannattaa siirtyä Microsoft Edgeen.|
| **Tuotealueet, joihin vaikutetaan**         | Kaikki Dynamics 365 -tuotteet |
| **Käytön asetukset**              | Kaikki|
| **Tila**                         | Vanhentunut. Internet Explorer 11:tä ei tueta elokuun 2021 jälkeen.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Supply Chain Managementin sisäisen pääsuunnittelumoduulin käyttö valmistusskenaarioissa

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Jotta suorituskyky paranisi ja SQL-tietokannan kuormitus pienenisi pääsuunnittelun aikana, sisäinen Supply Chain Managementin pääsuunnittelumoduuli korvataan suunnittelun optimoinnilla. Suunnittelun optimointi mahdollistaa nopeat suunnitteluajot, jotka voidaan suorittaa myös toimiston aukioloaikoina. Tämän ansiosta suunnittelijat voivat reagoida välittömästi kysynnän muutoksiin tai suunnitteluparametreihin. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen pääsuunnittelumoduulin. |
| **Tuotealueet, joihin vaikutetaan**         | Supply Chain Management – Pääsuunnittelu |
| **Käytön asetukset**              | Vain pilvipalvelussa. Suunnittelun optimointia ei tueta paikallisilla käyttöönotoilla. |
| **Tila**                         | Vanhentunut. 1. huhtikuun 2022 jälkeen valmistusskenaarioita ei enää tueta Dynamics 365 Supply Chain Managementin sisäisellä pääsuunnittelumoduulilla. Asiakkaiden on käytettävä valmistusskenaarioissa suunnittelun optimointia pääsuunnittelun laskelmissa. Lisätietoja on kohdassa [Suunnittelun optimoinnin dokumentointi](../master-planning/planning-optimization/planning-optimization-overview.md). Asiakkaat, joilla on käytössä paikalliset Dynamics 365 Supply Chain Management -käyttöönotot, voivat edelleen käyttää Supply Chain Managementin pääsuunnittelumoduulia valmistusskenaarioissa huhtikuun 2022 jälkeen. Muita ominaisuuksien parannuksia ei kuitenkaan ole käytettävissä. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Managementin version 10.0.11 poistetut tai vanhentuneet ominaisuudet

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Supply Chain Managementin sisäisen pääsuunnittelumoduulin käyttö jakeluskenaarioissa

|   |  |
|------------|--------------------|
| **Poiston tai vanhentumisen syy** | Jotta suorituskyky paranisi ja SQL-tietokannan kuormitus pienenisi pääsuunnittelun aikana, sisäinen Supply Chain Managementin pääsuunnittelumoduuli korvataan suunnittelun optimoinnilla. Suunnittelun optimointi mahdollistaa nopeat suunnitteluajot, jotka voidaan suorittaa myös toimiston aukioloaikoina. Tämän ansiosta suunnittelijat voivat reagoida välittömästi kysynnän muutoksiin tai suunnitteluparametreihin. |
| **Onko toinen ominaisuus korvannut?**   | Kyllä, suunnittelun optimointi tulee jossain vaiheessa korvaamaan nykyisen Supply Chain Managementin sisäisen pääsuunnittelumoduulin. |
| **Tuotealueet, joihin vaikutetaan**         | Supply Chain Management – Pääsuunnittelu |
| **Käytön asetukset**              | Vain pilvipalvelussa. Suunnittelun optimointia ei tueta paikallisilla käyttöönotoilla. |
| **Tila**                         | Vanhentunut. 1. huhtikuun 2021 jälkeen valmistusskenaarioita ei enää tueta Dynamics 365 Supply Chain Managementin sisäisellä pääsuunnittelumoduulilla. Jakeluskenaarioiden osalta asiakkaiden on käytettävä suunnittelun optimointia pääsuunnittelun laskennoissa. Lisätietoja on kohdassa [Suunnittelun optimoinnin dokumentointi](../master-planning/planning-optimization/planning-optimization-overview.md). Asiakkaat, joilla on käytössä paikalliset Dynamics 365 Supply Chain Management -käyttöönotot, voivat edelleen käyttää toimitusketjun hallinnan pääsuunnittelumoduulia jakeluskenaarioissa huhtikuun 2021 jälkeen. Muita ominaisuuksien parannuksia ei kuitenkaan ole käytettävissä. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Poistettujen tai vanhentuneiden toimintojen aiemmat ilmoitukset

Lisätietoja poistetuista tai vanhentuneista toiminnoista aiemmissa versioissa on kohdassa [Poistetut tai vanhentuneet toiminnot edellisissä versioissa](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]