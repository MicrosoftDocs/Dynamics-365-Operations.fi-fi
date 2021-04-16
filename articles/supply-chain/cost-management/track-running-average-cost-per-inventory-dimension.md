---
title: Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta
description: Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä. Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8da13a01b28ca09ce9c29ecd3a9342dfb9eaa4bd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834310"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a><span data-ttu-id="e406b-104">Varastodimensiokohtaisen juoksevan keskimääräisen kustannuksen seuranta</span><span class="sxs-lookup"><span data-stu-id="e406b-104">Track running average cost per inventory dimension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e406b-105">Jokaiseen varastonimikkeeseen liitetään varastodimensioryhmä.</span><span class="sxs-lookup"><span data-stu-id="e406b-105">An inventory dimension group is attached to every inventory item.</span></span> <span data-ttu-id="e406b-106">Siten nimikkeen keskimääräinen kustannushinta lasketaan niiden varastodimensioiden perusteella, joita seurataan rahoituksellisesti.</span><span class="sxs-lookup"><span data-stu-id="e406b-106">Therefore, the running average cost price of an item is calculated based on the selected inventory dimensions that are being tracked financially.</span></span>

<span data-ttu-id="e406b-107">Varastodimensioita on kolmentyyppisiä: tuote, varasto ja seuranta.</span><span class="sxs-lookup"><span data-stu-id="e406b-107">There are three types of inventory dimensions: product, storage, and tracking.</span></span> <span data-ttu-id="e406b-108">Tuotedimensioita ovat konfiguraatio, koko ja väri.</span><span class="sxs-lookup"><span data-stu-id="e406b-108">Product dimensions include configuration, size, and color.</span></span> <span data-ttu-id="e406b-109">Tuotedimensiota seurataan aina rahoituksellisesti.</span><span class="sxs-lookup"><span data-stu-id="e406b-109">Product dimensions are always tracked financially.</span></span> <span data-ttu-id="e406b-110">Varasto- ja seurantadimensioita ovat toimipaikka, varasto, sijainti, varaston tila, rekisterikilpi, eränumero ja sarjanumero.</span><span class="sxs-lookup"><span data-stu-id="e406b-110">Storage and tracking dimensions include site, warehouse, location, inventory status, license plate, batch number, and serial number.</span></span> <span data-ttu-id="e406b-111">Voit määrittää rahoituksellisesti seurattavat varasto- ja seurantadimensiot.</span><span class="sxs-lookup"><span data-stu-id="e406b-111">You can decide which storage and tracking dimensions are tracked financially.</span></span> 

<span data-ttu-id="e406b-112">**Esimerkki 1**</span><span class="sxs-lookup"><span data-stu-id="e406b-112">**Example 1**</span></span> 

<span data-ttu-id="e406b-113">Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti, jokaiselle varastolle lasketaan keskimääräinen kustannushinta.</span><span class="sxs-lookup"><span data-stu-id="e406b-113">If the storage dimension group that is attached to the item is financially tracked by warehouse, the running average cost price is calculated per warehouse.</span></span> <span data-ttu-id="e406b-114">Seuraavat ostotilaukset on laskutettu:</span><span class="sxs-lookup"><span data-stu-id="e406b-114">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="e406b-115">Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="e406b-115">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="e406b-116">Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="e406b-116">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW.</span></span>
-   <span data-ttu-id="e406b-117">Ostotilaus, jonka määrä on 5 ja kustannushinta 15,00 USD, on laskutettu varastolle MW.</span><span class="sxs-lookup"><span data-stu-id="e406b-117">A purchase order for a quantity of 5 at a cost price of USD 15.00 has been invoiced for warehouse MW.</span></span>

<span data-ttu-id="e406b-118">Varaston GW keskimääräinen kustannushinta on 11,20 USD ja varaston MW keskimääräinen kustannushinta on 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="e406b-118">The running average cost price for warehouse GW is USD 11.20, and the running average cost price for warehouse MW is USD 15.00.</span></span> <span data-ttu-id="e406b-119">Myyntitilauslasku kirjataan varastolle GW.</span><span class="sxs-lookup"><span data-stu-id="e406b-119">A sales order invoice is posted for warehouse GW.</span></span> <span data-ttu-id="e406b-120">Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 11,20 USD.</span><span class="sxs-lookup"><span data-stu-id="e406b-120">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 11.20.</span></span> <span data-ttu-id="e406b-121">Toinen myyntitilaus kirjataan varastolle MW.</span><span class="sxs-lookup"><span data-stu-id="e406b-121">Another sales order is posted for warehouse MW.</span></span> <span data-ttu-id="e406b-122">Varaston arvo ja myytyjen tuotteiden kustannukset (ennen varaston sulkemista ja ilman merkintää) ovat 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="e406b-122">The value of the inventory and the cost of goods sold (before inventory close is run and without marking) is USD 15.00.</span></span> 

<span data-ttu-id="e406b-123">**Esimerkki 2** Jos varasto seuraa nimikkeeseen liitettyä varastodimensioryhmää rahoituksellisesti ja eränumero seuraa seurantadimensioryhmää rahoituksellisesti, keskimääräinen kustannushinta lasketaan kullekin erälle.</span><span class="sxs-lookup"><span data-stu-id="e406b-123">**Example 2** If the storage dimension group that is attached to the item is financially tracked by warehouse, and the tracking dimension group is financially tracked by batch number, the running average cost price is calculated for each batch.</span></span> 

<span data-ttu-id="e406b-124">**Huomautus:** Kaikkien seurattavien taloushallinnon dimensioiden kustannushintaa on hyvä pitää silmällä.</span><span class="sxs-lookup"><span data-stu-id="e406b-124">**Note:** We recommend that you always view the cost price for all financial dimensions that are being tracked.</span></span> <span data-ttu-id="e406b-125">Seuraavat ostotilaukset on laskutettu:</span><span class="sxs-lookup"><span data-stu-id="e406b-125">The following purchase orders have been invoiced:</span></span>

-   <span data-ttu-id="e406b-126">Ostotilaus, jonka määrä on 2 ja kustannushinta 10,00 USD, on laskutettu varastolle GW ja erälle AAA.</span><span class="sxs-lookup"><span data-stu-id="e406b-126">A purchase order for a quantity of 2 at a cost price of USD 10.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="e406b-127">Ostotilaus, jonka määrä on 3 ja kustannushinta 12,00 USD, on laskutettu varastolle GW ja erälle AAA.</span><span class="sxs-lookup"><span data-stu-id="e406b-127">A purchase order for a quantity of 3 at a cost price of USD 12.00 has been invoiced for warehouse GW and batch AAA.</span></span>
-   <span data-ttu-id="e406b-128">Ostotilaus, jonka määrä on 2 ja kustannushinta 15,00 USD, on laskutettu varastolle GW ja erälle BBB.</span><span class="sxs-lookup"><span data-stu-id="e406b-128">A purchase order for a quantity of 2 at a cost price of USD 15.00 has been invoiced for warehouse GW and batch BBB.</span></span>

<span data-ttu-id="e406b-129">Varaston GW ja erän AAA keskimääräinen kustannushinta on 11,20 USD ja varaston MW ja erän BBB keskimääräinen kustannushinta on 15,00 USD.</span><span class="sxs-lookup"><span data-stu-id="e406b-129">The running average cost price for warehouse GW and batch AAA is USD 11.20, and the running average cost price for warehouse GW and batch BBB is USD 15.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]