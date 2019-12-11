---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tässä ohje aiheessa kuvataan tehtävät, jotka liittyvät uuden sähköisen kaupankäynnin sivuston luomiseen Dynamics 365 Commercessa.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697126"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="608bb-103">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="608bb-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="608bb-104">Tässä ohje aiheessa kuvataan tehtävät, jotka liittyvät uuden sähköisen kaupankäynnin sivuston luomiseen Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="608bb-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="608bb-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="608bb-105">Overview</span></span>

<span data-ttu-id="608bb-106">Jos haluat aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava sivuston muokkausympäristössä uusi sivusto.</span><span class="sxs-lookup"><span data-stu-id="608bb-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="608bb-107">Ennen kuin voit luoda uuden sivuston, Dynamics 365 Retail -sovellukseen on luotava vähintään yksi verkkokauppa.</span><span class="sxs-lookup"><span data-stu-id="608bb-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="608bb-108">Sivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="608bb-108">Set up your site</span></span>

<span data-ttu-id="608bb-109">Määritä sivusto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="608bb-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="608bb-110">Valitse Microsoft Lifecycle Services (LCS) -palvelussa sivuston muokkausympäristön linkki.</span><span class="sxs-lookup"><span data-stu-id="608bb-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="608bb-111">Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="608bb-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="608bb-112">Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="608bb-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="608bb-113">Kenttä</span><span class="sxs-lookup"><span data-stu-id="608bb-113">Field</span></span>                               | <span data-ttu-id="608bb-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="608bb-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="608bb-115">Sivuston nimi</span><span class="sxs-lookup"><span data-stu-id="608bb-115">Site name</span></span>                           | <span data-ttu-id="608bb-116">Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="608bb-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="608bb-117">Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="608bb-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="608bb-118">Sivuston järjestelmänvalvojan käyttöoikeusryhmä</span><span class="sxs-lookup"><span data-stu-id="608bb-118">Site administrator's security group</span></span> | <span data-ttu-id="608bb-119">Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="608bb-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="608bb-120">Oletuskanava (toimintayksikön numero)</span><span class="sxs-lookup"><span data-stu-id="608bb-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="608bb-121">Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on.</span><span class="sxs-lookup"><span data-stu-id="608bb-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="608bb-122">Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="608bb-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="608bb-123">Oletuskieli</span><span class="sxs-lookup"><span data-stu-id="608bb-123">Default language</span></span>                            | <span data-ttu-id="608bb-124">Määritä tämän verkkomyymälän ja -markkinan oletuskieli.</span><span class="sxs-lookup"><span data-stu-id="608bb-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="608bb-125">Verkkomyymälä voi tukea useita kieliä.</span><span class="sxs-lookup"><span data-stu-id="608bb-125">An online store can support multiple languages.</span></span> <span data-ttu-id="608bb-126">Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="608bb-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="608bb-127">Toimialue</span><span class="sxs-lookup"><span data-stu-id="608bb-127">Domain</span></span>                              | <span data-ttu-id="608bb-128">Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena.</span><span class="sxs-lookup"><span data-stu-id="608bb-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="608bb-129">Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="608bb-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="608bb-130">Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="608bb-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="608bb-131">Polku</span><span class="sxs-lookup"><span data-stu-id="608bb-131">Path</span></span>                              | <span data-ttu-id="608bb-132">Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="608bb-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="608bb-133">Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="608bb-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="608bb-134">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="608bb-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="608bb-135">Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="608bb-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="608bb-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="608bb-136">Additional resources</span></span>

[<span data-ttu-id="608bb-137">Verkkokaupan yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="608bb-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="608bb-138">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="608bb-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="608bb-139">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="608bb-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="608bb-140">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="608bb-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="608bb-141">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="608bb-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="608bb-142">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="608bb-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="608bb-143">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="608bb-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="608bb-144">Muokkauksen aloitussivun yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="608bb-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="608bb-145">Uuden sivuston sivun lisääminen</span><span class="sxs-lookup"><span data-stu-id="608bb-145">Add a new site page</span></span>](add-new-page.md)
