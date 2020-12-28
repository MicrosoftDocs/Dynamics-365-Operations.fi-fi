---
title: Attract-käyttäjät eivät voi hakea töitä uraportaalista
description: Tässä ohjeaiheessa kerrotaan, miten ratkaistaan ongelma, jossa Attract-käyttäjät eivät voi hakea uraportaalin töitä.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461009"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="d041c-103">Attract-käyttäjät eivät voi hakea töitä uraportaalista</span><span class="sxs-lookup"><span data-stu-id="d041c-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="d041c-104">Varasto-otto</span><span class="sxs-lookup"><span data-stu-id="d041c-104">Issue</span></span>

<span data-ttu-id="d041c-105">Attract-käyttäjät eivät voi hakea töitä uraportaalista.</span><span class="sxs-lookup"><span data-stu-id="d041c-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="d041c-106">Kun he yrittävät hakea Dynamics 365 Talent: Attractissa luotua työtä, selain lataa sivua jatkuvasti ilman toiminnon suorittamista.</span><span class="sxs-lookup"><span data-stu-id="d041c-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="d041c-107">Syy</span><span class="sxs-lookup"><span data-stu-id="d041c-107">Cause</span></span>

<span data-ttu-id="d041c-108">Tämä ongelma ilmenee, kun Talentin suhderyhmällä ei ole Talentin käyttäjäroolia.</span><span class="sxs-lookup"><span data-stu-id="d041c-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="d041c-109">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d041c-109">Resolution</span></span>

<span data-ttu-id="d041c-110">Määritä Talentin käyttäjärooli Talentin suhderyhmälle.</span><span class="sxs-lookup"><span data-stu-id="d041c-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="d041c-111">Kirjaudu sisään [Power Platformin hallintakeskukseen](https://admin.powerplatform.microsoft.com) jollakin seuraavista järjestelmänvalvojan valtuustiedoista:</span><span class="sxs-lookup"><span data-stu-id="d041c-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="d041c-112">Dynamics 365:n järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="d041c-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="d041c-113">Yleinen järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="d041c-113">Global admin</span></span>
   - <span data-ttu-id="d041c-114">Power Platformin järjestelmänvalvoja</span><span class="sxs-lookup"><span data-stu-id="d041c-114">Power Platform admin</span></span>

2. <span data-ttu-id="d041c-115">Valitse siirtymisruudussa **Ympäristöt** ja valitse sitten ympäristö, jossa Talentin käyttäjäryhmä liitetään Talentin suhderyhmään.</span><span class="sxs-lookup"><span data-stu-id="d041c-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Ympäristön valitseminen](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="d041c-117">Valitse **Ympäristöt**-ruudussa **Ympäristön URL-osoite** ja kirjaudu sisään ympäristön hallintaportaaliin (esimerkiksi https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d041c-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="d041c-118">Valitse **Asetukset**. Valitse **Järjestelmä** ja valitse sitten **Suojaus**.</span><span class="sxs-lookup"><span data-stu-id="d041c-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Siirtyminen kohtaan Suojaus](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="d041c-120">Valitse **Ryhmät**.</span><span class="sxs-lookup"><span data-stu-id="d041c-120">Select **Teams**.</span></span>

   ![Ryhmien valitseminen](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="d041c-122">Hae **Talentin suhderyhmää** hakuruudun avulla ja valitse ryhmä hakutuloksista.</span><span class="sxs-lookup"><span data-stu-id="d041c-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="d041c-123">Valitse **HALLINNOI ROOLEJA** valintanauhasta.</span><span class="sxs-lookup"><span data-stu-id="d041c-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="d041c-124">Valitse **Hallinnoi ryhmän rooleja** -valintaikkunassa **Talentin käyttäjä** käytettävissä olevista rooleista ja kohdista sitten rooli valitsemalla **OK**.</span><span class="sxs-lookup"><span data-stu-id="d041c-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Roolin kohdistaminen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="d041c-126">Testaa muutokset seuraavasti:</span><span class="sxs-lookup"><span data-stu-id="d041c-126">Test your changes:</span></span>

   1. <span data-ttu-id="d041c-127">Kirjaudu uraportaaliin uudesta selainikkunasta.</span><span class="sxs-lookup"><span data-stu-id="d041c-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="d041c-128">Hae työtä uraportaalista.</span><span class="sxs-lookup"><span data-stu-id="d041c-128">Apply for the job from the career portal.</span></span> 