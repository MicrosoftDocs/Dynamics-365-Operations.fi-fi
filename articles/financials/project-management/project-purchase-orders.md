---
title: Projektin ostotilaukset
description: Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 767a1805e7a2609c5c28bed891b42f7c8c3aaffc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556493"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="9f483-104">Projektin ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="9f483-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f483-105">Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten.</span><span class="sxs-lookup"><span data-stu-id="9f483-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="9f483-106">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="9f483-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="9f483-107">Voit luoda Microsoft Dynamics 365 for Finance and Operationsissa projektin ostotilauksia monella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="9f483-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="9f483-108">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="9f483-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="9f483-109">Menetelmät ostotilauksen luomiseksi</span><span class="sxs-lookup"><span data-stu-id="9f483-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="9f483-110">Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa käyttämällä jotakin seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="9f483-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="9f483-111">Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi myös sen, milloin nimikkeet veloitetaan projektissa.</span><span class="sxs-lookup"><span data-stu-id="9f483-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f483-112">Tapa</span><span class="sxs-lookup"><span data-stu-id="9f483-112">Method</span></span></th>
<th><span data-ttu-id="9f483-113">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="9f483-113">Purpose</span></span></th>
<th><span data-ttu-id="9f483-114">Nimikkeiden kulutus</span><span class="sxs-lookup"><span data-stu-id="9f483-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f483-115">Luo ostotilaus suoraan projektista.</span><span class="sxs-lookup"><span data-stu-id="9f483-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="9f483-116">Tällä menetelmällä voit ostaa nimikkeitä ulkopuoliselta toimittajalta projektissa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="9f483-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="9f483-117">Voit luoda ostotilauksen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="9f483-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="9f483-118">Itse projektista.</span><span class="sxs-lookup"><span data-stu-id="9f483-118">From the project itself.</span></span> <span data-ttu-id="9f483-119">Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="9f483-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="9f483-120">Siirtymällä projektin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="9f483-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="9f483-121">Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="9f483-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="9f483-122">Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</span><span class="sxs-lookup"><span data-stu-id="9f483-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f483-123">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="9f483-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="9f483-124">Käytä tätä menetelmää nimikkeiden ostamiseen, kun projektista luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="9f483-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="9f483-125">Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="9f483-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f483-126">Ostotilauksen luominen nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="9f483-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="9f483-127">Käytä tätä menetelmää nimikkeiden ostamiseen, kun luot projektista nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="9f483-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="9f483-128">Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="9f483-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="9f483-129">Kun toimittajalasku tai pakkausluettelo päivitetään, ohjelma pyytää päivittämään nimiketarpeen pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="9f483-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="9f483-130">Lisätietoja on ohjeaiheessa [Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="9f483-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

