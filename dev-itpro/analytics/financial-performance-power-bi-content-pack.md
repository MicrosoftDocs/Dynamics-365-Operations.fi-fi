---
title: "Taloudellinen suorituskyky Virranhallinta BI sisältö"
description: "Tässä ohjeaiheessa kuvataan Microsoft Power BI toimintojen taloudellisen suorituskyvyn sisältö Pack Microsoft Dynamics-365. Dashboard ja raportteja, jotka sisältyvät sisältö pack kuvaa ja tietoja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack."
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

# <a name="financial-performance-power-bi-content"></a>Taloudellinen suorituskyky Virranhallinta BI sisältö

Tässä ohjeaiheessa kuvataan Microsoft Power BI toimintojen taloudellisen suorituskyvyn sisältö Pack Microsoft Dynamics-365. Dashboard ja raportteja, jotka sisältyvät sisältö pack kuvaa ja tietoja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack.

<a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
--------------------------

Tuloksellisuuteen sisältöpaketti kaksi versiota ovat saatavilla. Yksi versio on saatavana Microsoft Dynamics Lifecycle Services (LCS)- ja toinen on saatavana PowerBI.com.

-   **Versio on ladattavissa LCS:** tuloksellisuuteen sisältöpaketti on saatavana LCS tukee Microsoft Dynamics-365-version toimintoja 1611. Löydät jaetun omaisuuden LCS-kirjaston sisältö pack. Saat lisätietoja siitä, miten sisältö pack ladata ja liittää sen Microsoft Dynamics-365, toimintojen tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).
-   **Versio on ladattavissa PowerBI.com:** tuloksellisuuteen sisältöpaketti on saatavana PowerBI.com tukee Microsoft Dynamics AX-versiota 7.0 että 7.0.1. Saat lisätietoja siitä, miten yhteyden ja ladata oman Dynamics 365 toimintoja tietojen [PowerBI.com sisällön käyttö Power BI](power-bi-home-page.md).

## <a name="main-account-setup"></a>Päätilin asetukset
Koska organisaatiot veloista ja tuloista summien näkyvän raporteissa positiivisina summina, päätilit-Dynamics 365 työvaiheiden määritys on tärkeää. Nämä päätilit, jotka ovat positiivisia määriä, päätilityypin on asetettava **vastuu** tai **tulojen**. Käytettäessä näitä tilityyppejä kautta Microsoft Power BI-raportoinnin käänteinen oireiden ja summat positiiviseksi.

## <a name="dashboard-and-reports-that-are-included-in-the-content-pack"></a>Dashboard ja raportteja, jotka sisältyvät sisältö pack
Kun olet liittänyt sisältöpaketin Dynamics 365 for Operations -tietoihin, taloustietosi näkyvät koontinäytössä ja raporteissa. Jos et ole koskaan käyttänyt ennen BI virran, saat siitä lisätietoja [Power BI sivulla ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Koontinäyttö sisältää yhteenvetoruutuja tiedoista, jotka perustuvat pohjana oleviin raportteihin. Kukin ruutu sisältää kuluvan vuoden yhteenvetotietoja, jotka koskevat kaikkia organisaation yrityksiä. Seuraavassa on joitakin laatat:

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

Kukin ruutu varmuuskopioidaan tukevat raportin. Nämä raportit sisältävät kaavioita ja taulukoita, joissa on lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                      | Raportin sisältämät tiedot                                                                                                                                                                                                                                                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Käteisanalyysi               | Oikeushenkilö, neljännesvuosittain rahaa, yhteensä rahaa ja rahaa tilillä rahaa **Huomautus:****rahaa neljännesvuosittain** raportti ei sisällä alkusaldot yhteensä ensimmäisen vuosineljänneksen. Siinä esitetään uusia tapahtumia, jotka on kirjattu kunkin vuosineljänneksen kokonaissumman.                                                                                |
| Nykyisen suhteen analyysi      | Nykyinen suhde yrityksittäin, neljännesvuosittain ja saldoittain nykyiselle omaisuudelle sekä nykyisille veloille                                                                                                                                                                                                                              |
| Nopean suhdeluvun analyysi        | Nopea suhdeluku mukaan oikeushenkilö, neljännesvuosittain ja saldot rahaa, nopea suhdeluku tilien myyntireskontran ja nykyiset velat                                                                                                                                                                                                                      |
| Myytyjen tuotteiden kustannusanalyysi | Yrityksen myytyjen tuotteiden kustannukset (MTKUST) kuluvana ja edellisenä vuonna neljännesvuosittain, MTKUST myynneille yrityksittäin, kokonais-MTKUST ja MTKUST myyntiprosenteittain                                                                                                                                                                                   |
| Käyttöpääoma-analyysi    | Käyttöpääoma yrityksittäin, neljännesvuosittain, nykyinen omaisuus ja velat sekä kokonaiskäyttöpääoma                                                                                                                                                                                                                   |
| Vara- ja velka-analyysi     | Kokonaisvarallisuuden tuotto ja velka yrityksittäin, velka - vastaavat yhteensä ja kokonaiskäyttöomaisuuden tuoton neljännes päivään saakka, varat ja velat                                                                                                                                                                                     |
| Katetuottoanalyysi      | Toteutuneet ja budjetoidut katetuotot yrityksittäin, tuoton merkitseminen neljänneksittäin, katetuottoprosentti ja katetuotto                                                                                                                                                                                                                       |
| Nettotuottoanalyysi         | Toteutunut ja budjetoitu nettotulo yrityksittäin, kuluvan ja edellisen vuoden nettotulo sekä kulujen ja nettotulon suhde                                                                                                                                                                                                                       |
| Ansioanalyysi           | Toteutuneet ja budjetoidut ansiot ennen korkoa ja veroja (EBIT) yrityksittäin, kuluvan ja edellisen vuoden EBIT, kulujen ja tuoton suhde prosentteina sekä toteutunut ja budjetoitu kulujen ja tuoton suhde                                                                                                                                                          |
| Tuottoanalyysi            | Kokonaistuotto, toteutunut ja budjetoitu kokonaistuotto yrityksittäin, kuluvan ja edellisen vuoden kokonaistuotto, tuottobudjetin varianssi yrityksittäin sekä kuluvan ja edellisen kauden kokonaistuotto                                                                                                                                                 |
| Kuluanalyysi            | Kokonaiskulut, toteutuneiden ja budjetoitujen kokonaiskulujen suhde yrityksittäin, toteutuneet ja budjetoidut kokonaiskulut neljännesvuosittain, kokonaiskulut tililuokittain sekä toimintakulujen suhde                                                                                                                                                                 |
| Laskutetun tuoton analyysi     | Myyntireskontra yhteensä, mukaan oikeushenkilön Myyntireskontra yhteensä, yhteensä myyntireskontran neljännesvuosittain, ja tilit saamiset-tilien saldojen **Huomautus:** raportit eivät sisällä tilit myyntireskontran kirjanpitotilien alkusaldot. Ne näyttävät uusia tapahtumia, jotka on kirjattu tileihin Myyntireskontran summa. |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Joka täyttää dashboard ja taloudellisen suorituskyvyn sisältöpaketti raporttien tiedot Dynamics 365 toimintojen tiedot. Sisältö pack perustana käytettiin seuraavia kohteita: **keräämään tietoja yksiköt**

-   **GeneralLedgerActivities** – tämän entiteetin kokoaa Kirjanpidon saldot ensimmäisen luokan mukaan.
-   **BudgetActivities** – tämän entiteetin kokoaa budjettisaldot ensimmäisen luokan mukaan.

**Data entities**

-   FiscalCalendars
-   MainAccounts
-   LegalEntities
-   Kirjanpidot
-   ChartofAccounts

Luo lasketut mitat tietomallin käytettiin entiteetit. Lasketut mitat käytetään laskettaessa Suorituskyvyn mittareiden (KPI: T) ja raportit, joita käytetään sisällön pack. Oletusarvon mukaan sisältöpaketti tuo edellisten kolmen vuoden sekä yhden tulevan vuoden tiedot. Voit muokata [Microsoft Excel -työkirjaa](https://mbs.microsoft.com/customersource/global/AX/downloads/reports/msdaxfinpercontentpowerbi) sisällyttääksesi lisälaskelmia raporteille ja koontinäytölle. Tämä työkirja on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](..\data-entities\data-entities.md)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](configure-power-bi-integration.md)



