---
title: Taloudellisen suorituskyvyn PowerBI.com-ratkaisu
description: "Tässä ohjeaiheessa käsitellään taloudellisen suorituskyvyn PowerBI.com-ratkaisua."
author: kweekley
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: b70d470da2160670848d2dca9c97f6d7a2d6cf60
ms.contentlocale: fi-fi
ms.lasthandoff: 08/08/2018

---

# <a name="financial-performance-powerbicom-solution"></a>Taloudellisen suorituskyvyn PowerBI.com-ratkaisu

[!include [banner](../includes/banner.md)]

> [!Note]
> Tämä PowerBI.com-ratkaisu on vanhentunut, kuten on ilmoitettu [AppSourcessa julkaistuissa Power BI -sisältöpaketeissa](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

Tässä ohjeaiheessa käsitellään **taloudellisen suorituskyvyn** PowerBI.com-ratkaisua. Siinä kerrotaan sisältyvistä koontinäytöistä ja raporteista sekä ratkaisun muodostamisessa käytetyistä tietomallista ja yksiköistä.

## <a name="main-account-setup"></a>Päätilin asetukset
Koska organisaatiot haluavat velkojen ja tuottosummien näkyvän raporteissa positiivisina summina, päätilien määritys on tärkeää. Jotta nämä päätilit näkyisivät positiivisina summina, päätilityypiksi on asetettava **Velka** tai **Tuotto**. Käytettäessä näitä tilityyppejä Power BI -raportointi kääntää merkit ja näyttää summat positiivisina.

## <a name="dashboard-and-reports-that-are-included-in-the-powerbicom-solution"></a>PowerBI.com-ratkaisuun sisältyvä koontinäyttö ja raportit
Koontinäyttö sisältää yhteenvetoruutuja tiedoista, jotka perustuvat pohjana oleviin raportteihin. Kukin ruutu sisältää kuluvan vuoden yhteenvetotietoja, jotka koskevat kaikkia organisaation yrityksiä. Tässä on esimerkkejä ruuduista:

- Maksu
- Kuluvan vuoden kokonaistuotto
- Kuluvan vuoden kokonaiskulut
- Kuluvan vuoden nettotulot
- Nopea suhdeluku
- Kuluvan vuoden kokonaiskulut tililuokittain
- Nykyinen suhde
- Velka - vastaavat yhteensä
- Todellinen vs. ennustettu tuotto
- Kuluvan vuoden laskutettu tuotto
- Kuluvan vuoden liiketoiminnan kulujen suhde
- Kuluvan vuoden katetuotto
- Todelliset vs. budjetoidut kulut – Kaikki yritykset

Kunkin ruudun taustatukena on raportti. Nämä raportit sisältävät kaavioita ja taulukoita, joissa on lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                      | Raportin sisältämät tiedot |
|-----------------------------|--------------------------------------|
| Käteisanalyysi               | Käteinen yrityksittäin, käteinen neljännesvuosittain ja käteinen tileittäin<br><br>**Huomautus:** Käteisvarojen neljännesvuosittaistiedoissa alkusaldot eivät sisälly ensimmäisen vuosineljänneksen kokonaissummaan. Se näyttää uusien, kussakin neljänneksessä kirjattujen, tapahtumien kokonaissumman.|
| Nykyisen suhteen analyysi      | Nykyinen suhde yrityksittäin, neljännesvuosittain ja saldoittain nykyiselle omaisuudelle sekä nykyisille veloille |
| Nopean suhdeluvun analyysi        | Nopea suhde yrityksittäin, neljännesvuosittain ja saldoittain käteiselle, myyntireskontralle sekä nykyisille veloille |
| Myytyjen tuotteiden kustannusanalyysi | Yrityksen myytyjen tuotteiden kustannukset (MTKUST) kuluvana ja edellisenä vuonna neljännesvuosittain, MTKUST myynneille yrityksittäin, kokonais-MTKUST ja MTKUST myyntiprosenteittain |
| Käyttöpääoma-analyysi    | Käyttöpääoma yrityksittäin, neljännesvuosittain, nykyinen omaisuus ja velat sekä kokonaiskäyttöpääoma |
| Vara- ja velka-analyysi     | Kokonaisvarallisuuden tuotto ja velka yrityksittäin, velka - vastaavat yhteensä ja kokonaiskäyttöomaisuuden tuoton neljännes päivään saakka, varat ja velat |
| Katetuottoanalyysi      | Toteutuneet ja budjetoidut katetuotot yrityksittäin, tuoton merkitseminen neljänneksittäin, katetuottoprosentti ja katetuotto |
| Nettotuottoanalyysi         | Toteutunut ja budjetoitu nettotulo yrityksittäin, kuluvan ja edellisen vuoden nettotulo sekä kulujen ja nettotulon suhde |
| Ansioanalyysi           | Toteutuneet ja budjetoidut ansiot ennen korkoa ja veroja (EBIT) yrityksittäin, kuluvan ja edellisen vuoden EBIT, kulujen ja tuoton suhde prosentteina sekä toteutunut ja budjetoitu kulujen ja tuoton suhde |
| Tuottoanalyysi            | Kokonaistuotto, toteutunut ja budjetoitu kokonaistuotto yrityksittäin, kuluvan ja edellisen vuoden kokonaistuotto, tuottobudjetin varianssi yrityksittäin sekä kuluvan ja edellisen kauden kokonaistuotto |
| Kuluanalyysi            | Kokonaiskulut, toteutuneiden ja budjetoitujen kokonaiskulujen suhde yrityksittäin, toteutuneet ja budjetoidut kokonaiskulut neljännesvuosittain, kokonaiskulut tililuokittain sekä toimintakulujen suhde |
| Laskutetun tuoton analyysi     | Kokonaismyyntireskontra, kokonaismyyntireskontra yrityksittäin ja neljännesvuosittain sekä myyntireskontratilien saldot<br><br>**Huomautus:** Tiedot eivät sisällä myyntireskontratilien alkusaldoja. Se näyttää niiden uusien tapahtumien kokonaissumman, jotka on kirjattu myyntireskontraan. |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
**Taloudellisen suorituskyvyn** PowerBI.com-ratkaisun perustana käytettiin seuraavia yksikköjä:

**Koostetietoyksiköt**

- **GeneralLedgerActivities** – tämä yksikkö kokoaa kirjanpidon saldot tililuokittain.
- **BudgetActivities** – tämä yksikkö kokoaa budjetin saldot tililuokittain.

**Tietoyksiköt**

- FiscalCalendars
- MainAccounts
- LegalEntities
- Kirjanpidot
- ChartofAccounts

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisällössä käytettävät tunnusluvut (KPI:t) ja raportit. Oletusarvoisesti sisältö noutaa kolmen viimeisen vuoden ja yhden tulevan vuoden tiedot. Voit muokata [Microsoft Excel -työkirjaa](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) sisällyttääksesi lisälaskelmia raporteille ja koontinäytölle. Tämä työkirja on sisällön luomisessa käytetty oletustietomalli. 

