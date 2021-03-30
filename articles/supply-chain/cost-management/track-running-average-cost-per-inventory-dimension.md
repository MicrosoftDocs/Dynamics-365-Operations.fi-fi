---
title: Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta
description: Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä. Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2bf04a42edf09c35e81742b1c60db8944eba2ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252867"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="ab550-104">Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta</span><span class="sxs-lookup"><span data-stu-id="ab550-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab550-105">Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä.</span><span class="sxs-lookup"><span data-stu-id="ab550-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="ab550-106">Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.</span><span class="sxs-lookup"><span data-stu-id="ab550-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="ab550-107">Varastodimensioita on kolmentyyppisiä: tuote, varasto ja seuranta.</span><span class="sxs-lookup"><span data-stu-id="ab550-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="ab550-108">Tuotedimensioita ovat konfiguraatio, koko ja väri.</span><span class="sxs-lookup"><span data-stu-id="ab550-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="ab550-109">Tuotedimensiota seurataan aina rahoituksellisesti.</span><span class="sxs-lookup"><span data-stu-id="ab550-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="ab550-110">Varasto- ja seurantadimensioita ovat toimipaikka, varasto, sijainti, varaston tila, rekisterikilpi, eränumero ja sarjanumero.</span><span class="sxs-lookup"><span data-stu-id="ab550-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="ab550-111">Voit määrittää rahoituksellisesti seurattavat varasto- ja seurantadimensiot.</span><span class="sxs-lookup"><span data-stu-id="ab550-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="ab550-112">**Esimerkki 1**</span><span class="sxs-lookup"><span data-stu-id="ab550-112">**Example 1**</span></span> 

<span data-ttu-id="ab550-113">Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti, jokaiselle varastolle lasketaan keskimääräinen kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="ab550-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="ab550-114">Seuraavat ostotilaukset on laskutettu:</span><span class="sxs-lookup"><span data-stu-id="ab550-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="ab550-115">Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="ab550-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="ab550-116">Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="ab550-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="ab550-117">Ostotilaus, jonka määrä on 5 ja kustannushinta 15,00 USD, on laskutettu varastolle MW.</span><span class="sxs-lookup"><span data-stu-id="ab550-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="ab550-118">Varaston GW keskimääräinen kustannushinta on 11,20 USD ja varaston MW keskimääräinen kustannushinta on 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="ab550-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="ab550-119">Myyntitilauslasku kirjataan varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="ab550-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="ab550-120">Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 11,20 USD.</span><span class="sxs-lookup"><span data-stu-id="ab550-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="ab550-121">Toinen myyntitilaus kirjataan varastolle MW.</span><span class="sxs-lookup"><span data-stu-id="ab550-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="ab550-122">Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="ab550-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="ab550-123">**Esimerkki 2** Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti ja eränumero seuraa seurantadimensioryhmää rahoituksellisesti, keskimääräinen kustannushinta lasketaan kullekin erälle.</span><span class="sxs-lookup"><span data-stu-id="ab550-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="ab550-124">**Huomautus:** Kaikkien seurattavien taloushallinnon dimensioiden kustannushintaa on hyvä pitää silmällä.</span><span class="sxs-lookup"><span data-stu-id="ab550-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="ab550-125">Seuraavat ostotilaukset on laskutettu:</span><span class="sxs-lookup"><span data-stu-id="ab550-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="ab550-126">Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW ja erälle AAA.</span><span class="sxs-lookup"><span data-stu-id="ab550-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="ab550-127">Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW ja erälle AAA.</span><span class="sxs-lookup"><span data-stu-id="ab550-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="ab550-128">Ostotilaus, jonka määrä on 2 ja kustannushinta 15,00 USD, on laskutettu varastolle GW ja erälle BBB.</span><span class="sxs-lookup"><span data-stu-id="ab550-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="ab550-129">Varaston GW ja erän AAA keskimääräinen kustannushinta on 11,20 USD ja varaston MW ja erän BBB keskimääräinen kustannushinta on 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="ab550-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]