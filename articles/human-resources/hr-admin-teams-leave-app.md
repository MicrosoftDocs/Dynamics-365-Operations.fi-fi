---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889737"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="83c32-103">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="83c32-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83c32-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="83c32-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="83c32-105">Työntekijät voivat pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="83c32-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="83c32-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="83c32-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="83c32-107">Lisäksi lähettää tietoja tulevista poissaoloista voidaan lähettää ryhmissä ja keskusteluissa Human Resources -sovelluksen ulkopuolella.</span><span class="sxs-lookup"><span data-stu-id="83c32-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Human Resources Teamsin lomasovelluksen botti](./media/hr-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resourcesin lomapyyntökortti](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="83c32-111">Asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="83c32-111">Install and setup</span></span>

<span data-ttu-id="83c32-112">Löydät Dynamics 365 Human Resources -sovelluksen Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="83c32-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="83c32-113">Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="83c32-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="83c32-114">Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="83c32-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="83c32-115">Jos haluat käyttäjien näkevän loma- ja poissaolokalenterin sovelluksessa, sinun on täytyy ottaa **Loma- ja poissaolokalenteri Teamsissa** -ominaisuus käyttöön ominaisuuksien hallinnasta.</span><span class="sxs-lookup"><span data-stu-id="83c32-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="83c32-116">Lisätietoja ominaisuuksien käyttöönotosta on kohdassa [Ominaisuuksien hallinta](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="83c32-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="83c32-117">Ilmoitusten käyttöönotto Teamsin Human Resources -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="83c32-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="83c32-118">Jos haluat, että käyttäjät voivat vastaanottaa lomapyyntöjen ilmoituksia Teams-sovelluksessa, sinun täytyy ottaa ilmoitukset käyttöön Dynamics 365 Human Resources -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="83c32-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="83c32-119">Vain Teamsiin kirjautuneet käyttäjät, jotka käyttävät Dynamics 365 Human Resources Teams -sovellusta, vastaanottavat ilmoituksia.</span><span class="sxs-lookup"><span data-stu-id="83c32-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="83c32-120">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="83c32-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="83c32-121">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="83c32-121">Select **Links**.</span></span>

3. <span data-ttu-id="83c32-122">Valitse **Asetukset**-kohdassa **Järjestelmäparametrit**.</span><span class="sxs-lookup"><span data-stu-id="83c32-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="83c32-123">Määritä **Yleistä**-välilehdessä **Ota käyttöön Teams-sovelluksen ilmoitukset** -kohdan arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="83c32-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto järjestelmäparametreissa](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="83c32-125">Jos haluat ottaa Teams-ilmoitukset käyttöön kaikille käyttäjille, valitse **Kyllä** pyydettäessä.</span><span class="sxs-lookup"><span data-stu-id="83c32-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Teams-ilmoitusten käyttöönotto kaikille käyttäjille](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="83c32-127">Teams-ilmoitusten ottaminen käyttöön tai poistaminen käytöstä yksittäisille käyttäjille</span><span class="sxs-lookup"><span data-stu-id="83c32-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="83c32-128">Kun olet ottanut ilmoitukset käyttöön Dynamics 365 Human Resources Teams -sovelluksessa, voit ottaa ilmoitukset käyttöön tai poistaa ne käytöstä yksittäisille käyttäjille.</span><span class="sxs-lookup"><span data-stu-id="83c32-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="83c32-129">Valitse Human Resourcesissa **Järjestelmän hallinta**.</span><span class="sxs-lookup"><span data-stu-id="83c32-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="83c32-130">Valitse **Linkit**.</span><span class="sxs-lookup"><span data-stu-id="83c32-130">Select **Links**.</span></span>

3. <span data-ttu-id="83c32-131">**Valitse käyttäjät** -kohdasta **Käyttäjän asetukset**.</span><span class="sxs-lookup"><span data-stu-id="83c32-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="83c32-132">Valitse **Työnkulku**-välilehti.</span><span class="sxs-lookup"><span data-stu-id="83c32-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="83c32-133">Määritä **Teams-sovelluksen Salli ilmoitukset** -kohdan arvoksi **Kyllä**, jos haluat ottaa ilmoitukset käyttöön käyttäjälle. Valitse **Ei**, jos haluat poistaa käyttäjän ilmoitukset käytöstä.</span><span class="sxs-lookup"><span data-stu-id="83c32-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Teams-sovelluksen ilmoitusten käyttöönotto käyttäjän asetusten Työnkulku-välilehdessä](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="83c32-135">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="83c32-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="83c32-136">Tuetut kielet</span><span class="sxs-lookup"><span data-stu-id="83c32-136">Supported languages</span></span>

<span data-ttu-id="83c32-137">Teamsin Dynamics 365 Human Resources -sovellus tukee seuraavia kieliä:</span><span class="sxs-lookup"><span data-stu-id="83c32-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="83c32-138">Kielialueen tunnus</span><span class="sxs-lookup"><span data-stu-id="83c32-138">Locale ID</span></span> | <span data-ttu-id="83c32-139">Kieli</span><span class="sxs-lookup"><span data-stu-id="83c32-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="83c32-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="83c32-140">de-DE</span></span> | <span data-ttu-id="83c32-141">saksa (Saksa)</span><span class="sxs-lookup"><span data-stu-id="83c32-141">German (Germany)</span></span> |
| <span data-ttu-id="83c32-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="83c32-142">es-ES</span></span> | <span data-ttu-id="83c32-143">espanja (Espanja)</span><span class="sxs-lookup"><span data-stu-id="83c32-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="83c32-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="83c32-144">es-MX</span></span> | <span data-ttu-id="83c32-145">espanja (Meksiko)</span><span class="sxs-lookup"><span data-stu-id="83c32-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="83c32-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="83c32-146">fr-CA</span></span> | <span data-ttu-id="83c32-147">ranska (Kanada)</span><span class="sxs-lookup"><span data-stu-id="83c32-147">French (Canada)</span></span> |
| <span data-ttu-id="83c32-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="83c32-148">fr-FR</span></span> | <span data-ttu-id="83c32-149">ranska (Ranska)</span><span class="sxs-lookup"><span data-stu-id="83c32-149">French (France)</span></span> |
| <span data-ttu-id="83c32-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="83c32-150">it-IT</span></span> | <span data-ttu-id="83c32-151">italia (Italia)</span><span class="sxs-lookup"><span data-stu-id="83c32-151">Italian (Italy)</span></span> |
| <span data-ttu-id="83c32-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="83c32-152">nl-NL</span></span> | <span data-ttu-id="83c32-153">hollanti (Alankomaat)</span><span class="sxs-lookup"><span data-stu-id="83c32-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="83c32-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="83c32-154">pt-BR</span></span> | <span data-ttu-id="83c32-155">portugali (Brasilia)</span><span class="sxs-lookup"><span data-stu-id="83c32-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="83c32-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="83c32-156">tr-TR</span></span> | <span data-ttu-id="83c32-157">turkki (Turkki)</span><span class="sxs-lookup"><span data-stu-id="83c32-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="83c32-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="83c32-158">zh-CN</span></span> | <span data-ttu-id="83c32-159">kiina (yksinkertaistettu)</span><span class="sxs-lookup"><span data-stu-id="83c32-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="83c32-160">Muistiinpanot</span><span class="sxs-lookup"><span data-stu-id="83c32-160">Notes</span></span>

<span data-ttu-id="83c32-161">Seuraavat työnimikkeet on ajoitettu tulevia julkaisuja varten:</span><span class="sxs-lookup"><span data-stu-id="83c32-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="83c32-162">Työnimike</span><span class="sxs-lookup"><span data-stu-id="83c32-162">Work item</span></span> | <span data-ttu-id="83c32-163">Tila</span><span class="sxs-lookup"><span data-stu-id="83c32-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="83c32-164">Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo.</span><span class="sxs-lookup"><span data-stu-id="83c32-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="83c32-165">Ennakointi ei ole vielä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="83c32-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="83c32-166">Saldo näkyy kuluvalta päivältä.</span><span class="sxs-lookup"><span data-stu-id="83c32-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="83c32-167">**Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="83c32-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="83c32-168">Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="83c32-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="83c32-169">Saldotiedot lasketaan kuluvasta päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="83c32-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="83c32-170">Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa.</span><span class="sxs-lookup"><span data-stu-id="83c32-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="83c32-171">Vianmääritys</span><span class="sxs-lookup"><span data-stu-id="83c32-171">Troubleshooting</span></span>

<span data-ttu-id="83c32-172">Jos käyttäjällä on vaikeuksia Human Resources Teams -sovellukseen kirjautumisessa tai sen käyttämisessä, seuraavat vianmääritysohjeet voivat olla hyödyllisiä.</span><span class="sxs-lookup"><span data-stu-id="83c32-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="83c32-173">Jos ongelmat jatkuvat vianmäärityksen jälkeen, ota yhteys tukeen.</span><span class="sxs-lookup"><span data-stu-id="83c32-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="83c32-174">Lisätietoja on kohdassa [Pyydä tukea](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="83c32-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="83c32-175">Kirjautuminen Human Resources -sovelluksen ei onnistu Teamsissa</span><span class="sxs-lookup"><span data-stu-id="83c32-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="83c32-176">Jos käyttäjä ottaa yhteyttä, koska hän ei pysty kirjautumaan sovellukseen, tarkista, että hänellä on työntekijätietue Human Resourcesissa.</span><span class="sxs-lookup"><span data-stu-id="83c32-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="83c32-177">Virhe hyväksyttäessä lomapyyntöjä Human Resources -sovelluksessa Teamsissa</span><span class="sxs-lookup"><span data-stu-id="83c32-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="83c32-178">Jos käyttäjä saa virheilmoituksen yrittäessään hyväksyä lomapyyntöjä Teams-sovelluksessa, kokeile seuraavaa vianmääritystä:</span><span class="sxs-lookup"><span data-stu-id="83c32-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="83c32-179">Tarkista, että käyttäjän Teams-tili on sama tili, jolla käyttäjä käyttää Human Resourcesiin.</span><span class="sxs-lookup"><span data-stu-id="83c32-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="83c32-180">Tarkista myös, että käyttäjä saa hyväksyä pyynnön. Voit tehdä tämän loman hyväksymistyönkulun asetuksissa.</span><span class="sxs-lookup"><span data-stu-id="83c32-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="83c32-181">Lisätietoja lomapyyntöjen työnkulusta on kohdassa [Lomapyyntötyönkulun luominen](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="83c32-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="83c32-182">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="83c32-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="83c32-183">Microsoftin Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="83c32-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="83c32-184">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="83c32-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="83c32-185">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="83c32-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="83c32-186">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="83c32-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="83c32-187">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="83c32-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="83c32-188">Nämä tiedot välitetään sitten Microsoftin  [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/), joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="83c32-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="83c32-189">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="83c32-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="83c32-190">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="83c32-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="83c32-191">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="83c32-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="83c32-192">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="83c32-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="83c32-193">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="83c32-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="83c32-194">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="83c32-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="83c32-195">Microsoft Teams, Azure-tapahtumaverkko ja Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="83c32-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="83c32-196">Kun Dynamics 365 Human Resources -sovellus on käytössä Microsoft Teamsissä, tietyt asiakastiedot voivat siirtyä sen maantieteellisen alueen ulkopuolelle, jossa vuokraajan Human Resources -palvelua käytetään.</span><span class="sxs-lookup"><span data-stu-id="83c32-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="83c32-197">Dynamics 365 Human Resources lähettää työntekijän lomapyynnön ja työnkulun tehtävän tiedot Microsoft Azuren tapahtumaruudukkoon ja Microsoft Teamsille.</span><span class="sxs-lookup"><span data-stu-id="83c32-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="83c32-198">Näitä tietoja voidaan tallentaa Microsoft Azure -tapahtumaverkossa enintään 24 tunnin ajan. Tiedot käsitellään Yhdysvalloissa ja ne salataan siirron ja tallennuksen aikana. Microsoft tai sen alihankkijat eivät käytä tietoja koulutuksessa tai palvelun parantamisessa.</span><span class="sxs-lookup"><span data-stu-id="83c32-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="83c32-199">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="83c32-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="83c32-200">Keskusteltaessa Human Resources -sovelluksen keskustelubotin kanssa keskustelun sisältö saatetaan tallentaa Azuren Cosmos DB:hen ja lähettää Microsoft Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="83c32-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="83c32-201">Nämä tiedot voidaan tallentaa Azuren Cosmos DB:hen enintään 24 tunniksi, ja niitä voidaan käsitellä sen maantieteellisen alueen ulkopuolella, jossa vuokralaisen Human Resources -palvelu on otettu käyttöön. Tiedot salataan siirrettäessä ja levossa, eikä Microsoft tai sen alihankkija käytä niitä koulutuksiin tai palvelujen parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="83c32-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="83c32-202">Tietoja siitä, mihin tietosi tallennetaan Teamsissä: [Tietojen sijainti Microsoft Teamsissä](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="83c32-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="83c32-203">Ohjeet Human Resources -sovelluksen käyttöoikeuksien rajoittamiseen Microsoft Teamsissä organisaatiosi tai sen käyttäjien osalta: [Sovellusten oikeuskäytäntöjen hallinta Microsoft Teamsissä](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="83c32-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="83c32-204">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="83c32-204">See also</span></span> 

[<span data-ttu-id="83c32-205">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="83c32-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="83c32-206">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="83c32-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="83c32-207">Lomapyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="83c32-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]