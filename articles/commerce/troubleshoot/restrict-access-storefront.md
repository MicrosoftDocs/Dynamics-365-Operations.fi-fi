---
title: Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2cdf131048e0fac940475322294ed99e76c0a53b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585307"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="8d36d-103">Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana</span><span class="sxs-lookup"><span data-stu-id="8d36d-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8d36d-104">Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="8d36d-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="8d36d-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="8d36d-105">Description</span></span>

<span data-ttu-id="8d36d-106">Sisäisen testauksen tai aktiivisen kehityksen aikana kannattaa ehkä rajoittaa sivuston käyttö, jotta ulkoiset käyttäjät eivät voi käyttää julkaistuja verkkokauppasivuja.</span><span class="sxs-lookup"><span data-stu-id="8d36d-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="8d36d-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="8d36d-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="8d36d-108">Azure AD B2C:n määrittäminen vakiokäyttäjätyönkulkujen avulla</span><span class="sxs-lookup"><span data-stu-id="8d36d-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="8d36d-109">Lisätietoja Azure Active DirectoryB2C:n (Azure AD B2C) konfiguroinnista verkkokauppasivustolle on kohdassa [Commercen B2C-vuokraajan määrittäminen](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="8d36d-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="8d36d-110">Rajoita käyttäjien pääsyä verkkokaupan sivuille ja estä uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="8d36d-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="8d36d-111">Rajoita verkkokaupan sivujen käyttöä Commerce-sivustonmuodostimen avulla noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="8d36d-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="8d36d-112">Siirry sivustoosi.</span><span class="sxs-lookup"><span data-stu-id="8d36d-112">Go to your site.</span></span>
1. <span data-ttu-id="8d36d-113">Valitse **Sivut** ja valitse sitten sivu, jonka käyttöä haluat rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="8d36d-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="8d36d-114">Valitse moduuli tai katkelmapaikka ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="8d36d-115">Valitse ominaisuusruudusta **Edellyttääkö kirjautumista?** ja valitse sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8d36d-116">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-116">Select **Publish**.</span></span>

<span data-ttu-id="8d36d-117">Estä uusien käyttäjien luominen Azure AD:ssä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="8d36d-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="8d36d-118">Siirry [Azure-portaaliin](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="8d36d-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="8d36d-119">Valitse Azure AD B2C -sovellus, jonka loit sivuston käyttöön.</span><span class="sxs-lookup"><span data-stu-id="8d36d-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="8d36d-120">Valitse vasemmanpuoleisessa siirtymisruudussa **Käyttäjätyönkulut**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="8d36d-121">Valitse **Käyttäjätyönkulut** -sivun yläosassa **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="8d36d-122">Valitse **Käyttäjätyönkulun tyyppi** -sivulla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="8d36d-123">Valitse sivun keskiosasta **Kirjautuminen v2**.</span><span class="sxs-lookup"><span data-stu-id="8d36d-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="8d36d-124">Noudata sitten [B2C-vuokraajan määritys Commercessa](../set-up-b2c-tenant.md) -ohjeen vaiheita, kun haluat määrittää työnkulun sivuston vakiokäyttäjätyönkuluksi Azure AD B2C:lle testauksen tai kehityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="8d36d-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d36d-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8d36d-125">Additional resources</span></span>

[<span data-ttu-id="8d36d-126">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="8d36d-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="8d36d-127">Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="8d36d-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
