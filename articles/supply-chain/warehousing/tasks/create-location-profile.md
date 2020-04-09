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
ms.openlocfilehash: 764d1dc1d7fb54e0fa14a681d6d3cdb1d829aa57
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146120"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="0fd5b-103">Luo toimipaikkaprofiili</span><span class="sxs-lookup"><span data-stu-id="0fd5b-103">Create a location profile</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0fd5b-104">Tässä ohjeaiheessa käsitellään sijaintiprofiilin luonti Dynamics 365 Supply Chain Managementissa.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-104">This topic explains how to create a location profile in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="0fd5b-105">Jokaisella varastosijainnilla on oltava liitetty sijaintiprofiili, joka kuvaa sijainnin ominaisuudet, kuten sen, salliiko sijainti yhdistetyt nimikkeet.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-105">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="0fd5b-106">Tässä menettelyssä luodaan profiili sijainnille, jossa ei vaadita rekisterikilpiohjausta.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-106">In this procedure we'll create a profile for a location that doesn't require license plate control.</span></span> <span data-ttu-id="0fd5b-107">Ota käyttöön yhdistetyt nimikkeet ja yhdistetyt varastoinnin tilat, sekä salli inventointi.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-107">We'll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="0fd5b-108">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-108">You can use this procedure in the USMF demo data company.</span></span>


1. <span data-ttu-id="0fd5b-109">Siirry kohtaan **Siirtymisruutu > Moduulit > Varastonhallinta > Asetukset > Varasto > Sijaintiprofiilit**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-109">In the navigation pane, go to **Modules > Warehouse management > Setup > Warehouse > Location profiles**.</span></span>
2. <span data-ttu-id="0fd5b-110">Valitse **Uusi**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-110">Select **New**.</span></span>
3. <span data-ttu-id="0fd5b-111">Kirjoita **Sijainnin profiilitunnus** -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-111">In the **Location profile ID** field, type a value.</span></span>
4. <span data-ttu-id="0fd5b-112">Kirjoita arvo **Nimi**-kenttään.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="0fd5b-113">Syötä tai valitse arvo **Sijainnin muoto** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-113">In the **Location format** field, enter or select a value.</span></span>
6. <span data-ttu-id="0fd5b-114">Anna tai valitse **Sijainnin tyyppi** -kentän arvo.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-114">In the **Location type** field, enter or select a value.</span></span>
7. <span data-ttu-id="0fd5b-115">Syötä tai valitse arvo **Lähetys- ja vastaanottoalueen hallintaprofiilin tunnus** -kenttään.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-115">In the **Dock management profile ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="0fd5b-116">Valitse **Salli yhdistetyt nimikkeet** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-116">Select **Yes** in the **Allow mixed items** field.</span></span>
9. <span data-ttu-id="0fd5b-117">Valitse **Salli yhdistetyt varastotilat** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-117">Select **Yes** in the **Allow mixed inventory statuses** field.</span></span>
10. <span data-ttu-id="0fd5b-118">Valitse **Salli inventointi** -kentässä **Kyllä**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-118">Select **Yes** in the **Allow cycle counting** field.</span></span>
11. <span data-ttu-id="0fd5b-119">Valitse **Tallenna**.</span><span class="sxs-lookup"><span data-stu-id="0fd5b-119">Select **Save**.</span></span>

