---
title: "Korvaukset ja edut Power BI-sisältö"
description: "Tässä aiheessa kuvataan toiminnot - korvaukset ja edut Power BI sisällön osalta Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>Korvaukset ja edut Power BI-sisältö

Tässä aiheessa kuvataan toiminnot - korvaukset ja edut Power BI sisällön osalta Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja.

<a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
--------------------------

Löydät jaetut varat kirjaston Microsoft Dynamics Lifecycle Services (LCS) sisältöpaketti korvauksia ja etuuksia. Saat lisätietoja siitä, miten sisältö pack ladata ja liittää sen Microsoft Dynamics-365, toimintojen tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältö pack
Sen jälkeen, kun olet muodostanut yhteyden oman Dynamics 365 toimintoja tietojen sisältö pack, raportit näkyvät organisaation tiedot. Jos et ole koskaan käyttänyt Microsoft Power BI ennen, saat siitä lisätietoja [sivulla ohjattu oppiminen Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raportit, jotka sisältyvät sisältö pack on sekä kaavioita ja taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                     | Sisältö                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Comp ja hyödyn analyysia | Tunti- ja tuntipalkkaisille työntekijöille yritys, keskimääräinen tuntipalkan keskimääräistä palkkaa kuukausipalkkainen, työntekijöiden työsuhteen tyypin mukaan ja suunnitelman voimaanastuminen |
| Työsuhde-etuudet          | Työntekijän mukaan valitun edun rekisteröimisen                                                                                               |

Voit suodattaa kaavioita ja laatat raporteissa ja kiinnitä kaavioita ja laatat Dashboardiin. Saat lisätietoja siitä, miten suodatin ja Power BI-pin [Luo ja määritä A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Työvaiheiden tietoja Dynamics 365 käytetään täyttämään raporttien sisältöpaketti korvauksia ja etuuksia. Seuraavassa taulukossa on esitetty kohteiden sisältö pack on perustunut.

| Kokonaisuus                            | Sisältö                                                                                                   | Suhteisiin                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työvoiman\_CalendarOffset         | Kalenterin siirtymät sektorin raportit                                                                          | Työvoiman\_työvoiman PastPositionAssignment\_PositionTrend Workorce\_WorkerTrend työvoiman\_TerminatedWorker                                                                                                                                                                                                                     |
| Työvoiman\_yrityksen                | Yritykset voivat suodattaa raporttien mukaan                                                                             | Työvoiman\_työvoiman CurrentCompensation\_CurrentWorker työvoiman\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Työvoiman\_korvaus           | Taksa ja kuinka usein ajan myötä                                                                           | Työvoiman\_työvoiman CurrentCompensation\_CurrentWorker työvoiman\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Työvoiman\_CurrentCompensation    | Taksa ja taajuus nykyisestä päivämäärästä                                                              | Työvoiman\_yrityksen työvoiman\_korvaus työvoiman\_demografia työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                            |
| Työvoiman\_CurrentPosition        | Nykyisestä päivämäärästä (FTE) kokopäiväisten toimien Avaa toimet ja avaa ja-täytetty toimet | Työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                                                                                               |
| Työvoiman\_CurrentWorker          | Työntekijöiden nykyistä päivämäärää, ikä ja Henkilöstömäärä                                                         | Työvoiman\_yrityksen työvoiman\_korvaus työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_WorkerName työvoiman\_työvoiman ReportsToWorkerName\_WorkerTitle työvoiman\_demografia työvoiman\_työn työvoiman\_työllisyys työvoiman\_sijoittaa työvoiman\_WorkerBenefit                                            |
| Työvoiman\_päivämäärä                   | Päiviä, viikkoja, kuukausia ja vuosia                                                                             | Työvoiman\_työvoiman PastPositionAssignment\_PositionTrend työvoiman\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Työvoiman\_demografia           | Syntymäajan, sukupuolen, etnisen alkuperän ja siviilisääty                                                   | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_työskentely             | Alkamispäivämäärä, päättymispäivämäärä ja tapahtumapäivämäärä                                                                  | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_GeographicLocation     | Paikkakunnan, läänin, postal code ja osavaltio tai provinssi                                                           | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_työ                    | Funktion tyyppi ja otsikko                                                                                  | Työvoiman\_työvoiman CurrentPosition\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Työvoiman\_PastPositionAssignment | Syy tehtävän, alkamispäivämäärä, päättymispäivämäärä ja työn                                                           | Työvoiman\_CalendarOffset työvoiman\_päivä työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                                                     |
| Työvoiman\_suorituskyvyn            | Luokitus ja arviointimallin kuvaus                                                                      | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_sijainti               | Osasto, FTE, sijainti, toimen ja otsikko                                                        | Työvoiman\_työvoiman CurrentPosition\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Työvoiman\_PositionTrend          | Toimien aika, FTE ja työn kautta                                                                          | Työvoiman\_CalendarOffset työvoiman\_päivä työvoiman\_projektin työvoiman\_sijainti                                                                                                                                                                                                                                                     |
| Työvoiman\_ReportsToWorkerName    | Etunimi, Sukunimi ja koko nimi                                                                       | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_taito                  | Taito, osaamisalueen ja luokitus                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Työvoiman\_TerminatedWorker       | Työntekijöiden työsuhteen loppumispäivämäärä, otsikko, sijainti ja työ päättyi                                             | Työvoiman\_yrityksen työvoiman\_korvausta työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_työvoiman WorkerName\_ReportsToWorkerName työvoiman\_CalendarOffset Workforces\_päivä työvoiman\_WorkerTitle työvoiman\_demografia työvoiman\_työllisyys työvoiman\_projektin työvoiman\_sijoittaa työvoiman\_WorkerBenefit |
| Työvoiman\_WorkerBenefit          | Voimaantulo, etu-vaihtoehdon, järjestelyyn ja etutyyppi                                             | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_WorkerName             | Etunimi, Sukunimi ja koko nimi                                                                       | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Työvoiman\_WorkerTitle            | Otsikko ja Virkaikä                                                                                   | Työvoiman\_työvoiman CurrentWorker\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Työntekijöiden aika, Henkilöstömäärä, yrityksen ja paikan päälle                                                        | Työvoiman\_yrityksen työvoiman\_korvausta työvoiman\_GeographicLocation työvoiman\_suorituskyvyn työvoiman\_työvoiman WorkerName\_ReportsToWorkerName työvoiman\_CalendarOffset Workforces\_päivä työvoiman\_WorkerTitle työvoiman\_demografia työvoiman\_työllisyys työvoiman\_projektin työvoiman\_WorkerBenefit                     |

Luo lasketut mitat tietomallin käytettiin entiteetit. Nämä lasketaan toimenpiteet sitten laskemisessa käytetään Suorituskyvyn mittareiden (KPI: T) ja raportit, joita käytetään sisällön pack. Jos haluat sisällyttää laskutoimitukset raportit ja Raporttinäkymät-ikkunan, voit ladata ja LCS-CompensationandBenefits.pbix-tiedoston muokkaaminen. Tämä tiedosto on oletusarvoisesti tietomalli, joka on luotu sisältö pack. Kun olet tehnyt muutokset, voit luoda sellaisen organisaation sisällön pack ja raporttinäkymät, jotka sisältävät tietoja, jotka olet lisännyt.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



