---
title: Luo valikkokohde mobiililaitteelle rekisterikilven konsolidointia varten
description: Tässä menettelyssä kuvataan, miten voit luodaan mobiililaitteen valikkovaihtoehto rekisterikilven konsolidointitöille.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3f5f572461de007f137ffa7ea05c535371f95b7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977235"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="74de8-103">Luo valikkokohde mobiililaitteelle rekisterikilven konsolidointia varten</span><span class="sxs-lookup"><span data-stu-id="74de8-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74de8-104">Tässä menettelyssä kuvataan, miten voit luodaan mobiililaitteen valikkovaihtoehto rekisterikilven konsolidointitöille.</span><span class="sxs-lookup"><span data-stu-id="74de8-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="74de8-105">Näin varastotyöntekijät voivat konsolidoida yhden rekisterikilven nimikkeitä toisen rekisterikilven nimikkeisiin samassa sijainnissa.</span><span class="sxs-lookup"><span data-stu-id="74de8-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="74de8-106">He voivat esimerkiksi käyttää tätä toimintoa, jos seuraavat väliaikaiset vaiheet ovat samat molemmilla työtilauksilla, jotta työn voisi tehdä vain kerran yhdistetyille nimikkeille.</span><span class="sxs-lookup"><span data-stu-id="74de8-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="74de8-107">Voit käyttää tätä menettelyä esittely-yrityksessä USMF.</span><span class="sxs-lookup"><span data-stu-id="74de8-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="74de8-108">Yleensä varastopäällikkö tekee tämän tehtävän.</span><span class="sxs-lookup"><span data-stu-id="74de8-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="74de8-109">Tätä toimintaohje koskee toimintoa, joka lisättiin Dynamics 365 for Operations -ohjelmiston versiossa 1611.</span><span class="sxs-lookup"><span data-stu-id="74de8-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="74de8-110">Valitse Varastonhallinta > Asetukset > Mobiililaite > Mobiililaitteen valikkovaihtoehdot.</span><span class="sxs-lookup"><span data-stu-id="74de8-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="74de8-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="74de8-111">Click New.</span></span>
3. <span data-ttu-id="74de8-112">Kirjoita arvo Valikkovaihtoehdon nimi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="74de8-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="74de8-113">Kirjoita Otsikko-kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="74de8-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="74de8-114">Valitse Tila-kentässä Epäsuora.</span><span class="sxs-lookup"><span data-stu-id="74de8-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="74de8-115">Valitse Toimintokoodi-kentässä "Konsolidoi rekisterikilvet".</span><span class="sxs-lookup"><span data-stu-id="74de8-115">In the Activity code field, select 'Consolidate license plates'.</span></span>

