---
title: Osallistu käyttääksesi luokituksia ja arvosteluja
description: Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697977"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="21e36-103">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="21e36-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="21e36-104">Tässä ohjeaiheessa kerrotaan, miten voit käyttää luokituksia ja arvosteluja Microsoft Dynamics 365 Commerce -sivustossa.</span><span class="sxs-lookup"><span data-stu-id="21e36-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="21e36-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="21e36-105">Overview</span></span>

<span data-ttu-id="21e36-106">Luokitukset ja arvostelut -ratkaisu on monikanavaratkaisu, jonka voit ottaa käyttöön Dynamics 365 Commerce -sovelluksessa käyttämällä Microsoft Dynamics Lifecycle Services (LCS) -palvelua.</span><span class="sxs-lookup"><span data-stu-id="21e36-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="21e36-107">LCS on hallintaportaali, jonka avulla jälleenmyyjät voivat hallita ympäristöjä aina valmistelusta käytöstäpoistoon asti.</span><span class="sxs-lookup"><span data-stu-id="21e36-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="21e36-108">Jos haluat käyttää luokitukset ja arvostelut -ratkaisua Commerce-sivustossa, sinun on ensin suostuttava sen käyttöön.</span><span class="sxs-lookup"><span data-stu-id="21e36-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="21e36-109">Osallistu käyttääksesi luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="21e36-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="21e36-110">Voit ottaa luokitukset ja arvostelut käyttöön sivustossa seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="21e36-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="21e36-111">Noudata kohdan [Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md) ohjeita.</span><span class="sxs-lookup"><span data-stu-id="21e36-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="21e36-112">Kun olet edelleen LCS-sovelluksessa, siirry kohtaan **Retail-käyttöönoton asetukset \> Muut asetukset**.</span><span class="sxs-lookup"><span data-stu-id="21e36-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="21e36-113">Määritä **Ota luokitukset ja arvostelut -palvelu käyttöön** -asetuksen arvoksi **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="21e36-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="21e36-114">Syötä **Luokitusten ja arvostelujen valvojan AAD-käyttöoikeusryhmä (käyttöoikeusryhmän objektin tunnus)** -kenttään sen Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmän tunnus, joka sisältää luokitusten ja arvosteluiden valvojat.</span><span class="sxs-lookup"><span data-stu-id="21e36-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Osallistu käyttääksesi luokituksia ja arvosteluja](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="21e36-116">Suorita sähköisen kaupankäynnin alustusprosessi loppuun.</span><span class="sxs-lookup"><span data-stu-id="21e36-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21e36-117">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="21e36-117">Additional resources</span></span>

[<span data-ttu-id="21e36-118">Luokitukset ja arvostelut – yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="21e36-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="21e36-119">Hallitse luokituksia ja arvosteluja</span><span class="sxs-lookup"><span data-stu-id="21e36-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="21e36-120">Määritä luokitukset ja arvostelut</span><span class="sxs-lookup"><span data-stu-id="21e36-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="21e36-121">Tuoteluokitusten synkronoiminen Dynamics 365 Retailissa</span><span class="sxs-lookup"><span data-stu-id="21e36-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
