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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174555"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="081ba-104">Projektin ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="081ba-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="081ba-105">Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten.</span><span class="sxs-lookup"><span data-stu-id="081ba-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="081ba-106">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="081ba-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="081ba-107">Menetelmät ostotilauksen luomiseksi</span><span class="sxs-lookup"><span data-stu-id="081ba-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="081ba-108">Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa käyttämällä jotakin seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="081ba-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="081ba-109">Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi myös sen, milloin nimikkeet veloitetaan projektissa.</span><span class="sxs-lookup"><span data-stu-id="081ba-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="081ba-110">Tapa</span><span class="sxs-lookup"><span data-stu-id="081ba-110">Method</span></span></th>
<th><span data-ttu-id="081ba-111">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="081ba-111">Purpose</span></span></th>
<th><span data-ttu-id="081ba-112">Nimikkeiden kulutus</span><span class="sxs-lookup"><span data-stu-id="081ba-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="081ba-113">Luo ostotilaus suoraan projektista.</span><span class="sxs-lookup"><span data-stu-id="081ba-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="081ba-114">Tällä menetelmällä voit ostaa nimikkeitä ulkopuoliselta toimittajalta projektissa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="081ba-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="081ba-115">Voit luoda ostotilauksen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="081ba-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="081ba-116">Itse projektista.</span><span class="sxs-lookup"><span data-stu-id="081ba-116">From the project itself.</span></span> <span data-ttu-id="081ba-117">Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="081ba-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="081ba-118">Siirtymällä projektin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="081ba-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="081ba-119">Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="081ba-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="081ba-120">Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</span><span class="sxs-lookup"><span data-stu-id="081ba-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="081ba-121">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="081ba-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="081ba-122">Käytä tätä menetelmää nimikkeiden ostamiseen, kun projektista luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="081ba-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="081ba-123">Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="081ba-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="081ba-124">Ostotilauksen luominen nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="081ba-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="081ba-125">Käytä tätä menetelmää nimikkeiden ostamiseen, kun luot projektista nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="081ba-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="081ba-126">Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="081ba-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="081ba-127">Kun toimittajalasku tai pakkausluettelo päivitetään, ohjelma pyytää päivittämään nimiketarpeen pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="081ba-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="081ba-128">Lisätietoja on ohjeaiheessa [Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="081ba-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

