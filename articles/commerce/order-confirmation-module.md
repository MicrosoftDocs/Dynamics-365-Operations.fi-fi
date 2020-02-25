---
title: Tilauksen tiedot -moduuli
description: Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026014"
---
# <a name="order-details-module"></a><span data-ttu-id="8adba-103">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8adba-104">Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="8adba-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8adba-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8adba-105">Overview</span></span>

<span data-ttu-id="8adba-106">Tilaustiedot-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="8adba-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="8adba-107">Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot ja toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="8adba-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="8adba-108">Tilauksen vahvistusmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="8adba-108">Order confirmation module properties</span></span>

| <span data-ttu-id="8adba-109">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="8adba-109">Property name</span></span>  | <span data-ttu-id="8adba-110">Arvot</span><span class="sxs-lookup"><span data-stu-id="8adba-110">Values</span></span> | <span data-ttu-id="8adba-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="8adba-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="8adba-112">Otsikko</span><span class="sxs-lookup"><span data-stu-id="8adba-112">Heading</span></span>        | <span data-ttu-id="8adba-113">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="8adba-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="8adba-114">Tilauksen vahvistusmoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="8adba-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="8adba-115">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="8adba-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="8adba-116">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="8adba-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="8adba-117">Yhteyshenkilön puhelinnumero</span><span class="sxs-lookup"><span data-stu-id="8adba-117">Contact number</span></span> | <span data-ttu-id="8adba-118">Text</span><span class="sxs-lookup"><span data-stu-id="8adba-118">Text</span></span> | <span data-ttu-id="8adba-119">Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero.</span><span class="sxs-lookup"><span data-stu-id="8adba-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="8adba-120">Moduulit, joita voidaan käyttää tilaustietosivulla</span><span class="sxs-lookup"><span data-stu-id="8adba-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="8adba-121">Kun luot tilaustiedot-sivun, voit lisätä muita asiaankuuluvia moduuleja tilaustiedot-moduulin lisäksi.</span><span class="sxs-lookup"><span data-stu-id="8adba-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="8adba-122">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="8adba-122">Here are some examples:</span></span>

- <span data-ttu-id="8adba-123">**Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilaustietosivulle ehdottamaan asiakkaalle muita tuotteita.</span><span class="sxs-lookup"><span data-stu-id="8adba-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="8adba-124">**Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilaustiedot-sivulle.</span><span class="sxs-lookup"><span data-stu-id="8adba-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="8adba-125">Tilaustietosivun moduulin luominen</span><span class="sxs-lookup"><span data-stu-id="8adba-125">Create an order details page module</span></span>

1. <span data-ttu-id="8adba-126">Luo sivumalli, jonka nimi on **Tilaustiedot -malli**.</span><span class="sxs-lookup"><span data-stu-id="8adba-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="8adba-127">Lisää tilauksen tietomoduuli oletussivun **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="8adba-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="8adba-128">Lisää tilauksen tietomoduuliin suositusten moduuli.</span><span class="sxs-lookup"><span data-stu-id="8adba-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="8adba-129">Tallenna ja esikatsele malli.</span><span class="sxs-lookup"><span data-stu-id="8adba-129">Save and preview the template.</span></span> <span data-ttu-id="8adba-130">Tilauksen tietomoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="8adba-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="8adba-131">Kun mallin muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="8adba-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="8adba-132">Käytä juuri luotua tilauksen tietomallia, kun haluat luoda sivun nimeltä **Tilaustietosivu**.</span><span class="sxs-lookup"><span data-stu-id="8adba-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="8adba-133">Lisää sivun jäsennykseen oletussivu.</span><span class="sxs-lookup"><span data-stu-id="8adba-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="8adba-134">Lisää **Ylätunniste**-paikkaan ylätunnisteen osa.</span><span class="sxs-lookup"><span data-stu-id="8adba-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="8adba-135">Lisää **Alatunniste**-paikkaan alatunnisteen osa.</span><span class="sxs-lookup"><span data-stu-id="8adba-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="8adba-136">Lisää tilauksen tietomoduuli **pääpaikkaan**.</span><span class="sxs-lookup"><span data-stu-id="8adba-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="8adba-137">Lisää tilauksen tietomoduulin ominaisuusruudussa otsikko **Tilaustiedot**.</span><span class="sxs-lookup"><span data-stu-id="8adba-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="8adba-138">Lisää tilauksen tietomoduulin alle suositusten moduuli ja määritä se niin, että se käyttää **Uusi**- ja **Myyvimmät**-asetuksia.</span><span class="sxs-lookup"><span data-stu-id="8adba-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="8adba-139">Tallenna ja esikatsele sivu.</span><span class="sxs-lookup"><span data-stu-id="8adba-139">Save and preview the page.</span></span>
1. <span data-ttu-id="8adba-140">Kun sivun muokkaus on valmis, julkaise se.</span><span class="sxs-lookup"><span data-stu-id="8adba-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8adba-141">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="8adba-141">Additional resources</span></span>

[<span data-ttu-id="8adba-142">Aloituspakkauksen yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="8adba-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8adba-143">Konttimoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8adba-144">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8adba-145">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8adba-146">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8adba-147">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8adba-148">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="8adba-148">Footer module</span></span>](author-footer-module.md)
