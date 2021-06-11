---
title: Fyysisesti vastaanotetut ostotilaukset eivät näy varaston sulkemisraportissa
description: Fyysisesti vastaanotetut ostotilaukset eivät näy varaston Tarkista avoimet määrät -sulkemisraportissa.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026473"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="d0ee9-103">Fyysisesti vastaanotetut ostotilaukset eivät näy varaston sulkemisraportissa</span><span class="sxs-lookup"><span data-stu-id="d0ee9-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="d0ee9-104">Tietopankin numero: 4612595</span><span class="sxs-lookup"><span data-stu-id="d0ee9-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="d0ee9-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="d0ee9-105">Symptoms</span></span>

<span data-ttu-id="d0ee9-106">Fyysisesti vastaanotetut ostotilaukset eivät näy varaston **Tarkista avoimet määrät** -sulkemisraportissa.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="d0ee9-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="d0ee9-107">Resolution</span></span>

<span data-ttu-id="d0ee9-108">**Tarkista avoimet määrät** -raportissa näkyvät varasto-ottotapahtumat, joita ei voi selvittää kirjanpitoon päivitettyjen varastovastaanottojen kanssa valittuna sulkemispäivämääränä.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="d0ee9-109">Voit sisällyttää fyysiset vastaanotot raporttiin.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="d0ee9-110">Tässä tapauksessa fyysiset vastaanotot näkyvät, jos ne voivat kattaa ne varasto-ottotapahtumat, joita ei voida selvittää.</span><span class="sxs-lookup"><span data-stu-id="d0ee9-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="d0ee9-111">Lisätietoja on kohdassa [Varaston sulkemisen valmisteleminen](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="d0ee9-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>