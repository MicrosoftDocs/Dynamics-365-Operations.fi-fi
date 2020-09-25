---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a022f8297066793080d254baa01410884a3fafd9
ms.sourcegitcommit: 55b729361ea852e38531c51972c6730e3d9c2b45
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/08/2020
ms.locfileid: "3776305"
---
# <a name="human-resources-app-in-teams"></a>Teamsin Human Resources -sovellus

[!include [banner](includes/preview-feature.md)]

Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa. Työntekijät voivat pyytää tietoja botin avustuksella. **Poissaolo**-välilehdessä on lisätietoja.

![Human Resources Teamsin lomasovelluksen botti](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a>Asentaminen ja määrittäminen

Human Resources -sovellus löytyy Teams-kaupasta. Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).

Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa

Jos haluat, että käyttäjät voivat vastaanottaa lomapyyntöilmoitukset Teams-sovelluksessa, sinun on otettava ilmoitukset käyttöön Human Resources -sovelluksessa.

>[!NOTE]
>Vain Teamsiin kirjautuneet käyttäjät, jotka käyttävät Human Resourcesin Teams-sovellusta, vastaanottavat ilmoituksia.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Linkit**.

3. Valitse **Asetukset**-kohdassa **Järjestelmäparametrit**.

4. Määritä **Yleistä**-välilehdessä **Ota käyttöön Teams-sovelluksen ilmoitukset** -kohdan arvoksi **Kyllä**.

   ![Teams-sovelluksen ilmoitusten käyttöönotto järjestelmäparametreissa](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Jos haluat ottaa Teams-ilmoitukset käyttöön kaikille käyttäjille, valitse **Kyllä** pyydettäessä.

   ![Teams-ilmoitusten käyttöönotto kaikille käyttäjille](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille

Kun olet ottanut ilmoitukset käyttöön Human Resourcesin Teams-sovelluksessa, voit ottaa ilmoitukset käyttöön tai poistaa ne käytöstä yksittäisille käyttäjille.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Linkit**.

3. **Valitse käyttäjät** -kohdasta **Käyttäjän asetukset**.

4. Valitse **Työnkulku**-välilehti.

5. Määritä **Teams-sovelluksen Salli ilmoitukset** -kohdan arvoksi **Kyllä**, jos haluat ottaa ilmoitukset käyttöön käyttäjälle. Valitse **Ei**, jos haluat poistaa käyttäjän ilmoitukset käytöstä.

   ![Teams-sovelluksen ilmoitusten käyttöönotto käyttäjän asetusten Työnkulku-välilehdessä](./media/hr-admin-teams-leave-app-notifications.png)

6. Valitse **Tallenna**.

## <a name="known-issues"></a>Tunnetut ongelmat

| Varasto-otto | Tila |
| --- | --- |
| Vaakasuuntainen vieritys ei toimi Android-puhelimissa | Vaakasuuntainen vieritys ei ole ongelma iOS- tai työpöytälaitteissa. Pyrimme korjaamaan asian Androidille. |
| Virhe: ongelma etsittäessä ympäristöä, johon muodostetaan yhteyttä. | Tämä virhe saattaa tulla näyttöön, vaikka olisit varmistanut, että käyttäjä voi käyttää yhtä tai useampaa henkilöstöresurssiympäristöä. Lisäksi et ehkä näe kaikkia odottamiasi ympäristöjä. Ennen kuin korjaat tämän ongelman, poista käyttäjä ja tuo ne sitten uudelleen, jotta ongelma voidaan ratkaista. |
| Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo. | Ennakointi ei ole vielä käytettävissä. Saldo näkyy kuluvalta päivältä. |
| **Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa. | Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun. |
| Saldotiedot lasketaan kuluvasta päivästä alkaen. | Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa. |

## <a name="privacy-notice"></a>Tietosuojatiedot

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoftin Language Understanding Intelligent Service (LUIS)

Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville. Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS). Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/). LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili). Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot. 

Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta. LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna. Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen. 

Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen. Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a>Microsoft Azuren tapahtumaruudukko ja Microsoft Teams

Kun Dynamics 365 Human Resources -sovelluksen ilmoitusominaisuus on käytössä Teamsissa, tietyt asiakastiedot siirtyvät sen maantieellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään. Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille. Näitä tietoja voidaan tallentaa enintään 24 tunnin ajan. Tiedot käsitellä Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.

## <a name="see-also"></a>Lisätietoja 

[Microsoft Teamsin lataaminen ja asentaminen](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teamsin ohje- ja tukikeskus](https://support.office.com/teams)</br>
[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md)

