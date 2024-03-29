---
title: Työntekijän osaamisalueiden ja kehittämisen Power BI -sisältö
description: Tässä artikkelissa käsitellään työntekijän osaamisalueiden ja kehityksen Power BI -sisältöä
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.openlocfilehash: 1ddc117c83e551374bc8da6872429e3bb9eeee58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280955"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Työntekijän osaamisalueiden ja kehittämisen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käsitellään työntekijän osaamisalueiden ja kehityksen Power BI -sisältöä 

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja on kohdassa [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                            | Sisältö                                               |
|-----------------------------------|--------------------------------------------------------|
| Osaamistiedot ja kehitys – analyysi | Ryhmän jäsenen osaamisaluetyypit ja ryhmän jäsenen taidot tyypin mukaan |
| Osaamisalueprofiili                     | Valitun työntekijän osaamisprofiili.                |
| Osaamisanalyysi                    | Osaamisalue tyypin ja luokituksen mukaan                              |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Sovelluksen tietoja käytetään työntekijän osaamisalueiden ja kehittymisen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteet muihin yksiköihin |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | Kalenterin siirtymät raporttien osittamiseen                                                                          | |
| Workforce\_Company                | Yritykset, joiden mukaan raportit suodatetaan                                                                             | |
| Workforce\_Compensation           | Maksut ja niiden tiheys ajan myötä                                                                           | |
| Workforce\_CurrentCompensation    | Maksut ja niiden tiheys nykyiseen päivämäärään                                                              | Workforce\_Company, Workforce\_CurrentCompensation, Workforce\_Demographics, Workforce\_Job, Workforce\_Position |
| Workforce\_CurrentPosition        | Paikat nykyiseen pvm:ään asti, täysiaikaista vastaavat, avoimet paikat ja avoimista täytetyiksi -paikat | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | Työntekijät nykyisellä päivämäärällä, ikä ja henkilöstömäärä                                                         | Workforce\_Company Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_PersonSkill, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Job, Workforce\_Employment, Workforce\_Position |
| Workforce\_Date                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | |
| Workforce\_Demographics           | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty                                                   | |
| Workforce\_Employment             | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                                                                  | |
| Workforce\_GeographicLocation     | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                                                           | |
| Workforce\_Job                    | Tehtävä, tyyppi ja nimike                                                                                  | |
| Workforce\_JobPreferredSkill      | Tärkeys, luokitus, taito ja taidon taso                                                                 | Workforce\_Skill, Workforce\_Job |
| Workforce\_PastPositionAssignment | Työtehtävän syy, aloituspvm, loppupvm ja työ                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | Pisteytys, kuvaus arviointimalli                                                                      | |
| Workforce\_PersonSkill            | Taso, tason päivämäärä ja taito                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | Sertifioitu, taso, tason päivämäärä ja taito                                                                    | Workforce\_WorkerName, Workforce\_Skill |
| Workforce\_Position               | Osasto, FTE, toimi, toimen tyyppi ja nimike                                                        | |
| Workforce\_PositionTrend          | Toimien ajan mukaan, FTE ja työ                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | Etunimi , sukunimi ja koko nimi                                                                       | |
| Workforce\_Skill                  | Taito, osaamisalueen tyyppi ja luokitus                                                                              | |
| Workforce\_TerminatedWorker       | Poistetut työntekijät, poistopvm, nimike, toimi ja työ                                             | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job, Workforce\_Position |
| Workforce\_WorkerName             | Etunimi , sukunimi ja koko nimi                                                                       | |
| Workforce\_WorkerTitle            | Nimike ja virkaikä                                                                                   | |
| Workorce\_WorkerTrend             | Työntekijät ajan kuluessa, henkilöstömäärä, yritys ja toimi                                                        | Workforce\_Company, Workforce\_Compensation, Workforce\_GeographicLocation, Workforce\_Performance, Workforce\_WorkerName, Workforce\_ReportsToWorkerName, Workforce\_CalendarOffset, Workforces\_Date, Workforce\_WorkerTitle, Workforce\_Demographics, Workforce\_Employment, Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
