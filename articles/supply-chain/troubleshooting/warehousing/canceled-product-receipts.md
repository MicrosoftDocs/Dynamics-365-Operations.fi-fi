---
title: Peruutetut tuotevastaanotot eivät päivitä tapahtuman tilaksi Rekisteröity
description: Kun olet peruuttanut saapuvan kuorman tuotevastaanotot, järjestelmä päivittää varastotapahtuman tilaksi automaattisesti Vastaanotettu-tilasta Tilattu-tilaan.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9c86457d50a7a9ac2a699a0e0a9c7bdf4cd7c67b
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294063"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a><span data-ttu-id="012bb-103">Peruutetut tuotevastaanotot eivät päivitä tapahtuman tilaksi Rekisteröity</span><span class="sxs-lookup"><span data-stu-id="012bb-103">Canceled product receipts don't update transaction status to Registered</span></span>

## <a name="symptoms"></a><span data-ttu-id="012bb-104">Oireet</span><span class="sxs-lookup"><span data-stu-id="012bb-104">Symptoms</span></span>

<span data-ttu-id="012bb-105">Kun olet suorittanut saapuvalle kuormalle **Peruuta tuotevastaanotot** -toiminnon, järjestelmä päivittää varastotapahtuman tilaksi automaattisesti *Vastaanotettu*-tilasta *Tilattu*-tilaan.</span><span class="sxs-lookup"><span data-stu-id="012bb-105">After you run the **Cancel product receipts** action on an inbound load, the system automatically updates the status of inventory transactions from *Received* to *Ordered*.</span></span>

## <a name="resolution"></a><span data-ttu-id="012bb-106">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="012bb-106">Resolution</span></span>

<span data-ttu-id="012bb-107">Kun lähtevien kuormien pakkausluettelot peruutetaan, varastotapahtumien tilana pysyy *Kerätty*.</span><span class="sxs-lookup"><span data-stu-id="012bb-107">When packing slips are canceled for outbound loads, the status of inventory transactions remains *Picked*.</span></span> <span data-ttu-id="012bb-108">Kun saapuvan kuorman tuotevastaanotot peruutetaan, varastotapahtumien tilaksi ei kuitenkaan palauteta *Rekisteröity*.</span><span class="sxs-lookup"><span data-stu-id="012bb-108">However, when product receipts from an inbound load are canceled, the status of inventory transactions isn't restored to *Registered*.</span></span> <span data-ttu-id="012bb-109">Kun siis saapuvan kuorman tuotevastaanotto on peruutettu, varastotyöntekijän on rekisteröitävä kuorman nimikemäärät uudelleen.</span><span class="sxs-lookup"><span data-stu-id="012bb-109">Therefore, after a product receipt from an inbound load is canceled, the warehouse worker must re-register item quantities for the loads.</span></span>

<span data-ttu-id="012bb-110">Lisätietoja on kohdassa [Saapuvan kuorman nimikemäärien rekisteröiminen](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span><span class="sxs-lookup"><span data-stu-id="012bb-110">For more information, see [Register item quantities that arrive on an inbound load](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).</span></span>
