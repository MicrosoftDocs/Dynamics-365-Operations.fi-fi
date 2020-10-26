---
title: Huollon tilan ja edistymisen kenttien vuorovaikutus
description: Huoltotilaukset-lomakkeessa huoltotilauksen otsikon Edistyminen-kenttä ilmaisee koko huoltotilauksen tilan ja Tila-kenttä yksittäisen huoltotilausrivin tilan.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a94f2df6a4ddb71a29ff951dfe38618ac7762783
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2020
ms.locfileid: "3975485"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="92a19-103">Huollon tilan ja edistymisen kenttien vuorovaikutus</span><span class="sxs-lookup"><span data-stu-id="92a19-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="92a19-104">**Huoltotilaukset**-lomakkeessa huoltotilauksen otsikon **Edistyminen**-kenttä ilmaisee koko huoltotilauksen tilan ja **Tila**-kenttä yksittäisen huoltotilausrivin tilan.</span><span class="sxs-lookup"><span data-stu-id="92a19-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92a19-105">Tila</span><span class="sxs-lookup"><span data-stu-id="92a19-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="92a19-106">Rivin 1 tila</span><span class="sxs-lookup"><span data-stu-id="92a19-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="92a19-107">Rivin 2 tila</span><span class="sxs-lookup"><span data-stu-id="92a19-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="92a19-108">Rivin 3 tila</span><span class="sxs-lookup"><span data-stu-id="92a19-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92a19-109"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-110"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-111"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-112"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a19-113"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-114"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-115"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-116"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92a19-117"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-118"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-119"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-120"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a19-121"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-122"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-123"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-124"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="92a19-125"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-126"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-127"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-128"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="92a19-129"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-130"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-131"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="92a19-132"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="92a19-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="92a19-133">Huoltotilauksen käsittely on meneillään, jos kaikkien rivien tilana on **Luotu**. Käsittely on meneillään myös silloin, jos joidenkin rivien tilana on **Peruutettu** tai **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="92a19-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="92a19-134">Jos huoltotilauksen kaikkien rivien tilana on **Kirjattu**, huoltotilauksen tilana on **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="92a19-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="92a19-135">Jos joidenkin rivien tilana on **Kirjattu** ja joidenkin **Peruutettu**, koko tilauksen tilana on edelleen **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="92a19-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


