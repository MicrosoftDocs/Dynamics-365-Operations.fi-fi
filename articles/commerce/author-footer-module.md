---
title: Alatunnistemoduuli
description: Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden muokkaamisesta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816958"
---
# <a name="footer-module"></a><span data-ttu-id="c6cdf-103">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6cdf-104">Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c6cdf-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c6cdf-105">Overview</span></span>

<span data-ttu-id="c6cdf-106">Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="c6cdf-107">Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="c6cdf-108">Seuraavassa kuvassa on esimerkki alatunnistemoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-108">The following image shows an example of a footer module on a site page.</span></span>

![Esimerkki alatunnistemoduulista](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="c6cdf-110">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="c6cdf-110">Footer module properties</span></span> 

<span data-ttu-id="c6cdf-111">Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="c6cdf-112">Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="c6cdf-113">Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="c6cdf-114">Alatunnistemoduulissa käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="c6cdf-114">Modules available in a footer module</span></span>

<span data-ttu-id="c6cdf-115">**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="c6cdf-116">Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="c6cdf-117">Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).</span><span class="sxs-lookup"><span data-stu-id="c6cdf-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="c6cdf-118">**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="c6cdf-119">Kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-119">A destination is required.</span></span> <span data-ttu-id="c6cdf-120">Kohteen oletusarvo on \#. Se vie käyttäjän sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="c6cdf-121">Alatunnistemoduulin lisääminen</span><span class="sxs-lookup"><span data-stu-id="c6cdf-121">Create a footer module</span></span>

1. <span data-ttu-id="c6cdf-122">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="c6cdf-123">Valitse **Uusi osa** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c6cdf-124">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c6cdf-125">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnisteluokka**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c6cdf-126">Valitse kolme pistettä (**...**) **Alatunnisteluokka**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c6cdf-127">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnistenimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c6cdf-128">Valitse **Alatunnistenimike**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="c6cdf-129">Voit lisätä alatunnistenimikkeitä toistamalla kullekin kohtien 5–7 toimet.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="c6cdf-130">Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla **Alatunnisteluokka**-paikka jäsennyspuussa kolmen pistettä (**...**) ja valitsemalla sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="c6cdf-131">Valitse **Lisää moduuli** -valintaikkunassa **Palaa alkuun** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c6cdf-132">Valitse **Palaa alkuun**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa teksti ja muut moduuliominaisuudet halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="c6cdf-133">Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="c6cdf-134">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="c6cdf-135">Lisää **Alatunniste**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="c6cdf-136">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="c6cdf-137">Kun lisäät sivumalleihin osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="c6cdf-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6cdf-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c6cdf-138">Additional resources</span></span>

[<span data-ttu-id="c6cdf-139">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c6cdf-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c6cdf-140">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c6cdf-141">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c6cdf-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c6cdf-143">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c6cdf-144">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c6cdf-145">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c6cdf-146">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c6cdf-146">Footer module</span></span>](author-footer-module.md)
