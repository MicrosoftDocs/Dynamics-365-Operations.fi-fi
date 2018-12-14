---
title: "Talent ei näy yhtenä Microsoft Dynamics 365 -sovelluksena (CDS1.0)"
description: "Tässä ohjeaiheessa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 32ae0ab807e953bd811a557e6878b9bee79d293c
ms.contentlocale: fi-fi
ms.lasthandoff: 12/04/2018

---

# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-cds10"></a><span data-ttu-id="99cc2-103">Talent ei näy yhtenä Microsoft Dynamics 365 -sovelluksena (CDS1.0)</span><span class="sxs-lookup"><span data-stu-id="99cc2-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (CDS1.0)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99cc2-104">**Ongelma**</span><span class="sxs-lookup"><span data-stu-id="99cc2-104">**Issue**</span></span>

<span data-ttu-id="99cc2-105">Asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.</span><span class="sxs-lookup"><span data-stu-id="99cc2-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="99cc2-106">**Tarkkuus**</span><span class="sxs-lookup"><span data-stu-id="99cc2-106">**Resolution**</span></span>

<span data-ttu-id="99cc2-107">Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft PowerAppsin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="99cc2-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="99cc2-108">Järjestelmänvalvoja, jolla on PowerApps -palvelupaketin 2 käyttöoikeus, on avattava [PowerAppsin hallintaportaali](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="99cc2-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="99cc2-109">Valitse ensin **Ympäristöt** ja sitten oikea Talentin ympäristö.</span><span class="sxs-lookup"><span data-stu-id="99cc2-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="99cc2-110">Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.</span><span class="sxs-lookup"><span data-stu-id="99cc2-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. <span data-ttu-id="99cc2-112">Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="99cc2-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. <span data-ttu-id="99cc2-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="99cc2-114">Select **Save**.</span></span>
6. <span data-ttu-id="99cc2-115">Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="99cc2-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="99cc2-116">Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="99cc2-116">Select **Sync** to update the user apps.</span></span>

    ![Synkronointipainike](media/get-more.png)

    <span data-ttu-id="99cc2-118">Kun synkronointi on valmis, Talent näkyy aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="99cc2-118">After synchronization is completed, Talent will appear on the home page.</span></span>

