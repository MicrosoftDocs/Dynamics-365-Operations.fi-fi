---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096771"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="a6701-103">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="a6701-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a6701-104">Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="a6701-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="a6701-105">Ennen kuin voit aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava uusi sivusto sivustuonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="a6701-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="a6701-106">Jos haluat aloittaa sähköisen kaupankäynnin sivuston kehittämisen, sinun on ensin luotava sivuston muokkausympäristössä uusi sivusto.</span><span class="sxs-lookup"><span data-stu-id="a6701-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="a6701-107">Ennen kuin voit luoda uuden sivuston, Commerce-sovellukseen on luotava vähintään yksi verkkokauppa.</span><span class="sxs-lookup"><span data-stu-id="a6701-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="a6701-108">Sivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a6701-108">Set up your site</span></span>

<span data-ttu-id="a6701-109">Määritä sivusto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="a6701-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="a6701-110">Avaa sivustonmuodostimen ympäristö.</span><span class="sxs-lookup"><span data-stu-id="a6701-110">Open the site builder environment.</span></span> <span data-ttu-id="a6701-111">Löydät linkin sivustonmuodostimeen Microsoft Lifecycle Servicesin (LCS) ympäristöominaisuuksien sivulta.</span><span class="sxs-lookup"><span data-stu-id="a6701-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="a6701-112">Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="a6701-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="a6701-113">Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="a6701-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="a6701-114">Kenttä</span><span class="sxs-lookup"><span data-stu-id="a6701-114">Field</span></span>                               | <span data-ttu-id="a6701-115">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="a6701-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="a6701-116">Sivuston nimi</span><span class="sxs-lookup"><span data-stu-id="a6701-116">Site name</span></span>                           | <span data-ttu-id="a6701-117">Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="a6701-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="a6701-118">Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="a6701-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="a6701-119">Sivuston järjestelmänvalvojan käyttöoikeusryhmä</span><span class="sxs-lookup"><span data-stu-id="a6701-119">Site administrator's security group</span></span> | <span data-ttu-id="a6701-120">Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="a6701-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="a6701-121">Oletuskanava (toimintayksikön numero)</span><span class="sxs-lookup"><span data-stu-id="a6701-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="a6701-122">Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on.</span><span class="sxs-lookup"><span data-stu-id="a6701-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="a6701-123">Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a6701-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="a6701-124">Oletuskieli</span><span class="sxs-lookup"><span data-stu-id="a6701-124">Default language</span></span>                            | <span data-ttu-id="a6701-125">Määritä tämän verkkomyymälän ja -markkinan oletuskieli.</span><span class="sxs-lookup"><span data-stu-id="a6701-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="a6701-126">Verkkomyymälä voi tukea useita kieliä.</span><span class="sxs-lookup"><span data-stu-id="a6701-126">An online store can support multiple languages.</span></span> <span data-ttu-id="a6701-127">Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="a6701-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="a6701-128">Toimialue</span><span class="sxs-lookup"><span data-stu-id="a6701-128">Domain</span></span>                              | <span data-ttu-id="a6701-129">Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena.</span><span class="sxs-lookup"><span data-stu-id="a6701-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="a6701-130">Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="a6701-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="a6701-131">Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="a6701-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="a6701-132">Polku</span><span class="sxs-lookup"><span data-stu-id="a6701-132">Path</span></span>                              | <span data-ttu-id="a6701-133">Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="a6701-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="a6701-134">Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="a6701-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="a6701-135">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="a6701-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="a6701-136">Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="a6701-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6701-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="a6701-137">Additional resources</span></span>

[<span data-ttu-id="a6701-138">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="a6701-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a6701-139">Uuden sähköisen kaupankäynnin sivuston käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="a6701-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a6701-140">Määritä verkkokauppakanava</span><span class="sxs-lookup"><span data-stu-id="a6701-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="a6701-141">Liitä verkkosivusto kanavaan</span><span class="sxs-lookup"><span data-stu-id="a6701-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a6701-142">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="a6701-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="a6701-143">URL-osoitteen uudelleenohjausten lataaminen joukkona</span><span class="sxs-lookup"><span data-stu-id="a6701-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="a6701-144">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="a6701-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="a6701-145">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="a6701-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a6701-146">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="a6701-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a6701-147">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="a6701-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a6701-148">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="a6701-148">Enable location-based store detection</span></span>](enable-store-detection.md)
