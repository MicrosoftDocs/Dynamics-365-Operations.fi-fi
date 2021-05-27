---
title: Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on vastauksia Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointia koskeviin usein kysyttyihin kysymyksiin.
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
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019467"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="01952-103">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="01952-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="01952-104">Tässä ohjeaiheessa on vastauksia Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integrointia koskeviin usein kysyttyihin kysymyksiin.</span><span class="sxs-lookup"><span data-stu-id="01952-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="01952-105">Kenestä myymälästä tulee ryhmän omistaja, kun Teams valmistellaan Commercesta?</span><span class="sxs-lookup"><span data-stu-id="01952-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="01952-106">Kaikki myymäläpäälliköt lisätään automaattisesti omistajiksi vastaavaan ryhmään, jotta he voivat suorittaa toimintoja, kuten lisätä yksityisen kanavan ja lisätä tai poistaa jäseniä.</span><span class="sxs-lookup"><span data-stu-id="01952-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="01952-107">Miten voin määrittää viestintäpäällikön roolin työntekijälle Commerce headquartersissa?</span><span class="sxs-lookup"><span data-stu-id="01952-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="01952-108">Viestintäpäälliköt Microsoft Teamsissa voivat luoda ja julkaista tehtäväluetteloita.</span><span class="sxs-lookup"><span data-stu-id="01952-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="01952-109">Organisaation työntekijöille, joiden on määrä tulla viestintäpäälliköksi, on oltava vähittäismyynnin tehtävienhallinnan rooli Commerce headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="01952-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="01952-110">Liitä vähittäismyynnin tehtävienhallinnan rooli työntekijään Commerce headquartersissa noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="01952-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="01952-111">Siirry kohtaan **Vähittäismyynti ja kauppa \> Työntekijät \> Käyttäjät**.</span><span class="sxs-lookup"><span data-stu-id="01952-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="01952-112">Valitse työntekijä.</span><span class="sxs-lookup"><span data-stu-id="01952-112">Select an employee.</span></span>
1. <span data-ttu-id="01952-113">Valitse **Käyttäjän roolit** -pikavälilehdessä **Määritä roolit**.</span><span class="sxs-lookup"><span data-stu-id="01952-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="01952-114">Valitse **Määritä roolit käyttäjälle** -valintaikkunassa **vähittäismyynnin tehtävienhallinnan** rooli ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="01952-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="01952-115">Miten tietty organisaatiohierarkia voidaan ladata Microsoft Teamsiin?</span><span class="sxs-lookup"><span data-stu-id="01952-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="01952-116">Commerce headquartersissa jokaisen organisaation hierarkia liittyy vähintään yhteen tarkoitukseen.</span><span class="sxs-lookup"><span data-stu-id="01952-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="01952-117">Varmista, että hierarkiaan, jonka haluat valmistella Microsoft Teamsiin, on liitetty **vähittäismyynnin raportoinnin** tarkoitus seuraavan esimerkkikuvan mukaisesti.</span><span class="sxs-lookup"><span data-stu-id="01952-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Esimerkki organisaatiohierarkian tarkoituksesta Commerce headquartersissa](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="01952-119">Miten sallin vähittäismyynnin työntekijöiden kirjautumisen Commerce-myyntipisteeseen Azure Active Directory (Azure AD) -todennuksella?</span><span class="sxs-lookup"><span data-stu-id="01952-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="01952-120">Lisätietoja Commerce-myyntipisteen kirjautumiskokemuksen määrittämisestä Azure AD-todennukseen on kohdassa [Ota Azure Active Directory -todennus käyttöön myyntipisteen kirjautumisessa](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="01952-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="01952-121">Miten myymälöiden ja niitä vastaavien ryhmien määritys Commerce headquarters -sovelluksessa toimii, jos organisaationi on jo luonut ryhmiä Microsoft Teamsissa?</span><span class="sxs-lookup"><span data-stu-id="01952-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="01952-122">Lisätietoja myymälöiden ja ryhmien yhdistämisestä, jos ryhmiä on aiemmin luotu, on kohdassa [Myymälöiden ja vastaavien ryhmien yhdistäminen, jos organisaatiossasi on aiemmin luotuja ryhmiä Microsoft Teamsissa](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="01952-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="01952-123">Miten poistan istunnon tallennustilaan tallennetun Microsoft Graph API -tunnuksen?</span><span class="sxs-lookup"><span data-stu-id="01952-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="01952-124">Käyttäjän, joka on kirjautunut myyntipisteeseen (POS) Azure Active Directory (Azure AD) tilillä, on kirjauduttava ulos myyntipisteestä tai suljettava sovellus tyhjentääkseen istunnon tallennustilan.</span><span class="sxs-lookup"><span data-stu-id="01952-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="01952-125">Suositeltava käytäntö on, että myymälätyöntekijät lukitsevat kassapäätteen tai kirjautuvat ulos istunnosta silloin, kun päätettä ei käytetä.</span><span class="sxs-lookup"><span data-stu-id="01952-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="01952-126">Mitä tapahtuu, jos myymälällä ei ole myymäläpäälliköitä?</span><span class="sxs-lookup"><span data-stu-id="01952-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="01952-127">Jos myymälällä ei ole päälliköitä, ryhmää ei luoda myymälälle tai Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="01952-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="01952-128">Mitä tapahtuu, jos myymäläpäällikkö lähtee yrityksestä?</span><span class="sxs-lookup"><span data-stu-id="01952-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="01952-129">Kuka tahansa, jolla on omistajarooli, voi lisätä uuden myymäläpäällikön Commerce headquarters -sovelluksessa ja valmistella Teamsin uudelleen, jotta uudella esimiehellä on ryhmän tarvittavat käyttöoikeudet Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="01952-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="01952-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="01952-130">Additional resources</span></span>

[<span data-ttu-id="01952-131">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="01952-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="01952-132">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="01952-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="01952-133">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="01952-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="01952-134">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="01952-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="01952-135">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="01952-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="01952-136">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="01952-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
