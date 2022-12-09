---
title: Lomapyyntöjen hallinta Teamsissa
description: Tässä artikkelissa käsitellään poissaolopyyntöjä Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa.
author: twheeloc
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 84f1190301e67b49535530f85784561b2e51a2df
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812156"
---
# <a name="manage-leave-requests-in-teams"></a>Lomapyyntöjen hallinta Teamsissa

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa. Voit käyttää bottia pyytääksesi tietoja ja aloittaaksesi lomapyynnön. **Poissaolo**-välilehdessä on lisätietoja. Voit myös lähettää ihmisille tietoja tulevista poissaoloista Teamsissa ja keskusteluissa Human Resources -sovelluksen ulkopuolella.

## <a name="install-the-app"></a>Sovelluksen asentaminen

Löydät Dynamics 365 Human Resources -sovelluksen Teams-kaupasta.

1. Siirry Microsoft Teamsissa sovellusluetteloon.
 
2. Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.

> [!NOTE]
> 20.12.2021 jälkeen Microsoftin vuokraajassa isännöidyt Human Resources App -bottipalvelut (versio 1.1.4) poistetaan käytöstä. Ajan tasalla oleva laajennus (versio 1.1.5) voidaan asentaa. Lisätietoja on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-admin-teams-leave-app.md#update-app).

3. Asenna sovellus valitsemalla **Lisää**-painike.

Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.

> [!NOTE]
> Jos kirjautumisikkuna ei ole näkyvissä, päivitä selaimen asetukset sallimaan ponnahdusikkunat. 

Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.

> [!NOTE]
> Sovellus tukee nyt järjestelmänvalvojan käyttöoikeusroolia.
 
## <a name="use-the-bot"></a>Botin käyttö

Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.

> [!NOTE]
> Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä. Jos kirjautumisikkuna ei ole näkyvissä, päivitä selaimen asetukset sallimaan ponnahdusikkunat.

Botilta voi pyytää seuraavia:

- Tarkastele nykyisiä lomasaldoja. Lähetä esimerkiksi sanoma, jossa sanotaan "Näytä lomasaldot".

- Lomapyynnön käynnistäminen käyttäjän puolesta. Lähetä esimerkiksi viesti Pidä vapaata tai Haluan pitää vapaata ensi torstaina ja perjantaina, jotta voit tarkemmin kysyä vapaata poissaolon lomatyypille. 

  ![Lomapyynnön käynnistäminen Teams-keskustelussa.](./media/hr-teams-leave-app-initiate.png)

- Keskustelubotti täyttää lomapyynnön puolestasi. Valitse **Pyydä vapaata** ja muokkaa pyyntösi tietoja.

   Jos haluat lähettää useita lomatyyppejä koskevat lomapyynnöt samana päivänä, valitse **Lisäasetukset**-valikosta **Jaa päivä**. 

   Jos valitset puoli päivää lomaa, kun pyynnön yksikkö on päiviä, voit määrittää, haluatko pyytää aamupäivän vai iltapäivän vapaata, valitsemalla **Lisäasetukset**-valikosta **Puoli päivää** -määritysvaihtoehdon.
   
   ![Puolen päivän määritelmät.](./media/HalfDayDefinitions.png)

- Kun olet muokannut lomapyyntösi tietoja, lähetä se hyväksyttäväksi valitsemalla **Lähetä**.

  ![Lomapyynnön lähettäminen.](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a>Lomien ja poissaolojen hallinta Teamsissa

**Poissaolo**-välilehdessä voi tarkastella seuraavia: 

- Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity

- Tulevat lomapyynnöt

- Poissaolopyynnöt

- Lomapyyntöluonnokset
 
### <a name="create-a-new-request"></a>Uuden pyynnön luominen

1. Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.

2. Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen.](./media/TimeOffHours.png)

3. Anna tarvittaessa syykoodi. Lisää myös mahdolliset kommentit ja liitteet.

4. Valitse **Jaa päivä** -vaihtoehto **Lisäasetukset** -valikosta, jos haluat lähettää useita lomapyyntömerkintöjä samalle päivälle eri lomalajeille.

5. Valitse **Puoli päivää -määritys**-vaihtoehto, kun haluat määrittää, haluatko pyytää aamupäivän vai iltapäivän vapaata. Tämä vaihtoehto on käytettävissä, kun lomapyynnön yksikkö on päivinä ja pyydetty määrä on 0,5 päivää.

6. Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi valitsemalla **Lähetä**. Jos haluat palata pyyntöön, voit syöttää **Tallenna luonnoksena**.

### <a name="manage-draft-requests"></a>Pyyntöluonnosten hallinta

1. Valitse **Luonnokset**-välilehti.

2. Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.

3. Tee tarvittavat muutokset. Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**. Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.
   
### <a name="respond-to-teams-notifications"></a>Teams-ilmoituksiin vastaaminen

Kun lomapyyntöjen lähetysten hyväksyjänä olet sinä tai vaihtoehtoisesti työntekijä, saat ilmoituksen Teamsin Human Resources -sovellukseen. Voit tarkastella ilmoitusta valitsemalla lomapyynnön. Ilmoitukset näkyvät myös **Keskustelu**-alueella.

Jos olet hyväksyjä, voit valita ilmoituksessa **Hyväksy** tai **Hylkää**. Voit myös määrittää valinnaisen sanoman.

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a>Tulevien poissaolotietojen lähettäminen työtovereille

Kun olet asentanut Teamsin Human Resources -sovelluksen, voit lähettää työtovereillesi helposti tietoja tulevista poissaoloistasi ryhmissä tai keskusteluissa.

1. Valitse ryhmässä tai Teams-keskustelussa Human Resources -painike keskusteluikkunan alapuolella.

   ![Human Resources -painike keskusteluikkunan alla.](./media/hr-teams-leave-app-chat-button.png)

2. Valitse jaettava lomapyyntö. Jos haluat jakaa lomapyyntöluonnoksen, valitse ensin **Luonnokset**.

Lomapyyntösi tulee näkyviin keskustelussa.

Jos olet jakanut pyyntöluonnoksen, se tulee näkyviin luonnoksena.

## <a name="view-your-teams-leave-calendar"></a>Ryhmän lomakalenterin tarkasteleminen

Jos olet esimies, jolla on suoria alaisia, voit tarkastella ryhmän hyväksyttyä ja hyväksyntää odottavia poissaoloja.

1. Valitse Teamsin Human Resources -sovelluksessa **Poissaolo**.

2. Valitse **Ryhmän kalenteri**. Kalenterissa näkyvät suorien alaisten hyväksytyt ja hyväksyntää odottavat poissaolot.

   > [!NOTE]
   > Jos et näe ryhmäkalenteria, pyydä järjestelmänvalvojaasi ottamaan se käyttöön. Lisätietoja on kohdassa [Asentaminen ja määrittäminen](hr-admin-teams-leave-app.md#install-and-setup).

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

## <a name="troubleshooting"></a>Vianmääritys

Jos sinulla on vaikeuksia Dynamics 365 Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä. Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen. Lisätietoja on kohdassa [Pyydä tukea](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a>Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa

Jos et voi kirjautua sovellukseen, Microsoft Teamsiin kirjautumiseen käytettyä tiliä ei ehkä ole liitetty työntekijätietueeseen Dynamics 365 Human Resourcesissa. Ota yhteys järjestelmänvalvojaan ja varmista, että työntekijätietue on liitetty oikein.

### <a name="cant-find-the-dynamics-365-human-resources-environment-in-settings"></a>Dynamics 365 Human Resources -ympäristöä ei löydy asetuksista

Jos et voi valita oikeaa Dynamics 365 -ympäristöä, käyttäjätietuetta ei ehkä ole synkronoitu oikein. Ota yhteyttä järjestelmänvalvojaan, jos haluat luoda käyttäjätietueen uudelleen ja liittää sen käyttäjän tunnistetietoihin. Yritä sitten kirjautua Human Resources -sovellukseen Microsoft Teamsille muutaman minuutin kuluttua.

### <a name="translations-dont-display-correctly"></a>Käännökset eivät näy oikein

Jos käännökset eivät näy odotetulla tavalla, varmista, että Teamsissa valitsemasi kieli vastaa Human Resources -sovelluksen **Käyttäjän asetukset** -osiossa valittua kieltä.

Tarkasta Teamsissa **Sovelluksen kieli** -asetus **Asetukset**-osiosta.

![Teams-asetukset.](./media/hr-teams-leave-app-settings.png)

Valitse Human Resources -sovelluksesta **Asetukset** ja sitten **Käyttäjän asetukset**. Varmista, että **Kieli**-kenttä vastaa Teamsin **Sovelluksen kieli** -kenttää.

![Human Resources -sovelluksen Käyttäjän asetukset -osio.](./media/hr-teams-leave-app-user-options.png)

Jos sinulla edelleen ilmenee käännöksiin liittyviä ongelmia, kerro niistä meille. Lisätietoa on kohdassa [Talous- ja toimintosovellusten tai Lifecycle Servicesin (LCS) tuen hakeminen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a>Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa

Jos saat virheilmoituksen, kun yrität hyväksyä lomapyyntöjä Teams-sovelluksessa, yritä tehdä seuraava vianmääritys:

1. Tarkista, että tili, jolla kirjaudut Microsoft Teamsiin, on sama kuin se, jolla käytät Dynamics 365 Human Resourcesia.

2. Tarkista myös, että saat hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa. Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a>Lomien hyväksyjät eivät saa Teams-keskustelusanomia lomapyyntöjen hyväksymistä varten

1. Varmista, että ympäristö- ja käyttäjäilmoitukset ovat käytössä. Lisätietoa on kohdissa [Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).

2. Varmista, että käyttäjät ovat kirjautuneet **Keskustelut**-välilehteen samoilla tunnistetiedoilla, kuin mitä he käyttävät lomapyyntöjen hyväksymisessä. Käytä viestejä "kirjaudu ulos" ja sitten "kirjaudu sisään" kirjautuaksesi sisään oikeilla tunnistetiedoilla.

3. Jos ongelma jatkuu, tarkista **Liiketoimintatapahtumat -järjestelmän** erätyön tila järjestelmänvalvojana. Jos se on **Odotetaan**- tai **Suoritetaan**-vaiheessa, tarkista uudelleen muutaman minuutin kuluttua. Jos tila ei muutu, kirjaa tukipalvelupyyntö, jotta tiimimme voi auttaa korjaamaan ongelman.

## <a name="known-accessibility-issues"></a>Tunnetut helppokäyttöisyyteen liittyvät ongelmat

Teamsin Human Resources -sovellus sisältää seuraavat käytettävyysongelmat. Ne pyritään korjaamaan tulevissa versioissa.

| Varasto-otto | Ratkaisuehdotus tai selitys |
| --- | --- |
| Työpöydän suurentaminen käyttämällä 400 %:n zoomausta piilottaa jotkin näkymän toimintopainikkeet. | Suosittelemme suurennuslasin käyttöä siihen asti, kunnes tämän zoomaustason tuki on käytettävissä. |
| **Poissaolo**-välilehdessä VoiceOver-toiminto ilmoittaa painiketoiminnosta, kun poissaoloruudukon otsikkoa luetaan. | Ruudukon otsikko ja elementit ryhmitellään vuoden mukaan, ja ne voidaan tiivistää. VoiceOver tulkitsee tämän esityksen toimintaa ohjaavaksi kohteeksi, vaikka näin ei ole. |
| **Poissaolo**-välilehdessä on ylimääräinen sipaisuele siirryttäessä uuden pyynnön **Syykoodi**-kohtaan. | Piilotettua ohjausobjektia, jota sipaisulla siirtyminen yrittää käyttää, ei ole. |
| Jos sipaiset **Poissaolo**-välilehdessä kalenterin ollessa auki, näkymä siirtyy ohjausobjektin ulkopuolelle uuden pyynnön yläosan tai pyynnön muokkauksen sijaan. | Kun käyttäjä on kohdassa **Siirry tähän päivään**, tätä pidetään ohjausobjektin päättymisenä. Näkymä siirtyy takaisin yläosaan sipaisemalla vastakkaiseen suuntaan. |
| **Keskustelu**-välilehdessä kohdistus siirtyy takaisin alkuun, jossa syötettiin päivämäärä käyttöä helpottavan työkalun tai näppäimistön siirtymistoiminnon avulla. | Siirry käyttämällä sarkainta, kunnes olet jälleen syöttöalueella. |

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
[Teamsin Human Resources -sovellus](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

