---
title: Määritä kuljetuksen maksuväline
description: Tässä menettelyssä näytetään, miten kuljetuksen maksuväline määritetään.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, TMSRouteWorkbench, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 928f445769f89764725adccb0a797fce0c8fdcee
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233532"
---
# <a name="set-up-a-transportation-tender"></a><span data-ttu-id="1d8b9-103">Määritä kuljetuksen maksuväline</span><span class="sxs-lookup"><span data-stu-id="1d8b9-103">Set up a transportation tender</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d8b9-104">Tässä menettelyssä näytetään, miten kuljetuksen maksuväline määritetään.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-104">This procedure shows how to set up a transportation tender.</span></span> <span data-ttu-id="1d8b9-105">Kuljetuskoordinaattori tekee tämän yleensä.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="1d8b9-106">Voit käyttää tätä menettelyä USMF:n esittely-yrityksessä.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-106">You can use this procedure in the USMF demo data company.</span></span>


## <a name="select-a-route"></a><span data-ttu-id="1d8b9-107">Valitse reitti</span><span class="sxs-lookup"><span data-stu-id="1d8b9-107">Select a route</span></span>
1. <span data-ttu-id="1d8b9-108">Valitse Kuljetustenhallinta > Suunnittelu > Kuormasuunnittelun työtila.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-108">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="1d8b9-109">Poista Piilota toimitettu ja vastaanotettu -valintaruudun valinta.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-109">Clear the Hide shipped and received check box.</span></span>
3. <span data-ttu-id="1d8b9-110">Valitse rivi, jolla on kuormatunnus 00006.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-110">Select the line with Load ID 00006.</span></span>
4. <span data-ttu-id="1d8b9-111">Valitse Hinnoittelu ja reititys.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-111">Click Rating and routing.</span></span>
5. <span data-ttu-id="1d8b9-112">Valitse Reitit.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-112">Click Routes.</span></span>

## <a name="create-the-transportation-tender"></a><span data-ttu-id="1d8b9-113">Luo kuljetuksen maksuväline</span><span class="sxs-lookup"><span data-stu-id="1d8b9-113">Create the transportation tender</span></span>
1. <span data-ttu-id="1d8b9-114">Valitse Kuljetuksen maksuvälineet.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-114">Click Transportation tenders.</span></span>
2. <span data-ttu-id="1d8b9-115">Valitse Uusi.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-115">Click New.</span></span>
3. <span data-ttu-id="1d8b9-116">Laajenna Yleiset-osa.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-116">Expand the General section.</span></span>
4. <span data-ttu-id="1d8b9-117">Kirjoita numero Pyydetyt hinnat -kenttään.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-117">In the Requested rates field, enter a number.</span></span>
5. <span data-ttu-id="1d8b9-118">Valitse Tallenna.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-118">Click Save.</span></span>
6. <span data-ttu-id="1d8b9-119">Valitse Päivitä tila.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-119">Click Update status.</span></span>
7. <span data-ttu-id="1d8b9-120">Valitse Lähetä.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-120">Click Submit.</span></span>
8. <span data-ttu-id="1d8b9-121">Valitse reitti.</span><span class="sxs-lookup"><span data-stu-id="1d8b9-121">Select a route.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]