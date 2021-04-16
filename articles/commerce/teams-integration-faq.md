---
title: Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on vastauksia Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointia koskeviin usein kysyttyihin kysymyksiin.
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
ms.openlocfilehash: 26e1dc53126c0615332457aa785415c4c7112bbd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842658"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä ohjeaiheessa on vastauksia Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointia koskeviin usein kysyttyihin kysymyksiin.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>Kenestä myymälästä tulee ryhmän omistaja, kun Teams valmistellaan Commercesta? 

Kaikki myymäläpäälliköt lisätään automaattisesti omistajiksi vastaavaan ryhmään, jotta he voivat suorittaa toimintoja, kuten lisätä yksityisen kanavan ja lisätä tai poistaa jäseniä. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>Miten voin määrittää viestintäpäällikön roolin työntekijälle Commerce headquartersissa? 

Viestintäpäälliköt Microsoft Teamsissa voivat luoda ja julkaista tehtäväluetteloita. Organisaation työntekijöille, joiden on määrä tulla viestintäpäälliköksi, on oltava vähittäismyynnin tehtävienhallinnan rooli Commerce headquarters -sovelluksessa.

Liitä vähittäismyynnin tehtävienhallinnan rooli työntekijään Commerce headquartersissa noudattamalla seuraavia ohjeita.

1. Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttäjät**.
1. Valitse työntekijä.
1. Valitse **Käyttäjän roolit** -pikavälilehdessä **Määritä roolit**.
1. Valitse **Määritä roolit käyttäjälle** -valintaikkunassa **vähittäismyynnin tehtävienhallinnan** rooli ja valitse **OK**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>Miten tietty organisaatiohierarkia voidaan ladata Microsoft Teamsiin?

Commerce headquartersissa jokaisen organisaation hierarkia liittyy vähintään yhteen tarkoitukseen. Varmista, että hierarkiaan, jonka haluat valmistella Microsoft Teamsiin, on liitetty **vähittäismyynnin raportoinnin** tarkoitus seuraavan esimerkkikuvan mukaisesti. 

![Esimerkki organisaatiohierarkian tarkoituksesta Commerce headquartersissa](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>Miten sallin vähittäismyynnin työntekijöiden kirjautumisen Commerce-myyntipisteeseen Azure Active Directory (Azure AD) -todennuksella?

Lisätietoja Commerce-myyntipisteen kirjautumiskokemuksen määrittämisestä Azure AD-todennukseen on kohdassa [Ota Azure Active Directory -todennus käyttöön myyntipisteen kirjautumisessa](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>Miten myymälöiden ja niitä vastaavien ryhmien määritys Commerce headquarters -sovelluksessa toimii, jos organisaationi on jo luonut ryhmiä Microsoft Teamsissa?

Lisätietoja myymälöiden ja ryhmien yhdistämisestä, jos ryhmiä on aiemmin luotu, on kohdassa [Myymälöiden ja vastaavien ryhmien yhdistäminen, jos organisaatiossasi on aiemmin luotuja ryhmiä Microsoft Teamsissa](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>Miten poistan istunnon tallennustilaan tallennetun Microsoft Graph API -tunnuksen?

Käyttäjän, joka on kirjautunut myyntipisteeseen (POS) Azure Active Directory (Azure AD) tilillä, on kirjauduttava ulos myyntipisteestä tai suljettava sovellus tyhjentääkseen istunnon tallennustilan. 

> [!TIP]
> Suositeltava käytäntö on, että myymälätyöntekijät lukitsevat kassapäätteen tai kirjautuvat ulos istunnosta silloin, kun päätettä ei käytetä. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>Mitä tapahtuu, jos myymälällä ei ole myymäläpäälliköitä?

Jos myymälällä ei ole päälliköitä, ryhmää ei luoda myymälälle tai Teamsissa. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>Mitä tapahtuu, jos myymäläpäällikkö lähtee yrityksestä?

Kuka tahansa, jolla on omistajarooli, voi lisätä uuden myymäläpäällikön Commerce headquarters -sovelluksessa ja valmistella Teamsin uudelleen, jotta uudella esimiehellä on ryhmän tarvittavat käyttöoikeudet Teamsissa. 

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)
