---
title: Projektin ostotilaukset
description: "Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten. Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 1797bc49877f1c8c06797083d1c7b76934675ba3
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="1e6b5-104">Projektin ostotilaukset</span><span class="sxs-lookup"><span data-stu-id="1e6b5-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1e6b5-105">Tässä artikkelissa kuvataan eri menetelmiä, joiden avulla voi luoda ostotilauksia projektia varten.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="1e6b5-106">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="1e6b5-107">Voit luoda Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionissa projektin ostotilauksia monella eri tavalla.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="1e6b5-108">Käytettävä menetelmä määräytyy ostotilauksen tarkoituksen, ostettujen nimikkeiden kulutusajankohdan sekä ostettujen nimikkeiden veloitusajankohdan mukaan.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="1e6b5-109">Menetelmät ostotilauksen luomiseksi</span><span class="sxs-lookup"><span data-stu-id="1e6b5-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="1e6b5-110">Voit luoda ostotilauksen projektinhallinnassa ja kirjanpidossa käyttämällä jotakin seuraavista menetelmistä.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="1e6b5-111">Ostotilauksen tarkoitus määrittää ostotilauksen kulutusajankohdan ja tämän vuoksi myös sen, milloin nimikkeet veloitetaan projektissa.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1e6b5-112">Tapa</span><span class="sxs-lookup"><span data-stu-id="1e6b5-112">Method</span></span></th>
<th><span data-ttu-id="1e6b5-113">Tarkoitus</span><span class="sxs-lookup"><span data-stu-id="1e6b5-113">Purpose</span></span></th>
<th><span data-ttu-id="1e6b5-114">Nimikkeiden kulutus</span><span class="sxs-lookup"><span data-stu-id="1e6b5-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1e6b5-115">Luo ostotilaus suoraan projektista.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="1e6b5-116">Tällä menetelmällä voit ostaa nimikkeitä ulkopuoliselta toimittajalta projektissa käytettäväksi.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="1e6b5-117">Voit luoda ostotilauksen kahdella tavalla:</span><span class="sxs-lookup"><span data-stu-id="1e6b5-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="1e6b5-118">Itse projektista.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-118">From the project itself.</span></span> <span data-ttu-id="1e6b5-119">Tässä tapauksessa projekti on jo määritetty ostotilaukselle.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="1e6b5-120">Siirtymällä projektin ostotilaukseen.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="1e6b5-121">Tällöin on valittava sekä toimittaja että projekti, jolle ostotilaus luodaan.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="1e6b5-122">Nimikkeet kulutetaan, kun toimittajalasku päivitetään.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1e6b5-123">Ostotilauksen luominen myyntitilauksesta</span><span class="sxs-lookup"><span data-stu-id="1e6b5-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="1e6b5-124">Käytä tätä menetelmää nimikkeiden ostamiseen, kun projektista luodaan myyntitilaus.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="1e6b5-125">Nimikkeet kulutetaan, kun myyntitilaus laskutetaan asiakkaalta.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1e6b5-126">Ostotilauksen luominen nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="1e6b5-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="1e6b5-127">Käytä tätä menetelmää nimikkeiden ostamiseen, kun luot projektista nimiketarpeen.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="1e6b5-128">Nimikkeet kulutetaan, kun nimiketarpeen pakkausluettelo päivitetään.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="1e6b5-129">Kun toimittajalasku tai pakkausluettelo päivitetään, ohjelma pyytää päivittämään nimiketarpeen pakkausluettelon.</span><span class="sxs-lookup"><span data-stu-id="1e6b5-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="1e6b5-130">Lisätietoja on ohjeaiheessa [Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="1e6b5-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


