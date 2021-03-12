---
title: Toimitusosoitemoduuli
description: Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985633"
---
# <a name="shipping-address-module"></a><span data-ttu-id="40a20-103">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="40a20-104">Tässä ohjeaiheessa on tietoja toimitusosoitemoduulista ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.</span><span class="sxs-lookup"><span data-stu-id="40a20-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40a20-105">Yhteenveto</span><span class="sxs-lookup"><span data-stu-id="40a20-105">Overview</span></span>

<span data-ttu-id="40a20-106">Toimitusosoitemoduulin avulla asiakkaat voivat lisätä tai valita tilauksen toimitusosoitteen kassatyönkulun aikana.</span><span class="sxs-lookup"><span data-stu-id="40a20-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="40a20-107">Jos asiakas on kirjautunut sisään, kaikki kyseiselle asiakkaalle aiemmin tallennetut osoitteet näytetään ja asiakas voi valita niistä.</span><span class="sxs-lookup"><span data-stu-id="40a20-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="40a20-108">Asiakas voi myös lisätä uuden osoitteen.</span><span class="sxs-lookup"><span data-stu-id="40a20-108">The customer can also add a new address.</span></span> <span data-ttu-id="40a20-109">Toimitusosoitemoduulia käytetään kaikissa tilauksen nimikkeissä, jotka edellyttävät toimitusta.</span><span class="sxs-lookup"><span data-stu-id="40a20-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="40a20-110">Toimitusosoitteen muodot voidaan määrittää kunkin maan tai alueen Commerce Headquarters -sovelluksessa, ja toimitusosoitemoduuli ottaa käyttöön maa-/aluekohtaiset säännöt.</span><span class="sxs-lookup"><span data-stu-id="40a20-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="40a20-111">Kun asiakkaat syöttävät toimitusosoitteen kassatyönkulun aikana, heillä on mahdollisuus tallentaa osoite ensisijaiseksi osoitteeksi.</span><span class="sxs-lookup"><span data-stu-id="40a20-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="40a20-112">Tämä vaihtoehto näkyy vain, jos asiakas on kirjautunut sisään.</span><span class="sxs-lookup"><span data-stu-id="40a20-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="40a20-113">Vaikka tämä toimitusosoitemoduuli ei sisällä osoitteen vahvistusta, tämä toiminto voidaan toteuttaa mukautuksen avulla.</span><span class="sxs-lookup"><span data-stu-id="40a20-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="40a20-114">Seuraavassa kuvassa on esimerkki uudesta toimitusosoitemoduulista maksusivulla.</span><span class="sxs-lookup"><span data-stu-id="40a20-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Esimerkki toimitusosoitemoduulista Kassalle-sivulla](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="40a20-116">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="40a20-116">Module properties</span></span>

| <span data-ttu-id="40a20-117">Ominaisuuden nimi</span><span class="sxs-lookup"><span data-stu-id="40a20-117">Property name</span></span> | <span data-ttu-id="40a20-118">Arvot</span><span class="sxs-lookup"><span data-stu-id="40a20-118">Values</span></span> | <span data-ttu-id="40a20-119">kuvaus</span><span class="sxs-lookup"><span data-stu-id="40a20-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="40a20-120">Otsikko</span><span class="sxs-lookup"><span data-stu-id="40a20-120">Heading</span></span> | <span data-ttu-id="40a20-121">Otsikkoteksti ja -tunnus (**H1**, **H2**, **H3**, **H4**, **H5** tai **H6**)</span><span class="sxs-lookup"><span data-stu-id="40a20-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="40a20-122">Toimitusosoitemoduulin valinnainen otsikko.</span><span class="sxs-lookup"><span data-stu-id="40a20-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="40a20-123">Näytä osoitetyyppi</span><span class="sxs-lookup"><span data-stu-id="40a20-123">Show address type</span></span> | <span data-ttu-id="40a20-124">**Tosi** vai **Epätosi**</span><span class="sxs-lookup"><span data-stu-id="40a20-124">**True** or **False**</span></span> | <span data-ttu-id="40a20-125">Jos tämän valinnaisen ominaisuuden arvo on **Tosi**, näkyviin tulee osoitetyyppi, esimerkiksi **koti** tai **yritys**.</span><span class="sxs-lookup"><span data-stu-id="40a20-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="40a20-126">Jos osoitetyyppiä ei ole määritetty, osoite tallennetaan automaattisesti **tyypiksi**=**Muu**.</span><span class="sxs-lookup"><span data-stu-id="40a20-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="40a20-127">Lisää toimitusosoitemoduuli kassalle-sivulle ja määritä pakolliset ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="40a20-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="40a20-128">Toimitusosoitemoduuli voidaan lisätä vain kassalle-moduuliin.</span><span class="sxs-lookup"><span data-stu-id="40a20-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="40a20-129">Lisätietoja toimitusosoitemoduulin konfiguroinnista ja lisäämisestä kassalle-sivulle on kohdassa [kassalle-moduuli](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="40a20-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40a20-130">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="40a20-130">Additional resources</span></span>

[<span data-ttu-id="40a20-131">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="40a20-132">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="40a20-133">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="40a20-134">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="40a20-135">Toimitusvaihtoehtomoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="40a20-136">Noudon tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="40a20-137">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="40a20-138">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="40a20-138">Gift card module</span></span>](add-giftcard.md)
