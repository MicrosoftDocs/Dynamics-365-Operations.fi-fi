---
title: Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa
description: Tässä ohjeaiheessa kuvataan Veloita lähetys -toiminto.
author: ashishmsft
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: b9e0c4f55fd823bf7471edfe6ce1d424b0179d21
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800468"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a><span data-ttu-id="93a5d-103">Tilausten lähetys toisesta myymälästä käyttämällä Veloita lähetys -toimintoa</span><span class="sxs-lookup"><span data-stu-id="93a5d-103">Ship orders from another store by using the Charge send feature</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93a5d-104">Commercen Veloita lähetys -toiminnon avulla asiakastilaukset voidaan tehdä yhdessä myymälässä ja lähettää toisesta myymälästä.</span><span class="sxs-lookup"><span data-stu-id="93a5d-104">With the Charge send feature in Commerce, customer orders can be placed in one store and shipped from another store.</span></span>

<span data-ttu-id="93a5d-105">Myyntipisteasiakasohjelmien asiakastilaukset tukevat useita toteutusvaihtoehtoja.</span><span class="sxs-lookup"><span data-stu-id="93a5d-105">Customer orders in the point of sale (POS) client support multiple fulfillment options.</span></span> <span data-ttu-id="93a5d-106">Seuraavassa esitellään joitakin toteutusvaihtoehtoja:</span><span class="sxs-lookup"><span data-stu-id="93a5d-106">Some examples of fulfillment options include:</span></span>

- <span data-ttu-id="93a5d-107">Noudo samasta myymälästä eri päivänä.</span><span class="sxs-lookup"><span data-stu-id="93a5d-107">Pick up from the same store on a different date.</span></span>
- <span data-ttu-id="93a5d-108">Nouto samasta myymälästä eri päivänä.</span><span class="sxs-lookup"><span data-stu-id="93a5d-108">Pick up from a different store on the same date or a different date.</span></span>
- <span data-ttu-id="93a5d-109">Lähetys myymälään liitetystä oletuslähetysvarastosta ja toimitus tiettynä päivänä.</span><span class="sxs-lookup"><span data-stu-id="93a5d-109">Ship from the default shipping warehouse that is assigned to the store, and deliver on a specific date.</span></span>

<span data-ttu-id="93a5d-110">Veloita lähetys -toiminto käyttää seuraavia myyntipisteen toimintoja: Lähetä kaikki tuotteet ja Lähetä valitut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="93a5d-110">The Charge send feature uses the following POS operations: Ship all products and Ship selected products.</span></span> <span data-ttu-id="93a5d-111">Näin myymälänhoitaja voi valita lähetyssijainnin, josta tilaus tai tilausrivi voidaan toteuttaa.</span><span class="sxs-lookup"><span data-stu-id="93a5d-111">This allows the store clerk to select the "ship from" location that the order or order line can be fulfilled from.</span></span> <span data-ttu-id="93a5d-112">Oletusarvoisesti lähetyssijainti on myymälään liitetty lähetysvarasto.</span><span class="sxs-lookup"><span data-stu-id="93a5d-112">By default, the "ship from" location is the shipping warehouse that is associated with the store.</span></span> <span data-ttu-id="93a5d-113">Myymälänhoitaja voi kuitenkin muuttaa tätä sijaintia ja valita minkä tahansa myymälän, joka on määritetty myymälälle liitettyyn myymälän paikanninryhmään.</span><span class="sxs-lookup"><span data-stu-id="93a5d-113">However, the store clerk can change this location and select any store that is defined in the store locator group that is assigned to the store.</span></span>

<span data-ttu-id="93a5d-114">Lähetysosoitteen valintavaihtoehdot säilyvät ennallaan.</span><span class="sxs-lookup"><span data-stu-id="93a5d-114">The ability to select "ship to" addresses remains unchanged.</span></span>

<span data-ttu-id="93a5d-115">Tilausrivin toteuttamisessa käytettävät toimitustavat perustuvat tuotteiden ja osoitteiden sallittujen toimitustilojen konfiguraatioon.</span><span class="sxs-lookup"><span data-stu-id="93a5d-115">The shipping methods that can be used to fulfill the order line are based on the configuration of valid modes of delivery for products and addresses.</span></span> <span data-ttu-id="93a5d-116">Koska sallittujen toimitustilojen sääntöjä ylläpidetään Headquarters-palvelussa, myyntipisteen asiakasohjelma hakee lähetysrivin sallitut toimitustavat reaaliaikaisesti.</span><span class="sxs-lookup"><span data-stu-id="93a5d-116">Because the rules about valid of modes of delivery are maintained only in the Headquarters (HQ), the POS client makes a real-time call to fetch the valid modes of delivery for a ship line.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]