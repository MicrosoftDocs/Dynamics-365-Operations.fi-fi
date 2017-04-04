---
title: "Työntekijän osaamista ja kehitystä Power BI-sisältö"
description: "Tässä aiheessa kuvataan työvaiheet - työntekijän osaamista ja sisältö virtaa BI Development for Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Työntekijän osaamista ja kehitystä Power BI-sisältö

Tässä aiheessa kuvataan työvaiheet - työntekijän osaamista ja sisältö virtaa BI Development for Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja.

<a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
--------------------------

Löydät työntekijän osaamista ja kehitystä sisältö pack jaettujen varojen kirjaston Microsoft Dynamics Lifecycle Services (LCS). Saat lisätietoja siitä, miten sisältö pack ladata ja liittää sen Microsoft Dynamics-365, toimintojen tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältö pack
Sen jälkeen, kun olet muodostanut yhteyden oman Dynamics 365 toimintoja tietojen sisältö pack, raportit näkyvät organisaation tiedot. Jos et ole koskaan käyttänyt Microsoft Power BI ennen, saat siitä lisätietoja [sivulla ohjattu oppiminen Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raportit, jotka sisältyvät sisältö pack on sekä kaavioita ja taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                            | Sisältö                                               |
|-----------------------------------|--------------------------------------------------------|
| Osaaminen & kehittäminen analyysi | Ryhmän jäsenen osaamisaluetyypit ja ryhmän jäsenten taitoja tyypin mukaan |
| Osaamisalueprofiili                     | Valitun työntekijän osaamisalueprofiilista                |
| Osaamisanalyysi                    | Osaamisalueiden tyyppi ja luokitus                              |

Voit suodattaa kaavioita ja laatat raporteissa ja kiinnitä kaavioita ja laatat Dashboardiin. Saat lisätietoja siitä, miten suodatin ja Power BI-pin [Luo ja määritä A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Raportit työntekijän osaamista ja kehitystä sisältöpaketti täyttämiseen käytetään työvaiheiden tietoja Dynamics 365. Seuraavassa taulukossa on esitetty kohteiden sisältö pack on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteisiin                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työvoiman\_CalendarOffset         | Kalenterin siirtymät sektorin raportit                                                                          |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_yrityksen                | Yritykset voivat suodattaa raporttien mukaan                                                                             |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_korvaus           | Taksa ja kuinka usein ajan myötä                                                                           |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_CurrentCompensation    | Taksa ja taajuus nykyisestä päivämäärästä                                                              | Työvoiman\_yrityksen työvoiman\_CurrentCompensation työvoiman\_demografia työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                            |
| Työvoiman\_CurrentPosition        | Nykyisestä päivämäärästä (FTE) kokopäiväisten toimien Avaa toimet ja avaa ja-täytetty toimet | Työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                                                                      |
| Työvoiman\_CurrentWorker          | Työntekijöiden nykyistä päivämäärää, ikä ja Henkilöstömäärä                                                         | Työvoiman\_yrityksen työvoiman\_korvausta työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_työvoiman PersonSkill\_WorkerName työvoiman\_työvoiman ReportsToWorkerName\_WorkerTitle työvoiman\_demografia työvoiman\_projektin työvoiman\_työllisyys työvoiman\_sijainti                     |
| Työvoiman\_päivämäärä                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_demografia           | Syntymäajan, sukupuolen, etnisen alkuperän ja siviilisääty                                                   |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_työskentely             | Alkamispäivämäärä, päättymispäivämäärä ja tapahtumapäivämäärä                                                                  |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_GeographicLocation     | Paikkakunnan, läänin, postal code ja osavaltio tai provinssi                                                           |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_työ                    | Funktion tyyppi ja otsikko                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_JobPreferredSkill      | Tärkeys, luokitus, taidon ja taidon taso                                                                 | Työvoiman\_työvoiman taitojen\_työ                                                                                                                                                                                                                                                                         |
| Työvoiman\_PastPositionAssignment | Syy tehtävän, alkamispäivämäärä, päättymispäivämäärä ja työn                                                           | Työvoiman\_ClaendarOffset työvoiman\_päivä työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                            |
| Työvoiman\_suorituskyvyn            | Luokitus ja arviointimallin kuvaus                                                                      |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_PersonSkill            | Tason ja taitojen tason päivämäärän                                                                               | Työvoiman\_taito                                                                                                                                                                                                                                                                                        |
| Työvoiman\_PersonSkillAnalysis    | Todistus, taso, taso päivämäärä ja taito                                                                    | Työvoiman\_WorkerName työvoiman\_taito                                                                                                                                                                                                                                                                  |
| Työvoiman\_sijainti               | Osasto, FTE, sijainti, toimen ja otsikko                                                        |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_PositionTrend          | Toimien aika, FTE ja työn kautta                                                                          | Työvoiman\_CalendarOffset työvoiman\_päivä työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                            |
| Työvoiman\_ReportsToWorkerName    | Etunimi, Sukunimi ja koko nimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_taito                  | Taito, osaamisalueen ja luokitus                                                                              |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_TerminatedWorker       | Työntekijöiden työsuhteen loppumispäivämäärä, otsikko, sijainti ja työ päättyi                                             | Työvoiman\_yrityksen työvoiman\_korvausta työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_työvoiman WorkerName\_ReportsToWorkerName työvoiman\_CalendarOffset Workforces\_päivä työvoiman\_WorkerTitle työvoiman\_demografia työvoiman\_työllisyys työvoiman\_projektin työvoiman\_sijainti |
| Työvoiman\_WorkerName             | Etunimi, Sukunimi ja koko nimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Työvoiman\_WorkerTitle            | Otsikko ja Virkaikä                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Työntekijöiden aika, Henkilöstömäärä, yrityksen ja paikan päälle                                                        | Työvoiman\_yrityksen työvoiman\_korvaus työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_työvoiman WorkerName\_ReportsToWorkerName työvoiman\_CalendarOffset Workforces\_päivä työvoiman\_WorkerTitle työvoiman\_demografia työvoiman\_työllisyys työvoiman\_työn                     |

Luo lasketut mitat tietomallin käytettiin entiteetit. Nämä lasketaan toimenpiteet sitten laskemisessa käytetään Suorituskyvyn mittareiden (KPI: T) ja raportit, joita käytetään sisällön pack. Jos haluat sisällyttää laskutoimitukset raportit ja Raporttinäkymät-ikkunan, voit ladata ja LCS-CompetenciesandDevelopment.pbix-tiedoston muokkaaminen. Tämä tiedosto on oletusarvoisesti tietomalli, joka on luotu sisältö pack. Kun olet tehnyt muutokset, voit luoda sellaisen organisaation sisällön pack ja raporttinäkymät, jotka sisältävät tietoja, jotka olet lisännyt.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



