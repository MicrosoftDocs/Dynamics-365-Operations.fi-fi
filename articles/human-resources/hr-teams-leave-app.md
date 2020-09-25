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
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="a6533-103">Loma- ja poissaolopyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="a6533-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a6533-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="a6533-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="a6533-105">Voit pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="a6533-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="a6533-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="a6533-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="a6533-107">Sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="a6533-107">Install the app</span></span>

<span data-ttu-id="a6533-108">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="a6533-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="a6533-109">Valitse Microsoft Teamsissa kolme pistettä.</span><span class="sxs-lookup"><span data-stu-id="a6533-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teamsin lomasovelluksen kolme pistettä](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="a6533-111">Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="a6533-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teamsin lomasovelluksen HR-ruutu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="a6533-113">Asenna sovellus valitsemalla **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="a6533-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teamsin lomasovelluksen asennus](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="a6533-115">Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a6533-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teamsin lomasovelluksen Asetukset-välilehti](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="a6533-117">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="a6533-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="a6533-118">Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="a6533-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="a6533-119">Sovellus ei tällä hetkellä tue järjestelmänvalvojan käyttöoikeusroolia ja näkyviin tulee virhesanoma, jos kirjautumiseen käytetään järjestelmävalvojan tiliä.</span><span class="sxs-lookup"><span data-stu-id="a6533-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="a6533-120">Kirjautumiseen käytettävän tilin voi vaihtaa valitsemalla **Asetukset**-välilehdessä **Vaihda tiliä** -painikkeen, jonka jälkeen kirjautumiseen voi käyttää käyttäjätiliä, jolla ei ole järjestelmänvalvojan käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="a6533-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="a6533-121">Botin käyttö</span><span class="sxs-lookup"><span data-stu-id="a6533-121">Use the bot</span></span>

<span data-ttu-id="a6533-122">Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="a6533-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams -lomasovelluksen botin tervehdyssanoma](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="a6533-124">Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="a6533-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="a6533-125">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="a6533-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="a6533-126">Botilta voi pyytää seuraavia:</span><span class="sxs-lookup"><span data-stu-id="a6533-126">You can ask the bot to:</span></span>

- <span data-ttu-id="a6533-127">Jokaisen sellaisen poissaolotyypin poissaolosaldon tietojen näyttäminen, johon kysyjä on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="a6533-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teamsin lomasovelluksen saldon näyttäminen](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="a6533-129">Tietyn lomatyypin lisätietojen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="a6533-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teamsin lomasovelluksen tietojen näyttäminen](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="a6533-131">Lomapyynnön käynnistäminen käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="a6533-131">Start a leave request for you.</span></span>

   ![Human Resources Teamsin lomasovelluksen lomapyyntö](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="a6533-133">Kun olet jättänyt lomapyynnön, voit muuttaa päiviä kortin sisällä.</span><span class="sxs-lookup"><span data-stu-id="a6533-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teamsin lomasovelluksen muokkauspyyntö](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="a6533-135">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="a6533-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="a6533-136">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="a6533-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teamsin lomasovelluksen pyynnön lähetys](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="a6533-138">Lomien ja poissaolojen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="a6533-138">Manage your leave in Teams</span></span>

<span data-ttu-id="a6533-139">**Poissaolo**-välilehdessä voi tarkastella seuraavia:</span><span class="sxs-lookup"><span data-stu-id="a6533-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="a6533-140">Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity</span><span class="sxs-lookup"><span data-stu-id="a6533-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="a6533-141">Tulevat lomapyynnöt</span><span class="sxs-lookup"><span data-stu-id="a6533-141">Upcoming leave requests</span></span>

- <span data-ttu-id="a6533-142">Poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="a6533-142">Time-off requests</span></span>

- <span data-ttu-id="a6533-143">Lomapyyntöluonnokset</span><span class="sxs-lookup"><span data-stu-id="a6533-143">Draft leave requests</span></span>

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="a6533-145">Uuden pyynnön luominen</span><span class="sxs-lookup"><span data-stu-id="a6533-145">Create a new request</span></span>

1. <span data-ttu-id="a6533-146">Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="a6533-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teamsin lomasovelluksen uusi pyyntö](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="a6533-148">Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="a6533-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="a6533-150">Anna tarvittaessa syykoodi.</span><span class="sxs-lookup"><span data-stu-id="a6533-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="a6533-151">Lisää myös mahdolliset kommentit ja liitteet.</span><span class="sxs-lookup"><span data-stu-id="a6533-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="a6533-152">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="a6533-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a6533-153">Jos haluat palata pyyntöön, voit kirjoittaa **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="a6533-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="a6533-154">Pyyntöluonnosten hallinta</span><span class="sxs-lookup"><span data-stu-id="a6533-154">Manage draft requests</span></span>

1. <span data-ttu-id="a6533-155">Valitse **Luonnokset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a6533-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teamsin lomasovelluksen Luonnokset-välilehti](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="a6533-157">Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.</span><span class="sxs-lookup"><span data-stu-id="a6533-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="a6533-158">Tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="a6533-158">Make any necessary changes.</span></span> <span data-ttu-id="a6533-159">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="a6533-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="a6533-160">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="a6533-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teamsin lomasovelluksen luonnoksen muokkaus](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="teams-notifications"></a><span data-ttu-id="a6533-162">Teams-ilmoitukset</span><span class="sxs-lookup"><span data-stu-id="a6533-162">Teams notifications</span></span>

<span data-ttu-id="a6533-163">Kun lomapyyntöjen lähetysten hyväksyjänä olet sinä tai vaihtoehtoisesti työntekijä, saat ilmoituksen Teamsin Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="a6533-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="a6533-164">Voit tarkastella ilmoitusta valitsemalla sen.</span><span class="sxs-lookup"><span data-stu-id="a6533-164">You can select the notification to view it.</span></span> <span data-ttu-id="a6533-165">Ilmoitukset näkyvät myös **Keskustelu**-alueella.</span><span class="sxs-lookup"><span data-stu-id="a6533-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="a6533-166">Jos olet hyväksyjä, voit valita ilmoituksessa **Hyväksy** tai **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="a6533-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="a6533-167">Voit myös määrittää valinnaisen sanoman.</span><span class="sxs-lookup"><span data-stu-id="a6533-167">You can also provide an optional message.</span></span>

![Human Resourcesin Teams-sovelluksen lomapyynnön ilmoitus](./media/hr-teams-leave-app-notification.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="a6533-169">Ryhmän lomakalenterin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="a6533-169">View your team's leave calendar</span></span>

<span data-ttu-id="a6533-170">Jos olet esimies, jolla on suoria alaisia, voit tarkastella ryhmän hyväksyttyä ja hyväksyntää odottavia poissaoloja.</span><span class="sxs-lookup"><span data-stu-id="a6533-170">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="a6533-171">Valitse Teamsin Human Resources -sovelluksessa **Poissaolo**.</span><span class="sxs-lookup"><span data-stu-id="a6533-171">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="a6533-172">Valitse **Ryhmän kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="a6533-172">Select **Team calendar**.</span></span>

   ![Human Resourcesin Teams-sovelluksen tarkasteleminen](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="a6533-174">Kalenterissa näkyvät suorien alaisten hyväksytyt ja hyväksyntää odottavat poissaolot.</span><span class="sxs-lookup"><span data-stu-id="a6533-174">The calendar displays your direct reports' approved and pending time off.</span></span>

![Human Resourcesin Teams-sovelluksen poissaolokalenteri](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="a6533-176">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="a6533-176">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a6533-177">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a6533-177">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a6533-178">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="a6533-178">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a6533-179">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a6533-179">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a6533-180">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a6533-180">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a6533-181">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="a6533-181">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a6533-182">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="a6533-182">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a6533-183">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="a6533-183">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a6533-184">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="a6533-184">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a6533-185">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="a6533-185">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a6533-186">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="a6533-186">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a6533-187">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a6533-187">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a6533-188">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a6533-188">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="a6533-189">Microsoft Azuren tapahtumaruudukko ja Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a6533-189">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="a6533-190">Kun Dynamics 365 Human Resources -sovelluksen ilmoitusominaisuus on käytössä Teamsissa, tietyt asiakastiedot siirtyvät sen maantieellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="a6533-190">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="a6533-191">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="a6533-191">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a6533-192">Näitä tietoja voidaan tallentaa enintään 24 tunnin ajan. Tiedot käsitellä Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="a6533-192">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a6533-193">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a6533-193">See also</span></span>

[<span data-ttu-id="a6533-194">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="a6533-194">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a6533-195">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="a6533-195">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a6533-196">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="a6533-196">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
