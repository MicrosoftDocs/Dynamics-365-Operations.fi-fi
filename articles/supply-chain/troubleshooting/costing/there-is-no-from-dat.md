---
title: Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä
description: Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dd13f6a3e5ce3c894e96f420358d337f2e43dba
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026488"
---
# <a name="there-is-no-from-date-value-on-the-active-prices-tab-of-the-item-price-page"></a><span data-ttu-id="a01d9-103">Päivämäärästä-arvoa ei ole Nimikkeen hinta -sivun Aktiiviset hinnat -välilehdessä</span><span class="sxs-lookup"><span data-stu-id="a01d9-103">There is no From date value on the Active prices tab of the Item price page</span></span>

<span data-ttu-id="a01d9-104">Tietopankin numero: 4613548</span><span class="sxs-lookup"><span data-stu-id="a01d9-104">KB number: 4613548</span></span>

## <a name="symptoms"></a><span data-ttu-id="a01d9-105">Oireet</span><span class="sxs-lookup"><span data-stu-id="a01d9-105">Symptoms</span></span>

<span data-ttu-id="a01d9-106">**Päivämäärästä-arvoa** ei ole **Nimikkeen hinta** -sivun **Aktiiviset hinnat** -välilehdessä.</span><span class="sxs-lookup"><span data-stu-id="a01d9-106">There is no **From date** value on the **Active prices** tab of the **Item price** page.</span></span>

## <a name="resolution"></a><span data-ttu-id="a01d9-107">Ratkaisu</span><span class="sxs-lookup"><span data-stu-id="a01d9-107">Resolution</span></span>

<span data-ttu-id="a01d9-108">Odottavassa hinnassa määritettyä **Päivämäärästä**-arvoa (voimaantulopäivämäärä) ei siirretä aktiiviseen hintaan.</span><span class="sxs-lookup"><span data-stu-id="a01d9-108">The **From date** value (effective date) that is set on the pending price isn't transferred to the active price.</span></span>

<span data-ttu-id="a01d9-109">Kun nimikkeen kustannustietue lisätään ensimmäisen kerran, sen tila on *Odottaa* ja siinä on voimaantulopäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a01d9-109">When an item cost record is first entered, it has a status of *Pending* and an intended effective date.</span></span> <span data-ttu-id="a01d9-110">Kun aktivoit nimikkeen kustannustietueen, tilaksi päivitetään *Aktiivinen* ja voimaantulopäivä päivitetään aktivointipäiväksi.</span><span class="sxs-lookup"><span data-stu-id="a01d9-110">When you activate the item cost record, the status is updated to *Active*, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="a01d9-111">Siksi aktiivisen hinnan aktivointipäivämäärä on aina todellinen aktivointipäivämäärä.</span><span class="sxs-lookup"><span data-stu-id="a01d9-111">Therefore, the active price's activation date is always the actual date of the activation.</span></span>

<span data-ttu-id="a01d9-112">Lisätietoja on kohdassa [Kustannuslaskelmaversiot](../../cost-management/costing-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a01d9-112">For more information, see [Costing versions overview](../../cost-management/costing-versions.md).</span></span>
