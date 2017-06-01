---
title: "Työhönoton Power BI -sisältö"
description: "Tässä aiheessa kuvataan Dynamics 365 for Operations - Recruiting -sovelluksen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: fi-fi
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>Työhönoton Power BI -sisältö

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan Dynamics 365 for Operations - Recruiting -sovelluksen Power BI -sisältöä. Siinä kuvataan, miten avaat sisältöpakettiin kuuluvat raportit. Lisäksi siinä kerrotaan sisältöpaketin rakentamisessa käytetystä tietomallista ja entiteeteistä.

<a name="accessing-the-content-pack"></a>Sisältöpaketin avaaminen
--------------------------

Löydät työhönoton sisältöpaketin Microsoft Dynamics Lifecycle Services (LCS):n jaettujen resurssien kirjastosta. Saat lisätietoja siitä, miten sisältöpaketti ladataan ja miten se liitetään Microsoft Dynamics 365 for Operationsin tietoihin, artikkelista [LCS:n Power BI -sisältö Microsoftilta ja kumppaneilta](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältöpakettiin
Kun olet liittänyt sisältöpaketin Dynamics 365 for Operations -tietoihin, organisaatiosi tiedot näkyvät raporteissa. Jos et ole käyttänyt Microsoft Power BI:tä aiemmin, lisätietoja löydät artikkelista [Power BI:n ohjattu oppiminen](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raporteissa, jotka sisältyvät sisältöpakettiin, on sekä kaavioita että taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                       | Sisältö                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Hakijan analyysi           | Hakijat työn mukaan, hakijoiden lähteet, hakijat sijainnin mukaan ja hakijoiden kokonaismäärä           |
| Hakijan tila             | Hakijat tyypin ja tilan mukaan sekä hakijan tila                                                    |
| Hakijan demografia       | Hakijat iän ja sukupuolen mukaan sekä hakijat koulutustason ja tilan mukaan                             |
| Työhönoton analyysi          | Työhönoton nettosuhde, palkkaukseen kuluvat keskimääräiset päivät, epäonnistuneiden palkkausten prosenttiosuus ja työhönoton kustannukset                    |
| Työhönottoprojektin analyysi | Työhönottoprojektien määrä, avoimet paikat työhönottoprojektin mukaan ja hakijat työhönottoprojektin mukaan |

Kaikkien raporttien kaavioita ja ruutuja voi suodattaa sekä kiinnittää koontinäyttöön. Lisätietoja suodattamisesta ja kiinnittämisestä Power BI -ohjelmassa löydät artikkelista [Koontinäytön luominen ja määrittäminen](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Dynamics 365 for Operations -ohjelman tietoja käytetään työhönoton sisältöpaketin raporttien täyttämiseen. Seuraavassa taulukossa on esitetty yksiköt, joihin sisältöpaketti on perustunut.

| Kokonaisuus                          | Sisältö                                                         | Suhteet muihin yksiköihin                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | Hakijat, palkatut hakijat, palkkauksen nettosuhde ja kustannukset          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | Hakijan etunimi, sukunimi ja koko nimi                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | Kalenterin siirtymät raporttien osittamiseen                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | Yritykset, joiden mukaan raportit suodatetaan                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | Päiviä, viikkoja, kuukausia ja vuosia                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | Syntymäaika, sukupuoli, etninen alkuperä ja siviilisääty         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | Hakija, suorituskyky, alkupäivämäärä ja hakijan tyyppi           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | Alkamispäivämäärä, päättymispäivämäärä ja siirtymispäivämäärä                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | Paikkakunta, lääni, postinumero ja osavaltio tai provinssi                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | Tehtävä, tyyppi ja nimike                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | Hakijoiden lähde                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | Pisteytys, kuvaus arviointimalli                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | Projektin kuvaus, projektin tila ja avoimet paikat                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | Työntekijät, joiden työsuhde on päätetty, syy, suorituskyky ja työsuhteen päättymispäivä | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

Näitä yksikköjä käytettiin laskettujen mittojen luomisessa. Näitä laskennallisia mittoja käytetään sitten laskemaan sisältöpaketissa käytettävät tunnusluvut (KPI:t) ja raportit. Jos haluat sisällyttää lisälaskutoimitukset raportteihin ja koontinäyttöön, voit ladata Recruiting.pbix-tiedoston LCS:stä ja muokata sitä. Tämä tiedosto on sisältöpaketin luomisessa käytetty oletustietomalli. Kun olet tehnyt haluamasi muutokset, voit luoda organisaation sisältöpaketin ja koontinäytön, joka sisältää lisäämäsi tiedot.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





