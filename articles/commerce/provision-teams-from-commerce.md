---
title: Microsoft Teamsin valmistelu Dynamics 365 Commercesta
description: Tässä aiheessa kuvataan, miten Microsoft Teams voidaan valmistella käyttäen organisaatiotietoja Dynamics 365 Commercesta.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022443"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>Microsoft Teamsin valmistelu Dynamics 365 Commercesta

[!include [banner](includes/banner.md)]

Tässä aiheessa kuvataan, miten Microsoft Teams voidaan valmistella käyttäen organisaatiotietoja Dynamics 365 Commercesta.

Dynamics 365 Commerce tarjoaa helpon tavan määrittää Teamsin, jos et ole vielä määrittänyt vähittäismyymälöille Teamsia. Käyttämällä Commercen hyvin määritettyjä tietoja, joita haluat käyttää Teamsissa, voit auttaa myymälän työntekijöitä pääsemään alkuun Teamsin käytössä. Näitä tietoja ovat organisaatiohierarkia, myymälän nimet, työntekijätiedot ja Azure Active Directory (Azure AD) -tilit. 

Teamsin varausprosessissa on kaksi päävaihetta:

1. Luo Teamsissa ryhmä kutakin vähittäismyymälää varten ja lisää myymälän työntekijöitä ryhmän jäseniksi. Jos työntekijä on liitetty yhteen vähittäismyymälään, ryhmän jäsenyys vastaa tätä määritystä. Luodaan viestintäryhmä, joka sisältää jäseniä aluepäälliköiksi, jotta tehtäviä voidaan julkaista Teamsissa.
1. Lataa organisaatiohierarkia Commercesta Teamsiin.

## <a name="provision-teams-in-commerce-headquarters"></a>Valmistele Teams Commerce headquarters -sovelluksessa

Tee seuraavat toimet ennen Microsoft Teamsin valmistelua:

- Vahvista, että kaikista aluepäälliköista on tehty viestintäpäälliköitä.
- Vahvista, että jokaisen myymäläpäällikön ja työntekijän Azure-tili on liitetty esimiehen tai työntekijätietueeseen Commerce headquarters -sovelluksessa.

Voit valmistella Teamsin Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.

1. Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.
1. Valitse toimintoruudussa **Valmistele Teams**. Luodaan erätyö, jonka nimi on **Teamsin valmistelu**.
1. Siirry kohtaan **Järjestelmänvalvonta \> Kyselyt \> Erätyöt** ja etsi uusin työ, jolla on nimi **Teamsin valmistelu**. Odota tämän työn valmistumista.

> [!TIP]
> Jos mikään aluepäälliköistä, myymäläpäälliköistä ja myymälätyöntekijöistä ei ole liitetty Teams-lisenssiin, näkyviin saattaa tulla seuraava virhesanoma: "Käyttäjän SKU-luokkien noutaminen ei onnistunut." Voit korjata ongelman valitsemalla toimintoruudusta **Synkronoi ryhmät ja jäsenet**.

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>Teamsin valmistelun vahvistaminen Teams-hallintakeskuksessa

Suorita seuraavat vaiheet, kun haluat vahvistaa Microsoft Teamsin valmistelun Microsoft Teams -hallintakeskuksessa.
    
1. Siirry [Teams-hallintakeskukseen](https://admin.teams.microsoft.com/) ja kirjaudu sisään sähköisen kaupankäynnin vuokraajan järjestelmänvalvojana.
1. Valitse vasemmassa siirtymisruudussa **Teams** laajentaaksesi sen ja valitse sitten **Ryhmien hallinta**.
1. Vahvista, että kullekin Commerce-vähittäismyymälälle on luotu yksi ryhmä.
1. Valitse ryhmä ja vahvista, että myymälän työntekijät on lisätty ryhmään jäseninä.
1. Valitse vasemmassa siirtymisruudussa **Käyttäjät** ja vahvista, että kaikkien myymälöiden kaikki myymälän työntekijät on lisätty käyttäjinä.

Seuraavassa kuvassa on esimerkki Teams-hallintakeskuksen **Ryhmien hallinta** -sivusta.

![Esimerkki Ryhmien hallinta -sivusta Teams-hallintakeskuksessa](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>Lataa Commercen organisaatiohierarkia Teamsiin
    
Commerce-organisaatiohierarkian avulla voit Microsoft Teamsissa julkaista tehtäviä kaikissa tai valituissa myymälöissä, jotka käyttävät samaa hierarkiarakennetta.

Jos haluat ladata Commerce-organisaatiohierarkian Teamsiin, toimi seuraavasti.
    
1. Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integroinnin määritys**.
1. Valitse **Lataa kohdehierarkia** ja lataa sitten organisaatiohierarkian pilkuilla erotettu CSV-tiedosto valitsemalla **Vähittäismyymälät alueen mukaan**.
1. Asenna Microsoft Teams PowerShell -moduuli noudattamalla ohjeita kohdassa [Asenna Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).
1. Kun järjestelmä antaa kehotteen Teams PowerShell -ikkunassa, kirjaudu sisään vuokraajan järjestelmänvalvojan Azure AD-tilin avulla.
1. Lataa kohdehierarkian CSV-tiedosto palvelimeen noudattamalla ohjeita kohdassa [Ryhmän kohdehierarkian määrittäminen](/microsoftteams/set-up-your-team-hierarchy).

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>Tarkista, että organisaatiohierarkia on ladattu Teamsiin

Tarkista seuraavien vaiheiden avulla, että organisaatiohierarkia on ladattu Microsoft Teamsiin.

1. Kirjaudu Teamsiin viestintäpäällikkönä.
1. Valitse vasemmanpuoleisesta siirtymisruudusta **Plannerin tehtävät**.
1. Luo **Julkaisut luettelot** -välilehdessä uusi luettelo, jolla on tyhjä tehtävä.
1. Valitse **Julkaise**. Organisaatiohierarkian pitäisi näkyä **Valitse kenelle julkaistaan** -valintaikkunassa seuraavan kuvan esimerkin mukaisesti.

![Esimerkki organisaatiohierarkiasta Valitse kenelle julkaistaan -valintaikkunassa](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)