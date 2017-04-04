---
title: "Työhönotosta vastaavan sisällön virtaa BI"
description: "Tässä aiheessa kuvataan toiminnot - Power BI työhönotosta vastaavan sisällön osalta Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Työhönotosta vastaavan sisällön virtaa BI

Tässä aiheessa kuvataan toiminnot - Power BI työhönotosta vastaavan sisällön osalta Dynamics-365. Artikkelissa kerrotaan, miten voit käyttää raportteja, jotka sisältyvät sisältö pack ja tietomallin ja yhteisöistä, joita käytettiin rakentaa sisältö pack tietoja.

<a name="accessing-the-content-pack"></a>Sisältö pack käyttäminen
--------------------------

Löydät työhönoton sisältöpaketti jaettujen varojen kirjaston Microsoft Dynamics Lifecycle Services (LCS). Saat lisätietoja siitä, miten sisältö pack ladata ja liittää sen Microsoft Dynamics-365, toimintojen tietojen [virtaa BI sisältöä Microsoftin ja kumppanien LCS-](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Raportit, jotka sisältyvät sisältö pack
Sen jälkeen, kun olet muodostanut yhteyden oman Dynamics 365 toimintoja tietojen sisältö pack, raportit näkyvät organisaation tiedot. Jos et ole koskaan käyttänyt Microsoft Power BI ennen, saat siitä lisätietoja [sivulla ohjattu oppiminen Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Raportit, jotka sisältyvät sisältö pack on sekä kaavioita ja taulukoita, jotka sisältävät lisätietoja. Seuraavassa taulukossa kuvataan raportit.

| Raportti                       | Sisältö                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Hakijan analysointi           | Hakijoiden mukaan työhön, hakijan lähteistä, sijaintiin ja hakijoiden määrä hakijoita           |
| Hakijan tilanne             | Hakijan tyyppi, tila ja Hakijan tilanne                                                    |
| Hakijan demografia       | Hakijan iän ja sukupuolen mukaan ja hakijoiden koulutustaso ja tila                             |
| Työhönoton analyysi          | NET vuokraus suhde, voit palkata huono palkkauksissa ja työhönoton kustannukset prosentteina käytettyjen päivien määrä keskimäärin                    |
| Rekrytointi-projektin analyysin | Työhönottoprojektien, aukkojen mukaan työhönottoprojektin työhönottoprojektin mukaan hakijoiden määrä |

Voit suodattaa kaavioita ja laatat raporteissa ja kiinnitä kaavioita ja laatat Dashboardiin. Saat lisätietoja siitä, miten suodatin ja Power BI-pin [Luo ja määritä A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Tietomallin ja yksiköiden tiedot
Työvaiheiden tietoja Dynamics 365 käytetään raporttien sisältö Pack työhönoton täyttämiseen. Seuraavassa taulukossa on esitetty kohteiden sisältö pack on perustunut.

| Kokonaisuus                          | Sisältö                                                         | Suhteisiin                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Työhönotosta vastaavan\_hakijalle           | Hakijoiden, palkattiin hakijoiden, suhde net vuokraus ja kustannukset          | Työhönotosta vastaavan\_ApplicantName rekrytointiominaisuuksien\_työhönotosta vastaavan yrityksen\_CalendarOffset Recuriting\_päivämäärä rekrytointiominaisuuksien\_GeographicLocation rekrytointiominaisuuksien\_rekrytointiominaisuuksien demografia\_työhönotosta vastaavan työn\_Media rekrytointiominaisuuksien\_RecruitmentProject                                |
| Työhönotosta vastaavan\_ApplicantName       | Hakijan Etunimi, Sukunimi ja koko nimi                   | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_CalendarOffset      | Kalenterin siirtymät sektorin raportit                                | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_yrityksen             | Yritykset voivat suodattaa raporttien mukaan                                   | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_päivämäärä                | Päiviä, viikkoja, kuukausia ja vuosia                                   | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_demografia        | Syntymäajan, sukupuolen, etnisen alkuperän ja siviilisääty         | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_EmployedApplicant   | Kirjoita hakijan, suorituskyky, aloituspäivämäärä ja hakijan           | Työhönotosta vastaavan\_työhönotosta vastaavan yrityksen\_työhönotosta vastaavan CalendarOffset\_työhönotosta vastaavan päivämäärän\_työhönotosta vastaavan GeographicLocation\_ApplicantName rekrytointiominaisuuksien\_työllisyyden rekrytointiominaisuuksien\_suorituskyvyn rekrytointiominaisuuksien\_työhönotosta vastaavan työn\_Media rekrytointiominaisuuksien\_RecruitmentProject          |
| Työhönotosta vastaavan\_työskentely          | Alkamispäivämäärä, päättymispäivämäärä ja tapahtumapäivämäärä                        | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_GeographicLocation  | Paikkakunnan, läänin, postal code ja osavaltio tai provinssi                 | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_työ                 | Funktion tyyppi ja otsikko                                        | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_Media               | Hakijoiden lähde                                             | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_suorituskyvyn         | Luokitus ja arviointimallin kuvaus                            | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_RecruitmentProject  | Hankkeen kuvaus, projektin tilan ja aukot                | Työhönotosta vastaavan\_hakijalle työhönotosta vastaavan\_työhönotosta vastaavan EmployedApplicant\_TerminatedApplicant                                                                                                                                                               |
| Työhönotosta vastaavan\_TerminatedApplicant | Päättynyt, hakijoiden, syy, suorituskyvyn ja työsuhteen päättymisen pvm | Työhönotosta vastaavan\_työhönotosta vastaavan yrityksen\_työhönotosta vastaavan CalendarOffset\_päivämäärä rekrytointiominaisuuksien\_työhönotosta vastaavan GeographicLocation\_työhönotosta vastaavan suorituskyvyn\_rekrytointiominaisuuksien demografia\_työllisyyden rekrytointiominaisuuksien\_Media rekrytointiominaisuuksien\_työhönotosta vastaavan RecruitmentProject\_ApplicantName |

Näiden yksiköiden oli käytettävä luoda laskettuja mittoja. Nämä lasketaan toimenpiteet sitten laskemisessa käytetään Suorituskyvyn mittareiden (KPI: T) ja raportit, joita käytetään sisällön pack. Jos haluat sisällyttää laskutoimitukset raportit ja Raporttinäkymät-ikkunan, voit ladata ja LCS-Recruiting.pbix-tiedoston muokkaaminen. Tämä tiedosto on oletusarvoisesti tietomalli, joka on luotu sisältö pack. Kun olet tehnyt muutokset, voit luoda sellaisen organisaation sisällön pack ja raporttinäkymät, jotka sisältävät tietoja, jotka olet lisännyt.

## <a name="additional-resources"></a>Lisäresurssit
Seuraavista linkeistä löydät hyödyllistä, entiteetteihin ja Power BI -sisällön rakentamiseen liittyvää tietoa:

-   [Tietoyksiköt](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisaation sisältöpakettien luominen](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Tietojen mallinnus Power BI:n avulla](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI -ruutujen lisääminen työtiloihin](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



