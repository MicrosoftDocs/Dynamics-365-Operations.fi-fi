---
title: Tilauksen vahvistusmoduuli
description: Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698323"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="c3405-103">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c3405-104">Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden luomisesta Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="c3405-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c3405-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c3405-105">Overview</span></span>

<span data-ttu-id="c3405-106">Tilauksen vahvistusmoduulin avulla näytetään vahvistussanoma tilausvahvistussivulla tilauksen asettamisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="c3405-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="c3405-107">Tilauksen vahvistusmoduulissa on tilauksen vahvistusnumero sekä uloskuittauksen aikana annettu asiakkaan sähköpostiosoite.</span><span class="sxs-lookup"><span data-stu-id="c3405-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="c3405-108">Jos tilaus tehdään uloskuittauksen aikana, tilauksen vahvistusnumero ja asiakkaan sähköpostiosoite välitetään tilausvahvistussivulle kyselymerkkijonona sivun URL-osoitteessa.</span><span class="sxs-lookup"><span data-stu-id="c3405-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="c3405-109">Tilauksen vahvistusmoduuli vastaanottaa nämä tiedot ja hahmontaa tilauksen tilan tilausvahvistussivulle.</span><span class="sxs-lookup"><span data-stu-id="c3405-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="c3405-110">Tilauksen vahvistusmoduuli vaatii tämän sivun kontekstin, jotta tilauksen tila voidaan antaa.</span><span class="sxs-lookup"><span data-stu-id="c3405-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="c3405-111">Tilauksen vahvistusmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="c3405-111">Order confirmation module properties</span></span>

| <span data-ttu-id="c3405-112">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="c3405-112">Property name</span></span> | <span data-ttu-id="c3405-113">Arvot</span><span class="sxs-lookup"><span data-stu-id="c3405-113">Values</span></span> | <span data-ttu-id="c3405-114">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="c3405-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c3405-115">Otsikko</span><span class="sxs-lookup"><span data-stu-id="c3405-115">Heading</span></span>       | <span data-ttu-id="c3405-116">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="c3405-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c3405-117">Tilauksen vahvistusmoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="c3405-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="c3405-118">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="c3405-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="c3405-119">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="c3405-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="c3405-120">Moduulit, joita voidaan käyttää tilausvahvistussivun moduulissa</span><span class="sxs-lookup"><span data-stu-id="c3405-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="c3405-121">**Suositukset** – Suositusten moduuli voidaan asettaa tilausvahvistussivulle ehdottamaan asiakkaalle muita tuotteita.</span><span class="sxs-lookup"><span data-stu-id="c3405-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="c3405-122">**Markkinointi** – Markkinointimoduuli voi lisätä markkinointisisältöä tilausvahvistussivulle.</span><span class="sxs-lookup"><span data-stu-id="c3405-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="c3405-123">Tilausvahvistussivun moduulin luominen</span><span class="sxs-lookup"><span data-stu-id="c3405-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="c3405-124">Luo sivumalli, jonka nimi on **Tilausvahvistusmalli**.</span><span class="sxs-lookup"><span data-stu-id="c3405-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="c3405-125">Lisää tilauksen vahvistusmoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="c3405-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="c3405-126">Lisää tilauksen vahvistusmoduuliin suositusten moduuli.</span><span class="sxs-lookup"><span data-stu-id="c3405-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="c3405-127">Tallenna ja esikatsele malli.</span><span class="sxs-lookup"><span data-stu-id="c3405-127">Save and preview the template.</span></span> <span data-ttu-id="c3405-128">Tilauksen vahvistusmoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="c3405-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="c3405-129">Kirjaa malli sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="c3405-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="c3405-130">Käytä juuri luotua tilauksen vahvistusmallia, kun haluat luoda sivun nimeltä **Tilausvahvistussivu**.</span><span class="sxs-lookup"><span data-stu-id="c3405-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="c3405-131">Lisää sivun jäsennykseen oletussivu.</span><span class="sxs-lookup"><span data-stu-id="c3405-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="c3405-132">Lisää **Ylätunniste**-paikkaan ylätunnisteen osa.</span><span class="sxs-lookup"><span data-stu-id="c3405-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="c3405-133">Lisää **Alatunniste**-paikkaan alatunnisteen osa.</span><span class="sxs-lookup"><span data-stu-id="c3405-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="c3405-134">Lisää tilauksen vahvistusmoduuli **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="c3405-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="c3405-135">Lisää tilauksen vahvistusmoduulin ominaisuusruudussa otsikon **tilausvahvistus**.</span><span class="sxs-lookup"><span data-stu-id="c3405-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="c3405-136">Lisää tilauksen vahvistusmoduulin alle suositusten moduuli ja määritä se niin, että se käyttää **Uusi**- ja **Myyvimmät**-asetuksia.</span><span class="sxs-lookup"><span data-stu-id="c3405-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="c3405-137">Tallenna ja esikatsele sivu, kirjaa se sisään ja julkaise se.</span><span class="sxs-lookup"><span data-stu-id="c3405-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3405-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="c3405-138">Additional resources</span></span>

[<span data-ttu-id="c3405-139">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="c3405-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c3405-140">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c3405-141">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c3405-142">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c3405-143">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c3405-144">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c3405-145">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="c3405-145">Footer module</span></span>](author-footer-module.md)
