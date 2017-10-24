---
title: "Työntekijän osaamisen ja kehittymisen Power BI -sisältö"
description: "Tässä ohjeaiheessa käsitellään Finance and Operationsin työntekijän osaamisalueiden ja kehittymisen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7ec68b859fe419ab31ddd2f8a7332ae8acee1e40
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---

# <a name="employee-competencies-and-development-power-bi-content"></a>Työntekijän osaamisen ja kehittymisen Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä ohjeaiheessa käsitellään Finance and Operationsin työntekijän osaamisalueiden ja kehittymisen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
--------------------------

Löydät työntekijän osaamisen ja kehittymisen sisältöpaketin Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Saat lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Microsoft Dynamics 365 for Finance and Operationsin tietoihin, artikkelista [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin Dynamics 365 for Finance and Operations -tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja löydät artikkelista [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                            | Sisältö                                               |
|-----------------------------------|--------------------------------------------------------|
| Osaamistiedot ja kehitys – analyysi | Ryhmän jäsenen osaamisaluetyypit ja ryhmän jäsenen taidot tyypin mukaan |
| Osaamisalueprofiili                     | Valitun työntekijän osaamisprofiili.                |
| Osaamisanalyysi                    | Osaamisalue tyypin ja luokituksen mukaan                              |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Finance and Operationsin tietoja käytetään työntekijän osaamisalueiden ja kehittymisen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteet muihin yksiköihin                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenterin siirtymät raporttien osittamiseen                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | Yritykset, joiden mukaan raportit suodatetaan                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | Maksut ja niiden tiheys ajan myötä                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | Tehtävä, tyyppi ja nimike                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | Tärkeys, luokitus, taito ja taidon taso                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | Pisteytys, kuvaus arviointimalli                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | Taso, tason päivämäärä ja taito                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | Sertifioitu, taso, tason päivämäärä ja taito                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | Toimien ajan mukaan, FTE ja työ                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | Etunimi , sukunimi ja koko nimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | Taito, osaamisalueen tyyppi ja luokitus                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | Etunimi , sukunimi ja koko nimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | Nimike ja virkaikä                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisältöpaketissa käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata CompetenciesandDevelopment.pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





