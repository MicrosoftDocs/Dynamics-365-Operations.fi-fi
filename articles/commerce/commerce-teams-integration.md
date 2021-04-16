---
title: Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus
description: Tämä ohjeaihe sisältää yhteenvedon ja Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integroinnista.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3b7872757815d4eec0393e8b1c8c6ff5467e9473
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842653"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tämä ohjeaihe sisältää yhteenvedon ja Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integroinnista.

Dynamics 365 Commerce integroidaan Teamsin kanssa, jotta asiakkaat ja niiden työntekijät voivat parantaa tuottavuutta synkronoimalla tehtävänhallinnan näiden kahden sovelluksen välillä. Commercen ja Teamsin integroinnin saumaton tehtävähallinta sallii myymäläpäälliköiden ja työntekijöiden luoda tehtäväluetteloita, määrittää tehtäviä useisiin myymälöihin sekä seurata eri myymälöiden tehtävien tilaa kummasta tahansa sovelluksesta.

Commercen ja Teamsin integrointi on käytettävissä Commerce-versiosta 10.0.18 eteenpäin.

## <a name="key-features"></a>Tärkeimmät ominaisuudet

Seuraavassa on Commercen ja Microsoft Teamsin integroinnin tärkeitä ominaisuuksia:

- Valmistele Teams käyttämällä Commercen hyvin määritettyjä tietoja, kuten organisaatiorakennetta ja myymälöiden, työntekijöiden, käyttöoikeuksien ja liiketoimintakontekstin tietoja.
- Synkronoi helposti käynnissä olevat muutokset (esimerkiksi uusien myymälöiden lisäys tai uusien työntekijöiden palkkaaminen) Commercen ja Teamsin välillä, mutta säilytä Commerce organisaatiorakenteen tietojen päälähteenä.
- Integroi tehtävien hallinta Commercen ja Teamsin välillä, jotta työntekijät, myymäläpäälliköt, alueelliset esimiehet ja viestintäpäälliköt voivat käsitellä tehtävänhallintaa kummasta tahansa sovelluksesta.

## <a name="prerequisites-for-using-integration-features"></a>Integrointiominaisuuksien käytön edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit aloittaa Microsoft Teams -integrointiominaisuuksien käytön:

- Microsoft 365 Business Standard License (Tämä lisenssi sisältää Teamsin.)
- Azure Active Directory(Azure AD) -tilit kaikille myymäläpäälliköille ja työntekijöille
- Myyntipistejärjestelmät, jotka on konfiguroitu Azure AD -todennuksella

## <a name="conceptual-architecture"></a>Käsitteellinen arkkitehtuuri

Seuraavassa kuvassa havainnollistetaan Dynamics 365 Commercen ja Microsoft Teamsin integroinnin käsitteellistä arkkitehtuuria, ja esimerkinä käytetään San Franciscon myymälää. Sekä Teams että Commercen myyntipistesovellus käyttävät Microsoft Planneria tietovarastona, jotta Teamsista julkaisut tehtävät näkyvät myyntipistesovelluksessa sekä myymäläpäälliköiden myyntipistesovelluksella luomat ad-hoc -tehtäviä näkyvät Teamsissa. Näin sovellusten välillä syntyy saumaton tehtävien hallinta.    

![Commercen ja Teamsin integroinnin arkkitehtuuri](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>Lisäresurssit

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)
