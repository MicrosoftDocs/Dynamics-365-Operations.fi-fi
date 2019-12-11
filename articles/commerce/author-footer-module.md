---
title: Alatunnistemoduuli
description: Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden muokkaamisesta Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 7c253cd9620180b09f2f5cae232e46d236deabdd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697310"
---
# <a name="footer-module"></a><span data-ttu-id="ae151-103">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-103">Footer module</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ae151-104">Tässä ohjeaiheessa on tietoja alatunnistemoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="ae151-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ae151-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ae151-105">Overview</span></span>

<span data-ttu-id="ae151-106">Alatunnistemoduuli on erillinen säilö, jota käytetään sivun alatunnisteessa näkyvien moduulien isännöintiin.</span><span class="sxs-lookup"><span data-stu-id="ae151-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="ae151-107">Se voi esimerkiksi sisältää linkkejä eri sivuston sivuille. Sivu voi olla esimerkiksi **Ota yhteyttä** tai **Myymälän käytännöt**.</span><span class="sxs-lookup"><span data-stu-id="ae151-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="ae151-108">Ylätunnistemoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="ae151-108">Footer module properties</span></span> 

<span data-ttu-id="ae151-109">Useimpien säilöjen tapaan alatunnistemoduuli tukee otsikon ja leveyden ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="ae151-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="ae151-110">Se tukee myös useiden alatunnisteluokkamoduulien lisäämistä.</span><span class="sxs-lookup"><span data-stu-id="ae151-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="ae151-111">Jokainen lisätty alatunnisteluokkamoduuli hahmonnetaan sarakkeeksi alatunnistemoduuliin.</span><span class="sxs-lookup"><span data-stu-id="ae151-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="ae151-112">Alatunnistemoduulissa käytettävissä olevat moduulit</span><span class="sxs-lookup"><span data-stu-id="ae151-112">Modules available in a footer module</span></span>

<span data-ttu-id="ae151-113">**Alatunnistenimikkeet** – Alatunnistenimikkeiden moduuli voi sisältää otsikon, kuvan ja linkin.</span><span class="sxs-lookup"><span data-stu-id="ae151-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="ae151-114">Otsikkoa voidaan käyttää yksin tai yhdessä kuvan ja linkin kanssa.</span><span class="sxs-lookup"><span data-stu-id="ae151-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="ae151-115">Jokainen alatunnisteen linkki voidaan määrittää siten, että siinä on vain teksti (esimerkiksi Ota yhteyttä ja Tietosuojalinkit) tai niin, että sillä on sekä tekstiä että kuva (esimerkiksi yhteisöpalveluiden linkit).</span><span class="sxs-lookup"><span data-stu-id="ae151-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="ae151-116">**Palaa alkuun** – Palaa alkuun -moduuli sisältää linkin, jonka avulla voi siirtyä nopeasti sivun yläreunaan.</span><span class="sxs-lookup"><span data-stu-id="ae151-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="ae151-117">Kohde on määritettävä.</span><span class="sxs-lookup"><span data-stu-id="ae151-117">A destination is required.</span></span> <span data-ttu-id="ae151-118">Kohteen oletusarvo on #. Se vie käyttäjän sivun yläosaan.</span><span class="sxs-lookup"><span data-stu-id="ae151-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="ae151-119">Alatunnistemoduulin muokkaaminen</span><span class="sxs-lookup"><span data-stu-id="ae151-119">Author a footer module</span></span>

1. <span data-ttu-id="ae151-120">Valitse siirtymisruudussa **Osat** ja valitse sitten **Uusi sivun osa**.</span><span class="sxs-lookup"><span data-stu-id="ae151-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ae151-121">Valitse **Uusi sivun osa** -valintaikkunassa alatunnistemoduuli. Syötä sivun osan nimi ja valitse **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae151-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="ae151-122">Valitse vasemmanpuoleisessa jäsennyspuussa alatunnistemoduulin kolmen pisteen painike (**...**) ja valitse **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="ae151-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ae151-123">Valitse **Lisää moduuli** -valintaikkunassa alatunnisteluokkamoduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae151-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="ae151-124">Valitse jäsennyspuussa alatunnisteluokkamoduulin kolmen pisteen painike (...) ja valitse **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="ae151-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ae151-125">Valitse **Lisää moduuli** -valintaikkunassa alatunnistenimikemoduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae151-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="ae151-126">Valitse jäsennyspuussa alatunnistenimikemoduuli.</span><span class="sxs-lookup"><span data-stu-id="ae151-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="ae151-127">Määritä sitten oikeanpuoleisessa ominaisuusruudussa otsikko, linkki, linkin teksti ja kuvat haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="ae151-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="ae151-128">Voit lisätä alatunnistenimikkeitä toistamalla kohtien 5–7 toimet.</span><span class="sxs-lookup"><span data-stu-id="ae151-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="ae151-129">Voit lisätä Palaa alkuun -linkin alatunnisteeseen valitsemalla alatunnisteluokkamoduulin jäsennyspuussa kolmen pisteen painikkeen ja valitsemalla sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="ae151-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ae151-130">Valitse **Lisää moduuli** -valintaikkunassa Palaa alkuun -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae151-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="ae151-131">Valitse jäsennyspuussa Palaa alkuun -moduuli.</span><span class="sxs-lookup"><span data-stu-id="ae151-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="ae151-132">Määritä sitten oikeanpuoleisessa ominaisuusruudussa Palaa alkuun -moduuli haluamallasi tavalla.</span><span class="sxs-lookup"><span data-stu-id="ae151-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="ae151-133">Tallenna sivun osa, kirjaa se sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="ae151-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="ae151-134">Noudata seuraavia vaiheita jokaiselle sivustolle luodulle sivumallille.</span><span class="sxs-lookup"><span data-stu-id="ae151-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="ae151-135">Lisää oletussivun **pääpaikkaan** alatunnistemoduulissa luomasi alatunnisteosa.</span><span class="sxs-lookup"><span data-stu-id="ae151-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="ae151-136">Tallenna malli, kirjaa se sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="ae151-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="ae151-137">Kun lisäät sivumalleihin sivun osan, voit varmistaa, että alatunniste hahmonnetaan jokaiselle sivulle.</span><span class="sxs-lookup"><span data-stu-id="ae151-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae151-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ae151-138">Additional resources</span></span>

[<span data-ttu-id="ae151-139">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="ae151-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ae151-140">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="ae151-141">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ae151-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ae151-143">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ae151-144">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ae151-145">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ae151-146">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ae151-146">Footer module</span></span>](author-footer-module.md)
