---
title: Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä
description: Tässä aiheessa kuvataan, kuinka tehtävänhallinta synkronoidaan Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 74d53a850113c83979fba6baa4ff3c3e5d9ca02d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020624"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a><span data-ttu-id="e6c59-103">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="e6c59-103">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6c59-104">Tässä aiheessa kuvataan, kuinka tehtävänhallinta synkronoidaan Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä.</span><span class="sxs-lookup"><span data-stu-id="e6c59-104">This topic describes how to synchronize task management between Microsoft Teams and Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="e6c59-105">Teamsin integroinnin päätatarkoituksia on mahdollistaa tehtävänhallinnan synkronointi myyntipistesovelluksen ja Teamsin välillä.</span><span class="sxs-lookup"><span data-stu-id="e6c59-105">One of the main purposes of Teams integration is to enable the synchronization of task management between the POS application and Teams.</span></span> <span data-ttu-id="e6c59-106">Näin myymälän työntekijät voivat hallita tehtäviä myyntipistesovelluksen tai Teamsin avulla, eikä heidän tarvitse vaihtaa sovellusta.</span><span class="sxs-lookup"><span data-stu-id="e6c59-106">In this way, store employees can use either the POS application or Teams to manage tasks, and don't have to switch applications.</span></span>

<span data-ttu-id="e6c59-107">Koska Planneria käytetään Teamsin tehtävien tietovarastona, Teamsin ja Dynamics 365 Commercen välillä on oltava linkki.</span><span class="sxs-lookup"><span data-stu-id="e6c59-107">Because Planner is used as a repository for tasks in Teams, there must be a link between Teams and Dynamics 365 Commerce.</span></span> <span data-ttu-id="e6c59-108">Tämä linkki voidaan luoda käyttämällä tietylle myymäläryhmälle tiettyä suunnitelman tunnusta.</span><span class="sxs-lookup"><span data-stu-id="e6c59-108">This link is established by using a specific plan ID for a given store team.</span></span>

<span data-ttu-id="e6c59-109">Seuraavissa menettelyissä näytetään, miten tehtävähallinnan synkronointi määritetään myyntipisteen ja Teams-sovellusten välillä.</span><span class="sxs-lookup"><span data-stu-id="e6c59-109">The following procedures show how to set up task management synchronization between the POS and Teams applications.</span></span>

## <a name="publish-a-test-task-list-in-teams"></a><span data-ttu-id="e6c59-110">Testitehtäväluettelon julkaiseminen Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e6c59-110">Publish a test task list in Teams</span></span>

<span data-ttu-id="e6c59-111">Seuraavissa ohjeissa oletetaan, että myymälätiimit käyttävät Commercen ja Microsoft Teamsin tehtävien hallinnan integrointia ensimmäistä kertaa.</span><span class="sxs-lookup"><span data-stu-id="e6c59-111">The following procedure assumes that your store teams are using Microsoft Teams task management integration with Commerce for the first time.</span></span>

<span data-ttu-id="e6c59-112">Voit julkaista testitehtäväluettelon Teamsissa noudattamalla seuraavia vaiheita.</span><span class="sxs-lookup"><span data-stu-id="e6c59-112">To publish a test task list in Teams, follow these steps.</span></span>

1. <span data-ttu-id="e6c59-113">Kirjaudu Teamsiin viestintäpäällikkönä.</span><span class="sxs-lookup"><span data-stu-id="e6c59-113">Sign in to Teams as a communications manager.</span></span> <span data-ttu-id="e6c59-114">Viestintäpäälliköt ovat yleensä käyttäjiä, joilla on Commercessa **aluepäällikön** rooli.</span><span class="sxs-lookup"><span data-stu-id="e6c59-114">Typically, communications managers are users who have the **Regional manager** role in Commerce.</span></span>
1. <span data-ttu-id="e6c59-115">Valitse vasemmanpuoleisesta siirtymisruudusta **Plannerin tehtävät**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-115">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="e6c59-116">Valitse **Julkaisut luettelot** -välilehden vasemmassa alakulmassa **Uusi luettelo** ja nimeä uusi luettelon nimellä **Testitehtäväluettelo**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-116">On the **Published lists** tab, select **New list** in the lower left, and name the new list **Test task list**.</span></span>
1. <span data-ttu-id="e6c59-117">Valitse **Luo**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-117">Select **Create**.</span></span> <span data-ttu-id="e6c59-118">Uusi luettelo näkyy **Luonnokset**-kohdassa.</span><span class="sxs-lookup"><span data-stu-id="e6c59-118">The new list appears under **Drafts**.</span></span>
1. <span data-ttu-id="e6c59-119">Anna **Tehtävän otsikko** -kohdassa ensimmäisen tehtävän otsikoksi **Teams-integroinnin testaus**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-119">Under **Task title**, give the first task the title **Testing Teams integration**.</span></span> <span data-ttu-id="e6c59-120">Valitse sitten **Syötä**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-120">Then select **Enter**.</span></span>
1. <span data-ttu-id="e6c59-121">Valitse tehtäväluettelo **Luonnos**-luettelosta.</span><span class="sxs-lookup"><span data-stu-id="e6c59-121">In the **Drafts** list, select the task list.</span></span> <span data-ttu-id="e6c59-122">Valitse sitten oikeasta yläkulmasta  **Julkaise** .</span><span class="sxs-lookup"><span data-stu-id="e6c59-122">Then select **Publish** in the upper-right corner.</span></span>
1. <span data-ttu-id="e6c59-123">Valitse **Valitse kenelle julkaistaan** -valintaikkunassa ryhmät, joiden tulisi vastaanottaa testitehtäväluettelo.</span><span class="sxs-lookup"><span data-stu-id="e6c59-123">In the **Select who to publish to** dialog box, select the teams that should receive the test task list.</span></span>
1. <span data-ttu-id="e6c59-124">Tarkista julkaisusuunnitelma valitsemalla **Seuraava**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-124">Select **Next** to review your publication plan.</span></span> <span data-ttu-id="e6c59-125">Jos muutoksia on tehtävä, valitse  **Takaisin**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-125">If you must make changes, select **Back**.</span></span> 
1. <span data-ttu-id="e6c59-126">Valitse **Jatka vahvistamalla** ja valitse sitten **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-126">Select **Confirm to proceed**, and then select **Publish**.</span></span>
1. <span data-ttu-id="e6c59-127">Kun julkaisu on valmis, **Julkaistut luettelot** -välilehden yläosassa oleva sanoma ilmaisee, onko tehtäväluettelo toimitettu onnistuneesti.</span><span class="sxs-lookup"><span data-stu-id="e6c59-127">After publishing is completed, a message at the top of the **Published lists** tab indicates whether your task list was successfully delivered.</span></span>

<span data-ttu-id="e6c59-128">Lisätietoja on kohdassa [Organisaation töiden luonti ja seuranta tehtäväluetteloita julkaisemalla](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span><span class="sxs-lookup"><span data-stu-id="e6c59-128">For more information, see [Publish task lists to create and track work in your organization](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).</span></span>

## <a name="link-pos-and-teams-for-task-management"></a><span data-ttu-id="e6c59-129">Myyntipisteen ja Teamsin linkitäminen tehtävien hallintaa varten</span><span class="sxs-lookup"><span data-stu-id="e6c59-129">Link POS and Teams for task management</span></span>

<span data-ttu-id="e6c59-130">Noudattamalla seuraavia ohjeita voit linkittää myyntipisteen ja Microsoft Teamsin tehtävien hallitsemiseksi Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="e6c59-130">To link the POS and Microsoft Teams applications for task management in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="e6c59-131">Siirry kohtaan **Retail ja Commerce \> Tehtävien hallinta \> Tehtävien integrointi Microsoft Teamsin kanssa**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-131">Go to **Retail and Commerce \> Task management \> Tasks integration with Microsoft Teams**.</span></span>
1. <span data-ttu-id="e6c59-132">Valitse toimintoruudussa **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-132">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e6c59-133">Määritä **Ota tehtävienhallinnan integrointi käyttöön** -asetukseksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-133">Set the **Enable Task Management Integration** option to **Yes**.</span></span>
1. <span data-ttu-id="e6c59-134">Valitse toimintoruudussa **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-134">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e6c59-135">Valitse toimintoruudussa **Määritä tehtävien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-135">On the Action Pane, select **Setup task management**.</span></span> <span data-ttu-id="e6c59-136">Näyttöön tulee ilmoitus, joka ilmaisee, että luodaan erätyötä, jonka nimi **Teamsin valmistelu**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-136">You should receive a notification that indicates that a batch job that is named **Teams provision** is being created.</span></span>
1. <span data-ttu-id="e6c59-137">Siirry kohtaan **Järjestelmänvalvonta \> Kyselyt \> Erätyöt** ja etsi uusin työ, jolla on nimi **Teamsin valmistelu**.</span><span class="sxs-lookup"><span data-stu-id="e6c59-137">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="e6c59-138">Odota tämän työn valmistumista.</span><span class="sxs-lookup"><span data-stu-id="e6c59-138">Wait until this job has finished running.</span></span>
1. <span data-ttu-id="e6c59-139">Suorita **CDX-työ 1070**, kun haluat julkaista suunnitelman tunnuksen ja myymälän viitteet Retail Serveriin.</span><span class="sxs-lookup"><span data-stu-id="e6c59-139">Run the **CDX job 1070** to publish the plan ID and store references to Retail Server.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6c59-140">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e6c59-140">Additional resources</span></span>

[<span data-ttu-id="e6c59-141">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="e6c59-141">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="e6c59-142">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="e6c59-142">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="e6c59-143">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="e6c59-143">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="e6c59-144">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="e6c59-144">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="e6c59-145">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="e6c59-145">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="e6c59-146">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="e6c59-146">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
