---
title: Valikoiman ulkopuolisten tuotteiden myyminen ja palauttaminen
description: "Dynamics 365 for Retaililla voit myydä ja palauttaa valikoiman ulkopuolisia tuotteita."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: 
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 7fa5b240bc9c9f96ae5483be316eff62df915570
ms.contentlocale: fi-fi
ms.lasthandoff: 07/18/2017

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="5ed73-103">Valikoiman ulkopuolisten tuotteiden myyminen ja palauttaminen</span><span class="sxs-lookup"><span data-stu-id="5ed73-103">Sell and return products outside of an assortment</span></span>
<span data-ttu-id="5ed73-104">Jälleenmyyjän yleinen skenaario on tuotteiden myyminen asiakkaalle tai palautusten hyväksyminen asiakkaalta, vaikka tiettyjä tuotteita ei olisi liikkeessä (ts. tuotevalikoimaa ei ole myymälässä).</span><span class="sxs-lookup"><span data-stu-id="5ed73-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="5ed73-105">Seuraavassa on joitakin tyypillisiä skenaarioita:</span><span class="sxs-lookup"><span data-stu-id="5ed73-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="5ed73-106">Jälleenmyyjällä ei ole kaikkia tuotteita tietyssä kaupassa.</span><span class="sxs-lookup"><span data-stu-id="5ed73-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="5ed73-107">Muut tuotteet säilytetään varastossa.</span><span class="sxs-lookup"><span data-stu-id="5ed73-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="5ed73-108">Myymälätyöntekijä voi auttaa asiakasta haussa tai varaston tuotteiden selaamisessa, lisätä tuotteet ostoskoriin ja valmistella tilauksen jättämisen valitsemalla toimitustavan, kuten lähetys asiakkaan osoitteeseen tai asiakkaan suorittama tuotekeräily tästä tai toisesta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="5ed73-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="5ed73-109">Jälleenmyyjällä ei ole tiettyjä tuotteita myymälässä tai varastossa, mutta tuotteita on muissa myymälöissä.</span><span class="sxs-lookup"><span data-stu-id="5ed73-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="5ed73-110">Myymäläpäällikkö voi auttaa asiakasta tuotteiden haussa tai selaamisessa toisessa myymälässä, lisätä ne ostoskoriin ja jättää tilauksen valitsemalla toimitusmenetelmän.</span><span class="sxs-lookup"><span data-stu-id="5ed73-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="5ed73-111">Jälleenmyyjällä on useita myymälöitä ja tietyssä kaupungissa tai postinumeroalueella eikä halua pakottaa asiakkaita palauttamaan tuotteita samaan myymälään josta ne ostettiin.</span><span class="sxs-lookup"><span data-stu-id="5ed73-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="5ed73-112">Sen sijaan asiakkaat voivat palauttaa tuotteet mihin tahansa myymälään.</span><span class="sxs-lookup"><span data-stu-id="5ed73-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="5ed73-113">Nämä yleiset skenaariota ovat jälleenmyyjien käytössä Dynamics 365 for Retailissa.</span><span class="sxs-lookup"><span data-stu-id="5ed73-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="5ed73-114">Retailin ominaisuudet:</span><span class="sxs-lookup"><span data-stu-id="5ed73-114">With Retail, you can:</span></span>
+ <span data-ttu-id="5ed73-115">Tuotteiden haku tai selaaminen toisissa myymälöissä</span><span class="sxs-lookup"><span data-stu-id="5ed73-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="5ed73-116">Kaikkien julkaistujen tuotteiden haku tai selaaminen.</span><span class="sxs-lookup"><span data-stu-id="5ed73-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="5ed73-117">Luo itsepalvelutukkutapahtumia tai asiakastilauksia.</span><span class="sxs-lookup"><span data-stu-id="5ed73-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="5ed73-118">Valitse asiakastilausten toimitukset.</span><span class="sxs-lookup"><span data-stu-id="5ed73-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="5ed73-119">Nouda nykyisen myymälän tai toisen myymälän tuotteita.</span><span class="sxs-lookup"><span data-stu-id="5ed73-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="5ed73-120">Peruuta nykyisen myymälän tai toisen myymälän tuotteiden tilaus.</span><span class="sxs-lookup"><span data-stu-id="5ed73-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="5ed73-121">Tilauksen palauttaminen kuitin kanssa tai ilman nykyiseen tai toiseen myymälään.</span><span class="sxs-lookup"><span data-stu-id="5ed73-121">Return an order with or without the receipt at the current store or another store.</span></span>

