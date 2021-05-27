---
title: Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus
description: Tämä ohjeaihe sisältää yhteenvedon ja Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integroinnista.
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
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021986"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="c2be5-103">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c2be5-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c2be5-104">Tämä ohjeaihe sisältää yhteenvedon ja Microsoft Dynamics 365 Commercen ja Microsoft Teamsin integroinnista.</span><span class="sxs-lookup"><span data-stu-id="c2be5-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="c2be5-105">Dynamics 365 Commerce integroidaan Teamsin kanssa, jotta asiakkaat ja niiden työntekijät voivat parantaa tuottavuutta synkronoimalla tehtävänhallinnan näiden kahden sovelluksen välillä.</span><span class="sxs-lookup"><span data-stu-id="c2be5-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="c2be5-106">Commercen ja Teamsin integroinnin saumaton tehtävähallinta sallii myymäläpäälliköiden ja työntekijöiden luoda tehtäväluetteloita, määrittää tehtäviä useisiin myymälöihin sekä seurata eri myymälöiden tehtävien tilaa kummasta tahansa sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="c2be5-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="c2be5-107">Commercen ja Teamsin integrointi on käytettävissä Commerce-versiosta 10.0.18 eteenpäin.</span><span class="sxs-lookup"><span data-stu-id="c2be5-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="c2be5-108">Tärkeimmät ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="c2be5-108">Key features</span></span>

<span data-ttu-id="c2be5-109">Seuraavassa on Commercen ja Microsoft Teamsin integroinnin tärkeitä ominaisuuksia:</span><span class="sxs-lookup"><span data-stu-id="c2be5-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="c2be5-110">Valmistele Teams käyttämällä Commercen hyvin määritettyjä tietoja, kuten organisaatiorakennetta ja myymälöiden, työntekijöiden, käyttöoikeuksien ja liiketoimintakontekstin tietoja.</span><span class="sxs-lookup"><span data-stu-id="c2be5-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="c2be5-111">Synkronoi helposti käynnissä olevat muutokset (esimerkiksi uusien myymälöiden lisäys tai uusien työntekijöiden palkkaaminen) Commercen ja Teamsin välillä, mutta säilytä Commerce organisaatiorakenteen tietojen päälähteenä.</span><span class="sxs-lookup"><span data-stu-id="c2be5-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="c2be5-112">Integroi tehtävien hallinta Commercen ja Teamsin välillä, jotta työntekijät, myymäläpäälliköt, alueelliset esimiehet ja viestintäpäälliköt voivat käsitellä tehtävänhallintaa kummasta tahansa sovelluksesta.</span><span class="sxs-lookup"><span data-stu-id="c2be5-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="c2be5-113">Integrointiominaisuuksien käytön edellytykset</span><span class="sxs-lookup"><span data-stu-id="c2be5-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="c2be5-114">Seuraavien edellytysten on oltava käytössä, ennen kuin voit aloittaa Microsoft Teams -integrointiominaisuuksien käytön:</span><span class="sxs-lookup"><span data-stu-id="c2be5-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="c2be5-115">Microsoft 365 Business Standard License (Tämä lisenssi sisältää Teamsin.)</span><span class="sxs-lookup"><span data-stu-id="c2be5-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="c2be5-116">Azure Active Directory(Azure AD) -tilit kaikille myymäläpäälliköille ja työntekijöille</span><span class="sxs-lookup"><span data-stu-id="c2be5-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="c2be5-117">Myyntipistejärjestelmät, jotka on konfiguroitu Azure AD -todennuksella</span><span class="sxs-lookup"><span data-stu-id="c2be5-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="c2be5-118">Käsitteellinen arkkitehtuuri</span><span class="sxs-lookup"><span data-stu-id="c2be5-118">Conceptual architecture</span></span>

<span data-ttu-id="c2be5-119">Seuraavassa kuvassa havainnollistetaan Dynamics 365 Commercen ja Microsoft Teamsin integroinnin käsitteellistä arkkitehtuuria, ja esimerkinä käytetään San Franciscon myymälää.</span><span class="sxs-lookup"><span data-stu-id="c2be5-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="c2be5-120">Sekä Teams että Commercen myyntipistesovellus käyttävät Microsoft Planneria tietovarastona, jotta Teamsista julkaisut tehtävät näkyvät myyntipistesovelluksessa sekä myymäläpäälliköiden myyntipistesovelluksella luomat ad-hoc -tehtäviä näkyvät Teamsissa. Näin sovellusten välillä syntyy saumaton tehtävien hallinta.</span><span class="sxs-lookup"><span data-stu-id="c2be5-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commercen ja Teamsin integroinnin arkkitehtuuri](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="c2be5-122">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c2be5-122">Additional resources</span></span>

[<span data-ttu-id="c2be5-123">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="c2be5-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="c2be5-124">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="c2be5-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="c2be5-125">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="c2be5-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="c2be5-126">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="c2be5-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="c2be5-127">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="c2be5-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="c2be5-128">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="c2be5-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
