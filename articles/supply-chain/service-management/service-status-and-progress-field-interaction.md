---
title: Huollon tilan ja edistymisen kenttien vuorovaikutus
description: Huoltotilaukset-lomakkeessa huoltotilauksen otsikon Edistyminen-kenttä ilmaisee koko huoltotilauksen tilan ja Tila-kenttä yksittäisen huoltotilausrivin tilan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2dd7b5160149a38dd62535901c1225bf704f404d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570783"
---
# <a name="service-status-and-progress-field-interaction"></a><span data-ttu-id="a7700-103">Huollon tilan ja edistymisen kenttien vuorovaikutus</span><span class="sxs-lookup"><span data-stu-id="a7700-103">Service status and progress field interaction</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a7700-104">**Huoltotilaukset**-lomakkeessa huoltotilauksen otsikon **Edistyminen**-kenttä ilmaisee koko huoltotilauksen tilan ja **Tila**-kenttä yksittäisen huoltotilausrivin tilan.</span><span class="sxs-lookup"><span data-stu-id="a7700-104">In the **Service orders** form, the **Progress** field on the service order header reflects the status of the whole service order, and the **Status** reports the status of individual service order lines.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a7700-105">Tila</span><span class="sxs-lookup"><span data-stu-id="a7700-105">Progress</span></span></p></th>
<th><p><span data-ttu-id="a7700-106">Rivin 1 tila</span><span class="sxs-lookup"><span data-stu-id="a7700-106">Line 1 Status</span></span></p></th>
<th><p><span data-ttu-id="a7700-107">Rivin 2 tila</span><span class="sxs-lookup"><span data-stu-id="a7700-107">Line 2 Status</span></span></p></th>
<th><p><span data-ttu-id="a7700-108">Rivin 3 tila</span><span class="sxs-lookup"><span data-stu-id="a7700-108">Line 3 Status</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a7700-109"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-109"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-110"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-110"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-111"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-111"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-112"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-112"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7700-113"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-113"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-114"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-114"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-115"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-115"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-116"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-116"><strong>Created</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7700-117"><strong>Käsittelyssä</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-117"><strong>In process</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-118"><strong>Luotu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-118"><strong>Created</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-119"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-119"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-120"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-120"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7700-121"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-121"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-122"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-122"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-123"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-123"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-124"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-124"><strong>Canceled</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a7700-125"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-125"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-126"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-126"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-127"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-127"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-128"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-128"><strong>Posted</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a7700-129"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-129"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-130"><strong>Kirjattu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-130"><strong>Posted</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-131"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-131"><strong>Canceled</strong></span></span></p></td>
<td><p><span data-ttu-id="a7700-132"><strong>Peruutettu</strong></span><span class="sxs-lookup"><span data-stu-id="a7700-132"><strong>Canceled</strong></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a7700-133">Huoltotilauksen käsittely on meneillään, jos kaikkien rivien tilana on **Luotu**. Käsittely on meneillään myös silloin, jos joidenkin rivien tilana on **Peruutettu** tai **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="a7700-133">The progress of a service order is in process if all lines have the status **Created**; it is still in process if some of the lines have a status of **Canceled** or **Posted**.</span></span>

<span data-ttu-id="a7700-134">Jos huoltotilauksen kaikkien rivien tilana on **Kirjattu**, huoltotilauksen tilana on **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="a7700-134">If all lines in a service order are marked as **Posted**, the progress of the status order is **Posted**.</span></span> <span data-ttu-id="a7700-135">Jos joidenkin rivien tilana on **Kirjattu** ja joidenkin **Peruutettu**, koko tilauksen tilana on edelleen **Kirjattu**.</span><span class="sxs-lookup"><span data-stu-id="a7700-135">If some lines are **Posted** and some are **Canceled**, the progress is still **Posted**.</span></span>

  


