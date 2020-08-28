---
title: Toimitusvaihtoehdot -moduuli
description: Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661200"
---
# <a name="delivery-options-module"></a><span data-ttu-id="07e6f-103">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="07e6f-104">Tässä ohjeaiheessa on tietoja toimitusvaihtoehtomoduuleista ja niiden määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="07e6f-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="07e6f-105">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="07e6f-105">Overview</span></span>

<span data-ttu-id="07e6f-106">Toimitusasetukset-moduulien avulla asiakkaat valitsevat toimitustavan, kuten lähetys tai nouto verkossa tehdylle tilaukselleen.</span><span class="sxs-lookup"><span data-stu-id="07e6f-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="07e6f-107">Toimitusosoite on pakollinen, jotta lähetystapa voidaan määrittää.</span><span class="sxs-lookup"><span data-stu-id="07e6f-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="07e6f-108">Jos toimitusosoite muuttuu, toimitusvaihtoehdot on noudettava uudelleen.</span><span class="sxs-lookup"><span data-stu-id="07e6f-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="07e6f-109">Jos tilauksessa on vain myymälästä noudettavia nimikkeitä, tämä moduuli piilotetaan automaattisesti.</span><span class="sxs-lookup"><span data-stu-id="07e6f-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="07e6f-110">Lisätietoja toimitustapojen määrittämisestä on ohjeaiheissa [Online-kanavan määrittäminen](channel-setup-online.md) ja [Toimitustapojen määrittäminen](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="07e6f-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="07e6f-111">Kullakin toimitustilalla voi olla siihen liittyvä maksu.</span><span class="sxs-lookup"><span data-stu-id="07e6f-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="07e6f-112">Lisätietoja verkkokaupan maksujen määrittämisestä on kohdassa [Monikanavaiset edistyneet automaattiset veloitukset](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="07e6f-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="07e6f-113">Commercen version 10.0.13 toimitusvaihtoehdot-moduuli on päivitetty siten, että se tukee **otsikkokulut ilman suhteellisuutta**- ja **lähetystoiminnot rivikuluina** -ominaisuuksia.</span><span class="sxs-lookup"><span data-stu-id="07e6f-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="07e6f-114">Jos suhteutus on poistettu käytöstä, on odotettavissa, että verkkokaupan työnkulku ei salli sekalaista toimitusta ostoskorin nimikkeille (eli jotkin nimikkeet valitaan lähetettäväksi, mutta toiset valitaan noudettavaksi).</span><span class="sxs-lookup"><span data-stu-id="07e6f-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="07e6f-115">**Otsikkoveloitukset ilman suhteutusta** -ominaisuus edellyttää, että **Ota käyttöön yhdenmukainen toimitustilan käsittelykanava** -lippu on käytössä Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="07e6f-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="07e6f-116">Kun lippu on käytössä, lähetysmaksut joko otetaan käyttöön joko otsikkotasolla tai rivitasolla riippuen Commerce Headquarters -kokoonpanosta.</span><span class="sxs-lookup"><span data-stu-id="07e6f-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="07e6f-117">Fabrikam-teema tukee moniosaista toimitustapaa, jossa tietyt nimikkeet valitaan lähetystä varten, mutta toiset valitaan noutoa varten.</span><span class="sxs-lookup"><span data-stu-id="07e6f-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="07e6f-118">Tässä tilassa kuljetusmaksut jaetaan kaikille nimikkeille, jotka on valittu toimitustapaa varten.</span><span class="sxs-lookup"><span data-stu-id="07e6f-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="07e6f-119">Jos haluat käyttää moniosaista toimitustapaa, sinun on ensin konfiguroitava **Otsikon kulut suhteutettuna** -ominaisuus Commerce Headquarters -sovelluksessa.</span><span class="sxs-lookup"><span data-stu-id="07e6f-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="07e6f-120">Lisätietoja tästä konfiguraatiosta on kohdassa [Kohdista otsikkoveloitukset myyntirivien mukaisiksi](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="07e6f-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="07e6f-121">Jos rivinimikkeisiin sovelletaan kuljetusmaksuja, ne voidaan näyttää kunkin nimikkeen ostoskorissa.</span><span class="sxs-lookup"><span data-stu-id="07e6f-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="07e6f-122">Tämä toiminto edellyttää, että **Näytä lähetyskulut rivinimikkeellä** -ominaisuus otetaan käyttöön sekä ostoskori- että kassalle-moduulissa.</span><span class="sxs-lookup"><span data-stu-id="07e6f-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="07e6f-123">Lisätietoja on kohdissa [Ostoskorimoduuli](add-cart-module.md) ja [Kassamoduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="07e6f-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="07e6f-124">Seuraavassa kuvassa on esimerkki toimitusvaihtoehdot-moduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="07e6f-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Esimerkki toimitusvaihtoehdot-moduulista Kassalle-sivulla](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="07e6f-126">Toimitusvaihtoehdot-moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="07e6f-126">Delivery options module properties</span></span>

| <span data-ttu-id="07e6f-127">Ominaisuus</span><span class="sxs-lookup"><span data-stu-id="07e6f-127">Property</span></span> | <span data-ttu-id="07e6f-128">Arvot</span><span class="sxs-lookup"><span data-stu-id="07e6f-128">Values</span></span> | <span data-ttu-id="07e6f-129">kuvaus</span><span class="sxs-lookup"><span data-stu-id="07e6f-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="07e6f-130">Otsikko</span><span class="sxs-lookup"><span data-stu-id="07e6f-130">Heading</span></span> | <span data-ttu-id="07e6f-131">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="07e6f-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="07e6f-132">Toimitusasetukset-moduulin valinnainen otsikko.</span><span class="sxs-lookup"><span data-stu-id="07e6f-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="07e6f-133">Mukautetun CSS-luokan nimi</span><span class="sxs-lookup"><span data-stu-id="07e6f-133">Custom CSS class name</span></span> | <span data-ttu-id="07e6f-134">Teksti</span><span class="sxs-lookup"><span data-stu-id="07e6f-134">Text</span></span> | <span data-ttu-id="07e6f-135">Mukautetun CSS-tyylisivut (CSS)-luokan nimi, jota käytetään tarvittaessa tämän moduulin muodostamiseen.</span><span class="sxs-lookup"><span data-stu-id="07e6f-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="07e6f-136">Toimitustavan suodatus -vaihtoehto</span><span class="sxs-lookup"><span data-stu-id="07e6f-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="07e6f-137">**Älä Suodata** tai **Ei-lähetys-tilat**</span><span class="sxs-lookup"><span data-stu-id="07e6f-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="07e6f-138">Arvo, joka määrittää, suodatetaanko toimitusasetukset-moduulissa kaikki muut kuin lähetyksen toimitustilat.</span><span class="sxs-lookup"><span data-stu-id="07e6f-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="07e6f-139">Lisää toimitusvaihtoehdot-moduuli kassalle-sivulle ja määritä pakolliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="07e6f-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="07e6f-140">Toimitusvaihtoehdot-moduuli voidaan lisätä vain kassalle-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="07e6f-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="07e6f-141">Lisätietoja toimitusasetukset-moduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="07e6f-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07e6f-142">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="07e6f-142">Additional resources</span></span>

[<span data-ttu-id="07e6f-143">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="07e6f-144">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="07e6f-145">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="07e6f-146">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="07e6f-147">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="07e6f-148">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="07e6f-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="07e6f-149">Online-kanavan määritys</span><span class="sxs-lookup"><span data-stu-id="07e6f-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="07e6f-150">Omnikanavan automaattiset etukäteisveloitukset</span><span class="sxs-lookup"><span data-stu-id="07e6f-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="07e6f-151">Otsikon kulujen suhteellinen jakaminen vastaaville myyntiriveille</span><span class="sxs-lookup"><span data-stu-id="07e6f-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="07e6f-152">Määritä toimitustavat</span><span class="sxs-lookup"><span data-stu-id="07e6f-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
