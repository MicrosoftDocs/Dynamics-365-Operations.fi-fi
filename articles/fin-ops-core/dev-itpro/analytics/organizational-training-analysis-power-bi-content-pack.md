---
title: Organisaatiokoulutuksen Power BI -sisältö
description: Tässä aiheessa kuvataan Finance and Operations - Organisaation opetus Power BI -sisältö.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd48c12ea3ea31904c437f678888a51e5381cfcfbeef0e1c709858b0c6cb857d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763545"
---
# <a name="organizational-training-power-bi-content"></a>Organisaatiokoulutuksen Power BI -sisältö

[!include [banner](../includes/banner.md)]

Tässä aiheessa kuvataan Finance and Operations - Organisaation opetus Power BI -sisältö.

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja on kohdassa [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti          | Sisältö                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kurssien analysointi | Ilmoittautuminen sijainnin mukaan, kurssin osallistujat tilan mukaan sekä ilmoittautumisluettelo |
| Kurssityypit    | Kurssityypit osaamisalueittain                                                       |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI:ssä on kohdassa [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Sovelluksen tietoja käytetään organisaation koulutuksen sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                    | Sisältö                                                         | Suhteet muihin yksiköihin |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | Kalenterin siirtymät raporttien osittamiseen                                | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Company         | Yritykset, joiden mukaan raportit suodatetaan                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Course          | Kurssi, kuvaus, opettajan nimi, sijainti, huone ja tila | Training\_CourseAgenda, Training\_CourseAttendees, Training\_CourseSkill |
| Training\_CourseAgenda    | Esityslista, kurssi sekä aloitus- ja lopetusajat                          | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Course |
| Training\_CourseAttendees | Nimi, tila, työ ja rekisteröinnin päivämäärä                         | Training\_Company, Training\_CalendarOffset, Training\_Date, Training\_Demographics, Training\_Employment, Training\_Course, Training\_WorkerName, Training\_WorkerTitle, Training\_Job, Training\_Position |
| Training\_CourseSkill     | Taito, osaamisalueen tyyppi ja taso                                     | Training\_Course |
| Training\_Date            | Päiviä, viikkoja, kuukausia ja vuosia                                   | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Demographics    | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty         | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Employment      | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Job             | Tehtävä, tyyppi ja nimike                                        | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_Position        | Toimi, nimike ja kokopäiväistä vastaavat (FTE)                  | Training\_CourseAgenda, Training\_CourseAttendees |
| Training\_WorkerName      | Etunimi , sukunimi ja koko nimi                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | Nimike ja virkaikä                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]