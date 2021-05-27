---
title: Microsoft Teamsin valmistelu Dynamics 365 Commercesta
description: Tässä aiheessa kuvataan, miten Microsoft Teams voidaan valmistella käyttäen organisaatiotietoja Dynamics 365 Commercesta.
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
ms.openlocfilehash: 1cb28fb50bdc972d1dae6d03a45f70a2f3a63357
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022443"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="814b8-103">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="814b8-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="814b8-104">Tässä aiheessa kuvataan, miten Microsoft Teams voidaan valmistella käyttäen organisaatiotietoja Dynamics 365 Commercesta.</span><span class="sxs-lookup"><span data-stu-id="814b8-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="814b8-105">Dynamics 365 Commerce tarjoaa helpon tavan määrittää Teamsin, jos et ole vielä määrittänyt vähittäismyymälöille Teamsia.</span><span class="sxs-lookup"><span data-stu-id="814b8-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="814b8-106">Käyttämällä Commercen hyvin määritettyjä tietoja, joita haluat käyttää Teamsissa, voit auttaa myymälän työntekijöitä pääsemään alkuun Teamsin käytössä.</span><span class="sxs-lookup"><span data-stu-id="814b8-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="814b8-107">Näitä tietoja ovat organisaatiohierarkia, myymälän nimet, työntekijätiedot ja Azure Active Directory (Azure AD) -tilit.</span><span class="sxs-lookup"><span data-stu-id="814b8-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="814b8-108">Teamsin varausprosessissa on kaksi päävaihetta:</span><span class="sxs-lookup"><span data-stu-id="814b8-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="814b8-109">Luo Teamsissa ryhmä kutakin vähittäismyymälää varten ja lisää myymälän työntekijöitä ryhmän jäseniksi.</span><span class="sxs-lookup"><span data-stu-id="814b8-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="814b8-110">Jos työntekijä on liitetty yhteen vähittäismyymälään, ryhmän jäsenyys vastaa tätä määritystä.</span><span class="sxs-lookup"><span data-stu-id="814b8-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="814b8-111">Luodaan viestintäryhmä, joka sisältää jäseniä aluepäälliköiksi, jotta tehtäviä voidaan julkaista Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="814b8-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="814b8-112">Lataa organisaatiohierarkia Commercesta Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="814b8-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="814b8-113">Valmistele Teams Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="814b8-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="814b8-114">Tee seuraavat toimet ennen Microsoft Teamsin valmistelua:</span><span class="sxs-lookup"><span data-stu-id="814b8-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="814b8-115">Vahvista, että kaikista aluepäälliköista on tehty viestintäpäälliköitä.</span><span class="sxs-lookup"><span data-stu-id="814b8-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="814b8-116">Vahvista, että jokaisen myymäläpäällikön ja työntekijän Azure-tili on liitetty esimiehen tai työntekijätietueeseen Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="814b8-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="814b8-117">Voit valmistella Teamsin Commerce headquarters -sovelluksessa seuraamalla alla olevia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="814b8-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="814b8-118">Siirry kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integrointimääritys**.</span><span class="sxs-lookup"><span data-stu-id="814b8-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="814b8-119">Valitse toimintoruudussa **Valmistele Teams**.</span><span class="sxs-lookup"><span data-stu-id="814b8-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="814b8-120">Luodaan erätyö, jonka nimi on **Teamsin valmistelu**.</span><span class="sxs-lookup"><span data-stu-id="814b8-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="814b8-121">Siirry kohtaan **Järjestelmänvalvonta \> Kyselyt \> Erätyöt** ja etsi uusin työ, jolla on nimi **Teamsin valmistelu**.</span><span class="sxs-lookup"><span data-stu-id="814b8-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="814b8-122">Odota tämän työn valmistumista.</span><span class="sxs-lookup"><span data-stu-id="814b8-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="814b8-123">Jos mikään aluepäälliköistä, myymäläpäälliköistä ja myymälätyöntekijöistä ei ole liitetty Teams-lisenssiin, näkyviin saattaa tulla seuraava virhesanoma: "Käyttäjän SKU-luokkien noutaminen ei onnistunut."</span><span class="sxs-lookup"><span data-stu-id="814b8-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="814b8-124">Voit korjata ongelman valitsemalla toimintoruudusta **Synkronoi ryhmät ja jäsenet**.</span><span class="sxs-lookup"><span data-stu-id="814b8-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="814b8-125">Teamsin valmistelun vahvistaminen Teams-hallintakeskuksessa</span><span class="sxs-lookup"><span data-stu-id="814b8-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="814b8-126">Suorita seuraavat vaiheet, kun haluat vahvistaa Microsoft Teamsin valmistelun Microsoft Teams -hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="814b8-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="814b8-127">Siirry [Teams-hallintakeskukseen](https://admin.teams.microsoft.com/) ja kirjaudu sisään sähköisen kaupankäynnin vuokraajan järjestelmänvalvojana.</span><span class="sxs-lookup"><span data-stu-id="814b8-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="814b8-128">Valitse vasemmassa siirtymisruudussa **Teams** laajentaaksesi sen ja valitse sitten **Ryhmien hallinta**.</span><span class="sxs-lookup"><span data-stu-id="814b8-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="814b8-129">Vahvista, että kullekin Commerce-vähittäismyymälälle on luotu yksi ryhmä.</span><span class="sxs-lookup"><span data-stu-id="814b8-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="814b8-130">Valitse ryhmä ja vahvista, että myymälän työntekijät on lisätty ryhmään jäseninä.</span><span class="sxs-lookup"><span data-stu-id="814b8-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="814b8-131">Valitse vasemmassa siirtymisruudussa **Käyttäjät** ja vahvista, että kaikkien myymälöiden kaikki myymälän työntekijät on lisätty käyttäjinä.</span><span class="sxs-lookup"><span data-stu-id="814b8-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="814b8-132">Seuraavassa kuvassa on esimerkki Teams-hallintakeskuksen **Ryhmien hallinta** -sivusta.</span><span class="sxs-lookup"><span data-stu-id="814b8-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Esimerkki Ryhmien hallinta -sivusta Teams-hallintakeskuksessa](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="814b8-134">Lataa Commercen organisaatiohierarkia Teamsiin</span><span class="sxs-lookup"><span data-stu-id="814b8-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="814b8-135">Commerce-organisaatiohierarkian avulla voit Microsoft Teamsissa julkaista tehtäviä kaikissa tai valituissa myymälöissä, jotka käyttävät samaa hierarkiarakennetta.</span><span class="sxs-lookup"><span data-stu-id="814b8-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="814b8-136">Jos haluat ladata Commerce-organisaatiohierarkian Teamsiin, toimi seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="814b8-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="814b8-137">Siirry Commerce headquartersissa kohtaan **Retail ja Commerce \> Kanavan asetukset \> Microsoft Teams -integroinnin määritys**.</span><span class="sxs-lookup"><span data-stu-id="814b8-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="814b8-138">Valitse **Lataa kohdehierarkia** ja lataa sitten organisaatiohierarkian pilkuilla erotettu CSV-tiedosto valitsemalla **Vähittäismyymälät alueen mukaan**.</span><span class="sxs-lookup"><span data-stu-id="814b8-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="814b8-139">Asenna Microsoft Teams PowerShell -moduuli noudattamalla ohjeita kohdassa [Asenna Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="814b8-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="814b8-140">Kun järjestelmä antaa kehotteen Teams PowerShell -ikkunassa, kirjaudu sisään vuokraajan järjestelmänvalvojan Azure AD-tilin avulla.</span><span class="sxs-lookup"><span data-stu-id="814b8-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="814b8-141">Lataa kohdehierarkian CSV-tiedosto palvelimeen noudattamalla ohjeita kohdassa [Ryhmän kohdehierarkian määrittäminen](/microsoftteams/set-up-your-team-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="814b8-141">Follow the steps in [Set up your team targeting hierarchy](/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="814b8-142">Tarkista, että organisaatiohierarkia on ladattu Teamsiin</span><span class="sxs-lookup"><span data-stu-id="814b8-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="814b8-143">Tarkista seuraavien vaiheiden avulla, että organisaatiohierarkia on ladattu Microsoft Teamsiin.</span><span class="sxs-lookup"><span data-stu-id="814b8-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="814b8-144">Kirjaudu Teamsiin viestintäpäällikkönä.</span><span class="sxs-lookup"><span data-stu-id="814b8-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="814b8-145">Valitse vasemmanpuoleisesta siirtymisruudusta **Plannerin tehtävät**.</span><span class="sxs-lookup"><span data-stu-id="814b8-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="814b8-146">Luo **Julkaisut luettelot** -välilehdessä uusi luettelo, jolla on tyhjä tehtävä.</span><span class="sxs-lookup"><span data-stu-id="814b8-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="814b8-147">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="814b8-147">Select **Publish**.</span></span> <span data-ttu-id="814b8-148">Organisaatiohierarkian pitäisi näkyä **Valitse kenelle julkaistaan** -valintaikkunassa seuraavan kuvan esimerkin mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="814b8-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Esimerkki organisaatiohierarkiasta Valitse kenelle julkaistaan -valintaikkunassa](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="814b8-150">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="814b8-150">Additional resources</span></span>

[<span data-ttu-id="814b8-151">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="814b8-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="814b8-152">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="814b8-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="814b8-153">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="814b8-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="814b8-154">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="814b8-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="814b8-155">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="814b8-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="814b8-156">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="814b8-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)