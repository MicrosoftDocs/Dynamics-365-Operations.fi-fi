---
title: Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella
description: Tässä menettelyssä osoitetaan, miten ostotilauksen nimikkeet vastaanotetaan nimiketarpeesta.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26572a49426719fba520338a5eccd7e0af78890e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572370"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="f462e-103">Ostotilauksen nimikkeiden vastaanotto nimiketarpeen perusteella</span><span class="sxs-lookup"><span data-stu-id="f462e-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f462e-104">Tässä menettelyssä osoitetaan, miten ostotilauksen nimikkeet vastaanotetaan nimiketarpeesta.</span><span class="sxs-lookup"><span data-stu-id="f462e-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="f462e-105">Kun käytät nimiketarvetta nimiketapahtuman sijaan, voit suunnitella toimituksen niin, että se tapahtuu juuri ennen nimikkeen käyttöä, luoda ostotilauksen, sisällyttää nimikkeen kauppasopimukseen ja sisällyttää nimiketarpeen tuotannonsuunnitteluun.</span><span class="sxs-lookup"><span data-stu-id="f462e-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="f462e-106">Tässä tehtävässä käytetään USSI-tietojoukkoa.</span><span class="sxs-lookup"><span data-stu-id="f462e-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f462e-107">Valitse Projektinhallinta ja kirjanpito > Projektit > Kaikki projektit.</span><span class="sxs-lookup"><span data-stu-id="f462e-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="f462e-108">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f462e-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="f462e-109">Valitse toimintoruudussa Suunnitelma.</span><span class="sxs-lookup"><span data-stu-id="f462e-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="f462e-110">Valitse Nimiketarpeet.</span><span class="sxs-lookup"><span data-stu-id="f462e-110">Click Item requirements.</span></span>
5. <span data-ttu-id="f462e-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="f462e-111">Click New.</span></span>
6. <span data-ttu-id="f462e-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f462e-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f462e-113">Syötä tai valitse arvo Nimiketunnus-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f462e-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="f462e-114">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="f462e-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="f462e-115">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="f462e-115">Click Save.</span></span>
10. <span data-ttu-id="f462e-116">Valitse toimintoruudussa Hallitse.</span><span class="sxs-lookup"><span data-stu-id="f462e-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="f462e-117">Valitse Toiminnot.</span><span class="sxs-lookup"><span data-stu-id="f462e-117">Click Functions.</span></span>
12. <span data-ttu-id="f462e-118">Valitse Luo ostotilaus.</span><span class="sxs-lookup"><span data-stu-id="f462e-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="f462e-119">Valitse Sisällytä-valintaruutu.</span><span class="sxs-lookup"><span data-stu-id="f462e-119">Select the Include check box.</span></span>
14. <span data-ttu-id="f462e-120">Anna tai valitse arvo Toimittajatili-kentässä.</span><span class="sxs-lookup"><span data-stu-id="f462e-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="f462e-121">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f462e-121">Click OK.</span></span>
16. <span data-ttu-id="f462e-122">Valitse Ostoreskontra > Ostotilaukset > Kaikki ostotilaukset.</span><span class="sxs-lookup"><span data-stu-id="f462e-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="f462e-123">Napsauta luettelossa valitulla rivillä olevaa linkkiä.</span><span class="sxs-lookup"><span data-stu-id="f462e-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f462e-124">Valitse toimintoruudussa Osta.</span><span class="sxs-lookup"><span data-stu-id="f462e-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="f462e-125">Valitse Vahvista.</span><span class="sxs-lookup"><span data-stu-id="f462e-125">Click Confirm.</span></span>
20. <span data-ttu-id="f462e-126">Valitse toimintoruudussa Vastaanota.</span><span class="sxs-lookup"><span data-stu-id="f462e-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="f462e-127">Valitse Tuotteen vastaanotto.</span><span class="sxs-lookup"><span data-stu-id="f462e-127">Click Product receipt.</span></span>
22. <span data-ttu-id="f462e-128">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="f462e-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="f462e-129">Kirjoita arvo Tuotteen vastaanotto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="f462e-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="f462e-130">Valitse OK.</span><span class="sxs-lookup"><span data-stu-id="f462e-130">Click OK.</span></span>

