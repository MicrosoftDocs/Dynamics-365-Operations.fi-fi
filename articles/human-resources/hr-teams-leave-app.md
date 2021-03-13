---
title: Loma- ja poissaolopyyntöjen hallinta Teamsissa
description: Tässä ohjeaiheessa käsitellään poissaolopyyntöjä Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
manager: tfehr
ms.date: 10/28/2020
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
ms.openlocfilehash: 342106ad09db3a5d9c2dec8ab18e824d70e0f6bf
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128158"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="3d913-103">Loma- ja poissaolopyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="3d913-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="3d913-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="3d913-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="3d913-105">Voit käyttää bottia pyytääksesi tietoja ja aloittaaksesi lomapyynnön.</span><span class="sxs-lookup"><span data-stu-id="3d913-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="3d913-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="3d913-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="3d913-107">Voit myös lähettää ihmisille tietoja tulevista poissaoloista ryhmissä ja keskusteluissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="3d913-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="3d913-108">Sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="3d913-108">Install the app</span></span>

<span data-ttu-id="3d913-109">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="3d913-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="3d913-110">Valitse Microsoft Teamsissa kolme pistettä.</span><span class="sxs-lookup"><span data-stu-id="3d913-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Human Resources Teamsin lomasovelluksen kolme pistettä](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="3d913-112">Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="3d913-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![Human Resources Teamsin lomasovelluksen HR-ruutu](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="3d913-114">Asenna sovellus valitsemalla **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="3d913-114">Select the **Add** button to install the app.</span></span>

   ![Human Resources Teamsin lomasovelluksen asennus](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="3d913-116">Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3d913-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Human Resources Teamsin lomasovelluksen Asetukset-välilehti](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="3d913-118">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="3d913-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="3d913-119">Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="3d913-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="3d913-120">Sovellus tukee nyt järjestelmänvalvojan käyttöoikeusroolia.</span><span class="sxs-lookup"><span data-stu-id="3d913-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="3d913-121">Botin käyttö</span><span class="sxs-lookup"><span data-stu-id="3d913-121">Use the bot</span></span>

<span data-ttu-id="3d913-122">Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="3d913-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Human Resources Teams -lomasovelluksen botin tervehdyssanoma](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="3d913-124">Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="3d913-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="3d913-125">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="3d913-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="3d913-126">Botilta voi pyytää seuraavia:</span><span class="sxs-lookup"><span data-stu-id="3d913-126">You can ask the bot to:</span></span>

- <span data-ttu-id="3d913-127">Jokaisen sellaisen poissaolotyypin poissaolosaldon tietojen näyttäminen, johon kysyjä on rekisteröity.</span><span class="sxs-lookup"><span data-stu-id="3d913-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Human Resources Teamsin lomasovelluksen saldon näyttäminen](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="3d913-129">Tietyn lomatyypin lisätietojen näyttäminen.</span><span class="sxs-lookup"><span data-stu-id="3d913-129">Show additional details about a specific leave type.</span></span>

   ![Human Resources Teamsin lomasovelluksen tietojen näyttäminen](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="3d913-131">Lomapyynnön käynnistäminen käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="3d913-131">Start a leave request for you.</span></span>

   ![Human Resources Teamsin lomasovelluksen lomapyyntö](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="3d913-133">Kun olet jättänyt lomapyynnön, voit muuttaa päiviä kortin sisällä.</span><span class="sxs-lookup"><span data-stu-id="3d913-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Human Resources Teamsin lomasovelluksen muokkauspyyntö](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="3d913-135">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="3d913-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="3d913-136">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="3d913-136">You can also select **Save as draft** to come back to it later.</span></span>

![Human Resources Teamsin lomasovelluksen pyynnön lähetys](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="3d913-138">Lomien ja poissaolojen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="3d913-138">Manage your leave in Teams</span></span>

<span data-ttu-id="3d913-139">**Poissaolo**-välilehdessä voi tarkastella seuraavia:</span><span class="sxs-lookup"><span data-stu-id="3d913-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="3d913-140">Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity</span><span class="sxs-lookup"><span data-stu-id="3d913-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="3d913-141">Tulevat lomapyynnöt</span><span class="sxs-lookup"><span data-stu-id="3d913-141">Upcoming leave requests</span></span>

- <span data-ttu-id="3d913-142">Poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="3d913-142">Time-off requests</span></span>

- <span data-ttu-id="3d913-143">Lomapyyntöluonnokset</span><span class="sxs-lookup"><span data-stu-id="3d913-143">Draft leave requests</span></span>

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="3d913-145">Uuden pyynnön luominen</span><span class="sxs-lookup"><span data-stu-id="3d913-145">Create a new request</span></span>

1. <span data-ttu-id="3d913-146">Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="3d913-146">To create a new leave request, select **New request**.</span></span>

   ![Human Resources Teamsin lomasovelluksen uusi pyyntö](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="3d913-148">Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="3d913-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="3d913-150">Anna tarvittaessa syykoodi.</span><span class="sxs-lookup"><span data-stu-id="3d913-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="3d913-151">Lisää myös mahdolliset kommentit ja liitteet.</span><span class="sxs-lookup"><span data-stu-id="3d913-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="3d913-152">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="3d913-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="3d913-153">Jos haluat palata pyyntöön, voit kirjoittaa **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="3d913-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="3d913-154">Pyyntöluonnosten hallinta</span><span class="sxs-lookup"><span data-stu-id="3d913-154">Manage draft requests</span></span>

1. <span data-ttu-id="3d913-155">Valitse **Luonnokset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="3d913-155">Select the **Drafts** tab.</span></span>

   ![Human Resources Teamsin lomasovelluksen Luonnokset-välilehti](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="3d913-157">Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.</span><span class="sxs-lookup"><span data-stu-id="3d913-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="3d913-158">Tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="3d913-158">Make any necessary changes.</span></span> <span data-ttu-id="3d913-159">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="3d913-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="3d913-160">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="3d913-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Human Resources Teamsin lomasovelluksen luonnoksen muokkaus](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="3d913-162">Teams-ilmoituksiin vastaaminen</span><span class="sxs-lookup"><span data-stu-id="3d913-162">Respond to Teams notifications</span></span>

<span data-ttu-id="3d913-163">Kun lomapyyntöjen lähetysten hyväksyjänä olet sinä tai vaihtoehtoisesti työntekijä, saat ilmoituksen Teamsin Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="3d913-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="3d913-164">Voit tarkastella ilmoitusta valitsemalla sen.</span><span class="sxs-lookup"><span data-stu-id="3d913-164">You can select the notification to view it.</span></span> <span data-ttu-id="3d913-165">Ilmoitukset näkyvät myös **Keskustelu**-alueella.</span><span class="sxs-lookup"><span data-stu-id="3d913-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="3d913-166">Jos olet hyväksyjä, voit valita ilmoituksessa **Hyväksy** tai **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="3d913-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="3d913-167">Voit myös määrittää valinnaisen sanoman.</span><span class="sxs-lookup"><span data-stu-id="3d913-167">You can also provide an optional message.</span></span>

![Human Resourcesin Teams-sovelluksen lomapyynnön ilmoitus](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="3d913-169">Tulevien poissaolotietojen lähettäminen työtovereille</span><span class="sxs-lookup"><span data-stu-id="3d913-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="3d913-170">Kun olet asentanut Teamsin Human Resources -sovelluksen, voit lähettää työtovereillesi helposti tietoja tulevista poissaoloistasi ryhmissä tai keskusteluissa.</span><span class="sxs-lookup"><span data-stu-id="3d913-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="3d913-171">Valitse ryhmässä tai Teams-keskustelussa Human Resources -painike keskusteluikkunan alapuolella.</span><span class="sxs-lookup"><span data-stu-id="3d913-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources -painike keskusteluikkunan alla](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="3d913-173">Valitse jaettava lomapyyntö.</span><span class="sxs-lookup"><span data-stu-id="3d913-173">Select the leave request you want to share.</span></span> <span data-ttu-id="3d913-174">Jos haluat jakaa lomapyyntöluonnoksen, valitse ensin **Luonnokset**.</span><span class="sxs-lookup"><span data-stu-id="3d913-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Jaettavan tulevan lomapyynnön valitseminen](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="3d913-176">Lomapyyntösi tulee näkyviin keskustelussa.</span><span class="sxs-lookup"><span data-stu-id="3d913-176">Your leave request will display in the chat.</span></span>

![Human Resourcesin lomapyyntökortti](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="3d913-178">Jos olet jakanut pyyntöluonnoksen, se tulee näkyviin luonnoksena:</span><span class="sxs-lookup"><span data-stu-id="3d913-178">If you shared a draft request, it will display as a draft:</span></span>

![Human Resourcesin lomapyyntöluonnoskortti](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="3d913-180">Ryhmän lomakalenterin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="3d913-180">View your team's leave calendar</span></span>

<span data-ttu-id="3d913-181">Jos olet esimies, jolla on suoria alaisia, voit tarkastella ryhmän hyväksyttyä ja hyväksyntää odottavia poissaoloja.</span><span class="sxs-lookup"><span data-stu-id="3d913-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="3d913-182">Valitse Teamsin Human Resources -sovelluksessa **Poissaolo**.</span><span class="sxs-lookup"><span data-stu-id="3d913-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="3d913-183">Valitse **Ryhmän kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="3d913-183">Select **Team calendar**.</span></span>

   ![Human Resourcesin Teams-sovelluksen tarkasteleminen](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="3d913-185">Kalenterissa näkyvät suorien alaisten hyväksytyt ja hyväksyntää odottavat poissaolot.</span><span class="sxs-lookup"><span data-stu-id="3d913-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Human Resourcesin Teams-sovelluksen poissaolokalenteri](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="3d913-187">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="3d913-187">Troubleshooting</span></span>

<span data-ttu-id="3d913-188">Jos sinulla on vaikeuksia Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä.</span><span class="sxs-lookup"><span data-stu-id="3d913-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="3d913-189">Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen.</span><span class="sxs-lookup"><span data-stu-id="3d913-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="3d913-190">Lisätietoja on kohdassa [Pyydä tukea](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="3d913-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="3d913-191">Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa</span><span class="sxs-lookup"><span data-stu-id="3d913-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="3d913-192">Jos et voi kirjautua sovellukseen, Microsoft Teamsiin kirjautumiseen käytettyä tiliä ei ehkä ole liitetty työntekijätietueeseen Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="3d913-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3d913-193">Ota yhteys järjestelmänvalvojaan ja varmista, että työntekijätietue on liitetty oikein.</span><span class="sxs-lookup"><span data-stu-id="3d913-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="3d913-194">Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa</span><span class="sxs-lookup"><span data-stu-id="3d913-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="3d913-195">Jos saat virheilmoituksen, kun yrität hyväksyä lomapyyntöjä Teams-sovelluksessa, yritä tehdä seuraava vianmääritys:</span><span class="sxs-lookup"><span data-stu-id="3d913-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="3d913-196">Tarkista, että tili, jolla kirjaudut Microsoft Teamsiin, on sama kuin se, jolla käytät Dynamics 365 Human Resourcesia.</span><span class="sxs-lookup"><span data-stu-id="3d913-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="3d913-197">Tarkista myös, että saat hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="3d913-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="3d913-198">Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="3d913-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="3d913-199">Tunnetut helppokäyttöisyyteen liittyvät ongelmat</span><span class="sxs-lookup"><span data-stu-id="3d913-199">Known accessibility issues</span></span>

<span data-ttu-id="3d913-200">Teamsin Human Resources -sovellus sisältää seuraavat käytettävyysongelmat. Ne pyritään korjaamaan tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="3d913-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="3d913-201">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="3d913-201">Issue</span></span> | <span data-ttu-id="3d913-202">Ratkaisuehdotus tai selitys</span><span class="sxs-lookup"><span data-stu-id="3d913-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="3d913-203">Työpöydän suurentaminen käyttämällä 400 %:n zoomausta piilottaa jotkin näkymän toimintopainikkeet.</span><span class="sxs-lookup"><span data-stu-id="3d913-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="3d913-204">Suosittelemme suurennuslasin käyttöä siihen asti, kunnes tämän zoomaustason tuki on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="3d913-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="3d913-205">**Poissaolo**-välilehdessä VoiceOver-toiminto ilmoittaa painiketoiminnosta, kun poissaoloruudukon otsikkoa luetaan.</span><span class="sxs-lookup"><span data-stu-id="3d913-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="3d913-206">Ruudukon otsikko ja elementit ryhmitellään vuoden mukaan. Ne voidaan tiivistää.</span><span class="sxs-lookup"><span data-stu-id="3d913-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="3d913-207">VoiceOver tulkitsee tämän toiminnalliseksi nimikkeeksi, vaikka näin ei ole.</span><span class="sxs-lookup"><span data-stu-id="3d913-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="3d913-208">**Poissaolo**-välilehdessä on ylimääräinen sipaisuele siirryttäessä uuden pyynnön **Syykoodi**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="3d913-208">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="3d913-209">Piilotettua ohjausobjektia, jota sipaisulla siirtyminen yrittää käyttää, ei ole.</span><span class="sxs-lookup"><span data-stu-id="3d913-209">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="3d913-210">Jos sipaiset **Poissaolo**-välilehdessä kalenterin ollessa auki, näkymä siirtyy ohjausobjektin ulkopuolelle uuden pyynnön yläosan tai pyynnön muokkauksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="3d913-210">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="3d913-211">Kun käyttäjä on kohdassa **Siirry tähän päivään**, tätä pidetään ohjausobjektin päättymisenä. Näkymä siirtyy takaisin yläosaan sipaisemalla vastakkaiseen suuntaan.</span><span class="sxs-lookup"><span data-stu-id="3d913-211">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="3d913-212">VoiceOver ei lue päivämäärien selitteitä.</span><span class="sxs-lookup"><span data-stu-id="3d913-212">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="3d913-213">Pareittain olevat päivämäärät ovat aina **alkamis**- ja **päättymispäivämäärä**.</span><span class="sxs-lookup"><span data-stu-id="3d913-213">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="3d913-214">**Keskustelu**-välilehdessä kohdistus siirtyy takaisin alkuun, jossa syötettiin päivämäärä käyttöä helpottavan työkalun tai näppäimistön siirtymistoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="3d913-214">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="3d913-215">Siirry käyttämällä sarkainta, kunnes olet jälleen syöttöalueella.</span><span class="sxs-lookup"><span data-stu-id="3d913-215">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="3d913-216">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="3d913-216">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="3d913-217">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="3d913-217">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="3d913-218">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="3d913-218">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="3d913-219">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="3d913-219">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="3d913-220">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="3d913-220">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="3d913-221">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="3d913-221">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="3d913-222">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="3d913-222">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="3d913-223">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="3d913-223">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="3d913-224">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="3d913-224">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="3d913-225">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="3d913-225">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="3d913-226">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="3d913-226">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="3d913-227">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="3d913-227">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="3d913-228">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="3d913-228">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="3d913-229">Microsoft Teams, Azure-tapahtumaverkko ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="3d913-229">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="3d913-230">Kun Dynamics 365 Human Resources -sovellus on käytössä Microsoft Teamsissä, tietyt asiakastiedot voivat siirtyä sen maantieteellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="3d913-230">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="3d913-231">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="3d913-231">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="3d913-232">Näitä tietoja voidaan tallentaa Microsoft Azure -tapahtumaverkossa enintään 24 tunnin ajan. Tiedot käsitellään Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="3d913-232">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="3d913-233">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="3d913-233">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="3d913-234">Keskusteltaessa Human Resources -sovelluksen keskustelubotin kanssa keskustelun sisältö saatetaan tallentaa Azuren Cosmos DB:hen ja lähettää Microsoft Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="3d913-234">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="3d913-235">Nämä tiedot voidaan tallentaa Azuren Cosmos DB:hen enintään 24 tunniksi, ja niitä voidaan käsitellä sen maantieteellisen alueen ulkopuolella, jossa vuokralaisen Human Resources -palvelu on otettu käyttöön. Tiedot salataan siirrettäessä ja levossa, eikä Microsoft tai sen alihankkija käytä niitä koulutuksiin tai palvelujen parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="3d913-235">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="3d913-236">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="3d913-236">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="3d913-237">Ohjeet Human Resources -sovelluksen käyttöoikeuksien rajoittamiseen Microsoft Teamsissä organisaatiosi tai sen käyttäjien osalta: [Sovellusten oikeuskäytäntöjen hallinta Microsoft Teamsissä](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="3d913-237">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="3d913-238">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="3d913-238">See also</span></span>

[<span data-ttu-id="3d913-239">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="3d913-239">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="3d913-240">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="3d913-240">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="3d913-241">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="3d913-241">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
