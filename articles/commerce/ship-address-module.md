---
title: Toimitusosoitemoduuli
description: Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fd48a04612159cbe29a2cc7cafea1c9c4c8745b4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795426"
---
# <a name="shipping-address-module"></a><span data-ttu-id="3f143-103">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f143-104">Tässä aiheessa kuvataan tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="3f143-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3f143-105">Toimitusosoitemoduulin avulla asiakkaat voivat lisätä tai valita tilauksen toimitusosoitteen kassatyönkulun aikana.</span><span class="sxs-lookup"><span data-stu-id="3f143-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="3f143-106">Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään ja asiakas voi valita niistä.</span><span class="sxs-lookup"><span data-stu-id="3f143-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="3f143-107">Asiakas voi myös lisätä uuden osoitteen.</span><span class="sxs-lookup"><span data-stu-id="3f143-107">The customer can also add a new address.</span></span> <span data-ttu-id="3f143-108">Toimitusosoitemoduulia käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta.</span><span class="sxs-lookup"><span data-stu-id="3f143-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="3f143-109">Toimitusosoitteen muodot voidaan määrittää kunkin maan tai alueen Commerce Headquarters -sovelluksessa, ja toimitusosoitemoduuli ottaa käyttöön maa-/aluekohtaiset säännöt.</span><span class="sxs-lookup"><span data-stu-id="3f143-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="3f143-110">Kun asiakkaat syöttävät toimitusosoitteen kassatyönkulun aikana, heillä on mahdollisuus tallentaa osoite ensisijaiseksi osoitteeksi.</span><span class="sxs-lookup"><span data-stu-id="3f143-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="3f143-111">Tämä vaihtoehto näkyy vain, jos asiakas on kirjautunut sisään.</span><span class="sxs-lookup"><span data-stu-id="3f143-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="3f143-112">Vaikka tämä toimitusosoitemoduuli ei sisällä osoitteen vahvistusta, tämä toiminto voidaan toteuttaa mukautuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="3f143-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="3f143-113">Seuraavassa kuvassa on esimerkki uudesta toimitusosoitemoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="3f143-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Esimerkki toimitusosoitemoduulista Kassalle-sivulla](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="3f143-115">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="3f143-115">Module properties</span></span>

| <span data-ttu-id="3f143-116">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="3f143-116">Property name</span></span> | <span data-ttu-id="3f143-117">Arvot</span><span class="sxs-lookup"><span data-stu-id="3f143-117">Values</span></span> | <span data-ttu-id="3f143-118">kuvaus</span><span class="sxs-lookup"><span data-stu-id="3f143-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3f143-119">Otsikko</span><span class="sxs-lookup"><span data-stu-id="3f143-119">Heading</span></span> | <span data-ttu-id="3f143-120">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="3f143-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3f143-121">Toimitusosoitemoduulin valinnainen otsikko.</span><span class="sxs-lookup"><span data-stu-id="3f143-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="3f143-122">Näytä osoitetyyppi</span><span class="sxs-lookup"><span data-stu-id="3f143-122">Show address type</span></span> | <span data-ttu-id="3f143-123">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="3f143-123">**True** or **False**</span></span> | <span data-ttu-id="3f143-124">Jos tämän valinnaisen ominaisuuden arvo on **Tosi**, näkyviin tulee osoitetyyppi, esimerkiksi **koti** tai **yritys**.</span><span class="sxs-lookup"><span data-stu-id="3f143-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="3f143-125">Jos osoitetyyppiä ei ole määritetty, osoite tallennetaan automaattisesti **tyypiksi**=**Muu**.</span><span class="sxs-lookup"><span data-stu-id="3f143-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="3f143-126">Ota automaattinen ehdotus käyttöön</span><span class="sxs-lookup"><span data-stu-id="3f143-126">Enable auto suggestion</span></span>| <span data-ttu-id="3f143-127">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="3f143-127">**True** or **False**</span></span> | <span data-ttu-id="3f143-128">Jos tämän valinnaisen ominaisuuden arvoksi määritetään **Tosi**, automaattisia osoite-ehdotuksia annetaan.</span><span class="sxs-lookup"><span data-stu-id="3f143-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="3f143-129">Ehdotukset saadaan Bing Maps -palvelusta.</span><span class="sxs-lookup"><span data-stu-id="3f143-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="3f143-130">Lisätietoja Bing Maps -integroinnin määrityksestä sivustossasi on [myymälän valitsinmoduulissa](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="3f143-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="3f143-131">Tämä ominaisuus on käytettävissä Commerce-version 10.0.15 julkaisussa.</span><span class="sxs-lookup"><span data-stu-id="3f143-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="3f143-132">Automaattisen ehdotuksen vaihtoehdot</span><span class="sxs-lookup"><span data-stu-id="3f143-132">Auto suggest options</span></span>| <span data-ttu-id="3f143-133">Numero</span><span class="sxs-lookup"><span data-stu-id="3f143-133">A number</span></span>| <span data-ttu-id="3f143-134">Jos automaattiset osoite-ehdotukset ovat käytössä, voit määrittää lisäasetuksia, kuten annettavien ehdotusten enimmäismäärän.</span><span class="sxs-lookup"><span data-stu-id="3f143-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="3f143-135">Lisää toimitusosoitemoduuli kassalle-sivulle ja määritä pakolliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="3f143-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="3f143-136">Toimitusosoitemoduuli voidaan lisätä vain kassalle-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="3f143-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="3f143-137">Lisätietoja toimitusosoitemoduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="3f143-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f143-138">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="3f143-138">Additional resources</span></span>

[<span data-ttu-id="3f143-139">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3f143-140">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3f143-141">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3f143-142">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3f143-143">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3f143-144">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="3f143-145">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3f143-146">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3f143-147">Myymälän valitsinmoduuli</span><span class="sxs-lookup"><span data-stu-id="3f143-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]