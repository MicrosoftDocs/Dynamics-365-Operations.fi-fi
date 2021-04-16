---
title: Konsolidoidut erätilaukset
description: Tässä artikkelissa kuvataan konsolidoitujen erätilausten käsite.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8d7656889b69cfd1dcffb45b52eb649bce59629
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809227"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="0fda1-103">Konsolidoidut erätilaukset</span><span class="sxs-lookup"><span data-stu-id="0fda1-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0fda1-104">Tässä artikkelissa kuvataan konsolidoitujen erätilausten käsite.</span><span class="sxs-lookup"><span data-stu-id="0fda1-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="0fda1-105">Tuotettua bulkkinimikettä käsitellään ylänimikkeenä, ja pakattua nimikettä on alanimikkeenä.</span><span class="sxs-lookup"><span data-stu-id="0fda1-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="0fda1-106">Bulkki- ja pakatun nimikkeen suhde esitetään bulkkinimikkeen muunnoksena.</span><span class="sxs-lookup"><span data-stu-id="0fda1-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="0fda1-107">Bulkkinimikkeen muunnos määritellään bulkkinimikkeessä itsessään.</span><span class="sxs-lookup"><span data-stu-id="0fda1-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="0fda1-108">Pakatut nimikkeet voidaan pakata joko yksittäiseen koon konttiin tai usean koon kontteihin, joita käsitellään yhtenä yksikkönä.</span><span class="sxs-lookup"><span data-stu-id="0fda1-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="0fda1-109">Konsolidoimalla bulkkinimikkeiden tilauksia voit tarkastella kaikkia liittyviä erätilauksia yhdessä näkymässä, jonka avulla voit määrittää jäljellä olevat työt, jotka on suoritettava.</span><span class="sxs-lookup"><span data-stu-id="0fda1-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="0fda1-110">Konsolidoitu erätilaus voi sisältää yhdistelmän mitä tahansa seuraavia tilauksia:</span><span class="sxs-lookup"><span data-stu-id="0fda1-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="0fda1-111">Yksittäinen bulkkitilaus ja useita pakattuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="0fda1-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="0fda1-112">Useita bulkki- sekä pakattuja tilauksia</span><span class="sxs-lookup"><span data-stu-id="0fda1-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="0fda1-113">Useita bulkkitilauksia ja yksittäinen pakattu tilaus</span><span class="sxs-lookup"><span data-stu-id="0fda1-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="0fda1-114">Vain pakatut tilaukset</span><span class="sxs-lookup"><span data-stu-id="0fda1-114">Only packed orders</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]