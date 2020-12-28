---
title: Osallistu käyttääksesi luokituksia ja arvosteluja
description: Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cbdb69202ebec19f4442041cfb1f99857da36d2e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411979"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9feab-103">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="9feab-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9feab-104">Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.</span><span class="sxs-lookup"><span data-stu-id="9feab-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="9feab-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9feab-105">Overview</span></span>

<span data-ttu-id="9feab-106">Luokitukset ja arvostelut -ratkaisu on monikanavaratkaisu, jonka voit ottaa käyttöön Dynamics 365 Commerce -sovelluksessa käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palvelua.</span><span class="sxs-lookup"><span data-stu-id="9feab-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="9feab-107">LCS on hallintaportaali, jonka avulla jälleenmyyjät voivat hallita ympäristöjä aina valmistelusta käytöstäpoistoon asti.</span><span class="sxs-lookup"><span data-stu-id="9feab-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="9feab-108">Jos haluat käyttää luokitukset ja arvostelut -ratkaisua Commerce-sivustossa, sinun on valittava luokitukset ja arvostelut verkkokauppasivuston käyttöönoton aikana Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="9feab-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="9feab-109">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="9feab-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="9feab-110">Voit ottaa luokitukset ja arvostelut käyttöön sivustossa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="9feab-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="9feab-111">Noudata kohdan [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="9feab-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="9feab-112">Kun olet edelleen LCS-sovelluksessa, siirry kohtaan **Retail-käyttöönoton asetukset \> Muut asetukset**.</span><span class="sxs-lookup"><span data-stu-id="9feab-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="9feab-113">Määritä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="9feab-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="9feab-114">Syötä **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä (käyttöoikeusryhmän objektin tunnus)** -kenttään sen Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmän tunnus, joka sisältää luokitusten ja arvosteluiden valvojat.</span><span class="sxs-lookup"><span data-stu-id="9feab-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Osallistu käyttääksesi luokituksia ja arvosteluja](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="9feab-116">Suorita sähköisen kaupankäynnin alustusprosessi loppuun.</span><span class="sxs-lookup"><span data-stu-id="9feab-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="9feab-117">Jos olet olemassa oleva Dynamics 365 Commerce -asiakas, joka on jo ottanut käyttöön e-Commerce-sivuston ilman luokitusten ja arvostelujen käyttöä ja haluat nyt käyttää Dynamics 365 Commerce -pakkauksen luokituksia ja arvosteluja, lähetä palvelupyyntö.</span><span class="sxs-lookup"><span data-stu-id="9feab-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="9feab-118">Lisätietoja huoltopyynnön lähettämisessä on ohjeaiheessa [Palvelupyyntöjen lähettämisprosessi](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9feab-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9feab-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="9feab-119">Additional resources</span></span>

[<span data-ttu-id="9feab-120">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="9feab-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="9feab-121">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="9feab-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="9feab-122">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="9feab-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="9feab-123">Tuoteluokitusten synkronoiminen Dynamics 365 Commerceissa</span><span class="sxs-lookup"><span data-stu-id="9feab-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)


