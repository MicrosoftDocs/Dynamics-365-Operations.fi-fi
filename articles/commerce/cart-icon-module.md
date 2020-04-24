---
title: Ostoskorikuvakemoduuli
description: Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261564"
---
# <a name="cart-icon-module"></a><span data-ttu-id="ed4b8-103">Ostoskorikuvakemoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed4b8-104">Tässä ohjeaiheessa käsitellään ostoskorimoduulia ja sen lisäämistä sivuston sivuille Microsoft Dynamics 365 Commercessa.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ed4b8-105">Yleiskuvaus</span><span class="sxs-lookup"><span data-stu-id="ed4b8-105">Overview</span></span>

<span data-ttu-id="ed4b8-106">Ostoskorikuvakemoduuli edustaa koria sivun otsikkomoduulissa ja ilmaisee, kuinka monta nimikettä ostoskorissa on.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="ed4b8-107">Ostoskorikuvakemoduuli näyttää myös ostoskorin yhteenvedon (tunnetaan myös nimellä miniostoskori), kun hiiri viedään ostoskorikuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="ed4b8-108">Pienoiskori antaa käyttäjälle yhteenvedon ostoskorin nimikkeistä ilman, että sinun tarvitsee siirtyä ostoskorisivulle.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="ed4b8-109">Lisäksi se mahdollistaa myös käyttäjän siirtymisen suoraan kassasivulle, jos hän on tyytyväinen yhteenvetoon.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="ed4b8-110">Tämä vähentää sivusiirtymien määrää ja nopeuttaa uloskuittausta.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="ed4b8-111">Moduulin ominaisuudet</span><span class="sxs-lookup"><span data-stu-id="ed4b8-111">Module properties</span></span>

- <span data-ttu-id="ed4b8-112">**Näytä pienoiskori** – Jos valinta on tosi, tämä ominaisuus mahdollistaa ostoskorin yhteenvedon (pienoiskorin) näyttämisen, kun hiiri viedään ostoskorin kuvakkeen yli.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="ed4b8-113">Tätä toimintoa tuetaan vain työpöydän näkymäporteissa.</span><span class="sxs-lookup"><span data-stu-id="ed4b8-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="ed4b8-114">Ostoskorikuvakkeen lisääminen sivulle</span><span class="sxs-lookup"><span data-stu-id="ed4b8-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="ed4b8-115">Jos haluat lisätä ostoskorikuvakkeen moduulin, katso kohta [Otsikkomoduuli](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="ed4b8-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ed4b8-116">Lisäresurssit</span><span class="sxs-lookup"><span data-stu-id="ed4b8-116">Additional resources</span></span>

[<span data-ttu-id="ed4b8-117">Ostoruutumoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="ed4b8-118">Ostoskorimoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="ed4b8-119">Kassamoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="ed4b8-120">Tilauksen vahvistusmoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="ed4b8-121">Ylätunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="ed4b8-122">Alatunnistemoduuli</span><span class="sxs-lookup"><span data-stu-id="ed4b8-122">Footer module</span></span>](author-footer-module.md)
