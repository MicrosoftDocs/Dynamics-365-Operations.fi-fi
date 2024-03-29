---
title: Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä
description: Tässä artikkelissa kuvataan, kuinka tehtävänhallinta synkronoidaan Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä.
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746094"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, kuinka tehtävänhallinta synkronoidaan Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä.

Teamsin integroinnin päätatarkoituksia on mahdollistaa tehtävänhallinnan synkronointi myyntipistesovelluksen ja Teamsin välillä. Näin myymälän työntekijät voivat hallita tehtäviä myyntipistesovelluksen tai Teamsin avulla, eikä heidän tarvitse vaihtaa sovellusta.

Koska Planneria käytetään Teamsin tehtävien tietovarastona, Teamsin ja Dynamics 365 Commercen välillä on oltava linkki. Tämä linkki voidaan luoda käyttämällä tietylle myymäläryhmälle tiettyä suunnitelman tunnusta.

Seuraavissa menettelyissä näytetään, miten tehtävähallinnan synkronointi määritetään myyntipisteen ja Teams-sovellusten välillä.

## <a name="link-pos-and-teams-for-task-management"></a>Myyntipisteen ja Teamsin linkitäminen tehtävien hallintaa varten

Noudattamalla seuraavia ohjeita voit linkittää myyntipisteen ja Microsoft Teamsin tehtävien hallitsemiseksi Commerce headquartersissa.

> [!NOTE]
> Ennen kuin yrität integroida tehtävienhallinnan Teamsiin, varmista, että olet ottanut [Dynamics 365 Commerce- ja Microsoft Teams -integraation](enable-teams-integration.md) käyttöön. 

1. Siirry kohtaan **Retail ja Commerce \> Tehtävien hallinta \> Tehtävien integrointi Microsoft Teamsin kanssa**.
1. Valitse toimintoruudussa **Muokkaa**.
1. Määritä **Ota tehtävienhallinnan integrointi käyttöön** -asetukseksi **Kyllä**.
1. Valitse toimintoruudussa **Tallenna**.
1. Valitse toimintoruudussa **Määritä tehtävien hallinta**. Näyttöön tuleva ilmoitus kertoo, että järjestelmä luo erätyötä, jonka nimi **Teamsin valmistelu**.
1. Siirry kohtaan **Järjestelmänvalvonta \> Kyselyt \> Erätyöt** ja etsi uusin työ, jolla on nimi **Teamsin valmistelu**. Odota, kunnes tämä työ on suoritettu.
1. Suorita **CDX-työ 1070**, kun haluat julkaista suunnitelman tunnuksen ja myymälän viitteet Retail Serveriin.

## <a name="publish-a-test-task-list-in-teams"></a>Testitehtäväluettelon julkaiseminen Teamsissa

Seuraavissa ohjeissa oletetaan, että myymälätiimit käyttävät Commercen ja Microsoft Teamsin tehtävien hallinnan integrointia ensimmäistä kertaa.

Voit julkaista testitehtäväluettelon Teamsissa noudattamalla seuraavia vaiheita.

1. Kirjaudu Teamsiin viestintäpäällikkönä. Viestintäpäälliköt ovat yleensä käyttäjiä, joilla on Commercessa **aluepäällikön** rooli.
1. Valitse vasemmanpuoleisesta siirtymisruudusta **Plannerin tehtävät**.
1. Valitse **Julkaisut luettelot** -välilehden vasemmassa alakulmassa **Uusi luettelo** ja nimeä uusi luettelon nimellä **Testitehtäväluettelo**.
1. Valitse **Luo**. Uusi luettelo näkyy **Luonnokset**-kohdassa.
1. Anna **Tehtävän otsikko** -kohdassa ensimmäisen tehtävän otsikoksi **Teams-integroinnin testaus**. Valitse sitten **Syötä**.
1. Valitse tehtäväluettelo **Luonnos**-luettelosta. Valitse sitten oikeasta yläkulmasta  **Julkaise** .
1. Valitse **Valitse kenelle julkaistaan** -valintaikkunassa ryhmät, joiden tulisi vastaanottaa testitehtäväluettelo.
1. Tarkista julkaisusuunnitelma valitsemalla **Seuraava**. Jos muutoksia on tehtävä, valitse  **Takaisin**. 
1. Valitse **Jatka vahvistamalla** ja valitse sitten **Julkaise**.
1. Kun julkaisu on valmis, **Julkaistut luettelot** -välilehden yläosassa oleva sanoma ilmaisee, onko tehtäväluettelo toimitettu onnistuneesti.

Lisätietoja on kohdassa [Organisaation töiden luonti ja seuranta tehtäväluetteloita julkaisemalla](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> Kun tehtäväluettelo on julkaistu onnistuneesti Teamsissa, tehtävät näytetään myyntipisteessä. Tämän jälkeen myyntipisteen päälliköiden ja kassanhoitajien täytyy ottaa Azure AD -kirjautuminen käyttöön myyntipisteessä. Lisätietoja on artikkelissa [Azure Active Directory -todennuksen ottaminen käyttöön myyntipistekirjautumisessa](aad-pos-logon.md). 

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä](map-stores-existing-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)
