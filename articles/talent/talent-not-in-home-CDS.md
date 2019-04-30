---
title: Talent ei näy Microsoft Dynamics -sovellusten yhteydessä (Common Data Service 1.0)
description: Tässä ohjeaiheessa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ad5add2b572ccb6bff175806b965f63b53986152
ms.sourcegitcommit: 45b79d1e587e03f5cde2766cdec4eaa7a2a897a3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/02/2019
ms.locfileid: "949779"
---
# <a name="talent-doesnt-appear-among-the-microsoft-dynamics-365-apps-common-data-service-10"></a><span data-ttu-id="0d02a-103">Talent ei näy Microsoft Dynamics -sovellusten yhteydessä (Common Data Service 1.0)</span><span class="sxs-lookup"><span data-stu-id="0d02a-103">Talent doesn't appear among the Microsoft Dynamics 365 apps (Common Data Service 1.0)</span></span>

[!include [banner](includes/banner.md)]

**<span data-ttu-id="0d02a-104">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="0d02a-104">Issue</span></span>**

<span data-ttu-id="0d02a-105">Asiakas ei näe Microsoft Dynamics 365 for Talent -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.</span><span class="sxs-lookup"><span data-stu-id="0d02a-105">The customer doesn't see the Microsoft Dynamics 365 for Talent app among the Microsoft Dynamics 365 apps.</span></span>

**<span data-ttu-id="0d02a-106">Tarkkuus</span><span class="sxs-lookup"><span data-stu-id="0d02a-106">Resolution</span></span>**

<span data-ttu-id="0d02a-107">Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft PowerAppsin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="0d02a-107">The user must be added to the Environment Maker role for the environment in Microsoft PowerApps.</span></span>

1. <span data-ttu-id="0d02a-108">Järjestelmänvalvoja, jolla on PowerApps -palvelupaketin 2 käyttöoikeus, on avattava [PowerAppsin hallintaportaali](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="0d02a-108">The admin user who has a PowerApps Plan 2 license must open the [PowerApps Admin portal](https://preview.admin.powerapps.com/).</span></span>
2. <span data-ttu-id="0d02a-109">Valitse ensin **Ympäristöt** ja sitten oikea Talentin ympäristö.</span><span class="sxs-lookup"><span data-stu-id="0d02a-109">Select **Environments**, and select the correct environment for Talent.</span></span>
3. <span data-ttu-id="0d02a-110">Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.</span><span class="sxs-lookup"><span data-stu-id="0d02a-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. <span data-ttu-id="0d02a-112">Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="0d02a-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. <span data-ttu-id="0d02a-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0d02a-114">Select **Save**.</span></span>
6. <span data-ttu-id="0d02a-115">Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="0d02a-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>
7. <span data-ttu-id="0d02a-116">Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="0d02a-116">Select **Sync** to update the user apps.</span></span>

    ![Synkronointipainike](media/get-more.png)

    <span data-ttu-id="0d02a-118">Kun synkronointi on valmis, Talent näkyy aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="0d02a-118">After synchronization is completed, Talent will appear on the home page.</span></span>
