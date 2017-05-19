---
title: "Organisaation koulutuksen Power BI -sisältö"
description: "Tässä aiheessa kuvataan Dynamics 365 for Operationsin organisaation koulutuksen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpaketin. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 197bcecf21074413848bb1b22d46f17bf236fbc4
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisaation koulutuksen Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan Dynamics 365 for Operationsin organisaation koulutuksen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpaketin. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
--------------------------

Löydät organisaation koulutuksen sisältöpaketin Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Saat lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Microsoft Dynamics 365 for Operationsin tietoihin, artikkelista [LCS:n Power BI -sisältö Microsoftilta ja kumppaneilta](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin Dynamics 365 for Operations -tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja löydät artikkelista [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti          | Sisältö                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurssien analysointi | Ilmoittautuminen sijainnin mukaan, kurssin osallistujat tilan mukaan sekä ilmoittautumisluettelo |
| Kurssityypit    | Kurssityypit osaamisalueittain                                                       |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Dynamics 365 for Operations -sovelluksen tietoja käytetään organisaation koulutuksen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                    | Sisältö                                                         | Suhteet muihin yksiköihin                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | Kalenterin siirtymät raporttien osittamiseen                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | Yritykset, joiden mukaan raportit suodatetaan                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | Kurssi, kuvaus, opettajan nimi, sijainti, huone ja tila | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | Esityslista, kurssi sekä aloitus- ja lopetusajat                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | Nimi, tila, työ ja rekisteröinnin päivämäärä                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | Taito, osaamisalueen tyyppi ja taso                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | Päiviä, viikkoja, kuukausia ja vuosia                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | Tehtävä, tyyppi ja nimike                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | Toimi, nimike ja kokopäiväistä vastaavat (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | Etunimi , sukunimi ja koko nimi                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | Nimike ja virkaikä                                         | Training\_CourseAttendees                                                                                                                                                                          |

Näitä yksikköjä käytettiin luomaan laskettuja mittoja tietomallissa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisältöpaketissa käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata Training.pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





