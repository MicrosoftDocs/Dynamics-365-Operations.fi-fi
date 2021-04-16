---
title: Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille
description: Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799641"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="76009-103">Mukautettujen vastaussivujen luominen 4xx-/5xx-tilakoodien virheille</span><span class="sxs-lookup"><span data-stu-id="76009-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76009-104">Tässä ohjeaiheessa kerrotaan, miten mukautetut vastaussivut luodaan 4xx- ja 5xx-tilakoodivirheille käyttämällä Microsoft Dynamics 365 Commercen muokkaustyökaluja.</span><span class="sxs-lookup"><span data-stu-id="76009-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="76009-105">Jos pyyntö ei onnistu, palvelin antaa HTTP-tilakoodivirhevastaukset.</span><span class="sxs-lookup"><span data-stu-id="76009-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="76009-106">404-tilakoodi tallennetaan ja palautetaan, jos sivua ei löydy. 500-tilakoodi tallennetaan ja palautetaan, jos tapahtuu palvelinvirhe.</span><span class="sxs-lookup"><span data-stu-id="76009-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="76009-107">Dynamics 365 Commercessa sovelluksen käyttäjät voivat luoda mukautettuja tilakoodivirheiden vastausten sivuja, jotka näytetään käyttäjille näiden tilavirhekoodivirheiden vastauksina.</span><span class="sxs-lookup"><span data-stu-id="76009-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="76009-108">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="76009-108">Build a status code error response page</span></span>

<span data-ttu-id="76009-109">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="76009-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="76009-110">Kirjaudu haluamallasi selaimella sisään Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="76009-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="76009-111">Valitse sivusto, jolle haluat luoda 4xx-/5xx-tilakoodivirheen vastaussivun.</span><span class="sxs-lookup"><span data-stu-id="76009-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="76009-112">Mallin luominen</span><span class="sxs-lookup"><span data-stu-id="76009-112">Build the template</span></span>

<span data-ttu-id="76009-113">Voit luoda tilakoodivirheen vastaussivun mallin seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="76009-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="76009-114">Valitse **Mallit**.</span><span class="sxs-lookup"><span data-stu-id="76009-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="76009-115">Luo sivumalli valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="76009-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="76009-116">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan uuden mallin nimi ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="76009-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="76009-117">Luo malli sen rakenteen perusteella, jonka haluat määrittää tilakoodivirheen vastaussivulle.</span><span class="sxs-lookup"><span data-stu-id="76009-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="76009-118">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi mallin, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="76009-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="76009-119">Tilakoodivirheen vastaussivun luominen</span><span class="sxs-lookup"><span data-stu-id="76009-119">Build the status code error response page</span></span>

<span data-ttu-id="76009-120">Voit luoda tilakoodivirheen vastaussivun seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="76009-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="76009-121">Siirry kohtaan **Sivut**.</span><span class="sxs-lookup"><span data-stu-id="76009-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="76009-122">Luo sivu valitsemalla **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="76009-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="76009-123">Valitse malli **Valitse malli** -valinta ikkunassa ja kirjoita sitten **Sivun nimi** -kohtaan tilakoodin virhevastaussivun nimi.</span><span class="sxs-lookup"><span data-stu-id="76009-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="76009-124">Jätä **Sivun URL-osoite** -kenttä tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="76009-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="76009-125">Luo sivu.</span><span class="sxs-lookup"><span data-stu-id="76009-125">Build the page.</span></span>
1. <span data-ttu-id="76009-126">Valitse **Tallenna**, valitse **Viimeistele muokkaus** tarkistaaksesi sivun, ja julkaise se valitsemalla **Julkaise**.</span><span class="sxs-lookup"><span data-stu-id="76009-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="76009-127">Voit luoda erilliset tilakoodivirheen vastaussivut 4xx- ja 5xx-tilakoodivirheille.</span><span class="sxs-lookup"><span data-stu-id="76009-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="76009-128">Halutessasi voit käyttää samaa yleistä tilakoodivirheen vastaussivua molemmissa virheluokissa.</span><span class="sxs-lookup"><span data-stu-id="76009-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="76009-129">Tilakoodivirheen vastaussivun uudelleenohjauksen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="76009-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="76009-130">Voit määrittää tilakoodivirheen vastaussivun uudelleenohjauksen seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="76009-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="76009-131">Siirry kohtaan **URL-osoitteet \> Uusi \> Uusi alias** ja valitse aiemmin luotu tilakoodivirheen vastaussivu.</span><span class="sxs-lookup"><span data-stu-id="76009-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="76009-132">Syötä **Alias**-kenttään **oletusarvo - 4xx** tai **oletusarvo - 5xx** sen mukaan, mille tilakoodivirheen vastaussivulle olet määrittämässä uudelleenohjausta.</span><span class="sxs-lookup"><span data-stu-id="76009-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="76009-133">Nämä aliakset on julkaistava.</span><span class="sxs-lookup"><span data-stu-id="76009-133">These aliases must be published.</span></span> <span data-ttu-id="76009-134">Muussa tapauksessa uudelleenohjaus ei toimi.</span><span class="sxs-lookup"><span data-stu-id="76009-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="76009-135">Valitse **OK** vahvistaaksesi linkityksen.</span><span class="sxs-lookup"><span data-stu-id="76009-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="76009-136">Jos käytät molemmissa virheluokissa yhtä tilakoodivirheen vastaussivua, toista tämä proseduuri ja linkitä alias myös toiseen saman sivun virheluokkaan.</span><span class="sxs-lookup"><span data-stu-id="76009-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76009-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="76009-137">Additional resources</span></span>

[<span data-ttu-id="76009-138">Mallien käyttö</span><span class="sxs-lookup"><span data-stu-id="76009-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="76009-139">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="76009-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="76009-140">Sivun URL-osoitteen luominen</span><span class="sxs-lookup"><span data-stu-id="76009-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
