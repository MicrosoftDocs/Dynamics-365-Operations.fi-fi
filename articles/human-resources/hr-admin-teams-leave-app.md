---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
author: andreabichsel
manager: tfehr
ms.date: 09/30/2020
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
ms.openlocfilehash: ba520f873de5b20111f9134e87281bcdf4025785
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112377"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="73c9c-103">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="73c9c-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="73c9c-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="73c9c-105">Työntekijät voivat pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="73c9c-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="73c9c-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="73c9c-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="73c9c-107">Lisäksi lähettää tietoja tulevista poissaoloista voidaan lähettää ryhmissä ja keskusteluissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="73c9c-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teamsin lomasovelluksen botti](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resourcesin lomapyyntökortti](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="73c9c-111">Asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="73c9c-111">Install and setup</span></span>

<span data-ttu-id="73c9c-112">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="73c9c-112">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="73c9c-113">Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="73c9c-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="73c9c-114">Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="73c9c-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="73c9c-115">Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="73c9c-115">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="73c9c-116">Jos haluat, että käyttäjät voivat vastaanottaa lomapyyntöilmoitukset Teams-sovelluksessa, sinun on otettava ilmoitukset käyttöön Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-116">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="73c9c-117">Vain Teamsiin kirjautuneet käyttäjät, jotka käyttävät Human Resourcesin Teams-sovellusta, vastaanottavat ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="73c9c-117">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="73c9c-118">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-118">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="73c9c-119">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-119">Select **Links**.</span></span>

3. <span data-ttu-id="73c9c-120">Valitse **Asetukset**-kohdassa **Järjestelmäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-120">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="73c9c-121">Määritä **Yleistä**-välilehdessä **Ota käyttöön Teams-sovelluksen ilmoitukset** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-121">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto järjestelmäparametreissa](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="73c9c-123">Jos haluat ottaa Teams-ilmoitukset käyttöön kaikille käyttäjille, valitse **Kyllä** pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="73c9c-123">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-ilmoitusten käyttöönotto kaikille käyttäjille](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="73c9c-125">Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="73c9c-125">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="73c9c-126">Kun olet ottanut ilmoitukset käyttöön Human Resourcesin Teams-sovelluksessa, voit ottaa ilmoitukset käyttöön tai poistaa ne käytöstä yksittäisille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="73c9c-126">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="73c9c-127">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-127">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="73c9c-128">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-128">Select **Links**.</span></span>

3. <span data-ttu-id="73c9c-129">**Valitse käyttäjät** -kohdasta **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-129">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="73c9c-130">Valitse **Työnkulku**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="73c9c-130">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="73c9c-131">Määritä **Teams-sovelluksen Salli ilmoitukset** -kohdan arvoksi **Kyllä**, jos haluat ottaa ilmoitukset käyttöön käyttäjälle. Valitse **Ei**, jos haluat poistaa käyttäjän ilmoitukset käytöstä.</span><span class="sxs-lookup"><span data-stu-id="73c9c-131">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto käyttäjän asetusten Työnkulku-välilehdessä](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="73c9c-133">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="73c9c-133">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="73c9c-134">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="73c9c-134">Known issues</span></span>

| <span data-ttu-id="73c9c-135">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="73c9c-135">Issue</span></span> | <span data-ttu-id="73c9c-136">Tila</span><span class="sxs-lookup"><span data-stu-id="73c9c-136">Status</span></span> |
| --- | --- |
| <span data-ttu-id="73c9c-137">Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo.</span><span class="sxs-lookup"><span data-stu-id="73c9c-137">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="73c9c-138">Ennakointi ei ole vielä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="73c9c-138">Forecasting isn't yet available.</span></span> <span data-ttu-id="73c9c-139">Saldo näkyy kuluvalta päivältä.</span><span class="sxs-lookup"><span data-stu-id="73c9c-139">The balance displays for the current date.</span></span> |
| <span data-ttu-id="73c9c-140">**Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-140">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="73c9c-141">Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="73c9c-141">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="73c9c-142">Saldotiedot lasketaan kuluvasta päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="73c9c-142">Balance information is calculated as of today.</span></span> | <span data-ttu-id="73c9c-143">Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-143">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="73c9c-144">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="73c9c-144">Troubleshooting</span></span>

<span data-ttu-id="73c9c-145">Jos käyttäjällä on vaikeuksia Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä.</span><span class="sxs-lookup"><span data-stu-id="73c9c-145">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="73c9c-146">Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen.</span><span class="sxs-lookup"><span data-stu-id="73c9c-146">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="73c9c-147">Lisätietoja on kohdassa [Pyydä tukea](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="73c9c-147">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="73c9c-148">Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa</span><span class="sxs-lookup"><span data-stu-id="73c9c-148">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="73c9c-149">Jos käyttäjä ottaa yhteyttä, koska ei pysty kirjautumaan sovellukseen, tarkista, että käyttäjään on liitettyä työntekijätietue Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-149">If a user contacts you because they can't sign into the app, verify that the user has an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="73c9c-150">Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa</span><span class="sxs-lookup"><span data-stu-id="73c9c-150">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="73c9c-151">Jos käyttäjä saa virheilmoituksen yrittäessään hyväksyä lomapyyntöjä Teams-sovelluksessa, tee seuraava vianmääritys:</span><span class="sxs-lookup"><span data-stu-id="73c9c-151">If a user receives an error while trying to approve leave requests in the Teams app, perform the following troubleshooting steps:</span></span>

1. <span data-ttu-id="73c9c-152">Tarkista, että käyttäjän Teams-tili on sama tili, jolla käyttäjä käyttää Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="73c9c-152">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="73c9c-153">Tarkista myös, että käyttäjä saa hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-153">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="73c9c-154">Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="73c9c-154">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="73c9c-155">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="73c9c-155">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="73c9c-156">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="73c9c-156">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="73c9c-157">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="73c9c-157">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="73c9c-158">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="73c9c-158">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="73c9c-159">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="73c9c-159">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="73c9c-160">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="73c9c-160">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="73c9c-161">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="73c9c-161">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="73c9c-162">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="73c9c-162">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="73c9c-163">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="73c9c-163">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="73c9c-164">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="73c9c-164">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="73c9c-165">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="73c9c-165">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="73c9c-166">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="73c9c-166">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="73c9c-167">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="73c9c-167">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="73c9c-168">Microsoft Teams, Azure-tapahtumaverkko ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="73c9c-168">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="73c9c-169">Kun Dynamics 365 Human Resources -sovellus on käytössä Microsoft Teamsissä, tietyt asiakastiedot voivat siirtyä sen maantieteellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="73c9c-169">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="73c9c-170">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="73c9c-170">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="73c9c-171">Näitä tietoja voidaan tallentaa Microsoft Azure -tapahtumaverkossa enintään 24 tunnin ajan. Tiedot käsitellään Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="73c9c-171">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73c9c-172">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="73c9c-172">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="73c9c-173">Keskusteltaessa Human Resources -sovelluksen keskustelubotin kanssa keskustelun sisältö saatetaan tallentaa Azuren Cosmos DB:hen ja lähettää Microsoft Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="73c9c-173">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="73c9c-174">Nämä tiedot voidaan tallentaa Azuren Cosmos DB:hen enintään 24 tunniksi, ja niitä voidaan käsitellä sen maantieteellisen alueen ulkopuolella, jossa vuokralaisen Human Resources -palvelu on otettu käyttöön. Tiedot salataan siirrettäessä ja levossa, eikä Microsoft tai sen alihankkija käytä niitä koulutuksiin tai palvelujen parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="73c9c-174">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73c9c-175">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="73c9c-175">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="73c9c-176">Ohjeet Human Resources -sovelluksen käyttöoikeuksien rajoittamiseen Microsoft Teamsissä organisaatiosi tai sen käyttäjien osalta: [Sovellusten oikeuskäytäntöjen hallinta Microsoft Teamsissä](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="73c9c-176">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="73c9c-177">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="73c9c-177">See also</span></span> 

[<span data-ttu-id="73c9c-178">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="73c9c-178">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="73c9c-179">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="73c9c-179">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="73c9c-180">Lomapyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="73c9c-180">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

