---
title: Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan
description: Dynamics 365 Commercessa voi myydä ja palauttaa valikoiman ulkopuolisia tuotteita.
author: pdp1207
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b6bae9f0d3a236c69ee3ee47226c19c1e1dcaf42
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794040"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="fe10b-103">Myy ja palauta tuotteet, jotka eivät kuulu myymälän on valikoimaan</span><span class="sxs-lookup"><span data-stu-id="fe10b-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fe10b-104">Jälleenmyyjän yleinen skenaario on tuotteiden myyminen asiakkaalle tai palautusten hyväksyminen asiakkaalta, vaikka tiettyjä tuotteita ei olisi liikkeessä (tuotevalikoimaa ei siis ole myymälässä).</span><span class="sxs-lookup"><span data-stu-id="fe10b-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="fe10b-105">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="fe10b-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="fe10b-106">Jälleenmyyjällä ei ole kaikkia tuotteita tietyssä kaupassa.</span><span class="sxs-lookup"><span data-stu-id="fe10b-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="fe10b-107">Muut tuotteet säilytetään varastossa.</span><span class="sxs-lookup"><span data-stu-id="fe10b-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="fe10b-108">Myymälätyöntekijä voi auttaa asiakasta haussa tai varaston tuotteiden selaamisessa, lisätä tuotteet ostoskoriin ja valmistella tilauksen jättämisen valitsemalla toimitustavan, kuten lähetys asiakkaan osoitteeseen tai asiakkaan suorittama tuotekeräily tästä tai toisesta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="fe10b-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="fe10b-109">Jälleenmyyjällä ei ole tiettyjä tuotteita myymälässä tai varastossa, mutta tuotteita on muissa myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="fe10b-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="fe10b-110">Myymäläpäällikkö voi auttaa asiakasta tuotteiden haussa tai selaamisessa toisessa myymälässä, lisätä ne ostoskoriin ja jättää tilauksen valitsemalla toimitusmenetelmän.</span><span class="sxs-lookup"><span data-stu-id="fe10b-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="fe10b-111">Jälleenmyyjällä on useita myymälöitä ja tietyssä kaupungissa tai postinumeroalueella eikä halua pakottaa asiakkaita palauttamaan tuotteita samaan myymälään josta ne ostettiin.</span><span class="sxs-lookup"><span data-stu-id="fe10b-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="fe10b-112">Sen sijaan asiakkaat voivat palauttaa tuotteet mihin tahansa myymälään.</span><span class="sxs-lookup"><span data-stu-id="fe10b-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="fe10b-113">Nämä yleiset skenaariot ovat jälleenmyyjien käytettävissä Commercessa.</span><span class="sxs-lookup"><span data-stu-id="fe10b-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="fe10b-114">Commercen ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="fe10b-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="fe10b-115">Tuotteiden haku tai selaaminen toisissa myymälöissä</span><span class="sxs-lookup"><span data-stu-id="fe10b-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="fe10b-116">Kaikkien julkaistujen tuotteiden haku tai selaaminen.</span><span class="sxs-lookup"><span data-stu-id="fe10b-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="fe10b-117">Luo itsepalvelutukkutapahtumia tai asiakastilauksia.</span><span class="sxs-lookup"><span data-stu-id="fe10b-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="fe10b-118">Valitse asiakastilausten toimitukset.</span><span class="sxs-lookup"><span data-stu-id="fe10b-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="fe10b-119">Nouda nykyisen myymälän tai toisen myymälän tuotteita.</span><span class="sxs-lookup"><span data-stu-id="fe10b-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="fe10b-120">Peruuta nykyisen myymälän tai toisen myymälän tuotteiden tilaus.</span><span class="sxs-lookup"><span data-stu-id="fe10b-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="fe10b-121">Tilauksen palauttaminen kuitin kanssa tai ilman nykyiseen tai toiseen myymälään.</span><span class="sxs-lookup"><span data-stu-id="fe10b-121">Return an order with or without the receipt at the current store or another store.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]