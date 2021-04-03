---
title: Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa
description: Tässä artikkelissa kerrotaan, mitä on tehtävä, jos asiakas ei näe Microsoft Dynamics 365 Human Resources -sovellusta muiden Microsoft Dynamics 365 -sovellusten joukossa.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 9be1c2b862a01d6f14ad98dbcb01e061649c6af0
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463981"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a><span data-ttu-id="ba30c-103">Human Resources ei näy Microsoft Dynamics 365 -sovelluksissa</span><span class="sxs-lookup"><span data-stu-id="ba30c-103">Human Resources doesn't appear in Microsoft Dynamics 365 apps</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ba30c-104">**Lähetä**</span><span class="sxs-lookup"><span data-stu-id="ba30c-104">**Issue**</span></span>

<span data-ttu-id="ba30c-105">Asiakas ei näe Dynamics 365 Human Resourcesia Microsoft Dynamics 365 -sovellusten joukossa.</span><span class="sxs-lookup"><span data-stu-id="ba30c-105">The customer doesn't see Dynamics 365 Human Resources among the Microsoft Dynamics 365 apps.</span></span>

<span data-ttu-id="ba30c-106">**Ratkaisu**</span><span class="sxs-lookup"><span data-stu-id="ba30c-106">**Resolution**</span></span>

<span data-ttu-id="ba30c-107">Käyttäjä on lisättävä ympäristön tekijän rooliin Microsoft Power Appsin ympäristössä.</span><span class="sxs-lookup"><span data-stu-id="ba30c-107">The user must be added to the Environment Maker role for the environment in Microsoft Power Apps.</span></span>

1. <span data-ttu-id="ba30c-108">Järjestelmänvalvoja, jolla on Power Apps-palvelupaketin 2 käyttöoikeus, on avattava [Power Appsin hallintaportaali](https://preview.admin.powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="ba30c-108">The admin user who has a Power Apps Plan 2 license must open the [Power Apps Admin portal](https://preview.admin.powerapps.com/).</span></span>

2. <span data-ttu-id="ba30c-109">Valitse ensin **Ympäristöt** ja sitten oikea Human Resourcesin ympäristö.</span><span class="sxs-lookup"><span data-stu-id="ba30c-109">Select **Environments**, and select the correct environment for Human Resources.</span></span>

3. <span data-ttu-id="ba30c-110">Valitse **Ympäristöroolit**-välilehden **Suojaus**-välilehdessä **Ympäristön tekijä**.</span><span class="sxs-lookup"><span data-stu-id="ba30c-110">On the **Security** tab, on the **Environment roles** tab, select **Environment Maker**.</span></span>

    ![Ympäristöroolit-välilehti](media/environment-roles.png)

4. <span data-ttu-id="ba30c-112">Lisää käyttäjä tai organisaatio **Käyttäjät**-välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="ba30c-112">On the **Users** tab, add the user or your organization.</span></span>

    ![Käyttäjät-välilehti](media/environment-maker.png)

5. <span data-ttu-id="ba30c-114">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="ba30c-114">Select **Save**.</span></span>

6. <span data-ttu-id="ba30c-115">Käyttäjän on nyt kirjauduttava [Microsoft Dynamics 365:een](https://home.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="ba30c-115">The user must now sign in to [Microsoft Dynamics 365](https://home.dynamics.com/).</span></span>

7. <span data-ttu-id="ba30c-116">Päivitä käyttäjän sovellukset valitsemalla **Synkronoi**.</span><span class="sxs-lookup"><span data-stu-id="ba30c-116">Select **Sync** to update the user apps.</span></span>

    ![Synkronointipainike](media/get-more.png)

    <span data-ttu-id="ba30c-118">Kun synkronointi on valmis, Human Resources näkyy aloitussivulla.</span><span class="sxs-lookup"><span data-stu-id="ba30c-118">After synchronization is completed, Human Resources will appear on the home page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]