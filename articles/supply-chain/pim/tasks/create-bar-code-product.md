---
title: Viivakoodin luonti tuotteelle
description: Tässä toimintaohjeessa kuvataan viivakoodin manuaalinen luonti käyttämällä esimerkkinä nimiketunnusta M0001.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568601"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="95be9-103">Viivakoodin luonti tuotteelle</span><span class="sxs-lookup"><span data-stu-id="95be9-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95be9-104">Tässä toimintaohjeessa kuvataan viivakoodin manuaalinen luonti käyttämällä esimerkkinä nimiketunnusta M0001.</span><span class="sxs-lookup"><span data-stu-id="95be9-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="95be9-105">Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.</span><span class="sxs-lookup"><span data-stu-id="95be9-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="95be9-106">Valitse Vapautetun tuotteen ylläpito.</span><span class="sxs-lookup"><span data-stu-id="95be9-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="95be9-107">Valitse Vapautetut tuotteet.</span><span class="sxs-lookup"><span data-stu-id="95be9-107">Click Released products.</span></span>
3. <span data-ttu-id="95be9-108">Etsi haluamasi tietue luettelosta ja valitse se.</span><span class="sxs-lookup"><span data-stu-id="95be9-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="95be9-109">Valitse toimintoruudussa Varastonhallinta.</span><span class="sxs-lookup"><span data-stu-id="95be9-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="95be9-110">Valitse Viivakoodit.</span><span class="sxs-lookup"><span data-stu-id="95be9-110">Click Bar codes.</span></span>
6. <span data-ttu-id="95be9-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="95be9-111">Click New.</span></span>
7. <span data-ttu-id="95be9-112">Merkitse valittu rivi luettelossa.</span><span class="sxs-lookup"><span data-stu-id="95be9-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="95be9-113">Anna tai valitse Viivakoodi-kentässä arvo.</span><span class="sxs-lookup"><span data-stu-id="95be9-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="95be9-114">Syötä tai valitse arvo Viivakoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95be9-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="95be9-115">Kirjoita arvo Viivakoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95be9-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="95be9-116">Paina sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="95be9-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="95be9-117">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="95be9-117">Close the page.</span></span>
12. <span data-ttu-id="95be9-118">Kirjoita numero Määrä-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95be9-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="95be9-119">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="95be9-119">Click Save.</span></span>
    * <span data-ttu-id="95be9-120">Kun valitset Tallenna, viivakoodin tarkistetaan ja tässä tapauksessa se näyttää virheen, että tarkistusluku on 3, vaikka odotettu tarkistusluku pitäisi olla 8.</span><span class="sxs-lookup"><span data-stu-id="95be9-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="95be9-121">Päivitä viivakoodin numero käsin niin, että viimeinen numero on 8.</span><span class="sxs-lookup"><span data-stu-id="95be9-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="95be9-122">Syötä tai valitse arvo Viivakoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95be9-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="95be9-123">Kirjoita arvo Viivakoodi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="95be9-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="95be9-124">Paina sarkainnäppäintä.</span><span class="sxs-lookup"><span data-stu-id="95be9-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="95be9-125">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="95be9-125">Close the page.</span></span>
17. <span data-ttu-id="95be9-126">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="95be9-126">Click Save.</span></span>
18. <span data-ttu-id="95be9-127">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="95be9-127">Close the page.</span></span>

