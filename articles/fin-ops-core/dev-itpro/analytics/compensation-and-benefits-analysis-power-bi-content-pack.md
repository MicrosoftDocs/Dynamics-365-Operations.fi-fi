---
title: Kompensaatioiden ja etujen Power BI -sisältö
description: Tässä ohjeaiheessa käsitellään kompensaation ja etujen Power BI -sisältöä.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07a8be0a4c333e9d465341d9384e4b9a706f9e75
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559818"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Kompensaatioiden ja etujen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään kompensaation ja etujen Power BI -sisältöä. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja on kohdassa [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                     | Sisältö                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Kompensaatioiden ja etujen analyysi | Tunti- ja kuukausipalkkaiset työntekijät yrityksen mukaan, keskimääräinen tuntipalkka, keskimääräinen palkka, työntekijät työsuhteen tyypin mukaan ja suunnitelmien voimaanastuminen |
| Työsuhde-edut          | Työntekijän voimaanastuminen valitun edun mukaan                                                                                               |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Sovelluksen tietoja käytetään kompensaatioiden ja etujen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteet muihin yksiköihin |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenterin siirtymät raporttien osittamiseen                                                                          | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workorce\_WorkerTrend, Workforce\_TerminatedWorker |
| Workforce\_Company                | Yritykset, joiden mukaan raportit suodatetaan                                                                             | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Compensation           | Maksut ja niiden tiheys ajan myötä                                                                           | Workforce\_CurrentCompensation, Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_CurrentCompensation    | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Workforce\_Company, Workforce\_Compensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentWorker          | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_Date                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Workforce\_PastPositionAssignment, Workforce\_PositionTrend, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Demographics           | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Employment             | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_GeographicLocation     | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Job                    | Tehtävä, tyyppi ja nimike                                                                                  | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PastPositionAssignment | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Pisteytys, kuvaus arviointimalli                                                                      | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Position               | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | Workforce\_CurrentPosition, Workforce\_CurrentWorker |
| Workforce\_PositionTrend          | Toimien ajan mukaan, FTE ja työ                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Etunimi , sukunimi ja koko nimi                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_Skill                  | Taito, osaamisalueen tyyppi ja luokitus                                                                              | |
| Workforce\_TerminatedWorker       | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position, Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | Voimaantulopvm, etuvaihtoehto, etusuunnitelma ja etutyyppi                                             | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerName             | Etunimi , sukunimi ja koko nimi                                                                       | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTitle            | Nimike ja virkaikä                                                                                   | Workforce\_CurrentWorker, Workforce\_TerminatedWorker, Workforce\_WorkerTrend |
| Workforce\_WorkerTrend            | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]