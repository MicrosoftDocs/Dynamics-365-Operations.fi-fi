---
title: Loma- ja poissaolopyyntöjen hallinta Teamsissa
description: Tässä ohjeaiheessa käsitellään poissaolopyyntöjä Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097256"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="e97fb-103">Lomapyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e97fb-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e97fb-104">Microsoft Teamsin Dynamics 365 Human Resources -sovelluksessa voi tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldon tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="e97fb-105">Voit käyttää bottia pyytääksesi tietoja ja aloittaaksesi lomapyynnön.</span><span class="sxs-lookup"><span data-stu-id="e97fb-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="e97fb-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="e97fb-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="e97fb-107">Voit myös lähettää ihmisille tietoja tulevista poissaoloista Teamsissa ja keskusteluissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="e97fb-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="e97fb-108">Sovelluksen asentaminen</span><span class="sxs-lookup"><span data-stu-id="e97fb-108">Install the app</span></span>

<span data-ttu-id="e97fb-109">Löydät Dynamics 365 Human Resources -sovelluksen Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="e97fb-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="e97fb-110">Siirry Microsoft Teamsissa sovellusluetteloon.</span><span class="sxs-lookup"><span data-stu-id="e97fb-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="e97fb-111">Hae Dynamics 365 Human Resources ja valitse sitten **Henkilöstöhallinto**-ruutu.</span><span class="sxs-lookup"><span data-stu-id="e97fb-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="e97fb-112">Asenna sovellus valitsemalla **Lisää**-painike.</span><span class="sxs-lookup"><span data-stu-id="e97fb-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="e97fb-113">Jos sisäänkirjautuminen ei tapahdu automaattisesti, kirjaudu sitään valitsemalla **Asetukset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e97fb-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="e97fb-114">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="e97fb-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="e97fb-115">Jos käytössä on useita Human Resources -esiintymiä, valitse **Asetukset**-välilehdessä, mihin ympäristöön yhteys muodostetaan.</span><span class="sxs-lookup"><span data-stu-id="e97fb-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="e97fb-116">Sovellus tukee nyt järjestelmänvalvojan käyttöoikeusroolia.</span><span class="sxs-lookup"><span data-stu-id="e97fb-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="e97fb-117">Botin käyttö</span><span class="sxs-lookup"><span data-stu-id="e97fb-117">Use the bot</span></span>

<span data-ttu-id="e97fb-118">Kun sovellus on asennettu, näkyviin tuleva tervehdyssanoma ilmoittaa, minkälaisia toimintoja botti voi tehdä puolestasi.</span><span class="sxs-lookup"><span data-stu-id="e97fb-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="e97fb-119">Kun bottia käytetään ensimmäinen kerran, sisäänkirjautuminen voi olla välttämätöntä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="e97fb-120">Jos kirjautumisikkuna ei ole näkyvissä, varmista, että selaimen asetukset sallivat ponnahdusikkunat.</span><span class="sxs-lookup"><span data-stu-id="e97fb-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="e97fb-121">Botilta voi pyytää seuraavia:</span><span class="sxs-lookup"><span data-stu-id="e97fb-121">You can ask the bot to:</span></span>

- <span data-ttu-id="e97fb-122">Tarkastele nykyisiä lomasaldoja.</span><span class="sxs-lookup"><span data-stu-id="e97fb-122">View your current leave balances.</span></span> <span data-ttu-id="e97fb-123">Lähetä esimerkiksi sanoma, jossa sanotaan "Näytä lomasaldot".</span><span class="sxs-lookup"><span data-stu-id="e97fb-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="e97fb-124">Lomapyynnön käynnistäminen käyttäjän puolesta.</span><span class="sxs-lookup"><span data-stu-id="e97fb-124">Start a leave request for you.</span></span> <span data-ttu-id="e97fb-125">Lähetä esimerkiksi viesti "Pidä vapaata" tai "Haluan pitää vapaata ensi torstaina ja perjantaina", jotta voit tarkemmin kysyä vapaata poissaolon lomatyypille.</span><span class="sxs-lookup"><span data-stu-id="e97fb-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Lomapyynnön käynnistäminen Tiimit-keskustelussa](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="e97fb-127">Keskustelubotti täyttää lomapyynnön puolestasi.</span><span class="sxs-lookup"><span data-stu-id="e97fb-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="e97fb-128">Valitse **Pyydä vapaata** ja muokkaa pyyntösi tietoja.</span><span class="sxs-lookup"><span data-stu-id="e97fb-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="e97fb-129">Jos haluat lähettää useita lomatyyppejä koskevat lomapyynnöt samana päivänä, valitse **Lisäasetukset**-valikosta **Jaa päivä**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="e97fb-130">Jos valitset puoli päivää lomaa, kun pyynnön yksikkö on päiviä, voit määrittää, haluatko pyytää aamupäivän vai iltapäivän vapaata, valitsemalla **Lisäasetukset**-valikosta **Puoli päivää** -määritysvaihtoehdon.</span><span class="sxs-lookup"><span data-stu-id="e97fb-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Puolen päivän määritelmät](./media/HalfDayDefinitions.png)

- <span data-ttu-id="e97fb-132">Kun olet muokannut lomapyyntösi tietoja, lähetä se hyväksyttäväksi valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Lomapyynnön lähettäminen](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="e97fb-134">Lomien ja poissaolojen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e97fb-134">Manage your leave in Teams</span></span>

<span data-ttu-id="e97fb-135">**Poissaolo**-välilehdessä voi tarkastella seuraavia:</span><span class="sxs-lookup"><span data-stu-id="e97fb-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="e97fb-136">Jokaisen sellaisen poissaolotyypin poissaolosaldon tiedot, johon kysyjä on rekisteröity</span><span class="sxs-lookup"><span data-stu-id="e97fb-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="e97fb-137">Tulevat lomapyynnöt</span><span class="sxs-lookup"><span data-stu-id="e97fb-137">Upcoming leave requests</span></span>

- <span data-ttu-id="e97fb-138">Poissaolopyynnöt</span><span class="sxs-lookup"><span data-stu-id="e97fb-138">Time-off requests</span></span>

- <span data-ttu-id="e97fb-139">Lomapyyntöluonnokset</span><span class="sxs-lookup"><span data-stu-id="e97fb-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="e97fb-140">Uuden pyynnön luominen</span><span class="sxs-lookup"><span data-stu-id="e97fb-140">Create a new request</span></span>

1. <span data-ttu-id="e97fb-141">Uusi lomapyyntö luodaan valitsemalla **Uusi pyyntö**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="e97fb-142">Anna haluamasi poissaolopäivä tai -päivät ja valitse sitten **Lisää**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Human Resources Teamsin lomasovelluksen poissaolon lisääminen](./media/TimeOffHours.png)

3. <span data-ttu-id="e97fb-144">Anna tarvittaessa syykoodi.</span><span class="sxs-lookup"><span data-stu-id="e97fb-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="e97fb-145">Lisää myös mahdolliset kommentit ja liitteet.</span><span class="sxs-lookup"><span data-stu-id="e97fb-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="e97fb-146">Valitse **Jaa päivä** -vaihtoehto **Lisäasetukset** -valikosta, jos haluat lähettää useita lomapyyntömerkintöjä samalle päivälle eri lomalajeille.</span><span class="sxs-lookup"><span data-stu-id="e97fb-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="e97fb-147">Valitse **Puoli päivää -määritys**-vaihtoehto, kun haluat määrittää, haluatko pyytää aamupäivän vai iltapäivän vapaata.</span><span class="sxs-lookup"><span data-stu-id="e97fb-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="e97fb-148">Tämä vaihtoehto on käytettävissä, kun lomapyynnön yksikkö on päivinä ja pyydetty määrä on 0,5 päivää.</span><span class="sxs-lookup"><span data-stu-id="e97fb-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="e97fb-149">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi valitsemalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="e97fb-150">Jos haluat palata pyyntöön, voit syöttää **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="e97fb-151">Pyyntöluonnosten hallinta</span><span class="sxs-lookup"><span data-stu-id="e97fb-151">Manage draft requests</span></span>

1. <span data-ttu-id="e97fb-152">Valitse **Luonnokset**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="e97fb-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="e97fb-153">Muokkaa pyyntöä valitsemalla kynäkuvake tai poista pyyntö valitsemalla roskakori.</span><span class="sxs-lookup"><span data-stu-id="e97fb-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="e97fb-154">Tee tarvittavat muutokset.</span><span class="sxs-lookup"><span data-stu-id="e97fb-154">Make any necessary changes.</span></span> <span data-ttu-id="e97fb-155">Kun tiedot on annettu, lähetä pyyntö hyväksyttäväksi kirjoittamalla **Lähetä**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="e97fb-156">Voit palata pyyntöön, jos valitset **Tallenna luonnoksena**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="e97fb-157">Teams-ilmoituksiin vastaaminen</span><span class="sxs-lookup"><span data-stu-id="e97fb-157">Respond to Teams notifications</span></span>

<span data-ttu-id="e97fb-158">Kun lomapyyntöjen lähetysten hyväksyjänä olet sinä tai vaihtoehtoisesti työntekijä, saat ilmoituksen Teamsin Human Resources -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="e97fb-159">Voit tarkastella ilmoitusta valitsemalla sen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-159">You can select the notification to view it.</span></span> <span data-ttu-id="e97fb-160">Ilmoitukset näkyvät myös **Keskustelu**-alueella.</span><span class="sxs-lookup"><span data-stu-id="e97fb-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="e97fb-161">Jos olet hyväksyjä, voit valita ilmoituksessa **Hyväksy** tai **Hylkää**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="e97fb-162">Voit myös määrittää valinnaisen sanoman.</span><span class="sxs-lookup"><span data-stu-id="e97fb-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="e97fb-163">Tulevien poissaolotietojen lähettäminen työtovereille</span><span class="sxs-lookup"><span data-stu-id="e97fb-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="e97fb-164">Kun olet asentanut Teamsin Human Resources -sovelluksen, voit lähettää työtovereillesi helposti tietoja tulevista poissaoloistasi ryhmissä tai keskusteluissa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="e97fb-165">Valitse ryhmässä tai Teams-keskustelussa Human Resources -painike keskusteluikkunan alapuolella.</span><span class="sxs-lookup"><span data-stu-id="e97fb-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Human Resources -painike keskusteluikkunan alla](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="e97fb-167">Valitse jaettava lomapyyntö.</span><span class="sxs-lookup"><span data-stu-id="e97fb-167">Select the leave request you want to share.</span></span> <span data-ttu-id="e97fb-168">Jos haluat jakaa lomapyyntöluonnoksen, valitse ensin **Luonnokset**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="e97fb-169">Lomapyyntösi tulee näkyviin keskustelussa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="e97fb-170">Jos olet jakanut pyyntöluonnoksen, se tulee näkyviin luonnoksena.</span><span class="sxs-lookup"><span data-stu-id="e97fb-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="e97fb-171">Ryhmän lomakalenterin tarkasteleminen</span><span class="sxs-lookup"><span data-stu-id="e97fb-171">View your team's leave calendar</span></span>

<span data-ttu-id="e97fb-172">Jos olet esimies, jolla on suoria alaisia, voit tarkastella ryhmän hyväksyttyä ja hyväksyntää odottavia poissaoloja.</span><span class="sxs-lookup"><span data-stu-id="e97fb-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="e97fb-173">Valitse Teamsin Human Resources -sovelluksessa **Poissaolo**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="e97fb-174">Valitse **Ryhmän kalenteri**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-174">Select **Team calendar**.</span></span> <span data-ttu-id="e97fb-175">Kalenterissa näkyvät suorien alaisten hyväksytyt ja hyväksyntää odottavat poissaolot.</span><span class="sxs-lookup"><span data-stu-id="e97fb-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="e97fb-176">Jos et näe ryhmäkalenteria, pyydä järjestelmänvalvojaasi ottamaan se käyttöön.</span><span class="sxs-lookup"><span data-stu-id="e97fb-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="e97fb-177">Lisätietoja on kohdassa [Asentaminen ja määrittäminen](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="e97fb-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="e97fb-178">Tuetut kielet</span><span class="sxs-lookup"><span data-stu-id="e97fb-178">Supported languages</span></span>

<span data-ttu-id="e97fb-179">Teamsin Dynamics 365 Human Resources -sovellus tukee seuraavia kieliä:</span><span class="sxs-lookup"><span data-stu-id="e97fb-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="e97fb-180">Kielialueen tunnus</span><span class="sxs-lookup"><span data-stu-id="e97fb-180">Locale ID</span></span> | <span data-ttu-id="e97fb-181">Kieli</span><span class="sxs-lookup"><span data-stu-id="e97fb-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="e97fb-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="e97fb-182">de-DE</span></span> | <span data-ttu-id="e97fb-183">saksa (Saksa)</span><span class="sxs-lookup"><span data-stu-id="e97fb-183">German (Germany)</span></span> |
| <span data-ttu-id="e97fb-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="e97fb-184">es-ES</span></span> | <span data-ttu-id="e97fb-185">espanja (Espanja)</span><span class="sxs-lookup"><span data-stu-id="e97fb-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="e97fb-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="e97fb-186">es-MX</span></span> | <span data-ttu-id="e97fb-187">espanja (Meksiko)</span><span class="sxs-lookup"><span data-stu-id="e97fb-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="e97fb-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="e97fb-188">fr-CA</span></span> | <span data-ttu-id="e97fb-189">ranska (Kanada)</span><span class="sxs-lookup"><span data-stu-id="e97fb-189">French (Canada)</span></span> |
| <span data-ttu-id="e97fb-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="e97fb-190">fr-FR</span></span> | <span data-ttu-id="e97fb-191">ranska (Ranska)</span><span class="sxs-lookup"><span data-stu-id="e97fb-191">French (France)</span></span> |
| <span data-ttu-id="e97fb-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="e97fb-192">it-IT</span></span> | <span data-ttu-id="e97fb-193">italia (Italia)</span><span class="sxs-lookup"><span data-stu-id="e97fb-193">Italian (Italy)</span></span> |
| <span data-ttu-id="e97fb-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="e97fb-194">nl-NL</span></span> | <span data-ttu-id="e97fb-195">hollanti (Alankomaat)</span><span class="sxs-lookup"><span data-stu-id="e97fb-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="e97fb-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="e97fb-196">pt-BR</span></span> | <span data-ttu-id="e97fb-197">portugali (Brasilia)</span><span class="sxs-lookup"><span data-stu-id="e97fb-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="e97fb-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="e97fb-198">tr-TR</span></span> | <span data-ttu-id="e97fb-199">turkki (Turkki)</span><span class="sxs-lookup"><span data-stu-id="e97fb-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="e97fb-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="e97fb-200">zh-CN</span></span> | <span data-ttu-id="e97fb-201">kiina (yksinkertaistettu)</span><span class="sxs-lookup"><span data-stu-id="e97fb-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="e97fb-202">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="e97fb-202">Troubleshooting</span></span>

<span data-ttu-id="e97fb-203">Jos sinulla on vaikeuksia Dynamics 365 Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="e97fb-204">Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="e97fb-205">Lisätietoja on kohdassa [Pyydä tukea](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="e97fb-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="e97fb-206">Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e97fb-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="e97fb-207">Jos et voi kirjautua sovellukseen, Microsoft Teamsiin kirjautumiseen käytettyä tiliä ei ehkä ole liitetty työntekijätietueeseen Dynamics 365 Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e97fb-208">Ota yhteys järjestelmänvalvojaan ja varmista, että työntekijätietue on liitetty oikein.</span><span class="sxs-lookup"><span data-stu-id="e97fb-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="e97fb-209">Käännökset eivät näy oikein</span><span class="sxs-lookup"><span data-stu-id="e97fb-209">Translations don't display correctly</span></span>

<span data-ttu-id="e97fb-210">Jos käännökset eivät näy odotetulla tavalla, varmista, että Teamsissa valitsemasi kieli vastaa Human Resources -sovelluksen **Käyttäjän asetukset** -osiossa valittua kieltä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="e97fb-211">Tarkasta Teamsissa **Sovelluksen kieli** -asetus **Asetukset**-osiosta.</span><span class="sxs-lookup"><span data-stu-id="e97fb-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-asetukset](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="e97fb-213">Valitse Human Resources -sovelluksesta **Asetukset** ja sitten **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="e97fb-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="e97fb-214">Varmista, että **Kieli**-kenttä vastaa Teamsin **Sovelluksen kieli** -kenttää.</span><span class="sxs-lookup"><span data-stu-id="e97fb-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Human Resources -sovelluksen Käyttäjän asetukset -osio](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="e97fb-216">Jos sinulla edelleen ilmenee käännöksiin liittyviä ongelmia, kerro niistä meille.</span><span class="sxs-lookup"><span data-stu-id="e97fb-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="e97fb-217">Lisätietoja on kohdassa [Tuen pyytäminen Finance and Operations -sovelluksia tai Lifecycle Services (LCS) -sovellusta varten](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="e97fb-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="e97fb-218">Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e97fb-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="e97fb-219">Jos saat virheilmoituksen, kun yrität hyväksyä lomapyyntöjä Teams-sovelluksessa, yritä tehdä seuraava vianmääritys:</span><span class="sxs-lookup"><span data-stu-id="e97fb-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="e97fb-220">Tarkista, että tili, jolla kirjaudut Microsoft Teamsiin, on sama kuin se, jolla käytät Dynamics 365 Human Resourcesia.</span><span class="sxs-lookup"><span data-stu-id="e97fb-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="e97fb-221">Tarkista myös, että saat hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="e97fb-222">Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="e97fb-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="e97fb-223">Lomien hyväksyjät eivät saa Teams-keskustelusanomia lomapyyntöjen hyväksymistä varten</span><span class="sxs-lookup"><span data-stu-id="e97fb-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="e97fb-224">Varmista, että ympäristö- ja käyttäjäilmoitukset ovat käytössä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="e97fb-225">Lisätietoa on kohdissa [Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) ja [Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="e97fb-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="e97fb-226">Varmista, että käyttäjät ovat kirjautuneet **Keskustelut**-välilehteen samoilla tunnistetiedoilla, kuin mitä he käyttävät lomapyyntöjen hyväksymisessä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="e97fb-227">Käytä viestejä "kirjaudu ulos" ja sitten "kirjaudu sisään" kirjautuaksesi sisään oikeilla tunnistetiedoilla.</span><span class="sxs-lookup"><span data-stu-id="e97fb-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="e97fb-228">Jos ongelma säilyy, tarkista Business Events -järjestelmän erätyön tila järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="e97fb-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="e97fb-229">Jos se on odotus- tai suoritusvaiheessa, palaa muutaman minuutin kuluttua.</span><span class="sxs-lookup"><span data-stu-id="e97fb-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="e97fb-230">Jos tila ei muutu, kirjaa tukipalvelupyyntö, jotta tiimimme voi ratkaista ongelman.</span><span class="sxs-lookup"><span data-stu-id="e97fb-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="e97fb-231">Tunnetut helppokäyttöisyyteen liittyvät ongelmat</span><span class="sxs-lookup"><span data-stu-id="e97fb-231">Known accessibility issues</span></span>

<span data-ttu-id="e97fb-232">Teamsin Human Resources -sovellus sisältää seuraavat käytettävyysongelmat. Ne pyritään korjaamaan tulevissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="e97fb-233">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="e97fb-233">Issue</span></span> | <span data-ttu-id="e97fb-234">Ratkaisuehdotus tai selitys</span><span class="sxs-lookup"><span data-stu-id="e97fb-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="e97fb-235">Työpöydän suurentaminen käyttämällä 400 %:n zoomausta piilottaa jotkin näkymän toimintopainikkeet.</span><span class="sxs-lookup"><span data-stu-id="e97fb-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="e97fb-236">Suosittelemme suurennuslasin käyttöä siihen asti, kunnes tämän zoomaustason tuki on käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e97fb-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="e97fb-237">**Poissaolo**-välilehdessä VoiceOver-toiminto ilmoittaa painiketoiminnosta, kun poissaoloruudukon otsikkoa luetaan.</span><span class="sxs-lookup"><span data-stu-id="e97fb-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="e97fb-238">Ruudukon otsikko ja elementit ryhmitellään vuoden mukaan. Ne voidaan tiivistää.</span><span class="sxs-lookup"><span data-stu-id="e97fb-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="e97fb-239">VoiceOver tulkitsee tämän toiminnalliseksi nimikkeeksi, vaikka näin ei ole.</span><span class="sxs-lookup"><span data-stu-id="e97fb-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="e97fb-240">**Poissaolo**-välilehdessä on ylimääräinen sipaisuele siirryttäessä uuden pyynnön **Syykoodi**-kohtaan.</span><span class="sxs-lookup"><span data-stu-id="e97fb-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="e97fb-241">Piilotettua ohjausobjektia, jota sipaisulla siirtyminen yrittää käyttää, ei ole.</span><span class="sxs-lookup"><span data-stu-id="e97fb-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="e97fb-242">Jos sipaiset **Poissaolo**-välilehdessä kalenterin ollessa auki, näkymä siirtyy ohjausobjektin ulkopuolelle uuden pyynnön yläosan tai pyynnön muokkauksen sijaan.</span><span class="sxs-lookup"><span data-stu-id="e97fb-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="e97fb-243">Kun käyttäjä on kohdassa **Siirry tähän päivään**, tätä pidetään ohjausobjektin päättymisenä. Näkymä siirtyy takaisin yläosaan sipaisemalla vastakkaiseen suuntaan.</span><span class="sxs-lookup"><span data-stu-id="e97fb-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="e97fb-244">**Keskustelu**-välilehdessä kohdistus siirtyy takaisin alkuun, jossa syötettiin päivämäärä käyttöä helpottavan työkalun tai näppäimistön siirtymistoiminnon avulla.</span><span class="sxs-lookup"><span data-stu-id="e97fb-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="e97fb-245">Siirry käyttämällä sarkainta, kunnes olet jälleen syöttöalueella.</span><span class="sxs-lookup"><span data-stu-id="e97fb-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="e97fb-246">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="e97fb-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="e97fb-247">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="e97fb-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="e97fb-248">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="e97fb-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="e97fb-249">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="e97fb-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="e97fb-250">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="e97fb-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="e97fb-251">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="e97fb-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="e97fb-252">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="e97fb-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="e97fb-253">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="e97fb-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="e97fb-254">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="e97fb-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e97fb-255">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="e97fb-256">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="e97fb-257">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="e97fb-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="e97fb-258">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e97fb-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="e97fb-259">Microsoft Teams, Azure-tapahtumaverkko ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e97fb-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="e97fb-260">Kun Dynamics 365 Human Resources -sovellus on käytössä Microsoft Teamsissä, tietyt asiakastiedot voivat siirtyä sen maantieteellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="e97fb-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="e97fb-261">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="e97fb-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="e97fb-262">Näitä tietoja voidaan tallentaa Microsoft Azure -tapahtumaverkossa enintään 24 tunnin ajan. Tiedot käsitellään Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="e97fb-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e97fb-263">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e97fb-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="e97fb-264">Keskusteltaessa Human Resources -sovelluksen keskustelubotin kanssa keskustelun sisältö saatetaan tallentaa Azuren Cosmos DB:hen ja lähettää Microsoft Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="e97fb-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="e97fb-265">Nämä tiedot voidaan tallentaa Azuren Cosmos DB:hen enintään 24 tunniksi, ja niitä voidaan käsitellä sen maantieteellisen alueen ulkopuolella, jossa vuokralaisen Human Resources -palvelu on otettu käyttöön. Tiedot salataan siirrettäessä ja levossa, eikä Microsoft tai sen alihankkija käytä niitä koulutuksiin tai palvelujen parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="e97fb-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="e97fb-266">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="e97fb-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="e97fb-267">Ohjeet Human Resources -sovelluksen käyttöoikeuksien rajoittamiseen Microsoft Teamsissä organisaatiosi tai sen käyttäjien osalta: [Sovellusten oikeuskäytäntöjen hallinta Microsoft Teamsissä](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e97fb-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="e97fb-268">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e97fb-268">See also</span></span>

[<span data-ttu-id="e97fb-269">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="e97fb-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="e97fb-270">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="e97fb-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="e97fb-271">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="e97fb-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
