--- 
title: Luo valikkokohde mobiililaitteelle rekisterikilven konsolidointia varten
description: "Tässä menettelyssä kuvataan, miten voit luodaan mobiililaitteen valikkovaihtoehto rekisterikilven konsolidointitöille."
author: YuyuScheller
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7b8d20561ff092bd64c17c5d9335e9f54a1d191b
ms.contentlocale: fi-fi
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="2f3fe-103">Luo valikkokohde mobiililaitteelle rekisterikilven konsolidointia varten</span><span class="sxs-lookup"><span data-stu-id="2f3fe-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f3fe-104">Tässä menettelyssä kuvataan, miten voit luodaan mobiililaitteen valikkovaihtoehto rekisterikilven konsolidointitöille.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="2f3fe-105">Näin varastotyöntekijät voivat konsolidoida yhden rekisterikilven nimikkeitä toisen rekisterikilven nimikkeisiin samassa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="2f3fe-106">He voivat esimerkiksi käyttää tätä toimintoa, jos seuraavat väliaikaiset vaiheet ovat samat molemmilla työtilauksilla, jotta työn voisi tehdä vain kerran yhdistetyille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="2f3fe-107">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="2f3fe-108">Yleensä varastopäällikkö tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="2f3fe-109">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="2f3fe-110">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="2f3fe-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-111">Click New.</span></span>
3. <span data-ttu-id="2f3fe-112">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="2f3fe-113">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="2f3fe-114">Valitse Tila-kentässä Epäsuora.</span><span class="sxs-lookup"><span data-stu-id="2f3fe-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="2f3fe-115">Valitse Toimintokoodi-kentässä "Konsolidoi rekisterikilvet".</span><span class="sxs-lookup"><span data-stu-id="2f3fe-115">In the Activity code field, select 'Consolidate license plates'.</span></span>


