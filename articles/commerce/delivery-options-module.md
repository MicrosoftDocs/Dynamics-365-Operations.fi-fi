---
title: Toimitusvaihtoehdot -moduuli
description: Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
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
ms.openlocfilehash: 12b0281a27dcf5f567bcd6be5530fa8e26a4ae99
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937479"
---
# <a name="delivery-options-module"></a><span data-ttu-id="42a1b-103">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="42a1b-104">Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="42a1b-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="42a1b-105">Toimitusasetukset-moduulien avulla asiakkaat valitsevat toimitustavan, kuten lähetys tai nouto verkossa tehdylle tilaukselleen.</span><span class="sxs-lookup"><span data-stu-id="42a1b-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="42a1b-106">Toimitusosoite on pakollinen, jotta lähetystapa voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="42a1b-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="42a1b-107">Jos toimitusosoite muuttuu, toimitusvaihtoehdot on noudettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="42a1b-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="42a1b-108">Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="42a1b-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="42a1b-109">Lisätietoja toimitustapojen määrittämisestä on ohjeaiheissa [Online-kanavan määrittäminen](channel-setup-online.md) ja [Toimitustapojen määrittäminen](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="42a1b-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="42a1b-110">Kullakin toimitustilalla voi olla siihen liittyvä maksu.</span><span class="sxs-lookup"><span data-stu-id="42a1b-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="42a1b-111">Lisätietoja verkkokaupan maksujen määrittämisestä on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="42a1b-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="42a1b-112">Commercen version 10.0.13 toimitusvaihtoehdot-moduuli on päivitetty siten, että se tukee **otsikkokulut ilman suhteellisuutta**- ja **lähetystoiminnot rivikuluina** -ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="42a1b-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="42a1b-113">Jos suhteutus on poistettu käytöstä, on odotettavissa, että verkkokaupan työnkulku ei salli sekalaista toimitusta ostoskorin nimikkeille (eli jotkin nimikkeet valitaan lähetettäväksi, mutta toiset valitaan noudettavaksi).</span><span class="sxs-lookup"><span data-stu-id="42a1b-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="42a1b-114">**Otsikkoveloitukset ilman suhteutusta** -ominaisuus edellyttää, että **Ota käyttöön yhdenmukainen toimitustilan käsittelykanava** -lippu on käytössä Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="42a1b-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="42a1b-115">Kun ominaisuuden lippu on käytössä, lähetysmaksut joko otetaan käyttöön joko otsikkotasolla tai rivitasolla riippuen Commerce Headquarters -kokoonpanosta.</span><span class="sxs-lookup"><span data-stu-id="42a1b-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="42a1b-116">Fabrikam-teema tukee moniosaista toimitustapaa, jossa tietyt nimikkeet valitaan lähetystä varten, mutta toiset valitaan noutoa varten.</span><span class="sxs-lookup"><span data-stu-id="42a1b-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="42a1b-117">Tässä tilassa kuljetusmaksut jaetaan kaikille nimikkeille, jotka on valittu toimitustapaa varten.</span><span class="sxs-lookup"><span data-stu-id="42a1b-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="42a1b-118">Jos haluat käyttää moniosaista toimitustapaa, sinun on ensin konfiguroitava **Otsikon kulut suhteutettuna** -ominaisuus Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="42a1b-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="42a1b-119">Lisätietoja tästä konfiguraatiosta on kohdassa [Kohdista otsikkoveloitukset myyntirivien mukaisiksi](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="42a1b-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="42a1b-120">Jos rivinimikkeisiin sovelletaan kuljetusmaksuja, ne voidaan näyttää kunkin nimikkeen ostoskorissa.</span><span class="sxs-lookup"><span data-stu-id="42a1b-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="42a1b-121">Tämä toiminto edellyttää, että **Näytä lähetyskulut rivinimikkeellä** -ominaisuus otetaan käyttöön sekä ostoskori- että kassalle-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="42a1b-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="42a1b-122">Lisätietoja on kohdissa [Ostoskorimoduuli](add-cart-module.md) ja [Kassamoduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="42a1b-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="42a1b-123">Seuraavassa kuvassa on esimerkki toimitusvaihtoehdot-moduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="42a1b-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Esimerkki toimitusvaihtoehdot-moduulista Kassalle-sivulla](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="42a1b-125">Toimitusvaihtoehdot-moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="42a1b-125">Delivery options module properties</span></span>

| <span data-ttu-id="42a1b-126">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="42a1b-126">Property</span></span> | <span data-ttu-id="42a1b-127">Arvot</span><span class="sxs-lookup"><span data-stu-id="42a1b-127">Values</span></span> | <span data-ttu-id="42a1b-128">kuvaus</span><span class="sxs-lookup"><span data-stu-id="42a1b-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="42a1b-129">Otsikko</span><span class="sxs-lookup"><span data-stu-id="42a1b-129">Heading</span></span> | <span data-ttu-id="42a1b-130">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="42a1b-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="42a1b-131">Toimitusasetukset-moduulin valinnainen otsikko.</span><span class="sxs-lookup"><span data-stu-id="42a1b-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="42a1b-132">Mukautetun CSS-luokan nimi</span><span class="sxs-lookup"><span data-stu-id="42a1b-132">Custom CSS class name</span></span> | <span data-ttu-id="42a1b-133">Teksti</span><span class="sxs-lookup"><span data-stu-id="42a1b-133">Text</span></span> | <span data-ttu-id="42a1b-134">Mukautetun CSS-tyylisivut (CSS)-luokan nimi, jota käytetään tarvittaessa tämän moduulin muodostamiseen.</span><span class="sxs-lookup"><span data-stu-id="42a1b-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="42a1b-135">Toimitustavan suodatus -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="42a1b-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="42a1b-136">**Älä Suodata** tai **Ei-lähetys-tilat**</span><span class="sxs-lookup"><span data-stu-id="42a1b-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="42a1b-137">Arvo, joka määrittää, suodatetaanko toimitusasetukset-moduulissa kaikki muut kuin lähetyksen toimitustilat.</span><span class="sxs-lookup"><span data-stu-id="42a1b-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="42a1b-138">Toimitusvaihtoehdon automaattinen valinta</span><span class="sxs-lookup"><span data-stu-id="42a1b-138">Auto select a delivery option</span></span> | <span data-ttu-id="42a1b-139">**Älä suodata**, **Valitse toimitusvaihto automaattisesti ja näytä yhteenveto** tai **Valitse toimitusvaihto automaattisesti ja älä näytä yhteenvetoa**</span><span class="sxs-lookup"><span data-stu-id="42a1b-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="42a1b-140">Tämä ominaisuus käyttää automaattisesti ensimmäistä käytettävissä olevaa toimitusvaihtoehtoa uloskuittaukseen ilman, että käyttäjän pitää valita se.</span><span class="sxs-lookup"><span data-stu-id="42a1b-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="42a1b-141">Sitä tulee käyttää vain, jos toimitusvaihtoehtoja on yksi.</span><span class="sxs-lookup"><span data-stu-id="42a1b-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="42a1b-142">Tätä ominaisuutta tuetaan Commerce-version 10.0.19 julkaisusta alkaen.</span><span class="sxs-lookup"><span data-stu-id="42a1b-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="42a1b-143">Lisää toimitusvaihtoehdot-moduuli kassalle-sivulle ja määritä pakolliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="42a1b-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="42a1b-144">Toimitusvaihtoehdot-moduuli voidaan lisätä vain kassalle-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="42a1b-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="42a1b-145">Lisätietoja toimitusasetukset-moduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="42a1b-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42a1b-146">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="42a1b-146">Additional resources</span></span>

[<span data-ttu-id="42a1b-147">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="42a1b-148">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="42a1b-149">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="42a1b-150">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="42a1b-151">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="42a1b-152">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="42a1b-153">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="42a1b-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="42a1b-154">Online-kanavan määritys</span><span class="sxs-lookup"><span data-stu-id="42a1b-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="42a1b-155">Omnikanavan automaattiset etukäteisveloitukset</span><span class="sxs-lookup"><span data-stu-id="42a1b-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="42a1b-156">Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille</span><span class="sxs-lookup"><span data-stu-id="42a1b-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="42a1b-157">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="42a1b-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
