---
title: Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana
description: Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: cdc9b6af55bcba98f5ea7607bb1847f61a707778
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018335"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a><span data-ttu-id="76db2-103">Verkkokaupan käytön rajoittaminen testauksen tai kehityksen aikana</span><span class="sxs-lookup"><span data-stu-id="76db2-103">Restrict access to a storefront during testing or development</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="76db2-104">Tässä aiheessa kuvataan, kuinka Microsoft Dynamics 365 Commerce -verkkokaupan käyttöä rajoitetaan sisäisen testin tai kehityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="76db2-104">This topic explains how to restrict access to a Microsoft Dynamics 365 Commerce storefront while internal testing or development is occurring.</span></span>

## <a name="description"></a><span data-ttu-id="76db2-105">kuvaus</span><span class="sxs-lookup"><span data-stu-id="76db2-105">Description</span></span>

<span data-ttu-id="76db2-106">Sisäisen testauksen tai aktiivisen kehityksen aikana kannattaa ehkä rajoittaa sivuston käyttö, jotta ulkoiset käyttäjät eivät voi käyttää julkaistuja verkkokauppasivuja.</span><span class="sxs-lookup"><span data-stu-id="76db2-106">During internal testing or active development, you might want to restrict access to your site to prevent external users from accessing the published storefront pages.</span></span>

## <a name="resolution"></a><span data-ttu-id="76db2-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="76db2-107">Resolution</span></span>

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a><span data-ttu-id="76db2-108">Azure AD B2C:n määrittäminen vakiokäyttäjätyönkulkujen avulla</span><span class="sxs-lookup"><span data-stu-id="76db2-108">Set up Azure AD B2C by using standard user flows</span></span>

<span data-ttu-id="76db2-109">Lisätietoja Azure Active DirectoryB2C:n (Azure AD B2C) konfiguroinnista verkkokauppasivustolle on kohdassa [Commercen B2C-vuokraajan määrittäminen](../set-up-b2c-tenant.md).</span><span class="sxs-lookup"><span data-stu-id="76db2-109">For information about how to configure Azure Active Directory B2C (Azure AD B2C) for your e-commerce site, see [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md).</span></span>

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a><span data-ttu-id="76db2-110">Rajoita käyttäjien pääsyä verkkokaupan sivuille ja estä uusien käyttäjien luominen</span><span class="sxs-lookup"><span data-stu-id="76db2-110">Restrict user access to storefront pages and block the creation of new users</span></span>

<span data-ttu-id="76db2-111">Rajoita verkkokaupan sivujen käyttöä Commerce-sivustonmuodostimen avulla noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="76db2-111">To restrict user access to storefront pages in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="76db2-112">Siirry sivustoosi.</span><span class="sxs-lookup"><span data-stu-id="76db2-112">Go to your site.</span></span>
1. <span data-ttu-id="76db2-113">Valitse **Sivut** ja valitse sitten sivu, jonka käyttöä haluat rajoittaa.</span><span class="sxs-lookup"><span data-stu-id="76db2-113">Select **Pages**, and then select the page to restrict user access for.</span></span>
1. <span data-ttu-id="76db2-114">Valitse moduuli tai katkelmapaikka ja valitse sitten **Muokkaa**.</span><span class="sxs-lookup"><span data-stu-id="76db2-114">Select the module or fragment slot, and then select **Edit**.</span></span>
1. <span data-ttu-id="76db2-115">Valitse ominaisuusruudusta **Edellyttääkö kirjautumista?** ja valitse sitten **Lopeta muokkaus**.</span><span class="sxs-lookup"><span data-stu-id="76db2-115">In the properties pane, select **Requires sign-in?**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="76db2-116">Valitse **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="76db2-116">Select **Publish**.</span></span>

<span data-ttu-id="76db2-117">Estä uusien käyttäjien luominen Azure AD:ssä noudattamalla seuraavia ohjeita.</span><span class="sxs-lookup"><span data-stu-id="76db2-117">To block the creation of new users in Azure AD, follow these steps.</span></span>

1. <span data-ttu-id="76db2-118">Siirry [Azure-portaaliin](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="76db2-118">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="76db2-119">Valitse Azure AD B2C -sovellus, jonka loit sivuston käyttöön.</span><span class="sxs-lookup"><span data-stu-id="76db2-119">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="76db2-120">Valitse vasemmanpuoleisessa siirtymisruudussa **Käyttäjätyönkulut**.</span><span class="sxs-lookup"><span data-stu-id="76db2-120">In the left navigation, select **User flows**.</span></span>
1. <span data-ttu-id="76db2-121">Valitse **Käyttäjätyönkulut** -sivun yläosassa **Uusi käyttäjän työnkulku**.</span><span class="sxs-lookup"><span data-stu-id="76db2-121">At the top of the **User Flows** page, select **New user flow**.</span></span>
1. <span data-ttu-id="76db2-122">Valitse **Käyttäjätyönkulun tyyppi** -sivulla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="76db2-122">On the **Select a user flow type** page, select **Preview**.</span></span>
1. <span data-ttu-id="76db2-123">Valitse sivun keskiosasta **Kirjautuminen v2**.</span><span class="sxs-lookup"><span data-stu-id="76db2-123">In the middle of the page, select **Sign in v2**.</span></span> <span data-ttu-id="76db2-124">Noudata sitten [B2C-vuokraajan määritys Commercessa](../set-up-b2c-tenant.md) -ohjeen vaiheita, kun haluat määrittää työnkulun sivuston vakiokäyttäjätyönkuluksi Azure AD B2C:lle testauksen tai kehityksen aikana.</span><span class="sxs-lookup"><span data-stu-id="76db2-124">Then follow the steps in [Set up a B2C tenant in Commerce](../set-up-b2c-tenant.md) to configure the flow as your site's standard user flow for Azure AD B2C during testing or development.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76db2-125">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="76db2-125">Additional resources</span></span>

[<span data-ttu-id="76db2-126">Kuluttajakaupan vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="76db2-126">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

[<span data-ttu-id="76db2-127">Mukautettujen sivujen määrittäminen käyttäjän sisäänkirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="76db2-127">Set up custom pages for user sign-ins</span></span>](../custom-pages-user-logins.md)
