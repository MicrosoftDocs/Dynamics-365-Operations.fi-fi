---
title: Ostoskorikuvakemoduuli
description: Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab1609d332b96c0588b06aa086dd4fee944e5d9
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055757"
---
# <a name="cart-icon-module"></a><span data-ttu-id="b2553-103">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2553-104">Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="b2553-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b2553-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="b2553-105">Overview</span></span>

<span data-ttu-id="b2553-106">Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on.</span><span class="sxs-lookup"><span data-stu-id="b2553-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="b2553-107">Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="b2553-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="b2553-108">Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle.</span><span class="sxs-lookup"><span data-stu-id="b2553-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="b2553-109">Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="b2553-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="b2553-110">Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta.</span><span class="sxs-lookup"><span data-stu-id="b2553-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="b2553-111">Kortin kuvakemoduulin tuki on saatavana Dynamics 365 Commercen versiossa 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="b2553-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="b2553-112">Seuraavassa kuvassa näkyy esimerkki ostoskorin kuvakemoduulista, jossa näkyy pienoiskärry Fabrikam-otsikossa.</span><span class="sxs-lookup"><span data-stu-id="b2553-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Esimerkki ostoskärrykuvakemoduulista](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="b2553-114">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="b2553-114">Module properties</span></span>

- <span data-ttu-id="b2553-115">**Näytä pienoiskori** – Jos valinta on tosi, tämä ominaisuus mahdollistaa ostoskorin yhteenvedon (pienoiskorin) näyttämisen, kun hiiri viedään ostoskorin kuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="b2553-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="b2553-116">Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.</span><span class="sxs-lookup"><span data-stu-id="b2553-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="b2553-117">Ostoskorikuvakkeen lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="b2553-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="b2553-118">Jos haluat lisätä ostoskorikuvakkeen moduulin, katso kohta [Otsikkomoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="b2553-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2553-119">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="b2553-119">Additional resources</span></span>

[<span data-ttu-id="b2553-120">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b2553-121">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b2553-122">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b2553-123">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b2553-124">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b2553-125">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b2553-126">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="b2553-126">Gift card module</span></span>](add-giftcard.md)
