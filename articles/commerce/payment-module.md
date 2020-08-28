---
title: Maksumoduuli
description: Tässä ohjeaiheessa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661201"
---
# <a name="payment-module"></a><span data-ttu-id="67160-103">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="67160-104">Tässä ohjeaiheessa on tietoja maksumoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="67160-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="67160-105">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="67160-105">Overview</span></span>

<span data-ttu-id="67160-106">Maksumoduulin avulla asiakkaat voivat maksaa tilaukset käyttämällä luotto- tai maksukortteja.</span><span class="sxs-lookup"><span data-stu-id="67160-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="67160-107">Maksun integroinnin tässä moduulissa tarjoaa Dynamics 365 -maksuyhdistin Adyenille.</span><span class="sxs-lookup"><span data-stu-id="67160-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="67160-108">Lisätietoja maksuyhdistimen asentamisesta ja määrittämisestä on kohdassa [Dynamics 365 -maksuyhdistin Adyenille](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="67160-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="67160-109">Maksumoduuli isännöi Adyen-nimisen HTML-kehyksen (iframe) kautta tarjottuun maksuun liittyviä tietoja.</span><span class="sxs-lookup"><span data-stu-id="67160-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="67160-110">Maksumoduuli toimii yhdessä Commerce Scale Unitin kanssa noutaakseen Adyen-maksuja koskevat tiedot.</span><span class="sxs-lookup"><span data-stu-id="67160-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="67160-111">Osana Commerce Scale Unitin vuorovaikutusta maksumoduuli voi sallia, että laskutusosoite tiedot voidaan antaa joko iframe-muodossa tai erillisenä moduulina.</span><span class="sxs-lookup"><span data-stu-id="67160-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="67160-112">Fabrikam-teeman laskutusosoite näkyy erillisessä moduulissa.</span><span class="sxs-lookup"><span data-stu-id="67160-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="67160-113">Tämä lähestymistapa mahdollistaa muotoilun joustavuuden, koska osoiterivit voidaan muodostaa niin, että ne muistuttavat toimitusosoitteen rivejä.</span><span class="sxs-lookup"><span data-stu-id="67160-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="67160-114">Myös sisäänkirjautuneena olevat asiakkaat tallentavat maksatustietonsa.</span><span class="sxs-lookup"><span data-stu-id="67160-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="67160-115">Maksutiedot ja laskutusosoite tallennetaan ja niitä hallitaan Adyen-maksuyhdistimen kautta.</span><span class="sxs-lookup"><span data-stu-id="67160-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="67160-116">Maksumoduuli kattaa kaikki tilauskulut, jotka eivät kuulu kanta-asiakkuuspisteiden tai lahjakortin piiriin.</span><span class="sxs-lookup"><span data-stu-id="67160-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="67160-117">Jos tilauksen kokonaissumma on täysin kanta-asiakkuus pisteiden tai lahjakorttien hyvitysten peittämä, maksatusmoduuli piilotetaan ja asiakas voi tehdä tilauksen ilman sitä.</span><span class="sxs-lookup"><span data-stu-id="67160-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="67160-118">Adyen-yhdistin tukee myös asiakkaan vahvaa todennusta (SCA).</span><span class="sxs-lookup"><span data-stu-id="67160-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="67160-119">Osa Euroopan unionin (EU) maksupalveludirektiivistä 2.0 (PSD2.0) edellyttää, että online-ostajat todennetaan verkko-ostoskokemuksensa ulkopuolella, kun he käyttävät sähköistä maksutapaa.</span><span class="sxs-lookup"><span data-stu-id="67160-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="67160-120">Kassatyönkulun aikana asiakkaat ohjataan pankkisivustolle.</span><span class="sxs-lookup"><span data-stu-id="67160-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="67160-121">Sitten todennuksen jälkeen ne ohjataan takaisin Commerce Checkout -työnkulkuun.</span><span class="sxs-lookup"><span data-stu-id="67160-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="67160-122">Tämän uudelleenohjauksen aikana asiakkaan kassatyönkulkuun syötetyt tiedot (esimerkiksi toimitusosoite, toimitusvaihtoehdot, lahjakorttitiedot ja kanta-asiakastiedot) säilyvät ennallaan.</span><span class="sxs-lookup"><span data-stu-id="67160-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="67160-123">Ennen kuin voit ottaa tämän toiminnon käyttöön, maksuyhteys on konfiguroitava SCA:lle Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="67160-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="67160-124">Lisätietoja on kohdassa [vahva asiakastodennus käyttäen Adyen-sovellusta](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="67160-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="67160-125">Seuraavassa kuvassa on esimerkki lahjakortista, kanta-asiakkuudesta ja maksumoduuleista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="67160-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Esimerkki lahjakortista, kanta-asiakkuudesta ja maksumoduuleista maksusivulla](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="67160-127">Maksumoduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="67160-127">Payment module properties</span></span>

| <span data-ttu-id="67160-128">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="67160-128">Property name</span></span> | <span data-ttu-id="67160-129">Arvot</span><span class="sxs-lookup"><span data-stu-id="67160-129">Values</span></span> | <span data-ttu-id="67160-130">kuvaus</span><span class="sxs-lookup"><span data-stu-id="67160-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="67160-131">Otsikko</span><span class="sxs-lookup"><span data-stu-id="67160-131">Heading</span></span> | <span data-ttu-id="67160-132">Otsikon teksti</span><span class="sxs-lookup"><span data-stu-id="67160-132">Heading text</span></span> | <span data-ttu-id="67160-133">Maksumoduulin valinnainen otsikko.</span><span class="sxs-lookup"><span data-stu-id="67160-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="67160-134">Iframen korkeus</span><span class="sxs-lookup"><span data-stu-id="67160-134">Height of the iframe</span></span> | <span data-ttu-id="67160-135">Pikseliä</span><span class="sxs-lookup"><span data-stu-id="67160-135">Pixels</span></span> | <span data-ttu-id="67160-136">Iframe-kentän korkeus kuvapisteinä.</span><span class="sxs-lookup"><span data-stu-id="67160-136">The iframe height, in pixels.</span></span> <span data-ttu-id="67160-137">Korkeutta voi muuttaa tarvittaessa.</span><span class="sxs-lookup"><span data-stu-id="67160-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="67160-138">Näytä laskutusosoite</span><span class="sxs-lookup"><span data-stu-id="67160-138">Show billing address</span></span> | <span data-ttu-id="67160-139">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="67160-139">**True** or **False**</span></span> | <span data-ttu-id="67160-140">Jos tämän ominaisuuden arvo on **Tosi**, laskutusosoite näytetään Adyen-maksumoduulin iframe-ohjelman sisällä.</span><span class="sxs-lookup"><span data-stu-id="67160-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="67160-141">Jos arvo on **Epätosi**, laskutusosoitetta ei näytetä Adyenissa, ja Commerce-käyttäjän on konfiguroitava moduuli näyttämään laskutusosoite kassasivulla.</span><span class="sxs-lookup"><span data-stu-id="67160-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="67160-142">Maksun tyylin ohitus</span><span class="sxs-lookup"><span data-stu-id="67160-142">Payment style override</span></span> | <span data-ttu-id="67160-143">CSS-tyylisivut (CSS) -koodi</span><span class="sxs-lookup"><span data-stu-id="67160-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="67160-144">Koska maksumoduulia isännöidään iframe-ohjelmassa, muotoiluominaisuus on rajallinen.</span><span class="sxs-lookup"><span data-stu-id="67160-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="67160-145">Voit saavuttaa joitakin muotoiluja käyttämällä tätä ominaisuutta.</span><span class="sxs-lookup"><span data-stu-id="67160-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="67160-146">Sivuston tyylien ohittaminen edellyttää, että liität CSS-koodin tämän ominaisuuden arvoksi.</span><span class="sxs-lookup"><span data-stu-id="67160-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="67160-147">Sivuston muodostimen CSS-ohitukset ja tyylit eivät koske tätä moduulia.</span><span class="sxs-lookup"><span data-stu-id="67160-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="67160-148">Laskutusosoite</span><span class="sxs-lookup"><span data-stu-id="67160-148">Billing address</span></span>

<span data-ttu-id="67160-149">Maksumoduulin avulla asiakkaat voivat antaa laskutusosoitteen maksutiedoille.</span><span class="sxs-lookup"><span data-stu-id="67160-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="67160-150">Sen avulla he voivat myös käyttää toimitusosoitetta laskutusosoitteena, jotta kassatyönkulku sujuisi helpommin ja nopeammin.</span><span class="sxs-lookup"><span data-stu-id="67160-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="67160-151">Jos **Näytä laskutusosoite** -ominaisuuden arvo on **Epätosi**, maksumoduuli tulee määrittää kassalle-sivulla.</span><span class="sxs-lookup"><span data-stu-id="67160-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="67160-152">Lisää maksumoduuli kassasivulle ja määritä pakolliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="67160-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="67160-153">Maksumoduuli voidaan lisätä vain kassalle-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="67160-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="67160-154">Lisätietoja maksumoduulin määrittämisestä kassasivulle on kohdassa [Kassamoduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="67160-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67160-155">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="67160-155">Additional resources</span></span>

[<span data-ttu-id="67160-156">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="67160-157">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="67160-158">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="67160-159">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="67160-160">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="67160-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="67160-161">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="67160-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="67160-162">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="67160-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="67160-163">Dynamics 365 -maksuyhdistin Adyenia varten</span><span class="sxs-lookup"><span data-stu-id="67160-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="67160-164">Asiakkaan vahva todennus Adyen-yhdistimellä</span><span class="sxs-lookup"><span data-stu-id="67160-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
