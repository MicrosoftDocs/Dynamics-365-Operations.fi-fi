---
title: Loma- ja poissaolopyyntöjen hallinta Teamsissa
description: Tässä ohjeaiheessa käsitellään poissaolopyyntöjä Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fbf44fe35af3147fd5fb478b6cbfc5a5d0b109d
ms.sourcegitcommit: 5b620f670ac0f403a0fdcdeb9c3f970b163191ee
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/04/2020
ms.locfileid: "3766757"
---
# <a name="manage-leave-requests-in-teams"></a>Loma- ja poissaolopyyntöjen hallinta Teamsissa

[!include [banner](includes/preview-feature.md)]

Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa. Voit pyytää tietoja botin avustuksella. **Poissaolo**-välilehdessä on lisätietoja.

## <a name="install-the-app"></a>Sovelluksen asentaminen

Human Resources -sovellus löytyy Teams-kaupasta.

1. Valitse Microsoft Teamsissa kolme pistettä.

   ![Human Resources Teamsin lomasovelluksen kolme pistettä](./media/hr-teams-leave-app-ellipses.png)
 
2. Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.

   ![Human Resources Teamsin lomasovelluksen HR-ruutu](./media/hr-teams-leave-app-human-resources-tile.png)

3. Asenna sovellus valitsemalla **Lisää**-painike.

   ![Human Resources Teamsin lomasovelluksen asennus](./media/hr-teams-leave-app-in-store.png)

Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.

![Human Resources Teamsin lomasovelluksen Asetukset-välilehti](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat. 

Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.

> [!WARNING]
> Sovellus ei tällä hetkellä tue järjestelmänvalvojan käyttöoikeusroolia ja näkyviin tulee virhesanoma, jos kirjautumiseen käytetään järjestelmävalvojan tiliä. Kirjautumiseen käytettävän tilin voi vaihtaa valitsemalla **Asetukset**-välilehdessä **Vaihda tiliä** -painikkeen, jonka jälkeen kirjautumiseen voi käyttää käyttäjätiliä, jolla ei ole järjestelmänvalvojan käyttöoikeuksia.
 
## <a name="use-the-bot"></a>Botin käyttö

Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.

![Human Resources Teams -lomasovelluksen botin tervehdyssanoma](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä. Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.

Botilta voi pyytää seuraavia:

- Jokaisen sellaisen poissaolotyypin poissaolosaldon tietojen näyttäminen, johon kysyjä on rekisteröity.

   ![Human Resources Teamsin lomasovelluksen saldon näyttäminen](./media/hr-teams-leave-app-bot-balances.png)
 
- Tietyn lomatyypin lisätietojen näyttäminen.

   ![Human Resources Teamsin lomasovelluksen tietojen näyttäminen](./media/hr-teams-leave-app-bot-details.png)

- Lomapyynnön käynnistäminen käyttäjän puolesta.

   ![Human Resources Teamsin lomasovelluksen lomapyyntö](./media/hr-teams-leave-app-bot-request.png)
 
Kun olet jättänyt lomapyynnön, voit muuttaa päiviä kortin sisällä.

![Human Resources Teamsin lomasovelluksen muokkauspyyntö](./media/hr-teams-leave-app-bot-edit.png)
 
Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi valitsemalla **Lähetä**. Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.

![Human Resources Teamsin lomasovelluksen pyynnön lähetys](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a>Lomien ja poissaolojen hallinta Teamsissa

**Poissaolo**-välilehdessä voi tarkastella seuraavia:

- Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity

- Tulevat lomapyynnöt

- Poissaolopyynnöt

- Lomapyyntöluonnokset

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a>Uuden pyynnön luominen

1. Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.

   ![Human Resources Teamsin lomasovelluksen uusi pyyntö](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. Anna tarvittaessa syykoodi. Lisää myös mahdolliset kommentit ja liitteet.

4. Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**. Jos haluat palata pyyntöön, voit kirjoittaa **Tallenna luonnoksena**.

### <a name="manage-draft-requests"></a>Pyyntöluonnosten hallinta

1. Valitse **Luonnokset**-välilehti.

   ![Human Resources Teamsin lomasovelluksen Luonnokset-välilehti](./media/hr-teams-leave-app-drafts-tab.png)

2. Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.

3. Tee tarvittavat muutokset. Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**. Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.

   ![Human Resources Teamsin lomasovelluksen luonnoksen muokkaus](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a>Teams-ilmoitukset

Kun lomapyyntöjen lähetysten hyväksyjänä olet sinä tai vaihtoehtoisesti työntekijä, saat ilmoituksen Teamsin Human Resources -sovellukseen. Voit tarkastella ilmoitusta valitsemalla sen. Ilmoitukset näkyvät myös **Keskustelu**-alueella.

Jos olet hyväksyjä, voit valita ilmoituksessa **Hyväksy** tai **Hylkää**. Voit myös määrittää valinnaisen sanoman.

![Human Resourcesin Teams-sovelluksen lomapyynnön ilmoitus](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a>Ryhmän lomakalenterin tarkasteleminen

Jos olet esimies, jolla on suoria alaisia, voit tarkastella ryhmän hyväksyttyä ja hyväksyntää odottavia poissaoloja.

1. Valitse Teamsin Human Resources -sovelluksessa **Poissaolo**.

2. Valitse **Ryhmän kalenteri**.

   ![Human Resourcesin Teams-sovelluksen tarkasteleminen](./media/hr-teams-leave-app-view-calendar.png)

Kalenterissa näkyvät suorien alaisten hyväksytyt ja hyväksyntää odottavat poissaolot.

![Human Resourcesin Teams-sovelluksen poissaolokalenteri](./media/hr-teams-leave-app-calendar.png)

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
[Teamsin Human Resources -sovellus](hr-admin-teams-leave-app.md)
