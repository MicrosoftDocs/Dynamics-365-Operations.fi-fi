---
title: Käyttäjäroolien hallinta Microsoft Teamsissa
description: Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce -käyttäjärooleja hallitaan Microsoft Teamsissa.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2984bf1d4d93c3a83cb6ba215617074c786c2c99
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286381"
---
# <a name="manage-user-roles-in-microsoft-teams"></a>Käyttäjäroolien hallinta Microsoft Teamsissa

[!include [banner](includes/banner.md)]

Tässä artikkelissa kerrotaan, miten Microsoft Dynamics 365 Commerce -käyttäjärooleja hallitaan Microsoft Teamsissa.

Kun luot ryhmän kullekin myymälälle tai kanavalle Teamsissa, luodaan ryhmän jäsenyys, joka vastaa ryhmää (esim. `HOUSTON_D365@<YourTenantAzureADDomain>.com`). Ryhmän jäsenyyteen kuuluville kaikille myymälätyöntekijöille määritetään toinen seuraavista käyttäjärooleista: **Omistaja** tai **Jäsen**. Myymälän työntekijät, joilla on **Omistaja**-käyttäjärooli, voivat suorittaa toimintoja, kuten lisätä yksityisen kanavan sekä lisätä tai poistaa jäseniä. Myymäläpäälliköilla on yleensä **Omistaja**-käyttäjärooli.

Seuraavassa kuvassa on esimerkki ryhmän jäsenten ja niiden käyttäjäroolien luettelosta Microsoft Teams -hallintakeskuksessa.

![Ryhmän jäsenet ja käyttäjäroolit Microsoft Teams -hallintakeskuksessa.](media/d365-commerce-teams-integration-user-roles.png)

Lisätietoja on kohdassa [Ryhmän omistajien ja jäsenten määrittäminen Microsoft Teamsissa](/microsoftteams/assign-roles-permissions).

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)
