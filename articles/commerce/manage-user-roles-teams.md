---
title: Käyttäjäroolien hallinta Microsoft Teamsissa
description: Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commerce -käyttäjärooleja hallitaan Microsoft Teamsissa.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 73ae905b848588898f4a1c6e973bcd3a952c7dc1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842656"
---
# <a name="manage-user-roles-in-microsoft-teams"></a><span data-ttu-id="f01e5-103">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="f01e5-103">Manage user roles in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f01e5-104">Tässä ohjeaiheessa kerrotaan, miten Microsoft Dynamics 365 Commerce -käyttäjärooleja hallitaan Microsoft Teamsissa.</span><span class="sxs-lookup"><span data-stu-id="f01e5-104">This topic describes how to manage Microsoft Dynamics 365 Commerce user roles in Microsoft Teams.</span></span>

<span data-ttu-id="f01e5-105">Kun luot ryhmän kullekin myymälälle tai kanavalle Teamsissa, luodaan ryhmän jäsenyys, joka vastaa ryhmää (esim. `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span><span class="sxs-lookup"><span data-stu-id="f01e5-105">As you create a team for each store or channel in Teams, a group membership that corresponds to the team is created (for example, `HOUSTON_D365@<YourTenantAzureADDomain>.com`).</span></span> <span data-ttu-id="f01e5-106">Ryhmän jäsenyyteen kuuluville kaikille myymälätyöntekijöille määritetään toinen seuraavista käyttäjärooleista: **Omistaja** tai **Jäsen**.</span><span class="sxs-lookup"><span data-stu-id="f01e5-106">All the store workers under a team group membership are assigned one of two user roles: **Owner** or **Member**.</span></span> <span data-ttu-id="f01e5-107">Myymälän työntekijät, joilla on **Omistaja**-käyttäjärooli, voivat suorittaa toimintoja, kuten lisätä yksityisen kanavan sekä lisätä tai poistaa jäseniä.</span><span class="sxs-lookup"><span data-stu-id="f01e5-107">Store employees who have the **Owner** user role can perform operations such as adding a private channel, and adding or deleting members.</span></span> <span data-ttu-id="f01e5-108">Myymäläpäälliköilla on yleensä **Omistaja**-käyttäjärooli.</span><span class="sxs-lookup"><span data-stu-id="f01e5-108">Typically, store managers have the **Owner** user role.</span></span>

<span data-ttu-id="f01e5-109">Seuraavassa kuvassa on esimerkki ryhmän jäsenten ja niiden käyttäjäroolien luettelosta Microsoft Teams -hallintakeskuksessa.</span><span class="sxs-lookup"><span data-stu-id="f01e5-109">The following illustration shows an example of a list of team members and their user roles in the Microsoft Teams admin center.</span></span>

![Ryhmän jäsenet ja käyttäjäroolit Microsoft Teams -hallintakeskuksessa](media/d365-commerce-teams-integration-user-roles.png)

<span data-ttu-id="f01e5-111">Lisätietoja on kohdassa [Ryhmän omistajien ja jäsenten määrittäminen Microsoft Teamsissa](https://docs.microsoft.com/microsoftteams/assign-roles-permissions).</span><span class="sxs-lookup"><span data-stu-id="f01e5-111">For more information, see [Assign team owners and members in Microsoft Teams](https://docs.microsoft.com/microsoftteams/assign-roles-permissions).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f01e5-112">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="f01e5-112">Additional resources</span></span>

[<span data-ttu-id="f01e5-113">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="f01e5-113">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="f01e5-114">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="f01e5-114">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="f01e5-115">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="f01e5-115">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="f01e5-116">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="f01e5-116">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="f01e5-117">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="f01e5-117">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="f01e5-118">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="f01e5-118">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)