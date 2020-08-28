---
title: Ostoskorikuvakemoduuli
description: Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661144"
---
# <a name="cart-icon-module"></a><span data-ttu-id="e85a4-103">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e85a4-104">Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="e85a4-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e85a4-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="e85a4-105">Overview</span></span>

<span data-ttu-id="e85a4-106">Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on.</span><span class="sxs-lookup"><span data-stu-id="e85a4-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="e85a4-107">Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="e85a4-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="e85a4-108">Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle.</span><span class="sxs-lookup"><span data-stu-id="e85a4-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="e85a4-109">Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="e85a4-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="e85a4-110">Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta.</span><span class="sxs-lookup"><span data-stu-id="e85a4-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="e85a4-111">Seuraavassa kuvassa näkyy esimerkki ostoskorin kuvakemoduulista, jossa näkyy pienoiskärry Fabrikam-otsikossa.</span><span class="sxs-lookup"><span data-stu-id="e85a4-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Esimerkki ostoskärrykuvakemoduulista](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="e85a4-113">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="e85a4-113">Module properties</span></span>

- <span data-ttu-id="e85a4-114">**Näytä pienoiskori** – Jos valinta on tosi, tämä ominaisuus mahdollistaa ostoskorin yhteenvedon (pienoiskorin) näyttämisen, kun hiiri viedään ostoskorin kuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="e85a4-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="e85a4-115">Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.</span><span class="sxs-lookup"><span data-stu-id="e85a4-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="e85a4-116">Ostoskorikuvakkeen lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="e85a4-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="e85a4-117">Jos haluat lisätä ostoskorikuvakkeen moduulin, katso kohta [Otsikkomoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="e85a4-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e85a4-118">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="e85a4-118">Additional resources</span></span>

[<span data-ttu-id="e85a4-119">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e85a4-120">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e85a4-121">Maksumoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="e85a4-122">Toimitusosoitemoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="e85a4-123">Toimitusvaihtoehdot -moduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="e85a4-124">Tilauksen tiedot -moduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e85a4-125">Lahjakorttimoduuli</span><span class="sxs-lookup"><span data-stu-id="e85a4-125">Gift card module</span></span>](add-giftcard.md)
