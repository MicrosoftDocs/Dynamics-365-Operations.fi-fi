---
title: "Taloudellisen suorituskyvyn Power BI -sisältö"
description: "Tässä aiheessa kuvataan, mistä voit ladata Microsoft Dynamics 365 for Operations -järjestelmän taloudellisen suorituskyvyn sisältöpaketin Microsoft Power BI:lle. Siinä kuvataan koontinäytön käyttö sekä sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 227285720e7f28beeb135eea081940578531d458
ms.lasthandoff: 03/31/2017


---

# <a name="financial-performance-power-bi-content"></a>Taloudellisen suorituskyvyn Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan, mistä voit ladata Microsoft Dynamics 365 for Operations -järjestelmän taloudellisen suorituskyvyn sisältöpaketin Microsoft Power BI:lle. Siinä kuvataan koontinäytön käyttö sekä sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
--------------------------

Taloudellisen suorituskyvyn sisältöpaketeista on saatavilla kaksi versiota. Yksi versio on saatavana Microsoft Dynamics Lifecycle Services (LCS) -palvelusta ja toinen on saatavana osoitteesta PowerBI.com.

-   **Versio, joka on ladattavissa LCS:stä:** taloudellisen suorituskyvyn sisältöpaketti, joka on saatavana LCS:stä tukee Microsoft Dynamics 365 for Operations -versiota 1611. Löydät sisältöpaketin LCS:n jaetun omaisuuden kirjastosta. Saat lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Microsoft Dynamics 365 for Operationsin tietoihin, artikkelista [LCS:n Power BI -sisältö Microsoftilta ja kumppaneilta](power-bi-content-microsoft-partners.md).
-   **Versio, joka on saatavissa PowerBI.com-sivustosta:** taloudellisen suorituskyvyn sisältöpaketti, joka on saatavana PowerBI.com-sivustosta tukee Microsoft Dynamics AX -versioita 7.0 ja 7.0.1. Lisätietoja Dynamics 365 for Operations -tietojen liittämisestä ja lataamisesta on artikkelissa [Power BI -sisällön hakeminen PowerBI.com-sivustosta](power-bi-home-page.md).

## <a name="main-account-setup"></a>Päätilin asetukset
Koska organisaatiot haluavat velkojen ja tuottosummien näkyvän raporteissa positiivisina summina, päätilien määritys Dynamics 365 for Operationsissa on tärkeää. Jotta nämä päätilit näkyisivät positiivisina summina, päätilityypiksi on asetettava **Velka** tai **Tuotto**. Käytettäessä näitä tilityyppejä Microsoft Power BI -raportointi kääntää merkit ja näyttää summat positiivisina.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Koontinäyttö ja raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin Dynamics 365 for Operations -tietoihin, taloustietosi näkyvät koontinäytössä ja raporteissa. Jos et ole käyttänyt Power BI:tä aiemmin, lisätietoja löydät artikkelista [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Koontinäyttö sisältää yhteenvetoruutuja tiedoista, jotka perustuvat pohjana oleviin raportteihin. Kukin ruutu sisältää kuluvan vuoden yhteenvetotietoja, jotka koskevat kaikkia organisaation yrityksiä. Tässä on esimerkkejä ruuduista:

-   Maksu
-   Kuluvan vuoden kokonaistuotto
-   Kuluvan vuoden kokonaiskulut
-   Kuluvan vuoden nettotulot
-   Nopea suhdeluku
-   Kuluvan vuoden kokonaiskulut tililuokittain
-   Nykyinen suhde
-   Velka - vastaavat yhteensä
-   Todellinen vs. ennustettu tuotto
-   Kuluvan vuoden laskutettu tuotto
-   Kuluvan vuoden liiketoiminnan kulujen suhde
-   Kuluvan vuoden katetuotto
-   Todelliset vs. budjetoidut kulut – Kaikki yritykset

Kunkin ruudun taustatukena on raportti. Nämä raportit sisältävät kaavioita ja taulukoita, joissa on lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                      | Raportin sisältämät tiedot                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Käteisanalyysi               | Käteisvarat yrityksen mukaan, käteisvarat vuosineljänneksen mukaan, kokonaiskäteisvarat ja käteisvarat tilin mukaan **Huomautus:** **Käteisvarat vuosineljänneksen mukaan** -raportin summat eivät sisällä ensimmäisen vuosineljänneksen alkusaldoja. Se näyttää uusien, kussakin neljänneksessä kirjattujen, tapahtumien kokonaissumman.                                                                                |
| Nykyisen suhteen analyysi      | Nykyinen suhde yrityksittäin, neljännesvuosittain ja saldoittain nykyiselle omaisuudelle sekä nykyisille veloille                                                                                                                                                                                                                              |
| Nopean suhdeluvun analyysi        | Nopea suhde yrityksittäin, neljännesvuosittain ja saldoittain käteiselle, myyntireskontralle sekä nykyisille veloille                                                                                                                                                                                                                      |
| Myytyjen tuotteiden kustannusanalyysi | Yrityksen myytyjen tuotteiden kustannukset (MTKUST) kuluvana ja edellisenä vuonna neljännesvuosittain, MTKUST myynneille yrityksittäin, kokonais-MTKUST ja MTKUST myyntiprosenteittain                                                                                                                                                                                   |
| Käyttöpääoma-analyysi    | Käyttöpääoma yrityksittäin, neljännesvuosittain, nykyinen omaisuus ja velat sekä kokonaiskäyttöpääoma                                                                                                                                                                                                                   |
| Vara- ja velka-analyysi     | Kokonaisvarallisuuden tuotto ja velka yrityksittäin, velka - vastaavat yhteensä ja kokonaiskäyttöomaisuuden tuoton neljännes päivään saakka, varat ja velat                                                                                                                                                                                     |
| Katetuottoanalyysi      | Toteutuneet ja budjetoidut katetuotot yrityksittäin, tuoton merkitseminen neljänneksittäin, katetuottoprosentti ja katetuotto                                                                                                                                                                                                                       |
| Nettotuottoanalyysi         | Toteutunut ja budjetoitu nettotulo yrityksittäin, kuluvan ja edellisen vuoden nettotulo sekä kulujen ja nettotulon suhde                                                                                                                                                                                                                       |
| Ansioanalyysi           | Toteutuneet ja budjetoidut ansiot ennen korkoa ja veroja (EBIT) yrityksittäin, kuluvan ja edellisen vuoden EBIT, kulujen ja tuoton suhde prosentteina sekä toteutunut ja budjetoitu kulujen ja tuoton suhde                                                                                                                                                          |
| Tuottoanalyysi            | Kokonaistuotto, toteutunut ja budjetoitu kokonaistuotto yrityksittäin, kuluvan ja edellisen vuoden kokonaistuotto, tuottobudjetin varianssi yrityksittäin sekä kuluvan ja edellisen kauden kokonaistuotto                                                                                                                                                 |
| Kuluanalyysi            | Kokonaiskulut, toteutuneiden ja budjetoitujen kokonaiskulujen suhde yrityksittäin, toteutuneet ja budjetoidut kokonaiskulut neljännesvuosittain, kokonaiskulut tililuokittain sekä toimintakulujen suhde                                                                                                                                                                 |
| Laskutetun tuoton analyysi     | Kokonaismyyntireskontra, kokonaismyyntireskontra yrityksittäin ja neljännesvuosittain sekä myyntireskontratilien saldot **Huomautus:** Raportit eivät sisällä myyntireskontran kirjanpidon alkusaldoja. Ne näyttävät niiden uusien tapahtumien kokonaissumman, jotka on kirjattu myyntireskontraan. |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Tiedot, joita käytetään taloudellisen suorituskyvyn sisältöpaketin koontinäytön ja raporttien täyttämiseen, ovat peräisin Dynamics 365 for Operations -järjestelmästä. Sisältöpaketin perustana on käytetty seuraavia entiteettejä: **Koostetietoentiteetit**

-   **GeneralLedgerActivities** – tämä yksikkö kokoaa kirjanpidon saldot tililuokittain.
-   **BudgetActivities** – tämä yksikkö kokoaa budjetin saldot tililuokittain.

**Tietoyksiköt**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Kirjanpidot
-   ChartofAccounts

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisältöpaketissa käytettävät tunnusluvut (KPI:t) ja raportit. Oletusarvon mukaan sisältöpaketti tuo edellisten kolmen vuoden sekä yhden tulevan vuoden tiedot. Voit muokata [Microsoft Excel -työkirjaa](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) sisällyttääksesi lisälaskelmia raporteille ja koontinäytölle. Tämä työkirja on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)





