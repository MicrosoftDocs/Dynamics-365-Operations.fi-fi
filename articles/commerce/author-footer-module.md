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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979944"
---
# <a name="footer-module"></a><span data-ttu-id="bdd2c-103">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdd2c-104">Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bdd2c-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bdd2c-105">Overview</span></span>

<span data-ttu-id="bdd2c-106">Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="bdd2c-107">Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="bdd2c-108">Seuraavassa kuvassa on esimerkki alatunnistemoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-108">The following image shows an example of a footer module on a site page.</span></span>

![Esimerkki alatunnistemoduulista](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="bdd2c-110">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bdd2c-110">Footer module properties</span></span> 

<span data-ttu-id="bdd2c-111">Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="bdd2c-112">Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="bdd2c-113">Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="bdd2c-114">Alatunnistemoduulissa käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="bdd2c-114">Modules available in a footer module</span></span>

<span data-ttu-id="bdd2c-115">**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="bdd2c-116">Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="bdd2c-117">Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).</span><span class="sxs-lookup"><span data-stu-id="bdd2c-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="bdd2c-118">**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="bdd2c-119">Kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-119">A destination is required.</span></span> <span data-ttu-id="bdd2c-120">Kohteen oletusarvo on \#. Se vie käyttäjän sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="bdd2c-121">Alatunnistemoduulin lisääminen</span><span class="sxs-lookup"><span data-stu-id="bdd2c-121">Create a footer module</span></span>

1. <span data-ttu-id="bdd2c-122">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="bdd2c-123">Valitse **Uusi osa** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="bdd2c-124">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bdd2c-125">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnisteluokka**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bdd2c-126">Valitse kolme pistettä (**...**) **Alatunnisteluokka**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bdd2c-127">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnistenimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bdd2c-128">Valitse **Alatunnistenimike**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="bdd2c-129">Voit lisätä alatunnistenimikkeitä toistamalla kullekin kohtien 5–7 toimet.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="bdd2c-130">Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla **Alatunnisteluokka**-paikka jäsennyspuussa kolmen pistettä (**...**) ja valitsemalla sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="bdd2c-131">Valitse **Lisää moduuli** -valintaikkunassa **Palaa alkuun** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bdd2c-132">Valitse **Palaa alkuun**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa teksti ja muut moduuliominaisuudet halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="bdd2c-133">Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bdd2c-134">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="bdd2c-135">Lisää **Alatunniste**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="bdd2c-136">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bdd2c-137">Kun lisäät sivumalleihin osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="bdd2c-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdd2c-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bdd2c-138">Additional resources</span></span>

[<span data-ttu-id="bdd2c-139">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bdd2c-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bdd2c-140">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bdd2c-141">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bdd2c-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bdd2c-143">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bdd2c-144">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bdd2c-145">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bdd2c-146">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bdd2c-146">Footer module</span></span>](author-footer-module.md)
