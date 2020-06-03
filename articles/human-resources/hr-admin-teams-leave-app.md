---
title: Teamsin Human Resources -sovellus
description: Tässä ohjeaiheessa käsitellään Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovellusta.
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
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388113"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="e09eb-103">Teamsin Human Resources -sovellus</span><span class="sxs-lookup"><span data-stu-id="e09eb-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e09eb-104">Microsoft Teamsin Microsoft Dynamics 365 Human Resources -sovelluksen avulla työntekijät voivat tehdä nopeasti poissaolopyyntöjä ja tarkastella poissaolosaldonsa tietoja Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="e09eb-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="e09eb-105">Työntekijät voivat pyytää tietoja botin avustuksella.</span><span class="sxs-lookup"><span data-stu-id="e09eb-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="e09eb-106">**Poissaolo**-välilehdessä on lisätietoja.</span><span class="sxs-lookup"><span data-stu-id="e09eb-106">The **Time off** tab provides more detailed information.</span></span>

![Human Resources Teamsin lomasovelluksen botti](./media/hr-admin-teams-leave-app-bot.png)

![Human Resources Teamsin lomasovelluksen Poissaolo-välilehti](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="e09eb-109">Asentaminen ja määrittäminen</span><span class="sxs-lookup"><span data-stu-id="e09eb-109">Install and setup</span></span>

<span data-ttu-id="e09eb-110">Human Resources -sovellus löytyy Teams-kaupasta.</span><span class="sxs-lookup"><span data-stu-id="e09eb-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="e09eb-111">Lisätietoja Teams-sovelluksen asentamisesta on kohdassa [Lomapyyntöjen hallinta Teamsissa](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="e09eb-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="e09eb-112">Lisätietoja sovellusten käyttöoikeuksien hallinnasta Teamsissa on kohdassa [Sovellusten käyttöoikeuskäytäntöjen hallinta Microsoft Teamsissa](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="e09eb-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="e09eb-113">Tunnetut ongelmat</span><span class="sxs-lookup"><span data-stu-id="e09eb-113">Known issues</span></span>

| <span data-ttu-id="e09eb-114">Otto</span><span class="sxs-lookup"><span data-stu-id="e09eb-114">Issue</span></span> | <span data-ttu-id="e09eb-115">Tila</span><span class="sxs-lookup"><span data-stu-id="e09eb-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="e09eb-116">Saldo on virheellinen, kun lähetetään tulevaisuudessa olevaa päivämäärää koskeva poissaolo.</span><span class="sxs-lookup"><span data-stu-id="e09eb-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="e09eb-117">Ennakointi ei ole vielä käytettävissä.</span><span class="sxs-lookup"><span data-stu-id="e09eb-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="e09eb-118">Saldo näkyy kuluvalta päivältä.</span><span class="sxs-lookup"><span data-stu-id="e09eb-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="e09eb-119">Kun aiemmin luodussa pyynnössä olevien tuntien määrää vähennetään, **Jäljellä jäävä saldo** pienenee eikä suurene.</span><span class="sxs-lookup"><span data-stu-id="e09eb-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="e09eb-120">Tämä tunnettu ongelma otetaan huomioon tulevaisuudessa.</span><span class="sxs-lookup"><span data-stu-id="e09eb-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="e09eb-121">Näyttö on virheellinen, mutta summat oikaistaan lähetyksen yhteydessä.</span><span class="sxs-lookup"><span data-stu-id="e09eb-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="e09eb-122">Samoille päivämäärille näkyy kaksi **Tuleva poissaolo** -korttia.</span><span class="sxs-lookup"><span data-stu-id="e09eb-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="e09eb-123">Kortit ilmaisevat yksittäiset lähetykset.</span><span class="sxs-lookup"><span data-stu-id="e09eb-123">The cards represent individual submissions.</span></span> <span data-ttu-id="e09eb-124">Palautetta otetaan edelleen vastaan ja muutoksia tehdään.</span><span class="sxs-lookup"><span data-stu-id="e09eb-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="e09eb-125">**Tarkistuksessa**-tilassa olevaa pyyntöä ei voi peruuttaa.</span><span class="sxs-lookup"><span data-stu-id="e09eb-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="e09eb-126">Tätä toimintoa ei tällä hetkellä tueta ja se lisätään tulevaan julkaisuun.</span><span class="sxs-lookup"><span data-stu-id="e09eb-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="e09eb-127">Saldotiedot lasketaan kuluvasta päivästä alkaen.</span><span class="sxs-lookup"><span data-stu-id="e09eb-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="e09eb-128">Järjestelmä ei tällä hetkellä näytä jaksotuskauden saldoa, vaikka se on määritetty loma- ja poissaoloparametreissa.</span><span class="sxs-lookup"><span data-stu-id="e09eb-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="e09eb-129">Tietosuojatiedot</span><span class="sxs-lookup"><span data-stu-id="e09eb-129">Privacy notice</span></span>

<span data-ttu-id="e09eb-130">Microsoft Teamsin Dynamics 365 Human Resources -botin avulla käyttäjän tekstinsyöttö analysoidaan, jotta taustalla oleva kysely tai tarkoitus saataisiin selville.</span><span class="sxs-lookup"><span data-stu-id="e09eb-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="e09eb-131">Käyttäjän teksti, kuten Hae tili Contoso, reititetään yhteen Microsoftin kognitiiviseen palveluun, jonka nimi on Language Understanding Intelligent Service (LUIS).</span><span class="sxs-lookup"><span data-stu-id="e09eb-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="e09eb-132">Lisätietoja LUIS-palvelusta on  [täällä](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="e09eb-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="e09eb-133">LUIS-palvelu tulkitsee tai selvittää käyttäjän syötteen tarkoituksen (tässä tapauksessa tarkoituksena on etsiä tietoja) ja kohde-entiteetin (tässä tapauksessa tarkoitettu entiteetti on Contoso-niminen tili).</span><span class="sxs-lookup"><span data-stu-id="e09eb-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="e09eb-134">Nämä tiedot välitetään sitten Microsoftin [Azure-bottikehykseen](https://azure.microsoft.com/services/bot-service/) , joka käyttää Dynamics 365 Human Resourcesin tietoja ja noutaa käyttäjän kyselyn haluamat tiedot.</span><span class="sxs-lookup"><span data-stu-id="e09eb-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="e09eb-135">Asentamalla botin ja sallimalla sen käytön hyväksyt sen, että LUIS-palvelu ja Azure-bottikehys käsittelevät syötteen varsinaisen tarkoituksen, mikä parantaa käyttäjän keskustelukokemusta.</span><span class="sxs-lookup"><span data-stu-id="e09eb-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="e09eb-136">LUIS-palvelun ja Azure-bottikehyksen vaatimustenmukaisuustasot voivat vaihdella Dynamics 365 Human Resourcesiin verrattuna.</span><span class="sxs-lookup"><span data-stu-id="e09eb-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="e09eb-137">Vaikka LUIS-palvelu voi käyttää vain käyttäjäkyselyitä eikä sitä ole suunniteltu muodostamaan yhteyttä käyttäjän Dynamics 365 Human Resources -tietoihin tai -tiliin, Dynamics 365 Human Resources -botin käyttäjä voi vapaaehtoisesti tehdä kyselyn, joka sisältää asiakastietoja, henkilökohtaisia tietoja tai muita vastaavia tietoja ja kyseinen kysely voi tulla lähetetyksi LUIS-palveluun ja Azure-bottikehykseen.</span><span class="sxs-lookup"><span data-stu-id="e09eb-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="e09eb-138">Käyttäjän kyselyjen ja viestien sisältöä säilytetään LUIS-järjestelmässä enintään 30 päivää. Nämä tiedot salataan eikä niitä käytetä koulutuksen tai palvelun parantamiseen.</span><span class="sxs-lookup"><span data-stu-id="e09eb-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="e09eb-139">Lisätietoja kognitiivisista palveluista on  [täällä](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="e09eb-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="e09eb-140">Microsoft Teamsin sovellusten järjestelmänvalvojan asetuksia hallitaan [Microsoft Teams -hallintakeskuksessa](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="e09eb-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="e09eb-141">Lisätietoja</span><span class="sxs-lookup"><span data-stu-id="e09eb-141">See also</span></span> 

[<span data-ttu-id="e09eb-142">Microsoft Teamsin lataaminen ja asentaminen</span><span class="sxs-lookup"><span data-stu-id="e09eb-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="e09eb-143">Microsoft Teamsin ohje- ja tukikeskus</span><span class="sxs-lookup"><span data-stu-id="e09eb-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="e09eb-144">Loma- ja poissaolopyyntöjen hallinta Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e09eb-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

