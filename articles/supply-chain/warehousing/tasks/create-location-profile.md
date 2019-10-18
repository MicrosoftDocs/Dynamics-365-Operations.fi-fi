---
title: Luo toimipaikkaprofiili
description: Tässä ohjeaiheessa käsitellään sijaintiprofiilin luonti Dynamics 365 Supply Chain Managementissa.
author: ShylaThompson
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36bad7424ac247b8fd9a819928837de619e9e258
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026782"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="34cab-103">Luo toimipaikkaprofiili</span><span class="sxs-lookup"><span data-stu-id="34cab-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34cab-104">Tässä ohjeaiheessa käsitellään sijaintiprofiilin luonti Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="34cab-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="34cab-105">Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="34cab-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="34cab-106">Tässä menettelyssä luodaan profiili sijainnille, jossa ei vaadita rekisterikilpiohjausta.</span><span class="sxs-lookup"><span data-stu-id="34cab-106">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="34cab-107">Ota käyttöön yhdistetyt nimikkeet ja yhdistetyt varastoinnin tilat, sekä salli inventointi.</span><span class="sxs-lookup"><span data-stu-id="34cab-107">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="34cab-108">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="34cab-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="34cab-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="34cab-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="34cab-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="34cab-110">Select **New**.</span></span>
3. <span data-ttu-id="34cab-111">Kirjoita **Sijainnin profiilitunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="34cab-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="34cab-112">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="34cab-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="34cab-113">Syötä tai valitse arvo **Sijainnin muoto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="34cab-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="34cab-114">Anna tai valitse **Sijainnin tyyppi** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="34cab-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="34cab-115">Syötä tai valitse arvo **Lähetys- ja vastaanottoalueen hallintaprofiilin tunnus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="34cab-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="34cab-116">Valitse **Salli yhdistetyt nimikkeet** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="34cab-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="34cab-117">Valitse **Salli yhdistetyt varastotilat** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="34cab-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="34cab-118">Valitse **Salli inventointi** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="34cab-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="34cab-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="34cab-119">Select **Save**.</span></span>

