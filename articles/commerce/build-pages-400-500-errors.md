---
title: Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille
description: Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697103"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="5385a-103">Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille</span><span class="sxs-lookup"><span data-stu-id="5385a-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5385a-104">Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.</span><span class="sxs-lookup"><span data-stu-id="5385a-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5385a-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="5385a-105">Overview</span></span>

<span data-ttu-id="5385a-106">Jos pyyntö ei onnistu, palvelin antaa HTTP-tilakoodivirhevastaukset.</span><span class="sxs-lookup"><span data-stu-id="5385a-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="5385a-107">404-tilakoodi tallennetaan ja palautetaan, jos sivua ei löydy. 500-tilakoodi tallennetaan ja palautetaan, jos tapahtuu palvelinvirhe.</span><span class="sxs-lookup"><span data-stu-id="5385a-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="5385a-108">Dynamics 365 Commercessa sovelluksen käyttäjät voivat luoda mukautettuja tilakoodivirheiden vastausten sivuja, jotka näytetään käyttäjille näiden tilavirhekoodivirheiden vastauksina.</span><span class="sxs-lookup"><span data-stu-id="5385a-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="5385a-109">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="5385a-109">Build a status code error response page</span></span>

<span data-ttu-id="5385a-110">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5385a-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5385a-111">Kirjaudu haluamallasi selaimella sisään Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="5385a-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="5385a-112">Valitse sivusto, jolle haluat luoda 4xx-/5xx-tilakoodivirheen vastaussivun.</span><span class="sxs-lookup"><span data-stu-id="5385a-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="5385a-113">Mallin luominen</span><span class="sxs-lookup"><span data-stu-id="5385a-113">Build the template</span></span>

<span data-ttu-id="5385a-114">Voit luoda tilakoodivirheen vastaussivun mallin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5385a-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5385a-115">Siirry kohtaan **Mallit \> Uusi malli**.</span><span class="sxs-lookup"><span data-stu-id="5385a-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="5385a-116">Anna uudelle mallille nimi.</span><span class="sxs-lookup"><span data-stu-id="5385a-116">Name the new template.</span></span>
1. <span data-ttu-id="5385a-117">Luo malli sen rakenteen perusteella, jonka haluat määrittää tilakoodivirheen vastaussivulle.</span><span class="sxs-lookup"><span data-stu-id="5385a-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="5385a-118">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5385a-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="5385a-119">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="5385a-119">Build the status code error response page</span></span>

<span data-ttu-id="5385a-120">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5385a-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5385a-121">Siirry kohtaan **Sivut \> Uusi sivu**.</span><span class="sxs-lookup"><span data-stu-id="5385a-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="5385a-122">Anna tilakoodivirheen vastaussivulle nimi, mutta **älä** määritä **URL-osoite**-kentän arvoa.</span><span class="sxs-lookup"><span data-stu-id="5385a-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="5385a-123">Luo sivu.</span><span class="sxs-lookup"><span data-stu-id="5385a-123">Build the page.</span></span>
1. <span data-ttu-id="5385a-124">Kirjaa sivu sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="5385a-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="5385a-125">Voit luoda erilliset tilakoodivirheen vastaussivut 4xx- ja 5xx-tilakoodivirheille.</span><span class="sxs-lookup"><span data-stu-id="5385a-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="5385a-126">Halutessasi voit käyttää samaa yleistä tilakoodivirheen vastaussivua molemmissa virheluokissa.</span><span class="sxs-lookup"><span data-stu-id="5385a-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="5385a-127">Tilakoodivirheen vastaussivun uudelleenohjauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="5385a-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="5385a-128">Voit määrittää tilakoodivirheen vastaussivun uudelleenohjauksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="5385a-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="5385a-129">Siirry kohtaan **URL-osoitteet \> Uusi \> Uusi alias** ja valitse aiemmin luotu tilakoodivirheen vastaussivu.</span><span class="sxs-lookup"><span data-stu-id="5385a-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="5385a-130">Syötä **Alias**-kenttään **oletusarvo - 4xx** tai **oletusarvo - 5xx** sen mukaan, mille tilakoodivirheen vastaussivulle olet määrittämässä uudelleenohjausta.</span><span class="sxs-lookup"><span data-stu-id="5385a-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="5385a-131">Nämä aliakset on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="5385a-131">These aliases must be published.</span></span> <span data-ttu-id="5385a-132">Muussa tapauksessa uudelleenohjaus ei toimi.</span><span class="sxs-lookup"><span data-stu-id="5385a-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="5385a-133">Valitse **OK** vahvistaaksesi linkityksen.</span><span class="sxs-lookup"><span data-stu-id="5385a-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="5385a-134">Jos käytät molemmissa virheluokissa yhtä tilakoodivirheen vastaussivua, toista tämä proseduuri ja linkitä alias myös toiseen saman sivun virheluokkaan.</span><span class="sxs-lookup"><span data-stu-id="5385a-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5385a-135">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="5385a-135">Additional resources</span></span>

[<span data-ttu-id="5385a-136">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="5385a-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="5385a-137">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="5385a-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="5385a-138">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="5385a-138">Create a page URL</span></span>](create-page-url.md)
