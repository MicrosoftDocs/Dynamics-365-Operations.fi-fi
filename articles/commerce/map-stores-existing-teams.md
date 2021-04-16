---
title: Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä
description: Tässä ohjeaiheessa käsitellään myymälöiden ja niitä vastaavien ryhmien määritystä Dynamics 365 Commerce headquartersissa, jos organisaatio on jo luonut ryhmiä Microsoft Teamsissa ennen Commerce-integrointia.
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
ms.openlocfilehash: 3edd176788b24a5f5246e9b7bcb3c6fbcdca2254
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842655"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a><span data-ttu-id="a853b-103">Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä</span><span class="sxs-lookup"><span data-stu-id="a853b-103">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a853b-104">Tässä ohjeaiheessa käsitellään myymälöiden ja niitä vastaavien ryhmien määritystä Dynamics 365 Commerce headquartersissa, jos organisaatio on jo luonut ryhmiä Microsoft Teamsissa ennen Commerce-integrointia.</span><span class="sxs-lookup"><span data-stu-id="a853b-104">This topic covers how to map stores and corresponding teams in Dynamics 365 Commerce headquarters if your organization has already created teams in Microsoft Teams before Commerce integration.</span></span>

<span data-ttu-id="a853b-105">Organisaatiossasi voi olla ryhmiä luotuja joihinkin tai kaikkiin myymälöihin ennen Dynamics 365 Commercen ja Microsoft Teamsin integroimista.</span><span class="sxs-lookup"><span data-stu-id="a853b-105">Your organization may have teams created for some or all of your stores before integrating Dynamics 365 Commerce and Microsoft Teams.</span></span> <span data-ttu-id="a853b-106">Tässä tapauksessa voit määrittää Commerce-myyntipisteen ja Microsoft Teamsin välisen tehtävän synkronoinnin antamalla myymälöiden ja vastaavien tiimien määritykset Commerce headquartersissa.</span><span class="sxs-lookup"><span data-stu-id="a853b-106">If this is the case, to establish task synchronization between Commerce POS and Microsoft Teams you must provide the mapping of stores and corresponding team in Commerce headquarters.</span></span>

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a><span data-ttu-id="a853b-107">Myymälöiden ja vastaavien ryhmien määritys Commerce headquarters -sovelluksessa</span><span class="sxs-lookup"><span data-stu-id="a853b-107">Map stores and corresponding teams in Commerce headquarters</span></span> 

<span data-ttu-id="a853b-108">Tee myymälöiden ja vastaavien ryhmien määritys Commerce headquarters -sovelluksessa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a853b-108">To map stores and corresponding teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a853b-109">Valitse **Järjestelmänhallinta \> Työtila \> Tietojen hallinta**.</span><span class="sxs-lookup"><span data-stu-id="a853b-109">Go to **System Administration \> Workspace \> Data management**.</span></span>
1. <span data-ttu-id="a853b-110">Valitse **Vie**.</span><span class="sxs-lookup"><span data-stu-id="a853b-110">Select **Export**.</span></span> 
1. <span data-ttu-id="a853b-111">Valitse toimintoruudussa **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="a853b-111">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a853b-112">Kirjoita **ryhmän nimeksi** "Vie Teamsin määritys".</span><span class="sxs-lookup"><span data-stu-id="a853b-112">Under **Group name**, enter "Export Teams mapping".</span></span>
1. <span data-ttu-id="a853b-113">Valitse **Valitut yksiköt** -välilehdessä **Lisää yksikkö**.</span><span class="sxs-lookup"><span data-stu-id="a853b-113">On the **Selected entities** FastTab, select **Add entity**.</span></span> <span data-ttu-id="a853b-114">**Lisää yksikkö** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="a853b-114">The **Add entity** dialog box appears.</span></span>  
1. <span data-ttu-id="a853b-115">Valitse avattavasta **Yksikön nimi** -luettelosta **Teams-määritys lähteen ja ryhmän välillä**.</span><span class="sxs-lookup"><span data-stu-id="a853b-115">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="a853b-116">Valitse avattavasta **Kohdetietomuoto**-luettelosta **CSV**.</span><span class="sxs-lookup"><span data-stu-id="a853b-116">In the **Target data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="a853b-117">Valitse **Lisää** ja valitse sitten **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="a853b-117">Select **Add**, and then select **Close**.</span></span>
1. <span data-ttu-id="a853b-118">Valitse toimintoruudun vasemmassa yläreunassa **Vie nyt**.</span><span class="sxs-lookup"><span data-stu-id="a853b-118">On the top left under the Action Pane, select **Export now**.</span></span>
1. <span data-ttu-id="a853b-119">Valitse **Yksikön käsittelyn tila** -kohdasta **Lataa tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="a853b-119">Under **Entity processing status**, select **Download file**.</span></span>
1. <span data-ttu-id="a853b-120">Syötä vietyy CSV-tiedostoon arvot kohtiin **SOURCETYPE**, **SOURCEID** ja **TEAMID** seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="a853b-120">In the exported CSV file, enter values for **SOURCETYPE**, **SOURCEID**, and **TEAMID** as follows:</span></span>
    - <span data-ttu-id="a853b-121">Anna kohdassa **SOURCETYPE** arvo "RetailStore".</span><span class="sxs-lookup"><span data-stu-id="a853b-121">For **SOURCETYPE**, enter "RetailStore".</span></span> 
    - <span data-ttu-id="a853b-122">Kirjoita kohdassa **SOURCEID** myymälän numero (esimerkiksi San Franciscon myymälän numeroksi "000135").</span><span class="sxs-lookup"><span data-stu-id="a853b-122">For **SOURCEID**, enter the store number (for example, "000135" for the San Francisco store).</span></span> <span data-ttu-id="a853b-123">Myymälän numerot löytyvät kohdasta **Retail ja Commerce \> Kanavat \> Myymälät**.</span><span class="sxs-lookup"><span data-stu-id="a853b-123">You can find store numbers at **Retail and Commerce \> Channels \> Stores**.</span></span>
    - <span data-ttu-id="a853b-124">Määritä **TEAMID**-kohtaan vastaava ryhmätunnus Microsoft Teamsista (esimerkiksi 5f8bc92b-6aa8-451e-85d1-3949c01ddc6c).</span><span class="sxs-lookup"><span data-stu-id="a853b-124">For **TEAMID**, enter the corresponding team ID from Microsoft Teams (for example, "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c").</span></span> <span data-ttu-id="a853b-125">Löydät ryhmätunnustiedot kohdasta [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="a853b-125">You can find team ID information at [admin.teams.microsoft.com](https://admin.teams.microsoft.com).</span></span>
1. <span data-ttu-id="a853b-126">Tallenna CSV-tiedosto paikalliseen tietokoneeseen.</span><span class="sxs-lookup"><span data-stu-id="a853b-126">Save the CSV file to your local machine.</span></span>
1. <span data-ttu-id="a853b-127">Valitse **Järjestelmänhallinta \> Työtila \> Tietojen hallinta** ja valitse **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="a853b-127">Go to **System Administration \> Workspace \> Data management**, and then select **Import**.</span></span>
1. <span data-ttu-id="a853b-128">Valitse **Valitut yksiköt** -välilehdessä **Lisää tiedosto**.</span><span class="sxs-lookup"><span data-stu-id="a853b-128">On the **Selected entities** FastTab, select **Add file**.</span></span> <span data-ttu-id="a853b-129">**Lisää tiedosto** -valintaikkuna tulee näkyviin.</span><span class="sxs-lookup"><span data-stu-id="a853b-129">The **Add file** dialog box appears.</span></span>
1. <span data-ttu-id="a853b-130">Valitse avattavasta **Yksikön nimi** -luettelosta **Teams-määritys lähteen ja ryhmän välillä**.</span><span class="sxs-lookup"><span data-stu-id="a853b-130">In the **Entity name** drop-down list, select **Teams mapping between source and team**.</span></span>
1. <span data-ttu-id="a853b-131">Valitse avattavasta **Lähdetietomuoto**-luettelosta **CSV**.</span><span class="sxs-lookup"><span data-stu-id="a853b-131">In the **Source data format** drop-down list, select **CSV**.</span></span>
1. <span data-ttu-id="a853b-132">Valitse **Lataa palvelimeen ja lisää**, valitse aiemmin tallentamasi CSV-tiedosto ja valitse sitten **Avaa**.</span><span class="sxs-lookup"><span data-stu-id="a853b-132">Select **Upload and add**, select the CSV file that you saved previously, and then select **Open**.</span></span>
1. <span data-ttu-id="a853b-133">Valitse **Lisää tiedosto** -valintaikkunassa **Sulje**.</span><span class="sxs-lookup"><span data-stu-id="a853b-133">In the **Add file** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="a853b-134">Valitse toimintoruudussa ensin **Tallenna** ja sitten **Tuo**.</span><span class="sxs-lookup"><span data-stu-id="a853b-134">On the Action Pane, select **Save** , and then select **Import**.</span></span>

<span data-ttu-id="a853b-135">Seuraavassa esimerkkikuvassa on Commercen **Vie Teamsin määritys** -ryhmä, jossa **Lisää yksikkö** -elementit ja viedyn CSV-tiedoston otsikot korostettuina.</span><span class="sxs-lookup"><span data-stu-id="a853b-135">The following example image shows the **Export teams mapping** group in Commerce with **Add entity** elements and the exported CSV file headers highlighted.</span></span>

![Commercen Vie Teamsin määritys -ryhmä, jossa Lisää yksikkö -elementit ja viedyn CSV-tiedoston otsikot korostettuina](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> <span data-ttu-id="a853b-137">Kun olet suorittanut edelliset vaiheet, synkronoi tehtävänhallinta noudattamalla ohjetta [Synkronoi tehtävänhallinta Microsoft Teamsin ja myyntipisteen välillä](synchronize-tasks-teams-pos.md).</span><span class="sxs-lookup"><span data-stu-id="a853b-137">After you complete the preceeding steps, follow the steps in [Synchronize task management between Microsoft Teams and POS](synchronize-tasks-teams-pos.md) to synchronize task management.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a853b-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a853b-138">Additional resources</span></span>

[<span data-ttu-id="a853b-139">Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="a853b-139">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="a853b-140">Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön</span><span class="sxs-lookup"><span data-stu-id="a853b-140">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a853b-141">Microsoft Teamsin valmistelu Dynamics 365 Commercesta</span><span class="sxs-lookup"><span data-stu-id="a853b-141">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="a853b-142">Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä</span><span class="sxs-lookup"><span data-stu-id="a853b-142">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a853b-143">Käyttäjäroolien hallinta Microsoft Teamsissa</span><span class="sxs-lookup"><span data-stu-id="a853b-143">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a853b-144">Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset</span><span class="sxs-lookup"><span data-stu-id="a853b-144">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
