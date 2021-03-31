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
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211445"
---
# <a name="footer-module"></a><span data-ttu-id="bbb70-103">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="bbb70-104">Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="bbb70-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="bbb70-105">Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin.</span><span class="sxs-lookup"><span data-stu-id="bbb70-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="bbb70-106">Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="bbb70-107">Seuraavassa kuvassa on esimerkki alatunnistemoduulista sivuston sivulla.</span><span class="sxs-lookup"><span data-stu-id="bbb70-107">The following image shows an example of a footer module on a site page.</span></span>

![Esimerkki alatunnistemoduulista](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="bbb70-109">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="bbb70-109">Footer module properties</span></span> 

<span data-ttu-id="bbb70-110">Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="bbb70-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="bbb70-111">Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="bbb70-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="bbb70-112">Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="bbb70-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="bbb70-113">Alatunnistemoduulissa käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="bbb70-113">Modules available in a footer module</span></span>

<span data-ttu-id="bbb70-114">**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin.</span><span class="sxs-lookup"><span data-stu-id="bbb70-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="bbb70-115">Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa.</span><span class="sxs-lookup"><span data-stu-id="bbb70-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="bbb70-116">Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).</span><span class="sxs-lookup"><span data-stu-id="bbb70-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="bbb70-117">**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan.</span><span class="sxs-lookup"><span data-stu-id="bbb70-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="bbb70-118">Kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="bbb70-118">A destination is required.</span></span> <span data-ttu-id="bbb70-119">Kohteen oletusarvo on \#. Se vie käyttäjän sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="bbb70-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="bbb70-120">Alatunnistemoduulin lisääminen</span><span class="sxs-lookup"><span data-stu-id="bbb70-120">Create a footer module</span></span>

1. <span data-ttu-id="bbb70-121">Siirry kohtaan **Osat** ja **Uusi** luodaksesi uuden osan.</span><span class="sxs-lookup"><span data-stu-id="bbb70-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="bbb70-122">Valitse **Uusi osa** -valintaikkunassa **Kontti**-moduuli. Syötä osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="bbb70-123">Valitse kolme pistettä (**...**) **Oletuskontti**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbb70-124">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnisteluokka**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbb70-125">Valitse kolme pistettä (**...**) **Alatunnisteluokka**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbb70-126">Valitse **Lisää moduuli** -valintaikkunassa **Alatunnistenimike**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbb70-127">Valitse **Alatunnistenimike**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bbb70-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="bbb70-128">Voit lisätä alatunnistenimikkeitä toistamalla kullekin kohtien 5–7 toimet.</span><span class="sxs-lookup"><span data-stu-id="bbb70-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="bbb70-129">Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla **Alatunnisteluokka**-paikka jäsennyspuussa kolmen pistettä (**...**) ja valitsemalla sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="bbb70-130">Valitse **Lisää moduuli** -valintaikkunassa **Palaa alkuun** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="bbb70-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="bbb70-131">Valitse **Palaa alkuun**-paikka ja määritä sitten oikeanpuoleisessa ominaisuusruudussa teksti ja muut moduuliominaisuudet halutulla tavalla.</span><span class="sxs-lookup"><span data-stu-id="bbb70-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="bbb70-132">Valitse **Lopeta muokkaus** tallentaaksesi osan ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="bbb70-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bbb70-133">Voit varmistaa, että ylätunniste näkyy jokaisella sivulla, noudattamalla näitä ohjeita jokaisen sivustolle luodun sivumallin kohdalla.</span><span class="sxs-lookup"><span data-stu-id="bbb70-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="bbb70-134">Lisää **Alatunniste**-moduulin **Otsikko**-paikkaan alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="bbb70-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="bbb70-135">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="bbb70-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="bbb70-136">Kun lisäät sivumalleihin osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="bbb70-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbb70-137">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="bbb70-137">Additional resources</span></span>

[<span data-ttu-id="bbb70-138">Moduulikirjaston yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="bbb70-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bbb70-139">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bbb70-140">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bbb70-141">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bbb70-142">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bbb70-143">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bbb70-144">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bbb70-145">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="bbb70-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]