---
title: Loma- ja poissaolopyyntöjen hallinta Teamsissa
description: Tässä ohjeaiheessa käsitellään poissaolopyyntöjä Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 67501a1fa65493a1a23eb6176ece5be98d6e4659
ms.sourcegitcommit: 7fc0726c0a93ce6f4dafaad3232b4687f61cdc88
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/21/2020
ms.locfileid: "3393005"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="78723-103">Loma- ja poissaolopyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="78723-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="78723-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="78723-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="78723-105">Voit pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="78723-105">You can interact with a bot to request information.</span></span> <span data-ttu-id="78723-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="78723-106">The **Time off** tab provides more detailed information.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="78723-107">Sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="78723-107">Install the app</span></span>

<span data-ttu-id="78723-108">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="78723-108">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="78723-109">Valitse Microsoft Teamsissa kolme pistettä.</span><span class="sxs-lookup"><span data-stu-id="78723-109">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teamsin lomasovelluksen kolme pistettä](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="78723-111">Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="78723-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teamsin lomasovelluksen HR-ruutu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="78723-113">Asenna sovellus valitsemalla **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="78723-113">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teamsin lomasovelluksen asennus](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="78723-115">Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="78723-115">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teamsin lomasovelluksen Asetukset-välilehti](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="78723-117">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="78723-117">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="78723-118">Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="78723-118">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!WARNING]
> <span data-ttu-id="78723-119">Sovellus ei tällä hetkellä tue järjestelmänvalvojan käyttöoikeusroolia ja näkyviin tulee virhesanoma, jos kirjautumiseen käytetään järjestelmävalvojan tiliä.</span><span class="sxs-lookup"><span data-stu-id="78723-119">The app doesn't currently support the System Administrator security role, and will display an error message if you sign in with a System Administrator account.</span></span> <span data-ttu-id="78723-120">Kirjautumiseen käytettävän tilin voi vaihtaa valitsemalla **Asetukset**-välilehdessä **Vaihda tiliä** -painikkeen, jonka jälkeen kirjautumiseen voi käyttää käyttäjätiliä, jolla ei ole järjestelmänvalvojan käyttöoikeuksia.</span><span class="sxs-lookup"><span data-stu-id="78723-120">To sign in with a different account, on the **Settings** tab, select the **Switch accounts** button, and then sign in with a user account that doesn’t have System Administrator privileges.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="78723-121">Botin käyttö</span><span class="sxs-lookup"><span data-stu-id="78723-121">Use the bot</span></span>

<span data-ttu-id="78723-122">Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="78723-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams -lomasovelluksen botin tervehdyssanoma](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="78723-124">Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="78723-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="78723-125">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="78723-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="78723-126">Botilta voi pyytää seuraavia:</span><span class="sxs-lookup"><span data-stu-id="78723-126">You can ask the bot to:</span></span>

- <span data-ttu-id="78723-127">Jokaisen sellaisen poissaolotyypin poissaolosaldon tietojen näyttäminen, johon kysyjä on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="78723-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teamsin lomasovelluksen saldon näyttäminen](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="78723-129">Tietyn lomatyypin lisätietojen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="78723-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teamsin lomasovelluksen tietojen näyttäminen](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="78723-131">Lomapyynnön käynnistäminen käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="78723-131">Start a leave request for you.</span></span>

   ![Human Resources Teamsin lomasovelluksen lomapyyntö](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="78723-133">Kun lomapyyntö on käynnistetty, päiviä voi muuttaa kortissa. Pyyntöön voi lisätä lisätietoja valitsemalla **Muokkaa tietoja**.</span><span class="sxs-lookup"><span data-stu-id="78723-133">After you start a leave request, you can adjust the days right within the card, or you can select **Edit details** to add additional information to your request.</span></span>

![Human Resources Teamsin lomasovelluksen muokkauspyyntö](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="78723-135">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="78723-135">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="78723-136">Jos haluat palata pyyntöön, voit kirjoittaa **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="78723-136">You can also type **Save as draft** to come back to it later.</span></span>

![Human Resources Teamsin lomasovelluksen pyynnön lähetys](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="78723-138">Lomien ja poissaolojen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="78723-138">Manage your leave in Teams</span></span>

<span data-ttu-id="78723-139">**Poissaolo**-välilehdessä voi tarkastella seuraavia:</span><span class="sxs-lookup"><span data-stu-id="78723-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="78723-140">Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity</span><span class="sxs-lookup"><span data-stu-id="78723-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="78723-141">Tulevat lomapyynnöt</span><span class="sxs-lookup"><span data-stu-id="78723-141">Upcoming leave requests</span></span>

- <span data-ttu-id="78723-142">Poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="78723-142">Time-off requests</span></span>

- <span data-ttu-id="78723-143">Lomapyyntöluonnokset</span><span class="sxs-lookup"><span data-stu-id="78723-143">Draft leave requests</span></span>

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="78723-145">Uuden pyynnön luominen</span><span class="sxs-lookup"><span data-stu-id="78723-145">Create a new request</span></span>

1. <span data-ttu-id="78723-146">Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="78723-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teamsin lomasovelluksen uusi pyyntö](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="78723-148">Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="78723-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="78723-150">Anna tarvittaessa syykoodi.</span><span class="sxs-lookup"><span data-stu-id="78723-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="78723-151">Lisää myös mahdolliset kommentit ja liitteet.</span><span class="sxs-lookup"><span data-stu-id="78723-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="78723-152">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="78723-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="78723-153">Jos haluat palata pyyntöön, voit kirjoittaa **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="78723-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="78723-154">Pyyntöluonnosten hallinta</span><span class="sxs-lookup"><span data-stu-id="78723-154">Manage draft requests</span></span>

1. <span data-ttu-id="78723-155">Valitse **Luonnokset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="78723-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teamsin lomasovelluksen Luonnokset-välilehti](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="78723-157">Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.</span><span class="sxs-lookup"><span data-stu-id="78723-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="78723-158">Tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="78723-158">Make any necessary changes.</span></span> <span data-ttu-id="78723-159">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="78723-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="78723-160">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="78723-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teamsin lomasovelluksen luonnoksen muokkaus](./media/hr-teams-leave-app-drafts-edit.png)
   
## <a name="privacy-notice"></a><span data-ttu-id="78723-162">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="78723-162">Privacy notice</span></span>

<span data-ttu-id="78723-163">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="78723-163">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="78723-164">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="78723-164">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="78723-165">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="78723-165">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="78723-166">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="78723-166">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="78723-167">Nämä tiedot välitetään sitten Microsoftin [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/) , joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="78723-167">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="78723-168">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="78723-168">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="78723-169">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="78723-169">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="78723-170">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="78723-170">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="78723-171">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="78723-171">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="78723-172">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="78723-172">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="78723-173">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="78723-173">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="78723-174">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="78723-174">See also</span></span>

[<span data-ttu-id="78723-175">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="78723-175">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="78723-176">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="78723-176">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="78723-177">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="78723-177">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
