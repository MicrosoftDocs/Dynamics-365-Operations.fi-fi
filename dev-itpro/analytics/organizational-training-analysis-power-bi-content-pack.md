---
title: "Organisaation koulutus Power BI-sisältö"
description: "Tässä aiheessa kuvataan Dynamics-365 Operations - organisaation koulutus Power BI-sisältöä varten. Selitetään, miten sisältö pack ja kuvataan tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisaation koulutus Power BI-sisältö

Tässä aiheessa kuvataan Dynamics-365 Operations - organisaation koulutus Power BI-sisältöä varten. Selitetään, miten sisältö pack ja kuvataan tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack.

<a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
--------------------------

Voit etsiä organisaation koulutuksen sisältö pack jaettujen varojen kirjaston Microsoft Dynamics Lifecycle Services (LCS). Saat lisätietoja siitä, miten sisältö pack ladata ja liittää sen Microsoft Dynamics-365, toimintojen tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältö pack
Sen jälkeen, kun olet muodostanut yhteyden oman Dynamics 365 toimintoja tietojen sisältö pack, raportit näkyvät organisaation tiedot. Jos et ole koskaan käyttänyt Microsoft Power BI ennen, saat siitä lisätietoja [sivulla ohjattu oppiminen Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raportit, jotka sisältyvät sisältö pack on sekä kaavioita ja taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti          | Sisältö                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurssien analysointi | Sijainti, tila ja rekisteröintiluettelo kurssin osallistujien rekisteröinti |
| Kurssityypit    | Kurssityypit osaamisalueittain                                                       |

Voit suodattaa kaavioita ja laatat raporteissa ja kiinnitä kaavioita ja laatat Dashboardiin. Saat lisätietoja siitä, miten suodatin ja Power BI-pin [Luo ja määritä A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Raportit organisaation koulutuksen sisältö Pack täyttämiseen käytetään työvaiheiden tietoja Dynamics 365. Seuraavassa taulukossa on esitetty kohteiden sisältö pack on perustunut.

| Kokonaisuus                    | Sisältö                                                         | Suhteisiin                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koulutus\_CalendarOffset  | Kalenterin siirtymät sektorin raportit                                | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_yrityksen         | Yritykset voivat suodattaa raporttien mukaan                                   | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_kurssin          | Kurssin kuvaus, opettajan nimi, sijainti, huoneen ja tila | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees koulutuksen\_CourseSkill                                                                                                                             |
| Koulutus\_CourseAgenda    | Esityslistan ja kurssin aloitus- ja lopetusajat                          | Koulutus\_yrityksen koulutuksen\_CalendarOffset koulutus\_päivämäärä koulutus\_kurssin                                                                                                                         |
| Koulutus\_CourseAttendees | Nimi, tila, työn ja rekisteröinnin päivämäärä                         | Koulutus\_yrityksen koulutuksen\_CalendarOffset koulutus\_koulutuksen päivämäärä\_demografia koulutus\_työsuhteen koulutus\_kurssi koulutus\_WorkerName koulutuksen\_WorkerTitle koulutus\_työn koulutus\_sijainti |
| Koulutus\_CourseSkill     | Taito, osaamisalueen ja taso                                     | Koulutus\_kurssin                                                                                                                                                                                   |
| Koulutus\_päivämäärä            | Päiviä, viikkoja, kuukausia ja vuosia                                   | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_demografia    | Syntymäajan, sukupuolen, etnisen alkuperän ja siviilisääty         | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_työskentely      | Alkamispäivämäärä, päättymispäivämäärä ja tapahtumapäivämäärä                        | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_työ             | Funktion tyyppi ja otsikko                                        | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_sijainti        | Paikka, otsikko ja kokopäiväisten (FTE)                  | Koulutus\_koulutuksen CourseAgenda\_CourseAttendees                                                                                                                                                   |
| Koulutus\_WorkerName      | Etunimi, Sukunimi ja koko nimi                             | Koulutus\_CourseAttendees                                                                                                                                                                          |
| Koulutus\_WorkerTitle     | Otsikko ja Virkaikä                                         | Koulutus\_CourseAttendees                                                                                                                                                                          |

Luo lasketut mitat tietomallin käytettiin entiteetit. Nämä lasketaan toimenpiteet sitten laskemisessa käytetään Suorituskyvyn mittareiden (KPI: T) ja raportit, joita käytetään sisällön pack. Jos haluat sisällyttää laskutoimitukset raportit ja Raporttinäkymät-ikkunan, voit ladata ja LCS-Training.pbix-tiedoston muokkaaminen. Tämä tiedosto on oletusarvoisesti tietomalli, joka on luotu sisältö pack. Kun olet tehnyt muutokset, voit luoda sellaisen organisaation sisällön pack ja raporttinäkymät, jotka sisältävät tietoja, jotka olet lisännyt.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



