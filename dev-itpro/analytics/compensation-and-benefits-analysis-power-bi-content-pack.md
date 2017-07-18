---
title: "Kompensaatioiden ja etujen Power BI -sisältö"
description: "Tässä aiheessa kuvataan Finance and Operationsin kompensaatioiden ja etujen Power BI sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 70e35a33e06fe7c89dd64d17703f19a71d4a157e
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Kompensaatioiden ja etujen Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan Finance and Operationsin kompensaatioiden ja etujen Power BI sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
--------------------------

Löydät kompensaatioiden ja etujen sisältöpaketin Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Saat lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Microsoft Dynamics 365 for Finance and Operationsin tietoihin, artikkelista [Microsoftin ja kumppaneiden Power BI -sisältö LCS-sovelluksessa](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin Dynamics 365 for Finance and Operations -tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja löydät artikkelista [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                     | Sisältö                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Kompensaatioiden ja etujen analyysi | Tunti- ja kuukausipalkkaiset työntekijät yrityksen mukaan, keskimääräinen tuntipalkka, keskimääräinen palkka, työntekijät työsuhteen tyypin mukaan ja suunnitelmien voimaanastuminen |
| Työsuhde-edut          | Työntekijän voimaanastuminen valitun edun mukaan                                                                                               |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Finance and Operationsin tietoja käytetään kompensaatioiden ja etujen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteet muihin yksiköihin                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | Kalenterin siirtymät raporttien osittamiseen                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | Yritykset, joiden mukaan raportit suodatetaan                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | Maksut ja niiden tiheys ajan myötä                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Workforce\_Date                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | Tehtävä, tyyppi ja nimike                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PastPositionAssignment | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | Pisteytys, kuvaus arviointimalli                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Position               | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | Toimien ajan mukaan, FTE ja työ                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | Etunimi , sukunimi ja koko nimi                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | Taito, osaamisalueen tyyppi ja luokitus                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_TerminatedWorker       | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Voimaantulopvm, etuvaihtoehto, etusuunnitelma ja etutyyppi                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | Etunimi , sukunimi ja koko nimi                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerTitle            | Nimike ja virkaikä                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisältöpaketissa käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata CompensationandBenefits.pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





