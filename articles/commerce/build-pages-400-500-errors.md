---
title: Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille
description: Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d21ce20b2c7ac8c656a718749dabd76f33893da8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991462"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="ef073-103">Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille</span><span class="sxs-lookup"><span data-stu-id="ef073-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ef073-104">Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.</span><span class="sxs-lookup"><span data-stu-id="ef073-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ef073-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ef073-105">Overview</span></span>

<span data-ttu-id="ef073-106">Jos pyyntö ei onnistu, palvelin antaa HTTP-tilakoodivirhevastaukset.</span><span class="sxs-lookup"><span data-stu-id="ef073-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="ef073-107">404-tilakoodi tallennetaan ja palautetaan, jos sivua ei löydy. 500-tilakoodi tallennetaan ja palautetaan, jos tapahtuu palvelinvirhe.</span><span class="sxs-lookup"><span data-stu-id="ef073-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="ef073-108">Dynamics 365 Commercessa sovelluksen käyttäjät voivat luoda mukautettuja tilakoodivirheiden vastausten sivuja, jotka näytetään käyttäjille näiden tilavirhekoodivirheiden vastauksina.</span><span class="sxs-lookup"><span data-stu-id="ef073-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="ef073-109">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="ef073-109">Build a status code error response page</span></span>

<span data-ttu-id="ef073-110">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ef073-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ef073-111">Kirjaudu haluamallasi selaimella sisään Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ef073-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="ef073-112">Valitse sivusto, jolle haluat luoda 4xx-/5xx-tilakoodivirheen vastaussivun.</span><span class="sxs-lookup"><span data-stu-id="ef073-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="ef073-113">Mallin luominen</span><span class="sxs-lookup"><span data-stu-id="ef073-113">Build the template</span></span>

<span data-ttu-id="ef073-114">Voit luoda tilakoodivirheen vastaussivun mallin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ef073-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ef073-115">Valitse **Mallit**.</span><span class="sxs-lookup"><span data-stu-id="ef073-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="ef073-116">Luo sivumalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ef073-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="ef073-117">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan uuden mallin nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef073-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="ef073-118">Luo malli sen rakenteen perusteella, jonka haluat määrittää tilakoodivirheen vastaussivulle.</span><span class="sxs-lookup"><span data-stu-id="ef073-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="ef073-119">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ef073-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="ef073-120">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="ef073-120">Build the status code error response page</span></span>

<span data-ttu-id="ef073-121">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ef073-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ef073-122">Siirry kohtaan **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="ef073-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="ef073-123">Luo sivu valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="ef073-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="ef073-124">Valitse malli **Valitse malli** -valinta ikkunassa ja kirjoita sitten **Sivun nimi** -kohtaan tilakoodin virhevastaussivun nimi.</span><span class="sxs-lookup"><span data-stu-id="ef073-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="ef073-125">Jätä **Sivun URL-osoite** -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="ef073-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="ef073-126">Luo sivu.</span><span class="sxs-lookup"><span data-stu-id="ef073-126">Build the page.</span></span>
1. <span data-ttu-id="ef073-127">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="ef073-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ef073-128">Voit luoda erilliset tilakoodivirheen vastaussivut 4xx- ja 5xx-tilakoodivirheille.</span><span class="sxs-lookup"><span data-stu-id="ef073-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="ef073-129">Halutessasi voit käyttää samaa yleistä tilakoodivirheen vastaussivua molemmissa virheluokissa.</span><span class="sxs-lookup"><span data-stu-id="ef073-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="ef073-130">Tilakoodivirheen vastaussivun uudelleenohjauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="ef073-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="ef073-131">Voit määrittää tilakoodivirheen vastaussivun uudelleenohjauksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="ef073-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="ef073-132">Siirry kohtaan **URL-osoitteet \> Uusi \> Uusi alias** ja valitse aiemmin luotu tilakoodivirheen vastaussivu.</span><span class="sxs-lookup"><span data-stu-id="ef073-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="ef073-133">Syötä **Alias**-kenttään **oletusarvo - 4xx** tai **oletusarvo - 5xx** sen mukaan, mille tilakoodivirheen vastaussivulle olet määrittämässä uudelleenohjausta.</span><span class="sxs-lookup"><span data-stu-id="ef073-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="ef073-134">Nämä aliakset on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="ef073-134">These aliases must be published.</span></span> <span data-ttu-id="ef073-135">Muussa tapauksessa uudelleenohjaus ei toimi.</span><span class="sxs-lookup"><span data-stu-id="ef073-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="ef073-136">Valitse **OK** vahvistaaksesi linkityksen.</span><span class="sxs-lookup"><span data-stu-id="ef073-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="ef073-137">Jos käytät molemmissa virheluokissa yhtä tilakoodivirheen vastaussivua, toista tämä proseduuri ja linkitä alias myös toiseen saman sivun virheluokkaan.</span><span class="sxs-lookup"><span data-stu-id="ef073-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef073-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ef073-138">Additional resources</span></span>

[<span data-ttu-id="ef073-139">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="ef073-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="ef073-140">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="ef073-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ef073-141">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="ef073-141">Create a page URL</span></span>](create-page-url.md)
