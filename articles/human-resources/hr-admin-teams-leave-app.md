---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: debb18ab85e5b9011166a73571533a84d3f53512
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717080"
---
# <a name="human-resources-app-in-teams"></a>Teamsin Human Resources -sovellus


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa. Työntekijät voivat pyytää tietoja botin avustuksella. **Poissaolo**-välilehdessä on lisätietoja. Lisäksi lähettää tietoja tulevista poissaoloista voidaan lähettää ryhmissä ja keskusteluissa Human Resources -sovelluksen ulkopuolella.

![Human Resources Teamsin lomasovelluksen botti.](./media/hr-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti.](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resourcesin lomapyyntökortti.](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a>Asentaminen ja määrittäminen

Löydät Dynamics 365 Human Resources -sovelluksen Teams-kaupasta. Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).

Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](/MicrosoftTeams/teams-app-permission-policies).

Jos haluat käyttäjien näkevän loma- ja poissaolokalenterin sovelluksessa, sinun on täytyy ottaa **Loma- ja poissaolokalenteri Teamsissa** -ominaisuus käyttöön ominaisuuksien hallinnasta. Lisätietoja ominaisuuksien käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).

## <a name="update-app"></a>Päivitä sovellus
>[!NOTE]
> 20.12.2021 jälkeen Microsoftin vuokraajassa isännöidyt Human Resources App -bottipalvelut poistetaan käytöstä. Ajan tasalla olevaan laajennukseen (versio tai 1.1.5), joka voidaan asentaa, tämä ei vaikuta. Tärkein vaikutus on vanhentuneeseen laajennukseen (versio 1.1.4). Tämän version keskustelubotti lopettaa toiminnan. **Poissaolo**-välilehti toimii edelleen molemmissa laajennuksissa.

Versiossa 1.1.4 keskustelubotti lopettaa vastaamisen mihin tahansa sanomaan. Voit esimerkiksi **kirjautua sisään**, **tarkastella saldoja** ja **tarkastella poissaoloja**. Sovellus on päivitettävä manuaalisesti uusimpaan versioon. Lisätietoja on kohdassa [Sovellusten päivitys Microsoft Teamsissa](/MicrosoftTeams/apps-update-experience).

Päivitä versioon 1.1.5 seuraavasti:
1. Siirry Microsoft Teamsissa kohtaan **Sovellukset**.
2. Etsi **Human Resources** -sovellus.
3. Valitse **Päivitä**.

Voit tarkistaa Human Resources -sovelluksen version joko **Tietoja**-välilehdestä tai **Henkilökohtainen sovellus** -osasta.  

![Human Resourcesin **Tietoja**-välilehti.](./media/HR-teams-about.png)

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a>Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa

Jos haluat, että käyttäjät voivat vastaanottaa lomapyyntöjen ilmoituksia Teams-sovelluksessa, sinun täytyy ottaa ilmoitukset käyttöön Dynamics 365 Human Resources -sovelluksessa.

>[!NOTE]
>Vain Teamsiin kirjautuneet käyttäjät, jotka käyttävät Dynamics 365 Human Resources Teams -sovellusta, vastaanottavat ilmoituksia.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Linkit**.

3. Valitse **Asetukset**-kohdassa **Järjestelmäparametrit**.

4. Määritä **Yleistä**-välilehdessä **Ota käyttöön Teams-sovelluksen ilmoitukset** -kohdan arvoksi **Kyllä**.

   ![Teams-sovelluksen ilmoitusten käyttöönotto järjestelmäparametreissa.](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. Jos haluat ottaa Teams-ilmoitukset käyttöön kaikille käyttäjille, valitse **Kyllä** pyydettäessä.

   ![Teams-ilmoitusten käyttöönotto kaikille käyttäjille.](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a>Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille

Kun olet ottanut ilmoitukset käyttöön Dynamics 365 Human Resources Teams -sovelluksessa, voit ottaa ilmoitukset käyttöön tai poistaa ne käytöstä yksittäisille käyttäjille.

1. Valitse Human Resourcesissa **Järjestelmän hallinta**.

2. Valitse **Linkit**.

3. **Valitse käyttäjät** -kohdasta **Käyttäjän asetukset**.

4. Valitse **Työnkulku**-välilehti.

5. Määritä **Teams-sovelluksen Salli ilmoitukset** -kohdan arvoksi **Kyllä**, jos haluat ottaa ilmoitukset käyttöön käyttäjälle. Valitse **Ei**, jos haluat poistaa käyttäjän ilmoitukset käytöstä.

   ![Teams-sovelluksen ilmoitusten käyttöönotto käyttäjän asetusten Työnkulku-välilehdessä.](./media/hr-admin-teams-leave-app-notifications.png)

6. Valitse **Tallenna**.

## <a name="supported-languages"></a>Tuetut kielet

Teamsin Dynamics 365 Human Resources -sovellus tukee seuraavia kieliä:

| Kielialueen tunnus | Kieli |
| --- | --- |
| de-DE | saksa (Saksa) |
| es-ES | espanja (Espanja) |
| es-MX | espanja (Meksiko) |
| fr-CA | ranska (Kanada) |
| fr-FR | ranska (Ranska) |
| it-IT | italia (Italia) |
| nl-NL | hollanti (Alankomaat) |
| pt-BR | portugali (Brasilia) |
| tr-TR | turkki (Turkki) |
| zh-CN | kiina (yksinkertaistettu) |

## <a name="notes"></a>Muistiinpanot

Seuraavat työnimikkeet on ajoitettu tulevia julkaisuja varten:

| Työnimike | Tila |
| --- | --- |
| Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo. | Ennakointi ei ole vielä käytettävissä. Saldo näkyy kuluvalta päivältä. |
| **Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa. | Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun. |
| Saldotiedot lasketaan kuluvasta päivästä alkaen. | Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty **Loma- ja poissaoloparametrit** -sivulla. |

## <a name="troubleshooting"></a>Vianmääritys

Jos käyttäjällä on vaikeuksia Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä. Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen. Lisätietoja on kohdassa [Pyydä tukea](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="ensure-the-teams-human-resources-application-is-up-to-date"></a>Varmista, että Teamsin Human Resources -sovellus on ajan tasalla
Jos Teamsin Human Resources -sovelluksessa ilmenee ongelmia, sinun on vahvistettava, että käytössä on viimeisin versio. Tuettu vähimmäisversio on 1.1.5. Lisätietoja Teams-sovelluksen päivittämisestä on [Teamsin ohjeissa](/MicrosoftTeams/apps-update-experience).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa

Jos käyttäjä ottaa yhteyttä, koska hän ei pysty kirjautumaan sovellukseen, tarkista, että hänellä on työntekijätietue Human Resourcesissa.

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa

Jos käyttäjä saa virheilmoituksen yrittäessään hyväksyä lomapyyntöjä Teams-sovelluksessa, kokeile seuraavaa vianmääritystä:

1. Tarkista, että käyttäjän Teams-tili on sama tili, jolla käyttäjä käyttää Human Resourcesiin.

2. Tarkista myös, että käyttäjä saa hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa. Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Lomien hyväksyjät eivät saa Teams-keskustelusanomia lomapyyntöjen hyväksymistä varten

1. Varmista, että ympäristö- ja käyttäjäilmoitukset ovat käytössä. Lisätietoa on kohdissa [Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Varmista, että käyttäjät ovat kirjautuneet **Keskustelut**-välilehteen samoilla tunnistetiedoilla, kuin mitä he käyttävät lomapyyntöjen hyväksymisessä. Käytä viestejä "kirjaudu ulos" ja sitten "kirjaudu sisään" kirjautuaksesi sisään oikeilla tunnistetiedoilla.

3. Jos ongelma jatkuu, tarkista **Liiketoimintatapahtumat -järjestelmän** erätyön tila järjestelmänvalvojana. Jos se on **Odotetaan**- tai **Suoritetaan**-vaiheessa, tarkista uudelleen muutaman minuutin kuluttua. Jos tila ei muutu, kirjaa tukipalvelupyyntö, jotta tiimimme voi auttaa korjaamaan ongelman.

## <a name="privacy-notice"></a>Tietosuojatiedot

### <a name="microsoft-language-understanding-intelligent-service-luis"></a>Microsoftin Language Understanding Intelligent Service (LUIS)

Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville. Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS). Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/). LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili). Nämä tiedot välitetään sitten Microsoftin  [Azure Bot Frameworkiin](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.

Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta. LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna. Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure Bot Frameworkiin. 

Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen. Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/). 

Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a>Microsoft Teams, Azure-tapahtumaverkko ja Azure Cosmos DB

Kun Dynamics 365 Human Resources -sovellus on käytössä Microsoft Teamsissa, tietyt asiakastiedot voivat siirtyä sen maantieteellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.

Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille. Näitä tietoja voidaan tallentaa Microsoft Azure -tapahtumaverkossa enintään 24 tunnin ajan. Tiedot käsitellään Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa. Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).

Keskusteltaessa Human Resources -sovelluksen keskustelubotin kanssa keskustelun sisältö saatetaan tallentaa Azuren Cosmos DB:hen ja lähettää Microsoft Teamsiin. Nämä tiedot voidaan tallentaa Azuren Cosmos DB:hen enintään 24 tunniksi, ja niitä voidaan käsitellä sen maantieteellisen alueen ulkopuolella, jossa vuokralaisen Human Resources -palvelu on otettu käyttöön. Tiedot salataan siirrettäessä ja levossa, eikä Microsoft tai sen alihankkija käytä niitä koulutuksiin tai palvelujen parantamiseen. Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).
 
Ohjeet Human Resources -sovelluksen käyttöoikeuksien rajoittamiseen Microsoft Teamsissä organisaatiosi tai sen käyttäjien osalta: [Sovellusten oikeuskäytäntöjen hallinta Microsoft Teamsissä](/MicrosoftTeams/teams-app-permission-policies).

## <a name="see-also"></a>Lisätietoja 

[Microsoft Teamsin lataaminen ja asentaminen](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[Microsoft Teamsin ohje- ja tukikeskus](https://support.office.com/teams)</br>
[Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
