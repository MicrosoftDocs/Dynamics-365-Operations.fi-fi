---
title: Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan
description: Dynamics 365 Commerceissa voi myydä ja palauttaa valikoiman ulkopuolisia tuotteita.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412052"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="26e83-103">Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan</span><span class="sxs-lookup"><span data-stu-id="26e83-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26e83-104">Jälleenmyyjän yleinen skenaario on tuotteiden myyminen asiakkaalle tai palautusten hyväksyminen asiakkaalta, vaikka tiettyjä tuotteita ei olisi liikkeessä (tuotevalikoimaa ei siis ole myymälässä).</span><span class="sxs-lookup"><span data-stu-id="26e83-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="26e83-105">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="26e83-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="26e83-106">Jälleenmyyjällä ei ole kaikkia tuotteita tietyssä kaupassa.</span><span class="sxs-lookup"><span data-stu-id="26e83-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="26e83-107">Muut tuotteet säilytetään varastossa.</span><span class="sxs-lookup"><span data-stu-id="26e83-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="26e83-108">Myymälätyöntekijä voi auttaa asiakasta haussa tai varaston tuotteiden selaamisessa, lisätä tuotteet ostoskoriin ja valmistella tilauksen jättämisen valitsemalla toimitustavan, kuten lähetys asiakkaan osoitteeseen tai asiakkaan suorittama tuotekeräily tästä tai toisesta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="26e83-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="26e83-109">Jälleenmyyjällä ei ole tiettyjä tuotteita myymälässä tai varastossa, mutta tuotteita on muissa myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="26e83-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="26e83-110">Myymäläpäällikkö voi auttaa asiakasta tuotteiden haussa tai selaamisessa toisessa myymälässä, lisätä ne ostoskoriin ja jättää tilauksen valitsemalla toimitusmenetelmän.</span><span class="sxs-lookup"><span data-stu-id="26e83-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="26e83-111">Jälleenmyyjällä on useita myymälöitä ja tietyssä kaupungissa tai postinumeroalueella eikä halua pakottaa asiakkaita palauttamaan tuotteita samaan myymälään josta ne ostettiin.</span><span class="sxs-lookup"><span data-stu-id="26e83-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="26e83-112">Sen sijaan asiakkaat voivat palauttaa tuotteet mihin tahansa myymälään.</span><span class="sxs-lookup"><span data-stu-id="26e83-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="26e83-113">Nämä yleiset skenaariot ovat jälleenmyyjien käytettävissä Commercessa.</span><span class="sxs-lookup"><span data-stu-id="26e83-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="26e83-114">Commercen ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="26e83-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="26e83-115">Tuotteiden haku tai selaaminen toisissa myymälöissä</span><span class="sxs-lookup"><span data-stu-id="26e83-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="26e83-116">Kaikkien julkaistujen tuotteiden haku tai selaaminen.</span><span class="sxs-lookup"><span data-stu-id="26e83-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="26e83-117">Luo itsepalvelutukkutapahtumia tai asiakastilauksia.</span><span class="sxs-lookup"><span data-stu-id="26e83-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="26e83-118">Valitse asiakastilausten toimitukset.</span><span class="sxs-lookup"><span data-stu-id="26e83-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="26e83-119">Nouda nykyisen myymälän tai toisen myymälän tuotteita.</span><span class="sxs-lookup"><span data-stu-id="26e83-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="26e83-120">Peruuta nykyisen myymälän tai toisen myymälän tuotteiden tilaus.</span><span class="sxs-lookup"><span data-stu-id="26e83-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="26e83-121">Tilauksen palauttaminen kuitin kanssa tai ilman nykyiseen tai toiseen myymälään.</span><span class="sxs-lookup"><span data-stu-id="26e83-121">Return an order with or without the receipt at the current store or another store.</span></span>
