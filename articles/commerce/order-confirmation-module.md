---
title: Tilauksen tiedot -moduuli
description: Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.
author: anupamar
manager: annbe
ms.date: 06/18/2020
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
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015177"
---
# <a name="order-details-module"></a><span data-ttu-id="7d5b5-103">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d5b5-104">Tässä ohjeaiheessa on tietoja tilauksen tietomoduuleista ja niiden käytöstä Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d5b5-105">Yleiskatsaus</span><span class="sxs-lookup"><span data-stu-id="7d5b5-105">Overview</span></span>

<span data-ttu-id="7d5b5-106">Tilaustiedot-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="7d5b5-107">Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot ja toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="7d5b5-108">Tilauksen tietomoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="7d5b5-108">Order details module properties</span></span>

| <span data-ttu-id="7d5b5-109">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="7d5b5-109">Property name</span></span>  | <span data-ttu-id="7d5b5-110">Arvot</span><span class="sxs-lookup"><span data-stu-id="7d5b5-110">Values</span></span> | <span data-ttu-id="7d5b5-111">kuvaus</span><span class="sxs-lookup"><span data-stu-id="7d5b5-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="7d5b5-112">Otsikko</span><span class="sxs-lookup"><span data-stu-id="7d5b5-112">Heading</span></span>        | <span data-ttu-id="7d5b5-113">Otsikkoteksti ja -tunnus ( **H1** , **H2** , **H3** , **H4** , **H5** tai **H6** )</span><span class="sxs-lookup"><span data-stu-id="7d5b5-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="7d5b5-114">Tilauksen tietomoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-114">The order details module can have a heading.</span></span> <span data-ttu-id="7d5b5-115">Oletusarvoisesti otsikossa käytetään **H2** -otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="7d5b5-116">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="7d5b5-117">Yhteyshenkilön puhelinnumero</span><span class="sxs-lookup"><span data-stu-id="7d5b5-117">Contact number</span></span> | <span data-ttu-id="7d5b5-118">Text</span><span class="sxs-lookup"><span data-stu-id="7d5b5-118">Text</span></span> | <span data-ttu-id="7d5b5-119">Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="7d5b5-120">Moduulit, joita voidaan käyttää tilaustietosivulla</span><span class="sxs-lookup"><span data-stu-id="7d5b5-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="7d5b5-121">Kun luot tilaustiedot-sivun, voit lisätä muita asiaankuuluvia moduuleja tilaustiedot-moduulin lisäksi.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="7d5b5-122">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="7d5b5-122">Here are some examples:</span></span>

- <span data-ttu-id="7d5b5-123">**Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilaustietosivulle ehdottamaan asiakkaalle muita tuotteita.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="7d5b5-124">**Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilaustiedot-sivulle.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="7d5b5-125">Tilaustietomoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="7d5b5-125">Add an order details module to a page</span></span>

<span data-ttu-id="7d5b5-126">Voit lisätä tilaustietomoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d5b5-127">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7d5b5-128">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi** -kohtaan nimi **Tilauksen tietomalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-129">Valitse kolme pistettä ( **...** ) **Tekstiosa** -paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d5b5-130">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-131">Valitse **Oletussivu** -moduulin **Pää** -paikka. Valitse kolmen pisteen painike ( **...** ) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d5b5-132">Valitse **Lisää moduuli** -valintaikkunassa **Tilauksen tiedot** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-133">Valitse **Tallenna** ja esikatsele sitten mallia valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="7d5b5-134">Tilauksen tietomoduulia ei tule hahmontaa, koska se vaatii tilauksen vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="7d5b5-135">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d5b5-136">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7d5b5-137">Valitse **Valitse malli** -valintaikkunassa **Tilauksen tietomalli**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="7d5b5-138">Kirjoita **Sivun nimi** -kohtaan **Tilauksen tietosivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-139">Valitse **Oletussivu** -moduulin **Pää** -paikka. Valitse kolmen pisteen painike ( **...** ) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d5b5-140">Valitse **Lisää moduuli** -valintaikkunassa **Tilauksen tiedot** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-141">Valitse tilauksen tietomoduulin ominaisuusruudun kynäsymbolin vieressä **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="7d5b5-142">Anna **Otsikko** -valintaikkunan **Otsikon teksti** -kentästä otsikon tekstiksi **Tilauksen tiedot** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="7d5b5-143">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7d5b5-144">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="7d5b5-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d5b5-145">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="7d5b5-145">Additional resources</span></span>

[<span data-ttu-id="7d5b5-146">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7d5b5-147">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7d5b5-148">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7d5b5-149">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7d5b5-150">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7d5b5-151">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="7d5b5-152">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="7d5b5-152">Gift card module</span></span>](add-giftcard.md)
