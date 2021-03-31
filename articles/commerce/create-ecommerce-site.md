---
title: Sähköisen kaupankäynnin sivuston luominen
description: Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 465154ef7209547481c8598d5eaefb434359b1fd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207970"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="7ff4c-103">Sähköisen kaupankäynnin sivuston luominen</span><span class="sxs-lookup"><span data-stu-id="7ff4c-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ff4c-104">Tämä ohjeaihe sisältää ohjeet ja tiedot, jotka tarvitaan uuden sähköisen kaupankäynnin sivun luomiseen Dynamics 365 Commerce sivustonmuodostimessa.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="7ff4c-105">Kun lisensoit Dynamics 365 Commercen ominaisuuksia, sivuston luontiohjelmalle valmistellaan aloitussivusto, jota voit käyttää oman sivustosi pohjana.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="7ff4c-106">Jos kuitenkin haluat tehdä kaiken alusta tai jos haluat luoda toisen sivuston, sinun on luotava uusi sivusto sivuston muokkausympäristössä.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="7ff4c-107">Sivuston määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ff4c-107">Set up your site</span></span>

<span data-ttu-id="7ff4c-108">Määritä sivusto seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="7ff4c-109">Avaa sivustonmuodostimen ympäristö.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-109">Open the site builder environment.</span></span> <span data-ttu-id="7ff4c-110">Löydät linkin sivustonmuodostimeen Microsoft Lifecycle Servicesin (LCS) ympäristöominaisuuksien sivulta.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="7ff4c-111">Valitse sivuston muokkausympäristön aloitussivulla **Uusi sivusto**.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="7ff4c-112">Anna seuraavat tiedot **Uusi sivusto** -valintaikkunaan.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="7ff4c-113">Kenttä</span><span class="sxs-lookup"><span data-stu-id="7ff4c-113">Field</span></span>                               | <span data-ttu-id="7ff4c-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="7ff4c-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="7ff4c-115">Sivuston nimi</span><span class="sxs-lookup"><span data-stu-id="7ff4c-115">Site name</span></span>                           | <span data-ttu-id="7ff4c-116">Anna näyttönimi, jota käytetään sivuston muokkausympäristön sivustossa.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="7ff4c-117">Tämä nimi näkyy vain muokkausympäristössä. Se ei näy asiakkaille.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="7ff4c-118">Sivuston järjestelmänvalvojan käyttöoikeusryhmä</span><span class="sxs-lookup"><span data-stu-id="7ff4c-118">Site administrator's security group</span></span> | <span data-ttu-id="7ff4c-119">Määritä Microsoft Azure Active Directory (Azure AD) -käyttöoikeusryhmä. Se hallitsee käyttäjiä, joilla on tämän sivuston järjestelmänvalvojan rooli.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="7ff4c-120">Oletuskanava (toimintayksikön numero)</span><span class="sxs-lookup"><span data-stu-id="7ff4c-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="7ff4c-121">Valitse verkkomyymälä, jonka verkkomyymälä tämä sivusto on.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="7ff4c-122">Jos haluat, että sähköisen kaupankäynnin sivusto tukee useita verkkomyymälöitä, liitä myymälät sivustoon **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="7ff4c-123">Oletuskieli</span><span class="sxs-lookup"><span data-stu-id="7ff4c-123">Default language</span></span>                            | <span data-ttu-id="7ff4c-124">Määritä tämän verkkomyymälän ja -markkinan oletuskieli.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="7ff4c-125">Verkkomyymälä voi tukea useita kieliä.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-125">An online store can support multiple languages.</span></span> <span data-ttu-id="7ff4c-126">Jos haluat, että tämä verkkomyymälä tai toinen verkkomyymälä tukee useita kieliä, määritä tuki **Sivuston asetukset** -kohdassa sivuston määrityksen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="7ff4c-127">Toimialue</span><span class="sxs-lookup"><span data-stu-id="7ff4c-127">Domain</span></span>                              | <span data-ttu-id="7ff4c-128">Valitse toimialueen nimi, joka toimii tämän verkkomyymälän toimialueena.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="7ff4c-129">Jos et ole määrittänyt toimialueita LCS:ssä, voit jättää tämän kentän tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="7ff4c-130">Kun toimialue on määritetty LCS:ssä, lisää se verkkomyymälään **Sivuston asetukset** -kohdassa.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="7ff4c-131">Polku</span><span class="sxs-lookup"><span data-stu-id="7ff4c-131">Path</span></span>                              | <span data-ttu-id="7ff4c-132">Kun sivusto tukee useita kieliä tietyssä toimialueessa, käytä polkukenttää ja luo yksilöivä sivuston URL-osoite kyseiselle toimialueelle ja kielen yhdistelmälle.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="7ff4c-133">Jos **Oletuskieli**-kentässä määritetty kieli on ainoa kieli, jota tuetaan tässä toimialueessa, tai jos se on oletuskieli sen jälkeen kun sivusto on lokalisoitu muille kielille, suosittelemme, että tämä kenttä jätetään tyhjäksi.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="7ff4c-134">Kun sivusto on luotu, voit varmistaa, että se on liitetty verkkomyymälään, valitsemalla **Tuotteet**-välilehden. Näkyvissä on tuotevalikoima, joka on määritetty verkkomyymälälle.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="7ff4c-135">Voit käyttää avattavaa valikkoa sivun vasemmassa yläosassa, jos haluat käyttää kohdistettuja tuotteita luokan mukaan.</span><span class="sxs-lookup"><span data-stu-id="7ff4c-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ff4c-136">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7ff4c-136">Additional resources</span></span>

[<span data-ttu-id="7ff4c-137">Toimialueen nimen määrittäminen</span><span class="sxs-lookup"><span data-stu-id="7ff4c-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7ff4c-138">Uuden sähköisen kaupankäynnin vuokraajan käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="7ff4c-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7ff4c-139">Dynamics 365 Commerce -sivuston liittäminen online-kanavaan</span><span class="sxs-lookup"><span data-stu-id="7ff4c-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7ff4c-140">Robots.txt-tiedostojen hallinta</span><span class="sxs-lookup"><span data-stu-id="7ff4c-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7ff4c-141">URL-uudelleenohjausten joukkolataus palveluun</span><span class="sxs-lookup"><span data-stu-id="7ff4c-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7ff4c-142">B2C-vuokraajan määrittäminen Commercessa</span><span class="sxs-lookup"><span data-stu-id="7ff4c-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7ff4c-143">Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten</span><span class="sxs-lookup"><span data-stu-id="7ff4c-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7ff4c-144">Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä</span><span class="sxs-lookup"><span data-stu-id="7ff4c-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7ff4c-145">Sisältöverkon (CDN) tuen lisääminen</span><span class="sxs-lookup"><span data-stu-id="7ff4c-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7ff4c-146">Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto</span><span class="sxs-lookup"><span data-stu-id="7ff4c-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]