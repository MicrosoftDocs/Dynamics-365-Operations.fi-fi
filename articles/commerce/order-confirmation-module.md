---
title: Tilauksen vahvistusmoduuli
description: Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden käytämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/07/2020
ms.locfileid: "4412134"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="0462c-103">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0462c-104">Tässä ohjeaiheessa on tietoja tilauksen vahvistusmoduuleista ja niiden käytämisestä Microsoft Dynamics 365 Commerce -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="0462c-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0462c-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="0462c-105">Overview</span></span>

<span data-ttu-id="0462c-106">Tilausvahvistus-moduulia käytetään näyttämään tilausvahvistuksen yksityiskohdat tilauksen tekemisen jälkeen.</span><span class="sxs-lookup"><span data-stu-id="0462c-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="0462c-107">Se näyttää tilausvahvistuksen tunnuksen, tilauksen yhteystiedot ja muut tilaustiedot, kuten ostetut nimikkeet, maksutiedot, noutovaihtoehdot ja toimitustavan.</span><span class="sxs-lookup"><span data-stu-id="0462c-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="0462c-108">Tilauksen vahvistusmoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="0462c-108">Order confirmation module properties</span></span>

| <span data-ttu-id="0462c-109">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="0462c-109">Property name</span></span>  | <span data-ttu-id="0462c-110">Arvot</span><span class="sxs-lookup"><span data-stu-id="0462c-110">Values</span></span> | <span data-ttu-id="0462c-111">Kuvaus</span><span class="sxs-lookup"><span data-stu-id="0462c-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="0462c-112">Otsikko</span><span class="sxs-lookup"><span data-stu-id="0462c-112">Heading</span></span>        | <span data-ttu-id="0462c-113">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="0462c-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="0462c-114">Tilauksen vahvistusmoduulilla voi olla otsikko.</span><span class="sxs-lookup"><span data-stu-id="0462c-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="0462c-115">Oletusarvoisesti otsikossa käytetään **H2**-otsikkotunnusta.</span><span class="sxs-lookup"><span data-stu-id="0462c-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="0462c-116">Tunnuksen voi kuitenkin muuttaa, jotta helppokäyttötoimintojen vaatimukset täyttyvät.</span><span class="sxs-lookup"><span data-stu-id="0462c-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="0462c-117">Yhteyshenkilön puhelinnumero</span><span class="sxs-lookup"><span data-stu-id="0462c-117">Contact number</span></span> | <span data-ttu-id="0462c-118">Text</span><span class="sxs-lookup"><span data-stu-id="0462c-118">Text</span></span> | <span data-ttu-id="0462c-119">Tilaukseen liittyviin kysymyksiin voidaan antaa yhteyshenkilön numero.</span><span class="sxs-lookup"><span data-stu-id="0462c-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="0462c-120">Näytä noudon aikavälin tiedot</span><span class="sxs-lookup"><span data-stu-id="0462c-120">Show pickup timeslot information</span></span> | <span data-ttu-id="0462c-121">Tosi tai epätosi.</span><span class="sxs-lookup"><span data-stu-id="0462c-121">True or False</span></span> | <span data-ttu-id="0462c-122">Tämä ominaisuus on käytettävissä Dynamics 365 Commerce -versiossa 10.0.15 ja uudemmissa versioissa.</span><span class="sxs-lookup"><span data-stu-id="0462c-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="0462c-123">Jos arvo on Tosi, noudon aikavälin tiedot näytetään, jos ne on annettu noudettavalle nimikkeelle</span><span class="sxs-lookup"><span data-stu-id="0462c-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="0462c-124">Moduulit, joita voidaan käyttää tilausvahvistussivulla</span><span class="sxs-lookup"><span data-stu-id="0462c-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="0462c-125">Kun luot tilausvahvistus-sivun, voit lisätä muita asiaankuuluvia moduuleja tilausvahvistus-moduulin lisäksi.</span><span class="sxs-lookup"><span data-stu-id="0462c-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="0462c-126">Seuraavassa on muutamia esimerkkejä:</span><span class="sxs-lookup"><span data-stu-id="0462c-126">Here are some examples:</span></span>

- <span data-ttu-id="0462c-127">**Suositukset-moduuli** – Suositusten moduuli voidaan lisätä tilausvahvistussivulle ehdottamaan asiakkaalle muita tuotteita.</span><span class="sxs-lookup"><span data-stu-id="0462c-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="0462c-128">**Markkinointi moduulit** – Mikä tahansa markkinointimoduuli, josta näkyy markkinointisisältö, voidaan lisätä tilausvahvistus-sivulle.</span><span class="sxs-lookup"><span data-stu-id="0462c-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="0462c-129">Tilausvahvistusmoduulin lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="0462c-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="0462c-130">Voit lisätä tilausvahvistusmoduulin uudelle sivulle ja määrittää pakolliset ominaisuudet seuraavasti.</span><span class="sxs-lookup"><span data-stu-id="0462c-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="0462c-131">Siirry kohtaan **Mallit** ja valitse **Uusi** luodaksesi uuden sivumallin.</span><span class="sxs-lookup"><span data-stu-id="0462c-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="0462c-132">Kirjoita **Uusi malli** -valintaikkunan **Mallin nimi**-kohtaan nimi **Tilauksen vahvistusmalli** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-133">Valitse kolme pistettä (**...**) **Tekstiosa**-paikassa ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0462c-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0462c-134">Valitse **Lisää moduuli** -valintaikkunassa **Oletussivu**-moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-135">Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0462c-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0462c-136">Valitse **Lisää moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-137">Valitse **Tallenna** ja esikatsele sitten mallia valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="0462c-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="0462c-138">Tilauksen vahvistusmoduulia ei hahmonneta, koska se vaatii tilauksen vahvistusnumeron.</span><span class="sxs-lookup"><span data-stu-id="0462c-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="0462c-139">Valitse **Lopeta muokkaus** tallentaaksesi mallin ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="0462c-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="0462c-140">Siirry kohtaan **Sivut** ja valitse **Uusi** luodaksesi uuden sivun.</span><span class="sxs-lookup"><span data-stu-id="0462c-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0462c-141">Valitse **Valitse malli** -valintaikkunassa **Tilausvahvistus-malli**.</span><span class="sxs-lookup"><span data-stu-id="0462c-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="0462c-142">Kirjoita **Sivun nimi** -kohtaan **Tilausvahvistus-sivu** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-143">Valitse **Oletussivu**-moduulin **Pää**-paikka. Valitse kolmen pisteen painike (**...**) ja valitse sitten **Lisää moduuli**.</span><span class="sxs-lookup"><span data-stu-id="0462c-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0462c-144">Valitse **Lisää moduuli** -valintaikkunassa **Tilausvahvistus** -moduuli ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-145">Valitse tilauksen vahvistusmoduulin ominaisuusruudun kynäsymbolin vieressä **Otsikko**.</span><span class="sxs-lookup"><span data-stu-id="0462c-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="0462c-146">Anna **Otsikko**-valintaikkunan **Otsikon teksti** -kentästä otsikon tekstiksi **Tilausvahvistus** ja valitse sitten **OK**.</span><span class="sxs-lookup"><span data-stu-id="0462c-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="0462c-147">Valitse **Tallenna** ja esikatsele sitten sivua valitsemalla **Esikatselu**.</span><span class="sxs-lookup"><span data-stu-id="0462c-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="0462c-148">Valitse **Lopeta muokkaus** tallentaaksesi sivun ja valitse sitten **Julkaise** julkaistaksesi sen.</span><span class="sxs-lookup"><span data-stu-id="0462c-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0462c-149">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="0462c-149">Additional resources</span></span>

[<span data-ttu-id="0462c-150">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0462c-151">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="0462c-152">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0462c-153">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="0462c-154">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="0462c-155">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="0462c-156">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="0462c-157">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="0462c-157">Gift card module</span></span>](add-giftcard.md)
