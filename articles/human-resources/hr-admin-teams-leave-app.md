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
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="a16b9-103">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="a16b9-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="a16b9-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="a16b9-105">Työntekijät voivat pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="a16b9-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="a16b9-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="a16b9-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teamsin lomasovelluksen botti](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="a16b9-109">Asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a16b9-109">Install and setup</span></span>

<span data-ttu-id="a16b9-110">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="a16b9-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="a16b9-111">Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="a16b9-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="a16b9-112">Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="a16b9-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="a16b9-113">Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="a16b9-113">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="a16b9-114">Jos haluat, että käyttäjät voivat vastaanottaa lomapyyntöilmoitukset Teams-sovelluksessa, sinun on otettava ilmoitukset käyttöön Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-114">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="a16b9-115">Vain Teamsiin kirjautuneet käyttäjät, jotka käyttävät Human Resourcesin Teams-sovellusta, vastaanottavat ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="a16b9-115">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="a16b9-116">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-116">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a16b9-117">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-117">Select **Links**.</span></span>

3. <span data-ttu-id="a16b9-118">Valitse **Asetukset**-kohdassa **Järjestelmäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-118">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="a16b9-119">Määritä **Yleistä**-välilehdessä **Ota käyttöön Teams-sovelluksen ilmoitukset** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-119">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto järjestelmäparametreissa](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="a16b9-121">Jos haluat ottaa Teams-ilmoitukset käyttöön kaikille käyttäjille, valitse **Kyllä** pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-121">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-ilmoitusten käyttöönotto kaikille käyttäjille](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="a16b9-123">Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="a16b9-123">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="a16b9-124">Kun olet ottanut ilmoitukset käyttöön Human Resourcesin Teams-sovelluksessa, voit ottaa ilmoitukset käyttöön tai poistaa ne käytöstä yksittäisille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="a16b9-124">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="a16b9-125">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-125">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="a16b9-126">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-126">Select **Links**.</span></span>

3. <span data-ttu-id="a16b9-127">**Valitse käyttäjät** -kohdasta **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-127">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="a16b9-128">Valitse **Työnkulku**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="a16b9-128">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="a16b9-129">Määritä **Teams-sovelluksen Salli ilmoitukset** -kohdan arvoksi **Kyllä**, jos haluat ottaa ilmoitukset käyttöön käyttäjälle. Valitse **Ei**, jos haluat poistaa käyttäjän ilmoitukset käytöstä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-129">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto käyttäjän asetusten Työnkulku-välilehdessä](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="a16b9-131">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="a16b9-131">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="a16b9-132">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="a16b9-132">Known issues</span></span>

| <span data-ttu-id="a16b9-133">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="a16b9-133">Issue</span></span> | <span data-ttu-id="a16b9-134">Tila</span><span class="sxs-lookup"><span data-stu-id="a16b9-134">Status</span></span> |
| --- | --- |
| <span data-ttu-id="a16b9-135">Vaakasuuntainen vieritys ei toimi Android-puhelimissa</span><span class="sxs-lookup"><span data-stu-id="a16b9-135">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="a16b9-136">Vaakasuuntainen vieritys ei ole ongelma iOS- tai työpöytälaitteissa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-136">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="a16b9-137">Pyrimme korjaamaan asian Androidille.</span><span class="sxs-lookup"><span data-stu-id="a16b9-137">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="a16b9-138">Virhe: ongelma etsittäessä ympäristöä, johon muodostetaan yhteyttä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-138">Error: There is an issue finding an environment to connect to.</span></span> | <span data-ttu-id="a16b9-139">Tämä virhe saattaa tulla näyttöön, vaikka olisit varmistanut, että käyttäjä voi käyttää yhtä tai useampaa henkilöstöresurssiympäristöä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-139">You might receive this error even if you've verified that the user can access one or more Human Resources environments.</span></span> <span data-ttu-id="a16b9-140">Lisäksi et ehkä näe kaikkia odottamiasi ympäristöjä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-140">Also, you might not see all the environments you expect.</span></span> <span data-ttu-id="a16b9-141">Ennen kuin korjaat tämän ongelman, poista käyttäjä ja tuo ne sitten uudelleen, jotta ongelma voidaan ratkaista.</span><span class="sxs-lookup"><span data-stu-id="a16b9-141">Until we fix this issue, delete the user and then import them in again to resolve the problem.</span></span> |
| <span data-ttu-id="a16b9-142">Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo.</span><span class="sxs-lookup"><span data-stu-id="a16b9-142">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="a16b9-143">Ennakointi ei ole vielä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-143">Forecasting isn't yet available.</span></span> <span data-ttu-id="a16b9-144">Saldo näkyy kuluvalta päivältä.</span><span class="sxs-lookup"><span data-stu-id="a16b9-144">The balance displays for the current date.</span></span> |
| <span data-ttu-id="a16b9-145">**Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-145">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="a16b9-146">Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="a16b9-146">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="a16b9-147">Saldotiedot lasketaan kuluvasta päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="a16b9-147">Balance information is calculated as of today.</span></span> | <span data-ttu-id="a16b9-148">Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-148">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="a16b9-149">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="a16b9-149">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="a16b9-150">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="a16b9-150">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="a16b9-151">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="a16b9-151">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="a16b9-152">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="a16b9-152">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="a16b9-153">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="a16b9-153">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="a16b9-154">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="a16b9-154">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="a16b9-155">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="a16b9-155">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="a16b9-156">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="a16b9-156">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="a16b9-157">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="a16b9-157">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a16b9-158">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="a16b9-158">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="a16b9-159">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="a16b9-159">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="a16b9-160">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="a16b9-160">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="a16b9-161">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="a16b9-161">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-azure-event-grid-and-microsoft-teams"></a><span data-ttu-id="a16b9-162">Microsoft Azuren tapahtumaruudukko ja Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a16b9-162">Microsoft Azure Event Grid and Microsoft Teams</span></span>

<span data-ttu-id="a16b9-163">Kun Dynamics 365 Human Resources -sovelluksen ilmoitusominaisuus on käytössä Teamsissa, tietyt asiakastiedot siirtyvät sen maantieellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="a16b9-163">When using the notifications feature for the Dynamics 365 Human Resources app in Teams, certain customer data will flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span> <span data-ttu-id="a16b9-164">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="a16b9-164">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="a16b9-165">Näitä tietoja voidaan tallentaa enintään 24 tunnin ajan. Tiedot käsitellä Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="a16b9-165">This data may be stored for up to 24 hours and processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span>

## <a name="see-also"></a><span data-ttu-id="a16b9-166">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="a16b9-166">See also</span></span> 

[<span data-ttu-id="a16b9-167">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="a16b9-167">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="a16b9-168">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="a16b9-168">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="a16b9-169">Lomapyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="a16b9-169">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

