--- 
title: Luo toimipaikkaprofiili
description: Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: db3acfbc75829603f7b5f7a03386d019ab66cd3f
ms.contentlocale: fi-fi
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-location-profile"></a><span data-ttu-id="06f6a-103">Luo toimipaikkaprofiili</span><span class="sxs-lookup"><span data-stu-id="06f6a-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06f6a-104">Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="06f6a-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="06f6a-105">Tässä menettelyssä luodaan profiili sijainnille, jossa ei vaadita rekisterikilpiohjausta.</span><span class="sxs-lookup"><span data-stu-id="06f6a-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="06f6a-106">Ota käyttöön yhdistetyt nimikkeet ja yhdistetyt varastoinnin tilat, sekä salli inventointi.</span><span class="sxs-lookup"><span data-stu-id="06f6a-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="06f6a-107">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="06f6a-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="06f6a-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="06f6a-108">Click New.</span></span>
2. <span data-ttu-id="06f6a-109">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="06f6a-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="06f6a-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="06f6a-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="06f6a-111">Syötä tai valitse arvo Sijainnin muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="06f6a-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="06f6a-112">Anna tai valitse Sijainnin tyyppi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="06f6a-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="06f6a-113">Syötä tai valitse arvo Lähetys- ja vastaanottoalueen hallintaprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="06f6a-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="06f6a-114">Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="06f6a-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="06f6a-115">Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="06f6a-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="06f6a-116">Valitse Salli inventointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="06f6a-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="06f6a-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="06f6a-117">Click Save.</span></span>
11. <span data-ttu-id="06f6a-118">Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="06f6a-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>


