---
title: Luo toimipaikkaprofiili
description: Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8bc7705b7db46af8fbe8bf9e78a878a53249b452
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560900"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="9f8c2-103">Luo toimipaikkaprofiili</span><span class="sxs-lookup"><span data-stu-id="9f8c2-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f8c2-104">Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="9f8c2-105">Tässä menettelyssä luodaan profiili sijainnille, jossa ei vaadita rekisterikilpiohjausta.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="9f8c2-106">Ota käyttöön yhdistetyt nimikkeet ja yhdistetyt varastoinnin tilat, sekä salli inventointi.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="9f8c2-107">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="9f8c2-108">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-108">Click New.</span></span>
2. <span data-ttu-id="9f8c2-109">Kirjoita Sijainnin profiilitunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="9f8c2-110">Kirjoita arvo Nimi-kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9f8c2-111">Syötä tai valitse arvo Sijainnin muoto -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="9f8c2-112">Anna tai valitse Sijainnin tyyppi -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="9f8c2-113">Syötä tai valitse arvo Lähetys- ja vastaanottoalueen hallintaprofiilin tunnus -kenttään.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="9f8c2-114">Valitse Salli yhdistetyt nimikkeet -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="9f8c2-115">Valitse Salli yhdistetyt varastotilat -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="9f8c2-116">Valitse Salli inventointi -kentässä Kyllä.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="9f8c2-117">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-117">Click Save.</span></span>
11. <span data-ttu-id="9f8c2-118">Valitse Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit.</span><span class="sxs-lookup"><span data-stu-id="9f8c2-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>

