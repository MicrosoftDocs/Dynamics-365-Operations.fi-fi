---
title: Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa
description: Tässä artikkelissa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 Human Resources -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d39e6ef4168f08f20b92979a296ed088744ad0da
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008956"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="7b1f4-103">Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="7b1f4-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

<span data-ttu-id="7b1f4-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-104">**Issue**</span></span>

<span data-ttu-id="7b1f4-105">Asiakas ei näe Dynamics 365 Human Resourcesia Microsoft Dynamics 365 -sovellusten joukossa.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="7b1f4-106">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="7b1f4-106">**Resolution**</span></span>

<span data-ttu-id="7b1f4-107">Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft Power Appsin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="7b1f4-108">Järjestelmänvalvoja, jolla on Power Apps-palvelupaketin 2 käyttöoikeus, on avattava [Power Appsin hallintaportaali](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="7b1f4-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="7b1f4-109">Valitse ensin **Ympäristöt** ja sitten oikea Human Resourcesin ympäristö.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="7b1f4-110">Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. <span data-ttu-id="7b1f4-112">Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. <span data-ttu-id="7b1f4-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-114">Select **Save**.</span></span>

6. <span data-ttu-id="7b1f4-115">Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7b1f4-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="7b1f4-116">Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-116">Select **Sync** to update the user apps.</span></span>

    ![Synkronointipainike](media/get-more.png)

    <span data-ttu-id="7b1f4-118">Kun synkronointi on valmis, Human Resources näkyy aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="7b1f4-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>