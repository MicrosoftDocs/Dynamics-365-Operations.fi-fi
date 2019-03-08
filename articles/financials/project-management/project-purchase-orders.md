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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/29/2019
ms.locfileid: "348684"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="74ebc-104">Projektin ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="74ebc-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74ebc-105">Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten.</span><span class="sxs-lookup"><span data-stu-id="74ebc-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="74ebc-106">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="74ebc-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="74ebc-107">Voit luoda Microsoft Dynamics 365 for Finance and Operationsissa projektin ostotilauksia monella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="74ebc-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="74ebc-108">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="74ebc-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="74ebc-109">Menetelmät ostotilauksen luomiseksi</span><span class="sxs-lookup"><span data-stu-id="74ebc-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="74ebc-110">Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa käyttämällä jotakin seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="74ebc-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="74ebc-111">Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi myös sen, milloin nimikkeet veloitetaan projektissa.</span><span class="sxs-lookup"><span data-stu-id="74ebc-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74ebc-112">Tapa</span><span class="sxs-lookup"><span data-stu-id="74ebc-112">Method</span></span></th>
<th><span data-ttu-id="74ebc-113">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="74ebc-113">Purpose</span></span></th>
<th><span data-ttu-id="74ebc-114">Nimikkeiden kulutus</span><span class="sxs-lookup"><span data-stu-id="74ebc-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74ebc-115">Luo ostotilaus suoraan projektista.</span><span class="sxs-lookup"><span data-stu-id="74ebc-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="74ebc-116">Tällä menetelmällä voit ostaa nimikkeitä ulkopuoliselta toimittajalta projektissa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="74ebc-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="74ebc-117">Voit luoda ostotilauksen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="74ebc-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="74ebc-118">Itse projektista.</span><span class="sxs-lookup"><span data-stu-id="74ebc-118">From the project itself.</span></span> <span data-ttu-id="74ebc-119">Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="74ebc-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="74ebc-120">Siirtymällä projektin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="74ebc-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="74ebc-121">Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="74ebc-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="74ebc-122">Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</span><span class="sxs-lookup"><span data-stu-id="74ebc-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74ebc-123">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="74ebc-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="74ebc-124">Käytä tätä menetelmää nimikkeiden ostamiseen, kun projektista luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="74ebc-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="74ebc-125">Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="74ebc-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74ebc-126">Ostotilauksen luominen nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="74ebc-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="74ebc-127">Käytä tätä menetelmää nimikkeiden ostamiseen, kun luot projektista nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="74ebc-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="74ebc-128">Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="74ebc-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="74ebc-129">Kun toimittajalasku tai pakkausluettelo päivitetään, ohjelma pyytää päivittämään nimiketarpeen pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="74ebc-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="74ebc-130">Lisätietoja on ohjeaiheessa [Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="74ebc-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

