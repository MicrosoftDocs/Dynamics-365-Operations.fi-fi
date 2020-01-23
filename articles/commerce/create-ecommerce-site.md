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
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945832"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="0153d-103">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="0153d-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="0153d-104">Tässä ohje aiheessa kuvataan tehtävät, jotka liittyvät uuden sähköisen kaupankäynnin sivuston luomiseen Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="0153d-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0153d-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="0153d-105">Overview</span></span>

<span data-ttu-id="0153d-106">Jos haluat aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava sivuston muokkausympäristössä uusi sivusto.</span><span class="sxs-lookup"><span data-stu-id="0153d-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="0153d-107">Ennen kuin voit luoda uuden sivuston, Dynamics 365 Retail -sovellukseen on luotava vähintään yksi verkkokauppa.</span><span class="sxs-lookup"><span data-stu-id="0153d-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="0153d-108">Sivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0153d-108">Set up your site</span></span>

<span data-ttu-id="0153d-109">Määritä sivusto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0153d-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="0153d-110">Valitse Microsoft Lifecycle Services (LCS) -palvelussa sivuston muokkausympäristön linkki.</span><span class="sxs-lookup"><span data-stu-id="0153d-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="0153d-111">Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="0153d-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="0153d-112">Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="0153d-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="0153d-113">Kenttä</span><span class="sxs-lookup"><span data-stu-id="0153d-113">Field</span></span>                               | <span data-ttu-id="0153d-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0153d-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="0153d-115">Sivuston nimi</span><span class="sxs-lookup"><span data-stu-id="0153d-115">Site name</span></span>                           | <span data-ttu-id="0153d-116">Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="0153d-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="0153d-117">Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="0153d-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="0153d-118">Sivuston järjestelmänvalvojan käyttöoikeusryhmä</span><span class="sxs-lookup"><span data-stu-id="0153d-118">Site administrator's security group</span></span> | <span data-ttu-id="0153d-119">Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="0153d-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="0153d-120">Oletuskanava (toimintayksikön numero)</span><span class="sxs-lookup"><span data-stu-id="0153d-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="0153d-121">Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on.</span><span class="sxs-lookup"><span data-stu-id="0153d-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="0153d-122">Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0153d-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="0153d-123">Oletuskieli</span><span class="sxs-lookup"><span data-stu-id="0153d-123">Default language</span></span>                            | <span data-ttu-id="0153d-124">Määritä tämän verkkomyymälän ja -markkinan oletuskieli.</span><span class="sxs-lookup"><span data-stu-id="0153d-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="0153d-125">Verkkomyymälä voi tukea useita kieliä.</span><span class="sxs-lookup"><span data-stu-id="0153d-125">An online store can support multiple languages.</span></span> <span data-ttu-id="0153d-126">Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0153d-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="0153d-127">Toimialue</span><span class="sxs-lookup"><span data-stu-id="0153d-127">Domain</span></span>                              | <span data-ttu-id="0153d-128">Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena.</span><span class="sxs-lookup"><span data-stu-id="0153d-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="0153d-129">Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="0153d-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="0153d-130">Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="0153d-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="0153d-131">Polku</span><span class="sxs-lookup"><span data-stu-id="0153d-131">Path</span></span>                              | <span data-ttu-id="0153d-132">Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="0153d-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="0153d-133">Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="0153d-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="0153d-134">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="0153d-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="0153d-135">Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="0153d-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0153d-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0153d-136">Additional resources</span></span>

[<span data-ttu-id="0153d-137">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="0153d-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="0153d-138">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="0153d-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="0153d-139">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="0153d-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="0153d-140">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="0153d-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="0153d-141">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="0153d-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="0153d-142">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="0153d-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="0153d-143">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="0153d-143">Enable location-based store detection</span></span>](enable-store-detection.md)
