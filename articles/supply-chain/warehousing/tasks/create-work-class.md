--- 
title: "Työluokan luominen"
description: "Tässä menettelyssä näytetään, miten työluokka määritetään."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 11e506c41eb5e8d5bd28db8e6d5ca51ff9e72a62
ms.contentlocale: fi-fi
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-work-class"></a><span data-ttu-id="357f2-103">Työluokan luominen</span><span class="sxs-lookup"><span data-stu-id="357f2-103">Create a work class</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="357f2-104">Tässä menettelyssä näytetään, miten työluokka määritetään.</span><span class="sxs-lookup"><span data-stu-id="357f2-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="357f2-105">Työluokilla ohjataan ja/tai rajoitetaan työtilausrivityyppejä, joita varastotyötekijä voi käsitellä mobiililaitteessa.</span><span class="sxs-lookup"><span data-stu-id="357f2-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="357f2-106">Työntekijän käsiteltävissä olevat rivit määritetään niistä mobiililaitteen valikkovaihtoehtojen työluokista, joita varastotyöntekijä voi käyttää, ja työriveillä määritetystä työluokasta.</span><span class="sxs-lookup"><span data-stu-id="357f2-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that’s specified on the work lines.</span></span> <span data-ttu-id="357f2-107">Työluokilla voidaan myös tarkistaa työtilausrivin määrityssijainti.</span><span class="sxs-lookup"><span data-stu-id="357f2-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="357f2-108">Voit suorittaa tämän menettelyn esittely-yrityksen USMF kanssa tai käyttää omia tietojasi.</span><span class="sxs-lookup"><span data-stu-id="357f2-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="357f2-109">Tämä menettely on tarkoitettu varastopäällikölle.</span><span class="sxs-lookup"><span data-stu-id="357f2-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="357f2-110">Valitse Varastonhallinta > Asetukset > Työ > Työluokat.</span><span class="sxs-lookup"><span data-stu-id="357f2-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="357f2-111">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="357f2-111">Click New.</span></span>
3. <span data-ttu-id="357f2-112">Kirjoita Työluokan tunnus -kenttään arvo.</span><span class="sxs-lookup"><span data-stu-id="357f2-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="357f2-113">Kirjoita arvo Kuvaus-kenttään.</span><span class="sxs-lookup"><span data-stu-id="357f2-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="357f2-114">Valitse Työtilauksen tyyppi -kentässä vaihtoehto.</span><span class="sxs-lookup"><span data-stu-id="357f2-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="357f2-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="357f2-115">Click New.</span></span>
7. <span data-ttu-id="357f2-116">Kirjoita arvo Sijainnin tyyppi -kenttään.</span><span class="sxs-lookup"><span data-stu-id="357f2-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="357f2-117">Sijaintityypin valitseminen rajoittaa sijainteja, joihin nimikkeet voidaan sijoittaa sen jälkeen, kun ne on kerätty.</span><span class="sxs-lookup"><span data-stu-id="357f2-117">If you select a location type, this sets a restriction on where items can be put after they’ve been picked.</span></span> <span data-ttu-id="357f2-118">Tätä asetusta käytetään, kun sijaintidirektiivi yrittää ratkaista sijainnin tai jos varastotyöntekijä ilmoittaa manuaalisesti sijainnin mobiililaitteen valikkosijainnin valikkovaihtoehdossa.</span><span class="sxs-lookup"><span data-stu-id="357f2-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="357f2-119">Sulje sivu.</span><span class="sxs-lookup"><span data-stu-id="357f2-119">Close the page.</span></span>


